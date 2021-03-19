---
title: Xác định kỹ năng và độ thành thạo
description: Chủ đề này cung cấp thông tin về cách thiết lập mô hình mức độ thành thạo để đánh giá các nguồn lực.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279704"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="2ed03-103">Xác định kỹ năng và độ thành thạo</span><span class="sxs-lookup"><span data-stu-id="2ed03-103">Define skills and proficiencies</span></span>

<span data-ttu-id="2ed03-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="2ed03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2ed03-105">Kỹ năng là các đặc điểm của nguồn lực được chia sẻ giữa Dynamics 365 Project Operations và Dynamics 365 Field Service nếu có.</span><span class="sxs-lookup"><span data-stu-id="2ed03-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="2ed03-106">Để duy trì kho lưu trữ kỹ năng trong Project Operations, hãy chọn **Nguồn lực** \> **Kỹ năng của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="2ed03-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="2ed03-107">Sử dụng mô hình mức độ thành thạo để xếp hạng nguồn lực</span><span class="sxs-lookup"><span data-stu-id="2ed03-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="2ed03-108">Kỹ năng của nguồn lực được đánh giá bằng mô hình thành thạo.</span><span class="sxs-lookup"><span data-stu-id="2ed03-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="2ed03-109">Các xếp hạng cá nhân trong một mô hình mức độ thành thạo.</span><span class="sxs-lookup"><span data-stu-id="2ed03-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="2ed03-110">Để tạo mô hình thành thạo, hãy chuyển đến **Tài nguyên** \> **Mô hình mức độ thành thạo** rồi chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2ed03-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="2ed03-111">Trong mô hình xếp hạng mới, chỉ định giá trị xếp hạng tối thiểu, giá trị xếp hạng tối đa và thực thể đang được xếp hạng.</span><span class="sxs-lookup"><span data-stu-id="2ed03-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="2ed03-112">Trong lưới con **Giá trị xếp hạng**, bạn có thể xác định các giá trị xếp hạng khác nhau, từ tối thiểu cho đến tối đa.</span><span class="sxs-lookup"><span data-stu-id="2ed03-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="2ed03-113">Các giá trị xếp hạng này hiển thị trên các bộ lọc **Yêu cầu nguồn lực**, **Bảng lịch trình** và **Trợ lý lập lịch biểu**.</span><span class="sxs-lookup"><span data-stu-id="2ed03-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]