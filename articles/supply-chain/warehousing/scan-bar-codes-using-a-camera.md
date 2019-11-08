---
title: Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 for Finance and Operations“ – Sandėliavimo programa
description: Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 for Finance and Operations“ – Sandėliavimo programą, kad būtų galima nuskaityti brūkšninius kodus naudojant mobiliojo įrenginio kamerą.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 58cf27a250778d68bdffa1eefa5e939276e467fc
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578154"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Brūkšninių kodų nuskaitymas naudojant kamerą „Dynamics 365 Supply Chain Management“ – Sandėliavimo programa

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti „Dynamics 365 for Finance and Operations“ – Sandėliavimo programą, kad būtų galima nuskaityti brūkšninius kodus naudojant mobiliojo įrenginio kamerą. 

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami naudoti šią funkciją, turite įsidiegti Sandėliavimo programos 1.2.0.0 versiją ir jūsų įrenginyje turi būti kamera. Atidarę programą po atnaujinimo, būsite paraginti leisti programai naudoti kamerą. Jei įrenginyje kameros nėra, raginimas nebus rodomas ir negalėsite naudoti kameros kaip skaitytuvo. 

## <a name="setup"></a>Sąranka
„Warehousing“ programos rodymo parametruose galite pasirinkti, ar leisti naudoti kamerą brūkšniniams kodams nuskaityti. Jei įjungsite **Naudoti kamerą kaip skaitytuvą**, galėsite naudoti kamerą kiekviename įvesties lauke, kuriame kaip pageidaujamas įvesties režimas nustatytas **Nuskaitymas**. 

Norėdami įvesties lauką nustatyti kaip nuskaitomą, puslapyje **Sandėlio programos laukų pavadinimai** nustatykite parametro **Pageidaujamas įvesties režimas** parinktį **Nuskaitymas**. Pasirinkus šią pasirinktį, nuskaitymus „Warehouse“ programoje bus galima atlikti su kamera. Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti laukų pavadinimus programoje „Warehousing“, žr. [Programos „Warehousing“ laukų pavadinimų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

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

