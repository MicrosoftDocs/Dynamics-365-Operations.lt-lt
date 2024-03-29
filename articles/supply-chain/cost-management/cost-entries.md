---
title: Savikainos įrašai
description: Šiame straipsnyje pateikiama informacija apie savikainos įrašus ir kada jie kuriami. Savikainos įrašas yra toks įrašas, kuris registruoja tam tikro įvykio kiekį ir išlaidas.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07e0e5f2e579d81fc96e1e03a2c63aea4c5c956f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673276"
---
# <a name="cost-entries"></a>Savikainos įrašai

[!include [banner](../includes/banner.md)]

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

| Kvitas | Data       | Nuoroda      | Skaičius | Partijos numeris  | Kiekis | Suma  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 2015-01-01 | Pirkimo užsakymas | 100001 | 0000101 | 100,00   | 1 000,00 |
| 00002   | 2015-01-20 | Pirkimo užsakymas | 100001 | 0000101 |          | 100,00  |
| 00003   | 2015-01-31 | Koregavimas     | 100001 | 0000101 |          | 15,00   |

**Išlaidų įrašų** puslapyje galima filtruoti pagal dokumento ID ir dokumento datą. 

> [!NOTE]
> Galimi tik [išlaidų objektų](cost-object.md) arba išleistų produktų išlaidų įrašai.

## <a name="additional-resources"></a>Papildomi ištekliai

[Savikainos objektai](cost-object.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]