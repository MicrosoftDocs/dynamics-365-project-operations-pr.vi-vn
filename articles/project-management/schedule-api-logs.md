---
title: Nhật ký lên lịch dự án
description: Bài viết này cung cấp thông tin và mẫu sẽ giúp bạn sử dụng nhật ký Lập lịch dự án để theo dõi các sự cố liên quan tới Dịch vụ lập lịch dự án và API Lập lịch dự án.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923721"
---
# <a name="project-scheduling-logs"></a>Nhật ký lên lịch dự án

_**Áp dụng cho:** Project Operations cho các kịch bản dựa trên nguồn lực/không trữ kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_, _Project for the web_

Microsoft Dynamics 365 Project Operations sử dụng [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) làm công cụ lập lịch chính. Thay vì sử dụng giao diện lập trình ứng dụng (API) web Microsoft Dataverse tiêu chuẩn, Project Operations sử dụng API Lập lịch dự án mới để tạo, cập nhật và xóa nhiệm vụ dự án, phân công nguồn lực, các yếu tố phụ thuộc nhiệm vụ, bộ chứa dự án và thành viên nhóm dự án. Tuy nhiên, khi các hoạt động tạo, cập nhật hoặc xóa được chạy theo chương trình trên các thực thể cấu trúc phân tích công việc (WBS), lỗi có thể xảy ra. Để theo dõi những lỗi này và lịch sử hoạt động, hai nhật ký quản trị mới đã được triển khai: **Bộ thao tác** và **Dịch vụ lập lịch dự án (PSS)**. Để truy cập các nhật ký này, hãy truy cập **Cài đặt** \> **Tích hợp lịch biểu**.

Hình minh họa sau đây cho thấy mô hình dữ liệu cho nhật ký Lập lịch dự án.

![Mô hình dữ liệu cho nhật ký Lập lịch dự án.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Nhật ký Bộ thao tác

Nhật ký Bộ thao tác theo dõi việc thực hiện một bộ thao tác được sử dụng để chạy một hoặc nhiều thao tác tạo, cập nhật hoặc xóa theo lô trên các dự án, nhiệm vụ dự án, phân công nguồn lực, yếu tố phụ thuộc nhiệm vụ, bộ chứa dự án hoặc thành viên nhóm dự án. Trường **Trạng thái thao tác** hiển thị trạng thái tổng thể của bộ thao tác. Chi tiết về tải trọng của bộ thao tác được ghi lại trong bản ghi Chi tiết bộ thao tác.

### <a name="operation-set"></a>Bộ thao tác

Bảng dưới đây hiển thị các trường có liên quan đến thực thể **Bộ thao tác**.

| Tên lược đồ            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Ngày/giờ khi bộ thao tác hoàn thành hoặc không thành công.                                                | CompletedOn            |
| msdyn_correlationid   | Giá trị **correlationId** của yêu cầu.                                                                  | CorrelationId          |
| msdyn_description     | Mô tả của bộ thao tác.                                                                        | Description            |
| msdyn_executedon      | Ngày/giờ khi bản ghi được chạy.                                                                       | Ngày thực thi            |
| msdyn_operationsetId  | Mã định danh duy nhất của phiên bản thực thể.                                                                   | OperationSet           |
| msdyn_Project         | Dự án có liên quan đến bộ thao tác.                                                            | Dự án                |
| msdyn_projectid       | Giá trị **projectId** của yêu cầu.                                                                      | ProjectId (Không dùng nữa) |
| msdyn_projectName     | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_PSSErrorLog     | Mã định danh duy nhất của nhật ký lỗi Dịch vụ lập lịch dự án được liên kết với bộ thao tác. | Nhật ký lỗi PSS          |
| msdyn_PSSErrorLogName | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_status          | Trạng thái của bộ thao tác.                                                                             | Trạng thái                 |
| msdyn_statusName      | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_useraadid       | ID đối tượng Azure Active Directory (Azure AD) của người dùng có chứa yêu cầu này.                     | UserAADID              |

### <a name="operation-set-detail"></a>Chi tiết bộ thao tác

Bảng dưới đây hiển thị các trường có liên quan đến thực thể **Chi tiết bộ thao tác**.

| Tên lược đồ                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Các trường Dataverse được xếp theo thứ tự cho yêu cầu.                                            | CdsPayload            |
| msdyn_entityname           | Tên của thực thể cho yêu cầu.                                                     | EntityName            |
| msdyn_httpverb             | Phương thức yêu cầu.                                                                         | Hành động HTTP (Không dùng nữa) |
| msdyn_httpverbName         | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_operationset         | Mã định danh duy nhất của bộ thao tác có chứa bản ghi.                      | OperationSet          |
| msdyn_operationsetdetailId | Mã định danh duy nhất của phiên bản thực thể.                                                  | Chi tiết OperationSet   |
| msdyn_operationsetName     | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_operationtype        | Loại thao tác của chi tiết bộ thao tác.                                             | OperationType         |
| msdyn_operationtypeName    | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_psspayload           | Các trường Dịch vụ lập lịch dự án được tuần tự hóa cho yêu cầu.                           | PssPayload            |
| msdyn_recordid             | Mã định danh chính của bản ghi yêu cầu.                                                       | ID Bản ghi             |
| msdyn_requestnumber        | Một số được tạo tự động nhằm xác định thứ tự nhận yêu cầu. | Số yêu cầu        |

## <a name="project-scheduling-service-error-logs"></a>Nhật ký lỗi Dịch vụ lập lịch dự án

Nhật ký lỗi Dịch vụ lập lịch dự án ghi lại các lỗi xảy ra khi Dịch vụ lập lịch dự án thử thao tác **Lưu** hoặc **Mở**. Có ba trường hợp được hỗ trợ trong đó các nhật ký này được tạo:

- Các hành động do người dùng thực hiện không thành công (ví dụ: không thể tạo nhiệm vụ do thiếu đặc quyền).
- Dịch vụ lập lịch dự án không thể tạo, cập nhật, xóa hoặc thực hiện theo lập trình bất kỳ hoạt động xếp tầng nào khác trên một thực thể.
- Người dùng gặp lỗi khi bản ghi không mở được (ví dụ: khi một dự án được mở hoặc thông tin của một thành viên trong nhóm được cập nhật).

### <a name="project-scheduling-service-log"></a>Nhật ký Dịch vụ lập lịch dự án

Bảng dưới đây hiển thị các trường được bao gồm trong nhật ký Dịch vụ lập lịch dự án.

| Tên lược đồ          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Ngăn xếp cuộc gọi của ngoại lệ.                                               | Ngăn xếp cuộc gọi     |
| msdyn_correlationid | ID tương quan của lỗi.                                               | CorrelationId  |
| msdyn_errorcode     | Một trường được sử dụng để lưu trữ mã lỗi Dataverse hoặc mã lỗi HTTP. | Mã lỗi     |
| msdyn_HelpLink      | Liên kết đến tài liệu Trợ giúp công khai.                                       | Đường liên kết trợ giúp      |
| msdyn_log           | Nhật ký từ Dịch vụ lập lịch dự án.                                   | Nhật ký            |
| msdyn_project       | Dự án được liên kết với nhật ký lỗi.                             | Dự án        |
| msdyn_projectName   | Tên của dự án nếu tải trọng bộ thao tác sẽ được duy trì. | Không áp dụng |
| msdyn_psserrorlogId | Mã định danh duy nhất của phiên bản thực thể.                                     | Nhật ký lỗi PSS  |
| msdyn_SessionId     | ID phiên dự án.                                                        | ID phiên     |

## <a name="error-log-cleanup"></a>Dọn sạch nhật ký lỗi

Theo mặc định, cả nhật ký lỗi Dịch vụ lập lịch dự án và nhật ký Bộ thao tác đều có thể được dọn dẹp sau mỗi 90 ngày. Tất cả bản ghi lỗi có thời hạn quá 90 ngày sẽ bị xóa. Tuy nhiên, bằng cách thay đổi giá trị của trường **msdyn_StateOperationSetAge** trên trang **Tham số dự án**, quản trị viên có thể điều chỉnh phạm vi dọn dẹp để nó nằm trong khoảng từ 1 đến 120 ngày. Có một số phương thức để thay đổi giá trị này:

- Tùy chỉnh thực thể **Tham số dự án** bằng cách tạo một trang tùy chỉnh và thêm trường **Tuổi của tập hợp hoạt động cũ**.
- Sử dụng mã máy khách có sử dụng [bộ phát triển phần mềm (SDK) WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Sử dụng mã SDK Dịch vụ sử dụng phương thức Xrm SDK **updateRecord** (Tham chiếu API máy khách) trong các ứng dụng dựa trên mô hình. Power Apps bao gồm mô tả và các tham số được hỗ trợ cho phương thức **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
