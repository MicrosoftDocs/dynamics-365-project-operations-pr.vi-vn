---
title: Quản lý hợp đồng phụ trong Project Operations
description: Chủ đề này cung cấp thông tin tổng quan về quy trình quản lý hợp đồng phụ từ đầu đến cuối trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994257"
---
# <a name="subcontract-management-in-project-operations"></a>Quản lý hợp đồng phụ trong Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hợp đồng phụ trong Microsoft Dynamics 365 Project Operations hỗ trợ dòng quy trình công việc sau.

![Quy trình hợp đồng phụ](../media/SubcontractingProcessFlow.png)

Dưới đây là mô tả từng bước của quy trình hợp đồng phụ.

1. Người quản lý dự án tạo một hợp đồng phụ với một nhà cung cấp. Theo mặc định, bảng giá được đính kèm với hồ sơ nhà cung cấp được sử dụng cho hợp đồng phụ. Tài khoản nhà cung cấp có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**.
2. Người quản lý dự án có thể lặp lại tất cả các giao dịch mua dưới dạng mục hàng trên hợp đồng phụ. Mô tả hợp đồng phụ có thể là về thời gian, chi phí hoặc sản phẩm. Lớp giao dịch được chọn trên mỗi dòng hợp đồng phụ sẽ xác định dòng đó dùng để làm gì.
3. Người quản lý tài khoản của nhà cung cấp và người quản lý dự án có thể lặp lại hợp đồng phụ. Có thể điều chỉnh giá trong bảng giá mua đính kèm với hợp đồng phụ.
4. Tại thời điểm này hoặc sau đó trong quá trình, nếu mô tả hợp đồng phụ là thời gian, người quản lý tài khoản của nhà cung cấp sẽ kết hợp các địa chỉ liên hệ với từng mô tả hợp đồng phụ. Việc liên kết này cung cấp thông tin cho người quản lý dự án, người đang làm việc trên hợp đồng phụ. Khi một liên hệ được liên kết với một mô tả hợp đồng phụ, hệ thống sẽ tự động tạo nguồn lực có thể đặt trước từ liên hệ, nếu nguồn lực có thể đặt trước chưa tồn tại.
5. Phương thức thanh toán trên mỗi mô tả hợp đồng phụ có thể là **Giá cố định** hoặc **Thời gian và Vật liệu**. Đối với các mô tả hợp đồng phụ giá cố định, bạn có thể thiết lập lịch hóa đơn dựa trên mốc thời gian.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
