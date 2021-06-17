---
title: Đồng bộ hóa năng lực của nguồn lực
description: Chủ đề này cung cấp thông tin về cách đồng bộ hóa năng lực của nguồn lực trên lịch và dự án.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997537"
---
# <a name="synchronize-resource-capacity"></a>Đồng bộ hóa năng lực của nguồn lực

[!include [banner](../includes/banner.md)]

Các quy trình đồng bộ hóa nguồn lực giúp đảm bảo rằng thông tin cho lịch lịch và lịch cơ sở sẽ dần đi vào quá trình lập lịch trình nguồn lực dự án. Nếu lịch bị thay đổi, các quy trình sẽ thực hiện cập nhật bắt buộc đối với việc lập lịch trình các nguồn lực dự án. Các quy trình cũng giúp cải thiện hiệu suất, vì thông tin nguồn lực của lịch được đồng bộ hóa trước. Do đó, việc cập nhật thông tin lập lịch nguồn lực diễn ra nhanh hơn. Chúng tôi khuyên bạn nên lập lịch các quy trình theo loạt thay vì từng lần một. Nếu không, ai đó có thể quên những ngày được bao gồm khi thông tin được đồng bộ hóa lần gần nhất. Nếu các ngày bao gồm không được sử dụng, khoảng trống có thể xảy ra trong quá trình đồng bộ hóa ngày.

![Đồng bộ hóa lịch](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Đồng bồ hóa tổng hợp năng lực của nguồn lực

Quá trình đồng bộ hóa được thiết kế để đồng bộ hóa tất cả thông tin lịch nguồn lực. Thông tin này bao gồm thông tin lịch cơ sở về bất kỳ thay đổi nào đối với bảng năng lực lịch nguồn lực của dự án. Nếu các nguồn lực mới được thêm vào dự án, quá trình đồng bộ hóa sẽ đảm bảo rằng thông tin lịch cập nhật có sẵn. Việc đồng bộ hóa này có thể được thực hiện bất cứ lúc nào.

Chúng tôi khuyên bạn nên sử dụng loạt. Các tùy chọn có sẵn trong quá trình đồng bộ hóa các mục dự trữ năng lực.

1. Chọn **Quản lý dự án và kế toán** &gt; **Định kỳ** &gt; **Đồng bộ hóa năng lực** &gt; **Đồng bộ hóa tổng hợp năng lực của nguồn lực**.
2. Thiết lập các tùy chọn trong bảng sau.

    | Tùy chọn      | Mô tả |
    |-------------|-------------|
    | Mã thời kỳ | Tùy ý chọn mã khoảng ngày của sổ cái chung để đặt ngày bắt đầu và ngày kết thúc cho quá trình đồng bộ hóa cho tổng hợp năng lực của nguồn lực. |
    | Ngày bắt đầu  | Nhập ngày bắt đầu cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực. |
    | Ngày kết thúc    | Nhập ngày kết thúc cho quá trình đồng bộ hóa để tổng hợp năng lực của nguồn lực. |

[![Quá trình đồng bộ hóa](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]