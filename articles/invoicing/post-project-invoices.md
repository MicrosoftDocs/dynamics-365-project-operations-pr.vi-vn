---
title: Tổng quan về quy trình lập hóa đơn
description: Chủ đề này trình bày tổng quan về quy trình lập hóa đơn trong Project Operations cho các cho tình huống dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 804d42f7e8bfd103b9143dc0f5c7ddecdee9e66e6072c3e7bf76b2a8c549cf55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003797"
---
# <a name="invoicing-process-overview"></a>Tổng quan về quy trình lập hóa đơn

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho cung cấp các khả năng toàn diện phù hợp với nhu cầu của cả Người quản lý dự án và Kế toán công nợ/kế toán dự án. Đối với quy trình lập hóa đơn, Người quản lý dự án quản lý tồn đọng lập hóa đơn dự án và Kế toán công nợ/kế toán dự án tạo một hóa đơn tiêu chuẩn và chính xác cho khách hàng.

![Sơ đồ quy trình lập hóa đơn.](./media/invoicing-flow.png)

Mô tả hợp đồng dự án xác định phương thức thanh toán cho các giao dịch dự án liên kết. Khi người quản lý Dự án phê duyệt các giao dịch thời gian và chi phí, hệ thống sẽ ghi lại các giao dịch vào thực thể **Thực tế dự án** và gửi thông tin đến mô-đun **Quản lý dự án và kế toán** trong Dynamics 365 Finance. Sau đó, kế toán dự án sẽ xem xét và đăng các hồ sơ bằng cách sử dụng [nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Nhật ký này bao gồm các chi tiết kế toán quan trọng cho thực tế dự án, chẳng hạn như thanh toán, nhóm thuế bán hàng, nhóm thuế bán hàng của mặt hàng thanh toán và các thông số tài chính.

Người quản lý dự án có thể xem xét các giao dịch bán hàng chưa lập hóa đơn bằng cách dùng phương pháp thanh toán theo thời gian và vật tư trong [Tồn đọng lập hóa đơn thời gian và tài liệu](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) và phương pháp thanh toán giá theo cố định trong [Mốc giá cố định](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Các dạng xem này cho phép bạn lọc và chọn các giao dịch cần có trong chu kỳ thanh toán tiếp theo và sau đó đánh dấu chúng là **Đã sẵn sàng để lập hóa đơn**.

Bạn có thể [tạo thủ công hóa đơn ước giá](../proforma-invoicing/create-manual-proforma-invoice.md) hoặc sử dụng một [quy trình định kỳ](../proforma-invoicing/configure-automated-invoice-creation.md). Người quản lý dự án có thể [điều chỉnh bản nháp hóa đơn ước giá](../proforma-invoicing/manage-proforma-invoice.md) khi cần rồi xác nhận hóa đơn.

Hóa đơn ước giá đã xác nhận được gửi đến mô-đun **Quản lý dự án và kế toán** trong phần Finance. Kế toán dự án định dạng và cập nhật đề xuất hóa đơn dự án, sau đó đăng và in tài liệu đó. Các hóa đơn dự án đã đăng được ghi cả trong Sổ cái chung lẫn sổ cái phụ của Khách hàng và Dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]