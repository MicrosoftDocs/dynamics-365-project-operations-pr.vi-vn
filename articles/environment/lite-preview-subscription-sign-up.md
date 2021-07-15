---
title: Đăng ký gói xem trước - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đăng ký và triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334808"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="5c599-103">Đăng ký gói xem trước – bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="5c599-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="5c599-104">Chủ đề này giải thích cách đăng ký ưu đãi dùng thử và triển khai ưu đãi - triển khai bản đơn giản Dynamics 365 Project Operations cho lập hóa đơn ước giá.</span><span class="sxs-lookup"><span data-stu-id="5c599-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="5c599-105">Quá trình này sẽ thay đổi trong các phiên bản sắp tới của Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5c599-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5c599-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5c599-106">Prerequisites</span></span>
- <span data-ttu-id="5c599-107">Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure.</span><span class="sxs-lookup"><span data-stu-id="5c599-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="5c599-108">Bạn có thể tạo đối tượng thuê trong lần đổi ưu đãi đầu tiên.</span><span class="sxs-lookup"><span data-stu-id="5c599-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c599-109">Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="5c599-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="5c599-110">Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.</span><span class="sxs-lookup"><span data-stu-id="5c599-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="5c599-111">Đối tượng thuê chỉ có thể sử dụng bản dùng thử một lần.</span><span class="sxs-lookup"><span data-stu-id="5c599-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="5c599-112">Bạn chỉ có thể chạy bản dùng thử một lần.</span><span class="sxs-lookup"><span data-stu-id="5c599-112">You can only run a trial one time.</span></span> <span data-ttu-id="5c599-113">Chúng tôi khuyên bạn nên tạo đối tượng thuê mới cho mục đích dùng thử.</span><span class="sxs-lookup"><span data-stu-id="5c599-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="5c599-114">Dùng thử Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="5c599-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="5c599-115">Trước khi bạn bắt đầu, hãy đảm bảo rằng bạn đăng nhập trên trình duyệt bằng tài khoản cơ quan của người dùng trong đối tượng thuê nơi bạn muốn dùng bản xem trước Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5c599-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="5c599-116">Đi đến [Bản dùng thử Project Operations](https://aka.ms/try-po) để đổi mã ưu đãi đầu tiên, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="5c599-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="5c599-117">Xác nhận đơn hàng của bạn.</span><span class="sxs-lookup"><span data-stu-id="5c599-117">Confirm your order.</span></span>

  <span data-ttu-id="5c599-118">Bạn sẽ thấy ưu đãi xác nhận đã được đổi thành công.</span><span class="sxs-lookup"><span data-stu-id="5c599-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="5c599-119">Gán giấy phép</span><span class="sxs-lookup"><span data-stu-id="5c599-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c599-120">Bạn sẽ cần quyền truy nhập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="5c599-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="5c599-121">Chuyển đến [Trung tâm quản trị Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.</span><span class="sxs-lookup"><span data-stu-id="5c599-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="5c599-122">Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.</span><span class="sxs-lookup"><span data-stu-id="5c599-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="5c599-123">Xác minh rằng giấy phép **Dynamics 365 Project Operations** được chọn.</span><span class="sxs-lookup"><span data-stu-id="5c599-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="5c599-124">Chọn **Lưu thay đổi**.</span><span class="sxs-lookup"><span data-stu-id="5c599-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="5c599-125">Tạo môi trường Dataverse mới</span><span class="sxs-lookup"><span data-stu-id="5c599-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="5c599-126">Cung cấp môi trường triển khai Project Operations Dataverse mới bằng cách làm theo các hướng dẫn trong chủ đề [Mô hình triển khai Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="5c599-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="5c599-127">Khi bạn chọn loại môi trường, hãy bảo đảm sử dụng **Bản dùng thử (Dựa trên gói đăng ký)**.</span><span class="sxs-lookup"><span data-stu-id="5c599-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Môi trường mới](./media/19CreateEnvironment.png)

2. <span data-ttu-id="5c599-129">Chọn mục thiết đặt **Bật ứng dụng Dynamics 365** và để trống mục **Tự động triển khai các ứng dụng này**.</span><span class="sxs-lookup"><span data-stu-id="5c599-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="5c599-130">Chọn **Lưu** để tạo môi trường.</span><span class="sxs-lookup"><span data-stu-id="5c599-130">Select **Save** to create the environment.</span></span>

  ![Thêm cơ sở dữ liệu](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="5c599-132">Sau khi tạo môi trường, hãy cài đặt giải pháp **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="5c599-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Cài đặt giải pháp](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="5c599-134">Cài đặt cấu hình CDS và thiết lập dữ liệu demo</span><span class="sxs-lookup"><span data-stu-id="5c599-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="5c599-135">Cài đặt cấu hình CDS và thiết lập dữ liệu demo bằng cách làm theo các hướng dẫn trong chủ đề [Áp dụng dữ liệu cấu hình và thiết lập demo](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="5c599-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
