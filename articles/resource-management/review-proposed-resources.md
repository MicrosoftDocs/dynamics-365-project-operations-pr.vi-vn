---
title: Đánh giá nguồn lực được đề xuất
description: Chủ đề này cung cấp thông tin về cách đề xuất các nguồn lực dự án.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000777"
---
# <a name="review-proposed-resources"></a>Đánh giá nguồn lực được đề xuất

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Người quản lý nguồn lực có thể đề xuất nguồn lực với người quản lý dự án bằng yêu cầu nguồn lực.

1. Từ lưới yêu cầu hoặc tự yêu cầu, hãy chọn **Tìm nguồn lực**.
2. Trên trang **Trợ lý lập lịch biểu**, hãy chọn nguồn lực, sau đó trong ngăn **Tạo đăng ký nguồn lực**, trong trường **Trạng thái đăng ký**, hãy chọn **Đăng ký**.

Các bản cập nhật trạng thái sau xảy ra:

- Trên trang **Trợ lý lập lịch biểu**, chỉ báo trạng thái được cập nhật để biểu thị đăng ký được đề xuất và không được đăng ký chắc chắn.
- Trên yêu cầu nguồn lực, trạng thái này được thay đổi thành **Cần đánh giá**.
- Trên tab **Nhóm** của dự án này, giá trị **Trạng thái yêu cầu** của thành viên nhóm chung được thay đổi thành **Cần đánh giá**.

Người quản lý dự án có thể chấp nhận hoặc từ chối đề xuất.

Khi người quản lý nguồn lực xử lý các yêu cầu nguồn lực, họ có thể dùng bất kỳ cách tiếp cận nào sau đây:

- Đề xuất nhiều nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn để để thực hiện các giờ cần thiết. Các giờ đề xuất sau đó được chia cho nhiều nguồn lực có thể đáp ứng các giờ yêu cầu. Trong trường hợp này, giờ không thể chồng chéo.
- Đề xuất ít nguồn lực hơn yêu cầu. Trong trường hợp này, năng lực nguồn lực đề xuất ít hơn giờ yêu cầu mà người yêu cầu chỉ định. Do đó, khi người yêu cầu chấp nhận các nguồn lực đề xuất, các yêu cầu nguồn lực chưa hoàn thành được tạo để ghi lại nhu cầu còn lại.
- Đăng ký các nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn sẵn có để hoàn thành công việc.
- Đăng ký ít nguồn lực hơn yêu cầu. Trong trường hợp này, giờ đăng ký ít hơn giờ yêu cầu. Hệ thống hướng dẫn bạn đề xuất nguồn lực thay vì đăng ký để người yêu cầu có thể xác minh và theo dõi các nhu cầu còn lại.

## <a name="resource-availability"></a>Khả năng dùng nguồn lực

Điều quan trọng là người quản lý nguồn lực có thể xem trạng thái rảnh/bận của nguồn lực và cập nhật đăng ký. Trong một số trường hợp, không có nhu cầu chính thức (yêu cầu nguồn lực) nhưng người quản lý nguồn lực phải phản hồi với nhu cầu không theo kế hoạch qua các kênh như email, cuộc gọi điện thoại hoặc tin nhắn tức thời. Người quản lý nguồn lực dùng Bảng lịch trình để cập nhật tài nguyên và đăng ký.

Giờ làm việc của nguồn lực dùng làm cơ sở để tính toán trạng thái rảnh/bận của nguồn lực. Đăng ký nguồn lực tiêu thụ năng lực của nguồn lực.

Bảng lịch trình dùng màu và bóng để hiển thị đăng ký, trạng thái rảnh/bận, đăng ký quá mức và trạng thái của đăng ký. Cài đặt trong cài đặt Bảng lịch trình cho phép bạn hiển thị chú thích.

Nếu một mũi tên trỏ sang phải xuất hiện bên cạnh nguồn lực riêng có thể đăng ký trên Bảng lịch trình, thì nguồn lực có thể được mở rộng để hiển thị chi tiết của công việc mà nguồn lực được đăng ký.

Vì Dynamics 365 Project Operations dùng công cụ Universal Resource Scheduling, nếu bạn cũng có Dynamics 365 Field Service được cài đặt, bạn có thể xem chi tiết của đăng ký nguồn lực cho dự án, lệnh sản xuất và mọi thực thể khác mà bạn đã mở rộng lập lịch đến.

Để xem thêm chi tiết về nguồn lực riêng, hãy bấm chuột phải để mở thẻ nguồn lực.



[!INCLUDE[footer-include](../includes/footer-banner.md)]