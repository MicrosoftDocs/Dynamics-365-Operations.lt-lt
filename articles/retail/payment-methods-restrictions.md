---
title: Grąžinimo mokėjimo metodų be kvito apribojimas
description: Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 22e675fd9b7ee33c89f52ac4c8c15807580b86a7
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935857"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Grąžinimo mokėjimo metodų be kvito apribojimas


[!include [banner](includes/banner.md)]

Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą. Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.

## <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Norėdami nustatyti mokėjimo būdus, turite atlikti toliau nurodytus veiksmus.
1. Sukurkite mokėjimo būdus, priimamus visos organizacijos.
2. Sukurkite visai organizacijai taikomų kortelių tipus ir kortelių numerius. Jei priimamos kredito ar debeto kortelės, turite sukurti vieną mokėjimo būdą, naudojamą atsiskaitant kortelėmis, o po to sukurti visai organizacijai taikomus kortelių tipus ir kortelių numerius.
3. Nustatykite parduotuvės mokėjimo būdus. Susiekite mokėjimo būdus su kiekviena parduotuve, o po to įveskite kiekvienos parduotuvės mokėjimo būdo parametrus.
4. Nustatykite parduotuvių mokėjimo kortelėmis būdus. Nustatykite kiekvieno parduotuvės priimamo mokėjimo kortele būdo kortelę.

![„Retail“ parduotuvės sąranka](media/NoReceiptReturns1.png "„Retail“ parduotuvės sąranka") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Grąžinimo mokėjimo metodų be kvito apribojimas

Puslapyje **Parduotuvės valdymas**, prie parinkties **Grąžinimai be kvito** pasirinkite kiekvieno parduotuvės mokėjimo būdo parametro **Riboti grąžinimus be kvito** į parinktį **Taip**. 

Numatytoji jungiklio reikšmė yra **Ne**, kuri užtikrina, kad mokėjimo būdą galima naudoti grąžinant. 

Kai parametras **Riboti grąžinimus be kvito** nustatytas į parinktį **Taip**, pasirinktas mokėjimo būdas nebus leidžiamas naudoti grąžinant. 

![„Retail“ parduotuvės mokėjimo būdas](media/NoReceiptReturns3.png "„Retail“ parduotuvės mokėjimo būdas") 

> [!NOTE]
> Kai kasininkas pasirenka mokėjimo būdą, kuris yra apribotas naudoti grąžinant be kvito, rodomas pranešimas, kuriame reikia patvirtinti priimtinus mokėjimo būdus.

![Galimi mokėjimo būdai](media/NoReceiptReturns4.png "Galimi mokėjimo būdai") 

Jei operacijai priskiriami grąžinimai su kvitu ir be kvito, apribojimo sąlygos nebus taikomos, nes operacija bus grąžinimo darbo eiga su kvitu. 

