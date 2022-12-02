---
title: Tính năng mới kể từ tháng 4 năm 2021 – Triển khai Project Operations bản đơn giản
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong lần triển khai bản đơn giản của Project Operations phát hành vào tháng 4 năm 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931265"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Tính năng mới kể từ tháng 4 năm 2021 – Triển khai Project Operations bản đơn giản

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

  - Project Operations trên môi trường Dataverse phiên bản 4.9.0.221 

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Vật tư không tồn kho cho các dự án. Các tính năng chính bao gồm:
  - Ước tính và định giá vật tư không tồn kho trong chu kỳ bán hàng của một dự án. Để biết thêm thông tin, hãy xem phần [Thiết lập chi phí và tỷ lệ doanh số cho các sản phẩm trong danh mục - bản đơn giản](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Theo dõi việc sử dụng vật tư không tồn kho trong quá trình thực hiện dự án. Để biết thêm thông tin, hãy xem phần [Ghi mức sử dụng vật tư của dự án và nhiệm vụ dự án](../../material/material-usage-log.md).
  - Lập hóa đơn chi phí vật tư không tồn kho đã qua sử dụng. Để biết thêm thông tin, hãy xem [Quản lý mục tồn đọng lập hóa đơn - bản đơn giản](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - API mới trong Dynamics 365 Dataverse cho phép thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**. Để biết thêm thông tin, hãy xem [Sử dụng API lịch trình để thực hiện thao tác với các thực thể Lập lịch trình](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2224568 | Đã thêm logic để bật các chế độ tùy chỉnh liên quan đến việc gọi ra phần bổ trợ xác nhận hóa đơn. |
| Định giá và thanh toán | 2101098 | Đã cải thiện logic của các trường mặc định cho hóa đơn ước giá: **Địa chỉ nhận hóa đơn**, **Tên nhận hóa đơn** và **Điều khoản thanh toán** bây giờ là các trường mặc định từ hồ sơ khách hàng của hợp đồng dự án tương ứng. |
| Định giá và thanh toán | 2021413 | Đã cập nhật các trường **Chi phí thực tế** và **Bán hàng** trên thực thể **Nhiệm vụ** để đưa vào các giá trị doanh số từ các chi phí chưa lập hóa đơn và đã lập hóa đơn cho các nhiệm vụ. |
| Định giá và thanh toán | 2182110 | Khi sao chép hợp đồng dự án, ID mô tả hợp đồng sẽ được tái tạo trong hợp đồng dự án đích để đảm bảo ID này là duy nhất. |
| Quản lý cơ hội | 2186741 | Đã thêm các bước xác thực để đảm bảo không thể cập nhật trường **Gốc** và **Loại giao dịch** trên phần chi tiết mô tả báo giá hiện có. |
| Quản lý cơ hội | 2191353 | Không được tạo các mốc trên một mục mô tả hợp đồng thời gian và vật tư. |
| Quản lý cơ hội | 2216956 | Đã khắc phục sự cố **Cập nhật giá**. |
| Hoạch định và theo dõi dự án | 2182979 | Đã cải tiến chức năng sao chép dự án để đảm bảo các dòng ước tính chi phí được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184144 | Đã cải tiến chức năng sao chép dự án để đảm bảo tên vị trí nguồn lực được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184799 | Sao chép dự án: Kiểm soát chặt chẽ để đảm bảo không thể thay đổi ngày bắt đầu ước tính khi đang sao chép. |
| Hoạch định và theo dõi dự án | 2185134 | Sao chép dự án: Ngày bắt đầu dự kiến của dự án đích được đặt thành ngày hôm nay. |
| Hoạch định và theo dõi dự án | 2196373 | Sao chép dự án: Đảm bảo hồ sơ của người quản lý dự án và thành viên trong nhóm không bị trùng lặp trong nhóm dự án. |
| Hoạch định và theo dõi dự án | 2211833 | Sao chép dự án: Các công việc giao cho nguồn lực được sao chép từ nhiệm vụ của dự án nguồn sang dự án đích. |
| Hoạch định và theo dõi dự án | 2186541 | Đã khắc phục sự cố trong lưới **Ước tính** khi nhóm theo nguồn lực. |
| Hoạch định và theo dõi dự án | 2166906 | Phải sao chép thể loại giao dịch từ một nhiệm vụ vào thực thể **Công việc giao cho nguồn lực**. |
| Quản lý nguồn lực | 2125362 | Đã khắc phục sự cố khi tạo một thành viên nhóm chung bằng phương pháp phân bổ theo giờ. |
| Thời gian và Chi phí | 2113603 | Đã khắc phục sự cố liên quan đến tùy chỉnh bằng cách xóa các thuộc tính khỏi trang **Mục nhập thời gian**. Giờ đây, hệ thống sẽ kiểm tra xem thuộc tính có tồn tại trên trang hay không trước khi truy cập chúng bằng cách sử dụng tập lệnh. |
| Thời gian và Chi phí | 2204377 | Bảng chấm công đã sao chép phải tự động hiển thị khi bạn chọn **Sao chép tuần** trong mục nhập thời gian. |
| Thời gian và Chi phí | 2209059 | Bạn có thể chỉnh sửa trường **Trạng thái** cho các mục nhập thời gian trên Dynamics 365 Field Service. |
