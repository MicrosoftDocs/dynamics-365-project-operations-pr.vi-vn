---
title: Tổng quan về ghi nhận doanh thu
description: Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013782"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="843e0-103">Tổng quan về ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="843e0-103">Revenue recognition overview</span></span>

<span data-ttu-id="843e0-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="843e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="843e0-105">Trong Dynamics 365 Project Operations, các nguyên tắc ghi nhận doanh thu sẽ khác nhau theo phương thức thanh toán đã chọn cho dự án hoặc theo tỷ lệ dự án.</span><span class="sxs-lookup"><span data-stu-id="843e0-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="843e0-106">Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.</span><span class="sxs-lookup"><span data-stu-id="843e0-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="843e0-107">Kế toán giao dịch bằng phương pháp thanh toán theo thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="843e0-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="843e0-108">Ghi nhận doanh thu và ghi nhận chi phí có mối liên kết với nhau.</span><span class="sxs-lookup"><span data-stu-id="843e0-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="843e0-109">Chi phí giao dịch và lần bán chưa thanh toán sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="843e0-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="843e0-110">Chi phí dự án và hồ sơ doanh thu sẽ quyết định đến việc liệu các giao dịch bán hàng chưa thanh toán có được đăng vào sổ cái chung hay không.</span><span class="sxs-lookup"><span data-stu-id="843e0-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="843e0-111">Nếu chọn **Tích lũy doanh thu**, hệ thống sẽ dùng các tài khoản **giá trị bán hàng WIP** và **Giá trị bán hàng theo doanh thu tích lũy** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="843e0-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="843e0-112">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="843e0-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="843e0-113">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="843e0-113">Transaction type</span></span> | <span data-ttu-id="843e0-114">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="843e0-114">Debit/Credit</span></span> | <span data-ttu-id="843e0-115">Số lượng</span><span class="sxs-lookup"><span data-stu-id="843e0-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="843e0-116">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="843e0-116">WIP Sales value</span></span> | <span data-ttu-id="843e0-117">Nợ</span><span class="sxs-lookup"><span data-stu-id="843e0-117">Debit</span></span> | <span data-ttu-id="843e0-118">100</span><span class="sxs-lookup"><span data-stu-id="843e0-118">100</span></span> |
  | <span data-ttu-id="843e0-119">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="843e0-119">Accrued revenue sales value</span></span> | <span data-ttu-id="843e0-120">Có</span><span class="sxs-lookup"><span data-stu-id="843e0-120">Credit</span></span> | <span data-ttu-id="843e0-121">100</span><span class="sxs-lookup"><span data-stu-id="843e0-121">100</span></span> |

- <span data-ttu-id="843e0-122">Doanh thu sẽ được ghi nhận trong quá trình lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="843e0-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="843e0-123">Hệ thống sẽ dùng tài khoản **Doanh thu có hóa đơn** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="843e0-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="843e0-124">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="843e0-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="843e0-125">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="843e0-125">Transaction type</span></span> | <span data-ttu-id="843e0-126">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="843e0-126">Debit/Credit</span></span> | <span data-ttu-id="843e0-127">Số lượng</span><span class="sxs-lookup"><span data-stu-id="843e0-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="843e0-128">Số dư của khách hàng</span><span class="sxs-lookup"><span data-stu-id="843e0-128">Customer balance</span></span> | <span data-ttu-id="843e0-129">Nợ</span><span class="sxs-lookup"><span data-stu-id="843e0-129">Debit</span></span> | <span data-ttu-id="843e0-130">120</span><span class="sxs-lookup"><span data-stu-id="843e0-130">120</span></span> |
  | <span data-ttu-id="843e0-131">Thuế bán hàng phải trả</span><span class="sxs-lookup"><span data-stu-id="843e0-131">Sales tax payable</span></span> | <span data-ttu-id="843e0-132">Có</span><span class="sxs-lookup"><span data-stu-id="843e0-132">Credit</span></span> | <span data-ttu-id="843e0-133">20</span><span class="sxs-lookup"><span data-stu-id="843e0-133">20</span></span> |
  | <span data-ttu-id="843e0-134">Doanh thu có hóa đơn</span><span class="sxs-lookup"><span data-stu-id="843e0-134">Invoiced Revenue</span></span> | <span data-ttu-id="843e0-135">Có</span><span class="sxs-lookup"><span data-stu-id="843e0-135">Credit</span></span> | <span data-ttu-id="843e0-136">100</span><span class="sxs-lookup"><span data-stu-id="843e0-136">100</span></span> |

- <span data-ttu-id="843e0-137">Nếu chọn tích lũy doanh thu khi lần bán chưa thanh toán được đăng, hệ thống sẽ đảo ngược doanh thu tích lũy khi lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="843e0-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="843e0-138">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="843e0-138">Transaction type</span></span> | <span data-ttu-id="843e0-139">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="843e0-139">Debit/Credit</span></span> | <span data-ttu-id="843e0-140">Số lượng</span><span class="sxs-lookup"><span data-stu-id="843e0-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="843e0-141">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="843e0-141">WIP Sales value</span></span> | <span data-ttu-id="843e0-142">Có</span><span class="sxs-lookup"><span data-stu-id="843e0-142">Credit</span></span> | <span data-ttu-id="843e0-143">100</span><span class="sxs-lookup"><span data-stu-id="843e0-143">100</span></span> |
  | <span data-ttu-id="843e0-144">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="843e0-144">Accrued revenue sales value</span></span> | <span data-ttu-id="843e0-145">Nợ</span><span class="sxs-lookup"><span data-stu-id="843e0-145">Debit</span></span> | <span data-ttu-id="843e0-146">100</span><span class="sxs-lookup"><span data-stu-id="843e0-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="843e0-147">Kế toán giao dịch bằng phương pháp thanh toán theo giá cố định</span><span class="sxs-lookup"><span data-stu-id="843e0-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="843e0-148">Ghi nhận doanh thu và ghi nhận chi phí tách biệt với nhau.</span><span class="sxs-lookup"><span data-stu-id="843e0-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="843e0-149">Chi phí giao dịch sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="843e0-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="843e0-150">Giao dịch bán hàng chưa thanh toán sẽ không được tạo.</span><span class="sxs-lookup"><span data-stu-id="843e0-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="843e0-151">Doanh thu có thể được ghi nhận trong quá trình lập hóa đơn nếu chi phí dự án và hồ sơ doanh thu có tùy chọn **Nguyên tắc dùng để tính toán mức hoàn thành dự án** được đặt thành **Không WIP**.</span><span class="sxs-lookup"><span data-stu-id="843e0-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="843e0-152">Chỉ dùng phương pháp này đối với các dự án ngắn hạn, đơn giản.</span><span class="sxs-lookup"><span data-stu-id="843e0-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="843e0-153">Doanh thu có thể được ghi nhận bằng cách dùng các giá trị ước tính doanh thu theo giá cố định, với phương pháp **Hợp đồng hoàn tất** hoặc **Ghi nhận doanh thu theo phần trăm hoàn thành**.</span><span class="sxs-lookup"><span data-stu-id="843e0-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="843e0-154">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="843e0-154">Additional resources</span></span>
[<span data-ttu-id="843e0-155">Bài viết về đặt cấu hình hoạt động kế toán cho dự án có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="843e0-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="843e0-156">Dự án ước tính doanh thu giá cố định</span><span class="sxs-lookup"><span data-stu-id="843e0-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="843e0-157">Quản lý ước tính doanh thu</span><span class="sxs-lookup"><span data-stu-id="843e0-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="843e0-158">Phương pháp chi phí hoàn thành</span><span class="sxs-lookup"><span data-stu-id="843e0-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]