---
title: Chế độ lập lịch trình
description: Bài viết này cung cấp thông tin về các chế độ lập lịch.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923674"
---
# <a name="scheduling-modes"></a>Chế độ lập lịch trình

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Dynamics 365 Project Operations cung cấp khả năng cho các tổ chức để xác định cách họ quản lý thay đổi đối với các biến chính trong nhiệm vụ của cấu trúc phân tích công việc. Dựa trên nhu cầu cụ thể của tổ chức, Người quản lý dự án có thể thực hiện các thay đổi đối với chế độ lập lịch trình khi một dự án được tạo.

Có ba chế độ lập lịch trình có sẵn trong Project Operations:

  - Khoảng thời gian cố định (đây là chế độ mặc định)
  - Nỗ lực cố định (*Công việc*)
  - Đơn vị cố định

Các giá trị bị định nghĩa của một chế độ lập lịch trình cụ thể tác động được xác định theo công thức sau:

  Nỗ lực = Khoảng thời gian x Đơn vị

Khi xác định chế độ lập lịch trình của dự án, bạn đang thiết lập một trong những giá trị này, sau đó không thể thay đổi được. Duy trì giá trị này là một hằng số sẽ đặt ưu tiên cho giá trị đó, điều này sẽ thông báo cho hệ thống không thay đổi giá trị này khi hai giá trị khác thay đổi. Bảng sau đây cung cấp thông tin về tác động của việc chọn một chế độ cụ thể.

| **Trong nhiệm vụ này**             | **Nếu bạn sửa các đơn vị**   | **Nếu bạn sửa khoảng thời gian** | **Nếu bạn sửa nỗ lực**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Nhiệm vụ đơn vị cố định     | Khoảng thời gian được tính toán lại. | Nỗ lực được tính toán lại.    | Khoảng thời gian được tính toán lại. |
| Nhiệm vụ nỗ lực cố định    | Khoảng thời gian được tính toán lại. | Các đơn vị được tính toán lại.    | Khoảng thời gian được tính toán lại. |
| Nhiệm vụ khoảng thời gian cố định  | Nỗ lực được tính toán lại.   | Nỗ lực được tính toán lại.    | Các đơn vị được tính toán lại.   |

Để biết thêm thông tin về tác động của một chế độ nhất định, hãy xem [Thay đổi loại nhiệm vụ để lập lịch chính xác hơn](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Trong bài báo, thuật ngữ **Công việc** được sử dụng thay vì **Cố gắng**.

## <a name="change-the-organizations-scheduling-mode"></a>Thay đổi chế độ lập lịch trình của tổ chức

Hoàn thành các bước sau để xác định chế độ lập lịch trình của một tổ chức.

1. Chuyển đến phần **Cài đặt** \> **Chung** \> **Thông số** rồi chọn thông số dự án. 
2. Trên trang **Thông số dự án**, hãy chọn chế độ lập lịch trình mặc định cho tổ chức rồi xác định khả năng cho Người quản lý dự án ghi đè cài đặt khi tạo một dự án mới.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Thay đổi tùy chọn cài đặt của chế độ lập lịch trình trên một dự án

Nếu một tổ chức cho phép Người quản lý dự án ghi đè chế độ lập lịch trình mặc định, Người quản lý dự án có thể thực hiện thay đổi đó khi họ tạo một dự án mới. Tuy nhiên, sau khi dự án đã được lưu, không thể thay đổi chế độ lập lịch trình.

## <a name="copied-projects"></a>Dự án được sao chép

Vì dự án được tạo khi thực hiện thao tác sao chép dự án, nên Người quản lý dự án không thể thiết lập chế độ lập lịch trình. Dự án đích sẽ luôn mặc định chuyển về chế độ được xác định ở cấp tổ chức.

## <a name="copied-tasks"></a>Nhiệm vụ được sao chép

Khi được sao chép từ dự án này sang dự án khác, nhiệm vụ sẽ kế thừa chế độ lập lịch trình của dự án đích.
