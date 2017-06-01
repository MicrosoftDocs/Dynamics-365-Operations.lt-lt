---
title: "„Dynamics 365 for Operations“ – versijos „Warehousing“ diegimas ir konfigūravimas"
description: "Šioje temoje aprašoma, kaip diegti ir konfigūruoti „Microsoft Dynamics 365 for Operations“ – versiją „Warehousing“."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>„Dynamics 365 for Operations“ – versijos „Warehousing“ diegimas ir konfigūravimas

[!include[banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip diegti ir konfigūruoti „Microsoft Dynamics 365 for Operations“ – versiją „Warehousing“.

„Dynamics 365 for Operations“ – versija „Warehousing“ yra programa, kurią atsisiųsti iš „Google Play“ parduotuvės ir „Windows“ parduotuvės. Dabartinėje „Microsoft Dynamics 365 for Operations“ versijoje ši programa pateikiama kaip atskiras komponentas, todėl sandėlio užduotims atlikti naudojamuose įrenginiuose ją reikia įdiegti patiems. Norėdami naudoti programą „Dynamics 365 for Operations“ aplinkoje, turite atsisiųsti programą į kiekvieną įrenginį ir ją sukonfigūruoti, kad galėtumėte prijungti prie „Dynamics 365 for Operations“ aplinkos. Šioje temoje aprašoma, kaip diegti programą įrenginiuose. Joje taip pat paaiškinama, kaip programą sukonfigūruoti ir prijungti prie „Dynamics 365 for Operations“ aplinkos.

## <a name="prerequisites"></a>Būtinieji komponentai
Programą galima naudoti operacinėse sistemose „Android“ ir „Windows“. Norėdami naudoti šią programą, savo įrenginiuose turite būti įdiegę vieną iš toliau nurodytų operacinių sistemų. Taip pat jums reikia vienos iš toliau nurodytų palaikomų „Dynamics 365 for Operations“ versijų. Peržiūrėkite tolesnės lentelės informaciją ir įvertinkite, ar jūsų aparatūros ir programinės įrangos aplinkoje galima diegti programą.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | „Windows 10“ (visos versijos)                                                                                                                                                   |
| Dynamics 365 for Operations | „Microsoft Dynamics 365 for Operations“ 1611 versija arba „Microsoft Dynamics Dynamics AX“ 7.0 / 7.0.1 versija ir „Microsoft Dynamics AX“ platformos 2 naujinys su karštąja pataisa KB 3210014 |

## <a name="get-the-app"></a>Gaukite programą
-   „Windows“ (UWP) – [„Dynamics 365 for Operations“ – versija „Warehousing“ „Windows“ parduotuvėje](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   „Android“ – [„Dynamics 365 for Operations“ – versija „Warehousing“ „Google Play“ parduotuvėje](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Žiniatinklio tarnybos programos kūrimas „Active Directory“
Norėdami įjungti programos sąveiką su konkrečiu „Dynamics 365 for Operations“ serveriu, žiniatinklio tarnybos programą turite užregistruoti „Dynamics 365 for Operations“ nuomotojo „Azure Active Directory“. Saugumo sumetimais rekomenduojame sukurti kiekvieno naudojamo įrenginio žiniatinklio tarnybos programą. Norėdami žiniatinklio tarnybos programą kurti „Azure Active Directory“ („Azure AD“), atlikite tolesnius veiksmus.

1.  Žiniatinklio naršyklėje atidarykite puslapį adresu <https://manage.windowsazure.com>.
2.  Įveskite vartotojo, kuris turi prieigą prie „Azure“ prenumeratos, pavadinimą ir slaptažodį.
3.  „Azure“ portalo dešiniojoje naršymo srityje spustelėkite **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Tinklelyje pasirinkite „Active Directory“ egzempliorių, kurį naudoja „Dynamics 365 for Operations“.
5.  Viršutinėje įrankių juostoje spustelėkite **Programos**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Apatinėje srityje spustelėkite **Įtraukti**. Paleidžiamas vedlys **Įtraukti programą**.
7.  Įveskite programos pavadinimą ir pasirinkite **Žiniatinklio programa ir (arba) žiniatinklio API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Įveskite prisijungimo URL, kuris yra jūsų nuomotojo programos URL, šakninis „Operations“ URL. Prisijungimo URL šiuo metu nėra aktyviai naudojamas programai autentifikuoti, bet jis yra būtinas laukas. Tą patį URL įveskite lauke Programos ID URI. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Atidarykite skirtuką **Konfigūruoti**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Slinkite žemyn, kol pamatysite dalį **Prieigos prie kitų programų teisės**. Spustelėkite **Įtraukti programą**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Sąraše pasirinkite **Microsoft Dynamics ERP**. Viršutiniame dešiniajame puslapio kampe spustelėkite mygtuką **Baigti tikrinimą**. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Sąraše **Perduoti teises** pažymėkite visus žymės langelius. Spustelėkite **Įrašyti**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Pasižymėkite toliau nurodytą informaciją.
    -   **Kliento ID** – slinkdami puslapiu aukštyn pamatysite rodomą **Kliento ID**.
    -   **Raktas** – dalyje **Raktai** sukurkite raktą, pasirinkdami trukmę, ir nukopijuokite raktą. Šis raktas bus vėliau nurodytas kaip **Kliento paslaptis**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Vartotojo paskyros kūrimas ir konfigūravimas programoje „Dynamics 365 for Operations“
Norėdami leisti „Dynamics 365 for Operations“ naudoti jūsų „Azure AD“ programą, atlikite toliau nurodytus konfigūravimo veiksmus.

1.  Sukurkite naują vartotojo paskyrą „Dynamics 365 for Operations“ nuomotojo „Azure Active Directory“. Šios vartotojo paskyros paskirtis yra pasiekti konkrečią pasirinktinę sandėliavimo programos tarnybą, kurią pateikia „Dynamics 365 for Operations“ serveris. Atlikę šį veiksmą, turėsite WMDP vartotojo kredencialus, kuriuos sudaro WMDP el. pašto adresas ir WMDP slaptažodis. Norėdami sužinoti apie pagrindinius vartotojų įtraukimo į „Azure AD“ ir „Dynamics 365 for Operations“ veiksmus, žr. šią mokymo programą: [„Microsoft Dynamics 365 for Operations“ prenumeratos registracija](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Sukurkite „Dynamics 365 for Operations“ vartotoją, kuris atitinka sandėliavimo programos vartotojo kredencialus.
    1.  Programoje „Dynamics 365 for Operations“ atidarykite **Sistemos administravimas** &gt; **Bendra** &gt; **Vartotojai**.
    2.  Sukurkite naują vartotoją.
    3.  Priskirkite sandėlio mobiliojo įrenginio vartotoją, kaip parodyta tolesnėje ekrano kopijoje. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Susiekite savo „Azure Active Directory“ programą su sandėliavimo programos vartotoju.
    1.  Programoje „Dynamics 365 for Operations“ atidarykite **Sistemos administravimas** &gt; **Sąranka** &gt; **„Azure Active Directory“ programa**.
    2.  Sukurkite naują eilutę.
    3.  Įveskite **Kliento ID** (gautą anksčiau), suteikite jam pavadinimą ir pasirinkite anksčiau sukurtą vartotoją. Rekomenduojame pažymėti visus savo įrenginius, kad juos pametus galėtumėte lengvai pašalinti jų prieigą prie „Dynamics 365 for Operations“ iš šio puslapio. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Programos konfigūravimas
Turite sukonfigūruoti programą įrenginyje, kad „Dynamics 365 for Operations“ serverį prijungtumėte per „Azure AD“ programą. Norėdami tai padaryti, atlikite toliau nurodytus veiksmus.

1.  Programoje atidarykite **Ryšio parametrai**.
2.  Išvalykite lauką **Demonstracinis režimas**. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Įveskite šią informaciją: – **„Azure Active Directory“ kliento ID** – kliento ID gaunamas atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 13 veiksmą. – **„Azure Active Directory“ kliento paslaptis** – kliento paslaptis gaunama atliekant temos „Žiniatinklio tarnybos programos kūrimas „Active Directory“ 13 veiksmą. – **„Azure Active Directory“ išteklius** – „Azure AD“ išteklius nurodo „Dynamics 365 for Operations“ šakninį URL. **Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. – **„Azure Active Directory“ nuomotojas** – „Azure AD“ nuomotojas naudojamas kartu su „Dynamics 365 for Operations“ serveriu: https://login.windows.net/&lt;your-AD-tenant-ID&gt;. Pvz.: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Pastaba.** Šio lauko užbaigti pasvirojo brūkšnio simboliu (/) negalima. – **Įmonė** – programoje „Microsoft Dynamics 365 for Operations‟ įveskite juridinį subjektą, prie kurio norite prijungti programą. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Viršutiniame kairiajame programos kampe pasirinkite mygtuką **Atgal**. Dabar programa prijungs jūsų „Dynamics 365 for Operations“ serverį bus rodomas sandėlio darbuotojo prisijungimo ekranas. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Įrenginio prieigos šalinimas
Jei įrenginys buvo pamestas arba pažeista jo sauga, turite pašalinti įrenginio prieigą prie „Dynamics 365 for Operations“. Tolesni veiksmai aprašo rekomenduojamą prieigos šalinimo procesą.

1.  Programoje „Dynamics 365 for Operations“ atidarykite **Sistemos administravimas** &gt; **Sąranka** &gt; **„Azure Active Directory“ programa**.
2.  Panaikinkite eilutę, atitinkančią įrenginį, kurio prieigą norite šalinti. Pasižymėkite pašalintame įrenginyje naudojamą **Kliento ID**.
3.  Prisijunkite įprasto „Azure“ portalo adreso <https://manage.windowsazure.com>.
4.  Kairiajame meniu spustelėkite piktogramą **Active Directory** ir tada spustelėkite norimą katalogą.
5.  Viršutiniame meniu spustelėkite **Programos** ir tada spustelėkite programą, kurią norite konfigūruoti. Pasirodys puslapis **Greitas pasirengimas darbui**, kuriame pateikta bendrosios autentifikacijos ir kita konfigūravimo informacija.
6.  Spustelėkite skirtuką **Konfigūruoti**, slinkite žemyn ir įsitikinkite, kad programos **Kliento ID** yra toks pat, koks nurodytas šio skyriaus 2 veiksme.
7.  Komandų juostoje spustelėkite mygtuką **Naikinti**.
8.  Patvirtinimo pranešime spustelėkite **Taip**.





