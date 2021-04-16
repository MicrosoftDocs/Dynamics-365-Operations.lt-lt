---
title: Kliento kredito grupės
description: Šioje temoje pateikiama informacijos apie klientų kredito grupes.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835321"
---
# <a name="customer-credit-groups"></a>Kliento kredito grupės

[!include [banner](../includes/banner.md)]

Galite apibrėžti klientų grupes, kurių kredito limitas yra bendrai naudojamas. Taip pat nagrinėjamas individualus kredito limitas, apibrėžtas kliento SF sąskaitoje.

Kliento kredito grupės nariai gali būti pasirenkami iš skirtingų juridinių subjektų. Kai į kliento kredito grupę įtraukiate klientą į klientų sąrašą klientų kredito grupėje, kiekvieno kliento kredito limito galiojimo data pakeičiama į galiojimo datą, kuri priskirta grupei.

Puslapyje **Klientų kredito grupės** galite nustatyti klientų kredito grupes (**Kreditų valdymo \> Klientų kredito grupės \> Klientų kredito grupės**).

1. Laukuose **Grupės numeris** ir **Aprašas** įveskite grupės identifikatorių ir aprašą.
2. Laukuose **Kedito limitas** ir **Valiuta** įveskite kredito limitą ir valiutą, kuri turėtų būti naudojama, kai sistema patikrina visų grupės narių kredito limitą.
3. Lauke **Kredito limito pabaigos data** įveskite datą, kada baigiasi kredito limito galiojimo laikas. Klientų kredito grupės turi turėti galiojimo datą.

Kai baigsite nustatyti klientų kredito grupę, į ją galite įtraukti klientų nurodydami jų juridinį subjektą ir kliento sąskaitos ID. Kai į klientų kredito grupę įtraukiate naują klientą, sistema ieško to paties kliento sąskaitos visuose juridiniuose subjektuose ir paragina ją įtraukti į klientų kredito grupę.

Norėdami peržiūrėti išsamią informaciją apie visų SF klientų, esančių kliento kredito grupėje, skirstymo pagal terminus balansą, naudokite meniu **Suskirstyti pagal terminus balansai**. Puslapyje **Suskirstyti pagal terminus balansai** pateikiama SF kliento sąskaitų pagal terminus suskirstytų balansų suvestinė.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]