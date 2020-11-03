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
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="b6d14-103">Triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá</span><span class="sxs-lookup"><span data-stu-id="b6d14-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="b6d14-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="b6d14-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b6d14-105">Project Operations hỗ trợ nhiều mô hình triển khai.</span><span class="sxs-lookup"><span data-stu-id="b6d14-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="b6d14-106">Để xác định mô hình triển khai tốt nhất, hãy xem [Các loại triển khai](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="b6d14-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b6d14-107">Quá trình triển khai này, triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá, dẫn đến chỉ triển khai **Common Data Service của Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b6d14-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="b6d14-108">Cài đặt Project Operations vào môi trường CDS mới</span><span class="sxs-lookup"><span data-stu-id="b6d14-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="b6d14-109">Cài đặt vào môi trường CDS hiện có</span><span class="sxs-lookup"><span data-stu-id="b6d14-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="b6d14-110">Cài đặt Project Operations vào môi trường CDS mới</span><span class="sxs-lookup"><span data-stu-id="b6d14-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="b6d14-111">Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy tạo một môi trường CDS mới trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="b6d14-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="b6d14-112">Đảm bảo rằng **Cơ sở dữ liệu CDS** và **Ứng dụng Dynamics 365** được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="b6d14-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="b6d14-113">Để biết thêm thông tin, hãy xem [Tạo và quản lý các môi trường trong trung tâm quản trị Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="b6d14-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="b6d14-114">Chọn **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai các ứng dụng Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6d14-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="b6d14-115">Cài đặt Project Operations vào môi trường CDS hiện có</span><span class="sxs-lookup"><span data-stu-id="b6d14-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="b6d14-116">Là [Quản trị viên Power Platform hay Quản trị viên toàn cầu](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) có giấy phép Project Operations, hãy định vị môi trường trong [Trung tâm quản trị PowerPlatform](https://admin.powerplatform.com) nơi bạn muốn cài đặt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b6d14-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="b6d14-117">Cài đặt **Microsoft Dynamics 365 Project Operations** từ danh sách triển khai các ứng dụng Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6d14-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="b6d14-118">Để biết thêm thông tin, hãy xem [Quản lý ứng dụng Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="b6d14-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


