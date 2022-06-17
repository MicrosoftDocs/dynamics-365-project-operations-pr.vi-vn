---
title: Yêu cầu về hạng mục đối với hợp đồng dự án với nhiều nguồn tài trợ
description: Bài viết này cung cấp thông tin về cách định cấu hình và sử dụng các yêu cầu của mặt hàng với nhiều nguồn tài trợ.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931218"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Yêu cầu về hạng mục đối với hợp đồng dự án với nhiều nguồn tài trợ

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Một số thỏa thuận hợp đồng cho các sản phẩm được phân phối dựa trên dự án có thể yêu cầu nhiều nguồn tài trợ. Bài viết này giải thích cách chọn và cấu hình các nguồn tài trợ mong muốn khi cần có nhiều nguồn cho một dự án hoặc hợp đồng dự án.

## <a name="terminology"></a>Thuật ngữ

- **Nguồn tài trợ** - Đơn vị tài trợ cho công việc của hợp đồng dự án. Thực thể này có thể là một tổ chức nội bộ hoặc một tài khoản hóa đơn bên ngoài (khách hàng hoặc khoản tài trợ).
- **Khách hàng dự án** - Đơn vị mà công trình dự án được giao cho.
- **Tài khoản hóa đơn** - Đơn vị bên ngoài chi trả cho công việc của dự án.

## <a name="example"></a>Ví dụ:

Contoso đã giành được hợp đồng gia hạn thiết bị với hai khách hàng của mình: Adatum US và Adatum Corporate. Hợp đồng bao gồm phần cứng và dịch vụ cài đặt sẽ được giao cho Adatum US (khách hàng của dự án). Phần cứng sẽ được tài trợ bởi Adatum Corporate (tài khoản hóa đơn 1), và công việc cài đặt sẽ được tài trợ bởi Adatum US (tài khoản hóa đơn 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Thiết lập quy tắc mặc định tài khoản hóa đơn cho các yêu cầu mặt hàng

### <a name="prerequisites"></a>Điều kiện tiên quyết

- Microsoft Dynamics 365 Tài chính và Hoạt động **phiên bản 10.0.27 trở lên** bắt buộc phải sử dụng các yêu cầu mặt hàng có nhiều tài khoản hóa đơn.
- Quản trị viên hệ thống của bạn phải bật **Cho phép các yêu cầu về Mặt hàng với nhiều nguồn tài trợ cho Hoạt động dự án trong các tình huống có sẵn / dựa trên sản xuất** tính năng trong **Quản lý tính năng** không gian làm việc.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Thiết lập quy tắc mặc định tài khoản hóa đơn

Để thiết lập các quy tắc mặc định cho tài khoản hóa đơn, hãy làm theo các bước sau.

1. Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.
1. Trên **Chung** tab, trong **Đơn đặt hàng bán hàng và yêu cầu mặt hàng** phần, thiết lập **Cho phép các dự án có nhiều nguồn tài trợ** tùy chọn để **Đúng**.
1. Bên trong **Khách hàng mặc định**, chỉ định nơi khách hàng giao dự án theo yêu cầu hạng mục xuất phát theo mặc định:

    - **Từ nguồn tài trợ** - Khách hàng giao dự án mặc định đến từ nguồn tài trợ. Nếu nhiều nguồn tài trợ được liên kết với hợp đồng dự án, thì nguồn vốn đầu tiên trong danh sách sẽ được sử dụng.
    - **Từ dự án** - Khách hàng giao dự án mặc định đến từ khách hàng được chọn trong **Tài khoản hồ sơ dự án** đồng ruộng.

1. Tùy chọn: Đặt hoặc thay đổi tài khoản hóa đơn mặc định trên bản ghi dự án:

    1. Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án**, và mở chi tiết hồ sơ dự án.
    2. Trên **Chung** tab, đặt hoặc cập nhật **Tài khoản hóa đơn mặc định** đồng ruộng. Tài khoản mà bạn chỉ định sẽ được sử dụng làm tài khoản hóa đơn mặc định cho các yêu cầu mặt hàng mới được tạo cho dự án. Nếu bạn để trống trường này, tài khoản hóa đơn của nguồn tài trợ hợp đồng dự án đầu tiên sẽ được sử dụng theo mặc định. Tuy nhiên, người dùng sẽ có thể thay đổi tài khoản khi họ lưu bản ghi.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Chọn tài khoản hóa đơn để sử dụng khi bạn tạo yêu cầu mặt hàng

Để chọn tài khoản hóa đơn sẽ sử dụng khi bạn tạo yêu cầu mặt hàng, hãy làm theo các bước sau.

1. Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án**, và chọn bản ghi dự án.
1. Trên **Kế hoạch** tab, chọn **Yêu cầu mặt hàng**.
1. Tạo bản ghi yêu cầu mặt hàng mới.

    - Theo mặc định, **Tài khoản hóa đơn** trường trong bản ghi được đặt thành tài khoản hóa đơn được đặt cho dự án. Bạn có thể thay đổi giá trị của **Tài khoản hóa đơn** và sau đó lưu bản ghi. Sau khi bản ghi được lưu, bạn không còn có thể cập nhật **Tài khoản hóa đơn** giá trị. Nếu bạn phải cập nhật **Tài khoản hóa đơn** giá trị cho yêu cầu mặt hàng, xóa yêu cầu mặt hàng hiện có, sau đó tạo một yêu cầu mới có giá trị mong muốn.
    - Theo mặc định, **khách hàng** trường cho yêu cầu mặt hàng được đặt dựa trên **Khách hàng mặc định** giá trị được đặt trên **Các thông số kế toán và quản lý dự án** trang.

    Khi bản ghi yêu cầu mặt hàng được lưu, hệ thống sẽ liên kết nó với **Yêu cầu mặt hàng đơn đặt hàng** bản ghi tiêu đề. Nếu không có tiêu đề đơn đặt hàng mở nào có tài khoản hóa đơn đã chọn, hệ thống sẽ tạo một tài khoản và liên kết dòng yêu cầu mặt hàng với tài khoản đó.

> [!NOTE]
> Các yêu cầu về mặt hàng luôn được lập hóa đơn đầy đủ vào tài khoản hóa đơn được thiết lập trong hồ sơ. Hệ thống hiện không hỗ trợ các quy tắc phân bổ tài trợ có yêu cầu về mặt hàng và nó sẽ không phân chia việc đăng tải dựa trên thiết lập các quy tắc phân bổ tài trợ.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Tạo yêu cầu mặt hàng từ bản ghi dự báo mặt hàng

Để tạo yêu cầu mặt hàng từ bản ghi dự báo mặt hàng, hãy làm theo các bước sau.

1. Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án** và chọn bản ghi dự án.
1. Trên **Kế hoạch** tab, chọn **Dự báo mặt hàng**.
1. Tạo một bản ghi dự báo mặt hàng mới.
1. Tùy chọn: Trên **Dự án** tab, trong **Nguồn tài trợ** trường, chọn tài khoản hóa đơn mong muốn.
1. Lựa chọn **Tạo yêu cầu mặt hàng**, và xác nhận thông báo mà bạn nhận được.

    > [!NOTE]
    > Hệ thống sao chép **Nguồn tài trợ** giá trị từ bản ghi dự báo mặt hàng sang bản ghi yêu cầu mặt hàng mới được tạo.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Tài khoản hóa đơn mặc định khi hệ thống tự động tạo yêu cầu mặt hàng từ dòng đơn đặt hàng

Nếu **Tạo yêu cầu mặt hàng** tùy chọn được đặt thành **Đúng** trên **Quản lý dự án và các thông số kế toán** trang, hệ thống tự động tạo yêu cầu mặt hàng khi dòng đặt mua dự án mới được lưu. Theo mặc định, **Tài khoản hóa đơn** và **Yêu cầu mặt hàng** các trường được đặt thành giá trị của **Tài khoản hóa đơn mặc định** trường trong hồ sơ dự án. Hệ thống hiện không hỗ trợ cập nhật hoặc thay đổi tài khoản hóa đơn cho các bản ghi thuộc loại này.
