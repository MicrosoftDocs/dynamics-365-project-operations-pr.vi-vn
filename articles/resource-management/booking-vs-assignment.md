---
title: Mục đặt trước và mục chỉ định
description: Chủ đề này cung cấp thông tin về sự khác biệt giữa đặt trước nguồn lực và chỉ định nguồn lực.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841198"
---
# <a name="bookings-vs-assignments"></a>Mục đặt trước và mục chỉ định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn. Đăng ký chắc chắn chiếm năng lực của nguồn lực. Bookings trình bày những ý tưởng của tổ chức cho các nhóm để họ có thể hiểu các nguồn lực sẽ tham gia vào những dự án khác nhau như thế nào. Dynamics 365 Project Operations xem lượt đăng ký là một khái niệm ở cấp dự án. 

Khác với các lượt đăng ký, nhiệm vụ là cam kết về nguồn lực cho những tác vụ dự án trong lịch trình dự án. Các nguồn lực có thể chung chung hoặc được đặt tên.  Khi một yêu cầu nguồn lực có nguồn gốc từ các phân công nhiệm vụ dự án, Project Operations sử dụng phân phối giờ làm việc trong phân công nguồn lực để xây dựng phân phối giờ làm việc trong chi tiết yêu cầu nguồn lực. Tuy nhiên, tham chiếu đến các phân công nguồn lực không được duy trì. Nội dung cập nhật đối với lượt đăng ký bắt nguồn từ yêu cầu nguồn lực sẽ không cập nhật bất kỳ phân công nguồn lực nào.

Thông thường, tổng số lượt đăng ký cho một nguồn lực sẽ bằng tổng các nhiệm vụ của một hoặc nhiều tác vụ được chỉ định cho nguồn lực đó. Tuy nhiên, Project Operations không đảm bảo sự thống nhất này. Dạng xem **Điều hòa** cho Người quản lý dự án thấy các vị trí mà lượt đăng ký và nhiệm vụ của nguồn lực không thống nhất với nhau.


