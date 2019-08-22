---
title: Nustatyti dokumentą kaip
description: Šioje temoje pasakojama apie turto dokumentus, esančius modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783449"
---
# <a name="asset-documents"></a>Nustatyti dokumentą kaip

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje pasakojama apie turto dokumentus, esančius modulyje „Turto valdymas“.

Modulyje „Turto valdymas“ galite konfigūruoti dokumentus, kad jie būtų automatiškai siejami su užduoties tipais, turto gamintojais, turto tipais arba turtu. Ši funkcija yra naudinga, kai išleidžiamos atnaujintos dokumentų versijos. Tokiu atveju jums tereikia įtraukti atnaujintą dokumentą į standartinę vietą, kurią naudojate Microsoft Dynamics 365 for Finance and Operations dokumentams laikyti ir pridėti dokumentą prie turto dokumento įrašo, kurį buvote sukūrę. Tada atnaujintą dokumentą galima pasiekti einant į meniu elementus **Visas turtas**, **Aktyvusis turtas**, **Mano aktyvusis turtas**, **Visi darbo užsakymai** ir **Aktyviosios darbo užsakymo užduotys**. Dokumentų pridėjimo prie turto dokumentų įrašo procesas naudoja standartinę dokumentų tvarkymo sistemą programoje „Finance and Operations“.

**1 pavyzdys:** Dokumente, susijusiame su užduoties tipu, gali būti aprašyta to darbo tipo procedūra.

**2 pavyzdys:** Dokumentas, susijęs su turto tipo, gamintojo ir modelio deriniu, gali būti standartinis pasirinkto turto gamintojo modelio vadovas.

## <a name="create-asset-document-relation"></a>Kurti turto dokumento ryšį

1. Pasirinkite **Asset management** \> **Setup** \> **Asset documents**.
2. Pasirinkite **New**, kad sukurtumėte turto dokumento įrašą.
3. Atsižvelgdami į tai, kiek tiksliai norite, kad dokumentas būtų susijęs, atlikite atitinkamus pasirinkimus viename ar keliuose iš šių laukų: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, ir **Job requirement**. Parinktys, pasiekiamos laukuose **Užduoties tipo variantas** ir **Užduoties reikalavimas**, priklauso nuo žymėjimo lauke **Užduoties tipas**.

    > [!NOTE]
    > Sistema ieško dokumentų, kurie turėtų būti susieti su turtu arba darbo užsakymu, o modulis „Turto valdymas“ apdoroja visus turto dokumentų įrašus ir ieško galimų atitikčių. Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Užduoties reikalavimas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Užduoties tipo variantas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Užduoties tipas** ir t. t. Kaip matote pagal puslapio **Turto dokumentai** išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę. Keletas dokumentų gali būti susieti su turtu arba darbo užsakymu. Prireikus, galite redaguoti priežiūros prašymo arba darbo užsakymo aptarnavimo lygį.

4. Pasirinkite **Priedai**. Rodomas standartinis puslapis **Dokumentų tvarkymas** programoje „Finance and Operations“.
5. Nustatykite dokumentus arba pastabas, kurios turėtų būti pridėtos prie turto dokumento įrašo. Kai pridėsite dokumentus, lauke **Priedai** bus rodomas su įrašu susijusių dokumentų skaičius.
