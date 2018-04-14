---
title: "Paketinis įspėjimų vykdymas"
description: "Šioje temoje pateikiama informacija apie paketinį įspėjimų vykdymą „Microsoft Dynamics 365 for Finance and Operations“."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: f4c874c148dc10ac658f659896009981962a5802
ms.contentlocale: lt-lt
ms.lasthandoff: 03/23/2018

---

# <a name="batch-processing-for-alerts"></a>Paketinis įspėjimų vykdymas
[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

Įspėjimai apdorojami naudojant paketinio vykdymo funkciją programoje „Microsoft Dynamics 365 for Finance and Operations“. Turite nustatyti paketinį vykdymą, kad įspėjimai būtų pateikti.

„Finance and Operations“ palaiko dviejų tipų įvykius.

- Įvykiai, kuriuos suaktyvino pakeitimais pagrįsti įvykiai. Šie įvykiai taip pat yra vadinami kūrimo / naikinimo ir naujinimo įvykiais.
- Įvykius, kuriuos suaktyvino termino datos.

Galite nustatyti kiekvieno tipo įvykių paketinį vykdymą.
        
## <a name="batch-processing-for-change-based-events"></a>Pakeitimais pagrįstų įvykių paketinis vykdymas
„Finance and Operations“ perskaito visus pakeitimais pagrįstus įvykius, kurie įvyko po paskutinio paketinio vykdymo. Pakeitimais pagrįstų įvykiai apima laukų atnaujinimus, įrašų panaikinimą ir įrašų sukūrimą. Šie įvykiai yra lyginami su įspėjimo taisyklėse nustatytomis sąlygomis. Kai įvykis sutampa su taisyklės sąlygomis, paketinis vykdymas generuoja įspėjimą.

### <a name="frequency-for-change-based-events"></a>Pakeitimais pagrįstų įvykių dažnumas
Galite nustatyti pakeitimais pagrįstų įvykių paketinę užduotį, kuri įvykį apdoroja tuoj po to, kai sistema pakeitimą užregistruoja. Jei nustatysite paketinę užduotį pasikartoti dažniau, įvykus pasikeitimui vartotojai gaus įspėjimus anksčiau. Tačiau labai dažnas paketinis vykdymas gali neigiamai paveikti sistemos našumą.

Kita vertus, paketinė užduotis, kuri kartojasi retai ir yra suplanuota tuo laiku, kai sistemos apkrovimas yra mažas, gali padidinti sistemos našumą. Tačiau žemo dažnio paketinis vykdymas gali neatitikti vartotojų poreikio laiku gauti įspėjimus.

Todėl nustatydami pakeitimais pagrįstų įvykių paketinio vykdymo dažnumą pasistenkite išlaikyti pusiausvyrą tarp įspėjimų siuntimo laiku ir visos sistemos našumo. Kuo daugiau vartotojų kuria įspėjimo taisykles, tuo šis klausimas svarbesnis. Dažnumas neturi poveikio apdorotinų įvykių skaičiui. Tačiau, jei daugiau vartotojų kuria taisykles, reikia atlikti daugiau patikrinimų. Tokio tipo duomenų mainai gali paveikti sistemos našumą.

#### <a name="the-risks-of-low-batch-frequency"></a>Reto paketinio vykdymo pavojai
Jei nustatysite, kad pakeitimais pagrįstų įvykių paketinis vykdymas būtų atliekamas retai, įspėjimų taisyklių sąlygas atitinkantys duomenys pasikeičia prieš prasidedant paketiniam vykdymui. Todėl įspėjimai gali būti neteikiami.

Pavyzdžiui, nustatoma, kad įspėjimo taisyklė suaktyvins įspėjimą, kai įvyksta **kliento kontaktinės informacijos pakeitimas**, o jos sąlyga yra **klientas = BB**. Kitaip tariant, kai pasikeičia BB kliento kontaktinė informacija, užregistruojamas įvykis. Tačiau paketinio vykdymo sistema nustatyta taip, kad paketinis vykdymas vyksta rečiau nei įvedami duomenys. Jei kliento pavadinimas pasikeičia iš **BB** į **AA** prieš apdorojant įvykį, duomenų bazėje esantys duomenys nebeatitinka taisyklės sąlygos **klientas = BB**. Todėl galiausiai apdorojus įvykį, įspėjimas negeneruojamas.

### <a name="set-up-processing-for-change-based-alerts"></a>Įspėjimo dėl pakeitimų apdorojimo nustatymas
1. Pasirinkite **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Įspėjimai** &gt; **Keitimais pagrįsti įspėjimai**.
2. Dialogo lange **Keitimais pagrįsti įspėjimai** įveskite atitinkamą informaciją.

## <a name="batch-processing-for-due-date-events"></a>Termino įvykių paketinis vykdymas
„Finance and Operations“ aptinka visus įvykius, kuriuos suaktyvina terminai, ir šie įvykiai yra lyginami su įspėjimų taisyklėse nustatytomis sąlygomis. Kai įvykis sutampa su taisyklės sąlygomis, paketinis vykdymas generuoja įspėjimą.

### <a name="frequency-for-due-date-events"></a>Termino įvykių dažnumas
Galite nustatyti terminų paketines užduotis, kurios vykdomos naktį arba tam tikru dienos metu, kad būtų išlaikyta sistemos apkrovos pusiausvyra. Rekomenduojame nustatyti paketinę užduotį, kad vykdymas vyktų bent vieną kartą per dieną. Jei įspėjimai turėtų būti siunčiami kaip įmanoma anksčiau, nustatykite, kad paketinis vykdymas turėtų būti atliktas iš karto po to, kai pasikeičia sistemos data. Jei norite generuoti įspėjimus dėl termino įvykių, kurie įvyko po to, kai paketinė užduotis apdorojo įspėjimus, tą pačią dieną galite dar kartą vykdyti paketinę užduotį.

Pavyzdžiui, paketinė užduotis buvo vykdyta konkrečią dieną. Tada sukuriate pirkimo užsakymą, kurio termino data turėtų suaktyvinti įspėjimą tą pačią dieną. Norėdami gauti įspėjimą tą pačią dieną, turite vykdyti paketinę užduotį dar kartą po to, kai sukuriamas pirkimo užsakymas. Tačiau, jei tą dieną paketinės užduoties dar kartą nevykdysite, kitos dienos paketinė užduotis aptiks visus ankstesnių dienų neapdorotus termino įvykius.

> [!NOTE]
> Net jei paketinis vykdymas paleidžiamas kelis kartus per dieną, to paties termino ir tų pačių sąlygų įspėjimų dublikatai negeneruojami. Generuojami įspėjimai, skirti tik toms datoms, kurios praėjo dėl sistemos pakeitimų, įvykusių po paskutinio paketinės užduoties vykdymo.

### <a name="batch-processing-window"></a>Paketinio vykdymo langas
Įmonės įspėjimų taisyklių apdorojimą galima sustabdyti dėl kelių priežasčių. Tai gali būti atostogos, sistemos klaidos arba kitos priežastys, dėl kurių tam tikrą laiką paketinės užduotys nevykdomos.

Jei norite, kad termino įspėjimai netaptų pasenę, nes kelias dienas nebuvo vykdoma paketinė užduotis, galite nustatyti paketinio vykdymo langą. Paketinio vykdymo langą galima naudoti norint neleisti paketinę užduotį vykdyti nurodytą dienų skaičių.

Jei nustatysite paketinio vykdymo langą, įspėjimas bus siunčiamas, kai apdorojama įspėjimo taisyklė, net jei įspėjimas viršija termino kriterijuose nustatytą laiko apribojimą. Įspėjimas toliau siunčiamas tol, kol tęsiasi šiuo laiko apribojimu apibrėžtas laikotarpis ir paketinio vykdymo langas. Tačiau, kai laiko apribojimu apibrėžtas laikotarpis ir paketinio vykdymo langas baigiasi, įspėjimas nebesiunčiamas.

### <a name="set-up-processing-for-due-date-alerts"></a>Įspėjimo dėl termino apdorojimo nustatymas
1. Pasirinkite **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Įspėjimai** &gt; **Termino įspėjimai**.
2. Dialogo lange **Termino įspėjimai** įveskite atitinkamą informaciją.

