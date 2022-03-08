---
title: Tính năng mới kể từ tháng 11 năm 2020 – Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 11 năm 2020 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9eda9d75f5a4d71e6e4b8bd22dce973270639db3f927ac6a76be5b3c4303fc31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007982"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 11 năm 2020 – Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường CDS phiên bản 4.4.0.70
- Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Các bản cập nhật Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho

### <a name="project-operations-on-cds"></a>Project Operations trên CDS

| Lĩnh vực tính năng                 | Số tham chiếu | Cập nhật chất lượng                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Quản lý cơ hội       | 2036993          | Mô tả ước tính và mô tả hợp đồng chuyển nhượng nguồn lực được cập nhật trên các báo giá trúng thầu khi loại mô tả báo giá là **Tất cả nhiệm vụ**.                                                 |
| Định giá và thanh toán          | 2070392          | Các mô tả hợp đồng dự án trên hóa đơn tăng lên mỗi khi **Làm mới các giao dịch trên hóa đơn** được chọn.                                                                         |
| Lập kế hoạch dự án             | 2043336          | Không thể xóa hồ sơ thành viên nhóm dự án.                                                                                                                                  |
| Lập kế hoạch dự án             | 2046013          | Hành vi không nhất quán đối với cột thẻ Ước tính trong khi tải so với khi thay đổi loại giai đoạn thời gian.                                                                                   |
| Lập kế hoạch dự án             | 2046647          | Thời gian bắt đầu và kết thúc bị chênh lệch một giờ khi các thành viên trong nhóm dự án tạo yêu cầu về nguồn lực.                                                                      |
| Lập kế hoạch dự án             | 2053879          | (Theo bản phát hành CDS sắp tới) PublishUnassignedAssignments phá vỡ nỗ lực lưu một nhiệm vụ khi có lỗi "Giá trị được truyền cho ConditionOperator.In trống".                       |
| Lập kế hoạch dự án             | 2055501          | Để trống **Ngày bắt đầu dự án** sẽ gây ra lỗi trong lịch trình.                                                                                                      |
| Lập kế hoạch dự án             | 2066817          | Không thể tạo nguồn lực chung bằng cách sử dụng bộ chọn người trên tab **Nhiệm vụ**.                                                                                                   |
| Lập kế hoạch dự án             | 2067034          | Nút **Xem chi tiết** không có trên trang **Chi tiết nhiệm vụ**.                                                                                                       |
| Quản lý nguồn lực          | 2046667          | Các thành viên trong nhóm chung sẽ không bị xóa ngay cả khi tất cả các nguồn lực đã được đáp ứng.                                                                                                    |
| Mục nhập chi phí nhanh và thời gian | 2047499          | Nút **Mới** trên trang Mục nhập thời gian sẽ mở ra trang **Chữ ký email mới**.                                                                                               |
| Mục nhập chi phí nhanh và thời gian | 2059859          | Cửa sổ bật lên bất ngờ mở ra khi tạo mục nhập chi phí.                                                                                                                         |
| Khác                        | 2044181          | (Gỡ cài đặt đơn đặt hàng) Lỗi "Bản ghi không khả dụng" xảy ra khi cố gỡ cài đặt các giải pháp cốt lõi của Dịch vụ dự án msdyn_ProjectServiceCore_Patch và msdyn Project.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng        | Số tham chiếu | Cập nhật chất lượng                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ghi nhận doanh thu | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Phần trăm dự toán hoàn thành của dự án bị sai khi hợp đồng sử dụng ngoại tệ và phần trăm tiến độ công việc cho phương pháp hoàn thành.                     |
| Ghi nhận doanh thu | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Không thể đăng số liệu ước tính bằng phương pháp hoàn thành **Chi phí thực tế**.                                                                                                    |
| Ghi nhận doanh thu | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Quá trình loại bỏ không thành công do lỗi mất cân bằng chứng từ khi đơn vị tiền tệ của công ty và đơn vị tiền tệ giao dịch khác nhau.                                              |
| Quản lý chi phí  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Đối với người dùng không phải quản trị viên, giá trị tra cứu của các cột mô tả chi phí như **ID dự án** và **Thể loại chi phí** không hiển thị chính xác trong khung kết nối dữ liệu. |
| Quản lý chi phí  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Thuộc tính mô tả mặc định không hiển thị cho các thể loại Chi phí.                                                                                                         |
| Quản lý chi phí  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Tích hợp chi phí phải bao gồm thuộc tính mô tả từ báo cáo chi phí.                                                                                             |
| Lập hóa đơn           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Không thể đăng đề xuất hóa đơn dự án vì thông báo lỗi cho biết sự kết hợp của FD chưa được xác thực.                                                    |
| Lập hóa đơn           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Không thể xem các giao dịch từ trang chi tiết **hóa đơn**.                                                                                                              |
| Lập hóa đơn           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Các mô tả đề xuất hóa đơn có thể bị xóa.                                                                                                                                  |
| Kế toán dự án  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Các mục menu **Dự báo** không hiển thị trên trang danh sách **Dự án**.                                                                                                   |
| Kế toán dự án  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Không mở được **Bản báo cáo dự án**   > **Giao dịch và dự báo**.                                                                                                       |
| Kế toán dự án  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Điều chỉnh kế toán** không được kích hoạt cho các giao dịch dự án đã lập hóa đơn.                                                                                                  |
| Kế toán dự án  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Chi tiết kế toán không có trên bảng **ProjCDSActualsImport** khi nhật ký **Tích hợp** được đăng.                                                  |
| Kế toán dự án  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Mục nhập Dự báo dự án được nhân đôi khi bạn xóa rồi thêm lại một nguồn lực được chỉ định.                                                                            |
| Kế toán dự án  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Việc chọn liên kết ID dự án sẽ không mở URL liên kết sâu CDS.                                                                                                         |
| Kế toán dự án  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Không thể cập nhật ngày bắt đầu của một nhiệm vụ trong CDS.                                                                                                                           |
| Kế toán dự án  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Khi bật tính năng này, không thể có Nhiều mô tả hợp đồng nếu không tích hợp CDS.                                                                                   |

### <a name="regulatory-updates"></a>Bản cập nhật theo quy định
Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng Finance and Operations, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào LCS và xem các bản cập nhật theo quy định đã lên kế hoạch bằng cách sử dụng Công cụ tìm kiếm vấn đề. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]