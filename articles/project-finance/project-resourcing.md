---
title: Nguồn lực dự án
description: Chủ đề này cung cấp thông tin về nguồn lực dự án.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756992"
---
# <a name="project-resourcing"></a>Nguồn lực dự án

[!include [banner](../includes/banner.md)]

Chủ đề này cung cấp thông tin về nguồn lực dự án.

Một thách thức đối với các nhà quản lý dự án và quản lý nguồn lực trong giai đoạn lập kế hoạch dự án là phân bổ nguồn lực, nơi họ phải xác định và dành nguồn lực chính xác để làm việc trong một dự án. Trong Dynamics 365 Finance, khả năng cung ứng nguồn lực cho dự án cho phép bạn xác định các vai trò được coi là nguồn lực tạm thời có thể được dành cho một hoạt động thuê cụ thể hoặc một phần của hoạt động thuê đó. Loại nguồn lực này cho phép các nhà quản lý dự án và quản lý nguồn lực hoàn thành các nhiệm vụ sau:

- Xác định vai trò có các năng lực cần thiết để dễ dàng khớp các nguồn lực.
- Sử dụng các vai trò để xác định lịch trình tham gia ban đầu dựa trên các nguồn lực dành riêng.
- Ước tính chi phí và xác định ngân sách ban đầu, dựa trên các vai trò và nguồn lực được gán cho một dự án.
- Sử dụng các vai trò để ước tính số lượng dự trữ nguồn lực cần thiết cho mỗi hoạt động thuê.
- Ước tính số lượng nguồn lực cần thiết cho toàn bộ vòng đời của một dự án.
- Soạn thảo cấu trúc phân tích công việc (WBS) bằng cách sử dụng nội dung phân công nguồn lực ban đầu.

[![Vòng đời dự án](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Khi tiến hành lập kế hoạch dự án, có thể thay thế các nguồn lực theo kế hoạch bằng nguồn lực có biên chế. Người quản lý dự án cũng có thể quay lại và cập nhật dự trữ nguồn lực trong bất kỳ giai đoạn nào của dự án.

## <a name="set-up-project-resources"></a>Thiết lập nguồn lực dự án
Bạn phải thiết lập lịch và liên kết nó với nhân viên. Lịch được sử dụng để lập lịch trình cho dự án và thời gian làm việc của các nguồn lực được dành cho dự án. Trong quá trình thiết lập lịch, người quản lý dự án có thể cân bằng tài nguyên trong quá trình tối ưu hóa nguồn lực. Dựa trên lịch trình theo lịch, có thể đưa ra các hạn chế đối với nguồn lực. Bạn có thể thiết lập lịch trên trang **Lịch**.

Khi bạn thiết lập nhân viên làm nguồn lực dự án, bạn có thể chọn từ nhân viên làm việc trong công ty mà bạn đang thiết lập nguồn lực. Ngoài ra, bạn có thể chọn nhân viên từ các công ty khác trong tổ chức của mình. Những nhân viên này được gọi là nguồn lực liên công ty.

Các quy trình sau đây giải thích cách thiết lập một nhân viên làm nguồn lực dự án trong công ty của bạn và cách thiết lập nguồn lực dự án liên công ty.

### <a name="set-up-a-worker-as-a-project-resource"></a>Thiết lập nhân viên làm nguồn lực dự án

1. Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn nhân viên mà bạn đang thêm làm nguồn lực dự án và mở hồ sơ nhân viên.
2. Trên Ngăn hành động, chọn **Dự án** &gt; **Thiết lập** &gt; **Thiết lập dự án**.
3. Chọn lịch rồi đóng trang.

Bạn cũng có thể chỉ định các dự án mặc định cho một nguồn lực như một loại phân công trước. Phân công trước có thể được sử dụng khi người quản lý tài nguyên hoặc người quản lý dự án biết trước dự án mà nguồn lực sẽ thực hiện. Phân công trước cũng có thể dựa trên yêu cầu về người tài trợ dự án hoặc khách hàng. Để phân công trước dự án, trên trang **Chỉ định dự án**, trên tab **Dự án**, trong danh sách **Dự án còn lại**, chọn dự án thích hợp.

### <a name="set-up-an-intercompany-resource"></a>Thiết lập nguồn lực liên công ty

Khi bạn thiết lập một nhân viên làm nguồn lực liên công ty, bạn phải hoàn thành việc thiết lập ở cả công ty cho mượn và công ty mượn.

**Ở công ty cho mượn**

1. Trong Finance, hãy xác minh rằng công ty cho mượn đã được chọn, rồi hoàn thành quy trình trong phần trước đó: "Thiết lập nhân viên làm nguồn lực dự án".
2. Trên trang **Kế toán liên công ty**, chọn **Mới**.
3. Trong trường **ID pháp nhân**, chọn công ty cho mượn. Điền vào các trường còn lại là thích hợp, sau đó chọn **Lưu**.
4. Trên trang **Giá chuyển nhượng**, chọn **Mới**.
5. Trong trường **Pháp nhân mượn**, chọn công ty thích hợp.
6. Để chỉ cho mượn nguồn lực mà bạn tạo ở đầu phần này, trong trường **Nguồn lực**, chọn tên của nguồn lực mà bạn đã tạo. Để hiển thị toàn bộ nguồn lực của công ty cho mượn cho công ty mượn, hãy để trống trường **Nguồn lực**.
7. Trên trang **Tham số quản lý dự án và kế toán**, trên tab **Liên công ty**, đặt tùy chọn **Bật lập lịch và bảng chấm công nguồn lực** thành **Có**.

**Ở công ty mượn**

- Trên trang **Danh sách nguồn lực**, trong bộ lọc tìm kiếm, hãy nhập tên nguồn lực mà bạn đã tạo cho công ty cho mượn, để xác minh rằng tên đó có trong danh sách nguồn lực dành cho công ty mượn hay không.

## <a name="manage-resource-competencies"></a>Quản lý năng lực của nguồn lực
Năng lực của nguồn lực là một phần thiết yếu trong quản lý nguồn lực. Năng lực có thể được sử dụng làm cơ sở để xác định các nguồn lực có sự cân bằng chính xác về kỹ năng, giáo dục, chứng nhận và kinh nghiệm dự án. Bạn nên thiết lập thông tin này cho từng nguồn lực và cập nhật nó một cách thường xuyên. Bằng cách này, bạn có thể tối đa hóa khả năng khi các năng lực của nguồn lực cụ thể được khớp trong quá trình phân công nguồn lực dự án.

[![Ví dụ về kỹ năng, chứng chỉ, học vấn và kinh nghiệm dự án](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Các quy trình sau đây giải thích cách thiết lập một số năng lực cho nguồn lực.

Để thiết lập năng lực cho nhân viên, bạn có thể sử dụng trang danh sách **Nhân viên** trong Nhân sự hoặc trang danh sách **Nguồn lực** trong Quản lý dự án và kế toán. Đối với các quy trình sau đây, trang danh sách **Nhân viên** trong Nhân sự được sử dụng.

### <a name="set-up-competencies-certificates"></a>Thiết lập năng lực: Chứng chỉ

1. Trên trang danh sách **Nhân viên**, chọn dòng cho nhân viên để thêm thông tin chứng chỉ.
2. Trên Ngăn hành động, trên tab **Nhân viên**, trong nhóm **năng lực**, chọn **Chứng chỉ**.
3. Chọn **Mới** rồi trong trường **Loại chứng chỉ**, chọn **PMP**.
4. Trong trường **Ngày bắt đầu**, chọn **10/1/2015** rồi chọn **Lưu**.

### <a name="set-up-competencies-skills"></a>Thiết lập năng lực: Kỹ năng

1. Trên trang danh sách **Nhân viên**, hãy đảm bảo rằng nhân viên mà bạn đã sử dụng trong quy trình trước đó vẫn được chọn. Sau đó, trên Ngăn hành động, trên tab **Nhân viên**, trong nhóm **Năng lực**, chọn **Kỹ năng**.
2. Chọn **Mới**.
3. Trong trường **Kỹ năng**, chọn **Quản lý dự án**.
4. Trong trường **Cấp độ**, chọn **5 Chuyên gia**.
5. Trong trường **Ngày cấp độ**, chọn **1-/14/2014**.
6. Trong trường **Số năm kinh nghiệm**, nhập **10**.
7. Chọn**Lưu** rồi đóng trang.

## <a name="create-a-new-project"></a>Tạo dự án mới
1. Trên trang **Quản lý dự án**, chọn **Dự án mới** rồi nhập các giá trị sau đây:

    - **Loại dự án:** Thời gian và vật liệu
    - **Tên dự án:** Nâng cấp XYZ Giai đoạn 2
    - **Nhóm dự án:** TM\_WIP
    - **ID hợp đồng dự án:** 00000002

2. Chọn **Tạo dự án**.

### <a name="assign-a-resource-to-a-project"></a>Chỉ định nguồn lực cho dự án

1. Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn bản ghi cho nhân viên mà bạn đã thiết lập năng lực và mở bản ghi nhân viên.
2. Trên Ngăn hành động, trên tab **Dự án**, trong nhóm **Thiết lập**, chọn **Chỉ định dự án**.
3. Trên trang **Phân công dự án xác thực nguồn lực**, trên tab **Dự án**, trong trường **Thêm dự án vào các dự án đã chọn**, lọc trên dự án **Nâng cấp XYZ Giai đoạn 2**.
4. Trong ngăn **Dự án còn lại**, chọn dự án rồi chọn nút mũi tên để thêm vào ngăn **Dự án đã chọn**.

Bạn cũng có thể chỉ định các thể loại cho nguồn lực mà mình cần. Thể loại là **Chi phí** hoặc **Doanh thu**. Thể loại được xác định bởi tổ chức của bạn. Nếu không có thể loại nào được chỉ định cho nguồn lực, Finance sẽ tra cứu thể loại mặc định trên giá theo giờ để biết chi phí và doanh thu.

### <a name="set-up-project-resource-and-role-characteristics"></a>Thiết lập đặc điểm vai trò và nguồn lực dự án

Người quản lý dự án có thể sử dụng chức năng nguồn lực dự án để tạo các vai trò cần thiết cho dự án. Có thể sử dụng vai trò nếu nguồn lực đã xác nhận vẫn là không xác định khi nguồn lực đang được dự trữ. Các vai trò có thể được dự trữ tạm thời dưới dạng nguồn lực đã lập kế hoạch để bạn có thể tiếp tục các giai đoạn lập kế hoạch dự án.

[![Ví dụ về vai trò](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Tình huống:** Contoso được thuê để hoàn thành một dự án Thời gian và vật liệu có điều lệ dự án đã được phê duyệt. Người quản lý dự án cấp dưới vẫn đang hoàn thành phạm vi của dự án. Người quản lý tài nguyên hiện đang xác định các nguồn lực cụ thể sẽ được dự trữ để thực hiện dự án mới. Do tính chất quan trọng của dự án, nhà tài trợ dự án đã yêu cầu Người quản lý dự án cấp cao là một trong các vai trò. Người quản lý tài nguyên phải có được nguồn lực mới và xác định vai trò trong hệ thống trong trường hợp người quản lý dự án cấp dưới yêu cầu thông tin tài nguyên trong quá trình lập kế hoạch dự án.

Các bước sau đây cho thấy cách người quản lý nguồn lực có thể thiết lập vai trò Người quản lý dự án cấp cao và liên kết các đặc điểm của nguồn lực với vai trò đó. Sau đó, vai trò có thể được sử dụng để tìm kiếm các nguồn lực có sẵn phù hợp với năng lực của nguồn lực được yêu cầu.

1. Trên trang **Thiết lập vai trò**, chọn **Mới** rồi nhập các giá trị sau đây:

    - **ID vai trò:** Người quản lý dự án cấp cao
    - **Mô tả:** Người quản lý dự án cấp cao

2. Chọn **Tạo**.
3. Chọn vai trò **Người quản lý dự án cấp cao** rồi chọn **Đặt cấu hình đặc điểm**.
4. Trong trường **Loại đặc điểm**, chọn **Kỹ năng**.
5. Trong trường **Đặc điểm có sẵn**, nhập kỹ năng để tìm kiếm.
6. Trong trường **Loại đặc điểm**, chọn **Chứng chỉ**.
7. Trong trường **Đặc điểm có sẵn**, nhập loại chứng chỉ để tìm kiếm.

### <a name="assign-a-project-resource-to-a-project"></a>Chỉ định nguồn lực dự án cho dự án

1. Trên trang **Tất cả dự án**, chọn dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Trên tab **Nhóm dự án và lập lịch trình**, chọn **Thêm**.
3. Trong trường **Vai trò**, chọn **Thành viên nhóm**.
4. Chọn **Đặt từ lịch**.
5. Trên trang **Khả năng dùng nguồn lực**, chọn **Thiết đặt dạng xem**.
6. Trên trang **Điều chỉnh thiết đặt dạng xem**, nhập các giá trị sau đây:

    - **Định dạng cho dạng xem phạm vi ngày:** Ngày
    - **Hiển thị mô tả tình trạng rảnh/bận:** Có
    - **Hiển thị năng lực còn lại:** Có

7. Trong danh sách nguồn lực, chọn một nguồn lực.
8. Chọn **Đặt trước chắc chắn** và **Năng lực đầy đủ**.


### <a name="assign-a-resource-to-a-default-role"></a>Chỉ định nguồn lực cho vai trò mặc định

Giúp các nhà quản lý dự án hoặc nguồn lực xem chi tiết các nguồn lực có thể được dành riêng cho một dự án. Bạn có thể liên kết một vai trò mặc định với một tài nguyên hiện có hoặc một tài nguyên mới có được. Ví dụ: khi Daniel được thuê, anh ấy có kinh nghiệm và kỹ năng để đảm nhiệm vai trò Phân tích viên kinh doanh. Người quản lý nguồn lực đã gán vai trò này là vai trò mặc định của Daniel. Do đó, người quản lý nguồn lực đã thêm Daniel vào một nhóm các phân tích viên kinh doanh sẵn sàng làm việc trong các dự án.

Trong quá trình dự trữ nguồn lực, người quản lý dự án có thể lọc các nguồn lực vai trò có sẵn để thực hiện dự án. Họ có thể sử dụng thông tin này như một tiêu chí khi thực hiện phân tích quyết định đa tiêu chí trong quá trình thực hiện nguồn lực. Họ cũng có thể thêm các đặc điểm nguồn lực khác vào bộ lọc để tìm kiếm các tài nguyên có kỹ năng, trình độ học vấn và kinh nghiệm cụ thể cho một dự án nhất định.

**Tình huống:** Một dự án được phê duyệt đã bắt đầu và vai trò Người quản lý dự án cấp cao được dự trữ như một nguồn lực theo kế hoạch trong giai đoạn lập kế hoạch dự án. Người quản lý nguồn lực hiện đã có được một nguồn lực để thực hiện vai trò Người quản lý dự án cấp cao.

1. Trên trang **Danh sách nguồn lực**, chọn **Daniel Goldschmidt**.
2. Trên trang **Vai trò nguồn lực**, chọn **Mới** rồi nhập các giá trị sau đây:

    - **Có hiệu lực:** Nhập ngày hiện tại.
    - **Hết hạn:** Nhập **Không bao giờ**.
    - **Vai trò:** Nhập **Người quản lý dự án cấp cao**.

3. Chọn**Lưu** rồi đóng trang.
4. Trên tab **Năng lực**, thêm kỹ năng **Quản lý dự án** và chứng chỉ **PMP**.

## <a name="set-up-role-based-pricing"></a>Thiết lập giá dựa trên vai trò
Tất cả chi phí, giá bán và giá chuyển nhượng có thể được thiết lập cho các vai trò.

1. Trên trang **Giá bán (giờ)**, chọn **Mới** rồi nhập ngày có hiệu lực.
2. Trong cột **Vai trò**, chọn vai trò.
3. Trong cột **Giá**, nhập giá cho vai trò nguồn lực đã chọn.

## <a name="form-a-project-team"></a>Tạo nhóm dự án
Để sử dụng các vai trò đã được thiết lập trước đó trong một dự án, người quản lý dự án phải liên kết các vai trò đó với dự án. Có thể gán nhiều vai trò cho một dự án. Để tránh nhầm lẫn, các vai trò này được tự động gắn nhãn trong quá trình dự trữ. Ví dụ: nếu người quản lý dự án yêu cầu ba kỹ sư phần mềm, thì ba vai trò Kỹ sư phần mềm có nhãn là **kỹ sư phần mềm 1**, **kỹ sư phần mềm 2** và **kỹ sư phần mềm 3** sẽ được tạo tự động. Nếu các đặc điểm của vai trò đã được thiết lập cho vai trò, thì chúng được áp dụng như một bộ lọc trong quá trình tìm kiếm nguồn lực. Các đặc điểm bổ sung có thể được thêm vào theo yêu cầu để tinh chỉnh thêm nội dung tìm kiếm.

Cài đặt dạng xem cũng có thể được tùy chỉnh để mang lại dạng xem tốt hơn về tình trạng rảnh/bận của nguồn lực. Có các tùy chọn để hiển thị tình trạng rảnh/bận theo giờ, ngày, tuần, tháng, quý và năm. Ngoài ra, còn có một tùy chọn để hiển thị năng lực sẵn sàng và còn lại của nguồn lực. Tùy chọn này hữu ích cho việc quản lý thời gian, khi bạn ước tính thời gian sẵn có cho các hoạt động hoặc tình trạng rảnh/bận của nguồn lực.

Người quản lý dự án có thể chọn một vai trò trên trang và sau đó, nếu có sẵn một nguồn lực phù hợp với yêu cầu, hãy chọn dự trữ nguồn lực để thực hiện vai trò đó. Lưu ý rằng không cần dự trữ nguồn lực tại thời điểm này trong giai đoạn lập kế hoạch. Khi tạo một WBS, bạn có thể thay các vai trò bằng nguồn lực có biên chế cho dự án. Nếu vai trò được thay bằng nguồn lực có biên chế trong WBS, thiết lập nguồn lực sẽ tự động cập nhật danh sách và lịch trình của nhóm dự án.

[![Danh sách nhóm dự án bao gồm cả vai trò và nguồn lực thực tế](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Người quản lý dự án có nhiều tùy chọn khác nhau để đặt trước nguồn lực cho một dự án, chẳng hạn như **Năng lực còn lại**, **Năng lực đầy đủ**, **Phần trăm năng lực** và **Chỉ định giờ**. Các tùy chọn đặt trước này có thể bị hủy bỏ bất cứ lúc nào nếu việc phân công nguồn lực thay đổi. Hai loại đặt trước được hỗ trợ:

- **Đặt trước chắc chắn** – Việc dự trữ nguồn lực đã được phê duyệt và xác nhận để tiến hành thuê trong thời gian quy định.
- **Đặt trước dự kiến** – Việc dự trữ nguồn lực được dự kiến thiết lập để tiến hành thuê trong thời gian quy định.

Quy trình sau đây giải thích cách tạo nhóm dự án.

### <a name="create-a-project-team"></a>Tạo nhóm dự án

1. Trên trang danh sách **Tất cả dự án**, chọn dự án rồi chọn **Chỉnh sửa**.
2. Trên tab **Nhóm dự án và lập lịch trình**, trong trường **Lên lịch ngày kết thúc**, nhập ngày bắt đầu lịch trình cộng thêm một tháng. Ví dụ: nếu ngày bắt đầu lịch trình là ngày 24 tháng 6 năm 2017 (24/06/2017), hãy nhập **24/07/2017**.
3. Chọn **Thêm**.
4. Trong ngăn **Thêm vai trò vào dự án**, trong trường **Vai trò**, chọn **Người quản lý dự án cấp cao**.
5. Lựa chọn **Năng lực cần thiết**.
6. Trên trang **Chọn đặc điểm**, các đặc điểm mà bạn đã thiết lập cho vai trò Người quản lý dự án cấp cao được chọn theo mặc định. Chọn **OK**.
7. Trên trang **Thêm vai trò vào dự án**, trong trường **Số lượng tài nguyên**, nhập **1**.
8. Trong trường **Nguồn lực**, phần tra cứu hiển thị tất cả nguồn lực có năng lực cần thiết. Chọn **Daniel Goldschmidt** rồi chọn **Tạo**.
9. Trên trang **Dự án**, chọn **Thêm**.
10. Trong ngăn **Thêm vai trò vào dự án**, trong trường **Vai trò**, chọn **Thành viên nhóm**. Trong trường **Số nguồn lực**, nhập **5**.
11. Chọn **Tạo**.
12. Trên trang **Dự án**, chọn **Đáp ứng nguồn lực**.

## <a name="resource-capacity-synchronization"></a>Đồng bộ hóa năng lực của nguồn lực
Các quy trình đồng bộ hóa nguồn lực giúp đảm bảo rằng thông tin cho lịch lịch và lịch cơ sở sẽ dần đi vào quá trình lập lịch trình nguồn lực dự án. Nếu lịch bị thay đổi, các quy trình sẽ thực hiện cập nhật bắt buộc đối với việc lập lịch trình các nguồn lực dự án. Các quy trình cũng giúp cải thiện hiệu suất, vì thông tin nguồn lực của lịch được đồng bộ hóa trước. Do đó, việc cập nhật thông tin lập lịch nguồn lực diễn ra nhanh hơn. Chúng tôi khuyên bạn nên lập lịch các quy trình theo loạt thay vì từng lần một. Nếu không, ai đó có thể quên những ngày được bao gồm khi thông tin được đồng bộ hóa lần gần nhất. Nếu các ngày bao gồm không được sử dụng, khoảng trống có thể xảy ra trong quá trình đồng bộ hóa ngày.

![Đồng bộ hóa lịch](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Đồng bồ hóa tổng hợp năng lực của nguồn lực

Quá trình đồng bộ hóa được thiết kế để đồng bộ hóa tất cả thông tin lịch nguồn lực. Thông tin này bao gồm thông tin lịch cơ sở về bất kỳ thay đổi nào đối với bảng năng lực lịch nguồn lực của dự án. Nếu các nguồn lực mới được thêm vào dự án, quá trình đồng bộ hóa sẽ đảm bảo rằng thông tin lịch cập nhật có sẵn. Việc đồng bộ hóa này có thể được thực hiện bất cứ lúc nào.

Chúng tôi khuyên bạn nên sử dụng loạt. Các tùy chọn có sẵn trong quá trình đồng bộ hóa các mục dự trữ năng lực.

1. Chọn **Quản lý dự án và kế toán** &gt; **Định kỳ** &gt; **Đồng bộ hóa năng lực** &gt; **Đồng bộ hóa tổng hợp năng lực của nguồn lực**.
2. Thiết lập các tùy chọn trong bảng sau.

    | Tùy chọn      | Mô tả |
    |-------------|-------------|
    | Mã thời kỳ | Tùy ý chọn mã khoảng ngày của sổ cái chung để đặt ngày bắt đầu và ngày kết thúc cho quá trình đồng bộ hóa cho tổng hợp năng lực của nguồn lực. |
    | Ngày bắt đầu  | Nhập ngày bắt đầu cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực. |
    | Ngày kết thúc    | Nhập ngày kết thúc cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực. |

[![Quá trình đồng bộ hóa](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Thiết lập vai trò trên các mẫu WBS
Người quản lý dự án có thể thiết lập các mẫu WBS mà họ có thể áp dụng khi tạo một WBS cho các dự án mới. Người quản lý dự án có thể thêm vai trò khi họ tạo mẫu. Sử dụng quy trình sau để gán một vai trò cho mẫu WBS.

1. Chọn **Quản lý dự án và kế toán** &gt; **Thiết lập** &gt; **Dự án** &gt; **Mẫu cấu trúc phân tích công việc**.
2. Chọn **Chi tiết** cho mẫu WBS đã chọn.
3. Chọn một nhiệm vụ trong danh sách, trong **Vai trò**, chọn một vai trò để gán cho nhiệm vụ.

### <a name="work-with-a-wbs"></a>Làm việc với WBS

Bạn có thể tạo một WBS mới hoặc sao chép WBS từ một mẫu WBS hiện có. Người quản lý dự án có thể dễ dàng quản lý nguồn lực bằng cách gán vai trò cho các nhiệm vụ mới trên WBS. Có thể thay thế vai trò sau khi thu được nguồn lực hoặc sau khi nguồn lực đã xác định thực hiện nhiệm vụ được xác định. Tính linh hoạt này cho phép nhà quản lý dự án thực hiện các nhiệm vụ sau:

- Xác định số lượng nguồn lực yêu cầu cho các gói công việc WBS.
- Ước tính chi phí dự án.
- Xác định ngân sách sơ bộ.
- Ước tính khoảng thời gian hoạt động, dựa trên vai trò và nguồn lực.
- Xây dựng một số kế hoạch quản lý dự án, dựa trên thông tin dự án có sẵn.

Các tùy chọn bổ sung đã được thêm vào WBS để sử dụng tốt hơn chức năng nguồn lực.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tùy chọn</th>
<th>Mô tả</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gán nguồn lực</td>
<td>Xem các nguồn lực được chỉ định, ngày, số giờ và loại đặt trước cho các nhiệm vụ trên WBS.</td>
</tr>
<tr class="even">
<td>Tự động tạo nhóm</td>
<td>Tự động thêm nguồn lực theo kế hoạch bằng cách sử dụng các vai trò được liên kết với một nhiệm vụ. Finance tự động đề xuất các nguồn lực theo kế hoạch bằng cách sử dụng phân tích quyết định đa tiêu chí dựa trên vai trò. Sau khi các vai trò và nhân công (giờ) đã được thiết lập cho các nhiệm vụ trong WBS và sau khi cấu trúc đã được phát hành, hãy chọn <strong>Tự động tạo nhóm</strong>. Số lượng nguồn lực cần thiết được thêm vào WBS và tab <strong>Lập lịch trình dự án và nhóm</strong>.</td>
</tr>
<tr class="odd">
<td>Nguồn lực (danh sách thả xuống)</td>
<td>Trên trang <strong>Khởi chạy phân công nguồn lực</strong>, bạn có thể chọn nguồn lực để đặt trước chắc chắn hoặc đặt trước dự kiến, dựa trên khoảng thời gian cụ thể. Bạn có thể điều chỉnh thiết đặt dạng xem để xem và thiết lập khoảng thời gian của hoạt động nguồn lực. Bạn có thể chọn và chỉ định nguồn lực ở cấp độ gói công việc bằng cách sử dụng các tùy chọn sau:
<ul>
<li><strong>Chấp nhận</strong> – Xác nhận các thay đổi đối với nguồn lực được gán cho một nhiệm vụ.</li>
<li><strong>Hủy</strong> – Hủy các thay đổi đối với nguồn lực được gán cho một nhiệm vụ.</li>
<li><strong>Gán tự động</strong> – Một nguồn lực biên chế có vai trò phù hợp được tự động chọn và gán cho nhiệm vụ đã chọn.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Trên trang **Tất cả dự án**, chọn dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Chọn **Kế hoạch** &gt; **Hoạt động** &gt; **Cấu trúc phân tích công việc**.
3. Chọn **Mới** để thêm các hoạt động cấp độ một sau đây vào WBS:

    - Bắt đầu
    - Lập kế hoạch
    - Đang thực thi
    - Giám sát và kiểm soát
    - Đóng

4. Thiết lập ngày và nhân công (số giờ) như trong hình minh họa sau.

    [![Thiết lập ngày và nhân công](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Chọn dòng nhiệm vụ **Bắt đầu** rồi trong trường **Vai trò**, chọn **Người quản lý dự án cấp cao**.
6. Chọn **Xuất bản**.
7. Trên cùng một dòng, trong trường **Nguồn lực**, chọn **Daniel Goldschmidt** rồi chọn **Chấp nhận**.
8. Chọn dòng công việc **Lập kế hoạch**, rồi trong trường **Vai trò**, chọn **Phân tích viên kinh doanh**.
9. Chọn **Phát hành** rồi chọn **Tự động tạo nhóm**.
10. Trong hộp thông báo xuất hiện, chọn **Có**.
11. Trong trường **Nguồn lực**, xác minh rằng giá trị là **Phân tích viên kinh doanh 1**.
12. Đối với nguồn lực **Phân tích viên kinh doanh 1**, mở mục tra cứu rồi chọn **Triển khai phân công nguồn lực**. Sau đó, chọn nhân viên cho nhiệm vụ.
13. Chọn **Gán dự kiến** &gt; **Năng lực đầy đủ**.

    > [!NOTE] 
    > Bạn không nhận được cảnh báo rằng nguồn lực được chỉ định hiện là 2, vì số lượng nguồn lực vẫn là 1.

14. Trên trang **Cấu trúc phân tích công việc**, xác thực phân công nguồn lực trên WBS rồi chọn **Lưu**.

## <a name="resource-fulfillment-for-planned-resources"></a>Đáp ứng nguồn lực cho nguồn lực theo kế hoạch
Người quản lý dự án có thể lập kế hoạch các vai trò nguồn lực cần thiết cho một dự án. Người quản lý nguồn lực sẽ xem các nguồn lực theo kế hoạch này là yêu cầu trên trang **Đáp ứng nguồn lực** và có thể chỉ định nguồn lực thực tế.

1. Trên trang **Tất cả dự án**, chọn dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Chọn **Dự án** rồi chọn **Chỉnh sửa**.
3. Trên tab **Nhóm dự án và lập lịch trình**, chọn **Thêm**.
4. Trong hộp thoại **Thêm vai trò**, chọn vai trò **Kỹ sư phát triển phần mềm**.
5. Chọn**Tạo** rồi đóng trang dự án.
6. Trên trang **Đáp ứng nguồn lực**, chọn **Kỹ sư phát triển phần mềm 1** cho dự án **Nâng cấp XYZ Giai đoạn 2**.
7. Chọn nhân viên, sau đó chọn **Gán**.
8. Xác minh rằng dòng cho **Kỹ sư phát triển phần mềm 1** đã được loại bỏ cho trong **Dự án nâng cấp XYZ Giai đoạn 2**.
9. Trên tab **Nhóm dự án và lập lịch trình**, đối với dự án **Nâng cấp XYZ Giai đoạn 2**, hãy xác minh rằng nhân viên mà bạn chọn trong bước trước đó đã được thêm làm **Kỹ sư phát triển phần mềm**.

## <a name="requests-for-project-resources"></a>Yêu cầu nguồn lực dự án
Chức năng lập lịch trình nguồn lực dự án chỉ cho phép người quản lý nguồn lực phân phối nguồn lực biên chế trong hoạt động thuê hoặc dự án. Để bật chức năng này, hãy hoàn thành các nhiệm vụ sau hoặc xác minh rằng chúng đã được hoàn thành:

- Thiết lập chuỗi số.
- Thiết lập quy trình công việc kế toán và quản lý dự án.
- Bật quy trình công việc yêu cầu nguồn lực.

Sau khi hoàn thành các nhiệm vụ liên trước, bạn có thể hoàn thành các nhiệm vụ sau theo yêu cầu:

- Tạo một yêu cầu nguồn lực từ nguồn lực biên chế đã đặt trước dự kiến.
- Giám sát yêu cầu nguồn lực.
- Thực hiện các đề nghị nguồn lực.
- Yêu cầu nguồn lực biên chế từ WBS.
- Đặt trước nguồn lực cho dự án mà không có yêu cầu về nguồn lực biên chế.

## <a name="monitor-project-teams"></a>Giám sát các nhóm dự án
1. Trên trang **Tất cả dự án**, chọn liên kết **ID dự án** cho dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Trên **Nhóm dự án và lập lịch trình** FastTab, xác minh rằng các nguồn lực dự án được liệt kê là chính xác.
