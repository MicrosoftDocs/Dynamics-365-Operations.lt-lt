---
title: Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį
description: Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9587d39801ad39649aa5fa3ff682cdeab411516e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838804"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="ecf69-103">Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį</span><span class="sxs-lookup"><span data-stu-id="ecf69-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecf69-104">Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui.</span><span class="sxs-lookup"><span data-stu-id="ecf69-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="ecf69-105">Šis nuosavybės pakeitimas atliekamas kuriant ir registruojant atsargų nuosavybės pakeitimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="ecf69-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="ecf69-106">Nuosavybės pakeitimo žurnalo eilutes galima kurti neautomatiniu būdu arba, kaip parodyta šiame įraše, pagal esamą gamybos poreikį.</span><span class="sxs-lookup"><span data-stu-id="ecf69-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="ecf69-107">Paprastai šią užduotį atlieka darbo laiko prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="ecf69-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="ecf69-108">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="ecf69-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="ecf69-109">Jei naudojate savo duomenis, įsitikinkite, kad tenkinamos šios sąlygos: nustatytas atsargų nuosavybės pakeitimo žurnalo pavadinimas, tiekėjui priklausiančios turimos prekės fiziškai įrašytos ir yra viena arba daugiau medžiagos gamybos užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="ecf69-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="ecf69-110">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="ecf69-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="ecf69-111">Atsargų nuosavybės žurnalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ecf69-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="ecf69-112">Eikite į Atsargų valdymas > Žurnalo įrašai > Prekės > Atsargų nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="ecf69-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="ecf69-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ecf69-113">Click New.</span></span>
    * <span data-ttu-id="ecf69-114">Atsargų nuosavybės pakeitimo žurnalas naudojamas norint keisti konsignacijos atsargų savininką iš tiekėjo į dabartinį juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="ecf69-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="ecf69-115">Šis nuosavybės pakeitimas atliekamas išleidžiant turimas atsargas, kurios priklauso tiekėjui, ir tada gaunant tas atsargas dabartiniame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="ecf69-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="ecf69-116">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ecf69-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="ecf69-117">Galite pasirinkti tik atsargų žurnalų pavadinimus, kurių žurnalo tipas yra Nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="ecf69-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="ecf69-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ecf69-118">Click OK.</span></span>
5. <span data-ttu-id="ecf69-119">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="ecf69-119">Click Functions.</span></span>
6. <span data-ttu-id="ecf69-120">Spustelėkite Kurti žurnalo eilutes iš gamybos užsakymų.</span><span class="sxs-lookup"><span data-stu-id="ecf69-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="ecf69-121">Galite pradėti nuosavybės pakeitimo procesą, pateikdami užklausą dėl visų gamybos eilučių, kuriose yra žaliavų sunaudojimo poreikis.</span><span class="sxs-lookup"><span data-stu-id="ecf69-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="ecf69-122">Lauke Įtrauktinos atsargų išdavimo būsenos pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ecf69-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="ecf69-123">Ši parinktis leidžia filtruoti pagal atsargų operacijų išdavimo būseną.</span><span class="sxs-lookup"><span data-stu-id="ecf69-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="ecf69-124">Pavyzdžiui, galite kurti žurnalo eilutes, skirtas atsargoms, kurių būsena yra Paimta arba Rezervuota faktiškai.</span><span class="sxs-lookup"><span data-stu-id="ecf69-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="ecf69-125">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="ecf69-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="ecf69-126">Šis skyrius suteikia galimybę taikyti papildomus filtrus.</span><span class="sxs-lookup"><span data-stu-id="ecf69-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="ecf69-127">Pavyzdžiui, galite pasirinkti konkrečią žaliavų datą.</span><span class="sxs-lookup"><span data-stu-id="ecf69-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="ecf69-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ecf69-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="ecf69-129">Atsargų nuosavybės pakeitimo žurnalo registravimas</span><span class="sxs-lookup"><span data-stu-id="ecf69-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="ecf69-130">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="ecf69-130">Click Post.</span></span>
    * <span data-ttu-id="ecf69-131">Kai žurnalas užregistruojamas, tiekėjui priklausančios atsargos yra išleidžiamos naudojant nuorodą Nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="ecf69-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="ecf69-132">Tada atsargos yra gaunamos kaip turimas kiekis naudojant atsargų operaciją, kuri yra atnaujinama pirkimo užsakymo gavimo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ecf69-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="ecf69-133">Atkreipkite dėmesį, kad kuriamos tik operacijos, susijusios su užregistruotu žurnalu.</span><span class="sxs-lookup"><span data-stu-id="ecf69-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="ecf69-134">Numatomų atsargų operacijos nekuriamos.</span><span class="sxs-lookup"><span data-stu-id="ecf69-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="ecf69-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ecf69-135">Click OK.</span></span>
3. <span data-ttu-id="ecf69-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ecf69-136">Close the page.</span></span>

