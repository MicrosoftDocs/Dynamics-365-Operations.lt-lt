---
title: "„Dynamics 365 for Finance and Operations“ – versijos „Warehousing“ diegimas ir konfigūravimas"
description: "Šioje temoje aprašoma, kaip diegti ir konfigūruoti „Microsoft Dynamics 365 for Finance and Operations“ – versiją „Warehousing“."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: lt-lt
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>„Dynamics 365 for Finance and Operations“ – versijos „Warehousing“ diegimas ir konfigūravimas

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Šioje temoje aprašoma, kaip sukonfigūruoti visuotinėms debesies įdiegtims skirtą sandėliavimo funkciją. Jei ieškote, kaip konfigūruoti vietinėms visuotinėms įdiegtims skirtą sandėliavimo funkciją, žr. [Vietinėms visuotinėms įdiegtims skirtas sandėliavimas](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Šioje temoje aprašoma, kaip diegti ir konfigūruoti „Microsoft Dynamics 365 for Finance and Operations“ – versiją „Warehousing“.

„Finance and Operations“ – versija „Warehousing“ yra programa, kurią galima atsisiųsti iš „Google Play“ parduotuvės ir „Windows“ parduotuvės. Dabartinėje „Finance and Operations“ versijoje ši programa pateikiama kaip atskiras komponentas, todėl sandėlio užduotims atlikti naudojamuose įrenginiuose ją reikia įdiegti patiems. Norėdami naudoti programą „Finance and Operations“ aplinkoje, turite atsisiųsti programą į kiekvieną įrenginį ir ją sukonfigūruoti, kad galėtumėte prijungti prie „Finance and Operations“ aplinkos. Šioje temoje aprašoma, kaip diegti programą įrenginiuose. Joje taip pat paaiškinama, kaip programą sukonfigūruoti ir prijungti prie „Finance and Operations“ aplinkos.

## <a name="prerequisites"></a>Būtinieji komponentai
Programą galima naudoti operacinėse sistemose „Android“ ir „Windows“. Norėdami naudoti šią programą, savo įrenginiuose turite būti įdiegę vieną iš toliau nurodytų operacinių sistemų. Taip pat jums reikia vienos iš toliau nurodytų palaikomų „Finance and Operations“ versijų. Peržiūrėkite tolesnės lentelės informaciją ir įvertinkite, ar jūsų aparatūros ir programinės įrangos aplinkoje galima diegti programą.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „Android“                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | „Windows 10“ (visos versijos)                                                                                                                                                   |
| „Finance and Operations” | „Microsoft Dynamics 365 for Operations“ versija 1611 <br>Arba <br>„Microsoft Dynamics AX“ 7.0 / 7.0.1 versijos ir „Microsoft Dynamics AX“ platformos 2 naujinimas su karštosiomis pataisomis KB 3210014 |

## <a name="get-the-app"></a>Gaukite programą
-   Windows (UWP)
     - [„Finance and Operations – Warehousing“ parduotuvėje „Microsoft Store“](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   „Android“
    - [„Finance and Operations“ – versija „Warehousing“ „Google Play“ parduotuvėje](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [„Finance and Operations“ – versija „Warehousing“ „Zebra“ programų galerijoje](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“
Norėdami įjungti programos sąveiką su konkrečiu „Finance and Operations“ serveriu, žiniatinklio tarnybos programą turite užregistruoti „Finance and Operations“ nuomotojo „Azure Active Directory“. Saugumo sumetimais rekomenduojame sukurti kiekvieno naudojamo įrenginio žiniatinklio tarnybos programą. Norėdami žiniatinklio tarnybos programą kurti „Azure Active Directory“ („Azure AD“), atlikite tolesnius veiksmus.

1.  Interneto naršyklėje eikite į <https://portal.azure.com>.
2.  Įveskite vartotojo, kuris turi prieigą prie „Azure“ prenumeratos, pavadinimą ir slaptažodį.
3.  „Azure“ portalo dešiniojoje naršymo srityje spustelėkite **„Azure Active Directory“**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Įsitikinkite, kad „Active Directory“ egzempliorių naudoja „Finance and Operations“.
5.  Sąraše spustelėkite **Programų registracijos**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Viršutinėje srityje spustelėkite **Naujos programos registracija**. Paleidžiamas vedlys **Įtraukti programą**.
7.  Įveskite programos pavadinimą ir pasirinkite **Žiniatinklio programa / žiniatinklio API**. Įveskite prisijungimo URL, kuris yra žiniatinklio programos URL. Šis URL yra toks pats kaip ir diegimo URL, tačiau pabaigoje pridedamas „oauth“. Spustelėkite **Kurti**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Sąraše pasirinkite naująją programą. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Įsiminkite **programos ID**, jo jums reikės vėliau. **Programos ID** vėliau bus vadinamas **kliento ID**.
10. **Srityje Parametrai** spustelėkite **Raktai**. Sukurkite raktą skyriuje **Slaptažodžiai** įvesdami rakto aprašą ir trukmę. 
11. Spustelėkite **Įrašyti** ir nukopijuokite raktą. Šis raktas bus vėliau nurodytas kaip **Kliento paslaptis**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Vartotojo paskyros kūrimas ir konfigūravimas programoje „Finance and Operations“
Norėdami leisti „Finance and Operations“ naudoti jūsų „Azure AD“ programą, atlikite toliau nurodytus konfigūravimo veiksmus.

1.  Sukurkite naują vartotojo paskyrą „Finance and Operations“ nuomotojo „Azure Active Directory“. Šios vartotojo paskyros paskirtis yra pasiekti konkrečią pasirinktinę sandėliavimo programos tarnybą, kurią pateikia „Finance and Operations“ serveris. Atlikę šį veiksmą, turėsite WMDP vartotojo kredencialus, kuriuos sudaro WMDP el. pašto adresas ir WMDP slaptažodis. Norėdami sužinoti apie pagrindinius vartotojų įtraukimo į „Azure AD“ ir „Finance and Operations“ veiksmus, žr. šią mokymo programą: [„Finance and Operations“ prenumeratos registracija](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Sukurkite „Finance and Operations“ vartotoją, kuris atitinka sandėliavimo programos vartotojo kredencialus.
    1.  Programoje „Finance and Operations“ eikite į **Sistemos administravimas** &gt; **Bendra** &gt; **Vartotojai**.
    2.  Sukurkite naują vartotoją.
    3.  Priskirkite sandėlio mobiliojo įrenginio vartotoją, kaip parodyta tolesnėje ekrano kopijoje. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Susiekite savo „Azure Active Directory“ programą su sandėliavimo programos vartotoju.
    1.  Programoje „Finance and Operations“ eikite į **Sistemos administravimas** &gt; **Sąranka** &gt; **„Azure Active Directory“ programos**.
    2.  Sukurkite naują eilutę.
    3.  Įveskite **Kliento ID** (gautą anksčiau), suteikite jam pavadinimą ir pasirinkite anksčiau sukurtą vartotoją. Rekomenduojame pažymėti visus savo įrenginius, kad juos pametę galėtumėte lengvai pašalinti jų prieigą prie „Finance and Operations“ iš šio puslapio. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Programos konfigūravimas
Turite sukonfigūruoti programą įrenginyje, kad prie „Finance and Operations“ serverio prisijungtumėte per „Azure AD“ programą. Norėdami tai padaryti, atlikite toliau nurodytus veiksmus.

1.  Programoje atidarykite **Ryšio parametrai**.
2.  Išvalykite lauką **Demonstracinis režimas**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Įveskite šią informaciją: 
    + – **„Azure Active Directory“ kliento ID** – kliento ID, gaunamas atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 9 veiksmą. 
    + **„Azure Active Directory“ kliento paslaptis** – kliento paslaptis gaunama atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 11 veiksmą. 
    + **„Azure Active Directory“ išteklius** – „Azure AD“ išteklius nurodo „Finance and Operations“ šakninį URL. **Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. 
    + **„Azure Active Directory“ nuomotojas** – „Azure AD“ nuomotojas, naudojamas su „Finance and Operations“ serveriu: `https://login.windows.net/your-AD-tenant-ID`. Pavyzdžiui: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. 
    + **Įmonė** – programoje „Finance and Operations‟ įveskite juridinį subjektą, prie kurio norite prijungti programą. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Viršutiniame kairiajame programos kampe pasirinkite mygtuką **Atgal**. Dabar programa prijungs jūsų „Finance and Operations“ serverį ir bus rodomas sandėlio darbininko prisijungimo ekranas. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Norėdami gauti informacijos apie tai, kaip nustatyti, kad „Dynamics 365 for Finance and Operations – Warehousing“ mobiliojo įrenginio kamera nuskaitytų brūkšninius kodus, žr. [Brūkšninių kodų nuskaitymas naudojant kamerą programoje „Dynamics 365 for Finance and Operations – Warehousing“](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Įrenginio prieigos šalinimas
Jei įrenginys buvo pamestas arba pažeista jo sauga, turite pašalinti įrenginio prieigą prie „Finance and Operations“. Tolesni veiksmai aprašo rekomenduojamą prieigos šalinimo procesą.

1.  Programoje „Finance and Operations“ eikite į **Sistemos administravimas** &gt; **Sąranka** &gt; **„Azure Active Directory“ programos**.
2.  Panaikinkite eilutę, atitinkančią įrenginį, kurio prieigą norite šalinti. Įsiminkite su pašalintu įrenginiu naudotą **kliento ID**, jo jums reikės vėliau.
3.  Prisijunkite prie „Azure“ portalo adresu <https://portal.azure.com>.
4.  Kairiajame meniu spustelėkite piktogramą **„Active Directory“** ir įsitikinkite, kad esate teisingame kataloge.
5.  Sąraše spustelėkite **Programų registracijos**, tada spustelėkite programą, kurią norite konfigūruoti. Pasirodys sritis **Parametrai** su konfigūravimo informacija.
6.  Įsitikinkite, kad programos **kliento ID** yra toks pats, kaip šio skyriaus 2 veiksme.
7.  Viršutinėje srityje spustelėkite mygtuką **Naikinti**.
8.  Patvirtinimo pranešime spustelėkite **Taip**.

