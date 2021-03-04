---
title: Đặt cấu hình cài đặt tham số bổ sung
description: Làm cách nào đặt cấu hình các thiết đặt cho tham số bổ sung trong Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151594"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="08daf-103">Đặt cấu hình các thiết đặt cho tham số bổ sung (Project Service)</span><span class="sxs-lookup"><span data-stu-id="08daf-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="08daf-104">Sau khi đã đặt cấu hình các hạng mục trong chủ đề trước, bạn cần đặt tham số dự án bổ sung để sử dụng cho các dự án của mình.</span><span class="sxs-lookup"><span data-stu-id="08daf-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="08daf-105">Khi cài đặt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lần đầu tiên, bạn đã tạo cài đặt tham số để tạo tất cả các bản ghi đầu tiên cần thiết cho [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] để hoạt động.</span><span class="sxs-lookup"><span data-stu-id="08daf-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="08daf-106">Giờ là lúc quay lại và đặt cấu hình các trường bổ sung cho thiết đặt này.</span><span class="sxs-lookup"><span data-stu-id="08daf-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="08daf-107">Bạn sẽ cần đặt cấu hình các cài đặt sau đây:</span><span class="sxs-lookup"><span data-stu-id="08daf-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="08daf-108">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="08daf-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="08daf-109">Tần suất của hóa đơn</span><span class="sxs-lookup"><span data-stu-id="08daf-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="08daf-110">Mẫu giờ làm việc</span><span class="sxs-lookup"><span data-stu-id="08daf-110">Work hours template</span></span>  
  
-   <span data-ttu-id="08daf-111">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="08daf-111">Price list</span></span>  
 
<span data-ttu-id="08daf-112">Trong bước này, bạn cũng sẽ cho biết loại phân bổ nguồn lực mà bạn muốn:</span><span class="sxs-lookup"><span data-stu-id="08daf-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="08daf-113">**Tập trung**.</span><span class="sxs-lookup"><span data-stu-id="08daf-113">**Central**.</span></span> <span data-ttu-id="08daf-114">Chỉ người quản lý nguồn lực mới có thể phân bổ nguồn lực cho các dự án.</span><span class="sxs-lookup"><span data-stu-id="08daf-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="08daf-115">**Kết hợp**.</span><span class="sxs-lookup"><span data-stu-id="08daf-115">**Hybrid**.</span></span> <span data-ttu-id="08daf-116">Người quản lý nguồn lực, người quản lý dự án và người quản lý khách hàng có thể phân bổ nguồn lực cho dự án.</span><span class="sxs-lookup"><span data-stu-id="08daf-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="08daf-117">Để đặt các tham số dự án:</span><span class="sxs-lookup"><span data-stu-id="08daf-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="08daf-118">Đi tới **Project Service > Tham số**.</span><span class="sxs-lookup"><span data-stu-id="08daf-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="08daf-119">Bấm vào cài đặt tham số bạn muốn đặt cấu hình (cài đặt bạn đã tạo khi cài đặt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lần đầu) hoặc bấm vào **Mới** để tạo cài đặt mới.</span><span class="sxs-lookup"><span data-stu-id="08daf-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="08daf-120">Trong vùng **Chung**, đặt tất cả tùy chọn cho các tham số dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="08daf-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="08daf-121">Trong vùng **Bảng Giá**, bấm vào **+** để thêm bảng giá, chọn bảng giá trong danh sách thả xuống **Bảng Giá Tham số Dự án** và sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="08daf-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="08daf-122">Bấm vào nút **Lưu** ở góc dưới cùng bên phải màn hình.</span><span class="sxs-lookup"><span data-stu-id="08daf-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="08daf-123">Bản ghi tham số dự án phải được duy trì để Project Service hoạt động chính xác.</span><span class="sxs-lookup"><span data-stu-id="08daf-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="08daf-124">Không được xóa bản ghi này.</span><span class="sxs-lookup"><span data-stu-id="08daf-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="08daf-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="08daf-125">See Also</span></span>  
 [<span data-ttu-id="08daf-126">Thiết lập nguồn lực</span><span class="sxs-lookup"><span data-stu-id="08daf-126">Set up resources</span></span>](../psa/set-up-resources.md)
