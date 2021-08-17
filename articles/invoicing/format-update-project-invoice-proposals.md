---
title: Quản lý đề xuất hóa đơn dự án
description: Chủ đề này cung cấp chi tiết về quy trình xử lý hóa đơn dành cho khách hàng với Project Operations cho các cho tình huống dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989937"
---
# <a name="manage-project-invoice-proposals"></a>Quản lý đề xuất hóa đơn dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bộ phận thanh toán của bạn có thể xử lý đề xuất hóa đơn dự án khi hai điều kiện sau được đáp ứng:

  - Người quản lý dự án xác nhận hóa đơn ước giá trong Microsoft Dataverse.
  - Tất cả các giao dịch bán hàng chưa được thanh toán theo thời gian và vật tư có trong hóa đơn ước giá đều được đăng bằng nhật ký Tích hợp Dynamics 365 **Project Operations**.

Hãy thực hiện các bước sau để hoàn thành đề xuất hóa đơn dự án trong Dynamics 365 Finance.

1. Xem lại thông tin thanh toán cho các giao dịch thời gian và vật tư và đăng nhật ký **Tích hợp Project Operations**.
2. Xem lại thông tin thanh toán để biết các mốc thanh toán theo giá cố định.
3. Xem lại và định dạng đề xuất hóa đơn dự án.
4. Đăng và in hóa đơn dự án.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Quản lý thông tin thanh toán trong nhật ký Tích hợp Project Operations

Thực tế dự án được tạo trong Dataverse sẽ được Kế toán dự án đánh giá và đăng trên Finance. Để biết thêm thông tin về cách làm việc với Nhật ký tích hợp, hãy xem [Nhật ký tích hợp trong Project Operations](../project-accounting/project-operations-integration-journal.md).

Thực tế chi phí và thực tế bán hàng chưa lập hóa đơn được thêm vào Nhật ký tích hợp dưới dạng các dòng riêng biệt:

  - Đơn giá vốn và số tiền chi phí trên Thực tế chi phí được mặc định là từ giao dịch chi phí của thực tế dự án trong Dataverse.
  - Đơn giá bán và số tiền bán hàng trên Giao dịch bán hàng chưa thanh toán được mặc định là từ giao dịch bán hàng chưa lập hóa đơn của thực tế dự án trong Dataverse.

### <a name="billing-sales-tax"></a>Thuế bán hàng thanh toán

Việc tính thuế bán hàng để lập hóa đơn được xác định qua việc kết hợp hai trường **Nhóm thuế bán hàng thanh toán** và **Nhóm thuế bán hàng của mặt hàng thanh toán** trong bản ghi bán hàng chưa lập hóa đơn trên dòng nhật ký kế toán của **Tích hợp Project Operations**. Hệ thống mặc định các giá trị trong trường này dựa trên cài đặt trong tab **Tài chính** trên trang **Các tham số quản lý dự án và kế toán**.

- **Phương pháp nhóm thuế bán hàng** xác định logic mặc định cho giá trị nhóm thuế bán hàng thanh toán:
  
  - **Dự án**: Sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ dự án. Bạn có thể xem lại hoặc thay đổi nhóm thuế bán hàng thanh toán mặc định trên một dự án bằng cách chọn **Hiển thị giá trị kế toán mặc định** trên trang **Tất cả dự án**.
  - **Hợp đồng dự án**: Sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ hợp đồng dự án. Bạn có thể xem lại hoặc thay đổi nhóm thuế bán hàng thanh toán mặc định trên hợp đồng dự án bằng cách chọn **Hiển thị giá trị kế toán mặc định** trên trang **Hợp đồng dự án**.
  - **Khách hàng**: Sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ khách hàng.
  - **Tìm kiếm**: Sẽ tìm kiếm trên tất cả các thực thể ở trên và chọn giá trị có sẵn đầu tiên. Việc tìm kiếm bắt đầu từ thực thể **Dự án**, rồi đến thực thể **Hợp đồng dự án**, cuối cùng là thực thể **Khách hàng**.

- **Phương pháp nhóm thuế bán hàng theo mặt hàng** xác định logic mặc định cho giá trị nhóm thuế bán hàng của mặt hàng thanh toán:
  
  - Đối với các loại giao dịch thời gian, chi phí và phí, nhóm thuế bán hàng của mặt hàng thanh toán sẽ luôn mặc định lấy từ thực thể **Danh mục dự án**.
  - Đối với các loại giao dịch quan trọng, nhóm thuế bán hàng của mặt hàng thanh toán được mặc định dựa trên thiết lập **Phương pháp nhóm thuế bán hàng** trong **Các tham số quản lý dự án và kế toán**. Số mặt hàng mặc định là nhóm thuế bán hàng theo mặt hàng từ thực thể **Sản phẩm đã phát hành**. Danh mục mặc định là nhóm thuế bán hàng theo mặt hàng từ thực thể **Danh mục dự án**.

### <a name="financial-dimensions"></a>Các lĩnh vực tài chính

Các thông số tài chính cho bản ghi bán hàng chưa được lập hóa đơn trong nhật ký **Tích hợp Project Operations** từ thực thể **Dự án**. Có thể đánh giá và điều chỉnh các thông số tài chính bằng cách chọn **Phân phối số tiền**. Nếu bạn cần thay đổi các thông số tài chính trong bản ghi bán hàng chưa lập hóa đơn sau khi nhật ký Tích hợp được đăng nhưng trước khi xác nhận hóa đơn ước giá, hãy đi đến **Tất cả dự án** > **Quản lý** > **Giao dịch đã đăng**, chọn giao dịch, sau đó chọn **Xử lý** > **Điều chỉnh kế toán**.

### <a name="exchange-rates"></a>Tỷ giá hối đoái

Loại tiền giao dịch chưa lập hóa đơn trong Dataverse được dùng làm loại tiền giao dịch trong Finance và được chuyển đổi sang tiền tệ kế toán của công ty theo tỷ giá hối đoái đã xác định trong Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Quản lý thuộc tính tài chính của các mốc thanh toán 

Mô tả hợp đồng dự án sử dụng phương thức thanh toán theo giá cố định được lập hóa đơn thông qua [Mốc giá cố định](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Kế toán dự án có thể xem lại các mốc thanh toán trong mục Finance bằng cách đi tới **Quản lý dự án và kế toán** > **Tất cả dự án** > **Quản lý** > **Giao dịch trên tài khoản**.

### <a name="billing-sales-tax"></a>Thuế bán hàng thanh toán

Các giá trị **Nhóm thuế bán hàng** và **Nhóm thuế bán hàng theo mặt hàng** mặc định lấy từ cài đặt khi một mốc thanh toán mới được tạo trong Dataverse. Hệ thống mặc định các giá trị cho trường này dựa trên cài đặt trong tab **Tài chính** trên trang **Các tham số quản lý dự án và kế toán**.

- **Phương pháp nhóm thuế bán hàng** xác định logic mặc định cho giá trị **Nhóm thuế bán hàng thanh toán**:

    - **Dự án** sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ dự án. Bạn có thể xem lại hoặc thay đổi nhóm thuế bán hàng mặc định trên một dự án bằng cách chọn **Hiển thị giá trị kế toán mặc định** trên trang **Tất cả dự án**.
    - **Hợp đồng dự án** sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ hợp đồng dự án. Bạn có thể xem lại hoặc thay đổi nhóm thuế bán hàng mặc định trên hợp đồng dự án bằng cách chọn **Hiển thị giá trị kế toán mặc định** trên trang **Hợp đồng dự án**.
    - **Khách hàng**: sẽ luôn mặc định nhóm thuế bán hàng thanh toán được lấy từ khách hàng.
    - **Tìm kiếm** sẽ tìm kiếm trên tất cả các thực thể trong danh sách này và chọn giá trị có sẵn đầu tiên. Việc tìm kiếm bắt đầu từ thực thể **Dự án**, rồi đến thực thể **Hợp đồng dự án**, sau đó là thực thể **Khách hàng**.

- **Nhóm thuế bán hàng đối với sản phẩm có mốc giá cố định** được sử dụng làm giá trị mặc định trong trường **Nhóm thuế bán sản phẩm** cho mốc thanh toán. Kế toán viên có thể xem xét và sửa đổi giá trị này trên trang **Giao dịch trên tài khoản**. Hệ thống sử dụng giá trị từ giao dịch trên tài khoản khi tạo dòng đề xuất hóa đơn dự án.
 

### <a name="financial-dimensions"></a>Các lĩnh vực tài chính

Các thông số tài chính mặc định cho mốc thanh toán giá cố định được thiết lập trên mô tả hợp đồng Dự án. Đi đến **Hợp đồng dự án** > **Hiển thị giá trị kế toán mặc định** và trên tab **Mô tả hợp đồng**, chọn **mô tả hợp đồng giá cả**, sau đó đặt các thông số tài chính thành giá trị mặc định mà bạn muốn.

Kế toán dự án có thể chỉnh sửa thông tin về thuế bán hàng và thông số tài chính trên các mốc thời gian của hóa đơn cho đến khi Đề xuất hóa đơn dự án được tạo.


## <a name="create-project-invoice-proposals"></a>Tạo đề xuất hóa đơn dự án

Bạn có thể xem xét đề xuất hóa đơn dự án trong mô-đun **Quản lý dự án và kế toán** bằng cách đi tới **Hóa đơn dự án** > **Đề xuất hóa đơn dự án**.

Tiêu đề Đề xuất hóa đơn dự án được tạo trong Finance khi hóa đơn ước giá được xác nhận trong Dataverse. Để dễ dàng điều hòa hơn, hệ thống đặt số Đề xuất hóa đơn Dự án trong Finance giống với số ID Hóa đơn ước giá trong Dataverse. Vì Hóa đơn ước không nhất thiết phải được xác nhận theo đúng thứ tự được tạo, nên dãy số của Đề xuất hóa đơn dự án trong Finance phải cho phép thay đổi thành các số nhỏ hơn và lớn hơn. Làm theo các bước sau để định cấu hình dãy số:

1. Trong Finance, đi tới **Quản trị Tổ chức** > **Dãy số** > **Dãy số**.
2. Trong bộ lọc **Khu vực**, chọn **Dự án**.
3. Trong bộ lọc **Tham chiếu**, chọn **Đề xuất hóa đơn**.
4. Dùng trường **Công ty** để lọc từng pháp nhân có khả năng tích hợp Dataverse Project Operations.
5. Mở **Chi tiết Dãy số** và trên tab **Chung** hãy đặt:

    - **Cho phép người dùng thay đổi: Thành số bé hơn** = **Có**
    - **Cho phép người dùng thay đổi: Thành số lớn hơn** = **Có**

Các dòng đề xuất hóa đơn được hệ thống thêm vào qua quy trình định kỳ **Nhập từ bảng tách chuyển** (**Quản lý dự án và kế toán** > **Định kỳ** > **Tích hợp Project Operations** > **Nhập từ bảng tách chuyển**). Bạn có thể chạy quy trình này theo cách thủ công hoặc dùng lịch trình định kỳ. Hệ thống sẽ không thêm các dòng vào tài liệu đề xuất hóa đơn cho đến khi tất cả các dòng đã sẵn sàng để lập hóa đơn. Các giao dịch thời gian và vật tư chỉ sẵn sàng được lập hóa đơn khi được đăng thông qua nhật ký **Tích hợp Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Định dạng và in đề xuất hóa đơn

Kế toán dự án có thể tùy chỉnh bản in hóa đơn dự án bằng cách sử dụng trang **Định dạng đề xuất hóa đơn** và tính năng quản lý in.

### <a name="format-invoice-proposals"></a>Định dạng đề xuất hóa đơn

Trang **Định dạng đề xuất hóa đơn** cho phép các giao dịch nhóm tùy chỉnh hiển thị trong hóa đơn dự án của khách hàng.

1. Trên trang **Đề xuất hóa đơn dự án**, chọn **In** > **Định dạng đề xuất hóa đơn**.
2. Chọn **Mới** để tạo một nhóm mới cho bản in Hóa đơn dự án.
3. Trong trường **Chi tiết/Tóm tắt**, chọn các tùy chọn cho nhóm này:

    - Chọn **Chi tiết** để in các chi tiết giao dịch trong hóa đơn khách hàng.
    - Chọn **Tóm tắt** để in tóm tắt giao dịch của hóa đơn khách hàng.

> [!NOTE]
> Sự lựa chọn trong trường **Chi tiết/Tóm tắt** trên trang **Định dạng đề xuất hóa đơn** sẽ ghi đè lên tùy chọn đã chọn trong trường **Định dạng hóa đơn** trên trang **Đề xuất hóa đơn** để in hóa đơn chi tiết hoặc hóa đơn tóm tắt.

- Chọn các mô tả giao dịch để đưa vào phần này trên tab **Các giao dịch có sẵn** và chọn **Bao gồm các giao dịch** để di chuyển chúng đến tab **Các giao dịch đã chọn**.
- Chọn **Di chuyển lên** và **Di chuyển xuống** để thay đổi thứ tự các phần.
- Chọn **Xem trước khi in** để xem trước hóa đơn đã định dạng.

### <a name="print-management"></a>Quản lý in

Tính năng Quản lý in dùng các tệp báo cáo khác nhau để in, chỉ định đích và tùy chỉnh văn bản chân trang cho hóa đơn. Bạn có thể thiết lập Quản lý in ở cấp mô-đun, tuy nhiên, những cài đặt này có thể được ghi đè cho một khách hàng, hợp đồng hoặc đề xuất hóa đơn cụ thể. Để truy cập chức năng này trên trang **Đề xuất hóa đơn dự án**, chọn **In** > **Quản lý in**.

Thiết lập quản lý in được hiển thị ở chế độ xem dạng cây, trong đó mỗi cấp độ nút hiển thị các tài liệu có sẵn để điều chỉnh. Bạn có thể chỉ định các bản in tùy chỉnh ở cấp độ mô-đun, khách hàng, hợp đồng hoặc tài liệu đề xuất hóa đơn. Để sửa đổi bản in tài liệu gốc, hãy mở rộng nút mong muốn và chọn **Mục ban đầu**. Trong trường **Định dạng báo cáo**, chọn định dạng báo cáo sẽ được dùng để in. Bạn có thể dùng các định dạng báo cáo tùy chỉnh bằng cách sử dụng [Khung quản lý tài liệu kinh doanh](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Đăng đề xuất hóa đơn

Sau khi hóa đơn đã được xem xét và chỉnh sửa, các dòng đề xuất hóa đơn đạt yêu cầu, hãy kiểu tra tổng số của hóa đơn và thuế bán hàng. Trong nhóm **Chi tiết**, chọn **Tổng số** rồi chọn **Đăng** để đăng hóa đơn.

Để xem hóa đơn trước khi đăng, bỏ chọn ô **Đăng bài**. Từ **Ước giá** sẽ được in lên hóa đơn để xác nhận đây là hóa đơn mẫu. Để in hóa đơn, hãy chọn hộp kiểm **In hóa đơn**.

Ngoài trang **Đề xuất hóa đơn**, bạn cũng có thể đăng đề xuất hóa đơn bằng cách chạy công việc định kỳ là **Đăng đề xuất hóa đơn**. Để tìm công việc này, hãy truy cập vào **Quản lý dự án và kế toán** > **Định kỳ** > **Hóa đơn dự án** > **Đăng đề xuất hóa đơn**.

Trang này hiển thị tất cả các đề xuất hóa đơn đã sẵn sàng để đăng. Bạn có thể lên lịch đăng các đề xuất hóa đơn bằng cách chọn **Hàng loạt**. Đặt **Tham số xử lý hàng loạt** thành **Có** và đặt lặp lại quá trình xử lý hàng loạt bằng cách chọn **Lặp lại**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
