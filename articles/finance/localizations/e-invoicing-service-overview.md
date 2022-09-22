---
title: Elektroninių SF išrašymo priedo apžvalga
description: Šiame straipsnyje pateikta elektroninių SF išrašymo " Microsoft Dynamics 365 Finance" ir "Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d73b2dd7bf83c169aa776b41f962cc6addf5f19
ms.sourcegitcommit: a5a4c45bb265758c6e5c3483c8552503b1799a89
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524722"
---
# <a name="electronic-invoicing-overview"></a>Elektroninių SF išrašymo priedo apžvalga

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymas Microsoft Dynamics 365 Dynamics 365 Supply Chain Management finansams ir yra hyper-scalable multitenant paslauga, kuri įgalina konfigūruojamą elektroninių SF apdorojimą ir konfigūruojamus elektroninių dokumentų mainus. Apdorojimo ir integravimo taisyklės yra visiškai konfigūruojamos, o logika vykdoma už „Finance” ir „Supply Chain Management” ribų. Paslauga skirta daugiausia elektroninių SF dokumentų apdorojimui verslo valdymo scenarijuose. Tačiau jis gali būti konfigūruojamas pasirinktinai kitiems tikslams, pvz., "verslas verslui" skirtingo tipo dokumentams.

Elektroninių SF išrašymo priedas gali padėti pasiekti toliau nurodytus tikslus:

- Greitas ir lengvas konkrečių šalių / regionų reikalavimų taikymas
- Standartizuoti elektroninių SF išrašymo priedo sprendimo diegimai
- Išplėstinis dokumentų retrospektyvos atsekamumas
- Trumpesnis diegimo ciklas
- Sumažintos bendros nuosavybės išlaidos (TCO)
- Lengvai koreguojamos konfigūracijos, kurioms nereikia keisti kodo
- Supaprastintas konfigūracijos pakavimas
- Įtaisytasis eksportavimas, importavimas ir integravimas bei paprastas elektroninių SF dokumentų apdorojimo būdas
- Paprastas to paties eksportavimo, importavimo ir integravimo konfigūravimų pakartotinis naudojimas visose įmonėse

## <a name="service-availability"></a>Paslaugų prieinamumas

Šiuo metu elektroninių SF išrašymo funkcija galima finansų ir tiekimo grandinės valdymo klientams. Norėdami gauti daugiau informacijos, peržiūrėkite savo programos licencijos sąlygas.

Kadangi funkcijos, kurios adresuoja šaliai/regionui bingus reikalavimus, gali būti ribojamos skirtinguose paleidimo etapuose, visada turėtumėte peržiūrėti naujausias dokumentaciją, kurioje aprašomos palaikomų šalių/regionų sprendimų aprėpties ir aprėptis.

Elektroninių SF išrašymo priedas diegiamas toliau nurodytuose „Azure” regionuose:

- Jungtinės Valstijos
- Europa
- Jungtinė Karalystė
- Azija
- Japonija
- Šveicarija
- Brazilija
- Jungtiniai Arabų Emyratai
- Australija
- Kanada
- Prancūzija
- Indija

> [!NOTE]
> Elektroninių SF išrašymo priedas nepalaiko vietinių visuotinių diegimų.

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

- Out-box integravimas su finansų ir tiekimo grandinės valdymu
- Nuosekli vartotojų patirtis konfigūracijoje ir elektroninio SF proceso stebėjime visose šalyse ir regionuose
- Spartesnis, lengvesnis ir pigesnis elektroninių SF išrašymo priedo sprendimų taikymas naujose šalyse ar regionuose
- Tarnybos konfigūravimas, naudojant reguliavimo konfigūracijos tarnybos (RCS) ir globalizavimo funkcijų nustatymą
- Verslo duomenų pakeitimas į keletą elektroninių SF formatų (XML, "JavaScript" objektų notacijos \[JSON\], \[TXT ir kableliu atskirtų verčių CSV\]) naudojant RCS nustatytas konfigūracijas:

    - Elektroninių ataskaitų (ER) formatai, galimi šalims ir regionams, kuriuose negalima konfigūruoti elektroninės SF pakeitimo

- Konfigūruojamas elektroninių SF pateikimas išorinėms žiniatinklio paslaugoms, įskaitant sertifikavimo tvarkymą naudojant skaitmeninius parašus:

    - Įtaisytasis, lengvai išplečiamas ir konfigūruojamas integravimas su papildomu turiniu kelioms šalims ir regionams

- Žiniatinklio tarnybų atsakymų tvarkymas, įskaitant konfigūruojamus išimčių pranešimų tvarkymą
- Elektroninių parašų palaikymas (pvz., elektroninių parašų, kurie naudoja XMLDSig pasirašymo algoritmą)
- Galimybė siųsti dokumentus į el. laiškus ir juos saugoti SharePoint
- Elektroninių SF pranešimų paketinis apdorojimas
- Konfigūruojamas gaunamų dokumentų pakeitimas ir šių dokumentų apdorojimas finansų ir tiekimo grandinės valdymo procesuose
- Galimybė gauti gaunamus dokumentus iš kanalų, pvz., el. pašto ir SharePoint

## <a name="privacy-notice"></a>Privatumo pranešimas

Elektroninių SF išrašymo įgalinimas ir naudojimas gali reikalauti, kad būtų siunčiami riboti duomenys. Šie duomenys apima organizacijos mokesčių registracijos ID. Šie duomenys bus perduoti trečiųjų šalių agentūroms, kurias mokesčių inspekcija įgaliojo siųsti elektronines SF iš anksto nustatytais formatais, kurių reikia integravimui su vyriausybės tinklo tarnybomis. Iš šių išorinių sistemų importuojami duomenys į šią "Dynamics 365" interneto paslaugą priklauso nuo mūsų privatumo [patvirtinimo](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite šaliai/regionui brangesnių priemonių dokumentuose skyriuje "Privatumo pranešimas".

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
