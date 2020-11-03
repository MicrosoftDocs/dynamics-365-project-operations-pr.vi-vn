---
title: Xem mức sử dụng có thể tính phí cho các nguồn lực
description: Chủ đề này cung cấp thông tin về cách xem mức sử dụng nguồn lực.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087130"
---
# <a name="view-chargeable-utilization-for-resources"></a>Xem mức sử dụng có thể tính phí cho các nguồn lực
 
**Dạng xem thời gian làm việc** trên trang **Thời gian làm việc của nguồn lực trong Project Service** hiển thị thời gian làm việc có thể tính phí cho mỗi nguồn lực có thể đặt lịch. Vì dạng xem dựa trên bảng lịch trình, do đó, bạn sẽ tìm thấy nhiều chức năng tương tự.

> ![Ảnh chụp màn hình của Dạng xem Thời gian làm việc](media/FAQ-utilization-1.png)
 

Thời gian làm việc có thể tính phí được tính như sau:

   Thời gian làm việc có thể tính phí = (Số giờ thực có thể tính phí)/ (Năng lực của nguồn lực)

Các ô đại diện cho thời gian làm việc có thể tính phí được tính cho khoảng thời gian được chọn (ngày, tuần hoặc tháng).

Màu sắc trong mỗi ô hiển thị thời gian làm việc có thể tính phí đối với tài nguyên so với thời gian làm việc có thể tính phí mục tiêu. 

Thời gian làm việc mục tiêu có thể được đặt trên vai trò mặc định của nguồn lực hoặc trên bản thân nguồn lực. Việc tính toán xét đến từng nguồn lực trước, sau đó đến vai trò mặc định của nguồn lực.

## <a name="set-target-on-a-resource"></a>Đặt mục tiêu trên tài nguyên

1. Truy cập vào **Nguồn lực** \> **Nguồn lực**. 
2. Chọn một nguồn lực để mở bản ghi. 
3. Trên tab **Project Service** , bạn có thể đặt thời gian làm việc mục tiêu của nguồn lực.

> ![Ảnh chụp màn hình thao tác sử dụng tab Project Service để đặt thời gian làm việc mục tiêu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Đặt thời gian làm việc mục tiêu trên một vai trò

1. Truy cập **Nguồn lực** \> **Vai trò nguồn lực**. 
2. Chọn một vai trò và mở bản ghi. 
3. Đặt thời gian làm việc mục tiêu cho vai trò.

> ![Ảnh chụp màn hình khi sử dụng Vai trò Nguồn lực để đặt thời gian làm việc mục tiêu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Tính thời gian làm việc có thể tính phí cho một nguồn lực

Để tính toán thời gian làm việc có thể tính phí cho một nguồn lực, bạn cần phải thực hiện một số điều kiện tiên quyết. 

### <a name="set-default-role-for-individual-resource"></a>Đặt vai trò mặc định cho từng tài nguyên

Đầu tiên, thời gian làm việc mục tiêu phải được đặt trên từng nguồn lực hoặc trên vai trò của nguồn lực. Nếu bạn đang sử dụng vai trò của nguồn lực cho mục tiêu, từng nguồn lực phải có một vai trò mặc định. 

1. Để đặt, hãy vào phần **Nguồn lực** \> **Nguồn lực**. 
2. Chọn một nguồn lực, mở bản ghi, sau đó chọn tab **Project Service**. 
3. Trong lưới **Vai trò nguồn lực** , đảm bảo có một vai trò cho nguồn lực và **Là mặc định** được đặt là **Có**.
 
### <a name="change-billing-type-for-resource-role"></a>Thay đổi loại thanh toán cho vai trò nguồn lực này

Vai trò của nguồn lực phải được đặt để có một loại thanh toán **Có thể tính phí**. 

1. Truy cập **Nguồn lực** \> **Vai trò nguồn lực**. 
2. Trên bản ghi bạn muốn cập nhật, sau đó thiết lập loại thanh toán mặc định thành **Có thể tính phí**.

### <a name="set-working-hours-for-resource-role"></a>Đặt số giờ làm việc cho vai trò nguồn lực
 
Nguồn lực phải có giờ làm việc để tính toán năng lực. 

1. Truy cập vào **Nguồn lực** \> **Nguồn lực**. 
2. Chọn một nguồn lực để mở bản ghi, sau đó chọn **Hiện số giờ làm việc**. 
3. Bạn có thể cập nhật hàng loạt danh sách nguồn lực bằng cách áp dụng một **Mẫu giờ làm việc** từ dạng xem **Danh sách nguồn lực**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Khắc phục sự cố giờ thực tế tính phí

Giờ thực tế có thể tính phí có nguồn từ thực thể **Thực tế**. Quá trình tính toán bao gồm các thực tế với loại thanh toán **Có thể tính phí** và vì vậy, bạn phải có dự án mà trong đó các thực tế có thể tính phí.

Nếu không thấy thời gian làm việc có thể tính phí, bạn có thể kiểm tra một vài điều sau:

- Nguồn lực có giờ làm việc được xác định cho năng lực.
- Nguồn lực có thời gian làm việc mục tiêu được xác định riêng hoặc có một vai trò mặc định được gán riêng. Vai trò này có một thời gian làm việc mục được xác định riêng.
- Các thực tế có một loại thanh toán **Có thể tính phí** cho khoảng thời gian mà bạn dự kiến tính toán thời gian làm việc. Kiểm tra các mục sau đây nếu thấy các thực tế có loại thanh toán khác với có thể tính phí:

  - Vai trò được sử dụng trên thực tế có một loại thanh toán mặc định khác có thể tính phí.
  - Vai trò trên mô tả hợp đồng hỗ trợ dự án đã được đặt thành không thể tính phí.
  - Dự án không có mô tả hợp đồng được liên kết.

