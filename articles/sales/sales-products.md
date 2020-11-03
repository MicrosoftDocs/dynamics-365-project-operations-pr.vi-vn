---
title: Sản phẩm
description: Chủ đề này cung cấp thông tin về danh mục sản phẩm mà bạn có thể sử dụng để cung cấp thông tin cho khách hàng về các sản phẩm và giá mà tổ chức của bạn cung cấp.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 7116659c646b323667e3c92cb3f6de99184f5ae6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087205"
---
# <a name="products"></a>Sản phẩm

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sản phẩm là xương sống của doanh nghiệp của bạn. Danh mục sản phẩm trong Dynamics 365 Sales Professional là tập hợp các sản phẩm và thông tin giá cả. Giúp đại diện bán hàng của bạn dễ dàng tăng doanh thu hơn bằng cách nhanh chóng tạo ra một danh mục sản phẩm.

## <a name="add-a-product"></a>Thêm sản phẩm

1.  Đảm bảo rằng bạn có vai trò Chuyên gia Quản lý Bán hàng hoặc Quản trị viên Hệ thống để có thể thêm sản phẩm trong Dynamics 365 Sales Professional.
2.  Trong sơ đồ trang web, trong **Thiết lập** , hãy chọn **Sản phẩm**.
3.  Chọn **Thêm sản phẩm** và điền thông tin sau đây:

    -  **Tên**
    -  **ID sản phẩm**
    -  **Cấp độ cha** : Chọn dòng sản phẩm cấp độ cha cho sản phẩm. Nếu bạn đang tạo một sản phẩm cấp độ con trong một dòng sản phẩm, thì tên của dòng sản phẩm cấp độ cha sẽ xác định ở đây. Không thể thay đổi tên sau đã lưu bản ghi.
    -  **Hợp lệ Từ**/**Hợp lệ Tới** : Xác định khoảng thời gian một sản phẩm hợp lệ bằng cách chọn ngày **Hợp lệ Từ** và **Hợp lệ Tới**.
    -  **Nhóm Đơn vị** : Chọn nhóm đơn vị. Một nhóm đơn vị là một tập hợp các đơn vị khác nhau một sản phẩm được bán trong và định cách các mục riêng lẻ được nhóm lại thành số lượng lớn hơn. Ví dụ: nếu đang thêm hạt giống làm sản phẩm, bạn có thể đã tạo ra một nhóm đơn vị đo được gọi là "Hạt giống" và xác định đơn vị chính là "gói".
    -  **Đơn vị Mặc định** : Chọn đơn vị thông dụng nhất khi bán sản phẩm. Đơn vị có số lượng hoặc số đo mà bạn bán sản phẩm của mình. Ví dụ: nếu đang thêm hạt giống làm sản phẩm, bạn có thể bán hạt giống theo gói, hộp hoặc khay. Mỗi trong số này sẽ trở thành một đơn vị của sản phẩm. Nếu hạt giống được chủ yếu là bán trong gói dữ liệu, chọn mà như các đơn vị.
    -  **Bảng giá Mặc định** : Nếu đây là một sản phẩm mới, trường này ở trạng thái chỉ đọc. Trước khi có thể chọn bảng giá mặc định, bạn phải hoàn thành mọi trường bắt buộc rồi lưu bản ghi. Mặc dù danh sách giá mặc định là không cần thiết, nhưng sau khi lưu bản ghi sản phẩm, bạn nên đặt một bảng giá mặc định cho từng sản phẩm. Sau đó, nếu bản ghi khách hàng không bao gồm bảng giá, Sales có thể sử dụng bảng giá mặc định để tạo ra báo giá, đơn hàng và hóa đơn.
    -  **Số thập phân được hỗ trợ** : Nhập một số nguyên từ 0 đến 5. Nếu không thể chia sản phẩm thành các số lượng phân đoạn, hãy nhập 0. Độ chính xác của trường **Số lượng** trong bản ghi báo giá, đơn hàng hoặc thông tin hóa đơn được xác thực với giá trị trong trường này nếu sản phẩm không có bảng giá được liên kết.
    -  **Chủ đề** : Liên kết sản phẩm này với một chủ đề. Bạn có thể sử dụng chủ đề để phân loại sản phẩm của mình và lọc báo cáo.

4.  Chọn **Lưu**.
5.  Trên tab **Chi tiết bổ sung** , trong phần **Hạng mục trong bảng giá** , hãy chọn **Lệnh khác** rồi chọn **Thêm hạng mục trong bảng giá mới**.
7.  Trên tab **Chi tiết bổ sung** , trong phần **Mối quan hệ sản phẩm** , hãy chọn biểu tượng **Lệnh khác** rồi chọn **Thêm mối quan hệ sản phẩm mới.**
8.  Trong biểu mẫu **Mối quan hệ sản phẩm mới** , hãy nhập các chi tiết sau và trên thanh lệnh, chọn **Lưu và đóng** :

    -   **Sản phẩm liên quan** : Chọn một sản phẩm mà bạn muốn thêm làm sản phẩm liên quan vào bản ghi sản phẩm hiện có mà đang thực hiện.
    -   **Loại mối quan hệ bán hàng** : Chọn xem bạn có muốn thêm các sản phẩm như một sản phẩm bán thêm, bán chéo, phụ kiện, hoặc sản phẩm thay thế.
    -   **Chiều** : Chọn xem mối quan hệ giữa các sản phẩm sẽ là hướng một chiều hay hai chiều. Khi bạn chọn một chiều, các sản phẩm mà bạn chọn trong **Sản phẩm liên quan** sẽ được hiển thị ở dạng đề xuất cho các sản phẩm hiện có, nhưng không áp dụng ngược lại.

9.  Trên biểu mẫu Sản phẩm, hãy chọn **Lưu**.

## <a name="import-products"></a>Nhập sản phẩm

Bạn có thể sử dụng mẫu nhập để đưa hàng loạt dữ liệu sản phẩm vào Dynamics 365 Sales.

## <a name="revise-a-product"></a>Sửa đổi một sản phẩm

Giữ sản phẩm tồn kho luôn cập nhật một cách nhanh chóng khi sửa đổi thuộc tính của các sản phẩm theo yêu cầu, và xuất bản thông tin để các đại lý bán hàng của bạn có thể xem các thay đổi mới nhất đối với hàng tồn kho.

1.  Đảm bảo rằng bạn có một trong những vai trò bảo mật hoặc quyền tương đương sau: Quản trị viên Hệ thống, Người tùy chỉnh Hệ thống, Giám đốc Bán hàng, Phó giám đốc bán hàng, Phó giám đốc tiếp thị hoặc Giám đốc Kinh doanh-CEO.
2.  Trong sơ đồ trang web, hãy chọn **Sản phẩm**.
3.  Mở một sản phẩm hiện hoạt mà bạn muốn thay đổi và trên thanh lệnh, chọn **Sửa đổi**.
4.  Trong hộp thoại **Xác nhận Sửa đổi** , chọn **Xác nhận** Điều này sẽ thay đổi trạng thái sản phẩm thành **Đang được sửa đổi**.
5.  Sau khi bạn thực hiện thay đổi, trên thanh lệnh, hãy chọn **Phát hành**.

    > [!TIP]
    > Để hoàn nguyên thay đổi và tiếp tục với phiên bản hiện hoạt của sản phẩm, hãy chọn **Hoàn nguyên**. Này thay đổi trạng thái của sản phẩm trở lại **hoạt động**.

## <a name="clone-a-product"></a>Sao y một sản phẩm 

Khi bạn đang tạo ra một sản phẩm mới, hãy tiết kiệm thời gian bằng cách sao chép gói hiện có. Điều này tạo ra một bản sao của hồ sơ ban đầu với tất cả các chi tiết ngoại trừ tên và ID.

1.  Đảm bảo rằng bạn có một trong những vai trò bảo mật hoặc quyền tương đương sau: Quản trị viên Hệ thống, Người tùy chỉnh Hệ thống, Giám đốc Bán hàng, Phó giám đốc bán hàng, Phó giám đốc tiếp thị hoặc Giám đốc Kinh doanh-CEO.
2.  Trong sơ đồ trang web, hãy chọn **Sản phẩm**.
3.  Chọn bản ghi sản phẩm mà bạn muốn sao chép và trên thanh lệnh, chọn **Sao chép**. Một hộp thoại xác nhận sẽ xuất hiện.
4.  Chọn **Xác nhận**.

Một bản ghi sản phẩm mới mở ra với các chi tiết tương tự như một bản gốc ngoại trừ tên và ID.

## <a name="retire-a-product"></a>Hủy bỏ sản phẩm 

Nếu tổ chức của bạn không bán một sản phẩm nữa, hủy bỏ nó để không phải là sản phẩm là không có sẵn cho các đại lý bán hàng của bạn.

1.  Đảm bảo rằng bạn có vai trò bảo mật Quản trị viên hệ thống hoặc Người quản lý Sales Professional hoặc các quyền tương đương.
2.  Trong sơ đồ trang web, hãy chọn **Sản phẩm**.
3.  Mở một sản phẩm hiện hoạt mà bạn muốn ngừng cung cấp và trên thanh lệnh, chọn **Ngừng cung cấp**.
4.  Trong hộp thoại **Xác nhận Hủy bỏ** , chọn **Xác nhận**.


## <a name="delete-a-product"></a>Xóa sản phẩm

Để ngừng bán một sản phẩm, hãy xóa nó.

> [!IMPORTANT]
> Bạn không thể khôi phục bản ghi đã xóa.

1.  Đảm bảo rằng bạn có vai trò bảo mật Quản trị viên hệ thống hoặc Người quản lý Sales Professional hoặc các quyền tương đương.
2.  Trong sơ đồ trang web, hãy chọn **Sản phẩm**.
3.  Chọn bản ghi sản phẩm mà bạn muốn xóa và trên thanh lệnh, hãy chọn **Xóa**.
4.  Trong hộp thoại **Xác nhận xóa** , chọn **Tiếp tục**.
 
 ## <a name="quantity-factors-for-products"></a>Yếu tố số lượng cho sản phẩm

Các yếu tố số lượng hỗ trợ việc bán các sản phẩm dựa trên đăng ký. Đối với các sản phẩm dựa trên đăng ký, số lượng trên báo giá hoặc mô tả hợp đồng dự án được thể hiện ở dạng số tháng người dùng.

Thông thường, giá phần mềm đăng ký được lưu trữ trong danh mục ở dạng giá cho mỗi người dùng mỗi tháng. Tuy nhiên, bạn có thể sử dụng mô tả thời gian khác thay thế. Trong quá trình bán hàng, giá trên mô tả báo giá thường là giá trên mỗi người dùng, mỗi tháng được đại lý bán hàng CNTT thương lượng và giảm giá. Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau. Số lượng được dùng để tính toán lượng mô tả báo giá là sản phẩm của số lượng người dùng và số lượng tháng đăng ký.

Yếu tố số lượng dựa vào các thuộc tính sản phẩm. Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, bạn có thể gắn cờ một tập con của các thuộc tính đó hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.

Hệ thống xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng. Khi sản phẩm mà các yếu tố số lượng được đặt cấu hình được thêm vào mô tả báo giá, thì trường **Số lượng** trên mô tả báo giá trở thành trường chỉ đọc. Sau khi bạn nhập giá trị cho các thuộc tính sản phẩm là các yếu tố số lượng, số lượng của mô tả báo giá được tính toán.

Ví dụ, nếu có các thuộc tính sau đây: 

- **Số người dùng** : Số lượng người dùng 
- **Số tháng** : Số lượng tháng đăng ký
- **SKU sản phẩm** 

Các thuộc tính **Sô người dùng** và **Số tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm. 
