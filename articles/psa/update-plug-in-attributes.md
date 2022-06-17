---
title: Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới
description: Bài viết này cung cấp thông tin về cách cập nhật thuộc tính trình cắm cho các thứ nguyên đặt giá.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913232"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Nếu bạn không sử dụng các tính năng Báo giá và Hợp đồng Tự động hóa Dịch vụ Dự án (PSA), bạn có thể bỏ qua bài viết này.

Bài viết này giả định rằng bạn đã hoàn thành các thủ tục trong bài viết, [Tạo các trường và thực thể tùy chỉnh](create-custom-fields-entities.md),[Thêm các trường tùy chỉnh vào các thực thể thiết lập giá và giao dịch](field-references.md), và [Thiết lập các trường tùy chỉnh làm thứ nguyên đặt giá](set-up-pricing-dimensions.md). Nếu bạn chưa hoàn thành các thủ tục đó, hãy quay lại và hoàn thành chúng rồi quay lại bài viết này.

Khi chi tiết mô tả báo giá được tạo trên trang **Mô tả báo giá** cho chi tiết báo giá dự án, hệ thống sẽ tạo 2 mô tả ước tính trong nền -- một mô tả cho chi phí ước tính và một mô tả cho doanh số. Điều này tương tự cho các mô tả hợp đồng.

Khi bạn thay đổi số lượng hoặc trường đối với chi phí, thay đổi đó sẽ được chuyển sang bên doanh số. Điều này có thể do phần bổ trợ sau phải được đăng ký lại sau khi thay đổi thông số định giá.

- PreOperationContractLineDetailUpdate - Cập nhật **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Cập nhật **msdyn_quotelinetransaction**.

Các bước sau đây giải thích cho bạn quy trình đăng ký phần bổ trợ.

1. Mở **PluginRegistrationTool** và kết nối với phiên bản trực tuyến của bạn.
2. Bấm vào **Tìm kiếm** và tìm kiếm phần bổ trợ để được cập nhật.

 ![Ảnh chụp màn hình về cây tìm kiếm.](media/PRT-1.png)

3. Sau khi tìm thấy phần bổ trợ, hãy chọn phần bổ trợ đó rồi bấm vào **Chọn trên biểu mẫu chính**.

4. Chọn bước của phần bổ trợ sẽ được cập nhật, bấm chuột phải rồi chọn **Cập nhật**.

 ![Ảnh chụp màn hình về phần bổ trợ sẽ được cập nhật.](media/PRT-2.png)
 
5. Trong cửa sổ cập nhật, hãy bấm vào dấu ba chấm (**...**) trong các thuộc tính lọc.

 ![Ảnh chụp màn hình về Cập nhật thông tin cấu hình bước hiện có.](media/PRT-3.png)
 
6. Chọn hộp kiểm thuộc tính định giá.

 ![Ảnh chụp màn hình minh họa thao tác lựa chọn hộp kiểm cho thuộc tính định giá.](media/PRT-4.png)

7. Bấm **OK** để đóng trang rồi chọn **Cập nhật bước**.

 ![Ảnh chụp màn hình hiển thị nút “Cập nhật bước”.](media/PRT-5.png)
 
8. Lặp lại quá trình này cho phần bổ trợ thứ hai **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.

9. Đóng công cụ đăng ký phần bổ trợ.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
