---
title: Valiutos duomenų tipo perkėlimas dvigubui rašymui
description: Šioje temoje aprašoma, kaip pakeisti dešimtainių skaičius, kurie dvigubu rašymu palaiko valiutą.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456819"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="94b35-103">Valiutos duomenų tipo perkėlimas dvigubui rašymui</span><span class="sxs-lookup"><span data-stu-id="94b35-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94b35-104">Galite padidinti dešimtainių skaičių, palaikomų daugiausiai iki 10 valiutoms vertėms, kiekį.</span><span class="sxs-lookup"><span data-stu-id="94b35-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="94b35-105">Numatytoji riba yra keturi dešimtainiai skaičiai.</span><span class="sxs-lookup"><span data-stu-id="94b35-105">The default limit is four decimal places.</span></span> <span data-ttu-id="94b35-106">Padidinę dešimtainių skaičių kiekį, padėsite išvengti duomenų praradimo, kai naudosite dvigubo rašymo funkciją sinchronizuodami duomenis.</span><span class="sxs-lookup"><span data-stu-id="94b35-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="94b35-107">Dešimtainių skaičių padidinimas yra pasirenkamas pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="94b35-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="94b35-108">Norėdami jį įgyvendinti, turite paprašyti pagalbos iš „Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="94b35-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="94b35-109">Norėdami pakeisti dešimtainių skaičių kiekį, turite atlikti du žingsnius:</span><span class="sxs-lookup"><span data-stu-id="94b35-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="94b35-110">Perkėlimo užklausa iš „Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="94b35-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="94b35-111">Dešimtainių skaičių kiekio pakeitimas „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="94b35-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="94b35-112">„Finance and Operations” programėlė ir „Common Data Service” turi palaikyti tą patį dešimtainių skaičių kiekį valiutos vertėse.</span><span class="sxs-lookup"><span data-stu-id="94b35-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="94b35-113">Priešingu atveju, kai ši informacija sinchronizuojama tarp programėlių, gali dingti duomenys.</span><span class="sxs-lookup"><span data-stu-id="94b35-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="94b35-114">Perkėlimo procesas perkonfigūruoja, kaip saugomos valiutos ir valiutos kurso vertės, bet jokie duomenys nesikeičia.</span><span class="sxs-lookup"><span data-stu-id="94b35-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="94b35-115">Baigus perkėlimą, valiutų kodų ir kainų dešimtainių skaičių kiekis gali būti padidintas, o vartotojų įvesti ir peržiūrėti duomenys gali būti tikslesni dešimtainių tikslumu.</span><span class="sxs-lookup"><span data-stu-id="94b35-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="94b35-116">Perkėlimas yra neprivalomas.</span><span class="sxs-lookup"><span data-stu-id="94b35-116">Migration is optional.</span></span> <span data-ttu-id="94b35-117">Jei didesnio dešimtainių skaičių kiekio palaikymas jums naudingas, rekomenduojame apsvarstyti perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="94b35-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="94b35-118">Organizacijoms, kurioms nereikia jokių verčių, kuriose yra daugiau nei keturi dešimtainiai skaičiai, perkėlimas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="94b35-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="94b35-119">Perkėlimo užklausos siuntimas „Microsoft”</span><span class="sxs-lookup"><span data-stu-id="94b35-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="94b35-120">Saugojimas esamiems valiutos laukams „Common Data Service” negali palaikyti daugiau nei keturių dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="94b35-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="94b35-121">Todėl perkėlimo metu valiutos vertės nukopijuojamos į naujus duomenų bazės vidinius laukus.</span><span class="sxs-lookup"><span data-stu-id="94b35-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="94b35-122">Šis procesas vyksta nuolatos, kol bus perkelti visi duomenys.</span><span class="sxs-lookup"><span data-stu-id="94b35-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="94b35-123">Viduje perkėlimo pabaigoje, naujieji saugojimo tipai pakeičia senus saugojimo tipus, tačiau duomenų vertės lieka nepakitusios.</span><span class="sxs-lookup"><span data-stu-id="94b35-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="94b35-124">Valiutos laukai gali palaikyti iki 10 dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="94b35-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="94b35-125">Perkėlimo metu „Common Data Service” gali būti toliau naudojama be pertraukos.</span><span class="sxs-lookup"><span data-stu-id="94b35-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="94b35-126">Tuo pačiu metu keitimo kursai modifikuojami taip, kad jie palaikytų iki 12 dešimtainių skaičių, o ne dabartinę 10 limitą.</span><span class="sxs-lookup"><span data-stu-id="94b35-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="94b35-127">Šis pakeitimas būtinas, kad dešimtainių skaičių kiekis būtų toks „Finance and Operations” programėlėje ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="94b35-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="94b35-128">Perkėlimas nekeičia jokių duomenų.</span><span class="sxs-lookup"><span data-stu-id="94b35-128">Migration doesn't change any data.</span></span> <span data-ttu-id="94b35-129">Kai valiutos ir keitimo kurso laukai konvertuoti, administratoriai gali konfigūruoti sistemą, kad būtų galima naudoti iki 10 dešimtainių skaičių valiutos laukas nurodant kiekvienos operacijos valiutos ir kainos dešimtainių skaičių kiekį. </span><span class="sxs-lookup"><span data-stu-id="94b35-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="94b35-130">Perkėlimo užklausa</span><span class="sxs-lookup"><span data-stu-id="94b35-130">Request a migration</span></span>

<span data-ttu-id="94b35-131">Norėdami įjungti šią funkciją, susiekite el. paštu **CDSExpandDecimal@microsoft.com** ir nurodykite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="94b35-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="94b35-132">**Tema:** Užklausa įgalinti išplėstinį dešimtainių skaičių palaikymą, skirtą \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="94b35-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="94b35-133">**Pagrindinė dalis:** Norėčiau įgalinti išplėstinį dešimtainių skaičių palaikymą mano org. \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="94b35-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="94b35-134">„Microsoft” atstovas susisieks su jumis per dvi ar tris darbo dienas dėl tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="94b35-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="94b35-135">Kai prašote perkelti, turite žinoti apie šiuos dalykus ir pasiruošti jiems atitinkamai:</span><span class="sxs-lookup"><span data-stu-id="94b35-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="94b35-136">Laikas, skirtas perkelti duomenis, priklauso nuo duomenų kiekio sistemoje.</span><span class="sxs-lookup"><span data-stu-id="94b35-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="94b35-137">Didelių duomenų bazių perkėlimas gali užtrukti kelias dienas.</span><span class="sxs-lookup"><span data-stu-id="94b35-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="94b35-138">Perkėlimo metu duomenų bazės dydis laikinai padidėja, nes indeksuose reikia papildomos vietos.</span><span class="sxs-lookup"><span data-stu-id="94b35-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="94b35-139">Kai perkėlimas baigtas, dauguma papildomos vietos atlaisvinama.</span><span class="sxs-lookup"><span data-stu-id="94b35-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="94b35-140">Perkėlimo proceso metu įvykus klaidai, neleidžiančios užbaigti perkėlimo, sistema parodo įspėjimus „Microsoft Support”, kad „Support” personalas galėtų įsikišti.</span><span class="sxs-lookup"><span data-stu-id="94b35-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="94b35-141">Tačiau, net jei vykdant perkėlimą įvyksta klaidų, „Common Data Service” tolesnis naudojimas nesutrinka.</span><span class="sxs-lookup"><span data-stu-id="94b35-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="94b35-142">Perkėlimo procesas nėra grįžtamas.</span><span class="sxs-lookup"><span data-stu-id="94b35-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="94b35-143">Dešimtainių skaičių kiekio keitimas</span><span class="sxs-lookup"><span data-stu-id="94b35-143">Changing the number of decimal places</span></span>

<span data-ttu-id="94b35-144">Baigus perkėlimą, „Common Data Service” gali būti saugomi skaičiai, turintys daugiau dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="94b35-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="94b35-145">Administratoriai gali pasirinkti, kiek dešimtainių skaičių naudojama konkretiems valiutos kodams ir kainoms.</span><span class="sxs-lookup"><span data-stu-id="94b35-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="94b35-146">„Microsoft Power Apps” „Power BI”, ir „Power Automate” vartotojai gali tada peržiūrėti ir naudoti skaičius, turinčius daugiau dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="94b35-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="94b35-147">Norėdami atlikti šį keitimą, turite atnaujinti šiuos parametrus „Power Apps”:</span><span class="sxs-lookup"><span data-stu-id="94b35-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="94b35-148">**Sistemos parametrai: kainos valiutos tikslumas** – **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** lauke, nustatoma, kaip valiuta veiks organizacijoje, kai **Kainos tikslumas** pasirenkamas.</span><span class="sxs-lookup"><span data-stu-id="94b35-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="94b35-149">**Verslo valdymas: valiutos** – **Valiutos tikslumas** laukas leidžia nurodyti pasirinktinį dešimtainių skaičių kiekį konkrečiai valiutai.</span><span class="sxs-lookup"><span data-stu-id="94b35-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="94b35-150">Yra atsarginis visai organizacijai taikomas parametras.</span><span class="sxs-lookup"><span data-stu-id="94b35-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="94b35-151">Yra keletas apribojimų:</span><span class="sxs-lookup"><span data-stu-id="94b35-151">There are some limitations:</span></span>

+ <span data-ttu-id="94b35-152">Negalite sukonfigūruoti objekto valiutos lauko.</span><span class="sxs-lookup"><span data-stu-id="94b35-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="94b35-153">Galite nurodyti daugiau nei keturis dešimtainius skaičius **Kaina** ir **Operacijos valiuta** lygiuose.</span><span class="sxs-lookup"><span data-stu-id="94b35-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="94b35-154">Sistemos parametrai: valiutos kainos tikslumas</span><span class="sxs-lookup"><span data-stu-id="94b35-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="94b35-155">Baigus perkėlimą, administratoriai gali nustatyti valiutos tikslumą.</span><span class="sxs-lookup"><span data-stu-id="94b35-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="94b35-156">Eikite į **Parametrai \> Administravimas** ir pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="94b35-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="94b35-157">Tada **Bendra** skirtuke pakeiskite **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** lauko vertę, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="94b35-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Valiutos sistemos parametrai](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="94b35-159">Verslo valdymas: valiutos</span><span class="sxs-lookup"><span data-stu-id="94b35-159">Business Management: Currencies</span></span>

<span data-ttu-id="94b35-160">Jei jums reikia, kad valiutos tikslumas konkrečiai valiutai skirtųsi nuo valiutos tikslumo, naudojamo kainai, galite jį pakeisti.</span><span class="sxs-lookup"><span data-stu-id="94b35-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="94b35-161">Eikite į **Parametrai \> Verslo valdymas**, pasirinkite **Valiutos** ir pasirinkite valiutą, kurią norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="94b35-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="94b35-162">Tada nustatykite **Valiutos tikslumas** lauką pagal dešimtainių skaičių kiekį, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="94b35-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Konkrečios lokalės valiutos parametrai](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="94b35-164">Objektai: valiutos laukas</span><span class="sxs-lookup"><span data-stu-id="94b35-164">Entities: Currency field</span></span>

<span data-ttu-id="94b35-165">Galima tik keturis kartus koreguoti dešimtainių skaičių, skirtų konkrečios valiutos laukams, kiekius.</span><span class="sxs-lookup"><span data-stu-id="94b35-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>
