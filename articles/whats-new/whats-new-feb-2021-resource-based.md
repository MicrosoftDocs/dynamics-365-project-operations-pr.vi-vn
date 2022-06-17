---
title: Có gì mới tháng 2 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 2 năm 2021 của Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 38fede1746bcb09700c9c9c5e20653e0c39fea2a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910670"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 2 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

- Project Operations trên môi trường Dataverse 4.7.0.95
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.16 

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| **Định giá và thanh toán** | 2053736 | Giờ đây, bạn có thể truy cập vào phần chi tiết dòng hóa đơn bằng cách đi đến **Hóa đơn** > **Thông tin liên quan**. |
| **Định giá và thanh toán** | 2122613 | Hành đồng **Kích hoạt** và **Hủy kích hoạt** đã bị loại bỏ khỏi các thực thể liên kết **Bảng giá**. |
| **Định giá và thanh toán** | 2128606 | Đã khắc phục sự cố đối với **ullReferenceException** trong phần bổ trợ **GetEstimatesForProject**. |
| **Đợt triển khai và Cấu hình** | 2139346 | Đã giải quyết sự cố đối với việc nhập giải pháp **Dynamics365ProjectOperationsDualWrite** không quản lý. |
| **Đợt triển khai và Cấu hình** | 2140569 | Không được cài đặt giải pháp dự án trong môi trường Dataverse Teams. |
| **Đợt triển khai và Cấu hình** | 2086991 | Đã hạn chế việc tùy chỉnh cách bản địa hóa nguồn lực web. |
| **Quản lý cơ hội** | 2136794 | Hiển thị chính xác thông báo lỗi khi quá trình xử lý **Xác nhận hóa đơn** hoặc **Đánh dấu hóa đơn là đã thanh toán** thất bại. |
| **Quản lý cơ hội** | 2139330 | Việc thay đổi người quản lý dự án sẽ không đặt lại công ty chủ quản về giá trị mặc định. |
| **Quản lý cơ hội** | 2146376 | Mức thuế chính xác trong một giá trị thực tế không tính phí sẽ được tạo từ bản xác nhận hóa đơn. |
| **Hoạch định và theo dõi dự án** | 2099879 | Việc triển khai môi trường Dataverse sẽ tạo một danh mục giao dịch mặc định với ID tĩnh và sẽ không tạo ID ngẫu nhiên cho mỗi môi trường. |
| **Hoạch định và theo dõi dự án** | 2128577 | Đã sửa lỗi quyền người dùng Project Service cập nhật danh mục giao dịch trên một lượt chỉ định nguồn lực. |
| **Hoạch định và theo dõi dự án** | 2164035 | Đã khắc phục sự cố đối với chức năng **Sao chép dự án**. |
| **Mục nhập thời gian** | 2129161 | Đã áp dụng các giới hạn chặt chẽ hơn để đảm bảo rằng người dùng không thể thay đổi hoặc cập nhật mục nhập thời gian đã phê duyệt hoặc gửi. |
| **Mục nhập thời gian** | 2103572 | Việc phê duyệt thời gian đối với các mục nhập thời gian không thuộc dự án sẽ không tìm đến vai trò người phê duyệt dự án. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance 

Để biết thêm thông tin về quản lý dự án và kế toán trong Dynamics 365 Finance, hãy xem [Có gì mới Tháng 1 năm 2021 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các cập nhật quy định cho các ứng dụng Tài chính và Hoạt động, hãy xem [Cập nhật quy định](/dynamics365/finance/localizations/regulatory-updates). Một cách khác để tìm hiểu về các chi tiết cập nhật quy định là đăng nhập vào Lifecycle Services (LCS) và dùng công cụ tìm kiếm sự cố để xem các chi tiết cập nhật quy định đã lên kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]