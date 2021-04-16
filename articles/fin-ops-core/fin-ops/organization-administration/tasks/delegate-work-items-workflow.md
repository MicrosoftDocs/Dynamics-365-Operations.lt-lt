---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747374"
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
4. **Tikslas** laukelyje, pasirinkite parinktį:
    - Visi – perduoti visus jums priskirtus darbo elementus.
    - Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus. Jei pasirenkate šią parinktį, privalote pasirinkti darbo srauto tipą **Pavadinimas** laukelyje.
    - Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus. Jei pasirenkate šią parinktį, privalote pasirinkti darbo srauto tipą **Pavadinimas** laukelyje.  
5. **Pavadinimas** laukelis:
    - **Modulis** tikslui, pasirinkite paskirties modulį.
    - **Darbo srauto** tikslui, pasirinkite paskirties darbo srautą.
6. Lauke **Perduoti** pasirinkite vartotoją, kuriam perduosite darbo elementus. Naudokite **Datos/laiko pradžia** ir **Datos/laiko pabaiga** laukelius tam, kad nurodytumėte elementų automatinio priskyrimo laiką.  
7. Lauke **Pradžios data / laikas** įveskite datą ir laiką.
8. Lauke **Pabaigos data / laikas** įveskite datą ir laiką.
9. Pasirinkite žymės langelį **Įjungta**, kad aktyvuotumėte perdavimo taisyklę. 
10. Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]