---
title: Tính năng mới trong phần triển khai Project Operations lite – tháng 5 năm 2021
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản triển khai Project Operations lite vào tháng 5 năm 2021.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934208"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Tính năng mới trong phần triển khai Project Operations lite – tháng 5 năm 2021

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

   - Project Operations trên môi trường Dataverse phiên bản 4.10.0.186.

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- [Chế độ lập lịch trình](../../project-management/scheduling-modes.md): Người quản lý dự án giờ có thể xác định xem dự án nên được quản lý bằng chế độ lập lịch theo đơn vị cố định, công việc cố định hay thời gian cố định.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2224568 | Đã thêm logic để bật các chế độ tùy chỉnh liên quan đến việc gọi ra phần bổ trợ xác nhận hóa đơn. |
| Định giá và thanh toán | 2101098 | Cải thiện lô-gic của các trường mặc định cho hóa đơn ước giá. Các trường này bao gồm: **Địa chỉ nhận hóa đơn**, **Tên người nhận hóa đơn** và **Điều khoản thanh toán**. Các trường này giờ lấy mặc định từ bản ghi khách hàng của hợp đồng dự án tương ứng. |
| Định giá và thanh toán | 2021413 | Đã cập nhật các trường **Chi phí thực tế** và **Bán hàng** trên thực thể **Nhiệm vụ** để đưa vào các giá trị doanh số từ chi phí chưa lập hóa đơn và đã lập hóa đơn cho các nhiệm vụ. |
| Định giá và thanh toán | 2182110 | Khi sao chép hợp đồng dự án, ID mô tả hợp đồng sẽ được tái tạo trong hợp đồng dự án đích để đảm bảo ID này là duy nhất. |
| Quản lý cơ hội | 2186741 | Đã thêm các bước xác thực để bảo đảm không thể cập nhật trường **Gốc** và Loại giao dịch trên phần chi tiết mô tả báo giá hiện có. |
| Quản lý cơ hội | 2191353 | Không được phép tạo mốc trên một mục mô tả hợp đồng thời gian và vật tư. |
| Quản lý cơ hội | 2216956 | Đã khắc phục sự cố **Cập nhật giá**. |
| Hoạch định và theo dõi dự án | 2182979 | Đã cải thiện chức năng sao chép dự án để bảo đảm các dòng ước tính chi phí được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184144 | Đã cải tiến chức năng sao chép dự án để đảm bảo tên vị trí nguồn lực được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184799 | Đã cải thiện chức năng kiểm soát đối với hoạt động sao chép dự án để bảo đảm không thể thay đổi ngày bắt đầu ước tính trong quá trình sao chép. |
| Hoạch định và theo dõi dự án | 2185134 | Trong hoạt động sao chép dự án, ngày bắt đầu dự kiến của dự án đích được thiết lập thành ngày hôm nay. |
| Hoạch định và theo dõi dự án | 2196373 | Bảo đảm rằng các bản ghi của người quản lý dự án và thành viên trong nhóm không bị trùng lặp trong khi sao chép dự án. |
| Hoạch định và theo dõi dự án | 2211833 | Các mục chỉ định nguồn lực được sao chép từ nhiệm vụ của dự án nguồn sang dự án đích. |
| Hoạch định và theo dõi dự án | 2186541 | Đã khắc phục sự cố ở lưới **Ước tính** khi nhóm theo **Nguồn lực**. |
| Hoạch định và theo dõi dự án | 2166906 | Danh mục giao dịch từ một nhiệm vụ phải được sao chép sang thực thể **Công việc giao cho nguồn lực**. |
| Quản lý nguồn lực | 2125362 | Đã khắc phục sự cố khi tạo một thành viên trong nhóm chung qua phương thức phân bổ theo giờ. |
| Thời gian và Chi phí | 2113603 | Đã khắc phục sự cố liên quan đến tùy chỉnh bằng cách loại bỏ các thuộc tính khỏi trang **Mục nhập thời gian**. Hệ thống kiểm tra xem thuộc tính có tồn tại trên trang hay không trước khi truy nhập thuộc tính bằng tập lệnh. |
| Thời gian và Chi phí | 2204377 | Bảng chấm công đã sao chép phải tự động hiển thị khi bạn chọn **Sao chép tuần**. |
| Thời gian và Chi phí | 2209059 | Bạn có thể chỉnh sửa trường **Trạng thái** cho mục nhập thời gian trên Dynamics 365 Field Service. |
