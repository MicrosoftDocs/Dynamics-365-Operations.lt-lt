--- 
title: "Perkelti ilgalaikį turtą"
description: "Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b193cf6fbed810f0d5234514573d0f5c23c7b2c8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="d59f1-103">Perkelti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="d59f1-103">Transfer a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d59f1-104">Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="d59f1-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="d59f1-105">Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="d59f1-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d59f1-106">Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="d59f1-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d59f1-107">Sąraše raskite ir pasirinkite perkeltiną ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="d59f1-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="d59f1-108">Veiksmų srityje spustelėkite Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="d59f1-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="d59f1-109">Spustelėkite Perkelti ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="d59f1-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="d59f1-110">Lauke Perkėlimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d59f1-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="d59f1-111">Įveskite perkėlimą apibūdinančių komentarų.</span><span class="sxs-lookup"><span data-stu-id="d59f1-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="d59f1-112">Šiame sąraše rodomos visos ilgalaikio turto knygos.</span><span class="sxs-lookup"><span data-stu-id="d59f1-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="d59f1-113">Pažymėkite knygas, kurias norite perkelti į naują finansinių dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="d59f1-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="d59f1-114">Šiame sąraše rodomos pasirinktos knygos esamos finansinių dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="d59f1-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="d59f1-115">Pasirinkite, kurią pasirinktos ilgalaikio turto knygos finansinę dimensiją norite atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="d59f1-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="d59f1-116">Lauke Finansinė dimensija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="d59f1-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="d59f1-117">Tinkamai nustatykite kitas finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d59f1-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="d59f1-118">Įvykus perkėlimui, pasikeičia visos finansinių dimensijų reikšmės, nesvarbu, ar reikšmė buvo įvesta, ar palikta tuščia.</span><span class="sxs-lookup"><span data-stu-id="d59f1-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="d59f1-119">Pavyzdžiui, jei įvedėte VersloVienetas reikšmę, o finansines dimensijas IšlaidųCentras ir Skyrius palikote tuščias.</span><span class="sxs-lookup"><span data-stu-id="d59f1-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="d59f1-120">Jei jūsų sąskaitos struktūra leidžia reikšmes IšlaidųCentras ir Skyrius palikti tuščias, po perkėlimo kiekviena VersloVienetas vertinimo modelio reikšmė būtų nauja, o reikšmės IšlaidųCentras ir Skyrius – tuščios.</span><span class="sxs-lookup"><span data-stu-id="d59f1-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="d59f1-121">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="d59f1-121">Click Update.</span></span>
    * <span data-ttu-id="d59f1-122">Prieš baigdami perkėlimą, turite galimybę pakeitimus peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="d59f1-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="d59f1-123">Prieš perkeldami ilgalaikio turto knygas, peržiūrėkite rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d59f1-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="d59f1-124">Spustelėkite Perkelti.</span><span class="sxs-lookup"><span data-stu-id="d59f1-124">Click Transfer.</span></span>


