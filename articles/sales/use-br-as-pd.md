---
title: Dùng nguồn lực đăng ký được làm thông số định giá
description: Bài viết này cung cấp thông tin về cách sử dụng tài nguyên có thể đặt trước làm thứ nguyên định giá.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914842"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Dùng nguồn lực đăng ký được làm thông số định giá

 _**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_ 

Bài viết này cung cấp thông tin về cách sử dụng tài nguyên có thể đặt trước làm thứ nguyên định giá. Nếu chiến lược của bạn là thiết lập giá cả sao cho mỗi nguồn lực đăng ký được phải có một mức giá hoặc chi phí cụ thể, thì hãy dùng nguồn lực đăng ký được làm thông số định giá.

## <a name="prerequisites"></a>Điều kiện tiên quyết
Trước khi hoàn tất các thủ tục trong bài viết này, bạn phải có giải pháp thứ nguyên định giá mới cho tổ chức của mình. Nếu chưa tạo giải pháp như vậy, hãy xem [Tạo các trường và thực thể tùy chỉnh](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Thêm trường Nguồn lực đăng ký được vào các biểu mẫu và dạng xem
Để trường **Nguồn lực đăng ký được** hiển thị trong giải pháp thông số định giá, bạn phải thêm trường này vào tất cả biểu mẫu và dạng xem như một thực thể.

Bảng sau liệt kê tất cả mọi biểu mẫu và dạng xem sẵn dùng, theo thực thể. Bạn cũng phải thêm trường mới vào biểu mẫu hoặc dạng xem bổ sung bất kỳ trong các thực thể đã tùy chỉnh.

|   Thực thể        | Biểu mẫu   |Dạng xem        |
| ------------------------------|---------------------------------|----------------------------------|
|  Giá Vai trò| Thông tin | - Giá danh mục nguồn lực đang hoạt động<br> - Giá danh mục nguồn lực có liên kết |
|  Tăng giá theo Vai trò| Thông tin| - Phần tăng giá theo vai trò đang hoạt động<br>- Phần tăng giá theo vai trò có liên kết |
|  Chi tiết mô tả báo giá| - Thông tin dự án<br>- Tạo nhanh dự án| - Chi tiết về dòng báo giá đang hoạt động<br>- Chi tiết về dòng báo giá kết hợp<br>- Chi tiết về dòng báo giá có liên kết |
|  Chi tiết mô tả hợp đồng dự án| - Thông tin dự án<br>- Tạo nhanh dự án| - Chi tiết về dòng hợp đồng kết hợp<br>- Chi tiết về dòng hợp đồng đang hoạt động<br>- Chi tiết về dòng hợp đồng có liên kết |
|  Nhiệm vụ dự án| - Thông tin<br>- Biểu mẫu mới| &nbsp; |
|  Thành viên Nhóm Dự án| - Thông tin<br>- Biểu mẫu mới| - Thành viên nhóm dự án đang hoạt động<br>- Thành viên nhóm dự án<br>- Thành viên nhóm dự án có liên kết |
|  Mục nhập Thời gian| - Thông tin<br>- Tạo mục thời gian| - Mục thời gian của tôi theo ngày<br>- Mục thời gian của tôi cho tuần này<br>- Mục thời gian cần để phê duyệt|
|  Dòng nhật ký kế toán| - Thông tin<br>- Tạo nhanh| - Dòng nhật ký kế toán hiện hoạt<br>- Dòng nhật ký kế toán có liên kết |
|  Chi tiết Mô tả Hóa đơn| - Thông tin<br>- Tạo nhanh| - Chi tiết về dòng hóa đơn hiện hoạt<br>- Giao dịch hóa đơn có thể tính phí<br>- Giao dịch hóa đơn miễn phí<br>- Chi tiết về dòng hóa đơn có liên kết <br>- Giao dịch hóa đơn không thể tính phí|
|  Thực tế| - Thông tin<br>- Trường hợp thực tế hiện hoạt| Thực tế có liên kết |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Thiết lập nguồn lực đăng ký được làm thông số định giá
Để thiết lập nguồn lực đăng ký được làm thông số định giá, hãy làm theo các bước sau:

1. Đi tới **Cài đặt** > **Tham số**. 
2. Trên trang **Tham số**, trên tab **Thông số định giá dựa trên số tiền**, hãy xác minh rằng lưới này hiển thị các bản ghi trong thực thể **Thông số định giá**. 
2. Thêm **Nguồn lực có thể đặt lịch** và danh sách phương diện định giá này dưới dạng **msdyn_bookableresource**. 
3. Trong tab **Áp dụng cho chi phí** và **Áp dụng cho doanh số**, hãy chọn một giá trị.
4. Trong phần **Loại thông số**, hãy chọn **Dựa trên số tiền**. 
5. Chọn ưu tiên chi phí và bán hàng cho nguồn lực có thể đặt lịch. Thông thường, nguồn lực đăng ký được có mức ưu tiên cao nhất khi được thêm vào làm thông số định giá. Đặt mức độ ưu tiên thành **1** (hoặc **0** tùy theo cách bạn tính mức độ ưu tiên) để đảm bảo giữ nguyên hành vi này.

## <a name="set-up-pricing-dimension-field-names"></a>Thiết lập tên trường phương diện định giá

Khi tên trường của một thông số định giá trong bảng **Giá theo vai trò** khác với tên trường trong bất kỳ thể nào khác khi mà giá mặc định được sử dụng, thì bản ghi thông số định giá phải được thông báo về các tên khác nhau.  

Đối với nguồn lực đăng ký được, thực thể **Thành viên nhóm dự án** phải có tên trường hơi khác so với trên thực thể **Giá theo vai trò**: 

 - Thực thể **Thành viên nhóm dự án** = **msdyn_bookableresourceid**
 - Thực thể **Giá theo vai trò** = **msdyn_bookableresource**

Bản ghi thông số định giá của **msydn_bookableresource** phải được thông báo về sự khác biệt này.

1. Bấm đúp vào hàng trong lưới **Thông số định giá** để mở trang thông số của **msdyn_bookableresource**.
2. Trên trang thông số, ở tab **Có liên quan**, hãy chọn **Tên trường thông số định giá**.

  ![Tab tên trường phương diện định giá.](media/PD-fieldname.png)

3. Trong dạng xem liên kết mở ra, hãy chọn **Thêm tên trường thông số định giá mới**.

  ![Thêm tên trường phương diện định giá mới.](media/Add-NewPD-fieldname.png)

  Thao tác này sẽ mở ra trang **Tên trường phương diện định giá mới** cho **msdyn_bookableresource**. 

4. Trên trang **Tên trường thông số định giá mới**, hãy thêm **msdyn_projectteam** vào **Tên logic của thực thể**.
5. Thêm **msdyn_bookableresourceid** vào **Tên trường**.

 ![Biểu mẫu tên trường phương diện định giá mới.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]