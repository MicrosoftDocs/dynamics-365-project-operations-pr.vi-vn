---
title: Tiền tệ
description: Chủ đề này cung cấp thông tin về cách thêm và loại bỏ các loại tiền tệ trong Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7368dc5d4901e8083f15b0174b7cc58a6b6dbd91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277499"
---
# <a name="currency"></a>Tiền tệ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Loại tiền tệ quyết định giá sản phẩm trong danh mục sản phẩm và chi phí giao dịch, chẳng hạn như các đơn đặt hàng. Nếu khách hàng của bạn nằm rải rác trên nhiều vùng địa lý, hãy thêm loại tiền tệ của họ để quản lý các giao dịch của bạn. Thêm các loại tiền tệ phù hợp nhất cho nhu cầu kinh doanh hiện tại và trong tương lai của bạn.  

> [!NOTE]
> Nếu môi trường của bạn là một môi trường Common Data Service, bạn đang ở trong trung tâm quản trị Power Platform và bạn chọn trang **Tiền tệ** (**Môi trường** > [chọn môi trường] > **Thiết đặt** > **Kinh doanh** > **Tiền tệ**) thì trang này sẽ để trông. Điều này là do việc thiết lập một đơn vị tiền tệ không được hỗ trợ trong các môi trường Common Data Service.

## <a name="add-a-currency"></a>Thêm một loại tiền tệ  
Trước khi bạn bắt đầu quy trình này, hãy xác minh rằng vai trò bảo mật của bạn bao gồm quyền quản trị hệ thống. 

1. Trong trung tâm quản trị Power Platform, hãy chọn một môi trường. 
2. Chọn **Thiết đặt** > **Kinh doanh**.
3. Chọn **Loại tiền**.  
4. Chọn **Mới**.  
5. Điền thông tin được yêu cầu.  


   |          Trường          |                                                                                                                                                                                                                                                                                                                                                                            Mô tả                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Loại Tiền tệ**    | - **Hệ thống** - Chọn tùy chọn này nếu bạn muốn sử dụng các loại tiền tệ có sẵn trong ứng dụng dựa trên mô hình trong Dynamics 365. Để tìm đơn vị tiền tệ, hãy chọn nút **Tra cứu**. Khi bạn chọn một mã tiền tệ, **Tên Tiền tệ** và **Ký hiệu Tiền tệ** sẽ được tự động thêm cho loại tiền tệ đã chọn.<br />- **Tùy chỉnh** - Chọn tùy chọn này nếu bạn muốn thêm loại tiền tệ chưa có sẵn trong các ứng dụng dựa trên mô hình trong Dynamics 365. Trong trường hợp này, bạn phải nhập thủ công các giá trị cho **Mã Tiền tệ**, **Độ chính xác của Tiền tệ**, **Tên Tiền tệ**, **Ký hiệu Tiền tệ** và **Chuyển đổi Tiền tệ**. |
   |    **Mã Tiền tệ**    |                                                                                                                                                                                                                                                                                                                                            Dạng ngắn của tiền tệ. Ví dụ: **USD** cho Đô la Mỹ.                                                                                                                                                                                                                                                                                                                                            |
   | **Độ chính xác của loại tiền**  |                                                                                                                                                                                  Nhập số thập phân mà bạn muốn sử dụng cho tiền tệ.  Bạn có thể thêm một giá trị từ 0 đến 4. **Lưu ý:**  Nếu bạn đã đặt giá trị chính xác trong hộp thoại **Thiết đặt hệ thống**, giá trị đó sẽ xuất hiện ở đây.                                                                                                                                                                                  |
   |    **Tên loại tiền**    |                                                                                                                                                                                                                                         Nếu bạn đã chọn mã tiền tệ từ danh sách các loại tiền tệ có sẵn trong các ứng dụng dựa trên mô hình trong Dynamics 365, thì tên tiền tệ cho mã đã chọn sẽ hiển thị ở đây. Nếu bạn đã chọn **Tùy chỉnh** làm loại tiền tệ, hãy nhập tên tiền tệ.                                                                                                                                                                                                                                          |
   |   **Ký hiệu loại tiền**   |                                                                                                                                                                                                                                                                      Nếu bạn đã chọn mã tiền tệ từ danh sách các loại tiền tệ có sẵn, ký hiệu của tiền tệ đã chọn sẽ được hiển thị ở đây. Nếu bạn đã chọn **Tùy chỉnh** làm loại tiền tệ, hãy nhập ký hiệu cho tiền tệ mới.                                                                                                                                                                                                                                                                       |
   | **Chuyển đổi Tiền tệ** |                                                                                                                                                                                                                                     Nhập giá trị của tiền tệ đã chọn tính theo đô la Mỹ. Đây là số tiền khi loại tiền tệ đã chọn được chuyển đổi sang loại tiền tệ cơ sở. **Quan trọng:**  Hãy đảm bảo rằng bạn cập nhật giá trị này thường xuyên khi cần thiết để tránh mọi tính toán không chính xác trong các giao dịch của mình.                                                                                                                                                                                                                                      |


6. Khi đã hoàn tất, trên thanh lệnh, hãy chọn **Lưu** hoặc **Lưu và đóng**.  

   > [!TIP]
   >  Để chỉnh sửa một loại tiền tệ, hãy chọn loại tiền tệ đó rồi nhập hoặc chọn các giá trị mới.  

## <a name="delete-a-currency"></a>Xóa một loại tiền tệ  

1. Trong trung tâm quản trị Power Platform, hãy chọn một môi trường. 
2. Chọn **Thiết đặt** > **Kinh doanh**.
3. Chọn **Loại tiền**.  
4. Trong danh sách hiển thị các loại tiền tệ, hãy chọn loại tiền tệ cần xóa.  
5. Chọn **Xóa**.  
6. Xác nhận tác vụ xóa này.  

> [!IMPORTANT]
>  Bạn không thể xóa loại tiền tệ mà các hồ sơ khác đang sử dụng; bạn chỉ có thể hủy kích hoạt loại tiền tệ đó. Việc hủy kích hoạt hồ sơ tiền tệ sẽ không xóa thông tin tiền tệ được lưu trữ trong các hồ sơ hiện có, chẳng hạn như cơ hội hoặc đơn hàng. Tuy nhiên, bạn sẽ không thể chọn loại tiền tệ đã hủy kích hoạt cho các giao dịch mới.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]