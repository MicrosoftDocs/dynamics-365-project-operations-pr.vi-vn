---
title: Đáp ứng các yêu về nguồn lực chung
description: Chủ đề này cung cấp thông tin về đặt lịch nguồn lực có tên cho một yêu cầu nguồn lực chung.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897612"
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


