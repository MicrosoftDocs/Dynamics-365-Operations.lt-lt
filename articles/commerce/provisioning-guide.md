---
title: „Dynamics 365 Commerce“ vertinimo aplinkos parengimas
description: Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969906"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>„Dynamics 365 Commerce“ vertinimo aplinkos parengimas

[!include [banner](includes/banner.md)]

Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.

Prieš pradedant konfigūraciją, rekomenduojame perskaityti šią temą, kad suprastumėte proceso eigą.

> [!NOTE]
> Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskyru jų prašymu. Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.

## <a name="overview"></a>Peržiūra

Tam, kad sėkmingai parengtumėte Komercijos vertinimo aplinką privalote sukurti projektą, kuris turi konkretų gaminio pavadinimą ir tipą. Aplinka ir „Commerce Scale Unit“ (CSU) taip pat turi keletą specifinių parametrų, kuriuos privalote naudoti tikėdamiesi vėliau nustatyti „e-Commerce“. Šioje temoje pateiktos instrukcijos aprašo visus žingsnius būtinus užbaigti jūsų privalomą naudoti parengimą ir parametrus.

Kai sėkmingai parengėte savo Komercijos vertinimo aplinką, privalote užbaigti keletą žingsnių po nustatymo tam, kad pasirengtumėte naudojimui. Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti. Visada galite atlikti pasirinktinius veiksmus vėliau.

Dėl informacijos, kaip konfigūruoti savo Komercijos vertinimo aplinką po jos parengimo, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md). Dėl informacijos, kaip konfigūruoti pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [CKonfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).

## <a name="prerequisites"></a>Būtinieji komponentai

Toliau pateikti būtinieji komponentai privalo būti pritaikyti prieš jūsų Komercijos vertinimo aplinkos nustatymo:

- Buvote priimtas į vertinimo programą ir jums suteiktos galimybės vertinimo aplinkoje.
- Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.
- Esate „Microsoft Dynamics“ 365 partneris ar klientas ir galite sukurti „Dynamics 365 Commerce“ projektą.
- Jūs turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos ir galite susisiekti su jos administratoriumi, kuris pagelbės jums esant poreikiui.
- Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.
- Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.
- Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID. (Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)

Atkreipiame dėmesį, kad šis sąrašas nėra baigtinis. Jei turite problemų, susisiekite su „Microsoft“ partnerio pagalbos centru.

## <a name="provision-your-commerce-evaluation-environment"></a>Parenkite savo Komercijos vertinimo aplinką

Šios procedūros paaiškina, kaip galite parengti Komercijos vertinimo aplinką. Po to, kai jas sėkmingai atliksite, Komercijos vertinimo aplinka bus parengta konfigūravimui. Visos čia aprašytos veiklos vyksta LCS portale.

### <a name="create-a-new-project"></a>Kurti naują projektą

Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.

1. LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.
1. Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.

    - Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.
    - Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.

1. Įveskite pavadinimą, aprašą ir pramonės šaką.
1. Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Commerce**.
1. Lauke **Produkto versija** pasirinkite **Dynamics 365 Commerce**.
1. Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.
1. Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.
1. Pasirinkite **Kurti**. Pateikiamas projekto rodinys.

### <a name="add-the-azure-connector"></a>„Azure“ jungties įtraukimas

„Azure Connector“ įtraukimui į savo LCS projektą, atlikite šiuos žingsnius [Baigtame „Azure Resource Manager“ (ARM) įtraukimo procese](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>Aplinkos diegimas

Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.

> [!NOTE]
> Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami. Kai esate rodinyje **Aplinkos parametrai**, įsitikinkite, kad tekstas **Dynamics 365 Commerce – Demo (10.0.* x* su platformos atnaujinimu *xx*)** rodomas tiesiai virš lauko **Aplinkos pavadinimas**. Norėdami gauti išsamesnės informacijos, žr. iliustraciją, pavaizduotą po 8 veiksmo.

1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.
1. Lauke **Programos versija** pasirinkite naujausią versiją. Jei norite pasirinkti ne naujausią programos versiją, nesirinkite versijos, ankstesnės nei versija **10.0.14**.
1. Lauke **Platformos versija** naudokite platformos versiją, kuri automatiškai parenkama jūsų pasirinktai programos versijai. 

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. Pasirinkite **Toliau**.
1. Pasirinkite aplinkos topologiją **Demonstracinė versija**.

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą. Nekeiskite išplėstinių parametrų.

    ![Puslapis Diegti aplinką](./media/project4.png)

1. Pagal poreikį pakoreguokite VM dydį. (Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)
1. Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.
1. Pasirinkite **Toliau**.
1. Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**. Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.

    Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama. Aplinkos darbo eigoms užbaigti prireiks laiko. Todėl patikrinkite vėl maždaug po šešių–devynių valandų.

1. Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Inicijuoti „Commerce Scale Unit“ (debesyje)

Norėdami pradėti CSU, atlikite šiuos veiksmus.

1. Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.
1. Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**. Rodomas aplinkos išsamios informacijos rodinys.
1. Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.
1. Skirtuke **„Commerce“** pasirinkite **Inicijuoti**. Rodomas CSU inicijavimo parametrų rodinys.
1. **Regiono** laukelyje pasirinkite tą patį regioną arba artimą regioną, kuriame įdiegėte savo aplinką.
1. Palikite **Versija** laukelį tokį, koks yra.
1. Pasirinkite **Inicijuoti**.
1. Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**. Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„Commerce“**. Jūsų CSU jau buvo rengimo eilėje.
1. Prieš tęsdami įsitikinkite, kad jūsų CSU būsena yra **Pavyko**. Inicijavimas trunka maždaug dvi–penkias valandas.

Jei negalite surasti **Tvarkyti** nuorodos aplinkos informacijos peržiūroje, susisiekite su savo „Microsoft“ pagalbos centru.

Talpinimo proceso metu, galite gauti šią klaidos žinutę:

> Demonstracinės ar testinės aplinkos vertinimas turi būti registruojamas skalės vieneto jungties programoje \<application ID\> būstinėje.

Jei CSU pradžia nepavyksta ir gaunate šią klaidos žinutę, užsirašykite programos ID, kuris bendrai yra unikalus identifikatorius (GUID) ir tuomet atlikite veiksmus kitame skyriuje siekiant registruoti CSU talpinimo programą „Commerce“ būstinėje.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Registruoktie CSU talpinimo programą „Commerce“ būstinėje (jei būtina)

Norėdami registruoti CSU talpinimo programą „Commerce“ būstinėje, imkitės šių veiksmų.

1. „Commerce“ būstinėje, eikite į **Sistemos administravimas \> Nustatymai \> „Azure Active Directory“ programos**.
1. Stulpelyje **Kliento Id** įveskite programos ID iš CSU pradžios klaidos pranešimo, kurį gavote.
1. Stulpelyje **Pavadinimas** įveskite bet kokį aprašantį tekstą (pavyzdžiui, **„CSU Eval“**).
1. Stulpelyje **Vartotojo ID** įveskite **RetailServiceAccount**.
1. Dar kartą bandykite CSU pradžia ir talpinimas iš LCS.

### <a name="initialize-e-commerce"></a>El. prekybos inicijavimas

Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.

1. **e-Commerce** skirtuke peržiūrėkite vertinimo sutikimą ir tuomet pasirinkite **Sąranka**.
1. **„e-Commerce“ aplinkos pavadinimas** laukelyje, įveskite pavadinimą. Būkite atsargūs, nes šis pavadinimas bus rodomas kai kuriuose URL nuorodose, kurios veda į jūsų „e-Commerce“ objektą.
1. Lauke **„Commerce Scale Unit“ pavadinimas** iš sąrašo pasirinkite savo CSU. (Sąraše turėtų būti tik viena parinktis.)

    **„e-Commerce“ geografija** laukelis nustatomas automatiškai.

1. Pasirinkite **Pirmyn**, kad tęstumėte.
1. Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.
1. **AAD saugos grupė sistemos administratoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai.  Pasirinkite tinkamą saugos grupę sąraše.
1.  **AAD saugos grupė reitingavimo ir peržiūros moderatoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai.  Pasirinkite tinkamą saugos grupę sąraše.
1. Palikite **Reitingavimo ir peržiūros paslaugų įjungimas** parinktį nustatytą į **Taip**.
1. Pasirinkite **Inicijuoti**. Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“**. „E-Commerce“ inicijavimas pradėtas.
1. Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.
1. Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.

    * **„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.
    * **Komercijos vietos kūrėjas** – Nuoroda į vietos valdymo įrankį.

## <a name="next-steps"></a>Kiti veiksmai

Jūsų Komercijos vertinimo aplinkos parengimo ir konfigūravimo proceso tąsai, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką](cpe-post-provisioning.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)

[„Dynamics 365 Commerce“ vertinimo aplinkos DUK](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Commerce Scale Unit“ (debesyje)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]