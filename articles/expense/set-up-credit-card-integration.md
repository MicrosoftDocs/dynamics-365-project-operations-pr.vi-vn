---
title: Thiết lập phần tích hợp thẻ tín dụng
description: Chủ đề này giải thích cách nhập và duy trì các giao dịch thẻ tín dụng liên quan đến chi phí.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120884"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="3fc34-103">Thiết lập phần tích hợp thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="3fc34-103">Set up credit card integration</span></span>

<span data-ttu-id="3fc34-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="3fc34-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3fc34-105">Các giao dịch thẻ tín dụng liên quan đến chi phí có thể được thiết lập để tự động nhập vào theo lịch trình định kỳ.</span><span class="sxs-lookup"><span data-stu-id="3fc34-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3fc34-106">Ngoài ra, có thể nhập giao dịch theo cách thủ công khi cần.</span><span class="sxs-lookup"><span data-stu-id="3fc34-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3fc34-107">Các giao dịch thẻ tín dụng được nhập thông qua thực thể dữ liệu giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="3fc34-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3fc34-108">Nhập giao dịch thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="3fc34-108">Import credit card transactions</span></span>

1. <span data-ttu-id="3fc34-109">Trên trang **Giao dịch thẻ tín dụng**, chọn **Nhập giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3fc34-110">Nếu bạn mở tác vụ quản lý dữ liệu lần đầu tiên, hệ thống phải cập nhật danh sách các thực thể dữ liệu trước khi bạn có thể tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="3fc34-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3fc34-111">Trong trường **Tên**, nhập mô tả riêng của tác vụ nhập.</span><span class="sxs-lookup"><span data-stu-id="3fc34-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="3fc34-112">Trong trường **Định dạng dữ liệu nguồn**, chọn định dạng của tệp chứa giao dịch thẻ tín dụng để nhập.</span><span class="sxs-lookup"><span data-stu-id="3fc34-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3fc34-113">Chọn **Tải lên** rồi tìm và chọn tệp để nhập.</span><span class="sxs-lookup"><span data-stu-id="3fc34-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3fc34-114">Sau khi tệp đã được tải lên, hãy xác thực ánh xạ của tệp giao dịch thẻ tín dụng và các cột của thực thể dữ liệu giao dịch thẻ tín dụng bằng cách chọn liên kết **Xem bản đồ** trên ngăn xếp.</span><span class="sxs-lookup"><span data-stu-id="3fc34-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3fc34-115">Nếu có lỗi ánh xạ hoặc nếu bạn phải thay đổi ánh xạ, hãy thực hiện các thay đổi về ánh xạ trong tab **Trực quan hóa ánh xạ** hoặc tab **Chi tiết ánh xạ**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3fc34-116">Để tự động hóa các giao dịch thẻ tín dụng, hãy chọn **Tạo tác vụ dữ liệu định kỳ**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3fc34-117">Sau đó, bạn có thể đặt mức lặp lại để xác định tần suất nhập giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="3fc34-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3fc34-118">Sau khi hoàn tất, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3fc34-119">Để nhập tệp đã chọn ngay bây giờ, hãy chọn **Nhập**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3fc34-120">Nếu lỗi xảy ra trong quá trình nhập, bạn có thể xem nhật ký thực thi hoặc dữ liệu giai đoạn, tại đó có các lỗi mà bạn phải sửa để đảm bảo quá trình nhập diễn ra thành công.</span><span class="sxs-lookup"><span data-stu-id="3fc34-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3fc34-121">Nếu bạn phải nhập nhiều định dạng tệp, bạn phải tạo tác vụ nhập riêng cho từng loại định dạng.</span><span class="sxs-lookup"><span data-stu-id="3fc34-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3fc34-122">Chỉ định lại giao dịch thẻ tín dụng cho nhân viên bị chấm dứt hồ sơ</span><span class="sxs-lookup"><span data-stu-id="3fc34-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3fc34-123">Sau khi hồ sơ nhân viên bị chấm dứt, tài khoản Dịch vụ miền Active Directory (AD DS) của nhân viên đó sẽ bị vô hiệu hóa.</span><span class="sxs-lookup"><span data-stu-id="3fc34-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3fc34-124">Tuy nhiên, có thể có các giao dịch thẻ tín dụng đang hoạt động vẫn phải được chi tiêu và hoàn trả.</span><span class="sxs-lookup"><span data-stu-id="3fc34-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3fc34-125">Từ trang **Giao dịch thẻ tín dụng**, bạn có thể chỉ định lại nhân viên cho bất kỳ giao dịch thẻ tín dụng nào mà nhân viên liên quan đã bị chấm dứt hồ sơ.</span><span class="sxs-lookup"><span data-stu-id="3fc34-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3fc34-126">Chọn một hoặc nhiều giao dịch thẻ tín dụng, sau đó chọn **Chỉ định lại giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="3fc34-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3fc34-127">Sau đó, bạn có thể chọn một nhân viên khác để chỉ định giao dịch thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="3fc34-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3fc34-128">Sau khi chỉ định lại giao dịch thẻ tín dụng, bạn có thể chọn các giao dịch đó cho báo cáo chi phí và được thanh toán theo quy trình hoàn trả báo cáo chi phí thông thường.</span><span class="sxs-lookup"><span data-stu-id="3fc34-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
