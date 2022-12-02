---
title: Xác định tỷ lệ chi phí cho ước tính và số liệu thực tế theo dự án
description: Bài viết này cung cấp thông tin về cách xác định tỷ lệ chi phí cho giá trị thực tế và ước tính theo dự án.
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
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Xác định tỷ lệ chi phí cho ước tính và số liệu thực tế theo dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để quyết định giá vốn trên ước tính và số liệu thực tế được trong Microsoft Dynamics 365 Project Operations, hệ thống trước tiên sử dụng ngày và đơn vị tiền tệ trong ước tính sắp tới hoặc ngữ cảnh thực tế để xác định bảng giá bán hàng trước tiên. Trong ngữ cảnh thực tế cụ thể, hệ thống sử dụng trường **Ngày giao dịch** để xác định bảng giá nào được áp dụng. Giá trị **Ngày giao dịch** của ước tính sắp đến hoặc số liệu thực tế được so sánh với các giá trị **Ngày bắt đầu có hiệu lực (Độc lập về múi giờ)** và **Ngày kết thúc hiệu lực (Độc lập về múi giờ)** trên bảng giá. Sau khi bảng giá vốn được quyết định, hệ thống sẽ xác định tỷ lệ chi phí.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Quyết định tỷ lệ chi phí trong ước tính và ngữ cảnh thực tế cho Thời gian

Ước tính ngữ cảnh cho **Thời gian** đề cập đến:

- Chi tiết mô tả báo giá cho **Thời gian**.
- Chi tiết mô tả hợp đồng cho **Thời gian**.
- Phân công nguồn lực trên dự án.

Ngữ cảnh thực tế cho **Thời gian** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Thời gian**.
- Các dòng nhật ký kế toán được tạo khi mục nhập thời gian được gửi.

Sau khi quyết định bảng giá vốn, hệ thống sẽ hoàn tất các bước sau để nhập tỷ lệ chi phí mặc định.

1. Hệ thống khớp các trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực** trong ước tính hoặc ngữ cảnh thực tế cho **Thời gian** dựa trên mô tả giá theo vai trò trên bảng giá. Việc so khớp này giả định rằng bạn đang sử dụng các thông số định giá tiêu chuẩn cho chi phí nhân công. Nếu bạn đã đặt cấu hình để hệ thống so khớp trường thay cho hoặc bên cạnh **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** hoặc kèm theo các trường đó, thì một tổ hợp khác sẽ được sử dụng để truy xuất mục mô tả giá vai trò phù hợp.
1. Nếu hệ thống tìm thấy một mục mô tả giá vai trò có tỷ lệ chi phí cho tổ hợp trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực**, tỷ lệ chi phí đó sẽ được dùng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể so khớp các giá trị **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực**, nó sẽ giảm thứ nguyên có mức độ ưu tiên thấp nhất, tìm kiếm mô tả giá vai trò khớp với hai giá trị thứ nguyên khác và tiếp tục giảm dần thứ nguyên cho đến khi tìm thấy hàng giá vai trò trùng khớp. Tỷ lệ chi phí từ bản ghi đó sẽ được sử dụng làm tỷ lệ chi phí mặc định. Nếu hệ thống không tìm thấy hàng giá có vai trò khớp, giá sẽ được đặt thành **0** (không) theo mặc định.

> [!NOTE]
> Nếu bạn đặt cấu hình mức độ ưu tiên khác cho các trường **Vai trò** và **Đơn vị nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, thì hành vi liền trước này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò có giá trị phù hợp với từng giá trị thứ nguyên về giá theo thứ tự ưu tiên. Các hàng có giá trị rỗng cho các thứ nguyên đó đứng cuối cùng.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Quyết định tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Chi phí

Ước tính ngữ cảnh cho **Chi phí** đề cập đến:

- Chi tiết mô tả báo giá cho **Chi phí**.
- Chi tiết mô tả hợp đồng cho **Chi phí**.
- Ước tính chi phí trên dự án.

Ngữ cảnh ước tính cho **Chi phí** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Chi phí**.
- Các dòng nhật ký kế toán được tạo khi mục nhập chi phí được gửi.

Sau khi quyết định bảng giá vốn, hệ thống sẽ hoàn tất các bước sau để nhập tỷ lệ chi phí mặc định.

1. Hệ thống khớp các trường **Thể loại** và **Đơn vị** trong ước tính hoặc ngữ cảnh thực tế cho **Chi phí** dựa trên mô tả giá theo thể loại trên bảng giá.
1. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ chi phí cho tổ hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ chi phí đó sẽ được sử dụng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể đối chiếu các giá trị trường **Danh mục** và **Đơn vị**, thì giá được đặt về **0** (không) theo mặc định.
1. Trong ngữ cảnh ước tính, nếu hệ thống có thể tìm thấy dòng giá cả thể loại phù hợp nhưng phương pháp định giá không phải là **Đơn giá**, thì tỷ lệ chi phí được đặt thành **0** (không) theo mặc định.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Quyết định tỷ lệ chi phí trên dòng giá trị thực tế và giá trị ước tính cho Vật tư

Ước tính ngữ cảnh cho **Vật tư** đề cập đến:

- Chi tiết mô tả báo giá cho **Vật tư**.
- Chi tiết mô tả hợp đồng cho **Vật tư**.
- Ước tính vật tư trên dự án.

Ngữ cảnh ước tính cho **Vật tư** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Vật tư**.
- Các dòng nhật ký kế toán được tạo khi Nhật ký sử dụng vật tư được gửi.

Sau khi quyết định bảng giá vốn, hệ thống sẽ hoàn tất các bước sau để nhập tỷ lệ chi phí mặc định.

1. Hệ thống sử dụng các trường **Sản phẩm** và **Đơn vị** trong ước tính hoặc ngữ cảnh thực tế cho **Vật tư** dựa trên mô tả hạng mục trong bảng giá trên bảng giá.
1. Nếu hệ thống tìm thấy một mô tả hạng mục trong bảng giá có tỷ lệ chi phí cho tổ hợp trường **Sản phẩm** và **Đơn vị**, thì tỷ lệ chi phí đó sẽ được sử dụng làm tỷ lệ chi phí mặc định.
1. Nếu hệ thống không thể khớp các giá trị **Sản phẩm** và **Đơn vị**, thì chi phí đơn vị được đặt thành **0** (không) theo mặc định.
1. Trong ngữ cảnh ước tính hoặc thực tế, nếu hệ thống có thể tìm thấy mô tả hạng mục trong bảng giá phù hợp nhưng phương pháp định giá không phải là **Số tiền theo loại tiền**, thì chi phí đơn vị được đặt thành **0** theo mặc định. Hành vi này xảy ra bởi vì Project Operations chỉ hỗ trợ phương pháp giá **Số tiền theo loại tiền** cho các vật tư được sử dụng trong một dự án.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
