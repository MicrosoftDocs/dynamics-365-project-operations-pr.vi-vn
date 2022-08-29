---
title: Bô trí nhân sự cho một dự án với nhân viên hợp đồng và năng lực của hợp đồng phụ
description: Bài viết này giải thích cách các yêu cầu của dự án có thể được nhân viên sử dụng nhân viên hợp đồng hoặc năng lực hợp đồng phụ trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8edb053467ef200ca3e051e2fd78106734318389
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261281"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Bô trí nhân sự cho một dự án với nhân viên hợp đồng và năng lực của hợp đồng phụ

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các thành viên trong nhóm dự án chung có thể được biên chế với nhân viên hoặc lao động hợp đồng. Khi bố trí nhân sự cho một dự án với các nhân viên hợp đồng, bạn có thể giới hạn các lựa chọn nhân sự của mình cho các nhân viên hợp đồng cụ thể được chỉ định cho một dây chuyền hợp đồng phụ. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Tìm kiếm các yêu cầu về nguồn nhân viên với các nhân viên hợp đồng thuộc một dây chuyền hợp đồng phụ cụ thể

Để tìm kiếm và các yêu cầu về nguồn nhân viên với nhân viên hợp đồng thuộc một dây chuyền hợp đồng phụ cụ thể, hãy làm theo các bước sau:

1. Tạo một thành viên nhóm dự án chung tham chiếu đến hợp đồng phụ và dòng hợp đồng phụ.
2. Tạo yêu cầu tài nguyên cho thành viên nhóm dự án chung này bằng cách sử dụng **Tạo yêu cầu** nút trên lưới phụ thành viên nhóm dự án.
3. Chọn hàng thành viên trong nhóm và sau đó chọn **Sách** trên lưới phụ. 
4. Thao tác này sẽ mở Bảng lịch trình với bối cảnh yêu cầu. Cùng với các thuộc tính khác như ngày tháng, vai trò và các trường đơn vị tổ chức, bộ lọc Bảng lập biểu cũng được tự động điền với các trường dòng nhà cung cấp, nhà thầu phụ và nhà thầu phụ từ yêu cầu tài nguyên.
5. Hệ thống tìm kiếm các tài nguyên đáp ứng các tiêu chí lọc và liệt kê chúng. 
6. Chọn một trong các tài nguyên đã lọc và đặt trước tài nguyên cho yêu cầu. 
7. Một thành viên trong nhóm dự án được tạo và cập nhật với các tham chiếu dòng hợp đồng phụ và hợp đồng phụ. Đi đến **Dự toán dự án** và chọn **Cập nhật giá** để xem chi phí cập nhật của việc phân công tài nguyên. 

> [!NOTE]
> Không phải lúc nào cũng có thể cập nhật thành viên nhóm dự án với tham chiếu dòng thầu phụ và hợp đồng phụ trong quá trình đặt trước nếu nguồn lực được chỉ định cho nhiều dòng hợp đồng phụ. Nếu hệ thống không thể cập nhật thành viên nhóm dự án với dòng hợp đồng phụ và hợp đồng phụ, thì hãy mở hồ sơ thành viên nhóm dự án và cập nhật thủ công các trường này để ước tính chi phí tài chính phản ánh chính xác chi phí nhà thầu phụ.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Tìm kiếm và các yêu cầu về nguồn nhân viên với bất kỳ nhân viên hợp đồng nào

Để tìm kiếm và các yêu cầu về nguồn nhân viên với bất kỳ nhân viên hợp đồng nào, hãy làm theo các bước sau:

1. Tạo một thành viên nhóm dự án chung.
2. Tạo yêu cầu tài nguyên cho thành viên nhóm dự án chung này bằng cách sử dụng **Tạo yêu cầu** nút trên lưới phụ thành viên nhóm dự án.
3. Chọn hàng thành viên trong nhóm và sau đó chọn **Sách** trên lưới phụ. 
4. Thao tác này sẽ mở Bảng lịch trình với bối cảnh yêu cầu. Cùng với các thuộc tính khác như ngày tháng, vai trò và các trường đơn vị tổ chức, bộ lọc Bảng lập biểu cũng được tự động điền với các trường dòng nhà cung cấp, nhà thầu phụ và nhà thầu phụ từ yêu cầu tài nguyên. Vì yêu cầu không có bất kỳ giá trị dòng hợp đồng phụ hoặc hợp đồng phụ nào được điền vào, các thuộc tính này sẽ trống trên ngăn bộ lọc.
5. Hệ thống tìm kiếm các tài nguyên đáp ứng các tiêu chí lọc và liệt kê chúng.
6. Cập nhật **Loại công nhân** trường trên ngăn bộ lọc để **Nhân viên hợp đồng** để hạn chế việc tìm kiếm lao động hợp đồng. Cập nhật **Người bán** trên ngăn bộ lọc để chọn nhà cung cấp để giới hạn tìm kiếm chỉ hiển thị nhân viên hợp đồng thuộc một công ty nhà cung cấp cụ thể.
7. Chọn một nhân viên hợp đồng từ danh sách và đăng ký tài nguyên cho yêu cầu.
8. Một thành viên trong nhóm dự án được tạo. Tuy nhiên, thành viên nhóm dự án không được cập nhật bất kỳ hợp đồng phụ hoặc dòng hợp đồng phụ nào và do đó việc phân công nguồn lực sẽ không bị tính phí khi sử dụng cách định giá hợp đồng phụ. Cập nhật thủ công thành viên nhóm dự án với dòng hợp đồng phụ và đi tới **Dự toán dự án** và chọn **Cập nhật giá** để xem chi phí cập nhật của việc phân công tài nguyên.

> [!NOTE]
> Các thành viên trong nhóm dự án có **Loại công nhân** như **Nhân viên hợp đồng** nhưng không có tham chiếu hợp đồng phụ được gắn cờ là **Không hợp lệ** trên **Thành viên nhóm dự án** lưới điện. Nếu có bất kỳ thành viên nào trong nhóm dự án có trạng thái này, hãy mở hồ sơ thành viên nhóm dự án và cập nhật thủ công các trường dòng hợp đồng phụ và hợp đồng phụ để ước tính chi phí tài chính phản ánh chính xác chi phí của nhà thầu phụ trên **Ước tính** chuyển hướng. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
