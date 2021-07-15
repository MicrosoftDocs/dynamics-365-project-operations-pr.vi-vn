---
title: Tổng quan về ghi nhận doanh thu
description: Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368052"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="21d76-103">Tổng quan về ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="21d76-103">Revenue recognition overview</span></span>

<span data-ttu-id="21d76-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="21d76-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21d76-105">Trong Dynamics 365 Project Operations, các nguyên tắc ghi nhận doanh thu sẽ khác nhau theo phương thức thanh toán đã chọn cho dự án hoặc theo tỷ lệ dự án.</span><span class="sxs-lookup"><span data-stu-id="21d76-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="21d76-106">Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.</span><span class="sxs-lookup"><span data-stu-id="21d76-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="21d76-107">Kế toán giao dịch bằng phương pháp thanh toán theo thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="21d76-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="21d76-108">Ghi nhận doanh thu và ghi nhận chi phí có mối liên kết với nhau.</span><span class="sxs-lookup"><span data-stu-id="21d76-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="21d76-109">Chi phí giao dịch và lần bán chưa thanh toán sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="21d76-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="21d76-110">Chi phí dự án và hồ sơ doanh thu sẽ quyết định đến việc liệu các giao dịch bán hàng chưa thanh toán có được đăng vào sổ cái chung hay không.</span><span class="sxs-lookup"><span data-stu-id="21d76-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="21d76-111">Nếu chọn **Tích lũy doanh thu**, hệ thống sẽ dùng các tài khoản **giá trị bán hàng WIP** và **Giá trị bán hàng theo doanh thu tích lũy** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="21d76-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="21d76-112">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="21d76-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="21d76-113">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="21d76-113">Transaction type</span></span> | <span data-ttu-id="21d76-114">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="21d76-114">Debit/Credit</span></span> | <span data-ttu-id="21d76-115">Số lượng</span><span class="sxs-lookup"><span data-stu-id="21d76-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="21d76-116">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="21d76-116">WIP Sales value</span></span> | <span data-ttu-id="21d76-117">Nợ</span><span class="sxs-lookup"><span data-stu-id="21d76-117">Debit</span></span> | <span data-ttu-id="21d76-118">100</span><span class="sxs-lookup"><span data-stu-id="21d76-118">100</span></span> |
  | <span data-ttu-id="21d76-119">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="21d76-119">Accrued revenue sales value</span></span> | <span data-ttu-id="21d76-120">Có</span><span class="sxs-lookup"><span data-stu-id="21d76-120">Credit</span></span> | <span data-ttu-id="21d76-121">100</span><span class="sxs-lookup"><span data-stu-id="21d76-121">100</span></span> |

- <span data-ttu-id="21d76-122">Doanh thu sẽ được ghi nhận trong quá trình lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="21d76-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="21d76-123">Hệ thống sẽ dùng tài khoản **Doanh thu có hóa đơn** trong quá trình đăng.</span><span class="sxs-lookup"><span data-stu-id="21d76-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="21d76-124">Sau đây là ví dụ về phương pháp này.</span><span class="sxs-lookup"><span data-stu-id="21d76-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="21d76-125">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="21d76-125">Transaction type</span></span> | <span data-ttu-id="21d76-126">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="21d76-126">Debit/Credit</span></span> | <span data-ttu-id="21d76-127">Số lượng</span><span class="sxs-lookup"><span data-stu-id="21d76-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="21d76-128">Số dư của khách hàng</span><span class="sxs-lookup"><span data-stu-id="21d76-128">Customer balance</span></span> | <span data-ttu-id="21d76-129">Nợ</span><span class="sxs-lookup"><span data-stu-id="21d76-129">Debit</span></span> | <span data-ttu-id="21d76-130">120</span><span class="sxs-lookup"><span data-stu-id="21d76-130">120</span></span> |
  | <span data-ttu-id="21d76-131">Thuế bán hàng phải trả</span><span class="sxs-lookup"><span data-stu-id="21d76-131">Sales tax payable</span></span> | <span data-ttu-id="21d76-132">Có</span><span class="sxs-lookup"><span data-stu-id="21d76-132">Credit</span></span> | <span data-ttu-id="21d76-133">20</span><span class="sxs-lookup"><span data-stu-id="21d76-133">20</span></span> |
  | <span data-ttu-id="21d76-134">Doanh thu có hóa đơn</span><span class="sxs-lookup"><span data-stu-id="21d76-134">Invoiced Revenue</span></span> | <span data-ttu-id="21d76-135">Có</span><span class="sxs-lookup"><span data-stu-id="21d76-135">Credit</span></span> | <span data-ttu-id="21d76-136">100</span><span class="sxs-lookup"><span data-stu-id="21d76-136">100</span></span> |

- <span data-ttu-id="21d76-137">Nếu chọn tích lũy doanh thu khi lần bán chưa thanh toán được đăng, hệ thống sẽ đảo ngược doanh thu tích lũy khi lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="21d76-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="21d76-138">Loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="21d76-138">Transaction type</span></span> | <span data-ttu-id="21d76-139">Nợ/Có</span><span class="sxs-lookup"><span data-stu-id="21d76-139">Debit/Credit</span></span> | <span data-ttu-id="21d76-140">Số lượng</span><span class="sxs-lookup"><span data-stu-id="21d76-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="21d76-141">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="21d76-141">WIP Sales value</span></span> | <span data-ttu-id="21d76-142">Có</span><span class="sxs-lookup"><span data-stu-id="21d76-142">Credit</span></span> | <span data-ttu-id="21d76-143">100</span><span class="sxs-lookup"><span data-stu-id="21d76-143">100</span></span> |
  | <span data-ttu-id="21d76-144">Giá trị bán hàng theo doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="21d76-144">Accrued revenue sales value</span></span> | <span data-ttu-id="21d76-145">Nợ</span><span class="sxs-lookup"><span data-stu-id="21d76-145">Debit</span></span> | <span data-ttu-id="21d76-146">100</span><span class="sxs-lookup"><span data-stu-id="21d76-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="21d76-147">Kế toán giao dịch bằng phương pháp thanh toán theo giá cố định</span><span class="sxs-lookup"><span data-stu-id="21d76-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="21d76-148">Ghi nhận doanh thu và ghi nhận chi phí tách biệt với nhau.</span><span class="sxs-lookup"><span data-stu-id="21d76-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="21d76-149">Chi phí giao dịch sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="21d76-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="21d76-150">Giao dịch bán hàng chưa thanh toán sẽ không được tạo.</span><span class="sxs-lookup"><span data-stu-id="21d76-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="21d76-151">Doanh thu có thể được ghi nhận trong quá trình lập hóa đơn nếu chi phí dự án và hồ sơ doanh thu có tùy chọn **Nguyên tắc dùng để tính toán mức hoàn thành dự án** được đặt thành **Không WIP**.</span><span class="sxs-lookup"><span data-stu-id="21d76-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="21d76-152">Chỉ dùng phương pháp này đối với các dự án ngắn hạn, đơn giản.</span><span class="sxs-lookup"><span data-stu-id="21d76-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="21d76-153">Doanh thu có thể được ghi nhận bằng cách dùng các giá trị ước tính doanh thu theo giá cố định, với phương pháp **Hợp đồng hoàn tất** hoặc **Ghi nhận doanh thu theo phần trăm hoàn thành**.</span><span class="sxs-lookup"><span data-stu-id="21d76-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21d76-154">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="21d76-154">Additional resources</span></span>
[<span data-ttu-id="21d76-155">Bài viết về đặt cấu hình hoạt động kế toán cho dự án có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="21d76-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="21d76-156">Dự án ước tính doanh thu giá cố định</span><span class="sxs-lookup"><span data-stu-id="21d76-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="21d76-157">Quản lý ước tính doanh thu</span><span class="sxs-lookup"><span data-stu-id="21d76-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="21d76-158">Phương pháp chi phí hoàn thành</span><span class="sxs-lookup"><span data-stu-id="21d76-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]