---
title: Valiutos duomenų tipo perkėlimas dvigubui rašymui
description: Šioje temoje aprašoma, kaip pakeisti dešimtainių skaičius, kurie dvigubu rašymu palaiko valiutą.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: c4f663ae36f7d4ea3db9888e618f2fe3bf8c3256
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748952"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="eb00d-103">Valiutos duomenų tipo perkėlimas dvigubui rašymui</span><span class="sxs-lookup"><span data-stu-id="eb00d-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="eb00d-104">Galite padidinti dešimtainių skaičių, palaikomų daugiausiai iki 10 valiutoms vertėms, kiekį.</span><span class="sxs-lookup"><span data-stu-id="eb00d-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="eb00d-105">Numatytoji riba yra keturi dešimtainiai skaičiai.</span><span class="sxs-lookup"><span data-stu-id="eb00d-105">The default limit is four decimal places.</span></span> <span data-ttu-id="eb00d-106">Padidinę dešimtainių skaičių kiekį, padėsite išvengti duomenų praradimo, kai naudosite dvigubo rašymo funkciją sinchronizuodami duomenis.</span><span class="sxs-lookup"><span data-stu-id="eb00d-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="eb00d-107">Dešimtainių skaičių padidinimas yra pasirenkamas pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="eb00d-108">Norėdami jį įgyvendinti, turite paprašyti pagalbos iš „Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="eb00d-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="eb00d-109">Norėdami pakeisti dešimtainių skaičių kiekį, turite atlikti du žingsnius:</span><span class="sxs-lookup"><span data-stu-id="eb00d-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="eb00d-110">Perkėlimo užklausa iš „Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="eb00d-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="eb00d-111">Dešimtainių skaičių kiekio pakeitimas „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="eb00d-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="eb00d-112">„Finance and Operations” programėlė ir „Dataverse” turi palaikyti tą patį dešimtainių skaičių kiekį valiutos vertėse.</span><span class="sxs-lookup"><span data-stu-id="eb00d-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="eb00d-113">Priešingu atveju, kai ši informacija sinchronizuojama tarp programėlių, gali dingti duomenys.</span><span class="sxs-lookup"><span data-stu-id="eb00d-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="eb00d-114">Perkėlimo procesas perkonfigūruoja, kaip saugomos valiutos ir valiutos kurso vertės, bet jokie duomenys nesikeičia.</span><span class="sxs-lookup"><span data-stu-id="eb00d-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="eb00d-115">Baigus perkėlimą, valiutų kodų ir kainų dešimtainių skaičių kiekis gali būti padidintas, o vartotojų įvesti ir peržiūrėti duomenys gali būti tikslesni dešimtainių tikslumu.</span><span class="sxs-lookup"><span data-stu-id="eb00d-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="eb00d-116">Perkėlimas yra neprivalomas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-116">Migration is optional.</span></span> <span data-ttu-id="eb00d-117">Jei didesnio dešimtainių skaičių kiekio palaikymas jums naudingas, rekomenduojame apsvarstyti perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="eb00d-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="eb00d-118">Organizacijoms, kurioms nereikia jokių verčių, kuriose yra daugiau nei keturi dešimtainiai skaičiai, perkėlimas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="eb00d-119">Perkėlimo užklausos siuntimas „Microsoft”</span><span class="sxs-lookup"><span data-stu-id="eb00d-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="eb00d-120">Saugojimas esamiems valiutos stulpeliams „Dataverse” negali palaikyti daugiau nei keturių dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb00d-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="eb00d-121">Todėl perkėlimo metu valiutos vertės nukopijuojamos į naujus duomenų bazės vidinius stulpelius.</span><span class="sxs-lookup"><span data-stu-id="eb00d-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="eb00d-122">Šis procesas vyksta nuolatos, kol bus perkelti visi duomenys.</span><span class="sxs-lookup"><span data-stu-id="eb00d-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="eb00d-123">Viduje perkėlimo pabaigoje, naujieji saugojimo tipai pakeičia senus saugojimo tipus, tačiau duomenų vertės lieka nepakitusios.</span><span class="sxs-lookup"><span data-stu-id="eb00d-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="eb00d-124">Valiutos stulpeliai gali palaikyti iki 10 dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb00d-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="eb00d-125">Perkėlimo metu „Dataverse” gali būti toliau naudojama be pertraukos.</span><span class="sxs-lookup"><span data-stu-id="eb00d-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="eb00d-126">Tuo pačiu metu keitimo kursai modifikuojami taip, kad jie palaikytų iki 12 dešimtainių skaičių, o ne dabartinę 10 limitą.</span><span class="sxs-lookup"><span data-stu-id="eb00d-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="eb00d-127">Šis pakeitimas būtinas, kad dešimtainių skaičių kiekis būtų toks „Finance and Operations” programėlėje ir „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="eb00d-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="eb00d-128">Perkėlimas nekeičia jokių duomenų.</span><span class="sxs-lookup"><span data-stu-id="eb00d-128">Migration doesn't change any data.</span></span> <span data-ttu-id="eb00d-129">Kai valiutos ir keitimo kurso stulpeliai konvertuoti, administratoriai gali konfigūruoti sistemą, kad būtų galima naudoti iki 10 dešimtainių skaičių valiutos stulpeliams, nurodydami kiekvienos operacijos valiutos ir kainos dešimtainių skaičių kiekį.</span><span class="sxs-lookup"><span data-stu-id="eb00d-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="eb00d-130">Perkėlimo užklausa</span><span class="sxs-lookup"><span data-stu-id="eb00d-130">Request a migration</span></span>

<span data-ttu-id="eb00d-131">Norėdami įjungti šią funkciją, susiekite el. paštu **CDSExpandDecimal@microsoft.com** ir nurodykite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="eb00d-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="eb00d-132">**Tema:** Užklausa įgalinti išplėstinį dešimtainių skaičių palaikymą, skirtą \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="eb00d-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="eb00d-133">**Pagrindinė dalis:** Norėčiau įgalinti išplėstinį dešimtainių skaičių palaikymą mano org. \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="eb00d-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="eb00d-134">„Microsoft” atstovas susisieks su jumis per dvi ar tris darbo dienas dėl tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="eb00d-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="eb00d-135">Kai prašote perkelti, turite žinoti apie šiuos dalykus ir pasiruošti jiems atitinkamai:</span><span class="sxs-lookup"><span data-stu-id="eb00d-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="eb00d-136">Laikas, skirtas perkelti duomenis, priklauso nuo duomenų kiekio sistemoje.</span><span class="sxs-lookup"><span data-stu-id="eb00d-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="eb00d-137">Didelių duomenų bazių perkėlimas gali užtrukti kelias dienas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="eb00d-138">Perkėlimo metu duomenų bazės dydis laikinai padidėja, nes indeksuose reikia papildomos vietos.</span><span class="sxs-lookup"><span data-stu-id="eb00d-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="eb00d-139">Kai perkėlimas baigtas, dauguma papildomos vietos atlaisvinama.</span><span class="sxs-lookup"><span data-stu-id="eb00d-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="eb00d-140">Perkėlimo proceso metu įvykus klaidai, neleidžiančios užbaigti perkėlimo, sistema parodo įspėjimus „Microsoft Support”, kad „Support” personalas galėtų įsikišti.</span><span class="sxs-lookup"><span data-stu-id="eb00d-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="eb00d-141">Tačiau, net jei vykdant perkėlimą įvyksta klaidų, „Dataverse” tolesnis naudojimas nesutrinka.</span><span class="sxs-lookup"><span data-stu-id="eb00d-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="eb00d-142">Perkėlimo procesas nėra grįžtamas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="eb00d-143">Dešimtainių skaičių kiekio keitimas</span><span class="sxs-lookup"><span data-stu-id="eb00d-143">Changing the number of decimal places</span></span>

<span data-ttu-id="eb00d-144">Baigus perkėlimą, „Dataverse” gali būti saugomi skaičiai, turintys daugiau dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb00d-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="eb00d-145">Administratoriai gali pasirinkti, kiek dešimtainių skaičių naudojama konkretiems valiutos kodams ir kainoms.</span><span class="sxs-lookup"><span data-stu-id="eb00d-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="eb00d-146">„Microsoft Power Apps” „Power BI”, ir „Power Automate” vartotojai gali tada peržiūrėti ir naudoti skaičius, turinčius daugiau dešimtainių skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb00d-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="eb00d-147">Norėdami atlikti šį keitimą, turite atnaujinti šiuos parametrus „Power Apps”:</span><span class="sxs-lookup"><span data-stu-id="eb00d-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="eb00d-148">**Sistemos parametrai: kainos valiutos tikslumas** – **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** stulpelyje nustatoma, kaip valiuta veiks organizacijoje, kai **Kainos tikslumas** yra pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="eb00d-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="eb00d-149">**Verslo valdymas: valiutos** – **Valiutos tikslumas** stulpelis leidžia nurodyti pasirinktinį dešimtainių skaičių kiekį konkrečiai valiutai.</span><span class="sxs-lookup"><span data-stu-id="eb00d-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="eb00d-150">Yra atsarginis visai organizacijai taikomas parametras.</span><span class="sxs-lookup"><span data-stu-id="eb00d-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="eb00d-151">Yra keletas apribojimų:</span><span class="sxs-lookup"><span data-stu-id="eb00d-151">There are some limitations:</span></span>

+ <span data-ttu-id="eb00d-152">Negalite sukonfigūruoti valiutos stulpelio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="eb00d-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="eb00d-153">Galite nurodyti daugiau nei keturis dešimtainius skaičius **Kaina** ir **Operacijos valiuta** lygiuose.</span><span class="sxs-lookup"><span data-stu-id="eb00d-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="eb00d-154">Sistemos parametrai: valiutos kainos tikslumas</span><span class="sxs-lookup"><span data-stu-id="eb00d-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="eb00d-155">Baigus perkėlimą, administratoriai gali nustatyti valiutos tikslumą.</span><span class="sxs-lookup"><span data-stu-id="eb00d-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="eb00d-156">Eikite į **Parametrai \> Administravimas** ir pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="eb00d-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="eb00d-157">Tada skirtuke **Bendra** pakeiskite **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** stulpelio vertę, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="eb00d-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Valiutos sistemos parametrai](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="eb00d-159">Verslo valdymas: valiutos</span><span class="sxs-lookup"><span data-stu-id="eb00d-159">Business Management: Currencies</span></span>

<span data-ttu-id="eb00d-160">Jei jums reikia, kad valiutos tikslumas konkrečiai valiutai skirtųsi nuo valiutos tikslumo, naudojamo kainai, galite jį pakeisti.</span><span class="sxs-lookup"><span data-stu-id="eb00d-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="eb00d-161">Eikite į **Parametrai \> Verslo valdymas**, pasirinkite **Valiutos** ir pasirinkite valiutą, kurią norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="eb00d-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="eb00d-162">Tada nustatykite **Valiutos tikslumas** stulpelį pagal dešimtainių skaičių kiekį, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="eb00d-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Konkrečios lokalės valiutos parametrai](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="eb00d-164">lentelės: stulpelis Valiuta</span><span class="sxs-lookup"><span data-stu-id="eb00d-164">tables: Currency column</span></span>

<span data-ttu-id="eb00d-165">Galima tik keturis kartus koreguoti dešimtainių skaičių, skirtų konkrečios valiutos stulpeliams, kiekius.</span><span class="sxs-lookup"><span data-stu-id="eb00d-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]