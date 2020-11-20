---
title: Công nhật
description: Chủ đề này cung cấp thông tin về các quy tắc công tác phí được sử dụng trong Quản lý chi phí.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128534"
---
# <a name="per-diems"></a><span data-ttu-id="21fd9-103">Công nhật</span><span class="sxs-lookup"><span data-stu-id="21fd9-103">Per diems</span></span>

<span data-ttu-id="21fd9-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="21fd9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="21fd9-105">Công tác phí là một khoản phụ cấp được trả cho người lao động đi công tác.</span><span class="sxs-lookup"><span data-stu-id="21fd9-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="21fd9-106">Trong Quản lý chi phí, bạn có thể tạo quy tắc công tác phí cho các tình huống đi lại khác nhau.</span><span class="sxs-lookup"><span data-stu-id="21fd9-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="21fd9-107">Mức công tác phí có thể dựa trên thời gian trong năm, địa điểm đến hoặc cả hai.</span><span class="sxs-lookup"><span data-stu-id="21fd9-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="21fd9-108">Khi bạn tạo quy tắc công tác phí, bạn có thể chỉ định rằng tỷ lệ phần trăm công tác phí sẽ được giữ lại nếu người lao động nhận được các bữa ăn hoặc dịch vụ miễn phí.</span><span class="sxs-lookup"><span data-stu-id="21fd9-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="21fd9-109">Bạn cũng có thể đặt số giờ tối thiểu và tối đa mà mức công tác phí có thể áp dụng cho việc đi lại của người lao động.</span><span class="sxs-lookup"><span data-stu-id="21fd9-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="21fd9-110">Cấu hình</span><span class="sxs-lookup"><span data-stu-id="21fd9-110">Configuration</span></span> 

1. <span data-ttu-id="21fd9-111">Để thêm địa điểm cấp công tác phí, hãy truy cập **Thiết lập** > **Phép tính và mã** > **Địa điểm cấp công tác phí**.</span><span class="sxs-lookup"><span data-stu-id="21fd9-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="21fd9-112">Đối với mỗi địa điểm đã thêm ở trên, hãy chọn mức công tác phí và đơn vị tiền tệ hợp lệ giữa ngày bắt đầu và ngày kết thúc cụ thể cho khách sạn, bữa ăn và các chi phí khác.</span><span class="sxs-lookup"><span data-stu-id="21fd9-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="21fd9-113">Mức công tác phí và đơn vị tiền tệ được đặt cấu hình trong phần **Thiết lập** > **Phép tính và mã** > **Công tác phí**.</span><span class="sxs-lookup"><span data-stu-id="21fd9-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="21fd9-114">Trên trang **Địa điểm cấp công tác phí**, đặt cấu hình các bậc mức công tác phí.</span><span class="sxs-lookup"><span data-stu-id="21fd9-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="21fd9-115">Các bậc mức công tác phí cho phép bạn xác định tỷ lệ phần trăm của phụ cấp hàng ngày cho khách sạn, bữa ăn và các chi phí khác.</span><span class="sxs-lookup"><span data-stu-id="21fd9-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="21fd9-116">Để chỉ định mức giảm phần trăm bữa ăn cho bữa sáng, bữa trưa hoặc bữa tối, hãy cập nhật các trường trên trang **Các tham số quản lý chi phí** trên tab **Công tác phí**.</span><span class="sxs-lookup"><span data-stu-id="21fd9-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="21fd9-117">Gửi chi phí bằng công tác phí</span><span class="sxs-lookup"><span data-stu-id="21fd9-117">Submit expenses using per diem</span></span>
<span data-ttu-id="21fd9-118">Để gửi chi phí bằng công tác phí, hãy sử dụng danh mục chi phí **Công tác phí** khi bạn tạo báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="21fd9-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="21fd9-119">Nhập **Công tác phí từ ngày**, **Công tác phí đến nay** và **Địa điểm cấp công tác phí**.</span><span class="sxs-lookup"><span data-stu-id="21fd9-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="21fd9-120">Số tiền sẽ được tính dựa trên mức công tác phí cho địa điểm đã chọn và mức giảm trừ bữa ăn sẽ được tính dựa trên mức công tác phí.</span><span class="sxs-lookup"><span data-stu-id="21fd9-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
