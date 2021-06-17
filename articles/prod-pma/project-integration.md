---
title: Tích hợp Microsoft Project Client
description: Việc lập kế hoạch và duy trì lịch trình dự án có thể phức tạp, vì vậy người quản lý dự án cần sử dụng các công cụ giúp họ quản lý công việc này. Tích hợp với Microsoft Project Client cung cấp sự hỗ trợ để mở và quản lý cấu trúc phân tích công việc của dự án.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999472"
---
# <a name="microsoft-project-client-integration"></a>Tích hợp Microsoft Project Client

[!include [banner](../includes/banner.md)]

Việc lập kế hoạch và duy trì lịch trình dự án có thể phức tạp, vì vậy người quản lý dự án cần sử dụng các công cụ giúp họ quản lý công việc này. Tích hợp với Microsoft Project Client cung cấp sự hỗ trợ để mở và quản lý cấu trúc phân tích công việc của dự án. Người quản lý dự án có thể xuất bản bất kỳ thay đổi nào trở lại cấu trúc phân tích công việc dự án Dynamics 365 Finance.

> [!NOTE]
> Nếu bạn đang sử dụng bản cập nhật tháng 7 (phiên bản 10.0.4), bạn phải cài đặt KB 4054797 và 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Đặt cấu hình phần bổ trợ Microsoft Project Client
Để cho phép tích hợp với Microsoft Project Client, phần bổ trợ Microsoft Dynamics 365 bắt buộc phải được cài đặt trong ứng dụng Microsoft Project máy khách của người dùng. Điều này được thực hiện bằng cách mở **Không gian làm việc quản lý dự án**.

•   Nhấp vào **Đặt cấu hình phần bổ trợ máy khách dự án** từ phần **Liên kết** > **Thiết lập** của không gian làm việc.

•   Nhấp vào **Mở**, sau đó nhấp vào **Chạy** khi được nhắc.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Mở và chỉnh sửa cấu trúc phân tích công việc bản nháp hiện có trong Microsoft Project Client
Nếu một dự án trong Dynamics 365 Finance đã được tạo cấu trúc phân tích công việc, cấu trúc phân tích công việc đó có thể được mở trong ứng dụng Microsoft Project Client nếu cấu trúc phân tích công việc ở trạng thái bản nháp. Để mở từ trang **Dự án**, nhấp vào liên kết **Mở trong Microsoft Project** từ tab **Kế hoạch**. Trang này cũng có thể được mở từ trong ứng dụng Microsoft Project Client bằng cách nhấp vào **Mở** trong tab **Microsoft Dynamics 365**. Chọn **Pháp nhân** và **Dự án** từ danh sách.

> [!NOTE]
> Nếu bạn đang sử dụng Internet Explorer là trình duyệt của mình, bạn sẽ cần nhấp vào **Lưu** để mở thủ công từ vị trí tệp được tải xuống. Hoặc, nhấp vào **Lưu và mở** để mở tệp trong Microsoft Project Client. Không đổi tên tệp khi lưu.

Trước khi thực hiện bất kỳ chỉnh sửa nào đối với tệp bằng Microsoft Project Client, bạn cần kiểm tra nó. Nhấp vào **Kiểm tra** trong tab **Microsoft Dynamics 365**. Điều này sẽ ngăn những người dùng khác chỉnh sửa cấu trúc phân tích công việc từ bên trong Finance cùng một lúc. Để phát hành cấu trúc phân tích công việc sau khi hoàn thành bất kỳ chỉnh sửa nào, hãy nhấp vào **Kiểm nhập** trên tab **Microsoft Dynamics 365**.

Nếu một nhóm dự án đã được thêm vào dự án trong Finance, danh sách nguồn lực sẽ được điền với các thành viên trong nhóm. Nếu nhóm dự án chưa được thêm vào dự án, bạn có thể chọn nguồn lực và xây dựng nhóm trong Microsoft Project Client bằng cách nhấp vào nút **Nguồn lực** trên tab **Microsoft Dynamics 365**. 

Dữ liệu sau đây sẽ được đồng bộ hóa trở lại Finance như một phần của quy trình kiểm nhập:

•   Tên tác vụ

•   Ngày bắt đầu

•   Ngày hoàn thành

•   Người tiền nhiệm

•   Tên nguồn lực

•   Thể loại

•   Thể loại nguồn lực

•   Giờ làm việc

•   Ghi chú

•   Mức ưu tiên

> [!NOTE]
> Nếu bạn thêm bất kỳ cột nào khác vào tệp Microsoft Project Client của mình, chúng sẽ không được lưu vào tệp và sẽ không được hiển thị khi tệp được mở lại.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Tạo cấu trúc phân tích công việc cho một dự án hiện có bằng Microsoft Project Client
Để tạo cấu trúc phân tích công việc mới bằng Microsoft Project Client, hãy làm theo các bước sau:


1.  Mở Microsoft Project Client.

2.  Trên tab **Microsoft Dynamics 365**, nhấp vào **Mở**.

3.  Chọn **Pháp nhân** cho dự án.

4.  Chọn **Dự án**.

5.  Nhấp vào **Kiểm tra** trên tab **Microsoft Dynamics 365**.

6.  Khi sẵn sàng phát hành lên Finance, hãy nhấp vào **Đăng ký** trên tab **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Thay thế cấu trúc phân tích công việc hiện có cho một dự án hiện có bằng Microsoft Project Client
Để tạo cấu trúc phân tích công việc mới bằng Microsoft Project Client và thay thế cấu trúc phân tích công việc hiện có cho một dự án hiện có, hãy làm theo các bước sau:

1.  Mở Microsoft Project Client.

2.  Tạo lịch trình Microsoft Project Client.

3.  Trên tab **Microsoft Dynamics 365**, nhấp vào **Lưu thay đổi** > **Thay thế dự án hiện có**.

4.  Chọn **Pháp nhân** cho dự án.

5.  Chọn **Dự án**.

6.  Bấm **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Tạo một dự án mới từ trong Microsoft Project Client


1.  Mở Microsoft Project Client.

2.  Tạo lịch trình Microsoft Project Client.

3.  Trên tab **Microsoft Dynamics 365**, nhấp vào **Lưu thay đổi** > **Lưu vào Dự án mới**.

4.  Chọn **Pháp nhân** cho dự án.

5.  Nhập **ID dự án** nếu cần.

6.  Nhập **Tên dự án**.

7.  Chọn **Loại dự án**, **Nhóm dự án** và **ID hợp đồng dự án**. Ngoài ra, bạn có thể tạo hợp đồng dự án mới bằng cách nhấp vào **Mới**.

8.  Chọn **Lịch** để sử dụng cho việc cấp nguồn lực.

11. Bấm **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]