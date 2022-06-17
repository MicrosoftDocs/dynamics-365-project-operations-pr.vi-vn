---
title: Có gì mới tháng 2 năm 2021 – Project Operations bản triển khai giản đơn
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản triển khai Project Operations lite vào tháng 2 năm 2021.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 329bc31ad4c0958fe60e73b257e6b4c262bb60f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914060"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Có gì mới tháng 2 năm 2021 – Project Operations bản triển khai giản đơn

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

  - Project Operations trên môi trường Dataverse phiên bản 4.7.0.95

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| **Định giá và thanh toán** | 2053736 | Giờ đây, bạn có thể truy cập vào phần chi tiết dòng hóa đơn bằng cách đi đến **Hóa đơn** > **Thông tin liên quan**. |
| **Định giá và thanh toán** | 2122613 | Hành đồng **Kích hoạt** và **Hủy kích hoạt** đã bị loại bỏ khỏi các thực thể liên kết **Bảng giá**. |
| **Định giá và thanh toán** | 2128606 | Đã khắc phục sự cố đối với **ullReferenceException** trong phần bổ trợ **GetEstimatesForProject**. |
| **Đợt triển khai và Cấu hình** | 2140569 | Không được cài đặt giải pháp dự án trong môi trường Dataverse Teams. |
| **Đợt triển khai và Cấu hình** | 2086991 | Đã hạn chế việc tùy chỉnh cách bản địa hóa nguồn lực web. |
| **Quản lý cơ hội** | 2136794 | Hiển thị chính xác thông báo lỗi khi quá trình xử lý **Xác nhận hóa đơn** hoặc **Đánh dấu hóa đơn là đã thanh toán** thất bại, |
| **Quản lý cơ hội** | 2146376 | Mức thuế chính xác trong một giá trị thực tế không tính phí sẽ được tạo từ bản xác nhận hóa đơn. |
| **Hoạch định và theo dõi dự án** | 2099879 | Việc triển khai môi trường Dataverse sẽ tạo một danh mục giao dịch mặc định với ID tĩnh và sẽ không tạo ID ngẫu nhiên cho mỗi môi trường. |
| **Hoạch định và theo dõi dự án** | 2128577 | Đã sửa lỗi quyền người dùng Project Service cập nhật danh mục giao dịch trên một lượt chỉ định nguồn lực. |
| **Hoạch định và theo dõi dự án** | 2164035 | Đã khắc phục sự cố đối với chức năng **Sao chép dự án**. |
| **Mục nhập thời gian** | 2129161 | Đã áp dụng các giới hạn chặt chẽ hơn để đảm bảo rằng người dùng không thể thay đổi hoặc cập nhật mục nhập thời gian đã phê duyệt hoặc gửi. |
| **Mục nhập thời gian** | 2103572 | Việc phê duyệt thời gian đối với các mục nhập thời gian không thuộc dự án sẽ không tìm đến vai trò người phê duyệt dự án. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]