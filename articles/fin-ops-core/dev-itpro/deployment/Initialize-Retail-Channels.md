---
title: „Commerce Scale Unit“ (debesyje) inicijavimas
description: Šioje temoje paaiškinama, kaip inicijuoti komercijos masto vienetą (debesį)Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 84e70515accde161e7efa36755edec68d26be952
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092225"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>„Commerce Scale Unit“ (debesyje) inicijavimas

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip inicijuoti komercijos masto vienetą (debesį)Microsoft Dynamics 365 Commerce.

Jei naudojate 2 pakopos smėlio dėžę arba gamybinę aplinką, kurios programos versija yra 8.1.2.x arba naujesnė, turite inicijuoti komercijos mastelio vienetą (debesį), kad galėtumėte naudoti mažmeninės prekybos kanalo funkcijas pardavimo vietoje (POS) arba el. prekybos operacijoms, kai debesyje naudojamas Retail Server. Inicijuojant bus įdiegtas komercijos masto vienetas (debesis).

> [!IMPORTANT]
> Esamiems klientams, naudojantiems mažmeninės prekybos kanalo funkcijas debesyje, kad užtikrintumėte nuolatinį ir nenutrūkstamą jūsų verslo palaikymą, reikalaujame atnaujinti savo mažmeninės prekybos kanalus, kad galėtumėte naudoti komercijos masto vienetą. Naujos aplinkos, įdiegtos be „Commerce Scale Unit“, nebegaus debesyje priglobtų mažmeninės prekybos kanalų komponentų kokybės ir paslaugų naujinių. Klientams, kurie naudojasi tik „Commerce Scale Unit“ (savarankiškai priegloba), nereikia jokių veiksmų. Jei reikia plėtinio, susisiekite su „Microsoft FastTrack“ sprendimų architektu.

## <a name="prerequisites"></a>Būtinieji komponentai

1. Įdiekite 2 pakopos smėlio dėžę arba gamybos aplinką, kurios versija yra 8.1.2.x arba naujesnė.
2. Galite savarankiškai įdiegti iki 2 komercijos masto vienetų vienoje aplinkoje. Jei jums reikia daugiau nei 2 komercijos masto vienetų vienoje aplinkoje, žr Microsoft Dynamics Lifecycle Services (LCS), sukurkite palaikymo užklausą ir įveskite **Užklausa dėl papildomo komercinio masto vieneto** ir nurodykite aplinkos ID, komercijos masto vienetų skaičių ir norimus duomenų centro regionus. Prašymas bus įvykdytas per penkias darbo dienas. Jei jums nereikia daugiau nei 2 komercijos masto vienetų vienoje aplinkoje, jums nereikia kurti palaikymo užklausos. 
3. Kad galėtumėte inicijuoti „Commerce Scale Unit“, turite turėti projekto savininko leidimus „Lifecycle Services“.
4. Įsitikinkite, kad jūsų aplinkoje įjungti mažmeninės prekybos licencijos konfigūracijos raktai. Daugiau informacijos žr [Licencijos kodų ir konfigūracijos raktų ataskaita](../sysadmin/license-codes-configuration-keys-report.md). Turite įjungti toliau nurodytus klavišus, kad galėtumėte naudoti „Commerce Scale Unit“.

    - RetailBasic
    - RetaileCommerce – jei planuojate naudoti el. prekybą Dynamics 365 Commerce.
    - RetailGiftCard – jei planuojate naudoti dovanų korteles.
    - RetailInvent – jei planuojate naudoti atsargas.
    - RetailModernPos – jei planuojate naudoti pardavimo vietą (POS).
    - RetailReplenishment – jei planuojate naudoti papildymus.
    - RetailScheduler
    - Mažmeninės parduotuvės – jei planuojate naudoti POS.


## <a name="region-availability"></a>Regiono prieinamumas
„Commerce Scale Unit“ galima diegti šiuose regionuose.

| Pasaulinė vieta | Regionas              | Prieinamumas        |
|-----------------|---------------------|---------------------|
| AMERIKA        | Rytų JAV             | Bendrai prieinama |
| AMERIKA        | Rytų JAV 2           | Bendrai prieinama |
| AMERIKA        | Šiaurės vidurio JAV    | Bendrai prieinama |
| AMERIKA        | Pietų vidurio JAV    | Bendrai prieinama |
| AMERIKA        | JAV centras          | Bendrai prieinama |
| AMERIKA        | Vakarų JAV             | Bendrai prieinama |
| AMERIKA        | Vakarų JAV 2           | Bendrai prieinama |
| AMERIKA        | Kanados centrinė dalis      | Ribotas pajėgumas    |
| AMERIKA        | Rytų Kanada         | Ribotas pajėgumas    |
| AMERIKA        | Vakarų Centrinė JAV     | Ribotas pajėgumas    |
| APAC            | Rytų Australija      | Bendrai prieinama |
| APAC            | Pietryčių Azija      | Bendrai prieinama |
| APAC            | Rytų Japonija          | Bendrai prieinama |
| APAC            | Vakarų Japonija          | Bendrai prieinama |
| APAC            | Pietryčių Australija | Ribotas pajėgumas    |
| APAC            | Rytų Azija           | Ribotas pajėgumas    |
| APAC            | Pietų Indija         | Ribotas pajėgumas    |
| APAC            | Centrinė Indija       | Ribotas pajėgumas    |
| EMEA            | Vakarų Europa         | Bendrai prieinama |
| EMEA            | Šiaurės Europa        | Bendrai prieinama |
| EMEA            | JK pietuose            | Ribotas pajėgumas    |
| EMEA            | JK vakarai             | Ribotas pajėgumas    |

Diegimo pajėgumai riboto pajėgumo regionuose yra labai riboti. Prašymai dėl diegimo vertinami kiekvienu konkrečiu atveju. Jei turite įtikinamų verslo poreikių diegti riboto pajėgumo regionuose, galite pateikti paramos užklausą, kad būtumėte įtraukti į laukiančiųjų sąrašą.

![Žemėlapis, kuriame rodomas regiono prieinamumas.](media/Commerce-Scale-Unit-Region-Availability.png "Žemėlapis, kuriame rodomas regiono prieinamumas")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Inicijuoti komercijos masto vienetą kaip naujos aplinkos diegimo dalį

Įsitikinkite, kad būstinė yra laisva. Tai reikalinga norint užregistruoti masto vienetą būstinėje inicijavimo proceso metu. Nerekomenduojama inicijuoti svarstyklių bloko, kai būstinė yra prižiūrima, nes atliekant techninės priežiūros procesą jis gali būti neprieinamas.

1. Įsitikinkite, kad būstinės aplinka yra prieinama, o ne joje [Priežiūros režimas](../sysadmin/maintenance-mode.md).
2. LCS aplinkos informacijos puslapyje pasirinkite **Aplinkos ypatybės \> Komercija**.
3. Puslapyje „Commerce“ sąrankos diegimas pasirinkite **Inicijuoti**.
4. Pasirinkite „Commerce Scale Unit“ versiją, kurią norite inicijuoti.
5. Pasirinkite regioną, kuriame norite inicijuoti „Commerce Scale Unit“.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigūruokite kanalus, kad būtų naudojamas komercijos masto vienetas

Įdiegę „Commerce Scale Unit“ turite įsitikinti, kad jūsų kanalai sukonfigūruoti naudoti duomenų bazę. 

Norėdami sukonfigūruoti savo kanalus naudoti komercijos masto vieneto duomenų bazę, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Mažmeninė prekyba ir prekyba \> Būstinės įrengimas \> Prekybos planuotojas \> Kanalų duomenų bazė**.
1. Kairiojoje srityje pasirinkite kanalo duomenų bazę.
1. Ant **Mažmeninės prekybos kanalas** FastTab, pasirinkite **Papildyti**, tada išskleidžiamajame sąraše pasirinkite savo mažmeninės prekybos kanalą.
1. Pasirinkite **Papildyti**, tada išskleidžiamajame sąraše pasirinkite savo internetinį kanalą. 

Kai baigsite, eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Platinimo grafikas**, ir vykdyti darbą 9999.

> [!NOTE] 
> „Job 9999“ sinchronizuoja visus naujus produktus ir klientus su „Commerce Scale Unit“. Šis procesas gali užtrukti ilgai. Jei kanalas turi būti pasiekiamas tik el. prekybos svetainių kūrimo priemonės konfigūracijai, vietoj 9999 galite vykdyti 1070 užduotį.

### <a name="database-refresh-and-commerce-scale-units"></a>Duomenų bazės atnaujinimas ir prekybos masto vienetai

Prieš pradėdami įsitikinkite, kad esate susipažinę su [Veiksmai, kuriuos reikia atlikti po duomenų bazės atnaujinimo aplinkose, kuriose naudojamos „Commerce“ funkcijos](../database/database-refresh.md).

Mastelio vieneto kanalo duomenų bazės įrašai (kanalo duomenų bazės formoje) negali būti perkeliami į aplinką kaip duomenų bazės atnaujinimo dalis. Taip yra todėl, kad įrašai atspindi konkrečios aplinkos konfigūraciją.

Atnaujinus duomenų bazę, galite atkurti mastelio vieneto kanalo duomenų bazės įrašą, iš naujo įdiegdami savo mastelio įrenginį LCS. Bet kokia dislokavimo ar aptarnavimo operacija svarstyklių bloke bandys užregistruoti svarstyklių bloką būstinėje, jei bus nustatyta, kad registracijos nėra.

Galite leisti iš naujo įdiegti mastelio įrenginį nekeisdami jokių komponentų, pasirinkę diegti tą pačią versiją, kurią jau naudoja jūsų mastelio įrenginys. Tai galima padaryti LCS atliekant šiuos veiksmus:

1. LCS aplinkos informacijos puslapyje pasirinkite **Aplinkos ypatybės \> Mažmeninė**.
2. Sąrankos diegimo puslapyje pasirinkite mastelio vienetą, kurį norite perskirstyti.
3. Svarstyklių įrenginio veikimo meniu pasirinkite **Atnaujinti**.
4. Slankikliu, išskleidžiamajame meniu **Pasirinkite versiją**, pasirinkite parinktį **Nurodykite versiją**.
5. Žemiau esančiame teksto laukelyje **Nurodykite versiją**, įveskite savo mastelio vieneto versiją, rodomą šalia **Dabartinė versija** etiketė.
6. Spustelėkite **Atnaujinti** mygtuką.

Jums nereikia rinktis **Atnaujinkite plėtinius**, net jei anksčiau taikėte plėtinius, nes paskutinis mastelio blokui pritaikytas plėtinių paketas automatiškai parenkamas atnaujinant mastelio bloką.

Jei turite kelis svarstyklių vienetus, aukščiau aprašytą operaciją turite atlikti kiekvienam svarstyklių vienetui. Jei pageidaujate, šias operacijas galite atlikti lygiagrečiai.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Įdiekite papildomus prekybos masto vienetus (neprivaloma)

Kai inicijuojate „Commerce Scale Unit“, galite savarankiškai įdiegti antrą masto vienetą, jei jūsų licencija suteikia jums teisę tai padaryti. Norėdami įdiegti daugiau nei du mastelio vienetus, turite sukurti palaikymo užklausą. Palaikymo užklausoje nurodykite reikalingų prekybos masto vienetų skaičių, aplinkos pavadinimą ir norimus regionus. Daugiau informacijos apie licencijavimą žr [„Dynamics 365“ licencijavimo vadovas](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Kiekvienam papildomam komercijos masto vienetui, kurį įdiegėte, rekomenduojame sukurti atskirą kanalų duomenų bazės grupę, atlikdami šiuos veiksmus.

1. „Commerce“ pagrindinėje buveinėje eikite į **Mažmeninė prekyba ir prekyba >Retail Headquarters > Mažmeninės prekybos planuoklio sąranka > Kanalų duomenų bazės grupė**.
2. Kurti naują kanalo duomenų bazių grupę.
3. Eikite į **Mažmeninė prekyba ir prekyba >Retail Headquarters > Mažmeninės prekybos planuoklio sąranka > Kanalų duomenų bazė** ir pasirinkite kanalo duomenų bazę, atitinkančią naujai sukurtą komercijos masto vienetą.
4. Pasirinkite **Redaguoti** ir pasirinkite naują kanalų duomenų bazės grupę.
5. Pasirinkite **Įrašyti**.
6. Pasirinkite **Paleiskite Visą duomenų sinchronizavimą** pasirinktai kanalų duomenų bazei.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Papildomi svarstymai, jei esamoje aplinkoje inicijuojate debesyje prieglobos prekybos kanalo komponentus

Jei aplinkoje jau naudojate debesyje priglobtus Commerce kanalo komponentus, komercijos masto vieneto inicijavimas padės sumažinti prastovos laiką, kai tie komponentai bus atnaujinami. Prieš inicijuojant „Commerce Scale Unit“ reikia papildomo planavimo.

Kai inicijuojate savo pirmąjį komercijos masto vienetą aplinkoje, kurioje naudojami debesies prieglobos komercijos kanalo komponentai, inicijavimo procesas perkels kanalus, susietus su debesies prieglobos kanalo komponentais, į pirmąjį mastelio įrenginį. Kanalai, susieti su parduotuvės masto vienetais, neturi įtakos.

Perėjimo procesas yra skaidrus kanalams. Prasidėjus mastelio bloko inicijavimui, automatiškai atliekamos šios operacijos:

1. Bus sukurtas ir su aplinka susietas naujas prekybos masto vienetas.
2. Prekybos masto vienetas bus užregistruotas kaip galima kanalų duomenų bazė būstinėje.
3. Visi kanalai susieti su **Numatytas** kanalų duomenų bazė būstinėje bus atnaujinta, kad atitiktų naują komercijos masto vienetą.
4. A Commerce Data Exchange (CDX) bus atliktas visiškas duomenų sinchronizavimas, kad kanalo duomenys būtų perkelti į naują mastelio įrenginį.

**Prekybos masto vieneto inicijavimo planavimas ir testavimas** Paprastai inicijuodami „Commerce Scale Unit“ turite planuoti penkių valandų prastovos laikotarpį, skirtą parduotuvės operacijoms, taip pat bet kokioms el. prekybos kanalo operacijoms, kuriose naudojamas „Retail Server“ arba „Cloud Point of Sale“.

1. Atnaujinkite duomenų bazę iš gamybos aplinkos į smėlio dėžės UAT aplinką. 
2. Inicijuoti komercijos masto vienetą smėlio dėžės UAT aplinkoje. 
3. Atkreipkite dėmesį į komercijos masto vieneto inicijavimo laiką. Tai bus panašu į laiką, kurį ši operacija užtrunka jūsų gamybos aplinkoje, kai parduotuvės operacijos ir el. prekybos operacijos nebus pasiekiamos.

Prieš inicijuodami „Commerce Scale Unit“ turite atlikti šiuos papildomus veiksmus.

- **Uždarykite visas POS pamainas** - Po perkėlimo POS vartotojai negalės uždaryti jokių pamainų, kurios buvo aktyvios perkėlimo proceso metu.
- **Patvirtinkite, kad visi P darbai buvo sėkmingai atlikti** - Rekomenduojama, kad P-užduotys, skirtos sinchronizuoti laukiančias operacijas, būtų baigtos prieš inicijuojant CSU.
- **Atsijunkite nuo visų POS įrenginių** - Perkėlimo metu POS operacijos nepalaikomos.
- **Atšaukti ir panaikinti visas sustabdytas operacijas POS** – Sustabdytos operacijos neišsaugomos kaip inicijavimo dalis.

> [!IMPORTANT]
> Inicijuojant „Commerce Scale Unit“ ankstesnės sustabdytos operacijos bus prarastos ir jų nebus galima atšaukti. 

Štai kas vyksta inicijavimo laikotarpiu:

- Debesyje priglobti prekybos kanalai neveiks, nebent įjungsite POS neprisijungus funkciją.
- POS įrenginių, kurių funkcija neprisijungus, funkcija bus sumažinta.
- Bet kokie el. prekybos klientai, kurie priklauso nuo mažmeninės prekybos serverio, bus sutrikdyti.
- Kanalai, kurie yra priglobti komercijos masto vienetuose (savarankiškai priglobti), nebus paveikti.
- Pagrindinės buveinės funkcionalumas neturi įtakos.

Štai kas nutinka po inicijavimo:

- Išsaugoma visų aktyvuotų POS įrenginių įrenginio aktyvavimo būsena, o tai reiškia, kad įrenginių nereikės aktyvinti iš naujo.
- Atskiros aparatinės įrangos stoties egzemplioriai veiks ir toliau.
- POS kanalo ataskaitos bus nustatytos iš naujo ir jose nebus rodomi duomenys, buvę prieš inicijavimą.
- Žurnalo rodymo operacija taip pat bus nustatyta iš naujo ir nebus rodomi duomenys, buvę prieš inicijavimą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
