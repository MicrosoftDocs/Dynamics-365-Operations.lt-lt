---
title: Darbo eigos apžvalgos kūrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti darbo eigą.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "195583"
- intro-internal
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 1343061ba06d13e68a98b05c013867af0a4d07a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864492"
---
# <a name="create-workflows-overview"></a>Darbo eigos apžvalgos kūrimas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šiame straipsnyje paaiškinama, kaip sukurti darbo eigą.

## <a name="open-the-workflow-editor"></a>Darbo eigos rengyklės atidarymas

Modulis, kuriame dirbate, nustato galimus kurti darbo eigos tipus. Atlikite šiuos veiksmus, kad pasirinktumėte darbo eigos, kurią norite kurti, tipą ir atidarytumėte darbo eigos rengyklę.

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
3. Laikykitės darbo eigos ypatybės konfigūravimo [straipsnyje nurodytų](configure-workflow-properties.md) procedūrų.

## <a name="configure-the-elements-of-the-workflow"></a>Darbo eigos elementų konfigūravimas

Sukonfigūruokite kiekvieną elementą, kurį nuvilkote į kūrimo sritį. Daugiau informacijos, kaip konfigūruoti kiekvieną darbo eigos elementą, žr. tolesnes temas.

- [Neautomatizuotų darbo eigos užduočių konfigūravimas](configure-manual-task-workflow.md)
- [Automatizuotų darbo eigos užduočių konfigūravimas](configure-automated-task-workflow.md)
- [Darbo eigos patvirtinimo procesų konfigūravimas](configure-approval-process-workflow.md)
- [Darbo eigos patvirtinimo veiksmų konfigūravimas](configure-approval-step-workflow.md)
- [Neautomatinių darbo eigos sprendimų konfigūravimas](configure-manual-decision-workflow.md)
- [Sąlyginių darbo eigos sprendimų konfigūravimas](configure-conditional-decision-workflow.md)
- [Lygiagrečių darbo eigos šakų konfigūravimas](configure-parallel-activity-workflow.md)
- [Lygiagrečios šakos konfigūravimas](configure-parallel-branch-workflow.md)
- [Eilutės elemento darbo eigų konfigūravimas](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Visų klaidų ir perspėjimų sprendimas

Srityje **Klaidos ir perspėjimai**, esančioje darbo eigos rengyklės apačioje, rodomi sugeneruoti pranešimai apie darbo eigą. Norėdami rasti elementą, kuriame įvyko klaida arba buvo sugeneruotas perspėjimas, dukart spustelėkite klaidos arba perspėjimo pranešimą. Norint suaktyvinti darbo eigą, prieš tai reikia išspręsti visas klaidas ir perspėjimus.

## <a name="save-and-activate-the-workflow"></a>Darbo eigos įrašymas ir suaktyvinimas

Kai būsite pasirengę įrašyti ir suaktyvinti darbo eigą, atlikite toliau nurodytus veiksmus.

1. Spustelėkite **Įrašyti ir uždaryti**, kad uždarytumėte darbo eigos rengyklę ir atidarytumėte puslapį **Įrašyti darbo eigą**.
2. Įveskite komentarus apie atliktus darbo eigos pakeitimus, o tada spustelėkite **Gerai**.
3. Jei visos klaidos ir perspėjimai išspręsti, bus rodomas puslapis **Darbo eigos aktyvinimas**. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - Norėdami aktyvinti šią darbo eigos versiją, spustelėkite **Aktyvinti naują versiją**. Kai darbo eiga aktyvi, vartotojai galės pateikti dokumentus apdoroti.
    - Jei šios versijos aktyvinti nenorite, spustelėkite **Neaktyvinti naujos versijos**. Darbo eigą galite suaktyvinti vėliau.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]