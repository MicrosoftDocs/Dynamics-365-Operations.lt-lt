---
title: "Seniausio paketo paėmimas mobiliajame įrenginyje"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti seniausio paketo paėmimo parinktis iš mobiliojo įrenginio."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Seniausio paketo paėmimas mobiliajame įrenginyje

[!include[banner](../includes/banner.md)]

Konfigūraciją **Paimti seniausią paketą** galite pasiekti per mobiliojo įrenginio meniu, ir jis leidžia priversti sandėlio darbininkus paimti seniausią paketą jų dabartinėje vietoje arba juos apie tai įspėti.  

## <a name="where-it-applies"></a>Kai taikoma
Parinktis Paimti seniausią paketą sukonfigūruota mobiliojo įrenginio meniu elementuose ir turi įtakos toliau nurodytiems paketo paėmimo elementams.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Kaip nustatyti konfigūraciją Paimti seniausią paketą 
Prekėms, kurioms yra nustatyta naudoti esamą darbą, parinktis **Paimti seniausią paketą** mobiliojo įrenginio meniu gali būti nustatyta kaip **Nėra**, **Įspėti**, arba **Priversti**.

**Nėra**: darbininkai negaus jokių pranešimų ir galės paimti bet kurį paketą savo vietoje.

**Įspėti** ir **Priversti**: darbininkui pasirinkus paketą, virš paketo valdiklio bus rodomas (-i) paketas (-ai) su seniausia galiojimo data Jei vietos numerio lentelės kontroliuojamos, virš numerio lentelių valdiklio bus rodomas numerio lentelių, kuriose yra seniausias paketas, sąrašas. 
-   **Įspėti**: jei darbininkas pasirenka numerio lentelę arba paketą, kuris nėra rodomas sąraše, valdiklis ištuštėja ir rodomas įspėjimas, jog yra senesnis paketas, kurį galima pasirinkti. Kad būtų leidžiama tęsti darbą, darbuotojas gali dar kartą pasirinkti tą pačią numerio lentelę arba paketą.  
-   **Priversti**: darbininkai ir toliau gaus pranešimą, kad yra senesnis paketas, kurį reikia paimti.

