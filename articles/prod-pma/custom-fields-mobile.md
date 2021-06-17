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
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Triển khai trường tùy chỉnh cho ứng dụng Microsoft Dynamics 365 Project Timesheet dành cho thiết bị di động trên iOS và Android

[!include [banner](../includes/banner.md)]

Chủ đề này cung cấp các mẫu hình phổ biến để sử dụng tiện ích mở rộng để triển khai trường tùy chỉnh. Các chủ đề sau được đề cập:

- Các loại dữ liệu khác nhau mà khuôn khổ trường tùy chỉnh hỗ trợ
- Cách hiển thị trường chỉ đọc hoặc trường có thể chỉnh sửa trên các mục nhập trong bảng chấm công và lưu giá trị do người dùng cung cấp trở lại cơ sở dữ liệu
- Cách hiển thị trường chỉ đọc trong phần thông tin cơ bản về bảng chấm công
- Cách tích hợp logic nghiệp vụ tùy chỉnh khác để nhập giá trị mặc định vào các trường và thực hiện xác thực bổ sung

## <a name="audience"></a>Đối tượng

Chủ đề này được biên soạn cho các nhà phát triển tích hợp trường tùy chỉnh của họ vào ứng dụng Microsoft Dynamics 365 Project Timesheet dành cho thiết bị di động trên Apple iOS và Google Android. Chúng tôi giả định là người đọc đã quen thuộc với chức năng phát triển X++ và bảng chấm công dự án.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Hợp đồng dữ liệu – lớp TSTimesheetCustomField X++

Lớp **TSTimesheetCustomField** là lớp hợp đồng dữ liệu X++ đại diện cho thông tin về trường tùy chỉnh cho chức năng bảng chấm công. Danh sách các đối tượng trường tùy chỉnh được chuyển trên cả hợp đồng dữ liệu TSTimesheetDetails và hợp đồng dữ liệu TSTimesheetEntry để hiển thị các trường tùy chỉnh trong ứng dụng dành cho thiết bị di động.

- **TSTimesheetDetails** – Hợp đồng thông tin cơ bản về bảng chấm công.
- **TSTimesheetEntry** – Hợp đồng giao dịch trong bảng chấm công. Các nhóm đối tượng này có cùng thông tin dự án và giá trị **timesheetLineRecId** sẽ tạo thành một dòng.

### <a name="fieldbasetype-types"></a>fieldBaseType (Loại)

Thuộc tính **FieldBaseType** trên đối tượng **TsTimesheetCustom** xác định loại trường sẽ xuất hiện trong ứng dụng. Các giá trị **Loại** sau được hỗ trợ.

| Giá trị loại | Loại              | Ghi chú |
|-------------|-------------------|-------|
| 0           | Chuỗi (và Enum) | Trường này xuất hiện dưới dạng trường văn bản. |
| 1           | Integer           | Giá trị được hiển thị dưới dạng số không có chữ số thập phân. |
| 2           | Thực              | Giá trị được hiển thị dưới dạng số có chữ số thập phân.<p>Để hiển thị giá trị thực dưới dạng tiền tệ trong ứng dụng, hãy sử dụng thuộc tính **fieldExisededType**. Bạn có thể dùng thuộc tính **numberOfDecimals** để đặt số chữ số thập phân được hiển thị.</p> |
| 3           | Ngày              | Định dạng ngày được xác định theo mục thiết đặt **Ngày, giờ và định dạng số** của người dùng, giá trị đó được chỉ định ở phần **Tùy chọn ngôn ngữ và quốc gia/khu vực** trong **Tùy chọn người dùng**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Nếu thuộc tính **stringOptions** không được cung cấp trên đối tượng **TSTimesheetCustomField**, thì người dùng sẽ được cung cấp một trường văn bản tự do.

    Thuộc tính **stringLength** có thể được sử dụng để thiết lập độ dài chuỗi tối đa mà người dùng có thể nhập.

- Nếu thuộc tính **stringOptions** được cung cấp trên đối tượng **TSTimesheetCustomField**, thì các phần tử danh sách đó là những giá trị duy nhất mà người dùng có thể chọn bằng các nút tùy chọn (nút radio).

    Trong trường hợp này, trường chuỗi có thể đóng vai trò như một giá trị enum để người dùng nhập. Để lưu giá trị vào cơ sở dữ liệu dưới dạng enum, hãy ánh xạ thủ công giá trị chuỗi trở lại giá trị enum trước khi bạn lưu vào cơ sở dữ liệu bằng chuỗi lệnh (hãy xem ví dụ trong "Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu" ở phần sau của chủ đề này).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Bạn có thể sử dụng thuộc tính này để định dạng giá trị thực dưới dạng tiền tệ. Phương pháp này chỉ có thể áp dụng khi giá trị **fieldBaseType** là **Thực**.

- **TSCustomFieldExtendedType:None** – Không có định dạng nào được áp dụng.
- **TSCustomFieldExtendedType::Currency** – Định dạng giá trị dưới dạng tiền tệ.

    Khi tùy chọn định dạng tiền tệ đang hoạt động, trường **stringValue** có thể được sử dụng để chuyển mã tiền tệ sẽ được hiển thị trong ứng dụng. Giá trị này là giá trị chỉ đọc.

    Trường **realValue** chứa số tiền sẽ được lưu vào cơ sở dữ liệu.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Bạn có thể sử dụng thuộc tính này để chỉ định nơi hiển thị trường tùy chỉnh trong ứng dụng.

- **TSCustomFieldSection::Header** – Trường sẽ xuất hiện ở phần **Xem thêm chi tiết** trong ứng dụng. Các trường này luôn là chỉ đọc.
- **TSCustomFieldSection::Line** – Trường sẽ xuất hiện sau tất cả các trường dòng sẵn dùng trên các mục nhập bảng chấm công. Các trường này có thể là dạng chỉnh sửa được hoặc chỉ đọc.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Thuộc tính này xác định trường khi các giá trị mà ứng dụng cung cấp được lưu trở lại cơ sở dữ liệu.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Thuộc tính này xác định trường khi các giá trị mà ứng dụng cung cấp được lưu trở lại cơ sở dữ liệu.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Đặt thuộc tính này thành **Có** để chỉ định rằng người dùng có thể chỉnh sửa trường trong phần mục nhập bảng chấm công. Đặt thuộc tính thành **Không** để biến trường thành dạng chỉ đọc.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Đặt thuộc tính này thành **Có** để chỉ định rằng đây là trường bắt buộc trong phần mục nhập bảng chấm công.

### <a name="label-str"></a>label (str)

Thuộc tính này chỉ định nhãn được hiển thị bên cạnh trường trong ứng dụng.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Danh sách chuỗi)

Thuộc tính này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Chuỗi**. Nếu **stringOptions** được đặt, thì các giá trị chuỗi có thể chọn thông qua nút tùy chọn (nút radio) sẽ được chỉ định bằng các chuỗi trong danh sách. Nếu không có chuỗi nào được cung cấp, thì người dùng sẽ có thể nhập văn bản tự do trong trường chuỗi (xem "Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu" ở phần sau của chủ đề này).

### <a name="stringlength-int"></a>stringLength (int)

Thuộc tính này chỉ định độ dài tối đa cho một trường chuỗi. Mục này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Chuỗi**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Thuộc tính này chỉ định số chữ số thập phân được hiển thị cho một trường thực. Mục này chỉ áp dụng được khi **fieldBaseType** được đặt thành **Thực**.

### <a name="ordersequence-int"></a>orderSequence (int)

Thuộc tính này kiểm soát thứ tự hiển thị các trường tùy chỉnh trong ứng dụng khi có nhiều trường tùy chỉnh được chỉ định. Trường có số thấp hơn sẽ được hiển thị trước.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Đối với các trường thuộc loại **Boolean**, thuộc tính này chuyển giá trị Boolean của trường giữa máy chủ và ứng dụng.

### <a name="guidvalue-guid"></a>guidValue (guid)

Đối với các trường thuộc loại **GUID**, thuộc tính này chuyển giá trị mã định danh duy nhất toàn cầu (GUID) của trường giữa máy chủ và ứng dụng.

### <a name="int64value-int64"></a>int64Value (int64)

Đối với các trường thuộc loại **Int64**, thuộc tính này chuyển giá trị int64 của trường giữa máy chủ và ứng dụng.

### <a name="intvalue-int"></a>intValue (int)

Đối với các trường thuộc loại **Int**, thuộc tính này chuyển giá trị int của trường giữa máy chủ và ứng dụng.

### <a name="realvalue-real"></a>realValue (real)

Đối với các trường thuộc loại **Thực**, thuộc tính này chuyển giá trị thực của trường giữa máy chủ và ứng dụng.

### <a name="stringvalue-str"></a>stringValue (str)

Đối với các trường thuộc loại **Chuỗi**, thuộc tính này chuyển giá trị chuỗi của trường giữa máy chủ và ứng dụng. Mục này cũng được sử dụng cho các trường thuộc loại **Thực** được định dạng làm tiền tệ. Đối với các trường đó, thuộc tính được dùng để chuyển mã tiền tệ đến ứng dụng.

### <a name="datevalue-date"></a>dateValue (date)

Đối với các trường thuộc loại **Ngày**, thuộc tính này chuyển giá trị ngày của trường giữa máy chủ và ứng dụng.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Hiển thị và lưu trường tùy chỉnh trong phần mục nhập bảng chấm công

Dưới đây là ảnh chụp màn hình tạo mục nhập bảng chấm công trên ứng dụng dành cho thiết bị di động. Trong hình có các trường sẵn dùng và một trường tùy chỉnh ở phần "Mục nhập thời gian" gọi là "Chuỗi thử nghiệm", với giá trị enum đặt sẵn là "Tùy chọn thứ hai".

![Trường tùy chỉnh chuỗi thử nghiệm trong ứng dụng](media/timesheet-entry.jpg)



Dưới đây là ảnh chụp màn hình người dùng chọn một trong các tùy chọn enum có sẵn cho trường tùy chỉnh "Chuỗi thử nghiệm" trên ứng dụng dành cho thiết bị di động.  Hai tùy chọn "Tùy chọn đầu tiên" và "Tùy chọn thứ hai" được hiển thị dưới dạng nút radio. Tùy chọn thứ hai hiện được chọn.

![Các nút tùy chọn (nút radio) cho trường tùy chỉnh Chuỗi thử nghiệm](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Mở rộng bảng TSTimesheetLine để bảng có trường tùy chỉnh

Trong các kịch bản điển hình, có thể dữ liệu cho trường tùy chỉnh trong phần mục nhập bảng chấm công sẽ được lưu vào bảng TSTimesheetLine. Tuy nhiên, các bảng khác có thể được sử dụng nếu dữ liệu có thể được truy xuất dựa trên bản ghi TSTimesheetTrans được cung cấp, hoặc nếu không có ngữ cảnh bản ghi cụ thể (ví dụ: nếu trường được đặt là chỉ đọc trong tham số dự án).

Lưu ý rằng trường tùy chỉnh không nhất thiết phải có bất kỳ bản ghi cơ sở dữ liệu hỗ trợ nào. Chúng có thể được tạo động dựa trên logic X++. Phương pháp tiếp cận này có thể hữu ích trong các kịch bản chỉ đọc (xem phần "Sử dụng chuỗi lệnh trên lớp TSTimesheetDetails, phương pháp buildCustomFieldListForHeader để điền chi tiết bảng chấm công" để biết ví dụ về các giá trị trường tùy chỉnh được tạo động).

Dưới đây là ảnh chụp màn hình Cây đối tượng ứng dụng trên Visual Studio. Ảnh hiển thị phần mở rộng bảng TSTimesheetLine với trường TestLineString được thêm vào làm trường tùy chỉnh.

![Chuỗi dòng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldList của lớp TSTimesheetSettings để hiển thị trường trong phần mục nhập bảng chấm công

Mã này kiểm soát giá trị thiết đặt hiển thị cho trường trong ứng dụng. Chẳng hạn, nó kiểm soát loại trường, nhãn, liệu trường đó có phải là bắt buộc hay không và trường xuất hiện ở phần nào.

Ví dụ sau đây cho thấy một trường chuỗi trên các mục nhập thời gian. Trường này có hai tùy chọn, **Lựa chọn đầu tiên** và **Lựa chọn thứ hai**, có sẵn thông qua các nút tùy chọn (nút radio). Trường trong ứng dụng được liên kết với trường **TestLineString** đã thêm vào bảng TSTimesheetLine.

Ghi lại cách sử dụng phương pháp **TSTimesheetCustomField::newFromMetatdata()** để rút gọn quá trình khởi tạo thuộc tính trường tùy chỉnh: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** và **numberOfDecimals**. Bạn cũng có thể thiết lập thủ công các tham số này tùy thích.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldListForEntry của lớp TSTimesheetEntry để nhập giá trị vào mục nhập bảng chấm công

Phương pháp **buildCustomFieldListForEntry** được sử dụng để nhập giá trị trên các dòng của bảng chấm công đã lưu trong ứng dụng dành cho thiết bị di động. Phương pháp này sử dụng bản ghi TSTimesheetTrans làm tham số. Các trường trong bản ghi đó có thể được sử dụng để điền giá trị trường tùy chỉnh trong ứng dụng.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Sử dụng chuỗi lệnh trên lớp TSTimesheetEntryService để lưu mục nhập bảng chấm công từ ứng dụng trở lại cơ sở dữ liệu

Để lưu trường tùy chỉnh trở lại cơ sở dữ liệu theo cách sử dụng thông thường, bạn phải mở rộng nhiều phương pháp:

- Phương pháp **timesheetLineNeedsUpdating** được sử dụng để xác định xem có phải bản ghi dòng được người dùng thay đổi trong ứng dụng nên cần được lưu vào cơ sở dữ liệu hay không. Nếu hiệu suất không phải là mối quan tâm, thì phương pháp này có thể được rút gọn để luôn trả về **đúng**.
- Các phương pháp **populateTimesheetLineFromEntryDuringCreate** và **populateTimesheetLineFromEntryDuringUpdate** có thể được mở rộng để chúng nhập giá trị từ bản ghi hợp đồng dữ liệu TSTimesheetEntry được cung cấp vào bản ghi cơ sở dữ liệu TSTimesheetLine. Trong ví dụ sau, hãy lưu ý cách ánh xạ giữa trường cơ sở dữ liệu và trường nhập được thực hiện thủ công thông qua mã X++.
- Phương pháp **populateTimesheetWeekFromEntry** cũng có thể được mở rộng nếu trường tùy chỉnh ánh xạ tới đối tượng **TSTimesheetEntry** phải ghi lại vào bảng cơ sở dữ liệu TSTimesheetLineweek.

> [!NOTE]
> Ví dụ sau đây lưu giá trị **firstOption** hoặc **secondOption** mà người dùng lựa chọn vào cơ sở dữ liệu dưới dạng giá trị chuỗi thô. Nếu trường của cơ sở dữ liệu thuộc loại **Enum**, thì các giá trị đó có thể được ánh xạ thủ công với một giá trị enum rồi được lưu vào một trường enum trên bảng cơ sở dữ liệu.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Hiển thị trường tùy chỉnh trong phần thông tin cơ bản về bảng chấm công

Dưới đây là ảnh chụp màn hình người dùng xem bảng chấm công trên ứng dụng dành cho thiết bị di động. Nút "Thêm thông tin" được chọn ở góc trên bên phải để hiển thị tùy chọn "Xem thêm chi tiết".  

![Lệnh xem thêm chi tiết](media/show-more.png)

Dưới đây là ảnh chụp màn hình hiển thị phần "Thêm" của bảng chấm công trên ứng dụng dành cho thiết bị di động. Một trường tùy chỉnh gọi là "Tỷ lệ thời gian làm việc trong bảng chấm công này (trường tùy chỉnh được tính toán)" đã được thêm vào phần thông tin cơ bản về bảng chấm công. Giá trị chỉ đọc "0,667" được đặt trên trường tùy chỉnh.

![Phần Thêm](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Mở rộng bảng TSTimesheetTable để bảng có trường tùy chỉnh

Trong các kịch bản điển hình, có thể dữ liệu cho trường tùy chỉnh trong phần thông tin cơ bản sẽ được lấy từ bảng TSTimesheetHeader. Tuy nhiên, các bảng khác có thể được sử dụng nếu dữ liệu có thể được truy xuất dựa trên bản ghi TSTimesheetTable được cung cấp, hoặc nếu không có ngữ cảnh bản ghi cụ thể (ví dụ: nếu trường được đặt là chỉ đọc trong tham số dự án).

Lưu ý rằng trường tùy chỉnh không nhất thiết phải có bất kỳ bản ghi cơ sở dữ liệu hỗ trợ nào. Chúng có thể được tạo động dựa trên logic X++. Ví dụ sau đây minh họa phương pháp tiếp cận này.

Các trường trong phần thông tin cơ bản luôn ở dạng chỉ đọc trong ứng dụng.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldList của lớp TSTimesheetSettings để hiển thị trường trong phần thông tin cơ bản

Mã này kiểm soát giá trị thiết đặt hiển thị cho trường trong ứng dụng. Chẳng hạn, nó kiểm soát loại trường, nhãn, liệu trường đó có phải là bắt buộc hay không và trường xuất hiện ở phần nào.

Ví dụ sau đây cho thấy một giá trị được tính toán ở phần thông tin cơ bản trong ứng dụng.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Sử dụng chuỗi lệnh trên phương pháp buildCustomFieldListForHeader của lớp TSTimesheetDetails để điền chi tiết bảng chấm công

Phương pháp **buildCustomFieldListForHeader** được sử dụng để điền chi tiết thông tin cơ bản về bảng chấm công trong ứng dụng dành cho thiết bị di động. Phương pháp này sử dụng bản ghi TSTimesheetTable làm tham số. Các trường trong bản ghi đó có thể được sử dụng để điền giá trị trường tùy chỉnh trong ứng dụng. Ví dụ sau không đọc bất kỳ giá trị nào từ cơ sở dữ liệu. Thay vào đó, logic X++ được sử dụng để tạo ra một giá trị được tính toán rồi hiển thị trong ứng dụng.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Các cơ hội khả năng cấu hình/khả năng mở rộng khác

### <a name="adding-additional-validation-for-the-app"></a>Thêm tùy chọn xác thực bổ sung cho ứng dụng

Logic hiện có cho chức năng bảng chấm công ở cấp cơ sở dữ liệu sẽ vẫn hoạt động như dự kiến. Để làm gián đoạn việc hoàn thành hoạt động lưu hoặc gửi và hiển thị thông báo lỗi cụ thể, bạn có thể thêm **ném lỗi ("thông báo cho người dùng")** vào mã qua phần mở rộng chuỗi lệnh. Dưới đây là ba ví dụ về các phương pháp có thể mở rộng hữu ích:

- Nếu **validateWrite** trên bảng TSTimesheetLine trả về **sai** trong thao tác lưu cho một dòng bảng chấm công, thì thông báo lỗi sẽ được hiển thị trong ứng dụng dành cho thiết bị di động.
- Nếu **validateSubmit** trên bảng TSTimesheetTable trả về **sai** trong thao tác gửi bảng chấm công trong ứng dụng, thì thông báo lỗi sẽ được hiển thị cho người dùng.
- Logic điền giá trị vào các trường (ví dụ: **Thuộc tính dòng**) trong phương pháp **chèn** trên bảng TSTimesheetLine sẽ vẫn chạy.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ẩn và đánh dấu các trường sẵn dùng là chỉ đọc thông qua cấu hình

Từ các tham số dự án, bạn có thể đặt các trường sẵn dùng thành chỉ đọc hoặc ẩn trong ứng dụng dành cho thiết bị di động. Thiết lập các tùy chọn trong phần **Bảng chấm công trên thiết bị di động** trên tab **Bảng chấm công** của trang **Tham số quản lý dự án và số kế toán**.

![Tham số dự án](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Thay đổi các hoạt động có thể lựa chọn thông qua phần mở rộng

Các hoạt động có thể lựa chọn cho một dự án được điền thông qua phương pháp **getActivitiesForProject()** và **getActivityQuery()** ở lớp **TsTimesheetProjectService**. Bạn có thể sử dụng chuỗi lệnh để thay đổi hành vi này cho phù hợp với kịch bản kinh doanh của bạn đối với các hoạt động có thể lựa chọn cho một dự án cụ thể.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Nhập danh mục dự án mặc định vào các mục nhập bảng chấm công

Việc nhập danh mục dự án mặc định vào các mục nhập bảng chấm công xảy ra ở ba cấp độ. Bạn có thể sử dụng chuỗi lệnh để mở rộng hành vi ở bất kỳ hoặc tất cả các cấp độ này để đạt được hành vi mong muốn. Hệ thống phân cấp sau được sử dụng:

1. Ứng dụng cố gắng đặt danh mục mặc định từ tài nguyên dự án. Danh mục mặc định này được đặt trong phương pháp **getCurrentUserResource** và **getDeleratingResourcesForCurrentUser** ở lớp **TSTimesheetSettingsService**.
2. Nếu danh mục mặc định không được cung cấp ở cấp tài nguyên dự án, thì ứng dụng sẽ cố gắng lấy dữ liệu này từ hoạt động dự án. Danh mục mặc định này được đặt trong phương pháp **getActictivityForProject** ở lớp **TSTimesheetProjectService**.
3. Nếu danh mục mặc định không được cung cấp ở cấp hoạt động, thì dữ liệu này sẽ được lấy từ tham số dự án. Danh mục mặc định này được đặt trong phương pháp **getProjectDetailsbyRule** ở lớp **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]