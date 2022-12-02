---
title: Đăng ký bản dùng thử Project Operations
description: Bài viết này cung cấp thông tin về cách triển khai một bản dùng thử của Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 60790d83d5fcc8c75fef8eac2877d1ca14a761f2
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528046"
---
# <a name="sign-up-for-project-operations-trials"></a>Đăng ký bản dùng thử Project Operations 

_**Áp dụng đối với:** Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho, triển khai Lite - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_ 



Bài viết này giải thích cách đăng ký nhận ưu đãi dành cho đối tác xem trước và triển khai môi trường Dynamics 365 Project Operations.

Với bản dùng thử Project Operations mới, bạn có thể tự động triển khai bất kỳ tình huống triển khai nào trong ba trường hợp triển khai được hỗ trợ bằng cách hoàn thành bảng câu hỏi đề xuất phương pháp triển khai tốt nhất. Bài viết này cung cấp thông tin về cách thức:

- Đổi ưu đãi dùng thử của bạn.
- Bắt đầu cấp phép.
- Đặt cấu hình ghi kép.
- Tìm hiểu thêm về Project Operations. 

Bảng sau đây phác thảo các chi tiết của ưu đãi dùng thử mới.

| **Mặt hàng ưu đãi**               | **Details**                                  |
|------------------------------|----------------------------------------------|
| Loại ưu đãi                   | Loại ưu đãi này là Quản trị khách hàng tiềm năng nên cần phải có quản trị viên đối tượng thuê để đổi. |
| Sử dụng ưu đãi                    | Một lần cho mỗi đối tượng thuê                          |
| Thời hạn ưu đãi               | 30 ngày                             |
| Số lần đổi cho mỗi đối tượng thuê       | 1                                            |
| Phần mở rộng                    | 1 phần mở rộng, 30 ngày               |
| Số lượng môi trường dùng thử | 3                                            |


## <a name="admin-trial-details"></a>Thông tin chi tiết về bản dùng thử của quản trị viên
Bảng sau liệt kê các chi tiết về bản dùng thử và cách chúng áp dụng cho từng loại triển khai.

| **Mục**                      | **Bản đơn giản**                                     | **Nguyên vật liệu không nhập kho** | **Nguyên vật liệu trữ kho** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Đã cung cấp dữ liệu thiết lập           | Có                                          | Có                       | Có (USSI)            |
| Dữ liệu giao dịch            | No                                           | No                        | No                    |
| Thời gian cấp phép tính bằng phút  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Điều kiện tiên quyết
Để triển khai bản dùng thử Dynamics 365 Project Operations, các điều kiện tiên quyết sau đây là bắt buộc.

- Đăng ký [Dynamics 365 Project Operations - Bản dùng thử xem trước](https://www.aka.ms/try-po).
- Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure.

> [!IMPORTANT]
> Chỉ một người trong tổ chức, quản trị viên đối tượng thuê, cần thực hiện nhiệm vụ này. Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Bản dùng thử xem trước 

Trước khi bạn bắt đầu, hãy đăng nhập vào trình duyệt bằng tài khoản công việc người dùng trong đối tượng thuê nơi bạn muốn xem trước Project Operations.

1. Đổi mã ưu đãi đầu tiên **Dynamics 365 Project Operations - Bản dùng thử xem trước** bằng cách dán mã này vào URL trên trình duyệt.

    ![Đổi ưu đãi](./media/16RedeemFirstOfferNew.png)

2. Xác nhận đơn hàng của bạn.

    ![Xác nhận đơn hàng](./media/17ConfirmOrderNew.png)

  Bạn sẽ thấy ưu đãi xác nhận đã được đổi thành công.

   ![Xác nhận](./media/18OrderConfirmationNew.png)

  Bạn sẽ được chuyển đến trung tâm quản trị [Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Bảng câu hỏi và cấp phép

1.  Chuyển tới trung tâm quản trị [Power Platform](https://admin.powerplatform.com/projectoperationstrial) và hoàn thành bảng câu hỏi.  
2.  Xem lại loại triển khai được đề xuất và chọn **Bắt đầu thiết lập** để bắt đầu cấp phép.
3.  Xem xét các điều khoản và điều kiện, sau đó chọn **Bắt đầu**.

   Sau khi bắt đầu cấp phép, bạn được chuyển đến danh sách môi trường trong trung tâm quản trị Power Platform. Trong quá trình cấp phép, trạng thái môi trường của bạn là **Đang chuẩn bị phiên bản**.
 
  Khi quá trình cấp phép hoàn tất, trạng thái môi trường của bạn là **Sẵn sàng**. Quá trình cấp phép môi trường bao gồm việc triển khai dữ liệu demo.
 
4.  Chọn URL Microsoft Dataverse tương ứng và URL ứng dụng tài chính và hoạt động để xác thực việc triển khai.

## <a name="configuring-dual-write"></a>Đặt cấu hình ghi kép
- Để định cấu hình vai trò bảo mật cho ghi kép, hãy xem [Cập nhật các tùy chọn cài đặt bảo mật trong Project Operations trong Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Để truy cập cấu hình ghi kép, điều hướng đến phiên bản tài chính và hoạt động, sau đó điều hướng đến **Quản lý dữ liệu** > **Ghi kép**.
- Để định cấu hình ánh xạ ghi kép, hãy xem [Chạy ánh xạ ghi kép trong Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Gán giấy phép

Bạn sẽ cần quyền truy cập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.

1. Chuyển tới trung tâm quản trị [Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.

   ![Trang chủ trung tâm quản trị](./media/14AdminPortal.png)

2. Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.

   ![Gán giấy phép](./media/15AssignLicenses.png)

3. Xác minh rằng giấy phép Bản xem trước **Dynamics 365 Project Operations** đã được chọn, rồi chọn **Lưu thay đổi**.

## <a name="additional-resources"></a>Tài nguyên bổ sung

Các tài nguyên sau cung cấp hướng dẫn hữu ích khi bạn bắt đầu hành trình của mình với Project Operations:

- [Chuỗi video -Tổng quan về Project Operations, thông tin chi tiết về tính năng và lộ trình](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/training/modules/examine-dynamics-365-project-operations/)
- [Xác định loại triển khai của bạn](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Các câu hỏi thường gặp

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Nếu tôi cần có ALM hoặc ELM cho môi trường ứng dụng tài chính và hoạt động của mình thì sao?

- Đối với các đối tác yêu cầu khả năng quản lý vòng đời môi trường đầy đủ, hãy xem [Yêu cầu Giấy phép Hộp cát Đối tác](https://experience.dynamics.com/requestlicense) để xem lại ưu đãi mới dành cho đối tác. 
- Đối với các đối tác tìm kiếm thêm thông tin về Quyền sử dụng nội bộ, hãy xem [Lợi ích phần mềm và đám mây Quyền sử dụng nội bộ (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Tôi có thể gia hạn thời gian dùng thử của mình hơn 30 ngày không?
Để gia hạn thời gian dùng thử của bạn, hãy hoàn thành các bước sau.

1. Trong Trung tâm quản trị **Microsoft 365**, hãy chuyển đến phần **Thanh toán** > **Sản phẩm của bạn**.
2. Chọn **Dynamics 365 Project Operations (CE) - Bản dùng thử xem trước**.
3. Bên dưới **Ngày hết hạn**, chọn **Ngày gia hạn**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Tôi có thể nâng cấp từ triển khai bản đơn giản lên triển khai kịch bản dựa trên nguồn lực/hàng không nhập kho không?
Hiện tại, không có sự hỗ trợ nào để nâng cấp một môi trường từ bản đơn giản lên triển khai dựa trên hàng không nhập kho.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Tôi có thể truy cập Lifecycle Services (LCS) cho môi trường Tài chính của mình không?  
Không. Đối với những bản dùng thử này, việc triển khai được xử lý thông qua Trung tâm quản trị Power Platform. Quyền truy cập vào môi trường Tài chính bị hạn chế.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Tôi có thể cài đặt bản dùng thử của mình trên một môi trường hiện có không?
Nếu bạn hiện có một môi trường, bạn sẽ được phép cài đặt triển khai bản đơn giản trên môi trường Dataverse bán hàng hiện có từ Trung tâm quản trị Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
