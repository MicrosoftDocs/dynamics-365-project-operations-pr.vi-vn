---
title: Tạo tạm ứng đột xuất cho hợp đồng dự án
description: Bài viết này cung cấp thông tin về việc tạo khoản tạm ứng trên hợp đồng khi cần.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824888"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Tạo tạm ứng đột xuất cho hợp đồng dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Microsoft Dynamics 365 Project Operations hỗ trợ các trường hợp lập hóa đơn liên quan đến các khoản tạm ứng và trước thanh toán. Quy trình sử dụng khoản **Tạm ứng** trong **Project Operations** tương tự với các hợp đồng **Tạm ứng**. 

Hoàn tất các bước sau để lập hóa đơn tạm ứng cho khách hàng.

1. Chuyển đến trang **Hợp đồng dự án**, sau đó chọn tab **Trả trước và tạm ứng**.
2. Trong lưới con liệt kê tất cả các khoản tạm ứng và trả trước đã ghi lại trước đó, hãy chọn **+ Khoản tạm ứng trên Hợp đồng dự án mới**. 

    Biểu mẫu **Tạo nhanh** mở ra để ghi lại một khoản trả trước hoặc tạm ứng.
    
3. Bảng bên dưới liệt kê các trường dùng để ghi lại khoản tạm ứng và những lưu ý cần ghi nhớ khi bạn tạo các khoản tạm ứng mới:

    | Trường | Nội dung mô tả | Tác động xuôi tuyến |
    | --- | --- | --- |
    | **Khách hàng trên hợp đồng dự án** | Trường này cho biết khách hàng nào trên hợp đồng sẽ được lập hóa đơn cho khoản tạm ứng này. | Nếu bạn có nhiều khách hàng trong hợp đồng và muốn lập hóa đơn một khoản tạm ứng/trả trước cụ thể cho từng khách hàng, hãy tạo một khoản tạm ứng cho từng khách hàng. |
    | **Mô tả** | Phần mô tả mục đích hoặc thời gian tạm ứng để giúp xác định khoản tạm ứng này. | Phần mô tả này được hiển thị trên dòng mô tả của hóa đơn cho khoản tạm ứng này. |
    | **Số lượng** | Số tiền tạm ứng hoặc thanh toán trước. | Số tiền này được hiển thị trên dòng mô tả của hóa đơn cho khoản tạm ứng này. |
    | **Ngày lập hóa đơn** | Ngày mà khoản tạm ứng này được lập hóa đơn cho khách hàng. | Đây là ngày mà theo đó quy trình tạo hóa đơn tự động tạo một dòng mô tả của hóa đơn cho khoản tạm ứng này. |
    | **Trạng thái hóa đơn** | Đây là cài đặt tùy chọn cho biết liệu khoản tạm ứng này có được thêm vào hóa đơn nháp lập cho khách hàng này hay không. Các giá trị có thể có bao gồm:</br>- **Chưa sẵn sàng để lập hóa đơn**</br>- **Đã sẵn sàng để lập hóa đơn** | Khi một khoản tạm ứng hoặc trả trước được đánh dấu là **Sẵn sàng để lập hóa đơn**, khoản đó sẽ được thêm vào dưới dạng một dòng thời gian trên hóa đơn nháp. Chỉ khoản tạm ứng đã được lập hóa đơn đầy đủ mới có thể được dùng để đối chiếu với chi phí dự án cho kỳ hóa đơn tiếp theo. |

4. Chọn **Lưu và đóng** trên hộp thoại tạo nhanh để ghi lại khoản tạm ứng hoặc khoản trả trước đó.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
