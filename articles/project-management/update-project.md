---
title: Tạo và cập nhật dự án
description: Bài viết này cung cấp thông tin về cách cập nhật dự án trong Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911116"
---
# <a name="create-and-update-a-project"></a>Tạo và cập nhật dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sau đây là tóm tắt về các trường có thể được cập nhật trên một dự án sau khi nó đã được tạo. Điều này cũng bao gồm bất kỳ ngụ ý áp dụng nào dựa trên các bản cập nhật này.

## <a name="project-detail-fields"></a>Các trường chi tiết dự án

- **Tên**: Tiêu đề của dự án.
- **Mô tả**: Thông tin tổng quan về dự án.
- **Khách hàng**: Công ty mà dự án sẽ được chuyển giao.
- **Mẫu lịch**: Giờ làm việc của dự án. Khi trường được thay đổi, toàn bộ lịch trình sẽ được tính toán lại.
- **Tiền tệ**: Đơn vị tiền tệ cho dự án. Giá trị mặc định cho trường này dựa trên đơn vị tiền tệ được xác định trong đơn vị hợp đồng. Khi đơn vị hợp đồng được cập nhật, trường cũng được cập nhật.
- **Đơn vị ký hợp đồng**: Đơn vị tổ chức đại diện cho nhóm hoặc bộ phận của công ty có trách nhiệm chính là giành được hợp đồng bán hàng và quản lý việc cung cấp công việc cũng như dịch vụ cho khách hàng.  Khi đơn vị tổ chức của người quản lý dự án không được xác định, trường này mặc định là giá trị được xác định trong các tham số dự án.
- **Quản lý dự án** : Thành viên nhóm dự án, người có thẩm quyền xem xét và phê duyệt các mục nhập thời gian và chi phí.

## <a name="estimate-fields"></a>Trường ước tính

- **Ngày bắt đầu dự tính** : Ngày mà dự án sẽ bắt đầu. Khi trường này được cập nhật, mọi nhiệm vụ trên dự án sẽ di chuyển tương ứng với ngày bắt đầu mới.
- **Ngày kết thúc**: Ngày dự án kết thúc.
- **Nhân công**: Nhân công ước tính của dự án. Khi các nhiệm vụ được thêm vào dự án, trường này không thể chỉnh sửa được nữa.
- **Chi phí lao động ước tính**: Giá nhân công ước tính của dự án. Khi chi phí lao động được thêm vào dự án, trường này không thể chỉnh sửa được nữa.
- **Chi phí ước tính**: Các chi phí ước tính của dự án. Khi các chi phí được thêm vào dự án, trường này không thể chỉnh sửa được nữa.

## <a name="project-actual-fields"></a>Trường giá trị thực tế của dự án
- **Ngày bắt đầu thực tế** : Ngày mà dự án đã bắt đầu.
- **Ngày kết thúc thực tế** : Được cập nhật sau khi dự án đã hoàn thành.

## <a name="project-status-fields"></a>Trường trạng thái dự án

- **Trạng thái tổng thể của dự án**: Tình trạng tổng thể của dự án do người quản lý Dự án cung cấp.
- **Nhận xét**: Bản tường thuật về tình trạng hiện tại của dự án do người quản lý Dự án cung cấp.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
