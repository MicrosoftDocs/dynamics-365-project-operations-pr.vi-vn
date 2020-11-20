---
title: Đóng báo giá - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đóng báo giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175737"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="a1ab6-103">Đóng báo giá - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="a1ab6-103">Close a quote - lite</span></span>

<span data-ttu-id="a1ab6-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a1ab6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1ab6-105">Báo giá dự án ở trạng thái Đã giành được hoặc Đã mất.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a1ab6-106">Các hoạt động Kích hoạt và Sửa đổi trên báo giá không được hỗ trợ trong Microsoft Dynamics 365 Project Operations. Do đó, báo giá nháp có thể bị đóng.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a1ab6-107">Đóng báo giá dưới dạng Đã giành được</span><span class="sxs-lookup"><span data-stu-id="a1ab6-107">Close a quote as Won</span></span>

<span data-ttu-id="a1ab6-108">Việc đóng báo giá dự án dưới dạng Đã giành được sẽ đóng báo giá có trạng thái được đặt thành Đã đóng và lý do dẫn đến trạng thái được đặt thành Đã giành được.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="a1ab6-109">Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc và tạo ra bản nháp hợp đồng dự án có chứa thông tin báo giá.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a1ab6-110">Vì không thể mở lại báo giá đã đóng nên hộp thoại xác nhận Có hộp thoại xác nhận trước khi thực hiện thay đổi vì không thể mở lại báo giá đã đóng và không thể khôi phục các thay đổi được.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="a1ab6-111">Nếu báo giá được đính kèm với một cơ hội, bất kỳ báo giá dự án nào khác về cơ hội sẽ tự động bị đóng dưới dạng Đã mất.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a1ab6-112">Tác động tài chính của việc đóng báo giá là Đã giành được</span><span class="sxs-lookup"><span data-stu-id="a1ab6-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a1ab6-113">Nếu có bất kỳ giá trị thời gian thực tế nào đã ghi lại trên một dự án mà vẫn còn được đính kèm với báo giá nháp, thì chỉ chi phí của thời gian hoặc chi phí được ghi lại.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a1ab6-114">Sau khi một báo giá được đóng dưới dạng Đã giành được, ứng dụng sẽ cấu trúc lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo lại giá trị chi phí thực tế mới.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a1ab6-115">Ứng dụng sẽ xử lý các giá trị chi phí thực tế này dựa trên Phương thức thanh toán của mô tả hợp đồng dự án liên quan.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a1ab6-116">Nếu các giá trị thực tế chi phí tham chiếu đến mô tả hợp đồng về vật tư và thời gian, hệ thống sẽ tự động tạo các gái trị bán hàng thực tế chưa lập hóa đơn tương ứng cho thời điểm đóng báo giá và thời điểm tạo hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a1ab6-117">Nếu các giá trị chi phí thực tế tham chiếu đến mô tả hợp đồng theo giá cố định, ứng dụng sẽ ngừng xử lý lại các giá trị chi phí thực tế dựa trên các quy tắc thanh toán chia nhỏ cho khách hàng hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a1ab6-118">Đóng báo giá dưới dạng đã mất:</span><span class="sxs-lookup"><span data-stu-id="a1ab6-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a1ab6-119">Việc đóng báo giá dự án dưới dạng Đã mất sẽ đặt trạng thái thành Đã đóng và lý do dẫn đến trạng thái thành Đã mất.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="a1ab6-120">Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a1ab6-121">Vì không thể mở lại báo giá đã đóng, vì vậy trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a1ab6-122">Nếu báo giá dự án được đóng dưới dạng Đã mất có một dự án được tham chiếu trên bất kỳ mô tả nào của dự án, thì dự án đó cũng được đánh dấu là Đã đóng và mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a1ab6-123">Trong Project Operations, việc đóng báo giá dưới dạng Đã giành được hay Đã mất sẽ không ảnh hưởng đến trạng thái đó của Cơ hội. Cơ hội sẽ vẫn mở cho đến khi được đóng theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="a1ab6-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
