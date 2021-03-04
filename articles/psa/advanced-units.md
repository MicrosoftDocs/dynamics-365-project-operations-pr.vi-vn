---
title: Nhóm đơn vị và đơn vị
description: Chủ đề này cung cấp thông tin về nhóm đơn vị đo và đơn vị đo.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145609"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="aa96e-103">Nhóm đơn vị và đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aa96e-104">Nhóm đơn vị đo và đơn vị đo là các thực thể cơ bản trong Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aa96e-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="aa96e-105">Một đơn vị là một đơn vị đo lường và nhiều đơn vị đo có thể nhóm thành nhóm đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="aa96e-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="aa96e-106">Nhóm đơn vị đôi khi được gọi là lịch đơn vị trong giao diện người dùng (UI) Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aa96e-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="aa96e-107">Dưới đây là một số ví dụ về các đơn vị và nhóm đơn vị đo:</span><span class="sxs-lookup"><span data-stu-id="aa96e-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="aa96e-108">**Nhóm đơn vị đo**: Khoảng cách</span><span class="sxs-lookup"><span data-stu-id="aa96e-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="aa96e-109">**Đơn vị**: Dặm, Km, v.v.</span><span class="sxs-lookup"><span data-stu-id="aa96e-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="aa96e-110">**Nhóm đơn vị đo**: Thời gian</span><span class="sxs-lookup"><span data-stu-id="aa96e-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="aa96e-111">**Đơn vị**: Giờ, ngày, tuần, v.v.</span><span class="sxs-lookup"><span data-stu-id="aa96e-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="aa96e-112">Khi bạn thiết lập nhiều đơn vị trong một nhóm đơn vị, bạn cũng phải thiết lập một hệ số chuyển đổi giữa chúng bằng cách chỉ định đơn vị đầu tiên mà bạn thiết lập làm đơn vị chính hoặc mặc định cho nhóm đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="aa96e-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="aa96e-113">Ví dụ: trong nhóm đơn vị đo **Thời gian**, nếu bạn thiết lập **Giờ** làm đơn vị đầu tiên, thì hệ thống sẽ chỉ định **Giờ** là đơn vị mặc định.</span><span class="sxs-lookup"><span data-stu-id="aa96e-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="aa96e-114">Nếu đơn vị tiếp theo mà bạn thiết lập là **Ngày**, thì bạn phải thiết lập một hệ số chuyển đổi cho **Ngày** thành **Giờ**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="aa96e-115">Nếu sau đó bạn thêm **Tuần** làm đơn vị thứ ba, thì bạn phải thiết lập một hệ số chuyển đổi cho **Tuần** theo **Ngày** hoặc **Giờ**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="aa96e-116">Hình ảnh sau đây minh họa một thiết lập ví dụ cho đơn vị **Ngày**, trong đó trường **Số lượng** hiển thị số giờ trong một ngày và **Tuần**, trong đó trường **Số lượng** hiển thị số ngày trong một tuần.</span><span class="sxs-lookup"><span data-stu-id="aa96e-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Nhóm đơn vị đo: Trang thông tin](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="aa96e-118">Sử dụng đơn vị và nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="aa96e-118">Using units and unit groups</span></span>

<span data-ttu-id="aa96e-119">Dynamics 365 Project Service Automation sử dụng các đơn vị và nhóm đơn vị để xử lý các ước tính và mục nhập cho cả chi phí và thời gian.</span><span class="sxs-lookup"><span data-stu-id="aa96e-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="aa96e-120">Đối với chi phí, mỗi loại chi phí có nhóm đơn vị và đơn vị mặc định.</span><span class="sxs-lookup"><span data-stu-id="aa96e-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="aa96e-121">Các giá trị này được nhập như giá trị mặc định trên mục nhập bảng giá cho loại chi phí.</span><span class="sxs-lookup"><span data-stu-id="aa96e-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="aa96e-122">Ví dụ: bạn có một loại chi phí có tên **Quãng đường**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="aa96e-123">Nó có một nhóm đơn vị có tên là **Khoảng cách** và một đơn vị mặc định là **Dặm**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="aa96e-124">Nếu bạn thiết lập nhóm đơn vị đo **Khoảng cách** để nó có hai đơn vị (**Dặm** và **Km**), bạn có thể đặt hai giá cho danh mục **Quãng đường** trên một bảng giá: giá mỗi dặm và giá mỗi km.</span><span class="sxs-lookup"><span data-stu-id="aa96e-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="aa96e-125">Thể loại chi phí</span><span class="sxs-lookup"><span data-stu-id="aa96e-125">Expense category</span></span>  | <span data-ttu-id="aa96e-126">Nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="aa96e-126">Unit group</span></span>  | <span data-ttu-id="aa96e-127">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-127">Unit</span></span>      | <span data-ttu-id="aa96e-128">Phương pháp định giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-128">Pricing method</span></span>  | <span data-ttu-id="aa96e-129">Đơn giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="aa96e-130">Số dặm</span><span class="sxs-lookup"><span data-stu-id="aa96e-130">Mileage</span></span>           | <span data-ttu-id="aa96e-131">Khoảng cách</span><span class="sxs-lookup"><span data-stu-id="aa96e-131">Distance</span></span>      | <span data-ttu-id="aa96e-132">Dặm</span><span class="sxs-lookup"><span data-stu-id="aa96e-132">Mile</span></span>      | <span data-ttu-id="aa96e-133">Đơn giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-133">Price per unit</span></span>    | <span data-ttu-id="aa96e-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="aa96e-134">10 USD</span></span>            |
| <span data-ttu-id="aa96e-135">Số dặm</span><span class="sxs-lookup"><span data-stu-id="aa96e-135">Mileage</span></span>           | <span data-ttu-id="aa96e-136">Khoảng cách</span><span class="sxs-lookup"><span data-stu-id="aa96e-136">Distance</span></span>      | <span data-ttu-id="aa96e-137">Kilômét</span><span class="sxs-lookup"><span data-stu-id="aa96e-137">Kilometer</span></span> | <span data-ttu-id="aa96e-138">Đơn giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-138">Price per unit</span></span>    |  <span data-ttu-id="aa96e-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="aa96e-139">6 USD</span></span>            |

<span data-ttu-id="aa96e-140">Khi bạn nhập một chi phí vào dự án, hệ thống sẽ xác định giá thông qua tổ hợp các thể loại và đơn vị trên chi phí.</span><span class="sxs-lookup"><span data-stu-id="aa96e-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="aa96e-141">Mô tả chi phí</span><span class="sxs-lookup"><span data-stu-id="aa96e-141">Expense description</span></span>        | <span data-ttu-id="aa96e-142">Thể loại chi phí</span><span class="sxs-lookup"><span data-stu-id="aa96e-142">Expense category</span></span>  | <span data-ttu-id="aa96e-143">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-143">Unit</span></span>  | <span data-ttu-id="aa96e-144">Số lượng</span><span class="sxs-lookup"><span data-stu-id="aa96e-144">Quantity</span></span>  | <span data-ttu-id="aa96e-145">Đơn giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="aa96e-146">Lái xe đến vị trí khách hàng</span><span class="sxs-lookup"><span data-stu-id="aa96e-146">Drive to client location</span></span> | <span data-ttu-id="aa96e-147">Số dặm</span><span class="sxs-lookup"><span data-stu-id="aa96e-147">Mileage</span></span>             | <span data-ttu-id="aa96e-148">Dặm</span><span class="sxs-lookup"><span data-stu-id="aa96e-148">Mile</span></span>  | <span data-ttu-id="aa96e-149">10</span><span class="sxs-lookup"><span data-stu-id="aa96e-149">10</span></span>        | <span data-ttu-id="aa96e-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="aa96e-150">10 USD</span></span>         |

<span data-ttu-id="aa96e-151">Đối với thời gian, mỗi tiêu đề bảng giá đều có trường **Đơn vị thời gian mặc định**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="aa96e-152">Giá trị được đặt khi bạn tạo tiêu đề bảng giá.</span><span class="sxs-lookup"><span data-stu-id="aa96e-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="aa96e-153">Sau đó, đơn vị này được sử dụng để thiết lập tất cả các giá dựa trên vai trò trên bảng giá đó.</span><span class="sxs-lookup"><span data-stu-id="aa96e-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="aa96e-154">Các dòng ước tính cho trường **Thời gian trên báo giá** có thể được thể hiện ở bất kỳ đơn vị thời gian nào.</span><span class="sxs-lookup"><span data-stu-id="aa96e-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="aa96e-155">Tuy nhiên, dòng ước tính trên dự án và mục nhập thời gian cho dự án chỉ có thể sử dụng đơn vị thời gian là **Giờ**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="aa96e-156">Nếu đơn vị trên mục nhập thời gian hoặc dòng ước tính không khớp với đơn vị trên dòng bảng giá cho vai trò đó, thì hệ thống sẽ chuyển đổi giá sang đơn vị được xác định trên ước tính dự án hoặc giao dịch thực tế của dự án.</span><span class="sxs-lookup"><span data-stu-id="aa96e-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="aa96e-157">Ví dụ sau cho thấy cách PSA sử dụng nhóm đơn vị đo, đơn vị và hệ số chuyển đổi.</span><span class="sxs-lookup"><span data-stu-id="aa96e-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="aa96e-158">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-158">Units</span></span>

   - <span data-ttu-id="aa96e-159">**Nhóm đơn vị đo**: Thời gian</span><span class="sxs-lookup"><span data-stu-id="aa96e-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="aa96e-160">**Đơn vị**: Giờ</span><span class="sxs-lookup"><span data-stu-id="aa96e-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="aa96e-161">**Ngày** - Hệ số chuyển đổi: 8 giờ</span><span class="sxs-lookup"><span data-stu-id="aa96e-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="aa96e-162">**Tuần** - Hệ số chuyển đổi: 40 giờ</span><span class="sxs-lookup"><span data-stu-id="aa96e-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="aa96e-163">Thiết lập bảng giá trên dự án A:</span><span class="sxs-lookup"><span data-stu-id="aa96e-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="aa96e-164">**Tên**: Giá bán hàng ở Anh năm 2016</span><span class="sxs-lookup"><span data-stu-id="aa96e-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="aa96e-165">**Đơn vị thời gian mặc định**: Ngày</span><span class="sxs-lookup"><span data-stu-id="aa96e-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="aa96e-166">**Tiền tệ**: GBP</span><span class="sxs-lookup"><span data-stu-id="aa96e-166">**Currency**: GBP</span></span>

| <span data-ttu-id="aa96e-167">Vai trò</span><span class="sxs-lookup"><span data-stu-id="aa96e-167">Role</span></span>      | <span data-ttu-id="aa96e-168">Nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="aa96e-168">Unit group</span></span> | <span data-ttu-id="aa96e-169">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-169">Unit</span></span> | <span data-ttu-id="aa96e-170">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="aa96e-170">Organizational unit</span></span> | <span data-ttu-id="aa96e-171">Giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="aa96e-172">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="aa96e-172">Developer</span></span> | <span data-ttu-id="aa96e-173">Time</span><span class="sxs-lookup"><span data-stu-id="aa96e-173">Time</span></span>       | <span data-ttu-id="aa96e-174">Day</span><span class="sxs-lookup"><span data-stu-id="aa96e-174">Day</span></span>  | <span data-ttu-id="aa96e-175">Contoso Hoa Kỳ</span><span class="sxs-lookup"><span data-stu-id="aa96e-175">Contoso UK</span></span>          | <span data-ttu-id="aa96e-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="aa96e-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="aa96e-177">Mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="aa96e-177">Time entry</span></span>

<span data-ttu-id="aa96e-178">Bảng sau hiển thị các giao dịch phía bán hàng tạo ra bởi PSA cho một dự án ba giờ.</span><span class="sxs-lookup"><span data-stu-id="aa96e-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="aa96e-179">Dự án</span><span class="sxs-lookup"><span data-stu-id="aa96e-179">Project</span></span>   | <span data-ttu-id="aa96e-180">Nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="aa96e-180">Task</span></span>    | <span data-ttu-id="aa96e-181">Vai trò</span><span class="sxs-lookup"><span data-stu-id="aa96e-181">Role</span></span>      | <span data-ttu-id="aa96e-182">Số lượng</span><span class="sxs-lookup"><span data-stu-id="aa96e-182">Quantity</span></span> | <span data-ttu-id="aa96e-183">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="aa96e-183">Unit</span></span>  | <span data-ttu-id="aa96e-184">Đơn giá</span><span class="sxs-lookup"><span data-stu-id="aa96e-184">Unit price</span></span> | <span data-ttu-id="aa96e-185">Số tiền bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="aa96e-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="aa96e-186">Dự án A</span><span class="sxs-lookup"><span data-stu-id="aa96e-186">Project A</span></span> | <span data-ttu-id="aa96e-187">Thiết kế</span><span class="sxs-lookup"><span data-stu-id="aa96e-187">Design</span></span>  | <span data-ttu-id="aa96e-188">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="aa96e-188">Developer</span></span> | <span data-ttu-id="aa96e-189">3</span><span class="sxs-lookup"><span data-stu-id="aa96e-189">3</span></span>        | <span data-ttu-id="aa96e-190">Hour</span><span class="sxs-lookup"><span data-stu-id="aa96e-190">Hour</span></span>  | <span data-ttu-id="aa96e-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="aa96e-191">100 GBP</span></span>    | <span data-ttu-id="aa96e-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="aa96e-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="aa96e-193">Câu hỏi thường gặp về đơn vị thời gian</span><span class="sxs-lookup"><span data-stu-id="aa96e-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="aa96e-194">PSA có chuyển đổi sang các đơn vị khác trong trường hợp chi phí không?</span><span class="sxs-lookup"><span data-stu-id="aa96e-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="aa96e-195">Không.</span><span class="sxs-lookup"><span data-stu-id="aa96e-195">No.</span></span> <span data-ttu-id="aa96e-196">Chuyển đổi đơn vị chỉ hoạt động cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="aa96e-196">Unit conversion works only for time.</span></span> <span data-ttu-id="aa96e-197">Đối với chi phí, nếu hệ thống không thể tìm thấy giá cho tổ hợp loại chi phí và đơn vị, thì giá sẽ được đặt thành 0,00 theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="aa96e-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="aa96e-198">Tại sao PSA chuyển đổi đơn vị thời gian?</span><span class="sxs-lookup"><span data-stu-id="aa96e-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="aa96e-199">Ở một số quốc gia hoặc khu vực, có một yêu cầu pháp lý rằng tỉ suất hóa đơn được thiết lập theo ngày.</span><span class="sxs-lookup"><span data-stu-id="aa96e-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="aa96e-200">Đám phán giá và giảm giá trong chu kỳ báo giá được thực hiện bằng cách sử dụng tỉ suất ngày cho mỗi vai trò có thể lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="aa96e-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="aa96e-201">Ước tính lịch trình và mục nhập thời gian được thực hiện theo giờ.</span><span class="sxs-lookup"><span data-stu-id="aa96e-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="aa96e-202">Để hỗ trợ sự khác biệt này theo đơn vị thời gian, PSA sẽ quy đổi đơn vị thời gian.</span><span class="sxs-lookup"><span data-stu-id="aa96e-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="aa96e-203">Có thể thay đổi đơn vị thời gian trên ước tính dự án không?</span><span class="sxs-lookup"><span data-stu-id="aa96e-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="aa96e-204">Không.</span><span class="sxs-lookup"><span data-stu-id="aa96e-204">No.</span></span> <span data-ttu-id="aa96e-205">Ước tính lịch trình hiện bị giới hạn ở giờ và không thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="aa96e-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="aa96e-206">Có thể chỉnh sửa, xóa và thêm đơn vị cũng như nhóm đơn vị đo không?</span><span class="sxs-lookup"><span data-stu-id="aa96e-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="aa96e-207">Có chứ.</span><span class="sxs-lookup"><span data-stu-id="aa96e-207">Yes.</span></span> <span data-ttu-id="aa96e-208">Trừ trường hợp nhóm đơn vị đo **Thời gian** và đơn vị **Giờ**, có thể xóa hoặc chỉnh sửa tất cả các đơn vị, đồng thời có thể thêm đơn vị mới.</span><span class="sxs-lookup"><span data-stu-id="aa96e-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="aa96e-209">Trong PSA, không thể xóa nhóm đơn vị đo **Thời gian** và đơn vị **Giờ**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="aa96e-210">Tuy nhiên, có thể cập nhật các đơn vị này bằng một văn bản đã dịch cho trường **Tên**.</span><span class="sxs-lookup"><span data-stu-id="aa96e-210">However, they can be updated with a translated text for the **Name** field.</span></span>
