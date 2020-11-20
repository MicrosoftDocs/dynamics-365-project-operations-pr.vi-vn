---
title: Ước tính chi phí
description: Chủ đề này cung cấp thông tin về xác định hoặc ước tính chi phí dựa trên dự án.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131729"
---
# <a name="expense-estimates"></a><span data-ttu-id="48e2d-103">Ước tính chi phí</span><span class="sxs-lookup"><span data-stu-id="48e2d-103">Expense estimates</span></span>
<span data-ttu-id="48e2d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="48e2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48e2d-105">Cùng với việc xác định các ước tính dựa trên nguồn lực, Dynamics 365 Project Operations cho phép người quản lý dự án xác định chi phí dựa trên dự án cho từng dự án.</span><span class="sxs-lookup"><span data-stu-id="48e2d-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="48e2d-106">Mỗi hạng mục chi phí có thể được liên kết với một nhiệm vụ hoặc hạng mục chi phí cụ thể của dự án.</span><span class="sxs-lookup"><span data-stu-id="48e2d-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="48e2d-107">Các loại chi phí thường được xác định ở cấp độ tổ chức.</span><span class="sxs-lookup"><span data-stu-id="48e2d-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="48e2d-108">Giá cho từng loại chi phí thường được xác định theo hệ thống cấp bậc sau:</span><span class="sxs-lookup"><span data-stu-id="48e2d-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="48e2d-109">Tổ chức</span><span class="sxs-lookup"><span data-stu-id="48e2d-109">Organization</span></span>
- <span data-ttu-id="48e2d-110">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="48e2d-110">Customer</span></span>
- <span data-ttu-id="48e2d-111">Báo giá/hợp đồng</span><span class="sxs-lookup"><span data-stu-id="48e2d-111">Quote/contract</span></span>

<span data-ttu-id="48e2d-112">Hoàn thành các bước sau để xem, thêm hoặc xóa chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="48e2d-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="48e2d-113">Đi đến **Dự án** và chọn dự án bạn muốn làm việc.</span><span class="sxs-lookup"><span data-stu-id="48e2d-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="48e2d-114">Chọn tab **Ước tính dự án** và xem danh sách chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="48e2d-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="48e2d-115">Chọn **Chi phí mới** để thêm một khoản chi phí.</span><span class="sxs-lookup"><span data-stu-id="48e2d-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="48e2d-116">Hoặc, chọn một khoản chi phí để xóa, rồi chọn **Xóa chi phí**.</span><span class="sxs-lookup"><span data-stu-id="48e2d-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="48e2d-117">Các thuộc tính sau được xác định cho từng mục chi phí:</span><span class="sxs-lookup"><span data-stu-id="48e2d-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="48e2d-118">**Thể loại**: Các nhóm chung được sử dụng để mô tả tất cả các chi phí phát sinh trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="48e2d-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="48e2d-119">**Ngày bắt đầu**: Ngày dự báo chi phí sẽ phát sinh.</span><span class="sxs-lookup"><span data-stu-id="48e2d-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="48e2d-120">**Số lượng**: Số lượng mục chi phí ước tính cho một danh mục cụ thể.</span><span class="sxs-lookup"><span data-stu-id="48e2d-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="48e2d-121">**Giá vốn đơn vị**: Đơn giá dùng để tính toán chi phí.</span><span class="sxs-lookup"><span data-stu-id="48e2d-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="48e2d-122">**Giá bán hàng đơn vị**: Đơn giá dùng để tính toán giá bán hàng của chi phí.</span><span class="sxs-lookup"><span data-stu-id="48e2d-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

