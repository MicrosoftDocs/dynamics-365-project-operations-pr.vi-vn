---
title: Chi phí công nhật
description: Bài viết này cung cấp thông tin về cách làm việc với chi phí công nhật.
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
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923214"
---
# <a name="per-diem-expenses"></a>Chi phí công nhật

> [!IMPORTANT] 
> Chức năng được mô tả trong bài viết này khả dụng như một phần của bản phát hành xem trước đối với người dùng được nhắm mục tiêu.

Thanh toán công tác phí là một khoản trợ cấp hàng ngày cố định, được xác định trước mà một công ty trả cho nhân viên của mình để lưu trú (khách sạn), ăn uống và các chi phí phát sinh của nhân viên đó khi họ đi công tác. Công ty trả khoản phụ cấp này cho người lao động thay vì thanh toán chi phí đi lại thực tế. Nhân viên có thể sử dụng phụ cấp công tác phí **Phát sinh/Khác** để trang trải tiền boa, chi phí phục vụ phòng, giặt là hoặc giặt khô cho các cuộc gặp công việc quan trọng. Mức công tác phí có thể thay đổi, tùy thuộc vào việc chủ lao động chọn hoàn trả cho chi phí lưu trú và ăn uống, hay chỉ hoàn trả chi phí ăn uống và các chi phí phát sinh.

Mức công tác phí có thể dựa trên thời gian trong năm, địa điểm đến hoặc cả hai. Khi bạn tạo quy tắc công tác phí, bạn có thể chỉ định rằng tỷ lệ phần trăm công tác phí sẽ được giữ lại nếu nhân viên nhận được các bữa ăn hoặc dịch vụ miễn phí. Bạn cũng có thể đặt số giờ tối thiểu và tối đa mà mức công tác phí có thể áp dụng cho việc đi lại của nhân viên.

Công tác phí được tính bằng tổng số tiền phụ cấp được cung cấp mỗi ngày trừ đi mức giảm tiền ăn (chi phí bữa ăn miễn phí) được cung cấp cho nhân viên.

## <a name="configure-per-diems"></a>Thiết lập công tác phí

Để thiết lập chi phí công tác phí, hãy làm theo các bước sau.

1. Đi đến **Quản lý chi phí** \> **Thiết lập** \> **Chúng** \> **Tham số quản lý chi phí**.
2. Trên tab **Công tác phí**, trong trường **Tính toán giảm bữa ăn theo**, chọn phương thức tính công tác phí:

    - **Loại bữa ăn mỗi chuyến đi** – Tính công tác phí dựa trên loại bữa ăn được nhập (bữa sáng, bữa trưa hoặc bữa tối) và mức giảm tiền ăn được quy định cho từng loại bữa ăn đối với phụ cấp công tác phí trong suốt chuyến đi.
    - **Loại bữa ăn mỗi ngày** – Tính công tác phí dựa trên loại bữa ăn được nhập và mức giảm tiền ăn được quy định cho từng loại bữa ăn đối với phụ cấp công tác phí mỗi ngày.
    - **Số bữa ăn mỗi ngày** – Tính công tác phí dựa trên số bữa ăn được nhập mỗi ngày và dựa trên mức giảm tiền bữa ăn cho số bữa ăn được cung cấp mỗi ngày.

3. Đi đến **Quản lý chi phí** \> **Thiết lập** \> **Phép tính và mã** \> **Địa điểm cấp công tác phí**.
4. Thêm địa điểm có thể sử dụng công tác phí.
5. Đối với mỗi địa điểm mà bạn thêm, trên tab **Công tác phí**, hãy chọn mức công tác phí và đơn vị tiền tệ hợp lệ giữa ngày bắt đầu và ngày kết thúc cụ thể cho nơi lưu trú, bữa ăn và các chi phí khác. Để thiết lập mức công tác phí và đơn vị tiền tệ, hãy đi đến **Quản lý chi phí** \> **Thiết lập** \> **Phép tính và mã** \> **Công tác phí**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Công tác phí trong giao diện chi phí được mô phỏng lại

Tính năng công tác phí được hỗ trợ trong không gian làm việc **Quản lý chi phí** trong Microsoft Dynamics 365 Finance phiên bản 10.0.25 trở lên.

Để bật tính năng công tác phí, hãy làm theo các bước sau.

1. Trong không gian làm việc **Quản lý tính năng**, tìm và chọn **Báo cáo chi phí được xây dựng lại** trong danh sách, sau đó chọn **Kích hoạt ngay bây giờ**.
2. Tìm và chọn tính năng **Giao diện Công tác phí cho báo cáo chi phí** trong danh sách, sau đó chọn **Kích hoạt ngay bây giờ**.

## <a name="how-the-feature-works"></a>Cách thức hoạt động của tính năng

Phần này cung cấp các ví dụ cho ba tình huống cấu hình. Đối với mỗi ví dụ, trường **Tính toán giảm bữa ăn theo** được đặt thành một giá trị khác. Trong cả ba ví dụ, tổng số tiền phải trả là như nhau cho đến khi áp dụng mức giảm tiền bữa ăn. Sau thời điểm đó, tổng số tiền phải trả sẽ khác nhau đối với từng ví dụ.

Để tạo chi phí công tác phí được sử dụng cho cả ba ví dụ, hãy làm theo các bước sau.

1. Chuyển đến **Không gian làm việc** \> **Quản lý chi phí**.
2. Chọn **Báo cáo chi phí mới** hoặc chọn một báo cáo chi phí hiện có.
3. Thêm một chi phí mới. Trong trường **Thể loại**, chọn **Công tác phí**. Chọn địa điểm, ngày bắt đầu và ngày kết thúc chuyến đi của bạn. Công tác phí cho chỗ ở, ăn uống và các chi phí phát sinh (chi phí khác) được tính dựa trên phụ cấp hàng ngày được đặt cho địa điểm đã chọn.

    Ví dụ: bạn chọn **Redmond (Mỹ)** làm địa điểm. Phụ cấp hàng ngày cho địa điểm đó là 150 đô-la Mỹ (150 USD) cho chỗ ở, 75 USD cho bữa ăn và 5 USD cho các chi phí phát sinh. Ngày bắt đầu là ngày 10 tháng 1 và ngày kết thúc là ngày 14 tháng 1. Do đó, khoảng thời gian đã chọn là năm ngày khi cấu hình được chọn là các ngày theo lịch với thời gian, và thời gian đã chọn bắt đầu và kết thúc lúc 12:00 sáng vào ngày bắt đầu và ngày kết thúc. Dưới đây là các phép tính:

    - Tổng số tiền phải trả = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Bữa ăn và phần chi phí phát sinh của tổng số tiền = 5 × (75 + 5) = 400 USD

Nếu bữa sáng, bữa trưa và bữa tối được cung cấp trong suốt chuyến đi thì những bữa ăn đó phải được tính vào mức giảm tiền bữa ăn.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Ví dụ 1: Công tác phí trong đó các mức giảm tiền bữa ăn dựa theo loại bữa ăn cho mỗi chuyến đi

Trong ví dụ này, mức giảm tiền bữa ăn là 30 phần trăm cho bữa sáng, 30 phần trăm cho bữa trưa và 40 phần trăm cho bữa tối. Trên trang **Tham số quản lý chi phí**, trường **Tính toán giảm bữa ăn theo** được đặt thành **Loại bữa ăn mỗi chuyến đi**. Dưới đây là các phép tính nếu nhân viên được cung cấp ba bữa sáng, hai bữa trưa và không bữa tối:

- Giảm tiền bữa ăn = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Bữa ăn và các khoản phát sinh = 400 – 112,50 = 287,50 USD
- Tổng số tiền phải trả = Tổng phụ cấp – Mức giảm tiền bữa ăn = 1.150 - 112,50 = 1.037,50 USD

![Công tác phí trong đó mức giảm tiền bữa ăn dựa theo loại bữa ăn cho mỗi chuyến đi.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Ví dụ 2: Công tác phí trong đó các mức giảm tiền bữa ăn dựa theo loại bữa ăn mỗi ngày

Trong ví dụ này, mức giảm tiền bữa ăn là 30 phần trăm cho bữa sáng, 30 phần trăm cho bữa trưa và 40 phần trăm cho bữa tối. Trên trang **Tham số quản lý chi phí**, trường **Tính toán giảm bữa ăn theo** được đặt thành **Loại bữa ăn mỗi ngày**. Trong trường hợp này, lưới **Bữa ăn** trong hộp thoại **Chỉnh sửa chi phí**, bạn bỏ đánh dấu các hộp kiểm để cho biết bữa ăn nào đã được cung cấp cho bạn trong chuyến đi.

Ví dụ: đây là các phép tính nếu bữa sáng được cung cấp trong ba ngày đầu tiên của chuyến đi:

- Mức giảm tiền bữa ăn hàng ngày cho mỗi ngày trong ba ngày đầu tiên = 75 × 30% = 22,50 USD
- Tổng mức giảm tiền bữa ăn = 3 × 22,50 = 67,50 USD
- Các bữa ăn và các khoản phát sinh từ ngày 1 đến ngày 3 = 75 – 22,50 = 57,50 USD
- Tổng số bữa ăn và các khoản phát sinh = Tổng số bữa ăn và các khoản phát sinh trong 5 ngày = 400 – 67,50 = 332,50 USD
- Tổng số tiền phải trả = Tổng số tiền – Mức giảm tiền bữa ăn = 1.150 - 67,50 = 1.082,50 USD

![Công tác phí trong đó mức giảm tiền bữa ăn dựa theo loại bữa ăn mỗi ngày.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Ví dụ 3: Công tác phí trong đó các mức giảm tiền bữa ăn dựa theo số bữa ăn mỗi ngày

Trong ví dụ này, mức giảm tiền bữa ăn được tính dựa trên số bữa ăn được cung cấp mỗi ngày (nghĩa là trường **Tính toán giảm bữa ăn theo** trên trang **Tham số quản lý chi phí** được đặt thành **Số bữa ăn mỗi ngày**). Trong lưới **Bữa ăn** trong hộp thoại **Chỉnh sửa chi phí**, bạn bỏ đánh dấu các hộp kiểm để cho biết bữa ăn nào đã được cung cấp.
Trong trường hợp này, khoản giảm tiền bữa ăn chỉ dựa trên số lượng bữa ăn được cung cấp chứ không dựa trên loại bữa ăn (Bữa sáng/bữa trưa/bữa tối) được cung cấp.

Dưới đây là các phép tính cho công tác phí khi phụ cấp hàng ngày là 150 USD cho chỗ ở, 75 USD cho bữa ăn và 5 USD cho các chi phí phát sinh:

- **Tổng số tiền phải trả** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Một bữa ăn:** Giảm tiền bữa ăn = 20% = 15 USD
- **Hai bữa ăn:** Giảm tiền bữa ăn = 50% = 37,50 USD
- **Ba bữa ăn:** Giảm tiền bữa ăn = 100% = 75 USD

Đây là các tính toán cho **phụ cấp bữa ăn và chi phí phát sinh**, bao gồm 5 USD cho các chi phí phát sinh:

- Ngày 1 - Hai bữa ăn được cung cấp = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Ngày 2 - Hai bữa ăn được cung cấp = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Ngày 3 - Một bữa ăn được cung cấp = (75 – 15) + 5 = 60 + 5 = 65 USD
- Ngày 4 - Không có bữa ăn được cung cấp = (75 – 0) + 5 = 75 + 5 = 80 USD
- Ngày 5 - Ba bữa ăn được cung cấp = (75 – 75) + 5 = 0 + 5 = 5 USD

- Tổng số bữa ăn và các khoản phát sinh = Các bữa ăn và chi phí phát sinh cho Ngày 1+ Ngày 2 + Ngày 3 + Ngày 4+ Ngày 5 = 235 USD
- Tổng mức giảm tiền bữa ăn = Mức giảm tiền bữa ăn cho Ngày 1 + Ngày 2 + Ngày 3 + Ngày 4 + Ngày 5 = 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Tổng số tiền phải trả = Tổng phụ cấp – Tổng mức giảm tiền bữa ăn = 1.150 USD - 165 USD = 985 USD

![Công tác phí trong đó mức giảm tiền bữa ăn dựa theo số bữa ăn mỗi ngày.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Kể từ phiên bản Finance 10.0.23, nếu bạn sử dụng giao diện chi phí được mô phỏng lại, bạn không thể tạo chi phí công tác phí có ngày trùng lặp. Nếu bạn cố tạo, bạn sẽ nhận được thông báo lỗi.
