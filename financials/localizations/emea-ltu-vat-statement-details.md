---
title: PVM ataskaitos duomenys Lietuvai
description: "Šioje temoje aiškinama, kaip nustatyti PVM ataskaitą juridiniams asmenims Lietuvoje."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxReportVoucher, TaxTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266884
ms.assetid: 96122273-e9f8-40bf-ab2d-77875d029f9e
ms.search.region: Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: 99f2d9047537513d06d6cf5b8f7b463493c2eae1
ms.lasthandoff: 03/31/2017


---

# <a name="vat-statement-details-for-lithuania"></a>PVM ataskaitos duomenys Lietuvai

Šioje temoje aiškinama, kaip nustatyti PVM ataskaitą juridiniams asmenims Lietuvoje.

Šia tema apima šaliai/regionui būdingų informacija apie nustatymą, pridėtinės vertės mokestis (PVM) pažymos juridiniams asmenims Lietuvoje tik. Daugiau informacijos apie nustatymą PVM ataskaitas, ieškokite [PVM ataskaitų](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>PVM rinkėjų nustatymas
Generuoti PVM deklaraciją reikiamą formatą už atitinkamą mokesčių administratorius, turite nustatyti PVM rinkėjus ataskaitos maketą. Dėl į **PVM rinkėjus** p., be į **ataskaitos maketo** lauke, pasirinkite **Default**. Pasirinkite patį PVM rinkėjo PVM sudengimo laikotarpio, kuris bus naudojamas PVM kodų.

## <a name="set-up-sales-tax-reporting-codes"></a>Nustatyti PVM ataskaitų kodus
Čia pateikiamas pavyzdys, kad parodyti, kaip jūs galite naudoti PVM ataskaitų kodai kurti PVM ataskaitą. Šie PVM ataskaitų kodai gali būti sukurtas ir naudojamas su **ataskaitos nustatymas** FastTab, į **PVM kodus** puslapis.

| PVM ataskaitos kodas | aprašymas                                                           | Lauke pavadinimas, ataskaitos |
|--------------------------|-----------------------------------------------------------------------|------------------------|
| 11                       | Mokesčių bazės suma pardavimo apmokestinamiems pardavimo                                | E11                    |
| 12                       | Mokesčių bazės suma pardavimo apmokestinamiems pardavimo už 96 paragrafą               | E12                    |
| 13                       | Mokesčių bazės suma apmokestinamiems pardavimo                                  | E13                    |
| 14                       | Suvartojimo įmonės reikmėms                                  | E14                    |
| 15                       | Ilgalaikio turto gamyba                                                | E15                    |
| 16                       | Maržos sandorių, kurie turi specialias apmokestinimo schemos                   | E16                    |
| 17                       | Eksporto prekės (0 proc.)                                           | E17                    |
| 18                       | Pardavimo Europos Sąjungos (ES) PVM mokėtojams (0 proc.)                   | E18                    |
| 19                       | Kiti pardavimai, kurie turi 0 procentų PVM                                   | E19                    |
| 20                       | Ne apmokestinamiems pardavimo už Lietuvos ribų                          | E20                    |
| 21                       | Sumos prekėms, kurios įsigyjamos iš ES                        | E21                    |
| 22                       | Sumos prekėms, kurios įsigyjamos iš ES (trikampė prekyba)     | E22                    |
| 23                       | Paslaugų, kurios įsigyjamos iš užsienio šalyse/regionuose sumos  | E23                    |
| 24                       | Paslaugas, kurios yra įsigytos iš ES PVM mokėtojų suma.             | E24                    |
| 25                       | Nupirktų prekių ir paslaugų PVM suma                            | E25                    |
| 26                       | Sumokėtas importo PVM                                                       | E26                    |
| 27                       | Importo PVM, kuris bus išskaičiuoti mokesčių tarnyba kontroliuoja | E27                    |
| 29                       | Mokesčio suma pardavimų, kurie turi standartinį mokesčio tarifą                     | E29                    |
| 30                       | Mokesčių suma, kurių 9 procentų lengvatinis mokesčio tarifas         | E30                    |
| 31                       | Mokesčio suma pardavimo, kurios turi sumažintą akcizo tarifą 5 proc.         | E31                    |
| 32                       | Mokesčio suma už 95 punktą                                  | E32                    |
| 33                       | Mokesčio suma už 96 paragrafą                                  | E33                    |
| 34                       | Pardavimo PVM nuo prekių, kurios yra perkamos ES                       | E34                    |
| 35                       | Atskaitomas pirkimo ir importo PVM suma                             | E35                    |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Konfigūruoti elektroninė duomenų perdavimo modelis ir ataskaitų formos
Norėdami peržiūrėti arba pakeisti PVM ataskaitoje konfigūraciją, į **ataskaitų konfigūracijos** puslapyje, pasirinkite **PVM deklaracijos modelis**. Spustelėkite **dizaineris** peržiūrėti arba keisti modelį. Peržiūrėti arba keisti PVM ataskaitos formatą, kad **ataskaitų konfigūracijos** puslapyje, pasirinkite **PVM deklaracijos modelis**, ir tada spustelėkite **dizaineris**.

## <a name="generate-a-vat-statement"></a>Kurti PVM ataskaitą
Sukurti PVM XML failą, dėl to **PVM mokėjimus** puslapyje, pasirinkite vieną ar daugiau kvitus, o tada spustelėkite **eksporto PVM XML failą**.


