---
title: Thêm gói đăng ký Azure vào dự án LCS
description: Chủ đề này cung cấp thông tin về cách kết nối gói đăng ký Azure của bạn với dự án LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880564"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="28ce1-103">Thêm gói đăng ký Azure vào dự án LCS</span><span class="sxs-lookup"><span data-stu-id="28ce1-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="28ce1-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="28ce1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="28ce1-105">Môi trường được lưu trữ trên đám mây phải được triển khai bằng cách sử dụng đăng ký Azure hiện có.</span><span class="sxs-lookup"><span data-stu-id="28ce1-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="28ce1-106">Chủ đề này sẽ giải thích cách kết nối gói đăng ký Azure hiện có của bạn với dự án LCS.</span><span class="sxs-lookup"><span data-stu-id="28ce1-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="28ce1-107">Cấp sự đồng ý của quản trị viên</span><span class="sxs-lookup"><span data-stu-id="28ce1-107">Grant admin consent</span></span>

1. <span data-ttu-id="28ce1-108">Trong dự án LCS, trong phần **Môi trường**, hãy chọn **cài đặt Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Thiết đặt Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="28ce1-110">Trên trang **Thiết đặt dự án**, trên tab **Trình kết nối Azure**, hãy chọn **Cho phép**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="28ce1-111">Thao tác này cho phép các môi trường được triển khai cho dự án này.</span><span class="sxs-lookup"><span data-stu-id="28ce1-111">This allows environments to be deployed to this project.</span></span>

![Trình kết nối Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="28ce1-113">Chọn **Cho phép** một lần nữa để cung cấp sự đồng ý của quản trị viên.</span><span class="sxs-lookup"><span data-stu-id="28ce1-113">Select **Authorize** again to provide admin consent.</span></span>

![Cấp sự đồng ý của quản trị viên](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="28ce1-115">Chấp nhận yêu cầu quyền.</span><span class="sxs-lookup"><span data-stu-id="28ce1-115">Accept the permissions request.</span></span>

![Chấp nhận yêu cầu quyền](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="28ce1-117">Sự định quyền hiện đã hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="28ce1-117">The authorization is now complete.</span></span> 

![Định quyền thành công](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="28ce1-119">Cung cấp quyền truy cập vào Dịch vụ triển khai Dynamics cho đăng ký Azure của bạn</span><span class="sxs-lookup"><span data-stu-id="28ce1-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="28ce1-120">Chuyển đến [thanh toán Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) rồi chọn gói đăng ký của bạn.</span><span class="sxs-lookup"><span data-stu-id="28ce1-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="28ce1-121">Dịch vụ triển khai Dynamics cần truy cập vào gói đăng ký này để có thể triển khai các môi trường.</span><span class="sxs-lookup"><span data-stu-id="28ce1-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Thông tin chi tiết về Đăng ký Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="28ce1-123">Chọn **Kiểm soát truy cập (IAM)** trong ngăn điều hướng, sau đó chọn **Thêm gán vai trò**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="28ce1-124">Trong thanh trượt ở bên phải, hãy chọn **Vai trò người đóng góp** và trong danh sách được cung cấp, hãy tìm và chọn **Dịch vụ triển khai Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="28ce1-125">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-125">Select **Save**.</span></span>

![Quyền truy cập vào gói đăng ký](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="28ce1-127">Thêm trình kết nối gói đăng ký vào dự án LCS</span><span class="sxs-lookup"><span data-stu-id="28ce1-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="28ce1-128">Trong dự án LCS của bạn, trên trang **cài đặt Microsoft Azure**, hãy chọn **Thêm** để thêm một trình kết nối mới.</span><span class="sxs-lookup"><span data-stu-id="28ce1-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="28ce1-129">Nhập ID đăng ký Azure của bạn.</span><span class="sxs-lookup"><span data-stu-id="28ce1-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="28ce1-130">Bạn có thể tìm thấy ID đăng ký Azure của mình trong [Cổng thông tin Azure](https://ms.portal.azure.com/), ở phần  **Cài đặt**  ở phía dưới bên trái của màn hình.</span><span class="sxs-lookup"><span data-stu-id="28ce1-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="28ce1-131">Trong trường **Đặt cấu hình để sử dụng Azure Resource Manager**, hãy chọn **Có**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="28ce1-132">Đảm bảo Miền của đối tượng thuê AAD đăng ký của Azure khớp với đăng ký Azure sở hữu miền mà bạn đang sử dụng rồi chọn **Tiếp theo**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="28ce1-133">Trên màn hình **Thiết lập Microsoft Azure**, hãy chọn **Tiếp theo** để xác nhận.</span><span class="sxs-lookup"><span data-stu-id="28ce1-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="28ce1-134">Nếu bạn gặp lỗi trên màn hình này, hãy quay lại phần [Cấp quyền truy cập vào Dịch vụ triển khai Dynamics cho đăng ký Azure](#provide) trong chủ đề này và đảm bảo rằng bạn đã hoàn thành tất cả các bước.</span><span class="sxs-lookup"><span data-stu-id="28ce1-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="28ce1-135">Tải Chứng chỉ quản lý Azure xuống một thư mục cục bộ trên máy tính của bạn.</span><span class="sxs-lookup"><span data-stu-id="28ce1-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="28ce1-136">Yêu cầu quản trị viên đăng ký Azure của bạn tải chứng chỉ lên Cổng quản lý của Azure bằng cách chọn đăng ký rồi chuyển đến phần **Cài đặt** > **Chứng chỉ quản lý**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="28ce1-137">Chứng chỉ này cho phép LCS thay mặt bạn để giao tiếp với Azure.</span><span class="sxs-lookup"><span data-stu-id="28ce1-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="28ce1-138">Bạn có thể bỏ qua bước này nếu người dùng của bạn có quyền truy cập vào đăng ký.</span><span class="sxs-lookup"><span data-stu-id="28ce1-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="28ce1-139">Chọn  **Tiếp theo**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-139">Select  **Next**.</span></span>
8. <span data-ttu-id="28ce1-140">Chọn vùng Azure để triển khai và chọn một trung tâm dữ liệu gần nơi bạn định sử dụng hệ thống này.</span><span class="sxs-lookup"><span data-stu-id="28ce1-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="28ce1-141">Chọn  **Kết nối**.</span><span class="sxs-lookup"><span data-stu-id="28ce1-141">Select  **Connect**.</span></span>

<span data-ttu-id="28ce1-142">Bạn đã kết nối thành công đăng ký Azure của mình.</span><span class="sxs-lookup"><span data-stu-id="28ce1-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="28ce1-143">Bây giờ bạn có thể triển khai môi trường Dynamics 365 Finance được lưu trữ trên đám mây.</span><span class="sxs-lookup"><span data-stu-id="28ce1-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
