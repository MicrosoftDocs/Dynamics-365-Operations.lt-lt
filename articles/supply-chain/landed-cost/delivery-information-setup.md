---
title: Pristatymo informacijos sąranka
description: Šiame straipsnyje aprašoma, kaip nustatyti pristatymo informaciją pagal įkainojimo modulį.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5bf9c700ecd327ab3b3948f38dc60e24efbda94c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895618"
---
# <a name="delivery-information-setup"></a>Pristatymo informacijos sąranka

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti pristatymo informaciją pagal įkainojimo **modulį**.

## <a name="shipping-ports"></a>Gabenimo uostai

Siuntimo uostai nurodo, iš kur ir į kur siunčiamos prekės. Kiekvienam reisui apibrėžiamas išvykimo ir atvykimo uostas, atsižvelgiant į reiso laivui pasirinktą veiklos ciklą. Siuntimo uostai naudojami veiklos ciklo atkarpoms ir reiso veiklai kurti. Jie paprastai apibrėžiami naudojant miesto ir šalies arba regiojo, kuriame yra faktinis siuntimo uostas, pavadinimą.

Norėdami dirbti su siuntimo uostais, eikite į **Iškrovimo kaina \> Pristatymo informacijos nustatymas \> Siuntimo uostai**. Čia galite peržiūrėti, įtraukti ir pašalinti jūsų siuntimo uostų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Siuntimo uostas | Įveskite unikalų siuntimo uosto identifikavimo pavadinimą / numerį. |
| aprašymas | Įvesti siuntimo uosto aprašymą. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Sekimo valdymo centras

Sekimo kontrolės centras naudojamas gamybos laikui, būsenos atnaujinimui ir informacijos srautui, susijusiam su reisu, nustatyti, kai siuntimo konteineriai perkeliami iš vienos atkarpos į kitą. Kai sukuriate sekimo kontrolės įrašą, jis siejamas su konkrečia reiso veiklos ciklo atkarpa. Kai reisas atnaujina atkarpą, susietas įrašas atnaujinamas ir užpildomas kaip nurodyta. Atskirų reisų sekimo informaciją galima atnaujinti puslapyje **Visi reisai**.

Norėdami atidaryti sekimo kontrolės centrą, eikite į **Iškrovimo kaina \> Pristatymo informacijos nustatymas \> Sekimo kontrolės centras**.

Sekimo kontrolės centre rodomas vienas iš trijų puslapių rodinių, priklausomai nuo laukelyje **Kurti tipą** pasirinktos vertės sąrašo srityje: *Tuščias*, *Vykdymo laikas* arba *Būsenos atnaujinimas*. Kiekvienas kūrimo tipas atnaujina skirtingą informacijos rinkinį, susietą su reiso eiga nuo pradžios taško iki galutinės paskirties vietos.

### <a name="common-rule-settings"></a>Bendrieji taisyklių nustatymai

Toliau pateikiamoje lentelėje rodomi laukeliai, kuriuos galima naudoti visiems trims kūrimo tipams sekimo kontrolės centre.

| Laukas | aprašymas |
|---|---|
| Šaltinio lentelė, šaltinio laukas | Šie laukeliai identifikuoja šaltinio lentelę ir duomenų bazės laukelį. Taisyklė įkels vertę laukelyje, o tada ją naudos taip, kaip nurodo kiti taisyklės parametrai. |
| Paskirties lentelė, laukas laukelis | Šie laukeliai identifikuoja paskirties lentelę ir duomenų bazės laukelį. Taisyklė įkels vertę laukelyje, o tada ją naudos (ar užrašys) taip, kaip nurodo kiti taisyklės parametrai. |
| Veikla | Šiame laukelyje nustatomas veiklos, kuri turi būti taikoma siuntimo konteineriui, kuris atitinka taisyklę, tipas. |
| Atitikimo kriterijai | Šiame laukelyje apibrėžiama, kaip sistema identifikuoja taisyklės gretinimo pavadinimą. Kiekvienu atveju sistema peržiūri šaltinio ir paskirties lentelių duomenis, kad nustatytų, ar ir kada laukelį reikia atnaujinti paskirties lentelėje.<p>Pavyzdžiui, šaltinio lentelė yra *Reisai*, o paskirties lentelė yra *Pirkimo antraštė* arba *Pirkimo eilutės*. Lentelėje *Reisai* nurodoma vertė **Išvykimo uostas**, skirta *Honkongui*, o lentelėje *Pirkimo antraštė* nurodyto **Išvykimo uosto** vertė yra *Šanchajus*. Tada sukuriama taisyklė, kurioje išvykimo uostas nurodytas *Honkongas*. Šiuo atveju laukelio **Atitikimo kriterijai** vertės veiks taip:</p><ul><li>**Abu** – paskirties laukelis neatnaujinamas, nes vienas iš dviejų uostų nesutampa.</li><li>**Šaltinis** – tikslinis laukelis atnaujinamas, nes šaltinio lentelės išvykimo uostas yra *Honkongas*.</li><li>**Tikslas** – tikslinis laukelis neatnaujinamas, nes paskirties lentelės išvykimo uostas yra *Šanchajus* (ne *Honkongas*).</li></ul> |
| Kopijuoti veiksmą | Galimos vertės yra *Kopijuoti* ir *Numatytoji*. Pasirinkite *Kopijuoti*, jei šaltinio laukelyje esančią vertę norite nukopijuoti į paskirties laukelį. Pasirinkite *Numatytoji*, kad paskirties laukeliui nustatytumėte statinę vertę. |
| Numatyta | Kai laukelis **Kopijuoti veiksmą** nustatytas kaip *Numatytasis*, laukelis **Numatytasis** apibrėžia paskirties laukelio numatytąją vertę. Pavyzdžiui, jei veiksmas yra susijęs su uosto naujinimu, o laukelis **Kopijuoti veiksmą** nustatytas kaip *Numatytasis*, laukelis **Numatytasis** nurodo uostą. |
| Atkarpa | Šis laukelis identifikuoja veiklos ciklo, kuriam įvyksta nurodytas veiksmas, atkarpą, pvz., krovimas arba muitinė. |
| Paslaugos teikėjas | Jei dabartiniam veiklos ciklo būsenos atnaujinimui / atkarpai naudojamas konkretus paslaugų teikėjas, šiame laukelyje rodomas paslaugų teikėjas. Paslaugų teikėjai nustatomi tiekėjo paskyroje. |

### <a name="lead-time-rules"></a>Vykdymo laiko taisyklės

Vykdymo laikas – tai numatomas laikas, per kurį reisui reikės užbaigti nustatytą reiso veiklos ciklo atkarpą. Kiekvienos veiklos ciklo atkarpos vykdymo laikas naudojamas apskaičiuoti numatomą reiso pristatymo datą. Tada data įvedama į kiekvieno laukelio **Patvirtinta pristatymo data** kiekvienoje reiso pirkimo eilutėje.

Vykdymo laiko taisyklės naudojamos datų atnaujinimams valdyti. Veiklos generuojamos automatiškai, kai reisui naudojamas veiklos ciklo šablonas.

Norėdami sekimo kontrolės centre pridėti vykdymo laiko taisyklę, atlikite nurodytus veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Iškrovimo kaina \> Kelių atkarpų veiklos ciklo nustatymas \> Atkarpos**. Pasirinkite atkarpą, kuriai norite nustatyti vykdymo laikus, o tada veiksmų srityje pasirinkite **Sekimo kontrolės centras**. Sekimo kontrolės centre iš anksto įkeliama informacija apie pasirinktą atkarpą.
    - Eikite į **Iškrovimo kaina \> Pristatymo informacijos nustatymas \> Sekimo kontrolės centras**. Tada reikia rankiniu būdu pasirinkti atkarpą atliekant 4 šios procedūros veiksmą.

1. Sąrašo srityje laukelį **Kurti tipą** nustatykite kaip *Vykdymo laikas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Jei atlikdami 1 veiksmą pradėjote nuo sekimo kontrolės centro, laukelį **Atkarpa** nustatykite į tokią atkarpą, kuriai norite sukurti vykdymo laiko taisyklę. Jei pradėjote nuo puslapio **Atkarpos** laukelis **Atkarpa** nustatomas iš anksto pagal atkarpą, kurią pasirinkote prieš atidarydami sekimo kontrolės centrą.

    Atsižvelgiant į laukelio **Atkarpa** vertę, keli laukeliai nustatomi automatiškai, kaip parodyta čia:

    - **Šaltinio lentelė:** *Konteinerio veiklos*
    - **Šaltinio laukelis** *Pradžios data*
    - **Paskirties lentelė:** *Konteinerio veiklos*
    - **Paskirties laukelis:** *Numatoma pabaigos data*

1. Laukelyje **Veikla** pasirinkite veiklą, kuriai reikėtų taikyti dabartinę taisyklę.
1. Laukelyje **Vykdymo laikas** įveskite vykdymo laiką (dienomis), kurį reikėtų pritaikyti suaktyvinus dabartinę taisyklę.

### <a name="status-update-rules"></a>Būsenos naujinimo taisyklės

Įrašai, kuriuose laukelis **Kurti tipą** nustatytas kaip *Būsenos naujinimas* atnaujina pirkimo užsakymo eilučių būseną arba reiso būseną, siuntimo konteinerį arba registracijos lapo lygį. Būsenas galima nustatyti nepriklausomai. Jas naudokite, kad naudotoją arba skyrių informuotumėte apie reiso etapą (pvz., gautus dokumentus arba tranzito prekes).

Kai laukelis **Kurti tipą** nustatytas kaip *Būsenos naujinimas*, sekimo kontrolės centre yra „FastTab“ skirtukas **Eilutės**, kuriame galima apibrėžti savikainos tipą ir atnaujintą reiso būseną. Pavyzdžiui, yra eilutė, kurioje laukelis **Savikainos sritis** nustatyta kaip *Konteineris*, o laukelis **Reiso būsena** nustatoma kaip *Tranzito prekės*. Šiuo atveju, kai užsakymas užbaigia nurodytą atkarpą, siuntimo konteinerio laukelis **Reiso būsena** atnaujinamas į *Tranzito prekės*.

Būsenos atnaujinimai pateikia reiso būseną reiso eilutėse ir pirkimo užsakymo eilutėse, susijusiose su tuo reisu. Reisui judant savo veiklos ciklu iš uosto, navigacijos ir muitinės į paskirties sandėlį, reiso įrašo laukelyje **Reiso būsena** pateikiama trumpa būsenos, kurioje yra prekės, apžvalga.

Norėdami sekimo kontrolės centre pridėti būsenos naujinimo taisyklę, atlikite nurodytus veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Iškrovimo kaina \> Kelių atkarpų veiklos ciklo nustatymas \> Atkarpos**. Pasirinkite atkarpą, kuriai norite nustatyti būsenos naujinimą, o tada veiksmų srityje pasirinkite **Sekimo kontrolės centras**. Sekimo kontrolės centre iš anksto įkeliama informacija apie pasirinktą atkarpą.
    - Eikite į **Iškrovimo kaina \> Pristatymo informacijos nustatymas \> Sekimo kontrolės centras**. Tada reikia rankiniu būdu pasirinkti atkarpą atliekant 4 šios procedūros veiksmą.

1. Sąrašo srityje laukelį **Kurti tipą** nustatykite kaip *Būsenos naujinimas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Jei atlikdami 1 veiksmą pradėjote nuo sekimo kontrolės centro, laukelį **Atkarpa** nustatykite į tokią atkarpą, kuriai norite sukurti būsenos naujinimo taisyklę. Jei pradėjote nuo puslapio **Atkarpos** laukelis **Atkarpa** nustatomas iš anksto pagal atkarpą, kurią pasirinkote prieš atidarydami sekimo kontrolės centrą.

    Atsižvelgiant į laukelio **Atkarpa** vertę, keli laukeliai nustatomi automatiškai, kaip parodyta čia:

    - **Šaltinio lentelė:** *Konteinerio veiklos*
    - **Šaltinio laukelis:** *Faktinė pabaigos data*
    - **Paskirties lentelė:** šis laukelis paliekamas tuščias.
    - **Paskirties laukelis:** šis laukelis paliekamas tuščias.

1. Laukelyje **Veikla** pasirinkite veiklą, kuriai reikėtų taikyti jūsų taisyklę.
1. „FastTab“ skirtuke **Eilutės** įveskite kiekvienos savikainos srities būsenos naujinimus.

### <a name="blank-type-rules"></a>Tuščio tipo taisyklės

Naudokite įrašus, kurių vertė **Kurti tipą** yra *Tuščia*, kad ją apeitumėte arba įveskite laukelio vertę pagal kito laukelio duomenis. Laukelyje iš iškrovimo kainos duomenys bus užrašomi kitose „Microsoft Dynamics 365 Supply Chain Management“ srityse pagal taisykles, kurios nustatomos sekimo kontrolės centre.

1. Eikite į **Iškrovimo kaina \> Pristatymo informacijos nustatymas \> Sekimo kontrolės centras**.
1. Sąrašo srityje laukelį **Kurti tipą** nustatykite kaip *Tuščias*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Apibrėžkite šaltinio ir paskirties vertes, gretinimo kriterijus, kopijavimo veiksmą ir kitus atitinkamus parametrus, kaip reikalauja jūsų taisyklė.

### <a name="required-tracking-control-setup"></a>Būtinas sekimo kontrolės nustatymas

Kiekvienam veiklos ciklo šablonui sekimo kontrolės centre reikia nustatyti du įrašus. Abiejų šių įrašų vertė **Kurti tipą** yra *Tuščias*, ir jie abu naudojami visuose iškrovimo kainos diegimuose. Jie padeda užtikrinti, kad patvirtinta pirkimo data ir tranzito prekių numatomos datos būtų atnaujintos reisams ir susijusioms pirkimo užsakymo eilutėms.

Pirmasis įrašas reikalingas pirkimo eilutėms atnaujinti. Jame turi būti šie nustatymai:

- **Šaltinio lentelė:** *Konteinerio veiklos*
- **Šaltinio laukelis:** *Numatoma pabaigos data*
- **Paskirties lentelė:** *Pirkimo eilutės*
- **Paskirties laukelis:** *Patvirtinta arba pristatymo data*

Antrasis įrašas reikalingas tranzito prekių operacijoms atnaujinti. Jame turi būti šie nustatymai:

- **Šaltinio lentelė:** *Konteinerio veiklos*
- **Šaltinio laukelis:** *Numatoma pabaigos data*
- **Paskirties lentelė:** *Tranzito prekių užsakymas*
- **Paskirties laukelis:** *Numatoma data*
