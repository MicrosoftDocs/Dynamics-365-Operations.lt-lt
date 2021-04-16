---
title: Paketinis įspėjimų apdorojimas
description: Šioje temoje pateikiama informacija apie paketinį įspėjimų vykdymą.
author: RichdiMSFT
ms.date: 09/10/2010
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 471e7d32e3507fef7765adda105f203cb898346d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749881"
---
# <a name="batch-processing-of-alerts"></a>Paketinis įspėjimų apdorojimas

[!include [banner](../includes/banner.md)]

Įspėjimai apdorojami naudojant paketinio vykdymo funkciją. Turite nustatyti paketinį vykdymą prieš procesą ir įspėjimų pateikimą.

Paketinio vykdymo funkcijos palaiko dviejų tipų įvykius:

- Įvykiai, suaktyvinami dėl pakeitimais pagrįstų įvykių. Šie įvykiai taip pat yra vadinami kūrimo / naikinimo ir naujinimo įvykiais.
- Įvykiai, suaktyvinami dėl terminų.

Galite nustatyti kiekvieno tipo įvykių paketinį vykdymą.

## <a name="batch-processing-for-change-based-events"></a>Pakeitimais pagrįstų įvykių paketinis vykdymas

Sistema perskaito visus pakeitimais pagrįstus įvykius, kurie įvyko po paskutinio paketinio vykdymo. Pakeitimais pagrįstų įvykiai apima laukų atnaujinimus, įrašų panaikinimą ir įrašų sukūrimą. Šie įvykiai yra lyginami su sąlygomis, kurias nustatėte įspėjimo taisyklėse. Kai įvykis sutampa su taisyklės sąlygomis, paketinis vykdymas generuoja įspėjimą.

### <a name="frequency-for-change-based-events"></a>Pakeitimais pagrįstų įvykių dažnumas

Galite nustatyti pakeitimais pagrįstų įvykių paketinę užduotį, kuri įvykį apdoroja tuoj po to, kai sistema užregistruoja įvykį. Jei nustatysite paketinę užduotį pasikartoti dažniau, įvykus pasikeitimui vartotojai gaus įspėjimus anksčiau. Tačiau labai dažnas paketinis vykdymas gali neigiamai paveikti sistemos našumą.

Kita vertus, paketinė užduotis, kuri kartojasi retai ir kurią suplanuojate, kai sistemos apkrovimas yra mažas, gali padidinti sistemos našumą. Tačiau žemo dažnio paketinis vykdymas gali neatitikti vartotojų poreikio laiku gauti įspėjimus.

Todėl nustatydami pakeitimais pagrįstų įvykių paketinio vykdymo dažnumą pasistenkite išlaikyti pusiausvyrą tarp įspėjimų siuntimo laiku ir visos sistemos našumo. Kuo daugiau vartotojų kuria įspėjimo taisykles, tuo šis klausimas svarbesnis. Dažnumas neturi poveikio įvykių, kuriuos apdoroja sistema, skaičiui. Tačiau, jei daugiau vartotojų kuria taisykles, procese atliekama daugiau patikrinimų. Tokio tipo duomenų mainai gali paveikti sistemos našumą.

#### <a name="the-risks-of-low-batch-frequency"></a>Reto paketinio vykdymo pavojai

Jei nustatysite, kad pakeitimais pagrįstų įvykių paketinis vykdymas būtų atliekamas retai, įspėjimų taisyklių sąlygas atitinkantys duomenys gali pasikeisti prieš vykdymą. Todėl įspėjimai gali būti neteikiami.

Pavyzdžiui, sukuriate suaktyvinamą įspėjimą, kai įvykis yra **kliento kontaktinės informacijos pakeitimas** ir jo sąlyga yra **klientas = BB**. Kitaip tariant, kai pasikeičia BB kliento kontaktinė informacija, procese užregistruojamas įvykis. Tačiau paketinio vykdymo sistema nustatyta taip, kad paketinis vykdymas vyksta rečiau nei įvedami duomenys. Jei kliento pavadinimas pakeičiamas iš **„BB”** į **„AA”** prieš apdorojant įvykį, duomenų bazėje esantys duomenys nebeatitinka taisyklės sąlygos **klientas = BB**. Todėl galiausiai apdorojus įvykį, įspėjimas negeneruojamas.

### <a name="set-up-processing-for-change-based-alerts"></a>Įspėjimo dėl pakeitimų apdorojimo nustatymas

1. Pasirinkite **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Įspėjimai** &gt; **Keitimais pagrįsti įspėjimai**.
2. Dialogo lange **Keitimais pagrįsti įspėjimai** įveskite atitinkamą informaciją.

## <a name="batch-processing-for-due-date-events"></a>Termino įvykių paketinis vykdymas

Sistema aptinka visus įvykius, kuriuos suaktyvina terminai, ir šie įvykiai yra lyginami su įspėjimų taisyklėse nustatytomis sąlygomis. Kai įvykis sutampa su taisyklės sąlygomis, paketinis vykdymas generuoja įspėjimą.

### <a name="frequency-for-due-date-events"></a>Termino įvykių dažnumas

Galite nustatyti terminų paketines užduotis, kurios vykdomos naktį arba tam tikru dienos metu, kad būtų išlaikyta sistemos apkrovos pusiausvyra. Rekomenduojame nustatyti paketinę užduotį, kad vykdymas vyktų bent vieną kartą per dieną. Jei įspėjimai turėtų būti siunčiami kaip įmanoma anksčiau, nustatykite, kad paketinis vykdymas turėtų būti atliktas iš karto po to, kai pakeičiama sistemos data. Jei norite generuoti įspėjimus dėl termino įvykių, kurie įvyko po to, kai paketinė užduotis apdorojo įspėjimus, tą pačią dieną galite dar kartą vykdyti paketinę užduotį.

Pavyzdžiui, paketinė užduotis buvo vykdyta konkrečią dieną. Tada sukuriate pirkimo užsakymą, kurio termino data turėtų suaktyvinti įspėjimą tą pačią dieną. Norėdami gauti įspėjimą tą pačią dieną, turite vykdyti paketinę užduotį dar kartą po to, kai sukuriamas pirkimo užsakymas. Tačiau, jei tą dieną paketinės užduoties dar kartą nevykdysite, kitos dienos paketinė užduotis aptiks visus ankstesnių dienų neapdorotus termino įvykius.

> [!NOTE]
> Net jei paketinis vykdymas paleidžiamas kelis kartus per dieną, to paties termino ir tų pačių sąlygų įspėjimų dublikatai negeneruojami. Generuojami įspėjimai, skirti tik toms datoms, kurios praėjo dėl sistemos pakeitimų, įvykusių po paskutinio paketinės užduoties vykdymo.

### <a name="batch-processing-window"></a>Paketinio vykdymo langas

Įmonės įspėjimų taisyklių apdorojimą galima sustabdyti dėl kelių priežasčių. Tai gali būti atostogos, sistemos klaidos arba kitos priežastys, dėl kurių tam tikrą laiką paketinės užduotys nevykdomos.

Jei norite, kad termino įspėjimai netaptų pasenę, nes kelias dienas nebuvo vykdoma paketinė užduotis, galite nustatyti paketinio vykdymo langą. Paketinio vykdymo langą galima naudoti norint neleisti paketinę užduotį vykdyti nurodytą dienų skaičių.

Jei nustatysite paketinio vykdymo langą, įspėjimas bus siunčiamas, kai apdorojama įspėjimo taisyklė, net jei įspėjimas viršija termino kriterijuose nustatytą laiko apribojimą. Įspėjimas toliau siunčiamas tol, kol tęsiasi šiuo laiko apribojimu apibrėžtas laikotarpis ir paketinio vykdymo langas. Tačiau, kai laikotarpis viršija trukmę, apibrėžtą laiko apribojimu ir paketinio vykdymo langu, įspėjimas nebesiunčiamas.

### <a name="set-up-processing-for-due-date-alerts"></a>Įspėjimo dėl termino apdorojimo nustatymas

1. Pasirinkite **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Įspėjimai** &gt; **Termino įspėjimai**.
2. Dialogo lange **Termino įspėjimai** įveskite atitinkamą informaciją.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]