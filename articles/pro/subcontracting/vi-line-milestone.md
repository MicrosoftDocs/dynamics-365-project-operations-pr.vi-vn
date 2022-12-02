---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho các mốc
description: Bài viết này giải thích cách tạo mô tả hóa đơn của nhà cung cấp cho các mốc trên hợp đồng phụ.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261055"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho các mốc

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có các mô tả hóa đơn của nhà cung cấp cho các mốc được xác định trên một mô tả hợp đồng phụ. Người quản lý dự án có thể sử dụng mô tả hóa đơn của nhà cung cấp cho các mốc để ghi lại chi phí dịch vụ được mua dưới dạng chi phí dựa trên mốc phát sinh trên các dịch vụ hoặc sản phẩm được mua cho dự án.

Mô tả hóa đơn của nhà cung cấp cho các mốc phải luôn tham chiếu đến mô tả hợp đồng phụ có phương thức thanh toán Giá cố định. Khi mô tả hóa đơn của nhà cung cấp cho các mốc tham chiếu đến mô tả hợp đồng phụ, người quản lý dự án sẽ có thể đối sánh và xác minh các chi phí cơ bản về thời gian, chi phí hoặc vật tư liên quan đến mô tả hợp đồng phụ đó dựa trên mốc đang được nhà cung cấp lập hóa đơn.

Bảng dưới đây cung cấp các thông tin về các trường trên mô tả hóa đơn của nhà cung cấp cho các mốc.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của mô tả hóa đơn của nhà cung cấp để giúp xác định. | Tên này sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các dịch vụ và sản phẩm đang được lập hóa bởi nhà cung cấp trên mô tả hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các dịch vụ được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các mô tả trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các mô tả hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Mô tả hợp đồng phụ | Mô tả hợp đồng phụ mà các dịch vụ được đặt hàng. Danh sách các mô tả hợp đồng phụ có thể được chọn được giới hạn trong các mô tả trên hợp đồng phụ đã chọn. | Khi mô tả hợp đồng phụ được chọn trên mô tả hóa đơn của nhà cung cấp cho các mốc, các trường **Vai trò** và **Thể loại giao dịch** và các trường liên quan đến sản phẩm, không liên quan và không có sẵn. Các trường **Số lượng**, **Đơn vị**, và **Nhóm đơn vị** này cũng không liên quan đến các mô tả hóa đơn của nhà cung cấp dựa trên mốc. |
| Ngày giao dịch | Ngày mà chi phí thực tế của mô tả hóa đơn của nhà cung cấp sẽ được ghi lại trên dự án. | Không có |
| Lớp giao dịch | Chọn **Mốc** để ghi lại hóa đơn của nhà cung cấp cho một mốc hoàn thành đã được xác định trên mô tả hợp đồng phụ. | Không có |
| Mốc | Chọn mốc được xác định trên mô tả hợp đồng phụ có liên quan được đánh dấu là **Sẵn sàng lập hóa đơn**. | Các mốc mô tả hợp đồng có trạng thái **Sẵn sàng lập hóa đơn** có thể được chọn trên mô tả hóa đơn của nhà cung cấp. |
| Dự án | Tên của dự án mà các dịch vụ đang lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không thể để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các dịch vụ đang lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là không bắt buộc. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh mô tả hóa đơn của nhà cung cấp với lớp giao dịch trên mô tả hợp đồng phụ liên quan được ghi lại trên bất kỳ nhiệm vụ nào của dự án. Nếu mô tả hóa đơn của nhà cung cấp không tham chiếu đến mô tả hợp đồng phụ và trường này để trống, thì chi phí thực tế được tạo bởi mô tả hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ doanh số thực tế chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí có thể không được lập hóa đơn cho khách hàng cuối. |
| Số tiền mốc | Nhập giá trị của mốc được xác định trên mô tả hợp đồng phụ đã sẵn sàng lập hóa đơn. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng số tiền | Tổng số tiền của mô tả hợp hóa đơn của nhà cung cấp, bao gồm thuế. Trường này được tính là *Số tiền mốc* + *Thuế bán hàng*. | Không có |

> [!NOTE]
> Khi mô tả hóa đơn của nhà cung cấp tham chiếu đến mốc mô tả hợp đồng phụ được tạo, trạng thái của mốc hợp đồng phụ được cập nhật thành **Đã tạo hóa đơn của nhà cung cấp**. Sau đó, khi hóa đơn của nhà cung cấp đó được xác nhận, trạng thái của mốc mô tả hợp đồng phụ được cập nhật thành **Đã xác nhận hóa đơn của nhà cung cấp**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
