---
title: Tạo giao dịch liên công ty
description: Bài viết này cung cấp thông tin về cách tạo giao dịch liên công ty.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da6fd8e0e6bfe2e2543f5c4a453ed769e412f1e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919396"
---
# <a name="create-intercompany-transactions"></a>Tạo giao dịch liên công ty

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Giao dịch liên công ty là các giao dịch chi phí và thời gian trong hợp đồng dự án, thuộc về một công ty hoặc đơn vị tổ chức, trong khi nguồn lực trên hợp đồng dự án lại là một phần của công ty hoặc đơn vị tổ chức khác.

Khi một giao dịch liên công ty được phê duyệt, những giao dịch thực tế sau sẽ được tạo

| **Loại giao dịch** | **Bảng giá áp dụng** | **Loại tiền giao dịch** |
| --- | --- | --- |
| Chi phí | Bảng chi phí đơn vị hợp đồng | Tiền tệ trên dòng ghi giá |
| Lần bán chưa lập hóa đơn. Những giao dịch này chỉ được tạo cho các trường hợp thực tế liên kết với một dòng hợp đồng có chứa loại hóa đơn, thời gian và tài liệu. | Bảng giá bán theo hợp đồng dự án | Tiền tệ trên hợp đồng |
| Chi phí đơn vị nguồn lực | Bảng giá chi phí của đơn vị cung ứng nguồn lực | Tiền tệ trên dòng ghi giá |
| Lần bán của đơn vị liên tổ chức | Bảng chi phí đơn vị hợp đồng | Tiền tệ trên dòng ghi giá |

**Đơn vị tổ chức** sẽ quyết định tiền tệ và giá cả của giao dịch bán hàng đơn vị liên tổ chức, chi phí và chi phí của đơn vị cung ứng nguồn lực. Đây là điều bạn cần lưu ý khi quyết định cấu trúc của công ty và các đơn vị tổ chức khi triển khai.

Khi tạo cơ hội, báo giá, hợp đồng dự án và các bản ghi của dự án, hệ thống sẽ xác minh rằng tiền tệ của đơn vị hợp đồng khớp với tiền tệ kế toán của công ty hợp đồng. Nếu khác, những bản ghi này sẽ không được tạo. Bạn có thể thiết lập tiền tệ của đơn vị tổ chức trong Dynamics 365 Project Operations bằng cách đi tới **Dataverse** > **Cài đặt** > **Đơn vị tổ chức**. Bạn có thể thiết lập tiền tệ kế toán của công ty trong Dynamics 365 Finance bằng cách đi tới **Sổ cái chung** > **Thiết lập sổ cái** > **Sổ cái**. Tiền tệ sẽ được đồng bộ với môi trường Dataverse thông qua bản đồ Ghi kép sổ cái.

Hệ thống sẽ tạo giá trị thực cho chi phí của đơn vị cung ứng nguồn lực hoặc lần bán của đơn vị liên tổ chức trong các trường hợp sau:

  - Khi đơn vị cung ứng nguồn lực khác với đơn vị hợp đồng
  - Khi công ty cung ứng nguồn lực khác với công ty hợp đồng

Tuy nhiên, chỉ những giao dịch có công ty cung ứng nguồn lực khác với công ty hợp đồng thì mới được chuyển sang môi trường Dynamics 365 Finance để tiến hành hoạt động kế toán bổ sung.

Hoạt động kế toán đối với giá trị thực của dự án sẽ được ghi lại trong nhật ký tích hợp Project Operations của phần Tài chính. Hệ thống sẽ tạo các dòng nhật ký sau.

| **Loại giao dịch** | **Thực thể pháp lý** | **Tạo giao dịch dự án khi đăng** | **Thông số tài chính lấy mặc định từ** | **Nhóm thuế bán hàng thanh toán mặc định và nhóm thuế bán hàng của mặt hàng thanh toán** |
| --- | --- | --- | --- | --- |
| Chi phí | Không được thêm vào nhật ký tích hợp | Không áp dụng | Không áp dụng | Không áp dụng |
| Doanh thu chưa lập hóa đơn | Nhật ký tích hợp của pháp nhân đi thuê | Có | Dự án | **Nhóm thuế bán hàng thanh toán**: Dựa trên **khách hàng hợp đồng** <br/> **Nhóm thuế bán hàng của mặt hàng thanh toán**: Lấy từ danh mục dự án của pháp nhân hiện tại trên dòng nhật ký kế toán |
| Chi phí đơn vị nguồn lực | Nhật ký tích hợp của pháp nhân cho thuê | No | Khách hàng liên công ty | **Nhóm thuế bán hàng thanh toán**: Dựa trên **khách hàng liên công ty** <br/> **Nhóm thuế bán hàng của mặt hàng thanh toán**: Lấy từ danh mục dự án của pháp nhân hiện tại trên dòng nhật ký kế toán |
| Giao dịch liên tổ chức | Nhật ký tích hợp của pháp nhân cho thuê | No | Khách hàng liên công ty | **Nhóm thuế bán hàng thanh toán**: Dựa trên **khách hàng liên công ty** <br/> **Nhóm thuế bán hàng của mặt hàng thanh toán**: Lấy từ danh mục dự án của pháp nhân hiện tại trên dòng nhật ký kế toán |

### <a name="example-intercompany-transactions"></a>Ví dụ: Giao dịch liên công ty

Molly Clark, nhà phát triển được GBPM thuê có 10 giờ làm việc cho dự án của USPM Adventure Works, đã được quản lý dự án phê duyệt. Chi phí nhà phát triển của GBPM là 88 GBP mỗi giờ. GBPM sẽ thu USPM 120 USD cho mỗi giờ làm việc của nhà phát triển. USPM sẽ thu khách hàng của họ là Adventure Works 200 USD cho công việc mà nguồn lực của GBPM hoàn thành. Để biết thêm thông tin, xem [Đặt cấu hình hóa đơn liên công ty](configure-intercompany-invoicing.md).

1. Trong Project Operations, hãy đi tới **Nguồn lực** rồi chọn **Molly Clark** từ danh sách. Trên tab **Lịch làm việc**, trong trường **Công ty**, hãy chọn **GBPM**.
2. Đi tới **Bán hàng** > **Khách hàng** rồi chọn **Mới** để tạo bản ghi khách hàng mới cho Adventure Works.
    1. Đặt công ty thành **USPM**.
    2. Đặt **Mối quan hệ** thành **Khách hàng**.
    3. Chọn **Nhóm khách hàng 10 – Trong nước**.
    4. Đặt tiền tệ thành **USD**.
    5. Lưu bản ghi.
3. Đi tới **Bán hàng** > **Hợp đồng dự án** rồi tạo hợp đồng dự án mới cho Adventure Works.
    1. Đặt công ty sở hữu thành **USPM** và đơn vị hợp đồng thành **Contoso Robotics US**.
    2. Chọn Adventure Works làm khách hàng.
    3. Chọn bảng giá sản phẩm và lưu bản ghi.
    4. Trên tab **Dòng hợp đồng**, hãy tạo một dòng hợp đồng mới. Đặt tên bất kỳ, sau đó chọn **Thời gian và tài liệu** làm phương thức thanh toán.
    5. Tạo dự án mới và liên kết dự án đó với dòng hợp đồng này.
4. Đăng nhập với tư cách nguồn lực, **Molly Clark**. Đi tới **Dự án** > **Mục thời gian** rồi tạo một mục thời gian cho Adventure Works.
5. Đăng nhập với tư cách Quản lý dự án. Đi tới **Dự án** > **Phê duyệt** và phê duyệt giao dịch mục thời gian mà Molly Clark đã ghi.
6. Chuyển đến dự án Adventure Works rồi chọn **Có liên quan** > **Giá trị thực tế**. Những giao dịch thực tế sau đây sẽ được tạo.

| **Loại giao dịch** | **Giá** | **Loại tiền giao dịch** | **Số lượng** |
| --- | --- | --- | --- |
| Chi phí | 120 | USD | 1200 |
| Doanh thu chưa lập hóa đơn | 200 | USD | 2000 |
| Chi phí đơn vị nguồn lực | 88 | GBP | 880 |
| Lần bán của đơn vị liên tổ chức | 120 | USD | 1200 |

7. Đăng nhập với tư cách kế toán viên của USPM. Mở phiên bản Tài chính của Project Operations rồi chọn công ty **USPM**. 
8. Đi tới **Quản lý dự án và kế toán** > **Định kỳ** > **Project Operations trên Customer Engagement** > **Nhập từ bảng tách chuyển** rồi chọn chạy quy trình định kỳ. Quy trình định kỳ này sẽ điền vào nhật ký Tích hợp Project Operations.
9. Đi tới **Quản lý dự án và kế toán** > **Nhật ký** > **Nhật ký tích hợp Project Operations** rồi xem lại dòng nhật ký kế toán. Hệ thống sẽ tạo các dòng sau.

    | **Loại giao dịch** | **Giá** | **Loại tiền giao dịch** | **Số lượng** |
    | --- | --- | --- | --- |
    | Doanh thu chưa lập hóa đơn | 200 | USD | 2000 |

    Nếu thiết lập hệ thống tích lũy doanh thu cho dự án này, những thông tin sau đây sẽ được đăng:

    - Nợ: Dự án – giá trị WIP 200 USD
    - Có: Dự án – Doanh thu tích lũy 200 USD

    Giao dịch chưa thanh toán này giờ đã sẵn sàng để lập hóa đơn. Hóa đơn của khách hàng Adventure Works có thể được đăng dưới khía cạnh tài chính khi cần.

10. Đăng nhập với tư cách kế toán viên **GBPM**. Mở phiên bản Tài chính của Project Operations rồi chọn công ty **GBPM**. 
11. Chuyển đến **Quản lý dự án và kế toán** > **Định kỳ** > **Tích hợp Project Operations** > **Nhập từ bảng tách chuyển** rồi chạy quy trình định kỳ để điền vào nhật ký Tích hợp Project Operations.
12. Đi tới **Quản lý dự án và kế toán** > **Nhật ký** > **Nhật ký tích hợp Project Operations** rồi xem lại các dòng. Hệ thống sẽ tạo các dòng sau.

    | **Loại giao dịch** | **Giá** | **Loại tiền giao dịch** | **Số lượng** |
    | --- | --- | --- | --- |
    | Chi phí đơn vị nguồn lực | 88 | GBP | 880 |
    | Lần bán của đơn vị liên tổ chức | 120 | USD | 1200 |

    Việc đăng những bản ghi này sẽ dẫn đến các giao dịch chứng từ sau:

    - Nợ: Chi phí dự án là 88 GBP
    - Có: Phân bổ tiền lương 88 GBP

    Nếu thiết lập hệ thống tích lũy doanh thu liên công ty, những thông tin sau đây sẽ được đăng:

    - Nợ: Dự án – giá trị WIP 120 USD
    - Có: Dự án – Doanh thu tích lũy 120 USD

    Hệ thống giờ đã sẵn sàng để tọa hóa đơn khách hàng liên công ty.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
