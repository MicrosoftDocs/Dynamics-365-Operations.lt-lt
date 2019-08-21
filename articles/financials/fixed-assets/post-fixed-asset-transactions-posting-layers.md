---
title: Registruoti ilgalaikio turto operacijas registravimo sluoksniuose
description: Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab5adfdec259207898d25778e4e3bbbaebb452f1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840270"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="40798-103">Registruoti ilgalaikio turto operacijas registravimo sluoksniuose</span><span class="sxs-lookup"><span data-stu-id="40798-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40798-104">Šiame straipsnyje apžvelgiamos ilgalaikio turto operacijų registravimo sluoksnio funkcijos.</span><span class="sxs-lookup"><span data-stu-id="40798-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="40798-105">Ilgalaikio turto nusidėvėjimas skaičiuojamas įvairiais būdais ir siekiant įvairių tikslų.</span><span class="sxs-lookup"><span data-stu-id="40798-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="40798-106">Mokestiniais tikslais nusidėvėjimas apskaičiuojamas pagal tuo metu nustatytų mokesčių taisykles, kad prieš skaičiuojant mokesčius turtas nuvertėtų kaip galima daugiau. Ataskaitose fiksuojamas nusidėvėjimas apskaičiuojamas pagal apskaitos įstatymus ir standartus.</span><span class="sxs-lookup"><span data-stu-id="40798-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="40798-107">Įvairių tipų nusidėvėjimas apskaičiuojamas ir registruojamas atskirai skirtinguose registravimo sluoksniuose.</span><span class="sxs-lookup"><span data-stu-id="40798-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="40798-108">Kiekviena ilgalaikiam turtui priskirta knyga nustatoma konkrečiame registravimo sluoksnyje, turinčiame bendrą nusidėvėjimo tikslą.</span><span class="sxs-lookup"><span data-stu-id="40798-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="40798-109">Galima naudoti dešimt registravimo sluoksnių: Dabartinis, Operacijos, Mokestis ir septynis tipo Pasirinktinis sluoksnius.</span><span class="sxs-lookup"><span data-stu-id="40798-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="40798-110">Taip pat galite išjungti knygos registravimo DK funkciją, nustatydami lauką Registruoti DK į parinktį Ne.</span><span class="sxs-lookup"><span data-stu-id="40798-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="40798-111">Tada laukas Registravimo sluoksnis automatiškai nustatomas į parinktį Nėra.</span><span class="sxs-lookup"><span data-stu-id="40798-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="40798-112">Knygos, kurios neregistruojamos DK, paprastai naudojamos mokesčių registravimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="40798-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="40798-113">Tokiu būdu suteikiama daugiau lankstumo naikinant ankstesnes turto knygos operacijas, nes jos nebuvo perkeltos į DK.</span><span class="sxs-lookup"><span data-stu-id="40798-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="40798-114">Ilgalaikio turto žurnalai nustatomi naudojant puslapį Žurnalų pavadinimai, kurį galima atidaryti pasirinkus DK > Žurnalo nustatymas > Žurnalų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="40798-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="40798-115">Kiekvieną žurnalą, kuriame galima registruoti nusidėvėjimą, apibūdina jo pavadinimas, kuris gali būti priskirtas tik vienam registravimo sluoksniui.</span><span class="sxs-lookup"><span data-stu-id="40798-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="40798-116">Žurnalo registravimo sluoksnio keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="40798-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="40798-117">Šis apribojimas padeda užtikrinti, kad kiekvieno registravimo sluoksnio operacijos bus saugomos atskirai.</span><span class="sxs-lookup"><span data-stu-id="40798-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="40798-118">Kiekviename registravimo sluoksnyje turi būti sukurtas bent vienas žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="40798-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="40798-119">Jei naudojate knygas, kurios DK neregistruojamos, taip pat turite sukurti žurnalą, kuriame registravimo sluoksnis yra nustatytas į parinktį Nėra.</span><span class="sxs-lookup"><span data-stu-id="40798-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="40798-120">Puslapyje Ilgalaikio turto registravimo šablonai galite nustatyti DK sąskaitas, kuriose registruojamos ilgalaikio turto operacijos.</span><span class="sxs-lookup"><span data-stu-id="40798-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="40798-121">Kiekviename registravimo šablone turite pasirinkti reikiamą operacijos tipą bei knygą ir nurodyti DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="40798-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="40798-122">Nustatykite kiekvienos knygos, kuri bus registruojama DK, registravimo šablono įrašą.</span><span class="sxs-lookup"><span data-stu-id="40798-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="40798-123">Naudodami išvestines knygas, operacijas galite vienu metu registruoti skirtinguose registravimo sluoksniuose.</span><span class="sxs-lookup"><span data-stu-id="40798-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="40798-124">Pagrindinės knygos operacijas galite kurti žurnale, kuriame yra registravimo sluoksnis, atitinkantis knygos registravimo sluoksnį.</span><span class="sxs-lookup"><span data-stu-id="40798-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="40798-125">Išvestinės knygos operacijos registruojamos atitinkamuose registravimo sluoksniuose.</span><span class="sxs-lookup"><span data-stu-id="40798-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="40798-126">Norėdami gauti daugiau informacijos, žr. [Išvestinės knygos](derived-books.md) ir [Registravimas naudojant išvestines knygas](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="40798-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>



