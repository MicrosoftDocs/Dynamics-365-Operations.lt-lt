--- 
title: "Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas"
description: "Šioje procedūroje parodoma, kaip nustatyti atributais pagrįstą kainodarą."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip nustatyti atributais pagrįstą kainodarą. Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų. Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą atlieka produktų vadovas.


## <a name="create-a-new-price-model"></a>Naujo kainos modelio kūrimas
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Sąraše pasirinkite aukščiausios kokybės garsiakalbio eilutę, bet nespustelėkite pavadinimo nuorodos.
4. Veiksmų srityje spustelėkite Modelis.
5. Spustelėkite Kainos modeliai.
6. Spustelėkite Naujas.
7. Lauke Kainos modelio pavadinimas įveskite reikšmę.
    * Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.  
8. Lauke Aprašas įveskite reikšmę.
9. Spustelėkite Įrašyti.

## <a name="add-price-elements"></a>Kainos elementų įtraukimas
1. Spustelėkite Redaguoti.
    * Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius. Taip pat galite įtraukti kainas skirtingomis valiutomis.  
2. Lauke Bazinės kainos išraiška įveskite reikšmę.
    * Pavyzdžiui, įveskite 100.   Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.  
3. Spustelėkite Pridėti.
4. Lauke Pavadinimas įveskite Raudonmedžio.
    * Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas. Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.  
5. Spustelėkite Redaguoti sąlygą.
    * Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.  
6. Lauke ConstraintBody įveskite CabinetFinish=="Rosewood".
7. Spustelėkite GERAI.
8. Lauke Išraiška įveskite reikšmę.
    * Pavyzdžiui, įveskite 50.  
9. Uždarykite puslapį.
10. Uždarykite puslapį.


