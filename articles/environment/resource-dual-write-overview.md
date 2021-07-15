---
title: Tích hợp ghi kép của Project Operations
description: Chủ đề này cung cấp tổng quan về tích hợp ghi kép của Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368457"
---
# <a name="project-operations-dual-write-integration-overview"></a>Tổng quan về tích hợp ghi kép của Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Project Operations sử dụng [tính năng ghi kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) để đồng bộ hóa dữ liệu trên Microsoft Dataverse và Dynamics 365 Finance.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa như một phần của tích hợp này giữa Dataverse và Tài chính.

![Tổng quan về luồng dữ liệu của Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations trên Dataverse cung cấp giao diện người dùng (UI) hiện đại và khả năng mở rộng dễ dàng không mã/ít mã bằng cách sử dụng tính năng Power Platform. Người quản lý dự án, Người quản lý nguồn lực, thành viên nhóm Dự án và các nhân viên văn phòng khác thực hiện các hoạt động của họ trong Project Operations trên Dataverse.

Project Operations trong Tài chính cung cấp hỗ trợ kế toán dự án và ghi nhận doanh thu. Project Operations kết hợp với khuôn khổ tài chính trong Tài chính để tính thuế bán hàng, tỷ giá hối đoái, báo cáo lĩnh vực tài chính, v.v. Kinh nghiệm của kế toán viên Dự án chủ yếu dựa trên Tài chính.

Tích hợp Project Operations bao gồm tích hợp thành phần sau:


- [Tích hợp dữ liệu cấu hình và thiết lập Project Operations](resource-dual-write-setup-integration.md) 
- [Giá trị ước tính và thực tế của dự án](resource-dual-write-estimates-actuals.md)
- [Hóa đơn dự án](resource-dual-write-project-invoice.md)
- [Quản lý chi phí](resource-dual-write-expense.md)
- [Hóa đơn của nhà cung cấp](resource-dual-write-vendor-invoice.md)
