---
title: Thiết lập vai trò trên các mẫu cấu trúc phân tích công việc
description: Chủ đề này cung cấp thông tin về cách thiết lập thông tin vai trò trên các mẫu cấu trúc phân tích công việc.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087088"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Thiết lập vai trò trên các mẫu cấu trúc phân tích công việc

[!include [banner](../includes/banner.md)]

Người quản lý dự án có thể thiết lập các mẫu Cấu trúc phân tích công việc (WBS) mà họ có thể áp dụng khi tạo một WBS cho các dự án mới. Người quản lý dự án có thể thêm vai trò khi họ tạo mẫu. Sử dụng quy trình sau để gán một vai trò cho mẫu WBS.

1. Chọn **Kế toán và quản lý dự án** > **Thiết lập** > **Dự án** > **Mẫu cấu trúc phân tích công việc**.
2. Chọn **Chi tiết** cho mẫu WBS đã chọn.
3. Chọn một nhiệm vụ trong danh sách, trong **Vai trò** , chọn một vai trò để gán cho nhiệm vụ.

## <a name="work-with-a-wbs"></a>Làm việc với WBS

Bạn có thể tạo một WBS mới hoặc sao chép WBS từ một mẫu WBS hiện có. Người quản lý dự án có thể dễ dàng quản lý nguồn lực bằng cách gán vai trò cho các nhiệm vụ mới trên WBS. Có thể thay thế vai trò sau khi thu được nguồn lực hoặc sau khi nguồn lực đã xác định thực hiện nhiệm vụ được xác định. Tính linh hoạt này cho phép nhà quản lý dự án thực hiện các nhiệm vụ sau:

- Xác định số lượng nguồn lực yêu cầu cho các gói công việc WBS.
- Ước tính chi phí dự án.
- Xác định ngân sách sơ bộ.
- Ước tính khoảng thời gian hoạt động, dựa trên vai trò và nguồn lực.
- Xây dựng một số kế hoạch quản lý dự án, dựa trên thông tin dự án có sẵn.

Các tùy chọn bổ sung đã được thêm vào WBS để sử dụng tốt hơn chức năng nguồn lực.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tùy chọn</th>
<th>Mô tả</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gán nguồn lực</td>
<td>Xem các nguồn lực được chỉ định, ngày, số giờ và loại đặt trước cho các nhiệm vụ trên WBS.</td>
</tr>
<tr class="even">
<td>Tự động tạo nhóm</td>
<td>Tự động thêm nguồn lực theo kế hoạch bằng cách sử dụng các vai trò được liên kết với một nhiệm vụ. Finance tự động đề xuất các nguồn lực theo kế hoạch bằng cách sử dụng phân tích quyết định đa tiêu chí dựa trên vai trò. Sau khi các vai trò và nhân công (giờ) đã được thiết lập cho các nhiệm vụ trong WBS và sau khi cấu trúc đã được phát hành, hãy chọn <strong>Tự động tạo nhóm</strong>. Số lượng nguồn lực cần thiết được thêm vào WBS và tab <strong>Lập lịch trình dự án và nhóm</strong>.</td>
</tr>
<tr class="odd">
<td>Nguồn lực (danh sách thả xuống)</td>
<td>Trên trang <strong>Khởi chạy phân công nguồn lực</strong>, bạn có thể chọn nguồn lực để đặt trước chắc chắn hoặc đặt trước dự kiến, dựa trên khoảng thời gian cụ thể. Bạn có thể điều chỉnh thiết đặt dạng xem để xem và thiết lập khoảng thời gian của hoạt động nguồn lực. Bạn có thể chọn và chỉ định nguồn lực ở cấp độ gói công việc bằng cách sử dụng các tùy chọn sau:
<ul>
<li><strong>Chấp nhận</strong> – Xác nhận các thay đổi đối với nguồn lực được gán cho một nhiệm vụ.</li>
<li><strong>Hủy</strong> – Hủy các thay đổi đối với nguồn lực được gán cho một nhiệm vụ.</li>
<li><strong>Gán tự động</strong> – Một nguồn lực biên chế có vai trò phù hợp được tự động chọn và gán cho nhiệm vụ đã chọn.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Trên trang **Tất cả dự án** , chọn dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Chọn **Kế hoạch** > **Hoạt động** > **Cấu trúc phân tích công việc**.
3. Chọn **Mới** để thêm các hoạt động cấp độ một sau đây vào WBS:

    - Bắt đầu
    - Lập kế hoạch
    - Đang thực thi
    - Giám sát và kiểm soát
    - Đóng

4. Thiết lập ngày và nhân công (số giờ) như trong hình minh họa sau.

    [![Thiết lập ngày và nhân công](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Chọn dòng nhiệm vụ **Bắt đầu** rồi trong trường **Vai trò** , chọn **Người quản lý dự án cấp cao**.
6. Chọn **Xuất bản**.
7. Trên cùng một dòng, trong trường **Nguồn lực** , chọn **Daniel Goldschmidt** rồi chọn **Chấp nhận**.
8. Chọn dòng công việc **Lập kế hoạch** , rồi trong trường **Vai trò** , chọn **Phân tích viên kinh doanh**.
9. Chọn **Phát hành** rồi chọn **Tự động tạo nhóm**.
10. Trong hộp thông báo xuất hiện, chọn **Có**.
11. Trong trường **Nguồn lực** , xác minh rằng giá trị là **Phân tích viên kinh doanh 1**.
12. Đối với nguồn lực **Phân tích viên kinh doanh 1** , mở mục tra cứu rồi chọn **Triển khai phân công nguồn lực**. Sau đó, chọn nhân viên cho nhiệm vụ.
13. Chọn **Gán dự kiến** &gt; **Năng lực đầy đủ**.

    > [!NOTE] 
    > Bạn không nhận được cảnh báo rằng nguồn lực được chỉ định hiện là 2, vì số lượng nguồn lực vẫn là 1.

14. Trên trang **Cấu trúc phân tích công việc** , xác thực phân công nguồn lực trên WBS rồi chọn **Lưu**.
