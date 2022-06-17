---
title: Tính năng mới tháng 3 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 3 năm 2021 của Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có sẵn.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932966"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới tháng 3 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

- Project Operations trên môi trường Dataverse phiên bản 4.8.0.91 
- Quản lý dự án và kế toán trên môi trường Dynamics 365 Finance phiên bản 10.0.16 

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse


| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2133873 | Sửa lỗi hiển thị ký hiệu tiền tệ **Đơn giá bán hàng** trong lưới **Ước tính chi phí**. |
| Định giá và thanh toán | 2174616 | Khi giành được báo giá, bảng giá tùy chỉnh hợp đồng được tham chiếu đến các chi tiết dòng hợp đồng được sao chép từ báo giá. |
| Quản lý cơ hội | 2167475 | Số thuế cố định trong hóa đơn điều chỉnh có nguồn gốc từ một mục nhập thực tế chưa được lập hóa đơn. |
| Quản lý cơ hội | 2176285 | Số thuế không được sao chép từ chi tiết hợp đồng mua bán / dòng báo giá sang chi tiết hợp đồng chi phí / dòng báo giá. |
| Quản lý cơ hội | 2188079 | Quy tắc thanh toán tách biệt không được tạo cho các hợp đồng không dựa trên công việc. |
| Hoạch định và theo dõi dự án | 2125274 | Cập nhật thuộc tính **Bản đồ ghi kép dự án** cho **Lập bản đồ ngày bắt đầu dự án** từ **msdyn\_taskearlieststart** thành **msdyn\_actualstart**. |
| Hoạch định và theo dõi dự án | 2138853 | Chức năng sao chép dự án được cập nhật để đảm bảo các dòng ước tính chi phí mà các nhiệm vụ tham chiếu được sao chép vào dự án đích. |
| Hoạch định và theo dõi dự án | 2154306 | Đã khắc phục sự cố với việc xóa ước tính chi phí trong Project Operations cho các tình huống dựa trên tài nguyên. |
| Hoạch định và theo dõi dự án | 2173259 | Chức năng sao chép dự án được cập nhật để đảm bảo nó không hiển thị thông báo lỗi **Sao chép WBS** trong một số trường hợp nhất định. |
| Thời gian và Chi phí | 2148910 | Khắc phục lỗi hiển thị với trang **Chỉnh sửa mục nhập** trong lưới **Mục nhập thời gian**. |
| Thời gian và Chi phí | 2159798 | Kiểm soát chặt chẽ để đảm bảo không thể chỉnh sửa các mục chi phí đã được phê duyệt. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trên Dynamics 365 Finance

Để biết thêm thông tin, hãy xem [Tính năng mới tháng 1 năm 2021 - Project Operations cho trường hợp dựa trên nguồn lực/hàng không nhập kho](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các cập nhật quy định cho các ứng dụng Tài chính và Hoạt động, hãy xem [Cập nhật quy định](/dynamics365/finance/localizations/regulatory-updates). Một cách khác để tìm hiểu về các chi tiết cập nhật quy định là đăng nhập vào Lifecycle Services (LCS) và dùng công cụ tìm kiếm sự cố để xem các chi tiết cập nhật quy định đã lên kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]