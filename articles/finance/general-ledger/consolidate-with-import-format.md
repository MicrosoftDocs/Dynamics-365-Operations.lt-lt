---
title: Importuoti formatą konsolidavimui
description: Šioje temoje pateikta išsami informacija apie importavimo formatą, kuris naudojamas jums konsoliduojant finansinius duomenis iš įvairių juridinių asmenų.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: e3124ac0e161e003986d7e167e292cbb374e1bfa
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085455"
---
# <a name="import-format-for-consolidation"></a>Importuoti formatą konsolidavimui

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta išsami informacija apie importavimo formatą, kuris naudojamas jums konsoliduojant finansinius duomenis iš įvairių juridinių asmenų. Importavimo formatas turi būti įrašomas kaip tekstas (.txt) failas.

## <a name="import-format"></a>Importavimo formatas

Tolesnėje lentelėje yra importavimo formatai, kuriuos turėtumėte naudoti konsoldavimo metu importuodami.

| Įrašo lentelė | Formatuoti | Pastabos |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Įrašo lentelė</li><li>Šaltinio pagrindinės paskyros ID</li><li>Pagrindinės paskyros eilutė</li><li>Pagrindinės paskyros tipas</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Pagrindinės paskyros ID</li><li>Transakcijos data</li><li>Mokestinio laikotarpio tipas (**0** = Atidarymas, **1** = Veikimas ir **2** = Uždarymas)</li><li>Operacijos valiuta</li><li>Debito ar kredito (**0** = Debitas ir **1** = Kreditas)</li><li>Publikavimo sluoksnis</li><li>Transakcijos sumos</li><li>Kiekis</li><li>Vietinis RecID (dviprasmiškas, unikali int64 vertė transakcijai)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Objekto skaičius (biudžeto antraštės transakcijos skaičius)</li><li>Biudžeto antraštės numatytoji data</li><li>Biudžeto modelio ID</li><li>Integruojančios vertės transakcijos tipui numeravimas (tuščias, originalus biudžetas ir t.t.)</li><li>Eiltuės data</li><li>Pagrindinės paskyros ID eilutei</li><li>Valiutos kodas eilutei</li><li>Eilutės kiekis transakcijos valiutoje</li><li>Integruojančios vertės biudžeto tipo eilutei numeravimas (išlaidų ar pajamų)</li></ul> |
| 4            | DEMF | „RecordCompany“ yra šaltinio juridinis asmuo. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Pagrindinės sąskaitos ID</li><li>Operacijos data</li><li>Ataskaitinio laikotarpio tipas (0 – Atidarymo, 1 – Veikimo ir 2 – Uždarymo)</li><li>Operacijos valiuta</li><li>Debetas ar Kreditas (0 – Debetas ir 1 – Kreditas)</li><li>Registravimo sluoksnis</li><li>Operacijos suma</li><li>Kiekis</li><li>Vietinis recid (dviprasmiška, unikali, int64 operacijos reikšmė)</li></ul>  |
| 6            | Verslo struktūros vienetas – 1, Skyrius – 2 | Finansinės dimensijos atributai, kurie nustatomi segmento tvarkoje.<p>Galite naudoti **Eksportuoti** puslapį, kad patvirtintumėte, kaip atributai nustatomi.</p> |
| 7            | 002,1,658 | <ul><li>Finansinės dimensijos vertė</li><li>FInansinė dimensija kaip indeksas, kuris pateiktas Įrašo dimensijose</li><li>Kaip dviprasmiškas, unikalus įrašo ID, kuris susietas su unikaliu įrašo ID iš „RecordTrans“ ar „RecordTrans2“</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensijos vertės, kurios susietos su transakcija iš „RecordBudget“</li><li>FInansinė dimensija kaip indeksas, kuris pateiktas Įrašo dimensijose</li><li>Dviprasmiškas eilutės įrašo ID, kuris yra suderintas su transakcijos eilučių užsakymu faile</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
