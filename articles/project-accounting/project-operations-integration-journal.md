---
title: Nhật ký tích hợp trong Project Operations
description: Bài viết này cung cấp thông tin về cách làm việc với Nhật ký tích hợp trong Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541104"
---
# <a name="integration-journal-in-project-operations"></a>Nhật ký tích hợp trong Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các mục nhập thời gian, chi phí, phí và vật liệu tạo ra các giao dịch **Thực tế** thể hiện quan điểm hoạt động của công việc đã hoàn thành dựa trên một dự án. Dynamics 365 Project Operations cung cấp cho nhân viên kế toán một công cụ để đánh giá các giao dịch và điều chỉnh các thuộc tính kế toán khi cần. Sau khi đánh giá và điều chỉnh xong, các giao dịch được đăng lên Sổ cái dự án và Sổ cái. Nhân viên kế toán có thể thực hiện các hoạt động này bằng cách sử dụng nhật ký **Tích hợp Project Operations** (**Dynamics 365 Finance** > **Quản lý dự án và kế toán** > **Nhật ký** > **nhật ký Tích hợp Project Operations**).

![Luồng nhật ký tích hợp.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Tạo bản ghi trong nhật ký Tích hợp Project Operations

Các bản ghi trong nhật ký Tích hợp Project Operations được tạo bằng quy trình định kỳ **Nhập từ bảng tách chuyển**. Bạn có thể chạy quy trình này bằng cách đi tới **Dynamics 365 Finance** > **Quản lý dự án và kế toán** > **Định kỳ** > **Tích hợp Project Operations** > **Nhập từ bảng tách chuyển**. Bạn có thể chạy quy trình này theo cách tương tác hoặc đặt cấu hình quy trình để chạy trong nền khi cần.

Khi quy trình định kỳ chạy, bất kỳ giao dịch thực tế nào chưa được thêm vào nhật ký Tích hợp Project Operations đều được tìm thấy. Một dòng nhật ký kế toán cho mỗi giao dịch thực tế sẽ được tạo.
Hệ thống nhóm các dòng nhật ký kế toán thành các nhật ký riêng dựa trên giá trị được chọn trong trường **Đơn vị kỳ trên nhật ký Tích hợp Project Operations** (**Finance** > **Quản lý dự án và kế toán** > **Thiết lập** > **Các tham số quản lý dự án và kế toán**, **Project Operations trên tab Dynamics 365 Customer Engagement**). Các giá trị có thể có cho trường này bao gồm:

  - **Ngày**: Các giá trị thực tế được nhóm theo ngày giao dịch. Một nhật ký riêng được tạo cho mỗi ngày.
  - **Tháng**: Các giao dịch thực tế được nhóm theo tháng. Một nhật ký riêng được tạo cho mỗi tháng.
  - **Năm**: Các giao dịch thực tế được nhóm theo năm. Một nhật ký riêng được tạo cho mỗi năm.
  - **Tất cả**: Tất cả giao dịch thực tế được đưa vào cùng một nhật ký tích hợp. Nếu nhật ký không khả dụng khi quy trình định kỳ chạy, chẳng hạn như nếu nhật ký đang trong quá trình đăng các giao dịch, thì một nhật chí mới sẽ được tạo.

Các dòng nhật ký kế toán được tạo dựa trên giao dịch thực tế của dự án. Danh sách sau đây bao gồm một số quy tắc mặc định và chuyển đổi đáng chú ý hơn:

  - Mỗi giao dịch thực tế của dự án có một dòng trong nhật ký Tích hợp Project Operations. Chi phí và các giao dịch bán hàng chưa được thanh toán của loại hình thanh toán theo thời gian và vật tư được hiển thị trên các dòng riêng biệt.
  - Trường **Ngày** thể hiện ngày giao dịch. Trường **Ngày kế toán** thể hiện ngày giao dịch được ghi vào sổ cái. Nếu ngày kế toán là trong [kỳ tài chính đã chốt](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) và tham số **Tự động đặt ngày kế toán thành kỳ sổ cái mở** được đặt trên tab **Tài chính** của trang **Các tham số quản lý dự án và kế toán**, thì hệ thống sẽ điều chỉnh ngày kế toán của giao dịch thành ngày đầu tiên trong kỳ sổ cái mở tiếp theo.
  - Trường **Chứng từ** cho thấy số chứng từ của mọi giao dịch thực tế. Dãy số chứng từ được xác định trên tab **Dãy số**, trên trang **Các tham số quản lý dự án và kế toán**. Mỗi dòng được chỉ định một số mới. Sau khi chứng từ được đăng, bạn có thể xem chi phí và giao dịch bán hàng chưa được thanh toán có liên quan như thế nào bằng cách chọn **Chứng từ liên quan** trên trang **Giao dịch chứng từ**.
  - Trường **Thể loại** đại diện cho một giao dịch của dự án và là trường mặc định dựa trên thể loại giao dịch của giao dịch thực tế trong dự án có liên quan.
    - Nếu **Thể loại giao dịch** được đặt trong Giao dịch thực tế của dự án và một **Thể loại dự án** có liên quan tồn tại trong một pháp nhân nhất định, thì thể loại mặc định là thể loại dự án này.
    - Nếu **Thể loại giao dịch** không được đặt trong Giao dịch thực tế của dự án, hệ thống sử dụng giá trị trong trường **Thể loại dự án mặc định** trên tab **Project Operations trên tab Dynamics 365 Customer Engagement** trên trang **Các tham số quản lý dự án và kế toán**.
  - Trường **Nguồn** đại diện cho nguồn lực dự án liên quan đến giao dịch này. Nguồn lực được dùng làm tham chiếu trong các đề xuất hóa đơn của Dự án cho khách hàng.
  - Trường **Tỷ giá hối đoái** là trường mặc định từ **Tỷ giá hối đoái ngoại tệ** được đặt trong Dynamics 365 Finance. Nếu không thiết lập tỷ giá hối đoái, quy trình định kỳ **Nhập từ bảng tách chuyển** sẽ không thêm bản ghi vào nhật ký và một thông báo lỗi sẽ được thêm vào nhật ký thực hiện công việc.
  - Trường **Thuộc tính mô tả** đại diện cho loại hình thanh toán trong các Giao dịch thực tế của dự án. Việc ánh xạ thuộc tính mô tả và loại hình thanh toán được xác định trên tab **Project Operations trên Dynamics 365 Customer Engagement** trên trang **Tham số quản lý dự án và kế toán**.

Chỉ các thuộc tính kế toán sau mới được cập nhật trong các dòng nhật ký kế toán trên Project Operations:

- **Nhóm thuế bán hàng thanh toán** và **Nhóm thuế bán hàng của mặt hàng thanh toán**
- **Các lĩnh vực tài chính** (sử dụng hành động **Phân phối số tiền**)

Các mô tả nhật ký tích hợp có thể bị xóa. Tuy nhiên, bất kỳ dòng nào chưa được đăng sẽ được chèn lại vào nhật ký sau khi bạn chạy lại quy trình định kỳ **Nhập từ bảng tách chuyển**.

### <a name="post-the-project-operations-integration-journal"></a>Đăng nhật ký tích hợp Project Operations

Khi bạn đăng Nhật ký tích hợp, một sổ cái phụ của dự án và các giao dịch trên sổ cái chung sẽ được tạo. Chúng được dùng trong việc lập hóa đơn cho khách hàng hạ nguồn, ghi nhận doanh thu và báo cáo tài chính.

Nhật ký tích hợp Project Operations đã chọn có thể được đăng bằng cách sử dụng **Đăng** trên trang nhật ký tích hợp Project Operations. Tất cả các nhật ký có thể được đăng tự động bằng cách chạy một quy trình tại **Định kỳ** > **Tích hợp Project Operations** > **Đăng nhật ký tích hợp Project Operations**.

Việc đăng có thể được thực hiện theo cách tương tác hoặc theo lô. Lưu ý rằng tất cả các nhật ký có hơn 100 dòng sẽ tự động được đăng trong một lô. Để có hiệu suất tốt hơn khi các nhật ký có nhiều dòng được đăng trong một lô, hãy bật tính năng **Đăng nhật ký tích hợp Project Operations bằng cách sử dụng nhiều nhiệm vụ theo lô** trong không gian làm việc **Quản lý tính năng**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Chuyển tất cả các dòng có lỗi đăng sang một nhật ký mới

> [!NOTE]
> Để sử dụng khả năng này, hãy bật tính năng **Chuyển tất cả các dòng có lỗi đăng sang một nhật ký tích hợp Project Operations mới** trong không gian làm việc **Quản lý tính năng**.

Tính năng này giúp cải thiện trải nghiệm với nhật ký tích hợp Project Operations. Khi nó được bật, các sự cố về thời gian ghi kép và các vấn đề thiết lập không còn ngăn không cho đăng các nhật ký hợp lệ. Trong quá trình đăng nhật ký tích hợp Project Operations, hệ thống sẽ xác nhận mọi dòng trong nhật ký. Nó đăng tất cả các dòng không có lỗi và tạo một nhật mới cho tất cả các dòng có lỗi đăng.

Để xem lại các tạp chí có dòng có lỗi đăng, hãy truy cập **Quản lý dự án và kế toán** \> **Nhật ký** \> **Nhật ký tích hợp Project Operations** và lọc danh sách nhật ký bằng cách sử dụng trường **Nhật ký ban đầu**. Hình minh họa sau đây cho thấy một ví dụ trong đó các nhật ký trên trang **Nhật ký tích hợp Project Operations** đã được lọc theo cách này.

![Nhật ký ban đầu được hiển thị trên trang nhật ký tích hợp Project Operations.](./media/transferLines-originalJournal.png)

Nếu một công việc theo lô định kỳ được định cấu hình để đăng nhật ký tích hợp, việc đăng sẽ được thực hiện lại và các nhật ký sẽ được đăng nếu sự cố về thời gian đã được khắc phục. Mọi nhật ký còn lại nên được điều tra thủ công bằng cách xem lại nhật ký và thực hiện bất kỳ hành động bắt buộc nào.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
