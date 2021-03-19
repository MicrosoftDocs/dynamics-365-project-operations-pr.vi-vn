---
title: Đặt cấu hình tích hợp Project Operations cho mỗi pháp nhân
description: Chủ đề này cung cấp thông tin về cách thiết lập tích hợp theo pháp nhân trong Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277004"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="bd0ab-103">Đặt cấu hình tích hợp Project Operations cho mỗi pháp nhân</span><span class="sxs-lookup"><span data-stu-id="bd0ab-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="bd0ab-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="bd0ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bd0ab-105">Chủ đề này sẽ hướng dẫn bạn qua các bước cần thiết để định cấu hình Dynamics 365 Project Operations mỗi pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="bd0ab-106">Bật các khóa tính năng trong Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="bd0ab-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="bd0ab-107">Hoàn thành các bước sau để bật các tính năng cần thiết.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="bd0ab-108">Trong Dynamics 365 Finance, đi đến không gian làm việc **Quản lý tính năng**.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="bd0ab-109">Trong **Danh sách tính năng**, tìm và bật các tính năng sau:</span><span class="sxs-lookup"><span data-stu-id="bd0ab-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="bd0ab-110">**Cho phép nhiều mô tả hợp đồng cho một dự án**</span><span class="sxs-lookup"><span data-stu-id="bd0ab-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="bd0ab-111">**Bật Project Operations trên Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="bd0ab-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="bd0ab-112">Nếu bạn không thấy **Khóa tính năng** được liệt kê, xác minh rằng phiên bản Finance của bạn đáp ứng yêu cầu phiên bản tối thiểu (phiên bản ứng dụng 10.0.13 với tất cả các bản cập nhật chất lượng được áp dụng hoặc cao hơn).</span><span class="sxs-lookup"><span data-stu-id="bd0ab-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="bd0ab-113">Chọn **Kiểm tra cập nhật** để làm mới danh sách tính năng.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="bd0ab-114">Xác định kịch bản triển khai Project Operations cho một pháp nhân</span><span class="sxs-lookup"><span data-stu-id="bd0ab-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="bd0ab-115">Bạn có thể bật Project Operations trên Dynamics 365 Customer Engagement ở cấp độ pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="bd0ab-116">Bạn có thể có một pháp nhân sử dụng Project Operations trên Dynamics 365 Customer Engagement cho các kịch bản dựa trên nguồn lực/không trữ kho.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="bd0ab-117">Trong cùng một môi trường, bạn có thể có một pháp nhân khác sử dụng Project Operations cho các kịch bản trữ kho/lệnh sản xuất.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="bd0ab-118">Trong Dynamics 365 Finance, đi đến **Kế toán và quản lý dự án** > **Thiết lập** > **Tham số kế toán và quản lý dự án toàn cầu**.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="bd0ab-119">Trong danh sách các pháp nhân hiện có, hãy chọn thực thể có nhiều mô tả hợp đồng và Project Operations trên các tính năng Dynamics 365 Customer Engagement sẽ được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="bd0ab-120">Bỏ chọn các pháp nhân sẽ sử dụng Project Operations cho các kịch bản trữ kho/lệnh sản xuất.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="bd0ab-121">Một pháp nhân chỉ có thể được chọn nếu nó không có bất kỳ dự án hiện có nào.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="bd0ab-122">Đặt cấu hình quản lý dự án và các tham số kế toán</span><span class="sxs-lookup"><span data-stu-id="bd0ab-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="bd0ab-123">Mỗi pháp nhân sử dụng Project Operations trên Dynamics 365 Customer Engagement cần một tập hợp các tham số mặc định.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="bd0ab-124">Các tham số này được đặt cấu hình trên tab **Project Operations** trên trang **Tham số kế toán và quản lý dự án**.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="bd0ab-125">Các tham số là:</span><span class="sxs-lookup"><span data-stu-id="bd0ab-125">The parameters are:</span></span>

  - <span data-ttu-id="bd0ab-126">**Loại thanh toán mặc định**: Project Operations sử dụng một tập hợp cố định các loại thanh toán mặc định phải được ánh xạ tới thuộc tính mô tả Finance.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="bd0ab-127">Tạo bản ghi cho từng loại thanh toán: **Không được chỉ định**, **Có thể tính phí**, **Không tính phí**, **Miễn phí** và **Không có sẵn**.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="bd0ab-128">**Danh mục dự án mặc định**: Chọn các danh mục dự án mặc định sẽ được sử dụng cho từng loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="bd0ab-129">Các giá trị mặc định này sẽ được sử dụng trong **nhật ký Tích hợp Project Operations** và trong các giá trị ước tính mà không có danh mục giao dịch nào được chỉ định cho giá trị thực tế của dự án.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="bd0ab-130">**Dự báo**: Chọn mô hình dự báo được sử dụng để ước tính thời gian và chi phí.</span><span class="sxs-lookup"><span data-stu-id="bd0ab-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]