---
title: Mục đặt trước và mục chỉ định
description: Chủ đề này cung cấp thông tin về sự khác biệt giữa đặt trước nguồn lực và chỉ định nguồn lực.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086957"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="c53cd-103">Mục đặt trước và mục chỉ định</span><span class="sxs-lookup"><span data-stu-id="c53cd-103">Bookings vs assignments</span></span>

<span data-ttu-id="c53cd-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c53cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c53cd-105">Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="c53cd-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="c53cd-106">Đăng ký chắc chắn chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="c53cd-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="c53cd-107">Phân công là phân công nguồn lực cho các nhiệm vụ dự án trong lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="c53cd-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="c53cd-108">Các nguồn lực có thể là các nguồn lực thật hoặc chung.</span><span class="sxs-lookup"><span data-stu-id="c53cd-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="c53cd-109">Đối với các nguồn lực thực, tốt nhất là đăng ký và phân công nên nhất quán vì không khác nhau.</span><span class="sxs-lookup"><span data-stu-id="c53cd-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="c53cd-110">Tuy nhiên, Microsoft Dynamics Project Operations không thực thi thỏa thuận này.</span><span class="sxs-lookup"><span data-stu-id="c53cd-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="c53cd-111">Dạng xem **Điều hòa** hiển thị cho người quản lý dự án nơi đăng ký và phân công của nguồn lực không nhất quán.</span><span class="sxs-lookup"><span data-stu-id="c53cd-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
