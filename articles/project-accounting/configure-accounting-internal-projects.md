---
title: Đặt cấu hình hoạt động kế toán cho dự án nội bộ
description: Bài viết này cung cấp thông tin về cách thiết lập các thông lệ kế toán cho các dự án nội bộ trong Hoạt động Dự án.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919488"
---
# <a name="configure-accounting-for-internal-projects"></a>Đặt cấu hình hoạt động kế toán cho dự án nội bộ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Dự án nội bộ giúp cho các công ty theo dõi chi phí liên quan đến các hoạt động không được lập hóa đơn cho khách hàng. Các dự án nội bộ có thể là:

- Phát triển sản phẩm, chẳng hạn như ứng dụng dành cho thiết bị di động, và theo dõi chi phí liên quan đến việc phát triển.
- Quản lý thời gian và chi phí trước khi bán hàng. Sau này, dự án nội bộ trước khi bán hàng này có thể được chuyển đổi thành dự án có thể lập hóa đơn nếu bạn giành được báo giá.

Bất kỳ dự án nào không liên kết với một hợp đồng trong Dynamics 365 Project Operations đều được xem là nội bộ. Hồ sơ doanh thu và chi phí dự án không được sử dụng để xác định các quy tắc kế toán cho dự án này. Chi phí của dự án nội bộ luôn được đăng theo nguyên tắc lãi và lỗ. Tài khoản sổ dùng cho các mục đăng được xác định trên trang **Thiết lập đăng sổ**.

- Các giao dịch thời gian được đăng bằng cách ghi nợ vào tài khoản **Chi phí** và ghi có vào tài khoản **Phân bổ bảng lương**.
- Các giao dịch chi phí được đăng bằng cách ghi nợ vào tài khoản **Chi phí** và ghi có vào tài khoản **Tài khoản bù trừ chi phí**.
- Các giao dịch hạng mục được đăng bằng cách ghi nợ tài khoản **Chi phí** và ghi có tài khoản **Chi phí - Hạng mục**.

Sau khi các giao dịch được đăng vào dự án, nếu dự án được liên kết với hợp đồng dự án, thì hệ thống sẽ đảo ngược tất cả các giao dịch đã tích lũy và tạo giao dịch có thể lập hóa đơn mới. Giao dịch có thể lập hóa đơn tuân theo các quy tắc kế toán được xác định trong hồ sơ chi phí và doanh thu tương ứng của Dự án.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
