---
title: Đặt cấu hình quản lý chi phí
description: Bài viết này mô tả những cân nhắc và quyết định mà bạn phải thực hiện trong quá trình lập kế hoạch trước khi đặt cấu hình Quản lý chi phí trong Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007487"
---
# <a name="configure-expense-management"></a>Đặt cấu hình quản lý chi phí

Chủ đề này mô tả những cân nhắc và quyết định mà bạn phải thực hiện trong quá trình lập kế hoạch trước khi đặt cấu hình Quản lý chi phí. Trong Quản lý chi phí, bạn có thể lưu trữ thông tin về phương thức thanh toán, tiêu chuẩn đi lại, báo cáo chi phí, chính sách, v.v.

Bởi vì nhiều quyết định mà bạn đưa ra khi lập kế hoạch cấu hình cho Quản lý chi phí dựa trên hệ thống cấp bậc và cấu trúc tài chính của tổ chức bạn, bạn phải tham khảo các tài liệu lập kế hoạch cho các lĩnh vực đó.

## <a name="intercompany-expenses"></a>Chi phí liên công ty

Khi kích hoạt chi phí liên công ty, bạn cho phép các pháp nhân và nhân viên chịu chi phí thay mặt cho một pháp nhân khác và thu tiền thanh toán từ pháp nhân lao động trong tổ chức của bạn. Ví dụ: một nhân viên trong pháp nhân A hoàn thành một dự án cho pháp nhân B và dự án phát sinh các chi phí liên quan đến việc đi lại. Nếu chi phí liên công ty được kích hoạt, thì nhân viên có thể gửi báo cáo chi phí sẽ đăng chi phí đó cho pháp nhân B và chi phí phải do pháp nhân A thanh toán. Nếu tổ chức của bạn không có nhiều pháp nhân, bạn không phải kích hoạt chi phí liên công ty.

**Quyết định:** Bạn có muốn kích hoạt chi phí liên công ty không?

## <a name="financial-management"></a>Quản lý tài chính

Quản lý chi phí được tích hợp chặt chẽ với quản lý tài chính của tổ chức bạn. Rất nhiều cấu hình của bạn cho Quản lý chi phí sẽ dựa trên các quyết định mà bạn đã đưa ra về tài chính của tổ chức bạn. Các phần sau đây mô tả những lĩnh vực khác nhau yêu cầu lập kế hoạch và quyết định, dựa trên các quyết định tài chính của tổ chức bạn và hướng dẫn từ nhóm lãnh đạo của bạn.

### <a name="per-diems"></a>Công nhật

Bạn phải xác định công tác phí của nhân viên mà tổ chức của bạn cung cấp. Vì công tác phí thường được sử dụng để trang trải các chi phí như ăn uống, chỗ ở và các chi phí phát sinh khác, bạn có thể tạo quy tắc cho phụ cấp công tác phí mà tổ chức của bạn cung cấp. mức công tác phí có thể dựa trên thời gian trong năm, địa điểm đến hoặc cả hai. Khi bạn xác định quy tắc công tác phí, bạn có thể chỉ định rằng tỷ lệ phần trăm công tác phí sẽ được giữ lại nếu người lao động nhận được các bữa ăn hoặc dịch vụ miễn phí. Bạn cũng có thể xác định các bậc mức công tác phí để đặt số giờ tối thiểu và tối đa mà mức công tác phí có thể áp dụng cho việc đi lại của nhân viên.

**Quyết định:**

- Quy tắc công tác phí mặc định cho ngày đầu tiên và ngày cuối cùng:

    - Số giờ tối thiểu mà một nhân viên có thể yêu cầu trong một ngày mà vẫn nhận được công tác phí là bao nhiêu?
    - Có giảm số lượng được cung cấp cho các bữa ăn của ngày đầu tiên và ngày cuối cùng không? Nếu có giảm thì phần trăm giảm là bao nhiêu?
    - Có giảm số lượng được cung cấp cho chi phí khách sạn của ngày đầu tiên và ngày cuối cùng không? Nếu có giảm thì phần trăm giảm là bao nhiêu?
    - Có giảm số lượng được cung cấp cho các chi phí khác phát sinh vào ngày đầu tiên và ngày cuối cùng không? Nếu có giảm thì phần trăm giảm là bao nhiêu?

- Quy tắc công tác phí mặc định:

    - Ví dụ: Có giảm phần trăm phụ cấp công tác phí cho mỗi bữa ăn nếu bữa ăn đó là miễn phí không? Nếu có giảm thì phần trăm giảm cho mỗi bữa ăn là bao nhiêu?
    - Mức giảm tiền ăn được tính theo ngày, theo chuyến đi hay theo số bữa ăn trong ngày?
    - Số tiền công tác phí nên được làm tròn theo cách thông thường hay làm tròn tăng?
    - Công tác phí được tính theo chu kỳ 24 giờ hay theo ngày dương lịch?

- Quy tắc công tác phí dựa trên vị trí:

    - Mức công tác phí có thay đổi theo vị trí không? Bao gồm những vị trí nào?
    - Nếu mức công tác phí thay đổi theo vị trí thì đối với từng vị trí, tỷ lệ phần trăm được cung cấp cho các loại chi phí sau:

        - Bữa ăn
        - Khách sạn
        - Chi phí khác

### <a name="expense-management-journals-and-accounts"></a>Nhật ký và tài khoản quản lý chi phí

Quản lý chi phí yêu cầu bạn sử dụng nhiều nhật ký và tài khoản. Ví dụ: bạn phải quyết định xem cùng một tài khoản có được sử dụng cho các xung đột tạm ứng tiền mặt và thẻ tín dụng hay không.

**Quyết định:**

- Các báo cáo chi phí đã được phê duyệt được đăng lên nhật ký sổ cái nào?
- Tài khoản nào dùng để ứng trước tiền mặt?
- Có nên đăng ứng tiền mặt ngay lập tức không?

### <a name="payment-methods"></a>Phương thức thanh toán

Khi bạn cho phép nhân viên thanh toán chi phí thay mặt cho doanh nghiệp của mình, bạn phải xác định các phương thức thanh toán mà nhân viên được phép sử dụng. Ví dụ: bạn có thể cho phép nhân viên sử dụng tiền mặt hoặc thẻ tín dụng của công ty. Bạn cũng có thể cho phép nhân viên sử dụng thẻ tín dụng cá nhân, sau đó hoàn tiền cho nhân viên. Bạn phải đưa ra các quyết định sau cho từng phương thức thanh toán mà bạn cho phép.

**Quyết định:**

- Những phương thức thanh toán nào được phép?
- Ai sở hữu chi phí phương thức thanh toán?
- Có loại tài khoản bù trừ không? Nếu có một loại tài khoản bù trừ, loại tài khoản đó là gì?
- Nếu có một tài khoản bù trừ, tài khoản đó là gì?
- Nếu phương thức thanh toán là thẻ tín dụng, phương thức thanh toán chỉ nên được sử dụng với các giao dịch nhập khẩu?

### <a name="expense-categories-and-shared-categories"></a>Danh mục chi phí và danh mục chia sẻ

Khi nhân viên tạo báo cáo chi phí, mỗi khoản chi phí mà họ ghi lại phải được liên kết với một loại chi phí. Các danh mục chi phí có nguồn gốc từ các danh mục dùng chung có thể được chia sẻ giữa các pháp nhân trong tổ chức của bạn. Các danh mục này cũng có thể được chia sẻ trong Kế toán và quản lý dự án, tùy thuộc vào cách tổ chức của bạn được xác định. Dựa trên định nghĩa về tổ chức của bạn và hướng dẫn từ nhóm thực hiện, bạn phải xác định xem các danh mục được sử dụng trong quản lý Chi phí sẽ chỉ được sử dụng trong Quản lý chi phí hay nên được dùng chung giữa Quản lý dự án và Quản lý chi phí và kế toán. Lưu ý rằng các danh mục này có thể được chia sẻ giữa Dự án và chi phí hoặc Dự án và sản xuất, nhưng không được chia sẻ giữa Chi phí và Sản xuất. Bạn phải đưa ra các quyết định sau cho từng danh mục chi phí.

**Quyết định:**

- Thể loại chi phí là gì? Ví dụ bao gồm các danh mục cho chuyến bay, khách sạn hoặc số dặm.
- Danh mục chi phí cũng có thể được sử dụng trong Quản lý dự án và kế toán không?
- Loại chi phí là gì?
- Phương thức thanh toán mặc định cho loại chi phí là gì?
- Các khoản chi trong danh mục chi phí có phải được chia thành từng khoản không?
- Tài khoản chính mặc định cho loại chi phí là gì?
- Nhóm thuế bán hàng mặc định cho danh mục chi phí là gì?
- Các phương thức thanh toán bổ sung có được phép cho loại chi phí không? Nếu cho phép các phương thức thanh toán bổ sung, chúng là gì?
- Có danh mục phụ nào trong danh mục chi phí này không? Nếu có danh mục phụ, bạn cũng phải đưa ra các quyết định sau:

    - Có bất kỳ danh mục phụ nào bị loại trừ khỏi việc thu hồi thuế không?
    - Nhóm thuế bán hàng của các danh mục phụ là gì?

Nếu danh mục chi phí cũng được sử dụng trong Kế toán và quản lý dự án, hãy trả lời các câu hỏi còn lại. Nếu không, hãy chuyển sang phần tiếp theo.

- Tài khoản chi phí nào sẽ được sử dụng cho các khoản chi phí sau?

    - Chi phí
    - Phân bổ bảng lương
    - Giá trị chi phí WIP
    - Chi phí-mục
    - Mục giá trị chi phí WIP
    - Lỗ lũy kế
    - Lỗ lũy kế WIP

- Tài khoản doanh thu nào sẽ được sử dụng cho các khoản sau?

    - Doanh thu đã lập hóa đơn
    - Giá trị bán hàng – doanh thu tích lũy
    - Giá trị bán hàng WIP
    - Sản xuất – doanh thu tích lũy
    - Sản xuất WIP
    - Lợi nhuận – doanh thu tích lũy
    - WIP-lợi nhuận
    - Đăng ký – doanh thu tích lũy
    - Đăng ký –WIP

### <a name="taxes"></a>Thuế

Đối với các khoản thuế liên quan đến chi phí, bạn phải xác định những gì được bao gồm hoặc kích hoạt trên báo cáo chi phí.

**Quyết định:**

- Thuế bán hàng có được tính vào chi phí không?
- Có nên kích hoạt thu hồi thuế đối với chi phí không?

    > [!NOTE]
    > Khi lập kế hoạch sổ cái, nếu bạn quyết định áp dụng các quy tắc thuế sử dụng và thuế bán hàng của Hoa Kỳ, bạn không thể kích hoạt thu hồi thuế đối với chi phí. (Để áp dụng các quy tắc thuế bán hàng và thuế sử dụng của Hoa Kỳ, hãy đặt tùy chọn **Áp dụng các quy tắc đánh thuế bán hàng** thành **Có**.)

## <a name="policies"></a>Chính sách

Bằng cách tạo các chính sách báo cáo chi phí, bạn có thể giúp tổ chức của mình tiết kiệm thời gian và tiền bạc khi nhân viên thay mặt tổ chức thanh toán các khoản chi phí. Các chính sách giúp đảm bảo rằng nhân viên chi tiêu trong phạm vi ngân sách, cung cấp tất cả thông tin được yêu cầu và chỉ chi tiền khi họ yêu cầu. Bạn phải đưa ra các quyết định sau cho từng chính sách báo cáo chi phí và từng chính sách phê duyệt báo cáo chi phí mà bạn tạo.

**Quyết định:**

- Tên của chính sách là gì?
- Chính sách chi phí là gì?
- Nếu trước đây bạn quyết định cho phép chi phí liên công ty, thì chính sách này sẽ áp dụng cho những công ty nào trong tổ chức của bạn?
- Khi nào thì chính sách có hiệu lực?
- Khi nào chính sách hết hạn?
- Quy tắc chính sách là gì?
- Kết quả của quy tắc chính sách là gì?


[!INCLUDE[footer-include](../includes/footer-banner.md)]