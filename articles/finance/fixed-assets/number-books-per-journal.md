---
title: Vieno žurnalo knygų skaičius
description: Šioje temoje aprašomas ryšys tarp žurnalų ir turto knygų kuriant ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą vykdant paketinę užduotį. Galite nurodyti maksimalų knygų, įtrauktų į kiekvieną įsigijimą ir dėl nusidėvėjimo, skaičių.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f266e458802e65f0955ae8f8933f9bee2eca972
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256720"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="4148b-104">Vieno žurnalo knygų skaičius</span><span class="sxs-lookup"><span data-stu-id="4148b-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4148b-105">Šioje temoje aprašomas ryšys tarp žurnalų ir turto knygų kuriant ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą vykdant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="4148b-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="4148b-106">Galite nurodyti maksimalų visų pirkimo ir nusidėvėjimo knygų skaičių, naudojant laukus, esančius puslapio **Ilgalaikio turto parametrai** skirtuko **Bendra** skiltyje **Vieno žurnalo knygų skaičius** (**Ilgalaikis turtas \> Sąranka \> Ilgalaikio turto parametrai**).</span><span class="sxs-lookup"><span data-stu-id="4148b-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="4148b-107">Šie laukai leidžia paskirstyti turto knygų, skirtų pirkimo žurnalui ir nusidėvėjimo žurnalui, skaičių.</span><span class="sxs-lookup"><span data-stu-id="4148b-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="4148b-108">Įsigijimo pasiūlymo numatytoji vertė yra bent 10 000 knygų.</span><span class="sxs-lookup"><span data-stu-id="4148b-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="4148b-109">Nusidėvėjimo pasiūlymo numatytoji vertė yra bent 2000 knygų.</span><span class="sxs-lookup"><span data-stu-id="4148b-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="4148b-110">Pavyzdžiui, jei yra 4000 ilgalaikio turto ir dvi knygos yra susietos su kiekvienu turtu, viena knyga bus užregistruota dabartiniame sluoksnyje, o kita knyga bus užregistruota mokesčių sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="4148b-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="4148b-111">Jei įsigysite 4000 ilgalaikio turto vienetų per paketinį vykdymą, paketinė užduotis, kuri sukuria vieną ilgalaikio turto įsigijimo žurnalą, sudarys 4000 turto knygas.</span><span class="sxs-lookup"><span data-stu-id="4148b-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="4148b-112">Sukurtas žurnalas bus naudojamas, kol baigiama paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="4148b-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="4148b-113">Išvestinė knyga neįtraukta į didžiausią knygų, skirtų žurnalui, skaičių.</span><span class="sxs-lookup"><span data-stu-id="4148b-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="4148b-114">Norėdami vykdyti nusidėvėjimą tam pačiam įsigyto turto rinkiniui, galite naudoti paketinį apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="4148b-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="4148b-115">Pavyzdžiui, paketinė užduotis sukuria du nusidėvėjimo žurnalus, kurių kiekvienas susideda iš 2000 turto knygų.</span><span class="sxs-lookup"><span data-stu-id="4148b-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="4148b-116">Pirmajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 1 iki 2000.</span><span class="sxs-lookup"><span data-stu-id="4148b-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="4148b-117">Antrajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 2001 iki 4000.</span><span class="sxs-lookup"><span data-stu-id="4148b-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="4148b-118">Paketinio vykdymo užduotis neįtraukia uždarytų knygų.</span><span class="sxs-lookup"><span data-stu-id="4148b-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="4148b-119">Pavyzdžiui, atliekant nusidėvėjimo paketinę užduotį, uždaromos 10 iš pirmųjų 2000 knygų.</span><span class="sxs-lookup"><span data-stu-id="4148b-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="4148b-120">Tokiu atveju pirmajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 1 iki 2011.</span><span class="sxs-lookup"><span data-stu-id="4148b-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="4148b-121">Antrajame žurnale bus knygos, susietos su ilgalaikiu turtu, kuris numeruojamas nuo 2012 iki 4000.</span><span class="sxs-lookup"><span data-stu-id="4148b-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="4148b-122">Knygų skaičiaus limitas yra pritaikytas, jei tame pačiame žurnale nėra dubliuotų turto ID.</span><span class="sxs-lookup"><span data-stu-id="4148b-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="4148b-123">Tačiau, jei turto ID yra toks pats kaip knygos ID, galima viršyti žurnalo žurnalų skaičių, kad turto ID liktų tame pačiame žurnale.</span><span class="sxs-lookup"><span data-stu-id="4148b-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="4148b-124">Pavyzdžiui, yra 5001 ilgalaikio turto ID, trys knygos yra susietos su kiekvienu ilgalaikio turto ID, o kiekviena turto knyga užregistruojama tame pačiame registravimo lygmenyje.</span><span class="sxs-lookup"><span data-stu-id="4148b-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="4148b-125">Vykdote nebegaliojimą tris mėnesius iš eilės be santraukos.</span><span class="sxs-lookup"><span data-stu-id="4148b-125">You run depreciation for three consecutive months, without summarizing.</span></span>  <span data-ttu-id="4148b-126">Nusidėvėjimo žurnalas bus sukurtas naudojant paketines užduotis, o sistema sukurs septynis žurnalus, kuriuose yra 667 ilgalaikio turto ID ir trys knygos kiekvienam ilgalaikio turto ID.</span><span class="sxs-lookup"><span data-stu-id="4148b-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="4148b-127">Rezultatas bus 2001 knyga.</span><span class="sxs-lookup"><span data-stu-id="4148b-127">The result will be 2,001 books.</span></span> <span data-ttu-id="4148b-128">Todėl per tris mėnesius bus 6003 žurnalo eilutės, kad būtų išlaikyti tie patys turto ID tame pačiame žurnale.</span><span class="sxs-lookup"><span data-stu-id="4148b-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="4148b-129">Sistema taip pat sukurs po vieną žurnalą, kuriame yra 332 ilgalaikio turto ID ir trys knygos kiekvienam ilgalaikio turto identifikatoriui.</span><span class="sxs-lookup"><span data-stu-id="4148b-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="4148b-130">Per tris mėnesius bus 2988 eilutės.</span><span class="sxs-lookup"><span data-stu-id="4148b-130">In three months, there will be 2,988 lines.</span></span>

> [!Note] 
> <span data-ttu-id="4148b-131">Jei **Santrauko nebegaliojimo** parametras yra įjungtas jums kuriant nebegaliojimo pasiūlymą, tuomet vertė **Knygų skaičius žurnale - Nebegaliojimo pasiūlymas** laukelyje neturi jokio poveikio.</span><span class="sxs-lookup"><span data-stu-id="4148b-131">If the **Summarize depreciation** parameter is turned on when you're creating a depreciation proposal, then the value in the **Number of books per journal - Depreciation proposal** field has no effect.</span></span> <span data-ttu-id="4148b-132">Šiuo atveju, knygų skaičius žurnale yra 6000, o tai vidaus nustatytas apribojimas.</span><span class="sxs-lookup"><span data-stu-id="4148b-132">In this case number of books per journal is 6000, which is the internal defined limit.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]