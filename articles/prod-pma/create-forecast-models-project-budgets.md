---
title: Tạo mô hình dự báo cho ngân sách dự án
description: Chủ đề này mô tả cách tạo mô hình dự báo cho ngân sách còn lại.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087244"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="e2324-103">Tạo mô hình dự báo cho ngân sách dự án</span><span class="sxs-lookup"><span data-stu-id="e2324-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2324-104">Chủ đề này mô tả cách tạo mô hình dự báo cho ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="e2324-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="e2324-105">Một dự án được kiểm soát ngân sách sẽ sử dụng hai loại ngân sách: ngân sách ban đầu và ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="e2324-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="e2324-106">Khi tạo ngân sách dự án, bạn phải chỉ định mô hình dự báo ngân sách ban đầu và ngân sách còn lại đã được tạo ở trang **Mô hình dự báo**.</span><span class="sxs-lookup"><span data-stu-id="e2324-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="e2324-107">Ngân sách dự án dựa trên mô hình đã chỉ định sẽ được tạo khi bạn cam kết ngân sách dự án.</span><span class="sxs-lookup"><span data-stu-id="e2324-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="e2324-108">Mô hình dự báo dùng để kiểm soát ngân sách không được có mô hình con và không được dùng làm mô hình con.</span><span class="sxs-lookup"><span data-stu-id="e2324-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="e2324-109">Chọn **Quản lý dự án và kế toán** > **Thiết lập** > **Dự báo**  > **Mô hình dự báo**.</span><span class="sxs-lookup"><span data-stu-id="e2324-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="e2324-110">Chọn **Mới** để tạo mô hình dự báo mới, rồi nhập số ID mô hình và tên cho mô hình mới.</span><span class="sxs-lookup"><span data-stu-id="e2324-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="e2324-111">Đặt tùy chọn **Đã dừng** thành **Có** để ngăn chặn mọi sự thay đổi đối với dòng dự báo cho mô hình dự báo.</span><span class="sxs-lookup"><span data-stu-id="e2324-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="e2324-112">Nếu mô hình được liên kết với các dòng dự báo sẽ tạo ra dự báo dòng tiền trong sổ cái, hãy đặt **Đưa vào dự báo dòng tiền** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="e2324-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="e2324-113">Để sử dụng ngày dự án làm ngày lập hóa đơn, hãy đặt **Dự báo ngày lập hóa đơn** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="e2324-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="e2324-114">Ở trường **Loại ngân sách** , hãy chọn một trong các loại mô hình sau:</span><span class="sxs-lookup"><span data-stu-id="e2324-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="e2324-115">**Ngân sách ban đầu** : Sử dụng số tiền ngân sách ban đầu đã cam kết khi ngân sách ban đầu được tạo và phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="e2324-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="e2324-116">**Ngân sách còn lại** : Sử dụng số tiền ngân sách còn lại trong suốt vòng đời của dự án.</span><span class="sxs-lookup"><span data-stu-id="e2324-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="e2324-117">Số dư trong mô hình dự báo này bị giảm đi do các giao dịch thực tế và tăng hoặc giảm theo các mục sửa đổi ngân sách.</span><span class="sxs-lookup"><span data-stu-id="e2324-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="e2324-118">**Chuyển tiếp** : Sử dụng số tiền ngân sách chuyển tiếp cho dự án.</span><span class="sxs-lookup"><span data-stu-id="e2324-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="e2324-119">Chuyển tiếp là một quy trình không bắt buộc, có thể được chạy để chuyển số tiền ngân sách chưa sử dụng từ năm tài chính này sang năm tài chính khác.</span><span class="sxs-lookup"><span data-stu-id="e2324-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="e2324-120">Đặt các tùy chọn sau theo yêu cầu:</span><span class="sxs-lookup"><span data-stu-id="e2324-120">Set the following options as required:</span></span>

   - <span data-ttu-id="e2324-121">Kích hoạt **Dự báo ngày lập hóa đơn** để sử dụng ngày dự án làm ngày lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="e2324-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="e2324-122">Kích hoạt **Dự báo với WIP** để dự báo dựa trên công việc đang tiến hành (WIP), sau đó chọn loại WIP.</span><span class="sxs-lookup"><span data-stu-id="e2324-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="e2324-123">Bạn có thể giữ **Loại ngân sách** mặc định là **Không có** hoặc nhập một loại mới.</span><span class="sxs-lookup"><span data-stu-id="e2324-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="e2324-124">Bạn không thể thay đổi loại ngân sách sau khi thay đổi bản ghi.</span><span class="sxs-lookup"><span data-stu-id="e2324-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="e2324-125">Nếu bạn thay đổi loại ngân sách mặc định, thì tất cả các tùy chọn khác sẽ không có sẵn để cập nhật và bạn không thể sử dụng lại mô hình dự báo này.</span><span class="sxs-lookup"><span data-stu-id="e2324-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

