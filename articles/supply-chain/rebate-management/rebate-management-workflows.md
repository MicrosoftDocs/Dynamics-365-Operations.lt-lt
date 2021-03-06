---
title: Grąžinimų valdymo sandorio darbo eigos
description: Šioje temoje paaiškinama, kaip nustatyti grąžinimo valdymo sandorio darbo eigą, skirtą sandorių patvirtinimui ir aktyvavimui.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270962"
---
# <a name="rebate-management-deal-workflows"></a>Grąžinimų valdymo sandorio darbo eigos

[!include [banner](../includes/banner.md)]

Grąžinimo sandorių patvirtinimams grąžinimų valdymas naudoja tą pačią darbo eigos platformą kaip ir kitos „Finance and Operations” programos. Su kiekviena darbo eiga yra susieti du užduočių procesai:

- Kitas darbo eigos elementas patvirtina sandorį.
- Vienas darbo eigos elementas suaktyvina sandorį tam, kad vartotojas arba darbo eigos procesas galėtų patvirtinti operacijas.

Kad būtų galima naudoti grąžinimo sandorį, jis turi būti aktyvus **Grąžinimų valdymo** modulyje. Norėdami aktyvuoti sandorį, pirmiausia turite sukurti ir sukonfigūruoti *Grąžinimų valdymo sandorio darbo eigą*.

Vartotojai negali rankiniu būdu patvirtinti sandorių. Visada privaloma naudoti darbo eigą.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Grąžinimų valdymo sandorio darbo eigų kūrimas ir valdymas

Norėdami dirbti su savo grąžinimų valdymo sandorio darbo eigomis, eikite į **Grąžinimo valdymas \> Nustatymas \> Grąžinimų valdymo darbo eigos**. Ten galite peržiūrėti, kurti ir atnaujinti darbo eigas taip, kaip jums reikia. Tik viena šio tipo darbo eiga gali būti aktyvi tuo pačiu metu. Daugiau informacijos apie darbo eigas, kaip dirbti su **Grąžinimo darbo eigų** puslapių ir kaip kurti darbo eigas, rasite [Darbo eigos sistemos apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ir su ja susijusiose temose.

## <a name="use-a-workflow-to-activate-a-deal"></a>Sandorio aktyvavimas naudojant darbo eigą

Norėdami aktyvuoti sandorį naudodami darbo eigą, atidarykite sandorį (pavyzdžiui, **Visų grąžinimų valdymo sandorių** puslapyje). Tada veiksmų srityje pasirinkite **Darbo eiga \> Pateikti**. Kai naujas sandoris bus apdorotas ir patvirtintas per darbo eigą, jis bus aktyvus ir parengtas naudoti.

Aktyvavę sandorį negalite pakeisti didelės dalies jo nustatymo. Jeigu reikia pakeisti aktyvų sandorį, pirmiausia padarykite jį neaktyvų, o tada sukurkite naują sandorį. Jei naujas sandoris bus panašus į senąjį, galite sukurti jį nukopijuodami seną sandorį.

Galite keisti šiuos sandorio parametrus, kai jį suaktyvinate:

- Derinti pagal
- Kaupiamoji garantija
- Registravimo profilis
- Registravimo šablonas garantijai
- Dokumento pastabos
- Valiuta
- Nuo datos
- Iki datos

Be to, grąžinimų eilutes galima pašalinti.
