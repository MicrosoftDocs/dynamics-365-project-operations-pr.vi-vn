---
title: Ứng dụng Chi phí dành cho thiết bị di động
description: Chủ đề này cung cấp thông tin về Không gian làm việc di động Quản lý chi phí.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2cbce8fbfa622a143f3ebfc34d7d60a7da4a9171
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950912"
---
# <a name="mobile-expense-app"></a>Ứng dụng Chi phí dành cho thiết bị di động

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này cung cấp thông tin về Không gian làm việc di động **Quản lý chi phí**. Không gian làm việc này cho phép người dùng chụp và tải lên biên lai để họ có thể đính kèm biên lai đó vào báo cáo chi phí sau này. Người dùng cũng có thể nhanh chóng tạo dòng chi phí bằng cách sử dụng biên lai đính kèm, đồng thời tạo và quản lý các báo cáo chi phí của họ. Ngoài ra, những người phê duyệt có thể sử dụng không gian làm việc di động **Quản lý chi phí** để xem các báo cáo chi phí được gán cho họ, và phê duyệt hoặc từ chối các báo cáo chi phí đó.

Không gian làm việc di động này được thiết kế để sử dụng với ứng dụng di động Dynamics 365 Unified Ops.

Nhiều tổ chức yêu cầu đính kèm bản sao biên lai với báo cáo chi phí liên quan đến đi lại hoặc liên quan đến kinh doanh do nhân viên nộp để được hoàn lại chi phí. Không gian làm việc di động **Quản lý chi phí** cho phép người dùng tạo các dòng chi phí mới một cách nhanh chóng trên thiết bị di động mà họ lựa chọn bằng cách sử dụng ảnh biên lai đính kèm. Ngoài ra, người dùng có thể chụp ảnh biên lai rồi đính kèm nó vào báo cáo chi phí. Nhân viên cũng có thể tạo và quản lý báo cáo chi phí của mình, sau đó gửi chúng để được duyệt và hoàn trả chi phí bằng cách sử dụng thiết bị di động.

Cụ thể là, không gian làm việc di động **Quản lý chi phí** cho phép người dùng thực hiện các tác vụ sau:

- Chụp ảnh biên lai. Tải ảnh biên lai lên và đính kèm vào báo cáo chi phí sau này.
- Tải lên tệp dưới dạng ảnh biên lai. Bạn có thể đính kèm tệp đó vào báo cáo chi phí sau này.
- Tạo một dòng chi phí mới bằng cách sử dụng biên lai đính kèm. Sau đó bạn có thể thêm hạng mục dòng vào báo cáo chi phí sau này và gửi nó để được duyệt và hoàn trả chi phí.

Bạn cũng có thể sử dụng các tính năng sau:

- Tạo một báo cáo chi phí mới.
- Đính kèm các giao dịch thẻ tín dụng và các chi phí khác đã tạo trước đó vào báo cáo chi phí.
- Tạo các chi phí mới cho một báo cáo chi phí.
- Đính kèm biên lai vào bất kỳ khoản chi phí nào cho báo cáo chi phí, bằng cách chụp ảnh biên lai hoặc bằng cách tải lên một tệp dưới dạng ảnh biên lai.
- Tùy thuộc vào chính sách chi phí của công ty, hãy thêm danh sách khách hàng vào một chi phí.
- Tùy thuộc vào chính sách chi phí của công ty, hãy phân chia các chi phí.
- Gửi báo cáo chi phí để được duyệt và hoàn trả chi phí.
- Phê duyệt hoặc từ chối các báo cáo chi phí mà bạn là người phê duyệt được chỉ định.

## <a name="prerequisites"></a>Điều kiện tiên quyết
Các điều kiện tiên quyết khác nhau, dựa trên phiên bản đã được triển khai cho tổ chức của bạn.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Điều kiện tiên quyết nếu bạn sử dụng Dynamics 365 Finance 
Nếu Finance đã được triển khai cho tổ chức của bạn thì quản trị viên hệ thống phải phát hành không gian làm việc di động **Quản lý chi phí**. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Các điều kiện tiên quyết nếu bạn sử dụng phiên bản 1611 với bản cập nhật nền tảng từ 3 trở đi
Nếu phiên bản 1611 với bản cập nhật nền tảng từ 3 trở đi đã được triển khai cho tổ chức của bạn thì quản trị viên hệ thống phải hoàn thành các điều kiện tiên quyết sau. 

<table>
<thead>
<tr class="header">
<th>Điều kiện tiên quyết</th>
<th>Vai trò</th>
<th>Nội dung mô tả</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Triển khai KB 4019015.</td>
<td>Quản trị viên hệ thống</td>
<td>KB 4019015 là bản cập nhật X++ hoặc bản vá lỗi siêu dữ liệu có chứa không gian làm việc di động <strong>Quản lý thời gian</strong>. Để triển khai KB 4019015, quản trị viên hệ thống của bạn phải làm theo các bước sau.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Tải xuống các bản cập nhật từ Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Cài đặt bản sửa lỗi siêu dữ liệu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Tạo một gói có thể triển khai</a> chứa mô hình <strong>ApplicationSuite</strong> và <strong>ExpenseMobile</strong>, sau đó tải gói có thể triển khai lên LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Áp dụng gói có thể triển khai</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Phát hành không gian làm việc di động <strong>Quản lý chi phí</strong>.</td>
<td>Quản trị viên hệ thống</td>
<td>Xem <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Phát hành không gian làm việc di động</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Tải xuống và cài đặt ứng dụng di động Dynamics 365 Unified Ops
Tải xuống và cài đặt ứng dụng di động Dynamics 365 Unified Ops:

- [Đối với điện thoại Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Đối với iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Đăng nhập vào ứng dụng dành cho thiết bị di động
1. Khởi động ứng dụng trên thiết bị di động của bạn.
2. Nhập URL Dynamics 365.
4. Lần đầu tiên đăng nhập, bạn sẽ được nhắc nhập tên người dùng và mật khẩu của mình. Nhập thông tin xác thực của bạn.
5. Sau khi bạn đăng nhập, không gian làm việc có sẵn cho công ty của bạn sẽ được hiển thị. Nếu quản trị viên hệ thống của bạn phát hành không gian làm việc mới sau đó thì bạn sẽ phải làm mới danh sách không gian làm việc di động.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Chụp ảnh biên lai bằng cách sử dụng không gian làm việc di động Quản lý chi phí

1. Trên thiết bị di động của bạn, hãy mở không gian làm việc **Quản lý chi phí**.
2. Chọn **Chụp biên lai**.
3. Chọn **Chụp ảnh** hoặc **Chọn hình ảnh**.
4. Làm theo một trong các bước sau:

   - Nếu bạn đã chọn **Chụp ảnh**, hãy làm theo các bước sau:

      1. Bạn được đưa đến máy ảnh trên thiết bị di động của mình để bạn có thể chụp ảnh biên lai. 
      2. Khi bạn chụp ảnh xong, hãy chọn **OK** để chấp nhận bức ảnh.
      3. Tùy chọn: Nhập tên cho bức ảnh và nhập bất kỳ ghi chú nào.

    - Nếu bạn đã chọn **Chọn hình ảnh**, hãy làm theo các bước sau:

        1. Chọn một hình ảnh trong danh sách.
        2. Tùy chọn: Nhập tên cho hình ảnh và nhập bất kỳ ghi chú nào.

5. Chọn **Xong**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Nhập chi phí một cách nhanh chóng bằng cách sử dụng không gian làm việc di động Quản lý chi phí

1. Trên thiết bị di động của bạn, hãy mở không gian làm việc **Quản lý chi phí**.
2. Chọn **Nhập chi phí nhanh chóng**.
3. Chọn thể loại chi phí. Bạn xem danh sách các thể loại chi phí được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu thể loại của bạn không có trong danh sách, hãy chọn **tìm kiếm trực tuyến**. Tìm kiếm theo thể loại chi phí hoặc chuyển sang tìm kiếm theo loại chi phí.
4. Nhập ngày giao dịch của chi phí.
5. Tùy chọn: Nhập người bán về chi phí.
6. Nhập khoản chi phí.
7. Chọn đơn vị tiền tệ của chi phí. Bạn xem danh sách các mã tiền tệ được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 400 đơn vị tiền tệ được tải lên nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu đơn vị tiền tệ của bạn không có trong danh sách, hãy chọn **Tìm kiếm** để tìm kiếm trực tuyến. Tìm kiếm theo đơn vị tiền tệ hoặc chuyển sang tìm kiếm theo tên.
8. Chọn **Chụp ảnh** hoặc **Chọn hình ảnh**.
9. Làm theo một trong các bước sau:

    - Nếu bạn đã chọn **Chụp ảnh** thì bạn được đưa đến máy ảnh trên thiết bị di động để bạn có thể chụp ảnh biên lai. Khi bạn chụp ảnh xong, hãy chọn **OK** để chấp nhận bức ảnh.
    - Nếu bạn đã chọn **Chọn hình ảnh**, hãy chọn một hình ảnh trong danh sách.

10. Chọn **Xong**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Phê duyệt báo cáo chi phí bằng cách sử dụng không gian làm việc di động Quản lý chi phí (nếu bạn sử dụng bản cập nhật vào tháng 7 năm 2017)

1. Trên thiết bị di động của bạn, hãy mở không gian làm việc **Quản lý chi phí**.
2. **Phê duyệt chi phí** hiển thị số lượng báo cáo chi phí được chỉ định cho bạn để phê duyệt. Số lượng được cập nhật khoảng 30 phút một lần. Chọn **Phê duyệt chi phí**.

    Danh sách báo cáo chi phí mà bạn được chỉ định phê duyệt hiển thị.
    
3. Chọn một báo cáo chi phí để xem chi tiết chi phí của báo cáo.
4. Chọn một chi phí để xem chi tiết. Thông tin được hiển thị cho một chi phí bao gồm bất kỳ chi tiết về biên lai, khách hàng và từng khoản.
5. Quay lại trang **Báo cáo chi phí**, chọn để phê duyệt hoặc từ chối báo cáo chi phí.
6. Nhập bất kỳ nhận xét nào cho hành động phê duyệt.
7. Chọn **Xong**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Tạo một báo cáo chi phí mới và nộp báo cáo để phê duyệt bằng cách sử dụng không gian làm việc di động Quản lý chi phí (nếu bạn sử dụng bản cập nhật vào tháng 7 năm 2017)

1. Trên thiết bị di động của bạn, hãy mở không gian làm việc **Quản lý chi phí**.
2. Chọn **Nhập chi phí**.
3. Chọn **Báo cáo mới** hoặc chọn một báo cáo chi phí hiện có trong danh sách.
4. Đối với các báo cáo chi phí mới, hãy nhập mục đích và bất kỳ thông tin bổ sung nào có sẵn. Thông tin này khác nhau, tùy thuộc vào cách định cấu hình quản lý chi phí cho công ty của bạn.
5. Chọn **Xong**.
6. Để thêm các chi phí hiện có, chẳng hạn như giao dịch thẻ tín dụng, vào báo cáo chi phí, hãy chọn **Đính kèm**.
7. Chọn một hoặc nhiều chi phí trong danh sách.
8. Chọn **Xong**.
9. Để thêm một chi phí mới vào báo cáo chi phí, hãy chọn **Chi phí mới**.
10. Chọn thể loại chi phí. Bạn xem danh sách các thể loại chi phí được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu thể loại của bạn không có trong danh sách, hãy chọn **tìm kiếm trực tuyến**. Tìm kiếm theo thể loại chi phí hoặc chuyển sang tìm kiếm theo loại chi phí.
11. Tùy chọn: Nhập người bán về chi phí.
12. Nhập ngày giao dịch của chi phí.
13. Nhập khoản chi phí.
14. Chọn đơn vị tiền tệ của chi phí. Bạn xem danh sách các mã tiền tệ được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 400 đơn vị tiền tệ được tải lên nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu đơn vị tiền tệ của bạn không có trong danh sách, hãy chọn **Tìm kiếm** để tìm kiếm trực tuyến. Tìm kiếm theo đơn vị tiền tệ hoặc chuyển sang tìm kiếm theo tên.
15. Chọn **Xong**.
16. Để thêm các chi tiết khác vào chi phí, hãy chọn **Thêm chi tiết khác**. Các trường có sẵn phụ thuộc vào cài đặt định cấu hình quản lý chi phí cho công ty của bạn.
17. Nếu chính sách của công ty yêu cầu biên lai cho chi phí, hãy chọn **Biên lai** rồi sau đó làm theo các bước sau:

    1. Chọn **Chụp biên lai** hoặc **Đính kèm biên lai**.
    2. Làm theo một trong các bước sau:

        - Nếu bạn đã chọn **Chụp biên lai** thì hãy làm theo các bước sau:

            1. Chọn **Chụp ảnh** hoặc **Chọn hình ảnh**.
            2. Làm theo một trong các bước sau:

                - Nếu bạn đã chọn **Chụp ảnh**, hãy làm theo các bước sau:

                    1. Bạn được đưa đến máy ảnh trên thiết bị di động của mình để bạn có thể chụp ảnh biên lai. Khi bạn chụp ảnh xong, hãy chọn **OK** để chấp nhận bức ảnh.
                    2. Tùy chọn: Nhập tên cho bức ảnh và nhập bất kỳ ghi chú nào.

                - Nếu bạn đã chọn **Chọn hình ảnh**, hãy làm theo các bước sau:

                    1. Chọn một hình ảnh trong danh sách.
                    2. Tùy chọn: Nhập tên cho hình ảnh và nhập bất kỳ ghi chú nào.

            3.  Chọn **Xong**.

        - Nếu bạn đã chọn **Đính kèm biên lai** thì hãy làm theo các bước sau:

            1.  Chọn một hoặc nhiều hình ảnh trong danh sách.
            2.  Chọn **Xong**.

    3. Chọn nút **Quay lại** để quay lại phần chi tiết chi phí.

18. Nếu chính sách của công ty yêu cầu khách hàng sở hữu chi phí, hãy chọn **Biên lai** rồi sau đó làm theo các bước sau:

    1. Chọn **Khách hàng**, **Khách hàng trước đây**, hoặc **Đồng nghiệp**.
    2. Làm theo một trong các bước sau:

        - Nếu bạn đã chọn **Khách hàng**, hãy làm theo các bước sau:

            1. Nhập tên của khách hàng.
            2. Tùy chọn: Nhập tổ chức và / hoặc quốc gia của khách.
            3. Tùy chọn: Nhập chức vụ của khách hàng.
            4. Chọn **Xong**.

        - Nếu bạn đã chọn **Khách hàng trước đây** thì hãy làm theo các bước sau:

            1. Chọn một hoặc nhiều khách hàng trước đây trong danh sách. Bạn sẽ thấy danh sách những khách trước đây mà bạn đã thêm vào báo cáo chi phí trước đó đã được tải vào ứng dụng của bạn để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu khách hàng trước đây của bạn không có trong danh sách, hãy chọn **Tìm kiếm** để tìm kiếm trực tuyến. Tìm kiếm theo tên hoặc chuyển sang tìm kiếm theo tổ chức, quốc gia hoặc chức vụ.
            2. Chọn **Xong**.

        - Nếu bạn đã chọn **Đồng nghiệp**, hãy làm theo các bước sau:

            1. Chọn một hoặc nhiều đồng nghiệp trong danh sách. Bạn nhìn thấy danh sách đồng nghiệp được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu đồng nghiệp của bạn không có trong danh sách, hãy chọn **Tìm kiếm** để tìm kiếm trực tuyến. Tìm kiếm theo tên hoặc chuyển sang tìm kiếm theo công ty hoặc chức vụ.
            2. Chọn **Xong**.

    3. Chọn nút **Quay lại** để quay lại phần chi tiết chi phí.

19. Nếu chính sách của công ty yêu cầu bạn phải ghi từng khoản chi phí thì hãy chọn **Ghi thành từng khoản** rồi sau đó làm theo các bước sau:

    1. Chọn ngày đầu tiên để ghi lại từng khoản.
    2. Chọn **Thêm thông tin ghi lại từng khoản**.
    3. Chọn thể loại nhỏ để ghi lại từng khoản chi phí. Bạn nhìn thấy danh sách các thể loại phụ của chi phí được tải vào ứng dụng để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, nhà phát triển xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Nếu thể loại phụ của bạn không có trong danh sách, hãy chọn **Tìm kiếm** để tìm kiếm trực tuyến. Tìm kiếm theo tên thể loại phụ của chi phí.
    4. Nhập số tiền giao dịch cho từng khoản mục.
    5. Chỉnh sửa ngày giao dịch nếu được yêu cầu.
    6. Chọn **Xong**.
    7. Lặp lại các bước trước đó cho đến khi bạn thêm xong tất cả các hành động ghi thành từng khoản cho ngày đã chọn.
    8. Đối với những ngày bổ sung, bạn có thể chọn **Sao chép sang ngày tiếp theo** để sao chép các thông tin ghi thành từng khoản sang ngày tiếp theo. Ngoài ra, bạn có thể chọn ngày để ghi thành từng khoản và sau đó thêm các thông tin ghi thành từng khoản như bạn đã làm cho ngày đầu tiên.
    9. Sau khi bạn ghi xong từng khoản cho chi phí, hãy chọn nút **Quay lại** để quay lại chi tiết chi phí.

20. Chọn nút **Quay lại** để quay lại trang **Báo cáo chi phí** .
21. Lặp lại các bước trước đó cho đến khi bạn thêm xong mọi chi phí.
22. Chọn **Gửi**.
23. Nhập bất kỳ nhận xét nào dành cho người phê duyệt.
24. Chọn **Xong**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]