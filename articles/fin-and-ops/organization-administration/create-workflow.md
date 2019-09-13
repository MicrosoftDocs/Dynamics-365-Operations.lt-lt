---
title: Darbo eigos apžvalgos kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo eigą.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 1dc2b2cd6b9372fb60d0e112b5dbb0b60898caca
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865045"
---
# <a name="create-workflows-overview"></a>Darbo eigos apžvalgos kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti darbo eigą.

## <a name="open-the-workflow-editor"></a>Darbo eigos rengyklės atidarymas

„Microsoft Dynamics 365 for Finance and Operations“ modulis, kuriame dirbate, nustato galimus kurti darbo eigos tipus. Atlikite šiuos veiksmus, kad pasirinktumėte darbo eigos, kurią norite kurti, tipą ir atidarytumėte darbo eigos rengyklę.

1. Atidarykite modulį, kuriame norite sukurti naują darbo eigą. Pavyzdžiui, jei norite sukurti pirkimo paraiškų darbo eigą, eikite į modulį, spustelėkite **Paraiškos**.
2. Spustelėkite **Sąranka** &gt; **\[Modulio pavadinimas\] darbo eigos**.
3. Sąrašo puslapio, kuris pasirodo, veiksmų srityje spustelėkite skirtuką **Nauja**.
4. Puslapyje **Darbo eigos kūrimas** pasirinkite norimos kurti darbo eigos tipą ir tada spustelėkite **Kurti darbo eigą**. Atidaroma darbo eigos rengyklė. Dabar galite naudoti toliau nurodytas procedūras, kad sumodeliuotumėte darbo eigą.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Darbo eigos elementų nuvilkimas į kūrimo sritį

Darbo eigos rengyklės srityje **Darbo eigos elementai** pateikti elementai, kuriuos galite įtraukti į savo darbo eigą. Norėdami įtraukti elementus į darbo eigą, nuvilkite juos į drobę.

## <a name="connect-the-elements"></a>Elementų sujungimas

Norėdami vieną darbo eigos elementą sujungti su kitu, laikykite žymiklį ant elemento, kol atsiras jungties taškai. Spustelėkite sujungimo tašką ir vilkite jį prie kito elemento. Būtinai sujunkite visus elementus.

## <a name="configure-the-properties-of-the-workflow"></a>Darbo eigos ypatybių konfigūravimas

Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte darbo eigos ypatybes.

1. Spustelėkite kūrimo sritį, kad įsitikintumėte, jog nepasirinktas joks darbo eigos elementas.
2. Spustelėkite **Ypatybės**, kad atidarytumėte darbo eigos puslapį **Ypatybės**.
3. Naudokite procedūras, pateiktas temoje [Darbo eigos ypatybių konfigūravimas](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Darbo eigos elementų konfigūravimas

Sukonfigūruokite kiekvieną elementą, kurį nuvilkote į kūrimo sritį. Daugiau informacijos, kaip konfigūruoti kiekvieną darbo eigos elementą, žr. tolesnes temas.

- [Neautomatizuotos užduoties konfigūravimas](configure-manual-task-workflow.md)
- [Automatizuotos užduoties konfigūravimas](configure-automated-task-workflow.md)
- [Patvirtinimo proceso konfigūravimas](configure-approval-process-workflow.md)
- [Patvirtinimo veiksmo konfigūravimas](configure-approval-step-workflow.md)
- [Neautomatizuoto sprendimo konfigūravimas](configure-manual-decision-workflow.md)
- [Sąlyginio sprendimo konfigūravimas](configure-conditional-decision-workflow.md)
- [Lygiagrečios veiklos konfigūravimas](configure-parallel-activity-workflow.md)
- [Lygiagrečios šakos konfigūravimas](configure-parallel-branch-workflow.md)
- [Eilutės elemento darbo eigos konfigūravimas](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Visų klaidų ir perspėjimų sprendimas

Srityje **Klaidos ir perspėjimai**, esančioje darbo eigos rengyklės apačioje, rodomi sugeneruoti pranešimai apie darbo eigą. Norėdami rasti elementą, kuriame įvyko klaida arba buvo sugeneruotas perspėjimas, dukart spustelėkite klaidos arba perspėjimo pranešimą. Norint suaktyvinti darbo eigą, prieš tai reikia išspręsti visas klaidas ir perspėjimus.

## <a name="save-and-activate-the-workflow"></a>Darbo eigos įrašymas ir suaktyvinimas

Kai būsite pasirengę įrašyti ir suaktyvinti darbo eigą, atlikite toliau nurodytus veiksmus.

1. Spustelėkite **Įrašyti ir uždaryti**, kad uždarytumėte darbo eigos rengyklę ir atidarytumėte puslapį **Įrašyti darbo eigą**.
2. Įveskite komentarus apie atliktus darbo eigos pakeitimus, o tada spustelėkite **Gerai**.
3. Jei visos klaidos ir perspėjimai išspręsti, bus rodomas puslapis **Darbo eigos aktyvinimas**. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - Norėdami aktyvinti šią darbo eigos versiją, spustelėkite **Aktyvinti naują versiją**. Kai darbo eiga aktyvi, vartotojai galės pateikti dokumentus apdoroti.
    - Jei šios versijos aktyvinti nenorite, spustelėkite **Neaktyvinti naujos versijos**. Darbo eigą galite suaktyvinti vėliau.
