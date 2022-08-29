---
title: PVM išrašo informacija, skirta Lietuvai
description: Šiame straipsnyje paaiškinama, kaip nustatyti PVM išrašą juridiniams subjektams Lietuvaje.
author: AdamTrukawka
ms.date: 06/20/2017
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
ms.openlocfilehash: 8464eb80ee57d1de62c9cadf8595b00d71e58e70
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285755"
---
# <a name="vat-statement-details-for-lithuania"></a>PVM išrašo informacija, skirta Lietuvai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti PVM išrašą juridiniams subjektams Lietuvaje.

Šiame straipsnyje pateikiama šaliai/regionui konkreti informacija apie pridėtinės vertės mokesčio (PVM) išrašo nustatymą tik Lietuvos juridiniams subjektams. Norėdami gauti daugiau informacijos apie PVM išrašų sąranką, žr. [Europos PVM ataskaitos](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>PVM institucijų nustatymas
Norėdami generuoti PVM deklaraciją formatu, kurio reikalauja atitinkamas mokesčių rinkėjas, turite nustatyti PVM rinkėjo ataskaitos maketą. Puslapio **PVM rinkėjai** lauke **Ataskaitos maketas** pasirinkite **Numatytasis**. Pasirinkite tą patį PVM sudengimo laikotarpio PVM rinkėją, kuris bus naudojamas PVM koduose.

## <a name="set-up-sales-tax-reporting-codes"></a>Nustatyti PVM ataskaitų kodus
Čia pateikiamas pavyzdys, kuris parodo, kaip PVM ataskaitų kodus galite naudoti PVM išrašui generuoti. Toliau pateiktus PVM ataskaitų kodus galima kurti ir naudoti puslapio **PVM kodai** „FastTab‟ **Ataskaitų sąranka**.

| PVM ataskaitos kodas | aprašymas                                                           | Ataskaitos dėžės pavadinimas |
|--------------------------|-----------------------------------------------------------------------|------------------------|
| 11                       | Apmokestinamo pardavimo pagrindinio mokesčio suma                                | E11                    |
| 12                       | Apmokestinamo pardavimo pagrindinio mokesčio suma pagal 96 straipsnį               | E12                    |
| 13                       | Neapmokestinamo pardavimo pagrindinio mokesčio suma                                  | E13                    |
| 14                       | Suvartojimas įmonės poreikiams                                  | E14                    |
| 15                       | Ilgalaikio turto gamyba                                                | E15                    |
| 16                       | Sandorių, kuriems taikoma spec. apmokestinimo schema, marža                   | E16                    |
| 17                       | Prekių eksportas (0 proc.)                                           | E17                    |
| 18                       | Pardavimas Europos Sąjungos (ES) PVM mokėtojams (0 proc.)                   | E18                    |
| 19                       | Kitas pardavimas, kuriam taikomas 0 proc. PVM                                   | E19                    |
| 20                       | Neapmokestinamas pardavimas už Lietuvos ribų                          | E20                    |
| 21                       | ES šalyse nupirktų prekių suma                        | E21                    |
| 22                       | ES šalyse nupirktų prekių suma (trišalė prekyba)     | E22                    |
| 23                       | Užsienio šalyse / regionuose nupirktų paslaugų suma  | E23                    |
| 24                       | Iš ES PVM mokėtojų nupirktų paslaugų suma             | E24                    |
| 25                       | Nupirktų prekių ir paslaugų PVM suma                            | E25                    |
| 26                       | Sumokėtas importo PVM                                                       | E26                    |
| 27                       | Importo PVM, kurio atskaitymą kontroliuoja mokesčių tarnyba | E27                    |
| 29                       | Pardavimo, kuriam taikomas standartinis mokesčio tarifas, mokesčių suma                     | E29                    |
| 30                       | Pardavimo, kuriam taikomas sumažintas 9 proc. mokesčio tarifas, mokesčių suma         | E30                    |
| 31                       | Pardavimo, kuriam taikomas sumažintas 5 proc. mokesčio tarifas, mokesčių suma         | E31                    |
| 32                       | Pardavimo mokesčių suma pagal 95 straipsnį                                  | E32                    |
| 33                       | Pardavimo mokesčių suma pagal 96 straipsnį                                  | E33                    |
| 34                       | ES šalyse nupirktų prekių pardavimo PVM                       | E34                    |
| 35                       | Atskaitomo pirkimo ir importo PVM suma                             | E35                    |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Elektroninių ataskaitų modelio ir ataskaitos formato konfigūravimas
Norėdami peržiūrėti arba keisti PVM išrašo konfigūraciją, puslapyje **Ataskaitų konfigūracijos** pasirinkite **PVM deklaracijos modelis**. Tada spustelėkite **Dizaino įrankis**, kad peržiūrėtumėte arba pakeistumėte modelį. Norėdami peržiūrėti arba keisti PVM išrašo formatą, puslapyje **Ataskaitų konfigūracijos** pasirinkite **PVM deklaracijos modelis**, o tada spustelėkite **Dizaino įrankis**.

## <a name="generate-a-vat-statement"></a>PVM išrašo generavimas
Norėdami generuoti PVM XML failą, puslapyje **PVM mokėjimai** pasirinkite vieną ar daugiau kvitų, o tada spustelėkite **Eksportuoti PVM XML failą**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
