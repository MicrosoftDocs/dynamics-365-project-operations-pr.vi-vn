---
title: Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu
description: Bài viết này cung cấp thông tin và các mẫu để sử dụng API lịch trình dự án.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541151"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


**Thực thể lập lịch trình**

Các API lịch trình dự án cung cấp khả năng thực hiện các hoạt động tạo, cập nhật và xóa với **Các thực thể lập lịch trình**. Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web. Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.

Bảng sau cung cấp danh sách đầy đủ các thực thể lịch trình của Dự án.

| **Tên thực thể**         | **Tên logic của thực thể**     |
|-------------------------|-----------------------------|
| Dự án                 | msdyn_project               |
| Nhiệm vụ dự án            | msdyn_projecttask           |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | msdyn_projecttaskdependency |
| Gán Nguồn lực     | msdyn_resourceassignment    |
| Bộ chứa Dự án          | msdyn_projectbucket         |
| Thành viên Nhóm Dự án     | msdyn_projectteam           |
| Danh sách kiểm tra dự án      | msdyn_projectchecklist      |
| Nhãn dự án           | msdyn_projectlabel          |
| Nhiệm vụ dự án để gắn nhãn   | msdyn_projecttasktolabel    |
| Phân đoạn nước rút trong dự án          | msdyn_projectsprint         |

**OperationSet**

OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.

**API lịch trình dự án**

Sau đây là danh sách các API lịch trình Dự án hiện tại.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | API này được sử dụng để tạo dự án. Nhóm dự án và dự án mặc định được tạo ngay lập tức.                         |
| **msdyn_CreateTeamMemberV1**            | API này được sử dụng để tạo thành viên nhóm dự án. Hồ sơ thành viên trong nhóm được tạo ngay lập tức.                                  |
| **msdyn_CreateOperationSetV1**          | API này được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.                                        |
| **msdyn_PssCreateV1**                   | API này được sử dụng để tạo thực thể. Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động tạo. |
| **msdyn_PssUpdateV1**                   | API này được sử dụng để cập nhật thực thể. Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động cập nhật  |
| **msdyn_PssDeleteV1**                   | API này được sử dụng để xóa thực thể. Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động xóa. |
| **msdyn_ExecuteOperationSetV1**         | API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | API này được sử dụng để cập nhật đường viền công việc đã lên kế hoạch Phân công nguồn lực.                                                        |



**Sử dụng API lịch trình dự án với OperationSet**

Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**. Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.

**Thao tác được hỗ trợ**

| **Thực thể lập lịch trình**   | **Tạo** | **Update** | **Delete** | **Những điều quan trọng cần cân nhắc**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nhiệm vụ dự án            | Có        | Có        | Có        | Các trường **Tiến trình**, **EffortCompleted** và **EffortRemaining** có thể được chỉnh sửa trong Project for the Web nhưng không thể chỉnh sửa trong Project Operations.                                                                                                                                                                                             |
| Quan hệ phụ thuộc nhiệm vụ dự án | Có        | No         | Có        | Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật. Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.                                                                                                                                                                                                                                 |
| Công việc giao cho nguồn lực     | Có        | Có\*      | Có        | Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**. Bản ghi việc được giao không được cập nhật. Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo. Một API riêng biệt đã được cung cấp để cập nhật các đường viền Phân công nguồn lực. |
| Nhóm dự án          | Có        | Có        | Có        | Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**. Hỗ trợ tạo và xóa bộ chứa dự án đã được thêm vào trong Bản phát hành cập nhật 16.                                                                                                                                                                                                   |
| Thành viên nhóm dự án     | Có        | Có        | Có        | Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Dự án                 | Có        | Có        |            | Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**.                                                                                       |
| Danh sách kiểm tra dự án      | Có        | Có        | Có        |                                                                                                                                                                                                                                                                                                                                                         |
| Nhãn dự án           | No         | Có        | No         | Tên nhãn có thể được thay đổi. Tính năng này chỉ có sẵn trong Project for the Web                                                                                                                                                                                                                                                                      |
| Nhiệm vụ dự án để gắn nhãn   | Có        | No         | Có        | Tính năng này chỉ có sẵn trong Project for the Web                                                                                                                                                                                                                                                                                                  |
| Phân đoạn nước rút trong dự án          | Có        | Có        | Có        | Trường **Bắt đầu** phải có ngày sớm hơn trường **Kết thúc**. Các phân đoạn nước rút cho cùng một dự án không được trùng lặp với nhau. Tính năng này chỉ có sẵn trong Project for the Web                                                                                                                                                                    |




Thuộc tính ID là không bắt buộc. Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng. Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.

**Các giới hạn và vấn đề đã biết**

Sau đây là danh sách các giới hạn và vấn đề đã biết:

-   API lịch trình dự án chỉ có thể được sử dụng bởi **Người dùng có Giấy phép Microsoft Project**. Những đối tượng sau không thể sử dụng API lịch trình:
    -   Người dùng ứng dụng
    -   Người dùng hệ thống
    -   Người dùng tích hợp
    -   Những người dùng khác không có giấy phép bắt buộc
-   Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.
-   Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.
-   Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.
-   Mỗi thao tác Cập nhật đường viền phân công nguồn lực tính là một thao tác đơn lẻ.
-   Mỗi danh sách các đường viền được cập nhật có thể chứa tối đa 100 lát cắt thời gian.
-   Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.
-   Có tối đa 400 lát cắt cho mỗi dự án.
-   [Giới hạn và ranh giới đối với các dự án và nhiệm vụ](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Các nhãn hiện chỉ có sẵn trong Project for the Web.

**Xử lý lỗi**

-   Để xem lại các lỗi được tạo từ Bộ hoạt động, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Bộ hoạt động**.
-   Để xem lại các lỗi được tạo ra từ Dịch vụ lịch trình dự án, hãy truy cập **Cài đặt** \> **Tích hợp lịch trình** \> **Nhật ký lỗi PSS**.

**Chỉnh sửa đường viền phân công nguồn lực**

Không giống như tất cả các API lập lịch dự án khác có thể cập nhật một thực thể, API đường viên phân công tài nguyên chỉ chịu trách nhiệm cập nhật cho một trường duy nhất, msdyn_plannedwork, trên một thực thể duy nhất, msydn_resourceassignment.

Chế độ lịch trình đã cho là:

-   **đơn vị cố định**
-   lịch dự án là 9-5p là 9-5pst, Thứ Hai, Thứ Ba, Thứ Năm, Thứ Sáu (KHÔNG LÀM VIỆC THỨ TƯ)
-   và lịch nguồn lực là 9-1p PST từ Thứ Hai đến Thứ Sáu

Phân công này là cho một tuần, bốn giờ một ngày. Điều này là do lịch nguồn lực từ 9-1 PST, hoặc bốn giờ một ngày.

| &nbsp;     | Tác vụ | Ngày bắt đầu | Ngày kết thúc  | Số lượng | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| nhân viên 9-1 |  T1  | 13/6/2022  | 17/6/2022 | 20       | Tệp 4         | Tệp 4         | Tệp 4         | Tệp 4         | Tệp 4         |

Ví dụ: nếu bạn muốn nhân viên chỉ làm việc ba giờ mỗi ngày trong tuần này và cho phép một giờ cho các nhiệm vụ khác.

#### <a name="updatedcontours-sample-payload"></a>Tải trọng mẫu UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Đây là nhiệm vụ sau khi chạy API lình trình cập nhật đường viền.

| &nbsp;     | Tác vụ | Ngày bắt đầu | Ngày kết thúc  | Số lượng | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| nhân viên 9-1 | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Kịch bản mẫu**

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

** Các mẫu khác

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
