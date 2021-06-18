---
title: Tạo dự án mới
description: Chủ đề này cung cấp thông tin về cách tạo dự án mới.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006267"
---
# <a name="create-a-new-project"></a>Tạo dự án mới

[!include [banner](../includes/banner.md)]

Hoàn thành các bước sau để tạo dự án mới.

1. Trên trang **Quản lý dự án**, chọn **Dự án mới** rồi nhập các giá trị sau đây:

    - **Loại dự án:** Thời gian và vật liệu
    - **Tên dự án:** Nâng cấp XYZ Giai đoạn 2
    - **Nhóm dự án:** TM\_WIP
    - **ID hợp đồng dự án:** 00000002

2. Chọn **Tạo dự án**.

## <a name="assign-a-resource-to-a-project"></a>Chỉ định nguồn lực cho dự án

1. Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn bản ghi cho nhân viên mà bạn đã thiết lập năng lực và mở bản ghi nhân viên.
2. Trên Ngăn hành động, trên tab **Dự án**, trong nhóm **Thiết lập**, chọn **Chỉ định dự án**.
3. Trên trang **Phân công dự án xác thực nguồn lực**, trên tab **Dự án**, trong trường **Thêm dự án vào các dự án đã chọn**, lọc trên dự án **Nâng cấp XYZ Giai đoạn 2**.
4. Trong ngăn **Dự án còn lại**, chọn dự án rồi chọn nút mũi tên để thêm vào ngăn **Dự án đã chọn**.

Bạn cũng có thể chỉ định các thể loại cho nguồn lực mà mình cần. Thể loại là **Chi phí** hoặc **Doanh thu**. Thể loại được xác định bởi tổ chức của bạn. Nếu không có thể loại nào được chỉ định cho nguồn lực, Finance sẽ tra cứu thể loại mặc định trên giá theo giờ để biết chi phí và doanh thu.

## <a name="set-up-project-resource-and-role-characteristics"></a>Thiết lập đặc điểm vai trò và nguồn lực dự án

Người quản lý dự án có thể sử dụng chức năng nguồn lực dự án để tạo các vai trò cần thiết cho dự án. Có thể sử dụng vai trò nếu nguồn lực đã xác nhận vẫn là không xác định khi nguồn lực đang được dự trữ. Các vai trò có thể được dự trữ tạm thời dưới dạng nguồn lực đã lập kế hoạch để bạn có thể tiếp tục các giai đoạn lập kế hoạch dự án.

[![Ví dụ về vai trò](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Tình huống:** Contoso được thuê hoàn thành một dự án Thời gian và vật tư có đã được phê duyệt điều lệ dự án. Người quản lý dự án cấp dưới vẫn đang hoàn thành phạm vi của dự án. Người quản lý tài nguyên hiện đang xác định các nguồn lực cụ thể sẽ được dự trữ để thực hiện dự án mới. Do tính chất quan trọng của dự án, nhà tài trợ dự án đã yêu cầu Người quản lý dự án cấp cao là một trong các vai trò. Người quản lý tài nguyên phải có được nguồn lực mới và xác định vai trò trong hệ thống trong trường hợp người quản lý dự án cấp dưới yêu cầu thông tin tài nguyên trong quá trình lập kế hoạch dự án.

Các bước sau đây cho thấy cách người quản lý nguồn lực có thể thiết lập vai trò Người quản lý dự án cấp cao và liên kết các đặc điểm của nguồn lực với vai trò đó. Sau đó, vai trò có thể được sử dụng để tìm kiếm các nguồn lực có sẵn phù hợp với năng lực của nguồn lực được yêu cầu.

1. Trên trang **Thiết lập vai trò**, chọn **Mới** rồi nhập các giá trị sau đây:

    - **ID vai trò:** Người quản lý dự án cấp cao
    - **Mô tả:** Người quản lý dự án cấp cao

2. Chọn **Tạo**.
3. Chọn vai trò **Người quản lý dự án cấp cao** rồi chọn **Đặt cấu hình đặc điểm**.
4. Trong trường **Loại đặc điểm**, chọn **Kỹ năng**.
5. Trong trường **Đặc điểm có sẵn**, nhập kỹ năng để tìm kiếm.
6. Trong trường **Loại đặc điểm**, chọn **Chứng chỉ**.
7. Trong trường **Đặc điểm có sẵn**, nhập loại chứng chỉ để tìm kiếm.

## <a name="assign-a-project-resource-to-a-project"></a>Chỉ định nguồn lực dự án cho dự án

1. Trên trang **Tất cả dự án**, chọn dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Trên tab **Nhóm dự án và lập lịch trình**, chọn **Thêm**.
3. Trong trường **Vai trò**, chọn **Thành viên nhóm**.
4. Chọn **Đặt từ lịch**.
5. Trên trang **Khả năng dùng nguồn lực**, chọn **Thiết đặt dạng xem**.
6. Trên trang **Điều chỉnh thiết đặt dạng xem**, nhập các giá trị sau đây:

    - **Định dạng cho dạng xem phạm vi ngày:** Ngày
    - **Hiển thị mô tả tình trạng rảnh/bận:** Có
    - **Hiển thị năng lực còn lại:** Có

7. Trong danh sách nguồn lực, chọn một nguồn lực.
8. Chọn **Đặt trước chắc chắn** và **Năng lực đầy đủ**.

## <a name="assign-a-resource-to-a-default-role"></a>Chỉ định nguồn lực cho vai trò mặc định

Giúp các nhà quản lý dự án hoặc nguồn lực xem chi tiết các nguồn lực có thể được dành riêng cho một dự án. Bạn có thể liên kết một vai trò mặc định với một tài nguyên hiện có hoặc một tài nguyên mới có được. Ví dụ: khi Daniel được thuê, anh ấy có kinh nghiệm và kỹ năng để đảm nhiệm vai trò Phân tích viên kinh doanh. Người quản lý nguồn lực đã gán vai trò này là vai trò mặc định của Daniel. Do đó, người quản lý nguồn lực đã thêm Daniel vào một nhóm các phân tích viên kinh doanh sẵn sàng làm việc trong các dự án.

Trong quá trình dự trữ nguồn lực, người quản lý dự án có thể lọc các nguồn lực vai trò có sẵn để thực hiện dự án. Họ có thể sử dụng thông tin này như một tiêu chí khi thực hiện phân tích quyết định đa tiêu chí trong quá trình thực hiện nguồn lực. Họ cũng có thể thêm các đặc điểm nguồn lực khác vào bộ lọc để tìm kiếm các tài nguyên có kỹ năng, trình độ học vấn và kinh nghiệm cụ thể cho một dự án nhất định.

**Tình huống:** Một dự án được phê duyệt đã bắt đầu và vai trò Người quản lý dự án cấp cao được dự trữ như một nguồn lực theo kế hoạch trong giai đoạn lập kế hoạch dự án. Người quản lý nguồn lực hiện đã có được một nguồn lực để thực hiện vai trò Người quản lý dự án cấp cao.

1. Trên trang **Danh sách nguồn lực**, chọn **Daniel Goldschmidt**.
2. Trên trang **Vai trò nguồn lực**, chọn **Mới** rồi nhập các giá trị sau đây:

    - **Có hiệu lực:** Nhập ngày hiện tại.
    - **Hết hạn:** Nhập **Không bao giờ**.
    - **Vai trò:** Nhập **Người quản lý dự án cấp cao**.

3. Chọn **Lưu** rồi đóng trang.
4. Trên tab **Năng lực**, thêm kỹ năng **Quản lý dự án** và chứng chỉ **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]