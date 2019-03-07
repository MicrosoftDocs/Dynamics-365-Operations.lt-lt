---
title: Proceso veiklos
description: Šioje temoje pateikiama informacija apie įvairių tipų veiklas, kurias galima naudoti samdos procese.
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2019
ms.locfileid: "374762"
---
# <a name="activities-in-the-hiring-processes"></a>Samdos proceso veiklos

[!include[banner](../includes/banner.md)]

Veiklas galima įtraukti į „Dynamics 365 for Talent: Attract“ kaip samdos proceso dalį. Veiklas galima įtraukti į proceso šabloną arba jas galima tiesiogiai įtraukti į darbo samdos procesą. Apibrėžus darbą, pažymimas proceso šablono, o veiklos, kurios įtrauktos į šabloną, pritaikomos užduočiai. Jei šablonas nepasirenkamas, naudojamas numatytasis šablonas. Samdos procesą taip pat galima pakeisti užduotyje pritaikius šabloną.

> [!NOTE] 
> Proceso šablonai teikiami su išsamios įdarbinimo informacijos priedu.

## <a name="prospect-activity"></a>Potencialaus kliento veikla

Potencialaus kliento veikla kontroliuoja, ar potencialūs klientai gali būti įtraukti į darbą. Pagal numatytuosius parametrus potencialūs klientai gali būti įtraukti į darbą. Norėdami išjungti potencialaus kliento veiklą, nustatykite parinkties **Įjungti potencialius klientus** reikšmę **Išjungta**. Kai potencialaus kliento veikla išjungta, įdarbinimo vadovai gali įtraukti ir peržiūrėti potencialius klientus, o darbe rodomas skirtukas **Potencialus klientas**.

## <a name="application-activity"></a>Prašymo veikla

Prašymo veikla būtina samdos proceso šablone. Norėdami siųsti el. laiškus kandidatams, kai jie pateikia savo prašymą arba yra įtraukiami į prašymo teikimo etapą, nustatykite parinkties **Siųsti el. laišką kandidatams** reikšmę į **Įjungta**.

## <a name="interview-schedule-and-feedback-activity"></a>Pokalbio grafikas ir atsiliepimo veikla

Ši veikla turi tris komponentus: kandidato pasiekiamumo užklausą, grafiką ir atsiliepimą. Naudokite pokalbio veiklą užduoties šablone, jei norite įtraukti kandidato pasiekiamumo užklausą, grafiką ir atsiliepimą kaip proceso dalį, o ne naudoti juos atskirai samdos proceso metu. Daugiau informacijos žr. [Pokalbio planavimas ir atsiliepimas](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>„PowerApps“ veikla

„PowerApps“ veikla suteikia galimybę įterpti „Microsoft PowerApps“ programą į samdos procesą. Programa gali būti būtina visiems pretendentams, tik vidiniams pretendentams, tik išoriniams pretendentams arba jokiems pretendentams. Jei programa pažymėta kaip būtina, ji turi būti atlikta prieš pereinant į kitą etapą. Jei programa nėra pažymėta kaip būtina, veikla yra pasirinktinis veiksmas ir į kitą etapą galima pereiti net jei programa neatlikta.

Norėdami įrašyti „PowerApps“ veiklą į samdos procesą, turite įvesti „PowerApps“ ID. Norėdami rasti „PowerApps“ ID, atidarykite [PowerApps](https://web.powerapps.com), pasirinkite **Programos**, ir tada pasirinkite **Informacija**.

Pasirinkus parinktį **Leisti įtraukti dalyvių į šią veiklą**, galima įtraukti papildomų dalyvių į programą, kuri naudoja „PowerApps“ veiklą. Pvz., organizacija sukūrė „PowerApps“ programą, kuri yra pokalbio klausimų, skirtų techniniams vaidmenims, biblioteka. Dabar organizacija samdo naują programinės įrangos kūrėją ir įtraukė „PowerApps“ veiklą į programinės įrangos kūrėjo vaidmens samdos procesą. Jei pasirinkta parinktis **Leisti įtraukti dalyvių į šią veiklą**, įdarbintojas arba samdos vadovas, kuris yra peržiūri pretendentą į programinės įrangos kūrėjo vaidmenį, gali įtraukti žmonių „PowerApps“ veiklą. Tada šie žmonės gali peržiūrėti programą, kurioje yra pokalbio klausimų.

> [!NOTE]
> „PowerApps“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

## <a name="youtube-activity"></a>„YouTube“ veikla

„YouTube“ veikla suteikia galimybę bendrinti „YouTube“ vaizdo įrašą samdos proceso metu. Norėdami įrašyti „YouTube“ veiklą nuomos procese, turite nurodyti „YouTube“ vaizdo įrašo URL. Naudodami „PowerApps“ veiklą galite leisti dalyvius įtraukti į veiklą. Jei pasirenkate parinktį **Rodyti tik kandidatui**, vaizdo įrašas rodomas tik kandidatui. Jis nerodomas „Attract“ samdos procese.

> [!NOTE]
> „YouTube“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

## <a name="web-content-activity"></a>Žiniatinklio turinio veikla

Žiniatinklio turinio veikla suteikia galimybę įterpti interneto turinį samdos procese. Norėdami įrašyti žiniatinklio turinio veiklą nuomos procese, turite nurodyti turinio URL. Naudodami „PowerApps“ ir „YouTube“ veiklas galite leisti dalyvius įtraukti į veiklą. Jei pasirenkate parinktį **Rodyti tik kandidatui**, turinys rodomas tik kandidatui. Jis nerodomas „Attract“ samdos procese. Galite pasirinkti rodomo turinio dydį.

> [!NOTE]
> Žiniatinklio turinio veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

## <a name="microsoft-forms-activity"></a>„Microsoft Forms“ veikla

„Microsoft Forms“ veikla suteikia galimybę įterpti „Microsoft Forms“ formą į samdos procesą. „Microsoft Forms“ suteikia galimybę klausimynus, apklausas ir tyrimus. Norėdami įrašyti „Microsoft Forms“ veiklą nuomos procese, turite nurodyti formos URL. Naudodami „PowerApps“, „YouTube“ ir žiniatinklio turinio veiklas galite leisti dalyvius įtraukti į veiklą. Jei pasirenkate parinktį **Rodyti tik kandidatui**, forma rodoma tik kandidatui. Jis nerodomas „Attract“ samdos procese.

„Microsoft Forms“ autoriai gali keisti savo parametrus, kad į jų apklausą galėtų arba testą galėtų atsakyti organizacijai nepriklausantys vartotojai. Šiuo atveju vartotojai anonimiškai pateikia atsakymus. Jei norite pamatyti, kas pateikė apklausos arba testo atsakymus, galite reikalauti, kad apklausos arba testo vykdymo metu respondentai įvestų savo vardus bei pavardes.

> [!NOTE]
> „Microsoft Forms“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.
