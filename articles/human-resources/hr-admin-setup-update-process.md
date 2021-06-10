---
title: Atnaujinimo procesas
description: „Microsoft Dynamics 365 Human Resources“ yra tipiška programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus, skirtus programai ir platformai keisti.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053640"
---
# <a name="update-process"></a><span data-ttu-id="f8ac0-103">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="f8ac0-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f8ac0-104">„Microsoft Dynamics 365 Human Resources“ yra puiki programinės įrangos nuomos paslauga („SaaS“), teikianti nepertraukiamus, bekontakčius paslaugų naujinimus.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="f8ac0-105">Šiuose naujinimuose yra programos ir platformų keitimų, kurie dažnai teikia esminius paslaugų pagerinimus, įskaitant reguliavimo naujinimus.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="f8ac0-106">Naujinimo strategija</span><span class="sxs-lookup"><span data-stu-id="f8ac0-106">Update policy</span></span>

<span data-ttu-id="f8ac0-107">Naujinimai išleidžiami reguliariais intervalais visoms aplinkoms.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="f8ac0-108">„Human Resources“ palaikoma atsižvelgiant į [„Microsoft Lifecycle“ strategiją](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kuri numato nuoseklias ir prognozuojamas palaikymo pasiekiamumo gaires.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="f8ac0-109">Leidimo intervalai</span><span class="sxs-lookup"><span data-stu-id="f8ac0-109">Release cadence</span></span> 

<span data-ttu-id="f8ac0-110">„Human Resources“ naujinimai taikomi visoms aplinkoms automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="f8ac0-111">„Human Resources“ teikia dviejų tipų leidimus:</span><span class="sxs-lookup"><span data-stu-id="f8ac0-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="f8ac0-112">**Paslaugų naujinimai**: naujinimai, kuriuose yra klaidų taisymai ir naujos funkcijos, vykdomi kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="f8ac0-113">Į paslaugos naujinimus taip pat įtraukiami taikomi platformų naujinimai, kai jie išleidžiami.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="f8ac0-114">Norėdami sužinoti, kada platformų naujinimai išleidžiami, žr. [3 lentelė: platformų leidimai](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="f8ac0-115">Naujinimai kas dvi savaites regionuose bus įdiegti etapais.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="f8ac0-116">Daugiau informacijos apie naujinimus kas dvi savaites žr. [Kas nauja arba pasikeitė programoje „Dynamics 365 Human Resources“](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="f8ac0-117">Visi palaikomi duomenų centrai teikia naujinimus kas dvi savaites, nebent nurodyta kitaip.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="f8ac0-118">JAV, Australija, Europa, JK, Azija ir Kanada yra įtraukiamos į naujinimus, vykdomus kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="f8ac0-119">**„Dataverse“ sprendimų naujinimai**: šie naujinimai vykdomi maždaug kas šešios savaitės, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="f8ac0-120">Juose yra naujų objektų ir esamų objektų, esančių „Dataverse“, keitimų.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="f8ac0-121">Šie naujinimai išleidžiami tuose pačiuose regionuose kaip ir naujinimams, vykdomiems kas dvi savaites, bei užtrunka apie šešias savaites, kol jie dubliuojami visuose duomenų centruose.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="f8ac0-122">Sprendimų naujinimai sutampa arba nesutampa su paslaugų naujinimais, vykdomais kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="f8ac0-123">Sprendimų naujinimai pasiekiami visuose duomenų centruose, kai jie išleidžiami.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="f8ac0-124">Jei nenorite laukti, kol naujinimai bus dubliuojami automatiškai, galite rankiniu būdu taikyti šiuos naujinimus bet kuriai aplinkai bet kuriame duomenų centre.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="f8ac0-125">Kai reikia, „Human Resources“ taip pat teikia šiuos taisymų tipus:</span><span class="sxs-lookup"><span data-stu-id="f8ac0-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="f8ac0-126">**Tikslinimas (karštosios pataisos)**: klaidų pataisos, kurios gali būti vykdomos kartu su paslaugų naujinimo kas dvi savaites leidimu arba atskirai nuo jo</span><span class="sxs-lookup"><span data-stu-id="f8ac0-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="f8ac0-127">**Avarinis taisymas**: aktyvios ir reaktyviosios karštosios pataisos, kurios yra įprastai vykdomos atskirai, gali apimti tik konfigūracijų arba kodo keitimus, siekiant išspręsti tiesiogines svetainės problemas ir gali būti taikomos atskirai nuo paslaugų naujinimo kas dvi savaites leidimo</span><span class="sxs-lookup"><span data-stu-id="f8ac0-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="f8ac0-128">Leidimai yra peržiūrimi, tikrinami ir patvirtinami vidinėje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="f8ac0-129">Kai atsijungiama nuo komponavimo versijų, jos bus įdiegtos gamybai.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="f8ac0-130">Numatomi išleidimo intervalai 2021 m.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="f8ac0-131">Norint atsiskaityti už atostogas, toliau pateiktas 2021 m. lapkričio ir gruodžio mėn. leidimų grafikas.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="f8ac0-132">Lapkričio mėn. leidimas: lapkričio 1 d. – lapkričio 14 d.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="f8ac0-133">Gruodžio mėn. leidimas: lapkričio 29 d. – gruodžio 12 d.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="f8ac0-134">Dviejų savaičių išleidimo intervalai bus tęsiami kaip įprasta 2022 m. sausio 10 d.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="f8ac0-135">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="f8ac0-135">Communications</span></span>

<span data-ttu-id="f8ac0-136">Galite sužinoti, kas rengiama programai „Human Resources“ ir ką išleidome, šiose vietose:</span><span class="sxs-lookup"><span data-stu-id="f8ac0-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="f8ac0-137">„Dynamics 365 Human Resources“ veiksmų planas</span><span class="sxs-lookup"><span data-stu-id="f8ac0-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="f8ac0-138">„Dynamics 365“ leidimo planai</span><span class="sxs-lookup"><span data-stu-id="f8ac0-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="f8ac0-139">Kas nauja arba pasikeitė „Dynamics 365 Human Resources“</span><span class="sxs-lookup"><span data-stu-id="f8ac0-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="f8ac0-140">[Problemų ieška portale „Lifecycle Services“ (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (tik su platforma susijusioms klaidoms)</span><span class="sxs-lookup"><span data-stu-id="f8ac0-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="f8ac0-141">„Human Resources“ tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="f8ac0-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="f8ac0-142">„Human Resources“ „Yammer“ bendruomenė</span><span class="sxs-lookup"><span data-stu-id="f8ac0-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="f8ac0-143">Peržiūros funkcijos smėlio dėžės aplinkoje</span><span class="sxs-lookup"><span data-stu-id="f8ac0-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="f8ac0-144">Galite patikrinti peržiūros funkcijas smėlio dėžės aplinkoje prieš įjungdami jas savo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="f8ac0-145">Daugiau informacijos apie naujų funkcijų įjungimą žr. temoje [Funkcijų valdymo apžvalga](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="f8ac0-146">Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="f8ac0-147">Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="f8ac0-148">Kai tik pradedame naujas galimybes darbo srityje Funkcijų valdymas, galite jas įjungti.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="f8ac0-149">Kai kurios funkcijos gali būti pagal numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-149">Some features may be on by default.</span></span>

<span data-ttu-id="f8ac0-150">Kartais integrali funkcija bus įjungta pagal numatytuosius nustatymus ir jos nebus galima išjungti (pavyzdžiui, darbo sritis Funkcijų valdymas).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="f8ac0-151">Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="f8ac0-152">Darbo sritis Funkcijų valdymas nurodo, kada peržiūros funkcija taps privaloma.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="f8ac0-153">Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="f8ac0-154">Negalite išjungti privalomų funkcijų.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="f8ac0-155">Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="f8ac0-156">Primygtinai rekomenduojame peržiūrėti funkcijas, esančias smėlio dėžės arba bandomojoje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="f8ac0-157">Geriausia sukurti savo esamos gamybos aplinkos arba duomenų bazės kopiją į smėlio dėžės aplinką, kad galėtumėte gauti visą naujų funkcijų su savo duomenimis patirtį.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="f8ac0-158">Norėdami gauti daugiau informacijos apie smėlio dėžės aplinkos parengimą, žr. [„Human Resources“ projekto parengimas](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="f8ac0-159">Norėdami pašalinti tikrinimo aplinką, žr. [Egzemplioriaus šalinimas](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="f8ac0-160">Pranešimas apie klaidas</span><span class="sxs-lookup"><span data-stu-id="f8ac0-160">Report bugs</span></span>

<span data-ttu-id="f8ac0-161">Tikrindami peržiūros funkcijas arba išbandydami naujas galimybes, galite aptikti elementų, neveikiančių taip, kaip tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="f8ac0-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="f8ac0-162">Praneškite apie klaidas per [„Microsoft Dynamics 365“ palaikymą](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="f8ac0-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="f8ac0-163">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f8ac0-163">See also</span></span>

[<span data-ttu-id="f8ac0-164">„Dynamics 365“ ir „Power Platform“ leidimo planai</span><span class="sxs-lookup"><span data-stu-id="f8ac0-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="f8ac0-165">Kas nauja ar pasikeitė programoje „Dynamics 365 Human Resources”</span><span class="sxs-lookup"><span data-stu-id="f8ac0-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f8ac0-166">Programinės įrangos ciklo strategija</span><span class="sxs-lookup"><span data-stu-id="f8ac0-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]