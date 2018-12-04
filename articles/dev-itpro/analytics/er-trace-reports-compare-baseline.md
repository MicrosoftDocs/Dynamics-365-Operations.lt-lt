---
title: "Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis"
description: "Šioje temoje pateikta informacija apie tai, kaip galima palyginti sugeneruotų ER ataskaitų rezultatus su bazinės ataskaitos vertėmis."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis

[!include[banner](../includes/banner.md)]

Galite sekti ER formatų, kuriais generuojami siunčiami elektroniniai dokumentai, rezultatus. Kai įjungtas sekimo generavimas (ER vartotojo parametras **Vykdyti derinimo režimu**), naujas sekimo įrašas ER formato vykdymo žurnale sugeneruojamas kiekvieną kartą, kai paleidžiama ER ataskaita. Ši išsami informacija saugoma kiekviename sugeneruojamame sekime:

- Visi įspėjimai, sugeneruoti naudojant tikrinimo taisykles
- Visos klaidos, sugeneruotos naudojant tikrinimo taisykles
- Visi sugeneruoti failai, saugomi kaip sekimo įrašo priedai

Galite išsaugoti bet kurio ER formato individualius bazinius programos failus. Failai laikomi baziniais failais, kai jie aprašo numatytus vykdomų ataskaitų rezultatus. Jei yra ER formato bazinis failas, paleistas įjungus sekimo generavimą, sekimo informacija saugo kartu su išsamia informacija, kuri buvo paminėta anksčiau, sugeneruoto elektroninio dokumento palyginimo su baziniu failu rezultatą. Vienu spustelėjimu galite gauti ir sugeneruotą elektroninį dokumentą, ir jo bazinį failą viename suglaudintame faile. Tada galite atlikti išsamų palyginimą naudodami išorinį įrankį, pvz., „Windiff“.

Galite įvertinti sekimą, analizuodami, ar sugeneruojami elektroniniai dokumentai apima numatytą turinį. Šį įvertinimą galite atlikti vartotojo priėmimo bandymų (UAT) aplinkoje, kai pakeistas pagrindinis kodas (pvz., kai perkėlėte į naują programos egzempliorių, įdiegėte karštųjų pataisų paketus arba įdiegėte kodų pakeitimus). Taip galite užtikrinti, kad vertinimas neturės įtakos naudojamų ER ataskaitų vykdymui. Daugelio ER ataskaitų vertinimą galima atlikti režimu be priežiūros.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **ER ataskaitų generavimas ir rezultatų palyginimas (1 dalis)** ir **ER ataskaitų generavimas ir rezultatų palyginimas (2 dalis)**, kurie yra verslo proceso **7.5.4.3 Tikrinti IT paslaugas ir sprendimus (10679)** dalis, juos galima atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684). Šie užduočių vedliai parodys jums ER sistemos konfigūravimo procesą, norint naudoti bazinius failus sugeneruotiems elektroniniams dokumentams įvertinti.

