---
title: Tiekėjo sąskaitos faktūros automatizavimo rezultatų peržiūra (peržiūros versija)
description: Šioje temoje paaiškinama, kaip peržiūrėti tiekėjo sąskaitų faktūrų, kurios yra įtrauktos į automatizuoto pateikimo į darbo eigą procesą, būseną.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969731"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="85b70-103">Tiekėjo SF automatizavimo rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="85b70-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85b70-104">Šioje temoje paaiškinama, kaip peržiūrėti tiekėjo sąskaitų faktūrų, kurios yra įtrauktos į automatizuoto pateikimo į darbo eigą procesą, būseną.</span><span class="sxs-lookup"><span data-stu-id="85b70-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="85b70-105">Saugoma kiekvienos importuotos tiekėjo sąskaitos automatizavimo retrospektyvos informacija.</span><span class="sxs-lookup"><span data-stu-id="85b70-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="85b70-106">Atsižvelgiant į automatizuotus verslo procesus, puslapyje **Laukiančios tiekėjo SF** rodomos **Automatizuoto kvito gretinimo būsena** ir **Automatizuoto pateikimo į darbo eigą būsena** vertės.</span><span class="sxs-lookup"><span data-stu-id="85b70-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="85b70-107">Galite peržiūrėti išsamią informaciją ir susidaryti planą, skirtą sąskaitų faktūrų, kurių automatizavimo veiksmas buvo nesėkmingas, apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="85b70-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="85b70-108">Tada, kai išspręsite problemą, galėsite tęsti importuotų sąskaitų faktūrų automatizuotą procesą.</span><span class="sxs-lookup"><span data-stu-id="85b70-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="85b70-109">Tam, kad galėtumėte redaguoti pateiktą sąskaitą faktūrą, turite sustabdyti automatizuotą apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="85b70-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="85b70-110">Jei sąskaita automatizuotame pateikimo į darbo eigos procese turi būti sustabdyta, nustatykite lauko **Įtraukti į automatizuotą apdorojimą**, esančio puslapyje **Tiekėjo sąskaitos faktūros** reikšmę **Ne**.</span><span class="sxs-lookup"><span data-stu-id="85b70-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="85b70-111">Tada automatizavimas nebus vykdomas, kol nenustatysite lauko **Įtraukti į automatizuotą apdorojimą** reikšmės **Taip**.</span><span class="sxs-lookup"><span data-stu-id="85b70-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="85b70-112">Sąskaitos faktūros tolesnis automatizavimas gali būti sustabdytas, jei ji dar nėra darbo eigos sistemoje ir nėra naudojama automatizuoto proceso.</span><span class="sxs-lookup"><span data-stu-id="85b70-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="85b70-113">Jei importuota sąskaita faktūra yra įtraukta į pateikimo į darbo eigą procesą, jos **Automatizavimo būsena** vertę galite matyti puslapyje **Tiekėjo sąskaitos faktūros**.</span><span class="sxs-lookup"><span data-stu-id="85b70-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="85b70-114">Skiriamos šios būsenos:</span><span class="sxs-lookup"><span data-stu-id="85b70-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="85b70-115">**Įtraukta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai**, veikia tinkamai, tačiau dar nebaigė darbo.</span><span class="sxs-lookup"><span data-stu-id="85b70-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="85b70-116">**Pristabdyta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai** buvo paleisti, tačiau ne mažiau nei vienas veiksmas buvo nesėkmingas.</span><span class="sxs-lookup"><span data-stu-id="85b70-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="85b70-117">Būsena **Pristabdyta** taip pat taikoma, jei nustatyta lauko **Įtraukti į automatizuotą apdorojimą** reikšmė yra **Ne**.</span><span class="sxs-lookup"><span data-stu-id="85b70-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="85b70-118">Klaidas galite peržiūrėti pasirinkę **Peržiūrėti naujausius rezultatus**.</span><span class="sxs-lookup"><span data-stu-id="85b70-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="85b70-119">**Darbo eigoje** – importuota sąskaita faktūra buvo pateikta darbo eigos sistemai naudojant automatizuotą pateikimo į darbo eigą procesą arba rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="85b70-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="85b70-120">**Darbo eiga baigta** – importuotos sąskaitos faktūros darbo eigos procesas yra baigtas.</span><span class="sxs-lookup"><span data-stu-id="85b70-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
