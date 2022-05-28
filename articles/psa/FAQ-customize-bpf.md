---
title: Tôi có thể làm cách nào để tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án?
description: Tổng quan về cách tùy chỉnh dòng quy trình công việc ở các giai đoạn dự án.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7efbb19161878e13a1b0d33bc1bc4e06521445c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596996"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Tôi có thể làm cách nào để tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Có một giới hạn đã biết ở các phiên bản trước của ứng dụng Project Service là tên của các giai đoạn trong dòng quy trình công việc ở Các giai đoạn Dự án phải trùng chính xác với tên tiếng Anh dự tính (**Quote**, **Plan**, **Close**). Nếu không, theo lô-gic công việc dựa trên tên giai đoạn tiếng Anh sẽ không làm việc như mong đợi. Đó là lý do tại sao bạn không thấy các tác vụ quen thuộc như **Đổi Quy trình** hoặc **Sửa Quy trình** sẵn có trên mẫu dự án và không khuyến khích việc tùy chỉnh dòng quy trình công việc. 

Hạn chế này đã được khắc phục trong phiên bản 2.4.5.48 trở lên. Bài viết này cung cấp các cách giải quyết gợi ý cho các phiên bản cũ nếu bạn cần tùy chỉnh dòng quy trình công việc mặc định cho các phiên bản cũ hơn.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Lô-gic công việc yêu cầu khớp chính xác với tên giai đoạn tiếng Anh

Dòng quy trình công việc ở Các giai đoạn Dự án bao gồm lô-gic công việc điều khiển các hành vi sau trong ứng dụng:
- Khi dự án liên kết với một báo giá, mã sẽ đặt dòng quy trình công việc vào giai đoạn **Quote**.
- Khi dự án được liên kết với một hợp đồng, mã sẽ đặt dòng quy trình công việc vào giai đoạn **Plan**.
- Khi dòng quy trình công việc tiến tới giai đoạn **Close**, bản ghi dự án sẽ bị hủy kích hoạt. Khi dự án bị hủy kích hoạt, biểu mẫu dự án và cấu trúc phân tích công việc (WBS) được đặt về chế độ chỉ đọc, đăng ký nguồn lực được đặt tên được phát hành và bất kỳ bảng giá liên kết nào cũng bị hủy kích hoạt.

Lô-gic công việc này dựa trên tên tiếng Anh cho các giai đoạn dự án. Sự phụ thuộc vào tên giai đoạn tiếng Anh là lý do chính tại sao việc tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án lại không được khuyến khích. Cũng như tại sao bạn không thấy các tác vụ dòng quy trình công việc phổ thông như **Đổi Quy trình** hoặc **Sửa quy trình** trên thực thể dự án.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Điều gì sẽ xảy ra nếu tên giai đoạn không khớp với tên tiếng Anh?

Trong ứng dụng Project Service phiên bản 1.x trên nền tảng 8.2, khi các tên giai đoạn trong dòng quy trình công việc không khớp chính xác với các tên giai đoạn tiếng Anh, lô-gic công việc mà đặt giai đoạn đúng cho báo giá hoặc hợp đồng hoặc đóng dự án, sẽ bị bỏ qua. Không có thông báo lỗi nào được hiển thị. Do đó, điều đó có nghĩa bạn có thể tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án. Tuy nhiên, bạn sẽ không thấy bất kỳ quy trình tự động nào hoạt động cho báo giá, hợp đồng và đóng dự án.

Trong ứng dụng Project Service phiên bản 2.4.4.30 trở về trước trên nền tảng 9.0, đã có một thay đổi kiến trúc đáng kể cho dòng quy trình công việc mà cần viết lại lô-gic công việc của dòng quy trình công việc. Kết quả là nếu tên giai đoạn quy trình không khớp với tên tiếng Anh dự kiến, bạn nhận được một thông báo lỗi. 

Vì vậy, nếu bạn muốn tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án cho thực thể dự án, bạn chỉ có thể thêm giai đoạn mới hoàn toàn vào dòng quy trình công việc mặc định cho thực thể dự án trong khi giữ nguyên các giai đoạn **Quote**, **Plan** và **Close**. Giới hạn này đảm bảo bạn không gặp phải lỗi do lô-gic công việc phụ thuộc vào tên giai đoạn tiếng Anh trong dòng quy trình công việc.

Trong phiên bản 2.4.5.48 trở lên, lô-gic công việc được mô tả trong bài viết này đã được loại bỏ khỏi dòng quy trình công việc mặc định cho thực thể dự án. Nâng cấp từ phiên bản đó trở lên sẽ cho phép bạn tùy chỉnh hoặc thay đổi dòng quy trình công việc mặc định với dòng quy trình công việc của bạn. 

## <a name="workarounds-for-earlier-versions"></a>Cách giải quyết đối với các phiên bản cũ

Nếu nâng cấp không phải là một tùy chọn, bạn có thể tùy chỉnh dòng quy trình công việc ở Các giai đoạn Dự án cho thực thể dự án theo một trong hai cách sau:

1. Thêm các giai đoạn bổ sung vào cấu hình mặc định trong khi vẫn giữ nguyên tên giai đoạn tiếng Anh cho **Quote**, **Plan** và **Close**.


![Ảnh chụp màn hình khi thêm các giai đoạn vào cấu hình mặc định.](media/FAQ-Customize-BPF-1.png)
 
2. Tạo dòng quy trình công việc của riêng mình và biến thành dòng quy trình công việc chính cho thực thể dự án, như vậy bạn sẽ có bất kỳ tên giai đoạn nào mà bạn muốn. Tuy nhiên, nếu bạn muốn sử dụng các giai đoạn dự án theo chuẩn trước là **Quote**, **Plan** và **Close**, bạn cần thực hiện một số tùy chỉnh để bỏ tên giai đoạn tùy chỉnh của mình. Lô-gic phức tạp hơn là khi đóng dự án, khi đó bạn có thể vẫn kích hoạt bằng cách chỉ hủy kích hoạt bản ghi dự án.

![Tùy chỉnh BPF.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Các cân nhắc bổ sung đối với ứng dụng Project Service phiên bản 2.4.4.30 trở về trước trên nền tảng 9.0

Trong Project Service 2.4.4.30 trở về trước trên nền tảng 9.0, với dòng quy trình công việc tùy chỉnh, trường **Tên Giai đoạn** trên thực thể dự án được dùng trong các dạng xem danh sách dự án và biểu đồ **Dự án Theo Giai đoạn** sẽ không được cập nhật, bởi vì trường này được tích hợp với dòng quy trình công việc ở Các giai đoạn Dự án. Bạn có thể giải quyết vấn đề này theo các bước như sau:

- Thêm một trường tùy chỉnh để chụp giai đoạn dòng quy trình công việc mà được cập nhật khi người dùng tiến hành qua dòng quy trình công việc tùy chỉnh.

- Sửa đổi biểu đồ **Dự án Theo Giai đoạn** để làm việc với trường tùy chỉnh của bạn thay cho cấu hình mặc định.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Các bước để tạo dòng quy trình công việc của riêng mình cho thực thể dự án

Để tạo dòng quy trình công việc của riêng mình cho thực thể dự án, làm như sau:

1. Chuyển tới **Cài đặt** > **Trung tâm Quy trình**. Không sao chép dòng quy trình công việc ở Các giai đoạn Dự án bởi vì như thế cũng sao chép lô-gic công việc của Project Service.

  ![Tạo quy trình.](media/FAQ-Customize-BPF-3.png)

2. Sử dụng trình Thiết kế Quy trình để tạo tên giai đoạn mà bạn muốn. Nếu bạn muốn cùng chức năng đó là các giai đoạn mặc định cho **Quote**, **Plan** và **Close**, bạn sẽ phải tạo dựa trên những tên giai đoạn của dòng quy trình công tùy chỉnh của mình.

   ![Ảnh chụp màn hình của trình Thiết kế Quy trình được dùng để tùy chỉnh BPF.](media/FAQ-Customize-BPF-4.png) 

3. Trong trình Thiết kế Quy trình, **Sắp xếp Dòng Quy trình** để tạo dòng quy trình công việc tùy chỉnh thành dòng quy trình công việc chính cho thực thể dự án bằng cách di chuyển quy trình ở phía trên dòng quy trình công việc ở Các giai đoạn Dự án lên trên cùng của danh sách.


   [Ảnh chụp màn hình khi sử dụng Sắp xếp Dòng Quy trình](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Các bước sau đây áp dụng cho ứng dụng Project Service 2.4.4.30 trở về trước trên nền tảng 9.0

4. Thêm một trường tùy chỉnh mới vào thực thể dự án để chụp các giai đoạn tùy chỉnh trong dòng quy trình công việc tùy chỉnh của bạn. Bạn sẽ cần thêm lô-gic công việc (phần bổ trợ/dòng công việc) để cập nhật trường này khi giai đoạn trên dòng quy trình công việc được cập nhật.

   ![Ảnh chụp màn hình khi tùy chỉnh thực thể Dự án.](media/FAQ-Customize-BPF-6-720.png)

5. Sửa đổi biểu đồ **Dự án Theo Giai đoạn** để dùng trường tùy chỉnh mới cho các giai đoạn của bạn.

   ![Ảnh chụp màn hình khi sử dụng biểu đồ Dự án Theo Giai đoạn.](media/FAQ-Customize-BPF-7-720.png)

6. Sửa đổi bất kỳ dạng xem nào cho thực thể để đưa trường tùy chính mới cho các giai đoạn của bạn vào.

   ![Ảnh chụp màn hình khi chỉnh sửa dạng xem trên thực thể Dự án.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
