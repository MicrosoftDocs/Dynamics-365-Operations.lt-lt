---
title: Sandėlio atsargų koregavimas
description: Šioje temoje pateikiama informacija apie sandėlio atsargų koregavimo žurnalą ir apdorojimą, kai naudojate skalės vienetus.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938231"
---
# <a name="warehouse-inventory-adjustment"></a>Sandėlio atsargų koregavimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sandėlio atsargų keitimo funkcija yra naudojama, kai paleisti debesies ir kraštų [skalės vienetai, skirti gamybos darbo krūviui](cloud-edge-workload-manufacturing.md) ir [sandėlio valdymo darbo](cloud-edge-workload-warehousing.md) krūviui.

Kai darbuotojas koreguoja atsargas naudodamas sandėlio programą dėl skalės vieneto sandėlio valdymo darbo krūvio, sandėlio atsargų koregavimo žurnalo paketinė užduotis turi apdoroti faktiškai turimų atsargų atnaujinimą, kurį vykdote ir suplanuokite nueidami į  **Sandėlio** valdymas **> Periodinės užduotys > Sandėlio atsargų koregavimo** žurnalas.

Toliau nurodyti sandėlio programos darbo procesai šiuo metu naudoja **sandėlio atsargų koregavimo žurnalą** dėl skalės vieneto darbo krūvių:

- Keitimas (į/iš)
- Ciklo skaičiavimas
- Numerio lentelės įkėlimas

Kelios atsargų operacijos sukuriamos kaip debesies ir krašto dalis atsargų koregavimo procese, nes centro ir svarstyklių vienetų diegimas bendrai naudojamas atsargų įrašuose.

## <a name="inventory-adjustment-example"></a>Atsargų koregavimo pavyzdys

Šiame pavyzdyje sandėlio darbuotojas naudojo sandėlio programą, kad galėtų užregistruoti turimų atsargų kiekį.

Pirma, skalės vieneto darbo krūvis sukuria teigiamo faktinio koregavimo sandėlio atsargų koregavimo operaciją, kuri tada sinchronizuojama su centru ir padidina turimų atsargų kiekį centre.

| Tipas                                    | Skalės vienetas | Kryptis | Tranzito punktas |
|-----------------------------------------|------------|-----------|-----|
| Sandėlio atsargų koregavimas          | +1         | ->        | +1  |

Tada centras apdoroja skaičiavimo žurnalo registravimą, kuris gaunamas naudojant pranešimų [procesoriaus](cloud-edge-message-processor-messages.md) pranešimus. Taip atnaujinamos papildomos turimos atsargos. Siekiant išvengti dvigubo turimų atsargų kiekio, centras kaip šio proceso dalį sukuria korespondentinę operaciją ir pašalina anksčiau įrašytas turimų atsargų, susijusių su sandėlio atsargų koregavimu, atsargas.

| Tipas                                    | Skalės vienetas | Kryptis | Tranzito punktas |
|-----------------------------------------|------------|-----------|-----|
| Inventorizacija                                | +1         | <-        | +1  |
| Sandėlio atsargų koregavimas (korespondentinė sąskaita) | -1         | <-        | -1  |

Kai svarstyklių vienetas sukuria sandėlio atsargų koregavimo žurnalą centre, galite peržiūrėti inventorizacijos žurnalą ir korespondentinį žurnalą, kurie kuriami centro kaip koregavimo **koregavimo** **proceso** **dalis**.

Galite peržiūrėti visus šiuos žurnalo įrašus ir „Supply Chain Management“ operaciją atlikdami šiuos veiksmus:

1. Prisiregistruokite svarstyklių vienetais.
1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Sandėlio atsargų reguliavimo žurnalas**.
1. Sandėlio **atsargų koregavimo žurnalo puslapyje** raskite ir atidarykite žurnalą, kuriame įrašytas turimų atsargų pakeitimas. Žurnalo **eilučių skyriuje rodomi visi šio** žurnalo įrašyti koregavimai.
1. Prisiregistruoti prie centro.
1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Sandėlio atsargų reguliavimo žurnalas**.
1. Sandėlio atsargų koregavimo žurnalo puslapyje turite matyti tą patį žurnalą, jei **sinchronizuotas** centro ir svarstyklių vienetas.
1. Atidaryti žurnalą. Jei pranešimų [procesoriaus pranešimai apdoroti, antraštėje matysite saitus su inventorizacijos](cloud-edge-message-processor-messages.md) **žurnalu** ir **korespondentinio** žurnalu.
    - Inventorizacijos **žurnale** turi būti tos pačios dimensijų vertės kaip žurnalo eilutės.
    - Korespondentinis **žurnalas** turi rodyti korespondentinę sąskaitą, kuri pašalina dvigubą atsargų koregavimą.
    > [!NOTE]
    > Kai visi sinchronizuojami ir apdorojami, inventorizacijos žurnalas ir korespondentinis **žurnalas** sinchronizuojami **atgal** į svarstyklių vienetą. Juos taip pat galima peržiūrėti reikiamo **sandėlio atsargų koregavimo žurnalo** puslapyje.
