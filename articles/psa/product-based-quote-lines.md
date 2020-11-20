---
title: Mô tả báo giá dựa trên sản phẩm
description: Chủ đề này cung cấp thông tin về mô tả báo giá dựa trên sản phẩm.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
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
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123246"
---
# <a name="product-based-quote-lines"></a>Mô tả báo giá dựa trên sản phẩm

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Service Automation. Mô tả báo giá dựa trên sản phẩm có thể là mô tả chọn thêm hoặc các mục từ danh mục sản phẩm.

## <a name="product-catalog"></a>Danh mục sản phẩm

Các sản phẩm trong danh mục sản phẩm Dynamics 365 có đơn vị mặc định và nhóm đơn vị đo. Nếu một số sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó. Tất cả sản phẩm trong một dòng sản phẩm thừa kế cùng bộ thuộc tính.

Ví dụ: công ty bán các giấy phép gói đăng ký cho một loạt các phần mềm. Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:

- Số người dùng 
- Thời gian đăng ký (trong tháng)

Cách tốt nhất để duy trì loại danh mục này là tạo dòng sản phẩm có tên **Phần mềm đăng ký** và **Số người dùng** và **Khoảng thời gian đăng ký** ở dạng thuộc tính. Sau đó, bạn có thể thêm từng sản phẩm, chẳng hạn như **Dynamics 365 Sales** hoặc **Dynamics 365 Field Service** vào dòng sản phẩm **Phần mềm đăng ký**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Thêm các mục danh mục sản phẩm vào báo giá dự án

Các trang báo giá dự án và hợp đồng dự án có các phần cho 2 loại mô tả: mô tả dựa trên dự án và mô tả dựa trên sản phẩm. Đối với các mô tả dựa trên sản phẩm, Dynamics 365 dùng để thêm mục từ danh mục sản phẩm vào báo giá. Danh sách thả xuống trên mô tả báo giá hoặc mô tả hợp đồng dự án bao gồm tất cả sản phẩm và đơn vị trong bảng giá sản phẩm được đính kèm với báo giá hoặc hợp đồng dự án. Bạn cũng có thể thêm các sản phẩm không phải một phần trong bảng giá sản phẩm của báo giá.

Ngoài ra, bạn có thể chọn các sản phẩm từ bảng giá khác hoặc chọn các sản phẩm trực tiếp từ danh mục sản phẩm. Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng để nhận giá bán hàng của sản phẩm. Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về 0 (không).

Nếu mô tả báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả báo giá. Lưu ý rằng mô tả báo giá trong Dynamics 365 có trường **Giá**. Có hai giá trị:

- Thay thế giá  
- Dùng mặc định

Nếu bạn đặt trường này thành **Thay thế giá**, Dynamics 365 không đặt giá mặc định. Bạn phải nhập giá cho sản phẩm trên mô tả báo giá. Nếu bạn đặt trường này thành **Dùng mặc định**, Dynamics 365 sử dụng giá bán hàng mặc định và khóa trường để ngăn chỉnh sửa.

Sau khi bạn cài đặt PSA, giá bán hàng mặc định được nhập trên mô tả dựa trên sản phẩm trên báo giá. Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả báo giá.

> ![Đặt giá thay thế](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Yếu tố số lượng cho sản phẩm

PSA sử dụng các yếu tố số lượng để hỗ trợ việc bán các sản phẩm dựa trên đăng ký. Đối với các sản phẩm dựa trên đăng ký, số lượng trên báo giá hoặc mô tả hợp đồng dự án được thể hiện ở dạng số tháng người dùng.

Thông thường, giá phần mềm đăng ký được lưu trữ trong danh mục ở dạng giá cho mỗi người dùng mỗi tháng. Tuy nhiên, bạn có thể sử dụng mô tả thời gian khác thay thế. Trong quá trình bán hàng, giá trên mô tả báo giá thường là giá trên mỗi người dùng, mỗi tháng được đại lý bán hàng CNTT thương lượng và giảm giá. Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau. Số lượng được dùng để tính toán lượng mô tả báo giá là sản phẩm của số lượng người dùng và số lượng tháng đăng ký.

Để hỗ trợ loại bán hàng này, PSA giới thiệu khái nhiệm yếu tố số lượng. Yếu tố số lượng dựa vào các thuộc tính sản phẩm trong Dynamics 365. Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, PSA cho phép bạn gắn cờ một tập con của các thuộc tính đó hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.

PSA xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng. Khi sản phẩm mà các yếu tố số lượng được đặt cấu hình được thêm vào mô tả báo giá, thì trường **Số lượng** trên mô tả báo giá trở thành trường chỉ đọc. Sau khi bạn nhập giá trị cho các thuộc tính sản phẩm là các yếu tố số lượng, PSA tính số lượng của mô tả báo giá.

Ví dụ: Dynamics 365 có thể có các thuộc tính sau đây: 

- **Không có người dùng** – Số lượng người dùng 
- **Không có tháng** – Số lượng tháng đăng ký
- **SKU sản phẩm** 

Các thuộc tính **Không có người dùng** và **Không có tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm. 

> ![Gắn cờ Không có người dùng và Không có tháng ở dạng các yếu tố chất lượng](media/basic-guide-11.png)
 
