---
title: Tổng quan về ước tính dự án
description: Chủ đề này cung cấp thông tin về các ước tính trong Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d35be82563515adbba2c22402a751ed3daca8f83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131594"
---
# <a name="estimate-projects-overview"></a>Tổng quan về ước tính dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trên báo giá dựa trên dự án, bạn có thể sử dụng thực thể **Chi tiết dòng Báo giá** để ước tính công việc cần thiết cung cấp cho dự án. Sau đó, bạn có thể chia sẻ ước tính đó với khách hàng.

Các dòng báo giá dựa trên dự án không cần phải có nhiều chi tiết dòng báo giá. Chi tiết dòng báo giá được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. Microsoft Dynamics 365 Project Operations không cho phép các ước tính vật tư trên chi tiết dòng báo giá. Chúng được gọi là các lớp giao dịch. Ước tính số tiền thuế cũng có thể được nhập vào một lớp giao dịch.

Ngoài các lớp giao dịch, chi tiết dòng báo giá còn có một loại giao dịch. Hai loại giao dịch được hỗ trợ cho chi tiết dòng báo giá là: **Chi phí** và **Hợp đồng dự án**.

## <a name="estimate-by-using-a-contract"></a>Ước tính bằng cách sử dụng hợp đồng

Nếu bạn sử dụng một báo giá khi tạo một hợp đồng dựa trên dự án, ước tính mà bạn đã thực hiện cho mỗi dòng báo giá trên báo giá sẽ được sao chép vào hợp đồng dự án. Cấu trúc của một hợp đồng dự án giống như cấu trúc của báo giá dự án có các dòng, chi tiết về dòng và lịch trình hóa đơn.

Ước tính có thể được thực hiện trực tiếp trong một hợp đồng dự án, như trong một báo giá dự án. Đối với một báo giá dự án, ước tính được thực hiện bằng cách sử dụng các dòng hợp đồng và chi tiết dòng hợp đồng. Chi tiết dòng hợp đồng cũng có thể được tạo từ một kế hoạch dự án được tạo bằng cách sử dụng phương pháp ước tính doanh thu.

Chi tiết dòng hợp đồng có thể được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. Ước tính số tiền thuế cũng có thể được nhập vào chi tiết dòng hợp đồng.

Không cho phép các ước tính vật tư trên chi tiết dòng hợp đồng.

Quy trình được hỗ trợ trên hợp đồng dự án là tạo và xác nhận hóa đơn. Tạo hóa đơn sẽ tạo một bản nháp của một hóa đơn dựa trên dự án bao gồm tất cả doanh thu bán hàng chưa lập hóa đơn cho đến ngày hiện tại.

Xác nhận khiến hợp đồng chuyển sang trạng thái chỉ đọc và từ **Bản nháp** thành **Đã xác nhận**. Sau khi bạn thực hiện hành động này, bạn không thể hoàn tác nó. Bởi vì hành động này là vĩnh viễn, bạn nên duy trì hợp đồng ở trạng thái **Bản nháp**.

Sự khác biệt duy nhất giữa hợp đồng bản nháp và hợp đồng đã xác nhận là trạng thái của chúng và sự thật rằng hợp đồng bản nháp có thể chỉnh sửa trong khi hợp đồng đã xác nhận thì không thể. Có thể tạo hóa đơn và theo dõi doanh thu trên cả hợp đồng bản nháp và hợp đồng đã xác nhận.

Project operations không hỗ trợ thay đổi đơn đặt hàng trên hợp đồng hoặc dự án.

## <a name="estimating-projects"></a>Ước tính dự án

Bạn có thể ước tính thời gian và chi phí cho dự án. Project operations không cho phép ước tính vật tư hoặc phí trên dự án.

Ước tính thời gian được tạo khi bạn tạo một nhiệm vụ và xác định các thuộc tính cho một tài nguyên chung cần có để thực hiện nhiệm vụ. Ước tính thời gian được tạo từ nhiệm vụ theo lịch. Ước tính thời gian không được tạo nếu bạn tạo các thành viên nhóm chung bên ngoài ngữ cảnh của lịch biểu.

Ước tính chi phí được nhập vào lưới trên trang **Ước tính**.

## <a name="understanding-estimation"></a>Tìm hiểu về ước tính

Sử dụng bảng sau đây làm hướng dẫn để hiểu rõ logic công việc trong giai đoạn ước tính.

| Kịch bản                                                                                                                                                                                                                                                                                                                                          | Bản ghi thực thể                                                                                                                                                                                                       | Loại Giao dịch | Lớp Giao dịch | Thông tin bổ sung                                                            |
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
