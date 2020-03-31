---
title: Elektroninių ataskaitų (ER) išplėstinė formatų peržvalga
description: Šioje temoje aprašoma, kaip nustatyti ER formato nuorodą ER formatų peržvalgoje, kai reikiamas formatas saugomas bendrojoje saugykloje.
author: NickSelin
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c72335d7d83934146f827ef0bb568b79a585a7a5
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015321"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a><span data-ttu-id="468d4-103">Leidimo nustatyti ER formato nuorodą, pateikiančią užklausą dėl formato bendrojoje saugykloje, suteikimas vartotojams</span><span class="sxs-lookup"><span data-stu-id="468d4-103">Allow users to set up an ER format reference inquiring a format from the Global repository</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="468d4-104">Naudodami [elektroninių ataskaitų](general-electronic-reporting.md) (ER) sistemą, galite konfigūruoti siunčiamų dokumentų [formatus](general-electronic-reporting.md#FormatComponentOutbound) pagal teisinius įvairių šalių / regionų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="468d4-104">You can use the [Electronic reporting](general-electronic-reporting.md) (ER) framework to configure [formats](general-electronic-reporting.md#FormatComponentOutbound) for outbound documents in accordance to the legal requirements of various countries/regions.</span></span> <span data-ttu-id="468d4-105">ER sistemą taip pat galite naudoti, kad sukonfigūruotumėte gaunamų dokumentų analizavimo [formatus](general-electronic-reporting.md#FormatComponentInbound) ir naudotumėte šių dokumentų informaciją programos duomenims papildyti arba atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="468d4-105">You can also use the ER framework to configure [formats](general-electronic-reporting.md#FormatComponentInbound) for parsing inbound documents and use the information from those documents to append or update application data.</span></span> <span data-ttu-id="468d4-106">Visus šiuos formatus galima naudoti „Dynamics 365 Finance“ egzemplioriuje gaunamiems ir siunčiamiems verslo dokumentams tvarkyti vykdant konkretų verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="468d4-106">Each of these formats can used in your Dynamics 365 Finance instance for handling inbound or outbound business documents as part of a certain business process.</span></span> 

<span data-ttu-id="468d4-107">Paprastai turite nurodyti, koks ER formatas turi būti naudojamas konkrečiame verslo procese.</span><span class="sxs-lookup"><span data-stu-id="468d4-107">Usually, you must specify what ER format must be used in a certain business process.</span></span> <span data-ttu-id="468d4-108">Norėdami nurodyti formatą, peržvalgos lauke, sukonfigūruotame nustatant su verslo procesu susijusius parametrus, pasirinkite vieną ER formatą.</span><span class="sxs-lookup"><span data-stu-id="468d4-108">To do that, select a single ER format in a lookup field that is configured as part of business process-specific parameters.</span></span> <span data-ttu-id="468d4-109">Šie peržvalgos laukai paprastai įgyvendinami naudojant atitinkamą ER sistemos API.</span><span class="sxs-lookup"><span data-stu-id="468d4-109">These lookup fields are usually implemented by using the appropriate API of the ER framework.</span></span> <span data-ttu-id="468d4-110">Norėdami gauti daugiau informacijos, žr. [ER sistemos API kodas, kad būtų rodoma formato susiejimo peržvalga](er-apis-app73.md#code-to-display-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="468d4-110">For more information, see [ER framework API - code to display a format mapping lookup](er-apis-app73.md#code-to-display-a-format-mapping-lookup).</span></span>

<span data-ttu-id="468d4-111">Pavyzdžiui, sukonfigūravę [užsienio prekybos parametrus](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), turite nustatyti nuorodas į atskirus ER formatus, kurie bus naudojami generuojant Intrastat deklaraciją ir Intrastat deklaracijos kontrolės ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="468d4-111">For example, when you configure [foreign trade parameters](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), you need to set up the references to individual ER formats that will be used to generate the Intrastat declaration and the Intrastat declaration control report.</span></span> <span data-ttu-id="468d4-112">Toliau pateiktose ekrano nuotraukose parodyta, kaip ER formatų peržvalgos laukas atrodo puslapyje **Užsienio prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="468d4-112">The screenshots below show how the ER formats lookup field looks like in the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="468d4-113">Jeigu dabartiniame „Finance“ egzemplioriuje nėra ER formatų, susijusių su Intrastat verslo procesu, šis peržvalgos laukas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="468d4-113">If the current Finance instance contains no Intrastat business process related ER formats, this lookup field will be empty.</span></span>

<span data-ttu-id="468d4-114">[![Puslapis Užsienio prekybos parametrai](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span><span class="sxs-lookup"><span data-stu-id="468d4-114">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span></span>

<span data-ttu-id="468d4-115">Jeigu dabartiniame „Finance“ egzemplioriuje yra ER formatų, susijusių su Intrastat verslo procesu, šiame peržvalgos lauke pateikiami ER formatai.</span><span class="sxs-lookup"><span data-stu-id="468d4-115">If the current Finance instance contains Intrastat business process related ER formats, this lookup field offers the ER formats.</span></span>

<span data-ttu-id="468d4-116">[![Puslapis Užsienio prekybos parametrai](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-116">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span></span>

<span data-ttu-id="468d4-117">Šioje peržvalgoje pateikiami tik tie ER formatai, kurie jau importuoti į dabartinį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="468d4-117">This lookup offers only the ER formats that have already been imported to the current Finance instance.</span></span> <span data-ttu-id="468d4-118">Norėdami [importuoti](./tasks/er-import-configuration-lifecycle-services.md) ER sprendimus į dabartinį „Finance“ egzempliorių, turite turėti teises vykdyti atitinkamą ER sistemos funkciją, kuri palaiko ER sprendimų, kuriuose yra ER formatų, [ciklą](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="468d4-118">To [import](./tasks/er-import-configuration-lifecycle-services.md) ER solutions to the current Finance instance, you need to have permissions to run the appropriate function of the ER framework that supports the [lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md) of ER solutions that contain ER formats.</span></span>

<span data-ttu-id="468d4-119">Pradedant nuo „Finance“ 10.0.9 versijos (2020 balandžio mėn. leidimo), ER formato peržvalgos, įgyvendinamos naudojant ER sistemos API, vartotojo sąsaja buvo patobulinta.</span><span class="sxs-lookup"><span data-stu-id="468d4-119">Starting in the Finance version 10.0.9 (April 2020 release), the user interface of the ER format lookup that is implemented by using the ER framework API, has been extended.</span></span> <span data-ttu-id="468d4-120">Vis tiek galite pasirinkti esamus ER formatus, kurie yra „FastTab“ **Pasirinkti formato konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="468d4-120">You can still select the existing ER formats, which on the **Select format configuration** FastTab.</span></span> <span data-ttu-id="468d4-121">Be to, išplėstinėje peržvalgoje suteikiama nauja parinktis ieškoti bendrojoje saugykloje (BS) norint rasti konkrečių ER formatų.</span><span class="sxs-lookup"><span data-stu-id="468d4-121">In addition to that, the extended lookup offers the new option to search the Global repository (GR) to locate specific ER formats.</span></span> <span data-ttu-id="468d4-122">Visi BS esantys ER formatai pateikiami „FastTab“ **Importuoti iš bendrosios saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="468d4-122">All ER formats of the GR are offered on the **Import from Global repository** FastTab.</span></span>

<span data-ttu-id="468d4-123">[![Puslapis Užsienio prekybos parametrai](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-123">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span></span>

<span data-ttu-id="468d4-124">Panašiai kaip ir „FastTab“ **Pasirinkti formato konfigūraciją**, „FastTab“ **Importuoti iš bendrosios saugyklos** rodomi tik tie ER formatai, kurie taikomi verslo procesui, kuriam šiame peržvalgos lauke yra pasirinktas ER formatas.</span><span class="sxs-lookup"><span data-stu-id="468d4-124">Similar to the **Select format configuration** FastTab, the **Import from Global repository** FastTab shows only the ER formats that are applicable to the business process for which an ER format is selected in this lookup field.</span></span> <span data-ttu-id="468d4-125">Šiame pavyzdyje – Intrastat deklaracijos generavimas.</span><span class="sxs-lookup"><span data-stu-id="468d4-125">In this example, the generation of Intrastat declaration.</span></span> <span data-ttu-id="468d4-126">ER formatas taikomas įmonei, prie kurios vartotojas yra šiuo metu prisijungęs, atsižvelgiant į įmonės šalies kontekstą.</span><span class="sxs-lookup"><span data-stu-id="468d4-126">The ER format is applicable for the company to which the user is currently signed in, depending on the company country context.</span></span>

<span data-ttu-id="468d4-127">Kai pasirenkate ER formatą „FastTab“ **Importuoti iš bendrosios saugyklos**, pasirinkta ER formato [konfigūracija](general-electronic-reporting.md#Configuration) importuojama iš BS į dabartinį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="468d4-127">When you select an ER format on the **Import from Global repository** FastTab, the selected ER format [configuration](general-electronic-reporting.md#Configuration) is imported from the GR to the current Finance instance.</span></span>

<span data-ttu-id="468d4-128">[![Puslapis Užsienio prekybos parametrai](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-128">[![Foreign trade parameters page](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span></span>

<span data-ttu-id="468d4-129">Tada, jei importavimas atliekamas sėkmingai, nuoroda į importuotą ER formatą saugoma šiame peržvalgos lauke.</span><span class="sxs-lookup"><span data-stu-id="468d4-129">Then, if the import completes successfully, the reference to the imported ER format is stored in this lookup field.</span></span> <span data-ttu-id="468d4-130">Atkreipkite dėmesį, kad pirmą kartą norėdami pasiekti BS, turite pereiti pateiktu saitu, kad užsiregistruotumėte [„Regulatory Configuration Service“](https://aka.ms/rcs) (RCS), kuri naudojama prieigai prie BS valdyti.</span><span class="sxs-lookup"><span data-stu-id="468d4-130">Note that when you access the GR for the first time, you need to follow the link provided to sign up for the [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) that is used to manage access to the GR storage.</span></span>

<span data-ttu-id="468d4-131">[![Puslapis Užsienio prekybos parametrai](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-131">[![Foreign trade parameters page](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span></span>

<span data-ttu-id="468d4-132">Pagal numatytuosius nustatymus „FastTab“ **Importuoti iš bendrosios saugyklos** pateikiamas sąrašas ER formatų iš laikinos saugyklos, kuri automatiškai sukuriama pagal BS turinį našumui patobulinti.</span><span class="sxs-lookup"><span data-stu-id="468d4-132">By default, the **Import from Global repository** FastTab presents the list of ER formats from the temporary storage that is automatically created based on the GR content for performance improvements.</span></span> <span data-ttu-id="468d4-133">Tai atsitinka, kai „FastTab“ **Importuoti iš bendrosios saugyklos** atidaromas pirmą kartą, o tai gali užtrukti keletą sekundžių.</span><span class="sxs-lookup"><span data-stu-id="468d4-133">This happens when the **Import from Global repository** FastTab is opened the first time, which may take several seconds.</span></span>

<span data-ttu-id="468d4-134">Jei „FastTab“ **Importuoti iš bendrosios saugyklos** nematote reikiamo ER formato, bet esate tikri, kad šis ER formatas saugomas BS, pasirinkite parinktį **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="468d4-134">If you do not see the required ER format in the **Import from Global repository** FastTab, but you are sure that this ER format is stored in the GR, select the **Synchronize** option.</span></span> <span data-ttu-id="468d4-135">Taip atnaujinsite laikiną saugyklą ir sinchronizuosite ją su dabartiniu BS turiniu.</span><span class="sxs-lookup"><span data-stu-id="468d4-135">This will update the temporary storage and synchronize it with the current content of the GR.</span></span>

## <a name="feature-activation"></a><span data-ttu-id="468d4-136">Funkcijų aktyvinimas</span><span class="sxs-lookup"><span data-stu-id="468d4-136">Feature activation</span></span>

<span data-ttu-id="468d4-137">Šios funkcijos pasiekiamumas valdomas funkcijoje **Išplėstinė ER formato konfigūracijų peržvalga, leidžianti pateikti užklausą į bendrąją saugyklą**, esančioje puslapyje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="468d4-137">The availability of this functionality is controlled by the feature **Extended lookup of ER format configurations allowing to inquire the Global repository** in the **Feature management**.</span></span> <span data-ttu-id="468d4-138">Pagal numatytuosius nustatymus ši funkcija įjungta.</span><span class="sxs-lookup"><span data-stu-id="468d4-138">This feature is enabled by default.</span></span>

<span data-ttu-id="468d4-139">[![Puslapis Funkcijų valdymas](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-139">[![Feature management page](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span></span>

## <a name="security-considerations"></a><span data-ttu-id="468d4-140">Saugos klausimai</span><span class="sxs-lookup"><span data-stu-id="468d4-140">Security considerations</span></span>

<span data-ttu-id="468d4-141">Teisė **Prižiūrėti konfigūracijų saugyklas** (**ERMaintainSolutionRepositories**) valdo vartotojo, atidarančio ER formatų peržvalgą su įgalintu „FastTab“ **Importuoti iš bendrosios saugyklos**, prieigą prie BS.</span><span class="sxs-lookup"><span data-stu-id="468d4-141">The **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege controls access to the GR for a user opening the ER format lookup with the enabled **Import from Global repository** FastTab.</span></span> <span data-ttu-id="468d4-142">Kad vartotojai galėtų pasiekti BS turinį iš ER formatų peržvalgų, turite pakeisti saugos parametrus, suteikdami vartotojams teisę **ERMaintainSolutionRepositories** arba tiesiogiai, arba naudodami jau priskirtus vaidmenis ir pareigas.</span><span class="sxs-lookup"><span data-stu-id="468d4-142">To allow users to access the GR content from the ER format lookups, you need to change the security settings by granting the **ERMaintainSolutionRepositories** privilege to users either directly or by using already assigned roles and duties.</span></span>

<span data-ttu-id="468d4-143">Toliau pateikiamoje ekrano nuotraukoje parodyta, kaip šią teisę suteikti vartotojams, kuriems priskirtas vaidmuo **Buhalteris**.</span><span class="sxs-lookup"><span data-stu-id="468d4-143">The following screenshot shows how this privilege can be granted to users who are assigned to the **Accountant** role.</span></span> <span data-ttu-id="468d4-144">Šis vaidmuo leidžia vartotojams konfigūruoti užsienio prekybos parametrus ir nustatyti nuorodas į ER formatus laukuose **Failo formato susiejimas** ir **Ataskaitos formato susiejimas** puslapyje **Užsienio prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="468d4-144">This role makes allows users to configure foreign trade parameters and set up references to the ER formats in the **File format mapping** and **Report format mapping** fields on the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="468d4-145">[![Puslapis Saugos konfigūracija](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span><span class="sxs-lookup"><span data-stu-id="468d4-145">[![Security configuration page](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="468d4-146">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="468d4-146">Limitations</span></span>

<span data-ttu-id="468d4-147">Prieiga prie BS ER formatų peržvalgoje šiuo metu palaikoma tik ER formatų, naudojamų siunčiamiems dokumentams generuoti, atveju.</span><span class="sxs-lookup"><span data-stu-id="468d4-147">Access to the GR in the ER format lookup is currently only supported for the selection of ER formats that are used to generate outbound documents.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="468d4-148">Dažnai užduodami klausimai</span><span class="sxs-lookup"><span data-stu-id="468d4-148">Frequently asked questions</span></span>

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a><span data-ttu-id="468d4-149">Kodėl negaliu pasiekti bendrosios saugyklos iš ER formatų peržvalgos?</span><span class="sxs-lookup"><span data-stu-id="468d4-149">Why can't I access the Global repository from the ER format lookup?</span></span>

<span data-ttu-id="468d4-150">Jei įgalinote funkciją **Išplėstinė ER formato konfigūracijų peržvalga, leidžianti pateikti užklausą į bendrąją saugyklą** puslapyje **Funkcijų valdymas**, tačiau vartotojai nemato ER formatų „FastTab“ **Importuoti iš bendrosios saugyklos**, o parinktis **Sinchronizuoti** matoma, bet išjungta, įsitikinkite, kad vartotojui suteikta teisė **Prižiūrėti konfigūracijų saugyklas** (**ERMaintainSolutionRepositories**).</span><span class="sxs-lookup"><span data-stu-id="468d4-150">If you have enabled the **Extended lookup of ER format configurations allowing to inquire the Global repository** feature on the **Feature management** page, but users can't see ER formats on the **Import from Global repository** FastTab and the **Synchronize** option is visible but disabled, make sure that the **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege has been granted to the user.</span></span> <span data-ttu-id="468d4-151">Kreipkitės į sistemos administratorių, kad jums būtų suteikta ši teisė.</span><span class="sxs-lookup"><span data-stu-id="468d4-151">Contact your system administrator to receive this privilege.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="468d4-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="468d4-152">Additional resources</span></span>

- [<span data-ttu-id="468d4-153">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="468d4-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="468d4-154">Elektroninių ataskaitų (ER) sistemos API</span><span class="sxs-lookup"><span data-stu-id="468d4-154">Electronic reporting (ER) framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="468d4-155">Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas</span><span class="sxs-lookup"><span data-stu-id="468d4-155">Manage Electronic reporting (ER) configurations lifecycle</span></span>](general-electronic-reporting-manage-configuration-lifecycle.md)