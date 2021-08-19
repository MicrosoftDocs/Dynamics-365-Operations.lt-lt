---
title: Produkto varianto matavimo vieneto konvertavimas
description: Šioje temoje paaiškinama, kaip nustatyti produkto variantų matavimo vienetų konvertavimus. Joje pateikiamas nustatymo pavyzdys.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: b9ad41395055d9f63aae8ffa869e0613be330051390955599a95a30869a145dc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713643"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Produkto varianto matavimo vieneto konvertavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti įvairių produkto variantų matavimo vienetų konvertavimus.

Užuot kūrę kelis atskirus produktus, kuriuos reikia prižiūrėti, galite naudoti produkto variantus, kad sukurtumėte vieno produkto variantus. Pavyzdžiui, produkto variantas gali būti nurodyto dydžio ir spalvos marškinėliai.

Anksčiau vienetų konvertavimus buvo galima nustatyti tik bendrajam produktui. Todėl visi produkto variantai turėjo tokias pačias vienetų konvertavimo taisykles. Tačiau kai įjungta funkcija *Produkto variantų matavimo vieneto konvertavimas*, jei jūsų marškinėliai parduodami dėžėse, o marškinėlių skaičius, kurį galima supakuoti dėžėje, priklauso nuo marškinėlių dydžio, dabar galite nustatyti skirtingų marškinėlių dydžių ir pakavimui naudojamų dėžių vienetų konvertavimus.

## <a name="turn-on-the-feature-in-your-system"></a>Funkcijos įjungimas sistemoje

Jeigu šios funkcijos savo sistemoje dar nematote, eikite į dalį [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Produkto variantų matavimo vieneto konvertavimas*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Nustatyti produkto varianto vieneto konvertavimą

Produkto variantus galima kurti tik bendriesiems produktams. Daugiau informacijos žr. [Bendrojo produkto kūrimas](tasks/create-product-master.md). Produktams, kurie nustatyti esamo svorio procesams, funkcija *Produkto variantų matavimo vieneto konvertavimas* negalima.

Norėdami konfigūruoti bendrąjį produktą, kad būtų palaikomas kiekvieno varianto vienetų konvertavimas, atlikite toliau nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**.
1. Kurkite arba atidarykite bendrąjį produktą, jei norite eiti į jo puslapį **Produkto informacija**.
1. Nustatykite parinkties **Įjungti matavimo vienetų konvertavimą** reikšmę kaip *Taip*.
1. Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Vienetų konvertavimas**.
1. Atidaromas puslapis **Vienetų konvertavimas**. Pasirinkite vieną iš toliau nurodytų skirtukų.

    - **Vidiniai klasės konvertavimai** – pasirinkite šį skirtuką, jei norite konvertuoti vienetus, kurie priklauso tai pačiai vieneto klasei.
    - **Tarpklasiniai konvertavimai** – pasirinkite šį skirtuką, jei norite konvertuoti vienetus, kurie priklauso skirtingoms vienetų klasėms.

1. Norėdami įtraukti naują vieneto konvertavimą, spustelėkite **Naujas**.
1. Lauke **Sukurti konvertavimą, skirtą** nustatykite vieną iš toliau nurodytų reikšmių.

    - **Produktas** – jei pasirinksite šią reikšmę, galite nustatyti bendrojo produkto vieneto konvertavimą. Toks vieneto konvertavimas bus naudojamas kaip atsarginis visų produkto variantų, kuriems neapibrėžtas vienetų konvertavimas, konvertavimo būdas.
    - **Produkto variantas** – jei pasirinksite šią reikšmę, galite nustatyti konkretaus produkto varianto vieneto konvertavimą. Norėdami pasirinkti variantą, naudokite lauką **Produkto variantas**.

    ![Naujo vieneto konvertavimo įtraukimas.](media/uom-new-conversion.png "Naujo vieneto konvertavimo įtraukimas")

1. Vienetų konvertavimui nustatyti naudokite kitus pateikiamus laukus.
1. Norėdami įrašyti naują vieneto konvertavimą, pasirinkite **Gerai**.

> [!TIP]
> Produkto arba produkto varianto puslapį **Vienetų konvertavimas** galite atidaryti iš bet kurio iš toliau nurodytų puslapių.
> 
> - Produkto informacija
> - Patvirtintų produktų informacija
> - Patvirtinto produkto variantai

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šiame scenarijuje įmonė parduoda mažo, vidutinio, didelio ir labai didelio dydžio marškinėlius. Marškinėliai apibrėžiami kaip produktas, o skirtingi dydžiai – kaip to produkto variantai. Marškinėliai yra supakuoti dėžėse. Kiekvienoje dėžėje gali būti penkti mažo, vidutinio ir didelio dydžio marškinėliai. Tačiau, jei marškinėliai yra labai didelio dydžio, kiekvienoje dėžėje yra vietos tik keturiems marškinėliams.

Įmonė skirtingus variantus nori sekti pagal vienetą *Vienetai*, tačiau parduoda juos pagal vienetą *Dėžės*. Mažo, vidutinio ir didelio dydžio marškinėlių atsargų vieneto ir pardavimo vieneto konvertavimas yra 1 dėžė = 5 vienetai. Labai didelio dydžio marškinėlių konvertavimas yra 1 dėžė = 4 vienetai.

1. Iš produkto **Marškinėliai** puslapio **Patvirtinto produkto informacija** atidarykite puslapį  **Vienetų konvertavimas**.
1. Puslapyje **Vienetų konvertavimas** nustatykite patvirtinto produkto varianto **Labai didelis** toliau nurodyto vieneto konvertavimą.

    | Laukas                 | Parametras                 |
    |-----------------------|-------------------------|
    | Sukurti konvertavimą, skirtą | Produkto variantas         |
    | Produkto variantas       | Marškinėliai : : Labai didelis : : |
    | Iš vieneto             | Dėžės                   |
    | Koeficientas                | 4                       |
    | Į vienetą               | Dalys                  |

1. Visų produkto variantų **Mažas**, **Vidutinis** ir **Didelis** vienetų *Dėžė* ir *Vienetai* konvertavimas yra toks pat, todėl galite apibrėžti jų bendrojo produkto toliau nurodytą vieneto konvertavimą.

    | Laukas                 | Parametras |
    |-----------------------|---------|
    | Sukurti konvertavimą, skirtą | Produktas |
    | Produktas               | Marškinėliai |
    | Iš vieneto             | Dėžės   |
    | Koeficientas                | 5       |
    | Į vienetą               | Dalys  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Vieneto konvertavimo naujinimas naudojant „Excel“

Jei produktas yra daug produktų variantų, kurie turi skirtingus vienetų konvertavimus, verta eksportuoti vienetų konvertavimus į „Microsoft Excel“ darbaknygę, atnaujinti juos ir tada vėl publikuoti juos „Dynamics 365 Supply Chain Management“.

Norėdami eksportuoti vienetų konvertavimus į „Excel“, puslapio **Vienetų konvertavimas** veiksmų srityje pasirinkite **Atidaryti programoje „Microsoft Office“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Matavimo vienetų valdymas](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]