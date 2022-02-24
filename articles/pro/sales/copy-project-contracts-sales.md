---
title: Sao chép hợp đồng dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách sao chép hợp đồng dự án trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4137fc400c7fdd8fecd9d8349bf7f57f3470b51f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181433"
---
# <a name="copy-project-contracts---lite"></a>Sao chép hợp đồng dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể dễ dàng tạo hợp đồng dự án mới bằng cách tạo bản sao của các hợp đồng hiện có theo một trong hai cách: 

  - Trên trang danh sách **Hợp đồng dự án**, hãy chọn một hợp đồng dự án rồi chọn **Sao chép**.
  - Trên trang chi tiết **Hợp đồng dự án**, hãy chọn **Sao chép**.

Một hộp thoại sẽ mở ra để bạn có thể chọn các tham số của hợp đồng được sao chép. Hộp thoại có các trường sau đây. Tùy theo các giá trị bạn chọn trong hộp thoại này, quá trình sao chép có thể thay đổi.

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Chủ đề | Nhập chủ đề của hợp đồng mục tiêu. Khi trang hộp thoại mở ra, hệ thống sẽ đặt trường này thành tên hợp đồng nguồn kèm theo **- sao chép**. | Không có tác động xuôi tuyến đối với trường này. |
| Khách hàng | Tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi hộp thoại mở ra, hệ thống sẽ đặt trường này thành khách hàng trên hợp đồng nguồn. | Trường này là khách hàng chính trên hợp đồng. |
| Đơn vị Hợp đồng | Đơn vị tổ chức chịu trách nhiệm bàn giao (các) dự án được liên kết với thỏa thuận này. Khi trang hộp thoại mở ra, hệ thống sẽ đặt mục này thành đơn vị ký hợp đồng trên hợp đồng nguồn. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ. Đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |
| Tiền tệ | Đơn vị tiền tệ giao dịch trong thỏa thuận. Khi trang hộp thoại mở ra, hệ thống sẽ đặt trường này thành đơn vị tiền tệ của hợp đồng nguồn. Có thể thay đổi đơn vị tiền tệ. Nếu bạn thay đổi đơn vị tiền tệ, thì trường **Sao chép giá** sẽ luôn được đặt thành **Không**, vì bảng giá trên hợp đồng nguồn không còn phù hợp nữa. | Đơn vị tiền tệ được sử dụng cho bảng giá mặc định, cho việc xác định giá trị ước tính tài chính trên hợp đồng và để lập hóa đơn cho khách hàng khi thỏa thuận được chốt. |
| Ngày giao hàng đã yêu cầu | Ngày giao mà khách hàng yêu cầu. | Ngày này được sử dụng làm ngày kết thúc khi bạn tạo ngày lập hóa đơn theo một tần suất cụ thể. |
| Sao chép giá | Biểu thị có cần sao chép giá trên hợp đồng từ hợp đồng nguồn hay không. | Nếu trường này được đặt thành **Có**, thì các mục tham chiếu bảng giá dự án và bảng giá sản phẩm sẽ được sao chép từ hợp đồng nguồn sang hợp đồng đích. Nếu bạn chọn **Không**, thì bảng giá sẽ lấy mặc định dựa trên bảng giá mới nhất trên các tham số tài khoản hoặc dự án. |

Khi bạn chọn **OK** trên trang hộp thoại, hệ thống sẽ tạo một bản sao hợp đồng dựa trên các tham số đã chọn. Hợp đồng mới sẽ mở ra.

Thông tin sau không được sao chép từ **Hợp đồng nguồn** sang **Hợp đồng đích**:

  - Lịch trình hóa đơn
  - Khách hàng trong hợp đồng và mục mô tả hợp đồng
  - Mục tham chiếu dự án trên các mục mô tả hợp đồng dựa trên dự án
  - Thông tin về ngân sách của khách hàng

Vì đây là thông tin cụ thể cho từng hợp đồng, nên các trường và bản ghi này không được sao chép. Các mục mô tả hợp đồng cho các dự án và sản phẩm, giá trị ước tính trên thông tin chi tiết mô tả hợp đồng và các giá trị không vượt quá ở cấp độ hợp đồng sẽ được sao chép. Giá và tỷ lệ chi phí được lấy mặc định theo phần lựa chọn ở trường **Sao chép giá** trên trang hộp thoại **Sao chép tham số**.
