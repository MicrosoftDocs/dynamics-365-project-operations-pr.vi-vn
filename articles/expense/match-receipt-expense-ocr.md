---
title: Chụp biên nhận bằng OCR
description: Chủ đề này cung cấp thông tin về quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499877"
---
# <a name="capture-a-receipt-using-ocr"></a>Chụp biên nhận bằng OCR

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Quy trình nhập chi phí đã được nâng cao thông qua việc bổ sung quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai. Chức năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí.

## <a name="key-features"></a>Tính năng chính

- Hệ thống trích xuất tên người bán, ngày tháng và tổng số tiền từ biên lai.
- Hệ thống sẽ cố gắng so khớp các biên lai chưa đính kèm với các giao dịch chi phí chưa đính kèm.
- Bạn có thể tạo các giao dịch chi phí được nhập theo cách thủ công từ biên lai.

## <a name="attach-receipts-to-an-expense-report"></a>Đính kèm biên lai vào báo cáo chi phí

Để tự động đính kèm biên lai bao gồm các giao dịch bằng thẻ tín dụng khi báo cáo chi phí được tạo, hãy hoàn thành các bước sau.

  1. Mở không gian làm việc **Quản lý chi phí**.
  2. Trên tab **Biên lai**, hãy xác minh rằng biên lai chưa đính kèm có tồn tại. Bạn cũng có thể tải lên biên lai trên tab **Biên lai**.
  3. Trên tab **Biên lai**, hãy xác minh rằng chi phí chưa đính kèm có tồn tại. Thông thường, người quản lý chi phí nhập các chi phí này từ nhà cung cấp thẻ tín dụng.
  4. Chọn **Báo cáo chi phí mới**. Lưu ý rằng kể cả bây giờ, bạn cũng có thể kèm theo chi phí và biên lai khi tạo báo cáo chi phí. Nếu bạn thêm cả chi phí và biên lai, thao tác đối sánh tự động giữa các khoản thu với chi phí sẽ được kích hoạt.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Tạo hoặc so khớp biên lai vào báo cáo chi phí
Để tạo một khoản chi phí hoặc so khớp một khoản chi phí từ biên lai, hãy hoàn thành các bước sau.

  1. Trên báo cáo chi phí, trên tab **Biên lai**, hãy đính kèm biên lai bằng cách chọn **Thêm biên lai**.
  2. Dưới hình ảnh đã tải lên của biên lai, hãy lưu ý các tùy chọn **Tạo** và **So khớp**.

      - Chọn **Tạo** để tạo một giao dịch chi phí được nhập theo cách thủ công và điền vào các giá trị được trích xuất từ biên lai.
      - Nếu bạn chọn **So khớp**, hệ thống cố gắng khớp một khoản chi phí hiện có với biên lai.

## <a name="installation"></a>Cài đặt

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

## <a name="frequently-asked-questions"></a>Câu hỏi thường gặp

**Microsoft có sử dụng dữ liệu của tôi cho các mô hình của hãng không?**

Không, Microsoft đã xây dựng một mô hình máy học chung cho dịch vụ xử lý biên lai của hãng. Mô hình này không dựa vào biên lai mà bạn tải lên.

**Tính năng này được cung cấp và xử lý ở đâu?**

Hiện tại, có Hoa Kỳ được hỗ trợ.

**Biên lai của tôi sẽ chuyển tới đâu?**

Finance sẽ liên hệ với Cognitive Services để trích xuất dữ liệu trong trường này. Cognitive Services sẽ giữ lại bản sao biên lai của bạn trong tối đa 24 giờ trong khi quy trình xử lý diễn ra. Sau khi quy trình xử lý đã hoàn tất, Cognitive Services sẽ xóa biên lai. Biên lai vẫn được lưu trữ trong Finance.

Để biết thêm thông tin, hãy xem [Cho phép tìm hiểu về biên lai bằng chức năng mới của Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
