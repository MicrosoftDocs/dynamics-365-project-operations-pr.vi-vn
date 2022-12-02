---
title: Đặt cấu hình hoạt động kế toán cho dự án có thể tính phí
description: Bài viết này cung cấp thông tin về các tùy chọn kế toán cho những dự án có thể lập hóa đơn.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5020c978f0667543aed2b373d262dcda9688b02c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916452"
---
# <a name="configure-accounting-for-billable-projects"></a>Đặt cấu hình hoạt động kế toán cho dự án có thể tính phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ các lựa chọn kế toán khác nhau cho các dự án có thể lập hóa đơn, bao gồm cả các dự án theo giá cố định và theo thời gian và vật tư.

- **Giao dịch thời gian và vật tư**: Những giao dịch này được lập hóa đơn theo tiến độ công việc dựa trên mức sử dụng giờ, chi phí, mặt hàng hoặc phí trên dự án. Các chi phí giao dịch này có thể được khớp với doanh thu trên mỗi giao dịch và dự án được lập hóa đơn theo tiến độ công việc. Doanh thu dự án cũng có thể được tích lũy tại thời điểm diễn ra giao dịch. Trong quá trình lập hóa đơn, doanh thu được ghi nhận và nếu có, doanh thu tích lũy sẽ được đảo ngược.
- **Giao dịch giá cố định**: Những giao dịch này được lập hóa đơn theo lịch trình thanh toán dựa trên hợp đồng dự án. Doanh thu cho các giao dịch giá cố định có thể được ghi nhận khi lập hóa đơn hoặc được tính toán và đăng tải định kỳ, theo phương pháp **Hợp đồng đã hoàn thành** hoặc **Phần trăm hoàn thành**.

Một dự án được coi là có thể lập hóa đơn khi được liên kết với một hoặc nhiều mô tả hợp đồng. Mô tả hợp đồng dự án tự xác định phương thức thanh toán và loại giao dịch nào được phép.

Ví dụ: Fabrikam Robotics đã giành được hợp đồng dự án với tập đoàn Adatum để tối ưu hóa thiết bị. Adatum sẽ trả một số tiền cố định là 10.000 USD để trang trải các chi phí phát sinh của dự án. Đây là phương thức thanh toán giá cố định. Thời gian và phí dự án sẽ được lập hóa đơn cho mỗi lần sử dụng. Đây là phương thức thanh toán theo thời gian và vật tư. Tất cả công việc sẽ được theo dõi trong một dự án duy nhất có tên là tối ưu hóa thiết bị Adatum.

Một thành viên trong nhóm dự án báo cáo 8 giờ làm việc cho dự án tối ưu hóa thiết bị Adatum. Khi người quản lý dự án phê duyệt thời gian này, hệ thống sẽ sử dụng phương thức thanh toán theo thời gian và vật tư để tạo các giao dịch thực tế, hóa đơn và tài khoản. Giao dịch này sẽ không được bao gồm trong tính toán ước tính doanh thu theo giá cố định.

Một thành viên khác của nhóm dự án gửi chi phí đi lại 2000 USD cho dự án tối ưu hóa thiết bị Adatum. Khi người quản lý dự án phê duyệt nội dung này, hệ thống sẽ sử dụng phương thức thanh toán giá cố định để tạo các giao dịch thực tế và tài khoản cho chi phí dự án này. Khách hàng sẽ không được lập hóa đơn dựa trên giao dịch này. Thay vào đó, khách hàng sẽ được lập hóa đơn bằng cách sử dụng các mốc thanh toán được định cấu hình riêng. Giao dịch chi phí này, cùng với ước tính chi phí, sẽ được bao gồm trong tính toán ước tính doanh thu theo giá cố định.

Nguyên tắc kế toán cho các giao dịch dự án được xác định trong hồ sơ chi phí và doanh thu của dự án. Đối với mọi giao dịch dự án, hệ thống xác định hồ sơ doanh thu và chi phí dự án phù hợp bằng cách sử dụng các quy tắc về chi phí dự án và hồ sơ doanh thu đã được định cấu hình.

## <a name="define-project-cost-and-revenue-profiles"></a>Xác định hồ sơ doanh thu và chi phí dự án 

Chi phí dự án và hồ sơ doanh thu xác định các quy tắc kế toán cho giao dịch dự án. Các hồ sơ này được định cấu hình trong Quản lý dự án và kế toán. 

Hoàn thành các bước sau để tạo hồ sơ doanh thu và chi phí dự án mới. 

1. Đi đến **Quản lý dự án và kế toán** > **Thiết lập** > **Đăng** > **Hồ sơ doanh thu và chi phí dự án**. 
2. Chọn **Mới** để tạo hồ sơ doanh thu và chi phí dự án mới.
3. Trong trường **Tên**, nhập tên và mô tả ngắn gọn về hồ sơ.
4. Trong trường **Phương thức thanh toán**, chọn **Thời gian và vật tư** hoặc **Giá cố định**.
5. Bung rộng FastTab **Sổ cái**. Các trường trên tab này xác định các nguyên tắc kế toán được sử dụng khi các giao dịch dự án được ghi sổ nhật ký kế toán bằng cách sử dụng bút toán tích hợp Project Operations, sau đó được lập hóa đơn thông qua Đề xuất hóa đơn dự án.
6. Chọn thông tin thích hợp trong các trường sau trên FastTab **Sổ cái**:

    - **Đăng chi phí – giờ**:

       - *Không có sổ cái*: Chi phí cho các giao dịch thời gian sẽ không được đăng lên Sổ cái khi bút toán tích hợp Project Operations được đăng. Tuy nhiên, kế toán có thể đăng chi phí bằng cách sử dụng chức năng Đăng chi phí sau đó.
       - **Số dư**: Chi phí cho giao dịch thời gian sẽ được ghi nợ vào loại tài khoản Sổ cái, *WIP - Giá trị chi phí* và ghi có vào *Tài khoản phân bổ bảng lương* trong quá trình thiết lập đăng Sổ cái. Kế toán sẽ sử dụng chức năng Đăng chi phí để chuyển chi phí này từ tài khoản Số dư sang tài khoản Lãi lỗ theo định kỳ.
       - **Lãi và lỗ**: Khi đăng bút toán tích hợp Project Operations, chi phí giao dịch thời gian sẽ được ghi nợ vào loại tài khoản Sổ cái *Chi phí* và ghi có vào *Tài khoản phân bổ bảng lương* được xác định trên tab **Chi phí** trên trang **Thiết lập đăng sổ cái** (**Kế toán và quản lý dự án** \> **Thiết lập** \> **Đăng** \> **Thiết lập đăng Sổ cái**). Đây là thiết lập phổ biến nhất cho các giao dịch thời gian và vật tư.
        - *Không bao giờ vào Sổ cái*: Chi phí cho các giao dịch theo thời gian sẽ không bao giờ được đăng lên Sổ cái.

    - **Đăng chi phí – chi phí**:

         - **Số dư**: Khi đăng bút toán tích hợp Project Operations, chi phí trong giao dịch chi phí sẽ được ghi nợ vào loại tài khoản Sổ cái *WIP - Giá trị chi phí* như được xác định trên tab **Chi phí** trên trang **Thiết lập đăng sổ cái** và được ghi có vào tài khoản bù trừ trên dòng nhật ký kế toán. Các tài khoản bù trừ mặc định cho chi phí được xác định trong **Kế toán và quản lý dự án** > **Thiết lập** \> **Đăng** \> **Tài khoản bù trừ mặc định cho chi phí**. Kế toán sẽ sử dụng chức năng **Đăng chi phí** để chuyển chi phí này từ tài khoản số dư sang tài khoản lãi lỗ theo định kỳ.
        - **Lãi và lỗ**: Khi đăng bút toán tích hợp Project Operations, chi phí trong giao dịch chi phí sẽ được ghi nợ vào loại tài khoản Sổ cái *Chi phí* như được xác định trên tab **Chi phí** trên trang **Thiết lập đăng sổ cái** và được ghi có vào tài khoản bù trừ trên dòng nhật ký kế toán. Các tài khoản bù trừ mặc định cho chi phí được xác định trong **Kế toán và quản lý dự án** \> **Thiết lập** \> **Đăng** \> **Tài khoản bù trừ mặc định cho chi phí**.
      
    - **Đăng chi phí - hạng mục**:

         - **Số dư**: Khi đăng nhật ký Tích hợp Project Operations, chi phí giao dịch hạng mục sẽ được ghi nợ vào loại tài khoản Sổ cái *WIP - Giá trị chi phí - hạng mục* như được định nghĩa trên tab **Chi phí** trên trang **Thiết lập đăng sổ cái** và ghi có vào phần sau:
    
              - Đối với trường hợp sử dụng loại tài liệu: Tài khoản **Chi phí - hạng mục** trên trang **Thiết lập đăng sổ cái**.  
              - Đối với trường hợp mua loại tài liệu: **Tài khoản tích hợp mua sắm** trên **Quản lý dự án và các thông số kế toán**.
           Kế toán sẽ sử dụng chức năng **Đăng chi phí** để chuyển chi phí này từ tài khoản số dư sang tài khoản lãi lỗ theo định kỳ.
        - **Lợi nhuận và thua lỗ**: Khi đăng nhật ký Tích hợp Project Operations, chi phí giao dịch hạng mục sẽ được ghi nợ vào loại tài khoản Sổ cái *WIP - Giá trị chi phí - hạng mục* như được định nghĩa trên tab **Chi phí** trên trang **Thiết lập đăng sổ cái** và ghi có vào phần sau:
         
             - Đối với trường hợp sử dụng loại tài liệu: Tài khoản **Chi phí - hạng mục** trên trang **Thiết lập đăng sổ cái**.  
             - Đối với trường hợp mua loại tài liệu: **Tài khoản tích hợp mua sắm** trên **Quản lý dự án và các thông số kế toán**.
       
    - **Lập hóa đơn trên tài khoản**:

        - **Số dư**: Khi đăng đề xuất hóa đơn dự án, giao dịch trên tài khoản (mốc thanh toán) sẽ được ghi có vào loại tài khoản Sổ cái *WIP đã lập hóa đơn - trên toàn khoản* như được xác định trên tab **Doanh thu** trên trang **Thiết lập đăng Sổ cái** và được ghi nợ vào tài khoản số dư của khách hàng.
         - **Lãi và lỗ**: Khi đăng đề xuất hóa đơn dự án, giao dịch trên tài khoản (mốc thanh toán) sẽ được ghi có vào loại tài khoản Sổ cái *Doanh thu đã lập hóa đơn - trên toàn khoản* như được xác định trên tab **Doanh thu** trên trang **Thiết lập đăng Sổ cái** và được ghi nợ vào tài khoản số dư của khách hàng. Tài khoản số dư của khách hàng được xác định trong **Khoản phải thu** \> **Thiết lập** \> **Hồ sơ đăng khách hàng**.

   Khi xác định hồ sơ đăng cho các phương thức thanh toán theo thời gian và vật tư, bạn có tùy chọn tích lũy doanh thu cho mỗi loại giao dịch (giờ, chi phí, hạng mục và phí). Nếu tùy chọn **Tích lũy doanh thu** được đặt thành **Có**, các giao dịch bán hàng chưa được lập hóa đơn trong bút toán tích hợp Project Operations sẽ được ghi vào sổ cái. Giá trị bán hàng được ghi nợ vào **WIP - tài khoản giá trị bán hàng** và ghi có vào tài khoản **Doanh thu tích lũy - giá trị bán hàng** đã được thiết lập trên trang **Thiết lập đăng sổ cái** trên tab **Doanh thu**. 
  
  > [!NOTE]
  > Tùy chọn **Tích lũy doanh thu** chỉ khả dụng khi loại giao dịch tương ứng **Giá cả** được đăng vào tài khoản lãi và lỗ.
    
7. Bung rộng FastTab **Ước tính**. Các trường trên tab này xác định cài đặt tính toán cho ước tính doanh thu theo giá cố định. Các trường trên tab này chỉ áp dụng cho hồ sơ doanh thu và chi phí dự án với phương thức thanh toán là **Giá cố định**.
8. Chọn thông tin thích hợp trong các trường sau trên FastTab **Ước tính**:

    - **Nguyên tắc được sử dụng để tính toán hoàn thành dự án**:

        - **Hợp đồng đã hoàn thành**: Việc khớp chi phí và ghi nhận doanh thu không xảy ra cho đến khi kết thúc dự án. Chi phí được phản ánh dưới dạng WIP trong số dư cho đến khi dự án hoàn thành.
        - **Phần trăm hoàn thành**: Doanh thu tích lũy được tính toán và đăng lên sổ cái mỗi kỳ dựa trên tỷ lệ hoàn thành dự án. Có nhiều phương pháp để tính toán phần trăm hoàn thành. Các phương pháp này có thể tự động dựa trên cấu hình hoặc thủ công.
        - **Không có WIP**: Thiết lập này được sử dụng cho các dự án giá cố định có khoảng thời gian ngắn và trong đó hóa đơn và chi phí xảy ra trong cùng một khoảng thời gian. Trong trường hợp này, giá trị trường **Lập hóa đơn trên tài khoản** trên FastTab **Sổ cái** tự động được đặt thành **Lãi và lỗ** để đảm bảo doanh thu được ghi nhận khi lập hóa đơn. Quy trình ước tính doanh thu sẽ không được sử dụng cho hồ sơ doanh thu và chi phí dự án này.

    - **Nguyên tắc khớp**: Trường này xác định cách giá trị bán hàng được tính toán (doanh thu tích lũy) sẽ được đăng lên sổ cái.

        - Sử dụng nguyên tắc **Giá trị bán hàng**, hệ thống sẽ tính toán giá trị bán hàng bằng cách khớp chi phí và doanh thu, sau đó đăng thành một số tiền duy nhất.
        - Sử dụng nguyên tắc **Sản xuất và lợi nhuận**, hệ thống sẽ chia giá trị bán hàng thành chi phí thực hiện và lợi nhuận tính toán. Những giá trị này được đăng riêng.

    - **Mẫu chi phí**: Cho phép nhóm các giao dịch dự án dựa trên loại giao dịch và danh mục dự án và xác định quy tắc tính toán phần trăm hoàn thành cho các nhóm này.
    - **Mã thời kỳ**: Xác định tần suất mà ước tính doanh thu được tính cho một hồ sơ doanh thu và chi phí dự án nhất định.
    - **Danh mục ước tính**: Được sử dụng cho giá trị bán hàng (doanh thu tích lũy) để đăng lên các giao dịch dự án. Trước tiên, hãy định cấu hình thể loại dự án chuyên dụng cho loại giao dịch **Phí**, sau đó đặt cờ **Ước tính** cho thể loại dự án này. Tiếp theo, tùy thuộc vào nguyên tắc khớp đã chọn, hãy chọn thể loại dự án này trong giá trị **Bán hàng** hoặc **Lợi nhuận** trong hồ sơ doanh thu và chi phí dự án.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Cấu hình mẫu cho hồ sơ doanh thu và chi phí dự án

Thời gian và vật tư – không có WIP

![Hồ sơ doanh thu và chi phí: Thời gian và vật tư - không có WIP.](media/time-material-no-wip.png)

Thời gian và vật tư – WIP (doanh thu)

![Hồ sơ doanh thu và chi phí: Thời gian và vật tư - WIP.](media/time-material-with-wip.png)

Giá cố định – Không có WIP

![Hồ sơ doanh thu và chi phí: Giá cố định - không có WIP.](media/fixed-price-no-wip.png)

Giá cố định – hợp đồng đã hoàn thành

![Hồ sơ doanh thu và chi phí: Giá cố định - hợp đồng đã hoàn thành.](media/fixed-price-completed-contract.png)

Giá cố định – phần trăm hoàn thành

![Hồ sơ doanh thu và chi phí: Giá cố định - phần trăm hoàn thành.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Ví dụ về sự kiện kế toán cho hồ sơ doanh thu và chi phí dự án mẫu.

| Sự kiện kế toán                  | Thời gian và vật tư - Không có WIP                       | Thời gian và vật tư - WIP                                                                                           | Giá cố định – không có WIP                                            | Giá cố định – Hợp đồng đã hoàn thành                                                                            | Giá cố định – Phần trăm hoàn thành                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Đang ghi sổ nhật ký kế toán các giao dịch thời gian    | Nợ – Chi phí <br>Tín dụng – Phân bổ bảng lương          | Nợ - Chi phí <br>Tín dụng – Phân bổ bảng lương <br>Nợ – Giá trị bán hàng WIP <br>Tín dụng – Giá trị bán hàng doanh thu tích lũy                | Nợ – Chi phí <br>Tín dụng – Phân bổ bảng lương                         | Nợ – Chi phí <br>Tín dụng – Phân bổ bảng lương                                                                    | Nợ – Chi phí <br>Tín dụng – Phân bổ bảng lương                       |
| Đang ghi sổ nhật ký kế toán các giao dịch chi phí | Nợ – Chi phí <br>Tín dụng – Tài khoản bù trừ chi phí | Nợ – Chi phí <br>Tín dụng – Tài khoản bù trừ chi phí <br>Nợ – Giá trị bán hàng WIP <br>Tín dụng – Giá trị bán hàng doanh thu tích lũy      | Nợ – Chi phí <br>Tín dụng – Tài khoản bù trừ chi phí                 | Nợ – Chi phí<br> Tín dụng – Tài khoản bù trừ chi phí                                                            | Nợ – Chi phí <br>Tín dụng – Tài khoản bù trừ chi phí               |
| Đang lập hóa đơn khách hàng                | Nợ – Số dư khách hàng <br>Tín dụng – Doanh thu đã lập hóa đơn | Nợ – Số dư khách hàng <br>Tín dụng – Doanh thu đã lập hóa đơn <br>Tín dụng – Giá trị bán hàng WIP Nợ – Giá trị bán hàng doanh thu tích lũy | Nợ – Số dư khách hàng <br>Tín dụng – Doanh thu đã lập hóa đơn - trên tài khoản | Nợ – Số dư khách hàng <br>Tín dụng – WIP – Đã lập hóa đơn trên tài khoản                                                  | Nợ – Số dư khách hàng <br>Tín dụng – WIP - Đã lập hóa đơn trên tài khoản    |
| Đăng ước tính doanh thu             | Không áp dụng                                   | Không áp dụng                                                                                                    | Không áp dụng                                                  | Nợ – Giá trị chi phí WIP <br>Tín dụng – Chi phí                                                                         | Nợ - WIP - Giá trị bán hàng <br>Tín dụng – Giá trị bán hàng doanh thu tích lũy |
| Loại bỏ                         | Không áp dụng                                   | Không áp dụng                                                                                                    | Không áp dụng                                                  | Tín dụng – Giá trị chi phí WIP <br>Nợ – Chi phí <br>Tín dụng – Doanh thu tích lũy - Giá trị bán hàng <br>Nợ – WIP - Đã lập hóa đơn trên tài khoản | Nợ – WIP – Đã lập hóa đơn trên tài khoản <br>Tín dụng – WIP - Giá trị bán hàng     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Định cấu hình các quy tắc hồ sơ doanh thu và chi phí dự án

Các quy tắc về hồ sơ doanh thu và chi phí dự án xác định hồ sơ doanh thu và chi phí dự án phải được sử dụng khi xử lý bất kỳ giao dịch dự án có thể lập hóa đơn nào. Xác định các quy tắc bằng cách đi tới **Kế toán và quản lý dự án** \> **Thiết lập** \> **Đăng** \> **Quy tắc về hồ sơ doanh thu và chi phí dự án**.

Các quy tắc có thể được xác định theo hợp đồng dự án, nhóm dự án hoặc theo một dự án cụ thể. Hệ thống sẽ luôn chọn quy tắc chi tiết cao nhất trước.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
