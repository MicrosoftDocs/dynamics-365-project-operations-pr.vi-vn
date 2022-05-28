---
title: Hợp đồng dự án
description: Chủ đề này cung cấp các ví dụ về hợp đồng dự án mà bạn có thể tạo cho các loại dự án và nguồn tiền khác nhau, cũng như cách thức quản lý hợp đồng và lập hóa đơn cho khách hàng trong dự án.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cfc5183ce28574d865389eba72cafd3528741cc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683518"
---
# <a name="project-contracts"></a>Hợp đồng dự án

[!include [banner](../includes/banner.md)]

Bài viết này cung cấp các ví dụ về hợp đồng dự án mà bạn có thể tạo cho các loại dự án và nguồn tiền khác nhau, cũng như cách thức quản lý hợp đồng và lập hóa đơn cho khách hàng trong dự án.

Loại dự án mà bạn tạo cho hợp đồng dự án sẽ xác định phương pháp được sử dụng để lập hóa đơn cho khách hàng trong dự án. Bạn có thể thay đổi hợp đồng dự án và dự án liên quan, nhưng bạn không thể thay đổi loại dự án. 

Khi sử dụng hợp đồng dự án, bạn có thể lập hóa đơn cho một hoặc nhiều dự án cùng một lúc. Hợp đồng dự án cũng giúp bảo đảm quy trình lập hóa đơn nhất quán cho mọi dự án nhỏ trong cấu trúc dự án. 

Mọi dự án sẽ lập hóa đơn phải được liên kết với một hợp đồng dự án. Các mục thiết đặt cho hợp đồng dự án được áp dụng cho mọi dự án và dự án nhỏ được liên kết với hợp đồng dự án đó. 

Hợp đồng dự án có thể chỉ định một hoặc nhiều nguồn tiền. Do đó, bạn có thể chia việc thanh toán cho nhiều nhà tài trợ, thiết lập giới hạn cấp vốn để các nguồn tiền không được lập hóa đơn nhiều hơn mức tiền đã chỉ định và đặt cấu hình các quy tắc cấp vốn để tính phí chi tiêu.

## <a name="funding-for-project-contracts"></a>Tài trợ cho hợp đồng dự án
Một số hợp đồng dự án quy định rằng nhiều bên chia sẻ trách nhiệm cấp vốn chi phí dự án. Dưới đây là một số ví dụ:

-   Một khách hàng lớn có nhiều yêu cầu bộ phận rằng việc cấp vốn cho một dự án được chia theo bộ phận.
-   Công ty của bạn chia sẻ chi phí của một dự án lớn với một tổ chức bên ngoài.
-   Một dự án xây đường được hai thành phố đồng cấp vốn.
-   Một dự án xây cầu nhận được khoản trợ cấp của chính phủ và một tập đoàn tư nhân.

Trong Dynamics 365 Finance, bạn có thể chia nhỏ thanh toán cho một giao dịch hoặc toàn bộ dự án cho nhiều khách hàng, khoản tài trợ hoặc tổ chức. 

Trong dự án có nhiều nhà tài trợ, tất cả các bên góp tiền tài trợ cho một dự án tài trợ nâng cao sẽ được gọi là nguồn tiền. Sau khi khách hàng, tổ chức hoặc đơn vị tài trợ được xác định là nguồn tiền, nguồn này có thể được chỉ định cho một hoặc nhiều quy tắc cấp vốn. Quy tắc cấp vốn có các tiêu chí xác định cách thức phân bổ phí cho các nguồn tiền khác nhau trong một dự án. 

Vì các mặt hàng tồn kho, chẳng hạn như những mặt hàng xuất hiện trong yêu cầu mua hàng và đơn đặt hàng, không thể phân chia được, nên số tiền chi phí cũng không thể phân chia được cho nhiều nguồn tiền tại thời điểm phân phối. Do đó, giá trị nguồn tiền sẽ vẫn là 0 (không) cho đến khi vấn đề hàng tồn kho được đăng. Khi vấn đề hàng tồn kho được đăng, số tiền chi phí sẽ được phân phối theo quy tắc phân phối tài khoản cho dự án.

Sau đây là một số bước mà bạn có thể thực hiện để giúp việc phân chia thanh toán giữa nhiều nguồn tiền trở nên dễ dàng hơn:

-   Chỉ định rằng tất cả các giao dịch được nhập cho một dự án sẽ sử dụng cùng một loại tiền bán hàng như hợp đồng dự án.
-   Thiết lập giới hạn cấp vốn để nguồn tiền không được lập hóa đơn nhiều hơn một mức tiền cụ thể cho một dự án.
-   Đặt cấu hình quy tắc cấp vốn và giới hạn cấp vốn cho từng nhân viên, mặt hàng, danh mục, nhóm danh mục và loại giao dịch (hoặc cho tất cả các loại giao dịch).
-   Chọn ngày bắt đầu và ngày kết thúc tùy chọn để xác định khoảng thời gian hiệu lực cho mỗi quy tắc cấp vốn.
-   Chỉ định tỷ lệ phần trăm chi trả cho mỗi nguồn tiền.
-   Chỉ rõ nguồn tiền nào sẽ chịu trách nhiệm thanh toán phần chênh lệch làm tròn số trong phép tính phân bổ vốn.
-   Thiết lập các quy tắc xác định cách lập hóa đơn chi phí dự án cho khách hàng bên ngoài và cách tính phí cho các tổ chức nội bộ.
-   Ghi lại các giao dịch vào tài khoản cấp vốn tạm giữ cho đến khi có thể có thêm tiền hoặc cho đến khi bạn quyết định chịu chi phí nội bộ.

Để xác định nhóm thuế nào sẽ liên kết với một giao dịch, hệ thống tìm kiếm mục chỉ định nhóm thuế cho dự án. Nếu không có mục chỉ định nhóm thuế nào được lập ở cấp dự án, thì hợp đồng dự án được tìm kiếm.

### <a name="example-multiple-funding-sources-simple"></a>Ví dụ: Nhiều nguồn tiền (đơn giản)

Bảng sau đây cung cấp các kịch bản quản lý việc phân bổ kinh phí giữa nhiều nguồn tiền. Các kịch bản này được xây dựng dựa trên những giả định sau:

-   Các mục thiết đặt ưu tiên được tính vào việc phân bổ vốn trước khi áp dụng các tiêu chí quy tắc cấp vốn khác.
-   Không có phạm vi ngày nào được chỉ định để xác định khoảng thời gian d khi quy tắc cấp vốn có hiệu lực.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kịch bản</strong></td>
<td><strong>Nguồn tiền</strong></td>
<td><strong>Phần trăm phân bổ</strong></td>
<td><strong>Mức độ ưu tiên phân bổ</strong></td>
</tr>
<tr class="even">
<td>Bạn muốn phân bổ chi phí cho một nguồn tiền cho đến khi hết quỹ, rồi phân bổ chi phí cho nguồn tiền thứ hai cho đến khi hết quỹ và cuối cùng phân bổ phần chi phí còn lại cho nguồn tiền thứ ba.</td>
<td><ul>
<li>Nguồn　tiền　1</li>
<li>Nguồn　tiền　2</li>
<li>Nguồn　tiền　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Bạn muốn phân bổ 75 phần trăm chi phí cho một nguồn tiền và 25 phần trăm cho nguồn tiền thứ hai. Khi một trong hai nguồn tiền đó hết tiền, bạn muốn thanh toán các chi phí còn lại từ nguồn tiền thứ ba.</td>
<td><ul>
<li>Nguồn　tiền　1</li>
<li>Nguồn　tiền　2</li>
<li>Nguồn　tiền　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Bạn muốn phân bổ 75 phần trăm chi phí cho một nguồn tiền và 25 phần trăm cho nguồn tiền thứ hai. Khi một trong hai nguồn tiền đó hết tiền, bạn muốn phân tách phần chi phí còn lại cho nguồn tiền thứ ba và thứ tư.</td>
<td><ul>
<li>Nguồn　tiền　1</li>
<li>Nguồn　tiền　2</li>
<li>Nguồn　tiền　3</li>
<li>Nguồn　tiền　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Bạn muốn phân bổ 25 phần trăm chi phí đầu tiên cho một nguồn tiền và phần chi phí còn lại cho nguồn tiền thứ hai.</td>
<td><ul>
<li>Nguồn　tiền　1</li>
<li>Nguồn　tiền　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Ví dụ: Nhiều nguồn tiền (phức tạp)

Bạn có ba nguồn tiền và muốn sử dụng chúng theo thứ tự sau:

1.  Sử dụng nguồn tiền 2 và nguồn tiền 3 như nhau cho đến khi hết nguồn tiền 2.
2.  Tiếp tục sử dụng nguồn tiền 3 cho đến khi hết.
3.  Sử dụng nguồn 1 sau khi nguồn 3 hết.

Để đạt được mục tiêu này, bạn hãy làm như sau:

-   Thiết lập giới hạn tiền cho nguồn tiền 2 và nguồn tiền 3 theo số tiền tương ứng của chúng.
-   Tạo quy tắc cấp vốn sau đây:
    -   Quy tắc 1 (Ưu tiên 1): Phân bổ 50 phần trăm giao dịch cho nguồn tiền 2 và 50 phần trăm cho nguồn tiền 3.
    -   Quy tắc 2 (Ưu tiên 2): Phân bổ 100% giao dịch cho nguồn tiền 3.
    -   Quy tắc 3 (Ưu tiên 3): Phân bổ 100% giao dịch cho nguồn tiền 1.

Cách thiết lập này có tác dụng vì các giao dịch được đối sánh với các quy tắc và giới hạn để xác định xem có bất kỳ mục nào áp dụng được cho giao dịch không. Nếu không có quy tắc hoặc giới hạn cụ thể nào được áp dụng cho giao dịch, thì quy tắc Tất cả giao dịch sẽ được áp dụng. Quy tắc Tất cả các giao dịch sẽ so khớp tất cả các giao dịch. 

Nếu có một quy tắc khớp với một giao dịch, thì tỷ lệ phần trăm đã được phân bổ trong quy tắc đó sẽ được áp dụng trước, nhưng chỉ sau khi các kết quả so khớp đó được đối sánh với bất kỳ giới hạn nào được thiết lập. Nếu có một giới hạn phù hợp nhưng nguồn tiền đã cạn kiệt, thì quy tắc cấp vốn được liên kết với giới hạn cấp vốn đó sẽ bị bỏ qua và chương trình sẽ đối sánh với quy tắc tiếp theo được áp dụng. 

Trong một số trường hợp, chỉ một phần giao dịch có thể được phân bổ theo một quy tắc. Điều này có thể xảy ra vì số tiền sử dụng đã đạt đến giới hạn khi giao dịch được phân bổ. Trong trường hợp này, chỉ một số tiền nhất định được phân bổ theo quy tắc đó, chẳng hạn như 50 phần trăm cho mỗi nguồn tiền. Đây là trường hợp trong quy tắc 1 được mô tả bên trên trong phần này. Phần còn lại được phân bổ theo quy tắc tiếp theo trong chuỗi. 

Bảng sau đây xem xét chi tiết hơn tình huống này.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Tiêu điểm</strong></td>
<td><strong>Chi tiết</strong></td>
</tr>
<tr class="even">
<td>Quy tắc cấp vốn</td>
<td><ul>
<li>Quy tắc 1 (Ưu tiên 1): Tất cả các giao dịch. Phân bổ 50% nguồn tiền 2 và 50% nguồn tiền 3.</li>
<li>Quy tắc 2 (Ưu tiên 2): Tất cả các giao dịch. Phân bổ 100% nguồn tiền 3.</li>
<li>Quy tắc 3 (Ưu tiên 2): Tất cả các giao dịch. Phân bổ 100% nguồn tiền 1.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Giới hạn cấp vốn</td>
<td><ul>
<li>Giới hạn nguồn tiền 1 = 10.000,00</li>
<li>Giới hạn nguồn tiền 2 = 500,00</li>
<li>Giới hạn nguồn tiền 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Giao dịch 1</td>
<td><strong>Số tiền giao dịch:</strong> 100,00<strong>Nguồn tiền:</strong> Giao dịch chỉ được thanh toán theo quy tắc 1, vì giao dịch được thanh toán đầy đủ sau khi áp dụng quy tắc 1. Giao dịch được cấp vốn đều nhau giữa nguồn tiền 2 và nguồn tiền 3.
<ul>
<li>Nguồn tiền 2: 50,00</li>
<li>Nguồn tiền 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Giao dịch 2</td>
<td><strong>Số tiền giao dịch:</strong> 5.000,00<strong>Nguồn tiền:</strong> Giao dịch được thanh toán theo cả ba quy tắc. <strong>Quy tắc 1</strong>
<ul>
<li>Nguồn tiền 2: 450,00</li>
<li>Nguồn tiền 3: 450,00</li>
</ul>
<strong>Quy tắc 2</strong>
<ul>
<li>Nguồn tiền 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Quy tắc 3</strong>
<ul>
<li>Nguồn tiền 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tổng số tiền được phân phối cho từng nguồn tiền</td>
<td><ul>
<li>Nguồn tiền 1: 3.850,00</li>
<li>Nguồn tiền 2: 500,00</li>
<li>Nguồn tiền 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Quy tắc thanh toán
Khi bạn thương thảo hợp đồng dự án với khách hàng, bạn xác định cách thức và thời điểm có thể lập hóa đơn về khối lượng công việc trong một dự án cho khách hàng. Sau khi bạn thiết lập hợp đồng dự án và dự án, bạn có thể thiết lập quy tắc thanh toán cho dự án. Quy tắc thanh toán được lập dựa trên các điều khoản dự án đã quy định trong hợp đồng dự án. Quy tắc thanh toán mà bạn có thể tạo phụ thuộc vào các điều khoản của hợp đồng dự án và loại dự án, như Thời gian và vật tư hoặc Giá cố định, mà bạn liên kết với quy tắc thanh toán. Bạn có thể tạo nhiều quy tắc thanh toán cho một hợp đồng dự án. Bạn cũng có thể chỉ định một quy tắc thanh toán cho nhiều dự án được liên kết với cùng một hợp đồng dự án và có các điều khoản thanh toán tương tự nhau. 

Bạn có thể thiết lập các loại quy tắc thanh toán sau:

-   **Đơn vị giao hàng** – Lập hóa đơn cho khách hàng khi bạn hoàn thành một đơn vị giao hàng. Bạn xác định đơn vị giao hàng trong hợp đồng.
-   **Tiến độ** – Lập hóa đơn cho khách hàng khi bạn hoàn thành một tỷ lệ cụ thể của dự án. Bạn có thể thiết lập quy tắc thanh toán để tự động tính toán tỷ lệ phần trăm công việc đã hoàn thành hoặc bạn có thể tính toán thủ công tỷ lệ này và số tiền sẽ lập hóa đơn cho khách hàng.
-   **Mốc** – Lập hóa đơn toàn bộ số tiền tương ứng với một mốc dự án khi đạt đến mốc đó cho khách hàng.
-   **Phí** – Lập hóa đơn các dịch vụ của bạn cộng với phí quản lý, thường là tỷ lệ phần trăm của chi phí dịch vụ, cho khách hàng.
-   **Thời gian và vật tư** – Lập hóa đơn giá trị thời gian và vật tư được dùng trong một dự án cho khách hàng.

Đối với tất cả các loại quy tắc thanh toán, bạn có thể chỉ định tỷ lệ phần trăm giữ lại được khấu trừ vào hóa đơn cho khách hàng cho đến khi dự án đạt đến giai đoạn đã thỏa thuận. Tỷ lệ giữ lại thanh toán được quy định trong hợp đồng dự án. Số tiền được tính toán và trừ đi dựa trên tổng giá trị của các dòng trong hóa đơn cho khách hàng. 

Đối với quy tắc thanh toán **Thời gian và vật tư** và **Tiến độ**, bạn có thể chỉ định các danh mục có thể tính phí. Danh mục có thể tính phí cho biết những giao dịch nào cần được đưa vào hóa đơn cho khách hàng. 

Khi bạn đã sẵn sàng lập hóa đơn cho khách hàng, số tiền cần lập hóa đơn cho dự án sẽ được tính toán dựa trên các quy tắc thanh toán và một bản đề xuất hóa đơn dự án sẽ được tạo. 

Các phần sau đây cung cấp ví dụ cho thấy cách thiết lập và quản lý các quy tắc thanh toán cho một dự án.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Ví dụ: Tạo quy tắc thanh toán dựa trên số lượng đơn vị được phân phối

Tổ chức của bạn ký kết thỏa thuận cung cấp tổng cộng năm phiên đào tạo cho nhân viên của khách hàng với chi phí 10.000 mỗi buổi. Bạn lập hóa đơn cho khách hàng sau mỗi buổi đào tạo. 

Khi thiết lập các quy tắc thanh toán cho hợp đồng, bạn sử dụng các giá trị sau:

-   Đơn vị giao hàng là một phiên đào tạo.
-   Đơn giá là 10.000 mỗi phiên đào tạo.
-   Tổng số đơn vị là năm phiên đào tạo.

Khi bạn hoàn thành một phiên đào tạo, bạn có thể tạo hóa đơn 10.000 cho đơn vị đầu tiên đã được cung cấp và gửi hóa đơn cho khách hàng.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Ví dụ: Tạo quy tắc thanh toán dựa trên tỷ lệ phần trăm hoàn thành dự án cụ thể (tính toán thủ công)

Tổ chức của bạn (một công ty tư vấn phần mềm) ký kết thỏa thuận với khách hàng để phát triển một phần của sản phẩm mà khách hàng đang phát triển. Tổ chức của bạn đồng ý cung cấp mã phần mềm trong khoảng thời gian sáu tháng. Khách hàng đồng ý trả cho tổ chức của bạn tổng cộng 100.000 cho công việc này. Bạn tạo quy tắc thanh toán để lập hóa đơn cho khách hàng dựa trên tỷ lệ phần trăm công việc được hoàn thành trong dự án theo như quy định trong hợp đồng.

-   Đến cuối tháng đầu tiên, bạn gặp khách hàng để xác định phần trăm công việc đã hoàn thành. Sau khi bạn và khách hàng xem xét dự án, bạn quyết định rằng dự án đã hoàn thành được 15 phần trăm.
-   Bạn tạo hóa đơn 15.000 (15 phần trăm của 100.000) và gửi cho khách hàng.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Ví dụ: Tạo quy tắc thanh toán dựa trên tỷ lệ phần trăm hoàn thành dự án cụ thể (tính toán tự động)

Tổ chức của bạn (một công ty phát triển phần mềm) đồng ý phát triển gói kế toán tính lương cho một khách hàng với giá 30.000. Khách hàng đồng ý thanh toán cho tổ chức của bạn dựa trên tỷ lệ phần trăm công việc đã hoàn thành. Bạn ước tính rằng chi phí dự án là 20.000. Hợp đồng dự án chỉ định các hạng mục công việc được sử dụng trong quy trình thanh toán. Bạn thiết lập các quy tắc thanh toán tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc đã hoàn thành cho từng hạng mục. Bạn thiết lập ngân sách cho từng hạng mục:

-   **Phát triển** – Chi phí 15.000 và doanh thu 20.000
-   **Cài đặt** – Chi phí 5.000 và doanh thu 10.000

Ở lần đầu tiên bạn tạo hóa đơn cho khách hàng, số tiền trên hóa đơn được tính tự động dựa trên các thông tin sau:

-   Sau một tháng, nhân viên tham gia dự án nộp bảng chấm công cho dự án. Chi phí giờ công của nhân viên là 5.000 cho hạng mục phát triển và 1.000 cho hạng mục cài đặt. Công việc phát triển đã hoàn thành 33% (chi phí thực tế 5.000/chi phí ngân sách 15.000) và công việc cài đặt đã hoàn thành 20% (chi phí thực tế 1.000/chi phí ngân sách 5.000).
-   Số tiền trong hóa đơn được tính tự động là 8.667 (33% của 20.000 + 20% của 10.000).
-   Bạn tạo hóa đơn 8.667 và gửi cho khách hàng.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Ví dụ: Tạo quy tắc thanh toán dựa trên các mốc đã thỏa thuận

Tổ chức của bạn (một công ty tư vấn quản lý) đồng ý thực hiện nghiên cứu thị trường cho một sản phẩm tiêu dùng mà khách hàng định bán. Khách hàng đồng ý sử dụng dịch vụ của bạn trong thời gian ba tháng, bắt đầu từ tháng 3, và đồng ý trả 50.000 cho tổ chức của bạn. Dự án có ba mốc:

-   Mốc 1: Thu thập dữ liệu người tiêu dùng – 31 tháng 3
-   Mốc 2: Phân tích dữ liệu người tiêu dùng – 30 tháng 4
-   Mốc 3: Trình bày đề xuất khả năng tồn tại của sản phẩm – 31 tháng 5

Khách hàng đồng ý trả cho tổ chức của bạn 10.000 ở mốc đầu tiên, 20.000 ở mốc thứ hai và 20.000 ở mốc thứ ba. 

Khi bạn thiết lập hợp đồng dự án, bạn đồng ý xuất hóa đơn cho khách hàng dựa trên mốc thời gian đạt đến. Quy tắc thanh toán được thiết lập với các bước sau:

-   Xác định các mốc dự án.
-   Xác định số tiền sẽ lập hóa đơn cho khách hàng khi đến từng mốc.

Khi đến mốc đầu tiên vào ngày 31/03, bạn đánh dấu mốc là đã hoàn thành, sau đó lập hóa đơn 10.000 và gửi cho khách hàng. Bạn sẽ không thể tạo hóa đơn cho một mốc cho đến khi bạn đã đánh dấu mốc đó là đã hoàn thành.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Ví dụ: Tạo quy tắc thanh toán dựa trên dịch vụ cộng với phí quản lý

Tổ chức của bạn (một công ty tư vấn quản lý) đồng ý thực hiện nghiên cứu thị trường để đánh giá khả năng tồn tại của sản phẩm mà khách hàng (một công ty bán lẻ) đang phát triển. Các điều khoản của thỏa thuận nêu rõ rằng bạn sẽ cung cấp dịch vụ của ba nhà tư vấn quản lý hàng đầu, những người này sẽ tiến hành nghiên cứu trên cơ sở thời gian và vật tư. Khách hàng đồng ý trả 100 mỗi giờ, cộng với phí quản lý 10% cho số giờ tư vấn được tính cho dự án. 

Khi bạn thiết lập hợp đồng dự án, hãy tạo quy tắc thanh toán để thêm phí quản lý 10% vào số giờ tư vấn được tính cho dự án. 

Khi bạn tạo hóa đơn cho khách hàng, khách hàng sẽ bị tính phí quản lý 10% cộng với chi phí cho số giờ tư vấn. Chẳng hạn, nếu ba nhà tư vấn đã làm tổng cộng 200 giờ cho dự án, thì hóa đơn 22.000 sẽ được tạo dựa trên cách tính toán sau:

-   200 giờ với mức giá 100 mỗi giờ = 20.000
-   Phí quản lý 10% = 2.000
-   Tổng số tiền trên hóa đơn = 22.000

Nếu khách hàng phải chịu thuế phí và bạn chọn nhóm thuế bán hàng trong hợp đồng dự án, thì nhóm thuế bán hàng đó sẽ tự động được đưa vào quy tắc thanh toán để xác định phí.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Ví dụ: Tạo quy tắc thanh toán cho giá trị thời gian và vật tư

Tổ chức của bạn (một công ty tư vấn phần mềm) đồng ý cung cấp năm chuyên gia tư vấn kỹ thuật để làm việc trong một dự án phát triển phần mềm cho một khách hàng trong sáu tháng tới. Khách hàng đồng ý trả 150 cho mỗi giờ tư vấn, cộng với chi phí văn phòng phẩm. Tổ chức của bạn sẽ gửi hóa đơn cho khách hàng vào cuối mỗi tháng. 

Khi bạn thiết lập hợp đồng dự án, bạn đồng ý lập hóa đơn thời gian và vật tư cho dự án cho khách hàng mỗi tháng. Bạn tạo quy tắc thanh toán bao gồm các thông tin sau:

-   Thời hạn hợp đồng là sáu tháng.
-   Thời gian tư vấn được tính với mức giá 150 một giờ.
-   Văn phòng phẩm được lập hóa đơn theo chi phí và tổng chi phí cho dự án không được vượt quá 10.000.
-   Bạn tạo hóa đơn cho khách hàng vào cuối mỗi tháng theo lịch trong suốt thời gian dự án.

Trong tháng đầu tiên, các chuyên gia tư vấn đã ghi lại tổng cộng 800 giờ công trong dự án. Chi phí văn phòng phẩm được tính cho dự án là 2.000. Do đó, đến cuối tháng, bạn tạo hóa đơn 122.000, bao gồm 800 giờ với giá 150 mỗi giờ cộng với 2.000 cho văn phòng phẩm.





[!INCLUDE[footer-include](../includes/footer-banner.md)]