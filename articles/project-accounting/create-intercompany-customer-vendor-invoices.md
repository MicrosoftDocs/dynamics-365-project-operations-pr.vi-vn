---
title: Lập hóa đơn cho nhà cung cấp và khách hàng liên công ty
description: Bài viết này cung cấp thông tin về cách tạo hóa đơn khách hàng liên công ty và hóa đơn nhà cung cấp.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd7696c32760423c876362ca3ae0ee2c7b5716e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916406"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Lập hóa đơn cho nhà cung cấp và khách hàng liên công ty

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Kế toán viên dự án của pháp nhân cho thuê sẽ tạo một hóa đơn khách hàng liên công ty đối với các chi phí dự án được chuyển nhượng cho pháp nhân đi thuê. Sau khi hóa đơn khách hàng liên công ty được phê duyệt và đăng, pháp nhân cho thuê sẽ gửi hóa đơn liên công ty cho pháp nhân đi thuê.

Kế toán viên dự án của pháp nhân cho thuê có thể thiếp lập quy trình để tạo hàng loạt hóa đơn liên công ty theo định kỳ. Kế toán viên dự án xác định tiêu chí, chẳng hạn như dự án cụ thể, để tạo hàng loạt hóa đơn liên công ty.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Tạo thủ công hóa đơn khách hàng liên công ty cho các giao dịch dự án 

Dùng quy trình này để tạo thủ công hóa đơn khách hàng liên công ty cho các giao dịch dự án. Tìm kiếm số giờ mà nhân viên đăng lên các dự án của pháp nhân đi thuê, cũng như chi phí mà pháp nhân của bạn đã bỏ ra thay mặt pháp nhân đi thuê. Bạn có thể tìm kiếm theo tên pháp nhân, số hợp đồng của dự án, số dự án, khoảng ngày hoặc kết hợp bất kỳ những tùy chọn này. Trong kết quả tìm kiếm, hãy chọn các giao dịch cần thêm vào hóa đơn liên công ty. 

Các bước sau đây cần phải được thực hiện trong pháp nhân cho vay. 

1. Trong Dynamics 365 Finance, hãy đi tới **Quản lý dự án và kế toán** > **Hóa đơn dự án** > **Hóa đơn khách hàng liên công ty**. Trong trang danh sách **Hóa đơn khách hàng liên công ty**, trên Ngăn hành động, hãy chọn **Mới**.
2. Trên trang **Tạo hóa đơn liên công ty**, trong trường **Pháp nhân**, hãy chọn một pháp nhân đi thuê.
3. Không bắt buộc: Nhập hợp đồng dự án và mã số dự án cụ thể.
4. Thu hẹp phạm vi tìm kiếm bằng cách chọn khoảng ngày. Nhập ngày cụ thể trong các trường **Ngày bắt đầu** và **Ngày kết thúc**. Kết quả tìm kiếm sẽ chỉ hiển thị những giao dịch liên công ty được đăng trong khoảng ngày này.
5. Đặt **Tham số dòng nhật ký nâng cao của dự án** thành **Có** rồi chọn **Tìm kiếm**.
6. Trong kết quả tìm kiếm, hãy chọn các giao dịch bạn muốn thêm vào bản đề xuất hóa đơn liên công ty, sau đó chọn **OK**.
7. Trên trang **Hóa đơn khách hàng liên công ty**, các giao dịch dự án liên công ty mà bạn đã chọn từ kết quả tìm kiếm sẽ hiển thị. Để sửa đổi các giao dịch trước khi gửi hóa đơn cho pháp nhân đi thuê, hãy làm như sau:
  
    1. Trên trang **Hóa đơn khách hàng liên công ty**, hãy mở chi tiết hóa đơn rồi chọn **Thêm dòng**.
    2. Để xóa một dòng, hãy chọn dòng đó rồi bấm vào **Xóa**.
    3. Xem nhận xét, lý do, kích thước tài chính và thông tin khác về một dòng đã chọn trên chi tiết dòng hóa đơn.
    
8. Để đăng hóa đơn khách hàng liên công ty, trên Ngăn Hành động, hãy chọn **Đăng**.

> [!NOTE]
> Nếu tổ chức của bạn yêu cầu các hóa đơn liên công ty phải được xem xét trước khi đăng, thì một quản trị viên hệ thống có thể thiết lập quy trình dành cho hóa đơn liên công ty. Nếu không có quy trình dành cho hóa đơn liên công ty, bạn không thể đăng hóa đơn liên công ty.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Tạo tác vụ hàng loạt cho hóa đơn liên công ty

Bạn có thể tạo cùng lúc nhiều hóa đơn liên công ty cho tất cả pháp nhân đi thuê. Ví dụ: bạn có thể dùng chức năng tìm kiếm để tìm kiếm mọi giao dịch mà những nhân viên được cho thuê đã đăng và có liên quan đến các dự án do các pháp nhân khác quản lý. Sau đó, đối với mỗi pháp nhân đi thuê, bạn có thể tạo một hóa đơn liên công ty cho các giao dịch có trong kết quả tìm kiếm.

1. Đi tới **Quản lý dự án và kế toán** > **Định kỳ** > **Hóa đơn dự án** > **Tạo hóa đơn khách hàng liên công ty**.
2. Trên trang **Tạo hóa đơn khách hàng liên công ty**, trong trường **Công ty**, chọn pháp nhân cần lập hóa đơn. Nếu bạn không chọn công ty nào, mọi giao dịch khớp với tiêu chí tìm kiếm sẽ hiển thị cho tất cả pháp nhân cho thuê.
3. Trong phần **Tạo một hóa đơn theo**, hãy chọn xem bạn muốn tạo hóa đơn cho các giao dịch liên công ty dựa trên dự án hay dựa trên pháp nhân đi thuê.
4. Không bắt buộc: Để chọn dự án hoặc mã số dự án cụ thể cần tạo hóa đơn liên công ty, hãy bấm vào **Chọn**. Trên trang **Truy vấn**, trong trường **Tiêu chí**, hãy chọn hợp đồng dự án, mã số dự án hoặc cả hai rồi bấm vào **OK**.
5. Trên tab **Hàng loạt**, hãy thiết lập quy trình để tạo hàng loạt hóa đơn liên công ty theo định kỳ. Để biết thêm thông tin, hãy xem [Gửi tác vụ xử lý hàng loạt từ biểu mẫu](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Để đăng hóa đơn liên công ty, trên Ngăn Hành động, hãy chọn **Đăng**.

> [!NOTE]
> Nếu tổ chức của bạn đặt ra yêu cầu rằng các hóa đơn liên công ty phải được xem xét trước khi đăng, thì một quản trị viên hệ thống có thể thiết lập quy trình dành cho hóa đơn liên công ty. Nếu không có quy trình dành cho hóa đơn liên công ty, bạn không thể đăng hóa đơn liên công ty.

## <a name="post-the-intercompany-vendor-invoice"></a>Đăng hóa đơn nhà cung cấp liên công ty

Kế toán viên dự án của pháp nhân đi thuê có thể xem xét các hóa đơn đang chờ xử lý của nhà cung cấp khi họ đăng hóa đơn khách hàng liên công ty tương ứng. Trong phần Tài chính của pháp nhân đi thuê, hãy chuyển đến **Khoản phải trả** > **Hóa đơn** > **Hóa đơn đang chờ xử lý của nhà cung cấp**. Mã số hóa đơn đang chờ xử lý sẽ khớp với mã số hóa đơn khách hàng liên công ty. Hãy xác minh rằng hóa đơn là chính xác rồi đăng hóa đơn. Thao tác đăng háo đơn nhà cung cấp liên công ty sẽ tạo một sổ cái phụ dự án và một giao dịch sổ cái chung, phản ánh chi phí giao dịch trong pháp nhân đi thuê.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
