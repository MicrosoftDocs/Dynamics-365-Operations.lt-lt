---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916420"
---
# <a name="delegate-work-items-in-a-workflow"></a>Darbo eigos darbo elementų perdavimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Rankinis darbo elemento perdavimas

Norėdami perduoti atskirą darbo elementą, meniu **Darbo eiga** pasirinkite parinktį **Perduoti**, tada įveskite vartotoją, kuriam elementą reikia perduoti, ir komentarą. Taip darbo elementas bus iš naujo priskirtas tam vartotojui, kad jis elementą galėtų baigti.

## <a name="automatically-delegate-work-items"></a>Automatinis darbo elementų perdavimas

Jei tam tikrą laiką planuojate nebūti biure ar dėl kitų priežasčių negalėsite atlikti veiksmų su darbo elementais, naudodami puslapį **Vartotojo parinktys** naujus darbo elementus galite automatiškai perduoti kitiems vartotojams.

### <a name="set-up-automatic-delegation"></a>Automatinio perdavimo nustatymas
1. Eikite į **Bendra > Sąranka > Vartotojo parinktys**.
2. Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar perdavimo skyrius išplėstas. Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai. Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.  
3. Spustelėkite **Pridėti**.
4. Lauke **Aprėptis** pasirinkite parinktį.
    - Visi – perduoti visus jums priskirtus darbo elementus.
    - Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus. Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigos tipą.
    - Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus. Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigą.  
5. Lauke **Perduoti** pasirinkite vartotoją, kuriam perduosite darbo elementus. Norėdami nurodyti, kada darbo elementai turėtų būti perduodami automatiškai, naudokite laukų Pradžios data / laikas ir Pabaigos data / laikas reikšmes.  
6. Lauke **Pradžios data / laikas** įveskite datą ir laiką.
7. Lauke **Pabaigos data / laikas** įveskite datą ir laiką.
8. Pasirinkite žymės langelį **Įjungta**, kad aktyvuotumėte perdavimo taisyklę. Jei kaip aprėptį pasirinkote **Modulis**, turite pasirinkti modulį pavadinimo lauke. Jei kaip aprėptį pasirinkote **Darbo eiga**, turite pasirinkti konkrečią perdavimo darbo eigą pavadinimo lauke.  
9. Lauke **Komentaras** įveskite komentarą, kuriame paaiškinate kodėl perduodate darbo elementus.

