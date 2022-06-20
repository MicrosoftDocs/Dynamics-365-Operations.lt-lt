---
title: Turto dokumentai
description: Šiame straipsnyje paaiškinami turto valdymo dokumentai.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2e8d72dc938c43e266c6b7c39329f827c56607a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899475"
---
# <a name="asset-documents"></a>Turto dokumentai

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje paaiškinami turto valdymo dokumentai.

Modulyje „Turto valdymas“ galite konfigūruoti dokumentus, kad jie būtų automatiškai siejami su užduoties tipais, turto gamintojais, turto tipais arba turtu. Ši funkcija yra naudinga, kai išleidžiamos atnaujintos dokumentų versijos. Tokiu atveju jums tereikia įtraukti atnaujintą dokumentą į standartinę vietą, kurią naudojate „Supply Chain Management“ dokumentams laikyti ir pridėti dokumentą prie turto dokumento įrašo, kurį buvote sukūrę. Tada atnaujintą dokumentą galima pasiekti einant į meniu elementus **Visas turtas**, **Aktyvusis turtas**, **Mano aktyvusis turtas**, **Visi darbo užsakymai** ir **Aktyviosios darbo užsakymo užduotys**. Dokumentų pridėjimo prie turto dokumentų įrašo procesas naudoja standartinę dokumentų tvarkymo sistemą.

**1 pavyzdys:** Dokumente, susijusiame su užduoties tipu, gali būti aprašyta to darbo tipo procedūra.

**2 pavyzdys:** Dokumentas, susijęs su turto tipo, gamintojo ir modelio deriniu, gali būti standartinis pasirinkto turto gamintojo modelio vadovas.

## <a name="create-asset-document-relation"></a>Kurti turto dokumento ryšį

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto dokumentai**.
2. Pasirinkite **Naujas**, kad sukurtumėte turto dokumento įrašą.
3. Pagal tai, kiek konkreti turi būti dokumento sąsaja pagal jūsų pageidavimus, atitinkamai pasirinkite viename ar keliuose iš šių laukų: **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Užduoties tipo kategorija**, **Užduoties tipas**, **Užduoties tipo variantas** ir **Užduoties poreikis**. Parinktys, pasiekiamos laukuose **Užduoties tipo variantas** ir **Užduoties reikalavimas**, priklauso nuo žymėjimo lauke **Užduoties tipas**.

    > [!NOTE]
    > Sistema ieško dokumentų, kurie turėtų būti susieti su turtu arba darbo užsakymu, o modulis „Turto valdymas“ apdoroja visus turto dokumentų įrašus ir ieško galimų atitikčių. Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Užduoties reikalavimas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Užduoties tipo variantas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Užduoties tipas** ir t. t. Kaip matote pagal puslapio **Turto dokumentai** išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę. Keletas dokumentų gali būti susieti su turtu arba darbo užsakymu. Prireikus galite redaguoti priežiūros prašymo arba darbo užsakymo aptarnavimo lygį.

4. Pasirinkite **Priedai**. Rodomas standartinis puslapis **Dokumentų tvarkymas**.
5. Nustatykite dokumentus arba pastabas, kurios turėtų būti pridėtos prie turto dokumento įrašo. Kai pridėsite dokumentus, lauke **Priedai** bus rodomas su įrašu susijusių dokumentų skaičius.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]