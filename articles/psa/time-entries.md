---
title: Tạo mục nhập thời gian
description: Chủ đề này cung cấp thông tin về cách tạo mục nhập thời gian.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d0e21d0964788564d3db9173c3a0b3378cd0049b4455a23ccc1bccd1c21d9e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990432"
---
# <a name="create-time-entries"></a>Tạo mục nhập thời gian

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Trong các phiên bản Dynamics 365 Project Service Automation trước, mục nhập thời gian đã được nhập trên cơ sở hàng tuần. Trong phiên bản 3 của Project Service Automation, mục nhập thời gian được nhập trên cơ sở hàng ngày. Tuy nhiên, sau khi một vài mục nhập thời gian đã được tạo, bạn có thể tạo hoặc sao chép hàng loạt các mục nhập đó.

## <a name="create-a-time-entry"></a>Tạo mục nhập thời gian

Làm theo các bước sau để tạo mục nhập thời gian.

1. Trên trang **Mục nhập thời gian**, hãy chọn **Mới**.
2. Trong hộp thoại **Tạo nhanh: Mục thời gian**, hãy nhập khoảng thời gian của mục nhập thời gian theo phút, giờ hoặc ngày. Phải nhập khoảng thời gian theo định dạng sau: *x* phút, *x* giờ hoặc *x* ngày. Cũng có thể nhập giờ và ngày dưới dạng giá trị thập phân, chẳng hạn như *x.x* giờ hoặc *x.x* ngày.
3. Chọn loại mục nhập thời gian và dự án mà bạn đang nhập vào mục nhập thời gian.
4. Trong trường **Nhiệm vụ dự án**, hãy tìm nhiệm vụ cho mục nhập thời gian này.

    > [!NOTE]
    > Nếu bạn đang tạo mục nhập thời gian cho một nhiệm vụ không được gán cho người dùng, thì trong trường **nhiệm vụ dự án**, hãy chọn nút **Tìm kiếm**, chọn **Thay đổi dạng xem** rồi chọn **Tất cả nhiệm vụ dự án đang hoạt động** để liệt kê tất cả nhiệm vụ.

5. Nhập mô tả, nếu mô tả là bắt buộc, sau đó chọn **Lưu và Đóng**.

Sau khi mục nhập thời gian được tạo và lưu, bạn có thể chỉnh sửa trong lưới mục nhập thời gian. Lưới mục nhập thời gian hỗ trợ 2 định dạng:

- Bạn có thể nhập các mục nhập thời gian theo định dạng **hh:mm**. Sau đó, định dạng này được chuyển đổi thành giờ và phân số.
- Bạn có thể nhập trực tiếp số giờ và phân số.

Lưu ý rằng phân số của một giờ không phải là phút. Do đó, 1,5 giờ đại diện cho 1 giờ và 30 phút. Quy tắc này áp dụng cho cả phân số của một ngày. Một ngày là 24 giờ và 0,5 ngày đại diện cho 12 giờ.

## <a name="bulk-create-time-entries"></a>Tạo hàng loạt mục nhập thời gian

Sau khi một vài mục nhập thời gian được tạo, bạn có thể sao chép chúng để tạo thêm hàng loạt các mục nhập thời gian.

1. Trên trang **Mục nhập thời gian**, hãy chọn **Sao chép tuần**.
2. Trong nhóm trường **Từ khoảng thời gian**, trong các trường **Ngày bắt đầu** và **Ngày kết thúc**, hãy xác định phạm vi ngày để sao chép mục nhập thời gian từ đó.
3. Trong trường nhóm **Tới khoảng thời gian**, trong trường **Ngày bắt đầu**, hãy chỉ định ngày để tạo mục nhập thời gian.
4. Chọn **Sao chép** để tạo bản sao của mục nhập thời gian tương ứng với ngày trong tuần được chỉ định trong nhóm trường **Tới khoảng thời gian**. Ví dụ: mục nhập thời gian cho Thứ hai tuần cuối cùng được sao chép vào Thứ hai trong tuần được chỉ định trong nhóm trường  **Tới khoảng thời gian**.

## <a name="import-data-for-time-entries"></a>Nhập dữ liệu cho các mục nhập thời gian

Bạn có thể nhập dữ liệu từ các mục đặt trước và chỉ định. Khi bạn nhập dữ liệu, bạn có thể chỉ định phạm vi ngày của mục đặt trước sẽ nhập, sau đó chọn rõ ràng các mục đặt trước sẽ được tạo dưới dạng mục nhập thời gian **Nháp**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Nhóm theo, sắp xếp, tìm kiếm và lọc khả năng

Bạn có thể nhóm và lọc các mục nhập thời gian theo các thứ nguyên được chỉ định trong các cột. Trong trường **Nhóm theo**, hãy chọn thông số cần sử dụng để lọc các mục nhập thời gian. Bạn cũng có thể sắp xếp các bản ghi mục nhập thời gian theo thứ tự tăng dần hoặc giảm dần bằng cách sử dụng mũi tên sắp xếp trên các tiêu đề cột. Ngoài ra, bạn có thể hiển thị hoặc ẩn các mục nhập bằng cách chọn nút **Lọc** trên tiêu đề cột, rồi sau đó, trong hộp **Tìm kiếm**, nhập văn bản sẽ được sử dụng để tìm kiếm mục nhập thời gian theo tên dự án, nhiệm vụ dự án, mục nhập thời gian hoặc nguồn lực.


[!INCLUDE[footer-include](../includes/footer-banner.md)]