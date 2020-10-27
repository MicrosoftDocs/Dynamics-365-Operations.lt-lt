---
title: Kainos modeliavimas
description: Šiame straipsnyje pateikta informacija apie pasiūlymų kainos modeliavimą. Kainų modeliavimas padeda įvertinti lengvatų poveikį būsimoms pardavimo kainoms pasiūlymo proceso metu prieš pritaikant tam tikrą kainą.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 336fb51dc5fb66dfbe14091d121e0a4471b9662b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978898"
---
# <a name="price-simulation"></a>Kainos modeliavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie pasiūlymų kainos modeliavimą. Kainų modeliavimas padeda įvertinti lengvatų poveikį būsimoms pardavimo kainoms pasiūlymo proceso metu prieš pritaikant tam tikrą kainą.

Pasiūlymo kainos modeliavimas parodo naują bendrąją sumą remiantis nauja siūloma kaina. Kainų modeliavimas taip pat gali parodyti naują konkrečios eilutės, sukurtos esamame pasiūlyme, sumą. Kainų modeliavimą galite įvesti, o taikyti vėliau. Arba galite naudoti pradinį pasiūlymą be kainos modeliavimo ir atlikti daugiau keitimų dirbant su klientu pardavimų procese.  

Kainų modeliavimas nekeičia pasiūlymo kainos. Jei kainų modeliavimas taikomas visam pasiūlymui, jis laikomas specialia nuolaida pasiūlymo antraštėje. Jei kainų modeliavimas taikomas konkrečioms prekėms, jis laikomas specialia nuolaida pasiūlymo eilutėse. Vieneto pardavimo kaina sukurtoje pasiūlymo eilutėje nesikeičia pritaikius kainos modeliavimą. Vietoje to, taikomas nuolaidos procentas, atitinkantis pasiūlymo eilutės kainos sumažinimą. Kai pritaikomas kainų modeliavimas, vieneto pardavimo kaina ir nuolaidos procentas yra perkeliami į pasiūlymo eilutę arba pasiūlymo antraštę.  

>[Pastaba!] Atliekant kainos modeliavimą, modeliui kurti naudojama tik dabartinė pardavimo valiuta. Tačiau, kai peržiūrite bendrąsias pasiūlymo sumas, matote įmonės valiutos ir pardavimo valiutos derinį.  

Papildomos prekės, pridėtos į pasiūlymo eilutes, gali paleisti eilutės nuolaidas arba kelių eilučių nuolaidas. Jos taip pat gali paleisti bendrąsias nuolaidas, keičiančias pasiūlymo eilučių ir visos nuolaidos pelningumo maržas ir pelningumo koeficientą.  

Galite atlikti kelių kainų modeliavimą ir taip sekti kainos korekcijų, vykdomų atsižvelgiant į pasiūlymo tikslus, efektus. Vykdydami šiuos modeliavimus, galite koreguoti pasiūlymo bendrąją kainą arba vienos ar daugiau konkrečių pasiūlymo eilučių kainą ir tada pritaikyti modeliavimą, kuris geriausiai padėtų uždaryti pardavimą.  

Kurdami pasiūlymą, galite nustatyti įspėjimą. Toliau pateikti keli būdai, kaip įspėjimai naudojami.

-   Jie jus gali informuoti apie organizacijos pasiūlymų būseną.
-   Jie gali suaktyvinti konkretaus pasiūlymo peržiūrą arba informuoti, kai viršijamas nuolaidos limitas.

## <a name="price-simulation-and-discounts"></a>Kainų modeliavimas ir nuolaidos
Siekdami garantuoti, kad nuolaidos ir kainos būtų apskaičiuotos teisingai, vykdydami kainų modeliavimą pagal pasiūlymus, kuriems taikoma nuolaida, jam skirkite ypatingą dėmesį. Kadangi visi kainų modeliavimai yra laikomi specialiomis nuolaidomis aktyvioje pasiūlymo eilutėje arba visame pasiūlyme, turite stebėti nuolaidų skirtumus.

### <a name="types-of-discounts-in-trade-agreements"></a>Prekybos sutartyse esančių nuolaidų tipai

Tiekimo grandinės valdymo prekybos sutartyse gali būti keturių tipų kainų nuolaidos. Šios nuolaidos gali būti nustatytos skirtingoms prekėms, klientams ar prekių grupėms ir jos gali būti apribotos data. Siekiant išvengti skaičiavimo klaidų, vykdant kainų modeliavimą reikia atsižvelgti į prekybos sutartis. Toliau pateikti keturi prekybos sutartyse esančių nuolaidų tipai.

-   **Pardavimo kaina**– gali būti nurodytos kelios prekių pardavimo kainos. Kai sukuriamos pasiūlymo eilutės, programa ieško teisingos prekės pardavimo kainos ir ją perkelia į pasiūlymo eilutes. Todėl prekybos sutartis, kurioje yra tokia nuolaida, neturi įtakos kainų modeliavimui. Pardavimo kaina, kuri naudojama pasiūlymo eilutėje, atspindi prekybos sutartį.
-   **Eilutės nuolaida** – pagal užsakytą kiekį nurodomos specialios prekių nuolaidos. Prieš vykdant kainų modeliavimą, eilučių sumos paprastai sumažinamos pagal eilutės nuolaidą. Todėl prekybos sutartis, kurioje yra tokia nuolaida, turi įtakos kainų modeliavimui.
-   **Kelių eilučių nuolaida** – jei bendras kiekis viršija apibrėžtą ribą, iš anksto apibrėžti užsakytų prekių deriniai suaktyvina nuolaidą visam užsakymui. Prieš vykdant kainų modeliavimą, eilučių sumos paprastai sumažinamos pagal eilutės nuolaidą. Todėl prekybos sutartis, kurioje yra tokia nuolaida, turi įtakos kainų modeliavimui.
-   **Bendra nuolaida** – jei bendrosios sumos viršija apibrėžtą ribą, iš anksto apibrėžtos užsakytos prekės suaktyvina nuolaidą visam užsakymui. Bendrąją nuolaidą generuoja pasiūlymo eilutės. Tačiau kadangi bendroji nuolaida pasiūlymui taikoma kaip nuolaida, ji sumažina bendrąją pasiūlymo sumą. Todėl prekybos sutartis, kurioje yra tokia nuolaida, turi įtakos kainų modeliavimui.

### <a name="quotation-lines-and-trade-agreements"></a>Pasiūlymo eilutės ir prekybos sutartys

Kai kuriate arba koreguojate pasiūlymo eilutę, eilutės nuolaidos apskaičiuojamos automatiškai. Pagal prekybos sutartį randama aktuali prekės pardavimo kaina.

## <a name="price-simulation-examples"></a>Kainos modeliavimo pavyzdžiai
Šiuose pavyzdžiuose pateikiamas kainų modeliavimo naudojimas, skirtas pasiūlymų antraštėms ir atskiroms eilučių prekėms.

### <a name="price-simulation-for-quotation-headers"></a>Pasiūlymų antraščių kainos modeliavimas

Kuriate pasiūlymą, kuriame yra tokios eilutės:

-   10 prekės BR-12 vienetų (vieneto savikaina: 9,52 USD, vieneto pardavimo kaina: 15,32 USD).
-   12 prekės BR-14 vienetų (vieneto savikaina: 7,48 USD, vieneto pardavimo kaina: 13,75 USD).

Lentelėje pateiktos pasiūlymo eilutės.

|                            | Skaičiavimas                          | Rezultatas   |
|----------------------------|--------------------------------------|----------|
| Pardavimo kiekis             | 10 vienetų + 12 vienetų                  | 22 vienetai |
| Pardavimo vertė USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Išlaidų vertė USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Kontribucijos marža USD | 318,20 – 184,96                      | 133,24   |
| Pelningumo koeficientas         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87%   |

Galite vykdyti kainos modeliavimą ir taikyti 15 procentų bendrą nuolaidą visam pasiūlymui ar pasiūlymo antraštei. Lentelėje pateiktos naujos pasiūlymo bendrosios sumos po kainos modeliavimo vykdymo.

|                                                      | Skaičiavimas                               | Rezultatas   |
|------------------------------------------------------|-------------------------------------------|----------|
| Pardavimo kiekis                                       | 10 vienetų + 12 vienetų                       | 22 vienetai |
| Senoji pardavimo vertė USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Senoji išlaidų vertė USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Senoji kontribucijos marža USD                       | 318,20 – 184,96                           | 133,24   |
| Senasis įnašo koeficientas                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87%   |
| 15 procentų bendros nuolaidos kainos modeliavimas USD | (15 × 318,2) ÷ 100                        | 47,73    |
| Naujoji pardavimo vertė USD                               | 318,20 – 47,73                            | 270,47   |
| Naujoji kontribucijos marža USD                       | 270,47 – 184,96                           | 85,51    |
| Naujas pelningumo koeficientas                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61%   |

### <a name="price-simulation-for-single-line-items"></a>Atskirų eilučių elementų kainų modeliavimas

Kuriate pasiūlymą, kuriame yra tokios eilutės:

-   10 prekės BR-12 vienetų (vieneto savikaina: 9,52 USD, vieneto pardavimo kaina: 15,32 USD).
-   12 prekės BR-14 vienetų (vieneto savikaina: 7,48 USD, vieneto pardavimo kaina: 13,75 USD).

Lentelėje pateiktos pasiūlymo eilutės.

|                                      | Skaičiavimas                          | Rezultatas   |
|--------------------------------------|--------------------------------------|----------|
| Pardavimo kiekis                       | 10 vienetų + 12 vienetų                  | 22 vienetai |
| Pardavimo vertė USD už BR-12         | 10 × 15,32                           | 153,20   |
| Pardavimo vertė USD už BR-14         | 12 × 13,75                           | 165,00   |
| Išlaidų vertė USD už BR-12          | 10 × 9,52                            | 95,20    |
| Išlaidų vertė USD už BR-14          | 12 × 7,48                            | 89,76    |
| Kontribucijos marža USD už BR-12 | 153,20 – 95,20                       | 58,00    |
| Kontribucijos marža USD už BR-14 | 165,00 – 89,76                       | 75,24    |
| Kontribucijos koeficientas USD už BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Kontribucijos koeficientas USD už BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Bendra pardavimo vertė USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Bendra išlaidų vertė USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Bendra kontribucijos marža USD     | 318,20 – 184,96                      | 133,24   |
| Bendras įnašo koeficientas             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87%   |

Vykdote kainos modeliavimą ir taikote 10 procentų bendrą nuolaidą BR-12 vienetams. Lentelėje pateiktos naujos pasiūlymo bendrosios sumos po atskiro eilutės elemento kainos modeliavimo vykdymo.

|                                                   | Skaičiavimas                             | Rezultatas   |
|---------------------------------------------------|-----------------------------------------|----------|
| Pardavimo kiekis                                    | 10 vienetų + 12 vienetų                     | 22 vienetai |
| Senoji pardavimo vertė USD už BR-12                  | 10 × 15,32                              | 153,20   |
| Kainos modeliavimas, 10 procentų nuolaida BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Naujoji pardavimo vertė USD už BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Pardavimo vertė USD už BR-14                      | 12 × 13,75                              | 165,00   |
| Išlaidų vertė USD už BR-12                       | 10 × 9,52                               | 95,20    |
| Išlaidų vertė USD už BR-14                       | 12 × 7,48                               | 89,76    |
| Naujoji kontribucijos marža USD už BR-12          | 137,88 – 95,20                          | 42,68    |
| Kontribucijos marža USD už BR-14              | 165,00 – 89,76                          | 75,24    |
| Naujasis kontribucijos koeficientas USD už BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Kontribucijos koeficientas USD už BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Naujoji bendra pardavimo vertė USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Bendra išlaidų vertė USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Naujoji bendra kontribucijos marža USD              | 302,88 – 184,96                         | 117,92   |
| Naujas bendras pelningumo koeficientas                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93 %   |

Kainų modeliavimas paveikia tik tą eilutę, kuriai jis taikomas, ir sumažina bendrąsias tos eilutės sumas.



