---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "346254"
---
# <a name="delegate-work-items-in-a-workflow"></a>Perduoti darbo eigos darbo elementus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams. Ši procedūra padės sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitam vartotojui būtų perduodami automatiškai.



Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="set-up-automatic-delegation"></a>Automatinio perdavimo nustatymas
1. Eikite į Bendra > Nustatymas > Vartotojo parinktys.
2. Spustelėkite skirtuką Darbo eiga.
    * Įsitikinkite, kad dalis Perdavimas yra išskleista.    Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai. Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.  
3. Spustelėkite Pridėti.
4. Lauke Aprėptis pasirinkite parinktį.
    * Visi – perduoti visus jums priskirtus darbo elementus.    Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus. Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigos tipą.    Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus. Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigą.  
5. Lauke Perduoti pasirinkite vartotoją, kuriam norite perduoti darbo elementus.
    * Norėdami nurodyti, kada darbo elementai turėtų būti perduodami automatiškai, naudokite laukų Pradžios data / laikas ir Pabaigos data / laikas reikšmes.  
6. Lauke Pradžios data / laikas įveskite datą ir laiką.
7. Lauke Pabaigos data / laikas įveskite datą ir laiką.
8. Pasirinkite žymės langelį Įgalinta, kad suaktyvintumėte perdavimo taisyklę.
    * Jei modulį pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti modulį.    Jei darbo eigą pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti tam tikrą darbo eigą, kuriai reikia perduoti.  
9. Lauke Komentaras įveskite komentarą, paaiškinantį, kodėl perduodate darbo elementus.

