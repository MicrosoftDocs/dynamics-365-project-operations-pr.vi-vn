---
title: Tổng quan về điều hòa nguồn lực
description: Chủ đề này cung cấp thông tin về việc đảm bảo phân bổ hợp lý trong việc đăng ký và phân công nguồn lực cho dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087050"
---
# <a name="resource-reconciliation-overview"></a>Tổng quan về điều hòa nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Đối với các thành viên nhóm, đăng ký và phân công được kết hợp lỏng lẻo. Nói cách khác, nguồn lực có thể có phân công nhưng không có đăng ký hoặc ngược lại. Tốt hơn hết, đăng ký nên phù hợp với phân công để các nguồn lực có năng lực được cam kết có thể thực hiện các phân công nhiệm vụ. Tuy nhiên, đăng ký có thể dựa trên trạng thái rảnh/bận và thời gian nhiệm vụ có thể thay đổi khi dự án tiếp tục. Do đó, việc kết hợp lỏng lẻo đăng ký và phân công mang đến sự linh hoạt.

Tab **Điều hòa** trên biểu mẫu **Dự án** cho phép người quản lý dự án điều hòa việc đăng ký và phân công của các thành viên trong nhóm cho nhóm dự án.

Tab **Điều hòa** cũng hiển thị đăng ký và phân công cụ thể đến cấp độ phân công nhiệm vụ cá nhân cho từng thành viên trong nhóm. Số giờ được hiển thị trong các ô thể hiện khoảng thời gian từ tháng đến ngày.

Tab này cũng hiển thị tổng số ròng tổng thể cho dự án, cùng với cột **Tổng**.

Đối với mỗi nguồn lực, tab này tính toán khác biệt giữa đăng ký của thành viên nhóm và tổng số phân công nhiệm vụ của thành viên nhóm đó. Khác biệt lý tưởng nhất là 0 (không). Nói cách khác, không nên có sự khác biệt giữa đăng ký và phân công. Khác biệt được tô và đánh bóng để dễ thấy 2 trạng thái:

- **Thiếu đăng ký** – Thiếu đăng ký xảy ra khi nguồn lực có nhiều phân công hơn đăng ký. Do năng lực này không được đăng ký trước nên người quản lý dự án có thể chỉnh sửa trạng thái này bằng cách mở rộng đăng ký nguồn lực để trang trải thâm hụt.
- **Đăng ký vượt mức** – Đăng ký vượt mức có thể xảy ra khi nguồn lực được đăng ký cho dự án nhưng không được phân công cho nhiệm vụ. Trạng thái này có thể chấp nhận được trong các trường hợp nguồn lực được đăng ký cho dự án trước khi phân công nhiệm vụ diễn ra. Tuy nhiên, trong các trường hợp khác, nguồn lực không được lên kế hoạch để được phân công nhiệm vụ. Trong những trường hợp này, người quản lý dự án nên xem xét hủy bỏ các đăng ký của nguồn lực để năng lực đó có thể dùng cho dự án khác.

Trong một số trường hợp, khi thấy mức thời gian cao hơn mức ngày (ví dụ: mức tháng), bạn có thể thấy khác biệt thực 0 cho nguồn lực (nói cách khác là đăng ký = phân công). Tuy nhiên, nếu thấy thời gian ở mức tuần, bạn có thể thấy phân công 0 giờ hoặc đăng ký 40 giờ trong tuần đầu tiên nhưng phân công 40 giờ và đăng ký 0 giờ trong tuần thứ hai. Nhìn chung, đăng ký và phân công được điều hòa nhưng khác nhau giữa một tuần và tuần tiếp theo.

Khi bạn thấy thời gian ở các mức cao hơn, các ô trong tab **Điều hòa** có chỉ báo để báo cho bạn biết rằng có sự khác biệt ở các mức thấp hơn. Bằng cách bấm đúp vào một ô, bạn có thể phóng to để xem sự khác biệt. Sau đó, bạn có thể bấm chuột phải để thu nhỏ. Bằng cách chọn một nguồn lực, sau đó dùng điều khiển **Khác biệt tiếp theo** trên thanh công cụ lưới, bạn có thể chuyển đến khác biệt tiếp theo giữa đăng ký và phân công cho nguồn lực. Sau đó, bạn có thể dùng điều khiển **Khác biệt trước đó** để quay lại. Bạn cũng có thể tắt chỉ báo khác biệt và hành vi điều hướng trong **Cài đặt**.


Nếu bạn có phân công nhiệm vụ cho nguồn lực nhưng không có đăng ký, trên trang **Dự án** , trên tab **Điều hòa** , hãy chọn thiếu đăng ký rồi chọn **Mở rộng đăng ký**. Hộp thoại **Mở rộng đăng ký** xuất hiện và hiển thị đăng ký cần thiết để khắc phục tình trạng thiếu của nguồn lực. Hộp thoại này cũng hiển thị đăng ký hiện có của nguồn lực trên tất cả dự án hoặc các thực thể có thể lập lịch khác. Nếu chọn **OK** để tạo đăng ký cho nguồn lực, bất kể trạng thái rảnh/bận của nguồn lực, bạn có thể gây ra tình trạng đăng ký vượt mức.

Người quản lý dự án hoặc người quản lý nguồn lực có thể dùng Bảng lịch trình để quản lý mọi tình huống nguồn lực bị đăng ký quá mức so với năng lực của họ.

