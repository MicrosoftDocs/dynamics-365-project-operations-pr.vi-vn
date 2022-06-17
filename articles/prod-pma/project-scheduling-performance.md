---
title: Hiệu suất lập kế hoạch nguồn lực dự án
description: Bài viết này cung cấp thông tin về cách cải thiện hiệu suất của lập lịch tài nguyên cho một số lượng lớn các dự án.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 072476d43fb3b3d4f96480ec2d3dc5f9db28e501
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921926"
---
# <a name="project-resource-scheduling-performance"></a>Hiệu suất lập kế hoạch nguồn lực dự án

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Các vấn đề về hiệu suất liên quan đến lập kế hoạch nguồn lực có thể xảy ra khi số lượng dự án lên đến hàng nghìn. Để cải thiện hiệu suất lập kế hoạch nguồn lực, một tính năng có sẵn cho phép người dùng giảm thời gian khởi chạy biểu mẫu về tính sẵn sàng của nguồn lực. Cụ thể, điều này loại bỏ quá trình đồng bộ hóa tổng hợp năng lực của nguồn lực và sử dụng bảng **ResProjectResource** để tăng tốc độ tra cứu nguồn lực. Lưu ý rằng bảng **ResRollup** sẽ không còn được sử dụng.

> [!IMPORTANT]
> Nếu có đối tượng phụ thuộc trong quá trình đồng bộ hóa tổng hợp năng lực của nguồn lực hoặc bảng **ResProjectResource**, không sử dụng tính năng này.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Bật nâng cao hiệu suất lập kế hoạch nguồn lực
Để bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực, hãy hoàn thành các bước sau.

1. Đi đến **Quản lý tính năng** > **Tất cả** và trong danh sách tính năng, hãy định vị **Bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực dự án**.
2. Chọn **Bật ngay**.

> [!NOTE]
> Nếu bạn không thể tìm thấy tính năng trong danh sách, hãy chọn **Kiểm tra cập nhật** để làm mới danh sách.

3. Làm mới trình duyệt của bạn, sau đó đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Nguồn lực dự án** > **Đồng bộ hóa năng lực theo lịch nguồn lực trên tất cả công ty**.
4. Đặt **Xóa hồ sơ năng lực hiện có** thành **Có** để xóa dữ liệu trước đó. Nếu bạn muốn tạo dữ liệu gia tăng, hãy đặt thành **Không**.
5. Trong trường **Mã kỳ**, chọn khoảng thời gian mà dữ liệu sẽ được tạo. Nếu bạn chọn một mã kỳ, thì không cần xác định ngày bắt đầu và ngày kết thúc.
6. Nếu bạn để trống trường **Mã kỳ**, hãy chọn ngày bắt đầu và ngày kết thúc cụ thể để tạo dữ liệu.
7. Chọn **OK**.

 > [!NOTE]
 > Điều này sẽ phân phối dữ liệu chung tới bảng **ResCalendarCapacity** trên tất cả các công ty trong môi trường của bạn, vì vậy, công việc hàng loạt chỉ cần được chạy trong một pháp nhân. Cần có dữ liệu trong công việc hàng loạt này để tính toán năng lực của nguồn lực thông qua lịch liên quan.

8. Đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Nguồn lực dự án** > **Xác định nguồn lực dự án trên tất cả công ty**, sau đó chọn **OK**. Đây là tập lệnh nâng cấp dữ liệu cho dữ liệu chung trong các bảng **ResProjectResource**, **ResCalendarDateTimeRange** và **ResEffectiveDateTimeRange**. Giá trị cho trường **PSAPRojSchedRole.RootActivity** cũng được cập nhật. Nếu điều này không được chạy, bạn sẽ nhận được cảnh báo khi cố gắng thực hiện các hoạt động lập kế hoạch nguồn lực.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Tắt tính năng nâng cao hiệu suất lập kế hoạch nguồn lực

1. Đi đến **Quản lý tính năng** > **Tất cả** và tìm kiếm **Bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực dự án**.
2. Chọn tính năng, sau đó chọn nút **Tắt**.
3. Làm mới trình duyệt của bạn.
4. Đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Đồng bộ hóa năng lực** > **Đồng bộ hóa tổng hợp năng lực của nguồn lực**.
5. Trên trang **Đồng bộ hóa tổng hợp năng lực**, hãy đặt **Xóa hồ sơ năng lực hiện có** thành **Có** để xóa dữ liệu trước đó. Nếu bạn muốn tạo dữ liệu gia tăng, hãy đặt thành **Không**.
6. Trong trường **Mã kỳ**, chọn khoảng thời gian mà dữ liệu sẽ được tạo. Nếu bạn chọn một mã kỳ, thì không cần xác định ngày bắt đầu và ngày kết thúc.
7. Nếu bạn để trống trường **Mã kỳ**, hãy chọn ngày bắt đầu và ngày kết thúc cụ thể để tạo dữ liệu.
8. Chọn **OK**.

> [!NOTE]
> Điều này sẽ phân phối dữ liệu chung tới bảng **ResRollup** trên tất cả các công ty trong môi trường của bạn, vì vậy, công việc hàng loạt chỉ cần được chạy trong một pháp nhân. Công việc hàng loạt này là cần thiết cho tất cả dạng xem **Tính sẵn sàng của nguồn lực**. Nếu công việc hàng loạt này không được chạy, dữ liệu **ResRollup** sẽ được tạo nhanh chóng, có thể mất thời gian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]