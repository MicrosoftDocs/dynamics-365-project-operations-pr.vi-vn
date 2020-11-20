---
title: Tại sao giá được mặc định là 0 trên thực tế thời gian chi phí?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế chi phí bán hàng.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131413"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="6724f-103">Tại sao giá được mặc định là 0 trên thực tế thời gian chi phí?</span><span class="sxs-lookup"><span data-stu-id="6724f-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6724f-104">Câu hỏi thường gặp này áp dụng cho các thực tế mà lớp giao dịch được đặt thành Thời gian và loại giao dịch là Chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="6724f-105">Ba bước kiểm tra sau đây sẽ giúp bạn khắc phục sự cố tại sao giá (tỷ lệ thanh toán) mặc định là 0 vào trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="6724f-106">Bước 1: Xác định bảng giá chi phí dành cho dự án</span><span class="sxs-lookup"><span data-stu-id="6724f-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="6724f-107">Tìm dự án từ trường dự án của thực tế và đi đến trang dự án.</span><span class="sxs-lookup"><span data-stu-id="6724f-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="6724f-108">Nhấp vào liên kết đơn vị hợp đồng trong trường này.</span><span class="sxs-lookup"><span data-stu-id="6724f-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="6724f-109">Trên trang Đơn vị hợp đồng, kiểm tra xem đơn vị hợp đồng có bảng giá trong lưới Bảng Giá Vốn hay không.</span><span class="sxs-lookup"><span data-stu-id="6724f-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="6724f-110">Nếu có nhiều hơn một bảng giá, bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="6724f-111">Project Service chỉ hỗ trợ một bảng giá cho mỗi đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6724f-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="6724f-112">Loại bỏ tất cả bảng giá từ thực thể này cho đến khi chỉ có một bảng giá được đính kèm trong lưới Bảng Giá Vốn của Đơn vị Tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6724f-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="6724f-113">Nếu không có bảng giá đính kèm với Đơn vị Tổ chức, hãy ghi lại đơn vị tiền tệ của Đơn vị Tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6724f-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="6724f-114">Hãy vào Project Service, sau đó vào Tham số và mở tab Bảng giá. Kiểm tra xem có bất kỳ bảng giá nào có ngữ cảnh được đặt thành Chi phí và đơn vị tiền tệ khớp với đơn vị tiền tệ của Đơn vị Tổ chức hay không.</span><span class="sxs-lookup"><span data-stu-id="6724f-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="6724f-115">Nếu không có bảng giá nào phù hợp với tiêu chí đó, bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="6724f-116">Đảm bảo có ít nhất một bảng giá có ngữ cảnh được đặt thành Chi phí và đơn vị tiền tệ khớp với đơn vị tiền tệ của Đơn vị Tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6724f-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="6724f-117">Nếu có nhiều hơn một bảng giá phù hợp với tiêu chí đó, tiếp tục đọc tài liệu này để thực hiện kiểm tra thêm.</span><span class="sxs-lookup"><span data-stu-id="6724f-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="6724f-118">Bước 2: Có bất kỳ bảng giá nào được xác định ở trên hợp lệ cho ngày cụ thể của thực tế thời gian chi phí không?</span><span class="sxs-lookup"><span data-stu-id="6724f-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="6724f-119">Để Project Service xem xét đặt mức giá mặc định cho một bảng giá, bảng giá đó phải được áp dụng cho ngày cụ thể trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="6724f-120">Kiểm tra những điều sau đây để xem liệu (các) bảng giá được xác định ở trên có được áp dụng hay không:</span><span class="sxs-lookup"><span data-stu-id="6724f-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="6724f-121">Kiểm tra xem ngày bắt đầu và ngày kết thúc trên tab chung cho các bảng giá đính kèm có trống không.</span><span class="sxs-lookup"><span data-stu-id="6724f-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="6724f-122">Nếu ngày bắt đầu và kết thúc trên bảng giá được xác định ở trên trống, bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="6724f-123">Ghi chú về trường ngày bắt đầu trên thực tế thời gian chi phí của bạn và kiểm tra xem có bất kỳ danh sách giá nào được xác định có thể áp dụng cho ngày đó hay không.</span><span class="sxs-lookup"><span data-stu-id="6724f-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="6724f-124">Ví dụ: ngày trên thực tế thời gian chi phí phải nằm giữa ngày bắt đầu và ngày kết thúc trên bảng giá.</span><span class="sxs-lookup"><span data-stu-id="6724f-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="6724f-125">Nếu không có bảng giá nào bao gồm ngày đó trên thực tế thời gian chi phí thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="6724f-126">Thay đổi ngày bắt đầu và kết thúc của bảng giá để đảm bảo rằng bảng giá bao gồm ngày trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="6724f-127">Nếu có nhiều hơn một bảng giá bao gồm ngày đó trên thực tế thời gian cho phí thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="6724f-128">Bạn có thể sửa lỗi này bằng cách chỉnh sửa ngày bắt đầu và kết thúc của (các) bảng giá để chỉ có một bảng giá bao gồm ngày trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="6724f-129">Nếu có chỉ có một bảng giá bao gồm ngày đó chi phí thời gian thực tế, di chuyển đến phòng tiếp theo trong tài liệu.</span><span class="sxs-lookup"><span data-stu-id="6724f-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="6724f-130">Khi bạn đã thực hiện xong các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian chi phí hiển thị mức giá hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="6724f-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="6724f-131">Bước 3: Có mức giá nào trong bảng giá dành cho kích thước định giá trên thực tế thời gian chi phí không?</span><span class="sxs-lookup"><span data-stu-id="6724f-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="6724f-132">Nếu bạn đã hoàn thành Bước 1 và Bước 2, bây giờ bạn chỉ có một bảng giá được áp dụng cho ngày cụ thể trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="6724f-133">Mở Bảng giá này và di chuyển đến tab Giá Vai trò. Đảm bảo rằng có một hàng trên lưới dành cho kích thước giá trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="6724f-134">Nếu không có hàng nào trong lưới giá vai trò cho kích thước định giá trên thực tế thời gian chi phí thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="6724f-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="6724f-135">Tạo một hàng trong lưới Giá vai trò cho kích thước định giá trên thực tế thời gian chi phí.</span><span class="sxs-lookup"><span data-stu-id="6724f-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="6724f-136">Khi bạn đã thực hiện xong, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian chi phí hiển thị mức giá hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="6724f-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="6724f-137">Nếu bạn vẫn không thấy một mức giá hợp lệ trên thực tế thời gian chi phí của mình sau khi hoàn thành ba bước kiểm tra ở trên, vui lòng ghi một phiếu hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="6724f-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



