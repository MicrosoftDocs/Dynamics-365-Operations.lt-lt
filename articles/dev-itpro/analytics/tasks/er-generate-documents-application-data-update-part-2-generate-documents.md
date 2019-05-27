---
title: Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas
description: Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544523"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“.



Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą. Šios procedūros metu vykdoma ER importuota formato konfigūracija, sukurta pavyzdinei įmonei „Litware, Inc.“, kad būtų galima generuoti elektroninius dokumentus.



Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį. 



Prieš pradėdami pakeisti šalies kontekstą DEMF įmonei iš DEU (Vokietija) į BEL (Belgija). Spustelėkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai, kad atnaujintumėte šalies kodą juridinio subjekto DEMF pagrindiniame adrese. Paleiskite programą iš naujo.


## <a name="run-imported-er-format"></a>Paleiskite importuotą ER formatą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat (model)“.
3. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
4. Spustelėkite Vykdyti.
    * Paleiskite ER formato konfigūracijos juodraščio versiją, norėdami generuoti Intrastat ataskaitą.  
5. Lauke Įveskite failo pavadinimą įveskite „intrastat.xml“.
    * Nurodykite failo vardą.  
6. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą XML failą.  
7. Uždarykite puslapį.
8. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
    * Atidarykite šią formą, kad peržiūrėtumėte Intrastat operacijas, kurios yra įtrauktos sugeneruotą elektroninį dokumentą.  
9. Spustelėkite Intrastat archyvas.
    * Kadangi įvykdytame ER formate nėra jokių programos duomenų atnaujinimo parametrų, informacija apie užpildytą Intrastat ataskaitą nesuarchyvuota.  
10. Uždarykite puslapį.
11. Uždarykite puslapį.

