---
title: El. prekybos svetainės kopijavimas
description: Šiame straipsnyje aprašoma, kaip kopijuoti esamą el. komercijos svetainę svetainės generatoriaus el. komercijos aplinkose arba Microsoft Dynamics 365 Commerce tarp jų.
author: psimolin
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cb53a76b2ebe5b511bf5009727f20f20755e5720
ms.sourcegitcommit: 13c7a1cc4c90417e3e88db59b7d2165b3c40a56c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2022
ms.locfileid: "8935749"
---
# <a name="copy-an-e-commerce-site"></a>El. prekybos svetainės kopijavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kopijuoti esamą el. komercijos svetainę svetainės generatoriaus el. komercijos aplinkose arba Microsoft Dynamics 365 Commerce tarp jų.

Dynamics 365 Commerce palaiko kopijavimą ar įsimenant svetaines kaip savitarnos operaciją "Commerce Site Builder". Svetaines galima kopijuoti vienoje el. komercijos aplinkoje arba dviejose el. komercijos aplinkose. Svetainės kopijavimo operaciją inicijuojantis vartotojas turi būti nuomininkų administratorius šaltinio ir paskirties el. komercijos aplinkose.

Svetainės kopijavimo operacija kopijuoja visą šaltinio svetainės el. komercijos turinį. Šiame turinyje yra puslapiai, fragmentai, šablonai, URL ir turtas. Prieš pradedant naują svetainę, ji turi būti inicijuota per pirmojo vykdymo patirties (FRE) procesą. Kanalus galima susieti ir valdyti svetainės generatoriuje svetainės parametrų **kanaluose \>**.

Vietos kopijavimo operacijos trukmė pirmiausia priklauso nuo turto šaltinio teritorijoje skaičiaus. Panaudodami dideles vietas rekomenduojame apsvarstyti galimybę naudoti aplinkos kopijavimo operaciją. (Ši operacija taip pat vadinama duomenų prievado operacija).

> [!NOTE]
> - Šaltinio svetainė bus skaitoma tik per vietos kopijavimo operacijos trukmę.
> - Nukopijuojamos tik publikuotos dokumentų versijos. Jei versijos nebuvo publikuotos, nukopijuojamos tik paskutinės versijos.
> - Paskirties svetainėje nebus galima turinio versijų retrospektyva.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Kopijuoti svetainę el. komercijos aplinkoje

Norėdami nukopijuoti svetainę el. komercijos aplinkoje, atlikite šiuos veiksmus.

1. Prisiregistruokite prie aplinkos, kurioje norite vykdyti kopijavimo operaciją, generatoriaus.
1. Atidarykite svetainių sąrašo rodinį viršutiniame **dešiniajame kampe** pasirinkdami Svetainės perjungimo priemonė ir pasirinkdami Tvarkyti **svetaines**.
1. Raskite svetainę, kurią norite kopijuoti ar pakeisti, ir pasirinkite ją pažymėdami prie svetainės pavadinimo esantį žymės langelį.
1. Komandų juostoje pasirinkite Kopijuoti **svetainę**.
1. **Lauke Naujas** svetainės pavadinimas įveskite naujos **svetainės pavadinimą**, išsamūs kopijos svetainės meniu. Naujas svetainės pavadinimas turi būti unikalus el. komercijos aplinkoje. Šaltinio **nuomininkų** ir **šaltinio svetainės** laukai automatiškai nustatomi pagal dabartinio nuomininko ir pasirinktos svetainės informaciją.
1. Pasirinkite **Kurti kopiją**.

Patikrinę informaciją, pranešimas nurodo, kad sukurta nauja svetainės kopijavimo užduotis. Jūs galite stebėti užduoties progresą dešinėje [nuomininkų **užduočių puslapio** srityje](#monitor-the-site-copy-operation). Kai kopijavimo operacija sėkmingai baigiama, nauja svetainė rodoma svetainių sąrašo rodinio svetainių sąraše.

Šioje iliustracijoje rodomas svetainės generatoriaus **iškeliamos** svetainės meniu Kopijuoti svetainę pavyzdys.

![Kopijuoti svetainės ištūstų meniu svetainės generatoriuje.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Kopijuoti svetainę tarp dviejų el. komercijos aplinkos

Norėdami kopijuoti svetainę tarp dviejų el. komercijos aplinkos, atlikite šiuos veiksmus.

1. Prisiregistruokite prie paskirties el. komercijos aplinkos svetainės generatoriaus.
1. Komandų juostoje pasirinkite Kopijuoti **svetainę**.
1. **Lauke Naujas** svetainės pavadinimas įveskite naujos **svetainės pavadinimą**, išsamūs kopijos svetainės meniu. Naujas svetainės pavadinimas turi būti unikalus el. komercijos aplinkoje.
1. **Lauke Šaltinio nuomininkas** pasirinkite šaltinio nuomininko pavadinimą.
1. **Lauke Šaltinio svetainė** pasirinkite šaltinio šaltinį.
1. Pasirinkite **Kurti kopiją**.

> [!NOTE]
> Nuomininkų administratoriaus teisės būtinos ir šaltinio, ir paskirties el. komercijos aplinkose.

Patikrinę informaciją, pranešimas nurodo, kad sukurta nauja svetainės kopijavimo užduotis. Jūs galite stebėti užduoties progresą dešinėje [nuomininkų **užduočių puslapio** srityje](#monitor-the-site-copy-operation). Kai kopijavimo operacija sėkmingai baigiama, nauja svetainė rodoma svetainių sąrašo rodinio svetainių sąraše.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Susieti kanalus atliekant svetainės kopijavimo operaciją (pasirinktinai)

Šaltinio kanalai ir vietos gali būti susieti su paskirties kanalais ir lokalmis kaip svetainės kopijos operacijos dalis. Jei kanalas susiejamas kaip vietos kopijavimo operacijos dalis, svetainės inicijavimas naudojant FRE procesą ir kanalų konfigūravimas svetainės nustatymuose nebūtinas. 

Norėdami susieti visus kanalus ir vietos "taip kaip yra" (nuo 1 iki 1) svetainės generatoriuje, atlikite šiuos veiksmus.

1. Atidarykite svetainių sąrašo rodinį viršutiniame **dešiniajame kampe** pasirinkdami Svetainės perjungimo priemonė ir pasirinkdami Tvarkyti **svetaines**.
1. Raskite svetainę, kurią norite kopijuoti ar pakeisti, ir pasirinkite ją pažymėdami prie svetainės pavadinimo esantį žymės langelį.
1. Komandų juostoje pasirinkite Kopijuoti **svetainę**.
1. Meniu Kopijuoti **svetainę iškeliant** įveskite naujų **svetainės** pavadinimo, **·** **šaltinio nuomininkų ir šaltinio svetainės** (jei dar nėra) vertes.
1. Pasirinkite **Įtraukti kanalo susiejimus**.
1. Svetainės kanalų **ir vietų iškvietos** meniu sukonfigūruokite iškvietos meniu, **pasirinkite** Šaltinio kanalas, tada pasirinkite šaltinio kanalą.  
1. Pasirinkite **paskirties kanalą**, tada pasirinkite tą patį kanalą kaip šaltinio kanalas. 
1. Pasirinkite **Įtraukti lokalę**.
1. Pasirinkite **Šaltinio lokalė**, tada pasirinkite šaltinio lokalę.
1. Pasirinkite **Paskirties vietą**, tada pasirinkite tą pačią vietą kaip šaltinio vieta. 
1. Įveskite **unikalų URL** maršrutą, kuris šiuo metu nėra naudojamas paskirties aplinkoje.
1. Pakartokite žingsnius 8–11, kad kiekviena lokalė būtų susietos su kanalu.
1. Pasirinkite **Taikyti**.
1. Kiekvienam šaltinio kanalui pakartokite 6–11 veiksmus.
1. Pasirinkite **Uždaryti**.
1. Peržiūrėkite konfigūraciją, kad ji būtų tikslus, ir pasirinkite **Kopijuoti svetainę**.

> [!NOTE]
> Visi šaltinio kanalai ir vietos turi būti susieti ir gali būti susieti tik vieną kartą.

## <a name="monitor-the-site-copy-operation"></a>Stebėti vietos kopijavimo operaciją

Norėdami stebėti vietos kopijavimo operacijos eigą, atlikite šiuos veiksmus.

1. Prisiregistruokite prie paskirties el. komercijos aplinkos svetainės generatoriaus.
1. Kairiajame lange pasirinkite nuomininkų **užduotis**.
1. Nuomininkų **užduočių puslapyje** raskite ir pasirinkite svetainės kopijos užduotį iš sąrašo. Sritis pasirodo dešinėje ir rodo pasirinktos užduoties būseną ir informaciją.

Galite atšaukti užduotį, kurios būsena **Vykdoma**. Pasirinkite užduotį iš sąrašo, tada komandų juostoje **pasirinkite** Atšaukti.

Galite kartoti užduotį, kurios būsena Nepavyko arba **Baigta**, **kai yra klaidų**. Pasirinkite užduotį iš sąrašo ir komandų juostoje **pasirinkite** Kartoti.

> [!NOTE]
> Vaizdo įrašų turto apdorojimas gali tęstis baigus kopijuoti užduotį.

Šioje iliustracijoje pateikiamas svetainės generatoriaus dešinioji **vietos nuomininkų** užduočių puslapio pavyzdys.

![Užduoties informacija, esanti svetainės generatoriaus dešiniųjų nuomininkų užduočių puslapio srityje.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Inicijuoti naują svetainę naudojant FRE procesą

Prieš pradedant naują svetainę, ji turi būti inicijuota naudojant FRE procesą.

Norėdami inicijuoti naują svetainę naudodami FRE procesą, atlikite šiuos veiksmus.

1. Prisiregistruokite prie naujos svetainės generatoriaus.
1. Atidarykite svetainių sąrašo rodinį viršutiniame **dešiniajame kampe** pasirinkdami Svetainės perjungimo priemonė ir pasirinkdami Tvarkyti **svetaines**.
1. Raskite ir pasirinkite naują svetainę, kurią norite inicijuoti.
1. **Svetainės nustatymo dialogo lange** lauke **Pasirinkti domeną pasirinkite** domeną. Visus domenus, kurie inicijavimo metu buvo susieti su el. komercijos aplinka, galima pasirinkti.
1. Lauke Pasirinkti **numatytąjį kanalą** pasirinkite susietą interneto parduotuvės kanalą. Pasirinktas kanalas pateiks asortimentus ir kitą informaciją, kuri saugoma "Commerce Headquarters".
1. Lauke Pasirinkti **numatytąją kalbą** pasirinkite numatytąją kūrimo kalbą. Galima pasirinkti visas pasirinkto interneto parduotuvės kanalo konfigūracijas.
1. Lauke Maršrutas **reikšmė** susideda iš pagrindinio domeno ir pasirenkamo URL maršruto, kurį galite įvesti. Galite palikti URL maršrutą tuščią, jei kanalas bus naudojamas domeno šakniniame kataloge arba jei vėliau kanalo konfigūracijos rodinyje norite įvesti šią informaciją svetainės generatoriuje. Svetainės maršrutas turi būti unikalus el. komercijos aplinkoje.
1. Pasirinkite **Gerai**. Svetainė inicijuojama, naudojant jūsų pateiktą informaciją, ir jūs esate persiųstas į svetainės valdymo rodinį.

Šioje iliustracijoje pateikiamas svetainės generatoriaus **nustatymo dialogo** lango pavyzdys.

![Nustatykite savo svetainės dialogo langą svetainės generatoriuje.](media/site-copy_3.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[„robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-b2c-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-b2c-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
