---
title: Xác định ước tính doanh thu và chi phí dự án
description: Làm cách nào để xác định ước tính doanh thu và chi phí dự án trong Project Service
author: ruhercul
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 851e98cf5481ec7df3f430801a9d3b327794f68c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284969"
---
# <a name="determine-project-cost-and-revenue-estimates"></a><span data-ttu-id="9de97-103">Xác định ước tính doanh thu và chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="9de97-103">Determine project cost and revenue estimates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9de97-104">Ước tính dự án cung cấp dạng xem tài chính cho các công việc được ước tính và lên lịch trong cấu trúc phân tích chi tiết công việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="9de97-104">Project estimates provide the financial view for the work estimated and scheduled in the project’s work breakdown structure.</span></span> <span data-ttu-id="9de97-105">Dạng xem ước tính cho bạn biết tác động của chi phí và doanh thu với những công việc dự định.</span><span class="sxs-lookup"><span data-stu-id="9de97-105">The estimates view informs you of the cost and revenue impact of the planned work.</span></span> <span data-ttu-id="9de97-106">Dạng xem ước tính cung cấp công cụ để xem thông tin về một số thứ nguyên được định trước nhằm cho bạn biết về các tác động tài chính của dự án một cách khái quát nhất.</span><span class="sxs-lookup"><span data-stu-id="9de97-106">The estimates view provides a tool to see the information on a number of pre-defined dimensions to best inform you of the financial impact of the project.</span></span>  
  
## <a name="cost-and-sales-value-of-the-project"></a><span data-ttu-id="9de97-107">Giá trị chi phí và kinh doanh của dự án</span><span class="sxs-lookup"><span data-stu-id="9de97-107">Cost and sales value of the project</span></span>  
<span data-ttu-id="9de97-108">Bảng giá [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] xác định chi phí và mức tính phí cho các vai trò mà dự án sử dụng.</span><span class="sxs-lookup"><span data-stu-id="9de97-108">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] price lists define the cost and bill rates for roles projects use.</span></span> <span data-ttu-id="9de97-109">Dựa trên vai trò được liên kết với các nhiệm vụ trong cấu trúc phân tích chi tiết công việc của dự án, bạn có thể xác định tác động của chi phí và doanh thu đến các công việc liên quan.</span><span class="sxs-lookup"><span data-stu-id="9de97-109">Based on the roles associated with the tasks in the project’s work breakdown structure, you can determine the cost and revenue impact of the work involved.</span></span>  
  
## <a name="cost-price-defaulting"></a><span data-ttu-id="9de97-110">Đặt mặc định giá vốn</span><span class="sxs-lookup"><span data-stu-id="9de97-110">Cost price defaulting</span></span>  
<span data-ttu-id="9de97-111">Mọi dự án đều thuộc về một tổ chức (được thể hiện trong **Đơn vị sở hữu** trong dự án).</span><span class="sxs-lookup"><span data-stu-id="9de97-111">Every project belongs to an organization (indicated in **Owning Unit** in the project).</span></span> <span data-ttu-id="9de97-112">Biểu giá được liên kết với đơn vị tổ chức sở hữu xác định đơn giá vốn.</span><span class="sxs-lookup"><span data-stu-id="9de97-112">The price list associated with the owning organizational unit determines the unit cost price.</span></span> <span data-ttu-id="9de97-113">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] xác định giá vốn cho các vai trò bằng cách tìm kiếm bộ kết hợp vai trò, đơn vị hoặc đơn vị theo tổ chức trong bảng giá vốn để có giá vốn chính xác cho ngày có hiệu lực trên các đường dự toán.</span><span class="sxs-lookup"><span data-stu-id="9de97-113">The [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determine cost prices for roles by searching for the combination of role, unit, and organizational unit in the cost price list to get the correct cost price for the date effective on estimate lines.</span></span>  
  
<span data-ttu-id="9de97-114">Nếu sự kết hợp giữa vai trò, đơn vị và đơn vị tổ chức không dẫn đến giá vốn từ biểu giá của đơn vị sở hữu, đơn vị được bỏ qua để tạo điều kiện cho sự kết hợp giữa vai trò và đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="9de97-114">If the combination of role, unit, and organizational unit doesn’t result in a cost price from the owning unit’s price list, the unit is disregarded in favor of the combination of role and organizational unit.</span></span> <span data-ttu-id="9de97-115">Nếu có giá vốn, giá này sẽ được chuyển đổi thành đơn vị bạn đã chọn trên dòng ước tính.</span><span class="sxs-lookup"><span data-stu-id="9de97-115">If there is a cost price, this price is converted to the unit you chose on the estimate line.</span></span>  
  
<span data-ttu-id="9de97-116">Nếu sự kết hợp giữa vai trò và đơn vị tổ chức không dẫn đến một mức giá vốn, đơn vị tổ chức được bỏ qua để tạo điều kiện cho sự kết hợp giữa vai trò và đơn vị và giá được đặt mặc định sau khi áp dụng bất kỳ hoạt động chuyển đổi nào, nếu cần thiết.</span><span class="sxs-lookup"><span data-stu-id="9de97-116">If the combination of role and organizational unit doesn’t result in a cost price, the organizational unit is disregarded in favor of the role and unit combination, and the price is defaulted after applying any conversion, if necessary.</span></span>  
  
 <span data-ttu-id="9de97-117">Nếu không có một mức giá cho vai trò thì giá vốn được đặt mặc định thành 0,00 trên dòng ước tính.</span><span class="sxs-lookup"><span data-stu-id="9de97-117">If there isn’t a price for the role, then the cost price defaults to 0.00 on the estimate line.</span></span>  
  
 <span data-ttu-id="9de97-118">Tất cả số tiền chi phí trên dòng ước tính chi phí dự án sẽ theo đơn vị tiền tệ của đơn vị tổ chức sở hữu.</span><span class="sxs-lookup"><span data-stu-id="9de97-118">All cost amounts on project cost estimate lines are in the currency of the owning organizational unit.</span></span>  
  
## <a name="sales-price-defaulting"></a><span data-ttu-id="9de97-119">Đặt mặc định giá bán</span><span class="sxs-lookup"><span data-stu-id="9de97-119">Sales price defaulting</span></span>  
<span data-ttu-id="9de97-120">Biểu giá bán sẽ dựa vào thực thể bán mà dự án được gán đến.</span><span class="sxs-lookup"><span data-stu-id="9de97-120">The sales price list is based on the sales entity that the project is attached to.</span></span> <span data-ttu-id="9de97-121">Biểu giá bán được liên kết với báo giá hoặc hợp đồng sẽ xác định đơn giá bán.</span><span class="sxs-lookup"><span data-stu-id="9de97-121">The sales price list associated with the quote or contract determines the unit sales price.</span></span> <span data-ttu-id="9de97-122">Nếu báo giá hoặc hợp đồng có biểu giá tùy chỉnh, đấy sẽ là biểu giá bán mặc định cho các ước tính dự án.</span><span class="sxs-lookup"><span data-stu-id="9de97-122">If the quote or contract has a custom price list, it's the default sales price list for project estimates.</span></span> <span data-ttu-id="9de97-123">Nếu không có liên kết với các thực thể bán thì biểu giá bán mặc định được định cấu hình trong cài đặt tham số sẽ là biểu giá bán mặc định cho dự án.</span><span class="sxs-lookup"><span data-stu-id="9de97-123">If there is no association to the sales entities, then the default sales price list configured in parameters settings will be the default sales price list for the project.</span></span> <span data-ttu-id="9de97-124">Mỗi dòng ước tính được liên kết với một đơn vị tổ chức nguồn tài nguyên để chỉ ra đơn vị tổ chức nơi sẽ đặt nguồn tài nguyên để hoàn tất nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="9de97-124">Each estimate line has a resource organizational unit associated to indicate the organizational unit from which the resources will be booked for completing the task.</span></span> <span data-ttu-id="9de97-125">Giá bán cho các vai trò được liên kết được xác định bằng cách tìm kiếm các cách kết hợp giữa vai trò, đơn vị và thiết bị tổ chức nguồn tài nguyên trong biểu giá bán để nhận đúng giá bán cho ngày có hiệu lực trên dòng ước tính.</span><span class="sxs-lookup"><span data-stu-id="9de97-125">The sales price for the associated roles is determined by searching for the combination of role, unit, and resource organizational unit in the sales price list to get the correct sales price for the date effective on the estimate lines.</span></span>  
  
<span data-ttu-id="9de97-126">Nếu sự kết hợp giữa vai trò, đơn vị và đơn vị tổ chức nguồn tài nguyên không đưa ra một mức giá bán từ biểu giá bán, hệ thống sẽ bỏ qua đơn vị và tìm kiếm sự kết hợp giữa vai trò và đơn vị tổ chức nguồn tài nguyên.</span><span class="sxs-lookup"><span data-stu-id="9de97-126">If the combination of role, unit, and resource organizational unit doesn’t result in a sales price from the sales price list, the system will disregard unit and search for the combination of role and resource organizational unit.</span></span> <span data-ttu-id="9de97-127">Nếu thấy giá bán, giá này sẽ được chuyển đổi sang đơn vị bạn đã chọn trên dòng ước tính bán hàng.</span><span class="sxs-lookup"><span data-stu-id="9de97-127">If a sales price is found, it's converted to the unit you chose on the sales estimate line.</span></span>  
  
<span data-ttu-id="9de97-128">Nếu hệ thống không tìm thấy giá cho vai trò thì giá bán phải được đặt mặc định thành 0,00 trên dòng ước tính.</span><span class="sxs-lookup"><span data-stu-id="9de97-128">If the system doesn’t find a price for the role, then the sales price must default to 0.00 on the estimate line.</span></span>  
  
<span data-ttu-id="9de97-129">Dạng xem ước tính có dạng xem lưới hiển thị lưới đồng đều gồm các dòng ước tính có đơn vị, tổng chi phí và giá bán.</span><span class="sxs-lookup"><span data-stu-id="9de97-129">The estimates view has a grid view that displays a flat grid of estimate lines with unit and total cost and sales price.</span></span>  
  
## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="9de97-130">Dạng xem theo giai đoạn thời gian cho ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="9de97-130">Time-phased view of project estimates</span></span>  
<span data-ttu-id="9de97-131">Trong dạng xem theo giai đoạn thời gian cho ước tính dự án, dữ liệu ước tính từ dạng xem lưới được xoay theo mặc định theo vai trò và hiển thị bảng tính của các dữ liệu ước tính trên dòng thời gian trong tỷ lệ thời gian đã chọn.</span><span class="sxs-lookup"><span data-stu-id="9de97-131">In the time-phased view for project estimates, the estimates data from the grid view is pivoted by default by role, and shows a spread of estimate data across the timeline in the chosen timescale.</span></span>  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a><span data-ttu-id="9de97-132">Phân bổ ước tính nỗ lực dựa trên chế độ nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="9de97-132">Effort estimate allocation based on task mode</span></span>  
<span data-ttu-id="9de97-133">Trong dạng xem theo giai đoạn thời gian, toàn bộ nỗ lực được ước tính cho nhiệm vụ được phân phối bằng cách phân bổ số giờ cố gắng cụ thể cho mỗi khoảng thời gian đơn vị của tỷ lệ thời gian đã chọn.</span><span class="sxs-lookup"><span data-stu-id="9de97-133">In the time-phased view, total effort estimated for the task is distributed by allocating a certain number of effort hours per unit time period of the chosen timescale.</span></span> <span data-ttu-id="9de97-134">Trong Project Service, chế độ nhiệm vụ xác định cách thức phân bổ nỗ lực trên khoảng thời gian của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="9de97-134">In project service, the task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="9de97-135">Hai loại phân bổ là phân bổ đều và phân bổ dựa trên giờ làm việc.</span><span class="sxs-lookup"><span data-stu-id="9de97-135">The two kinds of allocation are even allocation and work hours-based allocation.</span></span> 
  
## <a name="work-hours-based-allocation"></a><span data-ttu-id="9de97-136">Phân bổ dựa trên giờ làm việc</span><span class="sxs-lookup"><span data-stu-id="9de97-136">Work hours-based allocation</span></span>  
<span data-ttu-id="9de97-137">Chế độ Tự động lên lịch nhiệm vụ với một nhiệm vi chi phối số lượng tài nguyên được dự tính trên nhiệm vụ, chúng được ước tính để được tận dụng cho toàn bộ số giờ làm việc mỗi ngày.</span><span class="sxs-lookup"><span data-stu-id="9de97-137">Auto scheduling task mode for a task governs that for the number of resources estimated on the task, they are estimated to be utilized for the full work hours per day.</span></span> <span data-ttu-id="9de97-138">Chế độ này sẽ áp dụng khi phân bổ nỗ lực bằng cách phân chia trên khoảng thời gian của nhiệm vụ trong dạng xem dựa trên giai đoạn thời gian.</span><span class="sxs-lookup"><span data-stu-id="9de97-138">This applies when allocating the effort by splitting it across the duration of tasks in the time phased view as well.</span></span> <span data-ttu-id="9de97-139">Ví dụ: trên một tỷ lệ thời gian 'Ngày', với một nhiệm vụ được ước tính cần hoàn tất bởi một tài nguyên, nhân công được phân bổ mỗi ngày sẽ không vượt quá số giờ làm việc mỗi ngày được xác định trong lịch của dự án.</span><span class="sxs-lookup"><span data-stu-id="9de97-139">For instance, on a ‘Day’ timescale, for a task estimated to be completed by one resource, the effort allocated per day will not exceed work hours per day defined in the project’s calendar.</span></span> <span data-ttu-id="9de97-140">Vì vậy, việc phân bổ nỗ lực luôn đảm bảo rằng các nguồn lực được ước tính để tận dụng cho cả ngày.</span><span class="sxs-lookup"><span data-stu-id="9de97-140">Therefore, the effort allocation always ensures that the resources are estimated to be utilized for the full day.</span></span>  
  
## <a name="even-distribution"></a><span data-ttu-id="9de97-141">Phân phối đều</span><span class="sxs-lookup"><span data-stu-id="9de97-141">Even distribution</span></span>  
<span data-ttu-id="9de97-142">Chế độ nhiệm vụ được lên lịch theo cách thủ công không tuân theo giờ làm việc, lịch dự án hay số nguồn lực được xác định cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="9de97-142">Manually scheduled task mode doesn't honor the work hours, project calendar, or number of resources defined on the task.</span></span> <span data-ttu-id="9de97-143">Lịch nhiệm vụ dựa trên mục nhập của người sử dụng.</span><span class="sxs-lookup"><span data-stu-id="9de97-143">The task schedule is based on user input.</span></span> <span data-ttu-id="9de97-144">Với các nhiệm vụ như vậy, phân bổ nỗ lực cho mỗi khoảng thời gian đơn vị cho tỷ lệ đã chọn không có bất kỳ yếu tố hạn chế nào.</span><span class="sxs-lookup"><span data-stu-id="9de97-144">For such tasks, the effort allocation per unit time period of the chosen timescale doesn't have any limiting factors.</span></span> <span data-ttu-id="9de97-145">Tổng nỗ lực trên một nhiệm vụ được chia và phân bổ đều cho mỗi khoảng thời gian đơn vị trên tỷ lệ thời gian đã chọn.</span><span class="sxs-lookup"><span data-stu-id="9de97-145">The total effort on the task is equally split and allocated for each unit time period on the chosen timescale.</span></span>  
  
<span data-ttu-id="9de97-146">Bằng cách này, chế độ nhiệm vụ được xác định cho nhiệm vụ sẽ xác định cách phân phối hoặc phân bổ nỗ lực trên mỗi khoảng thời gian đơn vị trong ước tính theo giai đoạn thời gian.</span><span class="sxs-lookup"><span data-stu-id="9de97-146">In this way, the task mode defined on the task determines the effort distribution or allocation of effort per unit time period in time-phased estimates.</span></span>  
  
## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="9de97-147">Tùy chọn theo giai đoạn thời gian và phân nhóm</span><span class="sxs-lookup"><span data-stu-id="9de97-147">Grouping and time-phasing options</span></span>  
<span data-ttu-id="9de97-148">Dạng xem này giúp bạn hiểu về cách phân phối nỗ lực, chi phí và ước tính bán hàn trên cơ sở mỗi ngày, mỗi tuần, mỗi tháng hoặc mỗi năm.</span><span class="sxs-lookup"><span data-stu-id="9de97-148">This view helps you understand the distribution of the effort, cost, and sales estimates on a per day, week, month, or year basis.</span></span> <span data-ttu-id="9de97-149">Tùy chọn Nhóm theo cho phép thay đổi dữ liệu ước tính dựa trên hai thứ nguyên khác: danh mục và tài nguyên.</span><span class="sxs-lookup"><span data-stu-id="9de97-149">The Group By option allows pivoting the estimates data on two other dimensions: category and resource.</span></span> <span data-ttu-id="9de97-150">Trên cả dạng xem lưới và dạng xem theo giai đoạn thời gian, bạn đều có thể chọn các trường cần được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="9de97-150">On both the grid view and the time-phased view you can choose the fields to be displayed.</span></span> <span data-ttu-id="9de97-151">Tổng số cho mỗi khối thời gian được hiển thị ở dưới cùng cho biết tổng số nhân công, chi phí và doanh số ước tính cho ngày, tuần, tháng hoặc năm.</span><span class="sxs-lookup"><span data-stu-id="9de97-151">Totals for each of the time blocks are displayed at the bottom indicating the total estimated effort, cost, and sales for the day, week, month, or year.</span></span>  
  
<span data-ttu-id="9de97-152">Giá vốn và giá bán hàng mặc định có hiệu lực theo ngày.</span><span class="sxs-lookup"><span data-stu-id="9de97-152">The cost and sales price default is date effective.</span></span> <span data-ttu-id="9de97-153">Khi tỷ lệ cho các vai trò thay đổi, dạng xem theo giai đoạn thời gian sẽ rõ ràng hơn khi xem dữ liệu ước tính được thay đổi theo ‘Tài nguyên’ và theo giai đoạn thời gian theo tuần.</span><span class="sxs-lookup"><span data-stu-id="9de97-153">When the rates for the roles change, it will be more transparent in the time-phased view when viewing estimate data pivoted on ‘Resource’ and time-phased by week.</span></span>  
  
## <a name="expense-estimates"></a><span data-ttu-id="9de97-154">Ước tính chi phí</span><span class="sxs-lookup"><span data-stu-id="9de97-154">Expense estimates</span></span>  
<span data-ttu-id="9de97-155">Bất kỳ chi phí nào phát sinh trong dự án mà không trực tiếp liên quan đến lao động được sử dụng có thể được ghi lại trong ước tính dự án ở dạng xem lưới.</span><span class="sxs-lookup"><span data-stu-id="9de97-155">Any expense that will be incurred in the project that is not directly related to labor to be expended can be recorded in the project estimates in the grid view.</span></span> <span data-ttu-id="9de97-156">Sử dụng tùy chọn **Thêm ước tính chi phí** trong dạng xem lưới, bạn có thể hoàn thành tác vụ này.</span><span class="sxs-lookup"><span data-stu-id="9de97-156">Using the **Add expense estimate** option in the grid view, you can accomplish this.</span></span> <span data-ttu-id="9de97-157">Có thể ghi lại các ước tính chi phí cho một nhiệm vụ cụ thể hoặc cho toàn bộ dự án.</span><span class="sxs-lookup"><span data-stu-id="9de97-157">The expense estimates can be recorded for a specific task or for the entire project.</span></span> <span data-ttu-id="9de97-158">Bạn có thể chọn loại chi phí trên những dòng này và chọn ngày dự kiến phát sinh chi phí dự kiến.</span><span class="sxs-lookup"><span data-stu-id="9de97-158">You can choose expense categories on these lines and choose a tentative date when the expense is expected to be incurred.</span></span> <span data-ttu-id="9de97-159">Nếu biểu giá bán và giá vốn được liên kết có giá mặc định hoặc tỷ lệ đánh dấu được xác định cho danh mục chi phí, giá đó sẽ được đặt mặc định trên dòng ước tính khi liên kết.</span><span class="sxs-lookup"><span data-stu-id="9de97-159">If the associated cost and sales price list have default prices, or markup percentages defined for expense categories, it will be defaulted on the estimate line on association.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9de97-160">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9de97-160">See Also</span></span>  
 [<span data-ttu-id="9de97-161">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="9de97-161">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]