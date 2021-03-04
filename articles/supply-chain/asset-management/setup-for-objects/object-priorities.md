---
title: Pasirinkite paslaugos lygį.
description: Šioje temoje pasakojama apie turto aptarnavimo lygius, esančius modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35e7a55b1ba230be6bb72b20fcd805ea061b648e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433501"
---
# <a name="asset-service-levels"></a>Pasirinkite paslaugos lygį.

[!include [banner](../../includes/banner.md)]

 

Šioje temoje pasakojama apie turto aptarnavimo lygius, esančius modulyje „Turto valdymas“. Turto aptarnavimo lygiai yra susiję su turtu ir perkeliami į priežiūros užklausas ir darbo užsakymus. Planuojant darbo užsakymą, jie yra naudojami apskaičiuoti darbo užsakymų prioritetą. Prireikus, galima keisti turto aptarnavimo lygius.

Daugiau informacijos apie konfigūraciją, susijusią su darbo užsakymo planavimo vertinimo rezultatų skaičiavimu, žr. [Turto valdymo parametrai](../setup-for-objects/enterprise-asset-management-parameters.md). Turite nustatyti bent vieną turto aptarnavimo lygio numatytąjį įrašą. Šis numatytasis įrašas naudojamas, jei planuojant darbo užsakymą, nerandama kitų atitikčių.

**1 pavyzdys:** Numatytasis paslaugų lygis, naudojamas, jei nerandama kita atitiktis. Šiame įraše pažymite tik aptarnavimo lygį.

**2 pavyzdys:** Aukštas aptarnavimo lygis, naudojamas planuojant „Volvo“ sunkvežimio variklio darbus. Šiame įraše pažymite atitinkamą turto tipą (pvz., **sunkvežimio variklis**), gamintoją (**„Volvo“**) ir aptarnavimo lygį.

## <a name="set-up-asset-service-levels"></a>Nustatykite paslaugos lygį.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto paslaugų lygiai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Atsižvelgdami į reikiamą turto aptarnavimo lygio informacijos lygį, pažymėkite atitinkamus duomenis laukuose **Funkcinė vieta**, **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Darbo užsakymo tipas** ir **Aptarnavimo lygis**.

    > [!NOTE]
    > Kai turto aptarnavimo lygis naudojamas dirbant su priežiūros užklausomis ir darbo užsakymais, modulis „Turto valdymas“ apdoroja visus turto dokumentų įrašus ir ieško galimos atitikties. Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Darbo užsakymo tipas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Turtas** atitikties ir t. t. Kaip matote pagal puslapio **Turto aptarnavimo lygiai** išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę. Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuris tuose laukuose pasirinkčių neturi.

4. Lauke **Aptarnavimo lygis** pasirinkite skaičių, nurodantį aptarnavimo lygį (prioritetą).


> [!NOTE]
> Jei puslapyje **Turto aptarnavimo lygiai** pakeisite turto aptarnavimo lygio įrašą, kurį jau naudojote darbo užsakyme, priežiūros užklausų ir darbo užsakymų aptarnavimo lygis nebus atitinkamai atnaujintas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]