---
title: Có gì mới vào tháng 2 năm 2022 - Triển khai Project Operations Lite
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản triển khai Project Operations lite tháng 2 năm 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922846"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Có gì mới vào tháng 2 năm 2022 - Triển khai Project Operations Lite

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.28.0.120

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Kể từ bản phát hành này, bạn có thể thêm tối đa 300 thành viên trong nhóm vào một dự án. Trước đây, giới hạn về số lượng thành viên trong nhóm là 150. Để biết thêm thông tin, hãy xem [Các giới hạn của dự án](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2497369 | Hiệu chỉnh vật liệu phải tuân theo giá trị ngày tháng trong **Điều chỉnh** thông số. |
| Định giá và thanh toán | 2498697 | Cải thiện cấu hình bảo mật cho **Thu hồi mục nhập thời gian**. |
| Định giá và thanh toán | 2517455 | Các **Các giao dịch dòng hóa đơn được làm mới** không được phép thực hiện hành động nhiều lần đồng thời cho cùng một hóa đơn. |
| Định giá và thanh toán | 2517465 | Các **Hủy kích hoạt chi tiết dòng hóa đơn** hành động bị chặn vì nó không được hỗ trợ. |
| Định giá và thanh toán | 2556660 | Đã sửa lỗi kiểm tra tính hiệu quả ngày được thực hiện trên bảng giá được đính kèm với bản ghi thông số dự án. |
|   Quản lý cơ hội | 2369202 | Đã chỉnh sửa logic nghiệp vụ xác minh rằng các bảng giá có ngày hiệu lực trùng nhau có thể được đính kèm vào cùng một hợp đồng dự án. |
|   Quản lý cơ hội | 2385965 | Đã sửa hành vi trên **Khách hàng** tab của **Hợp đồng dự án** trang khi bạn chọn **Lưu và đóng**. |
