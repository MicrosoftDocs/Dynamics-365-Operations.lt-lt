---
title: „Commerce Scale Unit“ (debesyje) inicijavimas
description: Šiame straipsnyje paaiškinama, kaip inicijuoti "Commerce Scale Unit" (debesį)Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 25ca054df6422370b1e61dff7965189ad90d7fcc
ms.sourcegitcommit: 7bcaf00a3ae7e7794d55356085e46f65a6109176
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/26/2022
ms.locfileid: "9357664"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>„Commerce Scale Unit“ (debesyje) inicijavimas

[!include[banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip inicijuoti "Commerce Scale Unit" (debesį)Microsoft Dynamics 365 Commerce.

Jei naudojate "Tier-2" sandų dėžę arba gamybos aplinką, kurioje yra 8.1.2.x arba naujesnė versijos programa, turite inicijuoti "Commerce Scale Unit" (debesį) ir tik tada galėsite naudoti mažmeninės prekybos kanalo funkcijas point sale (EKA) operacijoms arba el. komercijos operacijoms, kurios debesyje naudoja "Retail Server". Inicijuojant bus diegiamas "Commerce Scale Unit" (debesis).

> [!IMPORTANT]
> Norint užtikrinti nuolat ir nenusitęsią klientų, kurie naudoja mažmeninės prekybos kanalo funkcijas debesyje, verslo palaikymą, mes reikalaujame atnaujinti mažmeninės prekybos kanalus ir naudoti "Commerce Scale Unit". Naujos aplinkos, įdiegtos be "Commerce Scale Unit", nebegaus "Commerce Scale Unit" ir nebegaus "Commerce Scale Unit" kokybės ir paslaugų naujinimų, skirti "Retail" kanalo komponentams, kurie skirti debesies nuomojamoms svetainėms. Klientams, kurie naudoja tik "Commerce Scale Unit" (savitarnos), nereikia atlikti jokių veiksmų. Jei reikia plėtinio, kreipkitės į architektą "Microsoft FastTrack" sprendimą.

## <a name="prerequisites"></a>Būtinieji komponentai

1. Įdiekite "Tier-2" sand. dėžę arba gamybos aplinką, kurioje yra 8.1.2.x arba naujesnė versija.
2. Galima nustatyti ne daugiau kaip 2 "Commerce Scale Units" vienetus aplinkoje. Jei reikia daugiau nei 2 "Commerce Scale Unit" pagal aplinką, Microsoft Dynamics ciklo tarnybose (LCS) sukurkite palaikymo užklausą ir **įveskite papildomo "Commerce Scale** " vieneto užklausą ir nurodykite aplinkos ID, "Commerce Scale" vienetų skaičių ir norimus duomenų centro regionus. Užklausa bus baigta per penkis darbo dienas. Jei jums nereikia daugiau nei 2 "Commerce Scale Units" pagal aplinką, jums nereikia kurti palaikymo užklausos. 
3. Kad būtų galima inicijuoti "Commerce Scale Unit", reikia turėti valdymo ciklo tarnybų "Project Owner" teises.
4. Įsitikinkite, kad "Retail" licencijos konfigūracijos raktai yra įgalinti jūsų aplinkoje. Daugiau informacijos rasite licencijos kodų [ir konfigūracijos raktų ataskaita](../sysadmin/license-codes-configuration-keys-report.md). Norint naudoti "Commerce Scale Unit", turi būti įjungti šie raktai.

    - RetailBasic
    - RetaileCommerce – jei planuojate naudoti "E-Commerce", skirta Dynamics 365 Commerce.
    - RetailGiftCard – jei planuojate naudoti dovanų korteles.
    - RetailInvent – jei planuojate naudoti atsargas.
    - RetailModionalPos – jei planuojate naudoti point of sale (EKA).
    - RetailReplenishment – jei planuojate naudoti papildymus.
    - RetailScheduler
    - RetailStores – jei planuojate naudoti EKA.


## <a name="region-availability"></a>Regiono prieinamumas
"Commerce Scale Unit" galima diegti toliau nurodytose regionuose.

| Visuotinė vieta | Regionas              | Esamumas        | Komentarai                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERICAS        | Rytų JAV             | Bendrai prieinama |  Komentarų nėra.                         |
| AMERICAS        | Rytų JAV 2           | Bendrai prieinama |  Komentarų nėra.                          |
| AMERICAS        | Šiaurės vidurio JAV    | Ribotas pajėgumas    |  Komentarų nėra.                            |
| AMERICAS        | Pietų vidurio JAV    | Ribotas pajėgumas    |  Komentarų nėra.                            |
| AMERICAS        | JAV centras          | Bendrai prieinama |  Komentarų nėra.                            |
| AMERICAS        | Vakarų JAV             | Bendrai prieinama |  Komentarų nėra.                            |
| AMERICAS        | West JAV 2           | Bendrai prieinama |  Komentarų nėra.                            |
| AMERICAS        | Kanados centrinis centras      | Ribotas pajėgumas    |  Komentarų nėra.                            |
| AMERICAS        | Kanados Rytų         | Ribotas pajėgumas    |   Komentarų nėra.                           |
| AMERICAS        | West Central US     | Ribotas pajėgumas    |   Komentarų nėra.                           |
| APAC            | Rytų Australija      | Bendrai prieinama |   Komentarų nėra.                           |
| APAC            | Pietryčių Azija      | Pajėgumas apribotas | Diegti neleidžiama.    |
| APAC            | Rytų Japonija          | Bendrai prieinama |  Komentarų nėra.                            |
| APAC            | Vakarų Japonija          | Bendrai prieinama |   Komentarų nėra.                           |
| APAC            | Pietryčių Australija | Bendrai prieinama |   Komentarų nėra.                           |
| APAC            | Rytų Azija           | Ribotas pajėgumas    |   Komentarų nėra.                           |
| APAC            | Indija, Pietų         | Pajėgumas apribotas | Diegti neleidžiama.    |
| APAC            | Indijos centrinis centras       | Ribotas pajėgumas    | Reikalauja patvirtinimo proceso. |
| EMEA            | Vakarų Europa         | Bendrai prieinama    |  Komentarų nėra. |
| EMEA            | Šiaurės Europa        | Bendrai prieinama    |  Komentarų nėra. |
| EMEA            | Pietų Jk            | Bendrai prieinama |    Komentarų nėra.                          |
| EMEA            | UK West             | Bendrai prieinama |    Komentarų nėra.                          |
| Šveicarija     | Šveicarijos Šiaurės   | Ribotas pajėgumas    | Reikalauja patvirtinimo proceso. |
| Jae             | JAE Šiaurės           | Ribotas pajėgumas    | Reikalauja patvirtinimo proceso. |

Diegimas ribotuose pajėgumų regionuose yra ypač apribotas. Diegimo užklausos įvertinamos kiekvienu atveju atskirai. Jei turite verslo išteklių, kuriuos reikia įdiegti riboto pajėgumo regionuose, galite pateikti palaikymo užklausą, kurią reikia įtraukti į laukimo sąrašą. Šiuo metu pajėgumų ribotieji sritys šiuo metu neleidžia diegti "Commerce Scale Unit". 

![Žemėlapis, kuriame rodomas regiono pasiekiamumas.](media/Commerce-Scale-Unit-Region-Availability.png "Susieti, kad būtų rodomas regiono pasiekiamumas")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Inicijuoti "Commerce Scale Unit" kaip naujos aplinkos diegimo dalį

Įsitikinkite, kad yra būstinė. Tai būtina užregistruoti skalės vienetą su būstinėmis inicijavimo proceso metu. Nerekomenduojama inicijuoti svarstyklių vieneto, kai būstinė yra nepalaikoma, nes atliekant aptarnavimo procesą jis gali būti negalimas.

1. Įsitikinkite, kad būstinės aplinka pasiekiama, o ne [priežiūros režimu](../sysadmin/maintenance-mode.md).
2. LCS aplinkos informacijos puslapyje pasirinkite Aplinkos funkcijos **" \> Commerce"**.
3. "Commerce setup deployment" puslapyje pasirinkite **Inicijuoti**.
4. Pasirinkite "Commerce Scale Unit" versiją, kurią norite inicijuoti.
5. Pasirinkite regioną, kuriame norite inicijuoti "Commerce Scale Unit".

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigūruoti kanalus, kad būtų galima naudoti "Commerce Scale Unit"

Įdiegę "Commerce Scale Unit" turite užtikrinti, kad jūsų kanalai sukonfigūruoti naudoti jai duomenų bazę. 

Norėdami konfigūruoti savo kanalus ir naudoti "Commerce Scale Unit" duomenų bazę, atlikite šiuos veiksmus.

1. Commerce Headquarters eikite į "Retail" **ir "Commerce \> Headquarters" nustatymą " \> Commerce Scheduler \> Channel" duomenų bazę**.
1. Kairiajame lange pasirinkite kanalų duomenų bazę.
1. Mažmeninės prekybos **kanalo "** FastTab" **pasirinkite** Įtraukti, tada išplečiamajame sąraše pasirinkite mažmeninės prekybos kanalą.
1. Pasirinkite **Įtraukti**, tada išplečiamajame sąraše pasirinkite interneto kanalą. 

Baigę eikite į "Retail" ir " **Commerce Retail" ir "Commerce \> IT \> Distribution" grafiką** ir vykdykite 9999 užduotį.

> [!NOTE] 
> Užduotis 9999 sinchronizuoja visus naujus produktus ir klientus su "Commerce Scale Unit". Šis procesas gali ilgai užtrukti. Jei kanalas turi būti galimas tik el. komercijos svetainės generatoriaus konfigūracijai, vietoj užduoties 9999 galite vykdyti 1070 užduotį.

### <a name="database-refresh-and-commerce-scale-units"></a>Duomenų bazės atnaujinimas ir "Commerce Scale Units"

Prieš pradėdami įsitikinkite, kad baigę duomenų [bazės atnaujinimą esate susipažinę su "Commerce" funkciją naudojančiais veiksmais](../database/database-refresh.md).

Skalės vieneto kanalo duomenų bazės įrašų (formoje Kanalo duomenų bazė) negalima perkelti iš aplinkos kaip duomenų bazės atnaujinimo dalis. Taip yra todėl, kad įrašai atspindi aplinkos konfigūraciją.

Atnaujinę duomenų bazę galite iš naujo sugeneruoti skalės vieneto kanalų duomenų bazės įrašą, iš naujo įdę svarstyklių vienetą LCS. Bet kokia diegimo ar aptarnavimo operacija svarstyklių vienetais bandys užregistruoti svarstyklių vienetą būstinėje, jei registracijos nėra.

Galite iš naujo įdiegti skalės vienetą nekeičiant jokių komponentų, pasirinkdami diegti tą pačią versiją, kurios svarstyklių vienetas jau yra. Tai galima atlikti LCS, naudojant šiuos veiksmus:

1. LCS aplinkos informacijos puslapyje pasirinkite Aplinkos funkcijos **" \> Retail"**.
2. Nustatymo diegimo puslapyje pasirinkite skalės vienetą, kurį norite diegti iš naujo.
3. Skalės vieneto operacijų meniu pasirinkite **Naujinti**.
4. Išplečiamajame versijos Pasirinkti lauke **pasirinkite** pasirinktį Nurodyti **versiją**.
5. Teksto lauko dalyje Nurodyti versiją **įveskite versiją**, rodomą jūsų skalės vienetui, rodomą šalia dabartinės **versijos** žymos.
6. Spustelėkite mygtuką **Atnaujinti**.

Jums nereikia pasirinkti **Plėtinių Naujinti, net jei plėtinius taikėte anksčiau, nes paskutinis skalės vienetui pritaikytas plėtinio paketas automatiškai parenkamas atnaujinant svarstyklių** vienetą.

Jei turite kelis svarstyklių vienetus, turite atlikti operaciją virš kiekvieno svarstyklių vieneto. Jei reikia, šias operacijas galite atlikti lygiagrečiai.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Papildomų "Commerce Scale Units" diegimas (pasirinktinai)

Inicijadinę "Commerce Scale Unit", galite savitarnos diegti antrą skalės vienetą, jei jūsų licencija leidžia tai daryti. Norėdami diegti daugiau nei du skalės vienetus, turite sukurti palaikymo užklausą. Palaikymo užklausoje pateiskite pageidaujamų "Commerce Scale Units" skaičių, aplinkos pavadinimą ir norimus regionus. Daugiau informacijos apie licencijavimą ieškokite " [Dynamics 365" licencijavimo vadove](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Rekomenduojame kiekvienam papildomam "Commerce Scale" vienetui, kurį diegiate, sukurti atskirą kanalo duomenų bazės grupę, atlikti šiuos veiksmus.

1. Komercijos biure eikite į " **Retail" ir "Commerce > Retail Headquarters > Scheduler nustatymas > Kanalo duomenų bazės grupė**.
2. Kurti naują kanalo duomenų bazių grupę.
3. Eikite **į mažmeninės prekybos ir komercijos > Retail Headquarters > duomenų bazės duomenų bazės "Retail Scheduler>** ir pasirinkite kanalų duomenų bazę, kuri atitinka naujai sukurtą "Commerce Scale Unit".
4. Pasirinkite **Redaguoti ir** pasirinkite naują kanalo duomenų bazės grupę.
5. Pasirinkite **Įrašyti**.
6. Pasirinkite **pasirinktos kanalų duomenų bazės** parinktis Vykdyti visą duomenų sinchronizavimą.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Papildomos aplinkybės, jei inicijuojate debesies nuomojamus "Commerce" kanalo komponentus esamoje aplinkoje

Jei jau naudojate debesies nuomojamus "Commerce" kanalo komponentus aplinkoje, "Commerce Scale Unit" inicijavimas padės sumažinti prasto laiką, kai šie komponentai bus atnaujinti. Prieš inicijuojant "Commerce Scale Unit" reikia papildomo planavimo.

Kai inicijuojate savo pirmąjį "Commerce Scale" vienetą aplinkoje, kurioje naudojami "Commerce" kanalo komponentai, inicijavimo procesas perkels kanalus, susietus su debesies nuomojamais kanalo komponentais į pirmą skalės vienetą. Kanalai, susieti su parduotuvių skalės vienetais, nėra susiję.

Perkėlimo procesas yra permatomas kanalams. Po to, kai pradedamas skalės vieneto inicijavimas, automatiškai atliekamos šios operacijos:

1. Bus sukurtas naujas "Commerce Scale Unit" ir susietas su aplinka.
2. "Commerce Scale Unit" bus užregistruotas kaip galima kanalų duomenų bazė būstinėje.
3. Visi kanalai, susieti su numatytąja kanalų **duomenų** baze būstinėje, bus atnaujinti, kad būtų susieti su nauju "Commerce Scale Unit".
4. Siekiant Commerce Data Exchange kanalo duomenis atvesti į naują skalės vienetą, bus atliktas visas duomenų sinchronizavimas (CDX).

**"Commerce Scale Unit** " inicijavimo planavimas ir tikrinimas pagal bendrą taisyklę, inicijuojant "Commerce Scale Unit", parduotuvės operacijoms ir el. komercijos kanalo operacijoms, kurios naudoja "Retail Server" arba "Cloud Point of Sale", turi būti planuojama naudoti penkių valandų lėt. laiką.

1. Atnaujinkite duomenų bazę iš gamybos aplinkos į sandinę UAT aplinką. 
2. Inicijuoti "Commerce Scale Unit" sandbox UAT aplinkoje. 
3. Atsikreipkite dėmesį į "Commerce Scale Unit" inicijavimo laiką, kada reikia baigti. Tai bus lyginama su laiku, kurio reikia šiai operacijai jūsų gamybos aplinkoje, per kurį parduotuvės operacijos ir el. komercijos operacijos nebus galimos.

Prieš inicijuojant "Commerce Scale Unit", reikia atlikti šiuos papildomus veiksmus.

- **Uždarykite visas EKA** pamainas – po perkėlimo EKA vartotojai negalės uždaryti jokių perkėlimo proceso metu aktyvių pamainų.
- **Patikrinti, ar sėkmingai užbaigtos** visos P užduotys – rekomenduojama, kad prieš inicijuojant CSU būtų sinchronizuojamos laukiančios operacijos, būtų baigtos P užduotys.
- **Atsijungti nuo visų EKA įrenginio** – perkėlimo metu EKA operacijos nepalaikomos.
- **Atšaukti ir anuliuoti visas sulaikytas EKA operacijas** – sulaikytos operacijos nebus išsaugotos kaip inicijavimo dalis.

> [!IMPORTANT]
> Kaip "Commerce Scale Unit" inicijavimo dalis bus prarastos anksčiau sustabdytos operacijos ir jų negalima atšaukti. 

Čia yra tai, kas vyksta inicijavimo laikotarpiu:

- Debesyje laikomi "Commerce" kanalai neveikia, nebent įjungiate EKA atjungties režimu funkciją.
- Jei EKA įrenginiai, kuriuose įjungta autonominė funkcija, bus sumažintos funkcijos.
- Visi el. "Commerce" klientai, priklausomi nuo "Retail Server", bus nutraukti.
- "Commerce Scale Units" (savitarnos), laikomi kanalai nebus paveikti.
- Pagrindinės būstinės funkcijos nepaisomos.

Štai kas įvyksta baigus pradinio proceso pildyti:

- Išlaikoma visų suaktyvintų EKA įrenginių įrenginio suaktyvinimo būsena, o tai reiškia, kad įrenginių iš naujo aktyvinti nereikia.
- Autonominiai aparatūros stoties egzemplioriai toliau veiks.
- EKA kanalo ataskaitos bus iš naujo nustatyti ir nebus rodomi duomenys prieš inicijuojant.
- Rodyti žurnalo operaciją, taip pat bus iš naujo nustatyti ir nebus rodomi duomenys prieš pradinio inicijavimo metu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
