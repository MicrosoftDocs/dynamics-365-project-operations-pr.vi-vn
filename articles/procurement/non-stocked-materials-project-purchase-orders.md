---
title: Đặt mua vật liệu không trữ kho cho dự án sử dụng đơn đặt hàng cho dự án
description: Bài viết này giải thích cách bạn có thể đặt mua vật liệu không trữ kho cho dự án sử dụng đơn đặt hàng cho dự án.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929838"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Danh mục mua hàng hoặc vật tư không trữ kho cho dự án sử dụng đơn đặt hàng cho dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bộ phận Mua sắm trong tổ chức của bạn có thể sử dụng [đơn đặt hàng](/dynamics365/supply-chain/procurement/purchase-order-overview) để theo dõi các đơn đặt hàng hóa và dịch vụ. Đơn đặt hàng cho danh mục mua hoặc vật tư không trữ kho có thể được quy cho một dự án. Việc lập hóa đơn các đơn đặt hàng này ghi lại chi phí so với dự án.

## <a name="prerequisites"></a>Điều kiện tiên quyết
Hoàn thành các bước sau để bật chức năng đặt hàng dự án.

1. Trong Dynamics 365 Finance, hãy chuyển đến không gian làm việc **Quản lý tính năng**.
2. Trong danh sách tính năng hãy tìm và chọn tính năng **Bật đơn đặt hàng cho dự án trên Project Operations cho các tình huống dựa trên nguồn lực/không có hàng**.
3. Chọn **Bật**.
4. Đặt cấu hình nguyên liệu không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý như được mô tả trong [Đặt cấu hình nguyên liệu không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](configure-materials-nonstocked.md).
5. Định cấu hình các danh mục mua theo mô tả trong [Sử dụng danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Tạo đơn đặt hàng cho dự án từ danh sách đơn đặt hàng cho dự án

1. Trong phần Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** > **Dự án** > **Tất cả các dự án** và chọn một dự án.
2. Ở Ngăn nhiệm vụ, trên tab **Quản lý**, trong nhóm **Mới**, chọn **Nhiệm vụ mục** > **Đơn đặt hàng**.
3. Trên trang **Tạo đơn đặt hàng**, chọn nhà cung cấp mà bạn muốn đặt hàng, nhập thông tin khác nếu thích hợp, sau đó chọn **OK**.
4. Trên trang **Đơn đặt hàng**, trong lưới **Mô tả đơn hàng**, chọn **Thêm mô tả**.
5. Nhập số mặt hàng hoặc danh mục mua, số lượng, đơn vị, đơn giá và các thông tin khác nếu thích hợp.

    > [!NOTE]
    > Chỉ các danh mục mua, mặt hàng không trữ kho và dịch vụ mới có thể được sử dụng với các đơn đặt hàng của dự án. Các mặt hàng tồn kho không được hỗ trợ.

6. Tiếp tục thêm các mặt hàng hoặc danh mục mua theo yêu cầu và xác nhận đơn hàng.

    Biên lai hàng hóa và dịch vụ có thể được ghi lại bằng cách tạo và đăng một biên nhận sản phẩm.

    > [!NOTE]
    > Biên nhận sản phẩm không được ghi vào thực tế dự án trong Microsoft Dataverse và không ảnh hưởng đến sổ phụ của dự án.

    Sau khi nhà cung cấp gửi hóa đơn cho các mặt hàng và dịch vụ trong đơn đặt hàng, bộ phận mua sắm có thể tạo hóa đơn cho đơn đặt hàng bằng cách chuyển đến phần **Hóa đơn** > **Tạo** > **Hóa đơn** trên Ngăn nhiệm vụ. Để biết thêm thông tin về các hóa đơn của nhà cung cấp đang chờ xử lý, hãy xem [Mua vật liệu không tồn kho bằng cách sử dụng hóa đơn của nhà cung cấp đang chờ xử lý](pending-vendor-invoices.md).
