---
title: Mục nhập chi phí (bản đơn giản)
description: Chủ đề này cung cấp thông tin về cách làm việc với mục nhập chi phí trong một triển khai bản đơn giản.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965923"
---
# <a name="expense-entry-lite"></a>Mục nhập chi phí (bản đơn giản)

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Quản lý chi phí cơ bản hay đơn giản là khả năng ghi lại các khoản chi phí đơn giản. Bạn có thể ghi lại các chi phí cho một dự án, sau đó người phê duyệt dự án sẽ đánh giá và phê duyệt chúng.

Để biết thêm thông tin về khả năng chi phí trong Dynamics 365 Project Operations, hãy xem [Tổng quan về chi phí](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Ghi lại chi phí cơ bản

Bạn có thể ghi lại chi phí của mình để gửi cho người phê duyệt.

1. Đi đến **Chi phí** và chọn **Mới**.
2. Trên trang **Chi phí mới**, nhập thông tin chi phí bắt buộc, sau đó chọn **Lưu**.

## <a name="submit-a-basic-expense"></a>Gửi chi phí cơ bản

Sau khi hoàn tất việc ghi lại tất cả chi phí và sẵn sàng gửi để phê duyệt, bạn phải gửi chúng.

1. Đi đến **Chi phí** và chọn một chi phí. Hoặc chọn tất cả các chi phí bằng cách sử dụng hộp kiểm trên tiêu đề.
2. Chọn **Gửi**. Hệ thống xử lý các mục nhập đã chọn, sau đó tạo các yêu cầu phê duyệt chi phí.

## <a name="recall-a-basic-expense"></a>Thu hồi chi phí cơ bản

Khi gửi nhầm một khoản chi phí, bạn có thể thu hồi khoản chi phí đó. Thời gian cần thiết để thu hồi một mục nhập chi phí phụ thuộc vào giai đoạn phê duyệt của nó.  Nếu người phê duyệt chưa chấp thuận mục nhập, việc thu hồi có thể xảy ra ngay lập tức. Tuy nhiên, nếu mục nhập đã được phê duyệt, người phê duyệt được yêu cầu phê duyệt việc thu hồi và đảo ngược các giao dịch.

1. Đi đến **Chi phí**, sau đó, trong danh sách chi phí, hãy chọn chi phí cần thu hồi.
2. Chọn **Thu hồi**. Nếu mục nhập chi phí chưa được duyệt, hệ thống sẽ thu hồi ngay lập tức. Nếu mục nhập chi phí đã được phê duyệt, một yêu cầu thu hồi sẽ được tạo để thông báo cho người phê duyệt rằng bạn muốn đảo ngược chi phí. Khi đó, người phê duyệt sẽ xác nhận rằng việc đảo ngược có thể được thực hiện và mục nhập sẽ được trả lại.

## <a name="delete-a-basic-expense"></a>Xóa chi phí cơ bản

Các chi phí chưa được gửi có thể bị xóa. Để xóa một khoản chi phí đã được gửi, trước tiên bạn phải thu hồi nó.

## <a name="see-also"></a>Xem thêm

- [Tổng quan về phê duyệt](../approvals/approvals-overview.md)
