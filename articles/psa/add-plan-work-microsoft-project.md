---
title: Sử dụng Trình bổ sung của Project Service để hoạch định công việc của bạn trong Microsoft Project | MicrosoftDocs
description: Chủ đề này cung cấp thông tin về cách thêm, cấu hình và sử dụng phần bổ trợ Microsoft Project cho Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: 460b5bb7baabcb804b9745f5fddae9bcc3fc7541
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727984"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Sử dụng Trình bổ sung Project Service Automation để lập kế hoạch công việc của bạn trong Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] giúp bạn lập kế hoạch dự án của mình dễ dàng hơn, kể cả việc ước tính. Bạn có thể xác định công việc để có chi phí, nỗ lực và giá bán rõ ràng khi gửi đề xuất cuối cùng.  

 Bây giờ bạn có thể cài đặt [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] và thực hiện việc lập kế hoạch trong môi trường quen thuộc của [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Sử dụng các tính năng lập kế hoạch và quản lý mạnh mẽ của [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi cập nhật kế hoạch dự án của bạn trong Project Service Automation.  

> [!IMPORTANT]
> - Để dùng tính năng quản lý tài liệu SharePoint lưu trữ tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] của bạn cho các dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], quản trị viên [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] của bạn cần phải bật tính năng quản lý tài liệu. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] chỉ tương thích với [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Tải xuống và cài đặt trình bổ sung  
 Chuẩn bị sẵn sàng thông tin đăng nhập [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] của bạn. Bạn sẽ cần thông tin này để kết nối từ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] đến [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Từ Trung tâm tải xuống, hãy tải xuống phần bổ trợ cho phiên bản Project Service được hỗ trợ, [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) hoặc [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Bấm vào liên kết tải xuống.  

3.  Khi hoàn tất tải xuống, nhấp vào **Có** để cài đặt trình bổ sung.  

## <a name="configure-the-add-in"></a>Định cấu hình cho trình bổ sung  

1. Mở [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và bấm vào thẻ **Project Service**.  

2. Bấm vào **Kết nối**.  

3. Nhập thông tin đăng nhập của bạn rồi bấm vào **Đăng nhập**.  

   Bây giờ bạn có thể bắt đầu sử dụng trình bổ sung.  

## <a name="read-from-a-template"></a>Đọc từ một mẫu  
 Đọc từ một mẫu mà bạn tạo trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] và sao chép vào [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] để bắt đầu lên kế hoạch dự án của bạn. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Tạo mẫu dự án (Project Service Automation)](../psa/create-project-template.md)  

1.  Từ thẻ **Project Service**, bấm vào **Đọc** > **Mẫu Dự án Project Service Automation**.  

2.  Chọn một mẫu dự án từ danh sách rồi bấm vào **Mở**.  

    > [!NOTE]
    >  Theo mặc định, các tác vụ được sao chép từ mẫu vào Project được đặt ở chế độ đã lên lịch thủ công.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Gán vai trò [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cho nguồn lực dự án  

1.  Mở một dự án và bấm vào ruy băng **Tác vụ**.  

2.  Bấm vào menu **Biểu đồ Gantt** rồi chọn **Trang tính Nguồn lực**.  

3.  Trên Trang tính Nguồn lực, bấm vào menu thả xuống **Vai trò Nguồn lực trong Project Service** và chọn một vai trò trong Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Cung cấp nguồn lực cho dự án của bạn  

1.  Từ thẻ Project Service, chọn một hàng và bấm vào **Tìm Nguồn lực**.  

2.  Trên màn hình **Đăng ký Nguồn lực**, chọn nguồn lực bạn muốn sử dụng cho dự án.  

3.  Bấm vào **Đăng ký** rồi bấm vào **OK**.  

## <a name="publish-your-project"></a>Phát hành dự án của bạn  
Khi bạn hoàn tất lập kế hoạch dự án, bước tiếp theo là nhập và phát hành dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Dự án sẽ được nhập vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Quy trình tạo nhóm và định giá sẽ được áp dụng. Khi mở dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bạn sẽ thấy nhóm, ước tính dự án và cấu trúc phân tích công việc đã được tạo. Bảng sau hiển thị nơi để tìm thấy các kết quả:

| Dự án | Details |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Biểu đồ Gantt**   | Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Cấu trúc Phân tích Công việc**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Trang tính Nguồn lực** |   Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Mức sử dụng**    |    Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Ước tính dự án**.     |

**Để nhập và phát hành dự án của bạn**  
1. Từ thẻ **Project Service**, bấm vào **Phát hành** > **Dự án Project Service Automation mới**.  

2. Trên hộp thoại **Phát hành dự án mới trong Project Service**, nhập **Tên Dự án** và chọn **Khách hàng**.  

3. Bạn có thể chọn **Liên kết kế hoạch dự án với Project Service Automation** để liên kết tệp kế hoạch Project với Project Service Automation.  

4. Bấm vào **xuất bản**.  

   Việc liên kết tệp Project với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] làm cho tệp Project thành tệp chính và đặt cấu trúc phân tích công việc trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] thành chỉ đọc.  Để thực hiện thay đổi cho kế hoạch dự án, bạn cần làm điều đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và phát hành thay đổi dưới dạng cập nhật vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Chỉnh sửa dự án đã được nhập  
 Để thực hiện thay đổi đối với một kế hoạch dự án đã được nhập vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bạn có hai tùy chọn:  

- Mở tệp chính rồi chỉnh sửa kế hoạch đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Hủy liên kết tệp và chỉnh sửa tệp trực tiếp trong Project Service. Theo mặc định, một dự án được tải lên từ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] sẽ bị khóa và chỉ có thể được chỉnh sửa trong Project. Để chỉnh sửa tệp trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], tệp đó phải được hủy liên kết.  

### <a name="edit-in-pn_microsoft_project"></a>Chỉnh sửa trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Từ menu chính, bấm vào **Project Service** > **Dự án**.  

2. Từ danh sách các dự án, mở dự án bạn đã tạo trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Bấm vào **Mở trong MS Project** từ ruy băng. Thao tác này sẽ mở tệp chính được liên kết trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Hủy liên kết tệp và chỉnh sửa tệp trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Từ menu chính, bấm vào **Project Service** > **Dự án**.  

2. Từ danh sách các dự án, mở dự án bạn đã tạo trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Bấm vào **Hủy liên kết khỏi MS Project** từ ruy băng.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Tải một tệp Project lên SharePoint hoặc Nhóm Office  
 Bạn có thể tải tệp Project lên SharePoint và tìm thấy tệp đó trong Tài liệu Được liên kết cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] của bạn.  Bạn cần phải yêu cầu quản trị viên đặt cấu hình tính năng quản lý tài liệu SharePoint rồi bật tính năng đó cho thực thể Dự án. 

 Bạn cũng có thể tải tệp Project của mình lên [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] nếu đã thiết lập Nhóm Office.

### <a name="upload-a-file-for-sharepoint"></a>Tải tệp lên cho SharePoint  

1. Từ menu chính, bấm vào **Project Service** > **Tải lên**.  

2. Chọn **Lên Tài liệu Dự án trong Project Service Automation**.  

3. Trên hộp thoại **Bật Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, hãy chọn **Có** hoặc **Không**.  

   - Nếu bạn bấm vào **Có**, bạn có thể chọn nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** trong Project Service Automation, chạy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi tải tệp Dự án từ thư viện tài liệu SharePoint.  

   - Nếu bạn bấm vào **Không**, liên kết cho nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sẽ không hoạt động.  

4. Bạn có thể tìm thấy tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong **Tài liệu** cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cụ thể.  

### <a name="upload-a-file-for-office-groups"></a>Tải lên tệp dành cho Nhóm Office  

1. Từ menu chính, bấm vào **Project Service** > **Tải lên**.  

2. Chọn **Lên Tài liệu Dự án trong Project Service Automation**.  

3. Trên hộp thoại **Bật Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, hãy chọn **Có** hoặc **Không**.  

   - Nếu bấm vào **Có**, bạn sẽ có thể chọn nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** trong Project Service Automation, chạy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi tải tệp Dự án từ thư viện tài liệu SharePoint.  

   - Nếu bạn bấm vào **Không**, liên kết cho nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sẽ không hoạt động.  

4. Bạn có thể tìm thấy tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong **Tài liệu** cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cụ thể.  

## <a name="publish--your-project-as-a-template"></a>Phát hành dự án của bạn dưới dạng mẫu  
 Bạn có thể lưu dự án của mình và tái sử dụng bằng cách lưu dự án đó làm mẫu dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Mẫu dự án là các kế hoạch dự án có thể tái sử dụng trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Tạo mẫu dự án (Project Service Automation)](../psa/create-project-template.md)  

1. Từ thẻ **Project Service**, bấm vào **Phát hành** > **Mẫu Dự án Project Service Automation mới**.  

2. Trên hộp thoại **Phát hành dự án mới trong mẫu Project Service**, nhập **Tên mẫu dự án**.  

3. Hoặc, chọn **Liên kết kế hoạch dự án với Project Service Automation** để liên kết tệp Dự án với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Bấm vào **xuất bản**.  

Việc liên kết tệp Project với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] làm cho tệp Project thành tệp chính và đặt cấu trúc phân tích công việc trong mẫu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] thành chỉ đọc.  Để thực hiện thay đổi cho kế hoạch dự án, bạn cần làm điều đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và phát hành thay đổi dưới dạng cập nhật vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Đọc lịch trình đã tải của nguồn lực

Khi đọc một dự án từ Project Service Automation, lịch của nguồn lực sẽ không được đồng bộ với máy khách trên máy tính. Nếu có sự khác biệt về thời lượng, mức nỗ lực hoặc ngày kết thúc nhiệm vụ, nguyên nhân có thể là do nguồn lực và máy khách trên máy tính không có cùng lịch mẫu giờ làm việc áp dụng cho dự án.


## <a name="data-synchronization"></a>Đồng bộ hóa dữ liệu

Bảng sau trình bày cách đồng bộ hóa dữ liệu giữa Project Service Automation và phần bổ trợ trên máy tính Microsoft Project.

| **Thực thể** | **Trường** | **Microsoft Project với Project Service Automation** | **Project Service Automation với Microsoft Project** |
| --- | --- | --- | --- |
| Nhiệm vụ dự án | Ngày đến hạn | ● | - |
| Nhiệm vụ dự án | Nỗ lực Dự kiến | ● | - |
| Nhiệm vụ dự án | ID máy khách MS Project | ● | - |
| Nhiệm vụ dự án | Nhiệm vụ Mẹ | ● | - |
| Nhiệm vụ dự án | Dự án | ● | - |
| Nhiệm vụ dự án | Nhiệm vụ dự án | ● | - |
| Nhiệm vụ dự án | Tên Nhiệm vụ Dự án | ● | - |
| Nhiệm vụ dự án | Đơn vị nguồn lực (Không còn dùng trong v3.0) | ● | - |
| Nhiệm vụ dự án | Khoảng thời gian theo lịch | ● | - |
| Nhiệm vụ dự án | Ngày bắt đầu | ● | - |
| Nhiệm vụ dự án | ID WBS | ● | - |

| **Thực thể** | **Trường** | **Microsoft Project với Project Service Automation** | **Project Service Automation với Microsoft Project** |
| --- | --- | --- | --- |
| Thành viên Nhóm | ID máy khách MS Project | ● | - |
| Thành viên Nhóm | Tên Vị trí | ● | - |
| Thành viên Nhóm | dự án | ● | ● |
| Thành viên Nhóm | Nhóm Dự án | ● | ● |
| Thành viên Nhóm | Đơn vị Nguồn lực | - | ● |
| Thành viên Nhóm | Vai trò | - | ● |
| Thành viên Nhóm | Giờ làm việc | Chưa đồng bộ | Chưa đồng bộ |

| **Thực thể** | **Trường** | **Microsoft Project với Project Service Automation** | **Project Service Automation với Microsoft Project** |
| --- | --- | --- | --- |
| Gán Nguồn lực | Từ Ngày | ● | - |
| Gán Nguồn lực | Giờ | ● | - |
| Gán Nguồn lực | ID máy khách MS Project | ● | - |
| Gán Nguồn lực | Công việc Đã lên kế hoạch | ● | - |
| Gán Nguồn lực | Dự án | ● | - |
| Gán Nguồn lực | Nhóm Dự án | ● | - |
| Gán Nguồn lực | Gán Nguồn lực | ● | - |
| Gán Nguồn lực | Tác vụ | ● | - |
| Gán Nguồn lực | Đến Ngày | ● | - |

| **Thực thể** | **Trường** | **Microsoft Project với Project Service Automation** | **Project Service Automation với Microsoft Project** |
| --- | --- | --- | --- |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | Quan hệ phụ thuộc Nhiệm vụ Dự án | ● | - |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | Loại liên kết | ● | - |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | Nhiệm vụ Người tiền nhiệm | ● | - |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | Dự án | ● | - |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | Nhiệm vụ Người kế nhiệm | ● | - |

### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
