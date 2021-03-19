---
title: Tổng quan về ghi nhận doanh thu
description: Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278894"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="9dbb2-103">Tổng quan về ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="9dbb2-103">Revenue recognition overview</span></span>

<span data-ttu-id="9dbb2-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="9dbb2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9dbb2-105">Trong Dynamics 365 Project Operations, các nguyên tắc ghi nhận doanh thu sẽ khác nhau theo phương thức thanh toán đã chọn cho dự án hoặc theo tỷ lệ dự án.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="9dbb2-106">Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="9dbb2-107">Kế toán giao dịch bằng phương pháp thanh toán theo thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="9dbb2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="9dbb2-108">Ghi nhận doanh thu và ghi nhận chi phí có mối liên kết với nhau.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="9dbb2-109">Chi phí giao dịch và lần bán chưa thanh toán sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9dbb2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="9dbb2-110">Chi phí dự án và hồ sơ doanh thu sẽ quyết định đến việc liệu các giao dịch bán hàng chưa thanh toán có được đăng vào sổ cái chung hay không.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="9dbb2-111">Nếu chọn **Tích lũy doanh thu**, hệ thống sẽ dùng các tài khoản **giá trị bán hàng WIP** và **Giá trị bán hàng theo doanh thu tích lũy** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="9dbb2-112">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="9dbb2-113">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="9dbb2-113">Transaction type</span></span> | <span data-ttu-id="9dbb2-114">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-114">Debit/Credit</span></span> | <span data-ttu-id="9dbb2-115">Số lượng</span><span class="sxs-lookup"><span data-stu-id="9dbb2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9dbb2-116">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="9dbb2-116">WIP Sales value</span></span> | <span data-ttu-id="9dbb2-117">Nợ</span><span class="sxs-lookup"><span data-stu-id="9dbb2-117">Debit</span></span> | <span data-ttu-id="9dbb2-118">100</span><span class="sxs-lookup"><span data-stu-id="9dbb2-118">100</span></span> |
  | <span data-ttu-id="9dbb2-119">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9dbb2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="9dbb2-120">Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-120">Credit</span></span> | <span data-ttu-id="9dbb2-121">100</span><span class="sxs-lookup"><span data-stu-id="9dbb2-121">100</span></span> |

- <span data-ttu-id="9dbb2-122">Doanh thu sẽ được ghi nhận trong quá trình lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="9dbb2-123">Hệ thống sẽ dùng tài khoản **Doanh thu có hóa đơn** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="9dbb2-124">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="9dbb2-125">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="9dbb2-125">Transaction type</span></span> | <span data-ttu-id="9dbb2-126">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-126">Debit/Credit</span></span> | <span data-ttu-id="9dbb2-127">Số lượng</span><span class="sxs-lookup"><span data-stu-id="9dbb2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9dbb2-128">Số dư của khách hàng</span><span class="sxs-lookup"><span data-stu-id="9dbb2-128">Customer balance</span></span> | <span data-ttu-id="9dbb2-129">Nợ</span><span class="sxs-lookup"><span data-stu-id="9dbb2-129">Debit</span></span> | <span data-ttu-id="9dbb2-130">120</span><span class="sxs-lookup"><span data-stu-id="9dbb2-130">120</span></span> |
  | <span data-ttu-id="9dbb2-131">Thuế bán hàng phải trả</span><span class="sxs-lookup"><span data-stu-id="9dbb2-131">Sales tax payable</span></span> | <span data-ttu-id="9dbb2-132">Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-132">Credit</span></span> | <span data-ttu-id="9dbb2-133">20</span><span class="sxs-lookup"><span data-stu-id="9dbb2-133">20</span></span> |
  | <span data-ttu-id="9dbb2-134">Doanh thu có hóa đơn</span><span class="sxs-lookup"><span data-stu-id="9dbb2-134">Invoiced Revenue</span></span> | <span data-ttu-id="9dbb2-135">Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-135">Credit</span></span> | <span data-ttu-id="9dbb2-136">100</span><span class="sxs-lookup"><span data-stu-id="9dbb2-136">100</span></span> |

- <span data-ttu-id="9dbb2-137">Nếu chọn tích lũy doanh thu khi lần bán chưa thanh toán được đăng, hệ thống sẽ đảo ngược doanh thu tích lũy khi lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="9dbb2-138">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="9dbb2-138">Transaction type</span></span> | <span data-ttu-id="9dbb2-139">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-139">Debit/Credit</span></span> | <span data-ttu-id="9dbb2-140">Số lượng</span><span class="sxs-lookup"><span data-stu-id="9dbb2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="9dbb2-141">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="9dbb2-141">WIP Sales value</span></span> | <span data-ttu-id="9dbb2-142">Có</span><span class="sxs-lookup"><span data-stu-id="9dbb2-142">Credit</span></span> | <span data-ttu-id="9dbb2-143">100</span><span class="sxs-lookup"><span data-stu-id="9dbb2-143">100</span></span> |
  | <span data-ttu-id="9dbb2-144">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9dbb2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="9dbb2-145">Nợ</span><span class="sxs-lookup"><span data-stu-id="9dbb2-145">Debit</span></span> | <span data-ttu-id="9dbb2-146">100</span><span class="sxs-lookup"><span data-stu-id="9dbb2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="9dbb2-147">Kế toán giao dịch bằng phương pháp thanh toán theo giá cố định</span><span class="sxs-lookup"><span data-stu-id="9dbb2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="9dbb2-148">Ghi nhận doanh thu và ghi nhận chi phí tách biệt với nhau.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="9dbb2-149">Chi phí giao dịch sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9dbb2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="9dbb2-150">Giao dịch bán hàng chưa thanh toán sẽ không được tạo.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="9dbb2-151">Doanh thu có thể được ghi nhận trong quá trình lập hóa đơn nếu chi phí dự án và hồ sơ doanh thu có tùy chọn **Nguyên tắc dùng để tính toán mức hoàn thành dự án** được đặt thành **Không WIP**.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="9dbb2-152">Chỉ dùng phương pháp này đối với các dự án ngắn hạn, đơn giản.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="9dbb2-153">Doanh thu có thể được ghi nhận bằng cách dùng các giá trị ước tính doanh thu theo giá cố định, với phương pháp **Hợp đồng hoàn tất** hoặc **Ghi nhận doanh thu theo phần trăm hoàn thành**.</span><span class="sxs-lookup"><span data-stu-id="9dbb2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dbb2-154">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="9dbb2-154">Additional resources</span></span>
[<span data-ttu-id="9dbb2-155">Bài viết về đặt cấu hình hoạt động kế toán cho dự án có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="9dbb2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="9dbb2-156">Dự án ước tính doanh thu giá cố định</span><span class="sxs-lookup"><span data-stu-id="9dbb2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="9dbb2-157">Quản lý ước tính doanh thu</span><span class="sxs-lookup"><span data-stu-id="9dbb2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="9dbb2-158">Phương pháp chi phí hoàn thành</span><span class="sxs-lookup"><span data-stu-id="9dbb2-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]