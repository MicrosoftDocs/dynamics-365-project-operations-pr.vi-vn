---
title: Quyền truy cập sớm đợt 2 năm 2021 có gì mới - Triển khai Project Operations bản đơn giản
description: Bài viết này cung cấp thông tin về các tính năng có trong bản phát hành truy cập sớm làn sóng 2 năm 2021 của triển khai Project Operations lite.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924134"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Quyền truy cập sớm đợt 2 năm 2021 có gì mới - Triển khai Project Operations bản đơn giản

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

  - Project Operations trên môi trường Dataverse phiên bản 4.23.0.4

Bản phát hành chỉ được áp dụng khi một môi trường [đã chọn tham gia Quyền truy cập sớm](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

[Quản lý hợp đồng phụ](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Tính năng này cung cấp khả năng hiển thị và kiểm soát tốt hơn đối với tất cả các khía cạnh của công việc trong một dự án. Bản xem trước của quản lý hợp đồng phụ bao gồm các năng lực sau:

  - Người quản lý dự án có thể tạo một hợp đồng phụ với một nhà cung cấp. Theo mặc định, bảng giá được đính kèm với hồ sơ nhà cung cấp được sử dụng cho hợp đồng phụ. Tài khoản nhà cung cấp có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**.
  - Người quản lý dự án có thể lặp lại tất cả các giao dịch mua dưới dạng mục hàng trên hợp đồng phụ. Mô tả hợp đồng phụ có thể là về thời gian, chi phí hoặc sản phẩm. Lớp giao dịch của mô tả hợp đồng phụ sẽ xác định mô tả đó dùng để làm gì.
  - Người quản lý tài khoản của nhà cung cấp và người quản lý dự án có thể lặp lại hợp đồng phụ. Có thể điều chỉnh giá trong bảng giá mua đính kèm với hợp đồng phụ.
  - Trong quá trình này, nếu mô tả hợp đồng phụ là về thời gian, thì người quản lý tài khoản nhà cung cấp có thể kết hợp các địa chỉ liên hệ của nhà cung cấp với từng mô tả hợp đồng phụ. Việc liên kết này cung cấp thông tin cho người quản lý dự án, người đang làm việc trên hợp đồng phụ. Khi một liên hệ của nhà cung cấp được liên kết với một mô tả hợp đồng phụ, hệ thống sẽ tự động tạo nguồn lực có thể đặt trước từ liên hệ, nếu nguồn lực có thể đặt trước chưa tồn tại.
  - Phương thức thanh toán trên mỗi mô tả hợp đồng phụ có thể là giá cố định hoặc thời gian và vật liệu. Đối với các mô tả hợp đồng phụ giá cố định, lịch hóa đơn dựa trên cột mốc được thiết lập.