---
title: Tổng quan về Project Service Automation
description: Chủ đề này cung cấp thông tin về giải pháp tích hợp Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369645"
---
# <a name="project-service-automation-overview"></a>Tổng quan về Project Service Automation

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Dynamics 365 Finance và Dynamics 365 Project Service Automation qua Common Data Service. Mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu cho phép dòng dữ liệu về dự án, hợp đồng dự án, mô tả hợp đồng dự án, mốc thời gian mô tả hợp đồng dự án, nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ và ước tính chi phí từ Project Service Automation sang Finance.

> [!NOTE]
> - Nếu đang sử dụng phiên bản 7.3.0, bạn phải cài đặt KB 4074835. Sau đó, bạn sẽ có thể tích hợp các dự án giá cố định.
> - Nếu bạn đang sử dụng phiên bản 7.3.0 và bạn đang chuyển các giao dịch phí từ Project Service Automation, bạn phải cài đặt KB 4345320 để bao gồm các khoản phí đó trong hóa đơn dự án.
> - Nếu bạn đang sử dụng phiên bản 8.0, bạn có thể sử dụng tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng.
> - Nếu bạn đang sử dụng phiên bản 8.0.1 trở lên, bạn sẽ có thể đồng bộ hóa giá trị thực tế.

Trước khi bạn có thể tích hợp Project Service Automation Finance, bạn phải đặt cấu hình các tham số tích hợp Project Service Automation. Để biết thêm thông tin, hãy xem [tham số tích hợp Project Service Automation](PSA-parameters.md).

Giải pháp tích hợp này cho phép đồng bộ hóa trực tiếp trong các trường hợp sau:

- Duy trì các hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Tạo dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Duy trì các mô tả hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Duy trì các mốc thời gian mô tả hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Duy trì các nhiệm vụ dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Duy trì các thể loại giao dịch chi phí trong Finance và đồng bộ hóa chúng trực tiếp từ Finance sang Project Service Automation.
- Tạo ước tính giờ dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Tạo ước tính chi phí dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.
- Tạo thời gian dự án, chi phí và giá trị thực tế của chi phí trong Project Service Automation và tạo các giao dịch dự án trong nhật ký tích hợp Project Service Automation sao cho chúng có thể được đăng trên Finance.

## <a name="data-synchronization"></a>Đồng bộ hóa dữ liệu

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa như một phần của quá trình tích hợp giữa Project Service Automation và Finance.

> [!NOTE]
> Không phải tất cả các mẫu đều có sẵn. Các mẫu sẽ được phát hành khi chúng hoàn thành.

[![Tích hợp Project Service Automation với Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Yêu cầu hệ thống đối với Finance

Để sử dụng giải pháp tích hợp Project Service Automation với Finance, bạn phải cài đặt Enterprise Edition 7.3 với bản cập nhật Nền tảng từ 12 trở lên.

## <a name="system-requirements-for-project-service-automation"></a>Yêu cầu hệ thống đối với Project Service Automation

Để sử dụng giải pháp tích hợp Project Service Automation sang Finance, bạn phải cài đặt các thành phần sau:

- Dynamics 365 Project Service Automation phiên bản 9.0.0.0 trở lên
- Triển vọng giải pháp tiền mặt cho Dynamics 365 Sales, phiên bản 1.14.0.0 (v14) trở lên
- Giải pháp Project Service Automation sang Finance cho Dynamics 365 Project Service Automation phiên bản 1.0.0.0 trở lên

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Cài đặt giải pháp tích hợp Project Service Automation sang Finance trong phiên bản Project Service Automation của bạn

Tải xuống giải pháp tích hợp Project Service Automation sang Finance từ [Trung tâm Tải xuống của Microsoft ](https://www.microsoft.com/download/details.aspx?id=57016) và làm theo hướng dẫn đi kèm với giải pháp.


[!INCLUDE[footer-include](../includes/footer-banner.md)]