---
title: Đơn vị tổ chức
description: Bài viết này mô tả khái niệm đơn vị tổ chức và giải thích cách tạo và duy trì các đơn vị tổ chức trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921650"
---
# <a name="organizational-units-overview"></a>Tổng quan về đơn vị tổ chức

Trong Microsoft Dynamics 365 Project Operations, một *đơn vị tổ chức* là một nhóm hoặc bộ phận riêng biệt trong một công ty dịch vụ chuyên nghiệp sử dụng các nguồn lực có thể lập hóa đơn có mức chi phí.

Đối với các công ty dịch vụ chuyên nghiệp sử dụng các nguồn lực kỹ thuật trong các lĩnh vực thực hành hoặc ngành nghề kinh doanh khác nhau, chi phí để thực hiện một vai trò có thể khác nhau, tùy thuộc vào lĩnh vực hành nghề hoặc ngành nghề kinh doanh mà vai trò đó được thực hiện. Trong trường hợp này, khái niệm đơn vị tổ chức giúp cung cấp một cách để nhóm một tập hợp các vai trò có thể lập hóa đơn trong một bộ phận của công ty có cơ cấu chi phí riêng biệt cho các vai trò đó.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Khái niệm về các đơn vị tổ chức trong Hoạt động Dự án

Trong Hoạt động Dự án, một đơn vị tổ chức có một đơn vị tiền tệ cụ thể và các bảng giá chi phí cụ thể.

Tiền tệ của một đơn vị tổ chức là tiền tệ chính được dùng để theo dõi chi phí.

Có thể đính kèm một hoặc nhiều danh sách giá vốn với mỗi đơn vị tổ chức. Hoạt động Dự án đặt ra những hạn chế sau đối với bảng giá có thể được đính kèm với một đơn vị tổ chức:

- Các bảng giá phải bằng đơn vị tổ chức.
- Các bảng giá phải là bảng giá chi phí.

Ngoài ra, thực thể Nguồn lực bao gồm một thuộc tính cho đơn vị tổ chức. Có thể gán mỗi tài nguyên cho một đơn vị tổ chức.

### <a name="roles-of-organizational-units"></a>Các vai trò của đơn vị tổ chức

Đơn vị tổ chức đóng hai vai trò trong Hoạt động của Dự án:

- **Đơn vị ký hợp đồng** – Đơn vị tổ chức đại diện cho nhóm hoặc bộ phận của công ty có trách nhiệm chính là giành được hợp đồng bán hàng và quản lý việc cung cấp công việc cũng như dịch vụ cho khách hàng. Đơn vị ký hợp đồng được xác định trong trường **Đơn vị ký hợp đồng** ở phần tiêu đề của trang **Cơ hội**, **Báo giá**, **Hợp đồng dự án** và **Dự án**.
- **Đơn vị cấp nguồn lực** – Đơn vị tổ chức chứa một nguồn lực hoặc được chỉ định một nguồn lực. Đơn vị tổ chức này có thể cung cấp nguồn lực cho một số vai trò trên báo cáo công việc (SOW) và các dự án mà đơn vị ký hợp đồng sở hữu.

![Đơn vị ký hợp đồng và đơn vị cấp nguồn lực.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Câu hỏi thường gặp về đơn vị tổ chức

Sau đây là một số câu hỏi thường gặp về đơn vị tổ chức.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Thực thể Đơn vị tổ chức trong Hoạt động dự án có liên quan như thế nào với thực thể Tổ chức đã tồn tại trong Dynamics 365?

Thực thể Tổ chức trong Dynamics 365 đại diện cho tên của một phiên bản Dynamics 365 toàn cầu. Tên này thường là tên của doanh nghiệp toàn cầu.

Thực thể Đơn vị tổ chức đại diện cho một nhóm hoặc bộ phận trong doanh nghiệp toàn cầu. Nhóm hoặc bộ phận này có một tập hợp các vai trò và danh sách giá vốn cho các vai trò đó, đồng thời các vai trò và bảng giá đó khác với vai trò và bảng giá của các nhóm hay bộ phận khác trong doanh nghiệp.

Khi Hoạt động dự án được cài đặt, một đơn vị tổ chức mặc định được tạo dựa trên tổ chức. Tất cả các tài nguyên hiện có được gán cho đơn vị tổ chức mặc định. Nếu bất kỳ người dùng hoặc tài nguyên Active Directory mới nào được nhập vào Dynamics 365, quá trình nhập người dùng sẽ chỉ định chúng cho đơn vị tổ chức mặc định trong Hoạt động dự án.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Thực thể Đơn vị tổ chức khác với thực thể Đơn vị kinh doanh như thế nào?

Trong Dynamics 365, thực thể Đơn vị kinh doanh là một cấu trúc bảo mật. Tổ chức người dùng có đơn vị kinh doanh xác định các thực thể và bản ghi thực thể mà người dùng có quyền truy cập. Nó cũng xác định các quyền (tạo, đọc, ghi, xóa, nối, gắn vào, chỉ định hoặc chia sẻ) mà người dùng có đối với các hồ sơ thực thể đó.

Thực thể Đơn vị tổ chức đại diện cho một nhóm hoặc bộ phận trong công ty có giá chi phí riêng đối với nhân viên được chỉ định. Tổ chức nguồn lực với một đơn vị tổ chức xác định chi phí của một nguồn lực cho một dự án tham gia.

Khi bạn triển khai Dynamics 365, hãy tối ưu hóa ủy quyền bảo mật cho hệ thống phân cấp của đơn vị kinh doanh và gán người dùng cho đơn vị kinh doanh. Chỉ định tất cả người dùng thường phải truy cập cùng một bộ hồ sơ cho cùng một đơn vị kinh doanh. Đơn vị tổ chức không có hiệu lực về ủy quyền hoặc truy cập bảo mật.

**Ví dụ cho thấy một sự khác biệt tiềm ẩn trong việc mô hình hóa các đơn vị tổ chức và đơn vị kinh doanh**

Contoso, Ltd. sử dụng rất nhiều công nghệ của Microsoft. Đức và Cúc đều là các nhà phát triển C\# nhưng Cúc ở Hoa Kỳ còn Đức lại ở Ấn Độ. Hầu hết các hoạt động tham gia dự án đều yêu cầu tài nguyên từ cả Contoso Ấn Độ và Contoso Hoa Kỳ, đồng thời Prakash và Tricia yêu cầu cùng một mức độ truy cập bảo mật vào các dự án trong lĩnh vực thực tiễn này. Tuy nhiên, chi phí của các nhà phát triển từ Contoso Ấn độ có sự chênh lệch đáng kể so với chi phí của các nhà phát triển từ Contoso Hoa Kỳ.

Đây là một cách tối ưu để thiết kế cho tình huống này bằng cách sử dụng Dynamics 365 và Hoạt động dự án.

1. Tạo thực hành công nghệ của Microsoft dưới dạng một đơn vị kinh doanh rồi liên kết Đức và Cúc với nó. Bằng cách này, bạn giúp đảm bảo rằng cả hai nhân viên đều có cùng mức độ truy cập bảo mật vào bất kỳ dự án nào trong lĩnh vực thực hành đó. Cả hai đều có thể kiểm tra tiến độ và báo cáo thời gian, chi phí, việc sử dụng vật liệu và cập nhật nhiệm vụ.
2. Tạo hai đơn vị tổ chức để giúp đảm bảo rằng chi phí cho dự án được phản ánh chính xác.
3. Liên kết Tricia với Contoso US và Prakash với Contoso India.
4. Gán danh sách giá chi phí phù hợp cho cả hai đơn vị tổ chức. Bằng cách này, bạn giúp đảm bảo rằng chi phí được ghi lại trên dự án cho Prakash và Tricia phản ánh chính xác sự khác biệt về chi phí giữa Contoso Hoa Kỳ và Contoso Ấn Độ.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Có phải là đơn vị tổ chức liên quan đến lãnh thổ bán hàng trong Dynamics 365 không?

Không có hiệp hội hoặc mối quan hệ giữa lãnh thổ bán hàng và đơn vị tổ chức. Một lãnh thổ bán hàng thường là một khu vực địa lý diễn ra hoạt động bán hàng. Một bảng giá bán hàng có thể được liên kết với mỗi lãnh thổ bán hàng.

Đơn vị tổ chức là một nhóm hoặc bộ phận nội bộ trong công ty theo dõi chi phí cho một tập hợp các vai trò bán cho các bộ phận khác hoặc cho khách hàng bên ngoài.

**Ví dụ cho thấy một sự khác biệt tiềm ẩn trong việc lập mô hình các đơn vị tổ chức và lãnh thổ bán hàng**

Contoso, Ltd. có hai trung tâm phát triển: Contoso Hoa Kỳ và Contoso Ấn Độ. Chi phí tài nguyên có sự khác biệt rất lớn giữa hai trung tâm phát triển này. Contoso bán các dịch vụ công nghệ thông tin (CNTT) của mình tại nhiều thị trường quốc tế, chẳng hạn như Châu Mỹ Latinh, Bắc Mỹ, Châu Á - Thái Bình Dương, Tây Âu và Trung Đông. Mức phí cho các vai trò dự án tương tự có thể khác nhau khá lớn trên các thị trường này. Contoso Hoa Kỳ và Contoso Ấn Độ phải được thiết lập là đơn vị tổ chức và mỗi đơn vị tổ chức phải có danh sách giá chi phí riêng. Cần thiết lập Châu Á-Thái Bình Dương, Mỹ Latinh, Bắc Mỹ, Tây Âu và Trung Đông là lãnh thổ bán hàng, và mỗi lãnh thổ bán hàng cần có danh sách giá bán hàng riêng.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Tại sao có hạn chế về liên kết các danh sách giá với các đơn vị tổ chức?

Giá bán hàng thường là duy nhất cho các khu vực địa lý hoặc thị trường nơi các dịch vụ được bán. Các bộ phận nội bộ của một công ty thường không có giá bán hàng riêng cho cùng loại dịch vụ. Tuy nhiên, các bộ phận nội bộ có chi phí bán hàng (COGS) khác nhau, tùy thuộc vào kỹ năng của người mà họ tuyển dụng và các điều kiện lao động của khu vực nơi họ hoạt động. Bởi vì các đơn vị tổ chức được lập mô hình như là bộ phận trong một công ty, nên họ chỉ có thể có danh sách giá chi phí.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Tại sao chúng ta không thể liên kết bảng giá bán hàng với các đơn vị tổ chức?

Trong Hoạt động Dự án, bảng giá bán hàng có thể được liên kết với khách hàng và lãnh thổ bán hàng. Các thực thể giao dịch như Cơ hội, Báo giá, Hợp đồng Dự án và Dự án sử dụng bảng giá bán hàng được đính kèm với tài khoản khách hàng hoặc lãnh thổ bán hàng để xác định tỷ lệ hóa đơn và doanh thu tiềm năng cho việc tham gia dự án.

Danh sách giá chi phí được liên kết với đơn vị tổ chức. Các thực thể giao dịch như Cơ hội, Báo giá, Hợp đồng Dự án và Dự án sử dụng bảng giá chi phí được đính kèm với đơn vị ký hợp đồng để xác định chi phí cho một cam kết dự án.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Các đơn vị tổ chức có được phân cấp trong Hoạt động Dự án không?

Không. Trong bản phát hành hiện tại của Hoạt động dự án, các đơn vị tổ chức không có thứ bậc. Do đó, bạn không thể thực hiện các tác vụ sau:

- Định cấu hình một mẫu để nhập giá chi phí mặc định theo phân cấp.
- Báo cáo doanh thu hoặc chi phí được tổng hợp ở các cấp khác nhau của hệ thống phân cấp đơn vị tổ chức.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Chúng tôi là một công ty đa quốc gia lớn có hệ thống phân cấp phức tạp, đa cấp gồm các trung tâm chi phí, bộ phận và văn phòng thanh toán. Làm thế nào chúng ta có thể sử dụng tốt nhất khái niệm đơn vị tổ chức trong phiên bản Hoạt động dự án hiện tại?

Khi bạn có một hệ thống phân cấp phức tạp gồm các trung tâm chi phí, bộ phận, văn phòng thanh toán, v.v., hãy thiết lập các nút lá của hệ thống phân cấp đó thành các đơn vị tổ chức riêng biệt.

Ví dụ sau đây cho thấy một hệ thống phân cấp điển hình.

**Contoso Ấn Độ**

- Phương pháp SAP

    - Tư vấn kỹ thuật
    - Tư vấn chức năng

- Phương pháp công nghệ của Microsoft

    - Tư vấn kỹ thuật
    - Tư vấn chức năng

**Contoso US**

- Phương pháp SAP

    - Tư vấn kỹ thuật
    - Tư vấn chức năng

- Phương pháp công nghệ của Microsoft

    - Tư vấn kỹ thuật
    - Tư vấn chức năng

Nếu cấu trúc phân cấp của bạn giống với ví dụ này, bạn phải thiết lập nó dưới dạng danh sách phẳng, như được hiển thị ở đây:

- Contoso Ấn Độ - Phương pháp SAP - Tư vấn kỹ thuật
- Contoso Ấn Độ - Phương pháp SAP - Tư vấn chức năng
- Contoso Ấn Độ - Phương pháp Công nghệ Microsoft - Tư vấn chức năng
- Contoso Ấn Độ - Phương pháp Công nghệ Microsoft - Tư vấn chức năng
- Contoso Hoa Kỳ - Phương pháp SAP - Tư vấn kỹ thuật
- Contoso Hoa Kỳ - Phương pháp SAP - Tư vấn chức năng
- Contoso Hoa Kỳ - Phương pháp Công nghệ Microsoft - Tư vấn kỹ thuật
- Contoso Hoa Kỳ - Phương pháp Công nghệ Microsoft - Tư vấn chức năng

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Chúng tôi là một công ty dịch vụ chuyên nghiệp nhỏ, hoạt động chỉ như một bộ phận. Làm thế nào chúng ta có thể sử dụng tốt nhất khái niệm đơn vị tổ chức trong phiên bản Hoạt động dự án hiện tại?

Nếu công ty của bạn hoạt động như một đơn vị có một bảng giá chi phí, thì bạn không cần phải thiết lập bất kỳ đơn vị tổ chức nào. Việc cài đặt Hoạt động Dự án tạo ra một đơn vị tổ chức mặc định có cùng tên với tổ chức. Theo mặc định, tất cả người dùng được gán cho đơn vị tổ chức này. Bất cứ khi nào hệ thống yêu cầu chọn một đơn vị tổ chức, đơn vị tổ chức này được chọn theo mặc định.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Khi một dự án được tạo từ một báo giá hoặc mô tả hợp đồng dự án, đơn vị ký kết mặc định đến từ báo giá hoặc hợp đồng dự án. Đơn vị hợp đồng mặc định là gì nếu một dự án được tạo trước các thực thể bán hàng như Báo giá hoặc Hợp đồng dự án?

Khi một dự án được tạo, đơn vị hợp đồng mặc định của dự án sẽ dựa trên người dùng tạo ra nó. Người dùng đó cũng là người quản lý dự án mặc định. Nếu dự án được ánh xạ tới một thực thể bán hàng, chẳng hạn như báo giá hoặc hợp đồng dự án, thì đơn vị ký hợp đồng của dự án sẽ dựa trên thực thể bán hàng thay thế. Trong trường hợp này, ước tính dự án có thể được tính toán lại, vì bảng giá chi phí được sử dụng để tính toán chi phí ước tính sẽ thay đổi nếu đơn vị ký hợp đồng thay đổi. Bảng giá bán hàng được sử dụng để tính toán các ước tính bán hàng sẽ được thay đổi để chúng đồng bộ với bảng giá dự án của báo giá.

Các **Đơn vị ký kết** và **Tiền tệ** các trường của dự án bị khóa để chỉnh sửa, vì chúng phải đồng bộ với các giá trị của thực thể bán hàng (báo giá hoặc hợp đồng dự án) mà dự án được ánh xạ tới.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Tạo và duy trì các đơn vị tổ chức trong Hoạt động Dự án

Để tạo một đơn vị tổ chức trong Hoạt động Dự án, hãy làm theo các bước sau.

1. Đi đến **Cài đặt \> Đơn vị tổ chức**.
2. Chọn **Mới**.
3. Bên trong **Chung** khu vực, trong **Tên**, hãy nhập tên cho đơn vị tổ chức. Sau đó đặt các trường khác theo yêu cầu.
4. Lựa chọn **Tiết kiệm** để tạo bản ghi để bạn có thể tiếp tục chỉnh sửa nó.
5. Dưới **Bảng giá chi phí**, chọn dấu cộng (**+**) để thêm bảng giá. Bạn chỉ có thể thêm danh sách giá có **Phí tổn** bối cảnh ở đây.
6. Bên trong **Tên** trường, chọn **Tìm kiếm** và chọn một danh sách giá mà bạn muốn cung cấp cho đơn vị tổ chức. Tiếp tục bổ sung bảng giá theo yêu cầu.
7. Khi bạn đã hoàn tất việc thêm danh sách giá, hãy chọn **Tiết kiệm** ở góc dưới bên phải của trang.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
