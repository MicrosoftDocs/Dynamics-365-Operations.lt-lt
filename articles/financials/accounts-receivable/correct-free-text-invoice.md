---
title: Laisvos formos SF taisymas
description: "Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a353db68c2223d62cd8e5048f0e953ed134c0803
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="7959e-103">Laisvos formos SF taisymas</span><span class="sxs-lookup"><span data-stu-id="7959e-103">Correct a free text invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7959e-104">Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF.</span><span class="sxs-lookup"><span data-stu-id="7959e-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="7959e-105">Norėdami ištaisyti jau užregistruotą laisvos formos SF, atidarykite užregistruotą laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="7959e-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="7959e-106">Puslapyje **SF** pasirinkite **Atšaukti** ir tada pasirinkite **Taisyti SF**.</span><span class="sxs-lookup"><span data-stu-id="7959e-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="7959e-107">Pasirinkite priežasties kodą, pridėkite komentarų ir pasirinkite naujos pataisytos SF datą.</span><span class="sxs-lookup"><span data-stu-id="7959e-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="7959e-108">Pataisytą SF galite modifikuoti ir užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="7959e-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="7959e-109">Kai registruojate pataisytą SF, kredito sumai, kuri lygi pradinei SF sumai, sukuriama atšaukiamoji SF.</span><span class="sxs-lookup"><span data-stu-id="7959e-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="7959e-110">Todėl kombinuotasis pradinės SF ir atšaukiamosios SF balansas yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="7959e-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="7959e-111">Atšaukiamoji SF sudengiama pagal pradinę SF.</span><span class="sxs-lookup"><span data-stu-id="7959e-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="7959e-112">Užregistravę pataisytą SF, turėsite toliau nurodytas tris SF.</span><span class="sxs-lookup"><span data-stu-id="7959e-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="7959e-113">**Pradinė SF** – SF, kuri apima informaciją, kurią taisote.</span><span class="sxs-lookup"><span data-stu-id="7959e-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="7959e-114">**Atšaukiamoji SF** – sistemos sugeneruota kredito SF, kuri sukurta norint atšaukti SF, kuri buvo paskiausiai pataisyta.</span><span class="sxs-lookup"><span data-stu-id="7959e-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="7959e-115">**Pataisyta SF** – SF, kurioje yra pataisyta SF informacija.</span><span class="sxs-lookup"><span data-stu-id="7959e-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="7959e-116">Atšaukiamąją ir pataisytą SF galite identifikuoti toliau nurodytais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="7959e-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="7959e-117">**Visų laisvos formos SF** puslapyje yra **Taisymo** stulpelis, kuriame galite matyti, kurios SF yra atšaukiamosios, o kurios – pataisytos.</span><span class="sxs-lookup"><span data-stu-id="7959e-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="7959e-118">Laisvos formos SF antraštėje rodoma būsena  **Atšaukiamoji SF \[SF numeris\]** arba **Pataisyta SF \[SF numeris\]**.</span><span class="sxs-lookup"><span data-stu-id="7959e-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="7959e-119">Ši funkcija prieinama tik jei pasirinktas konfigūracijos raktą **Laisvos formos SF taisymas**.</span><span class="sxs-lookup"><span data-stu-id="7959e-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>



