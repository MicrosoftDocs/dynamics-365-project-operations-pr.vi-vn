---
title: Giao thầu phụ trong bản phát hành Quyền truy cập sớm vào tháng 10 năm 2021
description: Chủ đề này cung cấp thông tin tổng quan về các khả năng giao thầu phụ trong Project Operations thuộc bản phát hành quyền truy cập sớm vào tháng 10 năm 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383721"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Giao thầu phụ trong bản phát hành Quyền truy cập sớm vào tháng 10 năm 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này cung cấp thông tin tổng quan về các khả năng giao thầu phụ trong Dynamics 365 Project Operations thuộc bản phát hành quyền truy cập sớm vào tháng 10 năm 2021. Bộ tính năng này chưa sẵn sàng cho môi trường sản xuất hoặc trực tiếp, vì vậy các tính năng này sẽ vẫn ở trong bản phát hành quyền truy cập sớm cho đến khi bộ tính năng đầy đủ được phát hành. Chúng tôi thực sự khuyên bạn không nên sử dụng bộ tính năng giao thầu phụ cho các kịch bản sản xuất trực tiếp cho đến khi biểu ngữ xem trước bị xóa. 

Danh sách sau cung cấp sơ lược về những gì hiện có trong bản phát hành Quyền truy cập sớm vào tháng 10 năm 2021:

1. Người quản lý dự án tạo một hợp đồng phụ với một nhà cung cấp. Theo mặc định, bảng giá được đính kèm với hồ sơ nhà cung cấp được sử dụng cho hợp đồng phụ. Tài khoản nhà cung cấp có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**.

2. Người quản lý dự án có thể lặp lại tất cả các giao dịch mua dưới dạng mục hàng trên hợp đồng phụ. Mô tả hợp đồng phụ có thể là về thời gian, chi phí hoặc sản phẩm. Lớp giao dịch của mô tả hợp đồng phụ sẽ xác định mô tả đó dùng để làm gì.

3. Người quản lý tài khoản của nhà cung cấp và người quản lý dự án có thể lặp lại hợp đồng phụ. Có thể điều chỉnh giá trong bảng giá mua đính kèm với hợp đồng phụ.

4. Tại thời điểm này hoặc sau đó trong quá trình, nếu mô tả hợp đồng phụ là về thời gian, người quản lý tài khoản nhà cung cấp sẽ kết hợp các địa chỉ liên hệ của nhà cung cấp với từng mô tả hợp đồng phụ. Việc liên kết này cung cấp thông tin cho người quản lý dự án, người đang làm việc trên hợp đồng phụ. Khi một liên hệ của nhà cung cấp được liên kết với một mô tả hợp đồng phụ, hệ thống sẽ tự động tạo nguồn lực có thể đặt trước từ liên hệ, nếu nguồn lực có thể đặt trước chưa tồn tại.

5. Phương thức thanh toán trên mỗi mô tả hợp đồng phụ có thể là **Giá cố định** hoặc **Thời gian và Vật liệu**. Đối với các mô tả hợp đồng phụ giá cố định, lịch hóa đơn dựa trên cột mốc được thiết lập.

Các bước còn lại trong dòng quy trình công việc cho giao thầu phụ được nêu trong phần Tổng quan hiện không khả dụng. Khi chức năng mới được thêm vào, chủ đề này sẽ được cập nhật. 

Hình minh họa sau đây thể hiện bản phát hành Quyền truy cập sớm cho Giao thầu phụ tương phản với toàn bộ quy trình kinh doanh.

![Sòng quy trình giao thầu phụ](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Bản phát hành quyền truy cập sớm cho mô tả hợp đồng phụ dựa trên số lượng và mô tả hợp đồng phụ dựa trên công việc
Trong bản phát hành Quyền truy cập sớm vào tháng 10 năm 2021, chỉ các mô tả hợp đồng phụ dựa trên số lượng được hỗ trợ. Điều này có nghĩa là mô tả hợp đồng phụ có thể được sử dụng để mua thời gian, chi phí hoặc vật liệu từ một nhà cung cấp nhưng không phải là toàn bộ nội dung công việc. Điều này cũng có nghĩa là số lượng được mua (đơn vị thời gian, chi phí hoặc số lượng vật liệu) trên một mô tả hợp đồng phụ có thể được sử dụng cho bất kỳ dự án nào trong hệ thống.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
