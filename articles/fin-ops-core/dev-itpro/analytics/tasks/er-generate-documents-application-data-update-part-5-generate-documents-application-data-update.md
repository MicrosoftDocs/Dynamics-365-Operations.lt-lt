---
title: Dokumentų, kuriuose yra prašymų duomenys, generavimas
description: Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (4 dalis – modifikuoti formatą)“.
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
ms.openlocfilehash: 1d95feb3395c36f9cf8a23770dc3173377067d9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184881"
---
# <a name="generate-documents-that-have-application-data"></a>Dokumentų, kuriuose yra prašymų duomenys, generavimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (4 dalis: modifikuoti formatą)“.



Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis. Šioje procedūroje vykdote ER formato konfigūraciją, kad sugeneruotumėte Intrastat ataskaitą ir atnaujintumėte programos duomenis ataskaitų proceso archyvavimo informacijai.



Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį. Prieš pradėdami įsitikinkite, kad šalies kontekstas DEMF įmonei yra BEL (Belgija).


## <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus
1. Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.
2. Spustelėkite skirtuką Numeracijos.
    * Archyvuojami Intrastat ataskaitų kūrimo proceso informaciją, turime nustatyti kiekvieno archyvo, kurį sukūrėme, įrašus. Tam reikia konfigūruoti specialią numerių seką.  
3. Pasirinkite „Intrastat archyvo ID“ nuorodą.
4. Lauke Numeracijos kodas įveskite reikšmę.
    * Lauke „Numerių sekos kodas“ įveskite arba pasirinkite vertę „Fore_2“.  
5. ResolveChanges Numerio sekos kodas.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

## <a name="run-modified-er-format"></a>Paleiskite pakeistą ER formatą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat (model)“.
3. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
4. Spustelėkite Vykdyti.
5. Lauke Įveskite failo pavadinimą įveskite „intrastat2.xml“.
    * intrastat2.xml  
6. Spustelėkite GERAI.

## <a name="review-er-format-executions-results"></a>Peržiūrėkite ER formato vykdymo rezultatus
    * Peržiūrėkite sugeneruotą XML failą.  
1. Uždarykite puslapį.
2. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
    * Atidarykite šią formą, kurioje yra Intrastat operacijos, kurios buvo įtrauktos sugeneruotą elektroninį dokumentą.  
3. Spustelėkite Intrastat archyvas.
    * Kadangi įvykdyto ER formate dabar yra programos duomenų atnaujinimo parametrai, informacija apie užpildytą Intrastat ataskaitą suarchyvuota. Šioje formoje galite pamatyti sukurto archyvo antraštės įrašą.  
4. Spustelėkite Informacija.
    * Šioje formoje galite pamatyti sukurto archyvo išsamią informaciją.  
5. Uždarykite puslapį.
6. Uždarykite puslapį.
7. Uždarykite puslapį.
