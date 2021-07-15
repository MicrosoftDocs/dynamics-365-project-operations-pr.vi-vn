---
title: Triển khai ứng dụng Project Operations Dataverse theo cách thủ công có hỗ trợ ghi kép
description: Chủ đề này giải thích cách triển khai ứng dụng Project Operations Dataverse để hỗ trợ ghi kép.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274034"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="6139b-103">Triển khai ứng dụng Project Operations Dataverse theo cách thủ công có hỗ trợ ghi kép</span><span class="sxs-lookup"><span data-stu-id="6139b-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="6139b-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="6139b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6139b-105">Chủ đề này giải thích cách triển khai Microsoft Dynamics 365 Project Operations theo cách thủ công trong Microsoft Dataverse để hỗ trợ ghi kép.</span><span class="sxs-lookup"><span data-stu-id="6139b-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="6139b-106">Project Operations phát hiện cấu hình của môi trường và bổ sung hỗ trợ bổ sung cho tính năng ghi kép nếu các điều kiện tiên quyết được đáp ứng.</span><span class="sxs-lookup"><span data-stu-id="6139b-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="6139b-107">Trong quá trình triển khai thông qua Microsoft Dynamics Lifecycle Services (LCS), nếu bạn đã làm theo hướng dẫn trong chủ đề này, bạn có thể bỏ qua việc triển khai tích hợp Microsoft Power Platform (trước đây được gọi là môi trường Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="6139b-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="6139b-108">Quá trình triển khai Project Operations trong Dataverse để hỗ trợ ghi kép có bốn bước chính:</span><span class="sxs-lookup"><span data-stu-id="6139b-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="6139b-109">[Tạo một môi trường mới trong Dataverse hỗ trợ ghi kép](#create).</span><span class="sxs-lookup"><span data-stu-id="6139b-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="6139b-110">[Thêm điều kiện tiên quyết ghi kép vào môi trường](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="6139b-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="6139b-111">[Thêm ứng dụng Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="6139b-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="6139b-112">[Liên kết các môi trường của bạn](#link).</span><span class="sxs-lookup"><span data-stu-id="6139b-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="6139b-113">Tạo một môi trường mới trong Dataverse hỗ trợ ghi kép</span><span class="sxs-lookup"><span data-stu-id="6139b-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="6139b-114">Để hoàn thành quy trình này, bạn phải đăng nhập với tư cách quản trị viên.</span><span class="sxs-lookup"><span data-stu-id="6139b-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="6139b-115">Mở [Trung tâm quản trị Power Platform](https://admin.powerplatform.com) và đăng nhập với tư cách quản trị viên.</span><span class="sxs-lookup"><span data-stu-id="6139b-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="6139b-116">Và và đặt tên cho môi trường mới.</span><span class="sxs-lookup"><span data-stu-id="6139b-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="6139b-117">Chọn loại môi trường.</span><span class="sxs-lookup"><span data-stu-id="6139b-117">Select the environment type.</span></span> <span data-ttu-id="6139b-118">Nếu bạn đã đăng ký nhận ưu đãi dùng thử, hãy chọn **Bản dùng thử (dựa trên đăng ký)**.</span><span class="sxs-lookup"><span data-stu-id="6139b-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="6139b-119">Xác nhận khu vực triển khai.</span><span class="sxs-lookup"><span data-stu-id="6139b-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="6139b-120">Bật tùy chọn **Tạo cơ sở dữ liệu cho môi trường này**.</span><span class="sxs-lookup"><span data-stu-id="6139b-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="6139b-121">Xác nhận ngôn ngữ, sau đó xác nhận rằng đơn vị tiền tệ đó khớp với đơn vị tiền tệ cho ứng dụng Finance and Operations của bạn.</span><span class="sxs-lookup"><span data-stu-id="6139b-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="6139b-122">Bật tùy chọn **Ứng dụng Dynamics 365** và xác nhận rằng trường **Tự động triển khai những ứng dụng này** được đặt thành **Không có**.</span><span class="sxs-lookup"><span data-stu-id="6139b-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="6139b-123">Thêm một nhóm bảo mật, nếu một nhóm bảo mật được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="6139b-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="6139b-124">Chọn **Lưu** để tạo môi trường.</span><span class="sxs-lookup"><span data-stu-id="6139b-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="6139b-125">Chờ cho đến khi việc triển khai hoàn tất và môi trường đạt trạng thái **Sẵn sàng**.</span><span class="sxs-lookup"><span data-stu-id="6139b-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="6139b-126">Thêm điều kiện tiên quyết ghi kép vào môi trường</span><span class="sxs-lookup"><span data-stu-id="6139b-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="6139b-127">Hỗ trợ ghi kép bao gồm các trường bổ sung được thêm vào các thực thể chính, chẳng hạn như thực thể **Công ty**.</span><span class="sxs-lookup"><span data-stu-id="6139b-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="6139b-128">Nếu bạn đang thêm hỗ trợ ghi kép vào môi trường hiện có, bạn có thể phải cập nhật dữ liệu để bật hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="6139b-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="6139b-129">Để biết thông tin về cách khởi động dữ liệu, hãy xem [Dữ liệu công ty Bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="6139b-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="6139b-130">Để biết thêm thông tin về ghi kép, hãy xem [Yêu cầu hệ thống ghi kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="6139b-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="6139b-131">Hoàn thành quy trình này để thêm điều kiện tiên quyết ghi kép vào môi trường của bạn.</span><span class="sxs-lookup"><span data-stu-id="6139b-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="6139b-132">Mở môi trường mà bạn vừa tạo, sau đó đi tới **Tài nguyên** \> **Ứng dụng Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6139b-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="6139b-133">Chọn **Giải pháp chính ghi kép** trong danh sách ứng dụng và cài đặt giải pháp đó.</span><span class="sxs-lookup"><span data-stu-id="6139b-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="6139b-134">Chờ cho đến khi quá trình cài đặt hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="6139b-134">Wait until the installation is completed.</span></span> <span data-ttu-id="6139b-135">Sau đó, chọn **Giải pháp điều phối ứng dụng ghi kép** trong danh sách ứng dụng và cài đặt giải pháp đó.</span><span class="sxs-lookup"><span data-stu-id="6139b-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="6139b-136">Thêm ứng dụng Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="6139b-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="6139b-137">Bạn chỉ có thể hoàn thành quy trình này nếu đã hoàn thành các quy trình trước đó trước khi cài đặt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6139b-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="6139b-138">Trong quá trình cài đặt, hệ thống sẽ phân tích cấu hình môi trường và hỗ trợ thêm tính năng ghi kép nếu được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="6139b-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="6139b-139">Mở môi trường mà bạn đã tạo, sau đó đi tới **Tài nguyên** \> **Ứng dụng Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6139b-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="6139b-140">Chọn **Microsoft Dynamics 365 Project Operations** trong danh sách ứng dụng và cài đặt.</span><span class="sxs-lookup"><span data-stu-id="6139b-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="6139b-141">Liên kết các môi trường của bạn</span><span class="sxs-lookup"><span data-stu-id="6139b-141">Link your environments</span></span>

<span data-ttu-id="6139b-142">Sau khi môi trường Dataverse được triển khai, bạn có thể thiết lập liên kết trong ứng dụng Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6139b-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="6139b-143">Làm theo các bước trong [Sử dụng trình hướng dẫn ghi kép để liên kết các môi trường của bạn](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="6139b-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
