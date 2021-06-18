---
title: Các mô hình kỹ năng và mức độ thành thạo
description: Chủ đề này cung cấp thông tin về cách sử dụng các mô hình kỹ năng và mức độ thành thạo.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008697"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="d21d4-103">Các mô hình kỹ năng và mức độ thành thạo</span><span class="sxs-lookup"><span data-stu-id="d21d4-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d21d4-104">Kỹ năng là các đặc điểm của nguồn lực được chia sẻ giữa Dynamics 365 Project Service Automation và Dynamics 365 Field Service nếu có.</span><span class="sxs-lookup"><span data-stu-id="d21d4-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="d21d4-105">Để duy trì kho lưu trữ kỹ năng trong Project Service Automation, hãy chuyển đến **Nguồn lực** \> **Kỹ năng của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="d21d4-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Kỹ năng của nguồn lực](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="d21d4-107">Sử dụng mô hình mức độ thành thạo để xếp hạng nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d21d4-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="d21d4-108">Kỹ năng của nguồn lực được đánh giá bằng mô hình thành thạo.</span><span class="sxs-lookup"><span data-stu-id="d21d4-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="d21d4-109">Các xếp hạng cá nhân trong một mô hình mức độ thành thạo.</span><span class="sxs-lookup"><span data-stu-id="d21d4-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="d21d4-110">Để tạo mô hình thành thạo, hãy chuyển đến **Tài nguyên** \> **Mô hình mức độ thành thạo** rồi chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="d21d4-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="d21d4-111">Trong mô hình xếp hạng mới, chỉ định giá trị xếp hạng tối thiểu, giá trị xếp hạng tối đa và thực thể đang được xếp hạng.</span><span class="sxs-lookup"><span data-stu-id="d21d4-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="d21d4-112">Trong lưới con **Giá trị xếp hạng**, bạn có thể xác định các giá trị xếp hạng khác nhau, từ tối thiểu cho đến tối đa.</span><span class="sxs-lookup"><span data-stu-id="d21d4-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Xếp hạng tối thiểu và tối đa được xác định](media/Resource-Management-image85.png)

<span data-ttu-id="d21d4-114">Các giá trị xếp hạng này hiển thị trên các bộ lọc **Yêu cầu nguồn lực**, **Bảng lịch trình** và **Trợ lý lập lịch biểu**.</span><span class="sxs-lookup"><span data-stu-id="d21d4-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]