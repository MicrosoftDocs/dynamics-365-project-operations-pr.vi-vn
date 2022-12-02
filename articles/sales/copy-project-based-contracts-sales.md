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

Bạn có thể dễ dàng tạo hợp đồng dự án mới bằng cách sao chép các hợp đồng hiện có theo một trong hai cách:

- Trên trang danh sách **Hợp đồng dự án**, hãy chọn một hợp đồng dự án rồi chọn **Sao chép**.
- Trên trang chi tiết **Hợp đồng dự án**, hãy chọn **Sao chép**.

Trong cả hai trường hợp, một hộp thoại sẽ mở ra để bạn có thể đặt các tham số của hợp đồng được sao chép. Hộp thoại bao gồm các trường sau đây. Tùy thuộc vào các giá trị bạn chọn, quá trình sao chép có thể thay đổi.

| Trường | Description | Tác động xuôi tuyến |
| --- | --- | --- |
| Chủ đề | Nhập chủ đề của hợp đồng mục tiêu. Khi trang hộp thoại được mở ra, hệ thống sẽ đặt trường này thành tên hợp đồng nguồn nhưng có kèm theo từ "sao chép". | Không có tác động xuôi tuyến đối với trường này. |
| Quý khách hàng | Một tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi hộp thoại mở ra, hệ thống sẽ đặt trường này thành khách hàng trên hợp đồng nguồn. | Trường này là khách hàng chính trên hợp đồng. |
| Công ty sở hữu | Công ty chịu trách nhiệm bàn giao các dự án được liên kết với thỏa thuận này. Khi hộp thoại mở ra, hệ thống sẽ đặt trường này thành công ty sở hữu trên hợp đồng nguồn. | Công ty sở hữu là pháp nhân sẽ thực hiện dự án sau khi thỏa thuận được chốt. Đơn vị tiền tệ của công ty sở hữu phải khớp với đơn vị tiền tệ của đơn vị hợp đồng. |
| Đơn vị theo hợp đồng | Đơn vị tổ chức chịu trách nhiệm bàn giao các dự án được liên kết với thỏa thuận này. Khi hộp thoại mở ra, hệ thống sẽ đặt trường này thành đơn vị hợp đồng trên hợp đồng nguồn. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ. Đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |
| Tiền tệ | Đơn vị tiền tệ giao dịch trong thỏa thuận. Khi trang hộp thoại được mở ra, hệ thống sẽ đặt trường này thành đơn vị tiền tệ của hợp đồng nguồn. Có thể thay đổi đơn vị tiền tệ. Nếu bạn thay đổi đơn vị tiền tệ, thì trường **Sao chép giá** sẽ luôn được đặt thành **Không**, vì bảng giá trên hợp đồng nguồn không còn phù hợp nữa. | Đơn vị tiền tệ được sử dụng cho bảng giá mặc định để tạo giá trị ước tính tài chính trên hợp đồng và để lập hóa đơn cho khách hàng khi thỏa thuận được chốt. |
| Ngày giao hàng được yêu cầu | Ngày giao mà khách hàng yêu cầu. | Ngày này được sử dụng làm ngày kết thúc khi bạn tạo ngày lập hóa đơn theo một tần suất cụ thể. |
| Sao chép giá | Giá trị cho biết liệu có cần sao chép giá trên hợp đồng từ hợp đồng nguồn hay không. | Nếu trường này được đặt thành **Có**, thì các mục tham chiếu bảng giá dự án và bảng giá sản phẩm sẽ được sao chép từ hợp đồng nguồn sang hợp đồng đích. Nếu được đặt thành **Không**, các bảng giá mặc định được sử dụng dựa trên bảng giá mới nhất trên các tham số tài khoản hoặc dự án. |

Khi bạn chọn **OK** trên trang hộp thoại, hệ thống sẽ tạo một bản sao hợp đồng dựa trên các giá trị tham số bạn đặt. Sau đó, hợp đồng mới được mở.

Thông tin sau **không được** sao chép từ hợp đồng nguồn sang hợp đồng đích, vì nó là cụ thể cho từng hợp đồng:

- Lịch trình hóa đơn
- Khách hàng trong hợp đồng và mục mô tả hợp đồng
- Mục tham chiếu dự án trên các mục mô tả hợp đồng dựa trên dự án
- Thông tin về ngân sách của khách hàng

Các mục mô tả hợp đồng cho các dự án và sản phẩm, giá trị ước tính bằng thông tin chi tiết mô tả hợp đồng và các giá trị không vượt quá ở cấp độ hợp đồng sẽ được sao chép. Mục nhập giá mặc định và tỷ lệ chi phí tùy thuộc vào lựa chọn ở trường **Sao chép giá** trong hộp thoại **Sao chép tham số**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
