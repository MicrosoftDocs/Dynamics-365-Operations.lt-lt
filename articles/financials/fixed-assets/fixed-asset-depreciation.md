---
title: "Ilgalaikio turto nusidėvėjimas"
description: "Šiame straipsnyje apžvelgiamas ilgalaikio turto nusidėvėjimas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 536acd6b2c9f046c2459aec27a1e3b1b56fd5cc9
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="fe3e4-103">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="fe3e4-103">Fixed asset depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe3e4-104">Šiame straipsnyje apžvelgiamas ilgalaikio turto nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-104">This article provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="fe3e4-105">Nusidėvėjimas yra periodinė operacija, kuri paprastai balanso sąskaitoje sumažina ilgalaikio turto vertę. Ji pelno ir nuostolio sąskaitose užrašoma kaip išlaidos.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="fe3e4-106">Todėl pagrindinė sąskaita paprastai yra naudojama periodiniam nusidėvėjimui balanse kredituoti.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="fe3e4-107">Korespondentinė sąskaita yra sąskaitų plano pelno ir nuostolio dalies sąskaita.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="fe3e4-108">Nusidėvėjimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="fe3e4-108">Depreciation adjustment</span></span>
<span data-ttu-id="fe3e4-109">Paprastai užregistruotos nusidėvėjimo operacijos taisymas yra registruojamas kaip nusidėvėjimo koregavimas.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="fe3e4-110">Todėl pagrindinė sąskaita ir korespondentinė sąskaita yra nustatomos kaip nusidėvėjimo sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="fe3e4-111">Nusidėvėjimo koregavimas gali būti teigiama arba neigiama suma, bet pagrindinės sąskaitos (kaip balanso sąskaitos) ir korespondentinės sąskaitos (paprastai kaip pelno ir nuostolio sąskaitos) funkcija yra tokia pati.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="fe3e4-112">Visiškas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="fe3e4-112">Extraordinary depreciation</span></span>
<span data-ttu-id="fe3e4-113">Visiškas nusidėvėjimas veikia taip, kaip pagrindinis nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="fe3e4-114">Todėl pagrindinė sąskaita yra naudojama nusidėvėjimo sumai balanse kredituoti ir ilgalaikio turto vertei sumažinti.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="fe3e4-115">Korespondentinė sąskaita yra pelno ir nuostolio sąskaita, kurioje apskaičiuotas ataskaitinio laikotarpio nusidėvėjimas nustatomas kaip išlaidos.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="fe3e4-116">Visiškas nusidėvėjimas veikia nepriklausomai nuo pagrindinio nusidėvėjimo.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="fe3e4-117">Jei visišką nusidėvėjimą naudosite kaip atskirą operacijos tipą, galėsite registruoti visišką nusidėvėjimą atskirai nuo pagrindinio nusidėvėjimo.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="fe3e4-118">Specialioji nusidėvėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="fe3e4-118">Special depreciation allowance</span></span>
<span data-ttu-id="fe3e4-119">Norėdami įtraukti visiško nusidėvėjimo sumas per pirmuosius metus, kai turtas atiduodamas eksploatuoti ir nusidėvi, galite naudoti specialiąją nusidėvėjimo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="fe3e4-120">Specialiosios nusidėvėjimo nuolaidos turi būti visada apskaičiuojamos pirmiau nei visi kiti nusidėvėjimo skaičiavimai.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="fe3e4-121">Kadangi specialiosios nusidėvėjimo nuolaidos dažnai yra nežinomos, kol nepraeina tam tikras ilgalaikio turto dėvėjimo laikas, geriausia šį nusidėvėjimo tipą naudoti su knyga, kuri DK neregistruojama.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="fe3e4-122">Galite naudoti periodinę funkciją Panaikinti operacijas, kurios neužregistruotos DK, norėdami naikinti šių knygų praeities operacijas.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="fe3e4-123">Tada galite naikinti ilgalaikio turto knygos nusidėvėjimo retrospektyvą, registruoti specialiąją nusidėvėjimo nuolaidą, kai ji žinoma, ir tada registruoti likusias metų nusidėvėjimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="fe3e4-124">Galite kurti neribotą specialiosios nusidėvėjimo nuolaidos įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="fe3e4-125">Kai priskirsite tuos įrašus turto grupės knygai, jie bus taikomi turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="fe3e4-126">Specialioji nusidėvėjimo nuolaida įvedama procentais arba fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="fe3e4-127">Kai užregistruosite nusidėvėjimo pasiūlymus, knygoje specialiosios nusidėvėjimo nuolaidos operacijos bus registruojamos atskirai nei nusidėvėjimo operacijos.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="fe3e4-128"> Nusidėvėjimo kalendoriai</span><span class="sxs-lookup"><span data-stu-id="fe3e4-128">Depreciation calendars</span></span>
<span data-ttu-id="fe3e4-129">Kiekviena knyga turi kalendorių, kuris naudojamas nustatant ilgalaikio turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="fe3e4-130">Pagal numatytuosius parametrus, jei nenurodote knygos kalendoriaus, knyga naudos DK finansinį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="fe3e4-131">Turite pasirinkti knygos finansinį kalendorių, kai susijusiame knygos nusidėvėjimo šablone yra naudojami finansiniai nusidėvėjimo metai.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="fe3e4-132">Bendrai naudojamus kalendorius galite kurti DK puslapyje **Finansiniai kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="fe3e4-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="fe3e4-133">Norėdami daugiau informacijos žr. [Nusidėvėjimo metodai ir konvencijos](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="fe3e4-133">For more informations, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



