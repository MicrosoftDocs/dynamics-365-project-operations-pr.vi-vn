---
title: Gỡ cài đặt Dynamics 365 Project Operations
description: Chủ đề này cung cấp thông tin về cách gỡ cài đặt Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e2600c770477ad32cebb66f33a8ca31502a6da3d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575882"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Gỡ cài đặt Dynamics 365 Project Operations 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để gỡ cài đặt Dynamics 365 Project Operations, bạn phải được chỉ định vai trò Quản trị viên.

1. Chuyển tới **Thiết đặt** > **Giải pháp**.

    ![Trang Cài đặt.](./media/uninstall-proj-ops-solutions.png)
  
2. Loại bỏ các giải pháp theo đúng thứ tự mà chúng được liệt kê trong bảng sau. 

    | Bước | Tên giải pháp                                    | Ghi chú                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 2 | ProjectOperations_Anchor                           | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | Tệp 4 | Dynamics365ProjectOperationsDualWrite              | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 5 | ProjectService                                     | Không có ghi chú bổ sung.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Không có ghi chú bổ sung.                                                                         |
    | 7 | ProjectServiceCore                                 | Không có ghi chú bổ sung.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 9 | FieldServiceCommon                                 | Bắt buộc để ghi kép với Dynamics 365 Finance hoặc Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Bắt buộc để ghi kép với Dynamics 365 Finance hoặc Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Bắt buộc với Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 19 | Dynamics365Notes                                   | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 21 | DualWriteCore                                      | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 23 | Dynamics365AssetManagement                         | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 26 | HCMCommon                                          | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 28 | Bên                                              | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 29 | Dynamics365Company                                 | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 30 | CurrencyExchangeRates                              | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
    | 31 | AssetCommon                                        | Nếu không tìm thấy, hãy bỏ qua giải pháp này.                                                            |
