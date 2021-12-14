---
title: Nhật ký lập lịch dự án
description: Chủ đề này cung cấp thông tin và mẫu sẽ giúp bạn sử dụng nhật ký Lập lịch dự án để theo dõi các lỗi liên quan đến Dịch vụ lập lịch dự án và API lập lịch dự án.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877523"
---
# <a name="project-scheduling-logs"></a>Nhật ký lập lịch dự án

_**Áp dụng đối với:** Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho, triển khai Lite - đối phó với lập hóa đơn chiếu lệ_, _án cho Web_

Microsoft Dynamics 365 Project Operations sử dụng [Dự án cho Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) làm công cụ lập lịch chính của nó. Thay vì sử dụng Microsoft Dataverse giao diện lập trình ứng dụng web (API) tiêu chuẩn, Hoạt động dự án sử dụng API lập lịch dự án mới để tạo, cập nhật và xóa nhiệm vụ dự án, phân công tài nguyên, phụ thuộc nhiệm vụ, nhóm dự án và thành viên nhóm dự án. Tuy nhiên, khi các hoạt động tạo, cập nhật hoặc xóa được chạy theo chương trình trên các thực thể cấu trúc phân tích công việc (WBS), lỗi có thể xảy ra. Để theo dõi những lỗi này và lịch sử hoạt động, hai nhật ký quản trị mới đã được triển khai: **Bộ hoạt động** và **Dịch vụ lập lịch dự án (PSS)**. Để truy cập các nhật ký này, hãy truy cập **Cài đặt** \> **Tích hợp lịch biểu**.

Hình minh họa sau đây cho thấy mô hình dữ liệu cho nhật ký Lập lịch dự án.

![Mô hình dữ liệu cho nhật ký Lập lịch dự án.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Nhật ký Bộ hoạt động

Nhật ký Nhóm hoạt động theo dõi việc thực hiện một nhóm hoạt động được sử dụng để chạy một hoặc nhiều hoạt động tạo, cập nhật hoặc xóa trong một loạt dự án, nhiệm vụ dự án, phân công tài nguyên, phụ thuộc nhiệm vụ, nhóm dự án hoặc thành viên nhóm dự án. Các **Hoạt động ở trạng thái** trường hiển thị trạng thái tổng thể của tập hợp hoạt động. Chi tiết về tải trọng của nhóm hoạt động được ghi lại trong hồ sơ Chi tiết Nhóm hoạt động có liên quan.

### <a name="operation-set"></a>Bộ hoạt động

Bảng sau đây cho thấy các trường liên quan đến **Bộ hoạt động** thực thể.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Ngày / giờ khi thiết lập hoạt động được hoàn thành hoặc không thành công.                                                | CompletedOn            |
| msdyn_correlationid   | Các **tương quanId** giá trị của yêu cầu.                                                                  | CorrelationId          |
| msdyn_description     | Mô tả của bộ hoạt động.                                                                        | Description            |
| msdyn_executedon      | Ngày / giờ khi bản ghi được chạy.                                                                       | Ngày thực thi            |
| msdyn_operationsetId  | Định danh duy nhất của các cá thể thực thể.                                                                   | OperationSet           |
| msdyn_Project         | Dự án có liên quan đến bộ hoạt động.                                                            | Dự án                |
| msdyn_projectid       | Các **projectId** giá trị của yêu cầu.                                                                      | ProjectId (Không dùng nữa) |
| msdyn_projectName     | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_PSSErrorLog     | Định danh duy nhất của nhật ký lỗi Dịch vụ lập lịch dự án được liên kết với tập hoạt động. | Nhật ký lỗi PSS          |
| msdyn_PSSErrorLogName | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_status          | Trạng thái của tập hợp hoạt động.                                                                             | Trạng thái                 |
| msdyn_statusName      | Không áp dụng.                                                                                              | Không áp dụng         |
| msdyn_useraadid       | ID đối tượng Azure Active Directory (Azure AD) của người dùng chứa yêu cầu.                     | UserAADID              |

### <a name="operation-set-detail"></a>Chi tiết Bộ Hoạt động

Bảng sau đây cho thấy các trường liên quan đến **Chi tiết Bộ Hoạt động** thực thể.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Các trường Dataverse được tuần tự hóa cho yêu cầu.                                            | CdsPayload            |
| msdyn_entityname           | Tên của thực thể cho yêu cầu.                                                     | EntityName            |
| msdyn_httpverb             | Phương thức yêu cầu.                                                                         | Hành động HTTP (Không dùng nữa) |
| msdyn_httpverbName         | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_operationset         | Định danh duy nhất của tập hoạt động mà bản ghi thuộc về.                      | OperationSet          |
| msdyn_operationsetdetailId | Định danh duy nhất của các cá thể thực thể.                                                  | Chi tiết OperationSet   |
| msdyn_operationsetName     | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_operationtype        | Loại hoạt động của chi tiết tập hợp hoạt động.                                             | OperationType         |
| msdyn_operationtypeName    | Không áp dụng.                                                                             | Không áp dụng        |
| msdyn_psspayload           | Các trường Dịch vụ lập lịch dự án được tuần tự hóa cho yêu cầu.                           | PssPayload            |
| msdyn_recordid             | Định danh của bản ghi yêu cầu.                                                       | ID Bản ghi             |
| msdyn_requestnumber        | Một số được tạo tự động xác định thứ tự nhận được yêu cầu. | Số yêu cầu        |

## <a name="project-scheduling-service-error-logs"></a>Nhật ký lỗi Dịch vụ lập lịch dự án

Bản ghi lỗi của Dịch vụ lập lịch trình dự án ghi lại các lỗi xảy ra khi Dịch vụ lập lịch dự án thử một **Cứu** hoặc **Mở ra** hoạt động. Có ba trường hợp được hỗ trợ trong đó các nhật ký này được tạo:

- Các hành động do người dùng thực hiện nghiêm trọng không thành công (ví dụ: không thể tạo nhiệm vụ do thiếu đặc quyền).
- Dịch vụ lập lịch dự án không thể lập trình tạo, cập nhật, xóa hoặc thực hiện bất kỳ hoạt động xếp tầng nào khác trên một thực thể.
- Người dùng gặp lỗi khi bản ghi không mở được (ví dụ: khi một dự án được mở hoặc thông tin của một thành viên trong nhóm được cập nhật).

### <a name="project-scheduling-service-log"></a>Nhật ký dịch vụ lập lịch dự án

Bảng sau đây cho thấy các trường được bao gồm trong nhật ký Dịch vụ Lập lịch Dự án.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Ngăn xếp cuộc gọi của ngoại lệ.                                               | Ngăn xếp cuộc gọi     |
| msdyn_correlationid | ID tương quan của lỗi.                                               | CorrelationId  |
| msdyn_errorcode     | Trường được sử dụng để lưu trữ mã lỗi Dataverse hoặc mã lỗi HTTP. | Mã lỗi     |
| msdyn_HelpLink      | Một liên kết đến tài liệu Trợ giúp công khai.                                       | Đường liên kết trợ giúp      |
| msdyn_log           | Nhật ký từ Dịch vụ lập lịch dự án.                                   | Nhật ký            |
| msdyn_project       | Dự án được liên kết với nhật ký lỗi.                             | Dự án        |
| msdyn_projectName   | Tên của dự án nếu trọng tải của tập hoạt động sẽ được duy trì. | Không áp dụng |
| msdyn_psserrorlogId | Định danh duy nhất của các cá thể thực thể.                                     | Nhật ký lỗi PSS  |
| msdyn_SessionId     | ID phiên dự án.                                                        | ID phiên     |

## <a name="error-log-cleanup"></a>Lỗi dọn dẹp nhật ký

Theo mặc định, cả nhật ký lỗi Dịch vụ lập lịch dự án và nhật ký Bộ hoạt động đều có thể được dọn dẹp sau mỗi 90 ngày. Bất kỳ hồ sơ nào cũ hơn 90 ngày sẽ bị xóa. Tuy nhiên, bằng cách thay đổi giá trị của **msdyn_StateOperationSetAge** lĩnh vực trên **Tham số dự án**, quản trị viên có thể điều chỉnh phạm vi dọn dẹp sao cho từ 1 đến 120 ngày. Một số phương pháp để thay đổi giá trị này có sẵn:

- Tùy chỉnh **Tham số dự án** thực thể bằng cách tạo một trang tùy chỉnh và thêm **Hoạt động cũ đặt tuổi** đồng ruộng.
- Sử dụng mã khách hàng sử dụng [Bộ phát triển phần mềm WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Sử dụng mã SDK dịch vụ sử dụng Xrm SDK **updateRecord** (Tham chiếu API ứng dụng khách) trong các ứng dụng theo mô hình. Power Apps bao gồm mô tả và các thông số được hỗ trợ cho **updateRecord** phương pháp.

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
