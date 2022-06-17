---
title: Tích hợp hóa đơn của dự án
description: Bài viết này cung cấp thông tin về tích hợp ghi kép Hoạt động dự án để lập hóa đơn cho khách hàng.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912128"
---
# <a name="project-invoice-integration"></a>Tích hợp hóa đơn của dự án

Bài viết này cung cấp thông tin về tích hợp ghi kép Hoạt động dự án để lập hóa đơn cho khách hàng.

Trong Project Operations, Người quản lý dự án quản lý tồn đọng thanh toán của dự án và tạo hóa đơn ước giá cho khách hàng trong Microsoft Dataverse. Dựa trên hóa đơn ước giá này, nhân viên Kế toán khoản phải thu hoặc Kế toán viên của dự án lập hóa đơn giao cho khách hàng. Tích hợp ghi kép đảm bảo rằng các chi tiết hóa đơn chiếu lệ được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động. Sau khi hóa đơn giao cho khách hàng được đăng, hệ thống sẽ cập nhật các giá trị thực tế dự án có liên quan trong Dataverse với chi tiết kế toán. Hình ảnh dưới đây cung cấp tổng quan khái niệm cấp cao về quá trình tích hợp này.

   ![Tích hợp hóa đơn của dự án.](./media/DW5Invoicing.png)

Sau khi người quản lý Dự án xác nhận hóa đơn chiếu lệ trong Dataverse, thông tin tiêu đề hóa đơn chiếu lệ đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng sơ đồ bảng ghi kép, **Đề xuất hóa đơn dự án V2 (hóa đơn)**. Đây là tích hợp một chiều từ Dataverse cho các ứng dụng Tài chính và Hoạt động. Tạo hoặc xóa các đề xuất hóa đơn Dự án trực tiếp trong ứng dụng Tài chính và Hoạt động không được hỗ trợ.

Xác nhận hóa đơn trong Dataverse cũng kích hoạt logic nghiệp vụ để tạo các bản ghi liên quan đến thanh toán trong thực thể **Giá trị thực tế**. Các bản ghi này được đồng bộ hóa với Tài chính và Hoạt động bằng cách sử dụng sơ đồ bảng ghi kép, **Hướng dẫn tích hợp Hoạt động Dự án (msdyn\_ thực tế).** Để biết thêm thông tin, hãy xem [Giá trị ước tính và thực tế của dự án](resource-dual-write-estimates-actuals.md). 

Các mô tả đề xuất hóa đơn dự án được tạo bởi quy trình định kỳ **Nhập tổ chức biểu mẫu**. Quá trình này dựa trên các chi tiết thực tế của bán hàng được lập hóa đơn trong bảng **Tổ chức thực tế**. Để biết thêm thông tin, hãy xem [Quản lý các đề xuất hóa đơn dự án](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
