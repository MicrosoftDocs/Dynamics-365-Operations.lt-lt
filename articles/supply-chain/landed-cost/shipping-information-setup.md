---
title: Siuntimo informacijos sąranka
description: Šioje temoje aprašoma, kaip nustatyti siuntimo informaciją modulyje Iškrovimo kaina.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1ee099b923f3e2140f7f6962795fc6b6e87b913a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690308"
---
# <a name="shipping-information-setup"></a>Siuntimo informacijos sąranka

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti siuntimo informaciją modulyje **Iškrovimo kaina**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Prekių aprašas

Prekių aprašymai padeda identifikuoti reisą, gabenimo konteinerį arba prekių sąskaitos lapą ir jame aprašytas prekes. Galite pasirinkti prekių aprašymą gabenimo konteinerio antraštėje arba sąskaitos lapo antraštėje.

Norėdami dirbti su prekių aprašymais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Prekių aprašymas**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti prekių aprašymo įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Prekių aprašas | Įvesti unikalų prekių, kurioms bus naudojamas šis aprašymas, tipo identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite šios kategorijos prekių tipo aprašymą. |

## <a name="vessels"></a><a name="vessels"></a>Transporto priemonės

Transporto priemonė yra unikalus transporto priemonės, kurią naudoja siuntimo įmonė ar agentūra, pavadinimas. Kurdami reisą, visada turite pasirinkti arba įvesti jo transporto priemonės pavadinimą. Jei dažnai naudojate tas pačias transporto priemones, galite greičiau ir paprasčiau sukurti naują reisą, sukurdami kiekvienos transporto priemonės įrašą ir taip leisdami vartotojams pasirinkti iš sąrašo, o ne kaskart rankiniu būdu įvesti pavadinimą arba numerį.

Norėdami dirbti su transporto priemonėmis, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Transporto priemonės**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti transporto priemonių įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Transporto priemonė | Įvesti unikalų laivo, kuris bus naudojamas prekėms gabenti reiso metu, identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite transporto priemonės aprašą. Paprastai šiame aprašyme nurodomas laivo pavadinimas ir siuntimo įmonė / agentūra. |
| Pristatymo būdas | Pasirinkite transporto priemonės naudojamą pristatymo būdą (pvz., _Oru_, _Vandeniu_, or _Traukiniu_). |

## <a name="exporters"></a>Eksportuotojai

Kiekvienas eksportuotojo įrašas identifikuoja tiekėją arba eksportuotoją, kurį galima nurodyti kaip reiso tiekėją. Eksportuotojas gali būti susietas su reisu ir naudojamas ataskaitoms.

Norėdami dirbti su eksportuotojais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Eksportuotojai**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti eksportuotojų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Eksportuotojas | Įvesti unikalų reiso metu gabenamų prekių eksportuotojo identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite eksportuotojo aprašą. Paprastai šiame aprašyme nurodomas pilnas siuntimo įmonės / agentūros pavadinimas. |

## <a name="commodity-codes"></a>Prekių kodai

Prekių kodus naudojate norėdami padėti atlikti muitinės identifikavimą ir apskaičiuoti reiso prekių muito mokesčio tarifus. Prekių kodus galite pasirinkti puslapyje **Išleisti produktai**.

Norėdami dirbti su prekių kodais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Prekių kodai**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti prekių kodų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Prekės kodas | Įvesti unikalų šio prekės tipo kodą. |
| Aprašymas | Įveskite prekės tipo aprašymą. |

## <a name="customs-description"></a>Muitinės aprašymas

Muitinės aprašymai padeda identifikuoti prekes muitinės tikslais. Muitinės aprašymą galite pasirinkti puslapyje **Išleisti produktai** arba pirkimo užsakymo eilutėse.

Norėdami dirbti su muitinės aprašymais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Muitinės aprašymas**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti muitinės aprašymo įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Muitinės aprašymas | Įvesti unikalų šio muitinės klasifikavimo tipo kodą. Dažnai šis kodas yra oficialus aprašymas, kurį pateikia muitinė, skirtas prekių aprašymui ir kokybinei vertei nustatyti. |
| Aprašymas | Įveskite muitinės klasifikavimo aprašą. |
