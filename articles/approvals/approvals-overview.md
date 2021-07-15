---
title: Tổng quan về phê duyệt
description: Chủ đề này cung cấp thông tin về cách làm việc với các mục phê duyệt trong Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368682"
---
# <a name="approvals-overview"></a>Tổng quan về phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các mục nhập thời gian, chi phí và mức sử dụng vật tư đã gửi sẽ chuyển qua quy trình làm việc phê duyệt. Sau khi các mục nhập được phê duyệt, các giao dịch được ghi lại trong thực tế hoặc thời gian được đăng ký trong lịch trình.

## <a name="approvals-workflow"></a>Quy trình làm việc phê duyệt
Khi bạn tạo và gửi mục nhập thời gian, chi phí hoặc mức sử dụng vật tư, thì một bản ghi phê duyệt sẽ được tạo. Người phê duyệt dự án hoặc người quản lý xem xét và phê duyệt mục nhập đó. Nếu mục nhập có liên quan đến một dự án, các giá trị thực tế sẽ được tạo ra khi mục nhập được phê duyệt. Điều này cho phép theo dõi chi phí và thanh toán.

## <a name="approve-an-entry"></a>Phê duyệt một mục nhập
Trang **Phê duyệt** cho phép bạn chuyển đổi giữa các dạng xem khác nhau để bạn có thể xem các loại phê duyệt khác nhau.
  
1. Đi đến trang **Phê duyệt** rồi chọn **Chi phí**, **Thời gian**, **Sử dụng vật tư** hoặc **Thu hồi**.
2. Đánh giá từng phê duyệt và chọn những phê duyệt mà bạn muốn phê duyệt.
3. Chọn **Phê duyệt** để phê duyệt các mục nhập đã chọn.
Hệ thống xử lý các mục nhập này và tạo các giá trị thực tế.

## <a name="reject-an-entry"></a>Từ chối một mục nhập
Với tư cách là người phê duyệt dự án, bạn có thể phải gửi lại mục nhập cho người dùng để chỉnh sửa.
  
1. Đi đến **Phê duyệt** rồi chọn mục nhập để từ chối. 
2. Chọn **Từ chối**.
3. Bạn cũng có thể chọn cách thêm nhận xét trong hộp thoại **Nhận xét về lý do từ chối** để thông báo cho người dùng lý do tại sao mục nhập lại bị từ chối.
4. Chọn **OK**. Mục nhập sẽ được trả lại cho người dùng.
  
## <a name="cancel-approval"></a>Hủy phê duyệt
Trong một số trường hợp, bạn có thể cần phải hủy mục nhập đã được phê duyệt trước đó. Việc hủy một mục nhập đã được phê duyệt trước đó sẽ có ảnh hưởng đến tài chính. 

## <a name="approving-recall-requests"></a>Phê duyệt yêu cầu thu hồi
Trong một số trường hợp, tư vấn viên có thể cần thu hồi một mục nhập đã được phê duyệt trước đó. Việc hủy một mục nhập đã được phê duyệt trước đó sẽ có ảnh hưởng đến tài chính. Người phê duyệt dự án cần phải phê duyệt việc thu hồi để đảo ngược giao dịch trong mục Giá trị thực tế.

## <a name="specify-project-approvers"></a>Chỉ định người phê duyệt dự án
Mỗi dự án có một số thành viên trong nhóm dự án. Bạn có thể chỉ định thành viên nào trong nhóm cũng là người phê duyệt dự án.

1. Đi đến **Dự án** và mở dự án từ danh sách.
2. Tên tab **Nhóm**, chọn thành viên nhóm sẽ là người phê duyệt dự án, sau đó chọn **Chỉnh sửa**.
3. Đặt trường **Người phê duyệt dự án** thành **Có**.
4. Chọn **Lưu**.
5. Lặp lại các bước 2-4 để thêm người phê duyệt dự án bổ sung.

## <a name="configure-the-users-manager"></a>Định cấu hình người quản lý của người dùng

1. Đi tới **Thiết đặt** > **Bảo mật** > **Người dùng**.
2. Chọn người dùng mà bạn đang phân công người quản lý và trong vùng **Thông tin tổ chức**, chọn người quản lý từ danh sách. 
3. Chọn **Lưu**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
