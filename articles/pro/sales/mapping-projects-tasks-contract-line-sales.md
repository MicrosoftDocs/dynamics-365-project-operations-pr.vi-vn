---
title: Ánh xạ dự án và nhiệm vụ với mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Bài viết này cung cấp thông tin về cách thêm và xóa các dự án và nhiệm vụ vào một dòng hợp đồng.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c8075e3161acd904969f964e5ab32dfe04edc4b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932552"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Ánh xạ dự án và nhiệm vụ với mô tả hợp đồng dựa trên dự án 

_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

Trên các mô tả hợp đồng dựa trên dự án, bạn có thể ánh xạ các nhiệm vụ cụ thể trong một dự án vào mô tả hợp đồng.

Khi bạn ánh xạ các nhiệm vụ cụ thể vào một mô tả hợp đồng, phương thức thanh toán, tùy chọn khả năng tính phí, Giới hạn không vượt quá và khách hàng được xác định trên mô tả hợp đồng sẽ chỉ áp dụng cho các nhiệm vụ cụ thể đó.

Nếu có trường hợp trong đó một giai đoạn của dự án, chẳng hạn như Giai đoạn nguyên mẫu, là giá cố định và tất cả giai đoạn khác là thời gian và vật tư, thì bạn sẽ có thể liên kết Giai đoạn nguyên mẫu và tất cả nhiệm vụ con liên quan với mô tả hợp đồng cho giai đoạn đó qua một phương thức thanh toán giá cố định.

Bạn có thể liên kết tất cả giai đoạn khác trong cấu trúc phân tích công việc (WBS) dự án của mình với mô tả hợp đồng dựa trên thời gian và vật tư.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Liên kết các nhiệm vụ với mô tả hợp đồng dựa trên dự án

Bạn có thể liên kết các nhiệm vụ với mô tả hợp đồng từ tab **Nhiệm vụ phải thanh toán** trên trang **Mô tả hợp đồng** hoặc từ tab **Thanh toán nhiệm vụ** trên trang **Dự án**.

### <a name="from-the-contract-line-page"></a>Từ trang Mô tả hợp đồng

Hoàn thành các bước sau để liên kết các nhiệm vụ dự án với mô tả hợp đồng từ tab **Nhiệm vụ phải thanh toán** của trang **Mô tả hợp đồng**.

1. Trên tab **Tổng quát** của mô tả hợp đồng dựa trên dự án, hãy xác minh rằng trường **Dự án** được điền.
2. Trong trường **Nhiệm vụ được đưa vào**, hãy chọn **Chỉ các nhiệm vụ đã chọn**.
3. Lưu thay đổi của bạn. Biểu mẫu sẽ làm mới và tab **Nhiệm vụ phải thanh toán** sẽ hiển thị.
4. Chọn **Nhiệm vụ phải thanh toán** và trong lưới con, hãy chọn **Thêm một nhiệm vụ vào mô tả hợp đồng**.
5. Trên trang **Nhiệm vụ có trong mô tả hợp đồng**, trong danh sách thả xuống **Nhiệm vụ**, hãy chọn nhiệm vụ đó. 
6. Nhập thông tin vào trường **Loại hình thanh toán**, sau đó chọn **Lưu và đóng**. Nhiệm vụ đã chọn được liên kết với mô tả hợp đồng.

> [!NOTE]
> Đây không phải là trải nghiệm tối ưu nhất để liên kết các nhiệm vụ dự án với mô tả hợp đồng. Mỗi dự án sẽ phải được liên kết theo cách thủ công trong trải nghiệm này. Cách ưa dùng là từ tab **Thanh toán nhiệm vụ** trên trang **Dự án**.

### <a name="from-the-project-page"></a>Từ trang dự án

Đây là phương pháp tối ưu để liên kết nhiệm vụ với mô tả hợp đồng. Bạn có thể chọn nhiều nhiệm vụ và liên kết tất cả chúng cũng như các nhiệm vụ con của chúng với mô tả hợp đồng đã chọn. Hoàn thành các bước sau để liên kết nhiệm vụ với mô tả hợp đồng từ trang **Dự án**.

1. Trên tab **Tổng quát** của mô tả hợp đồng dựa trên dự án, hãy xác minh rằng trường **Dự án** được điền.
2. Trong trường **Nhiệm vụ được đưa vào**, hãy chọn **Chỉ các nhiệm vụ đã chọn**.
3. Lưu mô tả hợp đồng dựa trên dự án. Biểu mẫu sẽ làm mới và tab **Nhiệm vụ phải thanh toán** sẽ hiển thị. Điều này chỉ nhằm mục đích xác minh.
4. Trên tab **Tổng quát** của mô tả hợp đồng dựa trên dự án, trong trường **Dự án**, hãy chọn liên kết dự án.
5. Trên trang **Dự án**, hãy chọn tab **Thiết lập tùy chọn thanh toán nhiệm vụ**.
6. Có hai lưới. Một lưới dành cho các mô tả hợp đồng áp dụng cho toàn bộ dự án. Lưới thứ hai áp dụng cho thiết lập thanh toán theo nhiệm vụ cụ thể. Trong lưới thứ hai, hãy chọn một hoặc nhiều nhiệm vụ, sau đó chọn **Liên kết mô tả hợp đồng**.
7. Trong trang hộp thoại mở ra, hãy chọn một mô tả hợp đồng từ danh sách thả xuống.
8. Sử dụng danh sách thả xuống **Loại hình thanh toán** để đánh dấu các nhiệm vụ là phải thanh toán hoặc không phải thanh toán.
9. Chọn hộp kiểm để cho biết liệu quy trình liên kết có nên bao gồm cả nhiệm vụ con của các nhiệm vụ đã chọn hay không. Chọn hộp này cũng sẽ liên kết nhiệm vụ con của các nhiệm vụ đã chọn với mô tả hợp đồng.
10. Chọn **OK** để đóng hộp thoại.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Hủy liên kết các nhiệm vụ với mô tả hợp đồng dựa trên dự án

### <a name="from-the-contract-line-page"></a>Từ trang mô tả hợp đồng

Hoàn thành các bước sau để hủy liên kết các nhiệm vụ dự án với mô tả hợp đồng trên tab **Nhiệm vụ phải thanh toán** của trang **Mô tả hợp đồng**.

1. Trên tab **Nhiệm vụ phải thanh toán**, hãy chọn **Xóa nhiệm vụ liên kết với mô tả hợp đồng**.
2. Một thông báo cảnh báo cho biết rằng thao tác loại bỏ liên kết này có thể dẫn đến việc đảo ngược bất kỳ giá trị thực tế nào đã được ghi lại trước đó trên nhiệm vụ. Chọn **OK** trên hộp thoại để loại bỏ liên kết giữa nhiệm vụ và mô tả hợp đồng dựa trên dự án. 

> [!NOTE]
> Thao tác này không xóa nhiệm vụ khỏi dự án. Thay vào đó, thao tác này loại bỏ liên kết nhiệm vụ với mô tả hợp đồng dựa trên dự án.

### <a name="from-the-project-page"></a>Từ trang dự án

Đây là trải nghiệm tối ưu hơn để hủy liên kết nhiệm vụ với mô tả hợp đồng. Bạn có thể chọn nhiều nhiệm vụ và hủy liên kết tất cả chúng cũng như các nhiệm vụ con của chúng với mô tả hợp đồng đã chọn. Hoàn thành các bước sau để hủy liên kết nhiệm vụ với mô tả hợp đồng.

1. Từ tab **Tổng quát** của mô tả hợp đồng dựa trên dự án, trong trường **Dự án**, hãy nhấp vào liên kết của dự án.
2. Trên trang **Dự án**, hãy chọn tab **Thiết lập tùy chọn thanh toán nhiệm vụ**.
3. Có hai lưới trên trang. Một lưới dành cho các mô tả hợp đồng áp dụng cho toàn bộ dự án và lưới thứ hai áp dụng cho thiết lập thanh toán theo nhiệm vụ. Trong lưới thứ hai, hãy chọn một hoặc nhiều nhiệm vụ, sau đó chọn **Hủy liên kết mô tả hợp đồng**.
4. Trong trang hộp thoại mở ra, hãy chọn một mô tả hợp đồng từ danh sách thả xuống.
5. Chọn hộp kiểm để cho biết liệu có nên loại bỏ cả quy trình liên kết khỏi nhiệm vụ con bất kỳ của các nhiệm vụ đã chọn hay không. Chọn hộp này cũng sẽ hủy liên kết nhiệm vụ con của các nhiệm vụ đã chọn với mô tả hợp đồng.
6. Chọn **OK**. Một thông báo cảnh báo cho biết rằng thao tác loại bỏ liên kết này có thể dẫn đến việc đảo ngược bất kỳ giá trị thực tế nào đã được ghi lại trước đó trên nhiệm vụ. Chọn **OK** trên hộp thoại cảnh báo để loại bỏ liên kết giữa nhiệm vụ và mô tả hợp đồng dựa trên dự án.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
