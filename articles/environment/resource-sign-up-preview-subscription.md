---
title: Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về cách đăng ký và triển khai Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949142"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Đăng ký gói đăng ký xem trước Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này giải thích cách đăng ký bản xem trước/ưu đãi của đối tác và triển khai môi trường Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho.

## <a name="prerequisites"></a>Điều kiện tiên quyết

- Bạn sẽ nhận được một email mời bạn sử dụng bản xem trước. Bạn có thể yêu cầu xem trước trên [Trang web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Người dùng triển khai bản xem trước phải có quyền quản trị viên toàn cầu đối với đối tượng thuê Azure.
- Việc triển khai môi trường Finance yêu cầu đăng ký Azure hợp lệ sẽ được lập hóa đơn cho mỗi môi trường. Bạn có thể sử dụng đăng ký hiện có của tổ chức mình hoặc sử dụng [Bản dùng thử Azure](https://azure.microsoft.com/en-us/free/) để bắt đầu. Môi trường CDS sẽ được cung cấp miễn phí trong khoảng thời gian giới hạn 30 ngày.

## <a name="subscribe"></a>Đăng ký

Khi nhận được phê duyệt [yêu cầu xem trước](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), bạn sẽ nhận được hai ưu đãi từ Microsoft qua email. Những ưu đãi này cho phép bạn triển khai Bản xem trước của Project Operations:

- Dynamics 365 Project Operations – Bản dùng thử ở dạng xem trước
- Dynamics 365 for Finance and Operations Bản dùng thử ở dạng xem trước.

> [!IMPORTANT]
> Chỉ một cá nhân, quản trị viên đối tượng thuê, trong một tổ chức cần thực hiện nhiệm vụ này. Nếu bạn không phải là người đăng ký bản phát hành này, hãy đợi cho đến khi tổ chức của bạn được đăng ký và bạn đã nhận được thông tin xác thực người dùng của mình.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Bản dùng thử ở dạng xem trước

1. Đổi ưu đãi đầu tiên, **Bản dùng thử Dynamics 365 Project Operations** với URL được cung cấp trong email chào mừng của bạn.

![Ưu đãi đầu tiên](./media/1FirstOffer.png)

2. Xác minh rằng bạn đã đăng nhập với tư cách là người dùng thuộc tổ chức sẽ đăng ký dịch vụ.
3. Tiếp tục đổi ưu đãi. 
4. Chọn **Có, thêm vào tài khoản của tôi**.

![Đổi ưu đãi](./media/2RedeemFirstOffer.png)

![Xác nhận ưu đãi](./media/3ConfirmFirstOffer.png)

![Đã đổi ưu đãi](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance bản dùng thử ở dạng xem trước

Lặp lại các bước tương tự với ưu đãi thứ hai từ email Chào mừng.

## <a name="assign-licenses"></a>Gán giấy phép

> [!IMPORTANT]
> Bạn sẽ cần quyền truy cập quản trị vào Cổng thông tin Office 365 của tổ chức bạn để hoàn thành các bước sau.

1. Chuyển đến [Trung tâm quản trị Microsoft 365](https://portal.office.com/) để gán giấy phép cho người dùng của bạn.

![Cổng thông tin quản trị Office](./media/5OfficeAdminPortal.png)

2. Trên trang **Người dùng đang hoạt động**, hãy chọn người dùng mà bạn muốn gán giấy phép.

![Gán giấy phép](./media/6AssignLicenses.png)

3. Xác minh rằng giấy phép Project Operations đã được chọn và chọn **Lưu thay đổi**. 

> [!NOTE]
> Ưu đãi dùng thử Finance không cần phải được gán cho người dùng.

## <a name="start-a-new-project-in-lcs"></a>Bắt đầu một dự án mới trong LCS

Tạo dự án LCS mới như được mô tả trong chủ đề [Bắt đầu dự án mới trong LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Thêm gói đăng ký Azure vào dự án LCS

Để hoàn thành nhiệm vụ này, hãy làm theo các bước trong chủ đề [Thêm đăng ký Azure vào dự án LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Triển khai môi trường demo Finance với Project Operations kịch bản dựa trên nguồn lực/hàng không nhập kho

Làm theo hướng dẫn trong chủ đề [Cung cấp môi trường mới](resource-provision-new-environment.md) để hoàn thành việc triển khai. Sử dụng loại triển khai [môi trường demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) để xem trước.

## <a name="install-cds-setup-and-configuration-data"></a>Cài đặt dữ liệu cấu hình và thiết lập CDS

Cài đặt dữ liệu cấu hình và thiết lập CDS như được mô tả trong chủ đề [Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service](resource-apply-pro-setup-config-data.md).

