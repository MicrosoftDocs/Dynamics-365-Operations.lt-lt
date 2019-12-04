---
title: Įmonės informacijos konfigūravimas „Attract”
description: Šioje temoje paaiškinama, kaip konfigūruoti įmonės informaciją ir prekių ženklus, skirtus „Microsoft Dynamics 365 Talent - Attract”.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db3ec965f3a52810d5f310697b9ed830c3abe681
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833259"
---
# <a name="configure-company-information-in-attract"></a>Įmonės informacijos konfigūravimas „Attract”

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Talent: Attract“ administravimo centre pateikiami „Attract“ programos konfigūracijos parametrai, integravimo parinktys ir nustatymo parinktys.

## <a name="company-information"></a>Įmonės informacija

Įveskite rodomą įmonės pavadinimą ir įtraukite įmonės logotipą. Tada rodomą pavadinimą ir logotipą galima naudoti darbo skelbimuose ir supažindinimo metu.

## <a name="linkedin-integration"></a>„LinkedIn‟ integravimas

Nustatyti integravimą su „LinkedIn Recruiter System Connect“ (RSC). Prisijungę prie „LinkedIn“ naudodami savo „LinkedIn“ kredencialus, galite sinchronizuoti kandidato „LinkedIn“ profilį, programas, atsiliepimą apie pokalbį ir samdos komandos pastabas. Būtina turėti visą „LinkedIn“ įdarbintojo licenciją. Norėdami gauti daugiau informacijos apie „LinkedIn Recruiter“, žr. [„Recruiter System Connect“ (RSC) – DUK](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Vartotojo teisės

Priskirkite vaidmenis vartotojams jūsų organizacijoje. Galima naudoti šiuos vaidmenis: **Administratorius**, **Įdarbintojas**, **Samdos vadovas** ir **Tik skaityti**. Daugiau informacijos apie vartotojų teises žr. [Sauga ir vaidmenų valdymas sprendime „Attract“](./security-attract.md).

## <a name="feature-management"></a>Funkcijų valdymas

Pridedant naujų funkcijų, jos gali būti paskelbtos viešojoje peržiūroje. Viešosios peržiūros funkcijos atitinka ne visus aptarnavimo reikalavimus. Gaudami šias funkcijas sutinkate dalintis duomenimis su išorinėmis sistemomis. Gali būti, kad jūsų organizacijai nereikia visų naujų funkcijų, kurios paskelbiamos. Viešosios peržiūros funkcijas galite įjungti ir išjungti, priklausomai nuo organizacijos poreikių.

## <a name="template-management"></a>Šablonų valdymas

Proceso šablone pateikiamos visos veiklos, kurios turėtų būti įtrauktos samdymo į darbo vietą proceso metu. Jūsų organizacija gali leisti samdos proceso šablonus kurti visiems komandos nariams arba tik administratoriams. Norėdami komandos nariams leisti kurti nuosavus samdos proceso šablonus, įjunkite šablonų valdymo funkciją. Daugiau informacijos apie proceso šablonus žr. [Proceso šablono kūrimas sprendime „Attract“](./process-templates-attract.md).

## <a name="email-template-settings"></a>El. pašto šablonų parametrai

Organizacijų, gali kurti el. laiškų šablonus, skirtus įvairioms situacijoms. Galite pasirinkti antraštės vaizdą, kad įtrauktumėte el. laiškų šablonų. Tada pasirinkta antraštė bus rodoma visuose el. laiškų šablonuose. Šabloną poraštėje galite įtraukti saitą į jūsų organizacijos ryšių privatumo patvirtinimą ir sąlygas. Daugiau informacijos apie šablonus ieškokite [El. laiško šablonai](./email-templates.md).

## <a name="offer-process"></a>Pasiūlymo procesas

Galite konfigūruoti darbo pasiūlymų patvirtinimo procesą. Pavyzdžiui, galite nurodyti, ar pasiūlymas turi būti patvirtintas prieš jį siunčiant kandidatui. Taip pat galite reikalauti, kad tvirtintojai paliktų komentarą su savo pasiūlymo sprendimu.

Galima naudoti dvi patvirtinimo darbo eigas: **Lygiagreti** ir **Nuosekli**.

- **Lygiagreti** – patvirtinimai siunčiami visiems tvirtintojams tuo pačiu metu.
- **Nuosekli** – tvirtinimai siunčiami tvirtintojams konkrečia tvarka.

Taip pat galite konfigūruoti pasirinktis, susijusias su kandidato patirtimi. Pvz., viena parinktis suteikia galimybę nurodyti, ar kandidatai gali atmesti pasiūlymą be papildomų komentarų. Jei nustatysite parinkties **Leisti kandidatams atmesti pasiūlymą be papildomų komentarų** reikšmę **Ne**, kandidatams bus pateikiamas mygtukas **Atmesti pasiūlymą**. Jei nustatysite šios parinkties reikšmę **Taip**, kandidatai galės atmesti pasiūlymą pasirinkdami priežastį ir tada pasirinkdami **Atmesti pasiūlymą**.

Taip pat galite nustatyti ir taikyti pasiūlymų galiojimo datą. Jei nustatysite parinkties **Reikalauti visų pasiūlymų galiojimo datos** reikšmę **Taip**, pasiūlymai baigs galioti praėjus tam tikram valandų arba dienų skaičiui, kurį nurodysite.

Daugiau informacijos apie pasiūlymų valdymą žr. [Pasiūlymų valdymo nustatymas](./offer-setup.md).
