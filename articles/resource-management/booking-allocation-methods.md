---
title: Phương thức phân bổ đặt trước
description: Chủ đề này cung cấp thông tin về cách thức hoạt động của phương thức phân bổ đặt trước trong Hoạt động Dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897702"
---
# <a name="booking-allocation-methods"></a>Phương thức phân bổ đặt trước

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Cho dù bạn thêm một thành viên nhóm trực tiếp vào một dự án trên tab **Nhóm** hay đăng ký một nguồn lực cho một dự án hoặc yêu cầu từ bảng Lịch trình, bạn có thể sử dụng một vài phương pháp phân bổ đăng ký khác nhau. Chủ đề này giải thích cách mỗi phương pháp hoạt động và phương pháp nào có thể dẫn tới quá tải nguồn lực.

## <a name="booking-allocation-methods"></a>Phương thức phân bổ đặt trước

Có sáu phương thức phân bổ đặt trước mà bạn có thể sử dụng:

- [Năng lực đầy đủ](#full)
- [Năng lực còn lại](#remaining)
- [Năng lực theo dạng phần trăm](#percentage)
- [Giờ phân phối đồng đều](#evenly)
- [Giờ phân phối lượng công việc nặng lúc ban đầu](#front)
- [Không có](#none)

### <a name="full-capacity"></a><a name="full"></a>Năng lực đầy đủ 
Phương pháp Năng lực đầy đủ sẽ đăng ký năng lực đầy đủ của nguồn lực theo các ngày bắt đầu và kết thúc đã được chỉ định. Ví dụ: nếu một nguồn lực có lịch được sắp xếp làm việc 8 giờ một ngày, 5 ngày một tuần; lịch này có ngày bắt đầu và kết thúc kéo dài trong 5 ngày làm việc sẽ được đăng ký dưới dạng nguồn lực 40 giờ. Việc đăng ký được hoàn thành mà không phải chú ý tới năng lực còn lại của nguồn lực. Nếu một nguồn lực đã được đăng ký trên dự án khác trùng với khung thời gian đó, thì 40 giờ sẽ được đăng ký dưới dạng số giờ bổ sung, như vậy có khả năng dẫn tới việc quá tải đăng ký.

### <a name="remaining-capacity"></a><a name="remaining"></a>Năng lực còn lại
Phương pháp Năng lực còn lại chỉ sẵn có khi bạn đăng ký trực tiếp cho dự án sử dụng bảng Lịch trình. Phương pháp này đăng ký theo năng lực sẵn có của nguồn lực trong quãng ngày được chỉ định. Ví dụ: nếu một nguồn lực có năng lực là 40 giờ một tuần và đã được đăng ký 10 giờ, thì việc đăng ký cho tuần đó sẽ cho kết quả đăng ký được cho 30 giờ của năng lực còn lại cho tuần đó.

### <a name="percentage-capacity"></a><a name="percentage"></a>Năng lực theo dạng phần trăm
Phương pháp Năng lực theo phần trăm sẽ đăng ký nguồn lực theo tỉ lệ phần trăm năng lực cho những ngày bắt đầu và kết thúc được chỉ định. Ví dụ: nếu một nguồn lực có lịch được sắp xếp làm việc 8 giờ một ngày, 5 ngày một tuần; lịch này có ngày bắt đầu và kết thúc kéo dài trong 5 ngày làm việc ở mức 50% năng lực sẽ được đăng ký dưới dạng nguồn lực 20 giờ. Đăng ký cá nhân theo ngày được chia đều cho các khung thời gian. Ví dụ: 4 giờ một ngày trong ví dụ này. Việc đăng ký được hoàn thành mà không phải chú ý tới năng lực còn lại của nguồn lực. Nếu một nguồn lực đã được đăng ký trên dự án khác trùng với khung thời gian đó, thì 20 giờ sẽ được đăng ký dưới dạng số giờ bổ sung, như vậy có khả năng dẫn tới việc quá tải đăng ký.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Giờ phân phối đồng đều
Phương pháp Phân phối theo giờ đồng đều sẽ đăng ký nguồn lực cho số giờ được chỉ định, phân phối thời gian mỗi ngày đều nhau cho các ngày đã được chỉ định kể từ khi bắt đầu cho tới khi kết thúc. Ví dụ: nếu bạn đăng ký một nguồn lực cho 20 giờ trong khoảng thời gian 5 ngày thì phương pháp này sẽ chia đều 20 giờ cho mỗi ngày 4 giờ. Việc đăng ký được hoàn thành mà không phải chú ý tới năng lực còn lại của nguồn lực. Nếu một nguồn lực đã được đăng ký trên dự án khác trùng với khung thời gian đó, thì 20 giờ sẽ được đăng ký dưới dạng số giờ bổ sung, như vậy có khả năng dẫn tới việc quá tải đăng ký.

### <a name="front-load-hours"></a><a name="front"></a>Giờ phân phối lượng công việc nặng lúc ban đầu
Phương pháp Số giờ tải trước sẽ đăng ký nguồn lực cho số giờ được chỉ định, tải trước số giờ mỗi ngày trong các ngày được chỉ định từ khi bắt đầu cho tới khi kết thúc. Việc phân phối không đồng đều sẽ tốn năng lực sẵn có của nguồn lực theo cách “đăng ký trước, sử dụng trước”. Ví dụ: nếu lịch làm việc của nguồn lực là 8 giờ một ngày, 5 ngày một tuần và hiện họ không có đăng ký nào, việc đăng ký nguồn lực cho 20 giờ trong khoảng thời gian 5 ngày làm việc sẽ cho kết quả về kiểu đăng ký hàng ngày như sau: 

|                           |    Ngày 1    |    Ngày 2    |    Ngày 3    |    Ngày 4    |    Ngày 5    |    Tổng số    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Đăng ký   hiện tại**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Đăng ký   mới**          |    8        |    8        |    4        |    0        |    0        |    20       |

Phương pháp phân phối không đồng đều sẽ xem xét tới các đăng ký đã có và năng lực sẵn có. Ví dụ: nếu nguồn lực đã được đăng ký cho 20 giờ cho tuần làm việc, việc đăng ký mới sẽ tiêu tốn năng lực còn lại như sau:

|                     | Ngày 1 | Ngày 2 | Ngày 3 | Ngày 4 | Ngày 5 | Tổng số |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Đăng ký   hiện tại** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Đăng ký   mới**       | 0     | 0     | 4     | 8     | 8     | 20    |

Vì năng lực sẵn có được xem xét, bạn có thể gặp thông báo lỗi nếu nguồn lực không còn năng lực còn lại mà việc đăng ký có thể sử dụng. Bạn không thể đăng ký quá tải với phương pháp này.

### <a name="none"></a><a name="none"></a>Không
Phương pháp Không có chỉ sẵn dùng khi bạn đăng ký từ tab **Nhóm** trong dự án. Phương pháp này thêm nguồn lực là một thành viên nhóm vào dự án nhưng không tạo bất kỳ đăng ký gì sẽ sử dụng năng lực của nguồn lực. Phương pháp này được dùng khi thành viên nhóm của người quản lý dự án mặc định được thêm vào khi tạo dự án. Người dùng là người quản lý dự án chính là người tạo dự án được thêm vào dự án theo mặc định nên bản ghi thực thể dự án đó sẽ có chủ sở hữu và có một người phê chuẩn cho dự án. Bởi vì người dùng không có bất kỳ đăng ký nào, nếu bạn không muốn đăng ký nguồn lực, thì bạn có thể vừa xóa rồi thêm lại đăng ký bằng cách áp dụng phương pháp phân bổ khác hoặc thêm nguồn lực cho nhiệm vụ rồi sử dụng **Đăng ký Mở rộng** trên tab **Hợp nhất** để tạo đặt lịch cho phân công.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Các phương pháp phân bổ sẽ dẫn tới quá tải đăng ký
Tổng kết lại, các phương pháp phân bổ sau sẽ dẫn tới quá tải đăng ký nếu nguồn lực đã được cam kết cho các dự án khác (hoặc cho các lệnh sản xuất hoặc thực thể được lên lịch khác):

- Năng lực đầy đủ
- Năng lực tỉ lệ phần trăm
- Giờ phân phối đồng đều

Khi sử dụng một trong ba phương pháp phân bổ này, bạn sẽ không được thông báo khi nguồn lực bị quá tải đăng ký. Để khắc phục việc quá tải đăng ký, bạn sẽ cần sử dụng bảng Lịch trình.
