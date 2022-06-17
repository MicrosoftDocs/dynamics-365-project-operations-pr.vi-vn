---
title: Di chuyển các mốc thanh toán được lập hóa đơn đầy đủ tại thời điểm cắt
description: Bài viết này giải thích cách di chuyển các mốc thanh toán giá cố định đã được lập hóa đơn cho khách hàng đối với các hợp đồng dự án đang mở trước ngày hoạt động.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912266"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Di chuyển các mốc thanh toán được lập hóa đơn đầy đủ tại thời điểm cắt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

## <a name="scenario"></a>Kịch bản

Contoso sẽ phát trực tiếp với Microsoft Dynamics 365 Project Operations cho các tình huống tài nguyên / không có hàng. Là một phần của các hoạt động cắt bỏ, nhóm thực hiện phải di chuyển các hợp đồng dự án mở từ hệ thống cũ. Một số hợp đồng dự án bao gồm các dòng hợp đồng sử dụng phương pháp thanh toán giá cố định và đã được lập hóa đơn một phần cho khách hàng cuối cùng. Nhóm triển khai phải di chuyển các mốc thanh toán này thành **Hóa đơn khách hàng đã đăng**, bởi vì chúng phải được bao gồm trong tổng giá trị hợp đồng cho mục đích ghi nhận doanh thu. Tuy nhiên, số dư của khách hàng trong Các khoản phải thu và Sổ cái phải không bị ảnh hưởng.

## <a name="solution"></a>Giải pháp

### <a name="prerequisites"></a>Điều kiện tiên quyết

- Dynamics 365 Finance 10.0.24 trở lên phải được cài đặt.
- Môi trường nơi các bước di chuyển sẽ được hoàn thành phải ở chế độ bảo trì. Không có hoạt động nào khác nên được thực hiện trong khi các cột mốc đang được di chuyển.
- Các bước di chuyển phải được tuân thủ chính xác như được mô tả ở đây và chỉ có thể được sử dụng cho hoạt động chuyển đổi. Microsoft không hỗ trợ sử dụng khả năng này khác.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Tạo một phiên bản tóm tắt của dòng hợp đồng tích hợp Hoạt động dự án Các mốc quan trọng của bản đồ ghi kép 

1. Đảm bảo rằng ánh xạ mục tiêu cho **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án** thực thể được cập nhật. 

    1. Trong Tài chính, hãy chuyển đến **Quản lý dữ liệu** \> **Thực thể dữ liệu** và chọn **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án** thực thể. 
    2. Lựa chọn **Sửa đổi ánh xạ mục tiêu**. 
    3. Trên **Lập bản đồ giai đoạn để nhắm mục tiêu** trang, chọn **Tạo ánh xạ**, và sau đó xác nhận rằng bạn muốn tạo ánh xạ.

2. Dừng lại và làm mới **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án** (**msdyn\_ hợp đồng**) bản đồ ghi kép. 

    1. Đi đến **Quản lý dữ liệu** \> **Viết kép**, chọn bản đồ và mở chi tiết của nó. 
    2. Lựa chọn **Dừng lại** và đợi cho đến khi hệ thống dừng bản đồ. 
    3. Lựa chọn **Làm mới bảng**.

3. Thêm ánh xạ cho trạng thái giao dịch.

    1. Lựa chọn **Thêm ánh xạ**.
    2. Trên dòng mới, trong **Ứng dụng Tài chính và Hoạt động** chọn cột **TRANSSTATUS\[ TRANSSTATUS\]** đồng ruộng.
    3. Bên trong **Microsoft Dataverse** cột, chọn **msdyn\_ trạng thái hòa đơn\[ Trạng thái hòa đơn\]**.
    4. Bên trong **Loại bản đồ**, chọn mũi tên phải (**\>**).
    5. Trong hộp thoại xuất hiện, trong **Đồng bộ hóa hướng** trường, chọn **Dataverse cho các ứng dụng Tài chính và Hoạt động**.
    6. Lựa chọn **Thêm biến đổi**.
    7. Bên trong **Biến đổi kiểu** trường, chọn **Bản đồ giá trị**.
    8. Lựa chọn **Thêm ánh xạ giá trị**.
    9. Trong trường bên trái, hãy nhập **4**. Trong trường bên phải, hãy nhập **192350001**. 
    10. Lựa chọn **Tiết kiệm**, và sau đó đóng hộp thoại.

4. Lựa chọn **Lưu thành** để lưu phiên bản của bản đồ ghi kép. 
5. Bên trong **Thêm bảng** ngăn, trong **Nhà xuất bản** trường, chọn **Nhà xuất bản mặc định**.
6. Bên trong **Phiên bản** trường, nhập phiên bản.
7. Bên trong **Sự mô tả**, hãy nhập ghi chú về phiên bản cắt này của bản đồ. 
8. Chọn **Lưu.**
9. Bắt đầu bản đồ.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Di chuyển các mốc đã lập hóa đơn sang Dataverse Môi trường

1. Trong hoạt động dự án Dataverse môi trường, tạo các cột mốc có trạng thái hóa đơn là **Sẵn sàng cho việc lập hóa đơn**. Tại thời điểm này, đừng di chuyển bất kỳ cột mốc nào chưa được lập hóa đơn.

    > [!NOTE]
    > Trước khi bạn di chuyển các mốc thanh toán, hãy đảm bảo rằng các thứ nguyên tài chính liên quan đến dòng hợp đồng dự án được đặt như mong đợi. Không thể chỉnh sửa thứ nguyên tài chính sau khi quá trình di chuyển hoàn tất.

2. Sau khi tất cả các cột mốc được di chuyển, hãy dừng các bản đồ viết kép sau:

    - Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án (msdyn\_ hợp đồng
    - Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)
    - Đề xuất hóa đơn dự án V2 (hóa đơn)

    Để dừng bản đồ, hãy làm theo các bước sau:

    1. Trong Tài chính, hãy chuyển đến **Quản lý dữ liệu** \> **Viết kép**, chọn một bản đồ và mở chi tiết của nó.
    2. Lựa chọn **Dừng lại** và đợi cho đến khi hệ thống dừng bản đồ.

3. Trong hoạt động dự án Dataverse môi trường, tạo và xác nhận hóa đơn chiếu lệ cho các mốc thanh toán. 

    1. Trong sơ đồ trang web, hãy chuyển đến các hợp đồng dự án, chọn các hợp đồng, sau đó chọn **Tạo hóa đơn**.
    2. Sau khi các hóa đơn được tạo, hãy mở chúng từ **Hóa đơn** trong sơ đồ trang web, sau đó chọn **Xác nhận**.

    Bước này tạo các bản ghi được yêu cầu trong Dataverse Môi trường. Tuy nhiên, nó không ảnh hưởng đến tài chính và các khoản phải thu, vì các bản đồ ghi kép được liệt kê trước đây đã bị dừng.

4. Sau khi tất cả các hóa đơn chiếu lệ được xác nhận, hãy trả tất cả các bản đồ ghi kép về trạng thái ban đầu.

    1. Cập nhật phiên bản của **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án** (**msdyn\_ hợp đồng**) bản đồ ghi kép trở lại bản gốc. 
    2. Chọn bản đồ ghi kép trong danh sách bản đồ, chọn **Phiên bản bản đồ bảng**, và sau đó chọn phiên bản gốc của sơ đồ bảng.
    3. Chọn **Lưu.**
    4. Khởi động lại các bản đồ ghi kép sau:

        - Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án (msdyn\_ hợp đồng
        - Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)
        - Đề xuất hóa đơn dự án V2 (hóa đơn)

Các mốc hiện đã được di chuyển và hệ thống đã sẵn sàng cho các bước tiếp theo trong hoạt động chuyển đổi.
