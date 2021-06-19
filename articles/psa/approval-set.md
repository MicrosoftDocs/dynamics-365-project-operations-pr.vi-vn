---
title: Bộ phê duyệt
description: Chủ đề này cung cấp thông tin về bộ phê duyệt, yêu cầu và tập hợp con của các thao tác đó.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116897"
---
# <a name="approval-sets"></a><span data-ttu-id="3ea82-103">Bộ phê duyệt</span><span class="sxs-lookup"><span data-stu-id="3ea82-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3ea82-104">Bộ phê duyệt có tác dụng nhóm các yêu cầu phê duyệt lại với nhau thành các tập hợp thao tác nhỏ hơn.</span><span class="sxs-lookup"><span data-stu-id="3ea82-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="3ea82-105">Việc lập nhóm này giúp cho tính năng Dự án xử lý các mục phê duyệt theo thứ tự, cũng như cho phép thử lại và sắp xếp theo trình tự.</span><span class="sxs-lookup"><span data-stu-id="3ea82-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="3ea82-106">Việc lập nhóm sẽ cải thiện độ tin cậy và khả năng truy nguyên của quá trình phê duyệt đối với khối lượng phê duyệt lớn.</span><span class="sxs-lookup"><span data-stu-id="3ea82-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="3ea82-107">Các bộ phê duyệt cho biết trạng thái xử lý tổng thể của các bản ghi liên quan.</span><span class="sxs-lookup"><span data-stu-id="3ea82-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="3ea82-108">Khi một bản ghi phê duyệt được xử lý bằng bộ phê duyệt, bản ghi đó sẽ chuyển từ **Đã gửi** thành **Đã phê duyệt** và được hủy liên kết khỏi bộ phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3ea82-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="3ea82-109">Nếu bản ghi đã gửi không được phê duyệt, thì bản ghi đó vẫn ở trạng thái **Đã gửi** và bộ phê duyệt được đánh dấu là không thành công.</span><span class="sxs-lookup"><span data-stu-id="3ea82-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="3ea82-110">Bộ phê duyệt ghi lại thông báo lỗi về sự thất bại đó.</span><span class="sxs-lookup"><span data-stu-id="3ea82-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="3ea82-111">Xử lý mục phê duyệt và bộ phê duyệt</span><span class="sxs-lookup"><span data-stu-id="3ea82-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="3ea82-112">Các mục phê duyệt được xếp hàng đợi để xử lý sẽ xuất hiện ở dạng xem **Xử lý mục phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="3ea82-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="3ea82-113">Hệ thống sẽ cố gắng xử lý không đồng bộ tất cả các mục nhập nhiều lần, kể cả việc thử lại mục phê duyệt nếu những lần thử trước không thành công.</span><span class="sxs-lookup"><span data-stu-id="3ea82-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="3ea82-114">Trường **Thời gian tồn tại của bộ phê duyệt** ghi lại số lần thử còn lại để xử lý bộ phê duyệt trước khi mục này được đánh dấu là không thành công.</span><span class="sxs-lookup"><span data-stu-id="3ea82-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="3ea82-115">Mục phê duyệt và bộ phê duyệt không thành công</span><span class="sxs-lookup"><span data-stu-id="3ea82-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="3ea82-116">Dạng xem **Mục phê duyệt không thành công** liệt kê tất cả các mục phê duyệt cần có sự can thiệp của người dùng.</span><span class="sxs-lookup"><span data-stu-id="3ea82-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="3ea82-117">Hãy mở nhật ký bộ phê duyệt được liên kết để xác định nguyên nhân của sự thất bại.</span><span class="sxs-lookup"><span data-stu-id="3ea82-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="3ea82-118">Thao tác chọn **Thử lại** sẽ tăng số lần trong thời gian tồn tại của bộ phê duyệt, chuyển bộ phê duyệt trở lại trạng thái **Đang xử lý** và cố gắng xử lý các bản ghi còn lại.</span><span class="sxs-lookup"><span data-stu-id="3ea82-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="3ea82-119">Đặt cấu hình bộ phê duyệt</span><span class="sxs-lookup"><span data-stu-id="3ea82-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="3ea82-120">Bật tính năng Bộ phê duyệt</span><span class="sxs-lookup"><span data-stu-id="3ea82-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="3ea82-121">Trước khi bạn bật tính năng Bộ phê duyệt, hãy xác minh rằng không có mục phê duyệt nào hiện đang được xử lý.</span><span class="sxs-lookup"><span data-stu-id="3ea82-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="3ea82-122">Chuyển đến trang **Thông số dự án** và chọn **Kiểm soát tính năng** > **Bật phê duyệt hiện đại**.</span><span class="sxs-lookup"><span data-stu-id="3ea82-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="3ea82-123">Tắt tính năng Bộ phê duyệt</span><span class="sxs-lookup"><span data-stu-id="3ea82-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="3ea82-124">Trước khi bạn tắt tính năng Bộ phê duyệt, hãy xác minh rằng không có mục phê duyệt nào hiện đang được xử lý.</span><span class="sxs-lookup"><span data-stu-id="3ea82-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="3ea82-125">Chuyển đến trang **Thông số dự án** và chọn **Kiểm soát tính năng** > **Tắt phê duyệt hiện đại**.</span><span class="sxs-lookup"><span data-stu-id="3ea82-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="3ea82-126">Định cấu hình ngưỡng không đồng bộ</span><span class="sxs-lookup"><span data-stu-id="3ea82-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="3ea82-127">Khi các bộ phê duyệt được tạo, quá trình xử lý sẽ chuyển sang nền khi số lượng bản ghi đã chọn để phê duyệt vượt quá ngưỡng được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="3ea82-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="3ea82-128">Sử dụng trường **Ngưỡng không đồng thời** để đặt cấu hình khi nào hoạt động xử lý phê duyệt nên chạy đồng bộ hoặc không đồng bộ.</span><span class="sxs-lookup"><span data-stu-id="3ea82-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="3ea82-129">Các giá trị hợp lệ là:</span><span class="sxs-lookup"><span data-stu-id="3ea82-129">Valid values are:</span></span>

  - <span data-ttu-id="3ea82-130">Không: Tất cả các yêu cầu phải được xử lý không đồng bộ.</span><span class="sxs-lookup"><span data-stu-id="3ea82-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="3ea82-131">Số lớn hơn 0: Các mục phê duyệt chỉ được xử lý không đồng bộ khi số lượng mục phê duyệt đã gửi vượt quá giá trị này.</span><span class="sxs-lookup"><span data-stu-id="3ea82-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
