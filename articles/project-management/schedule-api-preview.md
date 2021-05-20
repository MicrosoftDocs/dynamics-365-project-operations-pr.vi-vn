---
title: Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình
description: Chủ đề này cung cấp thông tin và mẫu để sử dụng API lịch trình.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950830"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

> [!IMPORTANT] 
> Một số hoặc tất cả chức năng được ghi chú trong chủ đề này khả dụng như một phần của bản phát hành xem trước. Nội dung và chức năng có thể thay đổi. 

## <a name="scheduling-entities"></a>Thực thể lập lịch trình

API lịch trình cung cấp khả năng thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**. Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web. Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.

Bảng sau cung cấp danh sách đầy đủ các **Thực thể lập lịch trình**.

| Tên thực thể  | Tên logic của thực thể |
| --- | --- |
| Dự án | msdyn_project |
| Nhiệm vụ dự án  | msdyn_projecttask  |
| Quan hệ phụ thuộc Nhiệm vụ Dự án  | msdyn_projecttaskdependency  |
| Gán Nguồn lực | msdyn_resourceassignment |
| Bộ chứa Dự án  | msdyn_projectbucket |
| Thành viên Nhóm Dự án | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.

## <a name="schedule-apis"></a>API lịch trình

Sau đây là danh sách các API lịch trình hiện tại.

- **msdyn_CreateProjectV1**: API này có thể được dùng để tạo một dự án. Nhóm dự án và dự án mặc định được tạo ngay lập tức.
- **msdyn_CreateTeamMemberV1**: API này có thể được dùng để tạo một thành viên trong nhóm dự án. Hồ sơ thành viên trong nhóm được tạo ngay lập tức.
- **msdyn_CreateOperationSetV1**: API này có thể được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.
- **msdyn_PSSCreateV1**: API này có thể được dùng để tạo một thực thể. Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác tạo.
- **msdyn_PSSUpdateV1**: API này có thể được dùng để cập nhật một thực thể. Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác cập nhật.
- **msdyn_PSSDeleteV1**: API này có thể được dùng để xóa một thực thể. Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác xóa.
- **msdyn_ExecuteOperationSetV1**: API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.

## <a name="using-schedule-apis-with-operationset"></a>Sử dụng API lịch trình với OperationSet

Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**. Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.

## <a name="supported-operations"></a>Thao tác được hỗ trợ

| Thực thể lập lịch trình | Tạo | Update | Delete | Những điều quan trọng cần cân nhắc |
| --- | --- | --- | --- | --- |
Nhiệm vụ dự án | Có | Có | Có | Không có |
| Quan hệ phụ thuộc nhiệm vụ dự án | Có | Có | | Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật. Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo. |
| Công việc giao cho nguồn lực | Có | Có | | Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**. Bản ghi việc được giao không được cập nhật. Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo. |
| Nhóm dự án | Không áp dụng | Không áp dụng | Không áp dụng | Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**. |
| Thành viên nhóm dự án | Có | Có | Có | Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**. |
| Dự án | Có | Có | Không áp dụng | Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**. |

Các API này có thể được gọi ra với các đối tượng thực thể bao gồm các trường tùy chỉnh.

Thuộc tính ID là không bắt buộc. Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng. Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.

## <a name="restricted-fields"></a>Các trường bị hạn chế

Các bảng sau xác định các trường bị hạn chế trong **Tạo** và **Chỉnh sửa**.

### <a name="project-task"></a>Nhiệm vụ dự án

| **Tên lô-gic**                       | **Có thể tạo** | **Có thể chỉnh sửa**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | không             | không               |
| msdyn_actualcost_base                  | không             | không               |
| msdyn_actualend                        | không             | không               |
| msdyn_actualsales                      | không             | không               |
| msdyn_actualsales_base                 | không             | không               |
| msdyn_actualstart                      | không             | không               |
| msdyn_costatcompleteestimate           | không             | không               |
| msdyn_costatcompleteestimate_base      | không             | không               |
| msdyn_costconsumptionpercentage        | không             | không               |
| msdyn_effortcompleted                  | không             | không               |
| msdyn_effortestimateatcomplete         | không             | không               |
| msdyn_iscritical                       | không             | không               |
| msdyn_iscriticalname                   | không             | không               |
| msdyn_ismanual                         | không             | không               |
| msdyn_ismanualname                     | không             | không               |
| msdyn_ismilestone                      | không             | không               |
| msdyn_ismilestonename                  | không             | không               |
| msdyn_LinkStatus                       | không             | không               |
| msdyn_linkstatusname                   | không             | không               |
| msdyn_msprojectclientid                | không             | không               |
| msdyn_plannedcost                      | không             | không               |
| msdyn_plannedcost_base                 | không             | không               |
| msdyn_plannedsales                     | không             | không               |
| msdyn_plannedsales_base                | không             | không               |
| msdyn_pluginprocessingdata             | không             | không               |
| msdyn_progress                         | không             | không (có cho P4W) |
| msdyn_remainingcost                    | không             | không               |
| msdyn_remainingcost_base               | không             | không               |
| msdyn_remainingsales                   | không             | không               |
| msdyn_remainingsales_base              | không             | không               |
| msdyn_requestedhours                   | không             | không               |
| msdyn_resourcecategory                 | không             | không               |
| msdyn_resourcecategoryname             | không             | không               |
| msdyn_resourceorganizationalunitid     | không             | không               |
| msdyn_resourceorganizationalunitidname | không             | không               |
| msdyn_salesconsumptionpercentage       | không             | không               |
| msdyn_salesestimateatcomplete          | không             | không               |
| msdyn_salesestimateatcomplete_base     | không             | không               |
| msdyn_salesvariance                    | không             | không               |
| msdyn_salesvariance_base               | không             | không               |
| msdyn_scheduleddurationminutes         | không             | không               |
| msdyn_scheduledend                     | không             | không               |
| msdyn_scheduledstart                   | không             | không               |
| msdyn_schedulevariance                 | không             | không               |
| msdyn_skipupdateestimateline           | không             | không               |
| msdyn_skipupdateestimatelinename       | không             | không               |
| msdyn_summary                          | không             | không               |
| msdyn_varianceofcost                   | không             | không               |
| msdyn_varianceofcost_base              | không             | không               |

### <a name="project-task-dependency"></a>Quan hệ phụ thuộc nhiệm vụ dự án

| **Tên lô-gic**              | **Có thể tạo** | **Có thể chỉnh sửa** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | không             | không           |
| msdyn_linktypename            | không             | không           |
| msdyn_predecessortask         | có            | không           |
| msdyn_predecessortaskname     | có            | không           |
| msdyn_project                 | có            | không           |
| msdyn_projectname             | có            | không           |
| msdyn_projecttaskdependencyid | có            | không           |
| msdyn_successortask           | có            | không           |
| msdyn_successortaskname       | có            | không           |

### <a name="resource-assignment"></a>Công việc giao cho nguồn lực

| **Tên lô-gic**             | **Có thể tạo** | **Có thể chỉnh sửa** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | có            | không           |
| msdyn_bookableresourceidname | có            | không           |
| msdyn_bookingstatusid        | không             | không           |
| msdyn_bookingstatusidname    | không             | không           |
| msdyn_committype             | không             | không           |
| msdyn_committypename         | không             | không           |
| msdyn_effort                 | không             | không           |
| msdyn_effortcompleted        | không             | không           |
| msdyn_effortremaining        | không             | không           |
| msdyn_finish                 | không             | không           |
| msdyn_plannedcost            | không             | không           |
| msdyn_plannedcost_base       | không             | không           |
| msdyn_plannedcostcontour     | không             | không           |
| msdyn_plannedsales           | không             | không           |
| msdyn_plannedsales_base      | không             | không           |
| msdyn_plannedsalescontour    | không             | không           |
| msdyn_plannedwork            | không             | không           |
| msdyn_projectid              | có            | không           |
| msdyn_projectidname          | không             | không           |
| msdyn_projectteamid          | không             | không           |
| msdyn_projectteamidname      | không             | không           |
| msdyn_start                  | không             | không           |
| msdyn_taskid                 | không             | không           |
| msdyn_taskidname             | không             | không           |
| msdyn_userresourceid         | không             | không           |

### <a name="project-team-member"></a>Thành viên nhóm dự án

| **Tên lô-gic**                                 | **Có thể tạo** | **Có thể chỉnh sửa** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | không             | không           |
| msdyn_creategenericteammemberwithrequirementname | không             | không           |
| msdyn_deletestatus                               | không             | không           |
| msdyn_deletestatusname                           | không             | không           |
| msdyn_effort                                     | không             | không           |
| msdyn_effortcompleted                            | không             | không           |
| msdyn_effortremaining                            | không             | không           |
| msdyn_finish                                     | không             | không           |
| msdyn_hardbookedhours                            | không             | không           |
| msdyn_hours                                      | không             | không           |
| msdyn_markedfordeletiontimer                     | không             | không           |
| msdyn_markedfordeletiontimestamp                 | không             | không           |
| msdyn_msprojectclientid                          | không             | không           |
| msdyn_percentage                                 | không             | không           |
| msdyn_requiredhours                              | không             | không           |
| msdyn_softbookedhours                            | không             | không           |
| msdyn_start                                      | không             | không           |

### <a name="project"></a>Dự án

| **Tên lô-gic**                       | **Có thể tạo** | **Có thể chỉnh sửa** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | không             | không           |
| msdyn_actualexpensecost_base           | không             | không           |
| msdyn_actuallaborcost                  | không             | không           |
| msdyn_actuallaborcost_base             | không             | không           |
| msdyn_actualsales                      | không             | không           |
| msdyn_actualsales_base                 | không             | không           |
| msdyn_contractlineproject              | có            | không           |
| msdyn_contractorganizationalunitid     | có            | không           |
| msdyn_contractorganizationalunitidname | có            | không           |
| msdyn_costconsumption                  | không             | không           |
| msdyn_costestimateatcomplete           | không             | không           |
| msdyn_costestimateatcomplete_base      | không             | không           |
| msdyn_costvariance                     | không             | không           |
| msdyn_costvariance_base                | không             | không           |
| msdyn_duration                         | không             | không           |
| msdyn_effort                           | không             | không           |
| msdyn_effortcompleted                  | không             | không           |
| msdyn_effortestimateatcompleteeac      | không             | không           |
| msdyn_effortremaining                  | không             | không           |
| msdyn_finish                           | có            | có          |
| msdyn_globalrevisiontoken              | không             | không           |
| msdyn_islinkedtomsprojectclient        | không             | không           |
| msdyn_islinkedtomsprojectclientname    | không             | không           |
| msdyn_linkeddocumenturl                | không             | không           |
| msdyn_msprojectdocument                | không             | không           |
| msdyn_msprojectdocumentname            | không             | không           |
| msdyn_plannedexpensecost               | không             | không           |
| msdyn_plannedexpensecost_base          | không             | không           |
| msdyn_plannedlaborcost                 | không             | không           |
| msdyn_plannedlaborcost_base            | không             | không           |
| msdyn_plannedsales                     | không             | không           |
| msdyn_plannedsales_base                | không             | không           |
| msdyn_progress                         | không             | không           |
| msdyn_remainingcost                    | không             | không           |
| msdyn_remainingcost_base               | không             | không           |
| msdyn_remainingsales                   | không             | không           |
| msdyn_remainingsales_base              | không             | không           |
| msdyn_replaylogheader                  | không             | không           |
| msdyn_salesconsumption                 | không             | không           |
| msdyn_salesestimateatcompleteeac       | không             | không           |
| msdyn_salesestimateatcompleteeac_base  | không             | không           |
| msdyn_salesvariance                    | không             | không           |
| msdyn_salesvariance_base               | không             | không           |
| msdyn_scheduleperformance              | không             | không           |
| msdyn_scheduleperformancename          | không             | không           |
| msdyn_schedulevariance                 | không             | không           |
| msdyn_taskearlieststart                | không             | không           |
| msdyn_teamsize                         | không             | không           |
| msdyn_teamsize_date                    | không             | không           |
| msdyn_teamsize_state                   | không             | không           |
| msdyn_totalactualcost                  | không             | không           |
| msdyn_totalactualcost_base             | không             | không           |
| msdyn_totalplannedcost                 | không             | không           |
| msdyn_totalplannedcost_base            | không             | không           |


## <a name="limitations-and-known-issues"></a>Các giới hạn và vấn đề đã biết
Sau đây là danh sách các giới hạn và vấn đề đã biết:

- Chỉ **Người dùng có giấy phép dự án của Microsoft** là có thể sử dụng API lịch trình. Những đối tượng sau không thể sử dụng API lịch trình:
    - Người dùng ứng dụng
    - Người dùng hệ thống
    - Người dùng tích hợp
    - Những người dùng khác không có giấy phép bắt buộc
- Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.
- Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.
- Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.
- Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.
- API lịch trình ở Bản xem trước công khai. Microsoft không hỗ trợ sử dụng các API này trong Môi trường sản xuất.
- [Giới hạn và ranh giới đối với các dự án và nhiệm vụ](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Xử lý lỗi

   - Để xem lại các lỗi được tạo từ Bộ hoạt động, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Bộ hoạt động**.
   - Để xem lại các lỗi được tạo từ Dịch vụ lên lịch dự án, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Nhật ký lỗi PSS**.

## <a name="sample-scenario"></a>Kịch bản mẫu

Trong kịch bản này, bạn sẽ tạo một dự án, một thành viên nhóm, bốn nhiệm vụ và hai công việc giao cho nguồn lực. Tiếp theo, bạn sẽ cập nhật một nhiệm vụ, cập nhật dự án, xóa một nhiệm vụ, xóa một công việc giao cho nguồn lực và tạo một quan hệ phụ thuộc nhiệm vụ.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Các mẫu khác

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
