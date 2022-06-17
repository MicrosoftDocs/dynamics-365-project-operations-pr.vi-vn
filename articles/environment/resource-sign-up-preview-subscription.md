---
title: Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về cách đăng ký và triển khai Hoạt động dự án cho các tình huống dựa trên nguồn cung cấp / không có hàng.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920132"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_



Bài viết này giải thích cách đăng ký ưu đãi dùng thử và triển khai môi trường Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho.

## <a name="prerequisites"></a>Điều kiện tiên quyết
- Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure. Bạn có thể tạo đối tượng thuê trong lần đổi ưu đãi đầu tiên. 
- Việc triển khai môi trường Finance yêu cầu đăng ký Azure hợp lệ sẽ được lập hóa đơn cho mỗi môi trường. Bạn có thể sử dụng đăng ký hiện có của tổ chức mình hoặc sử dụng [Bản dùng thử Azure](https://azure.microsoft.com/free/) để bắt đầu. Môi trường CDS sẽ được cung cấp miễn phí trong khoảng thời gian giới hạn 30 ngày.

> [!IMPORTANT]
> Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này. Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.
> 
> Đối tượng thuê chỉ có thể sử dụng bản dùng thử một lần. Bạn chỉ có thể chạy bản dùng thử một lần. Chúng tôi khuyên bạn nên tạo đối tượng thuê mới cho mục đích dùng thử.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Bản dùng thử xem trước 

Trước khi bạn bắt đầu, hãy đảm bảo rằng bạn đăng nhập trên trình duyệt bằng tài khoản cơ quan của người dùng trong đối tượng thuê nơi bạn muốn dùng bản xem trước Project Operations.

1. Đổi mã ưu đãi đầu tiên, **Dynamics 365 Project Operations** tại đây [Bản dùng thử Project Operations](https://aka.ms/try-po).
2. Xác nhận đơn hàng của bạn.

  Bạn sẽ thấy ưu đãi xác nhận đã được đổi thành công.

### <a name="dynamics-365-finance-preview-trial"></a>Bản dùng thử xem trước Dynamics 365 Finance

Đi đến [Bản dùng thử xem trước Dynamics 365 for Finance](https://aka.ms/trypoche) và thực hiện lại các bước từ phần trước với ưu đãi, Đăng ký môi trường lưu trữ đám mây.  

## <a name="assign-licenses"></a>Gán giấy phép

> [!IMPORTANT]
> Bạn sẽ cần quyền truy cập quản trị vào Cổng thông tin Microsoft 365 của tổ chức bạn để hoàn thành các bước sau.

1. Đi đến [Microsoft 365 trung tâm quản trị](https://portal.office.com/) để chuyển nhượng giấy phép cho người dùng của bạn.

2. Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.

3. Xác minh rằng giấy phép **Dynamics 365 Project Operations** đã được chọn và chọn **Lưu thay đổi**.

> [!NOTE]
> Ưu đãi dùng thử Finance không cần phải được gán cho người dùng.

## <a name="start-a-new-project-in-lcs"></a>Bắt đầu một dự án mới trong LCS

Tạo một dự án LCS mới như được mô tả trong bài viết, [Bắt đầu một dự án mới trong LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Thêm gói đăng ký Azure vào dự án LCS

Để hoàn thành tác vụ này, hãy làm theo các bước trong bài viết, [Thêm đăng ký Azure vào dự án LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Triển khai môi trường demo Finance với Project Operations kịch bản dựa trên nguồn lực/hàng không nhập kho

Làm theo hướng dẫn trong bài viết, [Cung cấp một môi trường mới](resource-provision-new-environment.md) để hoàn thành việc triển khai. Sử dụng loại triển khai [môi trường demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) để xem trước. 

## <a name="install-cds-setup-and-configuration-data"></a>Cài đặt dữ liệu cấu hình và thiết lập CDS

Cài đặt dữ liệu cấu hình và thiết lập CDS như được mô tả trong bài viết, [Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service](resource-apply-pro-setup-config-data.md).
Chỉ hoàn thành bước này sau khi môi trường demo Finance được triển khai và dữ liệu demo đã sẵn sàng.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
