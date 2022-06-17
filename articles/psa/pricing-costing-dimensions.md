---
title: Trang chủ tham số giá và chi phí
description: Bài viết này cung cấp tổng quan về các thứ nguyên đặt giá.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 88c77d90bccaa5f10e8f75d60ae121d699bc0976
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925468"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Trang chủ tham số giá và chi phí

[!include [banner](../includes/psa-now-project-operations.md)]

Các thông số được sử dụng để đặt giá và tính chi phí nhân công trong các tổ chức dựa trên dự án chịu ảnh hưởng của các thuộc tính sau:

- Những người làm công việc giống với kinh nghiệm, vai trò hoặc vị trí địa lý của họ
- Công việc được thực hiện tương tự với mức độ phức tạp hoặc thời gian trong ngày

Do tính chất điển hình của các loại công việc này và những người cần thiết để thực hiện công việc, có hai loại giá trị thông số định giá có sẵn trong Project Service Automation: 

- **Bộ tùy chọn** - Thuộc tính là các số liệu liệt kê cố định cho một bộ giá trị.
- **Giá trị dựa trên thực thể** - Các thuộc tính có thể có một bộ giá trị đa dạng là hữu hạn nhưng có thể thay đổi theo thời gian.

## <a name="pricing-dimensions"></a>Thông số định giá

PSA vận chuyển với một bộ tham số giá mặc định. Bạn có thể xem các tham số này bằng các chuyển đến **Project Service** > **Tham số**. Trong bản ghi tham số, trên tab **Tham số giá dựa trên số tiền**, hãy xác minh rằng vai trò **msdyn_resourcecategory** và đơn vị tổ chức nguồn lực **msdyn_organizationalunit** có các trường **Áp dụng cho bán hàng** và **Áp dụng cho chi phí** được đặt thành **Có**. Điều này sẽ cho phép bạn thiết lập giá cả và chi phí cho mỗi kết hợp vai trò và đơn vị tổ chức.

![Ảnh chụp màn hình của tham số Project Service với "Áp dụng cho bán hàng" được đánh dấu.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Nếu bạn đã dùng các trường sẵn dùng của vai trò và đơn vị tổ chức ở dạng tham số giá trước phiên bản 3 của PSA, thì sẽ không có thay đổi nào có thể quan sát được. Bạn có thể tiếp tục sử dụng Project Service như bình thường. 

Nếu cần giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung, bạn có thể tạo các trường, thực thể và tham số tùy chỉnh. Để biết thêm thông tin, hãy xem các bài viết sau, tuy nhiên lưu ý rằng bạn phải hoàn thành các thủ tục theo thứ tự được liệt kê bên dưới:

- [Tạo các trường và thực thể tùy chỉnh](create-custom-fields-entities.md)
- [Thêm các trường tùy chỉnh vào thực thể thiết lập và giao dịch](field-references.md)
- [Thiết lập trường tùy chỉnh làm thông số định giá ](set-up-pricing-dimensions.md)
- [Cập nhật các thuộc tính phần bổ trợ để bao gồm tham số giá mới](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Định giá thời gian nguồn nhân lực
Cách một tổ chức định giá thời gian nguồn nhân lực thường là một cân nhắc quan trọng mang tính chiến lược ảnh hưởng trực tiếp đến lợi nhuận của tổ chức. Làm việc với các đội ngũ tài chính và người đứng đầu phụ trách thực hành khi tổ chức của bạn sẵn sàng xác định cách mong muốn để thiết lập tỷ lệ chi phí và hóa đơn cho thời gian nguồn nhân lực.

Các cân nhắc khác về giá bao gồm việc có tái sử dụng trường hoặc thực thể không phải là tham số giá hiện tại nhưng áp dụng dưới dạng tham số giá cho tổ chức của bạn hay không. Các trường như **Loại giao dịch** (**msdyn_transactioncategory**) và **Nguồn lực có thể đăng ký** (**bookableresource**) là các ví dụ về tham số của ứng viên. 

Bạn cũng nên cân nhắc xem liệu tham số định giá nên ở dạng bảng biểu hay bộ tùy chọn. Nếu thấy trước các thay đổi về giá trị của tham số sẽ vượt quá 10 hoặc 12 và bạn cần các thuộc tính bổ sung trên các giá trị này, hãy tạo một thực thể thay vì bộ tùy chọn. Duy trì một bộ tùy chọn, chẳng hạn như thêm hoặc loại bỏ các giá trị, yêu cầu một quản trị viên hoặc nhà phát triển trong khi thêm hàng mới vào bảng có thể được hầu hết người dùng doanh nghiệp thực hiện.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
