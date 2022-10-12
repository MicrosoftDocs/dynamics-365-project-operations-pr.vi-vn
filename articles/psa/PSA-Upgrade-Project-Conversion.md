---
title: Các thay đổi về tính năng của Tự động hóa dịch vụ dự án sang Hoạt động dự án
description: Bài viết này cung cấp tổng quan về các thay đổi tính năng đối với Microsoft Dynamics 365 Project Service Automation đến Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621364"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Các thay đổi về tính năng của Tự động hóa dịch vụ dự án sang Hoạt động dự án

Sau khi một dự án đã được nâng cấp thành công từ Microsoft Dynamics 365 Project Service Automation 3.X đến Dynamics 365 Project Operations Lite, không thể chỉnh sửa các tác vụ dự án trong cấu trúc phân tích công việc của lưới tác vụ (WBS). Khách hàng sẽ có thể xem lại các WBS trong lưới theo dõi nơi các trường mới đã được thêm vào để cung cấp tất cả các chi tiết liên quan đến nhiệm vụ. Đối với các dự án yêu cầu chỉnh sửa WBS, bạn có thể chuyển đổi một cách chọn lọc các dự án đủ điều kiện sang Dự án mới để có trải nghiệm lập lịch trình web.

## <a name="project-conversion-process"></a>Quy trình chuyển đổi dự án

Để chuyển đổi một dự án, hãy làm theo các bước sau.

1. Mở trang chính của dự án và chọn **Chuyển thành** trên Ngăn hành động.
1. Trong hộp thông báo xác nhận, hãy chọn **ĐƯỢC RỒI** để bắt đầu chuyển đổi dự án. Các hành động sau xảy ra:

    1. Một thanh thông báo xuất hiện trên trang chính của dự án cho biết, "Lịch trình dự án đang được chuyển đổi. Bạn không thể thực hiện các thay đổi đối với dự án cho đến khi quá trình chuyển đổi hoàn tất. "
    1. Bạn được chuyển hướng đến danh sách dự án.

    Sau khi hoàn thành chuyển đổi dự án, các hành động sau sẽ xảy ra:

    1. Người quản lý dự án được giao sẽ nhận được thông báo ở phía bên phải của ứng dụng.
    1. Thanh thông báo cho biết rằng quá trình chuyển đổi đang diễn ra sẽ bị xóa.
    1. Các **Lịch trình** tab hiển thị trải nghiệm lập lịch mới với Project cho web. Bất kỳ người dùng nào có giấy phép và vai trò bảo mật thích hợp đều có thể chỉnh sửa WBS.
    1. Các **Công cụ lập lịch trình** trường được cập nhật thành **Dự án cho web**.
    1. Các **Chuyển thành** bị xóa khỏi Ngăn hành động.

> [!IMPORTANT]
> Không cho phép chuyển đổi hàng loạt dự án. Mọi nỗ lực cập nhật một lượng lớn các dự án cùng một lúc sẽ bị hạn chế. Hạn chế này giúp đảm bảo hiệu suất cao cho mọi khách hàng.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tác vụ thủ công và tác vụ tự động

Khi một môi trường được nâng cấp từ Tự động hóa dịch vụ dự án lên Hoạt động dự án, tất cả các nhiệm vụ trong WBS được coi là tự động được lên lịch. Khái niệm về các tác vụ được lên lịch theo cách thủ công không có sẵn trong Project cho web. Tuy nhiên, bạn có thể xác định hành vi lập lịch ưa thích cho các dự án của mình bằng cách sử dụng [chế độ lập lịch trình](/project-management/scheduling-modes.md) thiết lập khi bạn tạo các dự án mới.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Các hoạt động bị hạn chế đối với các dự án chuyển đổi trước

Phần này phác thảo những khác biệt về chức năng mà bạn có thể mong đợi khi các dự án chưa được chuyển đổi.

### <a name="copy-project"></a>Sao chép dự án

Các **Sao chép** hoạt động chỉ được hỗ trợ trên các dự án đã chuyển đổi. Không thể sao chép các dự án đã nâng cấp trước khi chuyển đổi.

### <a name="move-project"></a>Di chuyển dự án

Một sự thay đổi đối với ngày bắt đầu của một dự án sẽ không thay đổi một cách tương ứng thời gian bắt đầu các nhiệm vụ trừ khi dự án đã được chuyển đổi.

## <a name="frequently-asked-questions"></a>Các câu hỏi thường gặp

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Sự khác biệt giữa các dự án được chuyển đổi và các dự án mới được tạo sau khi hoàn thành nâng cấp là gì?

Đối với các dự án được chuyển đổi sau khi môi trường đã được nâng cấp, một cờ sẽ được đặt để hướng dẫn lịch trình chỉ tôn trọng lịch dự án. Hành vi này khớp với hành vi trong Tự động hóa dịch vụ dự án. Tuy nhiên, cờ sẽ không được đặt cho các dự án mới được tạo sau khi nâng cấp. Do đó, lịch trình sẽ tôn trọng thời gian làm việc của các nguồn lực khi họ được giao cho một nhiệm vụ.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Tôi nên làm gì nếu dự án của tôi không được chuyển đổi?

Nếu dự án của bạn không được chuyển đổi, bước đầu tiên là xem lại nhật ký lỗi để xác định bất kỳ vấn đề phổ biến nào liên quan đến WBS của bạn. Nếu nhật ký không chỉ ra lỗi cụ thể mà bạn có thể thực hiện, hãy liên hệ với bộ phận Hỗ trợ khách hàng để chúng tôi có thể xem xét thêm trường hợp của bạn.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Việc đóng cửa doanh nghiệp được xử lý như thế nào trong Dự án cho web?

Dự án cho web không tôn trọng việc đóng cửa doanh nghiệp mà doanh nghiệp xác định ở cấp tổ chức. Tuy nhiên, nó sẽ tôn trọng các loại ngày nghỉ khác được xác định trong một mẫu giờ làm việc nhất định.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Những hạn chế của Project cho web là gì?

Nhìn thấy [Tạo cấu trúc phân tích công việc: Hạn chế của dự án](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Tôi có thể mong đợi những thay đổi đối với ước tính chi phí và doanh số bán hàng của mình không?

Trong một số trường hợp hiếm hoi, các đường bao phân bổ tài nguyên được tính toán lại hoặc khi chúng nằm trong ranh giới ngày khác với dự án nguồn, bạn có thể thấy sự khác biệt về doanh số và ước tính chi phí. Là một phần của quá trình nâng cấp, khách hàng phải kiểm tra một bộ dự án mẫu đại diện để họ có thể hiểu được bất kỳ sự thay đổi lịch trình tiềm năng nào.
