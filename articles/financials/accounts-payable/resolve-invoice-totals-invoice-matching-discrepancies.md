---
title: "Nesutapimų šalinimas gretinant SF bendrąsias sumas"
description: "Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48f7b8a7c1bb081b6cdc012ebe3668655b17f174
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="5450b-103">Nesutapimų šalinimas gretinant SF bendrąsias sumas</span><span class="sxs-lookup"><span data-stu-id="5450b-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5450b-104">Vienas iš SF gretinimo tikrinimo tipų – SF bendrųjų sumų gretinimas.</span><span class="sxs-lookup"><span data-stu-id="5450b-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="5450b-105">Norėdami nurodyti, kad sistemoje būtų gretinamos SF bendrosios sumos, puslapio **Mokėtinų sumų parametrai** skirtuke **SF tikrinimas** nustatykite parinkties **Gretinti SF bendrąsias sumas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5450b-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="5450b-106">Galite naudoti SF bendrųjų sumų gretinimo parinktį, kad užtikrintumėte, jog SF bendrosios sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu.</span><span class="sxs-lookup"><span data-stu-id="5450b-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="5450b-107">Puslapyje **SF bendrųjų sumų gretinimo informacija** palyginamos šešios bendrosios sumos.</span><span class="sxs-lookup"><span data-stu-id="5450b-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="5450b-108">Jei bet kuri bendroji suma nukrypsta nuo numatomos atitinkamos pirkimo užsakymo bendrosios sumos, vėliavėle pažymimas gretinimo nesutapimas.</span><span class="sxs-lookup"><span data-stu-id="5450b-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="5450b-109">Norėdami peržiūrėti SF, kurioje yra bendrųjų sumų gretinimo nesutapimų, darbo srityje **Tiekėjo SF įrašas** spustelėkite plytelę **Laukiančios SF**.</span><span class="sxs-lookup"><span data-stu-id="5450b-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="5450b-110">Tada veiksmų srities skirtuke **Peržiūra** spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="5450b-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="5450b-111">Aptikus gretinimo nesutapimus šalia SF sumos rodomos įspėjimo piktogramos.</span><span class="sxs-lookup"><span data-stu-id="5450b-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="5450b-112">Jei reikia daugiau informacijos apie bendrąsias sumas, galite peržiūrėti SF bendrųjų sumų gretinimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="5450b-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="5450b-113">Jei identifikavę nesutapimą manote, kad SF informacija yra neteisinga, kreipkitės į tiekėją.</span><span class="sxs-lookup"><span data-stu-id="5450b-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="5450b-114">Atsižvelgdami į galutinę sutartį su tiekėju galite atlikti kurį nors toliau nurodytą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="5450b-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="5450b-115">Patvirtinkite kainų skirtumą ir užregistruokite SF, kurioje yra gretinimo nesutapimų.</span><span class="sxs-lookup"><span data-stu-id="5450b-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="5450b-116">Sistemoje gali būti nustatytas patvirtinimo reikalavimas, kad būtų galima užregistruoti SF su gretinimo nesutapimais.</span><span class="sxs-lookup"><span data-stu-id="5450b-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="5450b-117">Tokiu atveju turite patvirtinti gretinimo nesutapimą ir galite įvesti patvirtinimo komentarą.</span><span class="sxs-lookup"><span data-stu-id="5450b-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="5450b-118">Tada galėsite pasirinkti SF registravimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="5450b-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="5450b-119">Peržiūrėkite SF sumą pagal numatomą sumą ir registruokite SF.</span><span class="sxs-lookup"><span data-stu-id="5450b-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="5450b-120">Iš tiekėjo reikalaukite viso kredito ir naujos pataisytos SF.</span><span class="sxs-lookup"><span data-stu-id="5450b-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="5450b-121">Daugiau informacijos žr. [Išnagrinėti arba pašalinti išimtis](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="5450b-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



