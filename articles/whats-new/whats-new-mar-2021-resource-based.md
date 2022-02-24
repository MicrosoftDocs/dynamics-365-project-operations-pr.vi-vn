---
title: Tính năng mới tháng 3 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 3 năm 2021 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d114ee64bd26d3271a1c72a7404c0f7035c2b61
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948085"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới tháng 3 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường Dataverse phiên bản 4.8.0.91 
- Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.16 

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

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

Để biết thêm thông tin, hãy xem [Tính năng mới tháng 1 năm 2021 - Project Operations cho trường hợp dựa trên nguồn lực/hàng không nhập kho](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng Finance and Operations, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Một cách khác để tìm hiểu về các chi tiết cập nhật quy định là đăng nhập vào Lifecycle Services (LCS) và dùng công cụ tìm kiếm sự cố để xem các chi tiết cập nhật quy định đã lên kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]