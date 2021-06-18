---
title: Đơn vị tổ chức
description: Chủ đề này cung cấp thông tin về các đơn vị tổ chức trong Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009642"
---
# <a name="organizational-units"></a>Đơn vị tổ chức 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, một đơn vị tổ chức là một nhóm hoặc bộ phận riêng biệt trong một công ty dịch vụ chuyên nghiệp chuyên thuê tuyển nguồn lực có thể tính phí theo tỷ lệ phí tổn.

Đối với các công ty dịch vụ chuyên nghiệp thuê tuyển nguồn lực kỹ thuật trong các lĩnh vực thực hành hoặc ngành nghề kinh doanh khác nhau, chi phí để tuyển một vai trò trong một khu vực thực hành hoặc ngành nghề kinh doanh có thể khác với chi phí để tuyển một vai trò trong một khu vực thực hành hoặc ngành nghề kinh doanh khác. Khái niệm đơn vị tổ chức có ích trong trường hợp này nhờ cung cấp một cách để nhóm một bộ vai trò có thể tính phí trong một bộ phận của công ty có cấu trúc phí riêng cho những vai trò này.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Các thuộc tính và mối liên kết chính của các đơn vị tổ chức

Trong PSA, một đơn vị tổ chức trong PSA có một loại tiền tệ cụ thể và danh sách giá vốn cụ thể.

Tiền tệ của một đơn vị tổ chức là tiền tệ chính được dùng để theo dõi chi phí.

Có thể đính kèm một hoặc nhiều danh sách giá vốn với mỗi đơn vị tổ chức. PSA đặt các giới hạn sau đây đối với các bảng giá có thể đính kèm với một đơn vị tổ chức:

- Bảng giá phải bằng đơn vị tiền tệ của đơn vị tổ chức
- Bảng giá phải là danh sách giá vốn

Ngoài ra, còn có một thuộc tính cho đơn vị tổ chức trên thực thể Tài nguyên. Có thể gán mỗi tài nguyên cho một đơn vị tổ chức.

## <a name="roles-of-organizational-units"></a>Các vai trò của đơn vị tổ chức

Đơn vị tổ chức đóng hai vai trò trong PSA:

- **Đơn vị ký hợp đồng** – Đơn vị tổ chức đại diện cho nhóm hoặc bộ phận của công ty có trách nhiệm chính là giành được hợp đồng bán hàng và quản lý việc cung cấp công việc cũng như dịch vụ cho khách hàng. Đơn vị ký hợp đồng được xác định trong trường **Đơn vị ký hợp đồng** ở phần tiêu đề của trang **Cơ hội**, **Báo giá**, **Hợp đồng dự án** và **Dự án**.
- **Đơn vị cấp nguồn lực** – Đơn vị tổ chức chứa một nguồn lực hoặc được chỉ định một nguồn lực. Đơn vị tổ chức này có thể cung cấp nguồn lực cho một số vai trò trên báo cáo công việc (SOW) và các dự án mà đơn vị ký hợp đồng sở hữu.

> ![Đơn vị ký hợp đồng và đơn vị cấp nguồn lực](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Câu hỏi thường gặp về đơn vị tổ chức

Sau đây là một số câu hỏi thường gặp về đơn vị tổ chức.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Thực thể Đơn vị tổ chức trong PSA được liên kết như thế nào với thực thể Tổ chức đã tồn tại trong Dynamics 365?

Thực thể Tổ chức trong Microsoft Dynamics 365 biểu thị tên của phiên bản Dynamics 365 toàn cầu. Tên này thường là tên của doanh nghiệp toàn cầu.

Thực thể Đơn vị tổ chức đại diện cho một nhóm hoặc bộ phận trong doanh nghiệp toàn cầu. Nhóm hoặc bộ phận này có một tập hợp các vai trò và danh sách giá vốn cho các vai trò đó, đồng thời các vai trò và bảng giá đó khác với vai trò và bảng giá của các nhóm hay bộ phận khác trong doanh nghiệp.

Khi cài đặt PSA, một đơn vị tổ chức mặc định sẽ được tạo dựa trên tổ chức. Tất cả các tài nguyên hiện có được gán cho đơn vị tổ chức mặc định. Nếu bất kỳ người dùng hoặc tài nguyên Active Directory mới nào được nhập vào Dynamics 365, thì quá trình nhập người dùng sẽ chỉ định họ vào đơn vị tổ chức mặc định trong PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Thực thể đơn vị tổ chức khác với thực thể đơn vị kinh doanh như thế nào?

Trong Dynamics 365, thực thể Đơn vị kinh doanh là một cấu trúc bảo mật. Tổ chức người dùng có đơn vị kinh doanh xác định các thực thể và bản ghi thực thể mà người dùng có quyền truy cập. Nó cũng xác định các quyền (tạo, đọc, ghi, xóa, nối, gắn vào, chỉ định hoặc chia sẻ) mà người dùng có đối với các hồ sơ thực thể đó.

Thực thể Đơn vị tổ chức đại diện cho một nhóm hoặc bộ phận trong công ty có giá chi phí riêng đối với nhân viên được chỉ định. Tổ chức nguồn lực với một đơn vị tổ chức xác định chi phí của một nguồn lực cho một dự án tham gia.

Khi bạn triển khai Dynamics 365, hãy tối ưu hóa ủy quyền bảo mật cho hệ thống phân cấp của đơn vị kinh doanh và gán người dùng cho đơn vị kinh doanh. Chỉ định tất cả người dùng thường phải truy cập cùng một bộ hồ sơ cho cùng một đơn vị kinh doanh. Đơn vị tổ chức không có hiệu lực về ủy quyền hoặc truy cập bảo mật.

#### <a name="example-of-organizational-units-and-business-units"></a>Ví dụ về đơn vị tổ chức và đơn vị kinh doanh

Contoso, Ltd. sử dụng rất nhiều công nghệ của Microsoft. Đức và Cúc đều là các nhà phát triển C\# nhưng Cúc ở Hoa Kỳ còn Đức lại ở Ấn Độ. Hầu hết các hoạt động tương tác trong dự án đòi hỏi có nguồn lực từ Contoso Ấn Độ và Contoso Hoa Kỳ, còn Prakash và Tricia phải có cùng một mức độ truy nhập bảo mật đối với các dự án trong khu vực thực hành này. Tuy nhiên, chi phí cho nhà phát triển ở Contoso Ấn Độ có sự chênh lệch đáng kể với chi phí cho nhà phát triển ở Contoso Hoa Kỳ.

Đây là một cách tối ưu để thiết kế cho trường hợp này bằng cách sử dụng Dynamics 365 và PSA.

1. Tạo thực hành công nghệ của Microsoft dưới dạng một đơn vị kinh doanh rồi liên kết Đức và Cúc với nó. Bằng cách này, bạn giúp đảm bảo rằng cả hai nhân viên đều có cùng mức độ truy cập bảo mật vào bất kỳ dự án nào trong khu vực thực hành đó. Cả hai đều sẽ có thể kiểm tra tiến độ và báo cáo thời gian, chi phí, và Cập Nhật nhiệm vụ. 
2. Tạo hai đơn vị tổ chức để đảm bảo rằng chi phí cho dự án được phản ánh chính xác. 
3. Liên kết Tricia với Contoso Hoa Kỳ và liên kết Prakash với Contoso Ấn Độ.
4. Gán danh sách giá chi phí phù hợp cho cả hai đơn vị tổ chức. Theo cách này, bạn sẽ bảo đảm rằng các chi phí được ghi lại trên dự án cho Prakash và Tricia phản ánh chính xác sự khác biệt về chi phí giữa Contoso Hoa Kỳ và Contoso Ấn Độ.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Có phải là đơn vị tổ chức liên quan đến lãnh thổ bán hàng trong Dynamics 365 không?

Không có hiệp hội hoặc mối quan hệ giữa lãnh thổ bán hàng và đơn vị tổ chức. Một lãnh thổ bán hàng thường là một khu vực địa lý diễn ra hoạt động bán hàng. Một bảng giá bán hàng có thể được liên kết với mỗi lãnh thổ bán hàng.

Đơn vị tổ chức là một nhóm hoặc bộ phận nội bộ trong công ty theo dõi chi phí cho một tập hợp các vai trò bán cho các bộ phận khác hoặc cho khách hàng bên ngoài.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Ví dụ về đơn vị tổ chức và lãnh thổ bán hàng

Contoso, Ltd. có hai trung tâm phát triển: Contoso Hoa Kỳ và Contoso Ấn Độ. Chi phí tài nguyên giữa hai trung tâm phát triển chênh lệch rất lớn.

Contoso bán các dịch vụ CNTT tại nhiều thị trường quốc tế, như: Mỹ Latinh, Bắc Mỹ, châu Á – Thái Bình Dương, Tây Âu và Trung Đông. Mức phí cho các vai trò dự án tương tự có thể khác nhau khá lớn trên các thị trường này.

Contoso Hoa Kỳ và Contoso Ấn Độ phải được thiết lập là đơn vị tổ chức và mỗi đơn vị tổ chức phải có bảng giá vốn riêng. Cần thiết lập Châu Á-Thái Bình Dương, Mỹ Latinh, Bắc Mỹ, Tây Âu và Trung Đông là lãnh thổ bán hàng, và mỗi lãnh thổ bán hàng cần có danh sách giá bán hàng riêng.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Tại sao có hạn chế về liên kết các danh sách giá với các đơn vị tổ chức? 

Giá bán hàng thường là duy nhất cho các khu vực địa lý hoặc thị trường nơi các dịch vụ được bán. Các bộ phận nội bộ của một công ty thường không có giá bán hàng riêng cho cùng loại dịch vụ. Tuy nhiên, các bộ phận nội bộ có chi phí bán hàng (COGS) khác nhau, tùy thuộc vào kỹ năng của người mà họ tuyển dụng và các điều kiện lao động của khu vực nơi họ hoạt động. Bởi vì các đơn vị tổ chức được lập mô hình như là bộ phận trong một công ty, nên họ chỉ có thể có danh sách giá chi phí.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Tại sao chúng tôi không thể liên kết danh sách giá bán với đơn vị tổ chức?

Trong PSA, danh sách giá bán hàng có thể được liên kết với khách hàng và lãnh thổ bán hàng. Các thực thể giao dịch như cơ hội, báo giá, hợp đồng dự án và dự án sử dụng bảng giá bán được đính kèm vào tài khoản khách hàng hoặc lãnh thổ bán hàng để xác định mức phí và doanh thu tiềm năng khi tham gia dự án.

Danh sách giá chi phí được liên kết với đơn vị tổ chức. Các thực thể giao dịch như cơ hội, báo giá, hợp đồng dự án và dự án sử dụng danh sách giá chi phí được đính kèm vào đơn vị ký kết để xác định chi phí tham gia dự án.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Có đơn vị tổ chức phân cấp trong PSA không?

Không. Trong bản phát hành hiện tại của PSA, đơn vị tổ chức không phân cấp. Điều này có nghĩa là bạn không thể:

- Cấu hình mẫu mặc định giá chi phí trong một hệ thống cấp bậc. 
- Báo cáo doanh thu hoặc chi phí làm tròn ở các cấp khác nhau của hệ thống đơn vị tổ chức.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Chúng tôi là một công ty đa quốc gia lớn với một hệ thống phân cấp đa dạng, phức tạp gồm các trung tâm chi phí, bộ phận và văn phòng thanh toán. Làm thế nào chúng tôi có thể tận dụng khái niệm đơn vị tổ chức trong phiên bản ứng dụng Project Service này?

Khi bạn có một hệ thống phân cấp phức tạp gồm các trung tâm chi phí, bộ phận, văn phòng thanh toán, v.v., hãy thiết lập các nút lá của hệ thống phân cấp như đơn vị tổ chức riêng biệt.
Ví dụ sau cho thấy một phân cấp điển hình:

**Contoso Ấn Độ**

  - Phương pháp SAP 

    - Tư vấn kỹ thuật 
    - Tư vấn chức năng 
    
  - Phương pháp công nghệ của Microsoft 

    - Tư vấn kỹ thuật
    - Tư vấn chức năng 
    
**Contoso Hoa Kỳ**

 - Phương pháp SAP 

    - Tư vấn kỹ thuật 
    - Tư vấn chức năng 
    
 - Phương pháp công nghệ của Microsoft 

    - Tư vấn kỹ thuật 
    - Tư vấn chức năng 
 
Nếu hệ thống phân cấp của bạn tương tự, bạn phải thiết lập nó như là một danh sách phẳng, như được hiển thị ở đây:
- Contoso Ấn Độ – Phương pháp SAP – Tư vấn kỹ thuật 
- Contoso Ấn Độ – Phương pháp SAP – Tư vấn chức năng       
- Contoso Ấn Độ – Phương pháp công nghệ Microsoft – Tư vấn chức năng 
- Contoso Ấn Độ – Phương pháp công nghệ Microsoft – Tư vấn chức năng 
- Contoso Hoa Kỳ – Phương pháp SAP – Tư vấn kỹ thuật  
- Contoso Hoa Kỳ – Phương pháp SAP – Tư vấn chức năng  
- Contoso Hoa Kỳ – Phương pháp công nghệ Microsoft – Tư vấn kỹ thuật 
- Contoso Hoa Kỳ – Phương pháp công nghệ Microsoft – Tư vấn chức năng

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Chúng tôi là một công ty dịch vụ chuyên nghiệp nhỏ, hoạt động chỉ như một bộ phận. Làm thế nào chúng tôi có thể tận dụng khái niệm đơn vị tổ chức trong phiên bản hiện tại của PSA?

Nếu công ty của bạn hoạt động như một đơn vị có một bảng giá chi phí, thì bạn không cần phải thiết lập bất kỳ đơn vị tổ chức nào. Trong quá trình cài đặt PSA, Dynamics 365 sẽ tạo một đơn vị tổ chức mặc định có cùng tên với tổ chức. Theo mặc định, tất cả người dùng được gán cho đơn vị tổ chức này. Bất cứ khi nào hệ thống yêu cầu chọn một đơn vị tổ chức, đơn vị tổ chức này được chọn theo mặc định.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Khi một dự án được tạo từ một báo giá hoặc mô tả hợp đồng dự án, đơn vị ký kết mặc định đến từ báo giá hoặc hợp đồng dự án. Nếu một dự án được tạo trước các thực thể bán hàng như báo giá hoặc hợp đồng dự án, đơn vị ký kết mặc định là gì?

Khi một dự án được tạo, đơn vị hợp đồng mặc định của dự án sẽ dựa trên người dùng tạo ra nó. Người dùng đó cũng là người quản lý dự án mặc định. Nếu dự án được ánh xạ tới một thực thể bán hàng như một báo giá hoặc hợp đồng dự án, thì đơn vị ký kết dự án dựa trên các tổ chức bán hàng. Trong trường hợp này, ước tính dự án có thể được tính toán lại, vì bảng giá chi phí được sử dụng để tính toán chi phí ước tính sẽ thay đổi nếu đơn vị ký hợp đồng thay đổi. Bảng giá bán được sử dụng để tính toán ước tính bán hàng sẽ thay đổi để chúng đồng bộ với danh sách giá dự án trên báo giá.

Các trường **Đơn vị hợp đồng** và **Tiền tệ** trên dự án không chỉnh sửa được vì chúng phải đồng bộ với các giá trị trên thực thể bán hàng (báo giá hoặc hợp đồng dự án) mà dự án được ánh xạ.


[!INCLUDE[footer-include](../includes/footer-banner.md)]