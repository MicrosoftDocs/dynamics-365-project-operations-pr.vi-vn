---
title: Làm thế nào để tôi "đăng ký dự kiến" các nguồn lực trong phiên bản ứng dụng 2.x?
description: Bài viết này mô tả cách "đăng ký dự kiến" các thành viên nhóm dự án bằng Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146509"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Làm thế nào để tôi "đăng ký dự kiến" nguồn lực trong ứng dụng web (ứng dụng Project Service phiên bản 2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Bạn có thể lên lịch trình dự kiến hoặc "đăng ký dự kiến" nguồn lực trên nhóm dự án để hiện nguồn lực bạn lên kế hoạch gán cho một dự án. Đăng ký dự kiến không sử dụng năng lực sẵn có của nguồn lực. Các thành viên nhóm được đăng ký dự kiến không thể được gán vào nhiệm vụ dự án. Chỉ có nguồn lực với tình trạng Đăng ký Xác nhận và Loại Cam kết Đã cam kết mới có thể được gán cho nhiệm vụ (giả sử các nguồn lực có đủ số giờ đăng ký xác nhận để thực hiện mức nỗ lực thực hiện nhiệm vụ).

Thành viên nhóm dự án được đăng ký dự kiến hiển thị trong lưới Thành viên Nhóm số giờ đăng ký dự kiến hiển thị trong cột Đăng ký Dự kiến. Các thành viên này cũng có mặt trên bảng lịch trình. Một lần nữa, các thành viên nhóm không cho thấy bất kỳ mức sử dụng năng lực nào vì đăng ký dự kiến không sử dụng năng lực sẵn có của nguồn lực.

Có ba cách để đăng ký dự kiến một thành viên nhóm vào một dự án với Project Service phiên bản 2.x. Bạn có thể đăng ký dự kiến với bảng lịch trình, sử dụng tính năng Duy trì Đăng ký hoặc bằng cách tạo ra một nguồn lực chung. Những phương pháp này được mô tả dưới đây.

## <a name="soft-book-with-the-schedule-board"></a>Đăng ký dự kiến với bảng lịch trình

Để đăng ký dự kiến với bảng lịch trình, hãy làm theo thủ tục này: 
1. Mở bảng lịch trình.
2. Chọn tab Dự án nằm ở cuối bảng điều khiển Yêu cầu Đăng ký của bảng lịch trình.
3. Tìm dự án bạn muốn đăng ký dự kiến nguồn lực vào. Nếu bạn có nhiều dự án, hãy nhấp vào tiêu đề của cột Dự án và sau đó sử dụng các bộ lọc để tìm kiếm dự án của bạn.
4. Nhấp vào dự án, sau đó kéo và thả nó trên lưới thời gian của nguồn lực.
5. Thao tác này sẽ mở bảng điều khiển Tạo Đăng ký Nguồn lực ở bên phải. Điều chỉnh ngày bắt đầu và kết thúc, chọn Trạng thái Đăng ký là Dự kiến và đặt giờ. 
6. Bấm Đăng ký.
7. Quay lại dự án, nguồn lực sẽ hiển thị như là một thành viên nhóm với số giờ đăng ký dự kiến trong cột Đăng ký Dự kiến.

Lưu ý rằng bạn không thể gán các nguồn lực vào các tác vụ trên cấu trúc phân tích công việc (WBS) vì nguồn lực phải được đăng ký xác nhận trong nhóm để được gán.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Đăng ký dự kiến bằng cách sử dụng tính năng Duy trì Đăng ký

Để đăng ký dự kiến với tính năng Duy trì Đăng ký, hãy làm theo thủ tục này:
1. Từ lưới thành viên nhóm, nhấp vào Mới.
2. Chọn ngày bắt đầu/kết thúc, vai trò, nguồn lực có thể đăng ký được.
3. Chọn một phương pháp phân bổ khác Không có:
- Năng lực đầy đủ
- Năng lực tỉ lệ phần trăm
- Theo Giờ Phân phối Đồng đều
- Theo Giờ Phân phối lượng công việc nặng lúc ban đầu
4. Bấm vào Lưu. Bạn sẽ thấy nguồn lực trên lưới nhóm và số giờ của chúng cho thấy là Xác nhận.
5. Duy trì trạng thái đăng ký của nguồn lực bằng cách nhấp vào Duy trì Đăng ký.
6. Khi bảng lịch trình mở ra, hãy mở rộng nguồn lực để hiện các đăng ký. Bạn sẽ thấy đăng ký cho thấy là Xác nhận.
7. Nhấp chuột phải đăng ký, dưới Thay đổi Trạng thái, chọn Đăng ký Dự kiến và sau đó là Dự kiến. Trạng thái đăng ký bây giờ là Dự kiến.
8. Sau khi đóng bảng lịch trình, bạn sẽ thấy số giờ dành cho nguồn lực đã thay đổi từ Xác nhận thành Dự kiến trên lưới thành viên nhóm.
Lưu ý rằng nếu bạn đăng ký xác nhận nguồn lực trên nhóm và sau đó gán chúng nhiệm vụ trên cấu trúc phân tích công việc, khi bạn sử dụng duy trì đăng ký để đổi trạng thái từ Xác nhận sang Dự kiến, thao tác này sẽ loại bỏ nhiệm vụ cho nguồn lực vì chỉ có nguồn lực được đăng ký xác nhận mới có thể được gán cho nhiệm vụ.

## <a name="soft-book-by-creating-a-generic-resource"></a>Đăng ký dự kiến bằng cách tạo ra một nguồn lực chung

Bạn có thể đăng ký dự kiến bằng cách tạo ra một thành viên nhóm nguồn lực chung, hoàn thành với bảng lịch trình hoặc Đề nghị Nguồn lực và thay đổi loại trong quá trình đăng ký.
Để thực hiện điều này, hãy làm theo thủ tục sau:

1. Trên WBS của dự án, hãy gán vai trò cho các nhiệm vụ bạn muốn tạo các thành viên nhóm chung cho.
2. Nhấp vào Tạo Thành viên Dự án/
3. Trên lưới thành viên nhóm của dự án. chọn nguồn lực chung và nhấp vào Đăng ký.
4. Trên bảng lịch trình, chọn nguồn lực bạn muốn đăng ký.
5. Trên bảng điều khiển Tạo Đăng ký Nguồn lực của bảng lịch trình, thay đổi Trạng thái Đăng ký từ Xác nhận sang Dự kiến.
6. Nhấp vào Đăng ký hay Đăng ký và Thoát.

Sau khi đóng bảng lịch trình, bạn sẽ thấy nguồn lực được chọn được thêm vào nhóm số giờ Đăng ký dự kiến cũng như số giờ được gán. Bạn cũng sẽ thấy nguồn lực chung vẫn còn trong nhóm như là một chỉ báo cho thấy các nhiệm vụ được gán cho một thành viên nhóm được đăng ký dự kiến.

Khi bạn sẵn sàng đổi nguồn lực thành viên nhóm được đăng ký dự kiến sang thành viên nhóm được đăng ký xác nhận để gán vào nhiệm vụ, thực hiện như sau:

1. Chọn nguồn lực đó và nhấp vào Duy trì Đăng ký.
2. Khi bảng lịch trình mở ra, hãy mở rộng nguồn lực để hiện các đăng ký. Bạn sẽ thấy đăng ký được đánh dấu là Dự kiến.
3. Nhấp chuột phải vào đăng ký, dưới Thay đổi Trạng thái, chọn Đăng ký Xác nhận và sau đó là Xác nhận. Trạng thái đăng ký bây giờ là Xác nhận.
4. Sau khi đóng bảng lịch trình, bạn sẽ thấy số giờ dành cho nguồn lực đã thay đổi từ Dự kiến thành Xác nhận trên lưới thành viên nhóm. Bây giờ bạn có thể gán tài nguyên cho nhiệm vụ (miễn là có sự liên kết giữa số giờ đăng ký xác nhận và số giờ nỗ lực của nhiệm vụ). Lưu ý rằng nếu bạn làm theo các bước hoàn thành nguồn lực chung trong mục #3 ở trên, khi bạn thay đổi trạng thái của nguồn lực được đăng ký dự kiến sang xác nhận, thành viên nhóm chung sẽ bị loại khỏi nhóm.


[!INCLUDE[footer-include](../includes/footer-banner.md)]