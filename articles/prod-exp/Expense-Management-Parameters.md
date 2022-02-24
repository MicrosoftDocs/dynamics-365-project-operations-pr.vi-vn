---
title: Tham số quản lý chi phí
description: Các tham số sau kiểm soát hành vi trong phần Quản lý chi phí.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 41d78726f6d0aa6b5e647dbb359824950cb6ca72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993757"
---
# <a name="expense-management-parameters"></a>Tham số quản lý chi phí


Các tham số này kiểm soát hành vi chung trong phần Quản lý chi phí.

### <a name="general"></a>Chung

| **Trường**                                                | **Nội dung mô tả**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Mức vận phí chuẩn**                             | Nhập mức bồi hoàn cho chi phí đi lại. Mức này được nhân với số dặm được nhập trên mục chi phí để tính số tiền hoàn trả cho chi phí đi lại.                       |
|**Chi phí cá nhân được thanh toán bởi**                             | Chọn người chịu trách nhiệm thanh toán mọi số tiền giao dịch thẻ tín dụng được phân loại là cá nhân.                                                                                                     |
|**Hiển thị toàn bộ báo cáo chi phí trên chi tiết**               | Chọn tùy chọn này để hiển thị tất cả các chi phí cho một báo cáo chi phí khi xem thông tin chi tiết của chứng từ gốc được xem cho một phiếu cụ thể được tạo khi đăng báo cáo chi phí.              |
|**Cần phải thẩm định trước chuyến đi**                 | Chọn tùy chọn này để yêu cầu nộp và phê duyệt yêu cầu đi lại trước khi nhân viên có thể gửi báo cáo chi phí.                                                                    |
|**Cho phép chỉnh sửa các bản phân phối trước khi đăng**            | Chọn xem có thể sửa các bản phân phối của báo cáo chi phí trước khi đăng hay không.                                                                                                                 |
|**Đánh giá các chính sách quản lý chi phí**                     | Chọn thời điểm đánh giá chi phí để xác định xem có vi phạm chính sách chi phí hay không. Việc đánh giá vi phạm đối với chi phí có thể được thực hiện khi bạn nhập và lưu mục chi phí hoặc khi bạn nộp chi phí để phê duyệt. Các quy tắc chính sách đối với biên lai phải có sẽ được kiểm tra khi dòng chi phí được lưu.                   |
|**Cho phép các dòng chi phí liên công ty**                         | Chọn xem có cho phép nhập chi phí cho các thực thể pháp lý khác trong báo cáo chi phí hay không.                                                                                                          |
|**Cho phép chỉnh sửa tỷ giá hối đoái cho các chi phí trên thẻ tín dụng** | Chọn tùy chọn này để cho phép người dùng chỉnh sửa tỷ giá hối đoái cho các chi phí trên thẻ tín dụng đã nhập.                                                                        |
|**Các trường hệ thống cấp bậc nhiều cấp để hiển thị**                  | Chọn trường người phê duyệt nào sẽ được hiển thị khi loại phân công quy trình làm việc được đặt thành hệ thống cấp bậc và mục lựa chọn hệ thống cấp bậc được thiết lập để sử dụng hệ thống cấp bậc phê duyệt nhiều cấp Chi phí. Khi hệ thống cấp bậc phê duyệt nhiều cấp được sử dụng cho quy trình làm việc, các trường đã chọn sẽ được hiển thị và có thể chỉnh sửa được trên báo cáo chi phí. |
|**Nhập số thẻ tín dụng của nhân viên (Bản cập nhật tháng 7 năm 2017)**     | Chọn xem có thể nhập và lưu số gồm 15 ký tự hay 16 ký tự trong trường **ID thẻ** trên trang **Thẻ tín dụng** cho một nhân viên.                                                                          |

### <a name="financial"></a>Tài chính

| **Trường**                                                            | **Mô tả**     |
|----------------------------------------------------------------------|------------------------------------|
|**Tên bút toán hàng ngày của sổ cái**                                         | Chọn tên bút toán sổ cái mà các báo cáo chi phí đã phê duyệt được đăng lên.            |
|**Cho phép thu hồi thuế từ chi phí**                                  | Chọn tùy chọn này để cho phép thu hồi thuế chi phí cho các khoản chi phí đủ điều kiện. Tùy chọn này không thể kích hoạt được nếu các quy tắc thuế bán hàng và thuế sử dụng của Hoa Kỳ được bật.      |
|**Đăng tạm ứng tiền mặt ngay lập tức**                                     | Chọn tùy chọn này để đăng một khoản tạm ứng tiền mặt đã phê duyệt khi hoàn tất quá trình Thanh toán và chuyển khoản. Nếu tùy chọn này không được chọn, thì quá trình Thanh toán và chuyển khoản sẽ tạo ra một bút toán chung chưa đăng. |
|**Ngày kế toán chính xác trong quá trình đăng**                             | Chọn tùy chọn này để cập nhật ngày hạch toán khi đăng chi phí nếu kỳ hiện tại đang bị treo hoặc đã đóng. Ngày kế toán sẽ được đặt sang kỳ mở tiếp theo.   |
|**Cho phép nhóm các giao dịch dựa trên tài khoản bù trừ được chỉ định trong phương thức thanh toán**      | Chọn tùy chọn này để tóm tắt các giao dịch chi phí cho một báo cáo chi phí, dựa trên tài khoản bù trừ được chỉ định trong phương thức thanh toán cho các chi phí đó.   
|**Bao gồm thuế**                                                   | Chọn tùy chọn này để bao gồm thuế bán hàng vào số tiền chi phí theo mặc định.             |
|**Giải quyết những vướng mắc khi đóng các yêu cầu đi lại**            | Chọn tùy chọn này để giải phóng các khoản tiền bị cản trở khi đóng yêu cầu đi lại đã phê duyệt.                                                                                   |
|**Cho phép gửi yêu cầu đi lại khi ngân sách bị thấu chi cho sổ đăng ký ngân sách và ngân sách dự án** | Chọn tùy chọn này để cho phép nhân viên gửi những yêu cầu đi lại vượt quá ngân sách cho phép được đặt trong sổ đăng ký ngân sách hoặc ngân sách được phép cho một dự án để được phê duyệt.            |
|**Cho phép gửi báo cáo chi phí khi ngân sách bị thấu chi cho sổ đăng ký ngân sách và ngân sách dự án**    | Chọn tùy chọn này để cho phép nhân viên gửi những báo cáo chi phí vượt quá ngân sách cho phép được đặt trong sổ đăng ký ngân sách hoặc ngân sách được phép cho một dự án để được phê duyệt.                |
|**Chỉ cho phép phê duyệt báo cáo chi phí khi ngân sách bị thấu chi cho sổ đăng ký ngân sách**                | Chọn tùy chọn này để cho phép người phê duyệt phê duyệt các báo cáo chi phí vượt quá ngân sách đã cho phép được đặt trong sổ đăng ký ngân sách.                                                                       |

### <a name="per-diem"></a>Công nhật

| **Trường**                             | **Nội dung mô tả**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Số giờ tối thiểu cho công tác phí**           | Nhập số giờ tối thiểu mặc định mà một nhân viên phải làm việc trong một ngày để đủ điều kiện nhận công tác phí cho các chi phí liên quan đến đi lại.  Giá trị này chỉ được sử dụng làm giá trị mặc định cho trường Số giờ tối thiểu trên các bậc mức công tác phí.                                                                                      |
|**Phần trăm bữa ăn**                          | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các bữa ăn được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại khi trường **Tính toán giảm bữa ăn theo** được đặt thành **Loại bữa ăn mỗi ngày** hoặc **Số bữa ăn mỗi ngày**. Ngày làm việc rơi vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí cho những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành 0 (không), thì khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0. |
|**Phần trăm khách sạn**                        | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các khách sạn được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại. Ngày làm việc rơi vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí cho những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành 0 (không), thì khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0.                                              |
|**Phần trăm khác**                        | Nhập tỷ lệ phần trăm mặc định của công tác phí cho các chi phí khác được sử dụng vào ngày đầu tiên và ngày cuối cùng của chi phí liên quan đến đi lại. Ngày làm việc rơi vào ngày đầu tiên và ngày cuối cùng có thể ngắn hơn ngày làm việc tiêu chuẩn. Do đó, số tiền công tác phí cho những ngày đó có thể khác với số tiền tiêu chuẩn. Nếu phần trăm được đặt thành 0 (không), thì khoản khấu trừ cho ngày đầu tiên và ngày cuối cùng sẽ là 0.                                                                                                     |
|**Giảm tỷ lệ phần trăm cho bữa sáng** | Nhập số tiền khấu trừ công tác phí cho bữa sáng. Chẳng hạn, nếu nhân viên nhận được bữa sáng miễn phí, thì có thể bạn sẽ muốn giảm 10 phần trăm số tiền công tác phí.                               |
|**Giảm tỷ lệ phần trăm cho bữa trưa**    | Nhập số tiền khấu trừ công tác phí cho bữa trưa. Chẳng hạn, nếu nhân viên nhận được bữa trưa miễn phí, thì có thể bạn sẽ muốn giảm 15 phần trăm số tiền công tác phí.                                       |
|**Giảm tỷ lệ phần trăm cho bữa tối**   | Nhập số tiền khấu trừ công tác phí cho bữa tối. Chẳng hạn, nếu nhân viên nhận được bữa tối miễn phí, thì có thể bạn sẽ muốn giảm 25 phần trăm số tiền công tác phí.                                     |
|**Tính toán giảm bữa ăn theo**         | Chọn cách thức hệ thống tính toán mức giảm công tác phí cho bữa ăn bằng cách chọn xem mức giảm dựa trên loại bữa ăn trong mỗi chuyến đi hay mỗi ngày hoặc dựa trên số lượng bữa ăn được phép mỗi ngày.|
|**Làm tròn công tác phí**                  | Chọn loại làm tròn được sử dụng cho chi phí công tác phí. Nếu bạn chọn làm tròn thông thường, mọi chi phí công tác phí có số tiền là 0,50 được làm tròn thành 1,00 và mọi chi phí công tác phí có số tiền nhỏ hơn 0,50 được làm tròn xuống thành 0,00.                                                                                              |
|**Tính toán công tác phí cơ sở vào**         | Chọn xem số tiền công tác phí dựa trên ngày dương lịch hay khoảng thời gian 24 giờ.       |

### <a name="fax-cover-pages"></a>Trang bìa fax

| **Trường**                      | **Nội dung mô tả**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Hướng dẫn**                   | Nhập các hướng dẫn mà nhân viên phải tuân theo khi họ tạo trang bìa cho bản fax được sử dụng để gửi biên lai liên quan đến báo cáo chi phí. Bấm vào nút **Bản dịch** để nhập nội dung bằng ngôn ngữ cụ thể sẽ được hiển thị dựa trên ngôn ngữ người dùng. |
|**ID người dùng (Thông tin mã vạch)** | Chọn tùy chọn này để lưu trữ mã định danh duy nhất của nhân viên bằng mã vạch dùng trên trang bìa của bản fax.                 |
|**Mã vạch**                      | Chọn mã vạch được sử dụng trên trang bìa của bản fax. Mã vạch 39 và 128 được hỗ trợ trong phần Quản lý chi phí.               |

### <a name="anti-corruption"></a>Chống tham nhũng

|                 <strong>Trường</strong>                 |                                                                                                                                                                                            <strong>Mô tả</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Hiển thị chứng thực chống tham nhũng</strong>  | Chọn tùy chọn này để hiển thị phần nội dung chống tham nhũng khi tạo báo cáo chi phí mới. Khi đó, các danh mục chi phí cụ thể có thể được kích hoạt và yêu cầu phải chọn phần chứng thực chống tham nhũng trên báo cáo chi phí. Lấy ví dụ, danh mục quà tặng liên quan đến chi phí chính thức của chính phủ có thể yêu cầu nhân viên xác nhận rằng chi phí đó đáp ứng chính sách của công ty liên quan đến các quan chức chính phủ. |
| <strong>Thông điệp chống tham nhũng dành cho người gửi</strong> |                                                                                             Nhập nội dung sẽ được hiển thị cho nhân viên khi tạo báo cáo chi phí mới. Bấm vào nút <strong>Bản dịch</strong> để nhập nội dung bằng ngôn ngữ cụ thể sẽ được hiển thị dựa trên ngôn ngữ người dùng.                                                                                             |
| <strong>Thông điệp chống tham nhũng dành cho người phê duyệt</strong>  |                                                                                             Nhập nội dung sẽ được hiển thị cho người phê duyệt khi tạo báo cáo chi phí mới. Bấm vào nút <strong>Bản dịch</strong> để nhập nội dung bằng ngôn ngữ cụ thể sẽ được hiển thị dựa trên ngôn ngữ người dùng.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]