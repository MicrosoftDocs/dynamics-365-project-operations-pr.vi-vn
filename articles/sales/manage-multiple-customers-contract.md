---
title: Quản lý nhiều khách hàng trên một hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách quản lý nhiều khách hàng trên một hợp đồng dự án.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5554cb062710c3587d81b1a29771a7af84d2d05f
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643199"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Quản lý nhiều khách hàng trên một hợp đồng dự án

Chủ đề này cung cấp thông tin về cách quản lý nhiều khách hàng trên một hợp đồng dự án. Bạn có thể dùng hợp đồng dự án khi thỏa thuận theo hợp đồng của nhiều khách hàng là cần thiết để cấp vốn cho một giao dịch. Trên trang **Hợp đồng dự án**, tab **Tóm tắt** bao gồm những thông tin về khách hàng chính của một giao dịch. Những khách hàng khác tham gia vào giao dịch có thể được thêm vào tab **Khách hàng**.

Tất cả các khách hàng trên hợp đồng ở tab **Khách hàng** của hợp đồng dự án đều mặc định là khách hàng trong phần mô tả hợp đồng của bất kỳ mô tả hợp đồng mới nào dựa trên dự án được tạo cho hợp đồng dự án. Mọi dòng hợp đồng hiện có dựa trên dự án sẽ không thừa hưởng hồ sơ khách hàng mới theo hợp đồng được tạo sau này.

Bạn có thể thêm, cập nhật hoặc xóa hợp đồng và khách hàng trên dòng hợp đồng bất cứ lúc nào hợp đồng được ký kết. Khách hàng trên hợp đồng dự án phải được thiết lập là khách hàng trong công ty hoặc pháp nhân sở hữu trên trang **Khách hàng**. Các pháp nhân được thiết lập trong mô-đun **Quản lý dự án và kế toán** của Dynamics 365 Project Operations và có sẵn như là các công ty trong các mô-đun **Bán hàng dự án** và **Giao hàng** của Project Operations.

## <a name="primary-customers"></a>Khách hàng chính

Khách hàng tiềm năng trên tab **Tóm tắt** của hợp đồng dự án là khách hàng chính của hợp đồng. Bạn không thể cập nhật khách hàng chính từ danh sách khách hàng trên hợp đồng. Nếu cố gắng xóa khách hàng chính khỏi danh sách khách hàng trên hợp đồng, bạn sẽ nhận được thông báo lỗi cho biết không thể xóa hồ sơ khách hàng chính trên hợp đồng. Thay vào đó, hãy thay đổi khách hàng trong trường **Khách hàng tiềm năng** trên tab **Tóm tắt** của hợp đồng dự án. Khi bạn cập nhật trường này, khách hàng mới chọn sẽ được thêm làm khách hàng mới trên hợp đồng với cờ **Chính** đặt thành **Có**. Khách hàng chính trước đó vẫn là một khách hàng trên hợp đồng, nhưng họ không còn là khách hàng chính nữa.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Tạo, cập nhật hoặc xóa hồ sơ khách hàng trên hợp đồng

Bạn có thể tạo, cập nhật hoặc xóa một khách hàng trên hợp đồng khỏi tab **Khách hàng trên hợp đồng** của trang **Hợp đồng dự án**. Các trường sau đây có trên bản ghi khách hàng theo hợp đồng của hợp đồng dự án.

| **Trường** | **Vị trí** | **Mô tả** | 
| --- | --- | --- | 
| T.khoản | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Liệt kê tất cả các tài khoản đang hoạt động. Trường này bị khóa sau khi bản ghi được tạo. Để cập nhật bản ghi, bạn phải xóa đi rồi tạo lại. Nếu đã ghi lại bất kỳ dữ liệu thực tế nào hoặc nếu hồ sơ khách hàng trên hợp đồng là hồ sơ khách hàng chính, thì bạn không thể xóa hồ sơ. Khi tạo xong dòng hợp đồng, khách hàng trên hợp đồng sẽ được sao chép dưới dạng khách hàng trên dòng hợp đồng. |
| Phần trăm Thanh toán Chia tách | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Thể hiện tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán được phân bổ cho khách hàng trên hợp đồng này. Khi tạo xong dòng hợp đồng mới cho dự án, tỷ lệ phân chia hóa đơn sẽ được sao chép sang dòng hợp đồng mới bất kỳ được tạo và sang khách hàng trên dòng hợp đồng của dự án. |
| Tên liên hệ xuất hóa đơn | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Trường văn bản này nên được dùng để xác định người liên hệ trên hóa đơn cho khách hàng. Giá trị mặc định được lấy từ hồ sơ tài khoản có liên quan. Tên người liên hệ được sao chép sang **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| Tên Nhận hóa đơn | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Dùng trường này để xác định người liên hệ trên hóa đơn cho khách hàng. Giá trị mặc định được lấy từ hồ sơ tài khoản có liên quan. Tên được sao chép sang trường **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| Điều khoản thanh toán | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Giá trị mặc định được lấy từ hồ sơ tài khoản có liên quan. Các điều khoản được sao chép sang **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| Công ty sở hữu | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng dự án** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng dự án. | Pháp nhân mà khách hàng được thiết lập trong mô-đun **Quản lý dự án và kế toán**. Trường này là trường chỉ đọc và được đặt thành công ty sở hữu của hợp đồng dự án.</br>Danh sách khách hàng cần thêm vào trường **Tài khoản** đã được lọc vào danh sách từ công ty sở hữu trong mô-đun **Quản lý dự án và kế toán** của Project Operations. Công ty sở hữu tương đương với pháp nhân trong mô-đun **Quản lý dự án và kế toán** của Project Operations. Tất cả chi phí và doanh thu phát sinh từ dự án này được hạch toán vào sổ cái chung của công ty sở hữu. |
| Là Làm tròn | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Cho biết khách hàng này có phải là khách hàng làm tròn mặc định cho giao dịch không. Chỉ có thể có một khách hàng làm tròn trong hợp đồng dự án. Khi việc phân tách chi phí và doanh số bán hàng chưa thanh toán theo số lượng và khách hàng tiềm năng dẫn đến chênh lệch do làm tròn số, thì chênh lệch đó được áp dụng cho số liệu thực tế ánh xạ đến khách hàng này. |
| Giới hạn không vượt quá | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu chính và trang tạo nhanh cho khách hàng trên hợp đồng. | Cho biết liệu có giới hạn hoặc mức trần đã được thương lượng cho tổng số tiền mà khách hàng sẽ được lập hóa đơn cho cam kết này hay không. Việc thiết lập Giới hạn không vượt quá ở cấp khách hàng trên hợp đồng sẽ được đánh giá dựa trên dữ liệu thực tế về doanh thu chưa thanh toán tham chiếu đến khách hàng trên hợp đồng này. |

## <a name="edit-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán trong lưới này. Khi tổng các tỷ lệ phần trăm thanh toán không bằng 100 phần trăm, lỗi sẽ xảy ra. Sau khi bạn chỉnh sửa tỷ lệ phần trăm thanh toán, hãy làm mới trang **Hợp đồng dự án** để loại bỏ lỗi đó.

Bạn cũng có thể chọn **Phân phối đồng đều** trên lưới con khách hàng trên hợp đồng dự án. Tỷ lệ thanh toán được phân bổ đều cho tất cả khách hàng trên hợp đồng dự án. Nếu có bất kỳ hệ số làm tròn nào, hệ số này sẽ được thêm cho khách hàng làm tròn. Một trong những khách hàng trên hợp đồng sẽ luôn có cờ **Làm tròn** đặt thành **Có**. Khách hàng đó là khách hàng làm tròn. Thông thường, khách hàng làm tròn cũng là khách hàng chính của hợp đồng, nhưng điều đó không bắt buộc.
