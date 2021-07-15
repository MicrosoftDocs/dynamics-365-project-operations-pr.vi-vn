---
title: Tổng quan về ghi nhận doanh thu
description: Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368052"
---
# <a name="revenue-recognition-overview"></a>Tổng quan về ghi nhận doanh thu

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Trong Dynamics 365 Project Operations, các nguyên tắc ghi nhận doanh thu sẽ khác nhau theo phương thức thanh toán đã chọn cho dự án hoặc theo tỷ lệ dự án. Chủ đề này cung cấp thông tin về ghi nhận doanh thu trong Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Kế toán giao dịch bằng phương pháp thanh toán theo thời gian và vật tư

- Ghi nhận doanh thu và ghi nhận chi phí có mối liên kết với nhau. Chi phí giao dịch và lần bán chưa thanh toán sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).
- Chi phí dự án và hồ sơ doanh thu sẽ quyết định đến việc liệu các giao dịch bán hàng chưa thanh toán có được đăng vào sổ cái chung hay không. Nếu chọn **Tích lũy doanh thu**, hệ thống sẽ dùng các tài khoản **giá trị bán hàng WIP** và **Giá trị bán hàng theo doanh thu tích lũy** trong quá trình đăng. Sau đây là ví dụ về phương pháp này.  

  | Loại giao dịch | Nợ/Có | Số lượng |
  | --- | --- | --- |
  | Giá trị bán hàng WIP | Nợ | 100 |
  | Giá trị bán hàng theo doanh thu tích lũy | Có | 100 |

- Doanh thu sẽ được ghi nhận trong quá trình lập hóa đơn. Hệ thống sẽ dùng tài khoản **Doanh thu có hóa đơn** trong quá trình đăng. Sau đây là ví dụ về phương pháp này.  

  | Loại giao dịch | Nợ/Có | Số lượng |
  | --- | --- | --- |
  | Số dư của khách hàng | Nợ | 120 |
  | Thuế bán hàng phải trả | Có | 20 |
  | Doanh thu có hóa đơn | Có | 100 |

- Nếu chọn tích lũy doanh thu khi lần bán chưa thanh toán được đăng, hệ thống sẽ đảo ngược doanh thu tích lũy khi lập hóa đơn.

  | Loại giao dịch | Nợ/Có | Số lượng |
  | --- | --- | --- |
  | Giá trị bán hàng WIP | Có | 100 |
  | Giá trị bán hàng theo doanh thu tích lũy | Nợ | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Kế toán giao dịch bằng phương pháp thanh toán theo giá cố định

- Ghi nhận doanh thu và ghi nhận chi phí tách biệt với nhau. Chi phí giao dịch sẽ được đăng bằng [Nhật ký tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Giao dịch bán hàng chưa thanh toán sẽ không được tạo.
- Doanh thu có thể được ghi nhận trong quá trình lập hóa đơn nếu chi phí dự án và hồ sơ doanh thu có tùy chọn **Nguyên tắc dùng để tính toán mức hoàn thành dự án** được đặt thành **Không WIP**. Chỉ dùng phương pháp này đối với các dự án ngắn hạn, đơn giản.
- Doanh thu có thể được ghi nhận bằng cách dùng các giá trị ước tính doanh thu theo giá cố định, với phương pháp **Hợp đồng hoàn tất** hoặc **Ghi nhận doanh thu theo phần trăm hoàn thành**.

## <a name="additional-resources"></a>Tài nguyên bổ sung
[Bài viết về đặt cấu hình hoạt động kế toán cho dự án có thể tính phí](../project-accounting/configure-accounting-billable-projects.md)

[Dự án ước tính doanh thu giá cố định](rev-rec-percentage-completion-method.md)

[Quản lý ước tính doanh thu](rev-rec-completed-contract-method.md)

[Phương pháp chi phí hoàn thành](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]