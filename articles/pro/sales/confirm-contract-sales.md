---
title: Xác nhận hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách xác nhận hợp đồng trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128313"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="287bb-103">Xác nhận hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="287bb-103">Confirm a project contract</span></span>

<span data-ttu-id="287bb-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="287bb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="287bb-105">Hợp đồng dự án trong Dynamics 365 Project Operations có thể ở trạng thái hiện hoạt với lý do **Đã xác nhận** hoặc bị đóng với lý do **Đã mất**.</span><span class="sxs-lookup"><span data-stu-id="287bb-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="287bb-106">Khi bạn xác nhận hợp đồng dự án, trạng thái sẽ được cập nhật từ **Bản nháp** thành **Hiện hoạt** và lý do dẫn đến trạng thái là **Đã xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="287bb-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="287bb-107">Bạn không thể chỉnh sửa hoặc mở lại hợp đồng hiện hoạt hoặc đã đóng.</span><span class="sxs-lookup"><span data-stu-id="287bb-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="287bb-108">Tác động tài chính của việc xác nhận hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="287bb-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="287bb-109">Sau khi hợp đồng dự án được xác nhận, ứng dụng sẽ tính lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo giá trị chi phí thực tế mới.</span><span class="sxs-lookup"><span data-stu-id="287bb-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="287bb-110">Sau đó, giá trị chi phí thực tế mới được xử lý dựa trên phương thức thanh toán của mục mô tả hợp đồng dự án được liên kết.</span><span class="sxs-lookup"><span data-stu-id="287bb-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="287bb-111">Nếu giá trị chi phí thực tế tham chiếu đến mục mô tả hợp đồng Thời gian và vật tư, thì ứng dụng sẽ tự động tạo lại các giá trị thực tế doanh số chưa lập hóa đơn tương ứng.</span><span class="sxs-lookup"><span data-stu-id="287bb-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="287bb-112">Nếu các giá trị chi phí thực tế tham chiếu đến mục mô tả hợp đồng Giá cố định, thì ứng dụng sẽ ngừng xử lý lại giá trị chi phí thực tế.</span><span class="sxs-lookup"><span data-stu-id="287bb-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="287bb-113">Giới hạn không vượt quá, mục thiết lập khả năng tính phí, giá và chi phí trên giá trị thực tế sẽ được đánh giá và sau đó được cập nhật trong quy trình xác nhận.</span><span class="sxs-lookup"><span data-stu-id="287bb-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="287bb-114">Đóng hợp đồng dự án ở dạng đã mất</span><span class="sxs-lookup"><span data-stu-id="287bb-114">Close a project contract as lost</span></span>

<span data-ttu-id="287bb-115">Khi bạn đóng hợp đồng dự án ở dạng đã mất, trạng thái hợp đồng được cập nhật thành **Đã đóng** và lý do dẫn đến trạng thái là **Đã mất**.</span><span class="sxs-lookup"><span data-stu-id="287bb-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="287bb-116">Hợp đồng dự án trở thành dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="287bb-116">The project contract becomes read-only.</span></span> <span data-ttu-id="287bb-117">Hộp thoại xác nhận được cung cấp trước khi các thay đổi hoàn tất, vì bạn không thể mở lại hợp đồng dự án đã đóng.</span><span class="sxs-lookup"><span data-stu-id="287bb-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="287bb-118">Nếu hợp đồng dự án đã đóng ở dạng bị mất tham chiếu đến một dự án trên các mục mô tả của nó, thì dự án đó cũng được đánh dấu là đã đóng.</span><span class="sxs-lookup"><span data-stu-id="287bb-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="287bb-119">Mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.</span><span class="sxs-lookup"><span data-stu-id="287bb-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="287bb-120">Nếu có giá trị thực tế doanh số chưa lập hóa đơn nào trong hợp đồng dự án chưa được đưa vào hóa đơn, thì mục đó sẽ được đảo ngược.</span><span class="sxs-lookup"><span data-stu-id="287bb-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="287bb-121">Trong Dynamics 365 Project Operations, việc đóng hợp đồng dự án ở dạng bị mất sẽ không ảnh hưởng đến trạng thái của cơ hội được liên kết.</span><span class="sxs-lookup"><span data-stu-id="287bb-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="287bb-122">Cơ hội sẽ vẫn mở và phải được đóng thủ công.</span><span class="sxs-lookup"><span data-stu-id="287bb-122">The opportunity will remain open and must be manually closed.</span></span>
