---
title: Sandėliavimo programos diegimo ir konfigūravimo apžvalga
description: Šioje temoje aprašoma, kaip diegti ir konfigūruoti programą „Dynamics 365 for Finance and Operations – Warehousing“.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f629fffc5c424c244a25bb8faef0435814398ee1
ms.sourcegitcommit: 4aac45c84b87f463b22b318f5f6f729f8d737090
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2548973"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Sandėliavimo programos diegimo ir konfigūravimo apžvalga

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Šioje temoje aprašoma, kaip sukonfigūruoti visuotinėms debesies įdiegtims skirtą sandėliavimo funkciją. Jei ieškote, kaip konfigūruoti vietinėms visuotinėms įdiegtims skirtą sandėliavimo funkciją, žr. [Vietinėms visuotinėms įdiegtims skirtas sandėliavimas](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Šioje temoje aprašoma, kaip diegti ir konfigūruoti programą „Dynamics 365 for Finance and Operations – Warehousing“.

Sandėliavimo programą galite parsisiųsti iš „Google Play" parduotuvės ir „Windows Store“ parduotuvės. Dabartinėje „Dynamics 365 Supply Chain Management“ versijoje ši programa pateikiama kaip atskiras komponentas, todėl sandėlio užduotims atlikti naudojamuose įrenginiuose ją reikia įdiegti patiems. Norėdami naudoti programą, turite atsisiųsti programą į kiekvieną įrenginį ir ją sukonfigūruoti, kad galėtumėte prijungti prie „Supply Chain Management“ aplinkos. Šioje temoje aprašoma, kaip diegti programą įrenginiuose. Joje taip pat paaiškinama, kaip programą sukonfigūruoti ir prijungti prie „Supply Chain Management“ aplinkos.

## <a name="prerequisites"></a>Būtinieji komponentai
Programą galima naudoti operacinėse sistemose „Android“ ir „Windows“. Norėdami naudoti šią programą, savo įrenginiuose turite būti įdiegę vieną iš toliau nurodytų operacinių sistemų. Taip pat turite turėti vieną iš palaikomų versijų. Peržiūrėkite tolesnės lentelės informaciją ir įvertinkite, ar jūsų aparatūros ir programinės įrangos aplinkoje galima diegti programą.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „Android“                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | „Windows 10“ (visos versijos)                                                                                                                                                   |
| „Finance and Operations” | „Microsoft Dynamics 365 for Operations“ 1611 versija <br>Arba <br>„Microsoft Dynamics AX“ 7.0 / 7.0.1 versijos ir „Microsoft Dynamics AX“ platformos 2 naujinimas su karštosiomis pataisomis KB 3210014 |

## <a name="get-the-app"></a>Gaukite programą
-   Windows (UWP)
     - [„Finance and Operations – Warehousing“ parduotuvėje „Microsoft Store“](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [„Finance and Operations“ – versija „Warehousing“ „Google Play“ parduotuvėje](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> „Zebra“ programų galerija nebenaudojama, o tai reiškia, kad „Warehousing“ programos nebebus galima atsisiųsti iš tos vietos.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“
Norėdami įjungti programos sąveiką su konkrečiu „Supply Chain Management“ serveriu, žiniatinklio tarnybos programą turite užregistruoti „Supply Chain Management“ nuomotojo „Azure Active Directory“. Saugumo sumetimais rekomenduojame sukurti kiekvieno naudojamo įrenginio žiniatinklio tarnybos programą. Norėdami žiniatinklio tarnybos programą kurti „Azure Active Directory“ („Azure AD“), atlikite tolesnius veiksmus.

1.  Interneto naršyklėje eikite į <https://portal.azure.com>.
2.  Įveskite vartotojo, kuris turi prieigą prie „Azure“ prenumeratos, pavadinimą ir slaptažodį.
3.  „Azure“ portalo dešiniojoje naršymo srityje spustelėkite **Azure Active Directory**[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Įsitikinkite, kad „Active Directory“ egzempliorius yra tas, kurį naudoja „Supply Chain Management“.
5.  Sąraše spustelėkite **Programų registracijos**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Viršutinėje srityje spustelėkite **Nauja registracija**. Paleidžiamas vedlys **Registruoti programą**.
7.  Įveskite programos pavadinimą ir pasirinkite **Paskyros tik šiame organizaciniame kataloge**. Spustelėkite **Registruotis**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Bus atidaroma nauja programos registracija. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Įsiminkite **programos ID**, jo jums reikės vėliau. **Programos ID** vėliau bus vadinamas **kliento ID**.
10. Spustelėkite **Sertifikatas ir paslaptys** srityje **Valdyti**. Spustelėkite **Nauja kliento paslaptis**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Sukurkite raktą skyriuje **Slaptažodžiai** įvesdami rakto aprašą ir trukmę. Spustelėkite **Įtraukti** ir nukopijuokite raktą. Šis raktas bus vėliau nurodytas kaip **Kliento paslaptis**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vartotojo paskyros kūrimas ir konfigūravimas programoje „Supply Chain Management“
Norėdami leisti „Supply Chain Management“ naudoti jūsų „Azure AD“ programą, atlikite toliau nurodytus konfigūravimo veiksmus.

1.  Sukurkite vartotoją, kuris atitinka sandėliavimo programos vartotojo kredencialus.
    1.  Eikite į **Sistemos administravimas** &gt; **Bendra** &gt; **Vartotojai**.
    2.  Sukurkite naują vartotoją.
    3.  Priskirkite sandėlio mobiliojo įrenginio vartotoją, kaip parodyta tolesnėje ekrano kopijoje. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Susiekite savo „Azure Active Directory“ programą su sandėliavimo programos vartotoju.
    1.  Programoje „Supply Chain Management“ pasirinkite **Sistemos administravimas** &gt; **Sąranka** &gt; **„Azure Active Directory“ programas**.
    2.  Sukurkite naują eilutę.
    3.  Įveskite **Kliento ID** (gautą anksčiau), suteikite jam pavadinimą ir pasirinkite anksčiau sukurtą vartotoją. Rekomenduojame pažymėti visus savo įrenginius, kad juos pametę galėtumėte lengvai pašalinti jų prieigą prie „Supply Chain Management“ iš šio puslapio. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Programos konfigūravimas
Turite sukonfigūruoti programą įrenginyje, kad prie „Supply Chain Management“ serverio prisijungtumėte per „Azure AD“ programą. Norėdami tai padaryti, atlikite toliau nurodytus veiksmus.

1.  Programoje atidarykite **Ryšio parametrai**.
2.  Išvalykite lauką **Demonstracinis režimas**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Įveskite šią informaciją: 
    + – **„Azure Active Directory“ kliento ID** – kliento ID, gaunamas atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 9 veiksmą. 
    + **„Azure Active Directory“ kliento paslaptis** – kliento paslaptis gaunama atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 11 veiksmą. 
    + **„Azure Active Directory“ išteklius** – „Azure AD“ išteklius nurodo „Supply Chain Management“ URL. **Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. 
    + **„Azure Active Directory“ nuomotojas** – „Azure AD“ nuomotojas, naudojamas su „Supply Chain Management“ serveriu: `https://login.windows.net/your-AD-tenant-ID`. Pavyzdžiui: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. 
    + **Įmonė** – programoje „Supply Chain Management‟ įveskite juridinį subjektą, prie kurio norite prijungti programą. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Viršutiniame kairiajame programos kampe pasirinkite mygtuką **Atgal**. Dabar programa prisijungs prie jūsų „Supply Chain Management“ serverio ir bus rodomas sandėlio darbininko prisijungimo ekranas. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Norėdami gauti informacijos apie tai, kaip nustatyti „Warehousing“ programą, kad mobiliojo įrenginio kamera nuskaitytų brūkšninius kodus, žr. [Brūkšninių kodų nuskaitymas naudojant kamerą programoje „Dynamics 365 for Finance and Operations – Warehousing“](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Įrenginio prieigos šalinimas
Jei įrenginys buvo pamestas arba pažeista jo sauga, turite pašalinti įrenginio prieigą prie „Supply Chain Management“. Tolesni veiksmai aprašo rekomenduojamą prieigos šalinimo procesą.

1.  Eikite į **Sistemos administravimas** &gt; **Sąranka** &gt; **Azure Active Directory programos**.
2.  Panaikinkite eilutę, atitinkančią įrenginį, kurio prieigą norite šalinti. Įsiminkite su pašalintu įrenginiu naudotą **kliento ID**, jo jums reikės vėliau.
3.  Prisijunkite prie „Azure“ portalo adresu <https://portal.azure.com>.
4.  Kairiajame meniu spustelėkite piktogramą **„Active Directory“** ir įsitikinkite, kad esate teisingame kataloge.
5.  Sąraše spustelėkite **Programų registracijos**, tada spustelėkite programą, kurią norite konfigūruoti. Pasirodys sritis **Parametrai** su konfigūravimo informacija.
6.  Įsitikinkite, kad programos **kliento ID** yra toks pats, kaip šio skyriaus 2 veiksme.
7.  Viršutinėje srityje spustelėkite mygtuką **Naikinti**.
8.  Patvirtinimo pranešime spustelėkite **Taip**.
