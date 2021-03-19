---
title: Tùy chỉnh mục nhập thời gian hàng tuần
description: Chủ đề này cung cấp thông tin về cách triển khai các quy tắc kinh doanh tùy chỉnh hỗ trợ cách thức của một tổ chức.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
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
ms.openlocfilehash: f1c8e150500334e87b25a1c8d04cf28c7b7beaeb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282089"
---
# <a name="customize-weekly-time-entry"></a>Tùy chỉnh mục nhập thời gian hàng tuần 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Trong Microsoft Dynamics 365 Project Service Automation phiên bản 3.3, Microsoft đã giới thiệu một lưới hiện đại cho phép nguồn lực dự án nhanh chóng nhập thời gian cho tối đa 1 tuần 1 lúc. Lưới mục nhập thời gian hàng tuần mới này có thể hiển thị tổng số cho các mục theo ngày, theo hàng hoặc theo tuần. Các nguồn lực có thể tạo bản sao của mục nhập thời gian trong tuần và cũng sao chép hàng loạt từ các tuần trước. Bộ tùy chỉnh hệ thống có thể tùy chỉnh dạng xem bằng cách thêm các trường, thêm thông tin tra cứu cho các thực thể khác và triển khai quy tắc kinh doanh tùy chỉnh để hỗ trợ phương thức của tổ chức.

Mục nhập thời gian và lưới thời gian hàng tuần mới được truy cập thông qua bản đồ trang web. Trải nghiệm mục nhập thời gian tùy chỉnh không mở rộng là một phần của phiên bản PSA trước đó đã được thay thế bằng lưới mục nhập thời gian hàng tuần mở rộng, đồng thời bằng một trải nghiệm thay thế trong lưới chỉ đọc và lịch. Do sự thay đổi này, người dùng có thể nhập thời gian vào số tiền hàng tuần.

## <a name="page-layout"></a>Bố cục trang
Lưới mục nhập thời gian hàng tuần là kiểm soát tùy chỉnh có thanh công cụ và hai phần chính **Thông số** và **Thời gian**. Thanh công cụ bao gồm một nút chỉ áp dụng cho điều khiển tùy chỉnh này cho lưới mục nhập thời gian. Ngược lại, các nút trên Ngăn nhiệm vụ ở đầu trang áp dụng cho ba loại điều khiển được hỗ trợ cho mục nhập thời gian: điều khiển mục nhập thời gian hàng tuần, điều khiển chỉ đọc và điều khiển lịch.

### <a name="dimensions"></a>Thông số
Phần **Thông số** hiển thị, như tiêu đề cột, tất cả các thông số có thể nhập được thời gian vào đó. Các thông số sau đây được hỗ trợ ngay lập tức:

- Dự án
- Nhiệm vụ Dự án
- Vai trò
- Loại
- Trạng thái mục nhập

Phần **Thông số** không cho phép chỉnh sửa nội tuyến. Phần này được hỗ trợ bởi một dạng xem cho phép thêm các trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần. Để biết thông tin về cách thêm trường tùy chỉnh, hãy xem phần "Khả năng mở rộng" sau trong chủ đề này.

### <a name="duration"></a>Khoảng thời gian
Phần Thời gian hiển thị các ngày trong tuần dưới dạng tiêu đề cột. Phần này cho phép chỉnh sửa nội tuyến. Sau khi hàng mục nhập thời gian được tạo có các thông số phù hợp, người dùng có thể nhanh chóng nhập nội tuyến khoảng thời gian mà họ đã dành cho các thông số đó.

## <a name="create-a-new-time-entry"></a>Tạo mục nhập thời gian mới
Để tạo một mục nhập thời gian mới trong lưới mục nhập thời gian, hãy chọn **Mới**. Hộp thoại **Tạo nhanh mục nhập thời gian** xuất hiện. Trong hộp thoại này, người dùng có thể chọn ngày nhập thời gian, sau đó nhập dữ liệu cho các thông số **Dự án**, **nhiệm vụ dự án**, **Vai trò** và **Khoảng thời gian** theo phút, giờ hoặc ngày bằng cách nhập **gi**, **ph** hoặc **ng**, cùng với số. Người dùng cũng có thể nhập mô tả và nhận xét có thể được chia sẻ bên ngoài cho mục nhập thời gian. Khi người dùng lưu các thay đổi, giá trị mà họ đã nhập vào các thông số sẽ xuất hiện trong phần **Thông số**. Thông tin khoảng thời gian mà họ đã nhập trong trường **Khoảng thời gian** sẽ xuất hiện vào ngày tạo mục nhập thời gian.

Trường tìm kiếm được các dạng xem hệ thống hỗ trợ. Ví dụ: sau khi người dùng nhập một dự án, trường **nhiệm vụ dự án** được đặt thành dạng xem **Sao chép** theo mặc định. Để tạo mục nhập thời gian cho các nhiệm vụ không được gán cho người dùng, hãy chọn **Thay đổi dạng xem** trong hộp thoại tra cứu, sau đó chọn dạng xem **Tất cả nhiệm vụ dự án đang hoạt động**.

## <a name="edit-a-time-entry"></a>Chinh sửa mục nhập thời gian
Thông tin chi tiết từ một số nguồn trên trang mục nhập thời gian, chẳng hạn như **Mô tả** và **Nhận xét bên ngoài**, không được hiển thị trong lưới mục nhập thời gian hàng tuần. Thay vào đó, một chỉ báo hình tham giác nhỏ sẽ xuất hiện trong các ô khoảng thời gian có thông tin chi tiết bổ sung. Chọn ô, sau đó chọn **Chỉnh sửa chi tiết** để xem dữ liệu trong ngăn **Chỉnh sửa nhanh**. Để chỉnh sửa hoặc cập nhật chi tiết cho một mục nhập thời gian cụ thể không thuộc lưới mục nhập thời gian hàng tuần, người dùng phải mở ngăn **Chỉnh sửa nhanh**.

## <a name="copy-a-time-entry-row"></a>Sao chép hàng mục nhập thời gian
Sau khi hàng mục nhập lần đầu tiên đã được tạo, người dùng có thể chọn **Sao chép hàng** để sao chép toàn bộ hàng vào một hàng mới. Khi một hàng được sao chép theo cách này, các thông số và khoảng thời gian cũng được sao chép. Người dùng cũng có thể chọn **Chỉnh sửa hàng** để cập nhật các giá trị thông số và khoảng thời gian nội tuyến trong phần **Khoảng thời gian**.

## <a name="open-a-time-entry"></a>Mở một mục nhập thời gian
Để hỗ trợ mục nhập tối ưu và nhanh chóng trong các trường nổi bật nhất, lưới mục nhập thời gian hàng tuần hiển thị tập hợp con của các thông số và khoảng thời gian đã chọn. Để xem tất cả thông tin chi tiết của một mục nhập thời gian, trong mục **Chỉnh sửa mục nhập**, hãy chọn **Mở**.

## <a name="submit-a-time-entry"></a>Gửi một mục nhập thời gian
Người dùng có thể gửi một mục nhập thời gian duy nhất hoặc một nhóm mục nhập thời gian bằng cách chọn một khối ô hoặc toàn bộ hàng mục nhập thời gian rồi chọn **Gửi**. Các mục nhập thời gian đã gửi xuất hiện dưới dạng các mục nhập đang chờ phê duyệt trên trang **Phê duyệt** của người phê duyệt. Không thể chỉnh sửa các mục nhập thời gian sau khi đã gửi thành công.

## <a name="recall-a-time-entry"></a>Lấy lại mục nhập thời gian
Bạn có thể lấy lại các mục nhập thời gian mà mình đã gửi. Bạn có thể lấy lại một mục nhập thời gian duy nhất, một khối mục nhập thời gian hoặc toàn bộ hàng mục nhập thời gian. Các mục nhập thời gian được lấy lại có sẵn cho các nguồn lực để chỉnh sửa.

## <a name="time-entry-status"></a>Trạng thái mục nhập thời gian
Các mục nhập thời gian mới được tự động gán trạng thái **Bản nháp**. Khi một mục nhập thời gian được gửi, trạng thái sẽ được cập nhật thành **Đã gửi**. Khi một mục nhập thời gian đã gửi được phê duyệt, trạng thái sẽ được cập nhật thành **Đã phê duyệt**. Nếu một mục nhập thời gian bị từ chối, trạng thái sẽ được cập nhật thành **Đã trả về** và mục nhập này sẽ có sẵn để sửa chữa và gửi lại. Chỉ có thể xóa các mục nhập thời gian có trạng thái **Bản nháp**.

## <a name="view-rejection-comments"></a>Xem các nhận xét từ chối
Khi người phê duyệt từ chối một mục nhập thời gian, họ có thể thêm nhận xét từ chối để nguồn lực hiểu được lý do từ chối. Để xem các nhận xét từ chối cho một mục nhập thời gian, hãy chọn **Mở mục nhập**. Nhận xét từ chối sẽ được hiển thị trong tiến trình thời gian. Trong tiến trình thời gian, nguồn lực có thể phản hồi các nhận xét từ chối trước khi gửi lại mục nhập.

## <a name="copy-week"></a>Sao chép tuần
Sau khi một vài mục nhập thời gian được tạo, người dùng có thể chọn **Sao chép tuần** để tạo hàng loạt các mục nhập thời gian bổ sung. Hộp thoại **Sao chép** sẽ xuất hiện. Trong phần **Từ khoảng thời gian**, hãy sử dụng các trường **Ngày bắt đầu** và **Ngày kết thúc** để xác định phạm vi ngày sẽ sao chép mục nhập thời gian từ đó. Trong phần **Tới khoảng thời gian**, trong trường **Ngày bắt đầu**, hãy chỉ định ngày để tạo mục nhập thời gian. Sau đó chọn **Sao chép**. Đối với ngày đã chỉ định trong khoảng thời gian "tới", một bản sao của các mục nhập thời gian cho ngày tương ứng trong tuần trong khoảng thời gian "từ" sẽ được tạo ra. Ví dụ: mục nhập thời gian của thứ Hai tuần trước được sao chép vào thứ Hai của tuần được chỉ định là khoảng thời gian "tới".

## <a name="import"></a>Nhập
Quá trình cơ bản tương tự được dùng để nhập từ các thông tin đặt trước, nội dung chỉ định và thông tin trao đổi. Người dùng có thể chỉ định phạm vi ngay nhập thông tin đặt trước. Sau đó, họ phải chọn rõ ràng các thông tin đặt trước sẽ được sao chép vào mục nhập thời gian nháp. Trong bản phát hành trước, mục nhập thời gian gợi ý xuất hiện trong lưới và lịch, đồng thời mất khi phiên được làm mới.

## <a name="extensibility"></a>Khả năng mở rộng
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Thêm các trường tùy chỉnh có mục tra cứu cho thực thể khác
Có 3 bước chính để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần.

1.  Thêm trường tùy chỉnh vào hộp thoại tạo nhanh.
2.  Cấu hình lưới để hiển thị trường tùy chỉnh.
3.  Thêm trường tùy chỉnh vào hàng chỉnh sửa dòng nhiệm vụ hoặc ô chỉnh sửa dòng nhiệm vụ, nếu thích hợp.

Ngoài ra, bạn phải đảm bảo rằng trường mới có các xác thực bắt buộc trong hàng hoặc ô chỉnh sửa luồng nhiệm vụ. Trong bước này, bạn phải khóa trường, theo trạng thái mục nhập thời gian.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Thêm trường tùy chỉnh vào hộp thoại tạo nhanh
Bạn phải thêm trường tùy chỉnh vào hộp thoại Tạo nhanh mục nhập thời gian. để người dùng có thể nhập một giá trị cho trường này khi họ thêm mục nhập thời gian bằng cách sử dụng nút **Mới**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Cấu hình lưới để hiển thị trường tùy chỉnh
Có 2 cách để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần. Lựa chọn đầu tiên là tùy chỉnh dạng xem **Mục nhập thời gian hàng ngày của tôi** và thêm trường tùy chỉnh vào đó. Bạn có thể chọn vị trí và kích thước của trường tùy chỉnh trong lưới bằng cách chỉnh sửa các thuộc tính đó trong dạng xem.

Lựa chọn thứ hai là tạo dạng xem mục nhập thời gian tùy chỉnh và đặt làm dạng xem mặc định. dạng xem này sẽ chứa các trường **Mô tả** và **Nhận xét bên ngoài**, ngoài các cột mà bạn muốn có trong lưới. Bạn có thể chọn vị trí, kích thước và thứ tự sắp xếp mặc định cho lưới bằng cách chỉnh sửa các thuộc tính đó trong dạng xem. Tiếp theo, cấu hình bộ kiểm soát tùy chỉnh cho dạng xem này để trở thành bộ kiểm soát **Lưới mục nhập thời gian**. Thêm bộ kiểm soát này vào dạng xem và chọn cho web, điện thoại và máy tính bảng. Tiếp theo, cấu hình các thông số cho lưới mục nhập thời gian hàng tuần. Đặt trường **Ngày bắt đầu** thành **msdyn_date**, đặt trường **Khoảng thời gian** thành **msdyn_duration** và đặt trường **Trạng thái** thành **msdyn_entrystatus**. Đối với dạng xem mặc định, trường **Danh sách trạng thái chỉ đọc** được đặt thành **192350002,192350003,192350004**, trường **Luồng nhiệm vụ chỉnh sửa hàng** được đặt thành **msdyn_timeentryrowedit** và trường **Luồng nhiệm vụ chỉnh sửa ô** được đặt thành **msdyn_timeentryedit**. Bạn có thể tùy chỉnh các trường này để thêm hoặc xóa trạng thái chỉ đọc hoặc sử dụng trải nghiệm dựa trên nhiệm vụ khác (TBX) để chỉnh sửa hàng hoặc ô editing. Các trường này sẽ bị ràng buộc với giá trị tĩnh.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Thêm trường tùy chỉnh vào luồng nhiệm vụ chỉnh sửa thích hợp
Có thể tìm thấy trang TBX được dùng để chỉnh sửa trong phần **Quy trình**. Trang mặc định là **Project Service - Chỉnh sửa hàng mục nhập thời gian** và **Project Service - Chỉnh sửa mục nhập thời gian**. Bạn có thể chỉnh sửa những trang mặc định này hoặc tạo trang TBX tùy chỉnh mới.

> [!NOTE] 
> Cả hai tùy chọn đều loại bỏ một số tính năng lọc sẵn cho các thực thể **Dự án** và **nhiệm vụ dự án**, từ đó tất cả dạng xem tra cứu cho các thực thể này đều hiển thị. Ban đầu, chỉ có dạng xem tra cứu phù hợp mới hiển thị.

Bạn phải xác định luồng nhiệm vụ phù hợp cho trường tùy chỉnh. Nhiều khả năng, nếu bạn đã thêm trường vào lưới, trường đó sẽ chuyển vào luồng nhiệm vụ chỉnh sửa hàng được dùng cho các trường áp dụng cho toàn bộ hàng mục nhập thời gian. Nếu trường tùy chỉnh có giá trị duy nhất mỗi ngày, chẳng hạn như trường tùy chỉnh cho **Thời gian kết thúc**, thì trường đó sẽ chuyển vào luồng nhiệm vụ chỉnh sửa ô.

Để thêm trường tùy chỉnh vào một luồng nhiệm vụ, hãy kéo thành phần **Trường** vào vị trí thích hợp trên trang, sau đó đặt thuộc tính cho trường đó. Đặt thuộc tính **Nguồn** thành **Mục nhập thời gian** và đặt thuộc tính **Trường dữ liệu** thành trường tùy chỉnh. Thuộc tính **Trường** chỉ định tên hiển thị trên trang TBX. Chọn **Áp dụng** để lưu các thay đổi với trường. Sau đó chọn **Cập nhật** để lưu các thay đổi với trường.

Để sử dụng trang TBX tùy chỉnh mới, hãy tạo một quy trình mới. Đặt danh mục thành **Luồng quy trình công việc**, đặt thực thể thành **Mục nhập thời gian** và đặt loại quy trình công việc thành **Chạy quy trình dưới dạng luồng nhiệm vụ**. Trong phần **Thuộc tính**, phải đặt thuộc tính **Tên trang** thành tên hiển thị cho trang. Thêm tất cả các trường liên quan vào trang TBX. Lưu và kích hoạt quy trình, sau đó cập nhật thuộc tính kiểm soát tùy chỉnh cho luồng nhiệm vụ liên quan thành giá trị **Tên** trên quy trình.

### <a name="add-new-option-set-values"></a>Thêm các giá trị bộ tùy chọn mới
Để thêm các giá trị bộ tùy chọn vào một trường sẵn có, hãy mở trang chỉnh sửa cho trường đó, sau đó trong **Loại**, hãy chọn **Chỉnh sửa** bên cạnh bộ tùy chọn. Tiếp theo, thêm tùy chọn mới có nhãn và màu tùy chỉnh. Nếu bạn muốn thêm trạng thái mục nhập thời gian mới, thì trường ban đầu phải được đặt tên là **Trạng thái mục nhập** chứ không phải là **Trạng thái**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Chỉ định trạng thái mục nhập thời gian mới là chỉ đọc
Để chỉ định trạng thái mục nhập thời gian mới thành chỉ đọc, hãy thêm giá trị mục nhập thời gian mới (số chứ không phải nhãn) vào thuộc tính **Danh sách trạng thái chỉ đọc**. Phần có thể chỉnh sửa của lưới mục nhập thời gian sẽ bị khóa cho các hàng có trạng thái mới.
Tiếp theo, hãy thêm các quy tắc công việc để khóa tất cả các trường trên trang TBX **Chỉnh sửa hàng mục nhập thời gian** và **Chỉnh sửa mục nhập thời gian**. Bạn có thể truy cập các quy tắc công việc cho những trang này bằng cách mở công cụ biên tập dòng quy trình công việc cho trang rồi chọn **Quy tắc công việcBusiness Rules**. Sau đó, bạn có thể thêm trạng thái mới vào điều kiện trong các quy tắc kinh doanh hiện có hoặc có thể thêm quy tắc công việc mới cho trạng thái mới.

### <a name="add-custom-validation-rules"></a>Thêm quy tắc xác thực tùy chỉnh
Có 2 loại quy tắc xác thực mà bạn có thể thêm cho trải nghiệm lưới mục nhập thời gian hàng tuần: •   Quy tắc công việc phía khách hàng hoạt động trong các hộp thoại tạo nhanh và trên trang TBX •   Quy tắc xác thực phía máy chủ áp dụng cho tất cả các nội dung cập nhật mục nhập thời gian

#### <a name="business-rules"></a>Quy tắc kinh doanh
Sử dụng quy tắc công việc để khóa và mở khóa các trường, nhập giá trị mặc định vào trường và xác định các quy tắc xác thực chỉ yêu cầu thông tin từ bản ghi mục nhập thời gian hiện tại. Bạn có thể truy cập các quy tắc công việc cho trang TBX bằng cách mở công cụ biên tập dòng quy trình công việc cho trang rồi chọn **Quy tắc công việc**. Sau đó, bạn có thể chỉnh sửa quy tắc công việc hiện có hoặc thêm quy tắc kinh doanh mới. Để có các quy tắc xác thực mang tính tùy chỉnh hơn, bạn có thể sử dụng quy tắc công việc để chạy JavaScript.

#### <a name="plug-in-validations"></a>Xác thực bổ trợ
Bạn nên sử dụng các quy tắc xác thực bổ trợ đối với mọi quá trình xác thực yêu cầu nhiều ngữ cảnh hơn ngữ cảnh có sẵn trong một bản ghi mục nhập thời gian, hoặc bất kỳ quá trình xác thực nào mà bạn muốn chạy trên các bản cập nhật nội tuyến trong lưới. Để hoàn tất quy trình xác thực, hãy tạo một phần bổ trợ trên thực thể **Mục nhập thời gian**.

> [!IMPORTANT] 
> Hiện tại, một sự cố đã biết trên trang TBX ngăn người dùng điều chỉnh thông tin và chọn lại Xong khi bản cập nhật không xác nhận được phần bổ trợ. Để khắc phục, hãy thiết lập các quy tắc xác thực quy tắc công việc để ngăn chặn tình huống này nhiều nhất có thể.


[!INCLUDE[footer-include](../includes/footer-banner.md)]