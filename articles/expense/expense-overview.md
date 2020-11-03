---
title: Tổng quan về chi phí
description: Chủ đề này cung cấp thông tin về chức năng Chi phí trong Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086988"
---
# <a name="expense-home-page"></a><span data-ttu-id="a5e5b-103">Trang chủ chi phí</span><span class="sxs-lookup"><span data-stu-id="a5e5b-103">Expense home page</span></span>

<span data-ttu-id="a5e5b-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a5e5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a5e5b-105">Dynamics 365 Project Operations hỗ trợ khả năng xử lý chi phí.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="a5e5b-106">Xử lý chi phí xảy ra có hoặc không có dự án bằng cách sử dụng quy trình làm việc có thể tùy chỉnh của các chính sách, danh mục giao dịch và phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="a5e5b-107">Trong Project Operations, có hai mô hình triển khai được hỗ trợ cho Chi phí:</span><span class="sxs-lookup"><span data-stu-id="a5e5b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="a5e5b-108">**Đầy đủ** : Triển khai đầy đủ có sẵn cho **Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho** hoặc **Project Operations cho các kịch bản dựa trên lệnh sản xuất**.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="a5e5b-109">**Cơ bản** : Triển khai cơ bản có sẵn cho **Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho** và **Triển khai đơn giản - giao dịch với lập hóa đơn chiếu lệ**.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="a5e5b-110">Đầy đủ</span><span class="sxs-lookup"><span data-stu-id="a5e5b-110">Full</span></span> 
<span data-ttu-id="a5e5b-111">Việc triển khai chi phí đầy đủ cung cấp khả năng thực thi chính sách hoàn chỉnh bao gồm khả năng tạo các chính sách, chẳng hạn như:</span><span class="sxs-lookup"><span data-stu-id="a5e5b-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="a5e5b-112">Giới hạn loại chi phí</span><span class="sxs-lookup"><span data-stu-id="a5e5b-112">Expense category limits</span></span>
  - <span data-ttu-id="a5e5b-113">Di chuyển</span><span class="sxs-lookup"><span data-stu-id="a5e5b-113">Travel</span></span>
  - <span data-ttu-id="a5e5b-114">Công nhật</span><span class="sxs-lookup"><span data-stu-id="a5e5b-114">Per diem</span></span>
  - <span data-ttu-id="a5e5b-115">Số lần nhập thẻ tín dụng</span><span class="sxs-lookup"><span data-stu-id="a5e5b-115">Credit card imports</span></span>
  - <span data-ttu-id="a5e5b-116">Nhận dạng ký tự quang học cho biên lai</span><span class="sxs-lookup"><span data-stu-id="a5e5b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="a5e5b-117">Cơ bản</span><span class="sxs-lookup"><span data-stu-id="a5e5b-117">Basic</span></span> 
<span data-ttu-id="a5e5b-118">Kịch bản triển khai chi phí cơ bản chỉ cho phép bạn ghi lại các chi phí cơ bản đối với một dự án.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="a5e5b-119">Để biết thêm thông tin, hãy xem [Mục nhập chi phí (đơn giản)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="a5e5b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="a5e5b-120">Xác định triển khai chi phí của bạn</span><span class="sxs-lookup"><span data-stu-id="a5e5b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="a5e5b-121">Để xác định xem bạn có đang chạy triển khai quản lý chi phí cơ bản hay không, hãy xác minh rằng URL địa chỉ kết thúc bằng **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="a5e5b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
