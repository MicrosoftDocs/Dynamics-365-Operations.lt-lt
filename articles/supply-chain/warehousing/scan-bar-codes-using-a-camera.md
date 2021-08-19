---
title: Brūkšninių kodų nuskaitymas sandėlio valdymo mobiliųjų įrenginių programėle naudojant kamerą
description: Šioje temoje paaiškinama, kaip nustatyti sandėlio valdymo mobiliųjų įrenginių programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 62280b8401c1f7d5dc859a2130981405e69d03cfb5383123d7069e71e6cb1f47
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711668"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Brūkšninių kodų nuskaitymas sandėlio valdymo mobiliųjų įrenginių programėle naudojant kamerą

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti sandėlio valdymo mobiliųjų įrenginių programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.

## <a name="setup"></a>Sąranka

Sandėlio valdymo mobiliųjų įrenginių programėlės rodymo parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti. Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**.

Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**. Pasirinkus šią parinktį, sandėlio valdymo mobiliųjų įrenginių programėlė naudos kamerą kodų nuskaitymui. Daugiau informacijos rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Palaikomi brūkšninių kodų formatai

Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus.

## <a name="navigation"></a>Naršymas

Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauko **Pageidaujamas įvesties režimas** yra nustatytas *Nuskaitymas*, kai būsite kameros puslapyje, naršymui naudokite šias parinktis:

- Pasirinkite sugrįžimo mygtuką, jei norite grįžti į **Užduočių ir išsamios informacijos** puslapį.
- Pasirinkite **Užduočių ir išsamios informacijos** puslapyje esantį pieštuką, jei norite pereiti į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.
- Pasirinkite **Užduočių ir informacijos** puslapyje esančią kamerą, jei norite sugrįžti į kameros puslapį.

Kameros puslapyje pasirinkus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą. Jeigu per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką. Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.

Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas. Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą. Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis. Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]