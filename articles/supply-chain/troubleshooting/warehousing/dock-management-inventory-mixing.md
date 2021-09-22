---
title: Naudojant rampos valdymo šabloną, naudojami skirtingų atsargų tipai
description: Norint, kad rampos valdymo profilis efektyviai valdytų atsargų maišymą, reikia nustatyti darbo antraštės lūžį pirma. Šiame puslapyje paaiškinama, kaip tai padaryti.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477076"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Inventoriaus tipai sumaišyti, naudojami skirtingų atsargų tipai

## <a name="symptoms"></a>Požymiai

Jūs naudojate *siuntos konsolidacijų strategijas*. Nustatėte *rampos valdymo profilį* kaip *vietos profilį*, tačiau sukūrus darbą, atsargų tipai susimaišo galutinėje vietoje.

## <a name="resolution"></a>Sprendimas

Rampos valdymo profiliai reikalauja iš anksto suskaidyti darbą. Kitaip tariant, rampos valdymo profilis tikisi, kad darbo antraštėje nebus kelių padėjimo vietų.

Norint, kad rampos valdymo profilis efektyviai valdytų atsargų maišymą, reikia nustatyti darbo antraštės lūžį.

Šiame pavyzdyje mūsų rampos valdymo profilis sukonfigūruotas taip, kad **Atsargų tipai, kurių negalima maišyti** būtų nustatytas į *Siuntos ID*, o mes jam nustatysime darbo antraštės lūžį:

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Pasirinkite **Darbo užsakymo tipą** redagavimui (pavyzdžiui, *Pirkimo užsakymai*).
1. Pasirinkite darbo šabloną redagavimui.
1. Veiksmų srityje pasirinkite **Redaguoti užklausą**.
1. Atidarykite **Rikiavimo** skirtuką ir pridėkite eilutę su šiais parametrais:
    - **Lentelė** - *Laikinos darbo operacijos*
    - **Išvestinė lentelė** - *Laikinos darbo operacijos*
    - **Laukas** - *Siuntos ID*
1. Pasirinkite **Gerai**.
1. Grįžtate į **Darbo šablonų** puslapį. Veiksmų juostoje pasirinkite **Darbo antraštės lūžiai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Pasirinkite žymės langelį, susietą su **Lauko pavadinimo** *Siuntos ID*.
1. Veiksmų srityje pasirinkite **Įrašyti**.
