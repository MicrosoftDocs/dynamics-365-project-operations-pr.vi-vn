---
title: Trang chủ nâng cấp
description: Chủ đề này cho biết nơi tìm thông tin quan trọng về các tính năng mới và đã thay đổi trong Dynamics 365 Project Service Automation và quá trình nâng cấp lên phiên bản mới nhất.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087189"
---
# <a name="upgrade-home-page"></a>Trang chủ nâng cấp

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Nâng cấp từ PSA phiên bản 2.x hoặc 1.x lên phiên bản 3.x

### <a name="new-instances"></a>Phiên bản mới

Kể từ ngày 17/5/2019, khi Project Service Automation được chọn trong khi cung cấp phiên bản mới, phiên bản 3.x is sẽ được cài đặt theo mặc định.

### <a name="existing-instances"></a>Các phiên bản hiện có

Trước đây, khách hàng có PSA phiên bản 2.x và cần nâng cấp lên phiên bản 3.x, là phiên bản PSA dựa trên Giao diện khách hàng hợp nhất (UCI), phải liên hệ với Bộ phận Hỗ trợ của Microsoft và cung cấp thông tin chi tiết về phiên bản của họ để đội ngũ hỗ trợ có thể cho phép nâng cấp lên phiên bản 3.x. Kể từ ngày 1 tháng 3 năm 2020, khách hàng có phiên bản PSA 2.x và cần nâng cấp lên phiên bản 3.x, sẽ có thể nâng cấp phiên bản của họ ngay từ Cổng thông tin quản trị mà không phải liên hệ với Bộ phận Hỗ trợ của Microsoft.  

> [!NOTE]
> PSA phiên bản 3.x bao gồm những thay đổi đáng kể. Phiên bản này được xây dựng trên khung Giao diện hợp nhất để giúp cung cấp trải nghiệm người dùng được cải thiện. Ứng dụng cải tiến cung cấp giao diện người dùng (UI) nhất quán, thống nhất và tuân theo các nguyên tắc thiết kế phản hồi để tối ưu hóa trải nghiệm xem trên mọi kích thước màn hình hoặc thiết bị. Ứng dụng còn có các thay đổi khác. Một số khía cạnh đã thay đổi, bao gồm giá, đăng ký và chỉ định nguồn lực, thời gian, chi phí và quy trình phê duyệt.

Trước khi bắt đầu quá trình nâng cấp, bạn nên hoàn thành các nhiệm vụ sau:

- Xác minh xem cả Dynamics 365 Field Service và Project Service Automation có được cài đặt trên phiên bản đã xác định hay chưa. Nếu cả hai giải pháp đã được cài đặt, bạn nên dự định nâng cấp cả hai trước khi tiếp tục sử dụng phiên bản này như bình thường.
- Cẩn thận xem xét những chủ đề sau. Nhận biết và hiểu về thay đổi giữa các phiên bản sẽ giúp bạn trong quá trình nâng cấp. Những chủ đề này cung cấp thông tin về những thay đổi chính trong PSA, cùng với những thông tin cần cân nhắc và đề xuất về kế hoạch nâng cấp lên phiên bản 3.x.

    - [Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3](whats-new-changed-v3.md)
    - [Những điểm cần cân nhắc khi nâng cấp - Project Service Automation phiên bản 2.x hoặc 1.x lên phiên bản 3](upgrade-v3.md)

- Nâng cấp phiên bản hộp cát để đánh giá các thay đổi trong quá trình thực hiện trước khi bạn nâng cấp phiên bản sản xuất.

Sau khi bạn đã xem lại các chủ đề được đề cập trước đây và đã sẵn sàng nâng cấp lên PSA phiên bản 3.x hoặc phiên bản dựa trên UCI, hãy gửi yêu cầu cho đội ngũ hỗ trợ của Microsoft để cung cấp bản nâng cấp từ Trung tâm quản trị. Trong yêu cầu của bạn, hãy cung cấp thông tin chi tiết về phiên bản.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Các phiên bản PSA khác (PSA phiên bản 2.x) là phiên bản mới tạo

Kể từ ngày 17/5/2019, tất cả các phiên bản mới sẽ có UCI là ứng dụng mặc định. Để phù hợp với thay đổi này, PSA phiên bản 3.x và Field Service phiên bản 8.x sẽ được cung cấp theo mặc định, vì những phiên bản này được thiết kế để hoạt động với ứng dụng UCI.

Bắt đầu từ ngày 1 tháng 3 năm 2020, khách hàng của Dynamics PSA sẽ không thể tạo môi trường mới với các phiên bản PSA cũ nữa, ví dụ: PSA phiên bản 2.x trở xuống. Mọi môi trường mới sẽ chỉ nhận phiên bản PSA 3.x.

> [!NOTE]
> Để có trải nghiệm tốt nhất khi sử dụng các phiên bản cũ của ứng dụng Field Service và PSA, hãy chuyển đến trang **Cài đặt hệ thống** và đối với trường **Chỉ sử dụng Giao diện hợp nhất mới (đề xuất)** , hãy chọn **Không** vì các phiên bản này không được thiết kế để được tải chính xác trong UCI. Sau khi đã tắt UCI, bạn có thể mở và chạy các phiên bản Field Service và PSA này bằng cách sử dụng ứng dụng web cũ. 