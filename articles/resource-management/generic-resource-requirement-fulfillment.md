---
title: Đáp ứng các yêu về nguồn lực chung
description: Chủ đề này cung cấp thông tin về cách đặt trước nguồn lực được nêu tên cho một yêu cầu nguồn lực chung.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005862"
---
# <a name="generic-resource-requirement-fulfillment"></a>Đáp ứng các yêu về nguồn lực chung

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể đặt một nguồn lực được đặt tên để thay thế nguồn lực chung có yêu cầu nguồn lực.

1. Trên trang **Dự án**, chọn tab **Nhóm**.
2. Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách, sau đó chọn **Đặt lịch**. Hoặc mở yêu cầu nguồn lực rồi nhấp chọn **Đặt lịch**.
3. Trên trang **Trợ lý lịch trình**, chọn nguồn lực có tên để đặt trước vào nhóm dự án của bạn rồi chọn **Đặt lịch**.

Khi đặt lịch xong và được thực hiện bởi một nguồn lực có tên, thì nguồn lực chung được thay thế bằng nguồn lực có tên đó.

Các phân công trên lịch trình cũng được cập nhật bằng nguồn lực có tên.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Hoàn thành một nguồn lực chung với nhiều nguồn lực được đặt tên
Thực hiện một yêu cầu cho một nguồn lực chung với nhiều nguồn lực có tên sẽ tương tự như việc gán một nguồn lực có tên. Ví dụ: có một nhiệm vụ với thời gian năm ngày và 120 giờ làm việc. Một nguồn lực không thể hoàn thành nhiệm vụ này trong tám giờ trong năm ngày trong tuần. 

Yêu cầu này là cho 120 giờ kỹ thuật robot trong năm ngày, trong đó mỗi ngày 24 giờ.

Đây là một ví dụ khi nhiều nguồn lực được đặt tên là cần thiết để hoàn thành một yêu cầu nguồn lực chung. Bạn sẽ cần phải đặt nhiều nguồn lực để hoàn thành yêu cầu.

Sự khác biệt chính trong trường hợp này là nguồn lực chung vẫn còn trên nhóm được chỉ định nhiệm vụ và các thành viên nhóm nguồn lực được đặt tên không được chỉ định là một phần của vị trí. Người quản lý dự án có thể gán công việc phù hợp với các nguồn lực được đặt tên. Dạng xem **Hợp nhất** có thể hỗ trợ người quản lý dự án trong việc chia các đặt lịch cho nhiều nguồn lực cho phân công nhiệm vụ. Điều này không được thực hiện tự động bởi vì trong bất kỳ trường hợp nào phức tạp hơn ví dụ đơn giản ở trên, chẳng hạn như nơi bạn có một yêu cầu gồm nhiều nhiệm vụ hoặc ý định về cách thức người quản lý dự án muốn chỉ định, mà hệ thống cần tính đến. Vì hệ thống không thể hiểu được ý định, nên các giả định có thể sẽ khác ý định và có thể xảy ra kết quả không chính xác hoặc không dự đoán được. Kết quả dự đoán được đó là nguồn lực chung vẫn được gán cho đến khi ngời quản lý dự án cố ý tạo phân công với sự trợ giúp của dạng xem **Hợp nhất**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]