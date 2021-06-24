---
title: Naudojimo valdymo skelbimų skelbimų lentos
description: Šioje temoje paaiškinama, kaip naudoti naudojimo valdymo skelbimų skelbimų skydą, norint stebėti elektroninių SF išrašymo paslaugos naudojimą ir toliau bus suderinama.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130511"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="901bb-103">Naudojimo valdymo skelbimų skelbimų lentos</span><span class="sxs-lookup"><span data-stu-id="901bb-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="901bb-104">Naudojimo **valdymo skelbimų** funkcija padeda stebėti elektroninių SF išrašymo tarnybos naudojimą, todėl jūsų organizacija gali toliau naudoti savo organizaciją kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="901bb-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="901bb-105">Atitikimas nustatomas apskaičiuojant pateikimo apimtį ir lyginant jį su įsigytu pateikimų kiekiu, norint nustatyti bet kokius nuokrypius tarp įsigyto tūrio ir naudomo tūrio.</span><span class="sxs-lookup"><span data-stu-id="901bb-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="901bb-106">Skelbimų srityje yra šie indikatoriai:</span><span class="sxs-lookup"><span data-stu-id="901bb-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="901bb-107">Vienas išlaidų indikatorius, kurį galite naudoti licencijos atitikimo tikslais stebėti suvartojimą:</span><span class="sxs-lookup"><span data-stu-id="901bb-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="901bb-108">Naudojimas per mėnesį (eksportas)</span><span class="sxs-lookup"><span data-stu-id="901bb-108">Usage per month (export)</span></span>

- <span data-ttu-id="901bb-109">Trys veikimo indikatoriai, kuriuos galite naudoti norėdami sekti elektroninių SF išrašymo paslaugos naudojimą valdymo tikslais:</span><span class="sxs-lookup"><span data-stu-id="901bb-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="901bb-110">Naudojimas pagal funkciją</span><span class="sxs-lookup"><span data-stu-id="901bb-110">Usage by feature</span></span>
    - <span data-ttu-id="901bb-111">Naudojimas pagal aplinką</span><span class="sxs-lookup"><span data-stu-id="901bb-111">Usage by environment</span></span>
    - <span data-ttu-id="901bb-112">Naudojimas per mėnesį (importas)</span><span class="sxs-lookup"><span data-stu-id="901bb-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="901bb-113">Matavimo tikslas</span><span class="sxs-lookup"><span data-stu-id="901bb-113">Measurement scope</span></span>

- <span data-ttu-id="901bb-114">Matavimo vienetai:</span><span class="sxs-lookup"><span data-stu-id="901bb-114">Unit of measure:</span></span> 

    <span data-ttu-id="901bb-115">Naudojimo **valdymo skelbimų** skelbimų srityje pateikiamas verslo dokumentai ir importuotos elektroninės SF.</span><span class="sxs-lookup"><span data-stu-id="901bb-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="901bb-116">Organizacija:</span><span class="sxs-lookup"><span data-stu-id="901bb-116">Organization:</span></span> 

    <span data-ttu-id="901bb-117">Skaičiavimas susumuojamas pagal jūsų organizacijos nuomininkų ID, neatsižvelgiant į skaičių arba juridinių subjektų skaičių, kur įgalinta elektroninių SF „Microsoft Dynamics 365 Finance“ bei „Dynamics 365 Supply Chain Management“ išrašymo tarnyba.</span><span class="sxs-lookup"><span data-stu-id="901bb-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="901bb-118">Indikatorius: naudojimas per mėnesį (eksportas)</span><span class="sxs-lookup"><span data-stu-id="901bb-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="901bb-119">Šis indikatorius pateikia informaciją apie elektronines SF, kurias jūsų organizacija išrašo nustatytą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="901bb-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="901bb-120">Aprėptis</span><span class="sxs-lookup"><span data-stu-id="901bb-120">Scope</span></span>
- <span data-ttu-id="901bb-121">Verslo dokumentų, pateiktų iš „Electronic Invoicing“ ir „ Supply Chain Management“ į elektroninių SF išrašymo paslaugą, skaičius neatsižvelgiant į eilučių, kurios yra tuose verslo dokumentuose, skaičių.</span><span class="sxs-lookup"><span data-stu-id="901bb-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="901bb-122">Pateiktų verslo dokumentų, kuriuos sėkmingai apdorojo elektroninių SF išrašymo tarnyba, skaičius.</span><span class="sxs-lookup"><span data-stu-id="901bb-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="901bb-123">Dokumentas laikomas sėkmingai apdorotu, kai baigiamas veiksmų srautas, apibrėžtas funkcijos nustatyme.</span><span class="sxs-lookup"><span data-stu-id="901bb-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="901bb-124">Kai elektroninė SF pateikiama išorinei žiniatinklio tarnybai, skaičiavimas nepriklauso nuo žiniatinklio tarnybos apdorojimo rezultatų (priimta, atmesta arba schemos tikrinimo klaida).</span><span class="sxs-lookup"><span data-stu-id="901bb-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="901bb-125">Jei žiniatinklio tarnyba gavo ir atsakė į elektroninių SF išrašymo tarnybos užklausą, pateikimas laikomas galiojančiu inventorizacija.</span><span class="sxs-lookup"><span data-stu-id="901bb-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="901bb-126">**Išimtis:** verslo dokumentai neskaičiuojami, jei jie iš naujo pateikiami iš finansų ir „Supply Chain Management“ į „Electronic Invoicing“ tarnybą, pvz., scenarijuose, kuriuose norint pakeisti elektroninės SF būseną reikia iš naujo pateikti tą patį verslo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="901bb-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="901bb-127">Pvz., Brazilijos elektroninės SF išdavimas skaičiuojamas kaip galiojantis, bet jo atšaukimo užklausa neskaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="901bb-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="901bb-128">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="901bb-128">Calculation</span></span>

<span data-ttu-id="901bb-129">Balanso skaičiavimas apskaičiuojamas taip:</span><span class="sxs-lookup"><span data-stu-id="901bb-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="901bb-130">Balansas = Laisvas + Nupirkta – Naudojama</span><span class="sxs-lookup"><span data-stu-id="901bb-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="901bb-131">Kur:</span><span class="sxs-lookup"><span data-stu-id="901bb-131">Where:</span></span>

- <span data-ttu-id="901bb-132">Laisvas:</span><span class="sxs-lookup"><span data-stu-id="901bb-132">Free:</span></span>
  
    <span data-ttu-id="901bb-133">Nemokamas verslo dokumentų kiekis, kurį klientas gali pateikti per mėnesį.</span><span class="sxs-lookup"><span data-stu-id="901bb-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="901bb-134">Joje yra 100 verslo dokumentų, kuriuos galima pateikti elektroninių SF išrašymo tarnybai, paketas.</span><span class="sxs-lookup"><span data-stu-id="901bb-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="901bb-135">Laisvas tūris nėra kaupiamas ir bet koks likęs balansas nėra sumuojamas į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="901bb-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="901bb-136">Nupirkta:</span><span class="sxs-lookup"><span data-stu-id="901bb-136">Purchased:</span></span>
  
    <span data-ttu-id="901bb-137">Joje yra 1000 verslo dokumentų, kuriuos galima pateikti elektroninių SF išrašymo tarnybai, paketas.</span><span class="sxs-lookup"><span data-stu-id="901bb-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="901bb-138">Šis paketas turi būti įsigytas jūsų organizacijai kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="901bb-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="901bb-139">Įsigytas tūris nėra kaupiamas ir bet koks likęs balansas nėra sumuojamas į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="901bb-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="901bb-140">Naudojamas:</span><span class="sxs-lookup"><span data-stu-id="901bb-140">Used:</span></span> 

    <span data-ttu-id="901bb-141">Verslo dokumentų pateikimo elektroninių SF išrašymo tarnybai pagal apibrėžtus kriterijus skaičius.</span><span class="sxs-lookup"><span data-stu-id="901bb-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="901bb-142">Jei jūsų organizacija planuoja viršyti 100 laisvos formos pateikimų per mėnesį apimtį, pirkite didžiausią apimtį, taip užtikrinsite, kad išliktų suderinama su Elektroninių SF išrašymo tarnybos Microsoft licencijavimo strategija.</span><span class="sxs-lookup"><span data-stu-id="901bb-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="901bb-143">Šiuo metu įsigytas kiekis turi būti įvestas rankiniu būdu, atsižvelgiant į įsigijimo datą, kaip keletą pakuočių iš 1000 pateikimų.</span><span class="sxs-lookup"><span data-stu-id="901bb-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="901bb-144">Indikatorius: naudojimas pagal priemonę</span><span class="sxs-lookup"><span data-stu-id="901bb-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="901bb-145">Šis indikatorius rodo elektroninių SF išrašymo priemonių naudojimą elektroninių SF išdavimui nustatytą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="901bb-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="901bb-146">Skaičiavimas:</span><span class="sxs-lookup"><span data-stu-id="901bb-146">Calculation:</span></span>
  
    <span data-ttu-id="901bb-147">Naudota = skaičius, kiek kartų kiekviena elektroninio SF išrašymo priemonė buvo naudojama pateikiant verslo dokumentus elektroninių SF išrašymo tarnybai.</span><span class="sxs-lookup"><span data-stu-id="901bb-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="901bb-148">Indikatorius: naudojimas pagal aplinką</span><span class="sxs-lookup"><span data-stu-id="901bb-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="901bb-149">Šis indikatorius rodo elektroninių SF išrašymo paslaugų aplinkos naudojimą apibrėžtu laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="901bb-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="901bb-150">Skaičiavimas:</span><span class="sxs-lookup"><span data-stu-id="901bb-150">Calculation:</span></span>
    
    <span data-ttu-id="901bb-151">Naudota = skaičius, kiek kartų kiekviena elektroninio SF išrašymo tarnybos aplinka buvo naudojama pateikiant verslo dokumentus elektroninių SF išrašymo tarnybai.</span><span class="sxs-lookup"><span data-stu-id="901bb-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="901bb-152">Indikatorius: naudojimas per mėnesį (importas)</span><span class="sxs-lookup"><span data-stu-id="901bb-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="901bb-153">Šis indikatorius rodo elektroninių SF pagal elektroninių SF išrašymo paslaugą „Finance and Supply Chain Management“ per nurodytą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="901bb-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="901bb-154">Aprėptis:</span><span class="sxs-lookup"><span data-stu-id="901bb-154">Scope:</span></span>

    <span data-ttu-id="901bb-155">Elektroninės SF, importuojamos į „Finance and Supply Chain Management“, neatsižvelgiant į eilučių, kurias sudaro tos elektroninės SF, skaičių.</span><span class="sxs-lookup"><span data-stu-id="901bb-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="901bb-156">Skaičiavimas:</span><span class="sxs-lookup"><span data-stu-id="901bb-156">Calculation:</span></span>

    <span data-ttu-id="901bb-157">Gauta = importuotų elektroninių SF į „Finance and Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="901bb-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="901bb-158">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="901bb-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="901bb-159">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="901bb-159">Purchase</span></span>

<span data-ttu-id="901bb-160">Skirtuke **Mėnesio naudojimas (eksportas)** pasirinkite **Pirkimas** norėdami rankiniu būdu užregistruoti įsigytų pateikimų sumą.</span><span class="sxs-lookup"><span data-stu-id="901bb-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="901bb-161">Nurodytą datą pasirinkite **Nauja** ir įveskite tą datą **įsigytų** pakuočių skaičių.</span><span class="sxs-lookup"><span data-stu-id="901bb-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="901bb-162">**Kiekis** yra skaičiuojamas taip:</span><span class="sxs-lookup"><span data-stu-id="901bb-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="901bb-163">Kiekis = Pakuotės \* 1000</span><span class="sxs-lookup"><span data-stu-id="901bb-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="901bb-164">Apskaičiuotas **kiekis** rodomas pirkta **naudojant** indikatorių Naudojimas **mėnesiui (eksportas)**.</span><span class="sxs-lookup"><span data-stu-id="901bb-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="901bb-165">Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="901bb-165">Update</span></span>

<span data-ttu-id="901bb-166">Veiksmų srityje pasirinkite **Naujinti,** kad būtų atnaujinti skaičiavimai ir atnaujinti duomenys, rodomi puslapyje ir diagramoje.</span><span class="sxs-lookup"><span data-stu-id="901bb-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="901bb-167">Iš naujo nustatyti istorijos duomenis</span><span class="sxs-lookup"><span data-stu-id="901bb-167">Reset history data</span></span>

<span data-ttu-id="901bb-168">Veiksmų srityje pasirinkite Iš naujo nustatyti **retrospektyvos duomenis**, kad atnaujinumėte duomenų bazę, iš kurios skaičiuojami indikatoriai.</span><span class="sxs-lookup"><span data-stu-id="901bb-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="901bb-169">Naudojimo **valdymo skelbimų** skelbimų srityje nerodyti piniginės sumos.</span><span class="sxs-lookup"><span data-stu-id="901bb-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="901bb-170">Vietoj to ji rodo tik suskaičiuotų pateikimų ir importuotų dokumentų apimtį.</span><span class="sxs-lookup"><span data-stu-id="901bb-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
