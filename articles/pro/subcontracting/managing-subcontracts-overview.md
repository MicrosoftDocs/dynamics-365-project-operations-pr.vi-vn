---
title: Quản lý hợp đồng phụ trong Project Operations
description: Bài viết này cung cấp thông tin tổng quan về toàn bộ quy trình quản lý hợp đồng phụ thường gặp trong các tổ chức dựa trên dự án.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522352"
---
# <a name="subcontract-management-in-project-operations"></a>Quản lý hợp đồng phụ trong Project Operations


_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này cung cấp thông tin tổng quan về toàn bộ quy trình quản lý hợp đồng phụ trong các tổ chức dựa trên dự án. Giao thầu phụ đối với các dịch vụ thường tuân theo dòng quy trình công việc được hiển thị trong sơ đồ sau.

![Sòng quy trình giao thầu phụ](../media/SubcontractingProcessFlow.png)

Danh sách sau đây mô tả từng bước về quy trình giao thầu phụ.

1. Người quản lý dự án tạo một hợp đồng phụ với một nhà cung cấp. Theo mặc định, bảng giá được đính kèm với hồ sơ nhà cung cấp được sử dụng cho hợp đồng phụ. Tài khoản nhà cung cấp có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**.
2. Người quản lý dự án có thể lặp lại tất cả các giao dịch mua dưới dạng mục hàng trên hợp đồng phụ. Mô tả hợp đồng phụ có thể là về thời gian, chi phí hoặc sản phẩm. Lớp giao dịch của mô tả hợp đồng phụ sẽ xác định mô tả đó dùng để làm gì.
3. Người quản lý tài khoản của nhà cung cấp và người quản lý dự án có thể lặp lại hợp đồng phụ. Có thể điều chỉnh giá trong bảng giá mua đính kèm với hợp đồng phụ.
4. Tại thời điểm này hoặc sau đó trong quá trình, nếu mô tả hợp đồng phụ là về thời gian, người quản lý tài khoản nhà cung cấp sẽ kết hợp các địa chỉ liên hệ của nhà cung cấp với từng mô tả hợp đồng phụ. Việc liên kết này cung cấp thông tin cho người quản lý dự án, người đang làm việc trên hợp đồng phụ. Khi một liên hệ của nhà cung cấp được liên kết với một mô tả hợp đồng phụ, hệ thống sẽ tự động tạo nguồn lực có thể đặt trước từ liên hệ, nếu nguồn lực có thể đặt trước chưa tồn tại.
5. Phương thức thanh toán trên mỗi mô tả hợp đồng phụ có thể là **Giá cố định** hoặc **Thời gian và Vật liệu**. Đối với các mô tả hợp đồng phụ giá cố định, lịch hóa đơn dựa trên cột mốc được thiết lập.
6.  Sau khi hợp đồng phụ được thiết lập và thương lượng hoàn tất, nó được xác nhận. Không thể chỉnh sửa hợp đồng phụ đã xác nhận nhưng nếu thay đổi xảy ra, hợp đồng phụ có thể được 'mở lại để chỉnh sửa', điều này đặt trạng thái từ **Đã xác nhận** về **Bản nháp** và thương lượng có thể được mở lại. 
7.  Khi tạo một thành viên nhóm chung trong một dự án, thành viên trong nhóm có thể được liên kết với một mô tả hợp đồng phụ. Điều này cho thấy sự cần thiết phải tuyển dụng thành viên nhóm chung có năng lực nhà thầu phụ.
8.  Các thành viên trong nhóm được đặt tên có thể được tạo trực tiếp trên một dự án hoặc được tạo bằng cách đặt chỗ cho họ bằng cách sử dụng trải nghiệm lập lịch nguồn lực. Nếu một thành viên trong nhóm dự án có tên là nhân viên hợp đồng, thì có thể liên kết điều này với một mô tả hợp đồng phụ. Điều này sẽ thu hẹp nguồn lực khả dụng trên một mô tả hợp đồng phụ.
9.  Các nguồn lực của nhà thầu phụ có thể ghi lại thời gian, chi phí và việc sử dụng vật liệu cho các dự án và nhiệm vụ dự án, sau đó gửi để phê duyệt. Điều này cũng tương tự đối với nhân viên. Khi ghi lại thời gian, nhân viên hợp đồng có thể chọn một hợp đồng phụ và mô tả hợp đồng phụ cụ thể.
10. Sau khi được phê duyệt, thời gian được phê duyệt bởi các hợp đồng phụ sẽ ghi lại thực tế chi phí dự án dựa trên giá mua của nhân viên hợp đồng hoặc vai trò mà họ thực hiện trong dự án.
11. Hóa đơn của nhà cung cấp và các mục hàng trong hóa đơn của nhà cung cấp có thể được ghi lại trong hệ thống cho công việc được thực hiện bởi nguồn lực của nhà cung cấp hoặc các sản phẩm do nhà cung cấp phân phối. Các dòng hóa đơn của nhà cung cấp phải cụ thể cho một dự án và cho một loại giao dịch về thời gian, chi phí, sản phẩm/vật liệu, cột mốc hoặc phí. Theo tùy chọn, các dòng hóa đơn của nhà cung cấp có thể tham chiếu đến mô tả hợp đồng phụ.
12. Hệ thống sẽ tự động kết hợp tất cả các chi phí thực tế phù hợp với mô tả hợp đồng phụ và dự án với hóa đơn của nhà cung cấp. Điều này sẽ tạo điều kiện thuận lợi cho quá trình xác minh và đối sánh 3 bên.
13. Sau đó, người quản lý dự án có thể xem xét các thực tế dự án phù hợp tự động, xóa hoặc thêm các số liệu thực tế về chi phí dự án khác và hoàn tất quá trình xác minh.
14. Hoàn tất quá trình xác minh trên tất cả các dòng sẽ đánh dấu hóa đơn của nhà cung cấp là **Sẵn sàng thanh toán**. Ở giai đoạn này, hóa đơn của nhà cung cấp và các dòng có thể được chuyển sang hệ thống Kế toán hoặc Khoản phải trả để xử lý thanh toán cho nhà cung cấp. Các chi phí dự án đã ghi trước đó sẽ được hoàn nhập và chi phí thực tế từ dòng hóa đơn của nhà cung cấp sẽ được ghi vào dự án.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Mô tả hợp đồng phụ dựa trên số lượng và mô tả hợp đồng phụ dựa trên công việc

Mô tả hợp đồng phụ có thể dựa trên số lượng hoặc dựa trên công việc. 

Khi một mô tả hợp đồng phụ **dựa trên số lượng**, thì số lượng được mua dựa trên mô tả hợp đồng phụ về thời gian, chi phí hoặc vật liệu có thể được sử dụng cho bất kỳ dự án nào.

Khi mô tả hợp đồng phụ **dựa trên công việc**, thì mô tả hợp đồng phụ ánh xạ tới phần nội dung công việc được thể hiện bằng một nút trong kế hoạch dự án. Giá trị của mô tả hợp đồng phụ là tổng của tất cả các thành phần được yêu cầu để cung cấp nội dung công việc đó. Chúng được mô hình hóa dưới dạng chi tiết mô tả hợp đồng phụ và có thể là tập hợp thời gian, chi phí hoặc vật liệu. Đối với mô tả hợp đồng phụ dựa trên công việc, mô tả hợp đồng phụ cũng dành riêng cho một dự án duy nhất. Các loại hợp đồng phụ này hiện không được hỗ trợ trong Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

