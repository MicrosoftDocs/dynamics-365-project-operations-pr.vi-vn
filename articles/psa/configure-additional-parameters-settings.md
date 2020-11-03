---
title: Đặt cấu hình cài đặt tham số bổ sung
description: Làm cách nào đặt cấu hình các thiết đặt cho tham số bổ sung trong Project Service
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087108"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="b9afd-103">Đặt cấu hình các thiết đặt cho tham số bổ sung (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b9afd-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b9afd-104">Sau khi đã đặt cấu hình các hạng mục trong chủ đề trước, bạn cần đặt tham số dự án bổ sung để sử dụng cho các dự án của mình.</span><span class="sxs-lookup"><span data-stu-id="b9afd-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="b9afd-105">Khi cài đặt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lần đầu tiên, bạn đã tạo cài đặt tham số để tạo tất cả các bản ghi đầu tiên cần thiết cho [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] để hoạt động.</span><span class="sxs-lookup"><span data-stu-id="b9afd-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="b9afd-106">Giờ là lúc quay lại và đặt cấu hình các trường bổ sung cho thiết đặt này.</span><span class="sxs-lookup"><span data-stu-id="b9afd-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="b9afd-107">Bạn sẽ cần đặt cấu hình các cài đặt sau đây:</span><span class="sxs-lookup"><span data-stu-id="b9afd-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="b9afd-108">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="b9afd-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="b9afd-109">Tần suất của hóa đơn</span><span class="sxs-lookup"><span data-stu-id="b9afd-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="b9afd-110">Mẫu giờ làm việc</span><span class="sxs-lookup"><span data-stu-id="b9afd-110">Work hours template</span></span>  
  
-   <span data-ttu-id="b9afd-111">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="b9afd-111">Price list</span></span>  
 
<span data-ttu-id="b9afd-112">Trong bước này, bạn cũng sẽ cho biết loại phân bổ nguồn lực mà bạn muốn:</span><span class="sxs-lookup"><span data-stu-id="b9afd-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="b9afd-113">**Tập trung**.</span><span class="sxs-lookup"><span data-stu-id="b9afd-113">**Central**.</span></span> <span data-ttu-id="b9afd-114">Chỉ người quản lý nguồn lực mới có thể phân bổ nguồn lực cho các dự án.</span><span class="sxs-lookup"><span data-stu-id="b9afd-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="b9afd-115">**Kết hợp**.</span><span class="sxs-lookup"><span data-stu-id="b9afd-115">**Hybrid**.</span></span> <span data-ttu-id="b9afd-116">Người quản lý nguồn lực, người quản lý dự án và người quản lý khách hàng có thể phân bổ nguồn lực cho dự án.</span><span class="sxs-lookup"><span data-stu-id="b9afd-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="b9afd-117">Để đặt các tham số dự án:</span><span class="sxs-lookup"><span data-stu-id="b9afd-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="b9afd-118">Đi tới **Project Service > Tham số**.</span><span class="sxs-lookup"><span data-stu-id="b9afd-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="b9afd-119">Bấm vào cài đặt tham số bạn muốn đặt cấu hình (cài đặt bạn đã tạo khi cài đặt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lần đầu) hoặc bấm vào **Mới** để tạo cài đặt mới.</span><span class="sxs-lookup"><span data-stu-id="b9afd-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="b9afd-120">Trong vùng **Chung** , đặt tất cả tùy chọn cho các tham số dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="b9afd-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="b9afd-121">Trong vùng **Bảng Giá** , bấm vào **+** để thêm bảng giá, chọn bảng giá trong danh sách thả xuống **Bảng Giá Tham số Dự án** và sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b9afd-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="b9afd-122">Bấm vào nút **Lưu** ở góc dưới cùng bên phải màn hình.</span><span class="sxs-lookup"><span data-stu-id="b9afd-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="b9afd-123">Bản ghi tham số dự án phải được duy trì để Project Service hoạt động chính xác.</span><span class="sxs-lookup"><span data-stu-id="b9afd-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="b9afd-124">Không được xóa bản ghi này.</span><span class="sxs-lookup"><span data-stu-id="b9afd-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="b9afd-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b9afd-125">See Also</span></span>  
 [<span data-ttu-id="b9afd-126">Thiết lập nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b9afd-126">Set up resources</span></span>](../psa/set-up-resources.md)
