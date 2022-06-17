---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho các mốc
description: Bài viết này giải thích cách tạo các dòng hóa đơn của nhà cung cấp cho các mốc quan trọng trong hợp đồng phụ.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931356"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho các mốc

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có các dòng hóa đơn của nhà cung cấp cho các mốc quan trọng được xác định trên một dòng hợp đồng phụ. Người quản lý dự án có thể sử dụng các dòng hóa đơn của nhà cung cấp cho các mốc quan trọng để ghi lại chi phí dịch vụ được mua sắm dưới dạng chi phí dựa trên mốc phát sinh trên các dịch vụ hoặc sản phẩm được mua sắm cho dự án.

Các dòng hóa đơn của nhà cung cấp cho các mốc quan trọng phải luôn tham chiếu đến dòng hợp đồng phụ có phương pháp thanh toán Giá cố định. Khi dòng hóa đơn của nhà cung cấp cho các mốc quan trọng tham chiếu đến dòng hợp đồng phụ, người quản lý dự án sẽ có thể đối sánh và xác minh các chi phí cơ bản về thời gian, chi phí hoặc vật liệu liên quan đến dòng hợp đồng phụ đó so với mốc đang được nhà cung cấp lập hóa đơn.

Bảng sau cung cấp thông tin về các trường trên các dòng hóa đơn của nhà cung cấp cho các mốc quan trọng.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của dòng hóa đơn của nhà cung cấp, để giúp xác định. | Tên này sẽ được hiển thị dưới dạng cột đầu tiên trong tất cả các tra cứu dựa trên các dòng hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các dịch vụ đang được nhà cung cấp lập hóa đơn trên dòng hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các dịch vụ được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các dòng trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các dòng hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Dòng hợp đồng phụ | Dòng hợp đồng phụ mà các dịch vụ đã được đặt hàng. Danh sách các dòng hợp đồng phụ có thể được chọn được giới hạn trong các dòng trên hợp đồng phụ đã chọn. | Khi dòng hợp đồng phụ được chọn trên dòng hóa đơn của nhà cung cấp cho các mốc quan trọng, **Vai diễn** và **Loại giao dịch** và các trường liên quan đến sản phẩm, không liên quan và không có sẵn. Các **Số lượng**, **vị**, và **Nhóm đơn vị** các trường cũng không liên quan đến các dòng hóa đơn của nhà cung cấp dựa trên cột mốc. |
| Ngày giao dịch | Ngày mà chi phí thực tế của dòng hóa đơn nhà cung cấp sẽ được ghi trên dự án. | Không có |
| Lớp giao dịch | Lựa chọn **Cột mốc** để ghi lại hóa đơn của nhà cung cấp cho một mốc hoàn thành đã được xác định trên dòng hợp đồng phụ. | Không có |
| Mốc | Chọn cột mốc được xác định trên dòng hợp đồng phụ có liên quan được đánh dấu là **Sẵn sàng lập hóa đơn**. | Các mốc của dòng hợp đồng phụ có trạng thái **Sẵn sàng xuất hóa đơn** có thể được chọn trên một dòng hóa đơn của nhà cung cấp. |
| Dự án | Tên của dự án mà các dịch vụ đang được lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không được để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các dịch vụ đang được lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là tùy chọn. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh dòng hóa đơn của nhà cung cấp với loại giao dịch trên dòng hợp đồng phụ có liên quan được ghi lại trên bất kỳ nhiệm vụ nào của dự án. Nếu dòng hóa đơn của nhà cung cấp không tham chiếu đến dòng hợp đồng phụ và trường này để trống, thì giá thực tế được tạo bởi dòng hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ hướng dẫn bán hàng chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí có thể không được lập hóa đơn cho khách hàng cuối cùng. |
| Số tiền mốc | Nhập giá trị của mốc được xác định trên dòng hợp đồng phụ đã sẵn sàng để lập hóa đơn. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng cộng | Tổng số tiền của dòng hóa đơn của nhà cung cấp, bao gồm cả thuế. Trường này được tính là *Số tiền quan trọng* + *Thuế doanh thu*. | Không có |

> [!NOTE]
> Khi dòng hóa đơn của nhà cung cấp tham chiếu đến mốc dòng hợp đồng phụ được tạo, trạng thái của mốc hợp đồng phụ được cập nhật thành **Hóa đơn của nhà cung cấp đã được tạo**. Sau đó, khi hóa đơn của nhà cung cấp đó được xác nhận, trạng thái của mốc dòng hợp đồng phụ được cập nhật thành **Hóa đơn của nhà cung cấp đã được xác nhận**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
