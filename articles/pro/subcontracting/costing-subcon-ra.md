---
title: Ước tính chi phí của các nhiệm vụ nguồn lực trong hợp đồng phụ
description: Bài viết này giải thích một số cách Microsoft Dynamics 365 Project Operations tính toán ước tính chi phí của các phân công nguồn lực trong hợp đồng phụ.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522682"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Ước tính chi phí của các nhiệm vụ nguồn lực trong hợp đồng phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Việc phân công nhiệm vụ của các thành viên nhóm dự án có hợp đồng phụ được tính bằng cách sử dụng bảng giá **Mua** đính kèm hợp đồng phụ trên bản ghi thành viên nhóm liên quan. Điều này khác với cách tính chi phí phân công nguồn lực nhân viên trong đó phân công nhiệm vụ của nguồn lực nhân viên được tính bằng cách sử dụng bảng giá **Chi phí** đính kèm với đơn vị hợp đồng của dự án. 

Đối với thành viên nhóm hợp đồng chung có hợp đồng phụ, việc phân công được tính phí bằng thiết lập giá dựa trên vai trò trong bảng giá mua được đính kèm với hợp đồng phụ. Giá mua cũng có thể được thiết lập cụ thể cho từng nguồn lực. Các mức giá dành riêng cho nguồn lực này sẽ được ưu tiên khi chi phí phân công nhiệm vụ của các thành viên nhóm dự án được có tên là nhân viên hợp đồng. 

Mức độ ưu tiên của việc sử dụng giá mua theo từng vai trò so với theo từng nguồn lực dựa trên việc thiết lập mức độ ưu tiên của thứ nguyên đặt giá trong **Tham số > Thứ nguyên định giá dựa trên vai trò**.

Chức năng tính giá động này dựa trên thiết lập thứ nguyên cho giá mua của nhà thầu phụ tương tự như cách tính chi phí và tỷ lệ hóa đơn cho nhân viên toàn thời gian. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tạo phân công nhiệm vụ để nhận được ước tính chi phí của các nguồn lực nhà thầu phụ

Có thể tạo phân công nhiệm vụ cho nhà thầu phụ theo hai cách: 
- Sử dụng tab **Nhiệm vụ**.
- Sử dụng tab **Nhóm**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Tạo phân công nguồn lực bằng tab Nhiệm vụ
Sử dụng danh sách **Nguồn lực** trong tab **Nhiệm vụ** cho một nhiệm vụ cụ thể, bạn có thể tạo một phân công nhiệm vụ cho một nguồn lực có tên hoặc nguồn lực chung. Nếu bạn chọn một nguồn lực được đặt tên từ menu thả xuống **Nguồn lực được phân công** trên nhiệm vụ và nguồn lực này là nhân viên hợp đồng, nguồn lực có tên được phân công cho nhiệm vụ và bản ghi thành viên nhóm dự án tương ứng được tạo với loại nhân công được đặt thành **Nhân viên hợp đồng** và **Hiệu lực** được đặt thành **Không hợp lệ**. Bước tiếp theo, bạn sẽ cần mở bản ghi thành viên nhóm dự án và chọn một hợp đồng phụ và mô tả hợp đồng phụ. Thao tác này sẽ cập nhật phân công nhiệm vụ để có tham chiếu đến hợp đồng phụ và mô tả hợp đồng phụ và cũng sẽ cập nhật trạng thái thành viên nhóm thành **Hợp lệ**.

Nếu bạn chọn tạo một thành viên nhóm chung từ menu thả xuống **Nguồn lực được phân công** trên nhiệm vụ, hộp thoại **Tạo thành viên nhóm chung** sẽ cho phép bạn chọn một hợp đồng phụ và mô tả hợp đồng phụ. Khi nguồn lực chung được chỉ định cho nhiệm vụ và bản ghi thành viên nhóm dự án tương ứng được tạo, bạn sẽ nhận thấy rằng bản ghi thành viên nhóm dự án được tạo với loại nhân công được đặt thành **Nhân viên hợp đồng** và **Hiệu lực** được đặt thành **Có hiệu lực**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Tạo thành viên nhóm dự án bằng tab Nhóm
Sử dụng tab Nhóm trên dự án, bạn có thể tạo một thành viên chung hoặc một thành viên nhóm có tên. Khi tạo thành viên nhóm, bạn có thể chọn mô tả hợp đồng phụ và hợp đồng phụ. Sau khi thành viên nhóm được tạo, bạn sẽ cần phân công cho thành viên nhóm một nhiệm vụ bằng cách sử dụng menu thả xuống **Nguồn lực được phân công** trên nhiệm vụ. 

## <a name="updating-estimates"></a>Cập nhật ước tính
Sau khi bạn đã chỉ định thành viên nhóm dự án vào nhiệm vụ, bạn sẽ cần điều hướng đến tab **Ước tính** trên dự án và chọn **Cập nhật giá** để đảm bảo rằng tỷ lệ chi phí của việc phân công nguồn lực của nhà thầu phụ được cập nhật dựa trên bảng giá mua đính kèm với hợp đồng phụ. Ước tính không được tạo cho các nhiệm vụ chưa được phân công trong Microsoft Dynamics 365 Project Operations. Do đó, bạn sẽ cần tạo các phân công nhiệm vụ vào các nhiệm vụ về giá và chi phí trên dự án của mình. 

> [LƯU Ý!] Thành viên nhóm dự án có **Loại nhân công** như **Nhân viên hợp đồng** nhưng không có tham chiếu hợp đồng phụ được gắn cờ là **Không hợp lệ** trên lưới **Thành viên nhóm dự án**. Nếu bất kỳ thành viên nhóm dự án nào có trạng thái này, hãy mở bản ghi thành viên nhóm dự án và cập nhật thủ công các trường hợp đồng phụ và mô tả hợp đồng phụ sao cho ước tính chi phí tài chính phản ánh chính xác chi phí thầu phụ trên tab **Ước tính**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
