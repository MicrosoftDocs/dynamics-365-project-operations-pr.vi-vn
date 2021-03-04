---
title: Đóng báo giá - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đóng báo giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764890"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="81a64-103">Đóng báo giá - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="81a64-103">Close a quote - lite</span></span>

<span data-ttu-id="81a64-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="81a64-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81a64-105">Báo giá dự án ở trạng thái Đã giành được hoặc Đã mất.</span><span class="sxs-lookup"><span data-stu-id="81a64-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="81a64-106">Báo giá nháp có thể bị đóng do các thao tác Kích hoạt và Sủa đổi trên báo giá không được hỗ trợ trong Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="81a64-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="81a64-107">Đóng báo giá dưới dạng Đã giành được</span><span class="sxs-lookup"><span data-stu-id="81a64-107">Close a quote as Won</span></span>

<span data-ttu-id="81a64-108">Khi đóng báo giá dưới dạng Giành được, trạng thái sẽ được chuyển sang Đã đóng và lý do dẫn đến trạng thái là Giành được.</span><span class="sxs-lookup"><span data-stu-id="81a64-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="81a64-109">Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc và tạo ra bản nháp hợp đồng dự án có chứa thông tin báo giá.</span><span class="sxs-lookup"><span data-stu-id="81a64-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="81a64-110">Do không thể mở báo giá đã đóng, một hộp thoại sẽ hiện lên để xác nhận các thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="81a64-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="81a64-111">Nếu báo giá được đính kèm với một cơ hội, bất kỳ báo giá dự án nào khác về cơ hội sẽ tự động bị đóng dưới dạng Đã mất.</span><span class="sxs-lookup"><span data-stu-id="81a64-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="81a64-112">Tác động tài chính của việc đóng báo giá là Đã giành được</span><span class="sxs-lookup"><span data-stu-id="81a64-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="81a64-113">Nếu có giá trị thực nào của thời gian trên một dự án trong khi vẫn đính kèm vào báo giá nháp, thì hệ thống sẽ chỉ ghi lại chi phí thời gian hoặc khoản chi tiêu.</span><span class="sxs-lookup"><span data-stu-id="81a64-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="81a64-114">Sau khi một báo giá được đóng dưới dạng Đã giành được, ứng dụng sẽ cấu trúc lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo lại giá trị chi phí thực tế mới.</span><span class="sxs-lookup"><span data-stu-id="81a64-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="81a64-115">Ứng dụng sẽ xử lý các giá trị chi phí thực tế này dựa trên Phương thức thanh toán của mô tả hợp đồng dự án liên quan.</span><span class="sxs-lookup"><span data-stu-id="81a64-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="81a64-116">Nếu các giá trị thực của chi phí tham chiếu một dòng mô tả về thời gian và nguyên vật liệu trên hợp đồng, các giá trị thực của giao dịch chưa lập hóa đơn sẽ được tạo khi báo giá bị đóng và hợp đồng dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="81a64-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="81a64-117">Nếu các giá trị thực của chi phí tham chiếu một dòng mô tả về giá cố định trên hợp đồng, thì ứng dụng sẽ ngừng xử lý lại các giá trị thực của chi phí được dựa trên quy tắc phân tách hóa đơn dành cho khách hàng trong hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="81a64-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="81a64-118">Đóng báo giá dưới dạng đã mất:</span><span class="sxs-lookup"><span data-stu-id="81a64-118">Closing a quote as lost:</span></span>

<span data-ttu-id="81a64-119">Khi đóng báo giá dưới dạng Đã mất, trạng thái sẽ được chuyển sang Đã đóng và lý do dẫn đến trạng thái là Đã mất.</span><span class="sxs-lookup"><span data-stu-id="81a64-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="81a64-120">Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="81a64-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="81a64-121">Vì không thể mở lại báo giá đã đóng, vì vậy trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="81a64-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="81a64-122">Nếu có báo giá đóng dưới dạng Đã mất tham chiếu một dự án trên dòng bất kỳ, thì dự án đó cũng sẽ được đánh dấu là Đã đóng.</span><span class="sxs-lookup"><span data-stu-id="81a64-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="81a64-123">Mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.</span><span class="sxs-lookup"><span data-stu-id="81a64-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="81a64-124">Trong Project Operations, việc đóng báo giá dưới dạng Đã giành được hay Đã mất sẽ không ảnh hưởng đến trạng thái đó của Cơ hội. Cơ hội sẽ vẫn mở cho đến khi được đóng theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="81a64-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
