---
title: Quản lý múi giờ
description: Khi một dự án được tạo, múi giờ của nó dựa trên múi giờ được xác định trong mẫu giờ làm việc được áp dụng.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961974"
---
# <a name="manage-time-zones"></a>Quản lý múi giờ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


## <a name="projects"></a>Dự án

Khi một dự án được tạo, múi giờ dựa trên múi giờ được xác định trong mẫu giờ làm việc được áp dụng. Trên **Dự án**, ngày luôn tương ứng với múi giờ của người dùng đăng nhập trên từng tab, ngoại trừ tab **Tác vụ**. Khi bạn xem cấu trúc phân tích công việc, ngày tháng sẽ luôn được hiển thị trong múi giờ của dự án.

## <a name="tasks"></a>Tác vụ

Khi một tác vụ được tạo, thời gian bắt đầu, thời gian kết thúc và giờ/ngày được kiểm soát bởi giờ làm việc của dự án. Ví dụ: nếu một tác vụ được tạo với một dự án có múi giờ là -8 PST và có các giờ làm việc sau đây: 9:00 sáng đến 5:00 chiều từ Thứ Hai đến Thứ Sáu, thì bất kỳ tác vụ nào được tạo mà không có sự phân công sẽ tuân theo thời gian bắt đầu và thời gian kết thúc của lịch dự án.

## <a name="manage-resources-with-time-zones"></a>Quản lý nguồn lực với múi giờ

Để có kết quả chính xác và dự đoán được khi sử dụng **Gia hạn mục đặt trước**, có hai điều kiện tiên quyết chính cần đáp ứng:  

- Người dùng phải đặt cấu hình múi giờ của thiết bị để khớp với múi giờ được xác định trong phần **Thiết đặt cá nhân hóa** của hệ thống.
 
  ![Cài đặt múi giờ trong Windows 10](media/reconcile-assignments-03.png)

  ![Cài đặt múi giờ trong cài đặt cá nhân hóa](media/reconcile-assignments-04.png)
 
- Nguồn lực có thể đặt trước phải có ít nhất một phút thời gian làm việc trùng với các phân phối được sử dụng để xác định gia hạn được yêu cầu. Ví dụ: các nguồn lực sau đây có giờ làm việc rơi vào khoảng từ 9:00 sáng đến 7:00 tối. 

  ![So sánh phân phối tài nguyên](media/reconcile-assignments-05.png)

Bảng sau đây hiển thị:

- Mẫu lịch dự án
- Nguồn lực A: Tài nguyên này có cùng lịch và nằm trong cùng múi giờ với dự án. Thời gian bắt đầu của các đăng ký sẽ là 9:00 giờ sáng.
- Nguồn lực B: Nguồn lực này thuộc một múi giờ khác so với dự án và bắt đầu lúc 7:00 sáng trong múi giờ của họ. Tuy nhiên, việc đăng ký sẽ bắt đầu lúc 9:00 giờ sáng vì đó là thời gian bắt đầu sớm nhất của phân phối giờ làm việc theo phân công.
- Nguồn lực C và D: Các nguồn lực thuộc các múi giờ khác nhau, cả hai đều khác nhau và khác dự án, và mục đặt trước của họ bắt đầu không sớm hơn thời gian rảnh tương ứng.

|Thực thể  |Lịch  |
|-|-|
|Mẫu lịch dự án   | ![lịch dự án](media/reconcile-assignments-06.png) |
|Nguồn lực A  | ![Lịch nguồn lực A](media/reconcile-assignments-06.png) |
|Nguồn lực B  |  ![Lịch nguồn lực B](media/reconcile-assignments-07.png) |
|Nguồn lực C  |  ![Lịch nguồn lực C](media/reconcile-assignments-08.png) |
|Nguồn lực D  | ![Lịch nguồn lực D](media/reconcile-assignments-09.png)  |
 
Khi bạn điều hướng đến dạng xem **Điều hòa**, các mục phân công tài nguyên và tình trạng thiếu đặt trước sẽ được hiển thị.

![Dạng xem điều hòa trước khi gia hạn](media/reconcile-assignments-10.png)

Sau khi chức năng gia hạn đặt trước đã được sử dụng cho mỗi nguồn lực, nội dung đặt trước được mở rộng thành công cho từng nguồn lực do giờ làm việc của mỗi nguồn lực trùng với ranh giới thiếu hụt.

![Dạng xem điều hòa sau khi gia hạn đăng ký](media/reconcile-assignments-11.png) 

Lưu ý rằng việc xem xét kỹ hơn các chi tiết của đặt chỗ sẽ cho thấy sự khác biệt về thời gian bắt đầu của mục đặt trước. Việc đặt trước bắt đầu không sớm hơn thời gian bắt đầu của ranh giới phân công và không sớm hơn thời gian bắt đầu có sẵn của nguồn lực.

![Các đăng ký nguồn lực mới trong bảng lịch trình](media/reconcile-assignments-12.png)
