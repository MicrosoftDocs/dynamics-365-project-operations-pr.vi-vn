---
title: Quản lý các đơn vị phức tạp như mỗi người dùng, mỗi tháng cho các mô tả báo giá dựa trên sản phẩm
description: Chủ đề này cung cấp thông tin về việc quản lý các đơn vị phức tạp cho mô tả báo giá dựa trên sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965921"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="08c3b-103">Quản lý các đơn vị phức tạp như mỗi người dùng, mỗi tháng cho các mô tả báo giá dựa trên sản phẩm</span><span class="sxs-lookup"><span data-stu-id="08c3b-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="08c3b-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="08c3b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="08c3b-105">Dynamics 365 Project Operations sử dụng các yếu tố số lượng để hỗ trợ việc bán các sản phẩm dựa trên đăng ký.</span><span class="sxs-lookup"><span data-stu-id="08c3b-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="08c3b-106">Đối với các sản phẩm dựa trên đăng ký, số lượng trên báo giá hoặc mô tả hợp đồng dự án được thể hiện ở dạng số tháng người dùng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="08c3b-107">Thông thường, giá phần mềm đăng ký được lưu trữ trong danh mục ở dạng giá cho mỗi người dùng mỗi tháng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="08c3b-108">Trong quá trình bán hàng, giá trên mô tả báo giá thường là giá trên mỗi người dùng, mỗi tháng được đại lý bán hàng CNTT thương lượng và giảm giá.</span><span class="sxs-lookup"><span data-stu-id="08c3b-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="08c3b-109">Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau.</span><span class="sxs-lookup"><span data-stu-id="08c3b-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="08c3b-110">Số lượng được dùng để tính toán mô tả báo giá là sản phẩm của số lượng người dùng và số lượng tháng đăng ký.</span><span class="sxs-lookup"><span data-stu-id="08c3b-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="08c3b-111">Để hỗ trợ loại bán hàng này, Project Operations giới thiệu khái nhiệm yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="08c3b-112">Yếu tố số lượng dựa vào các thuộc tính sản phẩm trong Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="08c3b-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="08c3b-113">Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, Project Operations cho phép bạn gắn cờ một tập con hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="08c3b-114">Project Operations xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="08c3b-115">Khi bạn thêm một sản phẩm có yếu tố số lượng vào mô tả báo giá, trường **Số lượng** trở thành chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="08c3b-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="08c3b-116">Sau khi bạn nhập giá trị cho các thuộc tính sản phẩm là các yếu tố số lượng, Project Operations sẽ tính số lượng của mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="08c3b-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="08c3b-117">Ví dụ: Dynamics 365 Sales có thể có các thuộc tính sau đây:</span><span class="sxs-lookup"><span data-stu-id="08c3b-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="08c3b-118">**Số người dùng**: Số lượng người dùng</span><span class="sxs-lookup"><span data-stu-id="08c3b-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="08c3b-119">**Số tháng**: Số lượng tháng đăng ký</span><span class="sxs-lookup"><span data-stu-id="08c3b-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="08c3b-120">**SKU sản phẩm**</span><span class="sxs-lookup"><span data-stu-id="08c3b-120">**Product SKU**</span></span>

<span data-ttu-id="08c3b-121">Bạn có thể gắn cờ **Số người dùng** và **Số tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="08c3b-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="08c3b-122">Để tạo yếu tố Số lượng từ thuộc tính Sản phẩm, hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="08c3b-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="08c3b-123">Trên ngăn điều hướng bên trái Project Operations, hãy đi tới **Bán hàng** > **Sản phẩm**.</span><span class="sxs-lookup"><span data-stu-id="08c3b-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="08c3b-124">Mở sản phẩm mà bạn cần đặt cấu hình yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="08c3b-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="08c3b-125">Đảm bảo rằng sản phẩm có các thuộc tính đã được đặt cấu hình.</span><span class="sxs-lookup"><span data-stu-id="08c3b-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="08c3b-126">Trên trang **Thông tin dự án** cho Sản phẩm, chọn tab **Yếu tố số lượng**.</span><span class="sxs-lookup"><span data-stu-id="08c3b-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="08c3b-127">Trong lưới con, chọn **+ Tính toán trường mới**.</span><span class="sxs-lookup"><span data-stu-id="08c3b-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="08c3b-128">Nhập tên của yếu tố Số lượng và chọn giá trị thuộc tính ánh xạ đến mục tính toán trường.</span><span class="sxs-lookup"><span data-stu-id="08c3b-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="08c3b-129">Lưu và đóng biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="08c3b-129">Save and close the form.</span></span> <span data-ttu-id="08c3b-130">Lặp lại các bước này cho tất cả các thuộc tính để tính toán số lượng cho mô tả báo giá dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="08c3b-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="08c3b-131">Khi bạn tạo mô tả báo giá dựa trên sản phẩm cho một sản phẩm, số lượng của mô tả báo giá sẽ bị khóa.</span><span class="sxs-lookup"><span data-stu-id="08c3b-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="08c3b-132">Số lượng sẽ được tính dưới dạng tích số của các giá trị thuộc tính mà bạn nhập cho mô tả báo giá đó.</span><span class="sxs-lookup"><span data-stu-id="08c3b-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
