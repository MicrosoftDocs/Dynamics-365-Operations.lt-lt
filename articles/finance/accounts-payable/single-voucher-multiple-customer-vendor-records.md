---
title: Vienas kvitas su keliais kliento arba tiekėjo įrašais
description: Šioje temoje pateikiama apžvalga, kas atsitinka, kai užregistruojate vieną kvitą su keliais kliento ir tiekėjo įrašais. Būsimose „Microsoft“ „Dynamics 365 Finance“ versijose ši funkcija nebebus naudojama, todėl nerekomenduojame naudoti šio registravimo būdo dėl apskaitos įtakos sudengimo apdorojimui.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8677eba2c38c6273555e1189c0153272a8ff9e005655f3846c0d7605b872ff94
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737046"
---
# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Vienas kvitas su keliais kliento arba tiekėjo įrašais

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama apžvalga, kas atsitinka, kai užregistruojate vieną kvitą su keliais kliento ir tiekėjo įrašais. Būsimose versijose ši funkcija nebebus naudojama, todėl nerekomenduojame naudoti šio registravimo būdo dėl apskaitos įtakos sudengimo apdorojimui. 

Prie pavyzdžių, kai vienas kvitas naudojamas keliems klientams arba tiekėjams, galima priskirti balanso perkėlimus tarp klientų ir padengimo balansus tarp klientų ir tiekėjų toje pačioje organizacijoje. 

Kvitas, kuriame yra daugiau nei vienas klientas arba tiekėjas gali būti įvedamas naudojant vieną iš šių metodų:

-   Naudojant žurnalą, kuriame pažymėta parinktis **Tik vienas kvito numeris**, kad kiekviena į žurnalą įtraukta eilutė būtų įtraukiama tame pačiame kvite.
-   Naudojant kelių eilučių kvitą, kuriame nėra korespondentinės DK sąskaitos, su daugiau nei vienu klientu arba tiekėju.
-   Įvedant kvitą, kurio sąskaita ir korespondentinė sąskaitą yra tiekėjas / tiekėjas, klientas / klientas, tiekėjas / klientas ar klientas / tiekėjas.

Šioje temoje rodoma, kaip bus apdorojamas sudengimas užregistravus vieną kvitą su keliais kliento arba tiekėjo įrašais. Be to, šioje temoje pateikiami apėjimo būdai, kad būtų lengviau suprasti, kaip galima nenaudoti vieno kvito su keliais klientais ar tiekėjais. Tiksliau kalbant, yra pavyzdžių, kuriuose vaizduojami du bendri sudengimo scenarijai, kuriems turi įtakos vieno kvito naudojimas su keliais klientais ar tiekėjais:

-   Mokėjimo nuolaidos apskaita
-   Perkainojimo apskaita

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Kokį poveikį sudengimas turi naudojant vieną kvitą
Registruojant kvitą, kuriame yra keletas kliento arba tiekėjo įrašų, sukuriamas vienas apskaitos kvitas, kuriame yra keli gautinų arba mokėtinų sumų balansai. Vykstant sudengimo procesui pradiniai apskaitos įrašai naudojami norint sukurti mokėjimo nuolaidos, negauto pelno ir nepatirtų nuostolių ir pradinio dokumento suminės sąskaitos nuolaidos apskaitos įrašus. Pavyzdžiui, jei mokėjimo nuolaida pritaikoma sudengiant tiekėjo mokėjimą į sąskaitą faktūrą, mokėjimo nuolaidos apskaitą reikia užregistruoti mokėtinų sumų didžiosios knygos sąskaitoje iš pradinės sąskaitos faktūros. Jei pradinė sąskaita faktūra užregistruota kvite, kuriame yra keli tiekėjo įrašai, parengiama pradinės apskaitos suvestinė. Tokiu atveju, kadangi nėra jokios galimybės pasiekti išsamų kiekvieno tiekėjo operacijos apskaitos įrašą viename kvite, nėra jokios galimybės nustatyti, kaip vartotojas norėjo, kad mokėjimo nuolaida būtų atskaityta.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Vienas kvitas su keliais tiekėjais ir poveikis mokėjimo nuolaidos apskaitai

Toliau pateikiamame pavyzdyje kelių tiekėjų sąskaitos faktūros įrašomos į didžiąją knygą viename puslapio **Bendrasis žurnalas** kvite. Šios sąskaitos faktūros paskirstomos kelių sąskaitų dimensijose.

| Kvitas | Kodo tipas | Paskyra  | aprašymas | Debetas | Kreditas |
|-------------|------------------|--------------|-----------------|-----------|------------|
| GNJL001     | Tiekėjas           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Tiekėjas           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Tiekėjas           | 1001         | INV3            |           | 300,00     |
| GNJL001     | DK           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | DK           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | DK           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | DK           | 606300-004-- | INV3            | 300,00    |            |

Užregistravus sukuriamas vienas kvitas.

| Kvitas | Paskyra  | Registravimo tipas | Suma operacijos valiuta |
|-------------|--------------|------------------|------------------------------------|
| GNJL001     | 606300-001-- | DK žurnalas   | 50,00                              |
| GNJL001     | 606300-002-- | DK žurnalas   | 50,00                              |
| GNJL001     | 606300-003-- | DK žurnalas   | 200,00                             |
| GNJL001     | 606300-004-- | DK žurnalas   | 300,00                             |
| GNJL001     | 200110-001-  | Tiekėjo balansas   | -100.00                            |
| GNJL001     | 200110-001-  | Tiekėjo balansas   | –200,00                            |
| GNJL001     | 200110-001-  | Tiekėjo balansas   | -300.00                            |

Atkreipkite dėmesį, kad kvite yra trys įrašai, skirti vieno kvito tiekėjo balanso registravimo tipui. Nėra jokios galimybės nurodyti, kad 606300-001 skirtas 50,00 debetas ir 606300-002 skirtas 50,00 debetas turėtų atidėti 200110-001 tiekėjo balanso įrašą. Taip yra todėl, kad vartotojas viename kvite įvedė kelis tiekėjo įrašus.

Naudodami šį pavyzdį mes galime analizuoti, kokį poveikį vieno kvito naudojimas turi proceso pabaigos sudengimo apskaitai. Tarkime, kad jūs apmokate 197,00 iš 200,00 sąskaitos faktūros ir jums pritaikoma 3,00 mokėjimo nuolaida. Atkreipkite dėmesį, kad mokėjimo nuolaidos sąskaitos vertė paskirstoma visose dimensijose iš sąskaitos faktūros kvito išlaidų sąskaitos. Taip yra todėl, kad vienas kvitas buvo naudojamas registruojant pirmiau minėtą sąskaitą faktūrą nenurodant, kaip vartotojas ketino susieti išlaidų paskirstymus su tiekėjo balansu viename kvite.

| Kvitas | Paskyra  | Registravimo tipas     | Debetas | Kreditas |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Tiekėjo balansas       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bankas                 |           | 197.00     |
| 14000056    | 520200-001-- | Tiekėjo mokėjimo nuolaida |           | 0.25       |
| 14000056    | 520200-002-- | Tiekėjo mokėjimo nuolaida |           | 0.25       |
| 14000056    | 520200-003-- | Tiekėjo mokėjimo nuolaida |           | 1,00       |
| 14000056    | 520200-004-- | Tiekėjo mokėjimo nuolaida |           | 1.50       |
| 14000056    | 200110-001-  | Tiekėjo balansas       | 3,00      |            |

Jei vartotojas nepatenkintas, kad mokėjimo nuolaida paskirstoma visuose pradinės sąskaitos faktūros išlaidų paskirstymuose, o ne viename kvite, norint įrašyti sąskaitas faktūras turėtų būti naudojami keli kvitai. Toliau pateikiamas pavyzdys, kaip į didžiąją knygą galima įvesti kelis kvitus, o ne naudoti vieną kvitą, kaip nurodyta šio pavyzdžio pradžioje.

| Kvitas | Kodo tipas | Paskyra  | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL001     | Tiekėjas           | 1001         | INV1            |           | 100,00     | DK          | &lt;tuščia&gt;      |
| GNJL001     | DK           | 606300-001-- | INV1            |   50,00   |            | DK          | &lt;tuščia&gt;      |
| GNJL001     | DK           | 606300-002-- | INV1            |   50,00   |            | DK          | &lt;tuščia&gt;      |
| GNJL002     | Tiekėjas           | 1001         | INV2            |           | 200,00     | DK          | 606300-003--       |
| GNJL003     | Tiekėjas           | 1001         | INV3            |           | 300,00     | DK          | 606300-004--       |

Dabar, kai apmokama INV2, pateikiamas toliau nurodytas įrašas. Atkreipkite dėmesį, kad mokėjimo nuolaidos finansinės dimensijos pateikiamos po susietųjų išlaidų finansinių dimensijų.

| Kvitas | Paskyra  | Registravimo tipas     | Debetas | Kreditas |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Tiekėjo balansas       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bankas                 |           | 197.00     |
| 14000056    | 520200-003-- | Tiekėjo mokėjimo nuolaida |           | 3,00       |
| 14000056    | 200110-001-  | Tiekėjo balansas       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Vienas kvitas su keliais tiekėjais ir poveikis gauto pelno / patirto nuostolio apskaitai

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Kodo tipas | Paskyra  |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| GNJL001     | Tiekėjas           | 1001        | INV1            |           | 100,00     | DK           | 606300-001-- |
| GNJL001     | Tiekėjas           | 1001        | INV2            |           | 200,00     | DK           | 606300-002-- |

Toliau pateikiamame pavyzdyje kelių tiekėjų sąskaitos faktūros įrašomos į didžiąją knygą viename puslapio **Bendrasis žurnalas** kvite. Šios sąskaitos faktūros paskirstomos kelių sąskaitų dimensijose. Užregistravus sukuriamas vienas kvitas.

| Kvitas | Paskyra  | Registravimo tipas | Suma operacijos valiuta (EUR) | Suma apskaitos valiuta (USD) |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| GNJL001     | 606300-001-- | DK žurnalas   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | DK žurnalas   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Tiekėjo balansas   | -100.00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Tiekėjo balansas   | –200,00                                  | -228.00                                 |

Atkreipkite dėmesį, kad kvite yra du įrašai, skirti vieno kvito tiekėjo balanso registravimo tipui. Nėra jokios galimybės nurodyti, kad 606300-001 skirtas debetas turėtų atidėti tiekėjo balanso 100,00 įrašą iki 200110-001. Taip yra todėl, kad vartotojas viename kvite įvedė kelis tiekėjo įrašus. 

Naudodami šį pavyzdį mes galime analizuoti, kokį poveikį vieno kvito naudojimas turi proceso pabaigos sudengimo apskaitai. Tarkime, kad jūsų apskaitos valiuta yra USD, o pirmiau minėtos operacijos užregistruotos nurodant operacijų valiutą EUR. Tarkime, kad visiškai apmokate 200,00 EUR sąskaitą faktūrą, bet dėl valiutos kurso skirtumo tuo metu, kai registruojate sąskaitą faktūrą ir tuo metu, kai atliekate mokėjimą, patiriate nuostolį. Atkreipkite dėmesį, kad patirto nuostolio sąskaitos vertė paskirstoma visose dimensijose iš sąskaitos faktūros kvito išlaidų sąskaitos. Šiuo atveju dimensijos 001 ir 002 buvo paskirstytos, net jei vartotojui gali atrodyti, kad į išlaidų sąskaitą iš padengiamos sąskaitos faktūros turėtų būti įtraukiama tik 002. Taip yra todėl, kad vienas kvitas buvo naudojamas registruojant pirmiau minėtą sąskaitą faktūrą nepaliekant jokios galimybės nurodyti, kaip vartotojas ketino susieti išlaidų paskirstymus su tiekėjo balansu viename kvite.

| Kvitas | Paskyra | Registravimo tipas   | Suma operacijos valiuta (EUR) | Suma apskaitos valiuta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Tiekėjo balansas     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bankas               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Valiutos kurso nuostolis | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Valiutos kurso nuostolis | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Tiekėjo balansas     |                                          | -2.00                                   |

Jei vartotojas nepatenkintas, kad valiutos kurso nuostolis paskirstomas visuose pradinės sąskaitos faktūros išlaidų paskirstymuose, o ne viename kvite, norint įrašyti sąskaitas faktūras turėtų būti naudojami keli kvitai. Toliau pateikiamas pavyzdys, kaip į didžiąją knygą galima įvesti kelis kvitus, o ne naudoti vieną kvitą, kaip nurodyta šio pavyzdžio pradžioje.

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL002     | Tiekėjas           | 1001        | INV1            |           | 100,00     | DK          | 606300-001--       |
| GNJL003     | Tiekėjas           | 1001        | INV2            |           | 200,00     | DK          | 606300-002--       |

Dabar, kai apmokama INV2, pateikiamas toliau nurodytas įrašas. Atkreipkite dėmesį, kad valiutos kurso nuostolio finansinės dimensijos pateikiamos po susietųjų išlaidų finansinių dimensijų.

| Kvitas | Paskyra | Registravimo tipas   | Suma operacijos valiuta (EUR) | Suma apskaitos valiuta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Tiekėjo balansas     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bankas               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Valiutos kurso nuostolis | 0,00                                     | 2,00                                    |
| 14000056    | 200110-001- | Tiekėjo balansas     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Vienas kvitas balanso perkėlimams ir padengimo scenarijams
Du dažniausiai naudojami scenarijai, kai naudojamas vienas kvitas, kuriame yra keli klientai arba tiekėjai, apima balanso perkėlimus iš vieno kliento / tiekėjo kitam klientui / tiekėjui ir kliento bei tiekėjo, kurie yra ta pati organizacija, padengimą. Toliau pateiktuose dviejuose pavyzdžiuose nurodomas pageidaujamas šių scenarijų įvedimo būdas, kaip alternatyva jų įvedimui į vieną kvitą. 

*Balanso perkėlimas* yra vienas kvitas su keliais klientais, kurie įvesti siekiant perkelti balansą iš vieno kliento kitam klientui (taip pat tiekėjui). Šis scenarijus gali įvykti, kai atsakomybė apmokėti sąskaitą faktūrą perkeliama kitai šaliai, pavyzdžiui, kai antrinė įmonė perkelia atsakomybę pirminei įmonei. 

Šiame pavyzdyje įsivaizduojama, kad atliekamas pardavimas, kai klientui gali būti pritaikoma mokėjimo nuolaida, jeigu mokėjimas atliekamas per 10 dienų. Šiame pavyzdyje klientas naudojasi draudimo įmonės, kuri bus atsakinga už sąskaitos apmokėjimą, paslaugomis. Draudimo įmonė sistemoje nustatoma kaip antras klientas. Pradinio kliento balansas perkeliamas draudimo įmonei, kuris apmoka sąskaitą, pasinaudodama 2 % mokėjimo nuolaida, jei apmokama nuolaidos taikymo laikotarpiu. 

Įsivaizduokite, kad klientui ACME atliekamas toliau nurodytas pardavimas. Toliau nurodomi apskaitos įrašai atitinka pardavimą.

| DK sąskaita | Registravimo tipas | Debetas | Kreditas |
|--------------------|------------------|-----------|------------|
| 401100-002-023-    | Įplaukos          |           | 100        |
| 130100-002-        | Kliento balansas | 100       |            |

Po to vartotojas perkelia mokėtiną balansą iš ACME draudimo įmonei viename kvite gautinų sumų mokėjimo žurnale. Draudimo įmonė nustatyta kaip kliento draudimas.

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Klientas         | ACME        | Perkėlimas        |           | 100,00     | Klientas        | Draudimas          |

Atkreipkite dėmesį, kad pirmiau pateiktas įrašas yra viename kvite. Šiame kvite yra du kliento įrašai. Toliau pateikiamas kvitas sukuriamas užregistravus pirmiau pateiktą didžiosios knygos įrašą.

| Kvitas | Paskyra | Registravimo tipas | Suma operacijos valiuta |
|-------------|-------------|------------------|------------------------------------|
| ARPAYM001   | 130100-002- | Kliento balansas | 100,00                             |
| ARPAYM001   | 130100-002- | Kliento balansas | -100.00                            |

Po to, tarkime, kad iš draudimo kliento gaunate mokėjimą, kurio suma 98,00, ir pasirenkate padengti mokėjimą naudodami perkeliant balansą sukurta sąskaita faktūra. Tokiu atveju bus užregistruojamas toliau nurodytas kvitas. Gali būti tikimasi, kad sudengiant bus naudojamos finansinės dimensijos iš pradinės sąskaitos faktūros, bet tai neįmanoma, nes nėra draudimo kliento sąskaitos faktūros dokumento. Atkreipkite dėmesį, kad pagal numatytuosius nustatymus mokėjimo nuolaidoje nurodytos paskirstymo dimensijos atsiranda iš perkeliant sukurtos operacijos, o ne iš pradinės sąskaitos faktūros įplaukų sąskaitos. Numatytasis nustatymas taikomas dėl to, kad perkeliant balansus buvo naudojamas vienas kvitas.

| Kvitas | Paskyra | Registravimo tipas | Debetas | Kreditas |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM002   | 110110-002- | Bankas             | 98.00     |            |
| ARPAYM002   | 130100-002- | Kliento balansas |           | 98.00      |

Susijusiame mokėjimo nuolaidos kvite numatytoji finansinė dimensija paimama iš atliekant perkėlimą sukurtos kliento operacijos, nes perkėlimas turi daugiau negu vieną klientą.

| Kvitas | Paskyra | Registravimo tipas       | Debetas | Kreditas |
|-------------|-------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002- | Kliento mokėjimo nuolaida | 2,00      |            |
| ARP-00001   | 130100-002- | Kliento balansas       |           | 2,00       |

Jei vartotojas nepatenkintas numatytomis mokėjimo nuolaidos finansinėmis dimensijomis, įrašant balanso perkėlimą turėtų būti naudojamas ne vienas, o keli kvitai. Šis scenarijus turėtų būti atliekamas sukuriant kliento kredito pažymą, kurioje nurodoma, kad balansas perkeltas IŠ, ir debeto pažymą arba sąskaitą faktūrą, nurodant klientą, KURIAM perkeliamas balansas. Toliau pateiktame pavyzdyje parodyta, kaip perkeliant balansą mokėtinų sumų mokėjimo žurnale galima įvesti kelis kvitus užuot naudojus vieną kvitą, kaip parodyta ankstesniame pavyzdyje.

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Klientas         | ACME        |                 |           | 100,00     | DK          | 401100-002-023-    |
| ARPAYM002   | Klientas         | Draudimas   |                 | 100,00    |            | DK          | 401100-002-023-    |

Tai reiškia, kad kai draudimo klientas, naudodamas kvitą ARPAYM02, sumoka 98,00, bus naudojamos teisingos kvito ARPAYM002 didžiosios knygos sąskaitos įrašo finansinės dimensijos.

| Kvitas | Paskyra | Registravimo tipas | Debetas | Kreditas |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM003   | 110110-002- | Bankas             | 98.00     |            |
| ARPAYM003   | 130100-002  | Kliento balansas |           | 98.00      |

Susijusiame mokėjimo nuolaidos kvite finansinės dimensijos bus naudojamos iš ARPAYM002 kvite nurodytos korespondentinių įplaukų sąskaitos.

| Kvitas | Paskyra     | Registravimo tipas       | Debetas | Kreditas |
|-------------|-----------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002-023- | Kliento mokėjimo nuolaida | 2,00      |            |
| ARP-00001   | 130100-002-     | Kliento balansas       |           | 2,00       |

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Vienas kvitas su kelių klientų ir tiekėjų padengimu
Padengimas gali būti naudingas, kai organizacija perka ir parduoda tai pačiai įmonei. Užuot mokėjus tiekėjui sąskaitas faktūras ir laukus, kol bus apmokėtos kliento sąskaitos faktūros, tiekėjo ir kliento sąskaitos faktūros padengiamos. Padengimo operacija sudengiama naudojant neapmokėtus balansus. 

Tarkime, kad tiekėjas 1001 ir klientas US-008 yra ta pati įmonė, todėl jūsų organizacija nori padengti mokėtinus ir gautinus balansus prie mokant / gaunant likusį balansą. Tarkime, kad kliento įrašas skolingas 75,00 EUR, tiekėjo įrašas skolingas 100,00 EUR, ir tai reiškia, kad jūs norėtumėte padengti balansus ir mokėti tiekėjui tik 25,00 EUR. Arba tarkime, kad apskaitos valiuta yra USD. Šiuo atveju padengimo operacija įvedama viename mokėtinų sumų mokėjimo žurnalo kvite.

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| APPAYM001   | Tiekėjas           | 1001        | Užskaita         |  75,00    |            | Klientas        | US-008             |

Norint išvengti nepageidaujamų problemų su būsimais šios operacijos sudengimais, užuot naudojus vieną kvitą, norint įrašyti padengimo operaciją, į žurnalą reikėtų įvesti kelis kvitus. Atkreipkite dėmesį, kad kliento ir tiekėjo balansai kompensuojami naudojant vieną tarpuskaitos sąskaitą, kad nereikėtų naudoti vieno kvito, kuriame yra keli kliento ir tiekėjo balansai.

| Kvitas | Kodo tipas | Paskyra | aprašymas | Debetas | Kreditas | Užskaitos tipas | Korespondentinė sąskaita |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| 001         | Klientas         | US-008      |                 |           |  75,00     | DK          | 999999---          |
| 002         | Tiekėjas           | 1001        |                 |  75,00    |            | DK          | 999999---          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]