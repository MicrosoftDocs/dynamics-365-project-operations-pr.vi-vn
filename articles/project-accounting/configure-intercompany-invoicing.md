---
title: Đặt cấu hình hóa đơn liên công ty
description: Chủ đề này cung cấp thông tin và ví dụ về cách thiết lập cấu hình hóa đơn liên công ty cho các dự án.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09bbd1bf640cc86b16afb8c2b824329b92f833df836e9313491d57a2f1646440
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994077"
---
# <a name="configure-intercompany-invoicing"></a>Đặt cấu hình hóa đơn liên công ty

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Hãy hoàn thành các bước sau để thiết lập hóa đơn liên công ty cho các dự án trong Dynamics 365 Project Operations. Giao dịch liên công ty là các giao dịch chi phí và thời gian trong hợp đồng dự án, thuộc về một công ty hoặc đơn vị tổ chức, trong khi nguồn lực trên hợp đồng dự án lại là một phần của công ty hoặc đơn vị tổ chức khác.

## <a name="example-configure-intercompany-invoicing"></a>Ví dụ: Đặt cấu hình hóa đơn liên công ty

Trong ví dụ sau, Contoso Robotics USA (USPM) là pháp nhân đi vay và Contoso Robotics UK (GBPM) là pháp nhân cho vay. 

1. **Đặt cấu hình kế toán liên công ty giữa các pháp nhân**. Mỗi cặp pháp nhân đi thuê và cho thuê phải được đặt cấu hình trên Sổ cái chung của trang [Kế toán liên công ty](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. Trong Dynamics 365 Finance, hãy đi tới **Sổ cái chung** > **Thiết lập đăng** > **Kế toán liên công ty**. Tạo một bản ghi chứa những thông tin sau:

        - **Công ty bắt nguồn** = **GBPM**
        - **Công ty đích** = **USPM**

2. **Đặt cấu hình mối quan hệ giao dịch giữa các pháp nhân**. Bản ghi khách hàng đại diện cho pháp nhân đi thuê phải được tạo trong pháp nhân cho thuê. Bản ghi nhà cung cấp đại diện cho pháp nhân cho thuê phải được tạo trong pháp nhân đi thuê.

     1. Trong phần Tài chính, hãy chọn pháp nhân **GBPM**.
     2. Đi đến **Khoản phải thu** > **Khách hàng** > **Tất cả khách hàng**. Tạo bản ghi mới cho pháp nhân **USPM**.
     3. Mở rộng **Tên**, lọc bản ghi theo **Loại** rồi chọn **Pháp nhân**. 
     4. Tìm và chọn bản ghi khách hàng cho **Contoso Robotics USA (USPM)**.
     5. Chọn **Dùng kết quả khớp**. 
     6. Chọn nhóm khách hàng **50 – Khách hàng liên công ty** rồi lưu bản ghi.
     7. Chọn pháp nhân **USPM**.
     8. Đi đến **Khoản phải trả** > **Nhà cung cấp** > **Tất cả nhà cung cấp**. Tạo bản ghi mới cho pháp nhân **GBPM**.
     9. Mở rộng **Tên**, lọc bản ghi theo **Loại** rồi chọn **Pháp nhân**. 
     10. Tìm và chọn bản ghi khách hàng cho **Contoso Robotics UK (GBPM)**.
     11. Chọn **Dùng kết quả khớp**, chọn nhóm nhà cung cấp rồi lưu bản ghi.
     12. Trong bản ghi nhà cung cấp, hãy chọn **Chung** > **Thiết lập** > **Liên công ty**.
     13. Trên tab **Quan hệ giao dịch**, hãy đặt **Đang hoạt động** thành **Có**.
     14. Đặt trường **Công ty khách hàng** thành **GBPM** và trong phần **Hồ sơ tài khoản của tôi**, hãy chọn hồ sơ khách hàng mà bạn đã tạo trước đó trong quy trình.

3. **Cài đặt các tùy chọn liên công ty trong phần quản lý dự án và các tham số kế toán**. 

    1. Chọn pháp nhân **USPM** rồi đi đến **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và các tham số kế toán**.
    2. Trên tab **Liên công ty**, hãy chọn danh mục mua sắm phù hợp với các hóa đơn nhà cung cấp được tạo tự động.
    3. Trong phần **Danh mục mặc định**, hãy chọn **Nguồn lực liên công ty**.
    4. Chọn pháp nhân **GBPM** rồi đi đến **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và các tham số kế toán**.
    5. Trên tab **Liên công ty**, hãy chọn danh mục dự án mặc định cho từng loại giao dịch. Danh mục dự án được sử dụng cho cấu hình thuế khi danh mục được lập hóa đơn trong các giao dịch liên công ty chỉ tồn tại ở pháp nhân vay. Bạn có thể chọn tích lũy doanh thu đối với các giao dịch liên công ty. Tích lũy xảy ra khi các giao dịch được đăng thông qua nhật ký Tích hợp Project Operations trong pháp nhân cho thuê. Nhật ký sẽ đảo ngược khi hóa đơn liên công ty được đăng.
    6. Trong nhóm **Khi cho thuê nguồn lực**, hãy chọn **...** > **Mới**. 
    7. Trong lưới này, hãy chọn những thông tin sau:

          - **Pháp nhân đi thuê** = **USPM**
          - **Tích lũy doanh thu** = **Có**
          - **Danh mục chấm công mặc định** = **Mặc định – Giờ**
          - **Danh mục chi phí mặc định** = **Mặc định – chi phí**

4. **Thiết lập tài khoản chi phí và doanh thu liên công ty trong phần thiết lập đăng của Sổ cái**. Tài khoản doanh thu liên công ty ghi có khi hóa đơn khách hàng liên công ty được đăng trong pháp nhân cho thuê. Tài khoản chi phí liên công ty ghi nợ khi hóa đơn nhà cung cấp đang chờ xử lý trùng khớp được đăng trong pháp nhân cho thuê. Những tài khoản này được thiết lập trong các pháp nhân tương ứng. 
      
     1. Trong phần Tài chính, hãy chọn pháp nhân đi thuê là **USPM**. 
     2. Đi tới **Quản lý dự án và kế toán** > **Thiết lập** > **Đăng** > **Thiết lập đăng trên Sổ cái**. 
     3. Trên tab **Tài khoản chi phí**, trong phần **Loại tài khoản sổ cái**, hãy chọn **Chi phí liên công ty**. Tạo một bản ghi mới chứa những thông tin sau:
      
        - **Pháp nhân cho thuê** = **GBPM**
        - **Tài khoản chính** = Chọn tài khoản chính cho chi phí liên công ty. Thiết lập này là bắt buộc. Thiết lập này được sử dụng cho các dòng liên công ty trong Tài chính, nhưng không sử dụng cho các dòng liên công ty liên quan đến dự án. Lựa chọn này không có tác động xuôi tuyến. 
        
     4. Chọn pháp nhân cho thuê là **GBPM**. 
     5. Đi tới **Quản lý dự án và kế toán** > **Thiết lập** > **Đăng** > **Thiết lập đăng trên Sổ cái**. 
     6. Trên tab **Tài khoản doanh thu**, trong phần **Loại tài khoản sổ cái**, hãy chọn **Doanh thu liên công ty**. Tạo một bản ghi mới chứa những thông tin sau:

        - **Pháp nhân đi thuê** = **USPM**
        - **Tài khoản chính** = Chọn tài khoản chính cho doanh thu liên công ty. Thiết lập này là bắt buộc. Thiết lập này được sử dụng cho các dòng liên công ty trong Tài chính, nhưng không sử dụng cho các dòng liên công ty liên quan đến dự án. Lựa chọn này không có tác động xuôi tuyến. 

5. **Thiết lập giá chuyển nhượng lao động**. Giá chuyển nhượng lao động được đặt cấu hình trong Project Operations trên Dataverse. Đặt cấu hình [tỷ lệ chi phí lao động](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) và [tỷ lệ hóa đơn lao động](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) cho hóa đơn liên công ty. Giá chuyển nhượng không hỗ trợ các giao dịch chi phí liên công ty. Giá bán đơn vị liên tổ chức sẽ luôn có cùng giá trị như giá chi phí đơn vị cung ứng nguồn lực.

      Chi phí nguồn lực của nhà phát triển trong Contoso Robotics UK là 88 GBP mỗi giờ. Contoso Robotics UK sẽ lập hóa đơn 120 USD cho Contoso Robotics USA 120 USD với mỗi giờ nguồn lực này hoạt động trên các dự án tại Hoa Kỳ. Contoso Robotics USA sẽ lập hóa đơn 200 USD cho khách hàng Adventure Works với công việc do nguồn lực nhà phát triển Contoso Robotics UK thực hiện.

      1. Trong Project Operations trên Dataverse, hãy đi tới **Bán hàng** > **Bảng giá**. Tạo một bảng giá chi phí mới được gọi là **Tỷ lệ chi phí Contoso Robotics UK.** 
      2. Trong bảng chi phí, hãy tạo một bản ghi chứa những thông tin sau:
         - **Vai trò** = **Nhà phát triển**
         - **Chi phí** = **88 GBP**
      3. Chuyển đến phần **Cài đặt** > **Đơn vị tổ chức** và đính kèm bảng giá chi phí này vào đơn vị tổ chức của **Contoso Robotics UK**.
      4. Đi tới **Bán hàng** > **Bảng giá**. Tạo một bảng giá chi phí mới được gọi là **Tỷ lệ chi phí Contoso Robotics USA**. 
      5. Trong bảng chi phí, hãy tạo một bản ghi chứa những thông tin sau:
          - **Vai trò** = **Nhà phát triển**
          - **Công ty cung cấp nguồn lực** = **Contoso Robotics UK**
          - **Chi phí** = **120 USD**
      6. Chuyển đến phần **Cài đặt** > **Đơn vị tổ chức** và đính kèm bảng giá chi phí **tỷ lệ chi phí Contoso Robotics USA** vào đơn vị tổ chức của **Contoso Robotics USA**.
      7. Đi tới **Bán hàng** > **Bảng giá**. Tạo bảng giá bán hàng có tên **Tỷ lệ hóa đơn Adventure Works**. 
      8. Trong bảng giá bán, hãy tạo một bản ghi chữa những thông tin sau:
          - **Vai trò** = **Nhà phát triển**
          - **Công ty cung cấp nguồn lực** = **Contoso Robotics UK**
          - **Mức thu** = **200 USD**
      9. Chuyển đến **Bán hàng** > **Hợp đồng dự án** rồi đính kèm bảng giá **tỷ lệ hóa đơn Adventure Works** vào bảng giá dự án Adventure Works của hợp đồng dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
