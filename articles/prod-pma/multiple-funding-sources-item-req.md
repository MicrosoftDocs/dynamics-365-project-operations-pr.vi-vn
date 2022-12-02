---
title: Yêu cầu về hạng mục đối với hợp đồng dự án với nhiều nguồn tài trợ
description: Bài viết này cung cấp thông tin về cách định cấu hình và sử dụng các yêu cầu mặt hàng với nhiều nguồn vốn.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028514"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Yêu cầu về hạng mục đối với hợp đồng dự án với nhiều nguồn tài trợ

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Một số thỏa thuận hợp đồng cho các sản phẩm phân phối dựa trên dự án có thể yêu cầu nhiều nguồn vốn. Bài viết này giải thích cách chọn và định cấu hình các nguồn vốn mong muốn khi cần có nhiều nguồn cho một dự án hoặc hợp đồng dự án.

## <a name="terminology"></a>Thuật ngữ

- **Nguồn vốn** – Thực thể cấp vốn cho công việc hợp đồng dự án. Thực thể này có thể là một tổ chức nội bộ hoặc một tài khoản hóa đơn bên ngoài (khách hàng hoặc khoản trợ cấp).
- **Khách hàng dự án** – Thực thể mà công việc dự án được bàn giao.
- **Tài khoản hóa đơn** – Thực thể bên ngoài chi trả cho công việc dự án.

## <a name="example"></a>Ví dụ:

Contoso đã giành được hợp đồng gia hạn thiết bị với hai khách hàng của mình: Adatum US và Adatum Corporate. Hợp đồng bao gồm phần cứng và dịch vụ lắp đặt sẽ được bàn giao Adatum US (khách hàng của dự án). Phần cứng sẽ được cấp vốn bởi Adatum Corporate (tài khoản hóa đơn 1), và công việc lắp đặt sẽ được cấp vốn bởi Adatum US (tài khoản hóa đơn 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Thiết lập quy tắc mặc định tài khoản hóa đơn cho các yêu cầu mặt hàng

### <a name="prerequisites"></a>Điều kiện tiên quyết

- Microsoft Dynamics 365 Finance **phiên bản 10.0.27 trở lên** là bắt buộc để sử dụng các yêu cầu mặt hàng có nhiều tài khoản hóa đơn.
- Quản trị viên hệ thống của bạn phải bật tính năng **Cho phép các yêu cầu mặt hàng với nhiều nguồn vốn cho các trường hợp dựa trên sản xuất/nhập kho của Project Operations** trong không gian làm việc **Quản lý tính năng**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Thiết lập quy tắc mặc định của tài khoản hóa đơn

Để thiết lập các quy tắc mặc định cho tài khoản hóa đơn, hãy làm theo các bước sau.

1. Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.
1. Trên tab **Chung**, trong phần **Đơn bán hàng và yêu cầu mặt hàng**, đặt tùy chọn **Cho phép các dự án có nhiều nguồn vốn** thành **Có**.
1. Trong trường **Khách hàng mặc định**, chỉ định nơi xuất phát của khách hàng bàn giao của dự án trên yêu cầu mặt hàng theo mặc định:

    - **Từ nguồn vốn** – Khách hàng bàn giao của dự án mặc định đến từ nguồn vốn. Nếu nhiều nguồn vốn được liên kết với hợp đồng dự án, thì nguồn vốn đầu tiên trong danh sách sẽ được sử dụng.
    - **Từ dự án** – Khách hàng bàn giao của dự án mặc định đến từ khách hàng được chọn trong trường **Tài khoản bản ghi dự án**.

1. Tùy chọn: Đặt hoặc thay đổi tài khoản hóa đơn mặc định trên bản ghi dự án:

    1. Chuyển tới **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án** và mở chi tiết bản ghi dự án.
    2. Trên tab **Chung**, đặt hoặc cập nhật trường **Tài khoản hóa đơn mặc định**. Tài khoản mà bạn chỉ định sẽ được sử dụng làm tài khoản hóa đơn mặc định cho các yêu cầu mặt hàng mới được tạo cho dự án. Nếu bạn để trống trường này, tài khoản hóa đơn của nguồn vốn hợp đồng dự án đầu tiên sẽ được sử dụng theo mặc định. Tuy nhiên, người dùng sẽ có thể thay đổi tài khoản khi họ lưu bản ghi.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Chọn tài khoản hóa đơn để sử dụng khi bạn tạo yêu cầu mặt hàng

Để chọn tài khoản hóa đơn để sử dụng khi bạn tạo yêu cầu mặt hàng, hãy làm theo các bước sau.

1. Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án** và chọn bản ghi dự án.
1. Trên tab **Kế hoạch**, chọn **Yêu cầu mặt hàng**.
1. Tạo một bản ghi yêu cầu mặt hàng.

    - Theo mặc định, trường **Tài khoản hóa đơn** trong bản ghi được đặt thành tài khoản hóa đơn được đặt cho dự án. Bạn có thể thay đổi giá trị của trường **Tài khoản hóa đơn** và sau đó lưu bản ghi. Sau khi bản ghi được lưu, bạn không còn có thể cập nhật giá trị **Tài khoản hóa đơn**. Nếu bạn phải cập nhật giá trị **Tài khoản hóa đơn** cho yêu cầu mặt hàng, hãy xóa yêu cầu mặt hàng hiện có, sau đó tạo một yêu cầu mới có giá trị mong muốn.
    - Theo mặc định, trường **Khách hàng** cho yêu cầu mặt hàng được đặt dựa trên giá trị **Khách hàng mặc định** được đặt trên trang **Quản lý dự án và các tham số kế toán**.

    Khi bản ghi yêu cầu mặt hàng được lưu, hệ thống sẽ liên kết nó với bản ghi tiêu đề **Đơn bán hàng của yêu cầu mặt hàng**. Nếu không có tiêu đề đơn bán hàng đang mở nào có tài khoản hóa đơn đã chọn, hệ thống sẽ tạo một tiêu đề và liên kết dòng yêu cầu mặt hàng với nó.

> [!NOTE]
> Các yêu cầu mặt hàng luôn được lập hóa đơn đầy đủ cho tài khoản hóa đơn được đặt trong bản ghi. Hệ thống hiện không hỗ trợ các quy tắc phân bổ vốn có yêu cầu về mặt hàng và nó sẽ không phân chia việc đăng tải dựa trên thiết lập các quy tắc phân bổ vốn.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Tạo yêu cầu mặt hàng từ bản ghi dự báo mặt hàng

Để tạo yêu cầu mặt hàng từ bản ghi dự báo mặt hàng, hãy làm theo các bước sau.

1. Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án** và chọn bản ghi dự án.
1. Trên tab **Kế hoạch**, chọn **Dự báo mặt hàng**.
1. Tạo một bản ghi dự báo mặt hàng mới.
1. Tùy chọn: Trên tab **Dự án**, trong trường **Nguồn vốn**, chọn tài khoản hóa đơn mong muốn.
1. Chọn **Tạo yêu cầu mặt hàng** và xác nhận thông báo bạn nhận được.

    > [!NOTE]
    > Hệ thống sao chép giá trị **Nguồn vốn** từ bản ghi dự báo mặt hàng sang bản ghi yêu cầu mặt hàng mới được tạo.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Tài khoản hóa đơn mặc định khi hệ thống tự động tạo yêu cầu mặt hàng từ dòng đơn mua hàng

Nếu tùy chọn **Tạo yêu cầu mặt hàng** được đặt thành **Có** trên trang **Quản lý dự án và các tham số kế toán**, hệ thống sẽ tự động tạo yêu cầu mặt hàng khi dòng đơn mua hàng mới được lưu. Theo mặc định, các trường **Tài khoản hóa đơn** và **Yêu cầu mặt hàng** được đặt thành giá trị của trường **Tài khoản hóa đơn mặc định** trong bản ghi dự án. Hệ thống hiện không hỗ trợ cập nhật hoặc thay đổi tài khoản hóa đơn cho các bản ghi thuộc loại này.
