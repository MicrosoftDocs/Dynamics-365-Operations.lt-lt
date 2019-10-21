---
title: „Power BI“ turinys Faktinis palyginti su biudžeto
description: Šioje temoje aprašomas „Power BI“ turinys Faktinis palyginti su biudžeto. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184398"
---
# <a name="actual-vs-budget-power-bi-content"></a>„Power BI“ turinys Faktinis palyginti su biudžeto

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Faktinis palyginti su biudžeto**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Faktinis palyginti su biudžeto** buvo sukurtas asmenims, kurie organizacijoje yra atsakingi už faktinio našumo stebėjimą palyginti su biudžeto. „Power BI“ turinys **Faktinis palyginti su biudžeto** leidžia matyti biudžeto nuokrypius. Norėdami geriau suprasti nuokrypių priežastį, galite analizuoti einamųjų metų biudžetą pagal sąskaitos kategoriją, biudžeto kodą, pagrindinę sąskaitą, pagrindinės sąskaitos aprašymus arba ataskaitinį laikotarpį.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitos rodomos darbo srityse **Didžiosios knygos biudžetas ir prognozės** ir **CFO**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Tolesnėje lentelėje pateikiama informacija apie metrikas, pateikiamas kiekviename „Power BI“ turinio **Faktinis palyginti su biudžeto** ataskaitų puslapyje.

| Ataskaita                      | Metrika                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Išlaidos - faktinės ir biudžeto | <ul><li>Visos išlaidos šiais metais</li><li>Visos biudžeto išlaidos šiais metais</li></ul>  |
| Įplaukos - faktinės ir biudžeto  | <ul><li>Visos įplaukos šiais metais</li><li>Visos biudžeto įplaukos šiais metais</li><ul>     |
| Išlaidos                     | <ul><li>Visos išlaidos šiais metais</li><li>Išlaidų tikslas pagal biudžetą</li><ul> |
| Įplaukos                     | <ul><li>Visos įplaukos šiais metais</li><li>Įplaukų tikslas pagal biudžetą</li><ul>   |
| Grynosios pajamos                  | <ul><li>Grynosios pajamos šiais metais</li><li>Grynųjų pajamų tikslas pagal biudžetą</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

| Objektas                    | Turinys                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Didžiosios knygos veikla | Didžiosios knygos operacijų sumos                                       |
| Biudžeto veikla         | Biudžeto registro operacijų sumos                                      |
| Pagrindinės sąskaitos             | Pagrindinės sąskaitos, pagal kurias filtruojamos ataskaitos                                               |
| Finansiniai kalendoriai          | Finansiniai metai, pagal kuriuos filtruojamos ataskaitos                                            |
| Didžiosios knygos                   | Didžiosios knygos, kurias galima naudoti norint filtruoti dabartinės didžiosios knygos ataskaitą              |
| Biudžeto kodai              | Biudžeto kodai, pagal kuriuos filtruojamos ataskaitos                                                |
| Juridiniai subjektai            | Juridiniai subjektai, kurias galima naudoti norint filtruoti dabartinio juridinio subjekto ataskaitą |