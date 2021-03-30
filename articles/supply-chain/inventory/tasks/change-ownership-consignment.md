---
title: Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį
description: Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 508226a3b5693b123af639cf6f130be07811c3c2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209520"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="10dda-103">Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį</span><span class="sxs-lookup"><span data-stu-id="10dda-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10dda-104">Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui.</span><span class="sxs-lookup"><span data-stu-id="10dda-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="10dda-105">Šis nuosavybės pakeitimas atliekamas kuriant ir registruojant atsargų nuosavybės pakeitimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="10dda-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="10dda-106">Nuosavybės pakeitimo žurnalo eilutes galima kurti neautomatiniu būdu arba, kaip parodyta šiame įraše, pagal esamą gamybos poreikį.</span><span class="sxs-lookup"><span data-stu-id="10dda-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="10dda-107">Paprastai šią užduotį atlieka darbo laiko prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="10dda-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="10dda-108">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="10dda-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="10dda-109">Jei naudojate savo duomenis, įsitikinkite, kad tenkinamos šios sąlygos: nustatytas atsargų nuosavybės pakeitimo žurnalo pavadinimas, tiekėjui priklausiančios turimos prekės fiziškai įrašytos ir yra viena arba daugiau medžiagos gamybos užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="10dda-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="10dda-110">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="10dda-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="10dda-111">Siunčiamų siuntų procesai ir automatinis nuosavybės žurnalo apdorojimas nepalaikomi.</span><span class="sxs-lookup"><span data-stu-id="10dda-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="10dda-112">Atsargų nuosavybės žurnalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="10dda-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="10dda-113">Eikite į Atsargų valdymas > Žurnalo įrašai > Prekės > Atsargų nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="10dda-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="10dda-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="10dda-114">Click New.</span></span>
    * <span data-ttu-id="10dda-115">Atsargų nuosavybės pakeitimo žurnalas naudojamas norint keisti konsignacijos atsargų savininką iš tiekėjo į dabartinį juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="10dda-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="10dda-116">Šis nuosavybės pakeitimas atliekamas išleidžiant turimas atsargas, kurios priklauso tiekėjui, ir tada gaunant tas atsargas dabartiniame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="10dda-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="10dda-117">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10dda-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="10dda-118">Galite pasirinkti tik atsargų žurnalų pavadinimus, kurių žurnalo tipas yra Nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="10dda-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="10dda-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="10dda-119">Click OK.</span></span>
5. <span data-ttu-id="10dda-120">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="10dda-120">Click Functions.</span></span>
6. <span data-ttu-id="10dda-121">Spustelėkite Kurti žurnalo eilutes iš gamybos užsakymų.</span><span class="sxs-lookup"><span data-stu-id="10dda-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="10dda-122">Galite pradėti nuosavybės pakeitimo procesą, pateikdami užklausą dėl visų gamybos eilučių, kuriose yra žaliavų sunaudojimo poreikis.</span><span class="sxs-lookup"><span data-stu-id="10dda-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="10dda-123">Lauke Įtrauktinos atsargų išdavimo būsenos pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="10dda-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="10dda-124">Ši parinktis leidžia filtruoti pagal atsargų operacijų išdavimo būseną.</span><span class="sxs-lookup"><span data-stu-id="10dda-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="10dda-125">Pavyzdžiui, galite kurti žurnalo eilutes, skirtas atsargoms, kurių būsena yra Paimta arba Rezervuota faktiškai.</span><span class="sxs-lookup"><span data-stu-id="10dda-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="10dda-126">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="10dda-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="10dda-127">Šis skyrius suteikia galimybę taikyti papildomus filtrus.</span><span class="sxs-lookup"><span data-stu-id="10dda-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="10dda-128">Pavyzdžiui, galite pasirinkti konkrečią žaliavų datą.</span><span class="sxs-lookup"><span data-stu-id="10dda-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="10dda-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="10dda-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="10dda-130">Atsargų nuosavybės pakeitimo žurnalo registravimas</span><span class="sxs-lookup"><span data-stu-id="10dda-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="10dda-131">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="10dda-131">Click Post.</span></span>
    * <span data-ttu-id="10dda-132">Kai žurnalas užregistruojamas, tiekėjui priklausančios atsargos yra išleidžiamos naudojant nuorodą Nuosavybės pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="10dda-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="10dda-133">Tada atsargos yra gaunamos kaip turimas kiekis naudojant atsargų operaciją, kuri yra atnaujinama pirkimo užsakymo gavimo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="10dda-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="10dda-134">Atkreipkite dėmesį, kad kuriamos tik operacijos, susijusios su užregistruotu žurnalu.</span><span class="sxs-lookup"><span data-stu-id="10dda-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="10dda-135">Numatomų atsargų operacijos nekuriamos.</span><span class="sxs-lookup"><span data-stu-id="10dda-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="10dda-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="10dda-136">Click OK.</span></span>
3. <span data-ttu-id="10dda-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="10dda-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]