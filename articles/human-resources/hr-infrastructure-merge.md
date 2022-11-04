---
title: Dynamics 365 Human Resources infrastruktūros suliejimo peržiūra
description: Šiame straipsnyje aprašomas "Microsoft" infrastruktūros Dynamics 365 Human Resources suliejimas.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732774"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources infrastruktūros suliejimas 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>"Dynamics Human Resources 365"

"Microsoft Dynamics 365 Human Resources " pateikia įrankius, kurie padeda personalo komandoms padidinti organizacinį sąsumą, transformuoti darbuotojų patirtį ir optimizuoti personalo programas, kad būtų sukurta darbo vieta, kurioje žmonės ir verslas gali dingti. Norėdami sužinoti daugiau apie Dynamics 365 Human Resources, žr.[Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformuoti darbuotojo patirtį.** Išlaikykite aukščiausius dėstytojais ir suteikti teisę vadovams ir darbuotojams pereiti prie susijusios savitarnos patirties, kuri veikia įsipareigojimą ir didėjimo galimybes.
- **Optimizuokite personalo programas.** Padėti sumažinti veikimo išlaidas ir sukurti žmonių centines atostogas bei neatvykimą, laiką, išmokas ir kompensavimo valdymo programas.
- **Padidinti organizacijos skirstymo pagal terminus.** Įgalinti personalą, kad būtų galima dirbti su dexterity Dataverse Microsoft Power Platform, kuris reikalingas verslui, naudojant ir centralizuoti žmonių duomenis bei lengvai išplėsti Dynamics 365 Human Resources.
- **Atrasti darbo jėgos informaciją.** Priimti duomenimis pagrįstus sprendimus, suteikia galimybę analizuoti ir vizualizuoti žmonių duomenis raiškiosiose skelbimų lentose, kurios galimos bet kuriame įrenginyje.

## <a name="human-resources-infrastructure-merge"></a>Personalo infrastruktūros suliejimas

Dynamics 365 Human Resources yra atskira programa, šiuo metu naudojanti kitokią infrastruktūrą nei kitos finansų ir operacijų programėlės, pvz., "Dynamics 365 Finance" arba ".Dynamics 365 Supply Chain Management Infrastruktūros suliejimas įves tą Dynamics 365 Human Resources pačią infrastruktūrą kaip ir kitos finansų ir operacijų programėlės.

Norėdami daugiau sužinoti apie personalo infrastruktūros suliejimą, žr. personalo [pasiūlymų suliejimą](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Atsakymų į dažnai užduodamus klausimus ieškokite Personalo infrastruktūros [suliejimo DUK](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Kliento perkėlimas ir klientų suliejimas

Kaip infrastruktūros suliejimo dalis visos personalo programos galimybės prieinamos finansų ir operacijų aplinkose. Klientai gali perkelti savo personalo aplinkas naudodami perkėlimo įrankį, kurį galima naudoti ciklo Microsoft Dynamics tarnybose. Be to, pasirinktinai jie gali sulieti savo duomenis su esama finansų ir operacijų aplinka. 

Klientų perkėlimas ir klientų suliejimas skiriasi tokiu būdu:

- **Klientų perkėlimas** – automatizuotas perkėlimo įrankis naudojamas norint atlikti kliento duomenų bazės lifto ir pamainos perkėlimą iš personalo infrastruktūros į finansų ir operacijų infrastruktūrą. Rezultatas yra nauja finansų ir operacijų aplinka, kuri naudoja kliento personalo duomenų bazę. 
- **Klientų suliejimas** – šio papildomo veiksmo "Microsoft" reikalauja. Tai atliekama kliento laisvu ir kliento laiko juosta. Šio veiksmo metu kliento duomenys perkeliami į esamą aplinką, pvz., finansų arba projekto operacijų aplinką. Dažniausiai tai galima atlikti rankiniu būdu naudojant duomenų valdymo sistemos (DMF) duomenų objektus. 

## <a name="planning-a-human-resources-environment-migration"></a>Personalo aplinkos perkėlimo planavimas

Kaip infrastruktūros suliejimo dalis iš atskirą infrastruktūrą visi klientai turės perkelti savo esamas personalo aplinkas. Siekiant padėti šiam procesui rekomenduojame naudoti automatinį perkėlimo įrankį ciklo tarnybose, kad perkeltų jūsų dabartines aplinkas į naują infrastruktūrą. 

Toliau pateikties skyriuose pateikiama daugiau informacijos, kaip naudoti ciklo tarnybų įrankius, norint perkelti atskirą personalo aplinką. 

Klientai, kurie planuoja perkėlimą, gali turėti tokias lūkesčius:

- Prieš perkeliant gamybos aplinką, visi klientai turės perkelti sandbox aplinką. 
- Perkėlimo įrankinis įrankis leidžia perkelti tik sandbox-to-sandbox ir perkėlimą nuo gamybos iki gamybos. Todėl jūsų aplinkos tipas nustatys, kokia aplinka gali būti tinkamai perkelta. 
- Klientai gali perkelti tiek sanddėčių, kiek reikia, prieš perkeldami savo gamybos aplinką, jei yra paskirties sandų dėžės atminties langelis. Klientai taip pat gali panaikinti perkeltą sandų dėžę ir permigti kelis kartus. 
- Jei sandų dėžės perkėlimas nepavyksta arba jei norite pradėti iš naujo, galite panaikinti finansų ir operacijų infrastruktūros aplinką ir permigti tą pačią aplinką.
- Perkėlimo metu jūsų personalo aplinkos URL bus skirtingas.
- Planuoti atitinkamą gamybos aplinkos perkėlimo prasto laiką. Numatomas automatinio perkėlimo proceso užbaigimo laikotarpis yra nuo trijų iki keturių valandų. Atsižvelgiant į jūsų organizacijos duomenis, laiko tarpas skirsis. Turite patikrinti, kiek laiko reikia norint perkelti sandbox aplinkas ir leisti atlikti visas papildomas neautomat užduotis.

> [!IMPORTANT] 
> Kai gamybos aplinka sėkmingai perkelta į finansų ir operacijų infrastruktūrą, šaltinio atskira gamybos aplinka automatiškai panaikinama. Turėtumėte panaikinti perkeltos gamybos aplinkos. 

Perkėlimo procesas dažniausiai yra automatinis. Tačiau jūsų verslo vartotojai po perkėlimo turės atlikti kelis neautomatinius veiksmus ir tikrinimą.

Būtina atlikti šiuos neautomatinius veiksmus:

- Sukurkite naują perkėlimo ciklo tarnybų projektą.
- Peržiūrėkite visus integravimą senoje aplinkoje į naują aplinką, remdami integravimą į naujus URL / galinius punktus, remdamasis kiekviena integravimo konfigūracija.
- Atnaujinti įdėtųjų ataskaitų duomenų saugyklą Power BI.
- Atnaujinkite duomenų objektų sąrašą iš DMF darbo srities.
- Žinyno saitas į ciklo tarnybas.
- Kurkite finansinius kalendorius.

Automatinio proceso metu šie veiksmai yra baigti ir turi būti patikrinti:

- Duomenų:

    - Konfigūracijos
    - Saugos vaidmenys (įskaitant pasirinktinius vaidmenis)
    - Darbo eigos
    - Personalizavimas ir įrašyti rodiniai
    - Operacijos
    - Pasirinktiniai laukai
    - Priedai

- Duomenų valdymas – suvesti savo duomenų bazę (BYOD).
- Priemonių valdymas – įgalintos / išjungtos funkcijos.
- Embedded Power Apps.
- Power Platform prijungto administratoriaus centro aplinka (tik gamyba).
- Paketinės užduotys.
- Sukuriama tuščia kiekvieno juridinio subjekto DK. Nustatytas numatytasis kiekvienos DK valiutos kurso tipas ir apskaitos valiuta.
- Naujas sąskaitų planas sukuriamas automatiškai ir susiejamas su kiekvieno juridinio **subjekto** DK puslapiu. Finansinės dimensijos, sukonfigūruotos jūsų personalo aplinkoje, bus automatiškai pridėtos prie naujos sąskaitos struktūros ir susietos su DK. 

> [!NOTE]
> Finansų ir operacijų infrastruktūrai kaip "Dynamics 365" finansų produkto dalis būtina DK. Atskiraje programoje buvusio pasirinktinio Dynamics 365 Human Resources dimensijos valdiklio nėra. Sulieta personalo infrastruktūra priklauso nuo finansų logikos, kad būtų galima rodyti finansines dimensijas personalo **modulyje**. Norėdami daugiau sužinoti apie sąskaitų planą ir finansines dimensijas, žiūrėkite [čia](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Aplinkybės

- Perkėlimas į aplinkas visada bus naujausia bendrai pasiekiama (GA) versija. Atsižvelgiant į jūsų perkėlimą ir bandymų planą, jei jūsų perkėlimo patikrinimas dėl sandų dėžės aplinkos buvo kitoje versijoje, rekomenduojame patvirtinti sandų dėžės perkėlimą toje pačioje versijoje kaip ir jūsų gamybos aplinkoje. 
- Perkeliant perkeltos aplinkos bus perkeltos tame pačiame regione kaip šaltinio atskira personalo aplinka.

## <a name="licensing"></a>Licencijavimas

Šiose srityse licencijavimo pakeitimų Dynamics 365 Human Resources nėra: 

- **Minimalus licencijos pirkimo reikalavimas**
- **Gamybos ir sandbox aplinkos licencijos – jei turite atskiras personalo licencijas**, kurios suteikia vieną gamybos aplinką ir vieną sandbox aplinką, finansų ir operacijų infrastruktūrai be papildomų išlaidų galima naudoti tą patį licencijų skaičių.
- **Papildomos sandbox licencijos – jei įsigijote papildomų sandbox licencijų atskirai personalo programai, tas pats sandbox licencijų skaičius yra galimas** standartiniam priėmimo bandymui (sandbox) aplinkai finansų ir operacijų infrastruktūrai be papildomų išlaidų. 
