---
title: PVM skaičiavimo metodas lauke Kilmė
description: Šiame straipsnyje paaiškinamos PVM kodų puslapio lauko Kilmė parinktys ir tai, kaip PVM skaičiuojamas pagal pasirinktą PVM kodo parinktį.
author: ShylaThompson
ms.date: 06/20/2017
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e57e97847c6aa7a775b0f2639dff93f1e3a9e7a2
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189378"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>PVM skaičiavimo metodas lauke Kilmė

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamos PVM kodų puslapio lauko Kilmė parinktys ir tai, kaip PVM skaičiuojamas pagal pasirinktą PVM kodo parinktį.

Turite pasirinkti kiekvieno puslapyje PVM kodai sukurto PVM kodo skaičiavimo metodą, taikomą mokesčio bazinei sumai lauke Kilmė.

## <a name="percentage-of-net-amount"></a>Grynosios sumos procentai
Grynosios sumos procento skaičiavimo metodas yra numatytoji vertė lauke Kilmė. PVM skaičiuojamas kaip pirkimo ar pardavimo sumos procentas, neįtraukiant visų kitų PVM.
### <a name="example"></a>Pavyzdys

Mokesčio tarifas yra 25%. SF eilutėje rodoma 10 prekių, kiekvienos kaina 1,00, o klientui suteikiama 10 % eilutės nuolaida. Grynoji suma: (10 x 1,00) – 10 % = 9,00 PVM: 9,00 x 25 % = 2,25 Bendroji suma: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Procentas nuo bendros sumos
Pasirinkus bendros sumos procento skaičiavimo metodą, PVM apskaičiuojamas kaip bendros pardavimo sumos procentas. Bendra suma yra grynoji eilutės suma, pridėjus visus eilutei taikomus mokesčius, išskyrus lauke Kilmė nurodytą mokestį = bendros sumos procentas.
### <a name="example"></a>Pavyzdys

Mokesčių institucija taiko prekei specialius muito mokesčius. Muito mokesčio sumos pridedamos prie grynosios sumos prieš PVM skaičiavimą. Duoti šie PVM kodai:
-   1 MUITO MOKESTIS = 10 %, taikant grynosios sumos procento skaičiavimo metodą
-   2 MUITO MOKESTIS = 20 %, taikant grynosios sumos procento skaičiavimo metodą
-   PVM = 25 %, taikant bendros sumos procento skaičiavimo metodą

Jei grynoji suma yra 10,00, tada 1 MUITO MOKESTIS yra 1,00 (10,00 x 10 %) o 2 MUITO MOKESTIS = 2,00 (10,00 x 20 %) Sumos turi būti tokios: bendra suma: grynoji suma + 1 MUITO MOKESČIO suma + 2 MUITO MOKESČIO suma (10,00 + 1,00 + 2,00) = 13,00 PVM = 13,00 x 25 % = 3,25 bendroji MUITO MOKESČIŲ ir PVM suma: 1,00 + 2,00 + 3,25 = 6,25 bendroji suma: 10,00 + 6,25 = 16,25

| **Pastaba.**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vienai operacijai gali būti naudojamas tik vienas mokesčio kodas su kilme = bendros sumos procentas. Jei operacijai naudojamas daugiau nei vienas toks mokesčio kodas, bus rodomas klaidos pranešimas, informuojantis, kad negalima apskaičiuoti PVM. |


## <a name="percentage-of-sales-tax"></a>PVM procentas

Kai lauke Kilmė pasirenkate PVM procentą, PVM yra apskaičiuojamas kaip PVM lauke, dalyje PVM, pasirinkto PVM procentas. Pirmiausia yra apskaičiuojamas PVM, pasirinktas PVM lauke, dalyje PVM. Tada skaičiuojamas antras PVM pagal pirmą PVM sumą.
### <a name="example"></a>Pavyzdys

Duoti šie PVM kodai:
-   1 MUITO MOKESTIS = 10 %, taikant grynosios sumos procento metodą
-   2 MUITO MOKESTIS = 20 %, taikant PVM procento metodą, kai PVM dalyje, PVM lauke pasirinktas 1 muito mokestis
-   PVM = 25 %, taikant bendros sumos procento metodą

Grynoji suma: 10,00 1 MUITO MOKESTIS: 10,00 x 10 % = 1,00 2 MUITO MOKESTIS: 1,00 x 20 % = 0,20 Bendra suma: 10,00 + 1,00 + 0,20 = 11,20 PVM: 11,20 x 25 % = 2,80 Visa MUITO MOKESČIŲ ir PVM suma: 1,00 + 0,20 + 2,80 = 4,00 Visa suma: 10,00 + 4,00 = 14,00

| **Pastaba.**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mokesčių skaičiavimai neapima kelių lygių mokesčių apskaičiavimo galimybės. Mokestis negali būti apskaičiuojamas pagal mokestį, kuris buvo apskaičiuotas remiantis kitu mokesčiu. Gali būti apskaičiuoti keli vieno lygio tam tikros operacijos mokesčiai remiantis mokesčių kodais. |

## <a name="amount-per-unit"></a> Suma pagal vienetą
Pasirinkus lauke Kilmė sumą už vienetą, PVM yra apskaičiuojamas kaip fiksuota suma už vienetą, padauginta iš dokumento eilutėje nurodyto kiekio. Vienetas turi būti pasirinktas lauke Vienetas. Suma už vienetą nurodyta puslapyje PVM kodų vertės.
### <a name="example"></a>Pavyzdys

PVM kodas nustatomas kaip: 1,20 JAV dol. už vienetą = langelį Pardavimo SF eilutėje parduoti 25 langeliai PVM apskaičiuojamas kaip 25 x 1,20 = 30,00

| **Pastaba.**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jei įvedant operaciją naudojami kitokie, nei PVM kodų dalyje nurodyti vienetai, jie automatiškai konvertuojami remiantis vienetų konvertavimo vertėmis, nustatytomis puslapyje Vienetų konvertavimas. |

###  <a name="amount-per-unit-additional-option"></a> Suma už vienetą (papildoma parinktis)

Skirtuke Skaičiavimas galite pasirinkti, ar sumos už vienetą mokestis bus apskaičiuojamas pirmiau, nei kiti mokesčių kodai, ir pridedamas prie grynosios sumos pirmiau, nei apskaičiuojami kiti mokesčių kodai su kilme = grynosios sumos procentu.

### <a name="examples"></a>Pavyzdžiai

Tarkime, turime apskaičiuoti 2 operacijos mokesčių kodus:

-   MUITO MOKESTIS: kilmė = suma už vienetą ir PVM, vertė nustatyta kaip 5,00 už vienetą = vnt.
-   SALESTAX: kilmė = kaip parodyta toliau pateikiamuose pavyzdžiuose, nustatyta vertė 25 %

Parduoti 1 prekės vienetą už 10,00
#### <a name="example-1"></a>1 pavyzdys

SALESTAX: kilmė = bendrosios sumos procento metodas Parinktis Skaičiuoti prieš PVM neturi įtakos, nes PVM yra skaičiuojamas kaip bendros sumos procentas. MUITO MOKESTIS: 1 x 5,00 = 5,00 Bendra suma: 10,00 + 5,00 = 15,00 PVM: 15,00 x 25 % = 3,75 Visa PVM suma: 5,00 + 3,75 = 8,75 Visa suma: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>2 pavyzdys

PVM: kilmė = grynosios sumos procentas Parinktis Skaičiuoti prieš PVM nepasirinkta MUITO MOKESČIUI skaičiuoti. Grynoji suma: 10,00 MUITO MOKESTIS: 1 x 5,00 = 5,00 PVM: 10,00 x 25 % = 2,50 Visa PVM suma: 5,00 + 2,50 = 7,50 Visa suma: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>3 pavyzdys

PVM: kilmė = grynosios sumos procentas Parinktis Skaičiuoti prieš PVM pasirinkta MUITO MOKESČIUI skaičiuoti. Grynoji suma: 10,00 MUITO MOKESTIS: 1 x 5,00 = 5,00 PVM: (10,00 + 5,00) x 25 % = 3,75 Visa PVM suma: 5,00 + 3,75 = 8,75 Visa suma: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>4 pavyzdys

3 ir 1 pavyzdžio rezultatas yra toks pat, nes yra tik vienas muito mokestis. Tarkime, kad turite du muito mokesčius ir tik vienas iš jų įtrauktas į grynoji suma, PVM skaičiavimas: muito mokestį 1: 5,00, naudojant vieneto metodą sumą ir toliau skaičiuoti prieš PVM pasirinktis yra pažymėtas muito 2: 2,50, naudojant vieneto metodą sumą ir toliau skaičiuoti prieš PVM pasirinktis nėra pasirinkto PVM : 25 %, naudojant grynoji suma metodas grynosios sumos procentai: 10,00 muito mokestį 1: 1 x 5,00 = 5,00 muito 2: 1 x 2,50 = 2,50 grynosios sumos, kurioms taikomas PVM: 10,00 + 5,00 = 15,00 SALESTAX: 15,00 x 25 % = 3,75 bendroji PVM, įskaitant mokesčius: 5,00 + 2,50 + 3,75 = 11,25 bendroji suma: 10,00 + 11,25 = 21,25 sumų grynoji suma (10,00) + 1 (5,00) muito mokestis skaičiuojamas SALESTAX 25 % = 15,00. 2 MUITO MOKESTIS pridedamas prie PVM sumos, kai PVM apskaičiuojamas.

## <a name="calculated-percentage-of-net-amount"></a> Apskaičiuotas grynosios sumos procentas
Apskaičiuojant grynosios sumos procentą mokesčių apskaičiavimas priklauso nuo dokumento ar žurnalo parametro Sumos, įskaitant PVM.
### <a name="example-1"></a>1 pavyzdys

Dokumento / žurnalo parametras Sumos, įskaitant PVM = Taip Operacijos eilutės suma: 10,00 Mokesčio tarifas: 25 % PVM: operacijos eilutės suma x mokesčio tarifas (10,00 x 25 %) = 2,50 Mokesčio bazinė suma (kilmės suma): operacijos eilutės suma – PVM (10,00 – 2,50) = 7,50

### <a name="example-2"></a>2 pavyzdys

Dokumento / žurnalo parametras Sumos, įskaitant PVM = Ne Operacijos eilutės suma: 10,00 Mokesčio tarifas: 25 % PVM: (operacijos eilutės suma x mokesčio tarifas) / (100 – mokesčio tarifas) (10,00 x 25 %) / (100 % – 25 %) = 3,33 Mokesčio bazinė suma (kilmės suma): operacijos eilutės suma = 10,00



## <a name="additional-resources"></a>Papildomi ištekliai

[PVM tarifai pagal bazinę ribą ir skaičiavimo metodus](marginal-base-field.md)

[PVM kodų skaičiavimo parinktys Visa suma ir Intervalas](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]