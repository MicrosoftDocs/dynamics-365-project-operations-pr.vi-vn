---
title: Di chuyển các mốc thanh toán được lập hóa đơn đầy đủ trong quá trình chuyển đổi
description: Bài viết này giải thích cách di chuyển các mốc lập hóa đơn giá cố định đã được lập hóa đơn cho khách hàng đối với các hợp đồng dự án đang mở trước ngày thực hiện chính thức.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028728"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Di chuyển các mốc thanh toán được lập hóa đơn đầy đủ trong quá trình chuyển đổi

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

## <a name="scenario"></a>Kịch bản

Contoso sẽ thực hiện chính thức với Microsoft Dynamics 365 Project Operations cho các trường hợp nguồn lực/không tồn kho. Là một phần của các hoạt động chuyển đổi, nhóm thực hiện phải di chuyển các hợp đồng dự án mở từ hệ thống cũ. Một số hợp đồng dự án bao gồm các mô tả hợp đồng sử dụng phương pháp lập hóa đơn giá cố định và đã được lập hóa đơn một phần cho khách hàng cuối. Nhóm thực hiện phải di chuyển các mốc lập hóa đơn này thành **Đã đăng hóa đơn khách hàng**, bởi vì chúng phải được bao gồm trong tổng giá trị hợp đồng cho mục đích ghi nhận doanh thu. Tuy nhiên, số dư của khách hàng trong Khoản phải thu và Sổ cái phải không bị ảnh hưởng.

## <a name="solution"></a>Giải pháp

### <a name="prerequisites"></a>Điều kiện tiên quyết

- Dynamics 365 Finance 10.0.24 trở lên phải được cài đặt.
- Môi trường nơi các bước di chuyển sẽ được hoàn thành phải ở chế độ bảo trì. Không nên thực hiện các hoạt động khác trong khi các mốc đang được di chuyển.
- Các bước di chuyển phải được thực hiện chính xác theo mô tả ở đây và chỉ có thể được sử dụng cho hoạt động chuyển đổi. Microsoft không hỗ trợ sử dụng khả năng này theo cách nào khác.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Tạo một phiên bản chuyển đổi của bản đồ ghi kép mốc mô tả hợp đồng tích hợp Project Operations 

1. Đảm bảo rằng ánh xạ mục tiêu cho thực thể **Các mốc của mô tả hợp đồng tích hợp Project Operations** được cập nhật. 

    1. Trong Finance, hãy chuyển đến **Quản lý dữ liệu** \> **Thực thể dữ liệu** và chọn thực thể **Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations**. 
    2. Chọn **Sửa đổi ánh xạ mục tiêu**. 
    3. Trên trang **Ánh xạ tách chuyển vào mục tiêu**, chọn **Tạo ánh xạ** rồi xác nhận rằng bạn muốn tạo ánh xạ.

2. Dừng lại và làm mới ánh xạ ghi kép **Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Đi đến **Quản lý dữ liệu** \> **Ghi kép**, chọn ánh xạ và mở chi tiết của nó. 
    2. Chọn **Dừng** và đợi cho đến khi hệ thống dừng bản đồ. 
    3. Chọn **Làm mới bảng**.

3. Thêm ánh xạ cho trạng thái giao dịch.

    1. Chọn **Thêm ánh xạ**.
    2. Trên mô tả mới, trong cột **Ứng dụng tài chính và hoạt động**, chọn trường **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Trong cột **Microsoft Dataverse**, chọn **msdyn\_invoicestatus \[Trạng thái hóa đơn\]**.
    4. Trong cột **Loại ánh xạ**, chọn mũi tên phải (**\>**).
    5. Trong hộp thoại xuất hiện, trong trường **Hướng đồng bộ**, chọn **Dataverse đến ứng dụng tài chính và hoạt động**.
    6. Chọn **Thêm chuyển đổi**.
    7. Ở trường **Loại chuyển đổi**, hãy chọn **ValueMap**.
    8. Chọn **Thêm ánh xạ giá trị**.
    9. Trong trường bên trái, hãy nhập **4**. Trong trường bên phải, hãy nhập **192350001**. 
    10. Chọn **Lưu** và đóng hộp thoại tài.

4. Chọn **Lưu thành** để lưu phiên bản ánh xạ ghi kép. 
5. Trong ngăn **Thêm bảng**, trong trường **Nhà phát hành**, chọn **Nhà phát hành mặc định**.
6. Trong trường **Phiên bản**, hãy nhập phiên bản.
7. Trong trường **Mô tả**, hãy nhập ghi chú về phiên bản chuyển đổi này của ánh xạ. 
8. Chọn **Lưu.**
9. Bắt đầu ánh xạ.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Di chuyển các mốc đã lập hóa đơn sang môi trường Dataverse

1. Trong môi trường Project Operations Dataverse, tạo các mốc có trạng thái hóa đơn là **Đã sẵn sàng để lập hóa đơn**. Tại thời điểm này, không di chuyển bất kỳ mốc nào chưa được lập hóa đơn.

    > [!NOTE]
    > Trước khi bạn di chuyển các mốc thanh toán, hãy đảm bảo rằng các thứ nguyên tài chính liên quan đến mô tả hợp đồng dự án được đặt như mong đợi. Không thể chỉnh sửa thứ nguyên tài chính sau khi quá trình di chuyển hoàn tất.

2. Sau khi tất cả các mốc được di chuyển, hãy dừng các ánh xạ ghi kép sau:

    - Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinescheduleofvalues)
    - Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)
    - Đề xuất hóa đơn dự án V2 (hóa đơn)

    Để dừng ánh xạ, hãy làm theo các bước sau:

    1. Trong Finance, hãy đi đến **Quản lý dữ liệu** \> **Ghi kép**, chọn ánh xạ và mở chi tiết của nó.
    2. Chọn **Dừng** và đợi cho đến khi hệ thống dừng bản đồ.

3. Trong môi trường Project Operations Dataverse, tạo và xác nhận hóa đơn ước giá cho các mốc thanh toán. 

    1. Trong sơ đồ trang web, hãy chuyển đến các hợp đồng dự án, chọn hợp đồng, sau đó chọn **Tạo hóa đơn**.
    2. Sau khi các hóa đơn được tạo, hãy mở chúng từ menu **Hóa đơn** trong sơ đồ trang web, sau đó chọn **Xác nhận**.

    Bước này tạo các bản ghi được yêu cầu trong môi trường Dataverse. Tuy nhiên, nó không ảnh hưởng đến tài chính và các khoản phải thu, vì ánh xạ ghi kép được liệt kê trước đó đã bị dừng.

4. Sau khi tất cả các hóa đơn ước giá được xác nhận, hãy trả tất cả các ánh xạ ghi kép về trạng thái ban đầu.

    1. Cập nhật phiên bản ánh xạ ghi kép **Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations** (**msdyn\_contractlinescheduleofvalues**) về ban đầu. 
    2. Chọn ánh xạ ghi kép trong danh sách ánh xạ, chọn **Phiên bản ánh xạ bảng**, và sau đó chọn phiên bản gốc của ánh xạ bảng.
    3. Chọn **Lưu.**
    4. Khởi động lại các ánh xạ ghi kép sau:

        - Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinescheduleofvalues)
        - Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)
        - Đề xuất hóa đơn dự án V2 (hóa đơn)

Các mốc quan trọng hiện đã được di chuyển và hệ thống đã sẵn sàng cho các bước tiếp theo trong hoạt động chuyển đổi.
