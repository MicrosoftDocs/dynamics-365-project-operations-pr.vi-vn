---
title: Quản lý tồn đọng lập hóa đơn dự án
description: Chủ đề này cung cấp thông tin về các dạng xem khác nhau có thể sử dụng khi quản lý mục tồn đọng lập hóa đơn trên các dự án.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988317"
---
# <a name="manage-project-billing-backlog"></a>Quản lý tồn đọng lập hóa đơn dự án 

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations có các chế độ xem chuyên biệt để giúp quản lý hóa đơn tồn đọng. Để quản lý công việc lập hóa đơn còn tồn đọng, hãy chọn các liên kết trong khu vực **Bán hàng**, phía dưới phần **Thanh toán**. 

Hiện có các dạng xem sau đây:

- Tiền tạm ứng và Tiền trả trước
- Tiền tạm ứng và Tiền trả trước khả dụng
- Mốc Giá Cố định
- Tồn đọng Thanh toán Sản phẩm
- Tồn đọng Thanh toán Thời gian và Vật liệu

## <a name="retainers-and-advances"></a>Tiền tạm ứng và Tiền trả trước

Dạng xem **Khoản trả trước và khoản tạm ứng** liệt kê mọi khoản trả trước và tạm ứng cho tất cả các hợp đồng dự án trong hệ thống. Sau khi một khoản trả trước hoặc tạm ứng được lập hóa đơn, số tiền tạm ứng/trả trước đó sẽ có sẵn để sử dụng.

## <a name="available-retainers-and-advances"></a>Tiền tạm ứng và Tiền trả trước khả dụng

Dạng xem **Khoản trả trước và khoản tạm ứng hiện có** liệt kê mọi khoản trả trước và tạm ứng hiện có cho tất cả các hợp đồng dự án trong hệ thống. Sau khi một khoản trả trước hoặc tạm ứng được lập hóa đơn, số tiền tạm ứng/trả trước đó sẽ có sẵn để sử dụng và được thêm vào danh sách này. Sau khi số tiền tạm ứng/trả trước được sử dụng hết, số tiền đó sẽ bị xóa khỏi danh sách.

## <a name="fixed-price-milestones"></a>Mốc Giá Cố định

Dạng xem **Mốc giá cố định** liệt kê mọi mốc giá cố định cho tất cả các phần mô tả hợp đồng trong hệ thống. Trong dạng xem này, một hoặc nhiều mốc có thể được đánh dấu là **Sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn**. Nếu đánh dấu một mốc là **Sẵn sàng để lập hóa đơn**, thì bạn có thể đưa mốc đó vào hóa đơn nháp.

Khi phần mô tả hợp đồng với nhiều khách hàng có phương thức thanh toán theo giá cố định, một mốc sẽ được tạo cho từng khách hàng có trong phần mô tả hợp đồng đó. Một mốc có thể được tạo, sau đó chia thành các hồ sơ của mốc dành riêng cho từng khách hàng. Việc phân chia này diễn ra nội bộ và phù hợp với tỷ lệ phần trăm thanh toán được xác định cho từng khách hàng trong phần mô tả hợp đồng. Ở dạng xem **Mốc giá cố định**, bạn sẽ thấy các hồ sơ của mốc dành riêng cho từng khách hàng. Mỗi bản ghi mốc này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này. Khi một hoặc nhiều mốc phân tách có liên quan được đánh dấu là **Sẵn sàng để lập hóa đơn**, trạng thái tiêu đề sẽ chuyển sang **Đang tiến hành** từ trạng thái **Chưa bắt đầu**. Khi tất cả các mốc phân tách được lập hóa đơn, trạng thái mốc trong tiêu đề sẽ được cập nhật thành **Đã hoàn thành**.

Một mốc trên hóa đơn nháp được hiển thị ở dạng xem này với trạng thái thanh toán là **Đã tạo hóa đơn khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên hồ sơ được cập nhật thành **Đã đăng hóa đơn khách hàng**. Không cập nhật giá trị trạng thái này bằng mã tùy chỉnh. Project Operations không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.

## <a name="product-billing-backlog"></a>Tồn đọng Thanh toán Sản phẩm

Dạng xem **Tồn đọng thanh toán sản phẩm** liệt kê mọi phần mô tả hợp đồng dựa trên sản phẩm cho tất cả các hợp đồng dự án trong hệ thống. Trong dạng xem này, một hoặc nhiều phần mô tả hợp đồng dựa trên sản phẩm có thể được đánh dấu là **Sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn**. Nếu đánh dấu một phần mô tả hợp đồng dựa trên sản phẩm là **Sẵn sàng để lập hóa đơn**, thì bạn có thể đưa phần mô tả đó vào hóa đơn nháp.

Phần mô tả hợp đồng dựa trên sản phẩm có trên hóa đơn nháp sẽ hiển thị ở dạng xem này với trạng thái thanh toán là **Đã tạo hóa đơn cho khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên bản ghi này được cập nhật thành **Đã đăng hóa đơn khách hàng**. Không cập nhật giá trị trạng thái này bằng mã tùy chỉnh. Project Operations không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.

## <a name="time-and-material-billing-backlog"></a>Tồn đọng Thanh toán Thời gian và Vật liệu

Dạng xem **Tồn đọng thanh toán cho thời gian và vật tư** liệt kê mọi giao dịch bán hàng thực tế chưa thanh toán cho tất cả các hợp đồng dự án trong hệ thống chưa được lập hóa đơn. Một hoặc nhiều giá trị thực tế doanh số chưa lập hóa đơn có thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn** ở dạng xem này. Việc đánh dấu một giá trị thực tế doanh số chưa lập hóa đơn là **Đã sẵn sàng để lập hóa đơn** sẽ làm cho mục chuyển sang trạng thái có sẵn để đưa vào hóa đơn nháp.

Bạn không thể đánh dấu các giao dịch bán hàng thực tế chưa thanh toán có trạng thái **Không vượt quá** (**Không thành công**) là **Sẵn sàng để lập hóa đơn**. Nếu các giao dịch thực tế này cần được đánh dấu là **Sẵn sàng để lập hóa đơn**, hãy đặt lại trạng thái đó trên các giao dịch thực tế khác trong phần mô tả hợp đồng đã cam kết. Sau đó, đánh giá lại trạng thái **Không vượt quá**.

Nếu phần mô tả hợp đồng với nhiều khách hàng có phương thức thanh toán theo thời gian và vật tư, thì khi thời gian và chi phí được phê duyệt, một giao dịch bán hàng thực tế chưa thanh toán sẽ được tạo cho từng khách hàng trên phần mô tả hợp đồng theo tỷ lệ phần trăm thanh toán được xác định cho từng khách hàng đó. Ở dạng xem **Tồn đọng thanh toán cho thời gian và vật tư**, bạn sẽ thấy các giao dịch bán hàng thực tế chưa thanh toán cho từng khách hàng cụ thể này. Mỗi bản ghi giá trị thực tế doanh số chưa lập hóa đơn này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này.

Một giao dịch bán hàng thực tế chưa thanh toán có trên hóa đơn nháp sẽ hiển thị trong dạng xem này với trạng thái thanh toán là **Đã tạo hóa đơn cho khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên bản ghi này được cập nhật thành **Đã đăng hóa đơn khách hàng**. Không cập nhật giá trị trạng thái này bằng mã tùy chỉnh. Project Operations không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
