---
title: Cách phân công một nhiệm vụ cho nguồn lực có thể đặt lịch trong ứng dụng web
description: Tổng quan về các cách bạn có thể phân công nguồn lực có thể đặt lịch.
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
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146599"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Làm thế nào để tôi gán nguồn lực có thể đăng ký được cho một nhiệm vụ trong ứng dụng web (ứng dụng Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Có hai cách để gán nguồn lực cho một nhiệm vụ trong Project Service. Bạn có thể đăng ký nguồn lực là thành viên nhóm và gán nguồn lực đó cho nhiệm vụ. Hoặc bạn có thể tạo thành viên nhóm chung nhờ việc phân công vai trò theo nhiệm vụ, tạo một nhóm và hoàn thành các yêu cầu hỗ trợ bằng nguồn lực được đặt tên.

Lưu ý rằng nếu bạn muốn gán một nguồn lực có thể đăng ký được cho nhiệm vụ, thành viên nhóm là nguồn lực có thể đăng ký được phải có đủ các đăng ký sẵn có. Tình trạng của đăng ký phải là Commit Type Hard Book (Đăng ký chắc chắn loại cam kết) và Status Committed (Trạng thái đã được cam kết). Nếu không có đủ số đăng ký cho nguồn lực, Project Service sẽ loại bỏ sự phân công và hiển thị thông báo lỗi như sau:

*Không thể gán nguồn lực cho nhiệm vụ - (Các) Nguồn lực sau không có đủ số giờ được đăng ký cho dự án*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Đăng ký một nguồn lực là một thành viên nhóm và sau đó gán nguồn lực cho nhiệm vụ

Với phương pháp này bạn có thể thêm nguồn lực cho nhóm dự án và sau đó gán nhiệm vụ cho nguồn lực trong lịch trình dự án. Đây là cách làm việc này:
1.  Trên lưới thành viên nhóm, thêm một thành viên nhóm bằng cách chọn **Mới**.
2.  Trên màn hình Team Member Quick Create (Tạo nhanh thành viên nhóm), chọn tên nguồn lực có thể đăng ký được và đặt vai trò.
3.  Chọn các ngày **Bắt đầu** và ngày **Kết thúc**.

    > [!div class="mx-imgBorder"] 
    > ![Ảnh chụp màn hình thêm thành viên nhóm](media/FAQ-Resources-to-Tasks2-1.png "Ảnh chụp màn hình thêm thành viên nhóm")
 
4.  Chọn một trong các phương pháp phân bổ sau để đăng ký nguồn lực:
    - **Năng lực đầy đủ** đăng ký năng lực đầy đủ của nguồn lực theo các ngày bắt đầu và kết thúc đã được chỉ định.
    - **Năng lực tỉ lệ phần trăm** đăng ký nguồn lực theo tỉ lệ phần trăm năng lực của nguồn lực theo những ngày bắt đầu và kết thúc.
    - **Phân phối theo giờ đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối thời gian mỗi ngày đều nhau cho các ngày đã được chỉ định kể từ khi bắt đầu cho tới khi kết thúc.
    - **Phân phối không đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối không đồng đều thời gian cho mỗi ngày trong các ngày được chỉ định từ khi bắt đầu cho tới khi kết thúc.

    Không nên chọn **Không có** vì tính năng này thêm nguồn lực vào nhóm nhưng không tạo bất kỳ đăng ký nào mà sử dụng năng lực của nguồn lực.
5.  Chọn **Lưu.**

    Lưu ý rằng số giờ của đăng ký phải đủ cho cả số giờ nỗ lực và quãng ngày của nhiệm vụ mà bạn gán nguồn lực này cho. Nếu chúng không được căn chỉnh, bạn không thể gán nguồn lực cho nhiệm vụ.

6.  Trên Cấu trúc phân tích công việc (WBS) cho nhiệm vụ, bấm vào danh sách thả xuống của ô nguồn lực. Vậy thì: 

    1. Chọn **Thêm**.
    2. Chọn danh sách thả xuống ở dưới **Nguồn lực** và chọn thành viên nhóm bạn đã thêm vào ở trên.
    3. Chọn **OK**. Thành viên nhóm hiện được gán cho nhiệm vụ.

    > [!div class="mx-imgBorder"] 
    > ![Ảnh chụp màn hình thêm tài nguyên với WBS](media/FAQ-Resources-to-Tasks2-2.png "Ảnh chụp màn hình thêm tài nguyên với WBS")
 
Trên lưới điện thành viên nhóm, bạn sẽ thấy sự tổng hợp của số giờ đã được gán của nguồn lực dưới phần Số giờ được gán. Số giờ đó sẽ ít hơn hoặc bằng với số giờ đã được đăng ký cho nguồn lực. 

> [!div class="mx-imgBorder"] 
> ![Ảnh chụp màn hình số giờ được chỉ định cho một tài nguyên](media/FAQ-Resources-to-Tasks2-3.png "Ảnh chụp màn hình số giờ được chỉ định cho một tài nguyên")
 
Nếu nhiệm vụ mà bạn đang cố gán cho nguồn lực bắt đầu sau ngày kết thúc của đăng ký nguồn lực, nguồn lực sẽ không hiện lên trong danh sách thả xuống.

Lưu ý rằng bạn có thể gán nguồn lực cho số giờ nhiều hơn số giờ đã được đăng ký của nguồn lực nếu nguồn lực còn một số năng lực còn lại mà chưa được gán. Trong trường hợp này, nguồn lực sẽ chỉ được gán từng phần cho đăng ký của nguồn lực. Bạn có thể xem số giờ nhiệm vụ chưa được gán bằng cách thêm cột Số giờ trống vào cấu trúc phân tích công việc.

Nếu nguồn lực được gán cho số giờ được đăng ký cho nguồn lực (số giờ được đăng ký cho nguồn lực bằng số giờ được gán cho nguồn lực), bạn sẽ thấy thông báo lỗi như sau khi bạn cố gán nguồn lực cho các nhiệm vụ sau:

*Không thể gán nguồn lực cho nhiệm vụ - (Các) Nguồn lực sau không có đủ số giờ được đăng ký cho dự án.*

Ngoài ra, thành viên nhóm của người quản lý dự án mặc định mà được thêm vào nhóm khi bạn tạo dự án được thêm mà không có bất kỳ đăng ký nào và không thể được đăng ký cho bất kỳ dự án nào. Chúng sẽ không được hiển thị trong danh sách nguồn lực thả xuống cho các nhiệm vụ.

Nếu bạn muốn gán nguồn lực này, bạn cần loại bỏ chúng khỏi nhóm và sau đó thêm chúng lại bằng phương pháp phân bổ chứ không để là Không có. Lý do chúng được thêm vào nhóm khi dự án được tạo là để dự án có tối thiểu một người phê chuẩn dự án theo mặc định.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Tạo một thành viên chung bằng cách phân công vai trò cho nhiệm vụ

Phương pháp này đảm bảo nguồn lực có đủ đăng ký cho nhiệm vụ. Đầu tiên, bạn tạo một nguồn lực chung hoặc nguồn lực giữ chỗ mà mô tả các đặc điểm của nguồn lực được đặt tên, cuối cùng bạn muốn làm việc với nhiệm vụ bằng cách tạo nhóm sau khi gán vai trò cho nhiệm vụ. Đây là cách làm việc này:

1. Trên cấu trúc phân tích công việc, chọn nhiệm vụ.
2. Chọn biểu tượng danh sách thả xuống **Vai trò được gán** trong ô nguồn lực.
3. Chọn danh sách thả xuống **Vai trò** và chọn vai trò cho nguồn lực chung.
4. Chọn **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Ảnh chụp màn hình dùng WBS để thêm tài nguyên](media/FAQ-Resources-to-Tasks2-4.png "Ảnh chụp màn hình dùng WBS để thêm tài nguyên")
 
Khi bạn hoàn thành việc gán vai trò cho nhiệm vụ trong WBS, chọn **Tạo nhóm dự án**. Project Service tạo số thành viên nhóm chung tối thiểu dựa trên vai trò, tạo nguồn lực đơn vị tổ chức, và lịch dự án bằng cách tập hợp các phân công nhiệm vụ.

> [!div class="mx-imgBorder"] 
> ![Ảnh chụp màn hình tạo nhóm dự án](media/FAQ-Resources-to-Tasks2-5.png "Ảnh chụp màn hình tạo nhóm dự án")
 
Trên lưới Thành viên nhóm, bạn sẽ thấy các nguồn lực của loại Nguồn lực chung với tên vị trí và vai trò. Nếu hai nguồn lực cần cho vai trò để hoàn thành công việc, tính năng Tạo nhóm sẽ tạo hai thành viên nhóm và dùng tên vị trí để phân biệt.

> [!div class="mx-imgBorder"] 
> ![Ảnh chụp màn hình thêm hai tài nguyên chung](media/FAQ-Resources-to-Tasks2-6.png "Ảnh chụp màn hình thêm hai tài nguyên chung")
 
Bạn có thể mở yêu cầu nguồn lực hỗ trợ cho thành viên nhóm chung bằng cách chon liên kết ở dưới Yêu cầu Nguồn lực.

> [!div class="mx-imgBorder"] 
> ![Ảnh chụp màn hình mở yêu cầu nguồn lực hỗ trợ](media/FAQ-Resources-to-Tasks2-7.png "Ảnh chụp màn hình mở yêu cầu nguồn lực hỗ trợ")

Chọn **Đăng ký** đối với nguồn lực chung và sau đó bạn có thể dùng bảng lịch trình để tìm và đăng ký nguồn lực thực. Bạn cũng có thể gửi yêu cầu hoàn thành bởi người quản lý nguồn lực bằng cách chọn **Gửi yêu cầu**.

Khi nguồn lực chung được hoàn thành bằng nguồn lực được đặt tên, nguồn lực chung sẽ được loại bỏ khỏi nhóm và các phân công nhiệm vụ cho nguồn lực chung được gán cho nguồn lực được đặt tên mà hoàn thành yêu cầu nguồn lực của nguồn lực.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]