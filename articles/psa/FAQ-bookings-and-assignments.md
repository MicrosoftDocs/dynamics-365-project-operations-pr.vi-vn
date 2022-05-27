---
title: Đặt lịch nguồn lực và các họ liên kết với phân công nhiệm vụ
description: Chủ đề này cung cấp thông tin về cách quản lý nguồn lực được đặt tên, đặt lịch nguồn lực và phân công nhiệm vụ cũng như cách chúng liên quan đến nhau.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575514"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Đặt lịch nguồn lực và các họ liên kết với phân công nhiệm vụ

[!include [banner](../includes/psa-now-project-operations.md)]

Có hai cách đặt lịch một nguồn lực có tên cho một nhóm dự án và phân công nhiệm vụ dự án:

- Nguồn lực có thể được đăng ký trực tiếp trên dự án và sau đó được phân công cho nhiệm vụ dự án.
- Các nhiệm vụ có thể được phân công cho một nguồn lực chung, nguồn lực này sau đó được dùng để tìm kiếm và thay thế phần chung bằng nguồn lực thực, được đặt tên. 

Trong cả hai trường hợp, hành động đăng ký nguồn lực bảo lưu năng lực của nguồn lực.

Người quản lý dự án hoạch định dự án sở hữu lịch trình và kế hoạch dự án. Bằng cách sử dụng nguồn lực chung cho việc phân công và sau đó tạo một yêu cầu nguồn lực từ việc phân công đó. Người quản lý dự án có thể đăng ký các nguồn lực trên dự án bằng các phân phối giờ làm việc được chỉ định trong kế hoạch dự án. Họ có thể đăng ký các nguồn lực trên dự án và sau đó phân công nguồn lực cho nhiệm vụ, tuy nhiên không có cách nào để căn chỉnh phân phối giờ làm việc được đăng ký với phân phối giờ làm việc của nhiệm vụ. Đặt lịch không ảnh hưởng đến lịch trình dự án.

Nên xem xét một dự án phức tạp có nhiều nhiệm vụ chồng chéo nhau với nhiều nguồn lực cùng loại cần làm việc đồng thời. Nếu một nguồn lực được cho một phân phối giờ làm việc mà khác với phân phối giờ làm việc của tổng toàn bộ các phân công, sẽ khó để sửa đổi các nhiệm vụ để phù hợp với phân phối giờ làm việc của đăng ký cho các nhiệm vụ riêng biệt và phân phối giờ làm việc ban đầu.

Trong ví dụ dưới đây, tổng nỗ lực yêu cầu bởi cùng nguồn lực từ một tập hợp của bốn nhiệm vụ là 62 giờ, hơn khoảng thời gian hai tuần và có một phân phối giờ làm việc đặc biệt. Nếu nguồn lực là Bob được đăng ký cho 62 giờ trong cùng hai tuần nhưng có phân phối giờ làm việc khác thì yêu cầu và các đăng ký sẽ được căn chỉnh.

| **Phân phối giờ làm việc theo nhiệm vụ**    | **Tổng số giờ** | Thứ hai, ngày 4 tháng 6 | Thứ ba, ngày 5 tháng 6 | Thứ tư, ngày 6 tháng 6 | Thứ năm, ngày 7 tháng 6 | Thứ sáu, ngày 8 tháng 6 | Thứ bảy, ngày 9 tháng 6 | Chủ nhật, ngày 10 tháng 6 | Thứ hai, ngày 11 tháng 6 | Thứ ba, ngày 12 tháng 6 | Thứ tư, ngày 13 tháng 6 | Thứ năm, ngày 14 tháng 6 | Thứ sáu, ngày 15 tháng 6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Nhiệm vụ 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Nhiệm vụ 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Nhiệm vụ 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Nhiệm vụ 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Tổng số**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Trạng thái sẵn sàng của Bob
| **Đăng ký   nguồn lực** | **Tổng số giờ** | Thứ hai, ngày 4 tháng 6 | Thứ ba, ngày 5 tháng 6 | Thứ tư, ngày 6 tháng 6 | Thứ năm, ngày 7 tháng 6 | Thứ sáu, ngày 8 tháng 6 | Thứ bảy, ngày 9 tháng 6 | Chủ nhật, ngày 10 tháng 6 | Thứ hai, ngày 11 tháng 6 | Thứ ba, ngày 12 tháng 6 | Thứ tư, ngày 13 tháng 6 | Thứ năm, ngày 14 tháng 6 | Thứ sáu, ngày 15 tháng 6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Tuy nhiên, không có cách nào theo hệ thống để gán phân phối giờ làm việc cho nhiều giờ đã đăng ký cho nhiệm vụ theo từng ngày. Nếu người quản lý dự án muốn đổi lịch trình dự án để đáp ứng trạng thái sẵn sàng của nguồn lực, sau đó họ sẽ phải loại bỏ sự phân công và đánh giá tất cả các nhiệm vụ để khớp với phân phối giờ làm việc được đăng ký.

Trong trường hợp tổ chức trao nhiệm vụ hoạch định dự án cho cả người quản lý dự án và người quản lý nguồn lực, người quản lý dự án sẽ lên lịch trình và lịch trình bao gồm cả việc phân phối giờ làm việc của công việc yêu cầu. Người quản lý nguồn lực không nên có khả năng tác động tới lịch trình mà không có kiến thức của người quản lý dự án bằng cách thay đổi phân phối giờ làm việc khi đăng ký nguồn lực thực. Nếu người quản lý nguồn lực thực hiện nhiệm vụ nào khác so với người quản lý dự án yêu cầu, họ cần thống nhất thỏa thuận với nhau về những thay đổi cần có trong lịch trình dự án.

Do việc đăng ký và phân công không liên kết quá chặt chẽ nên có thể đăng ký phân phối giờ làm việc mà khác với phân phối giờ làm việc của nhiệm vụ hoặc đổi sự phân công theo kết quả tùy trong những trường hợp việc đăng ký và phân công không được căn chỉnh.

**Dạng xem Hợp nhất** cho phép người quản lý dự án án xem các đăng ký và phân công cho từng thành viên nhóm dự án. Dạng xem sử dụng các màu sắc và màu bóng để thể hiện sự không khớp giữa các sự phân công và đăng ký của các thành viên nhóm. Dựa trên thông tin này, người quản lý dự án có thể thực hiện các hoạt động sửa chữa cho cả các đăng ký nguồn lực mở rộng cho những trường hợp có sự phân công và không đăng ký, hoặc hủy đăng ký với các nguồn lực đã được đăng ký nhưng không có sự phân công.

> [!NOTE]
> Nếu bạn di chuyển nhiệm vụ mà bạn đã phân phối giờ làm việc cho chính mình, những sự phân phối giờ làm việc đó sẽ không được duy trì. Phân phối giờ làm việc được tạo cho khách hàng theo lịch dự án cho các thay đổi về giờ làm việc và ngày nghỉ lễ. Điều này là do thiết kế vì hệ thống không hiểu được mục đích của phân phối giờ làm việc gốc và không thể xác định được việc duy trì phân phối giờ làm việc đó có ý nghĩa với khung thời gian mới hay không. Vì việc đăng ký và phân công đã bị mất kết nối, việc đăng ký duy trì theo các phân phối giờ làm việc mà ban đầu đăng ký. Trong trường hợp này, bạn sẽ cần hủy và đăng ký lại cho phân phối giờ làm việc được phân công mới.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
