---
title: Thêm các trường tùy chỉnh vào thực thể thiết lập giá và thực thể giao dịch
description: Chủ đề này cung cấp thông tin về việc thêm các trường tùy chỉnh cho các thực thể giao dịch và thiết lập giá.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e1a8d6319788ee73e0e2837a47cba89108c32572
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275339"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a><span data-ttu-id="5fe5c-103">Thêm các trường tùy chỉnh vào thực thể thiết lập giá và thực thể giao dịch</span><span class="sxs-lookup"><span data-stu-id="5fe5c-103">Add custom fields to price setup and transactional entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5fe5c-104">Chủ đề này giả định rằng bạn đã hoàn tất các quy trình trong chủ đề [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="5fe5c-104">This topic assumes that you have completed the procedures in the topic, [Create custom fields and entities](create-custom-fields-entities.md).</span></span> <span data-ttu-id="5fe5c-105">Nếu bạn chưa hoàn thành các quy trình đó, hãy quay lại và hoàn thành chúng rồi trở lại chủ đề này.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="5fe5c-106">Trong chủ đề này, các quy trình sẽ hiển thị cho bạn cách thêm tham chiếu trường tùy chỉnh bắt buộc vào các thực thể và vào các thành phần giao diện người dùng (UI) như biểu mẫu và dạng xem.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-106">In this topic, the procedures will show you how to add the required custom field references to entities and to the user interface (UI) elements such as forms and views.</span></span>

## <a name="add-custom-pricing-dimension-fields"></a><span data-ttu-id="5fe5c-107">Thêm các trường kích thước giá tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="5fe5c-107">Add custom pricing dimension fields</span></span> 
<span data-ttu-id="5fe5c-108">Sau khi các trường và thực thể tùy chỉnh được tạo, bước tiếp theo là thiết lập giá và thực thể giao dịch với sự cân nhắc đến bất kỳ thực thể tùy chỉnh hay bộ tùy chọn nào bằng cách tạo các trường tham chiếu.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-108">After custom fields and entities have been created, the next step is to make price setup and transactional entities aware of any custom entities or option sets by creating reference fields.</span></span> <span data-ttu-id="5fe5c-109">Tùy thuộc vào việc danh sách kích thước giá bao gồm các kích thước của bộ tùy chỉnh hay kích thước thực thể hay cả hai, chỉ làm theo các bước trong **Kích thước giá tùy chỉnh dựa trên bộ tùy chọn** hoặc **Kích thước giá tùy chỉnh dựa trên thực thể** hoặc cả hai.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-109">Depending on whether your pricing dimensions list includes option set dimensions or entity dimensions or both, follow only the steps in **Option set-based custom pricing dimensions** or **Entity-based custom pricing dimensions**, or both, respectively.</span></span>

### <a name="option-set-based-custom-pricing-dimensions"></a><span data-ttu-id="5fe5c-110">Kích thước giá tùy chỉnh dựa trên bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="5fe5c-110">Option set-based custom pricing dimensions</span></span>
<span data-ttu-id="5fe5c-111">Khi kích thước giá tùy chỉnh là dựa trên bộ tùy chọn, hãy thêm nó như một trường vào các thực thể Project Service chính.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-111">When a custom pricing dimension is option set-based, add it as a field to key Project Service entities.</span></span> <span data-ttu-id="5fe5c-112">Trong quy trình sau đây, **Vị trí làm việc của nhân lực** và **Số giờ làm việc của nhân lực** được dùng làm kích thước giá dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-112">In the following procedure, **Resource Work Location** and **Resource Work Hours** are used as the option set-based pricing dimensions.</span></span> <span data-ttu-id="5fe5c-113">Trước tiên phải thêm các thành phần này dưới dạng trường vào các thực thể giá, **Giá theo vai trò** và **Tăng giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-113">These must first be added as fields to the pricing entities, **Role Price** and **Role Price Markup**.</span></span>

1. <span data-ttu-id="5fe5c-114">Trong Project Service Automation (PSA), nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-114">In Project Service Automation (PSA), click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5fe5c-115">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-115">In Solution Explorer, on the left navigation pane, select **Entities > Role Price**.</span></span>
3. <span data-ttu-id="5fe5c-116">Mở rộng thực thể **Giá theo vai trò** và chọn **Trường**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-116">Expand the entity **Role Price** and select **Fields**.</span></span>
4. <span data-ttu-id="5fe5c-117">Nhấp vào **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn **Bộ tùy chọn** là loại trường.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-117">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="5fe5c-118">Chọn **Sử dụng bộ tùy chọn hiện có**, chọn bộ tùy chọn **Vị trí làm việc của nhân lực**, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-118">Select **Use an existing Option set**, select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="5fe5c-119">Lặp lại các bước 1-5 để thêm trường này vào thực thể **Tăng giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-119">Repeat steps 1 - 5 to add this field to the **Role Price Markup** entity.</span></span> 
7. <span data-ttu-id="5fe5c-120">Lặp lại bước 1-5 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-120">Repeat steps 1 - 5 for the **Resource Work Hours** option set.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fe5c-121">Khi bạn thêm một trường vào nhiều thực thể, hãy sử dụng cùng một tên trường trên tất cả các tổ chức.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-121">When you add a field to more than one entity, use the same field name across all of the entities.</span></span> 

> ![Thêm vị trí làm việc của nguồn lực vào giá theo vai trò](media/RWL-Field.png)

<span data-ttu-id="5fe5c-123">Trong giai đoạn bán hàng và ước tính cho một dự án, ước tính của nỗ lực công việc cần thiết để hoàn tất công việc **Tại địa phương** và **Tại chỗ**, trong **Giờ làm việc** và **Giờ làm thêm** được dùng để ước tính giá trị của Báo giá/Dự án.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-123">In the sales and estimation phases for a project, estimates of the work effort that is required to complete **Local** and **Onsite** work, in **Regular hours** and **Overtime hours**  are used to estimate the value of the Quote/Project.</span></span> <span data-ttu-id="5fe5c-124">Các trường **Vị trí làm việc của nguồn lực** và **Số giờ làm việc của nguồn lực** sẽ được thêm vào thực thể ước tính, **Chi tiết về dòng báo giá**, **Chi tiết về dòng hợp đồng**, **Nhiệm vụ dự án**, **Thành viên nhóm dự án** và **Dòng ước tính**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-124">The fields **Resource Work Location** and **Resource Work Hours** will be added to the estimation entities, **Quote Line Detail**, **Contract Line detail**, **Project Task**, **Project Team Member**, and **Estimate Line**.</span></span>

1. <span data-ttu-id="5fe5c-125">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-125">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5fe5c-126">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chi tiết dòng báo giá**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-126">In Solution Explorer, on the left navigation pane, select **Entities > Quote Line Detail**.</span></span>
3. <span data-ttu-id="5fe5c-127">Mở rộng thực thể **Chi tiết dòng báo giá**, chọn **Trường**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-127">Expand the **Quote Line Detail** entity, and select **Fields**.</span></span>
4. <span data-ttu-id="5fe5c-128">Nhấp vào **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn loại trường là **Bộ tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-128">Click **New** to create a new field called **Resource Work Location** and select the field type, **Option set**.</span></span> 
5. <span data-ttu-id="5fe5c-129">Chọn **Sử dụng bộ tùy chọn hiện có** và **Vị trí làm việc của nhân lực**, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-129">Select **Use an existing Option set** and **Resource Work Location**, and then click **Save**.</span></span>
6. <span data-ttu-id="5fe5c-130">Lặp lại các bước 1-5 để thêm trường này vào các thực thể **Chi tiết dòng hợp đồng dự án**, **Nhiệm vụ dự án**, **Thành viên nhóm dự án** và **Dòng ước tính**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-130">Repeat steps 1 - 5 to add this field to the **Project Contract line detail**,**Project Task**, **Project Team Member**, and **Estimate Line** entities.</span></span>
7. <span data-ttu-id="5fe5c-131">Lặp lại bước 1-6 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-131">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Thêm vị trí làm việc của nguồn lực vào dòng ước tính](media/RWL-Default-Value.png)


<span data-ttu-id="5fe5c-133">Đối với giao hàng và lập hóa đơn, công việc đã hoàn thành phải có giá chính xác để chọn liệu công việc đó được thực hiện **Tại địa phương** hay **Tại chỗ** và liệu công việc được thực hiện trong **Giờ làm việc** hay **Ngoài giờ làm việc** trên Thực tế dự án.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-133">For delivery and invoicing, completed work needs to be accurately priced to select whether it was performed **Local** or **Onsite**, and whether it was completed during **Regular hours** or **Overtime** on the Project Actuals.</span></span> <span data-ttu-id="5fe5c-134">Các trường **Vị trí làm việc của nguồn lực** và **Số giờ làm việc của nguồn lực** phải được thêm vào **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-134">The **Resource Work Location** and **Resource Work hours** fields should be added to the **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line** entities.</span></span>

1. <span data-ttu-id="5fe5c-135">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-135">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="5fe5c-136">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-136">In Solution Explorer, on the left navigation pane, select  **Entities > Time Entry**.</span></span>
3. <span data-ttu-id="5fe5c-137">Mở rộng thực thể **Chi tiết dòng báo giá**, sau đó chọn **Trường**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-137">Expand the **Quote Line Detail** entity, and then select **Fields**.</span></span>
4. <span data-ttu-id="5fe5c-138">Nhấp vào **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn **Bộ tùy chọn** là loại trường.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-138">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="5fe5c-139">Chọn **Sử dụng bộ tùy chọn hiện có**, chọn bộ tùy chọn **Vị trí làm việc của nhân lực**, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-139">Select **Use an existing Option set**, select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="5fe5c-140">Lặp lại bước 1-5 để thêm trường này vào các thực thể **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-140">Repeat steps 1 - 5 to add this field to the **Actual**, **Invoice Line Detail**, and **Journal Line** entities.</span></span>
7. <span data-ttu-id="5fe5c-141">Lặp lại bước 1-6 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-141">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Thêm vị trí làm việc của nguồn lực vào mục nhập thời gian](media/RWL-time-entry.png)

<span data-ttu-id="5fe5c-143">Thao tác này sẽ hoàn tất các thay đổi với giản đồ cần thiết cho các kích thước tùy chỉnh dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-143">This completes the schema changes required for option set-based custom dimensions.</span></span>

## <a name="entity-based-custom-pricing-dimensions"></a><span data-ttu-id="5fe5c-144">Kích thước giá tùy chỉnh dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="5fe5c-144">Entity-based custom pricing dimensions</span></span>

<span data-ttu-id="5fe5c-145">Khi kích thước giá tùy chỉnh là một thực thể, bạn sẽ thêm mối quan hệ 1:N giữa thực thể kích thước và thực thể Project Service chính.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-145">When the custom pricing dimension is an entity, you will add 1:N relationships between the dimension entity and key Project Service entities.</span></span> <span data-ttu-id="5fe5c-146">Sử dụng ví dụ Chức vụ tiêu chuẩn ở trên, có thể kỳ vọng rằng mỗi nhân viên sẽ được chỉ định một chức vụ tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-146">Using the Standard Title example from above, it is reasonable to expect that each employee is assigned a standard title.</span></span> <span data-ttu-id="5fe5c-147">Kết quả là bạn sẽ cần một mối quan hệ 1: N từ chức vụ tiêu chuẩn để có thể đặt lịch tài nguyên hoặc mối quan hệ N:1 nếu nó được tạo từ tài nguyên có thể đặt lịch thành chức vụ tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-147">SAs a result, you will need a 1:N relationship from Standard Title to Bookable Resource, or a N:1 relationship if it were created from Bookable Resource to Standard Title.</span></span>

1. <span data-ttu-id="5fe5c-148">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-148">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5fe5c-149">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-149">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
3. <span data-ttu-id="5fe5c-150">Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-150">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
4. <span data-ttu-id="5fe5c-151">Nhấp vào **Mới** để tạo mối quan hệ 1:N mới gọi là **Chức vụ tiêu chuẩn cho nguồn lực có thể đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-151">Click **New** to create a new 1:N relationship called **Standard Title to Bookable Resource**.</span></span> <span data-ttu-id="5fe5c-152">Nhập các thông tin cần thiết, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-152">Enter the required information, and then click **Save**.</span></span>

> ![Thêm chức vụ tiêu chuẩn làm trường tham chiếu vào tài nguyên có thể đặt lịch](media/ST-BR.png)

<span data-ttu-id="5fe5c-154">Bạn cũng cần thêm Chức vụ tiêu chuẩn vào các thực thể Giá Project Service, **Giá theo vai trò** và **Tăng giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-154">The Standard Title will also need to be added to Project Service Pricing entities, **Role Price** and **Role Price Markup**.</span></span> <span data-ttu-id="5fe5c-155">Bạn cũng có thể hoàn tất việc này bằng cách sử dụng mối quan hệ 1:N giữa các thực thể **Chức vụ tiêu chuẩn** và **Giá theo vai trò** và các thực thể **Chức vụ tiêu chuẩn** và **Tăng giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-155">This is also completed using 1:N relationships between the **Standard Title** and **Role Price** entities and **Standard Title** and **Role Price Markup** entities.</span></span>

1. <span data-ttu-id="5fe5c-156">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-156">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="5fe5c-157">Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-157">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="5fe5c-158">Nhấp vào **Mới** để tạo mối quan hệ 1:N mới gọi là **Chức vụ tiêu chuẩn cho Giá theo vai trò**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-158">Click **New** to create a new 1:N relationship called **Standard Title to Role Price**.</span></span> <span data-ttu-id="5fe5c-159">Nhập các thông tin cần thiết, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-159">Enter the required information, and then click **Save**.</span></span>
4. <span data-ttu-id="5fe5c-160">Lặp lại các bước 1-4 để tạo mối quan hệ 1:N giữa các thực thể **Chức vụ tiêu chuẩn** và **Tăng giá theo vai trò**,</span><span class="sxs-lookup"><span data-stu-id="5fe5c-160">Repeat steps 1 - 4 to create 1:N relationships between the **Standard Title** and **Role Price Markup** entities,</span></span>

<span data-ttu-id="5fe5c-161">Trong các giai đoạn bán hàng và dự toán cho dự án, để định giá cho Dự án/Báo giá, cần có ước tính nỗ lực làm việc cho mỗi chức vụ tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-161">In the sales and estimation phases for the project, to price the Quote/Project, estimates of the work effort are required for each standard title.</span></span> <span data-ttu-id="5fe5c-162">Điều này có nghĩa là cần có mối quan hệ 1: N từ chức vụ chuẩn cho mỗi thực thể ước tính trong Project Service:</span><span class="sxs-lookup"><span data-stu-id="5fe5c-162">This means that 1:N relationships from Standard Title to each of these estimation entities in Project Service are needed:</span></span> 

- <span data-ttu-id="5fe5c-163">**Chi tiết dòng báo giá**</span><span class="sxs-lookup"><span data-stu-id="5fe5c-163">**Quote line Detail**</span></span>
- <span data-ttu-id="5fe5c-164">**Chi tiết Mô tả Hợp đồng Dự án**</span><span class="sxs-lookup"><span data-stu-id="5fe5c-164">**Project Contract Line Detail**</span></span>
- <span data-ttu-id="5fe5c-165">**Nhiệm vụ dự án**</span><span class="sxs-lookup"><span data-stu-id="5fe5c-165">**Project Task**</span></span>
- <span data-ttu-id="5fe5c-166">**Thành viên Nhóm Dự án**</span><span class="sxs-lookup"><span data-stu-id="5fe5c-166">**Project Team Member**</span></span>
- <span data-ttu-id="5fe5c-167">**Mô tả Ước tính**</span><span class="sxs-lookup"><span data-stu-id="5fe5c-167">**Estimate Line**</span></span>

5. <span data-ttu-id="5fe5c-168">Lặp lại các bước 1-5 để tạo mối quan hệ 1:N từ **Chức vụ tiêu chuẩn** thành **Chi tiết dòng báo giá**, **Chi tiết dòng hợp đồng dự án**, **Nhiệm vụ dự án**, **Thành viên nhóm hợp đồng** và **Dòng ước tính**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-168">Repeat steps 1 - 5 to create 1:N relationships from **Standard Title** to **Quote line Detail**, **Project Contract Line Detail**, **Project Task**, **Project Team Member**, and **Estimate Line**.</span></span>

> ![Thêm chức vụ tiêu chuẩn làm trường tham chiếu cho dòng ước tính](media/ST-Estimate-Line.png)

<span data-ttu-id="5fe5c-170">Trong giai đoạn gửi và lập hóa đơn, công việc được hoàn thành bởi mỗi chức vụ tiêu chuẩn phải được định giá chính xác trên Thực tế dự án.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-170">In the Delivery and Invoicing phases, the work completed by each standard title must be accurately priced on the Project Actuals.</span></span> <span data-ttu-id="5fe5c-171">Điều này có nghĩa là cần có mối quan hệ 1:N từ các thực thể **Chức vụ tiêu chuẩn** cho **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-171">This means that there needs to be 1:N relationships from **Standard Title** to **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line entities**.</span></span>

6. <span data-ttu-id="5fe5c-172">Lặp lại các bước 1-6 để tạo mối quan hệ 1:N từ các thực thể **Chức vụ tiêu chuẩn** cho **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-172">Repeat steps 1 - 6 to create 1:N relationships from **Standard Title** to **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line entities**.</span></span>

> ![Thêm chức vụ tiêu chuẩn làm trường tham chiếu cho mục nhập thời gian](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a><span data-ttu-id="5fe5c-174">Thiết lập giá trị kích thước mặc định bằng cách sử dụng các tính năng ánh xạ của nền tảng</span><span class="sxs-lookup"><span data-stu-id="5fe5c-174">Set up Dimension value defaulting using the mappings features of the platform</span></span>
<span data-ttu-id="5fe5c-175">Đối với Mục nhập thời gian, việc để hệ thống mặc định chức vụ tiêu chuẩn trên Mục nhập thời gian từ Nguồn lực có thể đặt lịch đang ghi mục nhập thời gian rất hữu ích.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-175">For Time Entry, it would be helpful to have the system default the standard title on the Time Entry from the Bookable Resource that is recording the time entry.</span></span> <span data-ttu-id="5fe5c-176">Sử dụng các bước sau để thêm ánh xạ trường trên mối quan hệ 1:N từ **Tài nguyên có thể đặt lịch** thành **Mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-176">Use the following steps to add field mappings on the 1:N relationship from **Bookable Resource** to **Time Entry**.</span></span>

1. <span data-ttu-id="5fe5c-177">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-177">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="5fe5c-178">Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-178">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="5fe5c-179">Nhấp đúp vào **Tài nguyên có thể đặt lịch cho mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-179">Double-click **Bookable Resource to Time Entry**.</span></span> <span data-ttu-id="5fe5c-180">Trên trang **Mối quan hệ**, nhấp vào **Sử dụng ánh xạ trường**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-180">On the **Relationship** page, click **Use Field mappings**.</span></span> 
4. <span data-ttu-id="5fe5c-181">Nhấp vào **Mới** để tạo ánh xạ trường mới giữa trường **Chức vụ tiêu chuẩn** trên thực thể **Nguồn lực có thể đặt lịch** thành trường tham chiếu **Chức vụ tiêu chuẩn** trên thực thể **Mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-181">Click **New** to create a new field mapping between the **Standard Title** field on the **Bookable Resource** entity to the **Standard Title** reference field on **Time Entry** entity.</span></span> 

> ![Thiết lập ánh xạ trường để cho phép mặc định chức vụ tiêu chuẩn từ nguồn lực có thể đặt lịch vào mục nhập thời gian](media/ST-Mapping2.png)


<span data-ttu-id="5fe5c-183">Thao tác này sẽ hoàn tất các thay đổi với giản đồ cần thiết cho các kích thước tùy chỉnh dựa trên thực thể.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-183">This completes the schema changes required for entity-based custom dimensions.</span></span>

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a><span data-ttu-id="5fe5c-184">Thêm trường tùy chỉnh vào biểu mẫu, dạng xem và quy tắc công việc</span><span class="sxs-lookup"><span data-stu-id="5fe5c-184">Add custom fields to forms, views, and business rules</span></span>

<span data-ttu-id="5fe5c-185">Sau khi bạn đã thực hiện tất cả các thay đổi cần thiết với giản đồ, bước tiếp theo là làm cho các trường hiển thị trong giao diện người dùng bằng cách thêm các trường vào biểu mẫu và dạng xem.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-185">After you have made all of the required schema changes, the next step is to make the fields visible in the UI by adding the fields to the forms and views.</span></span>

1. <span data-ttu-id="5fe5c-186">Mở biểu mẫu hoặc dạng xem.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-186">Open the form or the view.</span></span> <span data-ttu-id="5fe5c-187">Trên ngăn điều hướng bên phải, chọn trường và kéo nó vào bảng tùy biến biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-187">On the right navigation pane, select the field and drag it on to the form canvas.</span></span> 
2. <span data-ttu-id="5fe5c-188">Nếu bạn đang chỉnh sửa dạng xem, hãy sử dụng ngăn điều hướng bên phải, nhấp vào **Thêm trường** và trong hộp thoại **Danh sách trường**, chọn các trường mà bạn cần rồi nhấp vào **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-188">If you are editing a view, use the right navigation pane, click **Add fields**, and in the **Field listing** dialog box, select the fields that you need and click **Ok**.</span></span>

<span data-ttu-id="5fe5c-189">Bảng sau đây cung cấp một danh sách toàn diện các biểu mẫu và dạng xem sẵn dùng, theo thực thể sẽ cần phải được cập nhật với các trường mới.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-189">The following table provides a comprehensive list of out-of-the-box forms and views, by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="5fe5c-190">Nếu bạn có bất kỳ dạng xem bổ sung hoặc biểu mẫu nào trong tùy chỉnh của mình trên các thực thể này, hãy thêm các trường mới vào các mục đó.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-190">If you have any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

| <span data-ttu-id="5fe5c-191">Thực thể Project Service</span><span class="sxs-lookup"><span data-stu-id="5fe5c-191">Project Service Entity</span></span>        | <span data-ttu-id="5fe5c-192">Các biểu mẫu cần trường mới</span><span class="sxs-lookup"><span data-stu-id="5fe5c-192">Forms that need the new field</span></span>   |<span data-ttu-id="5fe5c-193">Các dạng xem cần trường mới</span><span class="sxs-lookup"><span data-stu-id="5fe5c-193">Views that need the new field</span></span>      |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="5fe5c-194">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="5fe5c-194">Role Price</span></span>|<span data-ttu-id="5fe5c-195">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-195">• Information</span></span> |<span data-ttu-id="5fe5c-196">• Giá danh mục nguồn lực hoạt động</span><span class="sxs-lookup"><span data-stu-id="5fe5c-196">• Active Resource Category Prices</span></span><br> <span data-ttu-id="5fe5c-197">• Chế độ xem liên kết của Giá danh mục nguồn lực</span><span class="sxs-lookup"><span data-stu-id="5fe5c-197">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="5fe5c-198">Tăng giá theo Vai trò</span><span class="sxs-lookup"><span data-stu-id="5fe5c-198">Role Price Markup</span></span>|<span data-ttu-id="5fe5c-199">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-199">• Information</span></span>|<span data-ttu-id="5fe5c-200">• Tăng giá theo vai trò hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-200">• Active Role Price Markup</span></span><br><span data-ttu-id="5fe5c-201">• Chế độ xem liên kết tăng giá theo vai trò</span><span class="sxs-lookup"><span data-stu-id="5fe5c-201">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="5fe5c-202">Chi tiết mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="5fe5c-202">Quote line detail</span></span>|<span data-ttu-id="5fe5c-203">• Thông tin dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-203">• Project Information</span></span><br><span data-ttu-id="5fe5c-204">• Tạo nhanh dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-204">• Project Quick Create</span></span>|<span data-ttu-id="5fe5c-205">• Chi tiết mô tả báo giá hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-205">• Active Quote Line Detail</span></span><br><span data-ttu-id="5fe5c-206">• Chi tiết mô tả báo giá kết hợp</span><span class="sxs-lookup"><span data-stu-id="5fe5c-206">• Combined Quote Line Details</span></span><br><span data-ttu-id="5fe5c-207">• Dạng xem liên kết chi tiết mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="5fe5c-207">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="5fe5c-208">Chi tiết mô tả hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-208">Project Contract line detail</span></span>|<span data-ttu-id="5fe5c-209">• Thông tin dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-209">• Project Information</span></span><br><span data-ttu-id="5fe5c-210">• Tạo nhanh dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-210">• Project Quick Create</span></span>|<span data-ttu-id="5fe5c-211">• Chi tiết Mô tả Hợp đồng Kết hợp</span><span class="sxs-lookup"><span data-stu-id="5fe5c-211">• Combined Contract Line Details</span></span><br><span data-ttu-id="5fe5c-212">• Chi tiết mô tả hợp đồng hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-212">• Active Contract Line Details</span></span><br><span data-ttu-id="5fe5c-213">• Dạng xem Liên kết Chi tiết Mô tả Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="5fe5c-213">• Contract Line Details Associated View</span></span>|
|  <span data-ttu-id="5fe5c-214">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-214">Project Task</span></span>|<span data-ttu-id="5fe5c-215">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-215">• Information</span></span><br><span data-ttu-id="5fe5c-216">• Biểu mẫu mới</span><span class="sxs-lookup"><span data-stu-id="5fe5c-216">• New Form</span></span>||
|  <span data-ttu-id="5fe5c-217">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-217">Project Team Member</span></span>|<span data-ttu-id="5fe5c-218">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-218">• Information</span></span><br><span data-ttu-id="5fe5c-219">• Biểu mẫu mới</span><span class="sxs-lookup"><span data-stu-id="5fe5c-219">• New Form</span></span>|<span data-ttu-id="5fe5c-220">• Thành viên nhóm dự án hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-220">• Active Project Team Members</span></span><br><span data-ttu-id="5fe5c-221">• Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-221">• Project Team Members</span></span><br><span data-ttu-id="5fe5c-222">• Chế độ xem liên kết cho thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="5fe5c-222">• Project Team members associated View</span></span>|
|  <span data-ttu-id="5fe5c-223">Mục nhập Thời gian</span><span class="sxs-lookup"><span data-stu-id="5fe5c-223">Time Entry</span></span>|<span data-ttu-id="5fe5c-224">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-224">• Information</span></span><br><span data-ttu-id="5fe5c-225">• Tạo mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="5fe5c-225">• Create Time Entry</span></span>|<span data-ttu-id="5fe5c-226">• Mục nhập thời gian theo ngày của tôi</span><span class="sxs-lookup"><span data-stu-id="5fe5c-226">• My Time Entries By Date</span></span><br><span data-ttu-id="5fe5c-227">• Mục nhập thời gian của tôi trong tuần này</span><span class="sxs-lookup"><span data-stu-id="5fe5c-227">• My time Entries for this week</span></span><br><span data-ttu-id="5fe5c-228">• Mục nhập thời gian để phê duyệt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-228">• Time entries for approval</span></span>|
|  <span data-ttu-id="5fe5c-229">Dòng Nhật ký Kế toán</span><span class="sxs-lookup"><span data-stu-id="5fe5c-229">Journal Line</span></span>|<span data-ttu-id="5fe5c-230">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-230">• Information</span></span><br><span data-ttu-id="5fe5c-231">• Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="5fe5c-231">• Quick create</span></span>|<span data-ttu-id="5fe5c-232">• Dòng nhật ký kế toán hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-232">• Active journal lines</span></span><br><span data-ttu-id="5fe5c-233">• Chế độ xem liên kết dòng nhật ký kế toán</span><span class="sxs-lookup"><span data-stu-id="5fe5c-233">• Journal Line associated view</span></span>|
|  <span data-ttu-id="5fe5c-234">Chi tiết Mô tả Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="5fe5c-234">Invoice Line Detail</span></span>|<span data-ttu-id="5fe5c-235">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-235">• Information</span></span><br><span data-ttu-id="5fe5c-236">• Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="5fe5c-236">• Quick create</span></span>|<span data-ttu-id="5fe5c-237">• Chi tiết mô tả hóa đơn hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-237">• Active Invoice Line Details</span></span><br><span data-ttu-id="5fe5c-238">• Giao dịch hóa đơn có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="5fe5c-238">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="5fe5c-239">• Giao dịch hóa đơn miễn phí</span><span class="sxs-lookup"><span data-stu-id="5fe5c-239">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="5fe5c-240">• Dạng xem liên kết chi tiết mô tả hóa đơn</span><span class="sxs-lookup"><span data-stu-id="5fe5c-240">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="5fe5c-241">• Giao dịch hóa đơn không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="5fe5c-241">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="5fe5c-242">Thực tế</span><span class="sxs-lookup"><span data-stu-id="5fe5c-242">Actual</span></span>|<span data-ttu-id="5fe5c-243">• Thông tin</span><span class="sxs-lookup"><span data-stu-id="5fe5c-243">• Information</span></span><br><span data-ttu-id="5fe5c-244">• Thực tế hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="5fe5c-244">• Active Actuals</span></span>|<span data-ttu-id="5fe5c-245">• Dạng xem liên kết thực tế</span><span class="sxs-lookup"><span data-stu-id="5fe5c-245">• Actual Associated view</span></span>|

<span data-ttu-id="5fe5c-246">Trường tùy chỉnh cũng có thể cần được thêm vào các quy tắc kinh doanh tùy thuộc vào những gì bạn đã xác định.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-246">Custom fields may also need to be added on business rules depending on what you have defined.</span></span> <span data-ttu-id="5fe5c-247">Một ví dụ sẵn dùng là đối với quy tắc công việc **Khả năng chỉnh sửa mục nhập thời gian dựa trên trạng thái**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-247">One out-of-the-box example is for the business rule **Editability of Time Entry based on status**.</span></span> <span data-ttu-id="5fe5c-248">Quy tắc này xác định các trường cần bị khóa khi mục nhập thời gian ở trạng thái không thể chỉnh sửa như **Đã phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-248">This rule defines which fields need to be locked when the Time Entry is in a non-editable status such as **Approved**.</span></span> <span data-ttu-id="5fe5c-249">Thêm các trường vào quy tắc công việc này để không thể chỉnh sửa các trường khi mục nhập thời gian ở trạng thái không phải **Bản nháp** hoặc **Đã trả lại**.</span><span class="sxs-lookup"><span data-stu-id="5fe5c-249">Add fields to this business rule so that the fields are locked for editing when the Time Entry is in a status other than **Draft** or **Returned**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]