---
title: Analizės ataskaitų naudojimas „Microsoft Dynamics 365 for Talent - Attract”
description: Šioje temoje aprašoma „Microsoft Dynamics 365 for Talent - Attract” samdos procesų įžvalgų analizės ataskaitos.
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742894"
---
# <a name="use-analytic-reports"></a>Analizės ataskaitų naudojimas

Analitinės ataskaitos programoje „Attract“ suteikia nestandartinį (OOTB) sprendimą samdos proceso įžvalgoms. Galimos funkcijos:

- **Užduoties analizė**: spustelėkite skirtuką **Analizė**, kad pamatytumėte darbo pretendento darbo metriką.
- **Analizės telkinys:** spustelėkite **Analizė** kairiojoje naršymo srityje, kad būtų galima atlikti suvestines užduotis.
- **Vartotojo lygio sauga**: prieigą prie ataskaitų valdo „Attract“ [vaidmuo](security-attract.md) ir užduoties dalyvio vaidmuo.
- **Kryžminis filtravimas:** spustelėkite vizualizavimą ataskaitoje, kad peržiūrėtumėte kitus rodiklius, atfiltruotus pagal pasirinktus duomenis.

>[!NOTE] 
>- Šiuo metu naudojama funkcijos [peržiūra](access-preview-feature.md). Norėdami ją išbandyti, turite turėti [**Išsamios įdarbinimo informacijos priedą**](attract-comprehensive-hiring.md).
>- Visos viešosios peržiūros ataskaitos rodomos anglų kalba.
>- Ataskaitos atnaujinamos kas 3 val. Paskutinis atnaujinimo laikas (vietinėje lauko juostoje) yra ataskaitos viršuje. Atnaujinimo laikas yra apytikslis ir priklauso nuo jūsų regione esančio duomenų kiekio ir išteklių apkrovos.

## <a name="job-analytics"></a>Užduočių analizė

Užduoties analizės ataskaitos yra samdos konkrečiai samdos užduočiai momentinė kopija.  Pagrindinę metriką sudaro:

- Aktyvūs pretendentai pagal etapą
- Pretendento šaltinis
- Pretendento tipas (vidinis ar išorinis)

## <a name="analytics-hub"></a>Analizės tranzito punktas

Analizės tranzito punkto ataskaitose pateikiami suvestiniai darbų duomenys, siekiant išsiaiškinti samdos proceso tendencijas. „Attract“ sudaro dvi OOTB ataskaitos: galimybių suvestinė ir kanalo analizė.

### <a name="pipeline-summary"></a>Pardavimo galimybių suvestinė

Pardavimo galimybių suvestinės ataskaita apibendrina siūlomų darbų duomenis. Pagrindinę metriką sudaro:

- Pretendentai visose užduotyse pagal etapą
- Pretendento šaltinis
- Laisvos užduotys pagal paaukštinimo lygį

### <a name="funnel-analysis"></a>Kanalo analizė

Kanalo analizės ataskaita apibendrina darbo vietų, kurios buvo uždarytos kaip užimtos, duomenis. Pagrindinę metriką sudaro:

- Įdarbinimo laiką
- Konvertavimo metrika (užvedus žymiklį)
- Pasiūlymo priėmimo koeficientas

Pastaba: kad įdarbinimo laikp ataskaitos būtų kuo tikslesnės, rekomenduojama naudoti [pasiūlymo valdymą](offer-setup.md), funkciją, kuri yra išsamaus samdos priedo dalis.

>[!TIP] 
>Pabandykite užvesti žymiklį ant vaizdinių elementų, kad gautumėte papildomos informacijos. Pavyzdžiui, užvedus žymiklį ant **Aktyvūs pretendentai** parodomas vidutinis etapo dienų skaičius. Analizuojant šią informaciją galima gauti įžvalgų, padedančių sutrumpinti įdarbinimo laiką, ir padėti darbdaviams sutrumpinti kiekvieno etapo trukmę.

## <a name="user-specific-security"></a>Vartotojo lygio sauga

„Attract“ ataskaitas galima naudoti administratoriaus, skaityti visus, darbdavio ir samdos vadovo [vaidmenims.](security-attract.md) Nepriskirtiems vartotojams prieiga prie analizės ataskaitos puslapių (Užduoties analizė arba Analizės tranzito punktas) nesuteikiama.

Ataskaitose Užduoties analizė pateikiami pasirinktos užduoties duomenys. Analizės tranzito punkto ataskaitose apibendrinami visų užduočių duomenys, kuriuos gali peržiūrėti vartotojas. Vartotojams, kurie gali peržiūrėti puslapį Mano užduotys ir Visos užduotys, pasiekiami tie patys rodiniai kaip Analizės tranzito punkte.

## <a name="cross-filter"></a>Kryžminis filtravimas

Vienas iš puikiausių „Power BI“ savybių yra tai visų vaizdinių ataskaitos puslapio elementų ryšys. Jei viename iš vaizdinių elementų pasirenkate duomenų tašką, parodomi visi kiti puslapyje esantys vaizdiniai elementai, kuriuose yra duomenų pakeitimai, pagrįsti šiuo pasirinkimu. Sužinokite daugiau ir peržiūrėkite pavyzdį, [Kaip atliekamas vaizdinių elementų kryžminis filtravimas „Power BI“ ataskaitoje](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Eksportuoti į Excel

Norėdami peržiūrėti ataskaitos duomenis programoje „Excel“, galite spustelėti parinkčių meniu (tris taškus) ir pasirinkti **Eksportuoti pagrindinius duomenis.** Eksportuoti duomenys bus eksportuojami kaip filtruojami, atsižvelgiant į „Attract“ vartotojo teises. Norėdami gauti daugiau informacijos, žr. [Duomenų eksportavimas iš vaizdinių elementų](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
