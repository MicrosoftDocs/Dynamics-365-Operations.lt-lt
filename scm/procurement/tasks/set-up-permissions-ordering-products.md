--- 
title: "Teisių užsakyti produktus kito darbuotojo vardu nustatymas"
description: "Šioje procedūroje parodoma, kaip darbuotojų suteikti teisę pirkimo paraiškas rengti kitų darbuotojų vardu."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8f12f9eb949034f9bef91d93f31a0f3373e39e98
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Teisių užsakyti produktus kito darbuotojo vardu nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip darbuotojų suteikti teisę pirkimo paraiškas rengti kitų darbuotojų vardu. Kitaip tariant, pirkimo paraiškos „rengėjas“ gali kurti paraišką kitam „prašytojas“. Procedūroje taip pat parodoma, kaip darbuotojui suteikti teisę užsakyti prekes ir paslaugas skirtinguose juridiniuose subjektuose arba valdymo vienetuose. Šias užduotis paprastai atlieka pirkimo vadovas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba naudodami savo duomenimis.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Suteikti teisę kito darbuotojo vardu įvesti pirkimo paraiškas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo paraiškos teisės.
    * Įsitikinkite, kad laukas Dabartinio rodinys nustatytas į parinktį Pagal rengėją.  Kairiojoje srityje esančiame sąraše pateikiami asmenys, kuriems galima suteikti teisę rengti paraiškas kitų asmenų vardu.  
2. Pasirinkite asmenį, kuriam norite suteikti teisę (t. y. rengėją).
3. Spustelėkite Pridėti.
4. Raskite ir pasirinkite asmenį, kurį norite įtraukti kaip prašytoją.
    * Prašytojas yra asmuo, kurio vardu rengėjas gali kurti paraiškas.  
    * Lauke Autorizavimas pasirinkite Konkretus, norėdami, kad rengėjas galėtų kurti pirkimo paraiškas pasirinkto darbuotojo vardu. Pasirinkite Ataskaitos, norėdami, kad rengėjas taip pat galėtų kurti pirkimo paraiškas visų darbuotojų, teikiančių tam darbuotojui ataskaitas, vardu.  
5. Lauke Įsigalioja įveskite datą.
6. Lauke Galiojimo pabaiga įveskite datą.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Peržiūrėti rengėjus, kurie turi teisę pasirinktam darbuotojui kurti pirkimo paraiškas
1. Lauke Dabartinis rodinys pasirinkite Pagal prašytoją.
    * Šiame rodinyje rodomas rengėjų, kuriems suteikta teisė pasirinkto darbuotojo vardu kurti pirkimo paraiškas, sąrašas.  
2. Naudokite spartųjį filtrą, norėdami rasti darbuotoją, kurį ką tik įtraukėte kaip prašytoją.
3. Pasirinkite prašytoją.
    * Sąraše Rengėjas rodomi asmenys, kurie turi teisę prekes užsakyti kairiojoje srityje pasirinkto prašytojo vardu.   Čia galite įtraukti papildomų rengėjų.   Šiame rodinyje taip pat galite prašytojui suteikti teisę kurti paraiškas juridiniame subjekte ar valdymo vienete, kuris nėra to asmens pagrindinis juridinis subjektas ar valdymo vienetas.  


