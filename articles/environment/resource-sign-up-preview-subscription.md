---
title: Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về cách đăng ký và triển khai Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334853"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="83afd-103">Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho</span><span class="sxs-lookup"><span data-stu-id="83afd-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="83afd-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="83afd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="83afd-105">Chủ đề này giải thích cách đăng ký ưu đãi dùng thử và triển khai môi trường Project Operations cho các kịch bản dựa trên tài nguyên/không có kho.</span><span class="sxs-lookup"><span data-stu-id="83afd-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83afd-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="83afd-106">Prerequisites</span></span>
- <span data-ttu-id="83afd-107">Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure.</span><span class="sxs-lookup"><span data-stu-id="83afd-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="83afd-108">Bạn có thể tạo đối tượng thuê trong lần đổi ưu đãi đầu tiên.</span><span class="sxs-lookup"><span data-stu-id="83afd-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="83afd-109">Việc triển khai môi trường Finance yêu cầu đăng ký Azure hợp lệ sẽ được lập hóa đơn cho mỗi môi trường.</span><span class="sxs-lookup"><span data-stu-id="83afd-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="83afd-110">Bạn có thể sử dụng đăng ký hiện có của tổ chức mình hoặc sử dụng [Bản dùng thử Azure](https://azure.microsoft.com/en-us/free/) để bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="83afd-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="83afd-111">Môi trường CDS sẽ được cung cấp miễn phí trong khoảng thời gian giới hạn 30 ngày.</span><span class="sxs-lookup"><span data-stu-id="83afd-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83afd-112">Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="83afd-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="83afd-113">Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.</span><span class="sxs-lookup"><span data-stu-id="83afd-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="83afd-114">Đối tượng thuê chỉ có thể sử dụng bản dùng thử một lần.</span><span class="sxs-lookup"><span data-stu-id="83afd-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="83afd-115">Bạn chỉ có thể chạy bản dùng thử một lần.</span><span class="sxs-lookup"><span data-stu-id="83afd-115">You can only run a trial one time.</span></span> <span data-ttu-id="83afd-116">Chúng tôi khuyên bạn nên tạo đối tượng thuê mới cho mục đích dùng thử.</span><span class="sxs-lookup"><span data-stu-id="83afd-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="83afd-117">Dynamics 365 Project Operations (CE) - Bản dùng thử xem trước</span><span class="sxs-lookup"><span data-stu-id="83afd-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="83afd-118">Trước khi bạn bắt đầu, hãy đảm bảo rằng bạn đăng nhập trên trình duyệt bằng tài khoản cơ quan của người dùng trong đối tượng thuê nơi bạn muốn dùng bản xem trước Project Operations.</span><span class="sxs-lookup"><span data-stu-id="83afd-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="83afd-119">Đổi mã ưu đãi đầu tiên, **Dynamics 365 Project Operations** tại đây [Bản dùng thử Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="83afd-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="83afd-120">Xác nhận đơn hàng của bạn.</span><span class="sxs-lookup"><span data-stu-id="83afd-120">Confirm your order.</span></span>

  <span data-ttu-id="83afd-121">Bạn sẽ thấy ưu đãi xác nhận đã được đổi thành công.</span><span class="sxs-lookup"><span data-stu-id="83afd-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="83afd-122">Dynamics 365 Finance bản dùng thử ở dạng xem trước</span><span class="sxs-lookup"><span data-stu-id="83afd-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="83afd-123">Đi đến [Bản dùng thử xem trước Dynamics 365 for Finance](https://aka.ms/trypoche) và thực hiện lại các bước từ phần trước với ưu đãi, Đăng ký môi trường lưu trữ đám mây.</span><span class="sxs-lookup"><span data-stu-id="83afd-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="83afd-124">Gán giấy phép</span><span class="sxs-lookup"><span data-stu-id="83afd-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83afd-125">Bạn sẽ cần quyền truy nhập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="83afd-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="83afd-126">Chuyển đến [Trung tâm quản trị Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.</span><span class="sxs-lookup"><span data-stu-id="83afd-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="83afd-127">Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.</span><span class="sxs-lookup"><span data-stu-id="83afd-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="83afd-128">Xác minh rằng giấy phép **Dynamics 365 Project Operations** đã được chọn và chọn **Lưu thay đổi**.</span><span class="sxs-lookup"><span data-stu-id="83afd-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="83afd-129">Ưu đãi dùng thử Finance không cần phải được gán cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="83afd-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="83afd-130">Bắt đầu một dự án mới trong LCS</span><span class="sxs-lookup"><span data-stu-id="83afd-130">Start a new project in LCS</span></span>

<span data-ttu-id="83afd-131">Tạo dự án LCS mới như được mô tả trong chủ đề [Bắt đầu dự án mới trong LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="83afd-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="83afd-132">Thêm gói đăng ký Azure vào dự án LCS</span><span class="sxs-lookup"><span data-stu-id="83afd-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="83afd-133">Để hoàn thành nhiệm vụ này, hãy làm theo các bước trong chủ đề [Thêm đăng ký Azure vào dự án LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="83afd-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="83afd-134">Triển khai môi trường demo Finance với Project Operations kịch bản dựa trên nguồn lực/hàng không nhập kho</span><span class="sxs-lookup"><span data-stu-id="83afd-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="83afd-135">Làm theo hướng dẫn trong chủ đề [Cung cấp môi trường mới](resource-provision-new-environment.md) để hoàn thành việc triển khai.</span><span class="sxs-lookup"><span data-stu-id="83afd-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="83afd-136">Sử dụng loại triển khai [môi trường demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) để xem trước.</span><span class="sxs-lookup"><span data-stu-id="83afd-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="83afd-137">Cài đặt dữ liệu cấu hình và thiết lập CDS</span><span class="sxs-lookup"><span data-stu-id="83afd-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="83afd-138">Cài đặt dữ liệu cấu hình và thiết lập CDS như được mô tả trong chủ đề [Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="83afd-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="83afd-139">Chỉ hoàn thành bước này sau khi môi trường demo Finance được triển khai và dữ liệu demo đã sẵn sàng.</span><span class="sxs-lookup"><span data-stu-id="83afd-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
