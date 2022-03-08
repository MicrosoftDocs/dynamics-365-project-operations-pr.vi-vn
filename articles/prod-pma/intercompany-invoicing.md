---
title: Lập hóa đơn liên công ty
description: Bài viết này cung cấp thông tin và ví dụ về việc lập hóa đơn liên công ty cho dự án.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c201ccec2069869707409ff6a9236e81e125f06b391c67202927f5c038787d8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995832"
---
# <a name="intercompany-invoicing"></a>Lập hóa đơn liên công ty

[!include [banner](../includes/banner.md)]

Bài viết này cung cấp thông tin và ví dụ về việc lập hóa đơn liên công ty cho dự án.

Tổ chức của bạn có thể có nhiều bộ phận, công ty con và pháp nhân khác chuyển sản phẩm và dịch vụ cho nhau trong các dự án. Pháp nhân cung cấp dịch vụ hoặc sản phẩm được gọi là *pháp nhân cho vay*, còn pháp nhân nhận dịch vụ hoặc sản phẩm được gọi là *pháp nhân vay*. 

Hình sau đây minh họa một kịch bản điển hình: hai pháp nhân SI FR (pháp nhân vay) và SI USA (pháp nhân cho vay) chia sẻ nguồn lực để thực hiện một dự án cho khách hàng A. Trong kịch bản này, SI FR đã ký hợp đồng để cung cấp sản phẩm cho khách hàng A. 

[![Ví dụ về việc lập hóa đơn liên công ty.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Mục tiêu là làm cho việc kiểm soát chi phí, ghi nhận doanh thu, thuế và giá chuyển nhượng cho các giao dịch liên công ty trong dự án trở nên linh hoạt và mạnh mẽ hơn. Ngoài ra, các khả năng sau được cung cấp:

-   Tạo hóa đơn cho khách hàng đối với một dự án ở pháp nhân vay bằng bảng chấm công liên công ty, chi phí và hóa đơn cho nhà cung cấp ở pháp nhân cho vay.
-   Hỗ trợ tính toán thuế và chi phí gián tiếp.
-   Hoãn ghi nhận doanh thu ở pháp nhân cho vay và khi pháp nhân vay phải ghi nhận chi phí.
-   Tích lũy doanh thu công việc đang làm (WIP) ở pháp nhân cho vay.
-   Đặt giá chuyển nhượng có thể dựa trên các mô hình định giá khác nhau. Dưới đây là một số ví dụ:
    -   **Số lượng** – Số tiền bạn nhập vào trường **Định giá** là chi phí thực tế cho mỗi số lượng hoặc đơn vị.
    -   **Số tiền phí** – Giá/chi phí mỗi giao dịch cộng với số tiền phí mà bạn nhập vào trường **Định giá**.
    -   **Phần trăm phí** – Giá chuyển nhượng là giá/chi phí mỗi giao dịch nhân với tỷ lệ phần trăm phí mà bạn nhập vào trường **Định giá**.
    -   **Phần trăm giá bán** – Tỷ lệ phần trăm của giá bán được chuyển nhượng cho pháp nhân cho vay.
    -   **Số tiền dưới giá bán** – Số tiền giá bán mà pháp nhân vay giữ lại trước khi chuyển cho pháp nhân cho vay.
    -   **Tỷ lệ đóng góp** – Số bạn nhập vào trường **Định giá** là tỷ lệ đóng góp, được biểu thị bằng tỷ lệ phần trăm của giá bán.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Ví dụ 1: Thiết lập tham số cho việc lập hóa đơn liên công ty
Trong ví dụ này, USSI là pháp nhân cho vay và các nguồn lực của công ty báo cáo thời gian dành cho pháp nhân vay FRSI sở hữu hợp đồng với khách hàng cuối. Số giờ và chi phí mà nhân viên USSI báo cáo có thể được đưa vào hóa đơn dự án mà FRSI tạo. Ngoài ra, còn một nguồn giao dịch thứ ba có thể bắt nguồn từ pháp nhân cho vay (trong ví dụ này là USSI) khi công ty chia sẻ các dịch vụ của nhà cung cấp cho công ty con (chẳng hạn như FRSI), rồi chuyển các chi phí đó sang các dự án ở công ty con đó. Tất cả các chứng từ hóa đơn khớp và các phép tính thuế đều do Finance hoàn thành. 

Trong ví dụ này, FRSI phải là khách hàng ở pháp nhân USSI và USSI phải là nhà cung cấp ở pháp nhân FRSI. Sau đó, bạn có thể thiết lập mối quan hệ liên công ty giữa hai pháp nhân. Quy trình sau đây cho biết cách thiết lập các tham số để cả hai pháp nhân có thể tham gia vào việc lập hóa đơn liên công ty.

1. Thiết lập FRSI làm khách hàng ở pháp nhân USSI và thiết lập USSI làm nhà cung cấp ở pháp nhân FRSI. Có ba điểm nhập cho các bước cần thiết cho nhiệm vụ này.

   | Bước |                                                       Điểm nhập                                                        |                                                                                                                                                                                               Mô tả                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Trong USSI, bấm vào <strong>Tài khoản phải thu</strong> &gt; <strong>Khách hàng</strong> &gt; <strong>Tất cả khách hàng</strong>. |                                                                                                                                                                  Tạo bản ghi khách hàng mới cho FRSI và chọn nhóm khách hàng.                                                                                                                                                                  |
   |  B   |    Trong FRSI, bấm vào <strong>Tài khoản phải trả</strong> &gt; <strong>Nhà cung cấp</strong> &gt; <strong>Tất cả nhà cung cấp</strong>.     |                                                                                                                                                                    Tạo bản ghi nhà cung cấp mới cho USSI và chọn nhóm nhà cung cấp.                                                                                                                                                                    |
   |  C   |                                  Trong FRSI, mở bản ghi nhà cung cấp mà bạn vừa tạo.                                  | Trên ngăn Hành động, ở tab <strong>Chung</strong>, trong nhóm <strong>Thiết lập</strong>, bấm vào <strong>Liên công ty</strong>. Trên trang <strong>Liên công ty</strong>, ở tab <strong>Quan hệ giao dịch</strong>, chuyển thanh trượt <strong>Hiện hoạt</strong> sang <strong>Có</strong>. Trong trường <strong>Công ty khách hàng</strong>, chọn bản ghi khách hàng mà bạn đã tạo ở bước A. |


2. Bấm vào **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Tham số quản lý dự án và kế toán**, rồi bấm vào tab **Liên công ty**. Cách thức thiết lập tham số sẽ phụ thuộc vào việc bạn là pháp nhân vay hay pháp nhân cho vay.
   -   Nếu bạn là pháp nhân vay, hãy chọn danh mục mua sắm sẽ dùng để khớp các hóa đơn của nhà cung cấp được tạo tự động.
   -   Nếu bạn là pháp nhân cho vay, đối với mỗi pháp nhân vay, hãy chọn danh mục dự án mặc định cho từng loại giao dịch. Danh mục dự án được sử dụng cho cấu hình thuế khi danh mục được lập hóa đơn trong các giao dịch liên công ty chỉ tồn tại ở pháp nhân vay. Bạn có thể chọn tích lũy doanh thu đối với các giao dịch liên công ty. Khoản tích lũy này được thực hiện khi các giao dịch được đăng, sau đó, khoản này sẽ được đảo ngược khi hóa đơn liên công ty được đăng.

3. Bấm vào **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Giá** &gt; **Giá chuyển nhượng**.
4. Chọn đơn vị tiền tệ, loại giao dịch và mô hình giá chuyển nhượng. Đơn vị tiền tệ được sử dụng trên hóa đơn là đơn vị tiền tệ được đặt cấu hình trong bản ghi khách hàng cho pháp nhân vay ở pháp nhân cho vay. Đơn vị tiền tệ được sử dụng để khớp các mục trong bảng giá chuyển nhượng.
5. Bấm vào **Sổ cái** &gt; **Thiết lập đăng** &gt; **Kế toán liên công ty** và thiết lập mối quan hệ giữa USSI và FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Ví dụ 2: Tạo và đăng bảng chấm công liên công ty
Pháp nhân cho vay USSI phải tạo và đăng bảng chấm công cho một dự án từ pháp nhân vay FRSI. Có hai điểm nhập cho các bước cần thiết cho nhiệm vụ này.

| Bước | Điểm nhập                                                                       | Mô tả                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Quản lý dự án và kế toán** &gt; **Bảng chấm công** &gt; **Tất cả bảng chấm công** | Tạo bảng chấm công mới. Trên dòng bảng chấm công, ở trường **Pháp nhân**, chọn **FRSI**. Ở trường **ID dự án**, chọn dự án trong FRSI. Nhập số giờ cho mỗi ngày trong tuần. |
| B    | Trang **Bảng chấm công**                                                                | Sau khi quy trình làm việc chạy, hãy đăng bảng chấm công và ghi lại số chứng từ.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Ví dụ 3: Tạo và đăng hóa đơn của nhà cung cấp liên công ty
Pháp nhân cho vay USSI phải tạo và đăng hóa đơn của nhà cung cấp liên công ty cho một dự án từ pháp nhân vay FRSI. Hóa đơn của nhà cung cấp này biểu thị chi phí và nhân công thuê ngoài do các nhà cung cấp phân phối mà USSI phải thanh toán. Có hai điểm nhập cho các bước cần thiết cho nhiệm vụ này.

| Bước | Điểm nhập                                                                                      | Mô tả                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Tài khoản phải trả** &gt; **Hóa đơn** &gt; **Hóa đơn của nhà cung cấp đang mở** &gt; **Hóa đơn mới của nhà cung cấp** | Tạo hóa đơn mới của nhà cung cấp và nhập các dịch vụ đã được mua cho dự án của FRSI.                                                                                                                                                                                  |
| B    | Trang **Hóa đơn của nhà cung cấp**                                                                      | Nhập các dòng đại diện cho dịch vụ được thuê làm bên ngoài thay mặt cho FRSI. Trên FastTab **Chi tiết dòng**, trên tab **Dự án** cho dòng hóa đơn, ở trường **Công ty dự án**, nhập **FRSI**. Nhập dự án và thông tin tương ứng. Sau đó, đăng hóa đơn của nhà cung cấp. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Ví dụ 4: Tạo và đăng hóa đơn liên công ty
Pháp nhân cho vay USSI phải tạo và đăng hóa đơn liên công ty. Có hai điểm nhập cho các bước cần thiết cho nhiệm vụ này.

| Bước | Điểm nhập                                                                                             | Mô tả                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Quản lý dự án và kế toán** &gt; **Hóa đơn dự án** &gt; **Hóa đơn cho khách hàng liên công ty**  | Bấm vào **Mới** để mở trang **Tạo hóa đơn liên công ty**.                                                                                  |
| B    | **Quản lý dự án và kế toán** &gt; **Hóa đơn dự án** &gt; **Hóa đơn cho khách hàng liên công ty** | Trên trang **Tạo hóa đơn liên công ty**, nhập pháp nhân, chỉ định giao dịch cần đưa vào, rồi bấm vào **Tìm kiếm**. |
| C    | **Quản lý dự án và kế toán** &gt; **Hóa đơn dự án** &gt; **Hóa đơn cho khách hàng liên công ty** | Chọn các giao dịch cần lập hóa đơn hoặc bấm vào **Chọn tất cả** để lập hóa đơn cho tất cả các giao dịch trong danh sách, rồi bấm vào **OK**.                  |
| D    | Trang **Hóa đơn liên công ty**                                                                       | Đề xuất hóa đơn cho khách hàng liên công ty được hiển thị.                                                                                             |
| E    | Trang **Hóa đơn liên công ty**                                                                       | Bấm vào **Đăng**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Ví dụ 5: Đăng hóa đơn của nhà cung cấp và lập hóa đơn cho khách hàng
Khi pháp nhân cho vay USSI đăng hóa đơn cho khách hàng liên công ty, một hóa đơn của nhà cung cấp tương ứng, đang chờ xử lý sẽ được tạo ở pháp nhân vay FRSI. Sau khi hóa đơn của nhà cung cấp này được đăng, FRSI cũng lập hóa đơn cho khách hàng dự án theo số giờ mà USSI đã nhập. Có ba điểm nhập cho các bước cần thiết cho nhiệm vụ này.

| Bước | Điểm nhập                                                                                        | Mô tả                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Tài khoản phải trả** &gt; **Hóa đơn** &gt; **Hóa đơn của nhà cung cấp đang chờ xử lý**                            | Xem lại hóa đơn để bảo đảm trong đó đã có các giá trị trên bảng chấm công, rồi đăng hóa đơn của nhà cung cấp.                  |
| B    | **Quản lý dự án và kế toán** &gt; **Hóa đơn dự án** &gt; **Đề xuất hóa đơn dự án** | Tạo hóa đơn dự án mới cho dự án và xác minh rằng các giao dịch theo giờ đã đăng sẽ xuất hiện.            |
| C    | Trang **Hóa đơn dự án**                                                                       | Chọn hóa đơn dự án, rồi bấm vào **Xem chi tiết** để xem xét chi phí và số tiền bán hàng. Sau đó, đăng hóa đơn. |


Để biết thêm thông tin, hãy xem [Đặt cấu hình việc lập hóa đơn dự án liên công ty](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]