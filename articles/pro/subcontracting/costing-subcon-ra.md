---
title: Ước tính chi phí của các nhiệm vụ nguồn lực trong hợp đồng phụ
description: Bài viết này giải thích một số cách Microsoft Dynamics 365 Project Operations tính toán ước tính chi phí của các phân công tài nguyên được thầu phụ.
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

Việc phân công nhiệm vụ của các thành viên trong nhóm dự án được ký hợp đồng phụ được tính bằng cách sử dụng **Mua, tựa vào, bám vào** bảng giá kèm theo hợp đồng phụ trên hồ sơ thành viên đội liên quan. Điều này khác với cách tính chi phí của các nhiệm vụ tài nguyên của nhân viên trong đó các nhiệm vụ phân công tài nguyên của nhân viên được tính bằng cách sử dụng **Phí tổn** bảng giá kèm theo đơn giá thầu của dự án. 

Đối với các thành viên trong nhóm dự án chung được ký hợp đồng phụ, các nhiệm vụ được tính giá bằng cách sử dụng thiết lập giá dựa trên vai trò trong bảng giá mua kèm theo hợp đồng phụ. Giá mua cũng có thể được thiết lập cụ thể cho từng tài nguyên. Các mức giá dành riêng cho tài nguyên này sẽ được ưu tiên khi chi phí giao nhiệm vụ của các thành viên nhóm dự án được nêu tên là nhân viên hợp đồng. 

Mức độ ưu tiên của việc sử dụng giá mua cụ thể theo vai trò so với giá cụ thể theo tài nguyên được thúc đẩy bởi việc thiết lập mức độ ưu tiên của thứ nguyên đặt giá trong **Tham số> Thứ nguyên đặt giá dựa trên số lượng**.

Chức năng tính giá động này dựa trên thiết lập thứ nguyên cho giá mua của nhà thầu phụ tương tự như cách tính chi phí và tỷ lệ hóa đơn cho nhân viên toàn thời gian. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Tạo phân công nhiệm vụ để nhận được ước tính chi phí của các nguồn lực của nhà thầu phụ

Có thể tạo nhiệm vụ cho nhà thầu phụ theo hai cách: 
- Sử dụng **Nhiệm vụ** chuyển hướng.
- Sử dụng **Đội** chuyển hướng.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Tạo nhiệm vụ tài nguyên bằng tab Nhiệm vụ
Sử dụng **Tài nguyên** danh sách trong **Nhiệm vụ** cho một nhiệm vụ cụ thể, bạn có thể tạo một phân công nhiệm vụ cho một tài nguyên đã đặt tên hoặc một tài nguyên chung. Nếu bạn chọn một tài nguyên được đặt tên từ **Tài nguyên được chỉ định** thả xuống nhiệm vụ và tài nguyên này là nhân viên hợp đồng, tài nguyên được đặt tên được chỉ định cho nhiệm vụ và bản ghi thành viên nhóm dự án tương ứng được tạo với loại công nhân được đặt thành **Nhân viên hợp đồng** và **Hiệu lực** đặt thành **Không hợp lệ**. Bước tiếp theo, bạn sẽ cần mở hồ sơ thành viên nhóm dự án và chọn một hợp đồng phụ và dòng hợp đồng phụ. Thao tác này sẽ cập nhật phân công nhiệm vụ để có tham chiếu đến hợp đồng phụ và dòng hợp đồng phụ và cũng sẽ cập nhật trạng thái thành viên trong nhóm lên **Có giá trị**.

Nếu bạn chọn tạo một thành viên nhóm chung từ **Tài nguyên được chỉ định** thả xuống nhiệm vụ, **Tạo thành viên nhóm chung** hộp thoại sẽ cho phép bạn chọn một hợp đồng phụ và dòng hợp đồng phụ. Khi tài nguyên chung được chỉ định cho nhiệm vụ và bản ghi thành viên nhóm dự án tương ứng được tạo, bạn sẽ nhận thấy rằng bản ghi thành viên nhóm dự án được tạo với loại công nhân được đặt thành **Nhân viên hợp đồng** và **Hiệu lực** đặt thành **Có giá trị**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Tạo thành viên nhóm dự án bằng tab Nhóm
Sử dụng tab Nhóm trên dự án, bạn có thể tạo một thành viên chung hoặc một thành viên trong nhóm được đặt tên. Khi tạo thành viên trong nhóm, bạn có thể chọn dòng hợp đồng phụ và hợp đồng phụ. Sau khi thành viên trong nhóm được tạo, bạn sẽ cần chỉ định thành viên trong nhóm một nhiệm vụ bằng cách sử dụng **Tài nguyên được chỉ định** trình đơn thả xuống nhiệm vụ. 

## <a name="updating-estimates"></a>Cập nhật ước tính
Sau khi bạn đã chỉ định các thành viên trong nhóm dự án cho các nhiệm vụ, bạn sẽ cần điều hướng đến **Ước tính** trên dự án và chọn **Cập nhật giá** để đảm bảo rằng tỷ lệ chi phí của việc phân công nguồn lực của nhà thầu phụ được cập nhật dựa trên bảng giá mua kèm theo hợp đồng phụ. Ước tính không được tạo cho các nhiệm vụ chưa được giao trong Microsoft Dynamics 365 Project Operations. Do đó, bạn sẽ cần tạo các phân công nhiệm vụ để định giá và định giá các nhiệm vụ khác nhau trong dự án của mình. 

> [LƯU Ý!] Các thành viên trong nhóm dự án có **Loại công nhân** như **Nhân viên hợp đồng** nhưng không có tham chiếu hợp đồng phụ được gắn cờ là **Không hợp lệ** trên **Thành viên nhóm dự án** lưới điện. Nếu có bất kỳ thành viên nào trong nhóm dự án có trạng thái này, hãy mở hồ sơ thành viên nhóm dự án và cập nhật thủ công các trường dòng hợp đồng phụ và hợp đồng phụ để ước tính chi phí tài chính phản ánh chính xác chi phí nhà thầu phụ trên **Ước tính** chuyển hướng. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
