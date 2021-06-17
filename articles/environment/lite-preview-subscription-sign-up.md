---
title: Đăng ký gói xem trước - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đăng ký và triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997447"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Đăng ký gói xem trước - bản đơn giản 

Chủ đề này giải thích cách đăng ký ưu đãi của đối tác xem trước và triển khai Dynamics 365 Project Operations lite - xử lý vấn đề lập hóa đơn chiếu lệ.

> [!NOTE]
> Quá trình này sẽ thay đổi trong các phiên bản sắp tới của Project Operations.

## <a name="prerequisites"></a>Điều kiện tiên quyết

- Bạn sẽ nhận được một email mời bạn sử dụng bản xem trước. Bạn có thể yêu cầu xem trước trên [Trang web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure.
- Xem lại tất cả các điều khoản và điều kiện.

## <a name="subscribe"></a>Đăng ký

Khi được phê duyệt [yêu cầu xem trước](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), bạn sẽ nhận được hai ưu đãi của Microsoft qua email. Những ưu đãi này cho phép bạn triển khai Bản xem trước của Project Operations:

- Dynamics 365 Project Operations (CRM) - Bản dùng thử xem trước
- Office 365 Project Operations – Bản dùng thử ở dạng xem trước

> [!IMPORTANT]
> Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này. Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Bản dùng thử xem trước 

Trước khi bạn bắt đầu, hãy đảm bảo rằng bạn đăng nhập trên trình duyệt bằng tài khoản cơ quan của người dùng trong đối tượng thuê nơi bạn muốn dùng bản xem trước Project Operations.

1. Đổi mã ưu đãi đầu tiên **Dynamics 365 Project Operations (CRM) - Bản dùng thử xem trước** bằng cách dán mã này vào URL trên trình duyệt.

![Đổi ưu đãi](./media/16RedeemFirstOfferNew.png)

2. Xác nhận đơn hàng của bạn.
![Xác nhận đơn hàng](./media/17ConfirmOrderNew.png)

Bạn sẽ thấy thông báo xác nhận mã ưu đãi đã được đổi thành công.

![Xác nhận](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Bản dùng thử ở dạng xem trước

Thực hiện các bước tương tự như với mã ưu đãi đầu tiên. Bảo đảm bạn thêm mã ưu đãi thứ hai bằng chính tài khoản người dùng đã dùng với mã ưu đãi đầu tiên.

## <a name="assign-licenses"></a>Gán giấy phép

> [!IMPORTANT]
> Bạn sẽ cần quyền truy nhập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.


1. Chuyển đến [Trung tâm quản trị Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.

![Trang chủ trung tâm quản trị](./media/14AdminPortal.png)

2. Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.

![Gán giấy phép](./media/15AssignLicenses.png)

3. Xác minh rằng đã chọn các giấy phép **Bản xem trước Dynamics 365 Project Operations (CRM)** và **Bản xem trước Office 365 Project Operations**. 
4. Chọn **Lưu thay đổi**.

## <a name="create-a-new-cds-environment"></a>Tạo môi trường CDS mới

1. Cung cấp môi trường triển khai CDS Project Operations mới bằng cách làm theo các hướng dẫn trong chủ đề [Mô hình triển khai CDS](lite-deployment.md). Khi bạn chọn loại môi trường, hãy bảo đảm sử dụng **Bản dùng thử (Dựa trên gói đăng ký)**.
![Môi trường mới](./media/19CreateEnvironment.png)

2. Chọn mục thiết đặt **Bật ứng dụng Dynamics 365** và để trống mục **Tự động triển khai các ứng dụng này**.  
3. Chọn **Lưu** để tạo môi trường.

![Thêm cơ sở dữ liệu](./media/20CreateEnvironment1.png)

4. Sau khi tạo môi trường, hãy cài đặt giải pháp **Microsoft Dynamics 365 Project Operations**. 

![Cài đặt giải pháp](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Cài đặt cấu hình CDS và thiết lập dữ liệu demo

Cài đặt cấu hình CDS và thiết lập dữ liệu demo bằng cách làm theo các hướng dẫn trong chủ đề [Áp dụng dữ liệu cấu hình và thiết lập demo](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]