---
title: Vertinimo šablonai
description: Šioje temoja aprašoma, kaip nustatyti duomenis kainos profiliams.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de5789e1b8e36fc52f308967961fe12389628209ff423e26928d1fb15395a08f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772381"
---
# <a name="rating-profiles"></a>Vertinimo šablonai

Kainos profiliai rodo logistikos sutartį (bet ne teisinę sutartį). Jis naudojamas siekiant nustatyti gabenimo kainas kroviniams. 

Kiekvienas kainos profilis yra unikalus siuntimo vežėjui. Profilyje susiesite siuntimo vežėją su pagrindine kaina. Pagrindinė kaina nustato pagrindinės kainos priskyrimą ir pagrindinę kainą. Pagrindinė kaina nustato vežėjo kainą.

Galite nustatyti kainos profilį naudodami bendrą puslapį, kuriame rodoma esančių kainų profilių apžvalga. Kitu būdu, galite nustatyti kainos profilį tiesiai iš gabenimo vežėjo. Abiem atvejais, jūsų nustatyta informacija kainos profilyje yra tokia pati.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Kredito ar redagavimo kainos profilis kainos profilių puslapyje

Puslapyje **Kainų profiliai** galite peržiūrėti visus esamus kainų profilius. Galite taip pat redaguoti esančius profilius ir sukurti naujus.

1. Eikite į **Gabenimo valdymas \> Nustatymai \> Kainos \> Kainų profilis**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad įtrauktumėte naują kainų profilį į tinklelį ar pasirinkite **Redaguoti** siekiant redaguoti esantį profilį.
1. Naujo ar esančio kainų profilio eilutėje, nustatykite tolesnius laukelius:

    - **Kainų profilis** – Įveskite unikalų numerį (ID) kainų profiliui.
    - **Pavadinimas** – Įveskite kainų profilį aprašantį pavadinimą.
    - **Gabenimo vežėjas** – Pasirinkite gabenimo vežėją. Kainų profilis, kurį nustatote taip pat bus rodomas **Siuntimo vežėjų** puslapyje pasirinktam vežėjui.
    - **Vieta** ir **Sandėlis** – Pasirinkite vietą ir sandėlį.
    - **Kainos variklis** – Pasirinkite kainų variklį reitingo profiliui.
    - **Pagrindinė kaina** – Pasirinkite pagrindinę kainą reitingo profiliui. Galite naudoti pagrindines kainas, kad nustatytumėte pagrindinės kainos tipą ir pagrindinę kainą. Dėl daugiau informacijos, žr. [Nustatyti pagrindines kainas](set-up-rate-masters.md).
    - **Perdavimo laiko variklis** – Pasirinkite perdavimo laiko variklį reitingo profiliui.
    - **Vežėjo kuro indeksas** – Pasirinkite vežėjo kuro indeksą kainų profiliui.
    - **Įsigaliojimo pradžios data ir laikas** ir **Galiojimo pabaigos data ir laikas** – Nustatykite laikotarpį, per kurį kainos profilis turi būti įjungtas.

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Sukurkite kainų profilį tiesiogiai siuntimo vežėjų puslapyje

1. Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.
1. Pasirinkite gabenimo siuntėją sąraše.
1. „FastTab“ **Kainų profiliai** rinkitės **Naujas** tam, kad sukurtumėte kainų profilį.
1. Nustatykite laukelius naujam kainų profiliui. Šie laukeliai atitinka laukelius **Kainų profilio** puslapyje, kaip aprašyta ankstesniame šios temos skyriuje.

> [!NOTE]
> Profiliai sukurti **Siuntimo vežėjų** puslapyje yra taip pat rodomi **Kainų profilių** puslapyje.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]