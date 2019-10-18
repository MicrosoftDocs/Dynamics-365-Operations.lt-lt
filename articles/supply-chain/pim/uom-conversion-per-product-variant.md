---
title: Produkto varianto matavimo vieneto konvertavimas
description: Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 196b68db02867f8d864be8bcc593aa01f554f7c3
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249453"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Produkto varianto matavimo vieneto konvertavimas

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

Šioje temoje paaiškinama, kaip galima nustatyti produkto variantų matavimo vienetą. Joje pateikiamas nustatymo pavyzdys.

Ši funkcija leidžia įmonėms nustatyti skirtingų vienetų konvertavimą tarp to paties produkto variantų. Šioje temoje naudojamas toliau pateiktas pavyzdys. Įmonė parduoda mažo, vidutinio, didelio ir labai didelio dydžio marškinėlius. Marškinėliai apibrėžiami kaip produktas, o skirtingi dydžiai – kaip produkto variantai. Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri. Įmonė nori sekti skirtingų variantų marškinėlius pagal vienetą **Vienetai**, tačiau pardavinėja marškinėlius pagal vienetą **Dėžės**. Konvertavimo santykis tarp atsargų vieneto ir pardavimo vieneto yra 1 dėžė = 5 vienetai, išskyrus labai didelio dydžio variantą, kur santykis yra 1 dėžė = 4 vienetai.

## <a name="setup"></a>Sąranka

Galite konfigūruoti parametrus naudodami funkciją, skirtą produktams, kurie įgalinti **visiems procesams**, arba tik produktui, kuris įgalintas **sandėlio procesams**, naudodami parinktį **Įgalinti matavimo vieneto konvertavimą**, esančią puslapyje **Produkto informacijos parametrai**.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Nustatyti produkto varianto vieneto konvertavimą

Produkto variantus galima kurti tik produktams, kurių **Produkto potipis**: **Bendrasis produktas**. Daugiau informacijos žr. [Bendrojo produkto kūrimas](tasks/create-product-master.md).

Funkcija neįgalinta produktams, kurie nustatyti esamo svorio procesams. 

Kuriant bendrąjį produktą, matavimo vieneto konvertavimas įgalinamas naudojant parinktį **Įgalinti matavimo vieneto konvertavimą**, esančią puslapyje **Produkto informacija**.

Sukūrus bendrąjį produktą su išleistų produktų variantais, galima nustatyti vieneto konvertavimą pagal variantus. Galite rasti meniu elementą vieneto konvertavimo puslapiui atidaryti pagal toliau nurodytuose puslapiuose esantį produktą arba produkto variantą.

-   Puslapis **Produkto informacija**
-   Puslapis **Išleistų produktų informacija**
-   Puslapis **Išleisto produkto variantai**

Atidarydami puslapį **Vieneto konvertavimas** pagal bendrąjį produktą arba išleisto produkto variantą, galite pasirinkti, ar norite nustatyti produkto arba produkto varianto vieneto konvertavimą. Tai atlikti galite pasirinkdami **Produkto variantas** arba **Produktas** lauke **Sukurti konvertavimą, skirtą**.

### <a name="product-variant"></a>Produkto variantas

Pasirinkę **Produkto variantas**, galite pasirinkti, kuriam variantui norite nustatyti vieneto konvertavimą lauke **Produkto variantas**.

### <a name="product"></a>Produktas

Pasirinkę **Produktas**, galite nustatyti bendrojo produkto vieneto konvertavimą. Šis vieneto konvertavimas bus taikomas visiems produkto variantams, kurių vieneto konvertavimas neapibrėžtas.

### <a name="example"></a>Pavyzdys

Bendrasis produktas **Marškinėliai** turi keturis išleistų produktų variantus: mažą, vidutinį, didelį ir labai didelį. Marškinėliai supakuoti dėžėse, o vienoje dėžėje jų gali būti penkeri, išskyrus labai didelio dydžio marškinėlius, kurie į dėžę telpa tik ketveri.

Pirmiausia atidarykite puslapį **Vieneto konvertavimas**, esantį **marškinėliams** skirtame išleisto produkto informacijos puslapyje.

Puslapyje **Vieneto konvertavimas** nustatykite išleisto produkto varianto Labai didelis vieneto konvertavimą.

| **Laukas**             | **Parametras**             |
|-----------------------|-------------------------|
| Sukurti konvertavimą, skirtą | Produkto variantas         |
| Produkto variantas       | Marškinėliai : : Labai didelis : : |
| Iš vieneto             | Dėžės                   |
| Koeficientas                | 4                       |
| Į vienetą               | Dalys                  |

Išleisto produkto variantų Mažas, Vidutinis ir Didelis vieneto konvertavimas tarp vieneto dėžės ir vienetų yra toks pat, o tai reiškia, kad galite nustatyti šių bendrojo produkto variantų vieneto konvertavimą.

| **Laukas**             | **Parametras** |
|-----------------------|-------------|
| Sukurti konvertavimą, skirtą | Produktas     |
| Produktas               | Marškinėliai     |
| Iš vieneto             | Dėžės       |
| Koeficientas                | 5           |
| Į vienetą               | Dalys      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Vieneto konvertavimo naujinimas naudojant „Excel“

Jei produktas turi daug produkto variantų su skirtingų vienetų konvertavimu, naudinga eksportuoti vienetų konvertavimą iš puslapio **Vienetų konvertavimas** į „Excel“ skaičiuoklę, atnaujinti konvertavimą ir tada jį publikuoti Tiekimo grandinės valdyme.

Parinktis eksportuoti į „Excel“ ir vėl publikuoti redagavimą Tiekimo grandinės valdyme įgalinama per meniu elementą **Atidaryti naudojant „Microsoft Office“**, esantį Veiksmų srities puslapyje **Vienetų konvertavimas**.
