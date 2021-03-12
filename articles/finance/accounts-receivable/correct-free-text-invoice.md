---
title: Laisvos formos SF taisymas
description: Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3896a8574f7910ee09b360deb3ede10f061290bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991234"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="c1790-103">Laisvos formos SF taisymas</span><span class="sxs-lookup"><span data-stu-id="c1790-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1790-104">Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF.</span><span class="sxs-lookup"><span data-stu-id="c1790-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="c1790-105">Norėdami ištaisyti jau užregistruotą laisvos formos SF, atidarykite užregistruotą laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c1790-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="c1790-106">Puslapyje **SF** pasirinkite **Atšaukti** ir tada pasirinkite **Taisyti SF**.</span><span class="sxs-lookup"><span data-stu-id="c1790-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="c1790-107">Pasirinkite priežasties kodą, pridėkite komentarų ir pasirinkite naujos pataisytos SF datą.</span><span class="sxs-lookup"><span data-stu-id="c1790-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="c1790-108">Pataisytą SF galite modifikuoti ir užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="c1790-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="c1790-109">Kai registruojate pataisytą SF, kredito sumai, kuri lygi pradinei SF sumai, sukuriama atšaukiamoji SF.</span><span class="sxs-lookup"><span data-stu-id="c1790-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="c1790-110">Todėl kombinuotasis pradinės SF ir atšaukiamosios SF balansas yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="c1790-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="c1790-111">Atšaukiamoji SF sudengiama pagal pradinę SF.</span><span class="sxs-lookup"><span data-stu-id="c1790-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="c1790-112">Užregistravę pataisytą SF, turėsite toliau nurodytas tris SF.</span><span class="sxs-lookup"><span data-stu-id="c1790-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="c1790-113">**Pradinė SF** – SF, kuri apima informaciją, kurią taisote.</span><span class="sxs-lookup"><span data-stu-id="c1790-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="c1790-114">**Atšaukiamoji SF** – sistemos sugeneruota kredito SF, kuri sukurta norint atšaukti SF, kuri buvo paskiausiai pataisyta.</span><span class="sxs-lookup"><span data-stu-id="c1790-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="c1790-115">**Pataisyta SF** – SF, kurioje yra pataisyta SF informacija.</span><span class="sxs-lookup"><span data-stu-id="c1790-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="c1790-116">Atšaukiamąją ir pataisytą SF galite identifikuoti toliau nurodytais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="c1790-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="c1790-117">**Visų laisvos formos SF** puslapyje yra **Taisymo** stulpelis, kuriame galite matyti, kurios SF yra atšaukiamosios, o kurios – pataisytos.</span><span class="sxs-lookup"><span data-stu-id="c1790-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="c1790-118">Laisvos formos SF antraštėje rodoma būsena  **Atšaukiamoji SF \[SF numeris\]** arba **Pataisyta SF \[SF numeris\]**.</span><span class="sxs-lookup"><span data-stu-id="c1790-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="c1790-119">Ši funkcija prieinama tik jei pasirinktas konfigūracijos raktą **Laisvos formos SF taisymas**.</span><span class="sxs-lookup"><span data-stu-id="c1790-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="c1790-120">Daugiau informacijos apie tai, kaip įgalinti konfigūracijos raktus, rasite skyriuje Konfigūracijos raktų įjungimas (arba išjungimas), temoje [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c1790-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 



