---
title: Khái niệm về dự toán tài chính
description: Bài viết này cung cấp thông tin về ước tính tài chính của các dự án trong Hoạt động Dự án.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931034"
---
# <a name="financial-estimation-concepts"></a>Khái niệm về dự toán tài chính

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, bạn có thể dự toán tài chính cho các dự án của mình theo hai giai đoạn: 
1. Trong giai đoạn trước bán hàng trước khi đạt được thoả thuận. 
2. Trong giai đoạn thực hiện sau khi tạo hợp đồng dự án. 

Bạn có thể tạo dự toán tài chính cho công việc dựa trên dự án bằng cách sử dụng bất kỳ trang nào trong 3 trang sau:
- Trang **Mô tả báo giá**, sử dụng chi tiết mô tả báo giá.  
- Trang **Mô tả hợp đồng dự án**, sử dụng chi tiết mô tả hợp đồng. 
- Trang **Dự án**, sử dụng các trang tab **Nhiệm vụ** hoặc **Ước tính chi phí**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Sử dụng báo giá dự án để tạo ước tính
Trên báo giá dựa trên dự án, bạn có thể sử dụng thực thể **Chi tiết dòng Báo giá** để ước tính công việc cần thiết cung cấp cho dự án. Sau đó, bạn có thể chia sẻ ước tính đó với khách hàng.

Các dòng báo giá dựa trên dự án không cần phải có nhiều chi tiết dòng báo giá. Chi tiết dòng báo giá được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. Microsoft Dynamics 365 Project Operations không cho phép ước tính vật tư trên chi tiết dòng báo giá. Chúng được gọi là các lớp giao dịch. Ước tính số tiền thuế cũng có thể được nhập vào một lớp giao dịch.

Ngoài các lớp giao dịch, chi tiết dòng báo giá còn có một loại giao dịch. Hai loại giao dịch được hỗ trợ cho chi tiết dòng báo giá là: **Chi phí** và **Hợp đồng dự án**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Sử dụng hợp đồng dự án để tạo ước tính

Nếu bạn sử dụng một báo giá khi tạo một hợp đồng dựa trên dự án, ước tính mà bạn đã thực hiện cho mỗi dòng báo giá trên báo giá sẽ được sao chép vào hợp đồng dự án. Cấu trúc của một hợp đồng dự án giống như cấu trúc của báo giá dự án có các dòng, chi tiết về dòng và lịch trình hóa đơn.

Ước tính có thể được thực hiện trực tiếp trong một hợp đồng dự án, như trong một báo giá dự án. Đối với một báo giá dự án, ước tính được thực hiện bằng cách sử dụng các dòng hợp đồng và chi tiết dòng hợp đồng. Chi tiết dòng hợp đồng cũng có thể được tạo từ một kế hoạch dự án được tạo bằng cách sử dụng phương pháp ước tính doanh thu.

Chi tiết dòng hợp đồng có thể được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. Ước tính số tiền thuế cũng có thể được nhập vào chi tiết dòng hợp đồng.

Không cho phép các ước tính vật tư trên chi tiết dòng hợp đồng.

## <a name="use-a-project-to-create-an-estimate"></a>Sử dụng dự án để tạo ước tính 

Bạn có thể ước tính thời gian và chi phí cho dự án. Project Operations không hỗ trợ ước tính vật tư hoặc phí cho các dự án.

Ước tính thời gian được tạo khi bạn tạo một nhiệm vụ và xác định các thuộc tính cho một tài nguyên chung cần có để thực hiện nhiệm vụ. Ước tính thời gian được tạo từ nhiệm vụ theo lịch. Ước tính thời gian không được tạo nếu bạn tạo các thành viên nhóm chung bên ngoài ngữ cảnh của lịch biểu.

Chi phí ước tính được nhập vào lưới trên trang **Ước tính chi phí**.

Tạo giá trị ước tính cho một dự án được coi là phương pháp hay nhất vì bạn có thể xây dựng các giá trị ước tính chi tiết từ dưới lên cho nhân công hoặc thời gian và chi phí cho từng nhiệm vụ trong kế hoạch dự án. Sau đó, bạn có thể sử dụng giá trị ước tính chi tiết này để tạo các giá trị ước tính cho từng mục mô tả báo giá và xây dựng báo giá đáng tin cậy hơn cho khách hàng. Khi bạn nhập hoặc tạo giá trị ước tính chi tiết trên mục mô tả báo giá bằng cách sử dụng kế hoạch dự án, Project Operations sẽ nhập giá trị bán hàng và giá trị chi phí của những giá trị ước tính này. Sau khi nhập, bạn có thể xem các chỉ số về lợi nhuận, lợi nhuận biên và tính khả thi trên báo giá dự án.

## <a name="understanding-estimates"></a>Tìm hiểu về các giá trị ước tính

Sử dụng bảng sau đây làm hướng dẫn để hiểu rõ logic nghiệp vụ trong giai đoạn ước tính.

| Kịch bản                                                                                                                                                                                                                                                                                                                                          | Bản ghi thực thể                                                                                                                                                                                                       | Loại Giao dịch | Lớp giao dịch | Thông tin bổ sung                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Khi bạn cần ước tính giá trị thời gian bán hàng trên báo giá                                                                                                                                                                                                                                                                                    | Bản ghi chi tiết dòng báo giá (QLD) được tạo                                                                                                                                                                               | Hợp đồng dự án | Time        | Trường nguồn giao dịch trên hàng QLD phía bán hàng sẽ tham chiếu QLD phía chi phí |
|                                                                                                                                                                                                                                                                                     | Bản ghi QLD thứ hai được tạo bởi hệ thống để lưu trữ giá trị chi phí tương ứng. Tất cả các trường không phải là tiền được sao chép từ QLD bán hàng sang chi phí QLD bởi hệ thống.                                                                                                                                                                               | Chi phí | Time        | Trường nguồn giao dịch trên hàng chi tiết dòng báo giá (QLD) phía bán hàng sẽ tham chiếu QLD phía chi phí |
| Khi bạn cần ước tính giá trị thời gian bán hàng trên một hợp đồng                                                                                                                                                                                                                                                                                 | Bản ghi chi tiết dòng hợp đồng dự án (CLD) được tạo                                                                                                                                                                    | Hợp đồng Dự án | Time        | Trường nguồn giao dịch trên hàng CLD phía bán hàng sẽ tham chiếu CLD chi phí      |
|                                                                                                                                                                                                                                                                                  | Bản ghi CLD thứ hai được tạo bởi hệ thống để lưu trữ giá trị chi phí tương ứng. Tất cả các trường không phải là tiền được sao chép từ CLD bán hàng sang CLD chi phí bởi hệ thống.                                                                                                                                                                    | Chi phí | Time        | Trường nguồn giao dịch trên hàng CLD phía bán hàng sẽ tham chiếu CLD chi phí      |
| Khi người dùng mô tả tài nguyên trên một tác vụ dự án                                                                                                                                                                                                                                                                                            | Bản ghi dòng ước tính để hiển thị giá trị nhiệm vụ bán hàng được tạo khi một nhiệm vụ được tạo với tất cả các kích thước giá cần thiết. Vai trò và đơn vị tổ chức là các kích thước giá | Hợp đồng dự án | Thời gian        |                                                                                   |
|     | Bản ghi dòng ước tính để hiển thị giá trị chi phí của nhiệm vụ được tạo khi một nhiệm vụ được tạo với tất cả các kích thước giá cần thiết. Tất cả các trường không phải là tiền được sao chép từ dòng ước tính bán hàng sang dòng ước tính chi phí bởi hệ thống. Vai trò và đơn vị tổ chức là các kích thước giá cho cả chi phí và tỉ suất hóa đơn.                                                                                                                                                                                                                | Chi phí             | Thời gian           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tùy chỉnh thực thể chi tiết dòng Báo giá và chi tiết dòng Hợp đồng

Nếu bạn thêm một trường tùy chỉnh vào chi tiết dòng báo giá và muốn hệ thống nhập giá trị của trường dưới dạng một giá trị mặc định trên dòng chi phí liên quan mà nó tạo ra, hãy sử dụng công cụ đăng ký phần bổ trợ **PreOperationContractLineDetailUpdate** và **PreOperationQuoteLineDetailUpdate**. Phải đăng ký lại các phần bổ trợ này sau khi thay đổi chi tiết dòng báo giá hoặc chi tiết dòng hợp đồng. Làm theo các bước sau đây để hoàn thành quy trình.

1. Mở PluginRegistrationTool và kết nối với phiên bản trực tuyến của bạn.
2. Chọn **Tìm kiếm**, và tìm kiếm phần bổ trợ để cập nhật.
3. Chọn phần bổ trợ, sau đó, trên trang chính, nhấp vào **Chọn**.
4. Chọn bước trong phần bổ trợ để cập nhật, nhấp chuột phải, sau đó chọn **Cập nhật**.
5. Trong hộp thoại **Cập nhật bước hiện tại**, trong trường **Lọc thuộc tính**, chọn nút dấu chấm lửng (**...**):
6. Trong hộp thoại **Chọn thuộc tính**, chọn các hộp kiểm cho thuộc tính tùy chỉnh.
7. Chọn **OK** để đóng hộp thoại, và sau đó chọn **Bước cập nhật**.
8. Lặp lại các bước từ 1 đến 7 cho phần bổ trợ thứ hai.
9. Đóng **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
