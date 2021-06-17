---
title: Triển khai trường tùy chỉnh cho ứng dụng Microsoft Dynamics 365 Project Timesheet dành cho thiết bị di động trên iOS và Android
description: Chủ đề này cung cấp các mẫu hình phổ biến để sử dụng tiện ích mở rộng để triển khai trường tùy chỉnh.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003071"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="1cd41-103">Triển khai trường tùy chỉnh cho ứng dụng Microsoft Dynamics 365 Project Timesheet dành cho thiết bị di động trên iOS và Android</span><span class="sxs-lookup"><span data-stu-id="1cd41-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cd41-104">Chủ đề này cung cấp các mẫu hình phổ biến để sử dụng tiện ích mở rộng để triển khai trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="1cd41-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="1cd41-105">Các chủ đề sau được đề cập:</span><span class="sxs-lookup"><span data-stu-id="1cd41-105">The following topics are covered:</span></span>

- <span data-ttu-id="1cd41-106">Các loại dữ liệu khác nhau mà khuôn khổ trường tùy chỉnh hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="1cd41-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="1cd41-107">Cách hiển thị trường chỉ đọc hoặc trường có thể chỉnh sửa trên các mục nhập trong bảng chấm công và lưu giá trị do người dùng cung cấp trở lại cơ sở dữ liệu</span><span class="sxs-lookup"><span data-stu-id="1cd41-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="1cd41-108">Cách hiển thị trường chỉ đọc trong phần thông tin cơ bản về bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="1cd41-109">Cách tích hợp logic nghiệp vụ tùy chỉnh khác để nhập giá trị mặc định vào các trường và thực hiện xác thực bổ sung</span><span class="sxs-lookup"><span data-stu-id="1cd41-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="1cd41-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="1cd41-110">Audience</span></span>

<span data-ttu-id="1cd41-111">Chủ đề này được biên soạn cho các nhà phát triển tích hợp trường tùy chỉnh của họ vào ứng dụng Microsoft Dynamics 365 Project Timesheet dành cho thiết bị di động trên Apple iOS và Google Android.</span><span class="sxs-lookup"><span data-stu-id="1cd41-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="1cd41-112">Chúng tôi giả định là người đọc đã quen thuộc với chức năng phát triển X++ và bảng chấm công dự án.</span><span class="sxs-lookup"><span data-stu-id="1cd41-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="1cd41-113">Hợp đồng dữ liệu – lớp TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="1cd41-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="1cd41-114">Lớp **TSTimesheetCustomField** là lớp hợp đồng dữ liệu X++ đại diện cho thông tin về trường tùy chỉnh cho chức năng bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="1cd41-115">Danh sách các đối tượng trường tùy chỉnh được chuyển trên cả hợp đồng dữ liệu TSTimesheetDetails và hợp đồng dữ liệu TSTimesheetEntry để hiển thị các trường tùy chỉnh trong ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="1cd41-116">**TSTimesheetDetails** – Hợp đồng thông tin cơ bản về bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="1cd41-117">**TSTimesheetEntry** – Hợp đồng giao dịch trong bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="1cd41-118">Các nhóm đối tượng này có cùng thông tin dự án và giá trị **timesheetLineRecId** sẽ tạo thành một dòng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="1cd41-119">fieldBaseType (Loại)</span><span class="sxs-lookup"><span data-stu-id="1cd41-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="1cd41-120">Thuộc tính **FieldBaseType** trên đối tượng **TsTimesheetCustom** xác định loại trường sẽ xuất hiện trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="1cd41-121">Các giá trị **Loại** sau được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="1cd41-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="1cd41-122">Giá trị loại</span><span class="sxs-lookup"><span data-stu-id="1cd41-122">Types value</span></span> | <span data-ttu-id="1cd41-123">Loại</span><span class="sxs-lookup"><span data-stu-id="1cd41-123">Type</span></span>              | <span data-ttu-id="1cd41-124">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="1cd41-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="1cd41-125">0</span><span class="sxs-lookup"><span data-stu-id="1cd41-125">0</span></span>           | <span data-ttu-id="1cd41-126">Chuỗi (và Enum)</span><span class="sxs-lookup"><span data-stu-id="1cd41-126">String (and Enum)</span></span> | <span data-ttu-id="1cd41-127">Trường này xuất hiện dưới dạng trường văn bản.</span><span class="sxs-lookup"><span data-stu-id="1cd41-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="1cd41-128">1</span><span class="sxs-lookup"><span data-stu-id="1cd41-128">1</span></span>           | <span data-ttu-id="1cd41-129">Integer</span><span class="sxs-lookup"><span data-stu-id="1cd41-129">Integer</span></span>           | <span data-ttu-id="1cd41-130">Giá trị được hiển thị dưới dạng số không có chữ số thập phân.</span><span class="sxs-lookup"><span data-stu-id="1cd41-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="1cd41-131">2</span><span class="sxs-lookup"><span data-stu-id="1cd41-131">2</span></span>           | <span data-ttu-id="1cd41-132">Thực</span><span class="sxs-lookup"><span data-stu-id="1cd41-132">Real</span></span>              | <span data-ttu-id="1cd41-133">Giá trị được hiển thị dưới dạng số có chữ số thập phân.</span><span class="sxs-lookup"><span data-stu-id="1cd41-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="1cd41-134">Để hiển thị giá trị thực dưới dạng tiền tệ trong ứng dụng, hãy sử dụng thuộc tính **fieldExisededType**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="1cd41-135">Bạn có thể dùng thuộc tính **numberOfDecimals** để đặt số chữ số thập phân được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="1cd41-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="1cd41-136">3</span><span class="sxs-lookup"><span data-stu-id="1cd41-136">3</span></span>           | <span data-ttu-id="1cd41-137">Ngày</span><span class="sxs-lookup"><span data-stu-id="1cd41-137">Date</span></span>              | <span data-ttu-id="1cd41-138">Định dạng ngày được xác định theo mục thiết đặt **Ngày, giờ và định dạng số** của người dùng, giá trị đó được chỉ định ở phần **Tùy chọn ngôn ngữ và quốc gia/khu vực** trong **Tùy chọn người dùng**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="1cd41-139">4</span><span class="sxs-lookup"><span data-stu-id="1cd41-139">4</span></span>           | <span data-ttu-id="1cd41-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="1cd41-140">Boolean</span></span>           | |
| <span data-ttu-id="1cd41-141">15</span><span class="sxs-lookup"><span data-stu-id="1cd41-141">15</span></span>          | <span data-ttu-id="1cd41-142">GUID</span><span class="sxs-lookup"><span data-stu-id="1cd41-142">GUID</span></span>              | |
| <span data-ttu-id="1cd41-143">16</span><span class="sxs-lookup"><span data-stu-id="1cd41-143">16</span></span>          | <span data-ttu-id="1cd41-144">Int64</span><span class="sxs-lookup"><span data-stu-id="1cd41-144">Int64</span></span>             | |

- <span data-ttu-id="1cd41-145">Nếu thuộc tính **stringOptions** không được cung cấp trên đối tượng **TSTimesheetCustomField**, thì người dùng sẽ được cung cấp một trường văn bản tự do.</span><span class="sxs-lookup"><span data-stu-id="1cd41-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="1cd41-146">Thuộc tính **stringLength** có thể được sử dụng để thiết lập độ dài chuỗi tối đa mà người dùng có thể nhập.</span><span class="sxs-lookup"><span data-stu-id="1cd41-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="1cd41-147">Nếu thuộc tính **stringOptions** được cung cấp trên đối tượng **TSTimesheetCustomField**, thì các phần tử danh sách đó là những giá trị duy nhất mà người dùng có thể chọn bằng các nút tùy chọn (nút radio).</span><span class="sxs-lookup"><span data-stu-id="1cd41-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="1cd41-148">Trong trường hợp này, trường chuỗi có thể đóng vai trò như một giá trị enum để người dùng nhập.</span><span class="sxs-lookup"><span data-stu-id="1cd41-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="1cd41-149">Để lưu giá trị vào cơ sở dữ liệu dưới dạng enum, hãy ánh xạ thủ công giá trị chuỗi trở lại giá trị enum trước khi bạn lưu vào cơ sở dữ liệu bằng chuỗi lệnh (hãy xem ví dụ trong "Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu" ở phần sau của chủ đề này).</span><span class="sxs-lookup"><span data-stu-id="1cd41-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="1cd41-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="1cd41-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="1cd41-151">Bạn có thể sử dụng thuộc tính này để định dạng giá trị thực dưới dạng tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="1cd41-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="1cd41-152">Phương pháp này chỉ có thể áp dụng khi giá trị **fieldBaseType** là **Thực**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="1cd41-153">**TSCustomFieldExtendedType:None** – Không có định dạng nào được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="1cd41-154">**TSCustomFieldExtendedType::Currency** – Định dạng giá trị dưới dạng tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="1cd41-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="1cd41-155">Khi tùy chọn định dạng tiền tệ đang hoạt động, trường **stringValue** có thể được sử dụng để chuyển mã tiền tệ sẽ được hiển thị trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="1cd41-156">Giá trị này là giá trị chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="1cd41-156">The value is a read-only value.</span></span>

    <span data-ttu-id="1cd41-157">Trường **realValue** chứa số tiền sẽ được lưu vào cơ sở dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="1cd41-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="1cd41-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="1cd41-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="1cd41-159">Bạn có thể sử dụng thuộc tính này để chỉ định nơi hiển thị trường tùy chỉnh trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="1cd41-160">**TSCustomFieldSection::Header** – Trường sẽ xuất hiện ở phần **Xem thêm chi tiết** trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="1cd41-161">Các trường này luôn là chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="1cd41-161">These fields are always read-only.</span></span>
- <span data-ttu-id="1cd41-162">**TSCustomFieldSection::Line** – Trường sẽ xuất hiện sau tất cả các trường dòng sẵn dùng trên các mục nhập bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="1cd41-163">Các trường này có thể là dạng chỉnh sửa được hoặc chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="1cd41-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="1cd41-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="1cd41-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="1cd41-165">Thuộc tính này xác định trường khi các giá trị mà ứng dụng cung cấp được lưu trở lại cơ sở dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="1cd41-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="1cd41-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="1cd41-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="1cd41-167">Thuộc tính này xác định trường khi các giá trị mà ứng dụng cung cấp được lưu trở lại cơ sở dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="1cd41-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="1cd41-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1cd41-168">isEditable (NoYes)</span></span>

<span data-ttu-id="1cd41-169">Đặt thuộc tính này thành **Có** để chỉ định rằng người dùng có thể chỉnh sửa trường trong phần mục nhập bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="1cd41-170">Đặt thuộc tính thành **Không** để biến trường thành dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="1cd41-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="1cd41-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1cd41-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="1cd41-172">Đặt thuộc tính này thành **Có** để chỉ định rằng đây là trường bắt buộc trong phần mục nhập bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="1cd41-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="1cd41-173">label (str)</span></span>

<span data-ttu-id="1cd41-174">Thuộc tính này chỉ định nhãn được hiển thị bên cạnh trường trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="1cd41-175">stringOptions (Danh sách chuỗi)</span><span class="sxs-lookup"><span data-stu-id="1cd41-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="1cd41-176">Thuộc tính này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Chuỗi**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="1cd41-177">Nếu **stringOptions** được đặt, thì các giá trị chuỗi có thể chọn thông qua nút tùy chọn (nút radio) sẽ được chỉ định bằng các chuỗi trong danh sách.</span><span class="sxs-lookup"><span data-stu-id="1cd41-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="1cd41-178">Nếu không có chuỗi nào được cung cấp, thì người dùng sẽ có thể nhập văn bản tự do trong trường chuỗi (xem "Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu" ở phần sau của chủ đề này).</span><span class="sxs-lookup"><span data-stu-id="1cd41-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="1cd41-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="1cd41-179">stringLength (int)</span></span>

<span data-ttu-id="1cd41-180">Thuộc tính này chỉ định độ dài tối đa cho một trường chuỗi.</span><span class="sxs-lookup"><span data-stu-id="1cd41-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="1cd41-181">Mục này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Chuỗi**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="1cd41-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="1cd41-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="1cd41-183">Thuộc tính này chỉ định số chữ số thập phân được hiển thị cho một trường thực.</span><span class="sxs-lookup"><span data-stu-id="1cd41-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="1cd41-184">Mục này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Thực**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="1cd41-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="1cd41-185">orderSequence (int)</span></span>

<span data-ttu-id="1cd41-186">Thuộc tính này kiểm soát thứ tự hiển thị các trường tùy chỉnh trong ứng dụng khi có nhiều trường tùy chỉnh được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="1cd41-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="1cd41-187">Trường có số thấp hơn sẽ được hiển thị trước.</span><span class="sxs-lookup"><span data-stu-id="1cd41-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="1cd41-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="1cd41-188">booleanValue (boolean)</span></span>

<span data-ttu-id="1cd41-189">Đối với các trường thuộc loại **Boolean**, thuộc tính này chuyển giá trị Boolean của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="1cd41-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="1cd41-190">guidValue (guid)</span></span>

<span data-ttu-id="1cd41-191">Đối với các trường thuộc loại **GUID**, thuộc tính này chuyển giá trị mã định danh duy nhất toàn cầu (GUID) của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="1cd41-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="1cd41-192">int64Value (int64)</span></span>

<span data-ttu-id="1cd41-193">Đối với các trường thuộc loại **Int64**, thuộc tính này chuyển giá trị int64 của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="1cd41-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="1cd41-194">intValue (int)</span></span>

<span data-ttu-id="1cd41-195">Đối với các trường thuộc loại **Int**, thuộc tính này chuyển giá trị int của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="1cd41-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="1cd41-196">realValue (real)</span></span>

<span data-ttu-id="1cd41-197">Đối với các trường thuộc loại **Thực**, thuộc tính này chuyển giá trị thực của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="1cd41-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="1cd41-198">stringValue (str)</span></span>

<span data-ttu-id="1cd41-199">Đối với các trường thuộc loại **Chuỗi**, thuộc tính này chuyển giá trị chuỗi của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="1cd41-200">Mục này cũng được sử dụng cho các trường thuộc loại **Thực** được định dạng làm tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="1cd41-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="1cd41-201">Đối với các trường đó, thuộc tính được dùng để chuyển mã tiền tệ đến ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="1cd41-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="1cd41-202">dateValue (date)</span></span>

<span data-ttu-id="1cd41-203">Đối với các trường thuộc loại **Ngày**, thuộc tính này chuyển giá trị ngày của trường giữa máy chủ và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1cd41-204">Hiển thị và lưu trường tùy chỉnh trong phần mục nhập bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="1cd41-205">Dưới đây là ảnh chụp màn hình tạo mục nhập bảng chấm công trên ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="1cd41-206">Trong hình có các trường sẵn dùng và một trường tùy chỉnh ở phần "Mục nhập thời gian" gọi là "Chuỗi thử nghiệm", với giá trị enum đặt sẵn là "Tùy chọn thứ hai".</span><span class="sxs-lookup"><span data-stu-id="1cd41-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Trường tùy chỉnh chuỗi thử nghiệm trong ứng dụng](media/timesheet-entry.jpg)



<span data-ttu-id="1cd41-208">Dưới đây là ảnh chụp màn hình người dùng chọn một trong các tùy chọn enum có sẵn cho trường tùy chỉnh "Chuỗi thử nghiệm" trên ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="1cd41-209">Hai tùy chọn "Tùy chọn đầu tiên" và "Tùy chọn thứ hai" được hiển thị dưới dạng nút radio.</span><span class="sxs-lookup"><span data-stu-id="1cd41-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="1cd41-210">Tùy chọn thứ hai hiện được chọn.</span><span class="sxs-lookup"><span data-stu-id="1cd41-210">The second option is currently selected.</span></span>

![Các nút tùy chọn (nút radio) cho trường tùy chỉnh Chuỗi thử nghiệm](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1cd41-212">Mở rộng bảng TSTimesheetLine để bảng có trường tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="1cd41-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="1cd41-213">Trong các kịch bản điển hình, có thể dữ liệu cho trường tùy chỉnh trong phần mục nhập bảng chấm công sẽ được lưu vào bảng TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="1cd41-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="1cd41-214">Tuy nhiên, các bảng khác có thể được sử dụng nếu dữ liệu có thể được truy xuất dựa trên bản ghi TSTimesheetTrans được cung cấp, hoặc nếu không có ngữ cảnh bản ghi cụ thể (ví dụ: nếu trường được đặt là chỉ đọc trong tham số dự án).</span><span class="sxs-lookup"><span data-stu-id="1cd41-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1cd41-215">Lưu ý rằng trường tùy chỉnh không nhất thiết phải có bất kỳ bản ghi cơ sở dữ liệu hỗ trợ nào.</span><span class="sxs-lookup"><span data-stu-id="1cd41-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1cd41-216">Chúng có thể được tạo động dựa trên logic X++.</span><span class="sxs-lookup"><span data-stu-id="1cd41-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1cd41-217">Phương pháp tiếp cận này có thể hữu ích trong các kịch bản chỉ đọc (xem phần "Sử dụng chuỗi lệnh trên lớp TSTimesheetDetails, phương pháp buildCustomFieldListForHeader để điền chi tiết bảng chấm công" để biết ví dụ về các giá trị trường tùy chỉnh được tạo động).</span><span class="sxs-lookup"><span data-stu-id="1cd41-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="1cd41-218">Dưới đây là ảnh chụp màn hình Cây đối tượng ứng dụng trên Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1cd41-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="1cd41-219">Ảnh hiển thị phần mở rộng bảng TSTimesheetLine với trường TestLineString được thêm vào làm trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="1cd41-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Chuỗi dòng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1cd41-221">Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldList của lớp TSTimesheetSettings để hiển thị trường trong phần mục nhập bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="1cd41-222">Mã này kiểm soát giá trị thiết đặt hiển thị cho trường trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1cd41-223">Chẳng hạn, nó kiểm soát loại trường, nhãn, liệu trường đó có phải là bắt buộc hay không và trường xuất hiện ở phần nào.</span><span class="sxs-lookup"><span data-stu-id="1cd41-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1cd41-224">Ví dụ sau đây cho thấy một trường chuỗi trên các mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="1cd41-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="1cd41-225">Trường này có hai tùy chọn, **Lựa chọn đầu tiên** và **Lựa chọn thứ hai**, có sẵn thông qua các nút tùy chọn (nút radio).</span><span class="sxs-lookup"><span data-stu-id="1cd41-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="1cd41-226">Trường trong ứng dụng được liên kết với trường **TestLineString** đã thêm vào bảng TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="1cd41-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="1cd41-227">Ghi lại cách sử dụng phương pháp **TSTimesheetCustomField::newFromMetatdata()** để rút gọn quá trình khởi tạo thuộc tính trường tùy chỉnh: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** và **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="1cd41-228">Bạn cũng có thể thiết lập thủ công các tham số này tùy thích.</span><span class="sxs-lookup"><span data-stu-id="1cd41-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="1cd41-229">Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldListForEntry của lớp TSTimesheetEntry để nhập giá trị vào mục nhập bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="1cd41-230">Phương pháp **buildCustomFieldListForEntry** được sử dụng để nhập giá trị trên các dòng của bảng chấm công đã lưu trong ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="1cd41-231">Phương pháp này sử dụng bản ghi TSTimesheetTrans làm tham số.</span><span class="sxs-lookup"><span data-stu-id="1cd41-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="1cd41-232">Các trường trong bản ghi đó có thể được sử dụng để điền giá trị trường tùy chỉnh trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="1cd41-233">Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu</span><span class="sxs-lookup"><span data-stu-id="1cd41-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="1cd41-234">Để lưu trường tùy chỉnh trở lại cơ sở dữ liệu theo cách sử dụng thông thường, bạn phải mở rộng nhiều phương pháp:</span><span class="sxs-lookup"><span data-stu-id="1cd41-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="1cd41-235">Phương pháp **timesheetLineNeedsUpdating** được sử dụng để xác định xem có phải bản ghi dòng được người dùng thay đổi trong ứng dụng nên cần được lưu vào cơ sở dữ liệu hay không.</span><span class="sxs-lookup"><span data-stu-id="1cd41-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="1cd41-236">Nếu hiệu suất không phải là mối quan tâm, thì phương pháp này có thể được rút gọn để luôn trả về **đúng**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="1cd41-237">Các phương pháp **populateTimesheetLineFromEntryDuringCreate** và **populateTimesheetLineFromEntryDuringUpdate** có thể được mở rộng để chúng nhập giá trị từ bản ghi hợp đồng dữ liệu TSTimesheetEntry được cung cấp vào bản ghi cơ sở dữ liệu TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="1cd41-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="1cd41-238">Trong ví dụ sau, hãy lưu ý cách ánh xạ giữa trường cơ sở dữ liệu và trường nhập được thực hiện thủ công thông qua mã X++.</span><span class="sxs-lookup"><span data-stu-id="1cd41-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="1cd41-239">Phương pháp **populateTimesheetWeekFromEntry** cũng có thể được mở rộng nếu trường tùy chỉnh ánh xạ tới đối tượng **TSTimesheetEntry** phải ghi lại vào bảng cơ sở dữ liệu TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="1cd41-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="1cd41-240">Ví dụ sau đây lưu giá trị **firstOption** hoặc **secondOption** mà người dùng lựa chọn vào cơ sở dữ liệu dưới dạng giá trị chuỗi thô.</span><span class="sxs-lookup"><span data-stu-id="1cd41-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="1cd41-241">Nếu trường của cơ sở dữ liệu thuộc loại **Enum**, thì các giá trị đó có thể được ánh xạ thủ công với một giá trị enum rồi được lưu vào một trường enum trên bảng cơ sở dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="1cd41-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="1cd41-242">Hiển thị trường tùy chỉnh trong phần thông tin cơ bản về bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="1cd41-243">Dưới đây là ảnh chụp màn hình người dùng xem bảng chấm công trên ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="1cd41-244">Nút "Thêm thông tin" được chọn ở góc trên bên phải để hiển thị tùy chọn "Xem thêm chi tiết".</span><span class="sxs-lookup"><span data-stu-id="1cd41-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Lệnh xem thêm chi tiết](media/show-more.png)

<span data-ttu-id="1cd41-246">Dưới đây là ảnh chụp màn hình hiển thị phần "Thêm" của bảng chấm công trên ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="1cd41-247">Một trường tùy chỉnh gọi là "Tỷ lệ thời gian làm việc trong bảng chấm công này (trường tùy chỉnh được tính toán)" đã được thêm vào phần thông tin cơ bản về bảng chấm công.</span><span class="sxs-lookup"><span data-stu-id="1cd41-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="1cd41-248">Giá trị chỉ đọc "0,667" được đặt trên trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="1cd41-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Phần Thêm](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1cd41-250">Mở rộng bảng TSTimesheetTable để bảng có trường tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="1cd41-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="1cd41-251">Trong các kịch bản điển hình, có thể dữ liệu cho trường tùy chỉnh trong phần thông tin cơ bản sẽ được lấy từ bảng TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="1cd41-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="1cd41-252">Tuy nhiên, các bảng khác có thể được sử dụng nếu dữ liệu có thể được truy xuất dựa trên bản ghi TSTimesheetTable được cung cấp, hoặc nếu không có ngữ cảnh bản ghi cụ thể (ví dụ: nếu trường được đặt là chỉ đọc trong tham số dự án).</span><span class="sxs-lookup"><span data-stu-id="1cd41-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1cd41-253">Lưu ý rằng trường tùy chỉnh không nhất thiết phải có bất kỳ bản ghi cơ sở dữ liệu hỗ trợ nào.</span><span class="sxs-lookup"><span data-stu-id="1cd41-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1cd41-254">Chúng có thể được tạo động dựa trên logic X++.</span><span class="sxs-lookup"><span data-stu-id="1cd41-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1cd41-255">Ví dụ sau đây minh họa phương pháp tiếp cận này.</span><span class="sxs-lookup"><span data-stu-id="1cd41-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="1cd41-256">Các trường trong phần thông tin cơ bản luôn ở dạng chỉ đọc trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="1cd41-257">Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldList của lớp TSTimesheetSettings để hiển thị trường trong phần thông tin cơ bản</span><span class="sxs-lookup"><span data-stu-id="1cd41-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="1cd41-258">Mã này kiểm soát giá trị thiết đặt hiển thị cho trường trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1cd41-259">Chẳng hạn, nó kiểm soát loại trường, nhãn, liệu trường đó có phải là bắt buộc hay không và trường xuất hiện ở phần nào.</span><span class="sxs-lookup"><span data-stu-id="1cd41-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1cd41-260">Ví dụ sau đây cho thấy một giá trị được tính toán ở phần thông tin cơ bản trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="1cd41-261">Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldListForHeader của lớp TSTimesheetDetails để điền chi tiết bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="1cd41-262">Phương pháp **buildCustomFieldListForHeader** được sử dụng để điền chi tiết thông tin cơ bản về bảng chấm công trong ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="1cd41-263">Phương pháp này sử dụng bản ghi TSTimesheetTable làm tham số.</span><span class="sxs-lookup"><span data-stu-id="1cd41-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="1cd41-264">Các trường trong bản ghi đó có thể được sử dụng để điền giá trị trường tùy chỉnh trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="1cd41-265">Ví dụ sau không đọc bất kỳ giá trị nào từ cơ sở dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="1cd41-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="1cd41-266">Thay vào đó, logic X++ được sử dụng để tạo ra một giá trị được tính toán rồi hiển thị trong ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="1cd41-267">Các cơ hội khả năng cấu hình/khả năng mở rộng khác</span><span class="sxs-lookup"><span data-stu-id="1cd41-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="1cd41-268">Thêm tùy chọn xác thực bổ sung cho ứng dụng</span><span class="sxs-lookup"><span data-stu-id="1cd41-268">Adding additional validation for the app</span></span>

<span data-ttu-id="1cd41-269">Logic hiện có cho chức năng bảng chấm công ở cấp cơ sở dữ liệu sẽ vẫn hoạt động như dự kiến.</span><span class="sxs-lookup"><span data-stu-id="1cd41-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="1cd41-270">Để làm gián đoạn việc hoàn thành hoạt động lưu hoặc gửi và hiển thị thông báo lỗi cụ thể, bạn có thể thêm **ném lỗi ("thông báo cho người dùng")** vào mã qua phần mở rộng chuỗi lệnh.</span><span class="sxs-lookup"><span data-stu-id="1cd41-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="1cd41-271">Dưới đây là ba ví dụ về các phương pháp có thể mở rộng hữu ích:</span><span class="sxs-lookup"><span data-stu-id="1cd41-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="1cd41-272">Nếu **validateWrite** trên bảng TSTimesheetLine trả về **sai** trong thao tác lưu cho một dòng bảng chấm công, thì thông báo lỗi sẽ được hiển thị trong ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="1cd41-273">Nếu **validateSubmit** trên bảng TSTimesheetTable trả về **sai** trong thao tác gửi bảng chấm công trong ứng dụng, thì thông báo lỗi sẽ được hiển thị cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="1cd41-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="1cd41-274">Logic điền giá trị vào các trường (ví dụ: **Thuộc tính dòng**) trong phương pháp **chèn** trên bảng TSTimesheetLine sẽ vẫn chạy.</span><span class="sxs-lookup"><span data-stu-id="1cd41-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="1cd41-275">Ẩn và đánh dấu các trường sẵn dùng là chỉ đọc thông qua cấu hình</span><span class="sxs-lookup"><span data-stu-id="1cd41-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="1cd41-276">Từ các tham số dự án, bạn có thể đặt các trường sẵn dùng thành chỉ đọc hoặc ẩn trong ứng dụng dành cho thiết bị di động.</span><span class="sxs-lookup"><span data-stu-id="1cd41-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="1cd41-277">Thiết lập các tùy chọn trong phần **Bảng chấm công trên thiết bị di động** trên tab **Bảng chấm công** của trang **Tham số quản lý dự án và số kế toán**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Tham số dự án](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="1cd41-279">Thay đổi các hoạt động có thể lựa chọn thông qua phần mở rộng</span><span class="sxs-lookup"><span data-stu-id="1cd41-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="1cd41-280">Các hoạt động có thể lựa chọn cho một dự án được điền thông qua phương pháp **getActivitiesForProject()** và **getActivityQuery()** ở lớp **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="1cd41-281">Bạn có thể sử dụng chuỗi lệnh để thay đổi hành vi này cho phù hợp với kịch bản kinh doanh của bạn đối với các hoạt động có thể lựa chọn cho một dự án cụ thể.</span><span class="sxs-lookup"><span data-stu-id="1cd41-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="1cd41-282">Nhập danh mục dự án mặc định vào các mục nhập bảng chấm công</span><span class="sxs-lookup"><span data-stu-id="1cd41-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="1cd41-283">Việc nhập danh mục dự án mặc định vào các mục nhập bảng chấm công xảy ra ở ba cấp độ.</span><span class="sxs-lookup"><span data-stu-id="1cd41-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="1cd41-284">Bạn có thể sử dụng chuỗi lệnh để mở rộng hành vi ở bất kỳ hoặc tất cả các cấp độ này để đạt được hành vi mong muốn.</span><span class="sxs-lookup"><span data-stu-id="1cd41-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="1cd41-285">Hệ thống phân cấp sau được sử dụng:</span><span class="sxs-lookup"><span data-stu-id="1cd41-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="1cd41-286">Ứng dụng cố gắng đặt danh mục mặc định từ tài nguyên dự án.</span><span class="sxs-lookup"><span data-stu-id="1cd41-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="1cd41-287">Danh mục mặc định này được đặt trong phương pháp **getCurrentUserResource** và **getDeleratingResourcesForCurrentUser** ở lớp **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="1cd41-288">Nếu danh mục mặc định không được cung cấp ở cấp tài nguyên dự án, thì ứng dụng sẽ cố gắng lấy dữ liệu này từ hoạt động dự án.</span><span class="sxs-lookup"><span data-stu-id="1cd41-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="1cd41-289">Danh mục mặc định này được đặt trong phương pháp **getActictivityForProject** ở lớp **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="1cd41-290">Nếu danh mục mặc định không được cung cấp ở cấp hoạt động, thì dữ liệu này sẽ được lấy từ tham số dự án.</span><span class="sxs-lookup"><span data-stu-id="1cd41-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="1cd41-291">Danh mục mặc định này được đặt trong phương pháp **getProjectDetailsbyRule** ở lớp **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="1cd41-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]