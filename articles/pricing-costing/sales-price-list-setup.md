---
title: Thiết lập bảng giá bán hàng
description: Chủ đề này cung cấp thông tin về bảng giá bán hàng cho giá dự án.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176277"
---
# <a name="set-up-a-sales-price-list"></a>Thiết lập bảng giá bán hàng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Đối với báo giá dự án và hợp đồng, bảng giá dự án có mô hình thay thế giá khác với bảng giá sản phẩm. Trên dòng báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá cho các vai trò và danh mục trực tiếp trên dòng báo giá vì mỗi dòng báo giá trỏ đến chính xác một mục trong danh mục. Tuy nhiên, trên dòng báo giá dựa trên dự án, bạn không thể thay thế giá cho vai trò và danh mục trực tiếp trên dòng báo giá. Bạn có thể sử dụng bảng giá dự án để làm việc với hai mô hình thay thế khác nhau.

> [!NOTE]
> Bạn nên có một bảng giá riêng cho tài nguyên dự án và các mục trên danh mục của bạn vì sự khác biệt về hành vi giữa hai thứ này khi bạn thay thế giá.

Mỗi thực thể sau có thể có một hoặc nhiều bảng giá bán hàng liên quan cho giá dự án:

- Khách hàng (tài khoản) 
- Cơ hội 
- Báo giá 
- Hợp đồng Dự án

Một liên kết các thực thể này với bảng giá được biểu thị bằng bảng giá dự án. Bạn có thể liên kết một hoặc nhiều bảng giá với các thực thể bán hàng khách hàng, cơ hội, báo giá và hợp đồng dự án.

Bảng giá dự án mặc định không tự động nhập vào bản ghi khách hàng. Tuy nhiên, bạn có thể tự đính kèm bảng giá dự án vào bản ghi khách hàng. Tuy nhiên, bạn nên đính kèm bảng giá dự án chỉ khi có thỏa thuận giá tùy chỉnh với khách hàng. 

Khi một bảng giá dự án được đính kèm vào một thực thể bán hàng, thông tin sau đây được xác thực:

- Bảng giá là có bối cảnh **Bán hàng**. 
- Tiền tệ của bảng giá phải khớp với loại tiền của khách hàng. 

Trên hợp đồng dự án, thứ tự ưu tiên sau đây được sử dụng để tự động đặt bảng giá dự án liên quan:

1. Báo giá
2. Cơ hội
3. Khách hàng 
4. Thiết đặt tổng thể 

Khi một bảng giá dự án được nhập theo mặc định, hệ thống sẽ xác thực rằng loại tiền tệ khớp với tiền tệ của khách hàng và các bảng giá mặc định đã nhập có bối cảnh **Bán hàng**.

Bạn có thể liên kết nhiều bảng giá dự án với các thực thể khách hàng, cơ hội, báo giá và hợp đồng dự án. Khả năng này hỗ trợ giá mặc định theo ngày cho một hợp đồng dự án dài, nơi bạn có thể yêu cầu nhiều bảng giá để tính đến khả năng cập nhật giá do lạm phát. Tuy nhiên, nếu bảng giá mà bạn liên kết với thực thể khách hàng, cơ hội, báo giá hoặc hợp đồng dự án có ngày hiệu lực chồng chéo, thì giá mặc định có thể không chính xác. Do đó, bạn phải đảm bảo rằng bảng giá dự án có ngày hiệu lực chồng chéo không liên kết với những thực thể đó.
