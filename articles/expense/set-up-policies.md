---
title: Xác định chính sách chi phí
description: Bạn có thể xác định các chính sách chi phí mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ae6de664fc18a00fd6d3d6c8177daa95da5754d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576940"
---
# <a name="define-expense-policies"></a>Xác định chính sách chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể xác định các chính sách mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại.         
Thực hiện các chính sách chi phí có thể giúp bạn quản lý chi phí một cách hiệu quả.         

Ví dụ: bạn có thể đặt chính sách cho chi phí khách sạn ở New York City, trong đó quy định rằng chi phí mỗi đêm không được vượt quá 250 USD.       
Nếu một nhân viên nộp báo cáo chi phí hoặc tiêu chuẩn đi lại mà giá phòng vượt quá số tiền này, hệ thống sẽ thông báo         
cho nhân viên rằng số tiền theo chính sách cho chi phí đó đã bị vượt quá. Bạn có thể đặt cấu hình thông báo mà nhân viên sẽ nhận được khi bạn        
xác định chính sách.      
        
Bạn có thể xác định 3 loại chính sách:         
        
- **Cảnh báo**: Cho phép nhân viên gửi báo cáo chi phí hoặc tiêu chuẩn đi lại nhưng chi phí sẽ được đánh dấu cho tất cả những người phê duyệt và         
  cho báo cáo về sau.        

- **Lỗi**: Yêu cầu nhân viên sửa đổi chi phí để tuân thủ chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.        
 
 - **Chứng minh**: Yêu cầu nhân viên hoặc người quản lý nhập chứng minh cho việc vượt quá số tiền theo chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.        

## <a name="policy-tips"></a>Mẹo chính sách
Dưới đây là một số gợi ý có thể hỗ trợ bạn khi tạo các chính sách mới để quản lý chi phí: 

- Các chính sách có hiệu lực theo ngày có nghĩa là chính sách sẽ không có hiệu lực nếu được tạo vào ngày sau ngày chi phí phát sinh. Ví dụ: bạn tạo chính sách mới hôm nay để áp dụng cho chi phí bữa ăn tối đa là 50 USD. Bất kỳ chi phí hiện có nào đã nhập từ ngày hôm qua sẽ không được kiểm tra theo chính sách này.
- Khi tạo chính sách cho danh mục chi phí có thể được chia thành từng khoản mục, hãy xem xét thêm điều kiện cho loại dòng chi phí. Một số chính sách, chẳng hạn như yêu cầu biên lai, có thể không áp dụng cho các dòng được chia thành từng khoản mục. Trong trường hợp này, chính sách chỉ được áp dụng cho dòng tiêu đề hoặc dòng không được chia thành từng khoản mục. 
- Các chính sách quản lý chi phí được đánh giá dựa trên thực thể nguồn theo mặc định. Đối với các tình huống liên công ty, bạn có thể đặt chính sách cần đánh giá dựa trên thực thể đích (thực thể mượn). Để chạy các chính sách dựa trên thực thể đích, hãy bật tính năng **Đánh giá chính sách chi phí dựa trên pháp nhân mượn** trong không gian làm việc **Quản lý tính năng**.

## <a name="when-to-evaluate-policies"></a>Thời điểm đánh giá chính sách

Trong các tham số quản lý chi phí, bạn có thể chọn để đánh giá các chính sách quản lý chi phí khi một dòng được lưu hoặc khi báo cáo chi phí được gửi. Nếu bạn chọn đánh giá vào thời điểm lưu dòng, người dùng sẽ sớm thấy được những gì mình cần làm để hoàn thành báo cáo chi phí của mình cùng một lúc. Nếu không, bạn có thể trì hoãn việc đánh giá chính sách và tiết kiệm thời gian bằng cách xác thực vào lúc cuối, trong khi gửi lên quy trình làm việc.


[!INCLUDE[footer-include](../includes/footer-banner.md)]