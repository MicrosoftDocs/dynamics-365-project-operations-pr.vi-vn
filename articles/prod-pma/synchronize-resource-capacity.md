---
title: Đồng bộ hóa năng lực của nguồn lực
description: Chủ đề này cung cấp thông tin về cách đồng bộ hóa năng lực của nguồn lực trên lịch và dự án.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997537"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="7a518-103">Đồng bộ hóa năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="7a518-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a518-104">Các quy trình đồng bộ hóa nguồn lực giúp đảm bảo rằng thông tin cho lịch lịch và lịch cơ sở sẽ dần đi vào quá trình lập lịch trình nguồn lực dự án.</span><span class="sxs-lookup"><span data-stu-id="7a518-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="7a518-105">Nếu lịch bị thay đổi, các quy trình sẽ thực hiện cập nhật bắt buộc đối với việc lập lịch trình các nguồn lực dự án.</span><span class="sxs-lookup"><span data-stu-id="7a518-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="7a518-106">Các quy trình cũng giúp cải thiện hiệu suất, vì thông tin nguồn lực của lịch được đồng bộ hóa trước.</span><span class="sxs-lookup"><span data-stu-id="7a518-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="7a518-107">Do đó, việc cập nhật thông tin lập lịch nguồn lực diễn ra nhanh hơn.</span><span class="sxs-lookup"><span data-stu-id="7a518-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="7a518-108">Chúng tôi khuyên bạn nên lập lịch các quy trình theo loạt thay vì từng lần một.</span><span class="sxs-lookup"><span data-stu-id="7a518-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="7a518-109">Nếu không, ai đó có thể quên những ngày được bao gồm khi thông tin được đồng bộ hóa lần gần nhất.</span><span class="sxs-lookup"><span data-stu-id="7a518-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="7a518-110">Nếu các ngày bao gồm không được sử dụng, khoảng trống có thể xảy ra trong quá trình đồng bộ hóa ngày.</span><span class="sxs-lookup"><span data-stu-id="7a518-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Đồng bộ hóa lịch](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="7a518-112">Đồng bồ hóa tổng hợp năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="7a518-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="7a518-113">Quá trình đồng bộ hóa được thiết kế để đồng bộ hóa tất cả thông tin lịch nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7a518-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="7a518-114">Thông tin này bao gồm thông tin lịch cơ sở về bất kỳ thay đổi nào đối với bảng năng lực lịch nguồn lực của dự án.</span><span class="sxs-lookup"><span data-stu-id="7a518-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="7a518-115">Nếu các nguồn lực mới được thêm vào dự án, quá trình đồng bộ hóa sẽ đảm bảo rằng thông tin lịch cập nhật có sẵn.</span><span class="sxs-lookup"><span data-stu-id="7a518-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="7a518-116">Việc đồng bộ hóa này có thể được thực hiện bất cứ lúc nào.</span><span class="sxs-lookup"><span data-stu-id="7a518-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="7a518-117">Chúng tôi khuyên bạn nên sử dụng loạt.</span><span class="sxs-lookup"><span data-stu-id="7a518-117">We recommend that you use a batch.</span></span> <span data-ttu-id="7a518-118">Các tùy chọn có sẵn trong quá trình đồng bộ hóa các mục dự trữ năng lực.</span><span class="sxs-lookup"><span data-stu-id="7a518-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="7a518-119">Chọn **Quản lý dự án và kế toán** &gt; **Định kỳ** &gt; **Đồng bộ hóa năng lực** &gt; **Đồng bộ hóa tổng hợp năng lực của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="7a518-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="7a518-120">Thiết lập các tùy chọn trong bảng sau.</span><span class="sxs-lookup"><span data-stu-id="7a518-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="7a518-121">Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="7a518-121">Option</span></span>      | <span data-ttu-id="7a518-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="7a518-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="7a518-123">Mã thời kỳ</span><span class="sxs-lookup"><span data-stu-id="7a518-123">Period code</span></span> | <span data-ttu-id="7a518-124">Tùy ý chọn mã khoảng ngày của sổ cái chung để đặt ngày bắt đầu và ngày kết thúc cho quá trình đồng bộ hóa cho tổng hợp năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7a518-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7a518-125">Ngày bắt đầu</span><span class="sxs-lookup"><span data-stu-id="7a518-125">Start date</span></span>  | <span data-ttu-id="7a518-126">Nhập ngày bắt đầu cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7a518-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7a518-127">Ngày kết thúc</span><span class="sxs-lookup"><span data-stu-id="7a518-127">End date</span></span>    | <span data-ttu-id="7a518-128">Nhập ngày kết thúc cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7a518-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="7a518-129">[![Quá trình đồng bộ hóa](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a518-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]