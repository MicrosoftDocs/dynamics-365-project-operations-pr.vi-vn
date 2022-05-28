---
title: Triển khai ứng dụng Project Operations Dataverse theo cách thủ công có hỗ trợ ghi kép
description: Chủ đề này giải thích cách triển khai ứng dụng Project Operations Dataverse để hỗ trợ ghi kép.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591246"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Triển khai ứng dụng Project Operations Dataverse theo cách thủ công có hỗ trợ ghi kép

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này giải thích cách triển khai Microsoft Dynamics 365 Project Operations theo cách thủ công trong Microsoft Dataverse để hỗ trợ ghi kép. Project Operations phát hiện cấu hình của môi trường và bổ sung hỗ trợ bổ sung cho tính năng ghi kép nếu các điều kiện tiên quyết được đáp ứng.

Trong quá trình triển khai thông qua Microsoft Dynamics Lifecycle Services (LCS), nếu bạn đã làm theo hướng dẫn trong chủ đề này, bạn có thể bỏ qua việc triển khai tích hợp Microsoft Power Platform (trước đây được gọi là môi trường Common Data Service).

Quá trình triển khai Project Operations trong Dataverse để hỗ trợ ghi kép có bốn bước chính:

1. [Tạo một môi trường mới trong Dataverse hỗ trợ ghi kép](#create).
2. [Thêm điều kiện tiên quyết ghi kép vào môi trường](#prerequisites).
3. [Thêm ứng dụng Project Operations Dataverse](#dataverse).
4. [Liên kết các môi trường của bạn](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Tạo một môi trường mới trong Dataverse hỗ trợ ghi kép

Để hoàn thành quy trình này, bạn phải đăng nhập với tư cách quản trị viên.

1. Mở [Trung tâm quản trị Power Platform](https://admin.powerplatform.com) và đăng nhập với tư cách quản trị viên.
2. Và và đặt tên cho môi trường mới.
3. Chọn loại môi trường. Nếu bạn đã đăng ký nhận ưu đãi dùng thử, hãy chọn **Bản dùng thử (dựa trên đăng ký)**.
4. Xác nhận khu vực triển khai.
5. Bật tùy chọn **Tạo cơ sở dữ liệu cho môi trường này**. 
6. Xác nhận ngôn ngữ, sau đó xác nhận rằng đơn vị tiền tệ đó khớp với đơn vị tiền tệ cho các ứng dụng Tài chính và Hoạt động của bạn.
7. Bật tùy chọn **Ứng dụng Dynamics 365** và xác nhận rằng trường **Tự động triển khai những ứng dụng này** được đặt thành **Không có**.
8. Thêm một nhóm bảo mật, nếu một nhóm bảo mật được yêu cầu.
9. Chọn **Lưu** để tạo môi trường.
10. Chờ cho đến khi việc triển khai hoàn tất và môi trường đạt trạng thái **Sẵn sàng**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Thêm điều kiện tiên quyết ghi kép vào môi trường

Hỗ trợ ghi kép bao gồm các trường bổ sung được thêm vào các thực thể chính, chẳng hạn như thực thể **Công ty**. Nếu bạn đang thêm hỗ trợ ghi kép vào môi trường hiện có, bạn có thể phải cập nhật dữ liệu để bật hỗ trợ. Để biết thông tin về cách khởi động dữ liệu, hãy xem [Dữ liệu công ty Bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Để biết thêm thông tin về ghi kép, hãy xem [Yêu cầu hệ thống ghi kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Hoàn thành quy trình này để thêm điều kiện tiên quyết ghi kép vào môi trường của bạn.

1. Mở môi trường mà bạn vừa tạo, sau đó đi tới **Tài nguyên** \> **Ứng dụng Dynamics 365**.
2. Chọn **Giải pháp chính ghi kép** trong danh sách ứng dụng và cài đặt giải pháp đó.
3. Chờ cho đến khi quá trình cài đặt hoàn tất. Sau đó, chọn **Giải pháp điều phối ứng dụng ghi kép** trong danh sách ứng dụng và cài đặt giải pháp đó.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Thêm ứng dụng Project Operations Dataverse

Bạn chỉ có thể hoàn thành quy trình này nếu đã hoàn thành các quy trình trước đó trước khi cài đặt Project Operations. Trong quá trình cài đặt, hệ thống sẽ phân tích cấu hình môi trường và hỗ trợ thêm tính năng ghi kép nếu được yêu cầu.

1. Mở môi trường mà bạn đã tạo, sau đó đi tới **Tài nguyên** \> **Ứng dụng Dynamics 365**.
2. Chọn **Microsoft Dynamics 365 Project Operations** trong danh sách ứng dụng và cài đặt.

## <a name="link-your-environments"></a><a name="link"></a>Liên kết các môi trường của bạn

Sau Dataverse được triển khai, bạn có thể thiết lập liên kết trong ứng dụng Tài chính và Hoạt động của mình. Làm theo các bước trong [Sử dụng trình hướng dẫn ghi kép để liên kết các môi trường của bạn](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
