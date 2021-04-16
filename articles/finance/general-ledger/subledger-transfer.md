---
title: Papildomos knygos perkėlimas į didžiąją knygą
description: Šioje temoje aprašomos „Microsoft Dynamics 365 Finance” teikiamos galimybės, susijusios su papildomos knygos perkėlimo procesu didžiojoje knygoje.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d43b96176c51d12c35383da75bf65a1ad92f84c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815289"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="9f61e-103">Papildomos knygos perkėlimas į didžiąją knygą</span><span class="sxs-lookup"><span data-stu-id="9f61e-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f61e-104">Šioje temoje aprašomos „Microsoft Dynamics 365 Finance” teikiamos galimybės, susijusios su papildomos knygos žurnalo įrašų paketų perkėlimo taisyklėmis.</span><span class="sxs-lookup"><span data-stu-id="9f61e-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="9f61e-105">Versijoje 8.1 buvo atlikti pakeitimai, kad būtų leidžiama perkelti taisykles, pagal kurias nebenaudojama parinktis **Sinchroninis**.</span><span class="sxs-lookup"><span data-stu-id="9f61e-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="9f61e-106">Norėdami gauti daugiau informacijos, žr. [Pašalintos arba nerekomenduojamos „Finance and Operations” funkcijos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="9f61e-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="9f61e-107">Galimos toliau nurodytos papildomos knygos paketų perkėlimo parinktys.</span><span class="sxs-lookup"><span data-stu-id="9f61e-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="9f61e-108">Asinchroninė – pasirinkus šią parinktį, nedelsiant bus suplanuotas papildomos knygos apskaitos įrašų perkėlimas didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="9f61e-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="9f61e-109">Didžiosios knygos kvitas bus įrašytas iš karto, kai tik ištekliai galės laisvai apdoroti šią užklausą serveryje.</span><span class="sxs-lookup"><span data-stu-id="9f61e-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="9f61e-110">Planuojamas paketas – pasirinkus šią parinktį, bus įtraukti papildomos knygos apskaitos įrašai, persiunčiami į didžiosios knygos apdorojimo darbo grupę, kur įrašai bus apdorojami ta tvarka, kuria buvo gauti.</span><span class="sxs-lookup"><span data-stu-id="9f61e-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="9f61e-111">Didžiosios knygos kvitas bus įrašytas numatytu laiku, jei ištekliai galės laisvai apdoroti šią paketinę užduotį serveryje.</span><span class="sxs-lookup"><span data-stu-id="9f61e-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="9f61e-112">10.0.8 versijoje buvo atlikti patobulinimai, siekiant padidinti parinkties Asinchroninis efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="9f61e-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="9f61e-113">Ši funkcija aktyvinama funkcijos pavadinimu **Papildomos knygos perkėlimas į didžiosios knygos našumo optimizavimą**.</span><span class="sxs-lookup"><span data-stu-id="9f61e-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="9f61e-114">Ši funkcija pagerina duomenų perkėlimą iš papildomos knygos į didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="9f61e-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="9f61e-115">Tai leidžia vykdyti procesą efektyviau, sugrupuojant kartu mažesnes perkeltinas operacijas.</span><span class="sxs-lookup"><span data-stu-id="9f61e-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="9f61e-116">Tai leidžia efektyviau naudoti paketinio apdorojimo serverį.</span><span class="sxs-lookup"><span data-stu-id="9f61e-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="9f61e-117">Norint naudoti šią funkciją, reikia nustatyti, kad paketinio apdorojimo serveris būtų nustatytas, tinkle ir veiktų, kad veiktų asinchroninio perkėlimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="9f61e-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]