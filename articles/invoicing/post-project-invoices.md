---
title: Tổng quan về quy trình lập hóa đơn
description: Bài viết này cung cấp tổng quan về quy trình lập hóa đơn trong Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có hàng.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923122"
---
# <a name="invoicing-process-overview"></a>Tổng quan về quy trình lập hóa đơn

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho cung cấp các khả năng toàn diện phù hợp với nhu cầu của cả Người quản lý dự án và Kế toán công nợ/kế toán dự án. Đối với quy trình lập hóa đơn, Người quản lý dự án quản lý tồn đọng lập hóa đơn dự án và Kế toán công nợ/kế toán dự án tạo một hóa đơn tiêu chuẩn và chính xác cho khách hàng.

![Sơ đồ quy trình lập hóa đơn.](./media/invoicing-flow.png)

Mô tả hợp đồng dự án xác định phương thức thanh toán cho các giao dịch dự án liên kết. Khi người quản lý Dự án phê duyệt các giao dịch thời gian và chi phí, hệ thống sẽ ghi lại các giao dịch trong **Thực tế dự án** thực thể và gửi thông tin đến **Quản lý dự án và kế toán** mô-đun trong Dynamics 365 Finance. Sau đó, kế toán dự án sẽ xem xét và đăng các hồ sơ bằng cách sử dụng [nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Nhật ký này bao gồm các chi tiết kế toán quan trọng cho thực tế dự án, chẳng hạn như thanh toán, nhóm thuế bán hàng, nhóm thuế bán hàng của mặt hàng thanh toán và các thông số tài chính.

Người quản lý dự án có thể xem xét các giao dịch bán hàng chưa lập hóa đơn bằng cách dùng phương pháp thanh toán theo thời gian và vật tư trong [Tồn đọng lập hóa đơn thời gian và tài liệu](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) và phương pháp thanh toán giá theo cố định trong [Mốc giá cố định](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Các dạng xem này cho phép bạn lọc và chọn các giao dịch cần có trong chu kỳ thanh toán tiếp theo và sau đó đánh dấu chúng là **Đã sẵn sàng để lập hóa đơn**.

Bạn có thể [tạo thủ công hóa đơn ước giá](../proforma-invoicing/create-manual-proforma-invoice.md) hoặc sử dụng một [quy trình định kỳ](../proforma-invoicing/configure-automated-invoice-creation.md). Người quản lý dự án có thể [điều chỉnh bản nháp hóa đơn ước giá](../proforma-invoicing/manage-proforma-invoice.md) khi cần rồi xác nhận hóa đơn.

Hóa đơn ước giá đã xác nhận được gửi đến mô-đun **Quản lý dự án và kế toán** trong phần Finance. Kế toán dự án định dạng và cập nhật đề xuất hóa đơn dự án, sau đó đăng và in tài liệu đó. Các hóa đơn dự án đã đăng được ghi cả trong Sổ cái chung lẫn sổ cái phụ của Khách hàng và Dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]