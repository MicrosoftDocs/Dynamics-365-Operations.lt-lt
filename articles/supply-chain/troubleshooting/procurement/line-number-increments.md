---
title: Importuoti pirkimo užsakymai rodo neteisingus eilučių numerius
description: Kai pirkimo užsakymai importuojami naudojant duomenų valdymą, pirkimo užsakymo eilučių numeriai neatitinka sistemos parametruose nurodyto padidėjimo
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477047"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Importuoti pirkimo užsakymai rodo neteisingus eilučių numerius

## <a name="symptoms"></a>Požymiai

Numatyta, kad automatiškai sugeneruoti pirkimo užsakymo eilučių, kurios importuojamos per *Pirkimo užsakymo eilučių V2* duomenų objektą, numeriai nenaudoja sistemos parametruose nurodyto sistemos eilutės numerio padidėjimo. Jei kuriate pirkimo užsakymą rankiniu būdu ir pridedate eilutes per vartotojo sąsają (UI), eilučių numeriai yra padidinami tinkamai. Tačiau jei naudojate duomenų valdymo sistemą (DMF), jie nėra padidinami tinkamai.

Ši problema kyla dėl to, kad importuojant eilutes per DMF, jei eilučių numeriai dar nėra priskirti importuotam subjektui, sistema naudoja DMF metodą jiems priskirti. Šis metodas visada padidina eilučių numerius vienu skaičiumi.

## <a name="workaround"></a>Apėjimo būdas

Įsitikinkite, kad norimų eilučių numeriai jau yra pateikti duomenų subjekto eilutės numerio laukuose, kai importuojate pirkimo užsakymų eilutes. Šiuo atveju DMF neperrašys eilučių numerių.
