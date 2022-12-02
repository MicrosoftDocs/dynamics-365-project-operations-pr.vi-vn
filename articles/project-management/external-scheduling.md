---
title: Lập lịch trình bên ngoài
description: Bài viết này cung cấp thông tin về lập lịch trình bên ngoài.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736998"
---
# <a name="external-scheduling"></a>Lập lịch trình bên ngoài

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chế độ lập lịch trình bên ngoài cho phép bạn tạo, cập nhật và xóa nguyên bản các thực thể có liên quan đến cấu trúc phân tích công việc (WBS), nhưng không có giới hạn hiện tại được thực thi bởi Microsoft Project for the Web. Nó cũng cung cấp xác thực giới hạn. Chế độ này chỉ nên được sử dụng bởi những khách hàng sau:

- Khách hàng có các công cụ được yêu cầu để xác định một WBS bên ngoài logic lập lịch trình được cung cấp bởi Project Operations
- Những khách hàng phải quản lý hệ thống cấp bậc lịch trình, yếu tố phụ thuộc hoặc thời lượng nhiệm vụ

> [!IMPORTANT]
> Dữ liệu không được nhập chính xác vào các thực thể liên quan đến WBS có thể không được hiển thị trong lưới điều hòa nguồn lực, lưới ước tính, lưới theo dõi hoặc lưới phân bổ nguồn lực.

## <a name="configuration"></a>Cấu hình

Tính năng này được bật theo mặc định. Tuy nhiên, trên trang chính sẵn có cho các dự án, trường liên quan không hiển thị theo mặc định. Để kích hoạt trường, trong Maker portal, hãy mở trang chính cho thực thể dự án, chọn trường **Công cụ lên lịch**, và sau đó thay đổi trường thành **Hiển thị theo mặc định**. Nếu bạn không sử dụng trang chính của dự án sẵn có, hãy chỉnh sửa trang hiện có của bạn và thêm trường **Công cụ lập lịch** vào đó.

## <a name="settings"></a>Cài đặt

Để sử dụng chế độ lập lịch bên ngoài, trước tiên bạn phải tạo một dự án mới và chọn công cụ lập lịch **Được lập lịch bên ngoài** trong danh sách thả xuống trên trang chính của dự án. Sau khi chế độ này đã được thiết lập cho một dự án, bạn không thể thay đổi chế độ này.

## <a name="viewing-the-wbs"></a>Xem WBS

Nếu một dự án được lên lịch bên ngoài, quyền truy cập vào Project for the Web sẽ bị hạn chế đối với dự án đó. Để xem WBS, bạn phải chuyển đến lưới theo dõi, nơi WBS đầy đủ được hiển thị.

## <a name="creating-and-editing-the-wbs"></a>Tạo và chỉnh sửa WBS

Nếu lập lịch bên ngoài được bật cho một dự án, bạn phải xác định dữ liệu cho tất cả các thực thể liên quan đến WBS, bao gồm nhiệm vụ, thành viên nhóm, phân công nguồn lực và yếu tố phụ thuộc.

Hình minh họa sau đây cho thấy mô hình dữ liệu cho lập kế hoạch dự án.

![Mô hình dữ liệu lập kế hoạch dự án.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Các giới hạn chức năng

Các hoạt động sau đây không được cho phép trên các dự án được lên lịch bên ngoài.

### <a name="project-planning"></a>Lập kế hoạch dự án

- **Sao chép dự án** – Thao tác này không được hỗ trợ trên các dự án được lên lịch bên ngoài.
- **Di chuyển dự án** – Những thay đổi đối với ngày bắt đầu của một dự án sẽ không thay đổi thời điểm bắt đầu các nhiệm vụ hoặc phân công nguồn lực trong WBS.
- **Cập nhật Người quản lý dự án** – Các thay đổi đối với người quản lý dự án trên trang chính của dự án sẽ không tự động tạo thành viên nhóm dự án mới cho đến khi dự án đã được chuyển đổi.
- **Cập nhật mẫu giờ làm việc của dự án** – Các thay đổi đối với mẫu giờ làm việc của dự án sẽ không tính lại lịch trình của dự án.
- **Đường viên phân công nguồn lực** – Việc tạo các nhiệm vụ nguồn lực sẽ không tự động cập nhật trường **mdyn\_PlannedWork**. Trường này được sử dụng để lưu trữ các đường viền cho nỗ lực phân công nguồn lực. Nếu bạn hiển thị theo giai đoạn trong lưới phân công nguồn lực hoặc lưới điều hòa nguồn lực, bạn phải xác định các đường viền phân công nguồn lực hợp lệ. Các đường viền này phải được định dạng chính xác để chúng có thể kích hoạt việc tính toán cả đường viền chi phí và đường viền giá bán. Chúng tôi khuyên bạn nên tạo một dự án thử nghiệm được lên lịch bởi Project for the Web, sau đó xem lại dữ liệu liên quan để xác nhận các yêu cầu và định dạng.

### <a name="resource-management"></a>Quản lý nguồn lực

- **Thực hiện nguồn lực chung** – Thực hiện nguồn lực chung không được hỗ trợ cho các dự án được lên lịch bên ngoài. Nỗ lực thực hiện các yêu cầu mở đang hoạt động sẽ tạo thành viên nhóm dự án mới, nhưng nó sẽ không xóa thành viên nhóm chung hoặc thay thế thành viên nhóm chung trên bất kỳ phân công nguồn lực hiện có nào.
- **Xóa thành viên nhóm** – Việc xóa một thành viên nhóm sẽ không tự động xóa các phân công nguồn lực.

### <a name="quoting-and-contracting"></a>Báo giá và ký hợp đồng

- **Nhập chi tiết Mô tả báo giá và Mô tả hợp đồng** – Khi chi tiết mô tả hợp đồng hoặc báo giá được nhập từ một dự án, ứng dụng đã được thử nghiệm để hỗ trợ tối đa chỉ 500 nhiệm vụ trong WBA, dựa trên giới hạn 20 phân công cho mỗi nhiệm vụ.

### <a name="actuals-and-invoicing"></a>Số liệu thực tế và lập hóa đơn

- Mặc dù không có thay đổi nào đối với những xác thực hiện có giữa WBS và các giao dịch tài chính, nhưng điều quan trọng là bạn phải tuân thủ mô hình dữ liệu sẵn có, để đảm bảo rằng tất cả các giao dịch xuôi tuyến chạy như mong đợi.
