---
title: Khắc phục sự cố khi làm việc trong lưới Tác vụ
description: Bài viết này cung cấp thông tin khắc phục sự cố cần thiết khi làm việc trong lưới Nhiệm vụ.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188258"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Khắc phục sự cố khi làm việc trong lưới Tác vụ 


_**Áp dụng cho:** Project Operations cho các kịch bản dựa trên nguồn lực/không trữ kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá, Project for the web_

Lưới Nhiệm vụ được Dynamics 365 Project Operations sử dụng là một iframe được tổ chức bên trong Microsoft Dataverse. Do việc sử dụng này, các yêu cầu cụ thể phải được đáp ứng để đảm bảo xác thực và ủy quyền hoạt động chính xác. Bài viết này phác thảo các vấn đề chung có thể ảnh hưởng đến khả năng kết xuất lưới điện hoặc quản lý các tác vụ trong cấu trúc phân tích công việc (WBS).

Các sự cố thường gặp bao gồm:

- Tab **Nhiệm vụ** trên lưới Nhiệm vụ trống.
- Khi mở dự án, dự án không tải và giao diện người dùng (UI) bị kẹt trên vòng quay.
- Quản lý các đặc quyền cho **Project for the Web**.
- Các thay đổi không được lưu khi bạn tạo, cập nhật hoặc xóa một công việc.

## <a name="issue-the-task-tab-is-empty"></a>Sự cố: Tab Nhiệm vụ trống

### <a name="mitigation-1-enable-cookies"></a>Giảm nhẹ 1: Bật cookie

Project Operations yêu cầu bật cookie của bên thứ ba để hiển thị cấu trúc phân tích công việc. Khi cookie của bên thứ ba không được bật, thay vì thấy các nhiệm vụ, bạn sẽ thấy trang trống khi chọn tab **Nhiệm vụ** trên trang **Dự án**.

Đối với Microsoft Edge hoặc trình duyệt Google Chrome, các quy trình sau đây trình bày cách cập nhật cài đặt trình duyệt của bạn để bật cookie của bên thứ ba.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Mở trình duyệt Edge.
2. Ở góc trên bên phải, chọn biểu tượng **dấu chấm lửng** (...), sau đó chọn **Cài đặt**.
3. Trong **Cookie và quyền đối với trang web**, chọn **Cookie và dữ liệu trang web**.
4. Tắt tùy chọn **Chặn cookie bên thứ ba**.
5. Làm mới trình duyệt của bạn. 

#### <a name="google-chrome"></a>Google Chrome

1. Mở trình duyệt Chrome.
2. Ở góc trên bên phải, chọn dấu 3 chấm dọc, sau đó chọn **Cài đặt**.
3. Trong **Quyền riêng tư và bảo mật**, chọn **Cookie và dữ liệu khác của trang web**.
4. Chọn **Cho phép tất cả cookie**.
5. Làm mới trình duyệt của bạn. 

> [!NOTE]
> Nếu bạn chặn cookie của bên thứ ba, tất cả cookie và dữ liệu trang web từ các trang web khác sẽ bị chặn, ngay cả khi trang web đó được cho phép trong danh sách ngoại lệ của bạn.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Giảm nhẹ 2: Xác thực Điểm cuối PEX đã được đặt cấu hình chính xác

Project Operations yêu cầu tham số dự án tham chiếu đến Điểm cuối PEX. Điểm cuối này được yêu cầu để giao tiếp với dịch vụ được sử dụng để hiển thị cấu trúc phân tích công việc. Nếu tham số không được bật, bạn sẽ nhận được lỗi "Tham số dự án không hợp lệ". Để cập nhật Điểm cuối PEX, hãy hoàn thành các bước sau.

1. Thêm trường **Điểm cuối PEX** vào trang **Tham số dự án**.
2. Xác định loại sản phẩm mà bạn đang sử dụng. Giá trị này được sử dụng khi PEX Endpoint được đặt. Khi truy xuất, loại sản phẩm đã được xác định trong PEX Endpoint. Giữ nguyên giá trị đó.
3. Cập nhật trường này với giá trị sau: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Bảng sau cung cấp tham số loại sẽ được sử dụng dựa trên loại sản phẩm.

      | **Loại sản phẩm**                     | **Nhập tham số** |
      |--------------------------------------|--------------------|
      | Project for the Web trên tổ chức mặc định   | loại=0             |
      | Project for the Web trên tổ chức do CDS đặt tên | loại=1             |
      | Project Operations                   | loại=2             |

4. Xóa trường khỏi trang **Tham số dự án**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Di chuyển 3: Đăng nhập vào project.microsoft.com

Trong trình duyệt của bạn, mở một tab mới, truy cập project.microsoft.com và đăng nhập với vai trò người dùng mà bạn đang sử dụng để truy cập Project Operations. Điều quan trọng là chỉ một người dùng đăng nhập vào sản phẩm của Microsoft trong trình duyệt. Thông báo lỗi "login.microsoftonline.com từ chối kết nối" thường xảy ra nhất khi có nhiều người dùng đăng nhập, như trong hình minh họa sau.

![Chọn một trang đăng nhập tài khoản hiển thị rằng hai người dùng đã đăng nhập.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Sự cố: Dự án không tải và giao diện người dùng bị kẹt trên vòng quay

Đối với mục đích xác thực, cửa sổ bật lên phải được bật để lưới Nhiệm vụ tải. Nếu không bật cửa sổ bật lên, màn hình sẽ bị kẹt trên vòng quay tải. Hình ảnh sau đây cho thấy URL có nhãn bật lên bị chặn trong thanh địa chỉ, dẫn đến việc vòng quay bị kẹt khi cố tải trang. 

   ![Bị mắc kẹt trong vòng quay và chặn cửa sổ bật lên.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Giảm nhẹ 1: Bật cửa sổ bật lên

Khi dự án của bạn bị kẹt trên vòng quay, có thể không bật được cửa sổ bật lên.

#### <a name="microsoft-edge"></a>Microsoft Edge

Có hai cách để bật cửa sổ bật lên trong trình duyệt Edge.

1. Trong trình duyệt Edge, chọn thông báo ở phía trên bên phải của trình duyệt.
2. Chọn **Luôn cho phép cửa sổ bật lên và chuyển hướng từ** môi trường Dataverse cụ thể.
 
     ![Cửa sổ bật lên bị chặn.](media/enablepopups.png)

Ngoài ra, bạn có thể hoàn thành các bước sau.

1. Mở trình duyệt Edge.
2. Ở góc trên bên phải, hãy chọn **dấu chấm lửng** (...), rồi chọn **Cài đặt** > **Quyền đối với site** > **Cửa sổ bật lên và chuyển hướng**.
3. Tắt **Cửa sổ bật lên và chuyển hướng** để chặn cửa sổ bật lên hoặc bật để cho phép cửa sổ bật lên trên thiết bị của bạn.
4. Sau khi bạn bật cửa sổ bật lên, hãy làm mới trình duyệt của bạn. 

#### <a name="google-chrome"></a>Google Chrome
1. Mở trình duyệt Chrome.
2. Điều hướng đến một trang có cửa sổ bật lên bị chặn.
3. Trong thanh địa chỉ, hãy chọn **Cửa sổ bật lên bị chặn**.
4. Chọn liên kết cho cửa sổ bật lên bạn muốn xem.
5. Sau khi bạn bật cửa sổ bật lên, hãy làm mới trình duyệt của bạn. 

> [!NOTE]
> Để luôn thấy cửa sổ bật lên cho trang web, hãy chọn **Luôn cho phép cửa sổ bật lên và chuyển hướng từ [site]** và sau đó chọn **Xong**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Sự cố 3: Quản lý các đặc quyền cho Project for the Web

Project Operations dựa vào một dịch vụ lập lịch bên ngoài. Dịch vụ yêu cầu người dùng có một số vai trò được chỉ định cho phép họ đọc và ghi vào các thực thể liên quan đến WBS. Các thực thể này bao gồm nhiệm vụ dự án, phân công nguồn lực và mức phụ thuộc nhiệm vụ. Nếu người dùng không thể hiển thị WBS khi họ điều hướng đến tab **Nhiệm vụ**, có thể là do **Dự án** vì chưa bật **Project Operations**. Người dùng có thể nhận được lỗi vai trò bảo mật hoặc lỗi liên quan đến từ chối quyền truy cập.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Giảm nhẹ 1: Xác thực vai trò bảo mật của người dùng ứng dụng và người dùng cuối

1. Chuyển đến **Cài đặt** > **Bảo mật** > **Người dùng** > **Người dùng ứng dụng**.  

   ![Trình đọc ứng dụng.](media/applicationuser.jpg)
   
2. Bấm đúp vào hồ sơ người dùng ứng dụng để xác minh:

     - Người dùng có quyền truy cập vào dự án. Bạn có thể làm điều này bằng cách xác minh rằng người dùng có vai trò bảo mật **Quản lý dự án**.
     - Người dùng ứng dụng Microsoft Project tồn tại và được định cấu hình chính xác.
 
3. Nếu người dùng này không tồn tại, hãy tạo một bản ghi người dùng mới. 
4. Chọn **Người dùng mới**, thay đổi biểu mẫu nhập thành **Người dùng ứng dụng** rồi thêm **ID ứng dụng**.

   ![Chi tiết người dùng ứng dụng.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Sự cố 4: Các thay đổi không được lưu khi bạn tạo, cập nhật hoặc xóa một công việc

Khi bạn thực hiện một hoặc nhiều bản cập nhật cho WBS, các thay đổi sẽ không thành công và không được lưu. Lỗi xảy ra trong lưới lịch biểu với thông báo "Không thể lưu thay đổi gần đây bạn đã thực hiện".

### <a name="mitigation-1-validate-the-license-assignment"></a>Giảm nhẹ 1: Xác thực việc chuyển nhượng giấy phép

1. Xác minh rằng người dùng đã được gán đúng giấy phép và dịch vụ được bật trong chi tiết gói dịch vụ của giấy phép.  
2. Xác minh rằng người dùng có thể mở **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Giảm nhẹ 2: Cấu hình xác thực của người dùng ứng dụng Dự án
1. Xác minh rằng Người dùng ứng dụng dự án đã được tạo.
2. Áp dụng các vai trò bảo mật sau cho người dùng:
  
  - Người dùng Dataverse hoặc người dùng Cơ sở
  - Hệ thống Project Operations
  - Hệ thống Dự án
  - Hệ thống ghi kép Project Operations. Cần có vai trò này cho kịch bản triển khai dựa trên nguồn lực/không trữ kho của Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
