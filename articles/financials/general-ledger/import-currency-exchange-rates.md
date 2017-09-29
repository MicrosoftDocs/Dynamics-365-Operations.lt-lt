---
title: "Importuoti valiutų kursus"
description: "Jei juridinis subjektas gavo SF užsienio valiuta, svarbu užsienio valiutą konvertuoti į vietos valiutą. Todėl reikalingi naujausi skirtingų valiutų kursai. Šioje temoje pateikiama informacija apie užsienio valiutų kursų nuorodų, kurias internete skelbia valiutų kursų teikėjai (pvz., Europos centrinis bankas ir Rusijos centrinis bankas), importavimo reikiamus parametrus ir apdorojimą."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c80f6eec7c4d5129337b6f7869fbd8a4cc978acd
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="import-currency-exchange-rates"></a><span data-ttu-id="672c4-105">Importuoti valiutų kursus</span><span class="sxs-lookup"><span data-stu-id="672c4-105">Import currency exchange rates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="672c4-106">Jei juridinis subjektas gavo SF užsienio valiuta, svarbu užsienio valiutą konvertuoti į vietos valiutą.</span><span class="sxs-lookup"><span data-stu-id="672c4-106">If a legal entity has received invoices in foreign currencies, it’s necessary to convert the foreign currency into the local currency.</span></span> <span data-ttu-id="672c4-107">Todėl reikalingi naujausi skirtingų valiutų kursai.</span><span class="sxs-lookup"><span data-stu-id="672c4-107">This means that up-to-date exchange rates for different currencies are required.</span></span> <span data-ttu-id="672c4-108">Šioje temoje pateikiama informacija apie užsienio valiutų kursų nuorodų, kurias internete skelbia valiutų kursų teikėjai (pvz., Europos centrinis bankas ir Rusijos centrinis bankas), importavimo reikiamus parametrus ir apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="672c4-108">This topic provides an overview of the required settings and processing for importing foreign exchange reference rates published over the Internet by the exchange rate providers, such as the European Central Bank and the Central Bank of Russia.</span></span>

<span data-ttu-id="672c4-109">Toliau pateikiamuose skyriuose aprašomas informacijos, kuri naudojama nustatant ir apdorojant užsienio valiutų kursų importavimo procesą, srautas.</span><span class="sxs-lookup"><span data-stu-id="672c4-109">The following sections describe the flow of information that is used for setting up and processing the import of foreign exchange rates.</span></span>

## <a name="configure-an-exchange-rate-provider"></a><span data-ttu-id="672c4-110">Valiutų kursų teikėjo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="672c4-110">Configure an exchange rate provider</span></span>
<span data-ttu-id="672c4-111">Prieš importuodami valiutų kursus turite nustatyti informaciją, kurios reikia valiutų kursų teikėjams.</span><span class="sxs-lookup"><span data-stu-id="672c4-111">Before you can import exchange rates, you must set up the information that is required by the providers who offer the exchange rates.</span></span> <span data-ttu-id="672c4-112">Naudokite puslapį **Konfigūruoti valiutų kursų teikėjus**, norėdami pasirinkti valiutų kursų teikėjus.</span><span class="sxs-lookup"><span data-stu-id="672c4-112">Use the **Configure exchange rate providers** page to select the exchange rate providers.</span></span> <span data-ttu-id="672c4-113">Kai kurie valiutų kursų teikėjai yra įtraukti į „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="672c4-113">Some exchange rate providers are included with the demo data in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="672c4-114">Toliau esančioje lentelėje pateikiami šio puslapio valdiklių aprašymai.</span><span class="sxs-lookup"><span data-stu-id="672c4-114">The following table provides descriptions for the controls on this page.</span></span>

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="672c4-115">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="672c4-115">**Field**</span></span> | <span data-ttu-id="672c4-116">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="672c4-116">**Description**</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="672c4-117">**Pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="672c4-117">**Name**</span></span>  | <span data-ttu-id="672c4-118">Valiutų kursų teikėjo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="672c4-118">The name of the exchange rate provider.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="672c4-119">**Raktas**</span><span class="sxs-lookup"><span data-stu-id="672c4-119">**Key**</span></span>   | <span data-ttu-id="672c4-120">Teikėjo reikalaujamas unikalus kiekvienos konfigūracijos informacijos dalies identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="672c4-120">The unique identifier for each piece of configuration information that is required by the provider.</span></span> <span data-ttu-id="672c4-121">Ši informacija automatiškai įtraukiama ir priskiriama kiekvienam valiutų kursų teikėjui, kurį įtraukiate spustelėdami mygtuką **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="672c4-121">This information is automatically added for each exchange rate provider that you add when you click the **Add** button.</span></span> |
| <span data-ttu-id="672c4-122">**Vertė**</span><span class="sxs-lookup"><span data-stu-id="672c4-122">**Value**</span></span> | <span data-ttu-id="672c4-123">Kiekvieno rakto informacija.</span><span class="sxs-lookup"><span data-stu-id="672c4-123">Information for each key.</span></span> <span data-ttu-id="672c4-124">Ši informacija įtraukiama ir priskiriama kiekvienam valiutų kursų teikėjui, kurį įtraukiate spustelėdami mygtuką **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="672c4-124">This information is added for each exchange rate provider that you add when you click the **Add** button.</span></span>                                                                                         |

## <a name="import-currency-exchange-rates"></a><span data-ttu-id="672c4-125">Importuoti valiutų kursus</span><span class="sxs-lookup"><span data-stu-id="672c4-125">Import currency exchange rates</span></span>
<span data-ttu-id="672c4-126">Galite importuoti valiutų kursus iš valiutų kursų teikėjų šaltinio ir juos nustatyti puslapyje **Valiutų kursai**.</span><span class="sxs-lookup"><span data-stu-id="672c4-126">You can import exchange rates from the exchange rate providers source, and set them up in the **Currency exchange rates** page.</span></span> <span data-ttu-id="672c4-127">Naudokite puslapį **Importuoti valiutų kursus**, norėdami importuoti valiutų kursus.</span><span class="sxs-lookup"><span data-stu-id="672c4-127">Use the **Import currency exchange rates** page to import the exchange rates.</span></span> <span data-ttu-id="672c4-128">Toliau esančioje lentelėje pateikiami laukų, reikalingų importavimo procesui sėkmingai atlikti, aprašai.</span><span class="sxs-lookup"><span data-stu-id="672c4-128">The following table provides descriptions the fields that are required to successfully complete the import process.</span></span>

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="672c4-129">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="672c4-129">**Field**</span></span>                              | <span data-ttu-id="672c4-130">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="672c4-130">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="672c4-131">**Valiutos kurso tipas**</span><span class="sxs-lookup"><span data-stu-id="672c4-131">**Exchange rate type**</span></span>                 | <span data-ttu-id="672c4-132">Valiutos kurso tipas.</span><span class="sxs-lookup"><span data-stu-id="672c4-132">An exchange rate type.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="672c4-133">**Valiutų kursų teikėjas**</span><span class="sxs-lookup"><span data-stu-id="672c4-133">**Exchange rate provider**</span></span>             | <span data-ttu-id="672c4-134">Valiutų kursų teikėjas.</span><span class="sxs-lookup"><span data-stu-id="672c4-134">An exchange rate provider.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="672c4-135">**Importuoti kaip**</span><span class="sxs-lookup"><span data-stu-id="672c4-135">**Import as of**</span></span>                       | <span data-ttu-id="672c4-136">Pagal šį parametrą nustatoma, ar importuoti šios dienos, ar datų intervalo valiutų kursus.</span><span class="sxs-lookup"><span data-stu-id="672c4-136">This parameter manages whether to import as of today’s date or for a date range.</span></span> <span data-ttu-id="672c4-137">Jei norite naudoti datų intervalą, Įveskite arba pasirinkite pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="672c4-137">If you want to use a date range, enter or select starting and ending dates.</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="672c4-138">**Sukurti būtinas valiutų poras**</span><span class="sxs-lookup"><span data-stu-id="672c4-138">**Create necessary currency pairs**</span></span>    | <span data-ttu-id="672c4-139">Pagal šį žymės langelį nustatomas automatinis valiutų porų kūrimas, jei importuojamų valiutų porų nėra.</span><span class="sxs-lookup"><span data-stu-id="672c4-139">This check box manages the automatic creation of currency pairs, if the currency pairs that are imported do not exist.</span></span> <span data-ttu-id="672c4-140">Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="672c4-140">This option might not be available for some providers.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="672c4-141">**Nepaisyti esamų valiutų kursų**</span><span class="sxs-lookup"><span data-stu-id="672c4-141">**Override existing exchange rates**</span></span>   | <span data-ttu-id="672c4-142">Pagal šį žymės langelį nustatomas esamo valiutų poros kurso naujinimas, kai tam tikros datos valiutos kursas jau nustatytas.</span><span class="sxs-lookup"><span data-stu-id="672c4-142">This check box manages the update of the existing exchange rate for a currency pair when the exchange rate for a specific date already exists.</span></span> <span data-ttu-id="672c4-143">Jei šio žymės langelio nepažymėsite, tam tikrų datų valiutos kursas nebus importuotas, kai nustatytas kitas valiutos kursas.</span><span class="sxs-lookup"><span data-stu-id="672c4-143">If you do not select this check box, the exchange rate for the specific dates is not imported if another exchange rate already exists.</span></span>                                                                                       |
| <span data-ttu-id="672c4-144">**Neleisti importuoti nacionalinės šventės metu**</span><span class="sxs-lookup"><span data-stu-id="672c4-144">**Prevent import on national holiday**</span></span> | <span data-ttu-id="672c4-145">Pagal šį žymės langelį nustatomas datos, kuri yra valstybinė šventė, valiutos kurso importavimas.</span><span class="sxs-lookup"><span data-stu-id="672c4-145">This check box manages the import of the exchange rate for a date that is a public holiday.</span></span> <span data-ttu-id="672c4-146">Pavyzdžiui, jei pažymėsite šį žymės langelį ir kaip valiutų kursų teikėją naudosite Europos centrinį banką, sistema nenaujins valiutos kurso per valstybinę šventę, susijusią su dabartiniu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="672c4-146">For example, if you select this check box and use the European Central Bank as the exchange rate provider, the system will not update the exchange rate on a public holiday that is related to the current legal entity.</span></span> <span data-ttu-id="672c4-147">Pasirinkus kai kuriuos teikėjus, šios parinkties naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="672c4-147">This option might not be available for some providers.</span></span> |





