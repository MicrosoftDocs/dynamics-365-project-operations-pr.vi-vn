---
title: Định cấu hình Bảng lịch trình để hiển thị công nhân hợp đồng và năng lực của hợp đồng phụ
description: Chủ đề này mô tả cách định cấu hình Bảng lịch biểu trong Microsoft Dynamics 365 Project Operations để hiển thị năng lực nguồn lực theo hợp đồng phụ khi nhân sự yêu cầu nguồn lực của dự án.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903809"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Định cấu hình Bảng lịch trình để hiển thị công nhân hợp đồng và năng lực của hợp đồng phụ 

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Lên lịch bảng trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để tìm kiếm tài nguyên theo hai cách:

- Tìm kiếm tài nguyên chung mà không có bối cảnh của bất kỳ yêu cầu tài nguyên dựa trên dự án cụ thể nào.
- Tìm kiếm tài nguyên theo yêu cầu cụ thể trong đó yêu cầu của dự án sẽ cung cấp bối cảnh cho các tài nguyên được đề xuất.

Để thông báo cho bảng lịch trình về năng lực tài nguyên được thầu phụ và nhân viên hợp đồng, bạn cần cập nhật cài đặt Bảng lịch biểu. Những cập nhật này bao gồm: 
- Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung.
- Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung
### <a name="update-filters-for-general-resource-search"></a>Cập nhật bộ lọc cho tìm kiếm tài nguyên chung
Khi bạn tìm kiếm tài nguyên, các bộ lọc có sẵn trên bảng lịch trình sẽ được cập nhật để bạn cũng có thể tìm kiếm các tài nguyên bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
  - Loại công nhân, cho dù các nguồn lực được hiển thị nên là công nhân hợp đồng hay nhân viên.
  - Công ty của nhà cung cấp mà tài nguyên nên thuộc về.
  - Các tài nguyên thuộc về một hợp đồng phụ hoặc dòng hợp đồng phụ cụ thể.
    
### <a name="update-retrieve-resource-query"></a>Cập nhật truy xuất truy vấn tài nguyên
Truy vấn được sử dụng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lịch trình để tìm kiếm tài nguyên chung:  
1. Mở **Lên lịch cài đặt bảng** cho một Bảng lịch trình cụ thể.
2. Mở **Cài đặt chung** tab và cuộn đến **Các thiết lập khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** đến **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy vấn Truy vấn Tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên chung](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu
### <a name="update-filters-for-requirement-specific-resource-search"></a>Cập nhật bộ lọc để tìm kiếm tài nguyên theo yêu cầu cụ thể 
Khi bạn tìm kiếm tài nguyên, các bộ lọc có sẵn trên bảng lịch trình sẽ được cập nhật để bạn cũng có thể tìm kiếm các tài nguyên bên ngoài bằng cách chỉ định bất kỳ hoặc tất cả những điều sau:
 - Loại công nhân, cho dù các nguồn lực được hiển thị nên là công nhân hợp đồng hay nhân viên.
 - Công ty của nhà cung cấp mà tài nguyên nên thuộc về.
 - Các tài nguyên thuộc về một hợp đồng phụ hoặc dòng hợp đồng phụ cụ thể.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Cập nhật truy xuất truy vấn tài nguyên để tìm kiếm tài nguyên theo yêu cầu cụ thể 
Truy vấn được sử dụng để tìm kiếm cũng phải được cập nhật để sử dụng các thuộc tính bộ lọc bổ sung này. Sử dụng các bước sau để cập nhật cấu hình Bảng lập lịch để tìm kiếm tài nguyên dựa trên yêu cầu:

1. Mở **Lên lịch cài đặt bảng** cho một Bảng lịch trình cụ thể và sau đó chọn **Mở cài đặt mặc định** để mở cài đặt cho tìm kiếm theo yêu cầu cụ thể.
2. Mở **Cài đặt chung** tab và cuộn đến **Các thiết lập khác**.
3. Trong danh sách cài đặt trong phần này, hãy cập nhật **Bố cục bộ lọc** đến **Bố cục bộ lọc mặc định cho Project Operations Lite**.
4. Cập nhật **Truy vấn Truy vấn Tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite**.
5. Mở **Các loại lịch biểu** tab và đi đến **Dự định**.
6. Trong cài đặt cho **Dự định**, cập nhật **Lên lịch Hỗ trợ Truy xuất Truy vấn Tài nguyên** đến **Truy vấn tài nguyên truy xuất mặc định cho Project Operations Lite** và cập nhật **Lên lịch truy vấn các ràng buộc hỗ trợ truy xuất** đến **Truy vấn Ràng buộc Truy xuất Mặc định cho Project Operations Lite**.

![Cập nhật cài đặt Bảng lịch trình để tìm kiếm tài nguyên dựa trên yêu cầu](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
