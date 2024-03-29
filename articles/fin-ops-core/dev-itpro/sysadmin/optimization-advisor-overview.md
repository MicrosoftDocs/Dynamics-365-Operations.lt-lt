---
title: Optimizavimo patarėjo apžvalga
description: Šiame straipsnyje aprašoma, kaip galima naudoti optimizavimo pagal biudžeto ir operacijų optimalią konfigūraciją.
author: kamaybac
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: f24e8dfecb04f928994bb5a197d32a7279022512
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281362"
---
# <a name="optimization-advisor-overview"></a>Optimizavimo patarėjo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip galima naudoti optimizavimo pagal biudžeto ir operacijų optimalią konfigūraciją.

## <a name="overview"></a>Apžvalga

Atlikus netinkamą modulio konfigūraciją ir sąranką, gali būti pasiekiamos ne visos programos funkcijos, be to, tai gali turėti įtakos sistemos efektyvumui, taip pat sklandžiam verslo procesų veikimui. Verslo duomenų kokybė (pvz., duomenų tikslumas, išsamumas ir tvarkingumas) taip pat turi įtakos sistemos efektyvumui, organizacijos sprendimų priėmimo pajėgumui, našumui ir t. t.

Darbo sritis **Optimizavimo patarėjas** yra įrankis, kuriuo naudodamiesi patyrę vartotojai, verslo analitikai, funkciniai konsultantai ir IT palaikymo funkcijos gali nustatyti modulio konfigūravimo ir verslo duomenų problemas. Optimizavimo patarėjas pasiūlo geriausią modulio konfigūraciją ir nustato, kurie verslo duomenys yra pasenę arba neteisingi.

Optimizavimo patarėjas periodiškai paleidžia geriausios praktikos taisyklių rinkinį. Pasiekiamas numatytasis taisyklių rinkinys, tačiau vartotojai taip pat gali kurti specialiai jų tinkinimams, nepriklausomų programinės įrangos pardavėjų (IVS) sprendimams ir verslo duomenims pritaikytas taisykles. Daugiau informacijos apie taisyklių kūrimą žr. [Optimizavimo patarėjo taisyklių kūrimas](./create-rules-optimization-advisor.md).

Aptikus taisyklės pažeidimą sugeneruojama ir darbo srityje **Optimizavimo patarėjas** rodoma optimizavimo galimybė. Vartotojas tiesiogiai darbo srityje **Optimizavimo patarėjas** gali atlikti tiesioginį koreguojamąjį veiksmą.

Galimybės gali būti pritaikytos konkrečiai įmonei arba visoms įmonėms, priklausomai nuo sąrankos tipo ir tikrinamų duomenų. Konkrečiai įmonei pritaikytas galimybes galima peržiūrėti pasirinkus bet kurią įmonę. Norėdami peržiūrėti konkrečios įmonės galimybę, pirmiausia turite pasirinkti įmonę.

Optimizavimo galimybėms taikomos standartinės saugos strategijos. Pavyzdžiui, su modulio **Sandėlio valdymas** konfigūracija susietas optimizavimo galimybes gali matyti tik tie vartotojai, kurie turi prieigą prie sandėlio valdymo ir gali keisti jo sąranką.

Atliekant tam tikrų optimizavimo galimybių veiksmus sistema apskaičiuoja galimybės poveikį trumpinant verslo procesų veikimo laiką. Deja, ši funkcija prieinama naudojantis ne visomis optimizavimo galimybėmis.

Norėdami daugiau sužinoti apie optimizavimo žodyną, ["Dynamics 365" finansų vaizdo įraše peržiūrėkite trumpą optimizavimo optimizavimą](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Optimizavimo taisyklės

Norėdami peržiūrėti visą optimizavimo patarėjo taisyklių sąrašą ir pamatyti, kaip dažnai taisyklės vertinamos, eikite į **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Diagnostikos tikrinimo priežiūros taisyklė**. Vertinamos tik tos taisykles, kurių būsena **Aktyvi**. Galima nustatyti, kaip dažnai atlikti vertinimą: **Kasdien**, **Kas savaitę**, **Kas mėnesį** arba **Neplanuotai**.

Norėdami atlikti nesuplanuotų taisyklių vertinimą arba iš naujo įvertinti periodines taisykles ne pagal joms numatytą grafiką, eikite į **Sistemos administravimas** &gt; **Periodinės užduotys** &gt; **Planuoti diagnostikos tikrinimo taisyklę**. Po to dialogo lange **Diagnostikos taisyklės tikrinimas** pasirinkite vertinimo dažnumą. Iš naujo patikrinamos visos nurodyto dažnio taisyklės.

Dabartinį optimizavimo taisyklių rinkinį galima suskirstyti į toliau nurodytas kategorijas.

### <a name="module-configuration-and-setup"></a>Modulio konfigūravimas ir sąranka

Sandėlio valdymo sąranka yra sudėtingas procesas. Siekiant palengvinti procesą sukurtos tam tikros sąrankos tinkamumo tikrinimą palengvinančios taisyklės. Pavyzdžiui, viena taisyklė įvertina fiksuotų produkto varianto vietų, pardavimo užsakymų ir perkėlimo užsakymų sandėlio vietos nurodymų sąranką.

Be to, tam tikros taisyklės patikrina, ar iš tiesų naudojamos įjungtos funkcijos. Pavyzdžiui, viena taisyklė nustato, ar naudojate modulį **Bendrasis planavimas**. Jei taisyklė nustato, kad modulio nenaudojate, sugeneruojama optimizavimo galimybė, siūlanti išjungti planavimo procesus.

### <a name="system-configuration"></a>Sistemos konfigūracija

Jei konkrečia konfigūracijos raktu valdoma funkcija nesinaudojama, sugeneruojama optimizavimo galimybė, siūlanti išjungti konfigūracijos raktą. Konfigūracijos raktų pavyzdžiai: **Esamas svoris**, **Biudžeto planavimas**, **Projektas** ir **Patvirtintų tiekėjų sąrašas**.

### <a name="business-data-consistency-and-cleanup"></a>Verslo duomenų nuoseklumas ir valymas

Jei neteisingi bendrieji duomenys (pavyzdžiui, jei nurodyti matavimo vienetų konvertavimai, bet nenurodyti matavimo vienetai arba jeigu nurodyti matavimo vienetų konvertavimai dalijasi iš 0 \[nulio\]), sugeneruojama optimizavimo galimybė, siūlanti pakoreguoti duomenis. 

Jei esama per daug paketinės užduoties retrospektyvos įrašų, pasenusių prekių, uždarytų sandėlyje laikyti įgalintų prekių turimo kiekio įrašų ir t. t. arba jei šie įrašai ir prekės per seni, sugeneruojamos optimizavimo galimybės, siūlančios išvalyti duomenis. Palaikydami savo duomenis švarius galite padėti pagerinti visos sistemos našumą.

### <a name="best-practices"></a>Geriausia praktika

Jei kai kuriuos verslo procesus naudojate nesivadovaudami geriausia praktika (pavyzdžiui, jei vykdote išankstinį atsargų uždarymą prieš uždarydami atsargas arba jei perkeldami papildomos knygos žurnalo paketą naudojate suplanuotą paketą), optimizavimo galimybės informuoja jus apie geriausią praktiką ir paprašo jos laikytis.

## <a name="optimization-opportunities"></a>Optimizavimo galimybės

Norėdami peržiūrėti atliekant optimizavimo taisyklių vertinimą sugeneruotas optimizavimo galimybes, atidarykite darbo sritį **Optimizavimo patarėjas**.

Šioje darbo srityje pasirinkę **Daugiau informacijos** galite peržiūrėti daugiau informacijos apie galimybę. Jei norite, kad sistema imtųsi veiksmų ir pakoreguotų sąranką, išvalytų duomenis ir t. t., kad jums nereikėtų patiems atidaryti tam tikrų puslapių, pasirinkite **Imtis veiksmų**.

Nėra jokios optimizavimo galimybių darbo eigos. Pasirinkus **Imtis veiksmų** arba pasinaudojus dialogo lange **Daugiau informacijos** pateiktu naršymo keliu optimizavimo galimybė sąraše neberodoma. Jei atlikus koreguojamąjį veiksmą nepavyksta visiškai išspręsti problemos, kitą kartą tikrinant taisyklę galimybė sugeneruojama iš naujo.

Jei galimybė nėra taikoma jūsų vaidmeniui, galite pasirinkti **Slėpti mano sąraše**. Net vėliau paleidus šios galimybės taisyklę galimybės savo sąraše nematysite.

Norėdami išjungti tam tikrų taisyklių vertinimą, pasirinkite taisyklės sugeneruotą galimybę, po to pasirinkite **Išjungti analizę**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Optimizavimo patariamojo įrankio taisyklių kūrimas](./create-rules-optimization-advisor.md)

["Dynamics 365 Finance" optimizavimas (vaizdo įrašas)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
