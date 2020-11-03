---
title: Bật các tính năng ứng dụng Project Finder Mobile
description: Làm cách nào để bật các tính năng ứng dụng Project Finder Mobile cho Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087115"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Bật các tính năng ứng dụng Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Nguồn lực của bạn có thể sử dụng ứng dụng Project Finder Mobile trên điện thoại của họ với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] để tìm các dự án mới để làm việc và cập nhật các bộ kỹ năng của họ.  
  
 Ứng dụng hiện khả dụng cho điện thoại [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] và [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Bạn cần thiết lập một vài tùy chọn trong cài đặt tham số cho đơn vị tổ chức để người dùng có thể xem các yêu cầu về nguồn lực dự án và cập nhật kỹ năng của họ.  
  
> [!NOTE]
>  Ứng dụng Project Finder Mobile chỉ hoạt động với [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], không phải bản cài đặt tại chỗ.  
  
1. Đi tới **Project Service > Tham số**.  
  
2. Bấm vào cài đặt tham số mà bạn muốn sử dụng để cho phép các tính năng của ứng dụng Project Finder Mobile.  
  
3. Trong vùng **Chung** , đặt **Hiển thị các yêu cầu về nguồn lực cho nguồn lực** thành **Có**.  
  
4. Đặt **Cho phép cập nhật kỹ năng theo nguồn lực** thành **Có**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Đây là một cài đặt toàn cầu. Người quản lý dự án có thể đặt có hiển thị từng dự án trên trang **Nhóm Dự án** của dự án đó hay không.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Thông báo qua email  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gửi email liên quan đến yêu cầu về nguồn lực cho những người nhận sau đây vào những thời điểm sau đây:  
  
|Người nhận|Sự kiện|  
|---------------|-----------|  
|Người quản lý dự án|-   Khi một nguồn lực đăng ký cho một dự án bằng ứng dụng Project Finder Mobile.|  
|Nguồn lực|-   Khi công việc dự án mà nguồn lực đăng ký vào đã được thực hiện bởi một nguồn lực khác.<br />-   Khi yêu cầu phê duyệt kỹ năng được chấp thuận hoặc từ chối.<br />-   Khi yêu cầu đăng ký dự án đã được chấp thuận hoặc từ chối.|  
  
## <a name="privacy-notice"></a>Thông báo bảo mật  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Thiết lập nguồn lực](../psa/set-up-resources.md)
