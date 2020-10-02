---
title: Thêm trường tùy chỉnh theo yêu cầu vào thực thể giao dịch và thiết lập giá
description: Chủ đề này cung cấp thông tin về cách thêm các thêm trường tùy chỉnh bắt buộc vào các thực thể cũng như biểu mẫu và dạng xem.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898332"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Thêm trường tùy chỉnh theo yêu cầu vào thực thể giao dịch và thiết lập giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này giả định rằng bạn đã hoàn tất các quy trình trong chủ đề, [Tạo trường và thực thể tùy chỉnh để được sử dụng là kích thước giá](create-custom-fields-entities-pricing-dimensions.md). Nếu bạn chưa hoàn thành các quy trình đó, hãy quay lại và hoàn thành chúng rồi trở lại chủ đề này. 

Trong chủ đề này, các quy trình sẽ hiển thị cho bạn cách thêm tham chiếu trường tùy chỉnh bắt buộc vào các thực thể và vào các thành phần giao diện người dùng (UI) như biểu mẫu và dạng xem.

## <a name="add-custom-pricing-dimension-fields"></a>Thêm các trường kích thước giá tùy chỉnh 
Sau khi các trường và thực thể tùy chỉnh được tạo, bước tiếp theo là thiết lập giá và thực thể giao dịch với sự cân nhắc đến bất kỳ thực thể tùy chỉnh hay bộ tùy chọn nào bằng cách tạo các trường tham chiếu. Tùy thuộc vào việc danh sách kích thước giá bao gồm các kích thước của bộ tùy chỉnh hay kích thước thực thể hay cả hai, chỉ làm theo các bước trong **Kích thước giá tùy chỉnh dựa trên bộ tùy chọn** hoặc **Kích thước giá tùy chỉnh dựa trên thực thể** hoặc cả hai.

### <a name="option-set-based-custom-pricing-dimensions"></a>Kích thước giá tùy chỉnh dựa trên bộ tùy chọn
Khi kích thước giá tùy chỉnh dựa trên bộ tùy chọn, hãy thêm nó như một trường vào các thực thể chính. Trong quy trình sau đây, **Vị trí làm việc của nhân lực** và **Số giờ làm việc của nhân lực** được dùng làm kích thước giá dựa trên bộ tùy chọn. Trước tiên phải thêm các thành phần này dưới dạng trường vào các thực thể giá, **Giá theo vai trò** và **Tăng giá theo vai trò**.

1. Trong Hoạt động dự án, hãy chọn **Cài đặt** > **Giải pháp**, và nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Giá theo vai trò**.
3. Mở rộng thực thể **Giá theo vai trò** và chọn **Trường**.
4. Chọn **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn **Bộ tùy chọn** là loại trường. 
5. Chọn **Sử dụng bộ tùy chọn hiện có**, chọn bộ tùy chọn **Vị trí làm việc của nguồn lực**, sau đó chọn **Lưu**.
6. Lặp lại các bước 1-5 để thêm trường này vào thực thể **Tăng giá theo vai trò**. 
7. Lặp lại bước 1-5 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**.

> [!IMPORTANT]
> Khi bạn thêm một trường vào nhiều thực thể, hãy sử dụng cùng một tên trường trên tất cả các tổ chức. 

Trong giai đoạn bán hàng và ước tính cho một dự án, ước tính của nỗ lực công việc cần thiết để hoàn tất công việc **Tại địa phương** và **Tại chỗ**, trong **Giờ làm việc** và **Giờ làm thêm** được dùng để ước tính giá trị của Báo giá/Dự án. Các trường **Vị trí làm việc của nguồn lực** và **Số giờ làm việc của nguồn lực** sẽ được thêm vào thực thể ước tính, **Chi tiết về dòng báo giá**, **Chi tiết về dòng hợp đồng**, **Thành viên nhóm dự án** và **Dòng ước tính**.

1. Trong Hoạt động dự án, hãy chọn **Chế độ Cài đặt** > **Giải pháp**, và nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chi tiết dòng báo giá**.
3. Mở rộng thực thể **Chi tiết dòng báo giá**, chọn **Trường**.
4. Chọn **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn loại trường là **Bộ tùy chọn**. 
5. Chọn **Sử dụng bộ tùy chọn hiện có** và **Vị trí làm việc của nhân lực**, sau đó chọn **Lưu**.
6. Lặp lại các bước 1-5 để thêm trường này vào các thực thể **chi tiết dòng hợp đồng dự án**, **Thành viên nhóm dự án** và **Dòng ước tính**.
7. Lặp lại bước 1-6 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**. 

Đối với giao hàng và lập hóa đơn, công việc đã hoàn thành phải có giá chính xác để chọn liệu công việc đó được thực hiện **Tại địa phương** hay **Tại chỗ** và liệu công việc được thực hiện trong **Giờ làm việc** hay **Ngoài giờ làm việc** trên Thực tế dự án. Các trường **Vị trí làm việc của nguồn lực** và **Số giờ làm việc của nguồn lực** phải được thêm vào **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký**.

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Mục nhập thời gian**.
3. Mở rộng thực thể **Chi tiết dòng báo giá**, sau đó chọn **Trường**.
4. Chọn **Mới** để tạo một trường mới tên là **Vị trí làm việc của nguồn lực** và chọn **Bộ tùy chọn** là loại trường. 
5. Chọn **Sử dụng bộ tùy chọn hiện có**, chọn bộ tùy chọn **Vị trí làm việc của nguồn lực**, sau đó chọn **Lưu**.
6. Lặp lại bước 1-5 để thêm trường này vào các thực thể **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.
7. Lặp lại bước 1-6 cho bộ tùy chọn **Số giờ làm việc của nguồn lực**. 

Thao tác này sẽ hoàn tất các thay đổi với giản đồ cần thiết cho các kích thước tùy chỉnh dựa trên bộ tùy chọn.

## <a name="entity-based-custom-pricing-dimensions"></a>Kích thước giá tùy chỉnh dựa trên thực thể

Khi kích thước giá tùy chỉnh là một thực thể, bạn sẽ thêm mối quan hệ 1:N giữa thực thể kích thước và thực thể chính. Sử dụng ví dụ Chức vụ tiêu chuẩn ở trên, có thể kỳ vọng rằng mỗi nhân viên sẽ được chỉ định một chức vụ tiêu chuẩn. Kết quả là bạn sẽ cần một mối quan hệ 1: N từ chức vụ tiêu chuẩn để có thể đặt lịch tài nguyên hoặc mối quan hệ N:1 nếu nó được tạo từ tài nguyên có thể đặt lịch thành chức vụ tiêu chuẩn.

1. Trong Hoạt động dự án, hãy chọn **Chế độ Cài đặt** > **Giải pháp**, và nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.
3. Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.
4. Chọn **Mới** để tạo mối quan hệ 1:N mới gọi là **Chức vụ tiêu chuẩn cho nguồn lực có thể đặt lịch**. Nhập các thông tin cần thiết, sau đó chọn **Lưu**.

Bạn cũng cần thêm Chức vụ tiêu chuẩn vào các thực thể Giá, **Giá theo vai trò** và **Tăng giá theo vai trò**. Bạn cũng có thể hoàn tất việc này bằng cách sử dụng mối quan hệ 1:N giữa các thực thể **Chức vụ tiêu chuẩn** và **Giá theo vai trò** và các thực thể **Chức vụ tiêu chuẩn** và **Tăng giá theo vai trò**.

1. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.
2. Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.
3. Chọn **Mới** để tạo mối quan hệ 1:N mới gọi là **Chức vụ tiêu chuẩn cho Giá theo vai trò**. Nhập các thông tin cần thiết, sau đó chọn **Lưu**.
4. Lặp lại các bước 1-4 để tạo mối quan hệ 1:N giữa các thực thể **Chức vụ tiêu chuẩn** và **Tăng giá theo vai trò**,

Trong các giai đoạn bán hàng và dự toán cho dự án, để định giá cho Dự án/Báo giá, cần có ước tính nỗ lực làm việc cho mỗi chức vụ tiêu chuẩn. Điều này có nghĩa là cần có mối quan hệ 1: N từ Chức vụ tiêu chuẩn cho mỗi thực thể ước tính này. 

- **Chi tiết dòng báo giá**
- **Chi tiết Mô tả Hợp đồng Dự án**
- **Thành viên Nhóm Dự án**
- **Mô tả Ước tính**

5. Lặp lại các bước 1-5 để tạo mối quan hệ 1:N từ **Chức vụ tiêu chuẩn** thành **Chi tiết dòng báo giá**, **Chi tiết dòng hợp đồng dự án**, **Thành viên nhóm hợp đồng** và **Dòng ước tính**.

  Trong giai đoạn gửi và lập hóa đơn, công việc được hoàn thành bởi mỗi chức vụ tiêu chuẩn phải được định giá chính xác trên Thực tế dự án. Điều này có nghĩa là cần có mối quan hệ 1:N từ các thực thể **Chức vụ tiêu chuẩn** cho **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.

6. Lặp lại các bước 1-6 để tạo mối quan hệ 1:N từ các thực thể **Chức vụ tiêu chuẩn** cho **Mục nhập thời gian**, **Thực tế**, **Chi tiết dòng hóa đơn** và **Dòng nhật ký kế toán**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Thiết lập giá trị kích thước mặc định bằng cách sử dụng các tính năng ánh xạ của nền tảng
Đối với Mục nhập thời gian, việc để hệ thống mặc định chức vụ tiêu chuẩn trên Mục nhập thời gian từ Nguồn lực có thể đặt lịch đang ghi mục nhập thời gian rất hữu ích. Sử dụng các bước sau để thêm ánh xạ trường trên mối quan hệ 1:N từ **Tài nguyên có thể đặt lịch** thành **Mục nhập thời gian**.

1. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể > Chức vụ tiêu chuẩn**.
2. Mở rộng thực thể **Chức vụ tiêu chuẩn** và chọn **Mối quan hệ 1:N**.
3. Nhấp đúp vào **Tài nguyên có thể đặt lịch cho mục nhập thời gian**. Trên trang **Mối quan hệ**, chọn **Sử dụng ánh xạ trường**. 
4. Nhấp vào **Mới** để tạo ánh xạ trường mới giữa trường **Chức vụ tiêu chuẩn** trên thực thể **Nguồn lực có thể đặt lịch** thành trường tham chiếu **Chức vụ tiêu chuẩn** trên thực thể **Mục nhập thời gian**. 

Thao tác này sẽ hoàn tất các thay đổi với giản đồ cần thiết cho các kích thước tùy chỉnh dựa trên thực thể.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Thêm trường tùy chỉnh vào biểu mẫu, dạng xem và quy tắc công việc

Sau khi bạn đã thực hiện tất cả các thay đổi cần thiết với giản đồ, bước tiếp theo là làm cho các trường hiển thị trong giao diện người dùng bằng cách thêm các trường vào biểu mẫu và dạng xem.

1. Mở biểu mẫu hoặc dạng xem. Trên ngăn điều hướng bên phải, chọn trường và kéo nó vào bảng tùy biến biểu mẫu. 
2. Nếu bạn đang chỉnh sửa dạng xem, hãy sử dụng ngăn điều hướng bên phải, chọn **Thêm trường** và trong hộp thoại **Danh sách trường**, chọn các trường mà bạn cần rồi chọn **OK**.

Bảng sau đây cung cấp một danh sách toàn diện các biểu mẫu và dạng xem sẵn dùng, theo thực thể sẽ cần phải được cập nhật với các trường mới. Nếu bạn có bất kỳ dạng xem bổ sung hoặc biểu mẫu nào trong tùy chỉnh của mình trên các thực thể này, hãy thêm các trường mới vào các mục đó.

| Thực thể        | Các biểu mẫu cần trường mới   |Các dạng xem cần trường mới      |
| ------------------------------|---------------------------------|----------------------------------|
|  Giá Vai trò|• Thông tin |• Giá danh mục nguồn lực hoạt động<br> • Chế độ xem liên kết của Giá danh mục nguồn lực|
|  Tăng giá theo Vai trò|• Thông tin|• Tăng giá theo vai trò hiện hoạt<br>• Chế độ xem liên kết tăng giá theo vai trò|
|  Chi tiết mô tả báo giá|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết mô tả báo giá hiện hoạt<br>• Chi tiết mô tả báo giá kết hợp<br>• Dạng xem liên kết chi tiết mô tả báo giá|
|  Chi tiết mô tả hợp đồng dự án|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết Mô tả Hợp đồng Kết hợp<br>• Chi tiết mô tả hợp đồng hiện hoạt<br>• Dạng xem Liên kết Chi tiết Mô tả Hợp đồng|
|  Thành viên Nhóm Dự án|• Thông tin<br>• Biểu mẫu mới|• Thành viên nhóm dự án hiện hoạt<br>• Thành viên nhóm dự án<br>• Chế độ xem liên kết cho thành viên nhóm dự án|
|  Mục nhập Thời gian|• Thông tin<br>• Tạo mục nhập thời gian|• Mục nhập thời gian theo ngày của tôi<br>• Mục nhập thời gian của tôi trong tuần này<br>• Mục nhập thời gian để phê duyệt|
|  Dòng Nhật ký Kế toán|• Thông tin<br>• Tạo nhanh|• Dòng nhật ký kế toán hiện hoạt<br>• Chế độ xem liên kết dòng nhật ký kế toán|
|  Chi tiết Mô tả Hóa đơn|• Thông tin<br>• Tạo nhanh|• Chi tiết mô tả hóa đơn hiện hoạt<br>• Giao dịch hóa đơn có thể tính phí<br>• Giao dịch hóa đơn miễn phí<br>• Dạng xem liên kết chi tiết mô tả hóa đơn<br>• Giao dịch hóa đơn không thể tính phí|
|  Thực tế|• Thông tin<br>• Thực tế hiện hoạt|• Dạng xem liên kết thực tế|

Trường tùy chỉnh cũng có thể cần được thêm vào các quy tắc kinh doanh tùy thuộc vào những gì bạn đã xác định. Một ví dụ sẵn dùng là đối với quy tắc công việc **Khả năng chỉnh sửa mục nhập thời gian dựa trên trạng thái**. Quy tắc này xác định các trường cần bị khóa khi mục nhập thời gian ở trạng thái không thể chỉnh sửa như **Đã phê duyệt**. Thêm các trường vào quy tắc công việc này để không thể chỉnh sửa các trường khi mục nhập thời gian ở trạng thái không phải **Bản nháp** hoặc **Đã trả lại**.
