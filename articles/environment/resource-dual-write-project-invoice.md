---
title: Tích hợp hóa đơn của dự án
description: Chủ đề này cung cấp thông tin về tích hợp ghi kép của Project Operations đối với hóa đơn của khách hàng.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993267"
---
# <a name="project-invoice-integration"></a>Tích hợp hóa đơn của dự án

Chủ đề này cung cấp thông tin về tích hợp ghi kép của Project Operations đối với hóa đơn của khách hàng.

Trong Project Operations, Người quản lý dự án quản lý tồn đọng thanh toán của dự án và tạo hóa đơn ước giá cho khách hàng trong Microsoft Dataverse. Dựa trên hóa đơn ước giá này, nhân viên Kế toán khoản phải thu hoặc Kế toán viên của dự án lập hóa đơn giao cho khách hàng. Tích hợp ghi kép đảm bảo rằng các chi tiết hóa đơn ước giá được đồng bộ hóa với ứng dụng Finance and Operations. Sau khi hóa đơn giao cho khách hàng được đăng, hệ thống sẽ cập nhật các giá trị thực tế dự án có liên quan trong Dataverse với chi tiết kế toán. Hình ảnh dưới đây cung cấp tổng quan khái niệm cấp cao về quá trình tích hợp này.

   ![Tích hợp hóa đơn của dự án.](./media/DW5Invoicing.png)

Sau khi Người quản lý dự án xác nhận hóa đơn ước giá trong Dataverse, thông tin tiêu đề hóa đơn ước giá đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng ghi kép **Đề xuất hóa đơn dự án V2 (hóa đơn)**. Đây là tích hợp một chiều từ Dataverse đến ứng dụng Finance and Operations. Tạo hoặc xóa các đề xuất hóa đơn Dự án trực tiếp trong ứng dụng Finance and Operations không được hỗ trợ.

Xác nhận hóa đơn trong Dataverse cũng kích hoạt logic nghiệp vụ để tạo các bản ghi liên quan đến thanh toán trong thực thể **Giá trị thực tế**. Các bản ghi này được đồng bộ hóa với Finance and Operations bằng bản đồ bảng ghi kép **Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals).** Để biết thêm thông tin, hãy xem [Giá trị ước tính và thực tế của dự án](resource-dual-write-estimates-actuals.md). 

Các mô tả đề xuất hóa đơn dự án được tạo bởi quy trình định kỳ **Nhập tổ chức biểu mẫu**. Quá trình này dựa trên các chi tiết thực tế của bán hàng được lập hóa đơn trong bảng **Tổ chức thực tế**. Để biết thêm thông tin, hãy xem [Quản lý các đề xuất hóa đơn dự án](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
