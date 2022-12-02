---
title: Đăng ký gói xem trước – bản đơn giản
description: Bài viết này cung cấp thông tin về cách đăng ký và triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410102"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Đăng ký gói xem trước – bản đơn giản 

Bài viết này giải thích cách đăng ký ưu đãi dùng thử và triển khai ưu đãi - triển khai bản đơn giản Dynamics 365 Project Operations cho lập hóa đơn ước giá.

> [!NOTE]
> Quá trình này sẽ thay đổi trong các phiên bản sắp tới của Project Operations.

## <a name="prerequisites"></a>Điều kiện tiên quyết
- Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure. Bạn có thể tạo đối tượng thuê trong lần đổi ưu đãi đầu tiên.

> [!IMPORTANT]
> Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này. Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.
> 
> Đối tượng thuê chỉ có thể sử dụng bản dùng thử một lần. Bạn chỉ có thể chạy bản dùng thử một lần. Chúng tôi khuyên bạn nên tạo đối tượng thuê mới cho mục đích dùng thử.

### <a name="dynamics-365-project-operations-trial"></a>Dùng thử Dynamics 365 Project Operations 

Trước khi bạn bắt đầu, hãy đảm bảo rằng bạn đăng nhập trên trình duyệt bằng tài khoản cơ quan của người dùng trong đối tượng thuê nơi bạn muốn dùng bản xem trước Project Operations.

1. Đi đến [Bản dùng thử Project Operations](https://aka.ms/try-po) để đổi mã ưu đãi đầu tiên, **Dynamics 365 Project Operations**.
2. Xác nhận đơn hàng của bạn.

  Bạn sẽ thấy ưu đãi xác nhận đã được đổi thành công.

## <a name="assign-licenses"></a>Gán giấy phép

> [!IMPORTANT]
> Bạn sẽ cần quyền truy cập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.


1. Chuyển đến trung tâm quản trị [Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.
2. Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.
3. Xác minh rằng giấy phép **Dynamics 365 Project Operations** được chọn. 
4. Chọn **Lưu thay đổi**.

## <a name="create-a-new-dataverse-environment"></a>Tạo môi trường Dataverse mới

1. Cung cấp môi trường triển khai Project Operations Dataverse mới bằng cách làm theo các hướng dẫn trong bài viết [Mô hình triển khai Dataverse](lite-deployment.md). Khi bạn chọn loại môi trường, hãy bảo đảm sử dụng **Bản dùng thử (Dựa trên gói đăng ký)**.

  ![Môi trường mới.](./media/19CreateEnvironment.png)

2. Chọn mục thiết đặt **Bật ứng dụng Dynamics 365** và để trống mục **Tự động triển khai các ứng dụng này**.  
3. Chọn **Lưu** để tạo môi trường.

  ![Thêm cơ sở dữ liệu.](./media/20CreateEnvironment1.png)

4. Sau khi tạo môi trường, hãy cài đặt giải pháp **Microsoft Dynamics 365 Project Operations**. 

![Cài đặt giải pháp.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Thiết lập dữ liệu demo

Thiết lập dữ liệu demo theo các hướng dẫn trong bài viết [Áp dụng dữ liệu cấu hình và thiết lập demo](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
