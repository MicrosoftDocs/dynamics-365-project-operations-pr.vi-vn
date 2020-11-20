---
title: Tạo hóa đơn ước giá thủ công - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo hóa đơn ước giá thủ công trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176412"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Tạo hóa đơn ước giá thủ công - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, hóa đơn ước giá có thể được tạo thủ công nếu cần. Bạn có thể tạo thủ công hóa đơn ước giá từ trang danh sách **Hợp đồng dự án** hoặc từ trang chi tiết **Hợp đồng dự án**.

##  <a name="project-contracts-list-page"></a>Trang danh sách Hợp đồng dự án

Ở trang danh sách **Hợp đồng dự án**, chọn một hoặc nhiều hợp đồng dự án và tạo hóa đơn cho tất cả các bản ghi được chọn.

Hệ thống kiểm tra xem hợp đồng dự án nào đã chọn có mục tồn đọng **Đã sẵn sàng để lập hóa đơn** được đề ngày trước ngày hôm nay. Từ những hợp đồng đó, hệ thống tạo ra hóa đơn ước giá nháp. Nếu hợp đồng dự án có nhiều khách hàng, thì mỗi khách hàng có thể được tạo một hóa đơn và có thể có nhiều hóa đơn cho một hợp đồng dự án.

Tất cả các hóa đơn dự án đã tạo đều có sẵn trên trang **Hóa đơn** ở phần **Thanh toán** của khu vực **Bán hàng**.

## <a name="project-contract-details-page"></a>Trang chi tiết Hợp đồng dự án

Bạn cũng có thể tạo hóa đơn ước giá từ trang chi tiết **Hợp đồng dự án**, đây là nơi tạo hóa đơn cho một hợp đồng dự án cụ thể. Hệ thống xác minh rằng hợp đồng dự án có mục tồn đọng **Đã sẵn sàng để lập hóa đơn** được đề ngày trước ngày hôm nay. Từ các hợp đồng này, hệ thống tạo hóa đơn ước giá nháp dựa trên số lượng khách hàng trên mỗi mục mô tả hợp đồng.

Khi có một hóa đơn ước giá được tạo,trang **Hóa đơn** sẽ mở ra. Nếu có nhiều hóa đơn được tạo cho hợp đồng dự án đó, thì trang danh sách **Hóa đơn** sẽ mở ra để hiển thị tất cả các hóa đơn đã tạo.
