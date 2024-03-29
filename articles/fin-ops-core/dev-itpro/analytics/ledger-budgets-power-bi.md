---
title: „Power BI“ turinys Faktinis palyginti su biudžeto
description: Šiame straipsnyje aprašomas faktinio ir biudžeto Power BI turinys. Joje paaiškinama, kaip pasiekti ataskaitas ir pateikiama informacija apie duomenų modelį.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847288"
---
# <a name="actual-vs-budget-power-bi-content"></a>„Power BI“ turinys Faktinis palyginti su biudžeto

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas faktinio **ir biudžeto** Microsoft Power BI turinys. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]