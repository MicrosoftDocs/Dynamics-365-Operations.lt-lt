---
title: Naudojimo teise valdomo turto nusidėvėjimo įrašymas (peržiūros versija)
description: Šiame straipsnyje paaiškinama, kaip sukurti amortizavimo, kuris reikalingas nuomai, kurios pripažįstamos organizacijos balanso lape, žurnalo įrašą.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903282"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Naudojimo teise valdomo turto nusidėvėjimo įrašymas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Jei nuoma pripažįstama organizacijos balanse, naudojimo teise valdomas turtas amortizuojamas kas mėnesį. Šiame straipsnyje paaiškinama, kaip sukurti amortizavimo žurnalo įrašą. Amortizacija debetuoja išlaidų DK sąskaitą ir kredituoja sukauptą nusidėvėjimo DK sąskaitą, atsižvelgiant į jūsų registravimo šablono sąranką ir nuomos tipą. Šie įrašai gali būti sukurti kiekvienai nuomai arba jie gali būti sukurti kelioms nuomoms, naudojant paketo žurnalo funkcijas.

## <a name="asset-depreciation-schedule"></a>Turto nusidėvėjimo grafikas

1. Puslapyje **Nuomos suvestinė** pasirinkite nuomą. Tada pasirinkite **Knygos \> Turto nusidėvėjimo grafikas**, kad būtų atidaromas puslapis **Turto nusidėvėjimo grafikas**.

    Naudojimo teise valdomo turto nusidėvėjimo išlaidų žurnalo įrašas yra paremtas suma, nurodyta stulpelyje **Nusidėvėjimo išlaidos**. Kaip pavyzdį pateikta informacija apie nurodymus, kaip užtikrinti apskaitos standarto atitikimą, [žr. RUB turto amortizavimo išlaidų skaičiavimą](#calculation-of-rou-asset-amortization-expense-for-finance-leases) finansų nuomos sekcijai toliau šiame straipsnyje.
    
2. Pasirinkite nusidėvėjimo laikotarpį ir pasirinkite **Kurti žurnalą**. Gausite pranešimą, kuriame nurodoma, kad sukurtas žurnalas, kuris bus naudojamas nusidėvėjimui įrašyti.
3. Pasirinkite **Žurnalai \> Turto nuomos žurnalai**, kad būtų atidarytas puslapis **Turto nuomos žurnalas**, kuriame galite peržiūrėti sukurtą nusidėvėjimo išlaidų žurnalo įrašą.

   Sistema užrakina tam tikrus finansinius laukus, kad išvengtų nuokrypių tarp operacijų ir grafikų. Kai kurie laukai, kurie yra užrakinti, apima **sąskaitą**, **sumas**, **finansines dimensijas**, **valiutą** ir **operacijos tipą**. Be to, žurnalo įrašų eilučių nebus galima įtraukti į žurnalo žurnalo įrašus, nes dėl to gali atsirasti nuokrypių tarp grafikų ir operacijų.

4. Pasirinkite žurnalo įrašą ir pasirinkite **Registruoti**, kad įrašytumėte nusidėvėjimo įrašą į DK.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Veiklos nuomos naudojimo teise valdomo turto amortizavimo išlaidų skaičiavimas

Veiklos nuomos nusidėvėjimo išlaidos apskaičiuojamos kaip skirtumas tarp mėnesio tiesioginių nuomos išlaidų ir mėnesio palūkanų išlaidų, esančių nuomos įsipareigojime, pagal apskaitos standartų kodifikavimą temoje Nr. 842 (ASC 842), kuri yra standartas bendrai priimtuose apskaitos principuose JAV (US GAAO). Tiesioginės nuomos išlaidos apskaičiuojamos kaip visų nuomos mokėjimų suma, padalyta iš nuomos laikotarpio mėnesiais. (Nuomos mokesčių suma apima bet kokius išankstinius mokėjimus, pradines tiesiogines išlaidas, išmontavimo išlaidas ir nuomos paskatas.) Šioje lentelėje pateikiamas veiklos nuomos amortizacijos išlaidų pavyzdys.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Veiklos nuomos naudojimo teise valdomo turto amortizavimo išlaidų pavyzdys

| Laukas                                          | Reikšmė       |
|------------------------------------------------|-------------|
| Mokėjimo suma                                 | 1000       |
| Mokėjimo dažnumas                              | Mėnesinis     |
| Nuomos terminas (mėnesiais)                            | 24          |
| Visi nuomos mokėjimai                           | 24,000      |
| Apskaičiuota skolinimosi palūkanų norma                     | 5 %          |
| Anuiteto tipas                                   | Mokėtinas anuitetas |
| Sujungimo intervalas                           | Mėnesinis     |
| Dabartinė būsimų minimalių nuomos mokesčių vertė | 22,888.87   |

Kaip minėta anksčiau, tiesioginės nuomos išlaidos apskaičiuojamos kaip visų mokėjimų suma, padalyta iš nuomos laikotarpio. Sistema automatiškai apskaičiuoja mėnesio palūkanų išlaidas pagal įsipareigojimo amortizacijos grafiką. Palūkanų išlaidos apskaičiuojamos naudojant faktinių palūkanų tarifo metodą. Sistema naudos tiesiogines nuomos išlaidas, kad būtų atimtos kiekvieno mėnesio palūkanų išlaidos. Reikšmė naudojama norint sumažinti naudojimo teise valdomą turtą.

| Mėnuo | Tiesioginės nuomos išlaidos | Palūkanų išlaidos                        | Naudojimo teise valdomo turto amortizavimo išlaidų skaičiavimas |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24 000 ÷ 24) = 1000,00 | (22 888,87 – 1000) × (5 % ÷ 12) = 91,20 | 1000 – 91,20 = 908,80                        |
| 2     | (24 000 ÷ 24) = 1000,00 | (21 980,08 – 1000) × (5 % ÷ 12) = 87,42 | 1000 – 87,42 = 912,58                        |
| 3     | (24 000 ÷ 24) = 1000,00 | (21 067,49 – 1000) × (5 % ÷ 12) = 83,62 | 1000 – 83,62 = 916,39                        |

> [!NOTE]
> Pagal ASC 842, veiklos nuomos naudojimo teise valdomo turto nusidėvėjimas yra priskiriamas prie pajamų išrašo nuomos išlaidų. Siekiant padidinti matomumą, turto nuoma apibūdina įrašą kaip naudojimo teise valdomo turto nusidėvėjimą. Tačiau debeto įrašas turi būti priskirtas veiklos nuomos išlaidų sąskaitai, o kredito įrašas turi būti priskirtas tiesiogiai veiklos nuomos naudojimo teise valdomam turtui. Nepaisant to, nuomos parametruose galite nurodyti, kad kredito įrašai turi būti registruojami veiklos naudojimo teise valdomo turto sukaupto nusidėvėjimo sąskaitoje.

Jei nuoma klasifikuota kaip veiklos nuoma, mėnesinis nusidėvėjimas po pablogėjimo bus skaičiuojamas naudojant tiesiogiai apskaičiuotą nusidėvėjimą.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Finansinės nuomos naudojimo teise valdomo turto amortizavimo išlaidų skaičiavimas

Dėl finansinės nuomos, kuriai priklauso finansinė klasifikacija, sistema apskaičiuoja naudojimo teise valdomo turto amortizaciją tiesiogiai. Todėl kiekvieno mėnesio nusidėvėjimo išlaidos bus vienodos.

Pagal tarptautinį finansinės atskaitomybės standartą Nr. 16 (IFRS 16) ir ASC 842 turtas bus amortizuotas per nuomos arba turto naudingo naudojimo laiką (bus pasirinktas trumpesnis laikotarpis). Be to, jei nuomos parametras **Nuosavybės perdavimas** įjungtas, nuoma automatiškai nusidėvės per turto naudingo naudojimo laiką.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Finansinės nuomos naudojimo teise valdomo turto amortizavimo išlaidų pavyzdys

| Laukas                                | Reikšmė                                   |
|--------------------------------------|-----------------------------------------|
| Naudojimo teise valdomo turto balanso pradžia | 22,889.87                               |
| Nuomos terminas (mėnesiais)                  | 24                                      |
| Turto naudingo naudojimo laikas (mėnesiais)           | 36                                      |
| Mėnuo                                | Naudojimo teise valdomo turto amortizacijos išlaidos |
| 1                                    | 22 889,87 ÷ 24 = 953,74                 |
| 2                                    | 22 889,87 ÷ 24 = 953,74                 |
| 3                                    | 22 889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
