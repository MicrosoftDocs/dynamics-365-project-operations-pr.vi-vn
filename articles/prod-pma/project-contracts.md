---
title: Hợp đồng dự án
description: Chủ đề này cung cấp các ví dụ về hợp đồng dự án mà bạn có thể tạo cho các loại dự án và nguồn tiền khác nhau, cũng như cách thức quản lý hợp đồng và lập hóa đơn cho khách hàng trong dự án.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289575"
---
# <a name="project-contracts"></a><span data-ttu-id="6b2be-103">Hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="6b2be-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b2be-104">Bài viết này cung cấp các ví dụ về hợp đồng dự án mà bạn có thể tạo cho các loại dự án và nguồn tiền khác nhau, cũng như cách thức quản lý hợp đồng và lập hóa đơn cho khách hàng trong dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="6b2be-105">Loại dự án mà bạn tạo cho hợp đồng dự án sẽ xác định phương pháp được sử dụng để lập hóa đơn cho khách hàng trong dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="6b2be-106">Bạn có thể thay đổi hợp đồng dự án và dự án liên quan, nhưng bạn không thể thay đổi loại dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="6b2be-107">Khi sử dụng hợp đồng dự án, bạn có thể lập hóa đơn cho một hoặc nhiều dự án cùng một lúc.</span><span class="sxs-lookup"><span data-stu-id="6b2be-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="6b2be-108">Hợp đồng dự án cũng giúp bảo đảm quy trình lập hóa đơn nhất quán cho mọi dự án nhỏ trong cấu trúc dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="6b2be-109">Mọi dự án sẽ lập hóa đơn phải được liên kết với một hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="6b2be-110">Các mục thiết đặt cho hợp đồng dự án được áp dụng cho mọi dự án và dự án nhỏ được liên kết với hợp đồng dự án đó.</span><span class="sxs-lookup"><span data-stu-id="6b2be-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="6b2be-111">Hợp đồng dự án có thể chỉ định một hoặc nhiều nguồn tiền.</span><span class="sxs-lookup"><span data-stu-id="6b2be-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="6b2be-112">Do đó, bạn có thể chia việc thanh toán cho nhiều nhà tài trợ, thiết lập giới hạn cấp vốn để các nguồn tiền không được lập hóa đơn nhiều hơn mức tiền đã chỉ định và đặt cấu hình các quy tắc cấp vốn để tính phí chi tiêu.</span><span class="sxs-lookup"><span data-stu-id="6b2be-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="6b2be-113">Tài trợ cho hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="6b2be-113">Funding for project contracts</span></span>
<span data-ttu-id="6b2be-114">Một số hợp đồng dự án quy định rằng nhiều bên chia sẻ trách nhiệm cấp vốn chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="6b2be-115">Dưới đây là một số ví dụ:</span><span class="sxs-lookup"><span data-stu-id="6b2be-115">Here are some examples:</span></span>

-   <span data-ttu-id="6b2be-116">Một khách hàng lớn có nhiều yêu cầu bộ phận rằng việc cấp vốn cho một dự án được chia theo bộ phận.</span><span class="sxs-lookup"><span data-stu-id="6b2be-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="6b2be-117">Công ty của bạn chia sẻ chi phí của một dự án lớn với một tổ chức bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="6b2be-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="6b2be-118">Một dự án xây đường được hai thành phố đồng cấp vốn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="6b2be-119">Một dự án xây cầu nhận được khoản trợ cấp của chính phủ và một tập đoàn tư nhân.</span><span class="sxs-lookup"><span data-stu-id="6b2be-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="6b2be-120">Trong Dynamics 365 Finance, bạn có thể tách hóa đơn cho một giao dịch hoặc toàn bộ dự án cho nhiều khách hàng, đơn vị tài trợ hoặc tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6b2be-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="6b2be-121">Trong dự án có nhiều nhà tài trợ, tất cả các bên góp tiền tài trợ cho một dự án tài trợ nâng cao sẽ được gọi là nguồn tiền.</span><span class="sxs-lookup"><span data-stu-id="6b2be-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="6b2be-122">Sau khi khách hàng, tổ chức hoặc đơn vị tài trợ được xác định là nguồn tiền, nguồn này có thể được chỉ định cho một hoặc nhiều quy tắc cấp vốn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="6b2be-123">Quy tắc cấp vốn có các tiêu chí xác định cách thức phân bổ phí cho các nguồn tiền khác nhau trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="6b2be-124">Vì các mặt hàng tồn kho, chẳng hạn như những mặt hàng xuất hiện trong yêu cầu mua hàng và đơn đặt hàng, không thể phân chia được, nên số tiền chi phí cũng không thể phân chia được cho nhiều nguồn tiền tại thời điểm phân phối.</span><span class="sxs-lookup"><span data-stu-id="6b2be-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="6b2be-125">Do đó, giá trị nguồn tiền sẽ vẫn là 0 (không) cho đến khi vấn đề hàng tồn kho được đăng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="6b2be-126">Khi vấn đề hàng tồn kho được đăng, số tiền chi phí sẽ được phân phối theo quy tắc phân phối tài khoản cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="6b2be-127">Sau đây là một số bước mà bạn có thể thực hiện để giúp việc phân chia thanh toán giữa nhiều nguồn tiền trở nên dễ dàng hơn:</span><span class="sxs-lookup"><span data-stu-id="6b2be-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="6b2be-128">Chỉ định rằng tất cả các giao dịch được nhập cho một dự án sẽ sử dụng cùng một loại tiền bán hàng như hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="6b2be-129">Thiết lập giới hạn cấp vốn để nguồn tiền không được lập hóa đơn nhiều hơn một mức tiền cụ thể cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="6b2be-130">Đặt cấu hình quy tắc cấp vốn và giới hạn cấp vốn cho từng nhân viên, mặt hàng, danh mục, nhóm danh mục và loại giao dịch (hoặc cho tất cả các loại giao dịch).</span><span class="sxs-lookup"><span data-stu-id="6b2be-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="6b2be-131">Chọn ngày bắt đầu và ngày kết thúc tùy chọn để xác định khoảng thời gian hiệu lực cho mỗi quy tắc cấp vốn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="6b2be-132">Chỉ định tỷ lệ phần trăm chi trả cho mỗi nguồn tiền.</span><span class="sxs-lookup"><span data-stu-id="6b2be-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="6b2be-133">Chỉ rõ nguồn tiền nào sẽ chịu trách nhiệm thanh toán phần chênh lệch làm tròn số trong phép tính phân bổ vốn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="6b2be-134">Thiết lập các quy tắc xác định cách lập hóa đơn chi phí dự án cho khách hàng bên ngoài và cách tính phí cho các tổ chức nội bộ.</span><span class="sxs-lookup"><span data-stu-id="6b2be-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="6b2be-135">Ghi lại các giao dịch vào tài khoản cấp vốn tạm giữ cho đến khi có thể có thêm tiền hoặc cho đến khi bạn quyết định chịu chi phí nội bộ.</span><span class="sxs-lookup"><span data-stu-id="6b2be-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="6b2be-136">Để xác định nhóm thuế nào sẽ liên kết với một giao dịch, hệ thống tìm kiếm mục chỉ định nhóm thuế cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="6b2be-137">Nếu không có mục chỉ định nhóm thuế nào được lập ở cấp dự án, thì hợp đồng dự án được tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="6b2be-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="6b2be-138">Ví dụ: Nhiều nguồn tiền (đơn giản)</span><span class="sxs-lookup"><span data-stu-id="6b2be-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="6b2be-139">Bảng sau đây cung cấp các kịch bản quản lý việc phân bổ kinh phí giữa nhiều nguồn tiền.</span><span class="sxs-lookup"><span data-stu-id="6b2be-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="6b2be-140">Các kịch bản này được xây dựng dựa trên những giả định sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="6b2be-141">Các mục thiết đặt ưu tiên được tính vào việc phân bổ vốn trước khi áp dụng các tiêu chí quy tắc cấp vốn khác.</span><span class="sxs-lookup"><span data-stu-id="6b2be-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="6b2be-142">Không có phạm vi ngày nào được chỉ định để xác định khoảng thời gian d khi quy tắc cấp vốn có hiệu lực.</span><span class="sxs-lookup"><span data-stu-id="6b2be-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b2be-143"><strong>Kịch bản</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="6b2be-144"><strong>Nguồn tiền</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="6b2be-145"><strong>Phần trăm phân bổ</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="6b2be-146"><strong>Mức độ ưu tiên phân bổ</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b2be-147">Bạn muốn phân bổ chi phí cho một nguồn tiền cho đến khi hết quỹ, rồi phân bổ chi phí cho nguồn tiền thứ hai cho đến khi hết quỹ và cuối cùng phân bổ phần chi phí còn lại cho nguồn tiền thứ ba.</span><span class="sxs-lookup"><span data-stu-id="6b2be-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-148">Nguồn　tiền　1</span><span class="sxs-lookup"><span data-stu-id="6b2be-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="6b2be-149">Nguồn　tiền　2</span><span class="sxs-lookup"><span data-stu-id="6b2be-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="6b2be-150">Nguồn　tiền　3</span><span class="sxs-lookup"><span data-stu-id="6b2be-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-151">100%</span><span class="sxs-lookup"><span data-stu-id="6b2be-151">100%</span></span></li>
<li><span data-ttu-id="6b2be-152">100%</span><span class="sxs-lookup"><span data-stu-id="6b2be-152">100%</span></span></li>
<li><span data-ttu-id="6b2be-153">100%</span><span class="sxs-lookup"><span data-stu-id="6b2be-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-154">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-154">1</span></span></li>
<li><span data-ttu-id="6b2be-155">2</span><span class="sxs-lookup"><span data-stu-id="6b2be-155">2</span></span></li>
<li><span data-ttu-id="6b2be-156">3</span><span class="sxs-lookup"><span data-stu-id="6b2be-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b2be-157">Bạn muốn phân bổ 75 phần trăm chi phí cho một nguồn tiền và 25 phần trăm cho nguồn tiền thứ hai.</span><span class="sxs-lookup"><span data-stu-id="6b2be-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6b2be-158">Khi một trong hai nguồn tiền đó hết tiền, bạn muốn thanh toán các chi phí còn lại từ nguồn tiền thứ ba.</span><span class="sxs-lookup"><span data-stu-id="6b2be-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-159">Nguồn　tiền　1</span><span class="sxs-lookup"><span data-stu-id="6b2be-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="6b2be-160">Nguồn　tiền　2</span><span class="sxs-lookup"><span data-stu-id="6b2be-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="6b2be-161">Nguồn　tiền　3</span><span class="sxs-lookup"><span data-stu-id="6b2be-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-162">75%</span><span class="sxs-lookup"><span data-stu-id="6b2be-162">75%</span></span></li>
<li><span data-ttu-id="6b2be-163">25%</span><span class="sxs-lookup"><span data-stu-id="6b2be-163">25%</span></span></li>
<li><span data-ttu-id="6b2be-164">100%</span><span class="sxs-lookup"><span data-stu-id="6b2be-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-165">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-165">1</span></span></li>
<li><span data-ttu-id="6b2be-166">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-166">1</span></span></li>
<li><span data-ttu-id="6b2be-167">2</span><span class="sxs-lookup"><span data-stu-id="6b2be-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b2be-168">Bạn muốn phân bổ 75 phần trăm chi phí cho một nguồn tiền và 25 phần trăm cho nguồn tiền thứ hai.</span><span class="sxs-lookup"><span data-stu-id="6b2be-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="6b2be-169">Khi một trong hai nguồn tiền đó hết tiền, bạn muốn phân tách phần chi phí còn lại cho nguồn tiền thứ ba và thứ tư.</span><span class="sxs-lookup"><span data-stu-id="6b2be-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-170">Nguồn　tiền　1</span><span class="sxs-lookup"><span data-stu-id="6b2be-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="6b2be-171">Nguồn　tiền　2</span><span class="sxs-lookup"><span data-stu-id="6b2be-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="6b2be-172">Nguồn　tiền　3</span><span class="sxs-lookup"><span data-stu-id="6b2be-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="6b2be-173">Nguồn　tiền　4</span><span class="sxs-lookup"><span data-stu-id="6b2be-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-174">75%</span><span class="sxs-lookup"><span data-stu-id="6b2be-174">75%</span></span></li>
<li><span data-ttu-id="6b2be-175">25%</span><span class="sxs-lookup"><span data-stu-id="6b2be-175">25%</span></span></li>
<li><span data-ttu-id="6b2be-176">50%</span><span class="sxs-lookup"><span data-stu-id="6b2be-176">50%</span></span></li>
<li><span data-ttu-id="6b2be-177">50%</span><span class="sxs-lookup"><span data-stu-id="6b2be-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-178">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-178">1</span></span></li>
<li><span data-ttu-id="6b2be-179">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-179">1</span></span></li>
<li><span data-ttu-id="6b2be-180">2</span><span class="sxs-lookup"><span data-stu-id="6b2be-180">2</span></span></li>
<li><span data-ttu-id="6b2be-181">2</span><span class="sxs-lookup"><span data-stu-id="6b2be-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b2be-182">Bạn muốn phân bổ 25 phần trăm chi phí đầu tiên cho một nguồn tiền và phần chi phí còn lại cho nguồn tiền thứ hai.</span><span class="sxs-lookup"><span data-stu-id="6b2be-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-183">Nguồn　tiền　1</span><span class="sxs-lookup"><span data-stu-id="6b2be-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="6b2be-184">Nguồn　tiền　2</span><span class="sxs-lookup"><span data-stu-id="6b2be-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-185">25%</span><span class="sxs-lookup"><span data-stu-id="6b2be-185">25%</span></span></li>
<li><span data-ttu-id="6b2be-186">100%</span><span class="sxs-lookup"><span data-stu-id="6b2be-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6b2be-187">1</span><span class="sxs-lookup"><span data-stu-id="6b2be-187">1</span></span></li>
<li><span data-ttu-id="6b2be-188">2</span><span class="sxs-lookup"><span data-stu-id="6b2be-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="6b2be-189">Ví dụ: Nhiều nguồn tiền (phức tạp)</span><span class="sxs-lookup"><span data-stu-id="6b2be-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="6b2be-190">Bạn có ba nguồn tiền và muốn sử dụng chúng theo thứ tự sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="6b2be-191">Sử dụng nguồn tiền 2 và nguồn tiền 3 như nhau cho đến khi hết nguồn tiền 2.</span><span class="sxs-lookup"><span data-stu-id="6b2be-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="6b2be-192">Tiếp tục sử dụng nguồn tiền 3 cho đến khi hết.</span><span class="sxs-lookup"><span data-stu-id="6b2be-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="6b2be-193">Sử dụng nguồn 1 sau khi nguồn 3 hết.</span><span class="sxs-lookup"><span data-stu-id="6b2be-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="6b2be-194">Để đạt được mục tiêu này, bạn hãy làm như sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="6b2be-195">Thiết lập giới hạn tiền cho nguồn tiền 2 và nguồn tiền 3 theo số tiền tương ứng của chúng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="6b2be-196">Tạo quy tắc cấp vốn sau đây:</span><span class="sxs-lookup"><span data-stu-id="6b2be-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="6b2be-197">Quy tắc 1 (Ưu tiên 1): Phân bổ 50 phần trăm giao dịch cho nguồn tiền 2 và 50 phần trăm cho nguồn tiền 3.</span><span class="sxs-lookup"><span data-stu-id="6b2be-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="6b2be-198">Quy tắc 2 (Ưu tiên 2): Phân bổ 100% giao dịch cho nguồn tiền 3.</span><span class="sxs-lookup"><span data-stu-id="6b2be-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="6b2be-199">Quy tắc 3 (Ưu tiên 3): Phân bổ 100% giao dịch cho nguồn tiền 1.</span><span class="sxs-lookup"><span data-stu-id="6b2be-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="6b2be-200">Cách thiết lập này có tác dụng vì các giao dịch được đối sánh với các quy tắc và giới hạn để xác định xem có bất kỳ mục nào áp dụng được cho giao dịch không.</span><span class="sxs-lookup"><span data-stu-id="6b2be-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="6b2be-201">Nếu không có quy tắc hoặc giới hạn cụ thể nào được áp dụng cho giao dịch, thì quy tắc Tất cả giao dịch sẽ được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="6b2be-202">Quy tắc Tất cả các giao dịch sẽ so khớp tất cả các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6b2be-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="6b2be-203">Nếu có một quy tắc khớp với một giao dịch, thì tỷ lệ phần trăm đã được phân bổ trong quy tắc đó sẽ được áp dụng trước, nhưng chỉ sau khi các kết quả so khớp đó được đối sánh với bất kỳ giới hạn nào được thiết lập.</span><span class="sxs-lookup"><span data-stu-id="6b2be-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="6b2be-204">Nếu có một giới hạn phù hợp nhưng nguồn tiền đã cạn kiệt, thì quy tắc cấp vốn được liên kết với giới hạn cấp vốn đó sẽ bị bỏ qua và chương trình sẽ đối sánh với quy tắc tiếp theo được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="6b2be-205">Trong một số trường hợp, chỉ một phần giao dịch có thể được phân bổ theo một quy tắc.</span><span class="sxs-lookup"><span data-stu-id="6b2be-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="6b2be-206">Điều này có thể xảy ra vì số tiền sử dụng đã đạt đến giới hạn khi giao dịch được phân bổ.</span><span class="sxs-lookup"><span data-stu-id="6b2be-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="6b2be-207">Trong trường hợp này, chỉ một số tiền nhất định được phân bổ theo quy tắc đó, chẳng hạn như 50 phần trăm cho mỗi nguồn tiền.</span><span class="sxs-lookup"><span data-stu-id="6b2be-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="6b2be-208">Đây là trường hợp trong quy tắc 1 được mô tả bên trên trong phần này.</span><span class="sxs-lookup"><span data-stu-id="6b2be-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="6b2be-209">Phần còn lại được phân bổ theo quy tắc tiếp theo trong chuỗi.</span><span class="sxs-lookup"><span data-stu-id="6b2be-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="6b2be-210">Bảng sau đây xem xét chi tiết hơn tình huống này.</span><span class="sxs-lookup"><span data-stu-id="6b2be-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b2be-211"><strong>Tiêu điểm</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="6b2be-212"><strong>Chi tiết</strong></span><span class="sxs-lookup"><span data-stu-id="6b2be-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b2be-213">Quy tắc cấp vốn</span><span class="sxs-lookup"><span data-stu-id="6b2be-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-214">Quy tắc 1 (Ưu tiên 1): Tất cả các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6b2be-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="6b2be-215">Phân bổ 50% nguồn tiền 2 và 50% nguồn tiền 3.</span><span class="sxs-lookup"><span data-stu-id="6b2be-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="6b2be-216">Quy tắc 2 (Ưu tiên 2): Tất cả các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6b2be-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="6b2be-217">Phân bổ 100% nguồn tiền 3.</span><span class="sxs-lookup"><span data-stu-id="6b2be-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="6b2be-218">Quy tắc 3 (Ưu tiên 2): Tất cả các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6b2be-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="6b2be-219">Phân bổ 100% nguồn tiền 1.</span><span class="sxs-lookup"><span data-stu-id="6b2be-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b2be-220">Giới hạn cấp vốn</span><span class="sxs-lookup"><span data-stu-id="6b2be-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-221">Giới hạn nguồn tiền 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="6b2be-222">Giới hạn nguồn tiền 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="6b2be-223">Giới hạn nguồn tiền 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b2be-224">Giao dịch 1</span><span class="sxs-lookup"><span data-stu-id="6b2be-224">Transaction 1</span></span></td>
<td><span data-ttu-id="6b2be-225"><strong>Số tiền giao dịch:</strong> 100,00<strong>Nguồn tiền:</strong> Giao dịch chỉ được thanh toán theo quy tắc 1, vì giao dịch được thanh toán đầy đủ sau khi áp dụng quy tắc 1.</span><span class="sxs-lookup"><span data-stu-id="6b2be-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="6b2be-226">Giao dịch được cấp vốn đều nhau giữa nguồn tiền 2 và nguồn tiền 3.</span><span class="sxs-lookup"><span data-stu-id="6b2be-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="6b2be-227">Nguồn tiền 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="6b2be-228">Nguồn tiền 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b2be-229">Giao dịch 2</span><span class="sxs-lookup"><span data-stu-id="6b2be-229">Transaction 2</span></span></td>
<td><span data-ttu-id="6b2be-230"><strong>Số tiền giao dịch:</strong> 5.000,00<strong>Nguồn tiền:</strong> Giao dịch được thanh toán theo cả ba quy tắc.</span><span class="sxs-lookup"><span data-stu-id="6b2be-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="6b2be-231"><strong>Quy tắc 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="6b2be-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="6b2be-232">Nguồn tiền 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="6b2be-233">Nguồn tiền 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="6b2be-234">
<strong>Quy tắc 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="6b2be-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="6b2be-235">Nguồn tiền 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="6b2be-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="6b2be-236">
<strong>Quy tắc 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="6b2be-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="6b2be-237">Nguồn tiền 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="6b2be-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b2be-238">Tổng số tiền được phân phối cho từng nguồn tiền</span><span class="sxs-lookup"><span data-stu-id="6b2be-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="6b2be-239">Nguồn tiền 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="6b2be-240">Nguồn tiền 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="6b2be-241">Nguồn tiền 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="6b2be-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="6b2be-242">Quy tắc thanh toán</span><span class="sxs-lookup"><span data-stu-id="6b2be-242">Billing rules</span></span>
<span data-ttu-id="6b2be-243">Khi bạn thương thảo hợp đồng dự án với khách hàng, bạn xác định cách thức và thời điểm có thể lập hóa đơn về khối lượng công việc trong một dự án cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="6b2be-244">Sau khi bạn thiết lập hợp đồng dự án và dự án, bạn có thể thiết lập quy tắc thanh toán cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="6b2be-245">Quy tắc thanh toán được lập dựa trên các điều khoản dự án đã quy định trong hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="6b2be-246">Quy tắc thanh toán mà bạn có thể tạo phụ thuộc vào các điều khoản của hợp đồng dự án và loại dự án, như Thời gian và vật tư hoặc Giá cố định, mà bạn liên kết với quy tắc thanh toán.</span><span class="sxs-lookup"><span data-stu-id="6b2be-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="6b2be-247">Bạn có thể tạo nhiều quy tắc thanh toán cho một hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="6b2be-248">Bạn cũng có thể chỉ định một quy tắc thanh toán cho nhiều dự án được liên kết với cùng một hợp đồng dự án và có các điều khoản thanh toán tương tự nhau.</span><span class="sxs-lookup"><span data-stu-id="6b2be-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="6b2be-249">Bạn có thể thiết lập các loại quy tắc thanh toán sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="6b2be-250">**Đơn vị giao hàng** – Lập hóa đơn cho khách hàng khi bạn hoàn thành một đơn vị giao hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="6b2be-251">Bạn xác định đơn vị giao hàng trong hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="6b2be-252">**Tiến độ** – Lập hóa đơn cho khách hàng khi bạn hoàn thành một tỷ lệ cụ thể của dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="6b2be-253">Bạn có thể thiết lập quy tắc thanh toán để tự động tính toán tỷ lệ phần trăm công việc đã hoàn thành hoặc bạn có thể tính toán thủ công tỷ lệ này và số tiền sẽ lập hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="6b2be-254">**Mốc** – Lập hóa đơn toàn bộ số tiền tương ứng với một mốc dự án khi đạt đến mốc đó cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="6b2be-255">**Phí** – Lập hóa đơn các dịch vụ của bạn cộng với phí quản lý, thường là tỷ lệ phần trăm của chi phí dịch vụ, cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="6b2be-256">**Thời gian và vật tư** – Lập hóa đơn giá trị thời gian và vật tư được dùng trong một dự án cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="6b2be-257">Đối với tất cả các loại quy tắc thanh toán, bạn có thể chỉ định tỷ lệ phần trăm giữ lại được khấu trừ vào hóa đơn cho khách hàng cho đến khi dự án đạt đến giai đoạn đã thỏa thuận.</span><span class="sxs-lookup"><span data-stu-id="6b2be-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="6b2be-258">Tỷ lệ giữ lại thanh toán được quy định trong hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="6b2be-259">Số tiền được tính toán và trừ đi dựa trên tổng giá trị của các dòng trong hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="6b2be-260">Đối với quy tắc thanh toán **Thời gian và vật tư** và **Tiến độ**, bạn có thể chỉ định các danh mục có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="6b2be-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="6b2be-261">Danh mục có thể tính phí cho biết những giao dịch nào cần được đưa vào hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="6b2be-262">Khi bạn đã sẵn sàng lập hóa đơn cho khách hàng, số tiền cần lập hóa đơn cho dự án sẽ được tính toán dựa trên các quy tắc thanh toán và một bản đề xuất hóa đơn dự án sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="6b2be-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="6b2be-263">Các phần sau đây cung cấp ví dụ cho thấy cách thiết lập và quản lý các quy tắc thanh toán cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="6b2be-264">Ví dụ: Tạo quy tắc thanh toán dựa trên số lượng đơn vị được phân phối</span><span class="sxs-lookup"><span data-stu-id="6b2be-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="6b2be-265">Tổ chức của bạn ký kết thỏa thuận cung cấp tổng cộng năm phiên đào tạo cho nhân viên của khách hàng với chi phí 10.000 mỗi buổi.</span><span class="sxs-lookup"><span data-stu-id="6b2be-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="6b2be-266">Bạn lập hóa đơn cho khách hàng sau mỗi buổi đào tạo.</span><span class="sxs-lookup"><span data-stu-id="6b2be-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="6b2be-267">Khi thiết lập các quy tắc thanh toán cho hợp đồng, bạn sử dụng các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="6b2be-268">Đơn vị giao hàng là một phiên đào tạo.</span><span class="sxs-lookup"><span data-stu-id="6b2be-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="6b2be-269">Đơn giá là 10.000 mỗi phiên đào tạo.</span><span class="sxs-lookup"><span data-stu-id="6b2be-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="6b2be-270">Tổng số đơn vị là năm phiên đào tạo.</span><span class="sxs-lookup"><span data-stu-id="6b2be-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="6b2be-271">Khi bạn hoàn thành một phiên đào tạo, bạn có thể tạo hóa đơn 10.000 cho đơn vị đầu tiên đã được cung cấp và gửi hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="6b2be-272">Ví dụ: Tạo quy tắc thanh toán dựa trên tỷ lệ phần trăm hoàn thành dự án cụ thể (tính toán thủ công)</span><span class="sxs-lookup"><span data-stu-id="6b2be-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="6b2be-273">Tổ chức của bạn (một công ty tư vấn phần mềm) ký kết thỏa thuận với khách hàng để phát triển một phần của sản phẩm mà khách hàng đang phát triển.</span><span class="sxs-lookup"><span data-stu-id="6b2be-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="6b2be-274">Tổ chức của bạn đồng ý cung cấp mã phần mềm trong khoảng thời gian sáu tháng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="6b2be-275">Khách hàng đồng ý trả cho tổ chức của bạn tổng cộng 100.000 cho công việc này.</span><span class="sxs-lookup"><span data-stu-id="6b2be-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="6b2be-276">Bạn tạo quy tắc thanh toán để lập hóa đơn cho khách hàng dựa trên tỷ lệ phần trăm công việc được hoàn thành trong dự án theo như quy định trong hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="6b2be-277">Đến cuối tháng đầu tiên, bạn gặp khách hàng để xác định phần trăm công việc đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="6b2be-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="6b2be-278">Sau khi bạn và khách hàng xem xét dự án, bạn quyết định rằng dự án đã hoàn thành được 15 phần trăm.</span><span class="sxs-lookup"><span data-stu-id="6b2be-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="6b2be-279">Bạn tạo hóa đơn 15.000 (15 phần trăm của 100.000) và gửi cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="6b2be-280">Ví dụ: Tạo quy tắc thanh toán dựa trên tỷ lệ phần trăm hoàn thành dự án cụ thể (tính toán tự động)</span><span class="sxs-lookup"><span data-stu-id="6b2be-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="6b2be-281">Tổ chức của bạn (một công ty phát triển phần mềm) đồng ý phát triển gói kế toán tính lương cho một khách hàng với giá 30.000.</span><span class="sxs-lookup"><span data-stu-id="6b2be-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="6b2be-282">Khách hàng đồng ý thanh toán cho tổ chức của bạn dựa trên tỷ lệ phần trăm công việc đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="6b2be-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="6b2be-283">Bạn ước tính rằng chi phí dự án là 20.000.</span><span class="sxs-lookup"><span data-stu-id="6b2be-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="6b2be-284">Hợp đồng dự án chỉ định các hạng mục công việc được sử dụng trong quy trình thanh toán.</span><span class="sxs-lookup"><span data-stu-id="6b2be-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="6b2be-285">Bạn thiết lập các quy tắc thanh toán tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc đã hoàn thành cho từng hạng mục.</span><span class="sxs-lookup"><span data-stu-id="6b2be-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="6b2be-286">Bạn thiết lập ngân sách cho từng hạng mục:</span><span class="sxs-lookup"><span data-stu-id="6b2be-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="6b2be-287">**Phát triển** – Chi phí 15.000 và doanh thu 20.000</span><span class="sxs-lookup"><span data-stu-id="6b2be-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="6b2be-288">**Cài đặt** – Chi phí 5.000 và doanh thu 10.000</span><span class="sxs-lookup"><span data-stu-id="6b2be-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="6b2be-289">Ở lần đầu tiên bạn tạo hóa đơn cho khách hàng, số tiền trên hóa đơn được tính tự động dựa trên các thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="6b2be-290">Sau một tháng, nhân viên tham gia dự án nộp bảng chấm công cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="6b2be-291">Chi phí giờ công của nhân viên là 5.000 cho hạng mục phát triển và 1.000 cho hạng mục cài đặt.</span><span class="sxs-lookup"><span data-stu-id="6b2be-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="6b2be-292">Công việc phát triển đã hoàn thành 33% (chi phí thực tế 5.000/chi phí ngân sách 15.000) và công việc cài đặt đã hoàn thành 20% (chi phí thực tế 1.000/chi phí ngân sách 5.000).</span><span class="sxs-lookup"><span data-stu-id="6b2be-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="6b2be-293">Số tiền trong hóa đơn được tính tự động là 8.667 (33% của 20.000 + 20% của 10.000).</span><span class="sxs-lookup"><span data-stu-id="6b2be-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="6b2be-294">Bạn tạo hóa đơn 8.667 và gửi cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="6b2be-295">Ví dụ: Tạo quy tắc thanh toán dựa trên các mốc đã thỏa thuận</span><span class="sxs-lookup"><span data-stu-id="6b2be-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="6b2be-296">Tổ chức của bạn (một công ty tư vấn quản lý) đồng ý thực hiện nghiên cứu thị trường cho một sản phẩm tiêu dùng mà khách hàng định bán.</span><span class="sxs-lookup"><span data-stu-id="6b2be-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="6b2be-297">Khách hàng đồng ý sử dụng dịch vụ của bạn trong thời gian ba tháng, bắt đầu từ tháng 3, và đồng ý trả 50.000 cho tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="6b2be-298">Dự án có ba mốc:</span><span class="sxs-lookup"><span data-stu-id="6b2be-298">The project has three milestones:</span></span>

-   <span data-ttu-id="6b2be-299">Mốc 1: Thu thập dữ liệu người tiêu dùng – 31 tháng 3</span><span class="sxs-lookup"><span data-stu-id="6b2be-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="6b2be-300">Mốc 2: Phân tích dữ liệu người tiêu dùng – 30 tháng 4</span><span class="sxs-lookup"><span data-stu-id="6b2be-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="6b2be-301">Mốc 3: Trình bày đề xuất khả năng tồn tại của sản phẩm – 31 tháng 5</span><span class="sxs-lookup"><span data-stu-id="6b2be-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="6b2be-302">Khách hàng đồng ý trả cho tổ chức của bạn 10.000 ở mốc đầu tiên, 20.000 ở mốc thứ hai và 20.000 ở mốc thứ ba.</span><span class="sxs-lookup"><span data-stu-id="6b2be-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="6b2be-303">Khi bạn thiết lập hợp đồng dự án, bạn đồng ý xuất hóa đơn cho khách hàng dựa trên mốc thời gian đạt đến.</span><span class="sxs-lookup"><span data-stu-id="6b2be-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="6b2be-304">Quy tắc thanh toán được thiết lập với các bước sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="6b2be-305">Xác định các mốc dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-305">Define the project milestones.</span></span>
-   <span data-ttu-id="6b2be-306">Xác định số tiền sẽ lập hóa đơn cho khách hàng khi đến từng mốc.</span><span class="sxs-lookup"><span data-stu-id="6b2be-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="6b2be-307">Khi đến mốc đầu tiên vào ngày 31/03, bạn đánh dấu mốc là đã hoàn thành, sau đó lập hóa đơn 10.000 và gửi cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="6b2be-308">Bạn sẽ không thể tạo hóa đơn cho một mốc cho đến khi bạn đã đánh dấu mốc đó là đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="6b2be-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="6b2be-309">Ví dụ: Tạo quy tắc thanh toán dựa trên dịch vụ cộng với phí quản lý</span><span class="sxs-lookup"><span data-stu-id="6b2be-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="6b2be-310">Tổ chức của bạn (một công ty tư vấn quản lý) đồng ý thực hiện nghiên cứu thị trường để đánh giá khả năng tồn tại của sản phẩm mà khách hàng (một công ty bán lẻ) đang phát triển.</span><span class="sxs-lookup"><span data-stu-id="6b2be-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="6b2be-311">Các điều khoản của thỏa thuận nêu rõ rằng bạn sẽ cung cấp dịch vụ của ba nhà tư vấn quản lý hàng đầu, những người này sẽ tiến hành nghiên cứu trên cơ sở thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="6b2be-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="6b2be-312">Khách hàng đồng ý trả 100 mỗi giờ, cộng với phí quản lý 10% cho số giờ tư vấn được tính cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6b2be-313">Khi bạn thiết lập hợp đồng dự án, hãy tạo quy tắc thanh toán để thêm phí quản lý 10% vào số giờ tư vấn được tính cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="6b2be-314">Khi bạn tạo hóa đơn cho khách hàng, khách hàng sẽ bị tính phí quản lý 10% cộng với chi phí cho số giờ tư vấn.</span><span class="sxs-lookup"><span data-stu-id="6b2be-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="6b2be-315">Chẳng hạn, nếu ba nhà tư vấn đã làm tổng cộng 200 giờ cho dự án, thì hóa đơn 22.000 sẽ được tạo dựa trên cách tính toán sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="6b2be-316">200 giờ với mức giá 100 mỗi giờ = 20.000</span><span class="sxs-lookup"><span data-stu-id="6b2be-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="6b2be-317">Phí quản lý 10% = 2.000</span><span class="sxs-lookup"><span data-stu-id="6b2be-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="6b2be-318">Tổng số tiền trên hóa đơn = 22.000</span><span class="sxs-lookup"><span data-stu-id="6b2be-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="6b2be-319">Nếu khách hàng phải chịu thuế phí và bạn chọn nhóm thuế bán hàng trong hợp đồng dự án, thì nhóm thuế bán hàng đó sẽ tự động được đưa vào quy tắc thanh toán để xác định phí.</span><span class="sxs-lookup"><span data-stu-id="6b2be-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="6b2be-320">Ví dụ: Tạo quy tắc thanh toán cho giá trị thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="6b2be-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="6b2be-321">Tổ chức của bạn (một công ty tư vấn phần mềm) đồng ý cung cấp năm chuyên gia tư vấn kỹ thuật để làm việc trong một dự án phát triển phần mềm cho một khách hàng trong sáu tháng tới.</span><span class="sxs-lookup"><span data-stu-id="6b2be-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="6b2be-322">Khách hàng đồng ý trả 150 cho mỗi giờ tư vấn, cộng với chi phí văn phòng phẩm.</span><span class="sxs-lookup"><span data-stu-id="6b2be-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="6b2be-323">Tổ chức của bạn sẽ gửi hóa đơn cho khách hàng vào cuối mỗi tháng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="6b2be-324">Khi bạn thiết lập hợp đồng dự án, bạn đồng ý lập hóa đơn thời gian và vật tư cho dự án cho khách hàng mỗi tháng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="6b2be-325">Bạn tạo quy tắc thanh toán bao gồm các thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="6b2be-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="6b2be-326">Thời hạn hợp đồng là sáu tháng.</span><span class="sxs-lookup"><span data-stu-id="6b2be-326">The contract period is six months.</span></span>
-   <span data-ttu-id="6b2be-327">Thời gian tư vấn được tính với mức giá 150 một giờ.</span><span class="sxs-lookup"><span data-stu-id="6b2be-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="6b2be-328">Văn phòng phẩm được lập hóa đơn theo chi phí và tổng chi phí cho dự án không được vượt quá 10.000.</span><span class="sxs-lookup"><span data-stu-id="6b2be-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="6b2be-329">Bạn tạo hóa đơn cho khách hàng vào cuối mỗi tháng theo lịch trong suốt thời gian dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="6b2be-330">Trong tháng đầu tiên, các chuyên gia tư vấn đã ghi lại tổng cộng 800 giờ công trong dự án.</span><span class="sxs-lookup"><span data-stu-id="6b2be-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="6b2be-331">Chi phí văn phòng phẩm được tính cho dự án là 2.000.</span><span class="sxs-lookup"><span data-stu-id="6b2be-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="6b2be-332">Do đó, đến cuối tháng, bạn tạo hóa đơn 122.000, bao gồm 800 giờ với giá 150 mỗi giờ cộng với 2.000 cho văn phòng phẩm.</span><span class="sxs-lookup"><span data-stu-id="6b2be-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]