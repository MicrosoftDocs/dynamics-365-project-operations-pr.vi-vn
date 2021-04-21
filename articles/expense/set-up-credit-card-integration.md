---
title: Thiết lập phần tích hợp thẻ tín dụng
description: Chủ đề này giải thích cách làm việc với các giao dịch thẻ tín dụng liên quan đến chi phí.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866709"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="4b043-103">Thiết lập phần tích hợp thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="4b043-103">Set up credit card integration</span></span>

<span data-ttu-id="4b043-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="4b043-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b043-105">Các giao dịch thẻ tín dụng liên quan đến chi phí có thể được thiết lập để tự động nhập vào theo lịch trình định kỳ.</span><span class="sxs-lookup"><span data-stu-id="4b043-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="4b043-106">Ngoài ra, có thể nhập giao dịch theo cách thủ công khi cần.</span><span class="sxs-lookup"><span data-stu-id="4b043-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="4b043-107">Các giao dịch thẻ tín dụng được nhập thông qua thực thể dữ liệu giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="4b043-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="4b043-108">Nhập giao dịch thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="4b043-108">Import credit card transactions</span></span>

<span data-ttu-id="4b043-109">Để nhập giao dịch thẻ tín dụng, hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="4b043-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="4b043-110">Trên trang **Giao dịch thẻ tín dụng**, chọn **Nhập giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="4b043-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="4b043-111">Nếu bạn mở tác vụ quản lý dữ liệu lần đầu tiên, hệ thống phải cập nhật danh sách các thực thể dữ liệu trước khi bạn có thể tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="4b043-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="4b043-112">Trong trường **Tên**, hãy nhập một thông tin mô tả duy nhất cho công việc nhập.</span><span class="sxs-lookup"><span data-stu-id="4b043-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="4b043-113">Trong trường **Định dạng dữ liệu nguồn**, chọn định dạng của tệp chứa giao dịch thẻ tín dụng để nhập.</span><span class="sxs-lookup"><span data-stu-id="4b043-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="4b043-114">Chọn **Tải lên** rồi tìm và chọn tệp để nhập.</span><span class="sxs-lookup"><span data-stu-id="4b043-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="4b043-115">Sau khi tệp đã được tải lên, hãy xác thực quá trình ánh xạ tệp giao dịch thẻ tín dụng và các cột của thực thể dữ liệu giao dịch thẻ tín dụng bằng cách chọn liên kết **Xem bản đồ** trên ngăn xếp.</span><span class="sxs-lookup"><span data-stu-id="4b043-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="4b043-116">Nếu có lỗi ánh xạ hoặc nếu bạn phải thay đổi ánh xạ, hãy thực hiện các thay đổi về ánh xạ trong tab **Trực quan hóa ánh xạ** hoặc tab **Chi tiết ánh xạ**.</span><span class="sxs-lookup"><span data-stu-id="4b043-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="4b043-117">Để tự động hóa các giao dịch thẻ tín dụng, hãy chọn **Tạo tác vụ dữ liệu định kỳ**.</span><span class="sxs-lookup"><span data-stu-id="4b043-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="4b043-118">Sau đó, bạn có thể đặt mức lặp lại để xác định tần suất nhập giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="4b043-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="4b043-119">Sau khi hoàn tất, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b043-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="4b043-120">Để nhập tệp đã chọn ngay bây giờ, hãy chọn **Nhập**.</span><span class="sxs-lookup"><span data-stu-id="4b043-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="4b043-121">Nếu xảy ra lỗi trong quá trình nhập, bạn có thể xem nhật ký thực thi hoặc dữ liệu phân đoạn để xem các lỗi mà bạn phải sửa để giúp đảm bảo nhập thành công.</span><span class="sxs-lookup"><span data-stu-id="4b043-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="4b043-122">Nếu cần nhập nhiều định dạng tệp, bạn phải tạo các lệnh nhập riêng cho từng loại định dạng.</span><span class="sxs-lookup"><span data-stu-id="4b043-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="4b043-123">Chỉ định lại giao dịch thẻ tín dụng cho nhân viên bị chấm dứt hồ sơ</span><span class="sxs-lookup"><span data-stu-id="4b043-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="4b043-124">Sau khi hồ sơ nhân viên bị chấm dứt, tài khoản Dịch vụ miền Active Directory (AD DS) của nhân viên đó sẽ bị vô hiệu hóa.</span><span class="sxs-lookup"><span data-stu-id="4b043-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="4b043-125">Tuy nhiên, có thể có các giao dịch thẻ tín dụng đang hoạt động vẫn phải được chi tiêu và hoàn trả.</span><span class="sxs-lookup"><span data-stu-id="4b043-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="4b043-126">Trên trang **Giao dịch thẻ tín dụng**, bạn có thể chỉ định lại nhân viên cho bất kỳ giao dịch thẻ tín dụng nào mà nhân viên được liên kết đã bị chấm dứt.</span><span class="sxs-lookup"><span data-stu-id="4b043-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="4b043-127">Chọn một hoặc nhiều giao dịch thẻ tín dụng, sau đó chọn **Chỉ định lại giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="4b043-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="4b043-128">Sau đó, bạn có thể chọn một nhân viên khác để chỉ định giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="4b043-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="4b043-129">Sau khi chỉ định lại giao dịch thẻ tín dụng, bạn có thể chọn các giao dịch đó cho báo cáo chi phí và được thanh toán theo quy trình hoàn trả báo cáo chi phí thông thường.</span><span class="sxs-lookup"><span data-stu-id="4b043-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="4b043-130">Xóa các giao dịch thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="4b043-130">Delete credit card transactions</span></span> 

<span data-ttu-id="4b043-131">Đôi khi, sau khi nhập xong các giao dịch thẻ tín dụng, bạn có thể cần xóa một số giao dịch.</span><span class="sxs-lookup"><span data-stu-id="4b043-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="4b043-132">Điều này có thể là do các giao dịch bị trùng lặp hoặc do dữ liệu có thể không chính xác.</span><span class="sxs-lookup"><span data-stu-id="4b043-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="4b043-133">Quản trị viên có thể sử dụng tính năng **"Xóa giao dịch thẻ tín dụng"** để chọn và xóa các giao dịch thẻ tín dụng **không đính kèm** với báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="4b043-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="4b043-134">Đi đến **Nhiệm vụ định kỳ** > **Xóa giao dịch thẻ tín dụng**.</span><span class="sxs-lookup"><span data-stu-id="4b043-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="4b043-135">Chọn **Bộ lọc** và cung cấp thông tin để xác định các bản ghi cần đưa vào.</span><span class="sxs-lookup"><span data-stu-id="4b043-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="4b043-136">Chọn **OK** để xóa các bản ghi.</span><span class="sxs-lookup"><span data-stu-id="4b043-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
