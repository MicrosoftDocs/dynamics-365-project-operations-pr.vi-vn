---
title: Triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá
description: Chủ đề này cung cấp thông tin về cách cài đặt triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086972"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a>Triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Project Operations hỗ trợ nhiều mô hình triển khai. Để xác định mô hình triển khai tốt nhất, hãy xem [Các loại triển khai](determine-deployment-type.md).


> [!IMPORTANT]
> Quá trình triển khai này, triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá, dẫn đến chỉ triển khai **Common Data Service của Project Operations**.

- [Cài đặt Project Operations vào môi trường CDS mới](#new)
- [Cài đặt vào môi trường CDS hiện có](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Cài đặt Project Operations vào môi trường CDS mới

1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy tạo một môi trường CDS mới trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com). Đảm bảo rằng **Cơ sở dữ liệu CDS** và **Ứng dụng Dynamics 365** được kích hoạt. Để biết thêm thông tin, hãy xem [Tạo và quản lý các môi trường trong trung tâm quản trị Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Chọn **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai các ứng dụng Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Cài đặt Project Operations vào môi trường CDS hiện có

1. Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.
2. Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai các ứng dụng Dynamics 365. Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).


