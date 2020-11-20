---
title: Mẫu dự án
description: Chủ đề này cung cấp thông tin về cách sử dụng mẫu dự án để thiết lập dự án nhanh chóng.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123066"
---
# <a name="project-templates"></a>Mẫu dự án 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Mẫu dự án là một khuôn khổ được xác định trước giúp bạn nhanh chóng và dễ dàng bắt đầu một dự án. Bạn có thể sử dụng một mẫu được xác định trước để tạo dự án mới chỉ bằng một cú bấm chuột. Như đối với dự án, bạn phải xác định điều kiện tiên quyết cho mẫu dự án. Bạn phải xác định lịch dự án cho từng mẫu dự án, và vai trò cũng như bảng giá phải được xác định trước trong tổ chức để các thành phần của mẫu có dữ liệu hữu ích.

Mẫu dự án bao gồm ba thành phần: lịch trình, ước tính dự án và các thành viên nhóm dự án.

## <a name="schedule"></a>Lịch trình

Lịch trình trong mẫu dự án có cùng bộ thành phần như lịch trình trong dự án. Bạn có thể tạo một hệ thống cấp bậc nhiệm vụ, liên kết vai trò với nhiệm vụ, xác định thuộc tính lịch trình và đặt mức phụ thuộc. Lịch trình trong mẫu dự án cũng hỗ trợ các chế độ nhiệm vụ cho từng nhiệm vụ. Do đó, lịch trình hỗ trợ các công cụ lập lịch. Bạn phải liên kết lịch trình dự án với dự án. Khi bạn tạo lịch trình công việc, không có sự khác biệt giữa mẫu dự án và dự án.

## <a name="project-estimates"></a>Ước tính dự án

Ước tính dự án trong một mẫu dự án hoạt động theo cách tương tự như ước tính dự án trong một dự án. Tuy nhiên, chi phí và giá bán được lấy từ bảng giá bán và chi phí mặc định được xác định trong các tham số.

## <a name="creating-a-project-from-a-template"></a>Tạo dự án từ mẫu
 
Có một số cách để tạo một dự án từ một mẫu dự án:

- Khi tạo dự án từ báo giá, bạn có thể chọn mẫu dự án trong hộp thoại **Tạo nhanh: Dự án**.

> ![Hộp thoại Tạo nhanh: Dự án](media/project-11.png)

- Khi bạn tạo một dự án bằng cách chọn **Dự án mới**, trang **Dự án** xuất hiện trước khi bản ghi được lưu. Trong trường **Chọn mẫu**, hãy chọn một trong các mẫu dự án đã xác định trước trong tổ chức.
- Sử dụng **Tạo dự án từ mẫu** trên trang **Thực thể mẫu**.

## <a name="copying-components-of-template-to-project"></a>Sao chép các thành phần của một mẫu vào dự án

Khi bạn sao chép các cấu phần của một mẫu dự án vào dự án, một vài thao tác thay thế có thể xảy ra, tuỳ thuộc vào thiết đặt trong dự án.

### <a name="copying-the-schedule"></a>Sao chép lịch trình

Khi bạn sao chép lịch trình từ mẫu dự án, nếu dự án có lịch trình dự án khác thay vì mẫu, giờ làm việc từ lịch của dự án đã được áp dụng cho lịch trình dự án. Trong cách này, lịch trình được điều chỉnh để khớp với lịch dự án hỗ trợ. Tương tự, nhiệm vụ đầu tiên trên lịch trình lấy ngày bắt đầu của dự án và lịch trình của phần còn lại của hệ thống cấp bậc được cập nhật dựa trên khoảng thời gian và mức phụ thuộc được chỉ định trong mẫu. 

### <a name="copying-project-estimates"></a>Sao chép ước tính dự án 

Khi bạn sao chép trên các mô tả ước tính dự án, bảng giá sẽ được cập nhật. Đối với bảng giá chi phí, những thông tin cập nhật này dựa trên đơn vị sở hữu của dự án. Đối với bảng giá bán, những thông tin cập nhật này dựa trên khách hàng. Đối với dự án liên kết với thực thể bán hàng, giá bán và chi phí được xác định dựa trên các bảng giá này.

### <a name="copying-a-project-team"></a>Sao chép một nhóm dự án

Khi nhóm dự án được sao chép từ mẫu dự án vào dự án, nguồn lực chung được sao chép cùng với kỹ năng và mức độ thành thạo được xác định trong mẫu. Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong mẫu dự án. Nguồn lực có tên không được hỗ trợ trong mẫu dự án.
