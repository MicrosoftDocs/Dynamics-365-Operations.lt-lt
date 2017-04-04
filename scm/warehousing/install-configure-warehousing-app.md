---
title: "Įdiegti ir konfigūruoti Microsoft Dynamics 365 operacijų & #8211; Sandėliavimo"
description: "Šioje temoje aprašoma, kaip įdiegti ir konfigūruoti Microsoft Dynamics 365 operacijų - sandėliavimo."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Įdiegti ir konfigūruoti Microsoft Dynamics 365 operacijų & #8211; Sandėliavimo

Šioje temoje aprašoma, kaip įdiegti ir konfigūruoti Microsoft Dynamics 365 operacijų - sandėliavimo.

Operacijų - sandėliavimo 365 dinamika yra programą galite rasti "Google Play Store" ir "Windows" parduotuvės. Dabartinės versijos Microsoft Dynamics 365 operacijoms, ši programa pateikiama kaip atskira sudedamoji, o tai reiškia, savarankiškai diegti įrenginiuose naudojamos sandėlio užduotys. Norint naudotis programa Dynamics 365 veiklos aplinką, turite atsisiųsti programėlę kiekviename įrenginyje ir konfigūruoti ją prijungti prie savo dinamika 365 veiklos aplinkoje. Šioje temoje aprašoma, kaip įdiegti programėlę savo įrenginiuose. Taip pat paaiškinama, kaip sukonfigūruoti programėlę, kad prisijungti prie jūsų Dynamics 365 veiklos aplinkoje.

## <a name="prerequisites"></a>Būtinieji komponentai
Programėlė yra prieinama "Android" ir "Windows" operacinėse sistemose. Norint naudoti šią programą, turite vieną iš šių palaikomų operacinių sistemų įdiegti įrenginiuose. Taip pat turite vieną iš šių palaikomų versijų Dynamics 365 operacijoms. Naudokite informaciją toliau pateiktoje lentelėje įvertinti, ar jūsų techninės ir programinės įrangos aplinka yra pasirengusi paremti diegimą.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Android"                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| "Windows" (UWP)               | "Windows 10" (visos versijos)                                                                                                                                                   |
| Dinamika 365 operacijoms | "Microsoft Dynamics 365" operacijų 1611 - ar - Microsoft Dynamics Dynamics AX versija 7.0/7.0.1 ir Microsoft Dynamics AX platforma atnaujinti 2 karštąją pataisą KB 3210014 |

## <a name="get-the-app"></a>Gaukite programėlę
-   "Windows" (UWP) - [Dynamics 365 operacijų - sandėliavimo "Windows" parduotuvėje](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   "Android" - [Dynamics 365 operacijų - sandėliavimo "Google Play Store"](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Sukurti žiniatinklio tarnybos taikomoji programa Active Directory
Norėdami įjungti programėlės bendrauti su konkrečių Dynamics "365" operacijų serverio, turite užsiregistruoti žiniatinklio tarnybos taikomoji programa Azure Active Directory Dynamics "365" dėl operacijų nuomininkas. Dėl saugumo priežasčių, mes rekomenduojame, kad jums sukurti žiniatinklio tarnybos taikomoji programa kiekvienam įrenginiui, kurį naudojate. Norėdami sukurti žiniatinklio tarnybos taikomoji programa Azure Active Directory (Azure AD), atlikite šiuos veiksmus:

1.  Naudodami žiniatinklio naršyklę, eikite į <https://manage.windowsazure.com>.
2.  Įveskite vardą ir slaptažodį, kad vartotojas, kuris turi prieigą prie Azure prenumeratos.
3.  Azure portalas, kairiojoje naršymo srityje spustelėkite **Active Directory**. [](./media/wh-01-active-directory-example.png)[![wh-01 – veikliosios medžiagos-katalogas-pvz.](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Tinklelį, pasirinkite Active Directory egzemplioriuje, kuris naudoja Dynamics 365 operacijoms.
5.  Viršų įrankių juostoje, spustelėkite **programų**. [![Wh-02 – veikliosios medžiagos-katalogas-programos](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Apatinėje srityje spustelėkite **pridėti**. Į **pridėti programą** vedlys paleidžiamas.
7.  Įveskite pavadinimą programos ir pasirinkite **žiniatinklio programa ir (arba) web API**. [![Wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Įveskite prisijungimo URL, kuris yra programos URL į savo nuomotojo, pagrindines operacijas URL. Prisijungimo URL yra šiuo metu nėra aktyviai naudojamas kas app, tačiau būtina užpildyti. Programos ID URI lauke įveskite tą patį URL. [![Wh-04-skelbimas-pridėti-savybės](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Eikite į į **konfigūruoti** tab. [![Wh-05-skelbimas-konfigūruoti-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Slinkite žemyn, kol pamatysite ir **teises į kitas programas** skyriuje. Spustelėkite **pridėti programą**. [![Wh-06-ad-App-Add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Pasirinkite **Microsoft Dynamics ERP** sąraše. Spustelėkite į **įregistravimo** puslapio dešiniajame kampe esantį mygtuką. [![Wh-07-skelbimas-pasirinkite-teises](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. – Į **atstovo teises** pažymėkite visus žymės langelius. Click **Save**. [![Wh-08-skelbimas-atstovo-teises](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Užsirašykite šią informaciją:
    -   **Kliento ID** - slinkti puslapį, jūs pamatysite **kliento ID** rodomas.
    -   **Raktas** – į **raktų** skyriuje, sukurti raktą, pasirinkdami trukmė ir nukopijuoti raktą. Šis raktas bus vėliau perduotas kaip į **kliento paslaptį**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Sukurti ir sukonfigūruoti vartotojo abonementą programoje Dynamics 365 operacijoms
Norėdami įgalinti Dynamics 365 operacijoms, skirtoms naudoti Azure AD programą, turite atlikite šiuos konfigūravimo veiksmus:

1.  Sukurkite naują vartotojo abonementą Azure Active Directory Dynamics "365" dėl operacijų nuomininkas. Šis Vartotojo abonentas tikslas pasiekti konkrečių muitinės paslaugos sandėliavimo App, kuri atskleidžia Dynamics 365 operacijų serverio. Baigę šį žingsnį, jūs turėsite WMDP vartotojo kredencialus, kurie sudaryti iš WMDP elektroninio pašto adresą ir slaptažodį WMDP. Norėdami sužinoti apie pagrindinius veiksmus įtraukti vartotojų į Azure AD Dynamics 365 operacijos, susijusios su Šiuo samouczku: [prisijungti prie Microsoft Dynamics 365 operacijų pasirašymo](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Sukurti Dynamics 365 operacijų vartotojui, kuris atitinka sandėliavimo app vartotojo kredencialus.
    1.  Dynamics 365 operacijoms, eikite į **sistemos administravimo**&gt;**bendras**&gt;**vartotojai**.
    2.  Sukurti naują vartotoją.
    3.  Priskirti sandėlį mobiliojo įrenginio naudotojui, kaip parodyta toliau ekrano. [![Wh-09-ADD-user-Security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Susieti Azure Active Directory programa su sandėliavimo programa vartotojui.
    1.  Dynamics 365 operacijoms, eikite į **sistemos administravimo**&gt;**nustatymo**&gt;**Azure Active Directory programos**.
    2.  Sukurkite naują eilutę.
    3.  Įvesti į **kliento ID** (gaunamas Antrame skyriuje), pavadinkite jį, tada pasirinkite anksčiau sukurtą vartotoją. Mes rekomenduojame pažymėti visuose savo įrenginiuose, kad galite lengvai pašalinti savo prieigos Dynamics 365 operacijoms iš šio puslapio, jei jie bus prarasti. [![Wh, 10, skelbimo, paraiškų formos](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Sukonfigūruoti, kad programa
Turite sukonfigūruoti programą įrenginyje prisijungti prie "Dynamics 365" operacijų serverio per Azure AD programą. Norėdami tai padaryti, atlikite šiuos veiksmus.

1.  Naudodami programėlę, eikite į **ry io parametrus**.
2.  Aišku, **"Demo" režimas** srityje. [![Wh-11-App-Connection-Settings-demo-Mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Įveskite šią informaciją:- **Azure Active katalogas kliento ID** -kliento ID yra gaunamas žingsnis 13 "Sukurkite interneto paslaugų programa Active Directory". - **Azure Active katalogas kliento paslaptį** -kliento paslaptį gaunamas "Sukurkite interneto paslaugų programa Active Directory" 13 žingsnis. - **Azure Active directory ištekliais** -Azure AD directory ištekliais pavaizduotas Dynamics 365 operacijas šakninis URL. **Pastaba**: nesibaigia šioje srityje į priekį pasvirojo brūkšnio simboliu (/). - **Azure Active katalogas nuomininkas** -Azure AD katalogas nuomininkas naudojamas Dynamics "365" operacijų serveris: https://login.windows.net/&lt;jūsų skelbimo nuomotojo ID&gt;. Pvz.: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Pastaba**: nesibaigia šioje srityje į priekį pasvirojo brūkšnio simboliu (/). - **Bendrovė** -juridinio asmens Dynamics 365 įvesti operacijas, iki kurio reikia programėlei jungtis. [![Wh-12-app-ryšio-parametrai](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Pasirinkite į **atgal** mygtuką, esantį viršutiniame kairiajame kampe paraiškos. Taikyti dabar bus prijungti prie jūsų Dynamics "365" operacijų serverio ir sandėlio darbuotojui prisijungimo ekrane bus rodomas. [![Wh-13-prisijungimo](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Pašalinti prieigos įrenginio
Tuo atveju, kai prarastas arba pažeistas prietaisas, turite pašalinti patekti į "Dynamics 365" operacijų įrenginio. Tolimesni veiksmai paaiškina rekomenduojama procesą pašalinti prieigą.

1.  Dynamics 365 operacijoms, eikite į **sistemos administravimo**&gt;**nustatymo**&gt;**Azure Active Directory programos**.
2.  Naikinti eilutę, kurią norite šalinti prieigos įrenginys atitinka. Užsirašykite į **kliento ID** naudojamas pašalinti įrenginį.
3.  Prisijungti žydros klasikinis portale, esančiame <https://manage.windowsazure.com>.
4.  Spustelėkite į **Active Directory** piktogramą kairėje pusėje esančiame meniu, o tada spustelėkite norimą katalogą.
5.  Viršutiniame meniu, spustelėkite **programų**, ir tada spustelėkite norimą konfigūruoti programą. Į **greitai pradėti** puslapis bus rodomas su bendrąją autentifikaciją ir kitą konfigūravimo informaciją.
6.  Spustelėkite į **konfigūruoti** skirtuką, pereikite ir užtikrinti, kad į **kliento ID** paraiškos yra toks pat kaip žingsnis 2 šiame skyriuje.
7.  Spustelėkite į **panaikinti** mygtuką valdymo juostoje.
8.  Spustelėkite **taip**, patvirtinimo pranešimas.



