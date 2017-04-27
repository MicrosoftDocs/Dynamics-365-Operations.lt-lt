---
title: "Savikainos įrašai"
description: "Šiame straipsnyje pateikiama informacija apie savikainos įrašus ir kada jie kuriami. Savikainos įrašas yra toks įrašas, kuris registruoja tam tikro įvykio kiekį ir išlaidas."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 55f5ee731c40acc40e8fe20c24d4ed707fe2c81a
ms.lasthandoff: 03/31/2017


---

# <a name="cost-entries"></a>Savikainos įrašai

Šiame straipsnyje pateikiama informacija apie savikainos įrašus ir kada jie kuriami. Savikainos įrašas yra toks įrašas, kuris registruoja tam tikro įvykio kiekį ir išlaidas.

Išlaidų įrašai yra atsargų operacijų telkimai, įrašyti aktyviose finansinių atsargų dimensijose.

## <a name="examples"></a>Pavyzdžiai
### <a name="example-1-no-cost-entries-are-created"></a>1 pavyzdys: nesukuriama jokių išlaidų įrašų

Registruojamas perkėlimo žurnalo įvykis. Įvykis vieną prekės A vienetą perkelia iš vietos A į vietą B. Vietos atsargų dimensija nelaikoma išlaidų objekto dalimi. Todėl įvykis sukuria dvi atsargų operacijas ir nė vieno išlaidų įrašo.

### <a name="example-2-cost-entries-are-created"></a>2 pavyzdys: sukuriama išlaidų įrašų

Registruojamas perkėlimo žurnalo įvykis. Įvykis vieną prekės A vienetą perkelia iš 1 teritorijos į 2 teritoriją. Teritorijos atsargų dimensija laikoma išlaidų objekto dalimi. Todėl įvykis sukuria dvi atsargų operacijas ir du išlaidų įrašus.

### <a name="example-3-one-cost-entry-is-created"></a>3 pavyzdys: sukuriamas vienas išlaidų įrašas

Registruojamas pirkimo užsakymo produkto gavimo įvykis. Įvykis užregistruoja 100 prekės A vienetų, kurio vieno kaina – 10,00 JAV dolerių (USD). Kadangi prekė A naudoja serijos numerį sekti atsargų valdymo paskirčiai, sukuriamas unikalus kiekvienos gautos prekės serijos numeris. Todėl įvykis sukuria 100 atsargų operacijų ir vieną išlaidų įrašą.

## <a name="cost-entries-page"></a>Išlaidų įrašų puslapis
Naujasis **Išlaidų įrašų** puslapis leidžia peržiūrėti ir valdyti kiekių bei išlaidų registravimą. Šis puslapis papildo **Atsargų operacijos** ir **Atsargų sudengimo** puslapius. Įvykio įrašai registruojami chronologine tvarka. Todėl galite greitai rasti ir valdyti sukauptas konkretaus įvykio ar visų įvykių, susijusių su dokumentu, išlaidas. Toliau pateikiamas pavyzdys.

-   Registruojamas prekės A produkto gavimo įvykis. Gaunama šimtas vienetų, kurio vieno kaina – 10,00 USD.
-   Praėjus kelioms dienoms po SF įvykio registravimo, kaina padidėja iki 11,00 USD. Todėl bendroji suma yra 1 100 USD. Sukuriamas antrasis kvitas, atitinkantis 100 USD skirtumą.
-   Po kelių dienų pirkimo užsakyme registruojamos papildomos 15,00 USD išlaidos, skirtos padengti transportavimo išlaidoms.

| Kvitas | Data       | Nuoroda      | Numeris | Partijos numeris  | Nuorodos partija | Grąžinamos partijos ID | Kiekis | Suma  |
|---------|------------|----------------|--------|---------|---------------|---------------|----------|---------|
| 00001   | 2015-01-01 | Pirkimo užsakymas | 100001 | 0000101 |               |               | 100,00   | 1 000,00 |
| 00002   | 2015-01-20 | Pirkimo užsakymas | 100001 | 0000101 |               |               |          | 100,00  |
| 00003   | 2015-01-31 | Koregavimas     | 100001 | 0000101 |               |               |          | 15,00   |

**Išlaidų įrašų** puslapyje galima filtruoti pagal dokumento ID ir dokumento datą. **Pastaba.** Galimi tik [išlaidų objektų](cost-object.md) arba išleistų produktų išlaidų įrašai.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Išlaidų objektai](cost-object.md)


