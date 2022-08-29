---
title: Įgalinti visuotinio išskaitomo mokesčio valiutos kurso tipo ir datos tipo nustatymą
description: Šiame straipsnyje paaiškinama, kaip įgalinti bendrą išskaitomo mokesčio valiutos kurso tipo ir datos tipo nustatymą.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229982"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Įgalinti visuotinio išskaitomo mokesčio valiutos kurso tipo ir datos tipo nustatymą

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Šiame straipsnyje paaiškinama, kaip įgalinti bendrą išskaitomo mokesčio valiutos kurso tipo ir datos tipo nustatymą. Dabar galite pasirinkti išskaitomo mokesčio valiutos paskirtą valiutos kurso tipą ir valiutos kurso skaičiavimo datos tipą. Šie pasirinkimai nustato užsienio valiutos kursą, naudojamą skaičiuojant išskaitomo mokesčio sumą mokėjimo operacijų metu išskaitomo mokesčio valiuta.

Šią funkciją galima naudoti Microsoft Dynamics 365 finansinėse versijose 10.0.29 ir vėlesnėje versijoje.

1. Eiti į **Mokesčių** \> **nustatymo** \> **parametrus** \> **DK parametrai.**
2. Skirtuke **Išskaitomas mokestis** nustatykite parinktį **Įgalinti išplėstinio išskaitomo mokesčio valiutos pasirinktį** **Taip**.
3. **Lauke Valiutos kurso tipas** pasirinkite išskaitomo mokesčio valiutos kurso tipą.
4. Lauke Skaičiavimo **datos tipas pasirinkite** skaičiavimo datos tipą, nustatantį išskaitomo mokesčio valiutos kursą:

    - **Mokėjimo data** – nustato valiutos kursą pagal mokėjimo žurnalo registravimo datą.
    - **SF data** – nustatykite valiutos kursą, remiantis SF žurnalo SF data. Jei kvito SF datos nėra, bus naudojama SF registravimo data. 
    - **Dokumento data** – nustatykite valiutos kursą, remiantis mokėjimo žurnalo dokumento data. Jei kvito dokumento datos nėra, bus naudojama mokėjimo data.

5. Pasirinkite **Įrašyti**.

Jei operacijos valiuta skiriasi nuo išskaitomo mokesčio valiutos, nustatytos išskaitomo mokesčio kode, suma, nurodyta išskaitomo mokesčio valiuta, bus apskaičiuota pagal operacijos valiutą, remiantis ankstesniais nustatymais, ir bus įrašyta užregistruotų išskaitomo mokesčio operacijose.
