---
title: Sao chép cơ hội dựa trên dự án
description: Chủ đề này cung cấp thông tin về việc sao chép cơ hội dựa trên dự án trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26ae5cc267bb06f958bbf9cdce2d80ccde9d3d24
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181716"
---
# <a name="copy-project-based-opportunities"></a>Sao chép cơ hội dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Cơ hội dự án có thể được sao chép dễ dàng để tạo cơ hội dự án mới. 

1. Hãy chuyển tới trang danh sách **Cơ hội dự án** và chọn một cơ hội trong danh sách. Hoặc, mở trang chi tiết của một cơ hội cụ thể. 
2. Ở một trong hai trang đó, hãy chọn **Sao chép**. Một trang hộp thoại chứa thông tin trường sau đây sẽ mở ra. Tùy theo giá trị được chọn trong hộp thoại này, quá trình sao chép có thể thay đổi.

    | **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
    | --- | --- | --- |
    | Chủ đề | Nhập chủ đề thích hợp của cơ hội mục tiêu. Khi hộp thoại mở ra, hệ thống sẽ đặt mục này thành chủ đề của cơ hội nguồn kèm theo **- sao chép**. | Không có tác động xuôi tuyến đối với trường này. |
    | T.khoản | Tham chiếu bản ghi công ty hoặc tài khoản của khách hàng. Khi hộp thoại mở ra, hệ thống sẽ đặt mục này thành khách hàng trên cơ hội nguồn. | Trường này là khách hàng chính trên cơ hội. |
    | Đơn vị Hợp đồng | Đơn vị tổ chức chịu trách nhiệm bàn giao dự án liên quan đến thỏa thuận này. Khi hộp thoại mở ra, hệ thống sẽ đặt mục này thành đơn vị ký hợp đồng trên cơ hội nguồn. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ và đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |
    | Tiền tệ | Đơn vị tiền tệ giao dịch trong thỏa thuận. Khi trang hộp thoại mở ra, hệ thống sẽ đặt mục này thành đơn vị tiền tệ trên cơ hội nguồn. | Đơn vị tiền tệ được sử dụng để lấy mặc định bảng giá và xây dựng giá trị ước tính tài chính trên báo giá. Cuối cùng, đơn vị tiền tệ được sử dụng để lập hóa đơn cho khách hàng khi thỏa thuận được chốt. |
    | Sao chép giá | Giá trị Có/Không cho biết liệu giá trên cơ hội có được sao chép từ cơ hội nguồn hay không. | Nếu là **Có**, thì bảng giá được sao chép từ cơ hội nguồn sang cơ hội mục tiêu. Nếu bạn chọn **Không**, thì bảng giá được lấy mặc định dựa trên bảng giá mới nhất đã được thiết lập. |

3. Chọn **OK**. Hệ thống tạo một bản sao cơ hội dự án dựa trên các tham số đã chọn và cơ hội dự án mới được mở ra.
