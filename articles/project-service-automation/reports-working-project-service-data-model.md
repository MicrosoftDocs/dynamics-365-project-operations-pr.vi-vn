---
title: Làm việc với mô hình dữ liệu Project Service Automation
description: Chủ đề này cung cấp thông tin về cách làm việc với mô hình dữ liệu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e1a177a8-cd16-4ac4-acb8-a8f1a8f9e4bf
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b909099af2493c4010103189c2add6175eea8add
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757110"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Làm việc với mô hình dữ liệu Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation mở rộng các thực thể ứng dụng khác và giới thiệu các thực thể của riêng mình trong mô hình dữ liệu Common Data Service. Chủ đề này mô tả một số thực thể mà bạn sẽ gặp phải trong các trường hợp báo cáo PSA điển hình.

## <a name="reporting-on-opportunities"></a>Báo cáo về cơ hội

Project Service Automation mở rộng thực thể **Cơ hội** Dynamics 365 Sales bằng cách thêm các trường cho phép tình huống dựa trên dự án. Các trường này được xác định bằng tên sơ đồ có tiền tố **msdyn\_**. Một trường mới quan trọng với báo cáo cơ hội PSA là **Loại đơn hàng**. Giá trị **Dựa trên công việc** cho trường này cho biết cơ hội đó là cơ hội PSA. Các trường khác được thêm vào thực thể bao gồm **Tổ chức ký hợp đồng** ghi lại tổ chức đang nắm giữ cơ hội này và **Người quản lý tài khoản** ghi lại tên người quản lý tài khoản phụ trách cơ hội này.

Thực thể **Mô tả cơ hội** cũng bao gồm các trường liên quan đến Project Service. **Phương thức thanh toán** cho biết mô tả cơ hội nên được lập hóa đơn trên cơ sở thời gian và tài liệu hoặc cơ sở giá cố định và **Dự án** ghi lại tên của dự án đang hỗ trợ cơ hội. Các trường khác mà bạn có thể báo cáo về chi phí thu nạp và khoản ngân sách khách hàng cho mục mô tả.

## <a name="reporting-on-quotes"></a>Báo cáo về báo giá

PSA mở rộng thực thể **Báo giá** Bán hàng bằng cách thêm các trường liên quan đến dự án. **Loại đơn hàng** phân biệt báo giá PSA với báo giá không phải PSA. Giá trị **Dựa trên công việc** cho trường này cho biết báo giá đó là báo giá PSA. Các trường khác có thể liên quan đến việc báo cáo về báo giá PSA bao gồm trường khoản tiền, như **Chi phí có thể tính**, **Chi phí không thể tính**, **Lãi gộp**, **Ước tính** và **Ngân sách**. Các trường hữu ích khác cho biết liệu báo giá có lợi nhuận hay không, cho dù nó sẽ được hoàn thành đúng tiến trình, và liệu nó có đáp ứng kỳ vọng ngân sách của khách hàng hay không.

PSA cũng mở rộng thực thể **Mô tả báo giá** Bán hàng. Một trường mà PSA thêm là **Phương thức thanh toán** cho biết cách mô tả báo giá sẽ được lập hóa đơn (thời gian và tài liệu hoặc giá cố định). Các trường khác được thêm vào thực thể ghi lại dự án liên quan hỗ trợ mô tả báo giá, lập hóa đơn, chi phí và ngân sách.

PSA cũng thêm các thực thể liên quan đến báo giá mới vào mô hình dữ liệu Dynamics 365. Dưới đây là một số ví dụ:

- **Chi tiết mô tả báo giá** – Thực thể này chứa chi tiết ước tính dự án của mô tả báo giá. Thực thể này có 2 bản ghi cho mỗi mô tả báo giá. Một bản ghi lưu trữ chi phí và chi tiết chi phí của mô tả báo giá và bản ghi khác lưu trữ khoản bán hàng và chi tiết bán hàng của mô tả báo giá.
- **Lịch trình hóa đơn mô tả báo giá** – Thực thể này chứa lịch trình thanh toán cho mô tả báo giá. Lịch trình này được tạo dựa trên tần suất lập hóa đơn được gán cho mô tả báo giá.
- **Mốc mô tả báo giá** – Thực thể này chứa mốc thanh toán cho mô tả báo giá cố định.
- **Chi tiết phân tích mô tả báo giá** – Thực thể này chứa chi tiết tài chính của một mô tả báo giá. Thông tin chi tiết này có thể hữu ích cho việc báo cáo số tiền bán hàng đã báo giá và số tiền chi phí ước tính theo nhiều tham số khác nhau.

Các thực thể khác mà PSA thêm vào báo giá là **Bảng giá dự án mô tả báo giá**, **Loại nguồn lực mô tả báo giá** và **Loại giao dịch mô tả báo giá**.

![Sơ đồ hiển thị báo giá, dòng báo giá và các mối quan hệ của dự án](media/PS-Reporting-image2.png "Sơ đồ hiển thị báo giá, dòng báo giá và các mối quan hệ của dự án")

## <a name="reporting-on-project-contracts"></a>Báo cáo về hợp đồng dự án

PSA mở rộng thực thể **Đơn** bán hàng được dùng khi hợp đồng dự án được ghi lại. PSA thêm một trường quan trọng mới, **Loại đơn hàng**, xác định hợp đồng ở dạng hợp đồng dự án PSA thay vì đơn bán hàng. Giá trị **Dựa trên công việc** cho trường này chỉ ra đơn hàng này là hợp đồng dự án PSA. Các trường mới khác được thêm vào thực thể **Đơn hàng** ghi lại thông tin chi tiết về chi phí, trạng thái hợp đồng PSA và tổ chức sở hữu hợp đồng.

PSA cũng mở rộng thực thể **Mô tả đơn bán hàng**. Trong số các trường mà nó thêm là trường ghi phương thức thanh toán (thời gian và tài liệu hoặc giá cố định), số tiền ngân sách khách hàng và dự án cơ bản.

PSA cũng thêm một số các thực thể được thiết kế dành cho hợp đồng dự án. Dưới đây là một số ví dụ:

- **Chi tiết mô tả hợp đồng dự án** – Thực thể này chứa chi tiết cấp mô tả được tổng hợp thành số tiền mô tả hợp đồng. Những mục này có thể được nêu chi tiết ở dạng mục mô tả được tạo từ lịch trình dự án ở cấp nhiệm vụ.
- **Lịch trình hóa đơn mô tả hợp đồng** – Thực thể này chứa lịch trình thanh toán được tạo dựa trên tần suất hóa đơn được gán cho mô tả hợp đồng.
- **Mốc hợp đồng** – Thực thể này chứa mốc thanh toán cho mô tả hợp đồng có điều khoản thanh toán giá cố định.

Các thực thể khác mà PSA thêm vào hợp đồng là **Bảng giá dự án mô tả hợp đồng dự án**, **Loại nguồn lực mô tả hợp đồng dự án** và **Loại giao dịch mô tả hợp đồng dự án**.

![Sơ đồ hiển thị đơn hàng, mô tả đơn hàng và các mối quan hệ của dự án](media/PS-Reporting-image3.png "Sơ đồ hiển thị đơn hàng, mô tả đơn hàng và các mối quan hệ của dự án")

## <a name="reporting-on-projects"></a>Báo cáo về dự án

Thực thể **Dự án** và các thực thể liên quan dành riêng cho PSA. **Dự án** là thực thể cấp cao nhất dùng để ghi công việc và bên chi phí hoạt động. Dưới đây là danh sách các thực thể liên quan:

- **Thành viên nhóm dự án** – Thực thể này chứa thông tin chi tiết về nguồn lực có thể đăng ký được gán cho dự án. Các nguồn lực đó có thể là nguồn lực chung có thể đăng ký hoặc nguồn lực có tên có thể đăng ký được người quản lý dự án nhập hoặc được tạo từ lịch trình dự án.
- **Nhiệm vụ dự án** – Thực thể này chứa các nhiệm vụ tạo thành kế hoạch hoặc lịch trình dự án.
- **Phân công nguồn lực** – Thực thể này chứa phân công nhiệm vụ cho nguồn lực có thể đăng ký.
- **Yêu cầu nguồn lực** – Thực thể này chứa yêu cầu cho mọi thành viên nhóm nguồn lực chung.
- **Ước tính** và **Mô tả ước tính** – Các thực thể này có mối quan hệ tiêu đề/mô tả và chứa ước tính chi phí cho dự án. Ước tính nhiệm vụ được lưu trữ trên thực thể **Ước tính nguồn lực**.

![Sơ đồ hiển thị yêu cầu nguồn lực và các mối quan hệ của dự án](media/PS-Reporting-image4.png "Sơ đồ hiển thị yêu cầu nguồn lực và các mối quan hệ của dự án")

## <a name="reporting-on-resources"></a>Báo cáo về nguồn lực

Nguồn lực dự án dùng các thực thể **Nguồn lực có thể đăng ký** từ Universal Resource Scheduling (URS) được chia sẻ bằng các ứng dụng khác, chẳng hạn như Microsoft Dynamics 365 Field Service. Dưới đây là danh sách các thực thể mà bạn có thể phải dùng khi báo cáo về các nguồn lực dự án:

- **Nguồn lực có thể đăng ký** – Thực thể này đại diện cho người dùng, liên hệ, nguồn lực chung, tài khoản, nhóm hoặc thiết bị dùng trên nhóm dự án.
- **Đặc điểm nguồn lực có thể đăng ký** – Thực thể này bao gồm kỹ năng, chứng nhận hoặc thông tin giáo dục của nguồn lực. Các đặc điểm có thể có giá trị xếp hạng được xác định bởi mô hình xếp hạng.
- **Loại nguồn lực có thể đăng ký** – Thực thể này đại diện cho vai trò của nguồn lực có thể đăng ký.
- **Đăng ký nguồn lực có thể đăng ký** – Thực thể này đại diện cho thời gian đã đăng ký trên dự án cho nguồn lực. Mỗi đăng ký có thực thể mô tả và thực thể tiêu đề. Mỗi mô tả có trạng thái biểu thị trạng thái của đăng ký.

![Sơ đồ hiển thị các mối quan hệ đặc điểm nguồn lực có thể đặt trước](media/PS-Reporting-image5.png "Sơ đồ hiển thị các mối quan hệ đặc điểm nguồn lực có thể đặt trước")

## <a name="reporting-on-actual-transactions"></a>Báo cáo về giao dịch thực tế

Khi bạn phê duyệt phiếu chấm công hoặc chi phí, hoặc lập hóa đơn hợp đồng trong PSA, giao dịch doanh nghiệp được ghi lại trong thực thể **Thực tế**. Thực thể này có thể dùng làm cơ sở cho hầu hết các báo cáo liên quan đến tài chính trong PSA. Thực thể **Thực tế** ghi lại chi phí và giao dịch bán hàng cho sự kiện kinh doanh. Thực thể này cũng ghi lại nhiều thuộc tính liên quan.

Khi đang làm việc với thực thể **Thực tế**, bạn phải hiểu giao dịch hoặc các giao dịch được ghi trong thực thể và thời điểm giao dịch được ghi. Dưới đây là các luồng thông thường mà bạn có thể làm việc với các mục nhập thời gian (luồng cho thực thể chi phí là tương tự):

1. Khi mục nhập thời gian được lưu, không có bản ghi nào được tạo trong thực thể **Thực tế**.
2. Khi mục nhập thời gian được gửi, không có bản ghi nào được tạo trong thực thể **Thực tế**.
3. Khi mục nhập thời gian được phê duyệt , một bản ghi được tạo trong thực thể **Thực tế** và bản ghi thứ hai cũng có thể được tạo. Bản ghi đầu tiên lưu trữ chi phí của mục nhập thời gian. Bản ghi thứ hai lưu trữ số tiền bán hàng chưa được lập hóa đơn của mục nhập thời gian. Bản ghi thứ hai phụ thuộc vào dự án hoặc có một khách hàng, báo giá hoặc một mô tả hợp đồng được gán cho bản ghi đó.

    | Ngày phát hành tài liệu | Loại giao dịch | Lớp giao dịch | Khách hàng         | Hợp đồng   | Nguồn lực     | Vai trò nguồn lực | Loại thanh toán | Số lượng | Đơn giá | Tổng số |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Chi phí             | Time              | Alpine ski house | Alpine CRM | Chế Hà | Người quản lý dự án   | Có thể tính phí   | 8.0      | 50.00      | 400.00 |
    | 3/2/18        | Doanh thu chưa lập hóa đơn   | Time              | Alpine ski house | Alpine CRM | Chế Hà | Người quản lý dự án   | Có thể tính phí   | 8.0      | 100.00     | 800.00 |

    2 bản ghi này là riêng biệt nhưng vẫn có liên quan. Các bản ghi này không phải là ghi nợ cũng không phải tín dụng.

4. Nếu hợp đồng liên kết với dự án, khi mục nhập thời gian được lập hóa đơn, 2 bản ghi khác sẽ được tạo trong thực thể **Thực tế**. Trước tiên, một khoản âm cho bản ghi bán hàng chưa được lập hóa đơn được tạo ra. Bản ghi này chủ yếu đảo ngược việc bán hàng chưa lập hóa đơn. Thứ hai, một giao dịch cho bán hàng được lập hóa đơn được tạo ra. Một lần nữa, các bản ghi này riêng biệt nhưng vẫn có liên quan, không phải tín dụng cũng không phải ghi nợ.

    | Ngày phát hành tài liệu | Loại giao dịch | Lớp giao dịch | Khách hàng         | Hợp đồng   | Nguồn lực     | Vai trò nguồn lực | Loại thanh toán | Số lượng | Giá đơn vị | Tổng số   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Doanh số chưa được lập hóa đơn   | Time              | Alpine ski house | Alpine CRM | Chế Hà | Người quản lý dự án   | Có thể tính phí   | - 8,0    | 100.00     | - 800,00 |
    | 4/2/18        | Doanh số đã lập hóa đơn     | Time              | Alpine ski house | Alpine CRM | Chế Hà | Người quản lý dự án   | Có thể tính phí   | 8.0      | 100.00     | 800.00   |

Thực thể **Nguồn gốc giao dịch** ghi lại nguồn gốc của bản ghi **Thực tế** và các bản ghi thực thể **Kết nối giao dịch** ghi lại các bản ghi cho bản ghi **Thực tế**. Ngoài ra, bản ghi **Thực tế** chứa tham chiếu dự án, hợp đồng dự án (đơn hàng), nguồn lực có thể đăng ký và khách hàng.

![Sơ đồ thể hiện kết nối giao dịch, nguồn gốc và các mối quan hệ thực tế](media/PS-Reporting-image6.png "Sơ đồ thể hiện kết nối giao dịch, nguồn gốc và các mối quan hệ thực tế")
