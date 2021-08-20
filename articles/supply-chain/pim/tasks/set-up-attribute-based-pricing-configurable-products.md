---
title: Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5abb2e7dc33b46589c1a3699e70b56af6f694aed49294eb81a2122db6d414a96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743559"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą. Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų. Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą atlieka produktų vadovas.


## <a name="create-a-new-price-model"></a>Naujo kainos modelio kūrimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Sąraše pasirinkite eilutę **Aukščiausios klasės garsiakalbis**, bet nepasirinkite vardo nuorodos.
1. Veiksmų srityje pasirinkite **Modelis**.
1. Pasirinkite **Kainų modeliai**.
1. Pasirinkite **Naujas**.
1. Lauke **Kainos modelio pavadinimas** įveskite reikšmę. Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.  
1. Lauke **Aprašo laukas** surinkite reikšmę.
1. Pasirinkite **Įrašyti**.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]