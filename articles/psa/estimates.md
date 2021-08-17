---
title: Ước tính
description: Chủ đề này cung cấp thông tin về ước tính trong Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
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
ms.openlocfilehash: ebb59d2b38bf99aed15206646e77c74003aba2a92a6d8d262e6e7b2017285ed3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992412"
---
# <a name="estimates"></a>Ước tính

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Trên báo giá dựa trên dự án, bạn có thể sử dụng thực thể chi tiết dòng Báo giá để ước tính công việc cần thiết nhằm cung cấp một dự án. Sau đó, bạn có thể chia sẻ ước tính đó với khách hàng.

Các dòng báo giá dựa trên dự án không cần phải có bất kỳ chi tiết dòng báo giá nào. Ngoài ra, chúng có thể có nhiều chi tiết dòng báo giá. Chi tiết dòng báo giá được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. PSA không cho phép các ước tính vật tư trên chi tiết dòng báo giá. Chúng được gọi là các lớp giao dịch. Ước tính số tiền thuế cũng có thể được nhập vào một lớp giao dịch.

Ngoài các lớp giao dịch, chi tiết dòng báo giá còn có một loại giao dịch. PSA hỗ trợ hai loại giao dịch đối với chi tiết dòng báo giá, đó là: **Chi phí** và **Hợp đồng dự án**.

## <a name="estimate-by-using-a-contract"></a>Ước tính bằng cách sử dụng hợp đồng

Nếu bạn sử dụng một báo giá PSA khi tạo một hợp đồng dựa trên dự án, ước tính mà bạn đã thực hiên cho mỗi dòng báo giá trên báo giá sẽ được sao chép vào hợp đồng dự án. Cấu trúc của một hợp đồng dự án giống như cấu trúc của báo giá dự án có các dòng, chi tiết về dòng và lịch trình hóa đơn.

Ước tính có thể được thực hiện trực tiếp trong một hợp đồng dự án, như trong một báo giá dự án. Đối với một báo giá dự án, ước tính được thực hiện bằng cách sử dụng các dòng hợp đồng và chi tiết dòng hợp đồng. Chi tiết dòng hợp đồng cũng có thể được tạo từ một kế hoạch dự án được tạo bằng cách sử dụng phương pháp ước tính doanh thu.

Chi tiết dòng hợp đồng có thể được sử dụng để ước tính thời gian, chi phí, hoặc lệ phí. Ước tính số tiền thuế cũng có thể được nhập vào chi tiết dòng hợp đồng.

PSA không cho phép các ước tính vật tư trên chi tiết dòng hợp đồng.

Quy trình được hỗ trợ trên hợp đồng dự án là tạo và xác nhận hóa đơn. Tạo hóa đơn sẽ tạo một bản nháp của một hóa đơn dựa trên dự án bao gồm tất cả doanh thu bán hàng chưa lập hóa đơn cho đến ngày hiện tại.

Xác nhận khiến hợp đồng chuyển sang trạng thái chỉ đọc và từ **Bản nháp** thành **Đã xác nhận**. Sau khi bạn thực hiện hành động này, bạn không thể hoàn tác nó. Bởi vì hành động này là vĩnh viễn, bạn nên duy trì hợp đồng ở trạng thái **Bản nháp**.

Sự khác biệt duy nhất giữa hợp đồng bản nháp và hợp đồng đã xác nhận là trạng thái của chúng và sự thật rằng hợp đồng bản nháp có thể chỉnh sửa trong khi hợp đồng đã xác nhận thì không thể. Có thể tạo hóa đơn và theo dõi doanh thu trên cả hợp đồng bản nháp và hợp đồng đã xác nhận.

PSA không hỗ trợ thay đổi đơn đặt hàng trên hợp đồng hoặc dự án.

## <a name="estimating-projects"></a>Ước tính dự án

Bạn có thể ước tính thời gian và chi phí cho dự án. PSA không cho phép ước tính vật tư hoặc phí trên dự án.

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
| Khi người dùng mô tả tài nguyên trên một tác vụ dự án                                                                                                                                                                                                                                                                                            | Bản ghi dòng ước tính để hiển thị giá trị nhiệm vụ bán hàng được tạo khi một nhiệm vụ được tạo với tất cả các kích thước giá cần thiết. Vai trò và đơn vị tổ chức là các kích thước giá của Project Service OOB | Hợp đồng Dự án | Time        |                                                                                   |
|     | Bản ghi dòng ước tính để hiển thị giá trị chi phí của nhiệm vụ được tạo khi một nhiệm vụ được tạo với tất cả các kích thước giá cần thiết. Tất cả các trường không phải là tiền được sao chép từ dòng ước tính bán hàng sang dòng ước tính chi phí bởi hệ thống. Vai trò và đơn vị tổ chức là các kích thước giá trị OOB PSA cho cả chi phí và tỉ suất hóa đơn.                                                                                                                                                                                                                | Chi phí             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Tùy chỉnh thực thể chi tiết dòng báo giá và chi tiết dòng hợp đồng

Nếu bạn thêm một trường tùy chỉnh vào chi tiết dòng báo giá và muốn hệ thống nhập giá trị của trường dưới dạng một giá trị mặc định trên dòng chi phí liên quan mà nó tạo ra, hãy sử dụng công cụ đăng ký phần bổ trợ PreOperationContractLineDetailUpdate và PreOperationQuoteLineDetailUpdate. Phải đăng ký lại các phần bổ trợ này sau khi thay đổi chi tiết dòng báo giá hoặc chi tiết dòng hợp đồng. Làm theo các bước sau đây để hoàn thành quy trình.

1. Mở PluginRegistrationTool và kết nối với phiên bản trực tuyến của bạn.
2. Chọn **Tìm kiếm**, và tìm kiếm phần bổ trợ để cập nhật.

    ![Hộp thoại Cây tìm kiếm.](media/basic-guide-19.png)

3. Chọn phần bổ trợ, sau đó, trên trang chính, chọn **Chọn**.
4. Chọn bước trong phần bổ trợ để cập nhật, nhấp chuột phải, sau đó chọn **Cập nhật**.

    ![Chọn một bước trong phần bổ trợ.](media/basic-guide-20.png)

5. Trong hộp thoại **Cập nhật bước hiện tại**, trong trường **Lọc thuộc tính**, chọn nút dấu chấm lửng (**...**):
 
    ![Hộp thoại cập nhật bước hiện có.](media/basic-guide-21.png)

6. Trong hộp thoại **Chọn thuộc tính**, chọn các hộp kiểm cho thuộc tính tùy chỉnh.

    ![Hộp thoại Chọn thuộc tính.](media/basic-guide-22.png)

7. Chọn **OK** để đóng hộp thoại, và sau đó chọn **Bước cập nhật**.
 
    ![Nút Bước cập nhật.](media/basic-guide-23.png)

8. Lặp lại các bước từ 1 đến 7 cho phần bổ trợ thứ hai.
9. Đóng PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]