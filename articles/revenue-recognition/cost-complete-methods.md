---
title: Phương pháp Chi phí hoàn thành
description: Bài viết này sẽ trình bày thông tin về phương pháp tính toán chi phí cần để hoàn thành dự án.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920316"
---
# <a name="cost-to-complete-methods"></a>Phương pháp Chi phí hoàn thành

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này sẽ trình bày thông tin về phương pháp tính toán chi phí cần để hoàn thành dự án. Bạn có thể dùng nhiều phương pháp để tính chi phí hoàn thành dự án. 

Khi ước tính dự án, trên trang **Tạo ước tính**, trong trường **Phương pháp Chi phí hoàn thành**, bạn có thể chọn một trong các phương pháp chi phí hoàn thành sau đây.

| Phương pháp chi phí hoàn thành    | Nội dung mô tả                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tổng chi phí-thực tế            | Nhập chi phí ước tính thủ công trong trường **Tổng chi phí** hoặc **Tổng số lượng** bằng cách dùng nút **Ước tính chi phí** trên **trang Ước tính**. Hệ thống sẽ trừ chi phí thực tế khỏi tổng bạn đã nhập. Tổng là chi phí cần để hoàn thành dự án. Phương pháp này không dùng các giá trị ước tính chi phí và phân công nguồn lực bạn nhập vào Project Operations tích hợp trong Microsoft Dataverse. Bạn có thể cập nhật tổng chi phí và tổng số lượng theo cách thủ công nếu cần.  |
| Tổng dự báo-thực tế        | Giá trị ước tính chi phí và cách phân công nguồn lực sẽ được dùng để xác định tổng tiền dự báo của dự án. Chi phí thực tế sẽ được so sánh với số tiền dự báo này để tính toán chi phí hoàn thành.                                                                                                                                                                                                                                                                          |
| Như ước tính trước         | Phương pháp ước tính ở kỳ trước sẽ được sử dụng lại ở đây. Phương pháp này đòi hỏi có mô hình dự báo nếu kỳ trước yêu cầu có mô hình dự báo.                                                                                                                                                                                                                                                                                                                           |
| Đặt chi phí hoàn thành thành 0 | Phương pháp này thường được dùng trước khi loại bỏ dự án ước tính, có tác dụng khớp giá trị tổng ước tính với các giao dịch thực tế đã đăng, cũng như xóa cột **Chi phí hoàn thành**. Khi hoàn thành, kết quả sẽ luôn là 100 phần trăm. Với mỗi dùng chi phí bạn tạo, ô **Dự báo** sẽ được bỏ đánh dấu và tổng ước tính sẽ được sao chép từ giá trị ước tính chi phí trước đó. Mức tiêu hao thực tế cho kỳ dự toán được trừ vào chi phí hoàn thành dự án.              |
| Từ mẫu chi phí           | Phương pháp chi phí hoàn thành được thiết lập trong mẫu chi phí và không liên kết với dự án ước tính đã chọn.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]