---
title: Nhật ký tích hợp trong Project Operations
description: Bài viết này cung cấp thông tin về cách làm việc với tạp chí Tích hợp trong Hoạt động Dự án.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923904"
---
# <a name="integration-journal-in-project-operations"></a>Nhật ký tích hợp trong Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các mục nhập thời gian và chi phí tạo ra các giao dịch **Thực tế** thể hiện quan điểm hoạt động của công việc đã hoàn thành dựa trên một dự án. Dynamics 365 Project Operations cung cấp cho nhân viên kế toán một công cụ để đánh giá các giao dịch và điều chỉnh các thuộc tính kế toán khi cần. Sau khi đánh giá và điều chỉnh xong, các giao dịch được đăng lên Sổ cái dự án và Sổ cái. Kế toán có thể thực hiện các hoạt động này bằng cách sử dụng **Tích hợp hoạt động dự án** tạp chí (**Dynamics 365 Finance** > **Quản lý dự án và kế toán** > **Tạp chí** > **Tích hợp hoạt động dự án** tạp chí.

![Luồng nhật ký tích hợp.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Tạo bản ghi trong nhật ký Tích hợp Project Operations

Các bản ghi trong nhật ký Tích hợp Project Operations được tạo bằng quy trình định kỳ **Nhập từ bảng tách chuyển**. Bạn có thể chạy quá trình này bằng cách đi tới **Dynamics 365 Finance** > **Quản lý dự án và kế toán** > **Định kỳ** > **Tích hợp hoạt động dự án** > **Nhập từ bảng dàn**. Bạn có thể chạy quy trình này theo cách tương tác hoặc đặt cấu hình quy trình để chạy trong nền khi cần.

Khi quy trình định kỳ chạy, bất kỳ giao dịch thực tế nào chưa được thêm vào nhật ký Tích hợp Project Operations đều được tìm thấy. Một dòng nhật ký kế toán cho mỗi giao dịch thực tế sẽ được tạo.
Hệ thống nhóm các dòng tạp chí thành các tạp chí riêng biệt dựa trên giá trị được chọn trong **Đơn vị kỳ trên tạp chí Tích hợp Hoạt động Dự án** đồng ruộng (**Tài chính** > **Quản lý dự án và kế toán** > **Thành lập** > **Quản lý dự án và các thông số kế toán**, **động Dự án trên Dynamics 365 Customer Engagement** chuyển hướng). Các giá trị có thể có cho trường này bao gồm:

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
    - Nếu **Loại giao dịch** không được đặt trong thực tế Dự án, hệ thống sử dụng giá trị trong **Danh mục dự án mặc định** lĩnh vực trên **Hoạt động Dự án trên Dynamics 365 Customer Engagement** tab trên **Quản lý dự án và các thông số kế toán** trang.
  - Trường **Nguồn** đại diện cho nguồn lực dự án liên quan đến giao dịch này. Nguồn lực được dùng làm tham chiếu trong các đề xuất hóa đơn của Dự án cho khách hàng.
  - Các **Tỷ giá** trường mặc định từ **Tỷ giá hối đoái** được đặt trong Dynamics 365 Finance. Nếu không thiết lập tỷ giá hối đoái, quy trình định kỳ **Nhập từ bảng tách chuyển** sẽ không thêm bản ghi vào nhật ký và một thông báo lỗi sẽ được thêm vào nhật ký thực hiện công việc.
  - Trường **Thuộc tính mô tả** đại diện cho loại hình thanh toán trong các Giao dịch thực tế của dự án. Thuộc tính dòng và ánh xạ loại thanh toán được xác định trên **Hoạt động Dự án trên Dynamics 365 Customer Engagement** tab trên **Các thông số kế toán và quản lý dự án** trang.

Chỉ các thuộc tính kế toán sau mới được cập nhật trong các dòng nhật ký kế toán trên Project Operations:

- **Nhóm thuế bán hàng thanh toán** và **Nhóm thuế bán hàng của mặt hàng thanh toán**
- **Các lĩnh vực tài chính** (sử dụng hành động **Phân phối số tiền**)

Các dòng nhật ký kế toán tích hợp có thể bị xóa. Tuy nhiên, bất kỳ dòng nào chưa được đăng sẽ được chèn lại vào nhật ký sau khi bạn chạy lại quy trình định kỳ **Nhập từ bảng tách chuyển**.

Khi bạn đăng Nhật ký tích hợp, một sổ cái phụ của dự án và các giao dịch trên sổ cái chung sẽ được tạo. Chúng được dùng trong việc lập hóa đơn cho khách hàng hạ nguồn, ghi nhận doanh thu và báo cáo tài chính.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
