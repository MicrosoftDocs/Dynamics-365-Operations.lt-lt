---
title: Dokumentų, kuriuose yra prašymų duomenys, generavimas
description: Norėdami atlikti šios procedūros veiksmus, pirmiausia turite užbaigti procedūrą "ER Generuoti dokumentus su programos duomenų naujuoju (4 dalis – Modifikuoti formatą)".
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0f4fe5c948d1d6ea7c306a37d629c6e381dbd00
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290461"
---
# <a name="generate-documents-that-have-application-data"></a>Dokumentų, kuriuose yra prašymų duomenų, generavimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: dokumentų su programos duomenų naujinimu generavimas (4 dalis. Formato modifikavimas)“.



Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis. Šioje procedūroje vykdote ER formato konfigūraciją, kad sugeneruotumėte Intrastat ataskaitą ir atnaujintumėte programos duomenis ataskaitų proceso archyvavimo informacijai.



Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį. Prieš pradėdami įsitikinkite, kad šalies kontekstas DEMF įmonei yra BEL (Belgija).


## <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus
1. Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.
2. Spustelėkite skirtuką Numeracijos.

    Archyvuojami Intrastat ataskaitų kūrimo proceso informaciją, turime nustatyti kiekvieno archyvo, kurį sukūrėme, įrašus. Tam reikia konfigūruoti specialią numerių seką.  

3. Pasirinkite „Intrastat“ archyvo ID“ nuorodą.
4. Lauke Numeracijos kodas įveskite reikšmę.

    Lauke „Numerių sekos kodas“ įveskite arba pasirinkite vertę „Fore_2“.  

5. ResolveChanges Numerio sekos kodas.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

## <a name="run-modified-er-format"></a>Paleiskite pakeistą ER formatą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat (model)“.
3. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
4. Spustelėkite Vykdyti.
5. Lauke Įveskite failo pavadinimą įveskite „intrastat2.xml“.
6. Spustelėkite Gerai.

## <a name="review-er-format-executions-results"></a>Peržiūrėkite ER formato vykdymo rezultatus
Peržiūrėkite sugeneruotą XML failą.  
1. Uždarykite puslapį.
2. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.

    Atidarykite šią formą, kurioje yra Intrastat operacijos, kurios buvo įtrauktos sugeneruotą elektroninį dokumentą.  

3. Spustelėkite Intrastat archyvas.

    Kadangi įvykdyto ER formate dabar yra programos duomenų atnaujinimo parametrai, informacija apie užpildytą Intrastat ataskaitą suarchyvuota. Šioje formoje galite pamatyti sukurto archyvo antraštės įrašą.  

4. Spustelėkite Informacija.

    Šioje formoje galite pamatyti sukurto archyvo išsamią informaciją.  

5. Uždarykite puslapį.
6. Uždarykite puslapį.
7. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
