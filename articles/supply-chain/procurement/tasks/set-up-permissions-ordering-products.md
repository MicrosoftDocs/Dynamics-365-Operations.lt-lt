---
title: Teisių užsakyti produktus kito darbuotojo vardu nustatymas
description: Šiame straipsnyje paaiškinama, kaip darbuotojams suteikti teisę parengti pirkimo paraiškas kitų darbuotojų vardu.
author: GalynaFedorova
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3053f28fdf97637b1da5f644f64676bfd10fb6a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854216"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Teisių užsakyti produktus kito darbuotojo vardu nustatymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip darbuotojams suteikti teisę parengti pirkimo paraiškas kitų darbuotojų vardu. Kitaip tariant, pirkimo paraiškos „rengėjas“ gali kurti paraišką kitam „rengėjui“. Procedūroje taip pat parodoma, kaip darbuotojui suteikti teisę užsakyti prekes ir paslaugas skirtinguose juridiniuose subjektuose arba valdymo vienetuose. Šias užduotis paprastai atlieka pirkimo vadovas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba naudodami savo duomenimis.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Suteikti teisę kito darbuotojo vardu įvesti pirkimo paraiškas
1. Naršymo srityje eikite į **Moduliai > Paraiškos > Sąranka > Strategijos > Pirkimo paraiškos teisės**. Įsitikinkite, kad lauke **Dabartinis rodinys** nustatyta reikšmė **Pagal rengėją**. Kairiojoje srityje esančiame sąraše pateikiami asmenys, kuriems galima suteikti teisę rengti paraiškas kitų asmenų vardu.  
2. Pasirinkite asmenį, kuriam norite suteikti teisę (t. y. rengėją).
3. Pasirinkite **Įtraukti**.
4. Raskite ir pasirinkite asmenį, kurį norite įtraukti kaip prašytoją.
    - Prašytojas yra asmuo, kurio vardu rengėjas gali kurti paraiškas.  
    - Lauke **Autorizavimas** pasirinkite **Specialus**, jei rengėjui turėtų būti leidžiama kurti pirkimo paraiškas pasirinkto darbuotojo vardu. Pasirinkite **Ataskaitų teikimas**, jei rengėjui taip pat turėtų būti leidžiama kurti pirkimo paraiškas visų darbuotojų, kurie atsiskaito tam darbuotojui, vardu.  
5. Lauke **Įsigalioja** įveskite datą.
6. Lauke **Galiojimo pabaiga** įveskite datą.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Peržiūrėti rengėjus, kurie turi teisę pasirinktam darbuotojui kurti pirkimo paraiškas
1. Lauke **Dabartinis rodinys** pasirinkite **Pagal prašytoją**. Šiame rodinyje rodomas rengėjų, kuriems suteikta teisė pasirinkto darbuotojo vardu kurti pirkimo paraiškas, sąrašas.  
2. Naudokite spartųjį filtrą, norėdami rasti darbuotoją, kurį ką tik įtraukėte kaip prašytoją.
3. Pasirinkite prašytoją. Sąraše Rengėjas rodomi asmenys, kurie turi teisę prekes užsakyti kairiojoje srityje pasirinkto prašytojo vardu.  Čia galite įtraukti papildomų rengėjų. Šiame rodinyje taip pat galite prašytojui suteikti teisę kurti paraiškas juridiniame subjekte ar valdymo vienete, kuris nėra to asmens pagrindinis juridinis subjektas ar valdymo vienetas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]