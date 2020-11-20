---
title: Tổng quan về thông số định giá
description: Chủ đề này cung cấp thông tin về các tham số định giá trong Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128489"
---
# <a name="pricing-dimensions-overview"></a>Tổng quan về thông số định giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các tham số dùng trong nguồn nhân lực để thiết lập giá và chi phí rơi vào hai loại sau:

- Mọi người
- Công việc theo kế hoạch

Do vậy, có 2 loại giá trị tham số định giá được cung cấp:

- **Bộ tùy chọn**: Tham số là các số liệu liệt kê cố định cho một bộ giá trị.
- **Giá trị dựa trên thực thể**: Tham số có thể là bộ giá trị khác nhau.

## <a name="pricing-dimensions"></a>Thông số định giá

Dynamics 365 Project Operations đi kèm với một bộ tham số định giá mặc định. Bạn có thể xem các tham số định giá này bằng cách chuyển tới **Hoạt động dự án** > **Tham số**. Trong bản ghi tham số, trên tab **Tham số giá dựa trên số tiền**, hãy xác minh rằng vai trò **msdyn_resourcecategory** và đơn vị tổ chức nguồn lực **msdyn_organizationalunit** có các trường **Áp dụng cho bán hàng** và **Áp dụng cho chi phí** được đặt thành **Có**. Khi đã bật các trường này lên, bạn có thể thiết lập giá cả và chi phí cho từng tổ hợp vai trò và đơn vị tổ chức.

Nếu cần giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung, bạn có thể tạo các trường, thực thể và tham số tùy chỉnh.

## <a name="pricing-human-resource-time"></a>Định giá thời gian nguồn nhân lực
Cách một tổ chức định giá thời gian nguồn nhân lực thường là một cân nhắc quan trọng mang tính chiến lược ảnh hưởng trực tiếp đến lợi nhuận của tổ chức. Làm việc với các đội ngũ tài chính và người đứng đầu phụ trách thực hành khi tổ chức của bạn sẵn sàng xác định cách mong muốn để thiết lập tỷ lệ chi phí và hóa đơn cho thời gian nguồn nhân lực.

Các cân nhắc khác về giá bao gồm việc có tái sử dụng trường hoặc thực thể không phải là tham số giá hiện tại nhưng áp dụng dưới dạng tham số giá cho tổ chức của bạn hay không. Các trường như **Loại giao dịch** (**msdyn_transactioncategory**) và **Nguồn lực có thể đăng ký** (**bookableresource**) là các ví dụ về tham số của ứng viên. 

Bạn cũng nên cân nhắc xem liệu tham số định giá nên ở dạng bảng biểu hay bộ tùy chọn. Nếu thấy trước các thay đổi về giá trị của tham số sẽ vượt quá 10 hoặc 12 và bạn cần các thuộc tính bổ sung trên các giá trị này, bạn có thể tạo một thực thể thay vì bộ tùy chọn. Duy trì một bộ tùy chọn, chẳng hạn như thêm hoặc loại bỏ các giá trị, yêu cầu một quản trị viên hoặc nhà phát triển trong khi thêm hàng mới vào bảng có thể được hầu hết người dùng thực hiện.

Ví dụ sau cho thấy tỷ lệ hóa đơn được thiết lập dựa trên vai trò và đơn vị tổ chức nguồn lực mà nguồn lực thuộc về. Tỷ lệ chi phí thường dựa trên thang lương của nhân viên và đơn vị tổ chức mà họ thuộc về. Trong ví dụ này, các bảng tỷ lệ hóa đơn và tỷ lệ chi phí có dạng như sau.

**Tỷ lệ hóa đơn mẫu**

| Vai trò        | Đơn vị tổ chức    |Đơn vị      |Giá      |Tiền tệ  |
| ------------|-------------|----------|----------:|----------|
| Nhà phát triển   | Contoso US  |Hour | 200|Giải pháp USD     |
| Nhà phát triển   | Đàm Ấn Độ |Hour|   112|Giải pháp USD     |


**Tỷ lệ chi phí mẫu**

| Mức lương     | Đơn vị tổ chức    |Đơn vị      |Giá      |Tiền tệ  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hour | 145|Giải pháp USD     |
| My company_Band2 | Đàm Ấn Độ |Hour|   67|Giải pháp USD     |
