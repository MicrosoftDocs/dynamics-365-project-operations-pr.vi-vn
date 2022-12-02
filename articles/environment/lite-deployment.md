---
title: Triển khai Project Operations - bản đơn giản
description: Bài viết này cung cấp thông tin về cách cài đặt triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930344"
---
# <a name="deploy-project-operations---lite"></a>Triển khai Project Operations - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_



Project Operations hỗ trợ nhiều mô hình triển khai. Để xác định mô hình triển khai tốt nhất, hãy xem [Các loại triển khai](determine-deployment-type.md).


> [!IMPORTANT]
> Quá trình triển khai này, triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá, dẫn đến chỉ triển khai **Dataverse của Project Operations**.

- [Cài đặt Project Operations vào môi trường Dataverse mới](#new)
- [Cài đặt vào môi trường Dataverse hiện có](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Cài đặt Project Operations vào môi trường Dataverse mới

1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy tạo một môi trường Dataverse mới trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com). Đảm bảo rằng **Tạo cơ sở dữ liệu cho môi trường này** và **Ứng dụng Dynamics 365** được kích hoạt. Để biết thêm thông tin, hãy xem [Tạo và quản lý các môi trường trong trung tâm quản trị Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Chọn **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Cài đặt Project Operations vào môi trường Dataverse hiện có
1. Đảm bảo rằng môi trường chưa được định cấu hình với [ghi kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) là cài đặt sau đó sẽ cài đặt các khả năng [Project Operations cho các kịch bản dựa trên nguồn lực/không trữ kho](project-operations-integrated-deployment-overview.md).
2. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.
3. Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai của các ứng dụng Dynamics 365. Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
