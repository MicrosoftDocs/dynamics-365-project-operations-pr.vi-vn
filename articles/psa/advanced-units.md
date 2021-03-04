---
title: Nhóm đơn vị và đơn vị
description: Chủ đề này cung cấp thông tin về nhóm đơn vị đo và đơn vị đo.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145609"
---
# <a name="unit-groups-and-units"></a>Nhóm đơn vị và đơn vị

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nhóm đơn vị đo và đơn vị đo là các thực thể cơ bản trong Microsoft Dynamics 365. Một đơn vị là một đơn vị đo lường và nhiều đơn vị đo có thể nhóm thành nhóm đơn vị đo. Nhóm đơn vị đôi khi được gọi là lịch đơn vị trong giao diện người dùng (UI) Dynamics 365. 

Dưới đây là một số ví dụ về các đơn vị và nhóm đơn vị đo:
 
- **Nhóm đơn vị đo**: Khoảng cách 
    - **Đơn vị**: Dặm, Km, v.v.
- **Nhóm đơn vị đo**: Thời gian
    - **Đơn vị**: Giờ, ngày, tuần, v.v. 

Khi bạn thiết lập nhiều đơn vị trong một nhóm đơn vị, bạn cũng phải thiết lập một hệ số chuyển đổi giữa chúng bằng cách chỉ định đơn vị đầu tiên mà bạn thiết lập làm đơn vị chính hoặc mặc định cho nhóm đơn vị đo. 

Ví dụ: trong nhóm đơn vị đo **Thời gian**, nếu bạn thiết lập **Giờ** làm đơn vị đầu tiên, thì hệ thống sẽ chỉ định **Giờ** là đơn vị mặc định. Nếu đơn vị tiếp theo mà bạn thiết lập là **Ngày**, thì bạn phải thiết lập một hệ số chuyển đổi cho **Ngày** thành **Giờ**. Nếu sau đó bạn thêm **Tuần** làm đơn vị thứ ba, thì bạn phải thiết lập một hệ số chuyển đổi cho **Tuần** theo **Ngày** hoặc **Giờ**. 

Hình ảnh sau đây minh họa một thiết lập ví dụ cho đơn vị **Ngày**, trong đó trường **Số lượng** hiển thị số giờ trong một ngày và **Tuần**, trong đó trường **Số lượng** hiển thị số ngày trong một tuần.

> ![Nhóm đơn vị đo: Trang thông tin](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Sử dụng đơn vị và nhóm đơn vị đo

Dynamics 365 Project Service Automation sử dụng các đơn vị và nhóm đơn vị để xử lý các ước tính và mục nhập cho cả chi phí và thời gian. 

Đối với chi phí, mỗi loại chi phí có nhóm đơn vị và đơn vị mặc định. Các giá trị này được nhập như giá trị mặc định trên mục nhập bảng giá cho loại chi phí. 

Ví dụ: bạn có một loại chi phí có tên **Quãng đường**. Nó có một nhóm đơn vị có tên là **Khoảng cách** và một đơn vị mặc định là **Dặm**. Nếu bạn thiết lập nhóm đơn vị đo **Khoảng cách** để nó có hai đơn vị (**Dặm** và **Km**), bạn có thể đặt hai giá cho danh mục **Quãng đường** trên một bảng giá: giá mỗi dặm và giá mỗi km.

| Thể loại chi phí  | Nhóm đơn vị đo  | Đơn vị      | Phương pháp định giá  | Đơn giá  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Số dặm           | Khoảng cách      | Dặm      | Đơn giá    | 10 USD            |
| Số dặm           | Khoảng cách      | Kilômét | Đơn giá    |  6 USD            |

Khi bạn nhập một chi phí vào dự án, hệ thống sẽ xác định giá thông qua tổ hợp các thể loại và đơn vị trên chi phí. 

| Mô tả chi phí        | Thể loại chi phí  | Đơn vị  | Số lượng  | Đơn giá   |
|----------------------------|---------------------|-------|-----------|----------------|
| Lái xe đến vị trí khách hàng | Số dặm             | Dặm  | 10        | 10 USD         |

Đối với thời gian, mỗi tiêu đề bảng giá đều có trường **Đơn vị thời gian mặc định**. Giá trị được đặt khi bạn tạo tiêu đề bảng giá. Sau đó, đơn vị này được sử dụng để thiết lập tất cả các giá dựa trên vai trò trên bảng giá đó.

Các dòng ước tính cho trường **Thời gian trên báo giá** có thể được thể hiện ở bất kỳ đơn vị thời gian nào. Tuy nhiên, dòng ước tính trên dự án và mục nhập thời gian cho dự án chỉ có thể sử dụng đơn vị thời gian là **Giờ**. Nếu đơn vị trên mục nhập thời gian hoặc dòng ước tính không khớp với đơn vị trên dòng bảng giá cho vai trò đó, thì hệ thống sẽ chuyển đổi giá sang đơn vị được xác định trên ước tính dự án hoặc giao dịch thực tế của dự án.

Ví dụ sau cho thấy cách PSA sử dụng nhóm đơn vị đo, đơn vị và hệ số chuyển đổi.
- Đơn vị

   - **Nhóm đơn vị đo**: Thời gian 
   - **Đơn vị**: Giờ 
    
    - **Ngày** - Hệ số chuyển đổi: 8 giờ       
    - **Tuần** - Hệ số chuyển đổi: 40 giờ  
        
- Thiết lập bảng giá trên dự án A:

    - **Tên**: Giá bán hàng ở Anh năm 2016 
    - **Đơn vị thời gian mặc định**: Ngày 
    - **Tiền tệ**: GBP

| Vai trò      | Nhóm đơn vị đo | Đơn vị | Đơn vị tổ chức | Giá   |
|-----------|------------|------|---------------------|---------|
| Nhà phát triển | Time       | Day  | Contoso Hoa Kỳ          | 800 GBP |

### <a name="time-entry"></a>Mục nhập thời gian

Bảng sau hiển thị các giao dịch phía bán hàng tạo ra bởi PSA cho một dự án ba giờ.


| Dự án   | Nhiệm vụ    | Vai trò      | Số lượng | Đơn vị  | Đơn giá | Số tiền bán hàng chưa lập hóa đơn |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Dự án A | Thiết kế  | Nhà phát triển | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Câu hỏi thường gặp về đơn vị thời gian

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>PSA có chuyển đổi sang các đơn vị khác trong trường hợp chi phí không?
Không. Chuyển đổi đơn vị chỉ hoạt động cho thời gian. Đối với chi phí, nếu hệ thống không thể tìm thấy giá cho tổ hợp loại chi phí và đơn vị, thì giá sẽ được đặt thành 0,00 theo mặc định.

### <a name="why-does-psa-convert-time-units"></a>Tại sao PSA chuyển đổi đơn vị thời gian?
Ở một số quốc gia hoặc khu vực, có một yêu cầu pháp lý rằng tỉ suất hóa đơn được thiết lập theo ngày. Đám phán giá và giảm giá trong chu kỳ báo giá được thực hiện bằng cách sử dụng tỉ suất ngày cho mỗi vai trò có thể lập hóa đơn. Ước tính lịch trình và mục nhập thời gian được thực hiện theo giờ. Để hỗ trợ sự khác biệt này theo đơn vị thời gian, PSA sẽ quy đổi đơn vị thời gian.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Có thể thay đổi đơn vị thời gian trên ước tính dự án không?
Không. Ước tính lịch trình hiện bị giới hạn ở giờ và không thể thay đổi.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Có thể chỉnh sửa, xóa và thêm đơn vị cũng như nhóm đơn vị đo không?
Có chứ. Trừ trường hợp nhóm đơn vị đo **Thời gian** và đơn vị **Giờ**, có thể xóa hoặc chỉnh sửa tất cả các đơn vị, đồng thời có thể thêm đơn vị mới. Trong PSA, không thể xóa nhóm đơn vị đo **Thời gian** và đơn vị **Giờ**. Tuy nhiên, có thể cập nhật các đơn vị này bằng một văn bản đã dịch cho trường **Tên**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]