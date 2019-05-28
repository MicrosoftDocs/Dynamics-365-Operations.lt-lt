---
title: Proceso veiklos
description: Šioje temoje pateikiama informacija apie įvairių tipų veiklas, kurias galima naudoti samdos procese.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c975b95e4195c795ec4c816b1f3a50461715feea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518686"
---
# <a name="activities-in-the-hiring-processes"></a>Samdos proceso veiklos

[!include[banner](../includes/banner.md)]

Veiklas galima įtraukti į „Dynamics 365 for Talent: Attract“ kaip samdos proceso dalį. Veiklas galima įtraukti į proceso šabloną arba jas galima tiesiogiai įtraukti į darbo samdos procesą. Apibrėžus darbą, pažymimas proceso šablono, o veiklos, kurios įtrauktos į šabloną, pritaikomos užduočiai. Jei šablonas nepasirenkamas, naudojamas numatytasis šablonas. Samdos procesą taip pat galima pakeisti užduotyje pritaikius šabloną.

> [!NOTE] 
> Proceso šablonai teikiami su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Potencialaus kliento veikla

Potencialaus kliento veikla kontroliuoja, ar potencialūs klientai gali būti įtraukti į darbą. Pagal numatytuosius parametrus potencialūs klientai gali būti įtraukti į darbą. Norėdami išjungti potencialaus kliento veiklą, nustatykite parinkties **Įjungti potencialius klientus** reikšmę **Išjungta**. Kai potencialaus kliento veikla išjungta, įdarbinimo vadovai gali įtraukti ir peržiūrėti potencialius klientus, o darbe rodomas skirtukas **Potencialus klientas**.

## <a name="application-activity"></a>Prašymo veikla

Prašymo veikla būtina samdos proceso šablone. Norėdami siųsti el. laiškus kandidatams, kai jie pateikia savo prašymą arba yra įtraukiami į prašymo teikimo etapą, nustatykite parinkties **Siųsti el. laišką kandidatams** reikšmę į **Įjungta**.

## <a name="interview-schedule-and-feedback-activity"></a>Pokalbio grafikas ir atsiliepimo veikla

Ši veikla turi tris komponentus: kandidato pasiekiamumo užklausą, grafiką ir atsiliepimą. Naudokite pokalbio veiklą užduoties šablone, jei norite įtraukti kandidato pasiekiamumo užklausą, grafiką ir atsiliepimą kaip proceso dalį, o ne naudoti juos atskirai samdos proceso metu. Daugiau informacijos žr. [Pokalbio planavimas ir atsiliepimas](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>„PowerApps“ veikla

„PowerApps“ veikla suteikia galimybę įterpti „Microsoft PowerApps“ programą į samdos procesą. Programa gali būti būtina visiems pretendentams, tik vidiniams pretendentams, tik išoriniams pretendentams arba jokiems pretendentams. Jei programa pažymėta kaip būtina, ji turi būti atlikta prieš pereinant į kitą etapą. Kad programa būtų laikoma baigta, lauką **JobApplicationStatus** reikia nustatyti į **Baigta**. Šis laukas pateiktas objekte JobApplicationActivity, todėl prieš pereinant į kitą etapą programa „PowerApps“ turės atnaujinti šį lauką. Jei programa nėra pažymėta kaip būtina, veikla yra pasirinktinis veiksmas ir į kitą etapą galima pereiti net jei programa neatlikta.

Norėdami įrašyti „PowerApps“ veiklą į samdos procesą, turite įvesti „PowerApps“ ID. Norėdami rasti „PowerApps“ ID, atidarykite [PowerApps](https://web.powerapps.com), pasirinkite **Programos**, ir tada pasirinkite **Informacija**.

Pagal numatytuosius parametrus, „PowerApps“ veikla pasiekiama samdos vadovui, įdarbintuojui ir jų atstovams. Pasirinkus parinktį **Leisti įtraukti dalyvių į šią veiklą**, į programą, kuri naudoja „PowerApps“ veiklą, galima įtraukti papildomų samdos komandos dalyvių. Pvz., organizacija sukūrė „PowerApps“ programą, kuri yra pokalbio klausimų, skirtų techniniams vaidmenims, biblioteka. Dabar organizacija samdo naują programinės įrangos kūrėją ir įtraukė „PowerApps“ veiklą į programinės įrangos kūrėjo vaidmens samdos procesą. Jei pasirinkta parinktis **Leisti įtraukti dalyvių į šią veiklą**, įdarbintojas arba samdos vadovas, kuris peržiūri pretendentą į programinės įrangos kūrėjo vaidmenį, gali įtraukti kalbintojų į „PowerApps“ veiklą. Tada šie žmonės gali peržiūrėti programą, kurioje yra pokalbio klausimų.

> [!NOTE]
> „PowerApps“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>„YouTube“ veikla

„YouTube“ veikla suteikia galimybę bendrinti „YouTube“ vaizdo įrašą samdos proceso metu. Norėdami įrašyti „YouTube“ veiklą nuomos procese, turite nurodyti „YouTube“ vaizdo įrašo URL. Galite pasirinkti, kad turinys būtų rodomas **samdos komandai**, **tik vidiniams kandidatams**, **tik išoriniams kandidatams** arba **visiems kandidatams**. Kaip ir „PowerApps“ veiklą, taip ir samdos komandos dalyvius galite leisti įtraukti į veiklą. Jei turinį pasirenkate rodyti kandidatams, vaizdo įrašas rodomas tik kandidatui, o ne nuomos procesui.

> [!NOTE]
> „YouTube“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Žiniatinklio turinio veikla

Žiniatinklio turinio veikla suteikia galimybę įterpti interneto turinį samdos procese. Norėdami įrašyti žiniatinklio turinio veiklą nuomos procese, turite nurodyti turinio URL. Galite pasirinkti, kad turinys būtų rodomas **samdos komandai**, **tik vidiniams kandidatams**, **tik išoriniams kandidatams** arba **visiems kandidatams**. Kaip ir „PowerApps“ bei „YouTube“ veiklą, taip ir samdos komandos dalyvius galite leisti įtraukti į veiklą. Jei turinį pasirenkate rodyti kandidatams, interneto turinys rodomas tik kandidatui, o ne nuomos procesui. Galite pasirinkti rodomo turinio dydį.

> [!NOTE]
> Žiniatinklio turinio veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>„Microsoft Forms“ veikla

„Microsoft Forms“ veikla suteikia galimybę įterpti „Microsoft Forms“ veiklą į samdos procesą. „Microsoft Forms“ suteikia galimybę klausimynus, apklausas ir tyrimus. Norėdami įrašyti „Microsoft Forms“ veiklą nuomos procese, turite nurodyti formos URL. Galite pasirinkti, kad turinys būtų rodomas **samdos komandai**, **tik vidiniams kandidatams**, **tik išoriniams kandidatams** arba **visiems kandidatams**. Kaip ir „PowerApps“, „YouTube“ bei interneto turinio veiklą, taip ir samdos komandos dalyvius galite leisti įtraukti į veiklą. Jei turinį pasirenkate rodyti kandidatams, forma rodoma tik kandidatui, o ne nuomos procesui.

„Microsoft Forms“ autoriai gali keisti savo parametrus, kad į jų apklausą galėtų arba testą galėtų atsakyti organizacijai nepriklausantys vartotojai. Šiuo atveju vartotojai anonimiškai pateikia atsakymus. Jei norite pamatyti, kas pateikė apklausos arba testo atsakymus, galite reikalauti, kad apklausos arba testo vykdymo metu respondentai įvestų savo vardus bei pavardes.

> [!NOTE]
> „Microsoft Forms“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Pasiūlymo veikla

Nuomos proceso šablonui reikalinga pasiūlymo veikla. Norėdami naudoti integruotą pasiūlymo valdymo programą, parinktį **Paleisti programą „Offer Management“ ruošiant pasiūlymą** nustatykite į **Įjungta**. Jei šis parametras išjungtas, kandidatas pasiūlymo programoje rodomas nebus, todėl kandidato pasiūlymo veiklos naujinimus turėsite sekti rankiniu būdu. Norėdami nurodyti, ar samdos vadovai gali paruošti kandidato pasiūlymą pasiūlymo programoje, parinktį **Samdos vadovai gali paruošti pasiūlymą** nustatykite į **Įjungta**. Jei kartu su užduotimi susietos kelios pareigos, galite nuspręsti, ar norite parengti keletą pasiūlymų atsižvelgiant į tą patį padėties numerį. Jei norite, kad dėl vienos užduoties pareigų būtų galima pateikti tik vieną pasiūlymą, parinktį **Leisti pakartotinai naudoti pareigas užduotyje** nustatykite į **Išjungta**.

> [!NOTE]
> Integruotą programą „Offer Management“ galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu. Daugiau informacijos ieškokite temoje [„Attract“ išsamios įdarbinimo informacijos priedo funkcijos](./attract-comprehensive-hiring.md).


