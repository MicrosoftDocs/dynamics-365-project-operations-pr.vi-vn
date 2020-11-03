---
title: Đơn vị và nhóm đơn vị
description: Chủ đề này cung cấp thông tin về cách tạo đơn vị và nhóm đơn vị đo trong Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087231"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="4ec39-103">Đơn vị và nhóm đơn vị</span><span class="sxs-lookup"><span data-stu-id="4ec39-103">Units and unit groups</span></span>

<span data-ttu-id="4ec39-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="4ec39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ec39-105">Đơn vị là số lượng hoặc phép đo mà bạn bán sản phẩm hoặc dịch vụ của mình.</span><span class="sxs-lookup"><span data-stu-id="4ec39-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="4ec39-106">Ví dụ: nếu bán vật tư làm vườn, bạn có thể bán hạt giống theo đơn vị gói, hộp và ngăn.</span><span class="sxs-lookup"><span data-stu-id="4ec39-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="4ec39-107">Một nhóm đơn vị là một bộ sưu tập của các đơn vị khác nhau.</span><span class="sxs-lookup"><span data-stu-id="4ec39-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="4ec39-108">Để hoàn thành các bước trong chủ đề này, hãy đảm bảo rằng bạn đã được chỉ định vào vai trò Quản trị viên hệ thống hoặc Người quản lý Sales Professional hoặc có các quyền tương đương.</span><span class="sxs-lookup"><span data-stu-id="4ec39-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="4ec39-109">Tạo nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="4ec39-109">Create a unit group</span></span>

1. <span data-ttu-id="4ec39-110">Trong sơ đồ trang web, hãy chọn **Đơn vị**.</span><span class="sxs-lookup"><span data-stu-id="4ec39-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="4ec39-111">Chọn **Mới** và trong hộp hội thoại **Tạo nhóm đơn vị đo** , nhập tên đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="4ec39-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="4ec39-112">Trong trường **Đơn vị chính** , nhập đơn vị đo thông dụng thấp nhấp dùng để bán sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="4ec39-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="4ec39-113">Ví dụ: bạn có thể nhập "cái" hoặc "ounce".</span><span class="sxs-lookup"><span data-stu-id="4ec39-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="4ec39-114">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ec39-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="4ec39-115">Thêm đơn vị đo vào nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="4ec39-115">Add units to a unit group</span></span>

1. <span data-ttu-id="4ec39-116">Mở nhóm đơn vị đo và trên tab **Có liên quan** , chọn **Đơn vị**.</span><span class="sxs-lookup"><span data-stu-id="4ec39-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="4ec39-117">Bạn sẽ thấy rằng đơn vị chính đã được thêm vào.</span><span class="sxs-lookup"><span data-stu-id="4ec39-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="4ec39-118">Chọn **Thêm đơn vị mới** và trên trang **Tạo nhanh: Đơn vị** , trong trường **Tên** , nhập tên của đơn vị.</span><span class="sxs-lookup"><span data-stu-id="4ec39-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="4ec39-119">Trong trường **Số lượng** , nhập số lượng mà đơn vị sẽ chứa đựng.</span><span class="sxs-lookup"><span data-stu-id="4ec39-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="4ec39-120">Ví dụ, nếu một hộp có chứa 2 cái, bạn nên nhập "2".</span><span class="sxs-lookup"><span data-stu-id="4ec39-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="4ec39-121">Trong trường **Đơn vị cơ sở** , chọn một đơn vị cơ sở để thiết lập đơn vị đo thấp nhất cho đơn vị đó.</span><span class="sxs-lookup"><span data-stu-id="4ec39-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="4ec39-122">Ví dụ: bạn có thể chọn "Cái".</span><span class="sxs-lookup"><span data-stu-id="4ec39-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="4ec39-123">Chọn **Lưu** :</span><span class="sxs-lookup"><span data-stu-id="4ec39-123">Select **Save** :</span></span>
