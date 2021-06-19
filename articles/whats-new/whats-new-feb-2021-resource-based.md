---
title: Có gì mới tháng 2 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 2 năm 2021 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 73be15d4d58531e6e181df92eaee2b4d7b924382
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012657"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 2 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường Dataverse 4.7.0.95
- Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.16 

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

Để biết thêm thông tin về hoạt động quản lý và kế toán dự án trong Dynamics 365 Finance, hãy xem [Có gì mới tháng 1 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng Finance and Operations, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Một cách khác để tìm hiểu về các chi tiết cập nhật quy định là đăng nhập vào Lifecycle Services (LCS) và dùng công cụ tìm kiếm sự cố để xem các chi tiết cập nhật quy định đã lên kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]