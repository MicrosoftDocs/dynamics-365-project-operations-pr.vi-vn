---
title: Đóng báo giá
description: Chủ đề này cung cấp thông tin về cách đóng báo giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277274"
---
# <a name="close-a-quote"></a><span data-ttu-id="e524b-103">Đóng báo giá</span><span class="sxs-lookup"><span data-stu-id="e524b-103">Close a quote</span></span>

<span data-ttu-id="e524b-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="e524b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e524b-105">Báo giá dự án ở trạng thái Đã giành được hoặc Đã mất.</span><span class="sxs-lookup"><span data-stu-id="e524b-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="e524b-106">Do các chức năng Kích hoạt và Xem lại không được hỗ trợ trên báo giá trong Microsoft Dynamics 365 Project Operations, bạn có thể đóng báo giá nháp.</span><span class="sxs-lookup"><span data-stu-id="e524b-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="e524b-107">Đóng báo giá dưới dạng Đã giành được</span><span class="sxs-lookup"><span data-stu-id="e524b-107">Close a quote as Won</span></span>

<span data-ttu-id="e524b-108">Việc đóng báo giá dự án dưới dạng Đã giành được sẽ đặt trạng thái báo giá thành **Đã đóng** và lý do dẫn đến trạng thái được đặt thành **Đã giành được**.</span><span class="sxs-lookup"><span data-stu-id="e524b-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="e524b-109">Việc đóng báo giá làm cho báo giá ở chế độ chỉ đọc và tạo ra bản nháp hợp đồng dự án có chứa tất cả thông tin báo giá.</span><span class="sxs-lookup"><span data-stu-id="e524b-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="e524b-110">Vì không thể mở lại báo giá đã đóng nên trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="e524b-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e524b-111">Hợp đồng dự án được tạo từ báo giá dự án cũng có sẵn trong mô-đun kế toán và quản lý dự án của Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e524b-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="e524b-112">Nếu hợp đồng dự án không được ánh xạ tới một dự án trên mọi mô tả hợp đồng, thì hợp đồng dự án này sẽ được cung cấp dưới dạng hợp đồng dự án không hoạt động và có hiệu lực ngay khi dự án được ánh xạ tới ít nhất một trong các mô tả hợp đồng của dự án đó.</span><span class="sxs-lookup"><span data-stu-id="e524b-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="e524b-113">Nếu báo giá được đính kèm với một cơ hội, bất kỳ báo giá dự án nào khác về cơ hội sẽ tự động bị đóng dưới dạng Đã mất.</span><span class="sxs-lookup"><span data-stu-id="e524b-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="e524b-114">Tác động tài chính của việc đóng báo giá là Đã giành được</span><span class="sxs-lookup"><span data-stu-id="e524b-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="e524b-115">Nếu có bất kỳ giá trị thời gian thực tế nào đã ghi lại trên một dự án mà vẫn còn được đính kèm với báo giá nháp, thì chỉ chi phí của thời gian hoặc chi phí được ghi lại.</span><span class="sxs-lookup"><span data-stu-id="e524b-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="e524b-116">Sau khi một báo giá được đóng dưới dạng Đã giành được, ứng dụng sẽ cấu trúc lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo lại giá trị chi phí thực tế mới.</span><span class="sxs-lookup"><span data-stu-id="e524b-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="e524b-117">Ứng dụng sẽ xử lý các giá trị chi phí thực tế này dựa trên Phương thức thanh toán của mô tả hợp đồng dự án liên quan.</span><span class="sxs-lookup"><span data-stu-id="e524b-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="e524b-118">Nếu các giá trị thực tế chi phí tham chiếu đến mô tả hợp đồng về vật tư và thời gian, hệ thống sẽ tự động tạo các gái trị bán hàng thực tế chưa lập hóa đơn tương ứng cho thời điểm đóng báo giá và thời điểm tạo hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e524b-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="e524b-119">Nếu các giá trị chi phí thực tế tham chiếu đến mô tả hợp đồng theo giá cố định, ứng dụng sẽ ngừng xử lý lại các giá trị chi phí thực tế dựa trên các quy tắc thanh toán chia nhỏ cho khách hàng hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="e524b-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="e524b-120">Tất cả các giá trị thực tế đã được xử lý lại đều có trong mô-đun kế toán và quản lý dự án để xem xét, cập nhật và đăng lên sổ cái.</span><span class="sxs-lookup"><span data-stu-id="e524b-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="e524b-121">Đóng báo giá dưới dạng Đã mất</span><span class="sxs-lookup"><span data-stu-id="e524b-121">Close a quote as Lost</span></span>

<span data-ttu-id="e524b-122">Việc đóng báo giá dự án dưới dạng **Đã mất** sẽ đặt trạng thái thành Đã đóng và lý do dẫn đến trạng thái thành **Đã mất**.</span><span class="sxs-lookup"><span data-stu-id="e524b-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="e524b-123">Việc đóng báo giá làm cho báo giá ở chế độ chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="e524b-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="e524b-124">Vì không thể mở lại báo giá đã đóng, vì vậy trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="e524b-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e524b-125">Nếu báo giá dự án được đóng dưới dạng Đã mất có một dự án được tham chiếu trên bất kỳ mô tả nào của dự án, thì dự án đó cũng được đánh dấu là Đã đóng và mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.</span><span class="sxs-lookup"><span data-stu-id="e524b-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="e524b-126">Trong Project Operations, việc đóng báo giá dưới dạng Đã giành được hay Đã mất sẽ không ảnh hưởng đến trạng thái đó của Cơ hội. Cơ hội sẽ vẫn mở cho đến khi được đóng theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="e524b-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]