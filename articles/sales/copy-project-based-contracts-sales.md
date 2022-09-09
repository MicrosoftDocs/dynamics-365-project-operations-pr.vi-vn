---
title: Sao chép hợp đồng dựa trên dự án
description: Bài viết này cung cấp thông tin về việc sao chép hợp đồng dự án trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410390"
---
# <a name="copy-project-based-contracts"></a>Sao chép hợp đồng dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bạn có thể dễ dàng tạo các hợp đồng dự án mới bằng cách sao chép các hợp đồng hiện có theo một trong hai cách:

- Trên **Hợp đồng dự án** trang danh sách, chọn một hợp đồng dự án, sau đó chọn **Sao chép**.
- Trên trang chi tiết **Hợp đồng dự án**, hãy chọn **Sao chép**.

Trong cả hai trường hợp, một hộp thoại xuất hiện, nơi bạn có thể đặt các thông số của hợp đồng đã sao chép. Hộp thoại bao gồm các trường sau đây. Tùy thuộc vào các giá trị bạn chọn, quá trình sao chép có thể thay đổi.

| Trường | Description | Tác động xuôi tuyến |
| --- | --- | --- |
| Chủ đề | Nhập chủ đề của hợp đồng mục tiêu. Khi hộp thoại được mở, hệ thống đặt trường thành tên của hợp đồng nguồn, nhưng từ "sao chép" được thêm vào nó. | Không có tác động xuôi tuyến đối với trường này. |
| Quý khách hàng | Một tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi hộp thoại được mở, hệ thống đặt trường vào tài khoản trên hợp đồng nguồn. | Trường này là khách hàng chính trên hợp đồng. |
| Công ty sở hữu | Công ty chịu trách nhiệm bàn giao các dự án có liên quan đến thương vụ này. Khi hộp thoại được mở, hệ thống đặt trường thành công ty sở hữu của hợp đồng nguồn. | Công ty sở hữu là pháp nhân sẽ thực hiện dự án sau khi thương vụ kết thúc. Đơn vị tiền tệ của công ty sở hữu phải phù hợp với đơn vị tiền tệ của đơn vị ký hợp đồng. |
| Đơn vị theo hợp đồng | Đơn vị tổ chức chịu trách nhiệm bàn giao các dự án liên quan đến thương vụ này. Khi hộp thoại được mở, hệ thống đặt trường thành đơn vị ký kết của hợp đồng nguồn. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ. Đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |
| Tiền tệ | Đơn vị tiền tệ giao dịch trong thỏa thuận. Khi hộp thoại được mở, hệ thống đặt trường thành đơn vị tiền tệ của hợp đồng nguồn. Có thể thay đổi đơn vị tiền tệ. Nếu đúng như vậy, **Sao chép giá cả** trường luôn được đặt thành **Không**, bởi vì bảng giá trên hợp đồng nguồn không còn phù hợp nữa. | Đơn vị tiền tệ này được sử dụng cho các bảng giá mặc định, để tạo ra các ước tính tài chính trên hợp đồng và để lập hóa đơn cho khách hàng khi thỏa thuận thắng. |
| Ngày giao hàng được yêu cầu | Ngày giao hàng mà khách hàng yêu cầu. | Ngày này được sử dụng làm ngày kết thúc khi bạn tạo ngày lập hóa đơn ở một tần suất cụ thể. |
| Sao chép giá | Một giá trị cho biết liệu giá trên hợp đồng có nên được sao chép từ hợp đồng nguồn hay không. | Nếu trường được đặt thành **Đúng**, các tham chiếu bảng giá dự án và sản phẩm được sao chép từ hợp đồng nguồn sang hợp đồng đích. Nếu nó được đặt thành **Không**, bảng giá mặc định được sử dụng, dựa trên bảng giá mới nhất trong tài khoản hoặc thông số dự án. |

Khi bạn chọn **ĐƯỢC RỒI** trong hộp thoại, hệ thống tạo một bản sao của hợp đồng, dựa trên các giá trị tham số mà bạn đã đặt. Sau đó, hợp đồng mới được mở.

Thông tin sau là **không phải** được sao chép từ hợp đồng nguồn sang hợp đồng đích, vì nó cụ thể cho từng hợp đồng:

- Lịch trình hóa đơn
- Khách hàng trong hợp đồng và mục mô tả hợp đồng
- Mục tham chiếu dự án trên các mục mô tả hợp đồng dựa trên dự án
- Thông tin về ngân sách của khách hàng

Các dòng hợp đồng cho các dự án và sản phẩm, các ước tính trong chi tiết dòng hợp đồng và các giá trị không vượt quá ở cấp độ hợp đồng được sao chép. Việc nhập giá mặc định và tỷ lệ chi phí phụ thuộc vào lựa chọn trong **Sao chép giá cả** lĩnh vực trong **Sao chép thông số** hộp thoại.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
