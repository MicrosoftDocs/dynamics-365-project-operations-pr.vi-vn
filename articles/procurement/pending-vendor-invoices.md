---
title: Mua vật tư không tồn kho bằng hóa đơn của nhà cung cấp đang chờ xử lý
description: Chủ đề này giải thích cách ghi lại các hóa đơn của nhà cung cấp đang chờ xử lý.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880698"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="6dd60-103">Mua vật tư không tồn kho bằng hóa đơn của nhà cung cấp đang chờ xử lý</span><span class="sxs-lookup"><span data-stu-id="6dd60-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="6dd60-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="6dd60-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6dd60-105">Khi công ty mua vật tư không tồn kho cho một dự án, chi phí có thể được ghi nhận ngay lập tức đối với dự án.</span><span class="sxs-lookup"><span data-stu-id="6dd60-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="6dd60-106">Ví dụ, Contoso Robotics US đang thực hiện một dự án đổi mới thiết bị và cần giấy phép phần mềm.</span><span class="sxs-lookup"><span data-stu-id="6dd60-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="6dd60-107">Nhà cung cấp bên thứ ba sẽ cấp các giấy phép này.</span><span class="sxs-lookup"><span data-stu-id="6dd60-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="6dd60-108">Khi sử dụng Dynamics 365 Finance, nhân viên ghi chép khoản phải trả ghi lại tài liệu hóa đơn của nhà cung cấp đang chờ xử lý và chỉ định chi phí giấy phép trực tiếp vào dự án đổi mới thiết bị.</span><span class="sxs-lookup"><span data-stu-id="6dd60-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="6dd60-109">Trước khi bạn sử dụng chức năng được mô tả trong chủ đề này, hãy đánh giá và áp dụng các cấu hình cần thiết.</span><span class="sxs-lookup"><span data-stu-id="6dd60-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="6dd60-110">Để biết thêm thông tin, hãy xem [Kích hoạt vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="6dd60-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="6dd60-111">Đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án</span><span class="sxs-lookup"><span data-stu-id="6dd60-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="6dd60-112">Hóa đơn của nhà cung cấp đang chờ xử lý có thể được ghi lại trên trang **Hóa đơn của nhà cung cấp đang chờ xử lý** (**Khoản phải trả** > **Hóa đơn** > **Hóa đơn của nhà cung cấp đang chờ xử lý**).</span><span class="sxs-lookup"><span data-stu-id="6dd60-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="6dd60-113">Hoàn thành các bước sau để đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án:</span><span class="sxs-lookup"><span data-stu-id="6dd60-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="6dd60-114">Chuyển đến **Khoản phải trả** > **Hóa đơn** rồi chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="6dd60-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="6dd60-115">Trong trường **Tài khoản hóa đơn**, hãy chọn một nhà cung cấp và trong trường **Mã số**, nhập mã nhận dạng hóa đơn của nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="6dd60-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="6dd60-116">Thêm một dòng vào hóa đơn của nhà cung cấp và trong trường **Số sản phẩm**, chọn sản phẩm không tồn kho được mua từ nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="6dd60-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="6dd60-117">Không thể ghi các dòng hóa đơn của nhà cung cấp dựa trên danh mục mua sắm đối với dự án.</span><span class="sxs-lookup"><span data-stu-id="6dd60-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="6dd60-118">Thêm số lượng đã mua.</span><span class="sxs-lookup"><span data-stu-id="6dd60-118">Add the quantity purchased.</span></span> <span data-ttu-id="6dd60-119">Hệ thống sẽ điền đơn giá dựa trên cấu hình giá của sản phẩm không tồn kho.</span><span class="sxs-lookup"><span data-stu-id="6dd60-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="6dd60-120">Xác minh tổng số tiền và các chi tiết cần thiết khác trên dòng.</span><span class="sxs-lookup"><span data-stu-id="6dd60-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="6dd60-121">Trên chi tiết mô tả, trên tab **Dự án**, hãy chọn ID của dự án mà sản phẩm này sẽ được ghi vào.</span><span class="sxs-lookup"><span data-stu-id="6dd60-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="6dd60-122">Theo tùy chọn, hãy chọn số hoạt động và cập nhật danh mục dự án cũng như thuộc tính dòng.</span><span class="sxs-lookup"><span data-stu-id="6dd60-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="6dd60-123">Đăng hóa đơn của nhà cung cấp đang chờ xử lý.</span><span class="sxs-lookup"><span data-stu-id="6dd60-123">Post pending vendor invoice.</span></span> <span data-ttu-id="6dd60-124">Khi hóa đơn được đăng, hệ thống ghi lại:</span><span class="sxs-lookup"><span data-stu-id="6dd60-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="6dd60-125">Số dư của nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="6dd60-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="6dd60-126">Số tiền thuế bán hàng.</span><span class="sxs-lookup"><span data-stu-id="6dd60-126">The sales tax amount.</span></span>
    - <span data-ttu-id="6dd60-127">Chi phí đối với dự án được ghi nhận vào tài khoản tính hợp mua sắm.</span><span class="sxs-lookup"><span data-stu-id="6dd60-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="6dd60-128">Giao dịch thực tế của dự án tại Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6dd60-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="6dd60-129">Giao dịch này được tiếp tục xử lý bằng [Nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="6dd60-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="6dd60-130">Việc đăng nhật ký này sẽ chuyển số tiền từ tài khoản tích hợp mua sắm sang tài khoản chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="6dd60-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
