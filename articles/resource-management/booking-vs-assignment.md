---
title: Mục đặt trước và mục chỉ định
description: Bài viết này cung cấp thông tin về sự khác biệt giữa đặt trước tài nguyên và ấn định tài nguyên.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918614"
---
# <a name="bookings-vs-assignments"></a>Mục đặt trước và mục chỉ định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn. Đăng ký chắc chắn chiếm năng lực của nguồn lực. Bookings trình bày những ý tưởng của tổ chức cho các nhóm để họ có thể hiểu các nguồn lực sẽ tham gia vào những dự án khác nhau như thế nào. Dynamics 365 Project Operations xem lượt đăng ký là một khái niệm ở cấp dự án. 

Khác với các lượt đăng ký, nhiệm vụ là cam kết về nguồn lực cho những tác vụ dự án trong lịch trình dự án. Các nguồn lực có thể chung chung hoặc được đặt tên.  Khi một yêu cầu nguồn lực có nguồn gốc từ các phân công nhiệm vụ dự án, Project Operations sử dụng phân phối giờ làm việc trong phân công nguồn lực để xây dựng phân phối giờ làm việc trong chi tiết yêu cầu nguồn lực. Tuy nhiên, tham chiếu đến các phân công nguồn lực không được duy trì. Nội dung cập nhật đối với lượt đăng ký bắt nguồn từ yêu cầu nguồn lực sẽ không cập nhật bất kỳ phân công nguồn lực nào.

Thông thường, tổng số lượt đăng ký cho một nguồn lực sẽ bằng tổng các nhiệm vụ của một hoặc nhiều tác vụ được chỉ định cho nguồn lực đó. Tuy nhiên, Project Operations không đảm bảo sự thống nhất này. Dạng xem **Điều hòa** cho Người quản lý dự án thấy các vị trí mà lượt đăng ký và nhiệm vụ của nguồn lực không thống nhất với nhau.




[!INCLUDE[footer-include](../includes/footer-banner.md)]