---
title: Ước tính doanh thu và chi phí của dự án khi một nguồn lực có thể đặt trước đáp ứng nhiều vai trò trong dự án
description: Chủ đề này cung cấp thông tin về cách các thông số định giá có thể được sử dụng để hỗ trợ định giá và tính chi phí cho một nguồn lực đáp ứng được nhiều vai trò trong dự án.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087160"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Ước tính doanh thu và chi phí của dự án khi một nguồn lực có thể đặt trước đáp ứng nhiều vai trò trong dự án 

Các công ty dựa trên dự án thường có nhu cầu về một nguồn lực đảm nhiệm được nhiều vai trò trong một dự án. Mỗi vai trò này có thể được định giá và tính chi phí khác nhau, có nghĩa là thời gian của cùng nguồn lực trong dự án có thể nhận được ước tính tài chính khác nhau tùy thuộc vào hóa đơn và chi phí cho mỗi vai trò. Project Service Automation cho phép thiết lập các giá trị trên bản ghi thành viên nhóm cho tài nguyên được đặt tên và cho phép các nội dung ghi đè khác nhau đối với từng nhiệm vụ mà thành viên nhóm được phân công.

Ví dụ sau giải thích cách ghi đè đơn giản của giá trị này cho phép một nguồn lực có nhiều vai trò trong dự án với các mức chi phí và hóa đơn khác nhau.

## <a name="create-tasks"></a>Tạo nhiệm vụ
Tạo hai nhiệm vụ dự án, mỗi nhiệm vụ 40 giờ, Nhiệm vụ A và Nhiệm vụ B. Chọn Nhiệm vụ A là nhiệm vụ trước Nhiệm vụ B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Thiết lập vai trò và đơn vị tổ chức cho một thành viên nhóm dự án chung

1. Trên trang **Lịch trình** , chọn hàng **Nhiệm vụ** cho Nhiệm vụ A. 
2. Trong trường **Nguồn lực** , chọn **Tạo** trong danh sách thả xuống.
3. Trên trang **Tạo nhanh thành viên nhóm** , chỉ định thuộc tính của thành viên nhóm chung có thể thực hiện nhiệm vụ này.
4. Chọn vai trò và đơn vị tổ chức thích hợp, sau đó chọn **Lưu và đóng**. Một thành viên nhóm chung được tạo và phân công nhiệm vụ này. 

Lặp lại các bước này cho Nhiệm vụ B và đảm bảo rằng vai trò và đơn vị tổ chức của thành viên nhóm chung được tạo cho Nhiệm vụ B khác với Nhiệm vụ A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Thiết lập vai trò và đơn vị tổ chức cho nhiệm vụ dự án

1. Sau khi bạn tạo Nhiệm vụ A, hãy chọn nhiệm vụ, sau đó chọn **Chỉnh sửa nhiệm vụ**.
2. Trên trang **Chi tiết nhiệm vụ** , tìm trường **Vai trò** và **Đơn vị tổ chức** , thêm các giá trị bắt buộc của nguồn lực sẽ thực hiện nhiệm vụ này. 

  > [!NOTE]
  > Nếu bạn đang hoàn thành kịch bản này bằng cách sử dụng dữ liệu demo Project Service Automation, hãy chọn **Trưởng nhóm tư vấn** cho vai trò và **Fabrikam US** là đơn vị tổ chức.

3. Chọn Nhiệm vụ B và sau đó chọn **Chỉnh sửa nhiệm vụ**.
4. Trên trang **Chi tiết nhiệm vụ** , tìm trường **Vai trò** và **Đơn vị tổ chức** , thêm các giá trị bắt buộc của nguồn lực sẽ thực hiện nhiệm vụ này. Đảm bảo rằng các giá trị trong trường **Vai trò** và **Đơn vị tổ chức** của Nhiệm vụ B khác với Nhiệm vụ A. 

  > [!NOTE]
  > Nếu bạn đang hoàn thành kịch bản này bằng cách sử dụng dữ liệu demo Project Service Automation, hãy chọn **Kỹ thuật viên mạng** cho vai trò và **Fabrikam US** là đơn vị tổ chức.

5. Lưu và đóng trang **Chi tiết nhiệm vụ**. 

## <a name="team-member-and-estimates-behaviour"></a>Thành viên nhóm và hành vi ước tính 

1. Trên trang **Chi tiết nhiệm vụ** , trên **Thành viên nhóm** , chọn hai Thành viên nhóm rồi chọn **Tạo yêu cầu**. Thao tác này sẽ tạo yêu cầu về nguồn lực. 
2. Chọn hàng thành viên nhóm cho **Trưởng nhóm tư vấn** rồi chọn **Đặt trước**. Bảng lịch trình mở ra và đặt trước một nguồn lực cho yêu cầu đó.
3. Chọn hàng thành viên nhóm cho **Kỹ thuật viên mạng** rồi chọn **Đặt trước**. Bảng lịch trình mở ra và đặt trước cùng nguồn lực cho yêu cầu đó.

### <a name="team-member-grid"></a>Lưới Thành viên nhóm 
Trên lưới **Thành viên nhóm** , hãy lưu ý rằng có 2 bản ghi thành viên nhóm chung bị xóa và được thay thế bằng một nguồn lực. Có một bộ giá trị cho nguồn lực đó cho thấy bộ giá trị mặc định cho **Vai trò** và **Đơn vị tổ chức**.
Khi bạn mở rộng hàng của bản ghi Thành viên nhóm đó, bạn có thể thấy các nhiệm vụ riêng biệt trên bản ghi thành viên nhóm cho cả hai nhiệm vụ đó. Mỗi hàng phân công có các giá trị cụ thể cho nhiệm vụ đối với **Vai trò** và **Đơn vị tổ chức**. 

### <a name="estimates-grid"></a>Lưới ước tính 
Khi bạn điều hướng đến lưới **Ước tính** , bạn sẽ nhận thấy rằng cả hai mục phân công cho cùng một nguồn lực có giá khác nhau.
Việc phân công nguồn lực trong Nhiệm vụ A được định giá bằng giá trị thuộc tính **Vai trò** của **Trưởng nhóm tư vấn**. Việc phân công nguồn lực đó trong Nhiệm vụ B được định giá bằng giá trị thuộc tính **Vai trò** của **Kỹ thuật viên mạng**.




