---
title: Sử dụng các API lịch trình dự án với Power Automate
description: Chủ đề này cung cấp một quy trình mẫu sử dụng các giao diện lập trình ứng dụng (API) theo lịch trình Dự án.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597732"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Sử dụng các API lịch trình dự án với Power Automate

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này mô tả quy trình mẫu cho biết cách tạo một kế hoạch dự án hoàn chỉnh bằng cách sử dụng Microsoft Power Automate, cách tạo Nhóm hoạt động và cách cập nhật một thực thể. Ví dụ minh họa cách tạo dự án, thành viên nhóm dự án, Bộ hoạt động, nhiệm vụ dự án và phân công tài nguyên. Chủ đề này cũng giải thích cách cập nhật một thực thể và thực hiện một Bộ hoạt động.

Sau đây là danh sách đầy đủ các bước được ghi lại trong quy trình mẫu trong chủ đề này:

1. [Tạo một PowerApps cò súng](#1)
2. [Tạo dự án](#2)
3. [Khởi tạo một biến cho thành viên trong nhóm](#3)
4. [Tạo một thành viên nhóm chung](#4)
5. [Tạo một nhóm hoạt động](#5)
6. [Tạo nhóm dự án](#6)
7. [Khởi tạo một biến cho trạng thái liên kết](#7)
8. [Khởi tạo một biến cho số lượng nhiệm vụ](#8)
9. [Khởi tạo một biến cho ID nhiệm vụ dự án](#9)
10. [Làm cho đến khi](#10)
11. [Đặt nhiệm vụ dự án](#11)
12. [Tạo một nhiệm vụ dự án](#12)
13. [Tạo phân công tài nguyên](#13)
14. [Giảm một biến](#14)
15. [Đổi tên nhiệm vụ dự án](#15)
16. [Chạy một bộ hoạt động](#16)

## <a name="assumptions"></a>Giả định

Chủ đề này giả định rằng bạn có kiến thức cơ bản về Dataverse nền tảng, các luồng đám mây và Giao diện lập trình ứng dụng theo lịch trình dự án (API). Để biết thêm thông tin, hãy xem [Người giới thiệu](#references) phần sau của chủ đề này.

## <a name="create-a-flow"></a>Tạo một dòng

### <a name="select-an-environment"></a>Chọn một môi trường

Bạn có thể tạo Power Automate chảy trong môi trường của bạn.

1. Đi đến<https://flow.microsoft.com> và sử dụng thông tin đăng nhập quản trị viên của bạn để đăng nhập.
2. Ở góc trên bên phải, hãy chọn **Môi trường**.
3. Trong danh sách, hãy chọn môi trường nơi Dynamics 365 Project Operations được cài đặt.

### <a name="create-a-solution"></a>Tạo một giải pháp

Làm theo các bước sau để tạo [dòng nhận biết giải pháp](/power-automate/overview-solution-flows). Bằng cách tạo luồng nhận biết giải pháp, bạn có thể dễ dàng xuất luồng để sử dụng sau này.

1. Trong ngăn dẫn hướng, hãy chọn **Các giải pháp**.
2. Trên **Các giải pháp** trang, chọn **Giải pháp mới**.
3. Bên trong **Giải pháp mới** hộp thoại, đặt các trường bắt buộc, sau đó chọn **Tạo ra**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Bước 1: Tạo một PowerApps cò súng

1. Trên **Các giải pháp** trang, chọn giải pháp mà bạn đã tạo, sau đó chọn **Mới mẻ**.
2. Trong ngăn bên trái, hãy chọn **Mây trôi** \> **Tự động hóa** \> **Dòng chảy của đám mây** \> **Lập tức**.
3. Bên trong **Tên luồng** trường, nhập **Lập lịch trình trình diễn API**.
4. Bên trong **Chọn cách kích hoạt luồng này** danh sách, chọn **Power Apps**. Khi bạn tạo một Power Apps kích hoạt, logic là tùy thuộc vào bạn với tư cách là tác giả. Trong chủ đề này, hãy để trống các tham số đầu vào cho mục đích thử nghiệm.
5. Chọn **Tạo**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Bước 2: Tạo dự án

Làm theo các bước sau để tạo một dự án mẫu.

1. Trong quy trình bạn đã tạo, hãy chọn **Bước mới**.

    ![Thêm một bước mới.](media/newstep.png)

2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.

    ![Chọn một hoạt động.](media/chooseactiontab.png)

3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.

![Đổi tên một bước.](media/renamestep.png)

4. Đổi tên bước **Tạo dự án**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ CreateProjectV1**.
6. Bên dưới **msdyn\_ môn học** trường, chọn **Thêm nội dung động**.
7. Trên **Biểu hiện**, trong trường chức năng, hãy nhập **Tên dự án - utcNow ()**.
8. Chọn **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Bước 3: Khởi tạo một biến cho thành viên trong nhóm

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **khởi tạo biến**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Thành viên nhóm Init**.
5. Bên trong **Tên** trường, nhập **TeamMemberAction**.
6. Bên trong **Gõ phím** trường, chọn **Sợi dây**.
7. Bên trong **Giá trị** trường, nhập **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Bước 4: Tạo một thành viên chung trong nhóm

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo thành viên trong nhóm**.
5. Cho **Tên hành động** trường, chọn **TeamMemberAction** bên trong **Nội dung động** hộp thoại.
6. Bên trong **Tham số hành động**, nhập thông tin tham số sau.

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

    Đây là giải thích về các tham số:

    - **\@\@ odata.type** - Tên thực thể. Ví dụ, nhập **"Microsoft.Dynamics.CRM.msdyn\_ nhóm dự án"**.
    - **msdyn\_ projectteamid** - Khóa chính của ID nhóm dự án. Giá trị là một biểu thức định danh duy nhất trên toàn cầu (GUID).   ID được tạo từ tab biểu thức.

    - **msdyn\_ dự định\@ odata.bind** - Mã dự án của dự án sở hữu. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo dự án". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/ msdyn\_ dự án (THÊM NỘI DUNG NĂNG ĐỘNG) "**.
    - **msdyn\_ Tên** - Tên của thành viên trong nhóm. Ví dụ, nhập **"Lịch trìnhAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Bước 5: Tạo Nhóm hoạt động

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo nhóm hoạt động**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ CreateOperationSetV1** Dataverse hành động tùy chỉnh.
6. Bên trong **Sự miêu tả** trường, nhập **ScheduleAPIDemoOperationSet**.
7. Bên trong **Dự định** trường, nhập **/ msdyn\_ dự án (**.
8. Bên trong **Nội dung động** hộp thoại, chọn **msdyn\_ CreateProjectV1Response ProjectId**.
9. Bên trong **Dự định** trường, nhập **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Bước 6: Tạo nhóm dự án

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thêm hàng mới**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo nhóm**.
5. Bên trong **Tên bảng** trường, chọn **Nhóm dự án**.
6. Bên trong **Tên** trường, nhập **Lên lịchAPIDemoBucket1**.
7. Cho **Dự định** trường, chọn **msdyn\_ CreateProjectV1Response ProjectId** bên trong **Nội dung động** hộp thoại.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Bước 7: Khởi tạo một biến cho trạng thái liên kết

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **khởi tạo biến**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Init linkstatus**.
5. Bên trong **Tên** trường, nhập **linkstatus**.
6. Bên trong **Gõ phím** trường, chọn **Số nguyên**.
7. Bên trong **Giá trị** trường, nhập **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Bước 8: Khởi tạo một biến cho số lượng nhiệm vụ

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **khởi tạo biến**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Init Số lượng nhiệm vụ**.
5. Bên trong **Tên** trường, nhập **số lượng nhiệm vụ**.
6. Bên trong **Gõ phím** trường, chọn **Số nguyên**.
7. Bên trong **Giá trị** trường, nhập **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Bước 9: Khởi tạo một biến cho ID nhiệm vụ dự án

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **khởi tạo biến**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Init ProjectTaskID**.
5. Bên trong **Tên** trường, nhập **số lượng nhiệm vụ**.
6. Bên trong **Gõ phím** trường, chọn **Sợi dây**.
7. Cho **Giá trị** trường, nhập **hướng dẫn ()** trong trình tạo biểu thức.

## <a name="step-10-do-until"></a><a id="10"></a> Bước 10: Làm cho đến khi

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **làm cho đến khi**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Đặt giá trị đầu tiên trong câu lệnh điều kiện thành **số lượng nhiệm vụ** biến từ **Nội dung động** hộp thoại.
4. Đặt điều kiện thành **nhỏ hơn bằng**.
5. Đặt giá trị thứ hai trong câu lệnh điều kiện thành **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Bước 11: Đặt nhiệm vụ dự án

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **đặt biến**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước mới, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Đặt nhiệm vụ dự án**.
5. Bên trong **Tên** trường, chọn **msdyn\_ projecttaskid**.
6. Cho **Giá trị** trường, nhập **hướng dẫn ()** trong trình tạo biểu thức.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Bước 12: Tạo nhiệm vụ dự án

Làm theo các bước sau để tạo nhiệm vụ dự án có ID duy nhất thuộc về dự án hiện tại và nhóm dự án mà bạn đã tạo.

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo nhiệm vụ dự án**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ PssCreateV1**.
6. Bên trong **Thực thể**, nhập thông tin tham số sau.

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

    Đây là giải thích về các tham số:

    - **\@\@ odata.type** - Tên thực thể. Ví dụ, nhập **"Microsoft.Dynamics.CRM.msdyn\_ projecttask "**.
    - **msdyn\_ projecttaskid** - ID duy nhất của nhiệm vụ. Giá trị phải được đặt thành một biến động từ **msdyn\_ projecttaskid**.
    - **msdyn\_ dự định\@ odata.bind** - Mã dự án của dự án sở hữu. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo dự án". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/ msdyn\_ dự án (THÊM NỘI DUNG NĂNG ĐỘNG) "**.
    - **msdyn\_ môn học** - Tên nhiệm vụ bất kỳ.
    - **msdyn\_ projectbucket\@ odata.bind** - Nhóm dự án chứa các nhiệm vụ. Giá trị sẽ là nội dung động đến từ phản hồi của bước "Tạo nhóm". Đảm bảo rằng bạn nhập đường dẫn đầy đủ và thêm nội dung động vào giữa các dấu ngoặc đơn. Dấu ngoặc kép là bắt buộc. Ví dụ, nhập **"/ msdyn\_ projectbuckets (THÊM NỘI DUNG NĂNG ĐỘNG) "**.
    - **msdyn\_ khởi đầu** - Nội dung động cho ngày bắt đầu. Ví dụ: ngày mai sẽ được biểu thị là **"addDays (utcNow (), 1)"**.
    - **msdyn\_ bắt đầu theo lịch trình** - Ngày bắt đầu dự kiến. Ví dụ: ngày mai sẽ được biểu thị là **"addDays (utcNow (), 1)"**.
    - **msdyn\_ kết thúc lịch trình** - Ngày kết thúc dự kiến. Chọn một ngày trong tương lai. Ví dụ, chỉ định **"addDays (utcNow (), 5)"**.
    - **msdyn\_ LinkStatus** - Trạng thái liên kết. Ví dụ, nhập **"192350000"**.

7. Cho **OperationSetId** trường, chọn **msdyn\_ CreateOperationSetV1Response** bên trong **Nội dung động** hộp thoại.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Bước 13: Tạo phân công tài nguyên

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Tạo bài tập**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ PssCreateV1**.
6. Bên trong **Thực thể**, nhập thông tin tham số sau.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Cho **OperationSetId** trường, chọn **msdyn\_ CreateOperationSetV1Response** bên trong **Nội dung động** hộp thoại.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Bước 14: Giảm một biến

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **biến giảm dần**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Bên trong **Tên** trường, chọn **số lượng nhiệm vụ**.
4. Bên trong **Giá trị** trường, nhập **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Bước 15: Đổi tên nhiệm vụ dự án

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Đổi tên Nhiệm vụ Dự án**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ PssUpdateV1**.
6. Bên trong **Thực thể**, nhập thông tin tham số sau.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Cho **OperationSetId** trường, chọn **msdyn\_ CreateOperationSetV1Response** bên trong **Nội dung động** hộp thoại.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Bước 16: Chạy một bộ hoạt động

1. Trong luồng, hãy chọn **Bước mới**.
2. Bên trong **Chọn một hoạt động** hộp thoại, trong trường tìm kiếm, hãy nhập **thực hiện hành động không ràng buộc**. Sau đó, trên **Hành động**, chọn thao tác trong danh sách kết quả.
3. Trong bước này, hãy chọn dấu chấm lửng (**...**), rồi chọn **Đổi tên**.
4. Đổi tên bước **Thực thi Bộ hoạt động**.
5. Bên trong **Tên hành động** trường, chọn **msdyn\_ ExecuteOperationSetV1**.
6. Cho **OperationSetId** trường, chọn **msdyn\_ CreateOperationSetV1Response OperationSetId** bên trong **Nội dung Dynamid** hộp thoại.

## <a name="references"></a>Tham chiếu

- [Tổng quan về cách tích hợp các luồng với Dataverse -Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](schedule-api-preview.md)
- [Tổng quan về các luồng đám mây -Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Tổng quan về các luồng nhận biết giải pháp -Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
