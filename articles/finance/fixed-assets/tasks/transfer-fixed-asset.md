---
title: Perkelti ilgalaikį turtą
description: Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446005"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="ee7e9-103">Perkelti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="ee7e9-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee7e9-104">Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="ee7e9-105">Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="ee7e9-106">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="ee7e9-107">Sąraše raskite ir pasirinkite perkeltiną ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="ee7e9-108">Veiksmų srityje spustelėkite **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="ee7e9-109">Spustelėkite **Perkelti ilgalaikį turtą**.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="ee7e9-110">Lauke **Perkėlimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="ee7e9-111">Įveskite perkėlimą apibūdinančių komentarų.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="ee7e9-112">Šiame sąraše rodomos visos ilgalaikio turto knygos.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="ee7e9-113">Pažymėkite knygas, kurias norite perkelti į naują finansinių dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="ee7e9-114">Šiame sąraše rodomos pasirinktos knygos esamos finansinių dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="ee7e9-115">Pasirinkite, kurią pasirinktos ilgalaikio turto knygos finansinę dimensiją norite atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="ee7e9-116">Lauke **Finansinė dimensija** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="ee7e9-117">Tinkamai nustatykite kitas finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="ee7e9-118">Įvykus perkėlimui, pasikeičia visos finansinių dimensijų reikšmės, nesvarbu, ar reikšmė buvo įvesta, ar palikta tuščia.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="ee7e9-119">Pavyzdžiui, jei įvedėte VersloVienetas reikšmę, o finansines dimensijas IšlaidųCentras ir Skyrius palikote tuščias.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="ee7e9-120">Jei jūsų sąskaitos struktūra leidžia reikšmes IšlaidųCentras ir Skyrius palikti tuščias, po perkėlimo kiekviena VersloVienetas vertinimo modelio reikšmė būtų nauja, o reikšmės IšlaidųCentras ir Skyrius – tuščios.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="ee7e9-121">Spustelėkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-121">Click **Update**.</span></span>
    * <span data-ttu-id="ee7e9-122">Prieš baigdami perkėlimą, turite galimybę pakeitimus peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="ee7e9-123">Prieš perkeldami ilgalaikio turto knygas, peržiūrėkite rezultatus.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="ee7e9-124">Spustelėkite **Perkelti**.</span><span class="sxs-lookup"><span data-stu-id="ee7e9-124">Click **Transfer**.</span></span>

