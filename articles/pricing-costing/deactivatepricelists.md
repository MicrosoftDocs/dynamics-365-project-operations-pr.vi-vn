---
title: Hủy kích hoạt bảng giá
description: Bài viết này giải thích cách hủy kích hoạt hoặc loại bỏ các bảng giá cũ hoặc không dùng đến.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924410"
---
# <a name="deactivate-price-lists"></a>Hủy kích hoạt bảng giá 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Để loại bỏ các bảng giá cũ hoặc không dùng đến khỏi Dynamics 365 Project Operations, có hai bước mà bạn phải hoàn thành. 

1. Loại bỏ hoặc xóa bảng giá khỏi các trang cụ thể.
2. Hủy kích hoạt hoặc xóa bảng giá khỏi Các bảng giá hiện hoạt trên trang **Bảng giá**.

>[!IMPORTANT]
> Bạn phải hoàn thành cả hai bước để loại bỏ hoàn toàn một bảng giá. Chỉ thực hiện bước 2, tức là trực tiếp xóa hoặc hủy kích hoạt bảng giá từ dạng xem Bảng giá hiện hoạt, là không đủ. Bạn cũng phải xóa liên kết của bảng giá này khỏi tất cả những nơi được đề cập trong bước 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Xóa bảng giá khỏi các trang cụ thể
1. Để xóa bảng giá khỏi Project Operations, hãy truy cập các trang sau:  

      - Trang **Tham số dự án** > tab **Bảng giá**
      - Trang **Đơn vị tổ chức** > lưới **Bảng giá**
      - Trang **Tài khoản** > lưới **Bảng giá dự án**
      - Trang **Báo giá dự án** > lưới **Bảng giá dự án**: Điều này áp dụng cho tất cả các báo giá dự án hiện hoạt.
      - Trang **Hợp đồng dự án** > lưới **Bảng giá dự án**: Điều này áp dụng cho tất cả các hợp đồng dự án hiện hoạt.

 2. Đối với mỗi trang, bạn cần chọn bảng giá mà mình muốn xóa, sau đó chọn **Xóa**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Xóa hoặc hủy kích hoạt bảng giá khỏi trang Bảng giá
 
1. Để xóa một bảng giá khỏi các bảng giá hiện hoạt, hãy đi đến **Bán hàng** > **Khách hàng** > **Bảng giá**. 
2. Chọn bảng giá mà mình muốn xóa, sau đó chọn **Xóa**. Nếu bảng giá được đề cập trên bất kỳ giao dịch hiện có nào, bạn sẽ không thể xóa bảng giá đó. Nếu điều này xảy ra, bạn có thể hủy kích hoạt để bảng giá không xuất hiện trong bất kỳ dạng xem nào. 
3. Để hủy kích hoạt bảng giá, hãy chọn lại bảng giá, sau đó chọn **Hủy kích hoạt**.   
