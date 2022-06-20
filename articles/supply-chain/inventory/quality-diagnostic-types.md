---
title: Neatitikimų diagnostikos tipai
description: Šiame straipsnyje aprašoma, kaip naudoti ir kurti diagnozės tipus, kurie gali būti naudojami su neatitiktimis.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b7a051f807c9faab3169d2672d47f663892225
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852453"
---
# <a name="diagnostic-types-for-nonconformances"></a>Neatitikimų diagnostikos tipai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti ir kurti diagnozės tipus, kurie gali būti naudojami su neatitiktimis.

Naudodami puslapį **Diagnostikos tipai** nurodykite diagnostikos veiksmų klasifikaciją. Tada, kai sukuriate neatitikties pataisymą, pasirenkate diagnostiką. Koregavimu nurodoma, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, ir kas turėtų imtis veiksmų. Juo taip pat nurodoma pageidaujama užbaigimo data ir planuojama užbaigimo data.

## <a name="examples-of-diagnostic-types"></a>Diagnostikos tipų pavyzdžiai:

Jūs dirbate gamybos įmonei ir kelių prekių kokybės bandymai nesėkmingi. Šios prekės perkeliamos į sulaikymo sritį ir pažymėtos kaip neatitikties produktai. Sukuriamas neatitikties įrašas taip, kad „Microsoft Dynamics 365 Supply Chain Management“ būtų galima stebėti išsamią informaciją naudojant išdavimo sprendimą.

Tokiu atveju kokybės problemos atsiranda dėl to, kad gamybos mašinos, kuri pakuoja prekes, buvo blogos ir yra per daug viršinės. Šios problemos sprendimas yra pakeisti įrenginio dalis.

Konfigūruokite diagnozės tipus, galite sukurti kelis įrašus, iš kurių kiekvienas nurodo skirtingą mašinos problemų tipą. Arba galite sukurti vieną bendrąjį diagnostikos tipą, kuris pristato mašinos remontą.

## <a name="create-a-diagnostic-type"></a>Diagnozės tipo kūrimas

1. Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Diagnostikos tipai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Diagnostika** – Įveskite unikalų ID ar diagnostikos tipo pavadinimą.
    - **Aprašas** – įveskite išsamų diagnostikos tipo aprašą.

1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Darbuotojai, atsakingi už neatitikties tvirtinimą](quality-responsible-workers.md)
- [Neatitikimų sulaikymo zonos](quality-quarantine-zones.md)
- [Neatitikimų diagnostikos problemos](quality-problem-types.md)
- [Neatitikimų kokybės mokesčiai](quality-charges.md)
- [Neatitikties operacijos](quality-operations.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
