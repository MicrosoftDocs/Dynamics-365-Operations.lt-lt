---
title: Pagrindinių tarifų nustatymas
description: Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRouteWorkbench, TMSRateMaster, TMSRateBaseType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d71aa15f8cec532980f412ff1cb48e142c4cb1
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016475"
---
# <a name="set-up-rate-masters"></a>Pagrindinių tarifų nustatymas

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą. Pagrindinius tarifus paprastai nustato logistikos vadovas atsižvelgdamas į su vežėjais pasirašytas sutartis. Šiame scenarijuje nustatysite pagrindinį tarifą oro vežėjui. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="set-up-rate-master"></a>Nustatyti pagrindinį tarifą
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Pagrindinis tarifas.
2. Spustelėkite Naujas.
3. Lauke „Pagrindinis tarifas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke „Vertinimo metaduomenų ID“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Vertinimo metaduomenų ID nulemia pagrindiniam tarifui reikalingus duomenis, nes jis apibrėžia metaduomenis, kurie skirti šį pagrindinį tarifą naudojančiam TMS mechanizmui.  
6. Šiam pavyzdžiui pasirinkite parinktį P2P
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Spustelėkite Įrašyti.

## <a name="set-up-rate-base"></a>Nustatyti tarifo pagrindą
1. Spustelėkite „Tarifo pagrindas“.
    * Tarifo pagrindas nulemia vežėjo tarifą ir gali būti naudojamas tarifų struktūrai nustatyti, nes jis nustato tarifų ribinius taškus, apibrėžtus bendrosiose ribose.  
2. Spustelėkite Naujas.
3. Lauke „Tarifo pagrindas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke „Bendrosios ribos“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti. Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.  
6. Šiam pavyzdžiui naudoti svorį
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Perjunkite skyriaus „Išsami informacija“ išplėtimą.
9. Spustelėkite Naujas.
10. Lauke „Pašto kodas atidavimui iš“ įveskite „30301“.
11. Lauke „Pašto kodas atidavimui į“ įveskite „30318“.
12. Lauke „Atidavimo šalis, regionas“ įveskite „JAV“.
13. Lauke „<1,00 Lbs“ įveskite „100“.
    * Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 1 svaras.  
14. Lauke „< 5,00 Lbs“ įveskite „300“.
    * Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 5 svarai.  
15. Lauke „< 20,00 Lbs“ įveskite „500“.
    * Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 20 svarų.  
16. Lauke „< 100,00 Lbs“ įveskite „1000“.
    * Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 100 svarų.  
17. Lauke „< 1.000,00 Lbs“ įveskite „3000“.
    * Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 1000 svarų.  
18. Spustelėkite Įrašyti.
19. Uždarykite puslapį.

## <a name="assign-rate-base"></a>Priskirti tarifo pagrindą
1. Perjunkite skyriaus „Tarifo pagrindo priskyrimai“ išplėtimą.
2. Spustelėkite Naujas.
    * Kiekvienam pagrindiniam tarifui galite priskirti keletą tarifų pagrindų. Tai sudaro galimybę kiekvienam vežėjui sukurti keletą skirtingų kainos apvalinimo taisyklių, atsižvelgiant į paskirties vietas, paslaugas ar skirtingus tarifų pagrindus. Šioje procedūroje sukursite tik vieną tarifo pagrindo priskyrimą.  
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke „Tarifo pagrindas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke „Paslauga“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke „Paėmimo pašto kodas“ įveskite „98052“.
    * Nurodykite, nuo kurio pašto kodo galios šis tarifo pagrindo priskyrimas.    
10. Lauke „Paėmimo šalis, regionas“ įveskite „JAV“.
11. Spustelėkite Įrašyti.

