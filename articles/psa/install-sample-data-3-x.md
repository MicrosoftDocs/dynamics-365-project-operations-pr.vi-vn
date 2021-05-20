---
title: Cài đặt dữ liệu mẫu
description: Chủ đề này cung cấp thông tin về việc cài đặt dữ liệu mẫu trong Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: c521fb4000b4856fc5c2fbf3275bf3b3e0dfa458
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950605"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Cài đặt dữ liệu mẫu cho ứng dụng Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Để giúp bạn xây dựng các môi trường demo riêng, Microsoft cung cấp các gói dữ liệu mẫu có thể tải xuống hiển thị khả năng của các ứng dụng của bạn. Có hai loại gói dữ liệu mẫu:
- dữ liệu thiết lập/tham chiếu
- dữ liệu bản demo (tham khảo/thiết lập và các dữ liệu giao dịch như lệnh sản xuất và dự án)

Có thể tải gói dữ liệu **tham khảo** mẫu trong ba gói khác nhau để bạn có thể cài đặt dữ liệu chỉ cho Project Service, chỉ cho Field Service hoặc bạn có thể cài đặt dữ liệu mẫu cho cả hai ứng dụng cùng một lúc.

Các gói dữ liệu thiết lập/tham khảo mẫu là:

- [**V902PSMasterData** - Chỉ Project Service phiên bản 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Chỉ Field Service phiên bản 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x và Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Gói dữ liệu **demo** mới nhất là:

 - [**FPSDemoData** - Field Service 8.x và Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Hướng dẫn cài đặt hơi khác trong phần người dùng tạo và định cấu hình, phần còn lại giống với [**bài đăng trên blog**](https://aka.ms/fpsdemodatablog) trước đó. Gói này có một tập hợp dữ liệu demo nhỏ gọn hơn và chỉ mất khoảng 3 giờ để cài đặt.

Các gói dữ liệu mẫu này chỉ có sẵn bằng tiếng Anh.

> [!IMPORTANT]
> **Không có cách gỡ cài đặt dữ liệu mẫu.** Bạn chỉ nên cài đặt các gói này trên hệ thống minh họa, đánh giá, đào tạo hoặc thử nghiệm. Ngoài ra, hãy lưu ý rằng việc cài đặt một gói riêng lẻ rồi cài đặt gói riêng lẻ còn lại không được hỗ trợ. (Nói cách khác, bạn không thể cài đặt **FSMasterData** rồi đến **PSMasterData** hoặc ngược lại.) Nếu cần dữ liệu mẫu cho cả hai ứng dụng bất kỳ lúc nào trong tương lai, bạn nên cài đặt gói **v902FPSMasterData**.

Khi bạn cài đặt bất kỳ gói dữ liệu mẫu nào, quá trình cài đặt sẽ thực hiện các hành động sau:

- Tạo hoặc đặt thông số mặc định cho việc sử dụng Project Service, Field Service hoặc cả hai ứng dụng (nếu thích hợp).

- Nhập dữ liệu mẫu cho các ứng dụng, chẳng hạn như nguồn lực có thể đặt trước, vai trò dành riêng cho ứng dụng, bảng giá vốn và bán hàng, đơn vị tổ chức, bản ghi quy trình bán hàng và các thực thể khác để minh họa những khả năng chính.  

Với gói **dữ liệu demo**, bạn sẽ tải dữ liệu giao dịch ở trên và bổ sung chẳng hạn như lệnh sản xuất và dự án.

Bạn muốn biết có thể minh họa những khả năng nào với dữ liệu mẫu? Xem tình huống tưởng tượng Fabrikam Robotics trong [Lưu ý kỹ thuật](#technical-notes).

Nếu bạn có câu hỏi về việc cài đặt các gói dữ liệu mẫu này, [hãy gửi email cho chúng tôi theo địa chỉ fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Yêu cầu

Giao thức cài đặt giả định những điều sau về phiên bản mục tiêu của bạn (org):

- Ngôn ngữ cơ sở là tiếng Anh và đơn vị tiền tệ cơ sở là đô la Mỹ (USD,$).

- Tổ chức chưa có dữ liệu Project Service hoặc Field Service hoặc chỉ có dữ liệu mặc định cơ bản đi kèm với mọi tổ chức mới.

- Phiên bản đúng của ứng dụng kinh doanh đã được cài đặt:
       
    - **Đối với FPSDemoData hoặc v902FPSMasterData:** Tổ chức đã cài đặt Field Service phiên bản 8.x và Project Service phiên bản 3.x.

    - **Đối với v902PSMasterData:** org có Project Service phiên bản 3.x đã cài đặt.

    - **Đối với v902FSMasterData:** org có Field Service phiên bản 8.x đã cài đặt.

> [!NOTE]
> Nếu cần cài đặt dữ liệu mẫu ở đầu môi trường demo hoặc thử nghiệm Project Service và Field Service hiện tại đã có dữ liệu (không đề xuất), bạn cần tạm ngưng các bước kiểm tra trước an toàn do trình cài đặt thực hiện. Để biết thêm thông tin, hãy xem các ghi chú kỹ thuật ở bên dưới.

## <a name="prepare-for-installation"></a>Chuẩn bị cài đặt

Bạn cần chạy trình cài đặt trên máy tính có phiên bản Windows gần đây (ưu tiên Windows 10).

Bạn nên có kế hoạch để máy tính duy trì trạng thái kết nối mạng và quá trình cài đặt chạy trong tối đa **1 giờ** cho **dữ liệu thiết lập/tham khảo**. (Thông thường, quá trình cài đặt mất khoảng 30 phút cho **FPSMasterData**, bao gồm dữ liệu mẫu cho cả hai ứng dụng.) Đối với **FPSDemoData**, quá trình cài đặt sẽ mất khoảng **3 giờ**.

Máy tính cần tắt chức năng trình bảo vệ màn hình. Nếu không, thông tin xác thực phiên cho quá trình cài đặt có thể mất khi trình bảo vệ màn hình hoạt động (trừ khi bạn giữ cho phiên luôn hoạt động xuyên suốt).

> [!div class="mx-imgBorder"]
> ![Ảnh chụp màn hình về cài đặt trình bảo vệ màn hình, trình bảo vệ màn hình đang tắt](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Tải xuống và giải nén

Trình cài đặt dữ liệu mẫu Project Service và Field Service được phân phối dưới dạng tự trích xuất có thể thực thi. Tên tệp có thể biến đổi tùy theo gói dữ liệu mẫu, nếu không các bước sẽ giống nhau cho dù bạn cài đặt gói nào.

Sau khi tải một gói xuống, chạy tệp .exe, sau đó chấp nhận điều khoản và điều kiện để giải nén tệp zip nén. Sau đó, bạn cần trích xuất nội dung của tệp đó sang một thư mục trên máy tính.

Tùy vào hệ điều hành và cài đặt bảo mật, bạn có thể cần thực hiện các bước sau đây sau khi giải nén tệp zip:

1. Tìm và nhấp chuột phải vào tệp **FPSDemoData.dll** trong thư mục **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Chọn **Bỏ chặn**.

3. Chọn **Áp dụng**.

4. Chọn **OK**.


## <a name="create-or-configure-users"></a>Tạo hoặc định cấu hình người dùng

Gói **FPSDemoData** yêu cầu sáu người dùng trong khi gói **FPSMasterData** yêu cầu một người dùng. Tham khảo một hướng dẫn phù hợp cho gói dữ liệu mẫu của bạn.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Tạo hoặc đặt cấu hình người dùng - gói dữ liệu thiết lập/tham khảo

Gói **FPSMasterData** được thiết kế để cài đặt với một người dùng có tên là Spencer Low với thiết đặt được mô tả ở đây. Để cài đặt gói này đúng cách, bạn cần tạo (hoặc đổi tên tạm thời) người dùng trong môi trường của mình để khớp với cấu hình dữ liệu mẫu mới.

Để tạo hoặc định cấu hình người dùng, hãy đi đến **Thiết đặt** > **Bảo mật** > **Người dùng** và thực hiện như sau:

1. Đặt UserFullname="Spencer Low" với tên người dùng "spencerl" (**viết thường**) thành các vai trò Người quản lý dự án và Người quản lý thực tiễn.

2. Chọn người dùng **Spencer Low** rồi chọn **Quản lý vai trò**. Tìm và chọn vai trò **Quản trị viên hệ thống**, sau đó chọn **OK** để cấp quyền quản trị đầy đủ cho Spencer Low. Bước này cần thiết để đảm bảo bản ghi mẫu được tạo bằng đúng quyền sở hữu người dùng và từ đó, đưa vào các dạng xem chính xác.

3. Từ trang đã tải xuống, bạn cần cập nhật một tệp ánh xạ dữ liệu với các địa chỉ email của ngữ cảnh người dùng mặc định. Để làm điều này, hãy mở **PkgFolder**, sau đó tìm và mở tệp **ImportUserMapFile.xml** trong Notepad (hoặc Visual Studio hay trình soạn thảo XML khác). Đặt trường **DefaultUserToMapTo=** thành các địa chỉ email của người dùng Spencer Low.

4. Nếu bạn hiện không sử dụng Spencer Low với tên người dùng **spencerl**, bạn cần cập nhật một tệp bổ sung. Mở tệp **DemoDataPreImportConfig.xml**, sau đó tìm thẻ **userstocreateandconfigure**. Cập nhật thẻ **\<login\>** với tên người dùng của người dùng Spencer Low. Để biết thêm thông tin, hãy xem [Lưu ý kỹ thuật](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Tạo hoặc đặt cấu hình người dùng - gói dữ liệu demo

Gói dữ liệu demo yêu cầu sáu người dùng. Để gói cài đặt đúng cách, hãy làm như sau:

 1. Tạo hoặc tạm thời đổi tên người dùng hiện có để khớp cấu hình dữ liệu mẫu sắp tới bằng cách truy cập **Cài đặt** > **Bảo mật** > **Người dùng**.
 
    Chỉ những bản demo dựa trên cá nhân mới cần những vai trò này.  
    - Tên đầy đủ của người dùng="David So" với tư cách Kỹ thuật viên Field Service   
    - Tên đầy đủ người dùng="Jamie Reding" với tư cách Người điều vận Customer Service & Field Service   
    - Tên đầy đủ người dùng="Molly Clark" với tư cách Quản lý khách hàng   
    - Tên đầy đủ người dùng="Spencer Low" với tư cách Quản lý dự án và phương pháp  
    - Tên đầy đủ người dùng="Veronica Quek" với tư cách Thành viên nhóm   
    - Tên đầy đủ của người dùng="William Contoso"
  
2. Đối với các mục đích nhập dữ liệu demo, hãy chỉ định vai trò Quản trị viên cho sáu người dùng ở trên để bản ghi mẫu nhập đúng cách. 

3. Mở **PkgFolder**, sau đó tìm và mở **ImportUserMapFile.xml**. Cập nhật các trường **New=** cho địa chỉ email của người dùng tương ứng trong hệ thống của bạn.

   > [!div class="mx-imgBorder"]
   > ![Ảnh chụp màn hình của UserMapFile](media/sample-data-7.png)

4. Nếu người dùng tên đầy đủ là "Spencer Low" có ID người dùng khác với **"spencerl"**, thì bạn cần cập nhật tệp bổ sung. Mở **DemoDataPreImportConfig.xml** và tìm thẻ **userstocreateandconfigure**. Cập nhật thẻ **\<login\>** bằng loginId (có phân biệt chữ hoa chữ thường). 

5. Lịch của người dùng đầu tiên (trong thẻ **userstocreateandconfigure** tag) được dùng để điền số giờ làm việc cho tất cả tài nguyên đã đặt lịch trên nhập dữ liệu demo. Điều hướng đến **Cài đặt** > **Bảo mật** > **Người dùng**, tìm người dùng "Spencer Low", và mở tùy chọn "Số giờ làm việc". Chỉnh sửa giờ làm việc hiện có, chọn tùy chọn **Nhập lịch trình nhắc lại hàng tuần từ bắt đầu đến kết thúc**. Đảm bảo **Giờ làm việc đặt thành 8 SA - 5 CH (9 tiếng), thứ Hai đến thứ Sáu với Múi giờ đặt thành Giờ Thái Bình Dương (Hoa Kỳ và Canada)**. Cần đặt mục này để đảm bảo rằng bảng Project và Lịch trình hiển thị như mong muốn.

**Khuyến nghị:** Cân nhắc tạo bản sao của org hiện tại, phòng khi bạn cần hoàn nguyên về điểm bắt đầu nếu có sự cố trong khi cài đặt dữ liệu mẫu. Để biết thêm thông tin, hãy xem [2Sao lưu và khôi phục các phiên bản](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Chạy Package Deployer

1. Tìm và chạy **PackageDeployer.exe** trong thư mục **v902FPSMasterData** HOẶC **PackageDeployer_FPSDemoData**.

2. Chấp nhận các điều khoản và điều kiện.

3. Trên cửa sổ tiếp theo:

   a. Chọn loại triển khai **Office 365**.

   b. Sử dụng người dùng và mật khẩu của người dùng quản trị viên hệ thống được định cấu hình trong "Tạo và định cấu hình người dùng" ("Spencer Low" với tên người dùng "spencerl").

   c. Đảm bảo đã chọn **Hiển thị danh sách tổ chức hiện có**.

      > [!div class="mx-imgBorder"]
      > ![Ảnh chụp màn hình cửa sổ Package Deployer với "Hiển thị danh sách các tổ chức có sẵn" được chọn](media/sample-data-2.png)

4. Chọn tổ chức nơi bạn muốn cài đặt dữ liệu mẫu.

5. Chọn **Tiếp** cho đến khi bạn thấy hộp thoại **Thiết lập dữ liệu demo**.

   > [!div class="mx-imgBorder"]
   > ![Ảnh chụp màn hình cửa sổ trạng thái trình cài đặt dữ liệu demo](media/sample-data-3.png)

6. Trước khi tiếp tục, hãy lưu ý rằng việc cài đặt dữ liệu mẫu có thể mất tối đa một giờ (thông thường là ~10 phút). Bạn sẽ cần phải đảm bảo rằng máy tính duy trì trạng thái bật và kết nối với mạng trong suốt quá trình cài đặt và phiên của bạn vẫn hoạt động.   

7. Khi bạn đã sẵn sàng, hãy bấm vào **Tiếp** để bắt đầu quá trình cài đặt dữ liệu mẫu. Sau khi dữ liệu mẫu được tải, bấm vào **Kết thúc**.

## <a name="verify-the-sample-data-installation"></a>Xác minh cài đặt dữ liệu mẫu

Để kiểm tra độ chính xác, hãy xác minh rằng số bản ghi và loại thực thể được liệt kê trong kịch bản hư cấu Fabrikam Robotics xuất hiện như dự kiến.

Sau khi dữ liệu mẫu tải hoàn toàn, đăng nhấp với tư cách người dùng Spencer Low và xác nhận những điều sau:

- Nếu ứng dụng Project Service được cài đặt, hãy đi đến **Project Service** > **Thiết đặt** > **Bảng giá**. Xác nhận rằng chi phí và mức tính phí tồn tại với đơn vị tiền tệ thích hợp cho mỗi quốc gia/vùng lãnh thổ trong tập hợp dữ liệu.

- Nếu ứng dụng Project Service được cài đặt, hãy đi đến **Universal Resource Scheduling** > **Cài đặt** > **Đơn vị tổ chức**. Xác nhận rằng một bảng giá vốn với đơn vị tiền tệ thích hợp đã được liên kết với mỗi đơn vị tổ chức (bao gồm cả mục nhập thành phố). Nếu thiếu, hãy tìm và liên kết bảng giá vốn chính xác.

- Nếu ứng dụng Field Service được cài đặt, hãy đi đến **Project Service** > **Thiết đặt** > **Bảng giá**. Xác nhận chi phí và mức tính phí tồn tại. Đi đến **Field Service** > **Thiết đặt** > **Bảng giá** và kiểm tra để đảm bảo chi phí và mức tính phí tồn tại, với đơn vị tiền tệ thích hợp, cho mỗi quốc gia/vùng lãnh thổ trong tập hợp dữ liệu.

  > [!div class="mx-imgBorder"]
  > ![Ảnh chụp màn hình một bảng giá hiện hoạt](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Ảnh chụp màn hình đơn vị tổ chức hiện hoạt](media/sample-data-5.png)

## <a name="technical-notes"></a>Ghi chú kỹ thuật

Xem dưới đây để biết thêm chi tiết kỹ thuật về việc cài đặt dữ liệu này.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Cài đặt dữ liệu mẫu trên dữ liệu hiện có (không khuyến nghị)

Nếu cần cài đặt dữ liệu mẫu ở đầu môi trường demo hoặc thử nghiệm Project Service hoặc Field Service hiện tại đã có dữ liệu, bạn cần tạm ngưng các bước kiểm tra trước an toàn do trình cài đặt thực hiện.

Để làm điều này, hãy đi đến thư mục **PkgFolder** để tìm và mở tệp **DemoDataPreImportConfig.xml** bằng Notepad (hoặc trình soạn thảo XML khác).

Tìm giá trị sau đây rồi thay đổi thiết đặt từ đúng thành sai:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Thay đổi này khiến trình cài đặt bỏ qua một số khâu kiểm tra an toàn quan trọng, trong đó có:

- Xác nhận rằng không có quá một bản ghi  **Đơn vị tổ chức** hiện hoạt, sau đó đổi tên bản ghi đó thành **Fabrikam US**.

- Xác nhận không có quá một bản ghi **Mẫu công việc** hiện hoạt.

- Xác nhận rằng không có quá một bản ghi **Thông số dự án** hiện hoạt, sau đó đổi tên bản ghi đó thành **Thông số**.

### <a name="configuration-components"></a>Thành phần cấu hình

Có nhiều thành phần cấu hình khác trong tệp cấu hình nhập trước này. Đối với người dùng kỹ thuật, một số thành phần bao gồm:

- **\<RequiredSolutions\>** chỉ định cài đặt giải pháp tiên quyết và số phiên bản.

- **\<InstallSampleData\>** kiểm soát xem dữ liệu mẫu sẵn dùng cho ứng dụng đã được cài đặt chưa.

    - sai - bỏ qua cài đặt dữ liệu tích hợp sẵn này (có thể loại bỏ)

    - đúng - cài đặt dữ liệu tích hợp sẵn đồng thời với cài đặt dữ liệu mẫu FS Và PSA

- **\<PreImportDataCollection\>** chỉ định Bản đồ dữ liệu tệp phẳng và Bản ghi được liên kết cần nhập trước khi cài đặt dữ liệu mẫu chính.

- **\<EntitiesToEnableScheduling\>** chỉ định những thực thể có thể bật cho Đặt lịch trong Microsoft Dynamics Scheduling (còn gọi là Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** chỉ định Nguồn lực có thể đặt trước sẽ được tạo (nếu chưa tồn tại) trước khi quá trình nhập dữ liệu mẫu thực thi. Lưu ý rằng Nguồn lực có thể đặt trước của dữ liệu mẫu hệ thống nguồn khớp với bản ghi Nguồn lực có thể đặt trước của hệ thống mục tiêu trên phần FullName và đăng nhập của mỗi nguồn lực. Vì vậy, KHÔNG thể thay đổi tên trong tệp cấu hình trước này trừ khi bạn nhập dữ liệu mẫu vào một hệ thống mục tiêu trước bằng các tên này, sau đó đổi tên Nguồn lực có thể đặt trước thành tên mong muốn được đặt cùng với bản ghi Đã bật người dùng, sau đó xuất dữ liệu lại để nhập vào hệ thống đích cuối cùng (cập nhật các mục nhập **ImportUserMapFile.xml** Cũ và Mới theo đó).

- **\<PluginsToDisable\>** chỉ định phần bổ trợ mục dòng riêng biệt phải tắt trong khi nhập dữ liệu mẫu và bật lại sau đó.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Kịch bản hư cấu Fabrikam Robotics

Các gói dữ liệu tham khảo Field Service và Project Service cài đặt giải pháp **Fabrikam Manufacturing Master Data (v3.0.0.0)**, cùng với khoảng 4.000 bản ghi và khoảng 40 thực thể khác nhau. Các gói dữ liệu mẫu riêng cho Field Service hoặc Project Service chứa một tập hợp con dữ liệu mẫu **v902FPSMasterData** cho ứng dụng đó. Gói **Dữ liệu Demo** cài đặt **giải pháp Fabrikam Manufacturing Demo Data (v3.0.0.7)** với khoảng 22.000 bản ghi trên 148 thực thể.

Công ty tưởng tượng Fabrikam Robotics là một nhà sản xuất rô-bốt dây chuyền lắp ráp thiết bị điện tử và có tiếng về chất lượng sản phẩm, cải tiến và dịch vụ khách hàng đáng tin cậy, bao gồm cả lên kế hoạch cài đặt, triển khai và các dịch vụ bảo dưỡng liên tục. Fabrikam có trụ sở tại Hoa Kỳ (Fabrikam Hoa Kỳ) và có các cơ sở dịch vụ theo dự án tại Pháp, Ấn Độ, Vương Quốc Anh và Thụy Sĩ.

Các cơ sở Field Service tập trung ở Hoa Kỳ, chủ yếu ở khu vực Seattle lớn hơn. Công ty tập trung khai thác khả năng kết nối của Vật dụng kết nối Internet (IoT) để giám sát hiệu quả tài sản của khách hàng và cung cấp các dịch vụ tại chỗ với tính chủ động ngày càng cao.

Tổng quan cấp cao về dữ liệu mẫu như sau:

- Các thành phần dữ liệu mẫu phổ biến (được bao gồm cho cả hai ứng dụng)

    - 1 người dùng

    - 71 tài khoản

    - 137 người liên hệ

    - Nhiều danh mục và loại giao dịch khác nhau

    - 50 sản phẩm với 1 bảng giá sản phẩm

    - 14 bảng giá/chi phí

    - 31 đặc điểm (kỹ năng của nguồn lực) trong 2 mô hình xếp hạng với 3 cấp độ (giá trị xếp hạng)

- Project Service

    - 8 đơn vị tổ chức

    - 6 cấp độ thời gian làm việc theo từng vai trò

    - 2,8k+ thông số kỹ thuật vai trò-giá

- Field Service

    - 4 vùng lãnh thổ

    - 5 loại lệnh sản xuất

    - 22 tài sản khách hàng

    - 9 loại sự cố với nhiều đặc điểm nguồn lực (9), dịch vụ (13) và nhiệm vụ dịch vụ (13) liên quan
   
Gói **Demo Data** cài đặt khoảng 179 lệnh sản xuất, 12 dự án và dữ liệu giao dịch liên kết. 

### <a name="change-the-work-hours-for-sample-resources"></a>Thay đổi giờ làm việc cho nguồn lực mẫu

Theo mặc định, tất cả các nguồn lực có thể đặt trước đều có lịch 24 giờ làm việc.

Nếu bạn cần thay đổi giờ làm việc cho các mẫu nguồn lực có thể đặt trước, hãy đi đến **Universal Resource Scheduling** > **Lập lịch** > **Nguồn lực**.

Chọn một người dùng (ví dụ: Spencer Low) và thay đổi giờ làm việc của Spencer thành giờ bạn muốn áp dụng cho nhiều người dùng. Đi đến **Universal Resource Scheduling** > **Thiết đặt** > **Mẫu giờ làm việc** và chỉnh sửa bản ghi **Mẫu công việc mặc định**. Trong trường **Nguồn lực mẫu**, chọn một người dùng có giờ làm việc mà bạn muốn áp dụng cho các nguồn lực khác. Đi đến **Universal Resource Scheduling** > **Lập lịch** > **Tài nguyên** > **Tài nguyên có thể đặt hoạt động**. Chọn nguồn lực bạn muốn thay đổi, sau đó chọn **Đặt lịch**. Trên danh sách thả xuống **Mẫu công việc**, hãy chọn mẫu **Giờ làm việc mặc định** hoặc một mẫu khác có nguồn lực mẫu chính xác. Khi đi đến bảng lịch trình, bạn có thể thấy các nguồn lực hiện đã có giờ làm việc được cập nhật.

> [!div class="mx-imgBorder"]
> ![Ảnh chụp màn hình nguồn lực có thể đặt trước hiện hoạt](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]