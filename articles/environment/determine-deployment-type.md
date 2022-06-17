---
title: Xác định kiểu triển khai của bạn
description: Bài viết này cung cấp thông tin để giúp bạn xác định loại triển khai chính xác của hoạt động Dự án cho công ty của bạn.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 592c1bfdaf5ea6bdbf6c67bc5b82dd5cf979b367
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912220"
---
# <a name="determine-your-deployment-type"></a>Xác định kiểu triển khai của bạn

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

> [!IMPORTANT]
> Sau khi bạn mua giấy phép, hãy bắt đầu tại đây để xác định mô hình triển khai tốt nhất cho Dynamics 365 Project Operations sử dụng [Quy trình cài đặt có hướng dẫn](https://aka.ms/provisionprojectoperations).
> Sau khi hoàn thành quy trình cài đặt có hướng dẫn, bạn sẽ được chuyển đến đúng cổng quản lý để hoàn tất quá trình cài đặt của mình. Xem thông tin chi tiết triển khai để hoàn tất việc cài đặt.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Khách hàng hiện tại của Dynamics đang sử dụng Dynamics 365 Project Service Automation
Project Operations bao gồm các khả năng đi kèm với Project Service Automation. Đường dẫn nâng cấp sẽ ra mắt những khách hàng này trong bản phát hành đợt 1 năm 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Khách hàng hiện tại của Dynamics 365 Finance sử dụng Quản lý dự án và kế toán 

Các khách hàng hiện tại của Finance sử dụng tính năng Kế toán và quản lý dự án vẫn có thể tiếp tục sử dụng tính năng này như cũ. Xem [Project Operations dành cho kịch bản dựa trên hàng nhập kho/lệnh sản xuất](#pma).


## <a name="deployment-regions"></a>Khu vực triển khai
Để xác định khu vực nào hỗ trợ triển khai Project Operations, hãy xem [Báo cáo khả năng cung cấp theo khu vực địa lý của Dynamics 365 và Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Chọn **Xem báo cáo** và mở rộng **Dynamics 365 > Ứng dụng Operations > Dynamics 365 Project Operations** để xem các khu vực được hỗ trợ.

## <a name="deployment-types"></a>Loại triển khai
Project Operations hỗ trợ nhiều tùy chọn triển khai để phù hợp với yêu cầu của bạn. Bất kể bạn là khách hàng Dynamics 365 mới hay là khách hàng hiện tại, Project Operations cũng có thể hỗ trợ nhu cầu của bạn.

[Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations) của chúng tôi sẽ giúp bạn xác định đúng mô hình triển khai. Kết quả sẽ hướng dẫn bạn đến một trong các kiểu triển khai sau:

- [Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn chiếu lệ](#lite)
- [Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho](#integrated)
- [Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất](#pma)

Project Operations hỗ trợ các kịch bản dựa trên hàng nhập kho/lệnh sản xuất và các kịch bản dựa trên hàng không nhập kho/nguồn lực trên cùng một môi trường thông qua các cấu hình cấp pháp nhân. Chẳng hạn, Contoso có thể sử dụng các khả năng trữ kho/lệnh sản xuất ở cơ sở sản xuất của họ tại Hoa Kỳ (Pháp nhân = Contoso Manufacturing United States). Contoso có thể sử dụng các khả năng dựa trên tài nguyên/không trữ kho trong cơ sở dịch vụ của Contoso tại Robotics Arms ở Vương quốc Anh (Pháp nhân = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá

Việc triển khai đơn giản bao gồm các khả năng sau:

- Quy trình bán hàng của các dự án mở rộng trải nghiệm cho ứng dụng Dynamics 365 Sales
- Lập kế hoạch dự án bằng Microsoft Project dành cho web
- Định giá dựa trên nhiều thông số
- Quản lý nguồn lực hợp nhất
- Theo dõi thời gian
- Chi phí cơ bản
- Lập hóa đơn ước giá để Người quản lý dự án xem xét và chỉnh sửa 

#### <a name="deployment-steps"></a>Các bước triển khai
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](lite-preview-subscription-sign-up.md) và [Cung cấp môi trường mới](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho
Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho bao gồm các khả năng sau:
 
- Quy trình bán hàng của các dự án mở rộng ứng dụng Dynamics 365 Sales
- Lập kế hoạch dự án bằng Microsoft Project dành cho web
- Định giá dựa trên nhiều thông số
- Quản lý nguồn lực hợp nhất
- Theo dõi thời gian
- Chi phí cơ bản
- Chi phí đầy đủ
- Biên nhận OCR
- Lập hóa đơn ước giá và hóa đơn dành cho khách hàng 
- Ghi nhận doanh thu cho dự án

#### <a name="deployment-steps"></a>Các bước triển khai
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](resource-sign-up-preview-subscription.md) và [Cung cấp môi trường mới](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất

- Lập kế hoạch dự án bằng WBS
- Quản lý nguồn lực
- Theo dõi thời gian
- Chi phí đầy đủ
- Biên nhận OCR
- Lập hóa đơn đầy đủ
- Ghi nhận doanh thu
- Lệnh sản xuất
- Vật tư tồn kho hỗ trợ với hàng tồn kho

#### <a name="deployment-steps"></a>Các bước triển khai
Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).

Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) và [Cung cấp môi trường mới](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]