---
title: Sao chép báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách sao chép báo giá dựa trên dự án trong Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e8611f34a23d6d87317cc785148c1a3f9c26dca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588072"
---
# <a name="copy-project-based-quotes"></a>Sao chép báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể dễ dàng tạo Báo giá dự án mới bằng cách sao chép báo giá hiện có. 

- Để sao chép Báo giá dự án, trên trang danh sách **Báo giá dự án** hoặc trang chi tiết **Báo giá dự án**, hãy chọn Báo giá dự án bạn muốn sao chép, sau đó chọn **Sao chép**.

Thao tác này sẽ mở ra một trang hộp thoại nơi bạn có thể nhập các tham số của bản sao. Bảng sau liệt kê các trường có trong trang hộp thoại. Tùy thuộc vào các giá trị bạn chọn, quá trình sao chép có thể thay đổi.

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Chủ đề | Nhập chủ đề hoặc tên có liên quan của báo giá đích. Khi hộp thoại mở, hệ thống sẽ đặt thành chủ đề của báo giá nguồn với **-sao chép** gắn kèm. | |
| Khách hàng Tiềm năng | Tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi hộp thoại mở, hệ thống sẽ đặt thành khách hàng trên báo giá nguồn. | Trường này là khách hàng chính trên báo giá. |
| Đơn vị Hợp đồng | Đơn vị tổ chức chịu trách nhiệm bàn giao dự án hoặc (các) dự án liên quan đến thỏa thuận này.
Khi hộp thoại mở, hệ thống sẽ đặt thành đơn vị ký hợp đồng trên báo giá nguồn. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ. Đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong quá trình thực hiện dự án. |
| Tiền tệ | Đây là đơn vị tiền tệ mà thỏa thuận được giao dịch. Khi hộp thoại mở, hệ thống sẽ đặt thành đơn vị tiền tệ trên báo giá nguồn. Thao tác này có thể được sửa đổi và nếu được thay đổi, thì trường **Sao chép giá** luôn được đặt thành **Không**. Điều này là do bảng giá trên báo giá nguồn không còn phù hợp nữa. | Đơn vị tiền tệ được sử dụng để mặc định một bảng giá, để xây dựng ước tính tài chính cho bảng báo giá và cuối cùng là để lập hóa đơn cho khách hàng khi thỏa thuận được chốt. |
| Ngày giao hàng đã yêu cầu | Đây là ngày giao hàng do khách hàng yêu cầu. | Ngày này được sử dụng làm ngày kết thúc khi tạo ngày lập hóa đơn theo một tần suất cụ thể. |
| Sao chép giá | Giá trị Có/Không cho biết liệu giá trên báo giá có được sao chép từ báo giá nguồn hay không. | Nếu chọn **Có**, các tham chiếu bảng giá dự án và bảng giá sản phẩm được sao chép từ báo giá nguồn sang báo giá đích. Nếu chọn **Không**, bảng giá được mặc định lại dựa trên bảng giá mới nhất đã được thiết lập trên tài khoản hoặc tham số dự án. |

Khi bạn chọn **OK** trên trang hộp thoại, hệ thống tạo một bản sao báo giá dự án dựa trên các tham số được chọn trong hộp thoại. Báo giá dự án mới sẽ mở. 

> [!NOTE]
> Thông tin sau không được sao chép từ Báo giá nguồn sang Báo giá đích:
>
> - Lịch trình hóa đơn
> - Khách hàng trên báo giá và mô tả báo giá
> - Tham chiếu dự án trên các mô tả báo giá dựa trên dự án – Thông tin ngân sách khách hàng
>
>Vì thông tin này rất cụ thể cho từng báo giá, các trường và bản ghi này không được sao chép. Các mô tả báo giá cho các dự án và sản phẩm, ước tính về chi tiết mô tả báo giá và các giá trị không vượt quá mức báo giá được sao chép. Giá và tỷ lệ chi phí mặc định phụ thuộc vào tùy chọn **Sao chép giá** được chọn trên trang hộp thoại **Sao chép tham số**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]