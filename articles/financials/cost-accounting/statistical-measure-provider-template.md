---
title: "Statistinių dimensijų nariai ir statistinių priemonių teikimo įrankio šablonai"
description: "Šioje temoje pateikiama informacijos apie statistinių dimensijų narius ir statistinių priemonių teikimo įrankių šablonus. Statistinių dimensijų narius galima naudoti kaip strategijų, pvz., išlaidų paskirstymo ir išlaidų priskyrimo, paskirstymo bazę. Juos taip pat galima naudoti nepiniginių išlaidų naudojimui pranešti."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: baefad4efd51661c236459493b7f02747593bbab
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statistinių dimensijų nariai ir statistinių priemonių teikimo įrankio šablonai

[!include[banner](../includes/banner.md)]

Naudojant statistinę dimensiją ir jos narius, modulyje Kaštų apskaita registruojami ir kontroliuojami nepiniginiai įrašai. Statistinių dimensijų narius galima naudoti dviem tolesniais tikslais.

- Kaip strategijų, pvz., išlaidų paskirstymo ir išlaidų priskyrimo, paskirstymo bazę.
- Nepiniginiam naudojimui pranešti.

## <a name="statistical-dimension"></a>Statistinė dimensija

Statistinė dimensija turi unikalų pavadinimą ir keletą unikalių dimensijos narių. Statistinė dimensija priskiriama kaštų apskaitos didžiosios knygos ID. Šiuo ryšiu visi atitinkami statistinės dimensijos nariai susiejami su kaštų apskaitos didžiąja knyga. Todėl visi statistiniai įrašai bus kuriami kaštų apskaitos didžiosios knygos kontekste.

> [!NOTE]
> Statistinę dimensiją galima priskirti daugiau nei vienai kaštų apskaitos didžiajai knygai.

Čia pateikiamas statistinės dimensijos pavyzdys.

| Vardas                        | Dimensijos narių duomenų jungtis |
|-----------------------------|--------------------------------------|
| Bendrai naudojami statistiniai elementai | Importuoti dimensijos nariai           |

Čia pateikiamas kaštų apskaitos didžiajai knygai priskirtos statistinės dimensijos pavyzdys.

| Vardas                  | Apskaitos valiuta | Valiutos kurso tipas | Finansinis kalendorius | Savikainos elemento dimensija | Statistinė dimensija       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Valdymo apskaita | USD                 | Pastovi valiuta  | Ataskaitinis laikotarpis   | Bendrai naudojami kaštų elementai   | Bendrai naudojami statistiniai elementai |

## <a name="statistical-dimension-members"></a>Statistinės dimensijos nariai

Statistinės dimensijos narys nurodo objektą, kurio nepinigines priemones norite registruoti. Šias priemones galima naudoti kaip paskirstymo bazę arba tiesiog nepiniginėms reikšmėms pranešti.

Statistinių dimensijų narius galima kurti rankiniu būdu. Arba juos galima importuoti iš failo naudojant modulio Duomenų valdymas importavimo / eksportavimo įrankį.

Statistinės dimensijos narys automatiškai tampa iš anksto apibrėžta paskirstymo baze. Jį galima naudoti kaip strategijų paskirstymo bazę arba įvesti į kitų tipų paskirstymo bazes.

Čia pateikiama keletas įprastų statistinės dimensijos narių pavyzdžių.

| Statistinės dimensijos pavadinimas  | Statistiniai elementai | aprašymas             | Vienetas |
|-----------------------------|----------------------|-------------------------|------|
| Bendrai naudojami statistiniai elementai | FTE                  | Darbuotojai, dirbantys visą darbo dieną     | Vnt.  |
| Bendrai naudojami statistiniai elementai | Elektros energija          | Elektros energijos suvartojimas | kwh  |
| Bendrai naudojami statistiniai elementai | Pakavimo CC              | Pakavimo išlaidų centras   | Val. |

## <a name="statistical-measure-provider-template"></a>Statistinių priemonių teikimo įrankio šablonas

Statistinės priemonės gali kilti iš įvairiausių šaltinių. „Microsoft Dynamics 365 for Finance and Operations‟ yra puikus statistinių priemonių išgavimo šaltinis. Naudodami statistinių priemonių teikimo įrankio šabloną galite lengvai konfigūruoti norimas ištraukti statistines priemones.

Statistinių priemonių teikimo įrankio šablono apibrėžtis yra bendro pobūdžio ir ją galima pakartotinai naudoti su keliais statistinių dimensijų nariais.

> [!NOTE]
> Kaip statistinių priemonių šaltinius galima naudoti visas lenteles, kuriose nurodomos finansinės dimensijos.

**Pavyzdys: išlaidų centro darbuotojų skaičius**

Išlaidų centro darbuotojų skaičius yra statistinė priemonė, kurią galima naudoti įvairiais valdymo įžvalgų tikslais:

- Statistinių ataskaitų priemonė pagal išlaidų centrą
- Įvairių tipų išlaidų paskirstymo bazė
- Vidinių išlaidų tarifai pagal išlaidų centrą:

    - Išlaidos pagal darbuotoją
    - Įplaukos pagal darbuotoją

HcmEmployment lentelėje pateikiamas visų egzemplioriaus darbuotojų sąrašas. Ši lentelė yra visuotinė. Todėl įrašai nėra susiję su konkrečiu duomenų srities ID.

Čia pateikiamas darbuotojų HcmEmployment lentelėje pavyzdys.

| Vardas       | Išlaidų centras | aprašymas   | Darbininko tipas |
|------------|-------------|----|-------------|
| 1 darbuotojas | CC001       | Personalas | Darbuotojas    |
| 2 darbuotojas | CC002       | FI | Darbuotojas    |
| 3 darbuotojas | CC002       | FI | Darbuotojas    |
| 4 darbuotojas | CC003       | AP | Darbuotojas    |
| 5 darbuotojas | CC003       | AP | Darbuotojas    |
| 6 darbuotojas | CC002       | FI | Rangovas  |

Kurdami įrašą **Statistinių priemonių teikimo įrankio šablonas** turite nuspręsti, kurią iš tolesnių funkcijų naudoti.

- **Skaičius** – perkeliamas išlaidų objekto įrašų skaičius.
- **Suma** – perkeliama išlaidų objekto įrašų suma. (Laukai **Suma** ir **Data** yra būtini.)

## <a name="using-the-count-function"></a>Funkcijos Skaičius naudojimas

Pavyzdžiui, statistinių priemonių teikimo įrankio šabloną galima nustatyti tolesniu būdu.

| Vardas  | Funkcija | Šaltinio lentelė  | Sumos laukas      | Datos laukas     |
|-------|----------|---------------|----------------|----------------|
| Visu etatu dirbantys darbuotojai  | Skaič.    | HcmEmployment | Netaikoma | Netaikoma |

Taip pat įtraukę vieną ar kelis diapazonus galite sumažinti iš šaltinio lentelės rodomų priemonių skaičių.

Jei šiame pavyzdyje norite tik suskaičiuoti visus visu etatu dirbančius darbuotojus (FTE), galite įtraukti diapazoną į lauką **Darbuotojo tipas**. Lauke **Kriterijai** pasirinkite **Darbuotojas**, kad pateikiamas diapazonas būtų apribotas taip, kaip parodyta toliau.

**Diapazonai**

| Šaltinio lentelė  | Laukas       | Kriterijai |
|---------------|-------------|----------|
| HcmEmployment | Darbininko tipas | Darbuotojas |

Kad statistines priemones galėtumėte perkelti į modulį Kaštų apskaita, turite nustatyti ryšį tarp statistinių priemonių teikimo įrankio šablono ir statistinės dimensijos nario. Šis ryšys sukuriamas pagal modulio Kaštų apskaita didžiąją knygą ir versiją. Ryšį sudaro duomenų jungtis ir duomenų teikimo įrankis. Vienas statistinės dimensijos narys gali turėti keletą duomenų jungčių ir duomenų teikimo įrankių.

> [!NOTE]
> Šiame pavyzdyje ryšį sukursime tik **faktinei versijai**.

Norėdami nustatyti ryšį, eikite į **Didžioji kaštų apskaitos knyga** \> **Faktinė versija** \> **Valdyti** \> **Statistinės priemonės**. Šiuo atveju pasirinkite duomenų teikimo įrankį **„Dynamics 365 for Finance and Operations‟ – statistinės priemonės**, nes duomenis norime išgauti iš „Finance and Operations‟.

**Duomenų šaltinis**

| Vardas        | Duomenų jungtis                                                                     | Statistinės dimensijos narys |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| Visu etatu dirbantys darbuotojai D365FO | „Dynamics 365 for Finance and Operations‟ – statistinės priemonės | Visu etatu dirbantys darbuotojai                         |

**Duomenų teikimo įrankio konfigūracija**

| Statistinio šablono pavadinimas |
|---------------------------|
| Visu etatu dirbantys darbuotojai                      |

Apdorojus statistinės priemonės šaltinio duomenis, modulyje Kaštų apskaita sukuriami tolesni statistiniai įrašai.

**Žurnalas**

| Žurnalas | Žurnalo tipas                       | Ataskaitinis kalendorinis laikotarpis | Metai   |  Laikotarpis  |  Versija | Duomenų jungties šaltinio įrašai|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Statistinių įrašų perkėlimo žurnalas | Finansiniai                 | 2017   | 1 laikotarpis | CA didžiosios knygos USMF | Visu etatu dirbantys darbuotojai                   |

**Statistinių įrašų perkėlimo žurnalo įrašai**

| Ataskaitinė data | Reikšmė | Statistinis elementas |   aprašymas       | Išlaidų centras |
|-----------------|-----------|---------------------|---------------------|-------------|
| 2017-01-31      | 1,00      | Visu etatu dirbantys darbuotojai                | Darbuotojai, dirbantys visą darbo dieną | CC001       |
| 2017-01-31      | 2,00      | Visu etatu dirbantys darbuotojai                | Darbuotojai, dirbantys visą darbo dieną | CC002       |
| 2017-01-31      | 2,00      | Visu etatu dirbantys darbuotojai                | Darbuotojai, dirbantys visą darbo dieną | CC003       |

**Statistiniai įrašai**

| Išlaidų objektas |    | Ataskaitinė data | Statistinės dimensijos narys |  aprašymas        | Reikšmė |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalas | 2017-01-31      | Visu etatu dirbantys darbuotojai                         | Darbuotojai, dirbantys visą darbo dieną | 1,00      |
| CC002       | FI | 2017-01-31      | Visu etatu dirbantys darbuotojai                         | Darbuotojai, dirbantys visą darbo dieną | 2,00      |
| CC003       | AP | 2017-01-31      | Visu etatu dirbantys darbuotojai                         | Darbuotojai, dirbantys visą darbo dieną | 2,00      |

Jei kaštų paskirstymo taisyklėje kaip paskirstymo bazė priskiriamas iš anksto nustatytas visu etatu dirbančių darbuotojų dimensijos nario paskirstymo pagrindas, kaštai bus paskirstomi naudojant tolesnį paskirstymo koeficientą.

| Išlaidų objektas | aprašymas    | Reikšmė | Paskirstymo koeficientas |
|-------------|----|-----------|-------------------|
| CC001       | Personalas | 1,00      | (1/5) × suma    |
| CC002       | FI | 2,00      | (2/5) × suma    |
| CC003       | AP | 2,00      | (2/5) × suma    |

## <a name="using-the-sum-function"></a>Funkcijos Suma naudojimas

Prieš produktus išsiunčiant klientams, jie supakuojami gamybos išlaidų centre CC010 (pakavimas). Tiesioginės darbo išlaidos prie produktų pridedamos naudojant komplektavimo specifikaciją (KS) ir maršrutą. Pagamintiems produktams taip pat reikia paskirstyti netiesiogines išlaidų centro eksploatavimo išlaidas. Dažnai geriausiai tokiam paskirstymui tinkanti statistinė priemonė yra nurodytu laikotarpiu užregistruotų produkto gamybos valandų skaičius.

Lentelėje ProdRouteTrans pateikiamos visos juridinio subjekto DataAreadID gamybos darbo operacijos.

Čia pateikiamas lentelės ProdRouteTrans pavyzdys.

| Nuoroda        | Skaičius | Operacija | Tipas | Laikas  | Faktinė data | Produktų grupė (finansinė dimensija) | Juridinis subjektas |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Gamybos užsakymas | P0001  | Pakuotės | Laikas | 8,00  | 2017-01-01    | Apelsinų sultys B2B                    | USMF         |
| Gamybos užsakymas | P0001  | Pakuotės | Laikas | 8,00  | 2017-02-01    | Apelsinų sultys B2B                    | USMF         |
| Gamybos užsakymas | P0002  | Pakuotės | Laikas | 4,00  | 2017-01-03    | Apelsinų sultys Klientas               | USMF         |
| Gamybos užsakymas | P0003  | Pakuotės | Laikas | 4,00  | 2017-01-03    | Apelsinų sultys Klientas               | USMF         |
| Gamybos užsakymas | P0004  | Rekonstr.  | Laikas | 10,00 | 2017-01-03    | Apelsinų sultys Klientas               | USMF         |

Kurdami įrašą **Statistinių priemonių teikimo įrankio šablonas** turite nuspręsti, kurią iš tolesnių funkcijų naudoti.

- **Skaičius** – perkeliamas išlaidų objekto įrašų skaičius.
- **Suma** – perkeliama išlaidų objekto įrašų suma. (Laukai **Suma** ir **Data** yra būtini.)

Statistinių priemonių teikimo įrankio šabloną galima nustatyti tolesniu būdu.

| Vardas    | Funkcija | Šaltinio lentelė   | Sumos laukas | Datos laukas    |
|---------|----------|----------------|-----------|---------------|
| Pakavimo CC | Suma      | ProdRouteTrans | Valandos     | Faktinė data |

Taip pat įtraukę diapazonų galite sumažinti iš šaltinio lentelės rodomų priemonių skaičių.

Jei šiame pavyzdyje norite tik susumuoti valandas, susijusias su išlaidų centru CC010 pakavimas, galite įtraukti diapazoną į lauką **Operacija**. Lauke **Kriterijai** pasirinkite **Pakavimas**, kad būtų apribotas pateikiamas diapazonas.

**Diapazonai**

| Šaltinio lentelė   | Laukas     | Kriterijai  |
|----------------|-----------|-----------|
| ProdRouteTrans | Operacija | Pakuotės |

Kad statistines priemones galėtumėte perkelti į modulį Kaštų apskaita, turite nustatyti ryšį tarp statistinių priemonių teikimo įrankio šablono ir statistinės dimensijos nario. Šis ryšys sukuriamas pagal modulio Kaštų apskaita didžiąją knygą ir versiją. Ryšį sudaro duomenų jungtis ir duomenų teikimo įrankis. Vienas statistinės dimensijos narys gali turėti keletą duomenų jungčių ir duomenų teikimo įrankių.

> [!NOTE]
> Šiame pavyzdyje ryšį sukursime tik **faktinei versijai**.

Norėdami nustatyti ryšį, eikite į **Didžioji kaštų apskaitos knyga** \> **Faktinė versija** \> **Valdyti** \> **Statistinės priemonės**. Šiuo atveju pasirinkite duomenų teikimo įrankį **„Dynamics 365 for Finance and Operations‟ – statistinės priemonės**, nes duomenis norime išgauti iš „Finance and Operations‟.

**Duomenų šaltinis**

| Vardas           | Duomenų jungtis                                                                     | Statistinės dimensijos narys |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Pakavimo CC D365FO | „Dynamics 365 for Finance and Operations‟ – statistinės priemonės | Pakavimo CC                      |

Sistema atpažįsta, kad ProdRouteTrans yra lentelė, kurioje kiekvienas įrašas priklauso atskiram juridiniam subjektui. Todėl jūsų bus paprašyta pasirinkti juridinį subjektą, iš kurios reikia importuoti operacijas.

**Duomenų teikimo įrankio konfigūracija**

| Statistinio šablono pavadinimas | Juridinis subjektas |
|---------------------------|--------------|
| Pakavimo CC                   | USMF         |

Apdorojus statistinės priemonės šaltinio duomenis, modulyje Kaštų apskaita sukuriami tolesni statistiniai įrašai.

**Žurnalas**

| Žurnalas | Žurnalo tipas                     | Ataskaitinis kalendorinis laikotarpis | Metai   | Laikotarpis | Versija   |   Duomenų jungties šaltinio įrašai  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Statistinių įrašų perkėlimo žurnalas | Finansiniai               | 2017    | 1 laikotarpis  | CA didžiosios knygos USMF | Pakavimo CC |

**Statistinių įrašų perkėlimo žurnalo įrašai**

| Ataskaitinė data | Reikšmė | Statistinis elementas |  aprašymas          | Produktų grupė         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 2017-01-31      | 16,00     | Pakavimo CC             | Pakavimo išlaidų centras | Apelsinų sultys B2B      |
| 2017-01-31      | 8,00      | Pakavimo CC             | Pakavimo išlaidų centras | Apelsinų sultys Klientas |

**Statistiniai įrašai**

| Išlaidų objektas           | Ataskaitinė data | Statistinės dimensijos narys |    aprašymas        | Reikšmė |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Apelsinų sultys B2B      | 2017-01-31      | Pakavimo CC                      | Pakavimo išlaidų centras | 16,00     |
| Apelsinų sultys Klientas | 2017-01-31      | Pakavimo CC                      | Pakavimo išlaidų centras | 8,00      |

Jei kaštų paskirstymo taisyklėje kaip paskirstymo bazė priskiriamas iš anksto nustatytas pakavimo CC dimensijos nario paskirstymo pagrindas, kaštai bus paskirstomi naudojant tolesnį paskirstymo koeficientą.

| Išlaidų objektas           | Reikšmė | Paskirstymo koeficientas  |
|-----------------------|-----------|--------------------|
| Apelsinų sultys B2B      | 16,00     | (16 ÷ 24) × suma |
| Apelsinų sultys Klientas | 8,00      | (8 ÷ 24) × suma  |

## <a name="imported-statistical-measures"></a>Importuotos statistinės priemonės

Statistines priemones į modulį Kaštų apskaita galite importuoti naudodami modulio Duomenų valdymas importavimo / eksportavimo įrankį.

Importuojant naudojamas duomenų objektas pavadintas Importuotos statistinės priemonės.

> [!NOTE]
> Šis duomenų objektas sukurtas taip, kad įrašas galėtų turėti daugiausia penkias unikalias dimensijų reikšmes.

Elektros vartojimas įrašomas programoje „Microsoft Excel‟ naudojant iš anksto nustatytą duomenų objekto formatą. Toliau pateikiamas pavyzdys.

| Ataskaitinė data | 1 dimensijos nario pavadinimas | 2 dimensijos nario pavadinimas | 5 dimensijos nario pavadinimas | Reikšmė  | Šaltinio identifikatorius |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 2017-01-31      | CC001                  |                        |                        | 2,450.00   | Elektros energija       |
| 2017-01-31      | CC002                  |                        |                        | 4,100.00   | Elektros energija       |
| 2017-01-31      | CC003                  |                        |                        | 15,000.00  | Elektros energija       |

Importavus duomenis naudojant modulį Duomenų valdymas, duomenys bus saugomi modulio Kaštų apskaita išdėstymo lentelėje. Todėl importuotus duomenis galima naudoti keliose didžiosiose modulio Kaštų apskaita knygose. Duomenų iš naujo įkelti nereikia.

Norėdami importuoti duomenis, eikite į **Importuoti duomenys** \> **Duomenų objektas** \> **Importuotos statistinės priemonės**.

| Šaltinio identifikatorius | Ataskaitinė data | Reikšmė  | 1 dimensijos nario pavadinimas | 2 dimensijos nario pavadinimas | 5 dimensijos nario pavadinimas |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektros energija       | 2017-01-31      | 2,450.00   | CC001                  |                        |                        |
| Elektros energija       | 2017-01-31      | 4,100.00   | CC002                  |                        |                        |
| Elektros energija       | 2017-01-31      | 15,000.00  | CC003                  |                        |                        |

Kad statistines priemones galėtumėte perkelti į modulį Kaštų apskaita, turite nustatyti ryšį tarp šaltinio identifikatoriaus ir statistinės dimensijos nario. Šis ryšys sukuriamas pagal modulio Kaštų apskaita didžiąją knygą ir versiją. Ryšį sudaro duomenų jungtis ir duomenų teikimo įrankis. Vienas statistinės dimensijos narys gali turėti keletą duomenų jungčių ir duomenų teikimo įrankių.

> [!NOTE]
> Šiame pavyzdyje ryšį sukursime tik **faktinei versijai**.

Norėdami nustatyti ryšį, eikite į **Didžioji kaštų apskaitos knyga** \> **Faktinė versija** \> **Valdyti** \> **Statistinės priemonės**. Šiuo atveju pasirinkite duomenų jungtį **Importuotos statistinės priemonės**, nes naudojant „Excel‟ duomenys buvo importuoti iš trečiosios šalies sistemos į modulį Kaštų apskaita.

**Duomenų šaltinis**

| Vardas        | Duomenų jungtis                | Statistinės dimensijos narys |
|-------------|-------------------------------|------------------------------|
| Elektros energija | Importuotos statistinės priemonės | Elektros energija                  |

**Duomenų teikimo įrankio konfigūracija**

| Importuoti šaltinio identifikatorių | Funkcija | 1 dimensija   | 2 dimensija | 5 dimensija |
|--------------------------|----------|--------------|------------|------------|
| Elektros energija              | Suma      | Išlaidų centrai |            |            |

> [!NOTE]
> Nustatydami duomenų teikimo įrankio konfigūraciją turite nurodyti, kurias išlaidų objekto dimensijas reikia gretinti su importuotomis operacijomis. Apdorojus statistinės priemonės šaltinio duomenis, modulyje Kaštų apskaita sukuriami tolesni statistiniai įrašai.

**Žurnalas**

| Žurnalas | Žurnalo tipas                       | Ataskaitinis kalendorinis laikotarpis | Metai  | Laikotarpis  |Versija      |Duomenų jungties šaltinio įrašai |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Statistinių įrašų perkėlimo žurnalas | Finansiniai                 | 2017  | 1 laikotarpis | CA didžiosios knygos USMF | Elektros energija |

**Statistinių įrašų perkėlimo žurnalo įrašai**

| Ataskaitinė data | Reikšmė  | Savikainos elementas |   aprašymas           | Išlaidų centras |
|-----------------|------------|--------------|-------------------------|-------------|
| 2017-01-31      | 2,450.00   | Elektros energija  | Elektros energijos suvartojimas | CC001       |
| 2017-01-31      | 4,100.00   | Elektros energija  | Elektros energijos suvartojimas | CC002       |
| 2017-01-31      | 15,000.00  | Elektros energija  | Elektros energijos suvartojimas | CC003       |

**Statistiniai įrašai**

| Išlaidų objektas |    | Ataskaitinė data | Statistinės dimensijos narys |      aprašymas                   | Reikšmė  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Personalas | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 2,450.00   |
| CC002       | FI | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 4,100.00   |
| CC003       | AP | 2017-01-31      | Elektros energija                  | Elektros energijos suvartojimas | 15,000.00  |

Jei kaštų paskirstymo taisyklėje kaip paskirstymo bazė priskiriamas iš anksto nustatytas elektros dimensijos nario paskirstymo pagrindas, kaštai bus paskirstomi naudojant tolesnį paskirstymo koeficientą.

| Išlaidų objektas |    | Reikšmė | Paskirstymo koeficientas          |
|-------------|----|-----------|----------------------------|
| CC001       | Personalas | 2,450.00  | (2 450 ÷ 21 550) × suma  |
| CC002       | FI | 4,100.00  | (4 100 ÷ 21 550) × suma  |
| CC003       | AP | 15,000.00 | (15 000 ÷ 21 550) × suma |

## <a name="see-also"></a>Taip pat žiūrėkite

[Paskirstymo bazės](allocation-bases.md)

