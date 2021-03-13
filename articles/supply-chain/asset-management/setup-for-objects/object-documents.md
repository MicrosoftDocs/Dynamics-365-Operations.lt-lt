---
title: Nustatyti dokumentą kaip
description: Šioje temoje pasakojama apie turto dokumentus, esančius modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8bcae99a96ccd83dc4543b1c56007a4263a19b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021684"
---
# <a name="asset-documents"></a><span data-ttu-id="3d679-103">Nustatyti dokumentą kaip</span><span class="sxs-lookup"><span data-stu-id="3d679-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3d679-104">Šioje temoje pasakojama apie turto dokumentus, esančius modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="3d679-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="3d679-105">Modulyje „Turto valdymas“ galite konfigūruoti dokumentus, kad jie būtų automatiškai siejami su užduoties tipais, turto gamintojais, turto tipais arba turtu.</span><span class="sxs-lookup"><span data-stu-id="3d679-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="3d679-106">Ši funkcija yra naudinga, kai išleidžiamos atnaujintos dokumentų versijos.</span><span class="sxs-lookup"><span data-stu-id="3d679-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="3d679-107">Tokiu atveju jums tereikia įtraukti atnaujintą dokumentą į standartinę vietą, kurią naudojate „Supply Chain Management“ dokumentams laikyti ir pridėti dokumentą prie turto dokumento įrašo, kurį buvote sukūrę.</span><span class="sxs-lookup"><span data-stu-id="3d679-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="3d679-108">Tada atnaujintą dokumentą galima pasiekti einant į meniu elementus **Visas turtas**, **Aktyvusis turtas**, **Mano aktyvusis turtas**, **Visi darbo užsakymai** ir **Aktyviosios darbo užsakymo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="3d679-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="3d679-109">Dokumentų pridėjimo prie turto dokumentų įrašo procesas naudoja standartinę dokumentų tvarkymo sistemą.</span><span class="sxs-lookup"><span data-stu-id="3d679-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="3d679-110">**1 pavyzdys:** Dokumente, susijusiame su užduoties tipu, gali būti aprašyta to darbo tipo procedūra.</span><span class="sxs-lookup"><span data-stu-id="3d679-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="3d679-111">**2 pavyzdys:** Dokumentas, susijęs su turto tipo, gamintojo ir modelio deriniu, gali būti standartinis pasirinkto turto gamintojo modelio vadovas.</span><span class="sxs-lookup"><span data-stu-id="3d679-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="3d679-112">Kurti turto dokumento ryšį</span><span class="sxs-lookup"><span data-stu-id="3d679-112">Create asset document relation</span></span>

1. <span data-ttu-id="3d679-113">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto dokumentai**.</span><span class="sxs-lookup"><span data-stu-id="3d679-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="3d679-114">Pasirinkite **Naujas**, kad sukurtumėte turto dokumento įrašą.</span><span class="sxs-lookup"><span data-stu-id="3d679-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="3d679-115">Pagal tai, kiek konkreti turi būti dokumento sąsaja pagal jūsų pageidavimus, atitinkamai pasirinkite viename ar keliuose iš šių laukų: **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Užduoties tipo kategorija**, **Užduoties tipas**, **Užduoties tipo variantas** ir **Užduoties poreikis**.</span><span class="sxs-lookup"><span data-stu-id="3d679-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="3d679-116">Parinktys, pasiekiamos laukuose **Užduoties tipo variantas** ir **Užduoties reikalavimas**, priklauso nuo žymėjimo lauke **Užduoties tipas**.</span><span class="sxs-lookup"><span data-stu-id="3d679-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d679-117">Sistema ieško dokumentų, kurie turėtų būti susieti su turtu arba darbo užsakymu, o modulis „Turto valdymas“ apdoroja visus turto dokumentų įrašus ir ieško galimų atitikčių.</span><span class="sxs-lookup"><span data-stu-id="3d679-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="3d679-118">Jis visada pirmiausiai tikrina konkrečiausius derinius.</span><span class="sxs-lookup"><span data-stu-id="3d679-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="3d679-119">Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Užduoties reikalavimas** atitikties.</span><span class="sxs-lookup"><span data-stu-id="3d679-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="3d679-120">Jei atitiktis nerasta, ieškoma lauko **Užduoties tipo variantas** atitikties.</span><span class="sxs-lookup"><span data-stu-id="3d679-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="3d679-121">Jei atitiktis nerasta, ieškoma lauko **Užduoties tipas** ir t. t.</span><span class="sxs-lookup"><span data-stu-id="3d679-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="3d679-122">Kaip matote pagal puslapio **Turto dokumentai** išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę.</span><span class="sxs-lookup"><span data-stu-id="3d679-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="3d679-123">Keletas dokumentų gali būti susieti su turtu arba darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="3d679-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="3d679-124">Prireikus galite redaguoti priežiūros prašymo arba darbo užsakymo aptarnavimo lygį.</span><span class="sxs-lookup"><span data-stu-id="3d679-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="3d679-125">Pasirinkite **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="3d679-125">Select **Attachments**.</span></span> <span data-ttu-id="3d679-126">Rodomas standartinis puslapis **Dokumentų tvarkymas**.</span><span class="sxs-lookup"><span data-stu-id="3d679-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="3d679-127">Nustatykite dokumentus arba pastabas, kurios turėtų būti pridėtos prie turto dokumento įrašo.</span><span class="sxs-lookup"><span data-stu-id="3d679-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="3d679-128">Kai pridėsite dokumentus, lauke **Priedai** bus rodomas su įrašu susijusių dokumentų skaičius.</span><span class="sxs-lookup"><span data-stu-id="3d679-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
