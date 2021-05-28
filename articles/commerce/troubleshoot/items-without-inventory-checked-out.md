---
title: Galima atsiskaityti už prekes, kurių nėra atsargose
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti klientams įtraukti ne atsargose esančias prekes į savo krepšelį ir vykdyti pirkimo užbaigimą.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018463"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Galima atsiskaityti už prekes, kurių nėra atsargose

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti klientams įtraukti ne atsargose esančias prekes į savo krepšelį ir vykdyti pirkimo užbaigimą.

## <a name="description"></a>Aprašymas

Vartotojai gali įtraukti prekę į savo krepšelį, net jei parduotuvėje nėra turimų atsargų, o tada pereiti į pirkimo užbaigimo puslapį.

## <a name="resolution"></a>Sprendimas

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>„Commerce” svetainių daryklėje įjungti ypatybę Rodyti neturimų atsargų klaidas

Norėdami „Commerce” svetainių daryklėje įjungti ypatybę **Rodyti neturimų atsargų klaidas**, atlikite šiuos veiksmus.

1. Pasirinkite svetainę, su kuria dirbate.
1. Kairiojoje naršymo srityje pasirinkite **Puslapiai**.
1. Pasirinkite **Krepšelio puslapis**, kad jį atidarytumėte.
1. Pasirinkite vietą **Krepšelis 1**, pasirinkite **Redaguoti**, tada ypatybių srityje pažymėkite žymės langelį **Rodyti neturimų atsargų klaidas**.
1. Įrašykite ir publikuokite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atsargų parametrų taikymas](../inventory-settings.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](../calculated-inventory-retail-channels.md)

[Atsargų buferių ir atsargų lygių konfigūravimas](../inventory-buffers-levels.md)
