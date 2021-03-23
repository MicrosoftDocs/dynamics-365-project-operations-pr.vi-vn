---
title: Đặt cấu hình hoạt động kế toán cho dự án nội bộ
description: Chủ đề này cung cấp thông tin về cách thiết lập các hoạt động kế toán cho dự án nội bộ trong Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287624"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="3c90c-103">Đặt cấu hình hoạt động kế toán cho dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="3c90c-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="3c90c-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="3c90c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3c90c-105">Dự án nội bộ giúp cho các công ty theo dõi chi phí liên quan đến các hoạt động không được lập hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="3c90c-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="3c90c-106">Các dự án nội bộ có thể là:</span><span class="sxs-lookup"><span data-stu-id="3c90c-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="3c90c-107">Phát triển sản phẩm, chẳng hạn như ứng dụng dành cho thiết bị di động, và theo dõi chi phí liên quan đến việc phát triển.</span><span class="sxs-lookup"><span data-stu-id="3c90c-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="3c90c-108">Quản lý thời gian và chi phí trước khi bán hàng.</span><span class="sxs-lookup"><span data-stu-id="3c90c-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="3c90c-109">Sau này, dự án nội bộ trước khi bán hàng này có thể được chuyển đổi thành dự án có thể lập hóa đơn nếu bạn giành được báo giá.</span><span class="sxs-lookup"><span data-stu-id="3c90c-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="3c90c-110">Bất kỳ dự án nào không liên kết với một hợp đồng trong Dynamics 365 Project Operations đều được xem là nội bộ.</span><span class="sxs-lookup"><span data-stu-id="3c90c-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="3c90c-111">Hồ sơ doanh thu và chi phí dự án không được sử dụng để xác định các quy tắc kế toán cho dự án này.</span><span class="sxs-lookup"><span data-stu-id="3c90c-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="3c90c-112">Chi phí của dự án nội bộ luôn được đăng theo nguyên tắc lãi và lỗ.</span><span class="sxs-lookup"><span data-stu-id="3c90c-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="3c90c-113">Tài khoản sổ dùng cho các mục đăng được xác định trên trang **Thiết lập đăng sổ**.</span><span class="sxs-lookup"><span data-stu-id="3c90c-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="3c90c-114">Các giao dịch thời gian được đăng bằng cách ghi nợ vào tài khoản **Chi phí** và ghi có vào tài khoản **Phân bổ bảng lương**.</span><span class="sxs-lookup"><span data-stu-id="3c90c-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="3c90c-115">Các giao dịch chi phí được đăng bằng cách ghi nợ vào tài khoản **Chi phí** và ghi có vào tài khoản **Tài khoản bù trừ chi phí**.</span><span class="sxs-lookup"><span data-stu-id="3c90c-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="3c90c-116">Sau khi các giao dịch được đăng vào dự án, nếu dự án được liên kết với hợp đồng dự án, thì hệ thống sẽ đảo ngược tất cả các giao dịch đã tích lũy và tạo giao dịch có thể lập hóa đơn mới.</span><span class="sxs-lookup"><span data-stu-id="3c90c-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="3c90c-117">Giao dịch có thể lập hóa đơn tuân theo các quy tắc kế toán được xác định trong hồ sơ chi phí và doanh thu tương ứng của Dự án.</span><span class="sxs-lookup"><span data-stu-id="3c90c-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]