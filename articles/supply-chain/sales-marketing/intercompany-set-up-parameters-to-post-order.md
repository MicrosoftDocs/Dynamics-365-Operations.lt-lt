---
title: Parametrų, skirtų vidinės įmonės užsakymui registruoti, nustatymas
description: Šioje temoje aiškinama, kaip nustatyti parametrus siekiant publikuoti vidinės įmonės užsakymą
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c728f2f491948ae1c8550396ba4d72f76f46fe85
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548422"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Parametrų, skirtų vidinės įmonės užsakymui registruoti, nustatymas

[!include [banner](../../includes/banner.md)]

Kai užregistruojama vidinės įmonės kliento SF, galite nustatyti, kad būtų automatiškai užregistruota vidinės įmonės pirkimo užsakymo ir kliento SF.

> [!NOTE]
> Prieš atlikdami šią procedūrą, nustatykite savo organizacijos spausdinimo valdymą, kad būtų galima nurodyti teisingą SF spausdintuvą. Taip pradinio pardavimo užsakymo SF bus išspausdinta tinkamu spausdintuvu.

Reikia nustatyti šiuos parametrus:

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**. Pasirinkite pardavimo užsakymą, su kuriuo norite dirbti.
1. Pardavimo užsakymo veiksmų srityje pasirinkite **Antraštės rodinį** tada pasirinkite **vidinės įmonės parametrus** „FastTab“ ir atverkite jį.
1. Eikite į veiksmų srityje, skirtuke **Pardavimo užsakymas**, ir tada rinkitės **Redaguoti**.
1. Grįžti prie **vidinės įmonės parametrų** „FastTab“ ir pasirinkite **Tiesioginis pristatymas** tam, kad įgalintumėte tiesioginį pristatymą visoje vidinės įmonės grandinėje (visų užsakymų).
1. Norėdami **įrašyti** pardavimo užsakymą su naujais nustatymais, pasirinkite Įrašyti. Tada pasirinkite **Uždaryti**, kad uždarytumėte pardavimo užsakymą.
1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Tiekėjai \> Visi tiekėjai**. Skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Puslapyje **Vidinė įmonė** rinkitės **Pirkimo užsakymo politikos** nuoroda. Lauko grupėje **Vidinės įmonės pirkimo užsakymo (tiesioginio pristatymo)** rinkitės **Publikuoti sąskaitą automatiškai** ir pašalinkite tikrinimo ženklinimą iš **Spausdinti sąskaitą automatiniu būdu** laukelyje.
1. Lauko grupėje **Originalus pardavimo užsakymas (tiesioginio pristatymo)** rinkitės **Publikuoti sąskaitą automatiškai** laukelyje ir pašalinkite tikrinimo ženklinimą iš **Spausdinti sąskaitą automatiniu būdu** laukelyje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
