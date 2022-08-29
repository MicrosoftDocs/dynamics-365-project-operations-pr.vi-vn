---
title: Đặt cấu hình Bảng lịch trình để hiển thị nhân viên hợp đồng và năng lực của hợp đồng phụ
description: Bài viết này mô tả cách định cấu hình Bảng lịch biểu trong Microsoft Dynamics 365 Project Operations để hiển thị năng lực nguồn lực theo hợp đồng phụ khi nhân sự yêu cầu nguồn lực của dự án.
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

Lên lịch bảng trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để tìm kiếm tài nguyên theo hai cách:

- Tìm kiếm tài nguyên chung mà không có bối cảnh của bất kỳ yêu cầu tài nguyên cụ thể dựa trên dự án nào.
- Tìm kiếm tài nguyên theo yêu cầu cụ thể trong đó yêu cầu của dự án sẽ cung cấp bối cảnh cho các tài nguyên được đề xuất.

Để thông báo cho bảng lịch trình về năng lực tài nguyên được hợp đồng phụ và nhân viên hợp đồng, bạn cần cập nhật cài đặt Bảng lịch biểu. Những cập nhật này bao gồm: 
- Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung.
- Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung
### <a name="update-filters-for-general-resource-search"></a>Cập nhật bộ lọc cho tìm kiếm tài nguyên chung
Khi bạn tìm kiếm một tài nguyên, các bộ lọc có sẵn trên bảng lịch trình phải được cập nhật để bạn cũng có thể tìm kiếm các tài nguyên bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
  - Loại công nhân, cho dù các nguồn lực được hiển thị nên là công nhân hợp đồng hay nhân viên.
  - Công ty của nhà cung cấp mà tài nguyên phải thuộc về.
  - Các tài nguyên thuộc về một hợp đồng phụ hoặc dòng hợp đồng phụ cụ thể.
    
### <a name="update-retrieve-resource-query"></a>Cập nhật truy xuất truy vấn tài nguyên
Truy vấn được sử dụng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lịch trình cho việc tìm kiếm tài nguyên chung:  
1. Mở **Lên lịch cài đặt bảng** cho một Bảng lịch trình cụ thể.
2. Mở **Cài đặt chung** tab và cuộn đến **Các thiết lập khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** đến **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy xuất truy vấn tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu
### <a name="update-filters-for-requirement-specific-resource-search"></a>Cập nhật bộ lọc để tìm kiếm tài nguyên theo yêu cầu cụ thể 
Khi bạn tìm kiếm một tài nguyên, các bộ lọc có sẵn trên bảng lịch trình phải được cập nhật để bạn cũng có thể tìm kiếm các tài nguyên bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
 - Loại công nhân, cho dù các nguồn lực được hiển thị nên là công nhân hợp đồng hay nhân viên.
 - Công ty của nhà cung cấp mà tài nguyên phải thuộc về.
 - Các tài nguyên thuộc về một hợp đồng phụ hoặc dòng hợp đồng phụ cụ thể.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Cập nhật truy vấn truy xuất tài nguyên để tìm kiếm tài nguyên theo yêu cầu cụ thể 
Truy vấn được sử dụng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lập lịch để tìm kiếm tài nguyên dựa trên yêu cầu:

1. Mở **Lên lịch cài đặt bảng** cho một Bảng lịch trình cụ thể và sau đó chọn **Mở cài đặt mặc định** để mở cài đặt cho tìm kiếm theo yêu cầu cụ thể.
2. Mở **Cài đặt chung** tab và cuộn đến **Các thiết lập khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** đến **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy xuất truy vấn tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite**.
5. Mở **Các loại lịch biểu** tab và đi đến **Dự án**.
6. Trong cài đặt cho **Dự án**, cập nhật **Lên lịch Hỗ trợ Truy xuất Truy vấn Tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite** và cập nhật **Lập lịch truy vấn các ràng buộc hỗ trợ truy xuất** đến **Truy vấn Ràng buộc Truy xuất Mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
