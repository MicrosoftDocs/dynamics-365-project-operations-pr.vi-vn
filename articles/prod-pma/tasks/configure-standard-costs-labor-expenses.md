---
title: Đặt cấu hình chi phí tiêu chuẩn cho nhân công và chi phí
description: Chủ đề này giải thích cách thiết lập chi phí tiêu chuẩn cho nhân công và chi phí cho dự án.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087165"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Đặt cấu hình chi phí tiêu chuẩn cho nhân công và chi phí

[!include [banner](../../includes/banner.md)]

Chủ đề này giải thích cách thiết lập chi phí tiêu chuẩn cho nhân công và chi phí cho dự án. Nhiệm vụ này sử dụng tập hợp dữ liệu USSI.

1. Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá vốn (giờ)**.
2. Chọn **Mới**.
3. Nhập ngày vào trường **Ngày có hiệu lực**.
4. Nhập số vào trường **Giá vốn**. Bạn có thể thiết lập giá vốn tiêu chuẩn cho danh mục dự án hoặc bạn có thể thiết lập giá vốn theo số hiệu nhân viên, số dự án, danh mục, ngày hoặc bất kỳ tổ hợp nào của các yếu tố này. Giá vốn được áp dụng là giá vốn có mức độ chi tiết cao nhất.  
5. Chọn **Lưu**.
6. Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá bán (giờ)**.
7. Chọn **Mới**.
8. Nhập ngày vào trường **Ngày có hiệu lực**.
9. Chọn một tùy chọn trong trường **Hợp lệ trong**.
10. Nhập số vào trường **Định giá**. Bạn có thể thiết lập giá bán tiêu chuẩn cho các giao dịch theo giờ hoặc cho một danh mục dự án. Bạn cũng có thể thiết lập giá bán theo số hiệu nhân viên, số dự án, danh mục, ngày giao dịch hoặc bất kỳ tổ hợp nào của các yếu tố này. Giá bán thực tế được áp dụng khi nhân viên nhập giao dịch vào nhật ký Giờ sẽ là giá bán có mức độ chi tiết cao nhất. Chẳng hạn, nếu cả giá bán chung và giá bán riêng theo nhân viên đều được thiết lập, thì giá bán riêng theo nhân viên sẽ được sử dụng.  
11. Chọn **Lưu**.
12. Đóng trang.
13. Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá vốn (chi phí)**.
14. Chọn **Mới**.
15. Nhập ngày vào trường **Ngày có hiệu lực**.
16. Nhập số vào trường **Giá vốn**. Bạn có thể điền nhiều trường, nhưng đây là mức tối thiểu cần có để lưu bản ghi.  
17. Chọn **Lưu**.
18. Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá bán (chi phí)**.
19. Chọn **Mới**.
20. Nhập ngày vào trường **Ngày có hiệu lực**.
21. Chọn một tùy chọn trong trường **Hợp lệ trong**.
22. Nhập số vào trường **Định giá**. Giá bán thực tế được áp dụng khi nhân viên nhập giao dịch vào nhật ký chi phí sẽ là giá bán có mức độ chi tiết cao nhất. Chẳng hạn, nếu cả giá bán chung và giá bán riêng theo nhân viên đều được thiết lập, thì giá bán riêng theo nhân viên sẽ được sử dụng.  
23. Chọn **Lưu**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]