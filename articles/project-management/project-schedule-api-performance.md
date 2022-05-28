---
title: Hiệu suất API lịch trình Dự án
description: Chủ đề này cung cấp thông tin về điểm chuẩn hiệu suất của các API lịch trình Dự án và xác định các phương pháp hay nhất để sử dụng tối ưu.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593868"
---
# <a name="project-schedule-api-performance"></a>Hiệu suất API lịch trình Dự án

_**Áp dụng cho:** Project Operations cho các kịch bản dựa trên nguồn lực/không trữ kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá, Project for the web_

Chủ đề này cung cấp thông tin về điểm chuẩn hiệu suất của các giao diện lập trình ứng dụng (API) theo lịch trình Dự án và xác định các phương pháp hay nhất để tối ưu hóa việc sử dụng.

## <a name="project-scheduling-service"></a>Dịch vụ lập lịch dự án
Dịch vụ lập lịch dự án là một dịch vụ nhiều đối tượng thuê chạy trong Microsoft Azure. Nó được thiết kế để cải thiện sự tương tác bằng cách cung cấp trải nghiệm nhanh chóng và linh hoạt khi người dùng làm việc trong các dự án. Cải tiến này đạt được bằng cách chấp nhận các yêu cầu thay đổi, xử lý chúng và sau đó trả lại kết quả ngay lập tức. Dịch vụ không đồng bộ vẫn tồn tại đến Dataverse và không chặn người dùng thực hiện các thao tác khác.

Các API lịch trình dự án dựa vào Dịch vụ lập lịch dự án để chạy các yêu cầu được mô tả chi tiết hơn trong các phần sau của chủ đề này.

Các API lịch trình dự án được thiết kế để hoạt động với các thực thể cấu trúc phân tích công việc (WBS) sau đây:

  - Dự án
  - Nhiệm vụ dự án
  - Quan hệ phụ thuộc Nhiệm vụ Dự án
  - Thành viên Nhóm Dự án
  - Gán Nguồn lực
  
Cả trường sẵn dùng và trường tùy chỉnh đều được hỗ trợ. Trừ khi có ghi chú khác, tất cả các thao tác phổ biến đều được hỗ trợ, chẳng hạn như tạo, cập nhật và xóa. Để biết thêm thông tin, hãy xem [Sử dụng API lịch trình dự án để thực hiện các hoạt động và các thực thể lập lịch](schedule-api-preview.md).

Là một phần của API lịch trình dự án, một mẫu đơn vị công việc đã được thêm vào. Mẫu này được gọi là OperationSet và nó có thể được sử dụng khi một số yêu cầu phải được xử lý trong một giao dịch duy nhất.

Hình minh họa sau đây cho thấy quy trình mà một đối tác sẽ trải qua khi sử dụng tính năng này.

![Dataverse và quy trình dịch vụ lập lịch dự án.](./media/dataverse-project-scheduling-service-flow.png)

**Bước 1**: Máy khách thực hiện lệnh gọi API tới điểm cuối Giao thức dữ liệu mở (OData) trong Dataverse để tạo một OperationSet.

**Bước 2**: Sau khi OperationSet mới được tạo, một giá trị **OperationSetId** được trả về.

**Bước 3**: Khách hàng sử dụng giá trị **OperationSetId** để thực hiện một yêu cầu API lịch trình dự án khác. Kết quả là một yêu cầu tạo, cập nhật hoặc xóa trên một thực thể lập lịch. Khi yêu cầu này được thực hiện, quá trình xác thực siêu dữ liệu được thực hiện. Nếu xác thực không thành công, yêu cầu sẽ bị chấm dứt và lỗi sẽ được trả về.

**Bước 4a – 4c**: Các bước này đại diện cho giai đoạn CHẤP NHẬN. Khách hàng gọi API **ExecuteOperationSetV1**, sẽ gửi tất cả các thay đổi đến Dịch vụ lập lịch dự án trong một đợt. Dịch vụ lập lịch dự án chạy các xác nhận của riêng nó đối với các yêu cầu trong đợt. Bất kỳ lỗi xác thực nào sẽ hoàn tác đợt đó và trả về một ngoại lệ cho người gọi. Nếu đợt đó được Dịch vụ lập lịch dự án chấp nhận thành công, trạng thái OperationSet được cập nhật để phản ánh thực tế là OperationSet đang được Dịch vụ lập lịch dự án xử lý.

**Bước 5**: Bước này thể hiện là giai đoạn PERSIST. Dịch vụ lập lịch dự án ghi đợt vào Dataverse trong một giao dịch. Nếu thao tác ghi thành công, OperationSet được đánh dấu là **Hoàn thành**. Bất kỳ lỗi nào sẽ quay trở lại giao dịch và đợt, và OperationSet được đánh dấu là **Không thành công**.

## <a name="performance-methodology"></a>Phương pháp hiệu suất
Thời gian thực thi được định nghĩa là thời gian từ cuộc gọi đến API **ExecuteOperationSetV1** cho đến khi Dịch vụ lập lịch dự án hoàn tất việc ghi vào Dataverse. Tất cả các hoạt động chạy tổng cộng 2.200 lần và các phép đo thời gian thực hiện P99 được báo cáo. Các hoạt động đơn lẻ và hàng loạt được đo lường.

Đối với một thao tác ghi đơn, OperationSet chứa một yêu cầu. Đối với các hoạt động hàng loạt, nó chứa 20, 50 hoặc 100 yêu cầu. Mỗi quy mô hàng loạt được báo cáo riêng.

Các hoạt động này chạy trên bản triển khai UR 15 Project Operations Lite ở Bắc Mỹ.

## <a name="results"></a>Kết quả
### <a name="create-operations"></a>Tạo hoạt động
#### <a name="single-record-create-operations"></a>Hoạt động tạo bản ghi đơn
Bảng sau đây cho thấy thời gian thực hiện để tạo một bản ghi. Thời gian tính bằng giây.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Loại&nbsp;&nbsp;&nbsp;bản ghi</th>
    <th class="tg-0lax" colspan="2">Thời gian</th>
  </tr>
  <tr>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Dự án</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tác vụ</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hoạt động gán</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Thành viên nhóm</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Quan hệ phụ thuộc</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Hoạt động tạo hàng loạt
Bảng sau đây cho thấy thời gian thực hiện để tạo nhiều bản ghi. Cụ thể, Microsoft đã đo thời gian thực thi để tạo 20, 50 và 100 bản ghi trong một OperationSet. Thời gian tính bằng giây.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Loại&nbsp;&nbsp;&nbsp;bản ghi</th>
    <th class="tg-0lax" colspan="6">Thời gian</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 bản ghi</th>
    <th class="tg-0lax" colspan="2">50 bản ghi</th>
    <th class="tg-0lax" colspan="2">100 bản ghi</th>
  </tr>
  <tr>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tác vụ</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hoạt động gán</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Quan hệ phụ thuộc</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Các hoạt động tạo hàng loạt trên các thực thể **Dự án** và **Thành viên nhóm** không được bao gồm trong bảng này, vì thời gian chạy cho các hoạt động đó giống thời gian chạy khi API để tạo một bản ghi là được gọi nhiều lần. Các API này được chạy ngay lập tức trong Dataverse.

Hình minh họa sau đây cho thấy sơ đồ về thời gian thực thi của các thực thể **Nhiệm vụ**, **Chỉ định** và **Sự phụ thuộc** khi các bản ghi 20, 50 và 100 được tạo và tất cả các trường được hỗ trợ đều được sử dụng.

![Tạo đồ thị thời gian thực hiện bản ghi.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Cập nhật hoạt động
#### <a name="single-record-update-operations"></a>Hoạt động cập nhật bản ghi đơn
Bảng sau đây cho thấy thời gian thực hiện để cập nhật một bản ghi. Thời gian tính bằng giây.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Loại&nbsp;&nbsp;&nbsp;bản ghi</th>
    <th class="tg-0lax" colspan="2">Thời gian</th>
  </tr>
  <tr>
    <th class="tg-0lax">Trường bắt buộc </th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Dự án</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tác vụ</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Thành viên nhóm</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Cập nhật hoạt động trên thực thể **Chỉ định nguồn lực** và **Sự phụ thuộc vào nhiệm vụ dự án** không được hỗ trợ.

#### <a name="bulk-update-operations"></a>Hoạt động cập nhật hàng loạt
Bảng sau đây cho thấy thời gian thực hiện để cập nhật nhiều bản ghi. Cụ thể, Microsoft đã đo thời gian thực thi để cập nhật 20, 50 và 100 bản ghi trong một OperationSet. Thời gian tính bằng giây.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Loại&nbsp;&nbsp;&nbsp;bản ghi</th>
    <th class="tg-0lax" colspan="6">Thời gian</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 bản ghi</th>
    <th class="tg-0lax" colspan="2">50 bản ghi</th>
    <th class="tg-0lax" colspan="2">100 bản ghi</th>
  </tr>
  <tr>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
    <th class="tg-0lax">Trường bắt buộc</th>
    <th class="tg-0lax">Tất cả các trường được hỗ trợ</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tác vụ</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Thành viên nhóm</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Cập nhật hoạt động trên thực thể **Chỉ định nguồn lực** và **Sự phụ thuộc vào nhiệm vụ dự án** không được hỗ trợ.

Hình minh họa sau đây cho thấy sơ đồ về thời gian thực thi của các thực thể Nhiệm vụ và Thành viên nhóm khi các bản ghi 20, 50 và 100 được cập nhật và tất cả các trường được hỗ trợ đều được sử dụng.

![Cập nhật đồ thị thời gian thực hiện bản ghi.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Hoạt động xóa
#### <a name="single-record-delete-operations"></a>Hoạt động xóa bản ghi đơn
Bảng sau đây cho thấy thời gian thực hiện để xóa một bản ghi. Thời gian tính bằng giây.

| Loại bản ghi | Thời gian  |
|-------------|-------|
| Tác vụ        | 20.12 |
| Hoạt động gán  | 10.86 |
| Thành viên nhóm | 12.52 |
| Quan hệ phụ thuộc  | 20.89 |

> [!NOTE]
> Các thao tác xóa trên thực thể **Dự án** không được hỗ trợ.

#### <a name="bulk-delete-operations"></a>Thao tác xóa hàng loạt
Bảng sau đây cho thấy thời gian thực hiện để xóa nhiều bản ghi. Cụ thể, Microsoft đã đo thời gian thực thi để xóa 20, 50 và 100 bản ghi trong một OperationSet. Thời gian tính bằng giây.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Loại&nbsp;&nbsp;&nbsp;bản ghi</th>
    <th class="tg-0lax" colspan="3">Thời gian</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 bản ghi</th>
    <th class="tg-0lax">50 bản ghi</th>
    <th class="tg-0lax">100 bản ghi</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tác vụ</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Hoạt động gán</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Thành viên nhóm</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Quan hệ phụ thuộc</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Các thao tác xóa trên thực thể **Dự án** không được hỗ trợ.

Hình minh họa sau đây cho thấy sơ đồ về thời gian thực hiện cho các thực thể **Nhiệm vụ**, **Chỉ định**, **Thành viên nhóm** và **Sự phụ thuộc** khi các bản ghi 20, 50 và 100 bị xóa.

![Xóa đồ thị thời gian thực hiện bản ghi.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Quan sát
Đối với mỗi hoạt động ghi, API **ExecuteOperationSet** mất khoảng 800 mili giây để gửi yêu cầu đến Dịch vụ lập lịch dự án. Sau đó, Dịch vụ lập lịch dự án mất khoảng 5 giây để xử lý tải trọng và cuộc gọi Dataverse. Phần còn lại của thời gian thực thi được dành để chạy logic kinh doanh và ghi dữ liệu vào cơ sở dữ liệu trong Dataverse.

Khi 100 bản ghi được tạo, cập nhật hoặc xóa, API **ExecuteOperationSet** mất khoảng ba giây để gửi yêu cầu đến Dịch vụ lập lịch dự án. Sau đó, Dịch vụ lập lịch dự án mất khoảng 5 giây để xử lý các yêu cầu và cuộc gọi Dataverse. Các hoạt động hàng loạt phải trả **thuế Dịch vụ lập lịch dự án** một lần, cho tất cả các bản ghi trong OperationSet. Do đó, các hoạt động hàng loạt có thời gian thực hiện trung bình thấp hơn đáng kể so với các hoạt động ghi đơn.

## <a name="scenarios"></a>Kịch bản
Bảng sau đây cho thấy thời gian thực thi khi các API lịch trình dự án được sử dụng để hoàn thành các tình huống cụ thể. Thời gian tính bằng giây.

| Kịch bản                                                                   | Thời gian  |
|----------------------------------------------------------------------------|-------|
| Tạo một dự án có 40 nhiệm vụ.                                      | 36.01 |
| Tạo một dự án có 40 nhiệm vụ và 20 mục phụ thuộc.                  | 38.11 |
| Tạo một dự án có 40 nhiệm vụ và 30 phân công.                   | 60.17 |
| Tạo một dự án có 40 nhiệm vụ, 20 mục phụ thuộc và 30 phân công. | 60.27 |

## <a name="best-practices"></a>Thực tiễn tốt nhất
Dựa trên kết quả tình huống trước đó, các API hoạt động tốt hơn trong các điều kiện sau:

  - Nhóm càng nhiều hoạt động với nhau càng tốt. Thời gian chạy trung bình cho các hoạt động hàng loạt tốt hơn thời gian chạy trung bình cho các hoạt động ghi đơn. Số lượng OperationSets được sử dụng càng nhỏ thì thời gian thực thi trung bình càng nhanh.
  - Chỉ đặt các thuộc tính tối thiểu cần thiết để hoàn thành kịch bản của bạn. Hãy chọn lọc về các loại trường không bắt buộc có trong yêu cầu OperationSet. Các trường có chứa khóa ngoại hoặc trường tổng số sẽ ảnh hưởng tiêu cực đến hiệu suất.
