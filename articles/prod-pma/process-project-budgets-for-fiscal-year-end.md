---
title: Chuyển ngân sách dự án vào cuối năm tài chính
description: Bài viết này cung cấp thông tin về cách chuyển số tiền ngân sách còn lại sang các năm trong tương lai và tạo chi tiết sổ đăng ký ngân sách.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008067"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Chuyển ngân sách dự án vào cuối năm tài chính

[!include [banner](../includes/banner.md)]

Khi thực hiện một dự án kéo dài nhiều năm, bạn có thể còn lại ngân sách vào cuối năm tài chính. Bạn có thể chuyển số tiền ngân sách còn lại sang một năm trong tương lai và tạo chi tiết sổ đăng ký ngân sách cho số tiền trong các tài khoản sổ cái liên quan. Trước khi bạn chuyển tiếp số tiền còn lại, hãy xem xét và phân tích số tiền ngân sách còn lại.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Xem xét và phân tích số tiền ngân sách còn lại

Hoàn thành các bước sau để xem xét số tiền ngân sách cuối năm cho các dự án, nhưng không chuyển số tiền này.

1. Đi đến **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**. 
2. Trên trang **Quy trình chuyển tiếp ngân sách dự án**, trên tab **Tùy chọn cuối năm**, xác minh rằng **Chuyển tiếp số tiền ngân sách dự án còn lại** không được kích hoạt.
3. Trên tab **Tham số**, trong trường **Năm ngân sách dự án**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại. 
4. Trong trường **Bắt đầu năm tài chính**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại. 
5. Trong trường **Từ mô hình dự báo**, chọn **Ngân sách còn lại**. 
6. Để bao gồm các dự án đáp ứng tiêu chí bạn đã chọn và không còn ngân sách, hãy chọn **Hiển thị không còn lại**.  
7. Trên tab **Chọn ngân sách**, chọn **Truy xuất tất cả ngân sách** để tải tất cả các ngân sách phù hợp với tiêu chí bạn đã chọn, sau đó chọn **Xử lý**. 
8. Để thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.

Để biết thêm thông tin về một dòng cụ thể trong ngăn, hãy chọn dòng, sau đó chọn **Xem chi tiết ngân sách** hoặc **Xem tài khoản**.

## <a name="carry-forward-remaining-budget-amounts"></a>Chuyển tiếp số tiền ngân sách còn lại 

Khi xử lý số tiền ngân sách còn lại, bạn có thể tạo các giao dịch trong sổ cái cho số tiền bạn đang chuyển tiếp. Để tạo các giao dịch sổ cái, hãy hoàn thành các bước trong phần [Chuyển tiếp số tiền ngân sách và tạo các giao dịch sổ cái](#carry-forward). 

> [!NOTE]
> Số tiền ngân sách chuyển tiếp được chuyển sang mô hình dự báo được chọn trong trang **Các mô hình dự báo** làm mô hình dự báo chuyển tiếp.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Chuyển tiếp số tiền ngân sách và tạo các giao dịch sổ cái

1.  Chọn **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**. 
2. Trên trang **Quy trình chuyển tiếp ngân sách dự án**, chọn **Cuối năm**, sau đó bật **Chuyển tiếp số tiền ngân sách dự án còn lại** và **Tạo mục đăng ký ngân sách trong sổ cái**. 
3. Trên tab **Tham số**, trong nhóm trường **Tham số dự án**, chọn các mục sau:

   - **Năm ngân sách dự án**: Chọn đầu năm tài chính mà bạn muốn xem số tiền ngân sách còn lại. 
   - **Lãi và lỗ**: Tạo giao dịch lãi và lỗ trong sổ cái. 
   -  **WIP**: Tạo các giao dịch Đang tiến hành (WIP) trong sổ cái.
   -  **Bảng lương**: Tạo giao dịch phân bổ bảng lương trong sổ cái. 

5. Trong nhóm trường **Sổ cái**, hãy cung cấp thông tin sau: 

   - Trong trường **Bắt đầu năm tài chính**, hãy chọn năm tài chính mà bạn muốn chuyển tiếp số tiền ngân sách còn lại cho dự án. Giá trị mặc định là một năm sau giá trị trong trường **Năm ngân sách dự án**.
   -  Trong trường **Kỳ chuyển tiếp**, chọn kỳ mà bạn muốn tạo chi tiết đăng ký nhật ký trong sổ cái. Đây thường là kỳ đầu tiên trong năm tài chính mở.

6. Trong nhóm trường **Sao chép từ/tới**, hãy cung cấp thông tin sau:

   - Trong trường **Từ mô hình dự báo**, chọn mô hình dự báo ngân sách dự án liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển cho dự án. 
   - Trong trường **Đến mô hình ngân sách sổ cái**, chọn mô hình ngân sách sổ cái liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển sang sổ cái. 
   -  Chọn **Chuyển đơn vị tiền tệ bán hàng** để sử dụng đơn vị tiền tệ bán hàng của dự án cho các giao dịch sổ cái được tạo khi bạn chuyển số tiền ngân sách cho dự án. Khi tùy chọn không được chọn, các giao dịch sẽ sử dụng đơn vị tiền tệ kế toán. 
   -  Chọn **Hiển thị không còn lại** để bao gồm các dự án không còn số tiền ngân sách, nhưng đáp ứng các tiêu chí khác mà bạn chọn trong các dự án được hiển thị ở ngăn dưới cùng.

7. Trên tab **Chọn ngân sách**, hãy chọn **Truy xuất tất cả ngân sách** để tải tất cả ngân sách phù hợp với tiêu chí bạn đã chọn. Nếu bạn muốn thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách dự án cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.
8. Đối với mỗi dự án mà bạn muốn xử lý, hãy chọn tùy chọn ở đầu dòng cho dự án.

    > [!TIP]
    > Để chọn tất cả hoặc hầu hết các dự án, hãy chọn dấu kiểm ở góc trên bên trái. Để loại trừ việc xử lý bất kỳ dự án nào, hãy xóa dấu kiểm cho dự án đó.

9. Để chuyển số tiền ngân sách còn lại cho các dự án đã chọn sang năm tài chính đã chọn và tạo chi tiết đăng ký ngân sách trong sổ cái, hãy chọn **Xử lý**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Chuyển tiếp số tiền ngân sách mà không tạo các giao dịch sổ cái

1. Đi đến **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**.
2. Trên trang **Quy trình chuyển tiếp ngân sách dự án**, trong trường **Tùy chọn cuối năm**, chọn **Chuyển tiếp số tiền ngân sách dự án còn lại**.
3. Trong nhóm **Tham số**, trong trường **Năm ngân sách dự án**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại.
4. Trong nhóm **Sao chép từ/tới**, hãy cung cấp thông tin sau:

   - Trong trường **Từ mô hình dự báo**, chọn mô hình dự báo ngân sách dự án liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển cho dự án. 
   - Chọn **Hiển thị không còn lại** để bao gồm các dự án không còn ngân sách, nhưng đáp ứng các tiêu chí khác mà bạn đã chọn.
   - Trong nhóm **Chọn ngân sách**, hãy chọn **Truy xuất tất cả ngân sách** để tải tất cả ngân sách phù hợp với tiêu chí bạn đã chọn. Để thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách dự án cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.

5. Đối với mỗi dự án mà bạn muốn xử lý, hãy chọn tùy chọn ở đầu dòng cho dự án. 
6. Chọn **Xử lý** để chuyển số tiền ngân sách còn lại cho các dự án đã chọn sang năm tài chính đã chọn.



[!INCLUDE[footer-include](../includes/footer-banner.md)]