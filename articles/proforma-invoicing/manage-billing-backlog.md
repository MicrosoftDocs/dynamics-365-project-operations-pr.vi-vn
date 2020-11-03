---
title: Quản lý mục tồn đọng lập hóa đơn
description: Chủ đề này cung cấp thông tin về cách xem và làm việc với mục tồn đọng lập hóa đơn trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088164"
---
# <a name="manage-the-billing-backlog"></a>Quản lý mục tồn đọng lập hóa đơn

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations có hai dạng xem chuyên dụng để giúp bạn làm việc và quản lý mục tồn đọng lập hóa đơn. Chúng là **Mốc giá cố định** và **Tồn đọng thanh toán thời gian và vật tư**. Để chọn một dạng xem, trong khu vực **Bán hàng** của Project Operations, trên trang điều hướng bên trái, hãy chọn **Thanh toán**. Các liên kết mục tồn đọng lập hóa đơn được lưu ở đó.

## <a name="fixed-price-milestones"></a>Mốc Giá Cố định

Dạng xem này liệt kê tất cả các mốc giá cố định trên tất cả các mục mô tả hợp đồng dự án trong hệ thống. Một hoặc nhiều mốc có thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn** ở dạng xem này. Khi bạn đánh dấu một mốc là **Đã sẵn sàng để lập hóa đơn** , mốc đó sẽ có sẵn để tạo hóa đơn nháp.

Khi các mục mô tả hợp đồng nhiều khách hàng có phương thức thanh toán là giá cố định, mỗi khách hàng trên mục mô tả hợp đồng sẽ được tạo một mốc. Người dùng tạo một mốc và mốc đó được chia nội bộ thành các bản ghi mốc riêng cho khách hàng, theo tỷ lệ phần trăm phân chia thanh toán được xác định cho từng khách hàng trên mục mô tả hợp đồng. Ở dạng xem **Mốc giá cố định** , bạn sẽ thấy các bản ghi mốc riêng cho khách hàng cụ thể. Mỗi bản ghi mốc này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này. Khi một hoặc nhiều phần phân tách mốc có liên quan được đánh dấu là **Đã sẵn sàng để lập hóa đơn** , tiêu đề sẽ chuyển từ trạng thái **Chưa bắt đầu** sang **Đang tiến hành**. Khi tất cả các phần phân tách mốc đã được lập hóa đơn, trạng thái mốc ở tiêu đề sẽ trở thành **Đã hoàn thành**.

Một mốc trên hóa đơn nháp được hiển thị ở dạng xem này với trạng thái thanh toán là **Đã tạo hóa đơn khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên bản ghi này được cập nhật thành **Đã đăng hóa đơn**. Bạn không nên cập nhật giá trị trạng thái này bằng mã tùy chỉnh. Project Operations sẽ không hoạt động chính xác nếu các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.

## <a name="time-and-material-billing-backlog"></a>Tồn đọng Thanh toán Thời gian và Vật liệu

Dạng xem này liệt kê tất cả các giá trị thực tế doanh số chưa được lập hóa đơn trên tất cả các hợp đồng dự án trong hệ thống. Một hoặc nhiều giá trị thực tế doanh số chưa lập hóa đơn có thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn** ở dạng xem này. Việc đánh dấu một giá trị thực tế doanh số chưa lập hóa đơn là **Đã sẵn sàng để lập hóa đơn** sẽ làm cho mục chuyển sang trạng thái có sẵn để đưa vào hóa đơn nháp.

Các giá trị thực tế doanh số chưa lập hóa đơn có trạng thái **Không quá** là **Không thành công** sẽ không thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn**. Nếu các giá trị thực tế này cần được đánh dấu như vậy, hãy đặt lại trạng thái trên các giá trị thực tế khác trên mục mô tả hợp đồng đã cam kết, rồi đánh giá trạng thái **Không quá**.

Trong trường hợp mục mô tả hợp đồng nhiều khách hàng có phương thức thanh toán là thời gian và vật tư, khi thời gian và chi phí được chấp thuận, giá trị thực tế doanh số chưa lập hóa đơn sẽ được tạo cho mỗi khách hàng trên mục mô tả hợp đồng theo tỷ lệ phần trăm phân chia thanh toán được xác định cho từng khách hàng trên mục mô tả hợp đồng. Ở dạng xem **Tồn đọng thanh toán thời gian và vật tư** , bạn sẽ thấy các giá trị thực tế doanh số chưa lập hóa đơn riêng cho khách hàng cụ thể. Mỗi bản ghi giá trị thực tế doanh số chưa lập hóa đơn này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này.

Một giá trị thực tế doanh số chưa lập hóa đơn trên hóa đơn nháp được hiển thị ở dạng xem này với **Trạng thái thanh toán** là **Đã tạo hóa đơn khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên bản ghi này được cập nhật thành **Đã đăng hóa đơn khách hàng**. Bạn không nên cập nhật giá trị trạng thái này bằng mã tùy chỉnh khi bản ghi ở trạng thái này. Project Operations sẽ không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.
