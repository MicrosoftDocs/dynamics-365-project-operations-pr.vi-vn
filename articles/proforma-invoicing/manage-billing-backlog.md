---
title: Quản lý mục tồn đọng lập hóa đơn
description: Chủ đề này cung cấp thông tin về cách xem và làm việc với mục tồn đọng lập hóa đơn trong Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011937"
---
# <a name="manage-billing-backlog"></a>Quản lý mục tồn đọng lập hóa đơn

_ **Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

Dynamics 365 Project Operations có các chế độ xem chuyên biệt để giúp quản lý hóa đơn tồn đọng. Để quản lý công việc lập hóa đơn còn tồn đọng, hãy chọn các liên kết trong khu vực **Bán hàng**, phía dưới phần **Thanh toán**. 

Hiện có các dạng xem sau đây:

- Tiền tạm ứng và Tiền trả trước
- Tiền tạm ứng và Tiền trả trước khả dụng
- Mốc Giá Cố định
- Tồn đọng Thanh toán Thời gian và Vật liệu

## <a name="retainers-and-advances"></a>Tiền tạm ứng và Tiền trả trước

Dạng xem **Các khoản đặt cọc và tạm ứng** liệt kê những khoản đặt cọc và tạm ứng trên tất cả các hợp đồng dự án. Sau khi một khoản trả trước hoặc tạm ứng được lập hóa đơn, số tiền tạm ứng/trả trước đó sẽ có sẵn để sử dụng.

## <a name="available-retainers-and-advances"></a>Tiền tạm ứng và Tiền trả trước khả dụng

Dạng xem **Các khoản đặt cọc và tạm ứng hiện có** liệt kê tất cả các khoản đặt cọc và tạm ứng hiện có trên tất cả các hợp đồng dự án. Sau khi một khoản trả trước hoặc tạm ứng được lập hóa đơn, số tiền tạm ứng/trả trước đó sẽ có sẵn để sử dụng và được thêm vào danh sách này. Sau khi sử dụng hết số tiền đặt cọc hoặc tạm ứng, số tiền đó sẽ bị xóa khỏi danh sách.

## <a name="fixed-price-milestones"></a>Mốc Giá Cố định

Dạng xem **Các mốc giá cố định** liệt kê tất cả các mốc giá cố định trên tất cả các mục mô tả hợp đồng của dự án. Từ dạng xem này, một hoặc nhiều mốc có thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn** hoặc là **Chưa sẵn sàng để lập hóa đơn**. Nếu đánh dấu một mốc là **Sẵn sàng để lập hóa đơn**, thì bạn có thể đưa mốc đó vào hóa đơn nháp.

Khi phần mô tả hợp đồng với nhiều khách hàng có phương thức thanh toán theo giá cố định, một mốc sẽ được tạo cho từng khách hàng có trong phần mô tả hợp đồng đó. Một mốc có thể được tạo, sau đó chia thành các hồ sơ của mốc dành riêng cho từng khách hàng. Việc phân chia này diễn ra nội bộ và phù hợp với tỷ lệ phần trăm thanh toán được xác định cho từng khách hàng trong phần mô tả hợp đồng. Ở dạng xem **Mốc giá cố định**, bạn sẽ thấy các hồ sơ của mốc dành riêng cho từng khách hàng. Mỗi bản ghi mốc này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này. Khi một hoặc nhiều mốc phân chia có liên quan được đánh dấu là **Đã sẵn sàng để lập hóa đơn**, trạng thái tiêu đề sẽ cập nhật thành **Đang diễn ra** từ **Chưa bắt đầu**. Khi tất cả các mốc phân chia được lập hóa đơn, trạng thái mốc tiêu đề sẽ cập nhật thành **Đã hoàn thành**.

Một mốc trên hóa đơn nháp được hiển thị ở dạng xem này với trạng thái thanh toán là **Đã tạo hóa đơn khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên hồ sơ được cập nhật thành **Đã đăng hóa đơn khách hàng**. 

> [!NOTE] 
> Không cập nhật giá trị trạng thái này bằng cách sử dụng mã tùy chỉnh. Project Operations không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.

## <a name="time-and-material-billing-backlog"></a>Tồn đọng Thanh toán Thời gian và Vật liệu

Dạng xem **Tồn đọng thanh toán cho thời gian và vật tư** liệt kê mọi giao dịch bán hàng thực tế chưa thanh toán cho tất cả các hợp đồng dự án trong hệ thống chưa được lập hóa đơn. Một hoặc nhiều giá trị thực tế doanh số chưa lập hóa đơn có thể được đánh dấu là **Đã sẵn sàng để lập hóa đơn** hoặc **Chưa sẵn sàng để lập hóa đơn** ở dạng xem này. Việc đánh dấu một giá trị thực tế doanh số chưa lập hóa đơn là **Đã sẵn sàng để lập hóa đơn** sẽ làm cho mục chuyển sang trạng thái có sẵn để đưa vào hóa đơn nháp.

Bạn không thể đánh dấu các giao dịch bán hàng thực tế chưa thanh toán có trạng thái **Không vượt quá** (**Không thành công**) là **Sẵn sàng để lập hóa đơn**. Nếu các giá trị thực tế cần được đánh dấu là **Đã sẵn sàng để lập hóa đơn**, hãy đặt lại trạng thái cho các giá trị thực tế khác trên mục mô tả hợp đồng đã cam kết, sau đó đánh giá lại trạng thái **Không vượt quá**.

Nếu phần mô tả hợp đồng với nhiều khách hàng có phương thức thanh toán theo thời gian và vật tư, thì khi thời gian và chi phí được phê duyệt, một giao dịch bán hàng thực tế chưa thanh toán sẽ được tạo cho từng khách hàng trên phần mô tả hợp đồng theo tỷ lệ phần trăm thanh toán được xác định cho từng khách hàng đó. Ở dạng xem **Tồn đọng thanh toán cho thời gian và vật tư**, bạn sẽ thấy các giao dịch bán hàng thực tế chưa thanh toán cho từng khách hàng cụ thể này. Mỗi bản ghi giá trị thực tế doanh số chưa lập hóa đơn này có thể được đánh dấu riêng biệt là **Đã sẵn sàng để lập hóa đơn** ở dạng xem này.

Giá trị thực tế về doanh số chưa lập hóa đơn trên hóa đơn dự thảo được hiển thị trong dạng xem này với trạng thái lập hóa đơn là **Đã tạo hóa đơn khách hàng**. Khi hóa đơn nháp được xác nhận, trạng thái thanh toán trên bản ghi này được cập nhật thành **Đã đăng hóa đơn khách hàng**. 

> [!NOTE] 
> Không cập nhật giá trị trạng thái này bằng cách sử dụng mã tùy chỉnh. Project Operations không hoạt động chính xác khi các giá trị trạng thái này được cập nhật bằng mã tùy chỉnh.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
