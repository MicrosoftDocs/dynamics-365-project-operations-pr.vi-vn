---
title: Chi phí công tác phí
description: Chủ đề này cung cấp thông tin về cách làm việc với chi phí công tác phí.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596076"
---
# <a name="per-diem-expenses"></a>Chi phí công tác phí

> [!IMPORTANT] 
> Chức năng được mô tả trong chủ đề này có sẵn cho người dùng được nhắm mục tiêu như một phần của bản phát hành xem trước.

Thanh toán công tác phí là một khoản trợ cấp hàng ngày cố định, được xác định trước mà một công ty trả cho nhân viên của mình để đi ở (khách sạn), ăn uống và các chi phí phát sinh mà những nhân viên đó phải chịu khi họ đi công tác. Công ty trả khoản phụ cấp này cho người lao động thay vì thanh toán chi phí đi lại thực tế. Nhân viên có thể sử dụng **Sự cố / Khác** phụ cấp công tác phí để trang trải tiền boa, phục vụ phòng, giặt là hoặc giặt hấp cho các cuộc họp kinh doanh quan trọng. Mức công tác phí có thể thay đổi, tùy thuộc vào việc người sử dụng lao động chọn hoàn trả cho chi phí ăn ở và ăn uống kết hợp, hay chỉ cho chi phí ăn uống và các chi phí phát sinh.

Mức công tác phí có thể dựa trên thời gian trong năm, địa điểm đến hoặc cả hai. Khi bạn tạo quy tắc công tác phí, bạn có thể chỉ định rằng một tỷ lệ phần trăm của tỷ lệ công tác phí sẽ được giữ lại nếu một nhân viên nhận được các bữa ăn hoặc dịch vụ miễn phí. Bạn cũng có thể đặt số giờ tối thiểu và số giờ tối đa mà mức công tác phí có thể được áp dụng cho việc đi lại của nhân viên.

Công tác phí được tính bằng tổng phụ cấp được cung cấp mỗi ngày trừ đi khoản giảm tiền ăn (chi phí ăn uống miễn phí) được cung cấp cho người lao động.

## <a name="configure-per-diems"></a>Định cấu hình công tác phí

Để định cấu hình chi phí công tác phí, hãy làm theo các bước sau.

1. Đi đến **Quản lý chi tiêu** \> **Cài đặt** \> **Chung** \> **Các thông số quản lý chi phí**.
2. Trên **Công tác phí** tab, trong **Tính toán giảm bữa ăn theo**, chọn cách tính công tác phí:

    - **Loại bữa ăn cho mỗi chuyến đi** - Tính công tác phí dựa trên loại bữa ăn được nhập (bữa sáng, bữa trưa hoặc bữa tối) và mức giảm tiền ăn được quy định cho từng loại bữa ăn để được hỗ trợ công tác phí trong suốt thời gian của chuyến đi.
    - **Loại bữa ăn mỗi ngày** - Tính công tác phí dựa trên loại suất ăn được nhập và mức giảm tiền ăn được quy định cụ thể cho từng loại suất ăn để được hỗ trợ công tác phí mỗi ngày.
    - **Số bữa ăn trong ngày** - Tính công tác phí dựa trên số suất ăn được nhập trong ngày và mức giảm suất ăn của số suất ăn được cung cấp mỗi ngày.

3. Đi đến **Quản lý chi tiêu** \> **Cài đặt** \> **Tính toán và mã** \> **Địa điểm công tác phí**.
4. Thêm các địa điểm có thể sử dụng công tác phí.
5. Đối với mỗi vị trí mà bạn thêm, trên **Công tác phí cho mỗi**, chọn tỷ lệ công tác phí và đơn vị tiền tệ hợp lệ giữa ngày bắt đầu và ngày kết thúc cụ thể cho chỗ ở, bữa ăn và các chi phí khác. Để định cấu hình tỷ giá công tác phí và đơn vị tiền tệ, hãy truy cập **Quản lý chi tiêu** \> **Cài đặt** \> **Tính toán và mã** \> **Công tác phí cho mỗi**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Công tác phí trong giao diện chi phí được mô phỏng lại

Tính năng công tác phí được hỗ trợ trong **Quản lý chi tiêu** không gian làm việc trong Microsoft Dynamics 365 Finance phiên bản 10.0.25 trở lên.

Để bật công tác phí, hãy làm theo các bước sau.

1. Bên trong **Quản lý tính năng** không gian làm việc, tìm và chọn **Báo cáo chi phí được mô phỏng lại** trong danh sách, sau đó chọn **Kích hoạt ngay bây giờ**.
2. Tìm và chọn **Per-diem cho báo cáo chi phí giao diện được tưởng tượng lại** trong danh sách, sau đó chọn **Kích hoạt ngay bây giờ**.

## <a name="how-the-feature-works"></a>Cách hoạt động của tính năng

Phần này cung cấp các ví dụ cho ba trường hợp cấu hình. Đối với mỗi ví dụ, **Tính toán giảm bữa ăn theo** trường được đặt thành một giá trị khác. Đối với cả ba ví dụ, tổng số tiền phải trả là như nhau cho đến khi áp dụng mức giảm bữa ăn. Sau thời điểm đó, tổng số tiền phải trả sẽ khác nhau đối với từng ví dụ.

Để tạo chi phí công tác phí được sử dụng cho cả ba ví dụ, hãy làm theo các bước sau.

1. Đi đến **Không gian làm việc** \> **Quản lý chi tiêu**.
2. Lựa chọn **Báo cáo chi phí mới** hoặc chọn một báo cáo chi phí hiện có.
3. Thêm một khoản chi phí mới. Bên trong **Danh mục** trường, chọn **Công tác phí**. Chọn địa điểm, ngày bắt đầu và ngày kết thúc chuyến đi của bạn. Công tác phí cho chỗ ở, ăn uống và các chi phí phát sinh (chi phí khác) được tính dựa trên phụ cấp hàng ngày được quy định cho địa điểm đã chọn.

    Ví dụ, bạn chọn **Redmond (Mỹ)** như vị trí. Trợ cấp hàng ngày cho vị trí đó là 150 đô la Mỹ (150 USD) cho chỗ ở, USD 75 cho bữa ăn và USD 5 cho các chi phí phát sinh. Ngày bắt đầu là ngày 10 tháng Giêng và ngày kết thúc là ngày 14 tháng Giêng. Do đó, khoảng thời gian đã chọn là năm ngày khi cấu hình được chọn là các ngày theo lịch với thời gian và thời gian đã chọn bắt đầu và kết thúc lúc 12:00 sáng vào ngày bắt đầu và ngày kết thúc. Dưới đây là các tính toán:

    - Tổng số tiền phải trả = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Bữa ăn và phần phụ của tổng số tiền = 5 × (75 + 5) = USD 400

Nếu bữa sáng, bữa trưa và bữa tối đã được cung cấp trong suốt chuyến đi thì những bữa ăn đó phải được tính giảm bữa ăn.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Ví dụ 1: Công tác phí trong đó các bữa ăn được giảm trừ tùy theo loại bữa ăn cho mỗi chuyến đi

Trong ví dụ này, mức giảm bữa ăn là 30 phần trăm cho bữa sáng, 30 phần trăm cho bữa trưa và 40 phần trăm cho bữa tối. Trên **Các thông số quản lý chi phí** trang, **Tính toán giảm bữa ăn theo** trường được đặt thành **Loại bữa ăn cho mỗi chuyến đi**. Dưới đây là các phép tính nếu nhân viên cung cấp ba bữa sáng, hai bữa trưa và không bữa tối:

- Giảm bữa ăn = (3 ×\[ 75 × 30%\]) + (2 ×\[ 75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Bữa ăn và các khoản phát sinh = 400 - 112,50 = USD 287.50
- Tổng số tiền phải trả = Tổng phụ cấp - Giảm bữa ăn = 1.150 - 112,50 = USD 1,037.50

![Chi phí công tác phí trong đó mức giảm tiền ăn tùy theo loại suất ăn trong chuyến đi.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Ví dụ 2: Công tác phí trong đó mức giảm tiền ăn dựa trên loại bữa ăn trong ngày

Trong ví dụ này, mức giảm bữa ăn là 30 phần trăm cho bữa sáng, 30 phần trăm cho bữa trưa và 40 phần trăm cho bữa tối. Trên **Các thông số quản lý chi phí** trang, **Tính toán giảm bữa ăn theo** trường được đặt thành **Loại bữa ăn mỗi ngày**. Trong trường hợp này, trong **Bữa ăn** lưới trong **Chỉnh sửa chi phí** hộp thoại, bạn xóa các hộp kiểm để cho biết bữa ăn nào đã được cung cấp cho bạn trong chuyến đi của bạn.

Ví dụ: đây là các tính toán nếu bữa sáng được cung cấp cho ba ngày đầu tiên của chuyến đi:

- Giảm bữa ăn hàng ngày cho mỗi ngày trong ba ngày đầu tiên = 75 × 30% = USD 22.50
- Tổng số bữa ăn giảm = 3 × 22,50 = USD 67.50
- Các bữa ăn và các khoản phát sinh từ ngày 1 đến ngày 3 = 75 - 22,50 = USD 57.50
- Tổng số bữa ăn và các khoản phát sinh = Tổng số bữa ăn và các khoản phát sinh trong 5 ngày = 400 - 67,50 = USD 332.50
- Tổng số tiền phải trả = Tổng số tiền - Giảm bữa ăn = 1.150 - 67.50 = USD 1,082.50

![Chi phí công tác phí trong đó mức giảm tiền ăn theo loại bữa ăn trong ngày.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Ví dụ 3: Công tác phí trong đó mức giảm tiền ăn dựa trên số bữa ăn trong ngày

Trong ví dụ này, mức giảm bữa ăn được tính dựa trên số lượng bữa ăn được cung cấp mỗi ngày (nghĩa là **Tính toán giảm bữa ăn theo** lĩnh vực trên **Các thông số quản lý chi phí** trang được đặt thành **Số bữa ăn trong ngày**). Bên trong **Bữa ăn** lưới trong **Chỉnh sửa chi phí** hộp thoại, bạn xóa hộp kiểm để cho biết bữa ăn nào đã được cung cấp.
Trong trường hợp này, việc giảm bữa ăn chỉ dựa trên số lượng bữa ăn được cung cấp chứ không dựa trên loại bữa ăn (Bữa sáng / bữa trưa / bữa tối) được cung cấp.

Dưới đây là các tính toán cho công tác phí khi phụ cấp hàng ngày là USD 150 cho chỗ ở, USD 75 cho bữa ăn và USD 5 cho các chi phí phát sinh:

- **Tổng số tiền phải nộp** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Một bữa ăn:** Giảm bữa ăn = 20% = USD 15
- **Hai bữa ăn:** Giảm bữa ăn = 50% = USD 37.50
- **Ba bữa:** Giảm bữa ăn = 100% = USD 75

Đây là các tính toán cho **trợ cấp ăn uống và các chi phí phát sinh**, bao gồm USD 5 cho các sự cố phát sinh:

- Ngày 1 - Cung cấp hai bữa ăn = (75 - 37,50) + 5 = 37,50 + 5 = USD 42.50
- Ngày 2 - Cung cấp hai bữa ăn = (75 - 37,50) + 5 = 37,50 + 5 = USD 42.50
- Ngày 3 - Một bữa ăn được cung cấp = (75 - 15) + 5 = 60 + 5 = USD 65
- Ngày 4 - Không cung cấp bữa ăn nào = (75-0) + 5 = 75 + 5 = USD 80
- Ngày 5 - Cung cấp 3 bữa ăn = (75 - 75) + 5 = 0 + 5 = USD 5

- Tổng số bữa ăn và các khoản phát sinh = Các bữa ăn và sự cố cho Ngày 1+ Ngày 2 + Ngày 3 + Ngày 4+ Ngày 5 = USD 235
- Tổng số bữa ăn giảm = Giảm bữa ăn cho Ngày 1+ Ngày 2 + Ngày 3 + Ngày 4+ Ngày 5 = 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Tổng số tiền phải trả = Tổng phụ cấp - Tổng số tiền giảm bữa ăn = USD 1,150 - USD 165 = USD 985

![Công tác phí tính theo số bữa ăn trong ngày được giảm trừ tiền ăn.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Kể từ phiên bản Tài chính 10.0.23, nếu bạn sử dụng giao diện chi phí được mô phỏng lại, bạn không thể tạo chi phí công tác phí có ngày trùng lặp. Nếu bạn cố gắng, bạn sẽ nhận được thông báo lỗi.
