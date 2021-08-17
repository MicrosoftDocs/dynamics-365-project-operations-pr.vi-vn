---
title: Thiết lập mẫu chi phí
description: Chủ đề này cung cấp thông tin về cách tạo và sử dụng mẫu chi phí trong Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993582"
---
# <a name="set-up-cost-templates"></a>Thiết lập mẫu chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Chủ đề này cung cấp thông tin về cách tạo và sử dụng mẫu chi phí trong Project Operations. Mẫu chi phí giúp xác định:

- Thể loại dự án của các giao dịch thực tế và dự báo cần đưa vào trong phép tính phần trăm hoàn thành dự án. Giá trị phần trăm-hoàn thành sau đó sẽ được dùng để tính toán mức doanh thu đã ghi nhận.
- Có thể sửa đổi tỷ lệ phần trăm hoàn thành trong phép tính toán tự động hay không.
- Tỷ lệ phần trăm hoàn thành được tính theo số tiền hay đơn vị.

## <a name="cost-template-example"></a>Ví dụ về mẫu chi phí

Bạn đang thực hiện dự án thiết kế trang web cho khách hàng. Bạn tính phí ở mức cố định là 10.000 USD. Bạn dự báo rằng sẽ cần 100 giờ (5.000 USD) để hoàn thành dự án. Bạn cũng dự tính 2 vé máy bay và 4 đêm khách sạn cho chuyến đi đến địa điểm của khách hàng (1.800 USD). Tổng chi phí dự báo là 6.800 USD.

Khi chạy quy trình ghi nhận doanh thu theo giá cố định để tạo phép ước tính vào cuối tháng, bạn nhận thấy rằng mình đã làm việc 35 giờ cho dự án này. Con số này chưa bao gồm chi phí máy bay hoặc khách sạn. Bạn cũng bố trí một trợ lý nghiên cứu trong 5 giờ cho dự án này, với chi phí là 100 USD. Đây là khoản bạn chưa lập kế hoạch.

Khi tính toán giá trị phần trăm hoàn thành cho dự án này, bạn có những lựa chọn như sau:

- Bạn có muốn đưa vào toàn bộ chi phí (số giờ và khoản chi tiêu) hay chỉ số giờ?
- Bạn muốn đưa vào toàn bộ số giờ hay chỉ số giờ đã lên kế hoạch?
- Bạn muốn tính toán tỷ lệ phần trăm hoàn thành dựa trên chi phí tính theo USD đối với số giờ đã lên kế hoạch (5.000 USD) hay chỉ dựa trên số giờ (100)?

Lựa chọn của bạn cho những câu hỏi này sẽ quyết định những tùy chọn bạn thiết lập trên mẫu chi phí và các hạng mục bạn chọn trên các dòng mẫu chi phí.

Bảng sau minh họa kết quả của các phương pháp tính tỷ lệ phần trăm-hoàn thành khác nhau cho trường hợp này.

| Tỷ lệ hoàn thành dựa trên | Chi phí hoặc đơn vị tính theo USD | Phần trăm hoàn thành | Tính |
| --- | --- | --- | --- |
| Toàn bộ số giờ, không tính khoản chi tiêu | Chi phí tính theo USD | 37% 35 x USD 50 + USD 100 = USD 1.850 USD 1.850/USD 5.000 |
| Toàn bộ số giờ, không tính khoản chi tiêu | Đơn vị | 40% | 40 giờ / 100 giờ (bao gồm 5 giờ ngoài kế hoạch) |
| Số giờ theo kế hoạch, không tính khoản chi tiêu | Chi phí hoặc đơn vị tính theo USD | 35% | 35/100 giờ hoặc 35 x USD 50/5.000 |
| Toàn bộ số giờ và khoản chi tiêu | Chi phí tính theo USD | 27,2% | USD 1.850/USD 6.800 |

Bạn có thể cân nhắc một vài yếu tố sau đây khi đưa ra quyết định về phương pháp tạo mẫu chi phí:

- Nếu đưa số giờ ngoài kế hoạch vào mẫu chi phí, bạn sẽ gặp rủi ro đạt 100 phần trăm hoàn thành trước khi dự án hoàn thành. Điều này là do số giờ thực tế sẽ lớn hơn số giờ theo kế hoạch. Nếu dùng một tỏng 2 phương pháp đầu tiên trong bảng, bạn nên thay đổi kế hoạch (đơn vị đã dự báo) khi tính đến độ lệch. Trong trường hợp này, bạn nên cộng hoặc trừ số giờ dựa trên hiểu biết về những yêu cầu cần thiết để hoàn thành dự án. Nếu dự án cần 65 giờ nữa để hoàn thành, thì bạn nên cộng thêm 5 giờ vào kế hoạch, tổng cộng là 105 giờ. Nếu bạn biết rằng trợ lý của mình tiến hành nghiên cứu mất 5 giờ, thì tổng sẽ là 110 giờ.
- Nếu dùng phương pháp thứ 3 trong bảng, thì bạn chỉ cần cập nhật số giờ theo kế hoạch sao cho phù hợp với thời gian của mình để đảm bảo độ chính xác của phép tính tỷ lệ phần trăm-hoàn thành. Khả năng sinh lời sẽ thay đổi khi bạn ghi lại số giờ ngoài kế hoạch, nhưng bạn vẫn sẽ duy trì quỹ đạo phần trăm-hoàn thành đã biết.
- Nếu dùng phương pháp thứ tư trong bảng, bạn sẽ gặp phải rủi ro là khoản chi tiêu phát sinh ở thời điểm nào đó nhưng lại không được phản ánh trong tiến trình hoàn thành. Do đó, nếu được bao gồm, các khoản chi tiêu có thể khiến tỷ lệ phần trăm hoàn thành dao động hơn mức mong muốn. Ví dụ: do bạn chưa đáp chuyến bay, nên tỷ lệ phần trăm hoàn thành là 27 phần trăm thay vì 35 hay 37 phần trăm nếu bạn định tính toán chỉ dựa trên thời gian. Nếu bạn đã thực hiện chuyến đi kéo dài 2 đêm và dự báo chính xác chi phí máy bay và khách sạn, thì tỷ lệ phần trăm hoàn thành sẽ là 40,4 phần trăm (1850 USD phí nhân lực và 900 USD chi tiêu = USD 2750/6800 USD= 40,4 phần trăm). Do đó, khoản chi tiêu phát sinh cho một chuyến đi bằng máy bay sẽ thay đổi tỷ lệ phần trăm hoàn thành từ 27 lên 40 phần trăm.

## <a name="create-cost-templates"></a>Tạo mẫu chi phí
Để tạo mẫu chi phí, hãy làm theo các bước sau:

1. Để truy cập vào mẫu chi phí, trong môi trường Dynamics 365 Finance, hãy đi tới **Quản lý dự án và kế toán** > **Thiết lập** > **Ước tính** > **Mẫu chi phí**.
2. Chọn **Mới** để tạo mẫu chi phí mới. Nhập tên và mô tả.
3. Cung cấp ID dòng chi phí cho từng loại giao dịch.
4. Chọn một phương pháp hoàn thành làm mặc định:

  - **Tự động**: Tỷ lệ phần trăm hoàn thành được tính toán tự động cho dự án. Giá trị nhận được không thể thay đổi.
  - **Thủ công**: Tỷ lệ phần trăm hoàn thành được tính toán tự động cho dự án. Giá trị nhận được có thể thay đổi.

  > [!NOTE]
  > Đối với các phép tính toán thủ công, tỷ lệ phần trăm hoàn thành được duy trì trong phần **Tính toán thủ công** trên tab **Chung** của trang **Ước tính**.

5. Trong mục **Tỷ lệ hoàn thành dựa trên**, hãy chọn một trong các giá trị sau:

  - **Số tiền**: Tỷ lệ phần trăm hoàn thành được tính toán theo số tiền với đơn vị tiền tệ kế toán.
  - **Đơn vị**: Tỷ lệ phần trăm hoàn thành được tính theo số lượng.
  - **Tuyến tính**: Hệ thống tính toán phần trăm hoàn thành theo tỷ lệ bằng cách dùng ngày bắt đầu và ngày kết thúc dự án, từ đó xác định độ dài dự án.

6. Chọn **Dòng chi phí** để xem các dòng chi phí của mẫu chi phí. Mỗi loại giao dịch phải có ít nhất một dòng chi phí. Tuy nhiên, bạn có thể tạo nhiều dòng chi phí cho cùng một loại giao dịch và đặt các thuộc tính mong muốn cho những dòng này.
7. Trên tab **Hạng mục**, hãy chọn những hạng mục dự án bạn muốn đưa vào dòng mẫu chi phí.
8. Trên tab **Chung**, hãy chọn xem có đưa dòng này vào phép tính phần trăm hoàn thành hay không.
9. Chọn phương pháp phần trăm hoàn thành bạn muốn dùng khi tính toán tỷ lệ phần trăm hoàn thành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]