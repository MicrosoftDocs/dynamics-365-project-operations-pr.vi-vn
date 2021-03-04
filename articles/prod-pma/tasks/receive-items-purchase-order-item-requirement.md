---
title: Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng
description: Chủ đề này giải thích cách nhận các mặt hàng trong đơn đặt hàng từ một yêu cầu về mặt hàng.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087275"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng

[!include [banner](../../includes/banner.md)]

Chủ đề này giải thích cách nhận các mặt hàng trong đơn đặt hàng từ một yêu cầu về mặt hàng.

Bằng cách sử dụng yêu cầu mặt hàng thay vì giao dịch mặt hàng, bạn có thể lập kế hoạch giao hàng ngay trước khi mặt hàng đó thực sự được sử dụng, tạo đơn đặt hàng, đưa mặt hàng vào khuôn khổ thỏa thuận thương mại và đưa yêu cầu mặt hàng vào kế hoạch sản xuất. 

Nhiệm vụ này sử dụng tập hợp dữ liệu USSI.

1. Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Dự án > Tất cả dự án**.
2. Trong danh sách, chọn liên kết trong hàng mong muốn.
3. Ở ngăn Hành động, chọn **Kế hoạch**.
4. Chọn **Yêu cầu mặt hàng**.
5. Chọn **Mới**.
6. Trong hàng mới, hãy nhập hoặc chọn một giá trị trong trường **Số mặt hàng**.
7. Nhập số vào trường **Số lượng**.
8. Chọn **Lưu**.
9. Ở ngăn Hành động, chọn **Quản lý**.
10. Chọn **Chức năng**.
11. Chọn **Tạo đơn đặt hàng**.
12. Chọn hộp kiểm **Bao gồm tất cả**.
13. Trong trường **Tài khoản nhà cung cấp** , nhập hoặc chọn một giá trị.
14. Chọn **OK**.
15. Ở ngăn điều hướng, chuyển tới **Mô-đun > Tài khoản phải trả > Đơn đặt hàng > Tất cả đơn đặt hàng**.
16. Trong danh sách, chọn liên kết trong hàng mong muốn.
17. Ở ngăn Hành động, chọn **Mua hàng**.
18. Chọn **Xác nhận**.
19. Ở ngăn Hành động, chọn **Nhận**.
20. Chọn **Biên lai sản phẩm**.
21. Trong trường **Biên lai sản phẩm** , nhập giá trị.
22. Chọn **OK**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]