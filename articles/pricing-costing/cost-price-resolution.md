---
title: Xác định tỷ lệ chi phí cho các ước tính và thực tế dựa trên dự án
description: Bài viết này cung cấp thông tin về cách xác định tỷ lệ chi phí cho các ước tính và thực tế dựa trên dự án.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475305"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Xác định tỷ lệ chi phí cho các ước tính và thực tế dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để xác định giá chi phí trên ước tính và thực tế trong Microsoft Dynamics 365 Project Operations, trước tiên hệ thống sử dụng ngày và đơn vị tiền tệ trong ước tính đến hoặc ngữ cảnh thực tế để xác định bảng giá bán hàng. Trong ngữ cảnh thực tế cụ thể, hệ thống sử dụng **Ngày Giao dịch** trường để xác định bảng giá có thể áp dụng. Các **Ngày Giao dịch** giá trị của ước tính đến hoặc thực tế được so sánh với **Bắt đầu hiệu quả (Không phụ thuộc vào múi giờ)** và **Kết thúc có hiệu lực (Không phụ thuộc vào múi giờ)** các giá trị trên bảng giá. Sau khi bảng giá vốn được xác định, hệ thống xác định giá vốn.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Xác định tỷ lệ chi phí trong ước tính và bối cảnh thực tế cho Thời gian

Ước tính ngữ cảnh cho **Thời gian** đề cập đến:

- Trích dẫn chi tiết dòng cho **Thời gian**.
- Chi tiết dòng hợp đồng cho **Thời gian**.
- Phân công tài nguyên trên một dự án.

Bối cảnh thực tế cho **Thời gian** đề cập đến:

- Dòng tạp chí Entry and Correction cho **Thời gian**.
- Các dòng nhật ký được tạo khi gửi một mục thời gian.

Sau khi xác định được bảng giá vốn, hệ thống hoàn thành các bước sau để nhập giá vốn mặc định.

1. Hệ thống phù hợp với sự kết hợp của **Vai diễn**, **ty cung cấp dịch vụ**, và **Đơn vị cung ứng** các trường trong ngữ cảnh ước tính hoặc thực tế cho **Thời gian** chống lại các đường giá vai trò trên bảng giá. Kết hợp này giả định rằng bạn đang sử dụng các thứ nguyên định giá tiêu chuẩn cho chi phí lao động. Nếu bạn đã định cấu hình hệ thống để khớp với các trường khác với hoặc ngoài **Vai diễn**, **ty cung cấp dịch vụ** và **Đơn vị cung ứng**, một tổ hợp khác được sử dụng để truy xuất đường giá phù hợp với vai trò.
1. Nếu hệ thống tìm thấy một đường giá vai trò có tỷ lệ chi phí cho **Vai diễn**, **ty cung cấp dịch vụ**, và **Đơn vị cung ứng** kết hợp, tỷ lệ chi phí đó được sử dụng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể khớp với **Vai diễn**, **ty cung cấp dịch vụ**, và **Đơn vị cung ứng** giá trị, nó giảm thứ nguyên có mức độ ưu tiên thấp nhất, tìm kiếm đường giá vai trò phù hợp với hai giá trị thứ nguyên khác và tiếp tục giảm dần thứ nguyên cho đến khi tìm thấy hàng giá vai trò phù hợp. Tỷ lệ chi phí từ bản ghi đó sẽ được sử dụng làm tỷ lệ chi phí mặc định. Nếu hệ thống không tìm thấy hàng giá có vai trò phù hợp, giá sẽ được đặt thành **0** (không) theo mặc định.

> [!NOTE]
> Nếu bạn định cấu hình một mức độ ưu tiên khác của **Vai diễn** và **Đơn vị cung ứng** hoặc nếu bạn có các thứ nguyên khác có mức độ ưu tiên cao hơn, hành vi trước đó sẽ thay đổi tương ứng. Hệ thống truy xuất bản ghi giá vai trò có giá trị phù hợp với từng giá trị thứ nguyên đặt giá theo thứ tự ưu tiên. Các hàng có giá trị null cho các thứ nguyên đó đứng cuối cùng.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Xác định tỷ lệ chi phí trên dòng thực tế và ước tính cho Chi phí

Ước tính ngữ cảnh cho **Chi phí** đề cập đến:

- Trích dẫn chi tiết dòng cho **Chi phí**.
- Chi tiết dòng hợp đồng cho **Chi phí**.
- Dự toán chi phí cho một dự án.

Bối cảnh thực tế cho **Chi phí** đề cập đến:

- Dòng tạp chí Entry and Correction cho **Chi phí**.
- Các dòng nhật ký được tạo khi gửi một mục chi phí.

Sau khi xác định được bảng giá vốn, hệ thống hoàn thành các bước sau để nhập giá vốn mặc định.

1. Hệ thống phù hợp với sự kết hợp của **Loại** và **Đơn vị** các trường trong ngữ cảnh ước tính hoặc thực tế cho **Chi phí** so với các dòng giá thể loại trên bảng giá.
1. Nếu hệ thống tìm thấy dòng giá danh mục có tỷ lệ chi phí cho **Loại** và **Đơn vị** kết hợp, tỷ lệ chi phí đó được sử dụng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể khớp với **Loại** và **Đơn vị** giá trị, giá được đặt thành **0** (không) theo mặc định.
1. Trong ngữ cảnh ước tính, nếu hệ thống có thể tìm thấy đường giá danh mục phù hợp, nhưng phương pháp định giá là một cái gì đó khác với **Giá mỗi đơn vị**, tỷ lệ chi phí được đặt thành **0** (không) theo mặc định.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Xác định tỷ lệ chi phí trên dòng thực tế và ước tính cho Vật liệu

Ước tính ngữ cảnh cho **Vật chất** đề cập đến:

- Trích dẫn chi tiết dòng cho **Vật chất**.
- Chi tiết dòng hợp đồng cho **Vật chất**.
- Ước tính vật liệu về một dự án.

Bối cảnh thực tế cho **Vật chất** đề cập đến:

- Nhập và sửa dòng tạp chí cho **Vật chất**.
- Các dòng nhật ký được tạo khi gửi nhật ký sử dụng Nguyên liệu.

Sau khi xác định được bảng giá vốn, hệ thống hoàn thành các bước sau để nhập giá vốn mặc định.

1. Hệ thống sử dụng sự kết hợp của **Sản phẩm** và **Đơn vị** các trường trong ngữ cảnh ước tính hoặc thực tế cho **Vật chất** so với các dòng mục của bảng giá trên bảng giá.
1. Nếu hệ thống tìm thấy một dòng mục trong danh sách giá có tỷ lệ chi phí cho **Sản phẩm** và **Đơn vị** kết hợp, tỷ lệ chi phí đó được sử dụng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể khớp với **Sản phẩm** và **Đơn vị** giá trị, đơn giá được đặt thành **0** (không) theo mặc định.
1. Trong ngữ cảnh ước tính hoặc thực tế, nếu hệ thống có thể tìm thấy dòng mục trong danh sách giá phù hợp, nhưng phương pháp đặt giá là một cái gì đó khác với **Lượng ngoại tệ**, đơn giá được đặt thành **0** theo mặc định. Hành vi này xảy ra bởi vì Hoạt động Dự án chỉ hỗ trợ **Lượng ngoại tệ** phương pháp định giá cho các vật liệu được sử dụng trong một dự án.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
