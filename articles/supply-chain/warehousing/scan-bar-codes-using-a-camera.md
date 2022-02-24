---
title: Brūkšninių kodų nuskaitymas sandėlio programėle naudojant kamerą
description: Šioje temoje paaiškinama, kaip nustatyti „Warehousing“ programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965647"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Brūkšninių kodų nuskaitymas sandėlio programėle naudojant kamerą

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti „Warehousing“ programėlę brūkšninių kodų nuskaitymui naudojant mobiliojo įrenginio kamerą. 

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami naudotis šia funkcija, Jūsų įrenginyje turi būti įdiegta „Warehousing“ programėlės 1.2.0.0 versija ir įrenginyje turi būti kamera. Atidarę programą po atnaujinimo, būsite paraginti leisti programai naudoti kamerą. Jei įrenginyje kameros nėra, raginimas nebus rodomas ir negalėsite naudoti kameros kaip skaitytuvo. 

## <a name="setup"></a>Sąranka
„Warehousing“ programėlės Ekrano parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti. Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**. 

Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**. Pasirinkus šią parinktį, „Warehousing“ programėlė naudos kamerą kodų nuskaitymui. Daugiau informacijos apie tai, kaip konfigūruoti „Warehousing“ laukų pavadinimus, rasite [„Warehousing“ programėlės laukų pavadinimų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Palaikomi brūkšninių kodų formatai
Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus. 

## <a name="navigation"></a>Naršymas
Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauke kaip pageidaujamas įvesties režimas bus nustatytas Nuskaitymas. Įjungę kameros puslapį, naršykite naudodami šiuos mygtukus:
- Spustelėkite sugrįžimo mygtuką, jei norite grįžti į užduočių ir informacijos puslapį. 
- Spustelėkite užduočių ir informacijos puslapyje esantį pieštuką, kad pereitumėte į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.
- Spustelėkite užduočių ir informacijos puslapyje esančią kamerą, jei norite grįžti į kameros puslapį. 

| Užduočių ir informacijos puslapis | Kameros puslapis | 
| :---------------------: | :--------------------: |
| ![Kameros nuskaitymo užduočių informacijos puslapio pavyzdys](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameros nuskaitymo kameros mažesnio puslapio pavyzdys](./media/camera-scanning-example-camera-page50.png)          |

Kameros puslapyje spustelėjus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą. Jei per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką. Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.

Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas. Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą. Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis. Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.

