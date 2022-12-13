---
title: Triển khai Project Operations Lite
description: Bài viết này cung cấp thông tin về cách cài đặt triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811005"
---
# <a name="deploy-project-operations-lite"></a>Triển khai Project Operations Lite

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_



Project Operations hỗ trợ nhiều mô hình triển khai. Để xác định mô hình triển khai tốt nhất, hãy xem [Các loại triển khai](determine-deployment-type.md).


> [!IMPORTANT]
> Quá trình triển khai này, triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá, dẫn đến chỉ triển khai **Dataverse của Project Operations**.

- [Cài đặt Project Operations vào môi trường Dataverse mới](#new)
- [Cài đặt vào môi trường Dataverse hiện có](#existing)
- [Cài đặt vào một môi trường Dataverse hiện có có các thành phần ghi kép](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Cài đặt Project Operations Lite vào môi trường Dataverse mới

1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy tạo một môi trường Dataverse mới trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com). Đảm bảo rằng **Tạo cơ sở dữ liệu cho môi trường này** và **Ứng dụng Dynamics 365** được kích hoạt. Để biết thêm thông tin, hãy xem [Tạo và quản lý các môi trường trong trung tâm quản trị Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Chọn **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Cài đặt Project Operations Lite vào môi trường Dataverse hiện có 
1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.
1. Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365. Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Cài đặt Project Operations Lite vào môi trường Dataverse hiện có đã có các giải pháp ghi kép

Nếu muốn tiếp tục chạy Project Operations ở chế độ Triển khai bản rút gọn, bạn nên làm theo các bước sau:

1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.
1. Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365. Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](/power-platform/admin/manage-apps).
1. Do môi trường của bạn có các thành phần Ghi kép giúp tích hợp với các ứng dụng tài chính và vận hành được cài đặt, quá trình cài đặt Project Operations cũng sẽ cài đặt các chức năng và tiện ích mở rộng cần thiết để tích hợp dữ liệu liên quan đến Dự án vào các ứng dụng tài chính và vận hành. Vì bạn muốn chạy Project Operations trong triển khai Lite, nên các thành phần tích hợp này sẽ bị xóa vì chúng sẽ tạo ra các hạn chế và chi phí chung cho các kịch bản triển khai Lite. Gỡ cài đặt thủ công các giải pháp **Dynamics 365 Project Operations Dual Write** và **Dynamics 365 Project Operations Dual Write Entity Maps** để xóa các thành phần này.
1. Chuyển đến **Hoạt động dự án -> Cài đặt -> Tham số**. Mở trang chi tiết **Tham số dự án** và đặt trường **Hành vi nâng cấp giải pháp** thành **Lite Chỉ**. Điều này đảm bảo rằng mọi nâng cấp tiếp theo của Project Operations sẽ không đưa các thành phần tích hợp trở lại Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
