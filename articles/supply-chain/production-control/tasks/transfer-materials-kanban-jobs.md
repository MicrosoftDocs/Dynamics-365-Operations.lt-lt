---
title: Medžiagų su „kanban‟ užduotimis perkėlimas
description: Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d4e6d8bbdb50394ef575e1088dd238eb39170124854edb878f6dccb6c9e07d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771352"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Medžiagų su „kanban‟ užduotimis perkėlimas

[!include [banner](../../includes/banner.md)]

Šios procedūros tikslas yra vykdyti išėmimo „kanban“ užduotį, kad būtų perkeltos medžiagos. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta sandėlio darbuotojui.


## <a name="display-transfer-jobs"></a>Rodyti perkėlimo užduotis
1. Eikite į Gamybos kontrolė > „Kanban“ > Perkėlimo užduočių „Kanban“ sritis.
2. Išplėskite arba sutraukite skyrių Filtrai.
    * Skyriuje „Filtrai“ galite nurodyti, kokias užduotis norite matyti, filtruodami gamybos eigą, veiklos pavadinimą, išvykimo sandėlį ir vietą, atvykimo sandėlį ir vietą.  
3. Lauke „Išvykimo sandėlis“ įveskite „11“.
4. Lauke „Atvykimo vieta“ įveskite „12“.

## <a name="start-a-transfer-job"></a>Pradėti perkėlimo užduotį
1. Sąraše atžymėkite pasirinktą eilutę, jei tokių yra.
2. Sąraše pasirinkite 4 eilutę.
    * Pasirinkite pirmą užduotį, kurios būsena „Nesuplanuota“. Įsitikinkite, kad tai yra vienintelė pasirinkta užduotis.  
3. Spustelėkite Pradėti.
    * Atkreipkite dėmesį į piktogramą, kuri nurodo, kad užduotis pradėta.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Pasirinkti antrą perkėlimo užduotį ir pakeisti kiekį
1. Sąraše raskite ir pasirinkite norimą įrašą.
    * Galite pasirinkti kelias užduotis, tačiau dabar pasirinkite 5 eilutę.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Įsitikinkite, kad pažymėta tik ankstesnio veiksmo užduotis. Atžymėkite visas kitas užduotis.  
3. Užsirašykite lauke „Užduočių kiekis“ esančią reikšmę, kad vėliau ją žinotumėte
4. Nustatykite užduočių kiekio reikšmę „30“.
    * Atkreipkite dėmesį į perspėjimą! Jums neleidžiama perkelti 30. Pagal „kanban“ taisyklės konfigūraciją, galite perkelti tik pradinį kiekį.  
5. Naudoti anksčiau užsirašytą reikšmę lauke „Užduočių kiekis“
    * Nustatykite užduočių kiekį į ankstesnę reikšmę.  

## <a name="start-the-second-transfer-job"></a>Pradėti antrą perkėlimo užduotį
1. Spustelėkite Pradėti.
    * Tai pradės užduoties 5 eilutėje perkėlimą.  

## <a name="complete-both-transfer-jobs"></a>Baigti abi perkėlimo užduotis
1. Sąraše pasirinkite 4 eilutę.
    * Dabar 4 ir 5 eilutėse pažymėtos dvi perkėlimo užduotys.  
2. Spustelėkite Baigti.
    * Tai užbaigs abiejų užduočių perkėlimą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]