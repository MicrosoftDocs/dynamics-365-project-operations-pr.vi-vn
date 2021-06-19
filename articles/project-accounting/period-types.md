---
title: Loại chu kỳ
description: Chủ đề này cung cấp thông tin về cách thiết lập loại chu kỳ cho phép ước tính doanh thu.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013512"
---
# <a name="period-types"></a><span data-ttu-id="23c0e-103">Loại chu kỳ</span><span class="sxs-lookup"><span data-stu-id="23c0e-103">Period types</span></span>

<span data-ttu-id="23c0e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="23c0e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="23c0e-105">Loại chu kỳ xác định tần suất ước tính doanh thu của dự án.</span><span class="sxs-lookup"><span data-stu-id="23c0e-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="23c0e-106">Chủ đề này cung cấp thông tin về cách thiết lập loại chu kỳ cho phép ước tính doanh thu.</span><span class="sxs-lookup"><span data-stu-id="23c0e-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="23c0e-107">Tạo và làm việc với các loại chu kỳ</span><span class="sxs-lookup"><span data-stu-id="23c0e-107">Create and work with period types</span></span>
<span data-ttu-id="23c0e-108">Để tạo và làm việc với các loại chu kỳ, hãy hoàn thành các bước sau:</span><span class="sxs-lookup"><span data-stu-id="23c0e-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="23c0e-109">Trong môi trường Dynamics 365 Finance, hãy đi tới **Quản lý dự án và kế toán** > **Thiết lập** > **Ước tính** > **Loại chu kỳ**.</span><span class="sxs-lookup"><span data-stu-id="23c0e-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="23c0e-110">Chọn **Mới** để tạo loại chu kỳ mới.</span><span class="sxs-lookup"><span data-stu-id="23c0e-110">Select **New** to create new period type.</span></span> <span data-ttu-id="23c0e-111">Nhập tên và mô tả.</span><span class="sxs-lookup"><span data-stu-id="23c0e-111">Enter a name and description.</span></span>
3. <span data-ttu-id="23c0e-112">Trong trường **Tần suất**, hãy chọn một giá trị:</span><span class="sxs-lookup"><span data-stu-id="23c0e-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="23c0e-113">Nếu bạn chọn **Tuần**, **Hai tuần một lần**, **Nửa tháng**, **Tháng**, **Ngày**, **Quý** hoặc **Năm**, lịch sẽ được dùng để tạo chu kỳ.</span><span class="sxs-lookup"><span data-stu-id="23c0e-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="23c0e-114">Nếu bạn chọn **Chu kỳ sổ cái**, chu kỳ sổ cái của cấu hình Sổ cái chung sẽ được dùng để tạo chu kỳ.</span><span class="sxs-lookup"><span data-stu-id="23c0e-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="23c0e-115">Nếu chọn **Không giới hạn**, bạn có thể tùy chỉnh chu kỳ.</span><span class="sxs-lookup"><span data-stu-id="23c0e-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="23c0e-116">Chọn bản ghi loại chu kỳ rồi bấm vào **Tạo chu kỳ** để tạo các chu kỳ cho loại chu kỳ.</span><span class="sxs-lookup"><span data-stu-id="23c0e-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="23c0e-117">Dựa trên tần suất chu kỳ vừa chọn, bạn có thể dùng tùy chọn này để xác định ngày bắt đầu hoặc số lượng chu kỳ cần tạo.</span><span class="sxs-lookup"><span data-stu-id="23c0e-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="23c0e-118">Chọn **Chu kỳ** để xem lại các chu kỳ vừa tạo.</span><span class="sxs-lookup"><span data-stu-id="23c0e-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]