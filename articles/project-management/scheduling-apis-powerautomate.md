---
title: Sử dụng các API lịch trình dự án bằng Power Automate
description: Bài viết này cung cấp quy trình mẫu sử dụng các giao diện lập trình ứng dụng (API) theo lịch trình Dự án.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404468"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Sử dụng các API lịch trình dự án bằng Power Automate

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này mô tả quy trình mẫu cho biết cách tạo một kế hoạch dự án hoàn chỉnh bằng cách sử dụng Microsoft Power Automate, cách tạo Bộ thao tác và cách cập nhật một thực thể. Ví dụ minh họa cách tạo dự án, thành viên nhóm dự án, Bộ thao tác, nhiệm vụ dự án và phân công nguồn lực. Bài viết này cũng giải thích cách cập nhật một thực thể và thực hiện một Bộ thao tác.

Sau đây là danh sách đầy đủ các bước được ghi lại trong quy trình mẫu trong bài viết này:

1. [Tạo trình kích hoạt PowerApps](#1)
2. [Tạo dự án](#2)
3. [Khởi tạo một biến cho thành viên nhóm](#3)
4. [Tạo thành viên nhóm chung](#4)
5. [Tạo Bộ thao tác](#5)
6. [Tạo bộ chứa dự án](#6)
7. [Khởi tạo một biến cho trạng thái liên kết](#7)
8. [Khởi tạo một biến cho số nhiệm vụ](#8)
9. [Khởi tạo một biến cho ID nhiệm vụ dự án](#9)
10. [Làm cho đến khi](#10)
11. [Đặt nhiệm vụ dự án](#11)
12. [Tạo nhiệm vụ dự án](#12)
13. [Tạo phân công nguồn lực](#13)
14. [Giảm dần một biến](#14)
15. [Đổi tên nhiệm vụ dự án](#15)
16. [Chạy Bộ thao tác](#16)

## <a name="assumptions"></a>Giả định

Bài viết này giả định rằng bạn có kiến thức cơ bản về nền tảng Dataverse, dòng đám mây và Giao diện lập trình ứng dụng (API) theo lịch trình Dự án. Để biết thêm thông tin, hãy xem phần [Tham chiếu](#references) ở phần sau trong bài viết này.

## <a name="create-a-flow"></a>Tạo một dòng

### <a name="select-an-environment"></a>Chọn một môi trường

Bạn không thể dòng Power Automate trong môi trường của mình.

1. Chuyển đến <https://flow.microsoft.com> và sử dụng thông tin xác thực của quản trị viên để đăng nhập.
2. Ở góc trên cùng bên phải, chọn **Môi trường**.
3. Trong danh sách, hãy chọn môi trường nơi Dynamics 365 Project Operations được cài đặt.

### <a name="create-a-solution"></a>Tạo một giải pháp

Làm theo các bước này để tạo [dòng nhận biết giải pháp](/power-automate/overview-solution-flows). Bằng cách tạo dòng nhận biết giải pháp, bạn có thể dễ dàng xuất dòng để sử dụng sau này.

1. Ở ngăn điều hướng, hãy chọn **Giải pháp**.
2. Trên trang **Giải pháp**, chọn **Giải pháp mới**.
3. Trong hộp thoại **Giải pháp mới**, đặt các trường bắt buộc rồi chọn **Tạo**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Bước 1: Tạo trình kích hoạt PowerApps

1. Trên trang **Giải pháp**, chọn giải pháp mà bạn tạo rồi chọn **Mới**.
2. Trong ngăn bên trái, chọn **Dòng đám mây** \> **Tự động hóa** \> **Dòng đám mây** \> **Tức thì**.
3. Trong trường **Tên dòng**, nhập **Lập lịch dòng demo API**.
4. Trong danh sách **Chọn cách kích hoạt dòng này**, chọn **Power Apps**. Khi bạn tạo một trình kích hoạt Power Apps, logic là tùy thuộc vào bạn với tư cách là tác giả. Trong bài viết này, hãy để trống các tham số đầu vào cho mục đích thử nghiệm.
5. Chọn **Tạo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Bước 2: Tạo dự án

Làm theo các bước sau để tạo dự án mẫu.

1. Trong dòng mà bạn tạo, chọn **Bước mới**.

    ![Thêm một bước mới.](media/newstep.png)

2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.

    ![Chọn một thao tác.](media/chooseactiontab.png)

3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.

![Đổi tên bước.](media/renamestep.png)

4. Đổi tên bước **Tạo dự án**.
5. Trong trường **Tên hành động**, chọn **msdyn\_CreateProjectV1**.
6. Trong trường **msdyn\_subject**, chọn **Thêm nội dung động**.
7. Trên tab **Biểu thức**, trong trường chức năng, nhập **Tên dự án - utcNow()**.
8. Chọn **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Bước 3: Khởi tạo một biến cho thành viên nhóm

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **khởi tạo biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Thành viên nhóm Init**.
5. Trong trường **Tên**, nhập **TeamMemberAction**.
6. Trong trường **Loại**, chọn **Chuỗi**.
7. Trong trường **Giá trị**, nhập **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Bước 4: Tạo thành viên nhóm chung

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo thành viên nhóm**.
5. Đối với trường **Tên hành động**, chọn **TeamMemberAction** trong hộp thoại **Nội dung động**.
6. Trong trường **Tham số hành động**, nhập thông tin tham số sau đây.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Dưới đây là giải thích về các tham số:

    - **\@\@odata.type** – Tên thực thể. Ví dụ: nhập **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Khóa chính của ID nhóm dự án. Giá trị là một biểu thức định danh duy nhất toàn cầu (GUID).   ID được tạo từ tab biểu thức.

    - **msdyn\_project\@odata.bind** – ID dự án của dự án sở hữu. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo dự án". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/msdyn\_projects(THÊM NỘI DUNG ĐỘNG)"**.
    - **msdyn\_name** – Tên của thành viên nhóm. Ví dụ: nhập **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Bước 5: Tạo Bộ thao tác

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo Bộ thao tác**.
5. Trong trường **Tên hành động**, chọn hành động tùy chỉnh Dataverse **msdyn\_CreateOperationSetV1**.
6. Trong trường **Mô tả**, nhập **ScheduleAPIDemoOperationSet**.
7. Trong trường **Dự án**, nhập **/msdyn\_projects(**.
8. Trong hộp thoại **Nội dung động**, chọn **msdyn\_CreateProjectV1Response ProjectId**.
9. Trong trường **Dự án**, nhập **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Bước 6: Tạo bộ chứa dự án

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thêm hàng mới**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo bộ chứa**.
5. Trong trường **Tên bảng**, chọn **Bộ chứa dự án**.
6. Trong trường **Tên**, nhập **ScheduleAPIDemoBucket1**.
7. Đối với trường **Dự án**, chọn **msdyn\_CreateProjectV1Response ProjectId** trong hộp thoại **Nội dung động**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Bước 7: Khởi tạo một biến cho trạng thái liên kết

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **khởi tạo biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Init linkstatus**.
5. Trong trường **Tên**, nhập **linkstatus**.
6. Trong trường **Loại**, chọn **Số nguyên**.
7. Trong trường **Giá trị**, hãy nhập **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Bước 8: Khởi tạo một biến cho số nhiệm vụ

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **khởi tạo biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Khởi tạo số nhiệm vụ**.
5. Trong trường **Tên**, nhập **số nhiệm vụ**.
6. Trong trường **Loại**, chọn **Số nguyên**.
7. Trong trường **Giá trị**, hãy nhập **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Bước 9: Khởi tạo một biến cho ID nhiệm vụ dự án

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **khởi tạo biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Init ProjectTaskID**.
5. Trong trường **Tên**, nhập **số nhiệm vụ**.
6. Trong trường **Loại**, chọn **Chuỗi**.
7. Trong trường **Giá trị**, nhập **guid()** trong trình tạo biểu thức.

## <a name="step-10-do-until"></a><a id="10"></a>Bước 10: Làm cho đến khi

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **do until**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Đặt giá trị đầu tiên trong câu lệnh điều kiện thành biến **số nhiệm vụ** từ hộp thoại **Nội dung động**.
4. Đặt điều kiện thành **nhỏ hơn bằng**.
5. Đặt giá trị thứ hai trong câu lệnh điều kiện thành **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Bước 11: Đặt nhiệm vụ dự án

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **đặt biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Đặt nhiệm vụ dự án**.
5. Trong trường **Tên**, chọn **msdyn\_projecttaskid**.
6. Trong trường **Giá trị**, nhập **guid()** trong trình tạo biểu thức.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Bước 12: Tạo nhiệm vụ dự án

Làm theo các bước sau để tạo nhiệm vụ dự án có ID duy nhất thuộc về dự án hiện tại và bộ chứa dự án bạn đã tạo.

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo nhiệm vụ dự án**.
5. Trong trường **Tên hành động**, chọn **msdyn\_PssCreateV1**.
6. Trong trường **Thực thể**, hãy nhập thông tin tham số sau đây.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Dưới đây là giải thích về các tham số:

    - **\@\@odata.type** – Tên thực thể. Ví dụ: nhập **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID duy nhất của nhiệm vụ. Giá trị phải được đặt thành một biến động từ **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID dự án của dự án sở hữu. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo dự án". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/msdyn\_projects(THÊM NỘI DUNG ĐỘNG)"**.
    - **msdyn\_subject** – Tên nhiệm vụ bất kỳ.
    - **msdyn\_projectbucket\@odata.bind** – Bộ chứa dự án chứa các nhiệm vụ. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo bộ chứa". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/msdyn\_projectbuckets(THÊM NỘI DUNG ĐỘNG)"**.
    - **msdyn\_start** – Nội dung động cho ngày bắt đầu. Ví dụ: ngày mai sẽ được biểu thị là **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Ngày bắt đầu theo lịch. Ví dụ: ngày mai sẽ được biểu thị là **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Ngày kết thúc theo lịch. Chọn một ngày trong tương lai. Ví dụ: chỉ định **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Trạng thái liên kết. Ví dụ: nhập **"192350000"**.

7. Đối với trường **OperationSetId**, chọn **msdyn\_CreateOperationSetV1Response** trong hộp thoại **Nội dung động**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Bước 13: Tạo một phân công nguồn lực

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo phân công**.
5. Trong trường **Tên hành động**, chọn **msdyn\_PssCreateV1**.
6. Trong trường **Thực thể**, hãy nhập thông tin tham số sau đây.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Đối với trường **OperationSetId**, chọn **msdyn\_CreateOperationSetV1Response** trong hộp thoại **Nội dung động**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Bước 14: Giảm dần một biến

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **giảm dần biến**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong trường **Tên**, chọn **số nhiệm vụ**.
4. Trong trường **Giá trị**, hãy nhập **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Bước 15: Đổi tên nhiệm vụ dự án

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Đổi tên nhiệm vụ dự án**.
5. Trong trường **Tên hành động**, chọn **msdyn\_PssUpdateV1**.
6. Trong trường **Thực thể**, hãy nhập thông tin tham số sau đây.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Đối với trường **OperationSetId**, chọn **msdyn\_CreateOperationSetV1Response** trong hộp thoại **Nội dung động**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Bước 16: Chạy Bộ thao tác

1. Trong dòng, chọn **Bước mới**.
2. Trong hộp thoại **Chọn thao tác**, trong trường tìm kiếm, nhập **thực hiện hành động không ràng buộc**. Sau đó, trên tab **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Thực hiện Bộ thao tác**.
5. Trong trường **Tên hành động**, chọn **msdyn\_ExecuteOperationSetV1**.
6. Đối với trường **OperationSetId**, chọn **msdyn\_CreateOperationSetV1Response OperationSetId** trong hộp thoại **Nội dung động**.

## <a name="references"></a>Tham chiếu

- [Tổng quan về cách tích hợp các dòng quy trình với Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](schedule-api-preview.md)
- [Tổng quan về dòng đám mây - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Tổng quan về các dòng nhận biết giải pháp - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
