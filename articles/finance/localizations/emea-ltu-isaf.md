---
title: Lietuvos i.SAF ataskaitos
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir dirbti su Lietuvos juridinių subjektų i.VZ ataskaita.
author: AdamTrukawka
ms.date: 03/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Lithuania
ms.author: atrukawk
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 266884
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
ms.openlocfilehash: 2c7d74e9a7d5d1630510125300c7bf6b71a2e6f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292261"
---
# <a name="isaf-reporting-for-lithuania"></a>Lietuvos i.SAF ataskaitos

[!include [banner](../includes/banner.md)]

Pagal Valstybinės mokesčių inspekcijos prie Lietuvos Respublikos finansų ministerijos viršininko 2004 m. balandžio 21 d. įsakymą Nr. VA-55 „Dėl Pridėtinės vertės mokesčio sąskaitų faktūrų registrų tvarkymo“, pridėtinės vertės mokesčio sąskaitų faktūrų registrų duomenų apdorojimas ir pateikimas atnaujinami, kad būtų sudarytos sąlygos apmokestinamiems asmenims pateikti informaciją apie pateiktas ir priimtas sąskaitas faktūras mokesčių institucijai, naudojant standartinį i.SAF programos formatą. i.SAF formatas turi atitikti dabartinio apskaitos duomenų failų standarto technines specifikacijas ir techninius reikalavimus (FileVersion iSAF1.2).

## <a name="overview"></a>Apžvalga

Šiame straipsnyje aprašoma, kaip nustatyti elektroninių ataskaitų (ER) konfigūracijas i.YRA ataskaitai ir kaip nustatyti ir naudoti elektroninių pranešimų (EM) funkcijas "Dynamics 365 Finance".

Šiame straipsnyje pateikiama informacija apie:

- Programai būdingų parametrų ir ER konfigūracijų importavimas ir nustatymas
- EM funkcijos nustatymas
- Naudokite EM funkciją i.SAF ataskaitai parengti.

## <a name="import-and-set-up-electronic-reporting-configurations"></a>Elektroninių ataskaitų konfigūracijų importavimas ir nustatymas

Norėdami paruošti programą „Finance“ i.SAF ataskaitų pateikimui, turite importuoti toliau pateikiamas ER konfigūracijas.

| Konfigūracijos pavadinimas    | Konfigūracijos tipas |
|---------------------|--------------------|
| Sąskaitų faktūrų ryšių modelis  | Duomenų modelis |
| i.SAF modelio susiejimas   | Modelio susiejimas |
| i.SAF formatas (LT) |   Formatas  |

Importuokite naujausias šių konfigūracijų versijas. Versijos apraše paprastai yra „Microsoft“ žinių bazės (KB) straipsnio, kuriame paaiškinami konfigūracijos versijoje įgyvendinti pakeitimai, numeris.

> [!NOTE]
> Importavus visas ER konfigūracijas iš ankstesnės lentelės, nustatykite parinktį **Numatytasis modelio susiejimas** į **Taip** ER konfigūracijai **i.SAF modelio susiejimas**.

Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti ER konfigūracijas iš „Microsoft" visuotinės saugyklos, žr. Atsisiųsti [ER konfigūracijas iš visuotinės](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md) saugyklos.

## <a name="standard-vat-codes-and-application-specific-parameters-setup"></a>Standartinių PVM kodų ir programai būdingų parametrų sąranka

1 lentelėje „PVM lentelė“, esančioje **„Standartinio apskaitos duomenų failo techninių specifikacijų lentelės“** (toliau – „Standartiniai PVM kodai“), apibrėžiami toliau pateikiami standartiniai PVM kodai, kuriuos Lietuvos įmonės naudoja pateikdamos i.SAF ataskaitas.

| **Standartinis PVM kodas** | **Aprašas**                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PVM1                  | Prekės ir paslaugos, teikiamos šalies teritorijoje (Lietuvos Respublikos pridėtinės vertės mokesčio įstatymo 19 straipsnio 1 dalis (LPVM))                                                                                                                                                                                                                                 |
| PVM2                  | Prekės ir paslaugos, teikiamos šalies teritorijoje (LPVM 19 straipsnio 3 dalis)                                                                                                                                                                                                                                                                                                     |
| PVM3                  | Prekės ir paslaugos, teikiamos šalies teritorijoje (PVM įstatymo 19 (4) straipsnis)                                                                                                                                                                                                                                                                                                |
| PVM4                  | Atvejai, kai PVM už įsigyjamas prekes ir paslaugas išskaito ir sumoka jų pirkėjas (LPVM 96 straipsnis), nebegalioja nuo 2016-03-31                                                                                                                                                                                                                                                                  |
| PVM25                 | Atvejai, kai PVM už įsigyjamas prekes ir paslaugas išskaito ir sumoka jų pirkėjas (LPVM 96 straipsnis), 21 proc. tarifas                                                                                                                                                                                                                                                                            |
| PVM26                 | Atvejai, kai PVM už įsigyjamas prekes ir paslaugas išskaito ir sumoka jų pirkėjas (LPVM 96 straipsnis), 9 proc. tarifas                                                                                                                                                                                                                                                                             |
| PVM27                 | Atvejai, kai PVM už įsigyjamas prekes ir paslaugas išskaito ir sumoka jų pirkėjas (LPVM 96 straipsnis), 5 proc. tarifas                                                                                                                                                                                                                                                                             |
| PVM5                  | Kai tiekiamos prekės ir teikiamos paslaugos neapmokestinamos PVM (LPVM 20–33 straipsniai ir 112 straipsnis)                                                                                                                                                                                                                                                                                                       |
| PVM51                | Operacijos, kurioms taikomas PVM įstatymo 19(5)(2) ir (3) prašymas (visi atvejai, įskaitant, pavyzdžiui, PVM sumos 5 straipsnį)                                                                                                                                                                                                                                                                                                       |
| PVM52                | Atvejai, kai operacijoms taikoma speciali apmokestinimo schema (marža) (II, III PVM tarifo skyriai)                                                                                                                                                                                                                                                                                                      |
| PVM53                | Atvejai, kai operacijoms taikoma speciali apmokestinimo schema (marža) (II, III PVM tarifo skyriai)                                                                                                                                                                                                                                                                                                      |
| PVM6                  | Kai tiekiamos prekės ir teikiamos paslaugos yra skirtos PVM mokėtojo privatiems poreikiams tenkinti (LPVM 5 ir 6 straipsniai), 21 proc. tarifas                                                                                                                                                                                                                                                                                       |
| PVM7                  | Kai tiekiamos prekės ir teikiamos paslaugos yra skirtos PVM mokėtojo privatiems poreikiams tenkinti (LPVM 5 ir 6 straipsniai), 9 proc. tarifas                                                                                                                                                                                                                                                                                        |
| PVM8                  | Kai tiekiamos prekės ir teikiamos paslaugos yra skirtos PVM mokėtojo privatiems poreikiams tenkinti (LPVM 5 ir 6 straipsniai), 5 proc. tarifas                                                                                                                                                                                                                                                                                        |
| PVM28                 | Kai tiekiamos prekės ir teikiamos paslaugos yra skirtos PVM mokėtojo privatiems poreikiams tenkinti (LPVM 5 ir 6 straipsniai), 0 proc. tarifas                                                                                                                                                                                                                                                                                        |
| PVM29                 | Kai tiekiamos prekės ir teikiamos paslaugos yra skirtos PVM mokėtojo privatiems poreikiams tenkinti (LPVM 5 ir 6 straipsniai), – tarifas                                                                                                                                                                                                                                                                                         |
| PVM9                  | Ilgalaikio materialiojo turto pasigaminimas, vykdomas PVM mokėtojo, ir pastatų (statinių), priklausančių arba nepriklausančių PVM mokėtojui, esminis pagerinimas (LPVM 6 straipsnis), 21 proc. tarifas                                                                                                                                                                                                                |
| PVM30                 | Ilgalaikio materialiojo turto pasigaminimas, vykdomas PVM mokėtojo, ir pastatų (statinių), priklausančių arba nepriklausančių PVM mokėtojui, esminis pagerinimas (LPVM 6 straipsnis), 9 proc. tarifas                                                                                                                                                                                                                 |
| PVM31                 | Ilgalaikio materialiojo turto pasigaminimas, vykdomas PVM mokėtojo, ir pastatų (statinių), priklausančių arba nepriklausančių PVM mokėtojui, esminis pagerinimas (LPVM 6 straipsnis), 5 proc. tarifas                                                                                                                                                                                                                 |
| PVM10                 | Kai operacijos apmokestinamos pagal specialią apmokestinimo schemą (maržą) (LPVM 101–105, 106–110 straipsniai,) negalioja nuo 2016-03-31, 21, 9, 5, 0 proc. tarifas                                                                                                                                                                                                                                    |
| PVM32                 | Kai operacijos apmokestinamos pagal specialią apmokestinimo schemą (maržą) (LPVM II, III skirsniai), 21 proc.                                                                                                                                                                                                                                                                 |
| PVM33                 | Specialios apmokestinimo schemos (maržos) taikymas operacijoms (LPVM II, III skirsniai), 0 proc.                                                                                                                                                                                                                                                                                    |
| PVM12                 | Prekių eksportas (LPVM 41 straipsnis), 0 proc. tarifas                                                                                                                                                                                                                                                                                                                                                   |
| PVM13                 | Prekės tiekiamos ES PVM mokėtojams (LPVM 49 straipsnio 1, 4 dalys), 0 proc. tarifas                                                                                                                                                                                                                                                                                                                       |
| PVM14                 | Kitų operacijų (LPVM 42, 43, 44, 45, 46, 47, 48 straipsniai, 49 straipsnio 2 ir 3 dalys, 51, 52 straipsniai, 53 straipsnio 1, 5, 6 ir 10 dalys) tarifas 0 %                                                                                                                                                                                                                                                                      |
| PVM15                 | Prekės ir paslaugos teikiamos už Lietuvos ribų. Jeigu PVM neapmokestinama, nes laikoma, kad prekės ir paslaugos teikiamos už Lietuvos ribų ir todėl joms netaikomas PVM Lietuvoje, tačiau PVM gali būti atskaitomas pagal LPVM tarifo 58 straipsnio 1 dalies 2 punkto nuostatas.                                                                            |
| PVM34                 | Prekės ir paslaugos teikiamos už Lietuvos ribų. Jeigu PVM neapmokestinama, nes laikoma, kad prekės ir paslaugos teikiamos už Lietuvos ribų, ir PVM negali būti atskaitomas pagal LPVM tarifo 58 straipsnio nuostatas.                                                                                                                       |
| PVM16                 | Jei laikoma, kad prekių buvo įsigyta iš kitų valstybių narių šalies teritorijoje (LPVM 41 ir 122 straipsniai), 21 proc. tarifas                                                                                                                                                                                                                         |
| PVM17                 | Jei laikoma, kad prekių buvo įsigyta iš kitų valstybių narių šalies teritorijoje (LPVM 41 ir 122 straipsniai), 9 proc. tarifas                                                                                                                                                                                                                          |
| PVM18                 | Jei laikoma, kad prekių buvo įsigyta iš kitų valstybių narių šalies teritorijoje (LPVM 41 ir 122 straipsniai), 5 proc. tarifas                                                                                                                                                                                                                          |
| PVM35                 | Jei laikoma, kad prekių buvo įsigyta iš kitų valstybių narių šalies teritorijoje (LPVM 41 ir 122 straipsniai), 0 proc. tarifas                                                                                                                                                                                                                          |
| PVM36                 | Jei laikoma, kad prekių buvo įsigyta iš kitų valstybių narių šalies teritorijoje (LPVM 41 ir 122 straipsniai)                                                                                                                                                                                                                            |
| PVM19                 | Kai prekės, kurias įsigijo Lietuvos Respublikos PVM mokėtojas, kuris yra tarpininkas (antroji šalis) trikampėje prekyboje, buvo tiesiogiai eksportuotos iš vienos valstybės narės į kitą valstybę narę ir buvo tiekiamos minėtos kitos valstybės narės PVM mokėtojui (LPVM 122 straipsnio 3 dalis)                                                                                                          |
| PVM20                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), 21 proc. tarifas                                                                                                                                                                                                                                     |
| PVM37                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), 5 proc. tarifas                                                                                                                                                                                                                                      |
| PVM38                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM pirkėjas neapskaičiuoja (LPVM 95 straipsnio 1 dalies 3 punktas), 0 proc. tarifas                                                                                                                                                                                                                               |
| PVM39                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM pirkėjas neapskaičiuoja (LPVM 95 straipsnio 1 dalies 2 punktas)                                                                                                                                                                                                                                 |
| PVM21                 | Kai paslaugų įsigyjama iš ES PVM mokėtojų, pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), 21 proc. tarifas                                                                                                                                                                                                                                                                   |
| PVM40                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), 5 proc. tarifas                                                                                                                                                                                                                                      |
| PVM41                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), 0 proc. tarifas                                                                                                                                                                                                                                      |
| PVM42                 | Kai paslaugų įsigyjama iš užsienio šalių (išskyrus ES PVM mokėtojus), o pardavimo PVM apskaičiuoja pirkėjas (LPVM 95 straipsnio 2 dalis), – proc. tarifas                                                                                                                                                                                                                                       |
| PVM22                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), negalioja nuo 2016-03-31, 21, 9 ir 5 proc. tarifas                                                                                                              |
| PVM43                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), 21 proc. tarifas                                                                                                                                      |
| PVM44                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), 9 proc. tarifas                                                                                                                                       |
| PVM45                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), 5 proc. tarifas                                                                                                                                       |
| PVM46                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), 0 proc. tarifas                                                                                                                                       |
| PVM47                 | Kai PVM už užsienio apmokestinamojo asmens, kuris neįsikūręs šalies teritorijoje (išskyrus PVM18, PVM19 atvejus), tiekiamas prekes ir teikiamas paslaugas yra skaičiuojamas ir sumokamas pirkėjo (LPVM 95 straipsnio 3, 4 ir 5 dalys), – tarifas                                                                                                                                        |
| PVM23                 | Apskaičiuotas importo PVM. 21, 9, 5 proc. tarifas                                                                                                                                                                                                                                                                                                                                                               |
| PVM24                 | Importo PVM, kai balansavimą kontroliuoja VMI. 21, 9, 5 proc. tarifas                                                                                                                                                                                                                                                                                                                         |
| PVM48                 | Už Lietuvos ribų įsigytos prekės ir paslaugos (įskaitant užsienio šalies ir prekių, skirtų naudoti šalies viduje, importo PVM taikymą), kai prekių ir paslaugų įsigijimas laikomas įvykusiu ne Lietuvos Respublikoje ir pardavimo PVM netaikomas, nes Lietuvoje įsigijimas neapmokestinamas PVM.  |
| PVM49                 | Kai žemės ūkio produktai ir paslaugos perkami iš ūkininkų, kuriems taikoma kompensacinio PVM tarifo schema, 6 proc. tarifas                                                                                                                                                                                                                                                              |
| PVM51                 | Operacijos, kurioms taikomas PVM įstatymo 19(5)(2) ir (3) prašymas (visi atvejai, įskaitant, pavyzdžiui, PVM sumos 5 straipsnį).                                                                                                                                                                                                                                                                                                      |
| PVM52                 | Atvejai, kai operacijoms taikoma speciali apmokestinimo schema (marža) (II, III PVM tarifo skyrius) 9% tarifas.                                                                                                                                                                                                                                                                                                       |
| PVM53                 | Atvejai, kai operacijoms taikoma speciali apmokestinimo schema (marža) (II, III PVM tarifo skyrius) 5% tarifas.                                                                                                                                                                                                                                                                                                       |
| PVM100                | Kiti atvejai                                                                                                                                                                                                                                                                                                                                                                                        |

Pradedant nuo **52.4** versijos **i.SAF formato (LT)** ER konfigūracijos, į formatą įtraukti programai būdingi parametrai, kai vartotojas turi nurodyti, kokie **PVM kodai** sistemoje atitinka PVM kodų sąrašo „Standartiniai PVM kodai“ vertes.

1. Norėdami nustatyti programai būdingus parametrus, eikite į darbo sritį **Elektroninės ataskaitos**, pasirinkite formatą **i.SAF formatas (LT)**, paskui pasirinkite **Konfigūracijos** > **Programai būdingi parametrai** > **Sąranka**.
2. Veiksmų srities skirtuke **Peržvalgos** pasirinkite **ReportTaxCodesLookup**, kad peržiūrėtumėte naujausią formato versiją.
3. „FastTab“ **Sąlygos** apibrėžkite, kurie **Standartiniai PVM kodai** turi atitikti tam tikrus **Sistemos PVM kodai**.

Pavyzdžiui, jei sistemoje yra du **Sistemos PVM kodai**, PVM1 ir PVM2, kuriuos reikia pateikti viename **Standartiniai PVM kodai, PVM1**, į „FastTab“ **Sąlygos** turite įtraukti toliau pateikiamas eilutes.

| Paieškos rezultatas | Eilutė | Mokesčio kodas |
|---------------|------|----------|
| **PVM1** (vertę reikia parinkti iš anksto sudarytame sąraše) | 1 | **VAT1** (vertę reikia parinkti verčių, kurio įrašai yra lentelėje **PVM kodai**, sąraše) |
| **PVM1** (vertę reikia parinkti iš anksto sudarytame sąraše) | 2 | **VAT2** (vertę reikia parinkti verčių, kurio įrašai yra lentelėje **PVM kodai**, sąraše) |

Stulpelis **Eilutės** naudojamas skaitiklyje, kuris kontroliuoja peržvalgos lauko sąlygų vykdymo tvarką.

4. Įtraukite visas „Standartinių PVM kodų“, kuriuos reikia pateikti juridinio subjekto ataskaitoje, sąlygas. Pagal dokumentaciją „Standartinių PVM kodų“ sąrašą sudaro toliau pateikiami kodai.

| **Paieškos rezultatas** | **Eilutė**              | **Mokesčio kodas**      |
|-------------------|-----------------------|-------------------|
| **PVM100**        | Paskutinis jūsų sąrašo punktas | **\*Užpildytas\*** |

> [!NOTE]
> Svarbu įtraukti „PVM100“, kuris turi rinkti duomenis pagal „kitus atvejus“ kaip paskutinis sąrašo punktas. Vertė **Eilutė** lentelėje turi būti paskutinė. 

Ši sąranka reiškia, kad į visas **PVM kodas** mokesčių operacijas, neturinčias konkrečios sąrankos, nes nėra jai nustatyto konkretaus „Standartinio PVM kodo“, bus atsižvelgiama **PVM100** atveju. Būtina apibrėžti šį peržvalgos rezultato lauką sąlygų sąrašo gale.

Galite lengvai eksportuoti programai būdingų parametrų sąranką iš vienos ataskaitos versijos ir importuoti ją į kitą versiją. Taip pat galite eksportuoti sąranką iš vienos ataskaitos ir importuoti ją į kitą ataskaitą, jei abiejose ataskaitose peržvalgos laukų struktūra yra vienoda.

Baigę nustatyti sąlygas, pakeiskite lauko **Būsena** vertę į **Baigta**, įrašykite keitimus ir uždarykite puslapį.

## <a name="import-a-package-of-data-entities-that-include-a-predefined-electronic-messaging-setup"></a>Duomenų objektų paketo, kuriame yra iš anksto apibrėžta el. pranešimų sąranka, importavimas

Funkcija **El. pranešimai** teikiama siekiant tvarkyti skirtingų dokumentų tipų skirtingus elektroninių ataskaitų procesus. Daugiau informacijos apie funkciją El. pranešimai žr. [El. pranešimai](../general-ledger/electronic-messaging.md).

i.SAF funkcijos El. pranešimai sąrankos procesą sudaro daug veiksmų. Kadangi kai kurių iš anksto nustatytų objektų pavadinimai naudojami ER konfigūracijose, svarbu naudoti iš anksto nustatytų verčių, pristatomų susijusių lentelių duomenų objektų pakete, rinkinį.

> [!NOTE]
> Prieš importuodami sąrankos duomenis iš duomenų objektų paketo, užbaikite ir įsitikinkite, kad jūsų programos duomenų objektai atnaujinami ir sinchronizuojami.

1. Programoje [LCS](https://lcs.dynamics.com/v2) eikite į bendrai naudojamo turto biblioteką ir pasirinkite turto tipą **Duomenų paketas**. 
2. Raskite **LT i.SAF sąranka funkcijai El. pranešimai.zip** duomenų paketų failų sąraše ir atsisiųskite jį į kompiuterį.
3. Atsisiuntę failą **LT i.SAF sąranka funkcijai El. pranešimai.zip**, atidarykite „Finance“, pasirinkite įmonę, su kuria bendradarbiausite, palaikydami ryšį su HMRC, paskui eikite į **Darbo sritys** \> **Duomenų valdymas**.
4. Darbo srityje **Duomenų valdymas** eikite **Sistemos parametrai**\>**Objekto parametrai**, tada pasirinkite **Atnaujinti objektų sąrašą**. Palaukite, kol bus patvirtinta, kad atnaujinimas baigtas. Norėdami gauti daugiau informacijos apie tai, kaip atnaujinti objektų sąrašą, žr. [Objektų sąrašo atnaujinimas](../../fin-ops-core/dev-itpro/data-entities/data-entities.md#entity-list-refresh).
5. Patikrinkite, ar tinkamai susieti šaltinio duomenys ir paskirties duomenys. Daugiau informacijos ieškokite temos [Duomenų importavimo ir eksportavimo užduotys](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md#validate-that-the-source-data-and-target-data-are-mapped-correctly) skyriuje apie tikrinimą.
6. Prieš naudojant duomenų objektus pirmą kartą duomenims iš paketo importuoti, sinchronizuokite šaltinio duomenų ir paskirties duomenų susiejimą. Paketo sąraše pasirinkite duomenų objektą, tada veiksmų srityje pasirinkite **Modifikuoti paskirties vietos susiejimą**. 
7. Virš paketo tinklelio pasirinkite **Generuoti susiejimą**, kad sukurtumėte susiejimą iš naujo, tada įrašykite susiejimą.
8. Prieš pradėdami importuoti, pakartokite 6 ir 7 veiksmus kiekvieno pakete esančio duomenų objekto atžvilgiu.

Daugiau informacijos apie duomenų valdymą žr. [Duomenų valdymas](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md). 

9. Dabar turite importuoti duomenis iš failo **LT i.SAF sąranka funkcijai El. pranešimai.zip** į pasirinktą įmonę. Darbo srityje **Duomenų valdymas** pasirinkite **Importuoti** ir lauke **Šaltinio duomenų formatas** nustatykite **Paketas**. 
10. Pasirinkite **Nusiųsti ir įtraukti**, kompiuteryje pasirinkite failą **LT i.SAF sąranka funkcijai El. pranešimai.zip** ir nusiųskite jį.

![Duomenų objektų paketo importavimas.](media/isaf-data-management.jpg)

Gausite pranešimą srityje **Pranešimai** arba galite rankiniu būdu atnaujinti puslapį, kad pamatytumėte duomenų importavimo eigą. Pasibaigus importavimo procesui, matysite rezultatus puslapyje **Vykdymo suvestinė**.

Pakete **LT i.SAF sąranka funkcijai El. pranešimai.zip** pateikiama **„i.SAF“** apdorojimo sąranka, kurioje palaikomas i.SAF ataskaitų pateikimo procesas, bendrai susidedantis iš toliau pateikiamų trijų elementų.

- **Automatiškai užpildyti sąskaitas faktūras** – sąskaitos faktūros įtraukiamos į lentelę **Pranešimo elementai**.
- **Atributų įvertinimas** – lauko **Dokumento tipas** vertės įvertinamos visose sąskaitose faktūrose, įtrauktose į lentelę **Pranešimo elementai**.
- **Generuoti pranešimą** – bus sukurtas **Elektroninis pranešimas**, o susiję **Pranešimo elementai** pagal būseną ir kriterijų sąranką bus susieti su sugeneruotu **Elektroninis pranešimas**. i.SAF ataskaita bus sugeneruota ir įtraukta į **Elektroninis pranešimas**.

## <a name="set-up-data-sources-to-collect-documents-to-be-reported"></a>Duomenų šaltinių sąranka siekiant surinkti į ataskaitą įtrauktinus dokumentus

Naudojant **i.SAF** apdorojimą, galima rinkti sąskaitas faktūras, apie kurias bus pateikta ataskaita juridiniam subjektui. Tada galite sugeneruoti i.SAF ataskaitą. Sąskaitų faktūrų rinkinys įgyvendinamas naudojant veiksmą **Automatiškai užpildyti sąskaitas faktūras**, kurio tipas yra **Automatiškai įvesti įrašą**. Norėdami tinkamai surinkti sąskaitas faktūras, turite nurodyti veiksmo **Automatiškai užpildyti sąskaitas faktūras** laikotarpį.

1. Eikite į **Mokesčiai** > **Sąranka** > **El. pranešimai** > **Automatinio įrašų įvedimo veiksmai** ir pasirinkite **Automatiškai užpildyti sąskaitas faktūras**. 

Naudojant **„i.SAF“** apdorojimą, numatytųjų duomenų šaltinių nustatymuose yra toliau pateikiami trys duomenų šaltiniai.

 - **VendInvoiceJour:** eikite į **Mokėtinos sumos** \> **Užklausos ir ataskaitos** \> **Sąskaita faktūra** \> **SF žurnalas**.
 - **CustInvoiceJour:** eikite į **Gautinos sumos** \> **Užklausos ir ataskaitos** \> **Sąskaita faktūra** \> **SF žurnalas**.
 - **ProjInvoiceJour:** eikite į **Projektų valdymas ir apskaita** \> **Projekto SF** \> **Projekto SF**

Pagal numatytuosius nustatymus visi šių duomenų šaltinių įrašai bus įvesti į lentelę **Pranešimo elementai**, kai pasirenkate **Automatiškai įvesti įrašus**.

2. „FastTab“ **Duomenų šaltinių nustatymas** pasirinkite įrašą **Tiekėjo SF žurnalas** ir pasirinkite **Redaguoti užklausą**. 
3. Lauke **Data** lentelėje **Tiekėjo SF žurnalas** nurodykite laikotarpį, kurio pasirinkto juridinio subjekto tiekėjo SF turi būti įtraukiamos į ataskaitas i.SAF formatu. Čia galite nurodyti kitus atrankos kriterijus, atitinkančius konkrečius jūsų įmonės reikalavimus, taikomus i.SAF ataskaitai. 
4. Atlikite tuos pačius kitų ataskaitos duomenų šaltinių (Pardavimo SF žurnalo, Projekto SF žurnalo) sąrankos veiksmus arba panaikinkite nereikalingus duomenų šaltinius iš sąrašo.

![SF duomenų šaltinių automatinis įvedimas.](media/isaf-populate-records.jpg)

## <a name="set-up-electronic-messaging-parameters-for-isaf"></a>i.SAF funkcijos El. pranešimai parametrų sąranka

Importavę duomenų objektus į duomenų bazę, atlikite nurodytus veiksmus ir funkcija El. pranešimai bus parengta naudoti.

1. Eikite į **Mokesčiai**\>**Sąranka**\>**El. pranešimai**\>**Vykdomosios klasės parametrai**, pasirinkite vykdomąjį klasę **EvaluateInvoiceType_LT** ir veiksmų srityje pasirinkite **Parametrai**. 
2. Lauke **SF tipas** pasirinkite **InvoiceType**, paskui spustelėkite **Gerai**.
3. Eikite į **Mokesčiai** \> **Sąranka** \> **El. pranešimai** \> **Pranešimų apdorojimo veiksmai** ir nustatykite toliau pateikiamų veiksmų susijusias GER konfigūracijas lauke **Formato susiejimas**.

| **Pranešimų apdorojimo veiksmų pavadinimas** | **GER konfigūracija** |
|-------------------------------------|-----------------------|
| Pranešimo generavimas                     | i.SAF formatas (LT)     |

4. Eikite į **Didžioji knyga** \> **Sąranka** \> **Parametrai**, kad nustatytumėte parinktį **Numeracijos**.

| **Numeracijų nuoroda** | **Numeracijų aprašas**                                                                                                                                                                                                                         |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Laiškas                        | Unikalus pranešimo raktas. Nustatykite šios Nuorodos netęstinę numeraciją. Ši numeracija bus naudojama numeruojant generuojamus pranešimus. |
| Pranešimo prekė                   | Unikalus pranešimo prekės raktas. Nustatykite šios Nuorodos netęstinę numeraciją. Ši numeracija bus naudojama numeruojant pranešimų prekes, generuojamas pagal šaltinio lentelės. |

## <a name="set-up-security-roles-for-electronic-message-processing"></a>Elektroninių pranešimų apdorojimo saugos vaidmenų nustatymas

Skirtingoms vartotojų grupėms gali reikėti prieigos prie **i.VZ., apdorojimo**. Galite riboti prieigą prie apdorojimo, atsižvelgiant į sistemoje nustatytas saugos grupes.

Atlikite toliau nurodytus veiksmus, norėdami apriboti prieigą prie **i.SAF** apdorojimo.

1. Eikite į **Mokesčiai** \> **Sąranka** \> **El. pranešimai** \> **El. pranešimų apdorojimas**. 
2. Pasirinkite **i.SAF** apdorojimą ir įtraukite saugos grupes, kurios turi dirbti su šiuo apdorojimu. Jei apdorojime saugos grupių nenurodyta, tik sistemos administratorius gali matyti apdorojimą puslapyje **El. pranešimai**.

## <a name="set-up-the-vat-registration-number-for-the-company-that-is-reporting-isaf"></a>Nustatyti pvm registracijos numerį įmonei, kuri teikia ataskaitas I.VZ.

Sistema iš juridinio subjekto ypatybėse nustatyto registracijos ID nuskaito įmonės, kuri teikia ataskaitas I.INKITĖS, PVM registracijos numerį. Daugiau informacijos ieškokite Registracijos [tipas ir](emea-registration-ids.md#registration-type-creation)[Registracijos kategorija](emea-registration-ids.md#supported-registration-categories). Mokesčio registracijos tipas turi būti priskirtas **PVM ID registracijos** kategorijai. Išsamesnės informacijos apie būtinas PVM ID registracijos sąlygas ieškokite Nustatyti [PVM ID](tasks/eur-00015-vat-id.md).

## <a name="collect-data-for-the-isaf-report"></a>i.SAF ataskaitos duomenų rinkimas

**„i.SAF“** apdorojimo sąranka, pateikiama naudojant duomenų objektų paketą, parodyta toliau pateikiamoje schemoje.

![i.SAF elektroninių pranešimų procesas.](media/isaf-processing.jpg)

Žali schemos langeliai rodo bendrą i.SAF ataskaitų generavimo procesą.

1. Eikite į **Mokesčiai** > **Užklausos ir ataskaitos** > **El. pranešimai** > **El. pranešimų prekės** ir veiksmų srityje pasirinkite **Vykdyti apdorojimą**. 
2. Lauke **Apdorojimas** pasirinkite **i.SAF**. 
3. Norėdami pradėti rinkti duomenis, skirtus i.SAF ataskaitai, pažymėkite žymės langelį **Pasirinkti veiksmą** ir pasirinkite **„Automatiškai užpildyti SF“**. Jei nepažymėsite žymės langelio **Pasirinkti veiksmą**, pasirinkus **„Automatiškai užpildyti SF“**, veiksmas bus vykdomas automatiškai kaip pirmas pasirinkto apdorojimo veiksmas. Pasirinkus **„Automatiškai užpildyti SF**, visos SF iš duomenų šaltinių, apibrėžtų procedūroje *Duomenų šaltinių sąranka siekiant surinkti į ataskaitą įtrauktinus dokumentus*, bus generuojamos lentelėje **Pranešimo prekės** pagal šiems duomenų šaltiniams nustatytus kriterijus. Visų SF **Pranešimo prekės tipas** bus tas pats: „Sąskaita faktūra“.
4. Pasirinkę **Originalus dokumentas** veiksmų srityje, peržiūrėsite pasirinktos **Pranešimo prekė** originalų dokumentą.

## <a name="define-invoice-types-for-isaf-reporting"></a>i.SAF ataskaitų SF tipų nustatymas

Kai SF sėkmingai užpildomos iš duomenų šaltinių lentelėje **Pranešimo prekės**, būtina nurodyti kiekvienos SF tipą. **SF tipas** saugomas kiekvienos SF grupėje **Papildomas laukas**. 

1. Norėdami nustatyti SF tipą, veiksmų srityje pasirinkite **Vykdyti apdorojimą**. 
2. Lauke **Apdorojimas** pasirinkite **i.SAF**. 
3. Pažymėkite žymės langelį **Pasirinkti veiksmą** ir pasirinkite **„Atributų įvertinimas“**, kad pradėtumėte apibrėžti SF tipą; nepažymėjus žymės langelio **Pasirinkti veiksmą**, veiksmas **„Atributų įvertinimas“** bus vykdomas automatiškai kaip kitas pasirinkto apdorojimo veiksmas. Atlikus veiksmą **„Atributų įvertinimas“**, visų SF, kurių būsena yra **Automatiškai įvesta**, SF tipas bus apibrėžtas ir rodomas lauke **SF tipas** kiekvienos SF grupėje **Papildomas laukas**.

![i.SAF SF tipo įvertinimas.](media/isaf-invoice-type.jpg)

## <a name="generate-the-isaf-report-in-xml"></a>i.SAF XML ataskaitos generavimas

i.SAF ataskaita turi būti sugeneruota ir pateikta mokesčių inspekcijai XML formatu.

Ataskaitoje i.SAF rodomi šie parametrai:

| **Parametro pavadinimas** | **Aprašas** |
|----------------|-------------|
| **Ataskaitos tipas** | Pasirinkite vieną iš leistinų ataskaitos tipų.<ul><li> - **F**: į ataskaitą bus įtrauktos gaunamos ir išrašomos SF</li><li> - **S**: į ataskaitą bus įtrauktos tik išrašomos SF</li><li> - **P**: į ataskaitą bus įtrauktos tik gaunamos SF </li></ul> |
| **Data Nuo** | Pasirinkite laikotarpio, kurio i.SAF ataskaita turi būti generuojama, pradžios datą. |
| **Data Iki** | Pasirinkite laikotarpio, kurio i.SAF ataskaita turi būti generuojama, pabaigos datą. |
| **Sudengimo laikotarpis** | Pasirinkę **Sudengimo laikotarpis**, nustatykite užregistruotas mokesčių operacijas, kai **Sudengimo laikotarpis** turi būti įtrauktas į ataskaitą. |
| **Dalies numeris** | Įveskite ataskaitos dalies numerį. |
| **Dalių skaičius** | Įveskite dalių skaičių. |

Šiuos parametrus reikia apibrėžti prieš pradedant generuoti i.SAF ataskaitą.

Jei planuojate generuoti i.SAF ataskaitą paketiniu režimu, patikrinkite, ar pažymėtas žymės langelis Naudoti parametrus naudojant **i.SAF elektroninių pranešimų apdorojimo veiksmą** **Generuoti** **pranešimą**.

![Elektroninių pranešimų apdorojimas.](media/isaf-use-parameters.png)

Norėdami nustatyti **i.SAF elektroninio pranešimo apdorojimo veiksmo Generuoti** **pranešimą** parametrus, atlikite šiuos veiksmus:

1. Eikite į **Mokesčiai** \> **Sąranka** \> **El. pranešimai** \> **El. pranešimų apdorojimas**.
2. Pasirinkite **„i.SAF“** elektroninio pranešimo apdorojimą ir **veiksmų** „FastTab" pasirinkite **Generuoti** pranešimą.
3. Patikrinkite, ar žymimas laukelis **Naudoti parametrus** yra pasirinktas.
4. „FastTab“ **Veiksmai** veiksmų juostoje pasirinkite **Parametrai**.
5. Nustatyti i.SAF ataskaitos parametrus, kuriuos sistema naudoja i.SAF generavimo metu. Pranešimo **parametro** laukas yra pasirinktinis.

![Parametrų juosta.](media/isaf-parameters-setup.png)

6.Pasirinkite **Gerai**.

### <a name="generate-the-isaf-report-in-batch-mode"></a>i.SAF ataskaitos generavimas bendru režimu

Norėdami kurti i.SAF ataskaitą bendru režimu, atlikite šiuos žingsnius.

1. Eikite į **Mokesčiai** \> **Užklausos ir ataskaitos** \> **Elektroniniai pranešimai** \> **Pranešimų objektai**. 
2. Puslapyje **Pranešimų objektai** veiksmų juostoje rinkitės **Vykdyti apdorojimą** 
3. Lauke **Apdorojimas** pasirinkite **i.SAF**.
4. Norėdami **įjungti** pokyčio veiksmo parametrą **Veiksmo** laukelyje kurkite i.SAF ataskaitą. 
5. Skirtuke Vykdyti fone „FastTab" nurodykite paketo parametrus ir pasirinkite Gerai, kad **sugeneruotumėte** **i.SAF** ataskaitą.

![Vykdyti apdorojimo slankiklį.](media/isaf-run-processing.png)

  Dėl veiksmo Generuoti pranešimą kiekvienai elektroninio pranešimo prekei, kurios būsena yra Įvertinta ir atitinka nurodytus ataskaitos parametrus, bus **sukurtas** **elektroninis** pranešimas, **kuris bus rodomas pranešimo stulpelyje kiekvienos SF** atžvilgiu. Į ataskaitą įtrauktų pranešimo prekių **Būsena** bus pakeista į **Pranešta**.
6. Norėdami peržiūrėti failą, pasirinkite el. pranešimo prekę, tada viršutiniame dešiniajame puslapio kampe pasirinkite **Priedai** (sąvaržėlės piktograma). 
7. Pasirinkto pranešimo puslapyje **Priedai** pasirinkite paskutinį priedą, tada veiksmų srityje pasirinkite **Atidaryti**.

### <a name="generate-isaf-report-in-non-batch-mode"></a>i.SAF ataskaitos generavimas ne bendru režimu

Norėdami kurti i.SAF ataskaitą ne bendru režimu, atlikite šiuos žingsnius.

1. Norėdami sugeneruoti i.SAF ataskaitą, eikite į **Mokesčiai** \> **Užklausos ir ataskaitos** \> **Pranešimų objektai** \> **Pranešimo prekės** ir veiksmų srityje pasirinkite **Generuoti ataskaitą**. 
2. Pasirinkite **„i.SAF“** lauke **Apdorojimas**, paskui pasirinkite **„Generuoti pranešimą“** lauke **Veiksmas**, kad sugeneruotumėte i.SAF ataskaitą. 
3. Elektroninės **ataskaitos parametrų** dialogo puslapyje galite koreguoti parametrus, kurie nurodyti veiksmui Generuoti pranešimą prieš ir pradėti ataskaitos **generavimą**. Ataskaita bus kuriama ne bendru režimu. Jei norite sugeneruoti paketo i.SAF ataskaitą, atlikite ankstesnę procedūrą, aprašantį, kaip generuoti i.SAF ataskaitą pakete.
4. Dėl veiksmo Generuoti pranešimą visiems EM objektams, kurios būsena yra Įvertinta ir atitinka nurodytus ataskaitos parametrus, bus **sukurtas** **elektroninis** pranešimas, **kuris bus rodomas pranešimo stulpelyje kiekvienos SF** atžvilgiu. Į ataskaitą įtrauktų pranešimo prekių **Būsena** bus pakeista į **Pranešta**.
5. Norėdami peržiūrėti failą, pasirinkite el. pranešimo prekę, tada viršutiniame dešiniajame puslapio kampe pasirinkite **Priedai** (sąvaržėlės piktograma). 
6. Pasirinkto pranešimo puslapyje **Priedai** pasirinkite paskutinį priedą, tada veiksmų srityje pasirinkite **Atidaryti**.

## <a name="regenerate-the-isaf-report"></a>i.SAF ataskaitos generavimas iš naujo 

Jei reikia iš naujo sugeneruoti tam tikrą prekių i.SAF ataskaitą, veiksmų srityje pasirinkite **Atnaujinti būseną**, kad pakeistumėte pranešimo prekių būseną į pradinę būseną. Dialogo puslapyje **Atnaujinti būseną** pasirinkite **i.SAF** apdorojimą, paskui pasirinkite **Atnaujinti į pradinę būseną**. Norėdami atkurti pradinę SF būseną, pasirinkite vieną iš leistinų verčių: **Automatiškai įvesta** arba **Įvertinta**.

## <a name="exclude-or-postpone-invoice-reporting-in-isaf"></a>SF ataskaitos pateikimo naudojant i.SAF neįtraukimas arba atidėjimas

Jei norite neįtraukti SF į i.SAF ataskaitą, veiksmų srityje pasirinkite **Atnaujinti būseną**, kad pranešimų prekių būsena būtų pakeista į **Neįtraukta**. SF, kurių būsena yra **Neįtraukta**, į ataskaitą įtrauktos nebus. Dialogo puslapyje **Atnaujinti būseną** pasirinkite **„i.SAF“** apdorojimą, pasirinkite **Neįtraukti pranešimo prekės** lauke **Veiksmas**, tada pasirinkite **Neįtraukta** lauke **Nauja būsena**. Galite nustatyti papildomų kriterijų, naudodami funkciją **Filtras**, ir nurodyti SF, kurios nereikia įtraukti į tolesnį apdorojimą.

![i.SAF Pranešimo prekės neįtraukimas į apdorojimą.](media/isaf-exclude-message-item.jpg)

Jei norite atidėti SF įtraukimą į i.SAF ataskaitą, veiksmų srityje pasirinkite **Atnaujinti būseną**, kad pranešimų prekių būsena būtų pakeista į **Atidėta**. SF, kurių būsena yra **Atidėta**, į ataskaitą įtrauktos nebus. Dialogo puslapyje **Atnaujinti būseną** pasirinkite **„i.SAF“** apdorojimą, pasirinkite **Pakeisti į Atidėta** lauke **Veiksmas**, tada pasirinkite **Atidėta** lauke **Nauja būsena**. Galite nustatyti papildomų kriterijų, naudodami funkciją **Filtras**, kad nurodytumėte, kuri (-ios) SF turi būti atidėta (-os) pagal kriterijus.

Galite bet kada pakeisti pranešimų prekių būseną **Neįtraukta** arba **Atidėta**, naudodami veiksmą **Atnaujinti į pradinę būseną**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
