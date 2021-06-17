---
title: Có gì mới hoặc thay đổi trong Bản phát hành cập nhật Project Service Automation 29.5, Bản vá, V3
description: Chủ đề này liệt kê các tính năng và những chi tiết sửa lỗi trong bản phát hành cập nhật Project Service Automation, bản vá 29.5, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/26/2021
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
ms.openlocfilehash: d5050945c4ab7c1da61b07ec08bed20f32e166b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999202"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-295-v3"></a><span data-ttu-id="ac258-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 29.5, V3</span><span class="sxs-lookup"><span data-stu-id="ac258-103">What's new or changed in Project Service Automation Update Release 29.5, V3</span></span>

<span data-ttu-id="ac258-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ac258-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ac258-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="ac258-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ac258-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ac258-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ac258-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="ac258-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ac258-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="ac258-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="ac258-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 29.5.</span><span class="sxs-lookup"><span data-stu-id="ac258-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.5.</span></span> <span data-ttu-id="ac258-110">Phiên bản này có số bản dựng là V3.10.47.150 và thường có sẵn thông qua bản tự cập nhật vào tháng 1 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="ac258-110">This version has a build number of V3.10.47.150 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-295"></a><span data-ttu-id="ac258-111">Phát hành bản cập nhật 29.5</span><span class="sxs-lookup"><span data-stu-id="ac258-111">Update Release 29.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ac258-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="ac258-112">Bug fixes</span></span>


<span data-ttu-id="ac258-113">**Bán hàng**</span><span class="sxs-lookup"><span data-stu-id="ac258-113">**Sales**</span></span>

<span data-ttu-id="ac258-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="ac258-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac258-115">Một ngoại lệ tham chiếu rỗng có thể xảy ra trong **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** khi bạn chốt một báo giá với trạng thái là thắng và báo giá không có bảng giá.</span><span class="sxs-lookup"><span data-stu-id="ac258-115">A possible null reference exception occurs in **ContractLineMapHelper.UpdateContractLineDetailPriceListReference** when you close a quote as won and the quote has no price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
