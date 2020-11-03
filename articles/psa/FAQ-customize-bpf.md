---
title: Tôi có thể làm cách nào để tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án?
description: Tổng quan về cách tùy chỉnh dòng quy trình công việc ở các giai đoạn dự án.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2dccc33088cd9e49e7ffe609f9d9754ef33a5dba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087294"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="6eb5d-103">Tôi có thể làm cách nào để tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án?</span><span class="sxs-lookup"><span data-stu-id="6eb5d-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="6eb5d-104">Có một giới hạn đã biết ở các phiên bản trước của ứng dụng Project Service là tên của các giai đoạn trong dòng quy trình công việc ở Các giai đoạn Dự án phải trùng chính xác với tên tiếng Anh dự tính ( **Quote** , **Plan** , **Close** ).</span><span class="sxs-lookup"><span data-stu-id="6eb5d-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names ( **Quote** , **Plan** , **Close** ).</span></span> <span data-ttu-id="6eb5d-105">Nếu không, theo lô-gic công việc dựa trên tên giai đoạn tiếng Anh sẽ không làm việc như mong đợi.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="6eb5d-106">Đó là lý do tại sao bạn không thấy các tác vụ quen thuộc như **Đổi Quy trình** hoặc **Sửa Quy trình** sẵn có trên mẫu dự án và không khuyến khích việc tùy chỉnh dòng quy trình công việc.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="6eb5d-107">Hạn chế này đã được khắc phục trong phiên bản 2.4.5.48 trở lên.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="6eb5d-108">Bài viết này cung cấp các cách giải quyết gợi ý cho các phiên bản cũ nếu bạn cần tùy chỉnh dòng quy trình công việc mặc định cho các phiên bản cũ hơn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="6eb5d-109">Lô-gic công việc yêu cầu khớp chính xác với tên giai đoạn tiếng Anh</span><span class="sxs-lookup"><span data-stu-id="6eb5d-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="6eb5d-110">Dòng quy trình công việc ở Các giai đoạn Dự án bao gồm lô-gic công việc điều khiển các hành vi sau trong ứng dụng:</span><span class="sxs-lookup"><span data-stu-id="6eb5d-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="6eb5d-111">Khi dự án liên kết với một báo giá, mã sẽ đặt dòng quy trình công việc vào giai đoạn **Quote**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="6eb5d-112">Khi dự án được liên kết với một hợp đồng, mã sẽ đặt dòng quy trình công việc vào giai đoạn **Plan**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="6eb5d-113">Khi dòng quy trình công việc tiến tới giai đoạn **Close** , bản ghi dự án sẽ bị hủy kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="6eb5d-114">Khi dự án bị hủy kích hoạt, biểu mẫu dự án và cấu trúc phân tích công việc (WBS) được đặt về chế độ chỉ đọc, đăng ký nguồn lực được đặt tên được phát hành và bất kỳ bảng giá liên kết nào cũng bị hủy kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="6eb5d-115">Lô-gic công việc này dựa trên tên tiếng Anh cho các giai đoạn dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="6eb5d-116">Sự phụ thuộc vào tên giai đoạn tiếng Anh là lý do chính tại sao việc tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án lại không được khuyến khích. Cũng như tại sao bạn không thấy các tác vụ dòng quy trình công việc phổ thông như **Đổi Quy trình** hoặc **Sửa quy trình** trên thực thể dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="6eb5d-117">Điều gì sẽ xảy ra nếu tên giai đoạn không khớp với tên tiếng Anh?</span><span class="sxs-lookup"><span data-stu-id="6eb5d-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="6eb5d-118">Trong ứng dụng Project Service phiên bản 1.x trên nền tảng 8.2, khi các tên giai đoạn trong dòng quy trình công việc không khớp chính xác với các tên giai đoạn tiếng Anh, lô-gic công việc mà đặt giai đoạn đúng cho báo giá hoặc hợp đồng hoặc đóng dự án, sẽ bị bỏ qua.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="6eb5d-119">Không có thông báo lỗi nào được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-119">No error messages are displayed.</span></span> <span data-ttu-id="6eb5d-120">Do đó, điều đó có nghĩa bạn có thể tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="6eb5d-121">Tuy nhiên, bạn sẽ không thấy bất kỳ quy trình tự động nào hoạt động cho báo giá, hợp đồng và đóng dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="6eb5d-122">Trong ứng dụng Project Service phiên bản 2.4.4.30 trở về trước trên nền tảng 9.0, đã có một thay đổi kiến trúc đáng kể cho dòng quy trình công việc mà cần viết lại lô-gic công việc của dòng quy trình công việc.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="6eb5d-123">Kết quả là nếu tên giai đoạn quy trình không khớp với tên tiếng Anh dự kiến, bạn nhận được một thông báo lỗi.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="6eb5d-124">Vì vậy, nếu bạn muốn tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án cho thực thể dự án, bạn chỉ có thể thêm giai đoạn mới hoàn toàn vào dòng quy trình công việc mặc định cho thực thể dự án trong khi giữ nguyên các giai đoạn **Quote** , **Plan** và **Close**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote** , **Plan** , and **Close** stages as-is.</span></span> <span data-ttu-id="6eb5d-125">Giới hạn này đảm bảo bạn không gặp phải lỗi do lô-gic công việc phụ thuộc vào tên giai đoạn tiếng Anh trong dòng quy trình công việc.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="6eb5d-126">Trong phiên bản 2.4.5.48 trở lên, lô-gic công việc được mô tả trong bài viết này đã được loại bỏ khỏi dòng quy trình công việc mặc định cho thực thể dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="6eb5d-127">Nâng cấp từ phiên bản đó trở lên sẽ cho phép bạn tùy chỉnh hoặc thay đổi dòng quy trình công việc mặc định với dòng quy trình công việc của bạn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="6eb5d-128">Cách giải quyết đối với các phiên bản cũ</span><span class="sxs-lookup"><span data-stu-id="6eb5d-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="6eb5d-129">Nếu nâng cấp không phải là một tùy chọn, bạn có thể tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án cho thực thể dự án theo một trong hai cách sau:</span><span class="sxs-lookup"><span data-stu-id="6eb5d-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="6eb5d-130">Thêm các giai đoạn bổ sung vào cấu hình mặc định trong khi vẫn giữ nguyên tên giai đoạn tiếng Anh cho **Quote** , **Plan** và **Close**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote** , **Plan** , and **Close**.</span></span>


![Ảnh chụp màn hình khi thêm các giai đoạn vào cấu hình mặc định](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="6eb5d-132">Tạo dòng quy trình công việc của riêng mình và biến thành dòng quy trình công việc chính cho thực thể dự án, như vậy bạn sẽ có bất kỳ tên giai đoạn nào mà bạn muốn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="6eb5d-133">Tuy nhiên, nếu bạn muốn sử dụng các giai đoạn dự án theo chuẩn trước là **Quote** , **Plan** và **Close** , bạn cần thực hiện một số tùy chỉnh để bỏ tên giai đoạn tùy chỉnh của mình.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-133">However, if you want to use the same standard project stages **Quote** , **Plan** , and **Close** , you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="6eb5d-134">Lô-gic phức tạp hơn là khi đóng dự án, khi đó bạn có thể vẫn kích hoạt bằng cách chỉ hủy kích hoạt bản ghi dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Tùy chỉnh BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="6eb5d-136">Các cân nhắc bổ sung đối với ứng dụng Project Service phiên bản 2.4.4.30 trở về trước trên nền tảng 9.0</span><span class="sxs-lookup"><span data-stu-id="6eb5d-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="6eb5d-137">Trong Project Service 2.4.4.30 trở về trước trên nền tảng 9.0, với dòng quy trình công việc tùy chỉnh, trường **Tên Giai đoạn** trên thực thể dự án được dùng trong các dạng xem danh sách dự án và biểu đồ **Dự án Theo Giai đoạn** sẽ không được cập nhật, bởi vì trường này được tích hợp với dòng quy trình công việc ở Các giai đoạn Dự án.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="6eb5d-138">Bạn có thể giải quyết vấn đề này theo các bước như sau:</span><span class="sxs-lookup"><span data-stu-id="6eb5d-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="6eb5d-139">Thêm một trường tùy chỉnh để chụp giai đoạn dòng quy trình công việc mà được cập nhật khi người dùng tiến hành qua dòng quy trình công việc tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="6eb5d-140">Sửa đổi biểu đồ **Dự án Theo Giai đoạn** để làm việc với trường tùy chỉnh của bạn thay cho cấu hình mặc định.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="6eb5d-141">Các bước để tạo dòng quy trình công việc của riêng mình cho thực thể dự án</span><span class="sxs-lookup"><span data-stu-id="6eb5d-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="6eb5d-142">Để tạo dòng quy trình công việc của riêng mình cho thực thể dự án, làm như sau:</span><span class="sxs-lookup"><span data-stu-id="6eb5d-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="6eb5d-143">Chuyển tới **Cài đặt** > **Trung tâm Quy trình**.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="6eb5d-144">Không sao chép dòng quy trình công việc ở Các giai đoạn Dự án bởi vì như thế cũng sao chép lô-gic công việc của Project Service.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Tạo quy trình](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="6eb5d-146">Sử dụng trình Thiết kế Quy trình để tạo tên giai đoạn mà bạn muốn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="6eb5d-147">Nếu bạn muốn cùng chức năng đó là các giai đoạn mặc định cho **Quote** , **Plan** và **Close** , bạn sẽ phải tạo dựa trên những tên giai đoạn của dòng quy trình công tùy chỉnh của mình.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-147">If you want the same functionality as the default stages for **Quote** , **Plan** , and **Close** , you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Ảnh chụp màn hình của trình Thiết kế Quy trình được dùng để tùy chỉnh BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="6eb5d-149">Trong trình Thiết kế Quy trình, **Sắp xếp Dòng Quy trình** để tạo dòng quy trình công việc tùy chỉnh thành dòng quy trình công việc chính cho thực thể dự án bằng cách di chuyển quy trình ở phía trên dòng quy trình công việc ở Các giai đoạn Dự án lên trên cùng của danh sách.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="6eb5d-150">Ảnh chụp màn hình khi sử dụng Sắp xếp Dòng Quy trình</span><span class="sxs-lookup"><span data-stu-id="6eb5d-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="6eb5d-151">Các bước sau đây áp dụng cho ứng dụng Project Service 2.4.4.30 trở về trước trên nền tảng 9.0</span><span class="sxs-lookup"><span data-stu-id="6eb5d-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="6eb5d-152">Thêm một trường tùy chỉnh mới vào thực thể dự án để chụp các giai đoạn tùy chỉnh trong dòng quy trình công việc tùy chỉnh của bạn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="6eb5d-153">Bạn sẽ cần thêm lô-gic công việc (phần bổ trợ/dòng công việc) để cập nhật trường này khi giai đoạn trên dòng quy trình công việc được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Ảnh chụp màn hình khi tùy chỉnh thực thể Dự án](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="6eb5d-155">Sửa đổi biểu đồ **Dự án Theo Giai đoạn** để dùng trường tùy chỉnh mới cho các giai đoạn của bạn.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Ảnh chụp màn hình khi sử dụng biểu đồ Dự án Theo Giai đoạn](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="6eb5d-157">Sửa đổi bất kỳ dạng xem nào cho thực thể để đưa trường tùy chính mới cho các giai đoạn của bạn vào.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Ảnh chụp màn hình khi chỉnh sửa dạng xem trên thực thể Dự án](media/FAQ-Customize-BPF-8-720.png)

