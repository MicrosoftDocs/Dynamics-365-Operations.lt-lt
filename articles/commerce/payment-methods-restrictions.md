---
title: Grąžinimo mokėjimo metodų be kvito apribojimas
description: Šiame straipsnyje aprašoma, kaip galima apriboti tam tikrų mokėjimo tipų grąžinimą, jei grąžinimai atliekami be kvito.
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281402"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Grąžinimo mokėjimo metodų be kvito apribojimas


[!include [banner](includes/banner.md)]

Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą. Šiame straipsnyje aprašoma, kaip galima apriboti tam tikrų mokėjimo tipų grąžinimą, jei grąžinimai atliekami be kvito.

## <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Norėdami nustatyti mokėjimo būdus, turite atlikti toliau nurodytus veiksmus.
1. Sukurkite mokėjimo būdus, priimamus visos organizacijos.
2. Sukurkite visai organizacijai taikomų kortelių tipus ir kortelių numerius. Jei priimamos kredito ar debeto kortelės, turite sukurti vieną mokėjimo būdą, naudojamą atsiskaitant kortelėmis, o po to sukurti visai organizacijai taikomus kortelių tipus ir kortelių numerius.
3. Nustatykite parduotuvės mokėjimo būdus. Susiekite mokėjimo būdus su kiekviena parduotuve, o po to įveskite kiekvienos parduotuvės mokėjimo būdo parametrus.
4. Nustatykite parduotuvių mokėjimo kortelėmis būdus. Nustatykite kiekvieno parduotuvės priimamo mokėjimo kortele būdo kortelę.

![Parduotuvės konfigūracija.](media/NoReceiptReturns1.png "„Retail“ parduotuvės sąranka") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Grąžinimo mokėjimo metodų be kvito apribojimas

Už kiekvieną parduotuvės apmokėjimo būdą, puslapyje **Parduotuvės valdymas**, skiltyje **Grąžinimai be kvito**, nustatykite **Grąžinimų be kvito ribojimas** į **Taip**. 

Numatytoji jungiklio reikšmė yra **Ne**, kuri užtikrina, kad mokėjimo būdą galima naudoti grąžinant. 

Kai parametras **Riboti grąžinimus be kvito** nustatytas į parinktį **Taip**, pasirinktas mokėjimo būdas nebus leidžiamas naudoti grąžinant. 

![Mokėjimo būdas parduotuvėje.](media/NoReceiptReturns3.png "„Retail“ parduotuvės mokėjimo būdas") 

> [!NOTE]
> Kai kasininkas pasirenka mokėjimo būdą, kuris yra apribotas naudoti grąžinant be kvito, rodomas pranešimas, kuriame reikia patvirtinti priimtinus mokėjimo būdus.

![Galimi mokėjimo būdai.](media/NoReceiptReturns4.png "Galimi mokėjimo būdai") 

Jei operacijai priskiriami grąžinimai su kvitu ir be kvito, apribojimo sąlygos nebus taikomos, nes operacija bus grąžinimo darbo eiga su kvitu. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
