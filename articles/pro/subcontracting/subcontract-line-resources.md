---
title: Nguồn lực mô tả hợp đồng phụ
description: Bài viết này giải thích cách chỉ định các tài nguyên chuyên dụng được nhà cung cấp cung cấp cho một dòng hợp đồng phụ cụ thể theo thời gian.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522399"
---
# <a name="subcontract-line-resources"></a>Nguồn lực mô tả hợp đồng phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, nhà cung cấp có thể chỉ định nguồn lực sẽ được sử dụng để cung cấp năng lực nguồn lực đang được mua trên mô tả hợp đồng phụ cho thời gian.

## <a name="create-subcontract-line-resources"></a>Tạo nguồn lực mô tả hợp đồng phụ

Để tạo nguồn lực mô tả hợp đồng phụ, hãy hoàn thành các bước sau.

1. Trên ngăn điều hướng, chọn **Hợp đồng phụ** và mở hợp đồng phụ mà bạn muốn làm việc.
2. Mở mô tả hợp đồng phụ cho thời gian mà bạn muốn chỉ định nguồn lực của nhà cung cấp.
3. Trên tab **Nguồn lực mô tả hợp đồng phụ**, trong lưới phụ, hãy chọn **+ Nguồn lực mô tả hợp đồng phụ mới**.
4. Trên trang **Nguồn lực mô tả hợp đồng phụ mới**, nhập thông tin cần thiết rồi chọn **Lưu và đóng**.

Bảng sau giải thích các trường trên nguồn lực mô tả hợp đồng phụ.

| Trường | Mô tả | Tác động chức năng |
| ----- | ----------- | ----------------- |
| Nguồn lực có thể đăng ký | Chọn nguồn lực có thể đặt trước thuộc loại **Nhân viên hợp đồng** mà bạn muốn sử dụng làm nguồn lực trên mô tả hợp đồng phụ.| Nếu bạn chưa tạo nguồn lực có thể đặt trước cho nhân viên hợp đồng, hãy để trống trường này. Nguồn lực có thể đặt trước sẽ được tạo khi bạn lưu bản ghi.  |
| Liên hệ | Bạn có thể tạo nguồn lực mô tả hợp đồng phụ của mình từ một địa chỉ liên hệ hiện có. Sử dụng tra cứu để xem danh sách các liên hệ đang hoạt động trong hệ thống. Chọn một địa chỉ liên hệ cho nhà cung cấp của hợp đồng phụ này. Nếu liên hệ bạn đã chọn không phải là liên hệ hợp lệ cho nhà cung cấp trên hợp đồng phụ, thì bản ghi nguồn lực mô tả hợp đồng phụ sẽ không được lưu.| Nếu không có nguồn lực có thể đặt trước cho liên hệ đã chọn, hệ thống sẽ tạo nguồn lực có thể đặt trước cho liên hệ đã chọn trước khi tạo nguồn lực mô tả hợp đồng phụ. |
| Người dùng | Bạn có thể tạo nguồn lực mô tả hợp đồng phụ bằng cách chọn một người dùng đang hoạt động. Sử dụng tra cứu để xem danh sách những người dùng đang hoạt động trong hệ thống.| Nếu không có nguồn lực có thể đặt trước cho người dùng đã chọn, hệ thống sẽ tạo nguồn lực có thể đặt trước cho người dùng đã chọn trước khi tạo nguồn lực mô tả hợp đồng phụ. |
| Ngày bắt đầu | Ngày mà công việc của nhân viên hợp đồng phụ sẽ bắt đầu.| Nếu nguồn lực này được đăng ký trong khoảng thời gian trước phạm vi ngày này, một cảnh báo sẽ xảy ra. |
| Ngày kết thúc | Ngày mà công việc của nhân viên hợp đồng phụ kết thúc.| Nếu nguồn lực này được đăng ký trong khoảng thời gian sau phạm vi ngày này, một cảnh báo sẽ xảy ra. |
| Nhân công | Tổng số giờ nỗ lực mà người lao động ký hợp đồng sẽ dành cho mô tả hợp đồng phụ này.| Nếu nguồn lực này được đặt trước vượt quá nỗ lực được phân bổ trong hợp đồng phụ này, thì sẽ xuất hiện cảnh báo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]