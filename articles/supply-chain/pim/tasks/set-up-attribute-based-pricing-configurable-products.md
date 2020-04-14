---
title: Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d23030b79670e31cc237b9ca53b0b3881678786f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149831"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą. Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų. Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą atlieka produktų vadovas.


## <a name="create-a-new-price-model"></a>Naujo kainos modelio kūrimas
1. Pagrindiniame puslapyje pasirinkite **Produkto varianto modelio aprašas**.
2. **Saitų** skyriuje pasirinkite **Produkto konfigūracijos modeliai**.
3. Sąraše pasirinkite eilutę **Aukščiausios klasės garsiakalbis**, bet nepasirinkite vardo nuorodos.
4. Veiksmų srityje pasirinkite **Modelis**.
5. Pasirinkite **Kainų modeliai**.
6. Pasirinkite **Naujas**.
7. Lauke **Kainos modelio pavadinimas** įveskite reikšmę. Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.  
8. Lauke **Aprašo laukas**surinkite reikšmę.
9. Pasirinkite **Įrašyti**.

## <a name="add-price-elements"></a>Kainos elementų įtraukimas
1. Pasirinkite **Redaguoti**. Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius. Taip pat galite įtraukti kainas skirtingomis valiutomis.  
2. Lauke **Bazinės kainos išraiška** įveskite reikšmę. Pavyzdžiui, įveskite 100. Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.  
3. Pasirinkite **Įtraukti**.
4. Lauke **Pavadinimas** įveskite `Rosewood`. Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas. Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.  
5. Pasirinkite **Redaguoti sąlygą**. Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.  
6. Lauke **Apribojimo turinys** įveskite `CabinetFinish=="Rosewood"`.
7. Pasirinkite **Gerai**.
8. Lauke **Išraiška** įveskite reikšmę. Pavyzdžiui, įveskite `50`. 
9. Uždarykite puslapį.

