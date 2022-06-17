---
title: Quản lý ước tính doanh thu
description: Bài viết này cung cấp thông tin về cách làm việc với ước tính doanh thu cho các dự án.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 051535ce8dd4997a923b1511d242638361076979
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928504"
---
# <a name="manage-revenue-estimates"></a>Quản lý ước tính doanh thu

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bạn có thể tạo, tính toán, đăng, đảo ngược hoặc loại bỏ các phép ước tính doanh thu. Bạn có thể thực hiện theo cách thủ công hoặc dùng quy trình định kỳ. Bài viết này cung cấp thông tin về cách làm việc với ước tính doanh thu cho các dự án.

### <a name="manage-revenue-estimates-manually"></a>Quản lý các phép ước tính doanh thu theo cách thủ công

Trên dự án ước tính doanh thu theo giá cố định hoặc trang **Truy vấn giá trị ước tính** (**Quản lý dự án và kế toán** > **Báo cáo và truy vấn** > **Truy vấn và báo cáo giá trị ước tính**), chọn **Ước tính**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Quản lý các phép ước tính doanh thu bằng quy trình định kỳ

Đi tới **Quản lý dự án và kế toán** > **Định kỳ** > **Ước tính** rồi chọn quy trình tương ứng.

## <a name="create-a-revenue-estimate"></a>Tạo phép ước tính doanh thu

Hoàn thành cách bước sau để tạo một phép ước tính doanh thu. 

1. Đi tới **Quản lý dự án và kế toán** > **Định kỳ** > **Ước tính**.
2. Chọn **Mới**. Trên trang **Tạo phép ước tính**, hãy chọn các tham số sau:

   - **Mã chu kỳ**: Mã này quyết định tần suất đăng các giá trị ước tính.
   - **Ngày ước tính**: Ngày xử lý phép ước tính.
   - **Liên tục**: Đánh dấu vào ô này để tạo các phép ước tính chỉ khi nếu các phép ước tính được đăng ở kỳ trước, hoặc nếu đây là lần đầu tiên phép ước tính được tạo. Nếu không chọn ô này, các phép ước tính sẽ được tạo kể cả khi các phép ước tính không được đăng ở chu kỳ trước đó.
   - **Phương pháp chi phí hoàn thành**: Xác định cách ước tính phần công việc còn lại của dự án. Để biết thêm thông tin, hãy xem [Phương pháp chi phí hoàn thành](cost-complete-methods.md).
   - **Phương pháp hoàn thành**: Chọn một phương pháp hoàn thành trong số các tùy chọn sau:
     - **Tự động**: Tỷ lệ phần trăm hoàn thành được tính toán tự động dựa trên các dòng chi phí được đưa vào phép tính. Mẫu chi phí giúp xác định các dòng chi phí được đưa vào.
     - **Thủ công**: Tỷ lệ phần trăm hoàn thành tương đương với phép ước tính gần nhất. Sau khi tạo phép ước tính, bạn có thể thay đổi **Phép tính thủ công** trên trang **Ước tính**.
     - **Từ mẫu chi phí**: Sự kết hợp giữa phương pháp tự động và thủ công. Tùy chọn này được đặt thành tự động hoặc thủ công tùy theo giá trị mặc định trong mẫu chi phí.
   - **Mô hình dự báo**: Chọn một mô hình dự báo cho ước tính.
   - **In danh sách phép ước tính**: Tạo và hiển thị danh sách phép ước tính. Danh sách này chứa trạng thái của chức năng hiện tại. Bạn có thể in cảnh báo bất kỳ về phép ước tính trên báo cáo. Những điều kiện sau khiến xuất hiện cảnh báo trên danh sách phép ước tính:
     - Tỷ lệ phần trăm hoàn thành lớn hơn 100 phần trăm.
     - Tỷ lệ phần trăm hoàn thành nhỏ hơn 0 phần trăm.
     - Cột **Cần hoàn thành** có giá trị âm.
     - Phép ước tính không có số tiền tương ứng trong hợp đồng.
     - Phép ước tính không có bản ước tính chi phí đính kèm.
   - **Hiện nhật ký thông tin** : Chọn tùy chọn này để nhận thông báo chứa thông tin về các dự án ước tính đã được xử lý khi tác vụ được chạy.


## <a name="post-wip-or-accruals"></a>Đăng WIP hoặc khoản tích lũy

Sau khi ước tính xong, các giá trị ước tính sẽ giữ nguyên, giảm hoặc tăng. Bạn có thể đăng WIP khi làm việc với nguyên tắc đánh giá **Hợp đồng đã hoàn tất**, hoặc đăng giá trị tích lũy khi bạn làm việc với nguyên tắc đánh giá **Tỷ lệ phần trăm hoàn tất**.
  
Trạng thái chu kỳ ước tính thay đổi từ **Đã tạo** sang **Đã đăng**.

## <a name="reverse-wip-or-accruals"></a>Đảo ngược WIP hoặc khoản tích lũy

Dùng tùy chọn đảo ngược để ghi có đối với WIP hoặc khoản tích lũy đã đăng, sau đó tạo các phép ước tính cho chu kỳ.

> [!NOTE]
> Để đảo ngược một chu kỳ giữa các chu kỳ khác, hãy đảo ngược các chu kỳ ước tính cần thiết, sau đó đăng lại. Vì tất cả chu kỳ tiếp theo phụ thuộc vào các phép ước tính của chu kỳ trước đó, vậy nên đừng bỏ qua bất cứ chu kỳ nào.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Loại bỏ dự án ước tính và kết thúc dự án

Bước cuối cùng trong quy trình ước tính là loại bỏ dự án ước tính và chấm dứt dự án theo giá cố định khi tỷ lệ phần trăm hoàn thành đạt 100 phần trăm.

Khi bạn chạy quy trình loại bỏ, những điều sau đây sẽ xảy ra:

- Đối với dự án theo giá cố định có hợp đồng đã hoàn thành, các giá trị WIP sẽ bị xóa khỏi tài khoản số dư và đăng vào tài khoản lợi nhuận và thua lỗ.
- Đối với mô hình giá cố định có tỷ lệ phần trăm đã hoàn thành, giá trị tích lũy sẽ bị xóa khỏi tài khoản lợi nhuận và thua lỗ.

Phép ước tính sẽ chuyển trạng thái thành **Đã loại bỏ**.

> [!NOTE]
> Trong một số trường hợp đặc biệt, tỷ lệ phần trăm có thể vượt quá 100 phần trăm. Khi đó, hãy giảm tỷ lệ phần trăm hoàn thành bằng cách dùng **Phương pháp đặt chi phí từ hoàn tất thành 0** đến khi đạt 100 phần trăm.

## <a name="reverse-elimination"></a>Đảo ngược quá trình loại bỏ

1. Đi tới **Quản lý dự án và kế toán** > **Định kỳ** > **Ước tính** > **Đảo ngược quy trình loại bỏ**. 
2. Trên Ngăn hành động, ở tab **Quy trình** trong nhóm **Giữ nguyên**, hãy chọn **Ước tính**. 
3. Chọn **Đảo ngược quá trình loại bỏ**.

Dùng trang này để đảo ngược tất cả các lần loại bỏ với ngày ước tính cụ thể và với trạng thái ước tính là **Đã loại bỏ**. Trạng thái giao dịch sẽ thay đổi sau khi bạn chọn đúng các trường.

Trạng thái dự án cũng sẽ tự động chuyển sang **Đang trong quy trình** nếu giai đoạn dự án được đặt là đã kết thúc. Trạng thái loại bỏ của chu kỳ dự án sẽ thay đổi lại thành **Đã đăng**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]