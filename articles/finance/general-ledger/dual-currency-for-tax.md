---
title: Mokesčiuose dviejų valiutų palaikymas
description: Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją mokesčių srityje, ir nurodoma, koks gali būti poveikis mokesčiams apskaičiuoti ir registruoti
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0a3245febe31857181d17bba42e12b65f4ebb40f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832975"
---
# <a name="dual-currency-support-for-sales-tax"></a>PVM dviejų valiutų palaikymas
[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip išplėsti dviejų valiutų apskaitos funkciją PVM srityje, ir nurodoma, koks gali būti poveikis PVM apskaičiuoti, registruoti ir sudengti.

„Dynamics 365 Finance“ dviejų valiutų funkcija atsirado 8.1 versijoje (2018 m. spalio mėn.). Ji pakeitė, kaip apskaičiuojami apskaitos įrašai ataskaitų valiuta.

Ankstesnėse versijose operacijos buvo konvertuojamos į ataskaitų valiutą tokia tvarka: 

- Operacijos suma buvo apskaičiuota operacijos valiuta > operacijos suma buvo konvertuota į apskaitos valiutą > apskaitos valiutos suma buvo konvertuota į ataskaitų valiutą

Įjungus dviejų valiutų funkciją, operacijos buvo konvertuotos į ataskaitų valiutą tokia tvarka:

- Suma operacijos valiuta > Suma ataskaitų valiuta

Daugiau informacijos apie dviejų valiutų funkciją rasite [Dvi valiutos](dual-currency.md).

Dėl dviejų valiutų palaikymo funkcijų valdyme atsirado dvi naujos funkcijos: 

- Prekybos mokesčių konvertavimas (naujas versijoje 10.0.13)

Dviejų valiutų palaikymas PVM srityje užtikrina, kad mokesčiai bus tiksliai apskaičiuoti mokesčių valiuta ir kad PVM sudengimo balansas bus apskaičiuotas tiksliai ir apskaitos valiuta, ir ataskaitų valiuta. 

## <a name="sales-tax-conversion"></a>PVM konvertavimas

Parametras **PVM konvertavimas** suteikia dvi parinktis, kaip galima konvertuoti mokesčių sumą iš operacijos valiutos į mokesčių valiutą. 

- Apskaitos valiuta: kelias: Suma operacijos valiuta > Suma apskaitos valiuta > Suma mokesčių valiuta. Apskaitos valiutos keitimo kurso tipas (konfigūruojamas mokesčių valiutos nustatyme) bus naudojamas valiutos konvertavimui.
- Ataskaitų valiuta: kelias: Suma operacijos valiuta > Suma ataskaitų valiuta > Suma mokesčių valiuta. Ataskaitų valiutos keitimo kurso tipas (konfigūruojamas mokesčių valiutos nustatyme) bus naudojamas valiutos konvertavimui.

### <a name="example"></a>Pavyzdys

Paprastas pavyzdys, skirtas šiai funkcijai pademonstruoti:

DK ir mokesčių valiutos nustatymas

| Operacijos valiuta | Apskaitos valiuta | Ataskaitų valiuta | Mokesčių valiuta |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | LT                | LT          |

Valiutos kursas

| Iš valiutos | Į valiutą | Koeficientas | Valiutos kursas |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1      | 1.11          |
| EUR           | LT         | 1      | 0.83          |
| USD           | LT         | 1      | 0.75          |

Mokesčio sumos skaičiavimas naudojant skirtingas parametro parinktis

Mokesčio suma = 100 EUR

| PVM konvertavimo parametrai | Operacijos valiuta (EUR) | Apskaitos valiuta (USD) | Ataskaitų valiuta (GBP) | Mokesčių valiuta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Apskaitos valiuta             | 100                        | 111                       | 83                       | **83.25**          |
| Ataskaitų valiuta              | 100                        | 111                       | 83                       | **83**             |

Šis parametras gali būti sukonfigūruotas, atsižvelgiant į tai, ko reikalauja mokesčių inspekcija.


### <a name="upgrade-consideration"></a>Atnaujinimo aplinkybės

Ši funkcija bus taikoma tik naujoms operacijoms. Mokesčių operacijai, kuri jau įrašyta TAXTRANS lentelėje, bet dar nėra sudengta, sistema neperskaičiuos mokesčių sumos mokesčių valiuta, nes registruojant mokestį nėra valiutos kurso.

Kad būtų užkirstas kelias ankstesniam scenarijui, rekomenduojame pakeisti šią parametro vertę nauju (švariu) mokesčių sudengimo laikotarpiu, kuriame nėra nesudengtų mokesčių operacijų. Norėdami pakeisti šią vertę mokesčių sudengimo laikotarpio viduryje, prieš keisdami šio parametro reikšmę vykdykite dabartinio mokesčių sudengimo laikotarpio programą Sudengti ir registruoti PVM.


## <a name="track-reporting-currency-tax-amount"></a>Mokesčių sumos ataskaitų valiuta sekimas

Trys nauji laukai buvo įtraukti į su mokesčiais susijusias lenteles, kad būtų galima sekti sumas ataskaitų valiuta. Šie laukai yra lentelėse TAXUNCOMMITTED ir TAXTRANS:

- TaxAmountRep: mokesčių suma ataskaitų valiuta
- TaxBaseAmountRep: bazinė suma ataskaitų valiuta
- TaxInCostPriceRep: neišskaitoma suma ataskaitų valiuta

Mokesčių, tik įrašytų lentelėje TAXUNCOMMITTED, bet dar neužregistruotų atveju sistema perskaičiuos mokesčių sumą ataskaitų valiuta, kai registruos, ir įrašys lentelėje TAXTRANS.

Šioje versijoje nėra pakeitimų, susijusių su ataskaitomis ir formomis, kuriose rodoma mokesčių suma ataskaitų valiuta. Ataskaitų ir formų pakeitimai bus pristatyti būsimose versijose.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Mokesčių sudengimo automatinis balansas ataskaitų valiuta

Jei mokesčių nustatymas yra nesubalansuotas ataskaitų valiutoje dėl tam tikrų priežasčių, tokių kaip prekybos mokesčių konveratvimo kelio „Apskaitos valiuta“ arba keitimo kurso pasikeitimo vieno mokesčio nustatymo laikotarpio metu, tuomet sistema automatiškai sukurs apskaitos įrašus, kad pakeistų mokesčio vertės pokyčius ir paleis juos pagal atliktų keitimų pelną ar nuostolius, kurie konfigūruojami mokesčių valiutos nustatyme.

Pagal ankstesnį pavyzdį šiai funkcijai pademonstruoti, įsivaizduokite, kad registravimo metu lentelėje TAXTRANS yra tokie duomenys.

| PVM konvertavimo parametrai | Operacijos valiuta (EUR) | Apskaitos valiuta (USD) | Ataskaitų valiuta (GBP) | Mokesčių valiuta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Apskaitos valiuta             | 100                        | 111                       | 83                       | **83.25**          |
| Ataskaitų valiuta              | 100                        | 111                       | 83                       | **83**             |

Paleidus PVM sudengimo programą mėnesio pabaigoje, apskaitos įrašas bus toks:
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scenarijus: PVM konvertavimas = apskaitos valiuta

| Korespondentinė sąskaita, subsąskaita           | Operacijos valiuta (GBP) | Apskaitos valiuta (USD) | Ataskaitų valiuta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Mokėtinas / susigrąžinamas mokestis | -83,25                     | -111                      | -83,25                   |
| Mokesčio sudengimas         | 83.25                      | 111                       | 83.25                    |
| Gautas pelnas / nuostolis     | 0                          | 0                         | -0,25                    |
| Mokėtinas / susigrąžinamas mokestis | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scenarijus: PVM konvertavimas = ataskaitų valiuta


| Korespondentinė sąskaita, subsąskaita           | Operacijos valiuta (GBP) | Apskaitos valiuta (USD) | Ataskaitų valiuta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Mokėtinas / susigrąžinamas mokestis | -83                        | -110,67                   | -83                      |
| Mokesčio sudengimas         | 83                         | 110.67                    | 83                       |
| Gautas pelnas / nuostolis     | 0                          | 0.33                      | 0                        |
| Mokėtinas / susigrąžinamas mokestis | 0                          | -0,33                     | 0                        |



Daugiau informacijos ieškokite šiose temose:

- [Dvi valiutos](dual-currency.md)
- [PVM apžvalga](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]