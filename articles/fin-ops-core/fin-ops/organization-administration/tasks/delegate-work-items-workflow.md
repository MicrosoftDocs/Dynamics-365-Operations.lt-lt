---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515769"
---
# <a name="delegate-work-items-in-a-workflow"></a>Darbo eigos darbo elementų perdavimas

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Rankinis darbo elemento perdavimas

Norėdami perduoti atskirą darbo elementą, meniu **Darbo eiga** pasirinkite parinktį **Perduoti**, tada įveskite vartotoją, kuriam elementą reikia perduoti, ir komentarą. Taip darbo elementas bus iš naujo priskirtas tam vartotojui, kad jis elementą galėtų baigti.

## <a name="manually-delegate-multiple-work-items"></a>Neautomatiniu būdu perduokite kelis darbo elementus

Gali būti perduoti keli darbo elementai kartu iš **Man perduoti darbo elementai** puslapio. Šiems darbo eigos tipams taikomas masinis pervedimas: pirkimo sutarties patvirtinimo darbo eiga, pirkimo užsakymo darbo eiga, pirkimo paraiškų peržiūra ir tiekėjo SF darbo eiga. Numatyta, kad **Perduoti keletą darbo elementų** funkcija yra išjungta ir gali būti suaktyvinta **Darbo sritys > Funkcijų valdymas**. Norėdami suaktyvinti šią funkciją, kreipkitės į sistemos administratorių.
1.  Pereikite į **Įprasti > Bendri > Darbo elementai > Man priskirti darbo elementai**.
2.  Pasirinkite darbo elementus, kurie bus perduoti.
3.  Spustelėkite **Perduoti darbo elementus** meniu.
4.  Lauke **Vartotojas** lauke pasirinkite vartotoją, kuriam perduosite darbo elementus.
5.  Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.
6.  Spustelėkite **Perduoti darbo elementus** mygtuką, kad užbaigtumėte darbo elementų perdavimą.

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
9. Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.

