---
title: Hủy kích hoạt bảng giá
description: Chủ đề này giải thích cách hủy kích hoạt hoặc loại bỏ các bảng giá cũ hoặc không dùng đến.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001362"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="279c7-103">Hủy kích hoạt bảng giá</span><span class="sxs-lookup"><span data-stu-id="279c7-103">Deactivate price lists</span></span> 

<span data-ttu-id="279c7-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="279c7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="279c7-105">Để loại bỏ các bảng giá cũ hoặc không dùng đến khỏi Dynamics 365 Project Operations, có hai bước mà bạn phải hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="279c7-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="279c7-106">Loại bỏ hoặc xóa bảng giá khỏi các trang cụ thể.</span><span class="sxs-lookup"><span data-stu-id="279c7-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="279c7-107">Hủy kích hoạt hoặc xóa bảng giá khỏi Các bảng giá hiện hoạt trên trang **Bảng giá**.</span><span class="sxs-lookup"><span data-stu-id="279c7-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="279c7-108">Bạn phải hoàn thành cả hai bước để loại bỏ hoàn toàn một bảng giá.</span><span class="sxs-lookup"><span data-stu-id="279c7-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="279c7-109">Chỉ thực hiện bước 2, tức là trực tiếp xóa hoặc hủy kích hoạt bảng giá từ dạng xem Bảng giá hiện hoạt, là không đủ.</span><span class="sxs-lookup"><span data-stu-id="279c7-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="279c7-110">Bạn cũng phải xóa liên kết của bảng giá này khỏi tất cả những nơi được đề cập trong bước 1.</span><span class="sxs-lookup"><span data-stu-id="279c7-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="279c7-111">Xóa bảng giá khỏi các trang cụ thể</span><span class="sxs-lookup"><span data-stu-id="279c7-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="279c7-112">Để xóa bảng giá khỏi Project Operations, hãy truy cập các trang sau:</span><span class="sxs-lookup"><span data-stu-id="279c7-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="279c7-113">Trang **Tham số dự án** > tab **Bảng giá**</span><span class="sxs-lookup"><span data-stu-id="279c7-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="279c7-114">Trang **Đơn vị tổ chức** > lưới **Bảng giá**</span><span class="sxs-lookup"><span data-stu-id="279c7-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="279c7-115">Trang **Tài khoản** > lưới **Bảng giá dự án**</span><span class="sxs-lookup"><span data-stu-id="279c7-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="279c7-116">Trang **Báo giá dự án** > lưới **Bảng giá dự án**: Điều này áp dụng cho tất cả các báo giá dự án hiện hoạt.</span><span class="sxs-lookup"><span data-stu-id="279c7-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="279c7-117">Trang **Hợp đồng dự án** > lưới **Bảng giá dự án**: Điều này áp dụng cho tất cả các hợp đồng dự án hiện hoạt.</span><span class="sxs-lookup"><span data-stu-id="279c7-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="279c7-118">Đối với mỗi trang, bạn cần chọn bảng giá mà mình muốn xóa, sau đó chọn **Xóa**.</span><span class="sxs-lookup"><span data-stu-id="279c7-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="279c7-119">Xóa hoặc hủy kích hoạt bảng giá khỏi trang Bảng giá</span><span class="sxs-lookup"><span data-stu-id="279c7-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="279c7-120">Để xóa một bảng giá khỏi các bảng giá hiện hoạt, hãy đi đến **Bán hàng** > **Khách hàng** > **Bảng giá**.</span><span class="sxs-lookup"><span data-stu-id="279c7-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="279c7-121">Chọn bảng giá mà mình muốn xóa, sau đó chọn **Xóa**.</span><span class="sxs-lookup"><span data-stu-id="279c7-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="279c7-122">Nếu bảng giá được đề cập trên bất kỳ giao dịch hiện có nào, bạn sẽ không thể xóa bảng giá đó.</span><span class="sxs-lookup"><span data-stu-id="279c7-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="279c7-123">Nếu điều này xảy ra, bạn có thể hủy kích hoạt để bảng giá không xuất hiện trong bất kỳ dạng xem nào.</span><span class="sxs-lookup"><span data-stu-id="279c7-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="279c7-124">Để hủy kích hoạt bảng giá, hãy chọn lại bảng giá, sau đó chọn **Hủy kích hoạt**.</span><span class="sxs-lookup"><span data-stu-id="279c7-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
