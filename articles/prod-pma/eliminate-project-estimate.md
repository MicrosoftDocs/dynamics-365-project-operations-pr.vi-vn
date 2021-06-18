---
title: Loại bỏ giá trị ước tính dự án
description: Chủ đề này cung cấp thông tin về việc loại bỏ giá trị ước tính dự án sau khi hoàn thành.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006942"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="8bc93-103">Loại bỏ giá trị ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="8bc93-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc93-104">Giá trị ước tính dự án cung cấp dạng xem tài chính cho công việc được ước tính và lập lịch trình cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="8bc93-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="8bc93-105">Để làm việc với các giá trị ước tính cho dự án, bạn phải đính kèm dự án ấy với một dự án ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="8bc93-106">Dự án ước tính luôn dựa trên một dự án hiện có, tuy nhiên, nhiều dự án có thể tham chiếu một dự án ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="8bc93-107">Chỉ dự án đầu tư và giá cố định mới có thể được đính kèm với dự toán và các dự án đó phải nằm trong cùng nhóm dự án với dự án ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="8bc93-108">Để loại bỏ một dự án ước tính, dự án đó phải được hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="8bc93-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="8bc93-109">Các bước sau đây giải thích cách loại bỏ giá trị ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="8bc93-110">Chuyển tới **Quản lý dự án và kế toán** > **Tất cả dự án** và mở dự án.</span><span class="sxs-lookup"><span data-stu-id="8bc93-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="8bc93-111">Chọn **Ước tính** trên tab **Quản lý** và trên trang **Ước tính**, hãy chọn **Loại bỏ**.</span><span class="sxs-lookup"><span data-stu-id="8bc93-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="8bc93-112">Trên trang **Loại bỏ giá trị ước tính** ở tab **Tổng quát**, hãy đặt các tùy chọn sau:</span><span class="sxs-lookup"><span data-stu-id="8bc93-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="8bc93-113">**Mã kỳ**: Chọn mã kỳ để chọn các dự án ước tính phù hợp.</span><span class="sxs-lookup"><span data-stu-id="8bc93-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="8bc93-114">**Ngày ước tính**: Chọn ngày ước tính thích hợp cần loại bỏ.</span><span class="sxs-lookup"><span data-stu-id="8bc93-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="8bc93-115">**Loại bỏ với cảnh báo WIP**: Kích hoạt tùy chọn này để cung cấp thông báo khi giá trị ước tính sẽ loại bỏ được liên kết với công việc đang tiến hành (WIP).</span><span class="sxs-lookup"><span data-stu-id="8bc93-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="8bc93-116">Khi tùy chọn này không được kích hoạt, hoạt động loại bỏ sẽ không thể tiếp tục nếu tồn tại bất kỳ giao dịch không ước tính nào.</span><span class="sxs-lookup"><span data-stu-id="8bc93-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="8bc93-117">Tùy chọn này chỉ khả dụng khi hoạt động loại bỏ được áp dụng cho dự án ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="8bc93-118">Tùy chọn này không có sẵn nếu bạn sử dụng mục đăng định kỳ.</span><span class="sxs-lookup"><span data-stu-id="8bc93-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="8bc93-119">Mục thiết đặt này hoạt động với mục thiết đặt trên tab **Ước tính** ở trang **Tham số dự án**, trong nhóm trường **Cho phép loại bỏ khi tồn tại giao dịch không ước tính**.</span><span class="sxs-lookup"><span data-stu-id="8bc93-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="8bc93-120">**Đặt giai đoạn thành Đã kết thúc**: Kích hoạt tùy chọn này để đặt giai đoạn của dự án ước tính thành **Đã kết thúc** sau khi bạn chạy hoạt động loại bỏ.</span><span class="sxs-lookup"><span data-stu-id="8bc93-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="8bc93-121">**In danh sách giá trị ước tính**: Chọn thông tin sẽ đưa vào khi in danh sách giá trị ước tính.</span><span class="sxs-lookup"><span data-stu-id="8bc93-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="8bc93-122">**Hiển thị Infolog**: Kích hoạt tùy chọn này để hiển thị Infolog.</span><span class="sxs-lookup"><span data-stu-id="8bc93-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="8bc93-123">**Ngày đăng**: Chọn ngày đăng giá trị ước tính vào sổ cái.</span><span class="sxs-lookup"><span data-stu-id="8bc93-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="8bc93-124">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bc93-124">Select **OK**.</span></span>
5. <span data-ttu-id="8bc93-125">Sau khi quy trình loại bỏ hoàn tất, dự án ước tính đã loại bỏ sẽ được hiển thị với giá trị âm.</span><span class="sxs-lookup"><span data-stu-id="8bc93-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="8bc93-126">Nếu bạn không định loại bỏ giá trị ước tính, thì bạn có thể chọn giá trị ước tính đã loại bỏ và chọn **Đảo ngược hoạt động loại bỏ**.</span><span class="sxs-lookup"><span data-stu-id="8bc93-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]