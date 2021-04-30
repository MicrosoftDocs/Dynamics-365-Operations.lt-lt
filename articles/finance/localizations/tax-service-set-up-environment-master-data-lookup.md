---
title: Bendrųjų duomenų peržvalgos aplinkos nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti aplinką, kad būtų galima naudoti Mokesčių skaičiavimo bendrųjų duomenų peržvalgos funkciją.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869085"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="c5a3c-103">Bendrųjų duomenų peržvalgos aplinkos nustatymas</span><span class="sxs-lookup"><span data-stu-id="c5a3c-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c5a3c-104">Šioje temoje paaiškinama, kaip nustatyti aplinką, kad būtų galima naudoti Mokesčių skaičiavimo bendrųjų duomenų peržvalgos funkciją.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="c5a3c-105">Nustatykite „Power Platform” integravimą „Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="c5a3c-106">Daugiau informacijos rasite [„Microsoft Power Platform” integravimas – Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="c5a3c-107">Nustatykite „Dynamics 365 Finance” ir „Microsoft Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="c5a3c-108">Daugiau informacijos rasite [Gauti sprendimą](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ir [Autentifikavimas ir autorizacija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="c5a3c-109">Importuokite *Būtinąjį mokesčių tarnybos virtualiojo objekto sprendimą* iš [Mokesčių tarnybos virtualiojo objekto](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="c5a3c-110">Nustatykite „Dynamics 365 Regulatory Configuration Service” (RCS).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="c5a3c-111">Sukurkite „Microsoft” paslaugos užklausą, kad būtų galima naudoti šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="c5a3c-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="c5a3c-112">„ERCds” Funkciją</span><span class="sxs-lookup"><span data-stu-id="c5a3c-112">ERCdsFeature</span></span>
      - <span data-ttu-id="c5a3c-113">Mokesčių tarnybos „CDS” funkciją</span><span class="sxs-lookup"><span data-stu-id="c5a3c-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="c5a3c-114">„Finance” programoje eikite į darbo sritį **Funkcijų valdymas** ir įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="c5a3c-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="c5a3c-115">(Peržiūros versija) Elektroninių ataskaitų „Dataverse” duomenų šaltinių palaikymas</span><span class="sxs-lookup"><span data-stu-id="c5a3c-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="c5a3c-116">(Peržiūros versija) Mokesčių tarnybos „Dataverse“ duomenų šaltinių palaikymas</span><span class="sxs-lookup"><span data-stu-id="c5a3c-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="c5a3c-117">(Peržiūros versija) Globalizacijos funkcijos</span><span class="sxs-lookup"><span data-stu-id="c5a3c-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="c5a3c-118">Prisijunkite prie RCS naudodami nuomotojo administratoriaus paskyrą.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="c5a3c-119">Eikite į **Elektroninėmis ataskaitos** > **Prijungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="c5a3c-120">Pasirinkite **Nauja** įrašui pridėti ir įveskite toliau nurodytą lauko informaciją.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="c5a3c-121">Lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="c5a3c-122">Lauke **Tipas** pasirinkite **„Dataverse”**.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="c5a3c-123">Lauke **Programa** įveskite savo „Dataverse” URL.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="c5a3c-124">Lauke **Nuomotojas** įveskite savo nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="c5a3c-125">Lauke **Pasirinktinis URL** įveskite savo „Dataverse” URL ir sujunkite jį su „/api/data/v9.1”.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="c5a3c-126">Pasirinkite **Tikrinti ryšį** ir užbaikite ryšio procesą.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="c5a3c-127">[![Mygtukas Tikrinti ryšį](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="c5a3c-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="c5a3c-128">Eikite į **Elektroninės ataskaitos** > **Mokesčių konfigūracijos** ir importuokite mokesčių konfigūracijas iš [Mokesčių konfigūracijų](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="c5a3c-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="c5a3c-129">[![Mokesčių konfigūracijų puslapis, Mokesčių duomenų modelio medis](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="c5a3c-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="c5a3c-130">Eikite į **Apmokestinto dokumento modelio susiejimas** arba **„Dataverse” modelio susiejimas**, jeigu naudojate „Microsoft” konfigūraciją ir lauke **Prijungta programa** pasirinkite įrašą, kurį sukūrėte 7 veiksme.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="c5a3c-131">Nustatykite **Numatytasis modelių susiejimui** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c5a3c-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="c5a3c-132">[![Modelio susiejimo puslapis](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="c5a3c-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
