---
title: Turto svarbos tipai
description: Šiame straipsnyje paaiškinami turto valdymo turto kritinės vertės tipai.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfde9a9bc681c0d758491fc5c361b5b046e20d9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899504"
---
# <a name="asset-criticality-types"></a>Turto svarbos tipai

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje paaiškinami turto valdymo turto kritinės vertės tipai. Turto svarba yra susijusi su turtu ir perkeliama į darbo užsakymus. Darbo užsakyme jos keisti negalima. Planuojant darbo užsakymą turto svarba naudojama siekiant apskaičiuoti darbo užsakymo svarbą. Kitaip tariant, ji naudojama apskaičiuoti, kokios įtakos turto priežiūros užduotis turi gamybos grafikui ir įmonės produktyvumui. Daugiau informacijos apie konfigūraciją, susijusią su darbo užsakymo planavimo vertinimo rezultatų skaičiavimu, žr. [Turto valdymo parametrai](../setup-for-objects/enterprise-asset-management-parameters.md).

Norėdami nustatyti svarbą, pirmiausia sukurkite svarbos tipus, kurie turėtų būti naudojami šioje turto konfigūracijoje. Tada nustatykite svarbos tipus.

## <a name="set-up-criticality-types"></a>Nustatyti pasirinktinius darbo tipus

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Svarbos tipai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Lauke **Svarba** įveskite skaičių, nurodantį svarbą.
4. Lauke **Pavadinimas** įveskite unikalų darbo eigos pavadinimą.
5. Lauke **Koeficientas** įveskite skaičių. Šis koeficientas naudojamas skaičiuojant darbo užsakymo planavimą, siekiant nustatyti svarbos įrašą, kurį reikėtų naudoti. (Visada naudojamas įrašas, turintis aukščiausią koeficientą.) Šis nustatymas yra svarbus, jei, kaip parodyta toliau pateiktoje iliustracijoje, sukuriamos tos pačios kritiškumo vertės kritiškumo eilutės.

    ![Puslapis Kritiškumo tipai.](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Ilgalaikio turto knygos nustatymas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto kritiškumai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Atsižvelgdami į reikiamą turto svarbos informacijos lygį, pasirinkite atitinkamus duomenis laukuose **Funkcinė vieta**, **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Užduoties tipo kategorija**, **Užduoties tipas**, **Užduoties tipo variantas** ir **Užduoties reikalavimas**.

    > [!NOTE]
    > Kai pasirenkate turto svarbą, turto valdymo programa apdoroja visus turto svarbos įrašus, kad surastų galimų atitikčių Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, turto valdymo programa pirmiausia tikrina **Užduoties reikalavimą**. Jei atitikties rasti nepavyksta, ji patikrina **Užduoties tipo variantą**. Jei atitikties rasti nepavyksta, ji patikrina **Darbo tipas** ir t. t. Kaip matote pagal puslapio išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę. Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuris pasirinkčių neturi.

4. Lauke **Kritiškumas** pasirinkite pagreitinimo kodus, kuriuos sukūrėte 1 procedūroje. Uždarykite formą.

### <a name="notes-about-criticality-setup"></a>Pastabos apie svarbos konfigūraciją

- Jei pakeisite turto svarbą konfigūracijoje, kurią jau naudojote darbo užsakyme, šio darbo užsakymo svarba nebus atitinkamai atnaujinta.
- Darbo užsakymo svarba iš naujo apskaičiuojama kaskart, kai prie darbo užsakymo pridedama arba pašalinama darbo užsakymo eilutė.
- Jei darbo užsakymą sudaro keletas darbo užsakymo užduočių, remiantis puslapyje **Svarbos tipai** esančiu lauku **Koeficientas**, didžiausia svarba visada teikiama darbo užsakymui.
- Paprastai per tam tikrą laiką turto svarba gali keistis. Svarbai gali turėti įtakos naujos įrangos pirkimas, atnaujinimas ir t. t. Apsvarstykite galimybę reguliariais intervalais (pvz., kartą per metus arba kas antrus metus) iš naujo įvertinti savo turto svarbą, siekdami įsitikinti, kad jūsų svarbos apibrėžtys atitinka dabartinę gamybos konfigūraciją.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]