---
title: Dòng báo giá dựa trên sản phẩm chi phí
description: Chủ đề này cung cấp thông tin về cách áp dụng giá vốn vào mô tả báo giá dựa trên sản phẩm.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001907"
---
# <a name="costing-product-based-quote-lines"></a>Dòng báo giá dựa trên sản phẩm chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Các dòng báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations cũng có trường **Giá vốn**. Trường này được sử dụng để theo dõi giá vốn của sản phẩm trên mô tả báo giá và để tính toán lợi nhuận trong tương lai.

Khi mô tả báo giá dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí của mô tả báo giá dựa trên sản phẩm được mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm. Trường chi phí tiêu chuẩn trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức. Chi phí đơn vị mặc định trên mô tả báo giá dựa trên sản phẩm được chuyển đổi thành đơn vị tiền tệ bán hàng trên báo giá.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Chi phí đơn vị trên mô tả báo giá dựa trên sản phẩm

Mục đích của việc có chi phí đơn vị trên mô tả báo giá dựa trên sản phẩm là cho phép các chi phí khác nhau cho một sản phẩm cho mỗi lần bán hàng. Đây không phải là một kịch bản điển hình, nhưng đôi khi chi phí của sản phẩm có thể được nhà cung cấp chiết khấu tùy thuộc vào khách hàng của đợt bán hàng cuối cùng.

Ví dụ:

Fabrikam Robotics đang lắp đặt các cánh tay robot tại dây chuyền lắp ráp của A Datum Corporation. Fabrikam cung cấp dịch vụ lắp đặt nhưng các cánh tay robot được mua từ công ty chế tạo robot Trey. Nếu việc lắp đặt cánh tay robot tại A Datum Corporation mở ra một ngành công nghiệp mới cho cánh tay robot của Trey, Trey có thể giảm giá đặc biệt đối với giao dịch này cho Fabrikam.

Trong trường hợp này, Fabrikam sẽ tạo dòng báo giá dựa trên sản phẩm cho cánh tay robot và nhập một chi phí đặc biệt trên mỗi đơn vị cho báo giá này. Chi phí này khác với chi phí tiêu chuẩn của cánh tay robot Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]