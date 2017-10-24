---
title: "Nesutapimų šalinimas gretinant SF bendrąsias sumas"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="71f43-102">Nesutapimų šalinimas gretinant SF bendrąsias sumas</span><span class="sxs-lookup"><span data-stu-id="71f43-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="71f43-103">Vienas iš SF gretinimo tikrinimo tipų – SF bendrųjų sumų gretinimas.</span><span class="sxs-lookup"><span data-stu-id="71f43-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="71f43-104">Norėdami nurodyti, kad sistemoje būtų gretinamos SF bendrosios sumos, puslapio **Mokėtinų sumų parametrai** skirtuke **SF tikrinimas** nustatykite parinkties **Gretinti SF bendrąsias sumas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="71f43-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="71f43-105">Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu.</span><span class="sxs-lookup"><span data-stu-id="71f43-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="71f43-106">Puslapyje **SF bendrųjų sumų gretinimo informacija** palyginamos šešios bendrosios sumos.</span><span class="sxs-lookup"><span data-stu-id="71f43-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="71f43-107">Jei bet kuri bendroji suma nukrypsta nuo numatomos atitinkamos pirkimo užsakymo bendrosios sumos, vėliavėle pažymimas gretinimo nesutapimas.</span><span class="sxs-lookup"><span data-stu-id="71f43-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="71f43-108">Norėdami peržiūrėti SF, kurioje yra bendrųjų sumų gretinimo nesutapimų, darbo srityje **Tiekėjo SF įrašas** spustelėkite plytelę **Laukiančios SF**.</span><span class="sxs-lookup"><span data-stu-id="71f43-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="71f43-109">Tada veiksmų srities skirtuke **Peržiūra** spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="71f43-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="71f43-110">Aptikus gretinimo nesutapimus šalia SF sumos rodomos įspėjimo piktogramos.</span><span class="sxs-lookup"><span data-stu-id="71f43-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="71f43-111">Jei reikia daugiau informacijos apie bendrąsias sumas, galite peržiūrėti SF bendrųjų sumų gretinimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="71f43-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="71f43-112">Jei identifikavę nesutapimą manote, kad SF informacija yra neteisinga, kreipkitės į tiekėją.</span><span class="sxs-lookup"><span data-stu-id="71f43-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="71f43-113">Atsižvelgdami į galutinę sutartį su tiekėju galite atlikti kurį nors toliau nurodytą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="71f43-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="71f43-114">Patvirtinkite kainų skirtumą ir užregistruokite SF, kurioje yra gretinimo nesutapimų.</span><span class="sxs-lookup"><span data-stu-id="71f43-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="71f43-115">Sistemoje gali būti nustatytas patvirtinimo reikalavimas, kad būtų galima užregistruoti SF su gretinimo nesutapimais.</span><span class="sxs-lookup"><span data-stu-id="71f43-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="71f43-116">Tokiu atveju turite patvirtinti gretinimo nesutapimą ir galite įvesti patvirtinimo komentarą.</span><span class="sxs-lookup"><span data-stu-id="71f43-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="71f43-117">Tada galėsite pasirinkti SF registravimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="71f43-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="71f43-118">Peržiūrėkite SF sumą pagal numatomą sumą ir registruokite SF.</span><span class="sxs-lookup"><span data-stu-id="71f43-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="71f43-119">Iš tiekėjo reikalaukite viso kredito ir naujos pataisytos SF.</span><span class="sxs-lookup"><span data-stu-id="71f43-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="71f43-120">Daugiau informacijos žr. [Išnagrinėti arba pašalinti išimtis](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="71f43-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



