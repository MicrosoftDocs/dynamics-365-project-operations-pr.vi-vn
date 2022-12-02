---
title: Đặt cấu hình Bảng lịch trình để hiển thị nhân viên hợp đồng và năng lực của hợp đồng phụ
description: Bài viết này mô tả cách định cấu hình Bảng lịch trình trong Microsoft Dynamics 365 Project Operations để hiển thị năng lực nguồn lực theo hợp đồng phụ khi bố trí nhân sự theo yêu cầu nguồn lực của dự án.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262243"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Đặt cấu hình Bảng lịch trình để hiển thị nhân viên hợp đồng và năng lực của hợp đồng phụ 

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng lịch trình trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để tìm kiếm nguồn lực theo hai cách:

- Tìm kiếm nguồn lực chung mà không có bối cảnh của bất kỳ yêu cầu nguồn lực dựa trên dự án cụ thể nào.
- Tìm kiếm nguồn lực theo yêu cầu cụ thể trong đó yêu cầu của dự án sẽ cung cấp bối cảnh cho các nguồn lực được đề xuất.

Để thông báo bảng nguồn lực về năng lực nguồn lực theo hợp đồng phụ và nhân viên hợp đồng, bạn cần cập nhật cài đặt Bảng lịch trình. Các cập nhật này bao gồm: 
- Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực chung.
- Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực dựa trên yêu cầu.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực chung
### <a name="update-filters-for-general-resource-search"></a>Cập nhật bộ lọc cho tìm kiếm nguồn lực chung
Khi bạn tìm kiếm một nguồn lực, các bộ lọc có sẵn trên bảng lịch trình sẽ được cập nhật để bạn cũng có thể tìm kiếm các nguồn lực bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
  - Loại nhân viên, cho dù các nguồn lực được hiển thị nên là nhân viên hợp đồng hay nhân viên.
  - Công ty nhà cung cấp sở hữu nguồn lực.
  - Các nguồn lực thuộc về một hợp đồng phụ hoặc mô tả hợp đồng phụ.
    
### <a name="update-retrieve-resource-query"></a>Cập nhật truy vấn truy xuất nguồn lực
Truy vấn dùng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lịch trình cho việc tìm kiếm nguồn lực chung:  
1. Mở **Cài đặt bảng lịch trình** cho một Bảng lịch trình cụ thể.
2. Mở tab **Cài đặt chung** và cuộn đến **Các cài đặt khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** thành **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy xuất truy vấn nguồn lực** thành **Truy vấn truy xuất nguồn lực mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực chung](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực dựa trên yêu cầu
### <a name="update-filters-for-requirement-specific-resource-search"></a>Cập nhật bộ lọc cho tìm kiếm nguồn lực cụ thể cho yêu cầu 
Khi bạn tìm kiếm một nguồn lực, các bộ lọc có sẵn trên bảng lịch trình sẽ được cập nhật để bạn cũng có thể tìm kiếm các nguồn lực bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
 - Loại nhân viên, cho dù các nguồn lực được hiển thị nên là nhân viên hợp đồng hay nhân viên.
 - Công ty nhà cung cấp sở hữu nguồn lực.
 - Các nguồn lực thuộc về một hợp đồng phụ hoặc mô tả hợp đồng phụ.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Cập nhật truy xuất truy vấn nguồn lực cho tìm kiếm nguồn lực cụ thể theo yêu cầu 
Truy vấn dùng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lịch trình cho việc tìm kiếm nguồn lực theo yêu cầu.

1. Mở **Cài đặt bảng lịch trình** cho một Bảng lịch trình cụ thể và sau đó chọn **Mở cài đặt mặc định** để mở cài đặt cho tìm kiếm theo yêu cầu cụ thể.
2. Mở tab **Cài đặt chung** và cuộn đến **Các cài đặt khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** thành **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy xuất truy vấn nguồn lực** thành **Truy vấn truy xuất nguồn lực mặc định cho Project Operations Lite**.
5. Mở tab **Loại lịch trình** và đi đến **Dự án**.
6. Trong cài đặt cho **Dự án**, hãy cập nhật **Truy vấn Truy xuất nguồn lực trợ lý lịch trình** thành **Truy vấn truy xuất nguồn lực mặc định cho Project Operations Lite** và cập nhật **Truy vấn Truy xuất ràng buộc trợ lý lịch trình** thành **Truy vấn truy xuất ràng buộc mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình cho tìm kiếm nguồn lực dựa trên yêu cầu](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
