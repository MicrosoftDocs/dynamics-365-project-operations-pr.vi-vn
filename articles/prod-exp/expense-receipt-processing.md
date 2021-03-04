---
title: Xử lý biên lai chi phí
description: Chủ đề này cung cấp thông tin về quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai. Tính năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí trong Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960318"
---
# <a name="expense-receipt-processing"></a>Xử lý biên lai chi phí

Quy trình nhập chi phí đã được nâng cao thông qua việc bổ sung quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai. Tính năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí.

## <a name="key-features"></a>Tính năng chính

- Tên người bán, ngày tháng và tổng số tiền được trích xuất từ biên lai.
- Tính năng này sẽ cố gắng so khớp các biên lai chưa đính kèm với các giao dịch chi phí chưa đính kèm.
- Người dùng có thể tạo các giao dịch chi phí được nhập thủ công từ biên lai.

## <a name="usage-examples"></a>Ví dụ sử dụng

Để tự động đính kèm biên lai có giao dịch bằng thẻ tín dụng khi báo cáo chi phí được tạo, hãy làm như sau:

  1. Mở không gian làm việc **Quản lý chi phí**.
  2. Trên tab **Biên lai**, hãy xác minh rằng biên lai chưa đính kèm có tồn tại. Bạn cũng có thể tải lên biên lai trên tab **Biên lai**.
  3. Trên tab **Biên lai**, hãy xác minh rằng chi phí chưa đính kèm có tồn tại. Thông thường, người quản lý chi phí nhập các chi phí này từ nhà cung cấp thẻ tín dụng.
  4. Chọn **Báo cáo chi phí mới**. Lưu ý rằng kể cả bây giờ, bạn cũng có thể kèm theo chi phí và biên lai khi tạo báo cáo chi phí. Nếu bạn thêm cả chi phí và biên lai, thao tác đối sánh tự động giữa các khoản thu với chi phí sẽ được kích hoạt.

Để tạo chi phí hoặc so khớp chi phí từ biên lai, hãy làm như sau:

  1. Trên báo cáo chi phí, trên tab **Biên lai**, hãy đính kèm biên lai bằng cách chọn **Thêm biên lai**.
  2. Dưới hình ảnh đã tải lên của biên lai, hãy lưu ý các tùy chọn **Tạo** và **So khớp**.

      - Chọn **Tạo** để tạo một giao dịch chi phí được nhập theo cách thủ công và điền vào các giá trị được trích xuất từ biên lai.
      - Nếu bạn chọn **So khớp**, hệ thống cố gắng khớp một khoản chi phí hiện có với biên lai.

## <a name="installation"></a>Cài đặt

Tính năng này hoạt động kết hợp với tính năng **Báo cáo chi phí được xây dựng lại** để mang đến trải nghiệm chi phí đơn giản hơn. Tính năng này chỉ khả dụng cho môi trường Cấp 2 trở lên, tức là Hộp cát và Sản xuất.

Để sử dụng các tính năng về chi phí nâng cao này, hãy cài đặt trình bổ sung Dịch vụ quản lý chi phí cho Microsoft Dynamics 365 Finance và bật các tính năng trong phiên bản của bạn. Bạn có thể truy cập vào trình bổ sung từ dự án của mình trong Microsoft Dynamics Lifecycle Services (LCS).

1. Đăng nhập vào LCS và mở môi trường mong muốn.
2. Chuyển tới **Chi tiết đầy đủ**.
3. Chọn **Duy trì =** hoặc cuộn xuống FastTab **Trình bổ sung cho môi trường**.
4. Chọn **Cài đặt trình bổ sung mới**.
5. Chọn **Dịch vụ quản lý chi phí**.
6. Làm theo hướng dẫn cài đặt và đồng ý với các điều khoản và điều kiện.
7. Chọn **Cài đặt**.

Trong không gian làm việc **Quản lý tính năng**, hãy bật các tính năng sau:

- Báo cáo chi phí đã được xây dựng lại
- Tự động so khớp và tạo chi phí từ biên lai

Khi bạn bật các tính năng này, các tác vụ sau sẽ diễn ra:

- Không gian làm việc **Quản lý chi phí** hiện có được thay thế bằng không gian làm việc mới.
- Một mục menu mới để hiển thị trường chi phí được thêm vào.
- Bạn vẫn có thể mở trang **Báo cáo chi phí** trước bằng cách chuyển tới **Quản lý chi phí> Chi phí của tôi > Báo cáo chi phí**.
- Quy trình làm việc và mọi mục phê duyệt vẫn đưa bạn đến trang báo cáo chi phí hiện có.
- Biên lai sẽ được xử lý thông qua Microsoft Azure Cognitive Services và siêu dữ liệu sẽ được trích xuất và thêm vào.
- Một tùy chọn được thêm vào, cho phép bạn tạo báo cáo chi phí bao gồm các biên lai chưa đính kèm đã được so khớp.
- Một tùy chọn được thêm vào báo cáo chi phí, cho phép bạn tạo dòng chi phí từ biên lai hoặc thử so khớp biên lai hiện có với dòng chi phí hiện có.

Để biết thêm thông tin về tính năng Báo cáo chi phí được xây dựng lại, hãy xem [Báo cáo chi phí được xây dựng lại](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Câu hỏi thường gặp

**Microsoft có sử dụng dữ liệu của tôi cho các mô hình của hãng không?**

Không, Microsoft đã xây dựng một mô hình máy học chung cho dịch vụ xử lý biên lai của hãng. Mô hình này không dựa vào biên lai mà bạn tải lên.

**Tính năng này được cung cấp và xử lý ở đâu?**

Hiện tại, có Hoa Kỳ được hỗ trợ.

**Biên lai của tôi sẽ chuyển tới đâu?**

Finance sẽ liên hệ với Cognitive Services để trích xuất dữ liệu trong trường này. Cognitive Services sẽ giữ lại bản sao biên lai của bạn trong tối đa 24 giờ trong khi quy trình xử lý diễn ra. Sau khi quy trình xử lý đã hoàn tất, Cognitive Services sẽ xóa biên lai. Biên lai vẫn được lưu trữ trong Finance.

Để biết thêm thông tin, hãy xem [Cho phép tìm hiểu về biên lai bằng chức năng mới của Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
