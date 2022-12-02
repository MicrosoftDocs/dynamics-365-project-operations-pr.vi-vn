---
title: Bô trí nhân sự cho một dự án với nhân viên hợp đồng và năng lực của hợp đồng phụ
description: Bài viết này giải thích cách các yêu cầu của dự án có thể được bố trí nguồn lực bằng cách sử dụng nhân viên hợp đồng hoặc năng lực hợp đồng phụ trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522462"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Bô trí nhân sự cho một dự án với nhân viên hợp đồng và năng lực của hợp đồng phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các thành viên nhóm dự án chung có thể được bố trí cùng với nhân viên hoặc nhân viên hợp đồng. Khi bố trí nhân sự cho một dự án bằng nhân viên hợp đồng, bạn có thể giới hạn các lựa chọn nhân sự của mình cho các nhân viên hợp đồng cụ thể được phân công vào mô tả hợp đồng phụ. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Tìm kiếm các yêu cầu nguồn lực với các nhân viên hợp đồng thuộc một mô tả hợp đồng phụ cụ thể

Để tìm kiếm và cung cấp các yêu cầu nguồn lực bằng các nhân viên hợp đồng thuộc một mô tả hợp đồng phụ cụ thể, hãy làm theo các bước sau:

1. Tạo một thành viên nhóm dự án chung có tham chiếu tới hợp đồng phụ và mô tả hợp đồng phụ.
2. Tạo yêu cầu nguồn lực cho thành viên nhóm dự án chung này bằng cách sử dụng nút **Tạo yêu cầu** trên lưới phụ thành viên nhóm dự án.
3. Chọn hàng thành viên nhóm và sau đó chọn nút **Đặt** trên lưới phụ. 
4. Thao tác này sẽ mở Bảng lịch trình với ngữ cảnh yêu cầu. Cùng với các thuộc tính khác như ngày tháng, vai trò và các trường đơn vị tổ chức, bộ lọc Bảng lịch trình cũng được tự động điền với các trường nhà cung cấp, hợp đồng phụ và mô tả hợp đồng phụ từ yêu cầu nguồn lực.
5. Hệ thống tìm kiếm các nguồn lực đáp ứng tiêu chí bộ lọc và liệt kê chúng. 
6. Chọn một trong các nguồn lực đã lọc và đặt nguồn lực cho yêu cầu. 
7. Thành viên nhóm dự án được tạo và cập nhật với tham chiếu hợp đồng phụ và mô tả hợp đồng phụ. Chuyển đến **Ước tính dự án** và chọn **Cập nhật giá** để xem chi phí cập nhật của phân công nguồn lực. 

> [!NOTE]
> Không phải lúc nào cũng có thể cập nhật thành viên nhóm dự án với tham chiếu mô tả hợp đồng phụ và hợp đồng phụ trong quá trình đặt nếu nguồn lực được chỉ định cho nhiều mô tả hợp đồng phụ. Nếu hệ thống không thể cập nhật thành viên nhóm dự án với mô tả hợp đồng phụ và hợp đồng phụ, thì hãy mở bản ghi thành viên nhóm dự án và cập nhật thủ công các trường này để ước tính chi phí tài chính phản ánh chính xác chi phí nhà thầu phụ.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Tìm kiếm và bố trí nguồn lực cho yêu cầu nguồn lực bằng bất kỳ nhân viên hợp đồng nào

Để tìm kiếm và bố trí nguồn lực cho yêu cầu nguồn lực bằng bất kỳ nhân viên hợp đồng nào, hãy làm theo các bước sau:

1. Tạo thành viên nhóm dự án chung.
2. Tạo yêu cầu nguồn lực cho thành viên nhóm dự án chung này bằng cách sử dụng nút **Tạo yêu cầu** trên lưới phụ thành viên nhóm dự án.
3. Chọn hàng thành viên nhóm và sau đó chọn nút **Đặt** trên lưới phụ. 
4. Thao tác này sẽ mở Bảng lịch trình với ngữ cảnh yêu cầu. Cùng với các thuộc tính khác như ngày tháng, vai trò và các trường đơn vị tổ chức, bộ lọc Bảng lịch trình cũng được tự động điền với các trường nhà cung cấp, hợp đồng phụ và mô tả hợp đồng phụ từ yêu cầu nguồn lực. Vì yêu cầu không có bất kỳ giá trị mô tả hợp đồng phụ hoặc hợp đồng phụ nào được điền vào, các thuộc tính này sẽ trống trên ngăn bộ lọc.
5. Hệ thống tìm kiếm các nguồn lực đáp ứng tiêu chí bộ lọc và liệt kê chúng.
6. Cập nhật trường **Loại nhân công** trên ngăn bộ lọc thành **Nhân viên hợp đồng** để giới hạn tìm kiếm ở nhân viên hợp đồng. Cập nhật **Nhà cung cấp** trên ngăn bộ lọc để chọn nhà cung cấp nhằm giới hạn tìm kiếm chỉ hiển thị nhân viên hợp đồng thuộc một công ty nhà cung cấp cụ thể.
7. Chọn một nhân viên hợp đồng từ danh sách và đặt nguồn lực cho yêu cầu.
8. Thành viên nhóm dự án được tạo. Tuy nhiên, thành viên nhóm dự án không được cập nhật bất kỳ hợp đồng phụ hoặc mô tả hợp đồng phụ nào và do đó việc phân công nguồn lực sẽ không bị tính phí khi sử dụng định giá hợp đồng phụ. Cập nhật thủ công thành viên nhóm dự án với mô tả hợp đồng phụ và đi tới **Ước tính dự án** và chọn **Cập nhật giá** để xem chi phí cập nhật của việc phân công nguồn lực.

> [!NOTE]
> Thành viên nhóm dự án có **Loại nhân công** như **Nhân viên hợp đồng** nhưng không có tham chiếu hợp đồng phụ được gắn cờ là **Không hợp lệ** trên lưới **Thành viên nhóm dự án**. Nếu bất kỳ thành viên nhóm dự án nào có trạng thái này, hãy mở bản ghi thành viên nhóm dự án và cập nhật thủ công các trường hợp đồng phụ và mô tả hợp đồng phụ sao cho ước tính chi phí tài chính phản ánh chính xác chi phí thầu phụ trên tab **Ước tính**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
