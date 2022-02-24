---
title: Đặt cấu hình vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý
description: Chủ đề này giải thích cách kích hoạt vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24418f3aad8356bd209eef7487a47a3870bce10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993937"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Đặt cấu hình vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

## <a name="minimum-version-requirement"></a>Yêu cầu phiên bản tối thiểu

Sử dụng vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý cho kịch bản dựa trên nguồn lực/vật tư không tồn kho của Dynamics 365 Project Operations yêu cầu các phiên bản sau:

Các giải pháp Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 trở lên
- Giải pháp điều phối ứng dụng ghi kép – 2.2.2.23 trở lên

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) trở lên. Đảm bảo rằng môi trường Tài chính của bạn ở trạng thái hiện tại và tất cả các bản cập nhật chất lượng đều được áp dụng để đáp ứng yêu cầu phiên bản tối thiểu.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Chạy Bản đồ ghi kép cho vật tư không tồn kho và tích hợp hóa đơn của nhà cung cấp

Phần này cung cấp thông tin về các bản đồ cụ thể cần thiết cho vật tư không tồn kho và hóa đơn của nhà cung cấp. Xác minh rằng các bản đồ điều kiện tiên quyết được liệt kê trong chủ đề [Cung cấp một môi trường mới](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) đang chạy trên môi trường của bạn.

1. Chuyển đến Lifecycle Services (LCS), điều hướng đến dự án LCS của bạn và truy cập vào trang **Chi tiết môi trường**.
2. Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps**. Sau khi bạn chọn liên kết, bạn sẽ được chuyển hướng đến danh sách các thực thể trong ánh xạ.
3. Đảm bảo rằng các bản đồ sau đang chạy. Nếu bản đồ không chạy, hãy khởi động và đảm bảo thêm tất cả các bản đồ bảng có liên quan.

    - CDS phát hành các sản phẩm riêng biệt (sản phẩm)
    - Nhà cung cấp v2 (msdyn_vendors)
    - Bảng Project Operations để ước tính vật tư (msdyn_estimatelines)
    - Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices)
    - Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoicelines)
    - Giá trị tích hợp thực tế của Project Operations (msdyn_actuals). Đảm bảo rằng bạn đang chạy phiên bản bản đồ 1.0.0.14 trở lên. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Bạn có thể kích hoạt phiên bản mới của bản đồ bằng cách chọn **Phiên bản bản đồ bảng** rồi lưu phiên bản đã chọn.

Nếu đang sử dụng dữ liệu minh họa tiêu chuẩn, bạn cũng có thể cần dừng và khởi động lại các bản đồ thực thể sau với đồng bộ hóa ban đầu:
  - Ngày thanh toán CDS V2 (msdyn_paymentdays)
  - Lịch thanh toán (msdyn_paymentschedules)
  - Điều khoản thanh toán (msdyn_paymentterms)
  - Nhóm nhà cung cấp (msdyn_vendorgroups)
  - Đơn vị (uom)

> [!NOTE]
> Đồng bộ ban đầu cho các nhóm và đơn vị nhà cung cấp có thể không thành công đối với một số bản ghi trong tập hợp dữ liệu minh họa hiện có. Bạn có thể bỏ qua lỗi vì các lỗi này sẽ không ngăn cản bạn sử dụng dữ liệu minh họa với Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Đặt cấu hình các điều kiện tiên quyết trong Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Kích hoạt quy trình làm việc để tạo tài khoản dựa trên pháp nhân nhà cung cấp

Giải pháp Điều phối ghi kép cung cấp [Tích hợp tổng thể nhà cung cấp](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md). Là một điều kiện tiên quyết cho tính năng này, dữ liệu nhà cung cấp phải được tạo trong thực thể **Tài khoản**. Kích hoạt quy trình làm việc mẫu để tạo nhà cung cấp trong bảng **Tài khoản** như được mô tả trong [Chuyển đổi giữa các thiết kế của nhà cung cấp](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Đặt các sản phẩm được tạo thành hiện hoạt

Vật tư không tồn kho phải được đặt cấu hình như **Sản phẩm đã phát hành** trong Tài chính. Giải pháp Điều phối ghi kép cung cấp một tính năng vượt trội giúp [Tích hợp sản phẩm đã phát hành vào Danh mục sản phẩm Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md). Theo mặc định, các sản phẩm từ Tài chính được đồng bộ hóa với Dataverse ở trạng thái bản nháp. Để đồng bộ hóa sản phẩm sang trạng thái hiện hoạt nhằm có thể sử dụng trực tiếp sản phẩm trong tài liệu sử dụng vật tư hoặc hóa đơn của nhà cung cấp đang chờ xử lý, hãy chuyển đến **Hệ thống** > **Quản trị** > **Quản trị hệ thống** > **Cài đặt hệ thống** và trên tab **Bán hàng**, hãy đặt **Tạo sản phẩm ở trạng thái hiện hoạt** thành **Có**.

## <a name="configure-prerequisites-in-finance"></a>Đặt cấu hình các điều kiện tiên quyết trong Tài chính

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Kích hoạt khóa tính năng cho các hóa đơn của nhà cung cấp đang chờ xử lý

Hoàn thành các bước sau để kích hoạt chức năng và thêm chi tiết dự án vào các dòng hóa đơn của nhà cung cấp đang chờ xử lý.

1. Trong Tài chính, hãy chuyển đến không gian làm việc **Quản lý tính năng**.
2. Trong danh sách tính năng, hãy tìm tính năng **Kích hoạt hóa đơn của nhà cung cấp đang chờ xử lý trên Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho** rồi chọn **Kích hoạt**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Xác định nhóm danh mục và danh mục dự án cho các hạng mục

Đặt cấu hình ít nhất một nhóm danh mục cho loại giao dịch **Hạng mục** và ít nhất một danh mục dự án sử dụng nhóm này. Để biết thêm thông tin, hãy xem [Đặt cấu hình danh mục dự án](../project-accounting/configure-project-categories.md#category-groups).

Xem lại hồ sơ chi phí và doanh thu của dự án, đồng thời đặt cấu hình thiết lập đăng sổ cái cho các giao dịch hạng mục. Để biết thêm thông tin, hãy xem [Đặt cấu hình hoạt động kế toán cho các dự án có thể tính phí](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Thiết lập sản phẩm chọn thêm

Trong Project Operations, bạn có thể ghi lại các ước tính và hoạt động sử dụng vật tư cho các sản phẩm danh mục được đặt cấu hình trong danh mục sản phẩm đã phát hành và cho các sản phẩm chọn thêm. Việc sử dụng các sản phẩm chọn thêm yêu cầu một sản phẩm đã phát hành duy nhất được đặt cấu hình trong Tài chính cho mục đích này. Hoàn thành các bước sau để đặt cấu hình sản phẩm chọn thêm. Lặp lại các bước này trong từng pháp nhân đang sử dụng Project Operations cho các kịch bản nguồn lực/vật tư không tồn kho.

1. Trong Tài chính, hãy chuyển đến phần **Quản lý thông tin sản phẩm** > **Sản phẩm** > **Sản phẩm đã phát hành** rồi chọn **Mới**.
2. Trong trường **Loại sản phẩm**, hãy chọn **Hạng mục** và trong trường **Loại phụ của sản phẩm**, chọn **Sản phẩm**.
3. Nhập số sản phẩm (WRITEIN) và tên sản phẩm (Sản phẩm chọn thêm).
4. Chọn nhóm mô hình hạng mục. Đảm bảo rằng nhóm mô hình hạng mục mà bạn chọn có trường **Sản phẩm tồn kho theo chính sách lưu kho** được đặt thành **Sai**.
5. Chọn các giá trị trong **Nhóm hạng mục**, **Nhóm kích thước lưu trữ** và trường **Theo dõi nhóm kích thước**. Chỉ sử dụng **Kích thước lưu trữ** cho **Trang web** và không đặt bất kỳ kích thước theo dõi nào.
6. Chọn các giá trị trong **Đơn vị hàng tồn kho**, **Đơn vị mua hàng** và trường **Đơn vị bán hàng** rồi lưu các thay đổi của bạn.
7. Trong tab **Kế hoạch**, đặt các cài đặt đơn hàng thành mặc định và trên tab **Hàng tồn kho**, đặt trang web và kho hàng thành mặc định.
8. Chuyển đến **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và các thông số kế toán** rồi mở **Project Operations trên Dynamics 365 Dataverse**. 
9. Trên tab **Vật tư**, trong trường **Sản phẩm chọn thêm**, hãy chọn sản phẩm bạn đã tạo.
10. Trong môi trường Dataverse của bạn, tại sơ đồ trang web, hãy mở thực thể **Sản phẩm** và tìm bản ghi sản phẩm chọn thêm. 
11. Mở chi tiết bản ghi và đặt trạng thái sản phẩm thành **Không dùng nữa**. Trạng thái sản phẩm này ngăn không cho mọi người vô tình sử dụng hồ sơ này trực tiếp trong các tài liệu sử dụng và ước tính vật tư.

### <a name="set-up-a-procurement-integration-account"></a>Thiết lập tài khoản tích hợp mua sắm

Tài khoản tích hợp mua sắm được sử dụng làm tài khoản thanh toán bù trừ khi đăng hóa đơn nhà cung cấp đang chờ xử lý với các dòng được coi là thuộc tính của dự án.

Khi hệ thống đăng một hóa đơn của nhà cung cấp đang chờ xử lý, tài khoản này được sử dụng cho số tiền chi phí của dự án. Chi tiết hóa đơn của nhà cung cấp được xử lý trong Dataverse và một dự án thực tế tương ứng được tạo. Thông tin từ tình trạng thực tế của dự án được thêm vào nhật ký Tích hợp Project Operations. Khi bạn đăng nhật ký tích hợp, số tiền sẽ được xóa khỏi tài khoản tích hợp mua sắm và được ghi vào chi phí dự án.

1. Để thiết lập tài khoản tích hợp mua sắm, hãy chuyển đến **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và các thông số kế toán** rồi mở **Project Operations trên Dynamics 365 Dataverse**. 
2. Chọn tab **Vật tư** và chọn một giá trị trong trường **Tài khoản tích hợp mua sắm**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Thiết lập giá trị mặc định của danh mục dự án cho một hạng mục

1. Trong Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và các thông số kế toán** rồi mở **Project Operations trên Dynamics 365 Dataverse**. 
2. Trên tab **Giá trị mặc định của danh mục dự án**, trong trường **Hạng mục** , hãy chọn một giá trị. Danh mục dự án này được sử dụng cho các giao dịch vật tư nếu danh mục dự án không được đặt trong hồ sơ giá trị thực tế của dự án.
