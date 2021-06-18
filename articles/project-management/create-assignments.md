---
title: Tạo nội dung phân công nguồn lực
description: Chủ đề này cung cấp thông tin về cách tạo nội dung phân công nguồn lực chung và có tên.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 610d9f7abbe7bc2eea8cc9a238dd7cfa1c626787
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006987"
---
# <a name="create-resource-assignments"></a>Tạo nội dung phân công nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Phân công nguồn lực là sự liên kết trực tiếp của một thành viên trong nhóm dự án với một nhiệm vụ nút lá. Chủ đề này cung cấp thông tin về các cách khác nhau để gán nguồn lực.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tạo thành viên nhóm chung bằng phân công nhiệm vụ


Khi tạo một thành viên nhóm chung thông qua phân công nhiệm vụ, bạn sẽ tạo một chỗ dành sẵn hoặc nguồn lực chung. Nguồn lực chung này mô tả các đặc tính của nguồn lực có tên mà cuối cùng bạn muốn làm việc trên nhiệm vụ. Sau đó bạn tạo một yêu cầu hoặc gửi một yêu cầu bằng cách sử dụng yêu cầu được dùng để tìm và đăng ký nguồn lực có tên.

1. Trên lưới Lịch trình cho nhiệm vụ, chọn biểu tượng Nguồn lực trong ô **Nguồn lực**.
2. Nhập một tên để làm tên của nguồn lực đặt chỗ. Ví dụ: Người quản lý Chương trình.
3. Chọn **Tạo** và trong trường **Tạo nhanh Thành viên Nhóm Dự án**, đặt vai trò cho nguồn lực chung.
4. Khi cần, gán nhiệm vụ cho nguồn lực giữ chỗ này bằng cách chọn nguồn lực trên **Bộ chọn nguồn lực** cho nhiệm vụ. Nguồn lực được liệt kê trong phần **Thành viên nhóm**.
5. Khi bạn hoàn thành việc gán nguồn lực chung, trên tab **Nhóm**, chọn nguồn lực chung, sau đó chọn **Tạo yêu cầu** để tạo yêu cầu nguồn lực cho nguồn lực chung.
6. Chọn **Đăng ký** đối với nguồn lực chung và sau đó bạn có thể dùng bảng Lịch trình để tìm và đăng ký nguồn lực thực. Bạn cũng có thể gửi yêu cầu để thực hiện bởi người quản lý nguồn lực.
7. Khi nguồn lực chung được thực hiện đầy đủ (việc đáp ứng yêu cầu nguồn lực một phần sẽ không dẫn đến việc phân công nguồn lực) với nguồn lực có tên, nguồn lực chung sẽ bị xóa khỏi nhóm. Phân công nhiệm vụ cho nguồn lực chung được chỉ định cho nguồn lực có tên đáp ứng yêu cầu về nguồn lực của nguồn lực chung.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Gán một nguồn lực được đặt tên từ danh sách tất cả các nguồn lực có thể đăng ký được

Bạn có thể dùng hộp tìm kiếm trong **Bộ chọn nguồn lực** để tìm tất cả các nguồn lực hiện hoạt có thể đăng ký và gán nguồn lực cho mọi nhiệm vụ nút lá. Các tài nguyên được chỉ định theo cách này sẽ được thêm vào nhóm mà không có bất kỳ đặt chỗ nào. Điều này tương tự như việc thêm một thành viên trong nhóm và chọn **Không có** làm phương pháp phân bổ. Nguồn lực được hiển thị trong tab **Nhóm**, **Phân công nguồn lực** và **Hợp nhất** như là nguồn lực chỉ có phân công còn đặt chỗ bị thâm hụt. Đăng ký chúng nếu bạn muốn sử dụng tính sẵn có của chúng.

1. Từ lưới nhiệm vụ, bảng hoặc dòng thời gian, hãy điều hướng đến ô **Đã phân công cho**.
2. Trong hộp tìm kiếm, bắt đầu nhập tên. Kết quả tìm kiếm cho tên được hiện thị trong **Bộ chọn nguồn lực** trong phần **Các nguồn lực khác**.
3. Chọn nguồn lực mà bạn muốn gán cho nhiệm vụ hoặc chọn tên của nguồn lực trong **Các nguồn lực nhóm khác**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]