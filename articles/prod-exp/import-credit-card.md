---
title: Nhập và duy trì các giao dịch thẻ tín dụng
description: Chủ đề này giải thích cách nhập và duy trì các giao dịch thẻ tín dụng liên quan đến chi phí. Bạn có thể thiết lập để các giao dịch này được nhập tự động theo lịch trình định kỳ hoặc được nhập thủ công khi cần.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271604"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="9936a-104">Nhập và duy trì các giao dịch thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="9936a-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="9936a-105">Các giao dịch thẻ tín dụng liên quan đến chi phí có thể được thiết lập để tự động nhập vào theo lịch trình định kỳ.</span><span class="sxs-lookup"><span data-stu-id="9936a-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="9936a-106">Ngoài ra, có thể nhập giao dịch theo cách thủ công khi cần.</span><span class="sxs-lookup"><span data-stu-id="9936a-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="9936a-107">Các giao dịch thẻ tín dụng được nhập thông qua thực thể dữ liệu giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="9936a-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="9936a-108">Để biết thêm thông tin về thực thể dữ liệu, hãy xem [Thực thể dữ liệu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="9936a-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="9936a-109">Nhập giao dịch thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="9936a-109">Import credit card transactions</span></span>

1. <span data-ttu-id="9936a-110">Trên trang **Giao dịch thẻ tín dụng**, chọn **Nhập giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="9936a-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="9936a-111">Nếu bạn mở tác vụ quản lý dữ liệu lần đầu tiên, hệ thống phải cập nhật danh sách các thực thể dữ liệu trước khi bạn có thể tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="9936a-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="9936a-112">Trong trường **Tên**, nhập mô tả riêng của tác vụ nhập.</span><span class="sxs-lookup"><span data-stu-id="9936a-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="9936a-113">Trong trường **Định dạng dữ liệu nguồn**, chọn định dạng của tệp chứa giao dịch thẻ tín dụng để nhập.</span><span class="sxs-lookup"><span data-stu-id="9936a-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="9936a-114">Chọn **Tải lên** rồi tìm và chọn tệp để nhập.</span><span class="sxs-lookup"><span data-stu-id="9936a-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="9936a-115">Sau khi tệp đã được tải lên, hãy xác thực ánh xạ của tệp giao dịch thẻ tín dụng và các cột của thực thể dữ liệu giao dịch thẻ tín dụng bằng cách chọn liên kết **Xem bản đồ** trên ngăn xếp.</span><span class="sxs-lookup"><span data-stu-id="9936a-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="9936a-116">Nếu có lỗi ánh xạ hoặc nếu bạn phải thay đổi ánh xạ, hãy thực hiện các thay đổi về ánh xạ trong tab **Trực quan hóa ánh xạ** hoặc tab **Chi tiết ánh xạ**.</span><span class="sxs-lookup"><span data-stu-id="9936a-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="9936a-117">Để tự động hóa các giao dịch thẻ tín dụng, hãy chọn **Tạo tác vụ dữ liệu định kỳ**.</span><span class="sxs-lookup"><span data-stu-id="9936a-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="9936a-118">Sau đó, bạn có thể đặt mức lặp lại để xác định tần suất nhập giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="9936a-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="9936a-119">Sau khi hoàn tất, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="9936a-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="9936a-120">Để nhập tệp đã chọn ngay bây giờ, hãy chọn **Nhập**.</span><span class="sxs-lookup"><span data-stu-id="9936a-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="9936a-121">Nếu lỗi xảy ra trong quá trình nhập, bạn có thể xem nhật ký thực thi hoặc dữ liệu giai đoạn, tại đó có các lỗi mà bạn phải sửa để đảm bảo quá trình nhập diễn ra thành công.</span><span class="sxs-lookup"><span data-stu-id="9936a-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="9936a-122">Nếu bạn phải nhập nhiều định dạng tệp, bạn phải tạo tác vụ nhập riêng cho từng loại định dạng.</span><span class="sxs-lookup"><span data-stu-id="9936a-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="9936a-123">Chỉ định lại giao dịch thẻ tín dụng cho nhân viên bị chấm dứt hồ sơ</span><span class="sxs-lookup"><span data-stu-id="9936a-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="9936a-124">Sau khi hồ sơ nhân viên bị chấm dứt, tài khoản Dịch vụ miền Active Directory (AD DS) của nhân viên đó sẽ bị vô hiệu hóa.</span><span class="sxs-lookup"><span data-stu-id="9936a-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="9936a-125">Tuy nhiên, có thể có các giao dịch thẻ tín dụng đang hoạt động vẫn phải được chi tiêu và hoàn trả.</span><span class="sxs-lookup"><span data-stu-id="9936a-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="9936a-126">Từ trang **Giao dịch thẻ tín dụng**, bạn có thể chỉ định lại nhân viên cho bất kỳ giao dịch thẻ tín dụng nào mà nhân viên liên quan đã bị chấm dứt hồ sơ.</span><span class="sxs-lookup"><span data-stu-id="9936a-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="9936a-127">Chọn một hoặc nhiều giao dịch thẻ tín dụng, sau đó chọn **Chỉ định lại giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="9936a-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="9936a-128">Sau đó, bạn có thể chọn một nhân viên khác để chỉ định giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="9936a-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="9936a-129">Sau khi chỉ định lại giao dịch thẻ tín dụng, bạn có thể chọn các giao dịch đó cho báo cáo chi phí và được thanh toán theo quy trình hoàn trả báo cáo chi phí thông thường.</span><span class="sxs-lookup"><span data-stu-id="9936a-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]