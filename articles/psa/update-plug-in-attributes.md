---
title: Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới
description: Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ cho các thông số định giá.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087191"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới

> [!NOTE]
> Nếu đang không dùng tính năng Báo giá và Hợp đồng của Project Service Automation (PSA), bạn có thể bỏ qua chủ đề này.

Chủ đề này giả định rằng bạn đã hoàn tất quy trình trong các chủ đề [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities.md), [Thêm các trường tùy chỉnh vào thực thể thiết lập và giao dịch giá](field-references.md) và [Thiết lập trường tùy chỉnh làm thông số định giá](set-up-pricing-dimensions.md). Nếu bạn chưa hoàn thành các quy trình đó, hãy quay lại và hoàn thành chúng rồi trở lại chủ đề này.

Khi chi tiết mô tả báo giá được tạo trên trang **Mô tả báo giá** cho chi tiết báo giá dự án, hệ thống sẽ tạo 2 mô tả ước tính trong nền -- một mô tả cho chi phí ước tính và một mô tả cho doanh số. Điều này tương tự cho các mô tả hợp đồng.

Khi bạn thay đổi số lượng hoặc trường đối với chi phí, thay đổi đó sẽ được chuyển sang bên doanh số. Điều này có thể do phần bổ trợ sau phải được đăng ký lại sau khi thay đổi thông số định giá.

- PreOperationContractLineDetailUpdate - Cập nhật **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Cập nhật **msdyn_quotelinetransaction**.

Các bước sau đây giải thích cho bạn quy trình đăng ký phần bổ trợ.

1. Mở **PluginRegistrationTool** và kết nối với phiên bản trực tuyến của bạn.
2. Bấm vào **Tìm kiếm** và tìm kiếm phần bổ trợ để được cập nhật.

 ![Ảnh chụp màn hình về cây tìm kiếm](media/PRT-1.png)

3. Sau khi tìm thấy phần bổ trợ, hãy chọn phần bổ trợ đó rồi bấm vào **Chọn trên biểu mẫu chính**.

4. Chọn bước của phần bổ trợ sẽ được cập nhật, bấm chuột phải rồi chọn **Cập nhật**.

 ![Ảnh chụp màn hình về phần bổ trợ sẽ được cập nhật](media/PRT-2.png)
 
5. Trong cửa sổ cập nhật, hãy bấm vào dấu ba chấm ( **...** ) trong các thuộc tính lọc.

 ![Ảnh chụp màn hình về Cập nhật thông tin cấu hình bước hiện có](media/PRT-3.png)
 
6. Chọn hộp kiểm thuộc tính định giá.

 ![Ảnh chụp màn hình minh họa thao tác lựa chọn hộp kiểm cho thuộc tính định giá](media/PRT-4.png)

7. Bấm **OK** để đóng trang rồi chọn **Cập nhật bước**.

 ![Ảnh chụp màn hình hiển thị nút “Cập nhật bước”](media/PRT-5.png)
 
8. Lặp lại quá trình này cho phần bổ trợ thứ hai **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.

9. Đóng công cụ đăng ký phần bổ trợ.

