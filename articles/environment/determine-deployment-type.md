---
title: Loại triển khai
description: Chủ đề này cung cấp thông tin nhằm giúp bạn xác định đúng loại triển khai Project Operations cho công ty của bạn.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949138"
---
# <a name="deployment-types"></a>Loại triển khai

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

> [!IMPORTANT]
> Sau khi bạn mua giấy phép, hãy bắt đầu tại đây để xác định mô hình triển khai tốt nhất của Dynamics 365 Project Operations bằng cách sử dụng [Quy trình cài đặt có hướng dẫn](https://aka.ms/provisionprojectoperations).
> Sau khi hoàn thành quy trình cài đặt có hướng dẫn, bạn sẽ được chuyển đến đúng cổng quản lý để hoàn tất quá trình cài đặt của mình. Xem chi tiết triển khai bên dưới để hoàn tất cài đặt.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Khách hàng hiện tại của Dynamics đang sử dụng Dynamics 365 Project Service Automation
Project Operations bao gồm các khả năng đi kèm với Project Service Automation. Đường dẫn nâng cấp sẽ được phát hành cho những khách hàng này trong tương lai.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Khách hàng hiện tại của Dynamics 365 Finance sử dụng kế toán và quản lý dự án 

Các khách hàng hiện tại của Finance sử dụng chức năng kế toán và quản lý dự án có thể tiếp tục sử dụng chức năng này. Xem [Project Operations dành cho kịch bản dựa trên hàng nhập kho/lệnh sản xuất](#pma).

Project Operations hỗ trợ nhiều tùy chọn triển khai để phù hợp với yêu cầu của bạn. Cho dù bạn là khách hàng Dynamics 365 mới hay hiện tại, Project Operations có thể hỗ trợ nhu cầu của bạn.

[Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations) của chúng tôi sẽ giúp bạn xác định đúng mô hình triển khai. Kết quả sẽ hướng dẫn bạn đến một trong các kiểu triển khai sau:

- [Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn chiếu lệ](#lite)
- [Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho](#integrated)
- [Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất](#pma)

Project Operations hỗ trợ các kịch bản dựa trên hàng nhập kho/lệnh sản xuất và các kịch bản dựa trên hàng không nhập kho/nguồn lực trên cùng một môi trường thông qua các cấu hình cấp pháp nhân. Ví dụ: Contoso có thể tận dụng khả năng hàng nhập kho/lệnh sản xuất tại cơ sở sản xuất ở Hoa Kỳ của họ (Pháp nhân = Contoso Manufacturing United States) và các khả năng dựa trên nguồn lực/hàng không nhập kho trong cơ sở cung cấp cánh tay robot Contoso của họ ở Vương quốc Anh (Pháp nhân = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá
Việc triển khai đơn giản bao gồm các khả năng sau:

- Lập kế hoạch dự án bằng Microsoft Project dành cho web
- Định giá dựa trên nhiều thông số
- Quản lý nguồn lực hợp nhất
- Theo dõi thời gian
- Chi phí cơ bản
- Đề xuất hóa đơn

### <a name="deployment-steps"></a>Các bước triển khai:
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](lite-preview-subscription-sign-up.md) và [Cung cấp môi trường mới](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho
Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho bao gồm các khả năng sau:
  
- Lập kế hoạch dự án bằng Microsoft Project dành cho web
- Định giá dựa trên nhiều thông số
- Quản lý nguồn lực hợp nhất
- Theo dõi thời gian
- Chi phí cơ bản
- Chi phí đầy đủ
- Biên nhận OCR
- Lập hóa đơn đầy đủ
- Ghi nhận doanh thu

### <a name="deployment-steps"></a>Các bước triển khai:
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](resource-sign-up-preview-subscription.md) và [Cung cấp môi trường mới](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất

- Lập kế hoạch dự án bằng WBS
- Quản lý nguồn lực
- Theo dõi thời gian
- Chi phí đầy đủ
- Biên nhận OCR
- Lập hóa đơn đầy đủ
- Ghi nhận doanh thu
- Đơn hàng sản xuất
- Hỗ trợ vật tư

### <a name="deployment-steps"></a>Các bước triển khai:
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) và [Cung cấp môi trường mới](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



