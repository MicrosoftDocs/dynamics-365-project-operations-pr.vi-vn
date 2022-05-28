---
title: Triển khai Project Operations - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách cài đặt triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580758"
---
# <a name="deploy-project-operations---lite"></a>Triển khai Project Operations - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_



Project Operations hỗ trợ nhiều mô hình triển khai. Để xác định mô hình triển khai tốt nhất, hãy xem [Các loại triển khai](determine-deployment-type.md).


> [!IMPORTANT]
> Quá trình triển khai này, triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá, dẫn đến chỉ triển khai **Dataverse của Project Operations**.

- [Cài đặt Hoạt động Dự án thành một Dataverse môi trường](#new)
- [Cài đặt vào một hiện có Dataverse môi trường](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Cài đặt Hoạt động Dự án thành một Dataverse môi trường

1. Như [Toàn cầu hoặc Power Platform Người quản lý](/power-platform/admin/global-service-administrators-can-administer-without-license) với giấy phép Hoạt động Dự án, hãy tạo một Dataverse môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com). Đảm bảo rằng **Tạo cơ sở dữ liệu cho môi trường này** và **Ứng dụng Dynamics 365** được kích hoạt. Để biết thêm thông tin, hãy xem [Tạo và quản lý các môi trường trong trung tâm quản trị Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Chọn **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Cài đặt Hoạt động Dự án thành hiện có Dataverse môi trường
1. Đảm bảo rằng môi trường chưa được định cấu hình với [viết kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) khi cài đặt sau đó sẽ cài đặt [Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho](project-operations-integrated-deployment-overview.md) các khả năng.
2. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.
3. Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365. Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
