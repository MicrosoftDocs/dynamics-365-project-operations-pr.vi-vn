---
title: Tạo nội dung phân công nguồn lực
description: Bài viết này cung cấp thông tin về cách tạo nội dung phân công nguồn lực chung và có tên.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812020"
---
# <a name="create-resource-assignments"></a>Tạo nội dung phân công nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Phân công nguồn lực là sự liên kết trực tiếp của một thành viên trong nhóm dự án với một nhiệm vụ nút lá. Bài viết này cung cấp thông tin về các cách khác nhau để gán nguồn lực.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tạo thành viên nhóm chung bằng phân công nhiệm vụ


Khi tạo một thành viên nhóm chung thông qua phân công nhiệm vụ, bạn sẽ tạo một chỗ dành sẵn hoặc nguồn lực chung. Tài nguyên chung này mô tả các đặc điểm của tài nguyên được đặt tên mà cuối cùng bạn muốn thực hiện các nhiệm vụ. Sau đó, bạn tạo yêu cầu hoặc bạn gửi yêu cầu bằng cách sử dụng yêu cầu được dùng để tìm kiếm và đăng ký tài nguyên được đặt tên.

1. Trên lưới Lịch trình cho nhiệm vụ, chọn biểu tượng Nguồn lực trong ô **Nguồn lực**.
2. Nhập tên để dùng làm tên của tài nguyên giữ chỗ. Ví dụ: Người quản lý Chương trình.
3. Chọn **Tạo** và trong trường **Tạo nhanh Thành viên Nhóm Dự án**, đặt vai trò cho nguồn lực chung.
4. Khi cần, gán nhiệm vụ cho nguồn lực giữ chỗ này bằng cách chọn nguồn lực trên **Bộ chọn nguồn lực** cho nhiệm vụ. Nguồn lực được liệt kê trong phần **Thành viên nhóm**.
5. Khi bạn chỉ định xong nguồn lực chung, trên tab **Nhóm**, hãy chọn nguồn lực chung rồi chọn **Tạo yêu cầu**  để tạo yêu cầu tài nguyên cho tài nguyên chung.
6. Chọn **Đăng ký** đối với nguồn lực chung và sau đó bạn có thể dùng bảng Lịch trình để tìm và đăng ký nguồn lực thực. Bạn cũng có thể gửi yêu cầu để thực hiện bởi người quản lý nguồn lực.
7. Khi nguồn lực chung được hoàn thành đầy đủ với một nguồn lực được đặt tên, nguồn lực chung sẽ bị xóa khỏi nhóm. (Việc thực hiện một phần yêu cầu nguồn lực sẽ không dẫn đến việc gán nguồn lực.) Việc gán nhiệm vụ cho nguồn lực chung được gán cho nguồn lực có tên đã đáp ứng yêu cầu nguồn lực của nguồn lực chung.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Gán một nguồn lực được đặt tên từ danh sách tất cả các nguồn lực có thể đăng ký được

Bạn có thể dùng hộp tìm kiếm trong **Bộ chọn nguồn lực** để tìm tất cả các nguồn lực hiện hoạt có thể đăng ký và gán nguồn lực cho mọi nhiệm vụ nút lá. Các tài nguyên được chỉ định theo cách này sẽ được thêm vào nhóm mà không có bất kỳ đặt chỗ nào. Điều này tương tự như việc thêm một thành viên trong nhóm và chọn **Không có** làm phương pháp phân bổ. Nguồn lực được hiển thị trong tab **Nhóm**, **Phân công nguồn lực** và **Hợp nhất** như là nguồn lực chỉ có phân công còn đặt chỗ bị thâm hụt. Đăng ký chúng nếu bạn muốn sử dụng tính sẵn có của chúng.

1. Từ lưới nhiệm vụ, bảng hoặc dòng thời gian, hãy điều hướng đến ô **Đã phân công cho**.
2. Trong hộp tìm kiếm, bắt đầu nhập tên. Kết quả tìm kiếm cho tên được hiện thị trong **Bộ chọn nguồn lực** trong phần **Các nguồn lực khác**.
3. Chọn nguồn lực mà bạn muốn gán cho nhiệm vụ hoặc chọn tên của nguồn lực trong **Các nguồn lực nhóm khác**.

## <a name="editing-resource-assignment-contours"></a>Chỉnh sửa đường cong gán nguồn lực

Theo mặc định, khi tài nguyên được gán cho một nhiệm vụ trong lịch trình, nỗ lực của họ được phân phối tuyến tính cho từng tài nguyên, dựa trên số giờ làm việc của tài nguyên đó và chế độ lịch trình của dự án. Người quản lý dự án có thể sử dụng lưới phân công nguồn lực để tinh chỉnh ước tính nỗ lực của từng nguồn lực được giao cho một hoặc nhiều nhiệm vụ trong các thang thời gian khác nhau. Tính năng này giúp người quản lý dự án tạo ra các ước tính chi phí và doanh thu chính xác hơn, được điều khiển bởi các đường viền phân bổ nguồn lực được tạo khi một nguồn lực được gán cho một nhiệm vụ. Ngoài ra, người quản lý dự án có thể dễ dàng phản ánh nhu cầu tài nguyên cần thiết để xây dựng nhu cầu trong yêu cầu tài nguyên.

### <a name="navigation"></a>Điều hướng

Để truy cập lưới chỉnh sửa đường viền, trước tiên, người quản lý dự án chọn thẻ **Nhiệm vụ** trên trang chính của dự án, sau đó chọn thẻ **Nhiệm vụ** tab.

![Tab Bài tập trên tab Nhiệm vụ của trang chính dự án.](media/AssignmentGrid.png)

Lưới hỗ trợ hai phương pháp để nhóm: **nhóm theo tài nguyên** và **nhóm theo nhiệm vụ**. Không giống như trong chế độ xem lưới, các cột không thể định cấu hình. Các cột duy nhất hiển thị là **Được gán cho**, **Tên tác vụ**, **Bắt đầu nhiệm vụ**,** Kết thúc nhiệm vụ **và** Nỗ lực thực hiện nhiệm vụ **.

Khi lưới được hiển thị ban đầu, nó sẽ bắt đầu ở đường viền được gán sớm nhất. Nếu lịch biểu của bạn không chứa bất kỳ nhiệm vụ nào cần nỗ lực, thì lưới sẽ trống và không hiển thị bất kỳ nội dung nào.

![Lưới phân công trống.](media/emptyassignmentgrid.png)

Nếu bạn muốn xem các đường viền và các thang thời gian khác nhau, lưới chỉ định tài nguyên chỉ đọc và lưới đối chiếu tài nguyên cũng có sẵn.

### <a name="resource-calendars"></a>Lịch tài nguyên

Khả năng chỉnh sửa đường viền cho một ngày cụ thể được điều chỉnh bởi số ngày làm việc của tài nguyên, như được phản ánh trong lịch của họ. Nếu một ô bị vô hiệu hóa cho một tài nguyên nhất định, thì tài nguyên đó không có ngày làm việc trong khoảng thời gian đó.

Các đường viền của tài nguyên có thể mở rộng ra ngoài ngày bắt đầu và ngày kết thúc hiện tại của nhiệm vụ được giao. Nếu một đường bao được cập nhật sao cho sau ngày kết thúc mới nhất của nhiệm vụ hoặc ngày bắt đầu sớm nhất của nhiệm vụ, thì ngày kết thúc hoặc ngày bắt đầu của nhiệm vụ sẽ được thay đổi khi thích hợp. Tuy nhiên, nếu một đường bao được cập nhật sớm hơn ngày bắt đầu của một nhiệm vụ được liên kết với nhiệm vụ tiền nhiệm, thì bản cập nhật sẽ không thành công vì nhiệm vụ sẽ kích hoạt nhiệm vụ bắt đầu trước khi nhiệm vụ tiền nhiệm của nó hoàn thành và hành vi đó hiện không có được hỗ trợ.

### <a name="co-authoring"></a>đồng tác giả

Các thay đổi đối với lưới phân công nguồn lực sẽ tự động được phản ánh trong bất kỳ dạng xem được liên kết nào, bao gồm dạng xem biểu đồ, dòng thời gian, bảng và lưới. Nếu nhiều người dùng đang xem xét dự án cùng một lúc, mọi thay đổi mà một người dùng thực hiện sẽ được phản ánh trong lưới. Ngược lại, bất kỳ thay đổi nào được thực hiện trong lưới phân công tài nguyên sẽ được hiển thị cho tất cả những người dùng khác đang xem dự án trong cùng một phiên.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
