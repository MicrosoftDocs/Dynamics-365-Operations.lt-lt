---
title: Atsargų skirstymo pagal terminus ataskaitos saugykla
description: Šioje temoje aprašomos funkcijos, leidžiančios vykdyti atsargų skirstymo pagal terminus ataskaitą ir įgalinti išvestis kaip formą ir diagramą.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005432"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="6151b-103">Atsargų skirstymo pagal terminus ataskaitos saugykla</span><span class="sxs-lookup"><span data-stu-id="6151b-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6151b-104">„Microsoft Dynamics 365 Supply Chain Management“ galite vykdyti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą ir įgalinti išvestį kaip formą ir diagramą.</span><span class="sxs-lookup"><span data-stu-id="6151b-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="6151b-105">Formoje stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į sukonfigūruotą maketą.</span><span class="sxs-lookup"><span data-stu-id="6151b-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="6151b-106">Diagramoje pateikiama vizualinė peržiūra, kuri palaiko filtravimą ir leidžia detalizuoti informaciją.</span><span class="sxs-lookup"><span data-stu-id="6151b-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="6151b-107">Be to, duomenų subjektas pavadinimu **Atsargų skirstymas pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą, kad būtų galima naudoti, pavyzdžiui, „Microsoft Excel“ failo arba PDF failo formatą.</span><span class="sxs-lookup"><span data-stu-id="6151b-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="6151b-108">Šis **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitos vykdymo metodas naudingas tais atvejais, kai išvestyje yra daug eilučių.</span><span class="sxs-lookup"><span data-stu-id="6151b-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="6151b-109">Pavyzdžiui, išvestyje yra daug eilučių, jei yra 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai, o jūs prašote atsargų skirstymo pagal terminus pagal prekę, teritoriją ir sandėlį.</span><span class="sxs-lookup"><span data-stu-id="6151b-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="6151b-110">Atsargų vertės saugyklos ataskaitos funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="6151b-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="6151b-111">Kad galėtumėte naudoti šią funkciją, turite ją įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="6151b-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="6151b-112">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įgalinti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="6151b-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6151b-113">Čia funkcija yra nurodyta kaip:</span><span class="sxs-lookup"><span data-stu-id="6151b-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="6151b-114">**Modulis** – kaštų valdymas</span><span class="sxs-lookup"><span data-stu-id="6151b-114">**Module** - Cost management</span></span>
- <span data-ttu-id="6151b-115">**Funkcijos pavadinimas** – Atsargų skirstymo pagal terminus ataskaitos saugykla</span><span class="sxs-lookup"><span data-stu-id="6151b-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="6151b-116">Atsargų skirstymo pagal terminus ataskaitos saugyklos vykdymas</span><span class="sxs-lookup"><span data-stu-id="6151b-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="6151b-117">Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų skirstymas pagal terminus**.</span><span class="sxs-lookup"><span data-stu-id="6151b-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="6151b-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6151b-118">Select **New**.</span></span>
1. <span data-ttu-id="6151b-119">Lauke **Proceso identifikatorius – pavadinimas** įveskite unikalų ataskaitos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6151b-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="6151b-120">Pasirinkite **Identifikavimas – ID** ataskaitą ir filtruokite ją, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="6151b-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="6151b-121">Ataskaitų vykdymas visada atliekamas paketinėje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="6151b-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="6151b-122">Po to, kai paketinė užduotis baigiama, išvestis rodoma puslapyje **Atsargų skirstymo pagal terminus saugojimas**.</span><span class="sxs-lookup"><span data-stu-id="6151b-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="6151b-123">Norėdami peržiūrėti rezultatą kaip formą, kurioje yra tradicinis tinklelio maketas, pasirinkite **peržiūrėti informaciją.**</span><span class="sxs-lookup"><span data-stu-id="6151b-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="6151b-124">Norėdami peržiūrėti išvestį kaip kaupiamąją diagramą, pasirinkite **Peržiūrėti diagramą**.</span><span class="sxs-lookup"><span data-stu-id="6151b-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6151b-125">Formoje nebus įtrauktos tarpinės sumos, kurios nurodytos ataskaitos makete.</span><span class="sxs-lookup"><span data-stu-id="6151b-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="6151b-126">Duomenų objektas **Atsargų skirstymo pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą taikant filtrą **Proceso identifikatorius – pavadinimas** bet kokiam formatui, kurį palaiko duomenų valdymas.</span><span class="sxs-lookup"><span data-stu-id="6151b-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
