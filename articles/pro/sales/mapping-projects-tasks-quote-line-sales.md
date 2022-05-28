---
title: Ánh xạ dự án và tác vụ với mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách ánh xạ các dự án và tác vụ thành một mô tả tác vụ dựa trên dự án.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff2fa219fd1981e5e11f93dfe7cd65afefc6afb9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597318"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Ánh xạ dự án và tác vụ với mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trên các mô tả báo giá dựa trên dự án, bạn có thể ánh xạ các nhiệm vụ cụ thể của một dự án đã được liên kết với mô tả báo giá.

Khi bạn ánh xạ các tác vụ với một mô tả báo giá, các mục sau đây bạn đã xác định trên mô tả báo giá sẽ chỉ áp dụng cho các tác vụ đó:

- Phương thức thanh toán
- Tùy chọn về khả năng tính phí
- Giới hạn không vượt quá
- Khách hàng

Ví dụ: bạn có thể có một dự án trong đó một giai đoạn là giá cố định và tất cả các giai đoạn khác là thời gian và vật tư. Trong trường hợp này, bạn có thể liên kết giai đoạn đầu tiên và tất cả các tác vụ con của nó với mô tả báo giá cho giai đoạn đó bằng phương thức thanh toán giá cố định. Sau đó, bạn có thể liên kết tất cả các giai đoạn khác với mô tả báo giá dựa trên thời gian và vật tư.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Liên kết tác vụ với mô tả báo giá dựa trên dự án

Bạn có thể liên kết các tác vụ với các mô tả báo giá từ các vị trí sau đây:

- Trang **Dự án** > tab **Thanh toán theo tác vụ** (tối ưu)
- Trang **Mô tả báo giá** > tab **Tác vụ có thể tính phí** 

### <a name="from-the-project-page"></a>Từ trang Dự án

Trang **Dự án** cung cấp trải nghiệm tối ưu cho việc liên kết các tác vụ với mô tả báo giá. Bạn có thể sử dụng trang này để chọn nhiều tác vụ và liên kết tất cả các tác vụ đó, cộng với các tác vụ con của chúng, với mô tả báo giá đã chọn.

1. Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, hãy xác minh là trường **Dự án** đã được điền vào.
2. Trong trường **Các tác vụ được đưa vào**, chọn **Chỉ các tác vụ được chọn**.
3. Lưu mô tả báo giá dựa trên dự án. Khi biểu mẫu làm mới, tab **Tác vụ có thể tính phí** sẽ hiển thị.
4. Trên tab **Tổng quát**, chọn liên kết cho dự án từ trường **Dự án**.
5. Trên trang **Dự án**, chọn tab **Thanh toán theo tác vụ**.
6. Trong lưới thứ hai, áp dụng cho thiết lập thanh toán theo tác vụ cụ thể, hãy chọn một hoặc nhiều tác vụ rồi chọn **Liên kết các mô tả báo giá**.
7. Trong trang hộp thoại xuất hiện, hãy chọn một mô tả báo giá hiển thị các mô tả báo giá dựa trên dự án trên báo giá.
8. Trong trường **Loại thanh toán**, cho biết những tác vụ này có thể tính phí hay không.
9. Chọn hộp kiểm để cho biết liệu liên kết có nên bao gồm tác vụ con của các tác vụ đã chọn hay không. Chọn hộp sẽ liên kết các tác vụ con của các tác vụ đã chọn với mô tả báo giá.
10. Chọn **OK** để đóng hộp thoại.

### <a name="from-the-quote-line-page"></a>Từ trang Mô tả báo giá

Bạn có thể liên kết các tác vụ dự án với mô tả báo giá từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**.

>[!NOTE]
>Nơi tối ưu để liên kết tác vụ dự án vào mô tả báo giá là trên tab **Thanh toán theo tác vụ** trên trang **Dự án**. Nếu bạn liên kết các tác vụ từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**, bạn phải liên kết từng dự án theo cách thủ công.

1. Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, hãy xác minh là có dự án được chọn trong trường **Dự án**.
2. Trong trường **Các tác vụ được đưa vào**, chọn **Chỉ các tác vụ được chọn**.
3. Lưu mô tả báo giá dựa trên dự án. Khi biểu mẫu làm mới, tab **Tác vụ có thể tính phí** sẽ hiển thị.
4. Trên tab **Tác vụ có thể tính phí**, chọn **Thêm tác vụ mô tả báo giá**.
5. Trên trang **Tác vụ mô tả báo giá**, trong trường **Tác vụ**, chọn tác vụ và trong trường **Loại thanh toán**, chọn **Lưu**. 
6. Đóng trang. Tác vụ vụ đã chọn bây giờ được liên kết với mô tả báo giá.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Dừng liên kết tác vụ với mô tả báo giá dựa trên dự án

### <a name="from-the-project-page"></a>Từ trang Dự án

Phương thức này cung cấp trải nghiệm tối ưu nhất cho việc dừng liên kết tác vụ với mô tả báo giá. Bạn có thể chọn nhiều tác vụ và dừng liên kết tất cả các tác vụ đó và tác vụ con của chúng với mô tả báo giá đã chọn.

1. Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, trong trường **Dự án**, chọn liên kết dự án.
2. Trên trang **Dự án**, chọn tab **Thanh toán theo tác vụ**.
3. Trong lưới thứ hai, áp dụng cho thiết lập thanh toán theo tác vụ cụ thể, hãy chọn một hoặc nhiều tác vụ rồi chọn **Dừng liên kết các mô tả báo giá**.
4. Trong trang hộp thoại xuất hiện, hãy chọn một mô tả báo giá.
5. Chọn hộp kiểm để cho biết liệu có nên loại bỏ cả liên kết khỏi các tác vụ con của tác vụ đã chọn không. Việc chọn hộp cũng sẽ dừng liên kết tác vụ con của các tác vụ đã chọn với mô tả báo giá.
6. Chọn **OK**. Một cảnh báo cho bạn biết rằng nếu bạn loại bỏ liên kết này, bất kỳ giá trị thực tế nào được ghi trước đó về tác vụ có thể bị đảo ngược. 
7. Chọn **OK** để tiếp tục và loại bỏ liên kết giữa tác vụ và mô tả báo giá dựa trên dự án.

### <a name="from-the-quote-line-page"></a>Từ trang Mô tả báo giá

Bạn cũng có thể dừng liên kết tác vụ dự án với mô tả báo giá từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**.

1. Trên tab **Tác vụ có thể tính phí**, chọn **Xóa tác vụ mô tả báo giá**.
2. Chọn **OK**. Một cảnh báo cho bạn biết rằng nếu bạn loại bỏ liên kết này, bất kỳ giá trị thực tế nào được ghi trước đó về tác vụ có thể bị đảo ngược. 
3. Chọn **OK** để tiếp tục và loại bỏ liên kết giữa tác vụ và mô tả báo giá dựa trên dự án.

>[!NOTE]
> Quy trình này không xóa tác vụ khỏi dự án. Nó chỉ xóa liên kết tác vụ khỏi mô tả báo giá dựa trên dự án.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]