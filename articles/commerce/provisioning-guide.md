---
title: „Dynamics 365 Commerce” smėlio dėžės aplinkos parengimas
description: Šiame straipsnyje paaiškinama, kaip parengti sandų Microsoft Dynamics 365 Commerce dėžės aplinką demonstracinių arba sandų dėžės naudojimui su įtaisytais demonstraciniais duomenimis.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283647"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>„Dynamics 365 Commerce” smėlio dėžės aplinkos parengimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip reikėtų parengti sandų Microsoft Dynamics 365 Commerce dėžės aplinką, kad būtų galima naudoti demonstracinį naudojimą su įdiegtais demonstraciniai duomenimis. Gamybos aplinkos nustatymo procesas yra panašus, bet jis labiau išsamus, nes daugelis sandingo aplinkos sąlygų jau yra pateiktos demonstraciniai duomenys.

Prieš pradedant rekomenduojame greitai nuskaityti šį straipsnį, kad gautumėte supratimą, ko reikalauja procesas.

Norėdami sėkmingai parengti "Commerce sandbox" aplinką, turite nurodyti kai kuriuos aplinkos ir "Commerce Scale Unit" (CSU) parametrus, kurie bus naudojami su "Commerce" vėliau. Šiame straipsnyje pateikiamose instrukcijose aprašomi visi žingsniai, kurie reikalingi norint atlikti parengimą, ir parametrai, kuriuos turite naudoti.

Sėkmingai su paruošę savo "Commerce" aplinką, turite atlikti keletą po paruošimo etapų, kad būtų galima naudoti. Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į sistemos aspektus, kuriuos norite naudoti. Visada galite atlikti pasirinktinius veiksmus vėliau.

Daugiau informacijos apie "Commerce" aplinkos konfigūravimą po konfigūravimo ieškokite " [Commerce sandbox" aplinkos konfigūravimas](cpe-post-provisioning.md). Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti pasirinktines "Commerce" aplinkos funkcijas, žr. " [Commerce Sandbox" aplinkos pasirinktinių funkcijų konfigūravimas](cpe-optional-features.md).

## <a name="prerequisites"></a>Būtinieji komponentai

Kad būtų galima nustatyti savo Commerce aplinką, turite įdiegti toliau nurodytus būtinuosius komponentus:

- Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.
- Jūs esate esamas Microsoft Dynamics 365 partneris arba klientas ir turite diegimo projektą, kurį galima naudoti LCS.  
- Sukūrėte () Azure Active Directory saugos Azure AD grupę, kurią galima naudoti kaip komercijos sistemos administratorių grupę ir kurios ID yra.
- Jūs sukūrėte saugos Azure AD grupę, kurią galima naudoti kaip vertinimus ir peržiūrėti moderatoriaus grupę, ir turite jos ID. (Ši saugos grupė gali būti tokia pati kaip ir Komercijos sistemos administratoriaus grupė.)
- Jūsų LCS įdiegtas būstinės egzempliorius. Norėdami gauti daugiau informacijos, žr [. Deploy naują aplinką](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Atkreipiame dėmesį, kad šis sąrašas nėra baigtinis. Jei turite problemų, susisiekite su „Microsoft“ partnerio pagalbos centru.

## <a name="provision-your-commerce-environment"></a>Komercijos aplinkos parengimas

Šiose procedūrose paaiškinama, kaip pateikti komercijos aplinką. Sėkmingai atlikus veiksmus jūsų "Commerce" aplinka bus parengta konfigūruoti. Visi toliau aprašyti veiksmai atlikti LCS portale.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Inicijuoti „Commerce Scale Unit“ (debesyje)

Norėdami pradėti CSU, atlikite šiuos veiksmus.

1. LCS iš sąrašo pasirinkite aplinką.
1. Dešinėje pusėje **pateiktame rodinyje ENVIRONMENTS** pasirinkite Išsami **informacija**. Rodomas aplinkos išsamios informacijos rodinys.
1. Aplinkos funkcijų **skyriuje Aplinkos valdymas** pasirinkite **Valdyti** **.**
1. Skirtuke **"Commerce Scale Units** " pasirinkite **Inicijuoti**. Rodomas rodinys **Įtraukti skalės** vienetą.
1. **Lauke REGIONAS** pasirinkite regioną, kuris yra toks pats arba artimas regionui, kuriame į kurią diegiate aplinką.
1. Versijos išplečiamajame **sąraše** pasirinkite naujausią galimą versiją.
1. Pasirinkite **Inicijuoti**.
1. Perspėjimo dialogo lange, kuriame prašoma patvirtinti komercijos skalės vieneto žymėjimą, pasirinkite **Taip**. CSU laukimo eilėje jau yra, kad būtų galima parengti.
1. Prieš tęsdami įsitikinkite, kad jūsų CSU būsena yra **SĖKMINGA**. Inicijavimas trunka maždaug dvi–penkias valandas.

Jei negalite surasti **Tvarkyti** nuorodos aplinkos informacijos peržiūroje, susisiekite su savo „Microsoft“ pagalbos centru.

### <a name="initialize-e-commerce"></a>El. prekybos inicijavimas

Norėdami inicijuoti "Commerce", atlikite šiuos veiksmus.

1. Skirtuke **El. prekyba** pasirinkite **Sąranka**.
1. **„e-Commerce“ aplinkos pavadinimas** laukelyje, įveskite pavadinimą. Būkite atsargūs, nes šis pavadinimas bus rodomas kai kuriuose URL nuorodose, kurios veda į jūsų „e-Commerce“ objektą.
1. Lauke **„Commerce Scale Unit“ pavadinimas** iš sąrašo pasirinkite savo CSU. (Sąraše turėtų būti tik viena parinktis.)

    **„e-Commerce“ geografija** laukelis nustatomas automatiškai.

1. Pasirinkite **Pirmyn**, kad tęstumėte.
1. Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.
1. **AAD saugos grupė sistemos administratoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai. Pasirinkite tinkamą saugos grupę sąraše.
1.  **AAD saugos grupė reitingavimo ir peržiūros moderatoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai. Pasirinkite tinkamą saugos grupę sąraše.
1. Palikite **Reitingavimo ir peržiūros paslaugų įjungimas** parinktį nustatytą į **Taip**.
1. Pasirinkite **Inicijuoti**. Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“**. „E-Commerce“ inicijavimas pradėtas.
1. Prieš tęsdami palaukite, kol komercijos inicijavimo būsena bus **sėkminga**.
1. Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.

    * **„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.
    * **Komercijos vietos kūrėjas** – Nuoroda į vietos valdymo įrankį.

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti "Commerce" aplinkos konfigūravimo ir konfigūravimo procesą, žr. " [Commerce sandbox" aplinkos konfigūravimą](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Sandbox aplinkos Dynamics 365 Commerce konfigūravimas](cpe-post-provisioning.md)

[Konfigūruoti BOPIS sandūrų Dynamics 365 Commerce saugyklos aplinkoje](cpe-bopis.md)

[Konfigūruokite pasirinktines sandūrų Dynamics 365 Commerce aplinkos priemones](cpe-optional-features.md)

[„Microsoft Lifecycle Services“ (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Commerce Scale Unit“ (debesyje)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
