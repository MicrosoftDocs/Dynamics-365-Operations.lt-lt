---
title: "Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 for Finance and Operations“ versijoje „Warehousing“"
description: "Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 for Finance and Operations“ versiją „Warehousing“, kad būtų galima nuskaityti brūkšninius kodus su mobiliojo įrenginio kamera."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: lt-lt
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 for Finance and Operations“ versijoje „Warehousing“

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 for Finance and Operations“ versiją „Warehousing“, kad būtų galima nuskaityti brūkšninius kodus su mobiliojo įrenginio kamera. 

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami naudoti šią funkciją, turite turėti įdiegtą 1.2.0.0 „Warehousing“ versiją ir jūsų įrenginys turi turėti kamerą. Atidarę programą po atnaujinimo, būsite paraginti leisti „Dynamics 365 for Finance and Operations“ versijos „Warehousing“ programai naudoti kamerą. Jei įrenginyje kameros nėra, raginimas nebus rodomas ir negalėsite naudoti kameros kaip skaitytuvo. 

## <a name="setup"></a>Sąranka
„Warehousing“ programos rodymo parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti. Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**. 

Norėdami įvesties lauką padaryti nuskaitomą, „Dynamics 365 for Finance and Operations“ programos puslapyje **„Warehouse“ programos laukų pavadinimai** esančiam **Pageidaujamam įvesties režimui** nustatykite parinktį **Nuskaitymas**. Pasirinkus šią pasirinktį, nuskaitymus „Warehouse“ programoje bus galima atlikti su kamera. Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti laukų pavadinimus programoje „Warehousing“, žr. [Programos „Warehousing“ laukų pavadinimų konfigūravimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Palaikomi brūkšninių kodų formatai
Palaikomi dažniausi brūkšninių kodų formatai, įskaitant kodą 128, kodą 39, kodą 93, EAN-8, EAN-13, UPC-E, UPC-A ir QR kodus. 

## <a name="navigation"></a>Naršymas
Kameros puslapis bus paleistas kiekviename puslapyje, kurio įvesties lauke kaip pageidaujamas įvesties režimas bus nustatytas Nuskaitymas. Įjungę kameros puslapį, naršykite naudodami šiuos mygtukus:
- Spustelėkite sugrįžimo mygtuką, jei norite grįžti į užduočių ir informacijos puslapį. 
- Spustelėkite užduočių ir informacijos puslapyje esantį pieštuką, kad pereitumėte į puslapį, kuriame galėsite įvesti informaciją rankiniu būdu.
- Spustelėkite užduočių ir informacijos puslapyje esančią kamerą, jei norite grįžti į kameros puslapį. 

| Užduočių ir informacijos puslapis | Kameros puslapis | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

Kameros puslapyje spustelėjus kameros mygtuką, jis bus rodomas blankesne spalva, kai bus bandoma identifikuoti brūkšninį kodą. Jei per 5 sekundes brūkšninis kodas nebus identifikuotas, procesas bus sustabdytas ir vėl bus galima naudoti kameros mygtuką. Tada galėsite bandyti nuskaityti brūkšninį kodą dar kartą.

Nukreipę kamerą brūkšninį kodą, laikykite brūkšninį kodą tarp rėmelių, kad būtų geriausias rezultatas. Kai brūkšninis kodas nuskaitomas sėkmingai, bus apdorojamas rezultatas ir būsite nukreipti atlikti kitą veiksmą. Jei kitame veiksme bus kitas įvesties laukas, kur kaip pageidaujamas įvesties režimas nustatytas Nuskaitymas, vėl bus atidarytas kameros puslapis. Jei kitame veiksme nebus nuskaitymo lauko, tada kameros puslapis nebus atidarytas.


