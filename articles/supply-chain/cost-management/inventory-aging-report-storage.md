---
title: Atsargų skirstymo pagal terminus ataskaita
description: Šioje temoje aprašomos funkcijos, leidžiančios vykdyti atsargų skirstymo pagal terminus ataskaitą ir įgalinti išvestis kaip formą ir diagramą.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810256"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="f8a7f-103">Atsargų skirstymo pagal terminus ataskaita</span><span class="sxs-lookup"><span data-stu-id="f8a7f-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f8a7f-104">„Microsoft Dynamics 365 Supply Chain Management“ galite vykdyti **Atsargų skirstymas pagal terminus** ataskaitą ir įgalinti išvestį kaip formą ir diagramą.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="f8a7f-105">Formoje stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į sukonfigūruotą maketą.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="f8a7f-106">Diagramoje pateikiama vizualinė peržiūra, kuri palaiko filtravimą ir leidžia detalizuoti informaciją.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="f8a7f-107">Be to, duomenų subjektas pavadinimu **Atsargų skirstymas pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymas pagal terminus** ataskaitą, kad būtų galima naudoti, pavyzdžiui, „Microsoft Excel“ failo arba PDF failo formatą.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="f8a7f-108">Šis **Atsargų skirstymas pagal terminus** ataskaitos vykdymo metodas naudingas tais atvejais, kai išvestyje yra daug eilučių.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="f8a7f-109">Pavyzdžiui, išvestyje yra daug eilučių, jei yra 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai, o jūs prašote atsargų skirstymo pagal terminus pagal prekę, teritoriją ir sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="f8a7f-110">Atsargų skirstymo pagal terminus ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="f8a7f-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="f8a7f-111">Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų skirstymas pagal terminus**.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="f8a7f-112">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-112">Select **New**.</span></span>
1. <span data-ttu-id="f8a7f-113">Lauke **Proceso identifikatorius – pavadinimas** įveskite unikalų ataskaitos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="f8a7f-114">Pasirinkite **Identifikavimas – ID** ataskaitą ir filtruokite ją, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="f8a7f-115">Ataskaitų vykdymas visada atliekamas paketinėje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="f8a7f-116">Po to, kai paketinė užduotis baigiama, išvestis rodoma puslapyje **Atsargų skirstymo pagal terminus saugojimas**.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="f8a7f-117">Norėdami peržiūrėti rezultatą kaip formą, kurioje yra tradicinis tinklelio maketas, pasirinkite **peržiūrėti informaciją.**</span><span class="sxs-lookup"><span data-stu-id="f8a7f-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="f8a7f-118">Norėdami peržiūrėti išvestį kaip kaupiamąją diagramą, pasirinkite **Peržiūrėti diagramą**.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8a7f-119">Formoje nebus įtrauktos tarpinės sumos, kurios nurodytos ataskaitos makete.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="f8a7f-120">Duomenų objektas**Atsargų skirstymo pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymas pagal terminus** ataskaitą taikant filtrą **Proceso identifikatorius – pavadinimas** bet kokiam formatui, kurį palaiko duomenų valdymas.</span><span class="sxs-lookup"><span data-stu-id="f8a7f-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
