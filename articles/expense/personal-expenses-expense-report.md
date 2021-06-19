---
title: Làm việc với chi phí cá nhân trên báo cáo chi phí
description: Chủ đề này cung cấp thông tin về cách làm việc với các chi phí cá nhân do nhân viên phát sinh khi đi công tác.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025710"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="2539f-103">Làm việc với chi phí cá nhân trên báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="2539f-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="2539f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="2539f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2539f-105">Trong thời gian đi công tác, một nhân viên có thể dùng thẻ tín dụng của công ty để thanh toán các chi phí cá nhân.</span><span class="sxs-lookup"><span data-stu-id="2539f-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="2539f-106">Nếu chưa có quy trình rõ ràng để xử lý các chi phí cá nhân, quy trình phê duyệt báo cáo chi phí có thể bị gián đoạn khi một nhân viên nộp báo cáo chi phí chia theo mục.</span><span class="sxs-lookup"><span data-stu-id="2539f-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="2539f-107">Có hai phương pháp bạn có thể sử dụng để giải quyết các chi phí cá nhân của nhân viên:</span><span class="sxs-lookup"><span data-stu-id="2539f-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="2539f-108">**Do nhân viên trả**: Tổ chức của bạn không thanh toán các chi phí cá nhân xuất hiện trên hóa đơn cho thẻ tín dụng công ty.</span><span class="sxs-lookup"><span data-stu-id="2539f-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2539f-109">Thay vào đó, nhân viên sẽ thanh toán trực tiếp cho nhà cung cấp thẻ tín dụng các chi phí đó.</span><span class="sxs-lookup"><span data-stu-id="2539f-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="2539f-110">**Do công ty trả**: Tổ chức của bạn thanh toán toàn bộ hóa đơn tính vào thẻ tín dụng công ty, sau đó ghi nợ các chi phí cá nhân vào tài khoản của nhân viên.</span><span class="sxs-lookup"><span data-stu-id="2539f-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2539f-111">Bạn có thể chọn phương pháp mà tổ chức sẽ sử dụng trên trang **Các tham số quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="2539f-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="2539f-112">Kích hoạt chức năng phân chia chi phí khi trường số tiền cá nhân được xác định giá trị</span><span class="sxs-lookup"><span data-stu-id="2539f-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="2539f-113">Tính năng **Kích hoạt chức năng phân chia chi phí khi trường số tiền cá nhân được xác định giá trị** chỉ áp dụng cho các báo cáo chi phí được phê duyệt bằng quy trình làm việc ở cấp độ dòng mô tả.</span><span class="sxs-lookup"><span data-stu-id="2539f-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="2539f-114">Bạn phê duyệt báo cáo bằng cách chuyển đến **Xử lý báo cáo chi phí** > **Báo cáo chi phí được giao cho tôi** > **Báo cáo chi phí mở**.</span><span class="sxs-lookup"><span data-stu-id="2539f-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="2539f-115">Để kích hoạt tính năng này, bạn hãy chuyển đến **Không gian làm việc** > **Quản lý tính năng**, chọn mục **Kích hoạt chức năng phân chia chi phí khi trường số tiền cá nhân được xác định giá trị**, rồi chọn **Kích hoạt ngay**.</span><span class="sxs-lookup"><span data-stu-id="2539f-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="2539f-116">Khi tính năng này được kích hoạt, các dòng chi phí sử dụng chức năng này sẽ tạo ra hai dòng trong quá trình gửi báo cáo.</span><span class="sxs-lookup"><span data-stu-id="2539f-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="2539f-117">Hai dòng được tạo ra để người phê duyệt có thể phê duyệt riêng từng dòng.</span><span class="sxs-lookup"><span data-stu-id="2539f-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
