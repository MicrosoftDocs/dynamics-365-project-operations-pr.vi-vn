---
title: Thêm gói đăng ký Azure vào dự án LCS
description: Chủ đề này cung cấp thông tin về cách kết nối gói đăng ký Azure của bạn với dự án LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175827"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Thêm gói đăng ký Azure vào dự án LCS

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Môi trường được lưu trữ trên đám mây phải được triển khai bằng cách sử dụng đăng ký Azure hiện có. Chủ đề này sẽ giải thích cách kết nối gói đăng ký Azure hiện có của bạn với dự án LCS. 

## <a name="grant-admin-consent"></a>Cấp sự đồng ý của quản trị viên

1. Trong dự án LCS, trong phần **Môi trường**, hãy chọn **cài đặt Microsoft Azure**.

![Thiết đặt Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Trên trang **Thiết đặt dự án**, trên tab **Trình kết nối Azure**, hãy chọn **Cho phép**. Thao tác này cho phép các môi trường được triển khai cho dự án này.

![Trình kết nối Azure](./media/2AzureConnectors.png)

3. Chọn **Cho phép** một lần nữa để cung cấp sự đồng ý của quản trị viên.

![Cấp sự đồng ý của quản trị viên](./media/3GrantAdminConsent.png)

4. Chấp nhận yêu cầu quyền.

![Chấp nhận yêu cầu quyền](./media/4AcceptPermissionRequest.png)

Sự định quyền hiện đã hoàn tất. 

![Định quyền thành công](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Cung cấp quyền truy cập vào Dịch vụ triển khai Dynamics cho đăng ký Azure của bạn

1. Chuyển đến [thanh toán Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) rồi chọn gói đăng ký của bạn. Dịch vụ triển khai Dynamics cần truy cập vào gói đăng ký này để có thể triển khai các môi trường.

![Thông tin chi tiết về Đăng ký Azure](./media/6AzureSubscription.png)

2. Chọn **Kiểm soát truy cập (IAM)** trong ngăn điều hướng, sau đó chọn **Thêm gán vai trò**.
3. Trong thanh trượt ở bên phải, hãy chọn **Vai trò người đóng góp** và trong danh sách được cung cấp, hãy tìm và chọn **Dịch vụ triển khai Dynamics**. 
4. Chọn **Lưu**.

![Quyền truy cập vào gói đăng ký](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Thêm trình kết nối gói đăng ký vào dự án LCS

1. Trong dự án LCS của bạn, trên trang **cài đặt Microsoft Azure**, hãy chọn **Thêm** để thêm một trình kết nối mới.
2. Nhập ID đăng ký Azure của bạn. Bạn có thể tìm thấy ID đăng ký Azure của mình trong [Cổng thông tin Azure](https://ms.portal.azure.com/), ở phần  **Cài đặt**  ở phía dưới bên trái của màn hình.
3. Trong trường **Đặt cấu hình để sử dụng Azure Resource Manager**, hãy chọn **Có**.
4. Đảm bảo Miền của đối tượng thuê AAD đăng ký của Azure khớp với đăng ký Azure sở hữu miền mà bạn đang sử dụng rồi chọn **Tiếp theo**.
5. Trên màn hình **Thiết lập Microsoft Azure**, hãy chọn **Tiếp theo** để xác nhận. Nếu bạn gặp lỗi trên màn hình này, hãy quay lại phần [Cấp quyền truy cập vào Dịch vụ triển khai Dynamics cho đăng ký Azure](#provide) trong chủ đề này và đảm bảo rằng bạn đã hoàn thành tất cả các bước.
6. Tải Chứng chỉ quản lý Azure xuống một thư mục cục bộ trên máy tính của bạn, sau đó tải nó lên Cổng thông tin quản lý Azure bằng cách truy cập vào phần **Cài đặt** > **Chứng chỉ quản lý**. Chứng chỉ này sẽ cho phép LCS thay mặt bạn kết nối với Azure. Bạn có thể bỏ qua bước này nếu người dùng của bạn có quyền truy cập vào đăng ký.
7. Chọn  **Tiếp theo**.
8. Chọn vùng Azure để triển khai và chọn một trung tâm dữ liệu gần nơi bạn định sử dụng hệ thống này.
9.  Chọn  **Kết nối**.

Bạn đã kết nối thành công đăng ký Azure của mình. Bây giờ bạn có thể triển khai môi trường Dynamics 365 Finance được lưu trữ trên đám mây.


