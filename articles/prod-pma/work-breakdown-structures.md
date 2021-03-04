---
title: Tổng quan về cấu trúc phân tích công việc
description: Cấu trúc phân tích công việc (WBS) là phần mô tả công việc sẽ được thực hiện cho một dự án. Đó là một hệ thống cấp bậc gồm các nhiệm vụ thể hiện sự hiểu biết của nhóm dự án về thành phần công việc, cũng như quy mô, chi phí và khoảng thời gian của từng thành phần hoặc nhiệm vụ.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0cfcc27c69695fc6fe897e798b2831528833e6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087083"
---
# <a name="work-breakdown-structures-overview"></a>Tổng quan về cấu trúc phân tích công việc

[!include [banner](../includes/banner.md)]

Cấu trúc phân tích công việc (WBS) là phần mô tả công việc sẽ được thực hiện cho một dự án. Đó là một hệ thống cấp bậc gồm các nhiệm vụ thể hiện sự hiểu biết của nhóm dự án về thành phần công việc, cũng như quy mô, chi phí và khoảng thời gian của từng thành phần hoặc nhiệm vụ. WBS có ba mục đích chính:

-   Mô tả cấu trúc phân tích hoặc thành phần công việc trong các nhiệm vụ.
-   Lập lịch trình công việc dự án.
-   Ước tính chi phí của từng nhiệm vụ.

Mức độ chi tiết trong WBS phụ thuộc vào mức độ chính xác được yêu cầu trong các ước tính và mức độ theo dõi được yêu cầu đối với các ước tính đó. Các dự án có dung sai trượt tiến độ hoặc chi phí rất thấp thường đòi hỏi có WBS chi tiết hơn, đồng thời cũng yêu cầu theo dõi cẩn thận tiến độ công việc và chi phí so với WBS. Loại dự án này phổ biến trong các ngành xây dựng và kỹ thuật. 

Ngược lại, dự án trong các ngành như truyền thông và quảng cáo, phần mềm và cơ sở hạ tầng CNTT thường mang tính đặc thù, đồng thời hiệu suất tương quan với kinh nghiệm và năng lực của cá nhân thực hiện nhiệm vụ. Do đó, các ngành này sử dụng WBS để nhận được ước lượng về quy mô của dự án, chứ không phải để theo dõi chi tiết tiến độ của dự án đó. 

Xây dựng WBS là một quá trình chuyên sâu thường được thực hiện trong một thời gian dài, đòi hỏi sự cộng tác và cung cấp thông tin từ nhiều người. Chủ đề này mô tả cách bạn có thể sử dụng các cải tiến của WBS để đáp ứng yêu cầu của mình về ước tính và theo dõi.

## <a name="prerequisites-for-creating-a-wbs"></a>Điều kiện tiên quyết để tạo WBS
Để tạo WBS, bạn phải có khả năng tạo lịch trình làm việc và ước tính chi phí công việc.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Điều kiện tiên quyết để tạo lịch trình làm việc

Để tận dụng khả năng lập lịch của các tính năng WBS, hãy hoàn tất quá trình thiết lập sau:

1.  Thiết lập lịch mặc định và lịch dự án:
    1.  Nhấp vào **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Tham số quản lý dự án và kế toán** &gt; **Lập lịch trình**. Trong trường **Lịch làm việc mặc định** , chỉ định lịch mặc định. Đây sẽ là lịch làm việc mặc định cho bất kỳ dự án mới nào được tạo.
    2.  Bạn có thể thay đổi lịch mặc định cho một dự án cụ thể. Nhấp vào trang chi tiết của dự án, sau đó, trên **Nhóm dự án và lập lịch trình** FastTab, cập nhật trường **Lịch lập lịch** bằng cách chọn một lịch khác.

2.  Thiết lập ngày làm việc tiêu chuẩn và giờ làm việc. Lịch mà bạn đặt làm lịch làm việc cho dự án của mình sẽ được sử dụng trong WBS để xác định thông tin sau:

-   Ngày làm việc và ngày lễ
-   Số giờ làm việc trong ngày

Để thiết lập ngày làm việc và giờ làm việc cho lịch hoặc để tạo lịch mới, hãy nhấp vào **Quản trị tổ chức** &gt; **Chung** &gt; **Lịch**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Điều kiện tiên quyết để ước tính chi phí công việc

Để tận dụng khả năng ước tính chi phí của WBS, bạn nên thiết lập chi phí và giá bán cho nhân công, loại lao động, phí tổn, phí và các hạng mục.

-   Để thiết lập chi phí và giá bán của nhân công, phí tổn và các loại phí, hãy nhấp vào **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Giá**.
-   Để thiết lập chi phí và giá bán của các hạng mục, hãy sử dụng trang **Thỏa thuận thương mại** cho mỗi mục trên trang danh sách **Sản phẩm đã phát hành** trong Quản lý thông tin sản phẩm.

## <a name="creating-a-wbs"></a>Đang tạo WBS
Tạo WBS bao gồm ba hoạt động:

1.  **Phân chia công việc** – Chia nhỏ công việc thành các khúc hoặc nhiệm vụ có thể quản lý được.
2.  **Lịch trình làm việc** – Ước tính thời gian cần thiết để hoàn thành một nhiệm vụ, đặt sự phụ thuộc lẫn nhau của nhiệm vụ, chọn ngày bắt đầu và ngày kết thúc cho nhiệm vụ.
3.  **Ước tính chi phí** – Ước tính chi phí cho từng nhiệm vụ.

Các phần sau đây thảo luận về cách mà các khả năng của WBS có thể trợ giúp từng hoạt động này.

### <a name="work-decomposition"></a>Phân chia công việc

Tạo bản chia nhỏ hoặc phân chia công việc thường là bước đầu tiên trong quá trình tạo WBS. Chức năng WBS hỗ trợ các cấu trúc cơ bản sau đây để chia nhỏ hoặc phân chia công việc. 

**Nhiệm vụ gốc của dự án** Nhiệm vụ gốc của dự án là nhiệm vụ tóm tắt cấp cao nhất của một dự án. Tất cả các nhiệm vụ khác của dự án được tạo trong nhiệm vụ này. Tên nhiệm vụ gốc luôn được đặt thành tên dự án. Nhân công, ngày và khoảng thời gian của nút gốc tóm tắt các giá trị cho các nhiệm vụ trong nhiệm vụ gốc. Bạn không thể sửa đổi thuộc tính của nút gốc hoặc xóa nút gốc.

**Nhiệm vụ tóm tắt hoặc vùng chứa** Nhiệm vụ tóm tắt là một nhiệm vụ có các nhiệm vụ con hoặc các nhiệm vụ cấu thành bên dưới nó. Nhiệm vụ tóm tắt không có bất kỳ nỗ lực làm việc hoặc chi phí riêng nào. Thay vào đó, nhân công làm việc và chi phí của một nhiệm vụ tóm tắt là tổng của nhân công làm việc và chi phí của các nhiệm vụ cấu thành nó. Ngày bắt đầu sớm nhất của nhiệm vụ cấu thành được dùng làm ngày bắt đầu nhiệm vụ tóm tắt, và ngày kết thúc sớm nhất nhiệm vụ cấu thành được dùng làm ngày kết thúc. Bạn có thể sửa đổi tên của nhiệm vụ tóm tắt nhưng không thể sửa đổi việc lập lịch các thuộc tính cho nhân công, ngày và khoảng thời gian. Nếu xóa nhiệm vụ tóm tắt, bạn cũng có thể xóa tất cả các nhiệm vụ cấu thành của nó. 

**Nhiệm vụ nút lá** Một nhiệm vụ nút lá đại diện cho gói công việc chi tiết nhất của dự án. Nhiệm vụ nút lá có nhân công ước tính, số nguồn lực theo kế hoạch, ngày bắt đầu và kết thúc theo kế hoạch và khoảng thời gian. 

Bạn có thể hoàn thành các thao tác hệ thống cấp bậc sau để cho phép tạo hệ thống cấp bậc hoặc phân chia công việc cho một dự án. 

**Nhiệm vụ mới** Bất kỳ nhiệm vụ mới nào bạn tạo sẽ được tự động thêm vào trong nút gốc và số WBS sẽ tự động được gán cho nhiệm vụ. Số WBS đại diện cho cấp của nhiệm vụ trong hệ thống cấp bậc. Đối với các nhiệm vụ ở cấp 1 trong nhiệm vụ gốc dự án, lược đồ đánh số 1, 2, 3, v.v. được sử dụng. Đối với các nhiệm vụ dưới cấp 1, lược đồ đánh số 1.1, 1.2, 1.3, v.v. được sử dụng. Đối với mỗi cấp độ được thêm vào cấp độ trước đó, một chuỗi số có dấu chấm mới sẽ được thêm vào. 

Hiện tại, bạn không thể tùy chỉnh việc đánh số WBS. 

**Thụt lề nhiệm vụ** Khi bạn thụt lề một nhiệm vụ, nhiệm vụ đó sẽ trở thành phần tử con của nhiệm vụ đứng trước nó. Số WBS của nhiệm vụ con mới sẽ tự động được tính toán lại dựa trên số WBS của phần tử mẹ mới. Nhiệm vụ mẹ giờ là nhiệm vụ tóm tắt hoặc vùng chứa, do đó trở thành tập hợp các nhiệm vụ cấu hình. 

> [!NOTE] 
> Khi bạn thụt lề tác vụ trong tác vụ là nút lá trước thao tác thụt lề, nhiệm vụ tóm tắt mới tạo sẽ mất ngày, nhân công và số tài nguyên của chính nó. Lúc này, nó sẽ sử dụng tóm tắt các giá trị của nhiệm vụ cấu thành mới. 

**Tăng lề nhiệm vụ** Khi bạn tăng lề nhiệm vụ, nó không còn là một nhiệm vụ cấu thành của nhiệm vụ mẹ nữa. Số WBS của nhiệm vụ này được tự động tính toán lại để phản ánh cấp độ mới của nhiệm vụ trong hệ thống cấp bậc. Nhân công, chi phí và ngày của nhiệm vụ mẹ phía trước được tính toán lại để loại trừ nhiệm vụ đó. 

**Chuyển lên và chuyển xuống** Khi bạn nhấp vào **Chuyển lên** và **Chuyển xuống** , bạn thay đổi vị trí của một nhiệm vụ trong hệ thống cấp bậc của nhiệm vụ mẹ. Vị trí của nhiệm vụ không ảnh hưởng đến nhân công, chi phí, ngày hoặc khoảng thời gian của nhiệm vụ. Tuy nhiên, số WBS của nhiệm vụ được tự động tính toán lại để phản ánh vị trí mới của nhiệm vụ.

### <a name="schedule-estimation"></a>Ước tính lịch trình

Ước tính lịch trình thường là bước thứ hai trong quy trình tạo WBS. Cách tốt nhất là bạn nên hoàn thành ước tính lịch trình sau khi tạo nhiệm vụ. Trang **Cấu trúc phân tích công việc** trong Finance có hai phần. Ngăn trên dùng để ước tính lịch trình và ngăn dưới bao gồm tab **Chi phí và doanh thu ước tính** mà bạn có thể sử dụng để ước tính chi phí. 
**Yếu tố phụ thuộc nhiệm vụ** Trong WBS, bạn có thể tạo mối quan hệ tiếp trước giữa các nhiệm vụ. Khi bạn gán các nhiệm vụ tiếp trước cho một nhiệm vụ, nhiệm vụ đó chỉ có thể bắt đầu sau khi tất cả các nhiệm vụ tiếp trước của nó được hoàn thành. Ngày bắt đầu theo kế hoạch của nhiệm vụ được tự động đặt thành ngày mới nhất của tất cả các nhiệm vụ tiếp trước. 

**Lập lịch trình tác vụ** Các yếu tố sau đây xác định lịch trình của các nhiệm vụ nút lá:

-   Người tiền nhiệm
-   Nỗ lực
-   Số tài nguyên
-   Ngày bắt đầu và ngày kết thúc

Ngày bắt đầu của một nhiệm vụ nút lá không có người tiền nhiệm sẽ tự động được đặt thành ngày bắt đầu lên lịch của dự án. Khoảng thời gian của nhiệm vụ nút lá luôn được tính toán là số ngày làm việc giữa của ngày bắt đầu và ngày kết thúc. 

*<strong><em>Quy tắc lập lịch trình</em></strong>* Khi tính năng hỗ trợ lập lịch trình tự động được bật, các quy tắc sau sẽ áp dụng cho việc lập lịch trình nhiệm vụ cho các nhiệm vụ nút lá:

-   Ngày bắt đầu và ngày kết thúc của nhiệm vụ phải là ngày làm việc, theo lịch lập lịch của dự án.
-   Ngày bắt đầu của nhiệm vụ có người tiền nhiệm sẽ tự động được đặt thành ngày kết thúc gần nhất của nhiệm vụ trước đó.
-   Nhân công cho một nhiệm vụ được tính toán tự động như sau:

Số người x Khoảng thời gian x Số giờ trong ngày làm việc tiêu chuẩn của lịch dự án. 

Trong một số trường hợp, bạn có thể cần phân biệt với những quy tắc này. Bạn có thể tắt lập lịch tự động để ngăn Finance tự động thiết lập hoặc sửa chữa bất kỳ thuộc tính nào của các nhiệm vụ nút lá. Khi bạn nhập thông tin cho một nhiệm vụ gây ra vi phạm bất kỳ quy tắc lập lịch nào, biểu tượng lỗi lập lịch sẽ hiển thị cho nhiệm vụ đó. Nếu bạn không muốn các lỗi lập lịch hiển thị, hãy nhấp vào **Lỗi lập lịch được hiển thị** để tắt tính năng. 

> [!NOTE] 
> Các giá trị cho nhiệm vụ tóm tắt hoặc vùng chứa tiếp tục được tính bằng tổng các giá trị của các nhiệm vụ cấu thành, bất kể tính năng hỗ trợ lập lịch tự động được bật hay tắt. 

**Sửa lỗi lập lịch** Khi tính năng hỗ trợ lập lịch tự động được bật, các lỗi lập lịch sẽ không có khả năng xảy ra. Tuy nhiên, nếu bạn tắt tính năng hỗ trợ lập lịch tự động rồi bật lại sau, các biểu tượng lỗi lập lịch có thể xuất hiện trong WBS. 

**Sửa lỗi lập lịch theo nhiệm vụ** Khi bạn bấm đúp vào biểu tượng lỗi lập lịch cho một nhiệm vụ cụ thể, một hộp thoại sẽ hiển thị tất cả các lỗi lập lịch cho nhiệm vụ đó. Bạn có thể quyết định những lỗi lập lịch nào cần sửa cho nhiệm vụ. 

**Sửa tất cả các lỗi lập lịch** Nếu bạn muốn Finance sửa tất cả các lỗi lập lịch trong WBS, trên Ngăn hành động, hãy nhấp vào **Sửa tất cả chênh lệch khi lập lịch**. 

> [!NOTE] 
> Tính năng này có thể tạo ra những sửa đổi đáng kể đối với WBS. Các lỗi được sửa lại theo thứ tự sau:

1.  Nhân công ước tính của tất cả nhiệm vụ được sửa đổi sao cho bằng với nguồn lực được xác định trong lịch dự án.
2.  Ngày bắt đầu của mỗi nhiệm vụ được sửa đổi để nhiệm vụ bắt đầu sau khi hoàn thành tất cả các nhiệm vụ tiếp trước.
3.  Ngày bắt đầu của mỗi nhiệm vụ được sửa đổi để loại bỏ khoảng trống trong ngày bắt đầu của các nhiệm vụ tiếp trước.

### <a name="cost-estimation"></a>Dự toán chi phí

Như đã đề cập trước đó trong tài liệu này, bạn nhập ước tính chi phí cho mỗi nhiệm vụ nút lá bằng cách sử dụng tab **Chi phí và doanh thu ước tính** trong ngăn dưới của trang **Cấu trúc phân tích công việc**. 

> [!NOTE] 
> Bạn không thể sửa đổi ước tính chi phí cho một nhiệm vụ tóm tắt hoặc vùng chứa. Ước tính chi phí cho một nhiệm vụ tóm tắt bằng tổng ước tính chi phí của các nhiệm vụ nút lá của nó. Tổng chi phí ước tính cho mỗi nhiệm vụ được tính bằng tổng chi phí ước tính cho các loại giao dịch sau:

-   Nhân công
-   Hạng mục hoặc vật liệu
-   Chi phí

Loại giao dịch **Phí** được dùng để ước tính doanh thu dựa trên phí. Loại giao dịch này không có thành phần chi phí và do đó không được xem xét khi ước tính chi phí. 

Loại giao dịch **Trên tài khoản** được sử dụng để ghi giá trị bán hàng theo hợp đồng trong một loại dự án có giá trị cố định. Loại giao dịch này cũng không được xem xét khi ước tính chi phí. 

Khi bạn ước tính chi phí nhân công, vật liệu và chi phí cho từng nhiệm vụ, bạn phải gán một thể loại dự án vào chi phí ước tính. 

**Ước tính chi phí nhân công** Đối với mỗi nhiệm vụ nút lá, bạn chỉ định nhân công làm việc theo giờ và một thể loại mặc định. Do đó, khi bạn thiết lập lịch trình cho một nhiệm vụ, ước tính chi phí nhân công cho nhiệm vụ đó sẽ tự động được thêm vào thể loại mặc định cho nhân công. Ước tính chi phí này được hiển thị trên tab **Chi phí và doanh thu ước tính** trong lưới **Chi tiết mô tả** cho nhiệm vụ đó. Nếu bạn cần thêm ước tính chi phí nhân công, bạn có thể thêm chúng vào tab này. Nếu bạn tăng hoặc giảm số giờ ước tính chi phí nhân công, lịch trình cho nhiệm vụ sẽ tự động được tính toán lại. 

**Ước tính phí tổn và chi phí vật liệu** Tab **Chi phí và doanh thu ước tính** cũng cho phép bạn ước tính phí tổn và chi phí vật liệu cho một nhiệm vụ, nếu bạn yêu cầu ước tính. 

Chi phí và giá bán cho mỗi dòng ước tính nhân công hoặc phí tổn đều dựa trên thiết lập được xác định cho từng thể loại trong bảng giá tại **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Định giá**. Đối với các hạng mục, chi phí và giá bán được thêm theo mặc định từ thỏa thuận hạng mục hoặc thương mại trên trang danh sách **Sản phẩm đã phát hành** trong mục Quản lý thông tin sản phẩm.

## <a name="tracking-progress-on-the-wbs"></a>Theo dõi tiến độ WBS
Một số ngành theo dõi tiến độ của một dự án dựa trên WBS ở cấp độ rất chi tiết, trong khi những ngành khác theo dõi tiến độ ở cấp độ WBS cao hơn. Phần này mô tả cách bạn có thể sử dụng tính năng theo dõi WBS cho các yêu cầu dự án của mình. 

Finance có ba dạng xem cho WBS của dự án: dạng xem Lập kế hoạch, dạng xem Theo dõi nhân công và dạng xem Theo dõi chi phí.

### <a name="planning-view"></a>Dạng xem Lập kế hoạch

Dạng xem Lập kế hoạch hiển thị ước tính theo kế hoạch hoặc cơ sở của thông tin lịch trình và chi phí. Mặc dù không có tính năng nào để theo dõi phiên bản và đường cơ sở cho WBS dự án, các giá trị trong dạng xem này nhằm đại diện cho phiên bản đường cơ sở. Các phần ước tính Lịch trình và ước tính Chi phí của chủ đề này mô tả dạng xem này và cách dùng nó để tạo WBS.

### <a name="effort-tracking-view"></a>Dạng xem theo dõi nhân công

Dạng xem Theo dõi nhân công hiển thị quá trình theo dõi tiến độ các nhiệm vụ trong WBS. Nó so sánh số giờ nhân công thực tế tích lũy cho một nhiệm vụ với số giờ nhân công theo kế hoạch. Các công thức sau cung cấp các giá trị ở dạng xem Theo dõi nhân công:

-   Phần trăm tiến độ = Nhân công thực tế cho đến nay ÷ Nhân công theo kế hoạch cho nhiệm vụ
-   Nhân công còn lại (còn gọi là Ước tính hoàn thành \[ETC\]) = Nhân công theo kế hoạch – Nhân công thực tế đến nay
-   Ước tính hoàn thành (EAC) = Nhân công còn lại + Nhân công thực tế cho đến nay
-   Chênh lệch nhân công dự kiến = Nhân công theo kế hoạch – EAC

Dạng xem Theo dõi nhân công hiển thị dự báo chênh lệch nhân công cho nhiệm vụ, dựa trên việc EAC nhiều hơn hay ít hơn nhân công theo kế hoạch:

-   Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu và đang chậm lịch trình.
-   Nếu EAC ít hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu và đang nhanh hơn lịch trình.

**Dự báo lại nhân công của người quản lý dự án** Đôi khi, người quản lý dự án hoặc một cá nhân khác đang theo dõi tiến độ của dự án sẽ phải sửa đổi các ước tính ban đầu về một nhiệm vụ. Nhiệm vụ có thể di chuyển nhanh hơn hoặc chậm hơn so với dự đoán ban đầu vì nhiều lý do. Ví dụ: phạm vi đã được giảm xuống hoặc nhân viên có ít kinh nghiệm hơn so với kế hoạch ban đầu. Dự báo là nhận định của người quản lý dự án về ước tính, dựa trên trạng thái hiện tại của dự án. Nhìn chung, bạn không nên thay đổi số đường cơ sở của dự án vì đường cơ sở của dự án đại diện cho một tài liệu được phát hành cho lịch trình và dự toán chi phí của dự án mà tất cả bên tham gia dự án đã thống nhất. 

Có hai cách mà người quản lý dự án có thể sửa đổi nhân công trên nhiệm vụ:

-   Sửa đổi nhân công còn lại được tự động đặt thành cập nhật nhân công còn lại thực tế trong nhiệm vụ.
-   Sửa đổi phần trăm tiến độ còn lại được tự động đặt thành cập nhật tiến độ thực tế trong nhiệm vụ.

Cả hai cách này mang đến một phép tính lại ETC, EAC và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trong nhiệm vụ. EAC, ETC và phần trăm tiến độ trên các nhiệm vụ tóm tắt cũng được tính toán lại và chênh lệch nhân công dự báo sẽ được cập nhật. 

**Nhân công được sửa đổi trong nhiệm vụ tóm tắt** Bạn có thể sửa đổi nhân công trên các nhiệm vụ tóm tắt hoặc vùng chứa. Dù bạn sửa đổi các giá trị này theo nhân công còn lại hoặc phần trăm tiến độ trên nhiệm vụ tóm tắt, các phép tính sẽ tự động diễn ra theo thứ tự sau đây:

1.  EAC, ETC và phần trăm tiến trình trên nhiệm vụ được tính.
2.  EAC mới được phân phối cho các nhiệm vụ con theo cùng một tỷ lệ như trong số lượng EAC ban đầu.
3.  EAC mới trên mỗi nhiệm vụ nút lá được tính toán.
4.  Nhân công còn lại và phần trăm tiến độ được tính toán lại cho tất cả nhiệm vụ con bị ảnh hưởng, dựa trên giá trị EAC mới. Chênh lệch nhân công của nhiệm vụ cũng được tính toán lại.
5.  EAC của các nhiệm vụ tóm tắt cũng được tính toán lại từ các nút lá.

Nhấp vào **Mở rộng lên cấp độ** trong dạng xem Theo dõi nhân công để đặt cấp độ theo dõi và duy trì WBS của bạn. WBS tự động được mở rộng đến mức đó trong dạng xem Theo dõi nhân công bất cứ khi nào bạn mở nó.

### <a name="cost-tracking-view"></a>Dạng xem theo dõi chi phí

Dạng xem Theo dõi chi phí hiển thị quá trình theo dõi mức sử dụng chi phí cho một nhiệm vụ. Trong dạng xem này, chi phí thực tế đã được chi tiêu cho một nhiệm vụ cho đến này được so sánh với chi phí theo kế hoạch của nhiệm vụ. Các công thức sau cung cấp các giá trị ở dạng xem Theo dõi chi phí:

-   Phần trăm chi phí đã sử dụng = Chi phí thực tế cho đến nay ÷ Chi phí theo kế hoạch cho nhiệm vụ
-   Chi phí hoàn thành (CTC) = Chi phí theo kế hoạch – Chi phí thực tế cho đến nay
-   Ước tính hoàn thành (EAC) = CTC + Chi phí thực tế cho đến nay
-   Chênh lệch chi phí dự kiến = Chi phí theo kế hoạch – EAC

Dạng xem Theo dõi chi phí hiển thị dự báo chênh lệch chi phí cho nhiệm vụ, dựa trên việc EAC nhiều hơn hay ít hơn chi phí theo kế hoạch:

-   Nếu EAC nhiều hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến dùng nhiều tiền hơn so với kế hoạch ban đầu và đang vượt quá ngân sách.
-   Nếu EAC ít hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến dùng ít tiền hơn so với kế hoạch ban đầu và chưa dùng hết ngân sách.

**Dự báo lại chi phí của người quản lý dự án** Người quản lý dự án phải sử dụng CTC để sửa lại dự toán chi phí ban đầu cho một nhiệm vụ. Người quản lý dự án có thể sửa đổi giá trị CTC thành chi phí cần thiết để hoàn thành nhiệm vụ. Nếu bạn sửa đổi giá trị CTC, CTC, EAC của nhiệm vụ, phần trăm chi phí đã dùng và chênh lệch chi phí dự báo trong nhiệm vụ đều sẽ được tính toán lại. EAC, ETC và phần trăm chi phí đã dùng trong các nhiệm vụ tóm tắt cũng được tính toán lại và chênh lệch chi phí dự báo sẽ được cập nhật. 

> [!NOTE] 
> Khi bạn sửa đổi nhân công cho một nhiệm vụ WBS trong dạng xem Theo dõi nhân công, CTC, EAC, phần trăm chi phí đã dùng và chênh lệch chi phí dự báo của nhiệm vụ đều được tính toán lại trong dạng xem Theo dõi chi phí. Tuy nhiên, sửa đổi chi phí không ảnh hưởng đến các giá trị trong dạng xem Theo dõi nhân công, vì chi phí theo loại giao dịch (nhân công, vật liệu hoặc phí tổn) hoặc thể loại dự án đều không được sửa đổi. 

**Sửa đổi dự báo cho chi phí trong nhiệm vụ tóm tắt** Bạn có thể sửa đổi chi phí trong các nhiệm vụ tóm tắt và các phép tính diễn ra tự động theo thứ tự sau:

1.  EAC, CTC và phần trăm chi phí đã dùng trong nhiệm vụ được tính toán lại.
2.  EAC mới được phân phối cho các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.
3.  EAC mới cho mỗi nhiệm vụ được tính toán.
4.  CTS và phần trăm chi phí đã dùng được tính toán lại cho các nhiệm vụ con bị ảnh hưởng, dựa trên giá trị EAC. Chênh lệch chi phí của nhiệm vụ cũng được tính toán lại.
5.  EAC cho tất cả các nhiệm vụ tóm tắt được tính toán lại dựa trên thay đổi này.

Nhấp vào **Mở rộng lên cấp độ** trong dạng xem Theo dõi chi phí để đặt cấp độ theo dõi và duy trì WBS của bạn. WBS tự động được mở rộng đến cấp độ đó trong dạng xem Theo dõi chi phí bất cứ khi nào bạn mở nó.

### <a name="earned-value-management"></a>Quản lý giá trị thu được

Bạn có thể sử dụng phương pháp giá trị thu được (EVM) để theo dõi tiến độ của một dự án. Bạn có thể xem số liệu về giá trị thu được trong Trung tâm vai trò của người quản lý dự án. Thành phần của biểu đồ giá trị thu được hiển thị các giá trị theo giai đoạn thời gian của giá trị theo kế hoạch và chi phí thực tế. Giá trị thu được tính đến ngày hiện tại được hiển thị dưới dạng điểm. Dữ liệu theo giai đoạn thời gian cho giá trị thu được hiện không có sẵn. 

Giai đoạn thời gian trên biểu đồ giá trị thu được sẽ hiển thị theo tuần hoặc theo tháng. Phần này mô tả ba trụ cột của EVM: giá trị theo kế hoạch, giá trị thu được và chi phí thực tế. 

**Giá trị theo kế hoạch** Lý thuyết EVM phát biểu rằng biểu đồ giá trị theo kế hoạch thể hiện tốc độ mà nhóm của dự án đã lên kế hoạch thu được giá trị từ dự án. 

Finance sử dụng quy tắc kiếm tiền 0:100 khi lập biểu đồ giá trị theo kế hoạch. Theo quy tắc này, giá trị của nhiệm vụ được đăng lên nhiệm vụ kể từ ngày kết thúc. Không có giá trị nào được đăng cho đến khi nhiệm vụ hoàn thành 100 phần trăm. 

Trong Quản lý dự án và kế toán, bạn nhập ngày kết thúc của các nút lá và chi phí theo kế hoạch cho nó. Khi biểu đồ giá trị theo kế hoạch được hiển thị theo tuần, giá trị kế hoạch được tóm tắt theo tuần cho tất cả các nhiệm vụ nút lá trong suốt thời gian của dự án. 

**Giá trị theo thu được** Lý thuyết EVM phát biểu rằng biểu đồ giá trị thu được thể hiện tốc độ mà nhóm của dự án thực tế thu được giá trị từ dự án. 

Finance sử dụng quy tắc kiếm tiền 0:100 khi lập biểu đồ giá trị thu được. Theo quy tắc này, giá trị của nhiệm vụ được đăng lên nhiệm vụ kể từ ngày kết thúc. Không có giá trị nào được đăng cho đến khi nhiệm vụ hoàn thành 100 phần trăm. 

Khi tính giá trị thu được, phần trăm tiến độ của từng nhiệm vụ sẽ được xem xét. Theo quy tắc kiếm tiền 0:100, chỉ những nhiệm vụ được hoàn thành trong một khoảng thời gian nhất định mới được xem xét để tính giá trị thu được vào cuối khoảng thời gian đó. Giá trị thu được từ dự án được tính cho tất cả các nhiệm vụ đã hoàn thành khi biểu đồ được tạo. 

> [!NOTE] 
> Hiện tại, hệ thống theo dõi WBS không có cấu trúc dữ liệu để lưu trữ tỷ lệ phần trăm tiến độ trước đây trong mỗi nhiệm vụ. Do đó, giá trị thu được chỉ có thể được báo cáo vào thời điểm khối lập phương được xử lý. Thường xuyên xử lý khối lập phương để cập nhật dữ liệu giá trị thu được hiển thị trên Trung tâm vai trò. 

**Chi phí thực tế** Lý thuyết EVM phát biểu rằng biểu đồ chi phí thực tế đại diện cho tốc độ chi tiêu tiền vào dự án. 

Các giao dịch được đăng cho một dự án được sử dụng để lập biểu đồ đường đẳng phí thực tế. Các chi phí được tóm tắt theo ngày. Sau đó, dữ liệu này được sử dụng để vẽ biểu đồ chi phí thực tế theo tuần hoặc theo tháng trên biểu đồ giá trị thu được.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Cách sử dụng các khái niệm về giá trị theo kế hoạch, giá trị thu được và chi phí thực tế

**Chênh lệch về lịch trình** Trong quá trình lập kế hoạch, bạn tạo dự báo cho công việc trên một dòng thời gian. Do đó, giá trị theo kế hoạch là tốc độ mà người lập kế hoạch dự án nghĩ rằng công việc sẽ được hoàn thành trong dự án. Khi dự án diễn ra, công việc được hoàn thành và dự án đó thu được giá trị. Bằng cách so sánh giá trị theo kế hoạch với giá trị thu được, bạn có thể xem tiến độ của công việc trong một dự án. Kết quả của sự so sánh này được gọi là chênh lệch lịch trình. 

Nếu giá trị theo kế hoạch trong một khoảng thời gian lớn hơn giá trị thu được, thì số lượng công việc đã được thực hiện trong một dự án sẽ ít hơn so với kế hoạch. Do đó, dự án đang chậm lịch trình. Do giá trị theo kế hoạch và giá trị thu được được biểu thị bằng số tiền, thời gian trễ của dự án cũng được tính bằng tiền. 

Nếu giá trị theo kế hoạch trong một khoảng thời gian ít hơn giá trị thu được, thì số lượng công việc đã được thực hiện trong một dự án sẽ nhiều hơn so với kế hoạch. Do đó, dự án đang nhanh hơn so với lịch trình. Khoảng thời gian nhanh hơn này cũng được tính bằng giá trị tiền tệ.

**Chênh lệch chi phí** Vì giá trị thu được sử dụng giá vốn làm hệ số nhân, giá trị thu được cho biết chi phí của công việc được thực hiện trong một dự án. Khi một dự án tiến triển, nhật ký giao dịch cung cấp bản ghi về số tiền thực sự được chi cho dự án đó. Bằng cách so sánh giá trị thu được với chi phí thực tế, bạn có thể xem số tiền đang được chi tiêu so với giá trị thu được. Kết quả của sự so sánh này được gọi là chênh lệch chi phí. 

Nếu chi phí thực tế đã bỏ ra trong một khoảng thời gian nhiều hơn giá trị thu được, thì số tiền đã bỏ ra nhiều hơn số tiền thu được. Do đó, dự án vượt quá ngân sách. 

Nếu chi phí thực tế đã bỏ ra trong một khoảng thời gian ít hơn giá trị thu được, thì số tiền thu được nhiều hơn số tiền bỏ ra. Do đó, dự án chưa dùng hết ngân sách.

## <a name="wbs-templates"></a>Mẫu WBS
Bạn có thể sử dụng chức năng mẫu WBS để tạo các mẫu tiêu chuẩn cho các dự án. Nếu các dự án mà công ty của bạn cung cấp liên quan đến nhiều công việc lặp lại, bạn nên cân nhắc việc tạo một mẫu WBS. 

Bạn có thể tạo một mẫu WBS từ WBS của một dự án hiện có, sao cho kiến thức và các phương pháp hay nhất mà bạn thu thập được trong quá trình lập kế hoạch cho dự án đó có thể được sử dụng lại cho các dự án tương tự trong tương lai. Tuy nhiên, đôi khi, việc lưu toàn bộ WBS làm mẫu có thể không hợp lý. Do đó, bạn cũng có thể tạo mẫu từ các phần của WBS cho một dự án.

### <a name="saving-a-projects-wbs-as-a-template"></a>Lưu WBS của một dự án làm mẫu

Sau khi bạn tạo một mẫu, bạn có thể nhập nó vào WBS của một dự án mới dưới nút gốc hoặc trong bất kỳ nhiệm vụ nào trong WBS của dự án.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Nhập mẫu WBS vào WBS của dự án

Khi bạn nhập nhiệm vụ, các nhiệm vụ trong mẫu được sắp xếp dựa trên ngày bắt đầu của nhiệm vụ mà chúng được nhập vào. Trong quá trình nhập, các mối quan hệ tiếp trước trên nhiệm vụ mẫu được sử dụng để tính toán ngày bắt đầu cho các nhiệm vụ đã nhập. Lịch công việc tiêu chuẩn của dự án đích được áp dụng để tính toán ngày kết thúc của các nhiệm vụ đã nhập, sao cho các ngày làm việc và giờ làm việc tiêu chuẩn được xác định trong lịch công việc của dự án hiện tại được giữ lại. 

Các khoản chi phí và giá bán trên đường ước tính được áp dụng để đảm bảo rằng giá cụ thể cho dự án hoặc hợp đồng dự án có ngày hiệu lực.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Sự khác biệt giữa WBS của dự án và mẫu WBS

-   Các nhiệm vụ trong mẫu WBS không có ngày bắt đầu và ngày kết thúc.

Ngày làm việc và ngày không làm việc không được đặt cho các mẫu WBS.

-   Các mẫu WBS luôn sử dụng lịch lập kế hoạch được thiết lập làm lịch mặc định cho tất cả các dự án.

Lịch lập lịch mặc định chỉ được sử dụng để tìm ra số giờ trong một ngày công tiêu chuẩn.

-   Các mối quan hệ tiếp trước không được sao chép vào mẫu WBS.

Vì các mẫu WBS không có ngày, nên không buộc phải có logic ngày bắt đầu dựa trên ngày kết thúc của nhiệm vụ tiếp trước.

-   Dòng ước tính chi phí nhân công được tạo tự động khi một nhiệm vụ được tạo trong mẫu WBS. Giá bán và khoản chi phí được sao chép từ nhân viên đã chọn.

Có thể tạo phí tổn và chi phí hạng mục theo cách thủ công, cũng như trên WBS của dự án.

-   Lỗi lập lịch được hiển thị khi có sai lệch so với công thức sau:

Nhân công = Số nguồn lực X Khoảng thời gian X Số giờ trong một ngày công tiêu chuẩn 

Bạn có thể sửa tất cả các lỗi lập lịch cùng một lúc bằng cách nhấp vào **Sửa tất cả các lỗi lập lịch**. 

Ngoài ra, bạn có thể sửa lỗi từng lỗi lập lịch bằng cách nhấp vào biểu tượng cảnh báo cho từng nhiệm vụ.





[!INCLUDE[footer-include](../includes/footer-banner.md)]