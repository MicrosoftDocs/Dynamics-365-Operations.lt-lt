--- 
title: "Dokumentų generavimas elektroninėse ataskaitose (ER) su atnaujintais prašymų duomenimis"
description: "Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (4 dalis – modifikuoti formatą)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b2844621bf50a385ad1a4770c0df2d97623dc77a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Dokumentų generavimas elektroninėse ataskaitose (ER) su atnaujintais prašymų duomenimis

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


