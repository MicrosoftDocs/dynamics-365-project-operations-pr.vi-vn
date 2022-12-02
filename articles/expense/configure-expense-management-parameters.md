---
title: Đặt cấu hình các tham số quản lý chi phí
description: Bài viết này mô tả các tham số kiểm soát hành vi chung trong Quản lý chi phí.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 6432e119f38071b028c013561bab99820778a11d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931494"
---
# <a name="configure-expense-management-parameters"></a>Đặt cấu hình các tham số quản lý chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này mô tả các tham số kiểm soát hành vi chung trong Quản lý chi phí.

## <a name="general"></a>Chung

| Trường                                                    | Nội dung mô tả |
|----------------------------------------------------------|-------------|
| Mức vận phí chuẩn                                 | Nhập mức bồi hoàn cho chi phí đi lại. Tỷ lệ này được nhân với số dặm được nhập cho chi phí để tính số tiền được hoàn trả cho chi phí đi lại. |
| Xác thực mục đích của chi phí                                 | Bật tùy chọn này để giới hạn người dùng đối với một tập hợp giá trị hiện có được định cấu hình trong trường **Mục đích của báo cáo chi phí** khi họ tạo báo cáo chi phí. |
| Chi phí cá nhân được thanh toán bởi                                | Chọn người chịu trách nhiệm thanh toán bất kỳ số tiền giao dịch thẻ tín dụng nào được phân loại là cá nhân. |
| Hiển thị toàn bộ báo cáo chi phí trên chi tiết               | Chọn tùy chọn này để hiển thị tất cả chi phí cho một báo cáo chi phí khi các chi tiết của chứng từ gốc được xem cho một chứng từ cụ thể được tạo khi đăng báo cáo chi phí. |
| Cần phải thẩm định trước chuyến đi                 | Chọn tùy chọn này để yêu cầu nộp và phê duyệt yêu cầu đi lại trước khi nhân viên có thể gửi báo cáo chi phí. |
| Cho phép chỉnh sửa các bản phân phối trước khi đăng            | Chọn xem có thể chỉnh sửa các bản phân phối của báo cáo chi phí trước khi đăng hay không. |
| Đánh giá các chính sách quản lý chi phí                     | Chọn thời điểm đánh giá chi phí để xác định xem có vi phạm chính sách chi phí hay không. Các khoản chi phí có thể được đánh giá về vi phạm khi nhập và lưu mục chi phí hoặc khi nộp chi phí để phê duyệt. Các quy tắc chính sách cho các khoản thu bắt buộc sẽ được đánh giá khi dòng chi phí được lưu. |
| Cho phép các dòng chi phí liên công ty                         | Chọn xem có thể nhập chi phí cho các pháp nhân khác trên báo cáo chi phí hay không. |
| Cho phép chỉnh sửa tỷ giá hối đoái cho các chi phí trên thẻ tín dụng | Chọn tùy chọn này để cho phép người dùng chỉnh sửa tỷ giá hối đoái cho các chi phí trên thẻ tín dụng đã nhập. |
| Các trường hệ thống cấp bậc nhiều cấp để hiển thị                  | Chọn trường người phê duyệt nào được hiển thị khi loại phân công quy trình làm việc được đặt thành hệ thống cấp bậc và lựa chọn **Hệ thống cấp bậc** được thiết lập để sử dụng hệ thống cấp bậc phê duyệt, phê duyệt nhiều cấp chi phí. Khi hệ thống cấp bậc phê duyệt nhiều cấp được sử dụng cho quy trình làm việc, các trường đã chọn sẽ được hiển thị trên báo cáo chi phí và có thể được chỉnh sửa. |
| Nhập số thẻ tín dụng của nhân viên                        | Chọn xem có thể nhập và lưu số gồm 15 ký tự hay 16 ký tự trong trường **ID thẻ** trên trang **Thẻ tín dụng** cho một nhân viên. |
| Xác thực mục đích của yêu cầu đi lại                      | Bật tùy chọn này để giới hạn người dùng đối với một tập hợp giá trị hiện có được định cấu hình trong trường **Mục đích của báo cáo chi phí** khi họ tạo yêu cầu đi lại. |

## <a name="financial"></a>Tài chính

| Trường                                                                                    | Nội dung mô tả |
|------------------------------------------------------------------------------------------|-------------|
| Tên bút toán hàng ngày của sổ cái                                                                | Chọn tên bút toán sổ cái mà các báo cáo chi phí đã phê duyệt được đăng lên. |
| Cho phép thu hồi thuế từ chi phí                                                        | Chọn tùy chọn này để cho phép thu hồi thuế chi phí cho các khoản chi phí đủ điều kiện. Không thể chọn tùy chọn này nếu các quy tắc thuế bán hàng và thuế sử dụng của Hoa Kỳ được bật. |
| Đăng tạm ứng tiền mặt ngay lập tức                                                           | Chọn tùy chọn này để đăng một khoản tạm ứng tiền mặt đã phê duyệt khi quá trình thanh toán và chuyển khoản hoàn tất. Nếu tùy chọn này không được chọn, quá trình thanh toán và chuyển khoản sẽ tạo ra một bút toán chung chưa được đăng. |
| Ngày kế toán chính xác trong quá trình đăng                                                   | Chọn tùy chọn này để cập nhật ngày kế toán khi chi phí được đăng, nếu kỳ hiện tại đang bị giữ hoặc đóng. Ngày kế toán sẽ được đặt sang kỳ mở tiếp theo. |
| Cho phép nhóm các giao dịch dựa trên tài khoản bù trừ được chỉ định trong phương thức thanh toán       | Chọn tùy chọn này để tóm tắt các giao dịch chi phí cho một báo cáo chi phí, dựa trên tài khoản bù trừ được chỉ định trong phương thức thanh toán chi phí. |
| Bao gồm thuế                                                                             | Chọn tùy chọn này để bao gồm thuế bán hàng vào số tiền chi phí theo mặc định. |
| Giải quyết những vướng mắc khi đóng các yêu cầu đi lại                                      | Chọn tùy chọn này để giải phóng các khoản tiền bị cản trở khi đóng yêu cầu đi lại đã phê duyệt. |
| Cho phép gửi yêu cầu đi lại khi ngân sách bị thấu chi cho sổ đăng ký ngân sách và ngân sách dự án | Chọn tùy chọn này để cho phép nhân viên gửi yêu cầu đi lại để được phê duyệt, ngay cả khi chúng vượt quá ngân sách cho phép được đặt trong sổ đăng ký ngân sách hoặc ngân sách được phép cho một dự án. |
| Cho phép gửi báo cáo chi phí khi ngân sách bị thấu chi cho sổ đăng ký ngân sách và ngân sách dự án     | Chọn tùy chọn này để cho phép nhân viên gửi báo cáo chi phí để được phê duyệt, ngay cả khi chúng vượt quá ngân sách cho phép được đặt trong sổ đăng ký ngân sách hoặc ngân sách được phép cho một dự án. |
| Chỉ cho phép phê duyệt báo cáo chi phí khi ngân sách bị thấu chi cho sổ đăng ký ngân sách                 | Chọn tùy chọn này để cho phép người phê duyệt phê duyệt các báo cáo chi phí vượt quá ngân sách đã cho phép được đặt trong sổ đăng ký ngân sách. |

## <a name="per-diem"></a>Công nhật

| Trường                                 | Nội dung mô tả |
|---------------------------------------|-------------|
| Số giờ tối thiểu cho công tác phí            | Nhập số giờ tối thiểu mặc định mà một nhân viên phải làm việc trong một ngày để đủ điều kiện nhận công tác phí cho các chi phí liên quan đến đi lại. Giá trị này chỉ được sử dụng làm giá trị mặc định cho trường **Số giờ tối thiểu** cho các bậc tỷ lệ công tác phí. |
| Phần trăm bữa ăn                          | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các bữa ăn được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại khi trường **Tính toán giảm bữa ăn theo** được đặt thành **Loại bữa ăn mỗi ngày** hoặc **Số bữa ăn mỗi ngày**. Ngày làm việc vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí vào những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành **0** (không), khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0. |
| Phần trăm khách sạn                         | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các khách sạn được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại. Ngày làm việc vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí vào những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành **0** (không), khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0. |
| Phần trăm khác                         | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các chi phí khác được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại. Ngày làm việc vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí vào những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành **0** (không), khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0. |
| Giảm tỷ lệ phần trăm cho bữa sáng | Nhập số tiền mà công tác phí được giảm cho bữa sáng. Ví dụ: nếu một nhân viên nhận được bữa sáng miễn phí, bạn có thể muốn giảm 10 phần trăm số tiền công tác phí. |
| Giảm tỷ lệ phần trăm cho bữa trưa     | Nhập số tiền mà công tác phí được giảm cho bữa trưa. Ví dụ: nếu một nhân viên nhận được bữa trưa miễn phí, bạn có thể muốn giảm 15 phần trăm số tiền công tác phí. |
| Giảm tỷ lệ phần trăm cho bữa tối    | Nhập số tiền mà công tác phí được giảm cho bữa tối. Ví dụ: nếu một nhân viên nhận được bữa tối miễn phí, bạn có thể muốn giảm 25 phần trăm số tiền công tác phí. |
| Tính toán giảm bữa ăn theo           | Chỉ định cách hệ thống sẽ tính toán mức giảm công tác phí bữa ăn, bằng cách chọn xem mức giảm dựa trên loại bữa ăn mỗi chuyến đi hoặc mỗi ngày hay dựa trên số lượng bữa ăn được phép mỗi ngày. |
| Làm tròn công tác phí                     | Chọn loại làm tròn được sử dụng cho chi phí công tác phí. Nếu bạn chọn làm tròn thông thường, mọi chi phí công tác phí có số tiền là 0,50 được làm tròn thành 1,00 và mọi chi phí công tác phí có số tiền nhỏ hơn 0,50 được làm tròn xuống thành 0,00. |
| Tính toán công tác phí cơ sở vào          | Chọn xem số tiền công tác phí dựa trên ngày dương lịch hay khoảng thời gian 24 giờ. |

## <a name="fax-cover-pages"></a>Trang bìa fax

| Trường                          | Nội dung mô tả |
|--------------------------------|-------------|
| Hướng dẫn                   | Nhập các hướng dẫn mà nhân viên phải tuân theo khi họ tạo trang bìa cho bản fax được sử dụng để gửi biên lai liên quan đến báo cáo chi phí. Để nhập văn bản theo ngôn ngữ cụ thể sẽ được hiển thị, dựa trên ngôn ngữ người dùng, hãy chọn **Bản dịch**. |
| ID người dùng (Thông tin mã vạch) | Chọn tùy chọn này để lưu trữ số nhận dạng duy nhất của nhân viên trong mã vạch được sử dụng trên trang bìa của bản fax. |
| Mã vạch                       | Chọn mã vạch được sử dụng trên trang bìa của bản fax. Mã vạch 39 và 128 được hỗ trợ trong quản lý Chi phí. |

## <a name="anti-corruption"></a>Chống tham nhũng

| Trường                                 | Nội dung mô tả |
|---------------------------------------|-------------|
| Hiển thị chứng thực chống tham nhũng   | Chọn tùy chọn này để hiển thị văn bản chống tham nhũng khi tạo báo cáo chi phí. Khi đó, các danh mục chi phí cụ thể có thể được kích hoạt và yêu cầu phải chọn chứng thực chống tham nhũng trên báo cáo chi phí. Ví dụ: danh mục quà tặng liên quan đến chi phí chính thức của chính phủ có thể yêu cầu nhân viên xác nhận rằng chi phí đó đáp ứng chính sách của công ty liên quan đến các quan chức chính phủ. |
| Thông điệp chống tham nhũng dành cho người gửi | Nhập văn bản sẽ được hiển thị cho nhân viên đang tạo báo cáo chi phí. Để nhập văn bản theo ngôn ngữ cụ thể sẽ được hiển thị, dựa trên ngôn ngữ người dùng, hãy chọn **Bản dịch**. |
| Thông điệp chống tham nhũng dành cho người phê duyệt  | Nhập văn bản sẽ được hiển thị cho người phê duyệt khi tạo báo cáo chi phí. Để nhập văn bản theo ngôn ngữ cụ thể sẽ được hiển thị, dựa trên ngôn ngữ người dùng, hãy chọn **Bản dịch**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]