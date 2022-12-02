---
title: Quy trình chuyển đổi lên lịch dự án từ Project Service Automation sang Project Operations
description: Bài viết này cung cấp thông tin tổng quan về các thay đổi tính cho Microsoft Dynamics 365 Project Service Automation thành Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642595"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Quy trình chuyển đổi lên lịch dự án từ Project Service Automation sang Project Operations

Sau khi một dự án đã được nâng cấp thành công từ Microsoft Dynamics 365 Project Service Automation 3.X lên Dynamics 365 Project Operations Lite, không thể chỉnh sửa các nhiệm vụ dự án trong cấu trúc phân tích công việc (WBS) của lưới tác vụ. Khách hàng sẽ có thể xem lại các WBS trong lưới theo dõi nơi các trường mới đã được thêm vào để cung cấp tất cả các chi tiết liên quan đến nhiệm vụ. Đối với các dự án yêu cầu chỉnh sửa WBS, bạn có thể chuyển đổi một cách chọn lọc các dự án đủ điều kiện sang trải nghiệm lập lịch Project for the Web mới.

## <a name="project-conversion-process"></a>Quy trình chuyển đổi dự án

Để chuyển đổi một dự án, hãy làm theo các bước này.

1. Mở trang chính của dự án và chọn **Chuyển đổi** trên Ngăn hành động.
1. Trong hộp thông báo xác nhận, hãy chọn **OK** để bắt đầu chuyển đổi dự án. Các hành động sau xảy ra:

    1. Một thanh thông báo xuất hiện trên trạng thái trang chính của dự án, "Lịch dự án đang được chuyển đổi. Bạn không thể thực hiện các thay đổi với dự án cho đến khi chuyển đổi xong."
    1. Bạn được chuyển hướng đến danh sách dự án.

    Sau khi hoàn thành chuyển đổi dự án, các hành động sau sẽ xảy ra:

    1. Người quản lý dự án được phân công sẽ nhận được thông báo ở phía bên phải của ứng dụng.
    1. Thanh thông báo cho biết rằng quá trình chuyển đổi đang diễn ra sẽ bị xóa.
    1. Tab **Lịch trình** hiển thị trải nghiệm lập lịch mới với Project for the web. Bất kỳ người dùng nào có giấy phép và vai trò bảo mật thích hợp đều có thể chỉnh sửa WBS.
    1. Trường **Công cụ lập lịch** được cập nhật thành **Project for the web**.
    1. Nút **Chuyển đổi** bị xóa khỏi Ngăn hành động.

> [!IMPORTANT]
> Không cho phép chuyển đổi hàng loạt dự án. Mọi hoạt động cập nhật một lượng lớn các dự án cùng một lúc sẽ bị hạn chế. Hạn chế này giúp đảm bảo hiệu suất cao cho mọi khách hàng.

## <a name="manual-tasks-vs-automatic-tasks"></a>Nhiệm vụ thủ công và nhiệm vụ tự động

Khi một môi trường được nâng cấp từ Project Service Automation lên Project Operations, tất cả các nhiệm vụ trong WBS được coi là tự động được lên lịch. Khái niệm về các nhiệm vụ được lập lịch theo cách thủ công không có sẵn trong Project for the web. Tuy nhiên, bạn có thể xác định hành vi lập lịch ưa thích cho các dự án của mình bằng cách sử dụng cài đặt [chế độ lập lịch](/project-management/scheduling-modes.md) khi bạn tạo các dự án mới.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Các hoạt động bị hạn chế đối với các dự án chuyển đổi trước

Phần này phác thảo những khác biệt về chức năng mà bạn có thể mong đợi khi các dự án chưa được chuyển đổi.

### <a name="copy-project"></a>Sao chép dự án

Thao tác **Sao chép** chỉ được hỗ trợ trên các dự án đã chuyển đổi. Không thể sao chép các dự án đã nâng cấp trước khi chuyển đổi.

### <a name="move-project"></a>Di chuyển dự án

Một sự thay đổi đối với ngày bắt đầu dự án sẽ không thay đổi một cách tương ứng thời gian bắt đầu các nhiệm vụ trừ khi dự án đã được chuyển đổi.

## <a name="frequently-asked-questions"></a>Các câu hỏi thường gặp

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Sự khác biệt giữa các dự án được chuyển đổi và các dự án mới được tạo sau khi hoàn thành nâng cấp là gì?

Đối với các dự án được chuyển đổi sau khi môi trường đã được nâng cấp, một cờ sẽ được đặt để hướng dẫn lịch trình theo lịch dự án. Hành vi này khớp với hành vi trong Project Service Automation. Tuy nhiên, cờ sẽ không được đặt cho các dự án mới được tạo sau khi nâng cấp. Do đó, lịch trình sẽ tôn trọng giờ làm việc của các nguồn lực khi họ được giao một nhiệm vụ.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Tôi nên làm gì nếu dự án của tôi không được chuyển đổi?

Nếu dự án của bạn không được chuyển đổi, bước đầu tiên là xem lại nhật ký lỗi để xác định bất kỳ vấn đề phổ biến nào liên quan đến WBS của bạn. Nếu nhật ký không chỉ ra lỗi cụ thể mà bạn có thể thực hiện, hãy liên hệ với bộ phận Hỗ trợ khách hàng để chúng tôi có thể xem xét thêm trường hợp của bạn.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Thời gian đóng cửa được xử lý như thế nào trong Project for the web?

Project for the web không tuân theo thời gian đóng cửa mà doanh nghiệp xác định ở cấp độ tổ chức. Tuy nhiên, nó sẽ tuân theo những loại ngày nghỉ khác được xác định trong một mẫu giờ làm việc nhất định.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the web có những hạn chế gì?

Xem [Tạo cấu trúc phân tích công việc: Giới hạn dự án](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Tôi có thể mong đợi những thay đổi đối với ước tính chi phí và doanh số không?

Trong những trường hợp hiếm, khi đường bao phân bổ nguồn lực được tính toán lại hoặc khi chúng nằm trong ranh giới ngày khác với dự án nguồn, bạn có thể thấy sự khác biệt giữa doanh số và ước tính chi phí. Là một phần của quá trình nâng cấp, khách hàng phải kiểm tra một tập hợp dự án mẫu đại diện để có thể hiểu được bất kỳ thay đổi lịch trình tiềm năng nào.
