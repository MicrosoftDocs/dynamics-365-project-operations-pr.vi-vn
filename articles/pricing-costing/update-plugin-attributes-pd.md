---
title: Cập nhật thuộc tính phần bổ trợ với các thông số định giá mới
description: Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ đối với các thông số định giá.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643244"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Cập nhật thuộc tính phần bổ trợ với các thông số định giá mới

Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ đối với các thông số định giá.

> [!NOTE]
> Chủ đề này chỉ áp dụng cho báo giá và hợp đồng có trong Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Điều kiện tiên quyết
Trước khi hoàn tất các bước trong chủ đề này, bạn phải hoàn thành xong các quy trình trong các chủ đề sau đây:

  - [Tạo thực thể và trường tùy chỉnh](create-custom-fields-entities-pricing-dimensions.md) 
  - [Thêm trường tùy chỉnh vào thực thể giao dịch và thiết lập giá ](add-custom-fields-price-setup-transactional-entities.md)
  - [Thiết lập trường tùy chỉnh làm thông số định giá](set-up-custom-fields-pricing-dimensions.md). 
  
Nếu bạn chưa hoàn thành các quy trình đó, hãy hoàn thành rồi trở lại chủ đề này.

## <a name="register-a-plug-in"></a>Đăng ký phần bổ trợ
Khi chi tiết của dòng báo giá được tạo trên trang **Dòng báo giá** cho một dòng báo giá dự án, hệ thống sẽ tạo 2 dòng ước tính. Một dòng là mặt chi phí của ước tính và dòng còn lại là mặt doanh số. Điều này tương tự cho các mô tả hợp đồng.

Khi bạn thay đổi số lượng hoặc trường đối với mặt chi phí, thay đổi đó cũng sẽ áp dụng cho mặt doanh số. Nguyên nhân có thể là do các phần bổ trợ PreOperation trên thực thể Quotelinedetail và contractline detail kết nối các thuộc tính cụ thể mở mặt chi phí với mặt doanh số của giao dịch. Nếu muốn các thay đổi đối với giá trị thông số định giá trên mặt doanh số cũng áp dụng cho mặt chi phí, thì bạn phải đăng ký những phần bổ trợ sau đây sau khi thay đổi thông số định giá.

Sau đây là những phần bổ trợ cần cập nhật và đăng ký lại:

- PreOperationContractLineDetailUpdate - **Cập nhật msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Cập nhật msdyn_quotelinetransaction**

Hoàn tất các bước sau để cập nhật và đăng ký lại các phần bổ trợ.

1. Mở **PluginRegistrationTool** rồi kết nối với môi trường Project Operations Dataverse.
2. Chọn **Tìm kiếm** rồi nhập một vài chữ cái đầu tiên của phần bổ trợ cần cập nhật.
3. Hãy chọn phần bổ trợ tìm thấy rồi bấm vào **Chọn trên biểu mẫu chính**.
4. Chọn bước **Cập nhật msdyn_orderlinetransaction**, bấm chuột phải rồi chọn **Cập nhật**.
5. Trong trang hộp thoại **Cập nhật**, hãy chọn dấu 3 chấm (**...**) trong thuộc tính lọc.
6. Cửa sổ thuộc tính lọc sẽ mở ra, chứa danh sách mọi thuộc tính lọc trong thực thể và các thông số định giá. Đánh dấu vào các ô tương ứng với các thuộc tính thông số định giá.
7. Chọn **OK** để đóng trang rồi chọn **Bước cập nhật**.
8. Lặp lại các bước từ 2-7 cho phần bổ trợ thứ hai **PreOperationQuoteLineDetail**. Đối với phần bổ trợ này, bạn cần cập nhật bước **Update of msdyn_quotelinetransaction**.
9. Đóng **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]