---
title: Planų tipų kūrimas
description: Plano tipas programoje „Microsoft Dynamics 365 Human Resources“ yra konkrečių išmokų tipų aukščiausio lygio grupavimas. Kiekvienam plano tipui taikomas plano tipo kodas, kuriuo nustatomos plano tipo taisykles.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e24c11fb6e84a7480a40b706b106cd8465470f5c
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113551"
---
# <a name="create-plan-types"></a>Planų tipų kūrimas

Plano tipas programoje „Microsoft Dynamics 365 Human Resources“ yra konkrečių išmokų tipų aukščiausio lygio grupavimas. Kiekvienam plano tipui taikomas plano tipo kodas, kuriuo nustatomos plano tipo taisykles. Pavyzdžiui, plano tipui „Basic Life“ bus priskiriamas plano tipo kodas „Life“, nes tai yra gyvybės draudimo plano rūšis ir turi atitikti taisykles, nustatytas plano „Life“ tipo kodui. Kitas plano tipas galėtų būti „Supplemental Life“, kuriam taip pat bus taikomas plano tipo kodas „Life“.

Kiekvienas plano tipas nurodo, keliems planams darbuotojas gali užsiregistruoti – vienam ar keletui. Pavyzdžiui, galbūt darbuotojas galės užsiregistruoti abiems „Life“ plano tipo polisams – „Basic Life“ ir „Supplemental Life“ – gauti. Greičiausiai darbuotojui bus leista užsiregistruoti tik vienam medicinos draudimo tipo polisui gauti.

Jei plano tipas apima kontaktus, plano tipas nurodo, kad yra kontaktai – gavėjai ar priklausomieji. Pavyzdžiui, į plano tipą „Basic Life“ būtų įtraukiami gavėjai, o į plano tipą „Basic Medical“ būtų įtraukiami priklausomieji. Kai kuriais atvejais į planą gali būti neįtraukta asmeninių kontaktų. Pavyzdžiui, lanksčiųjų išlaidų sąskaita arba automobilių stovėjimo nuolaida.

Plano tipas gali nurodyti padengimo pasirinktis. Padengimo parinktys nustatytos padengimo parinkčių formoje. Padengimo parinktis gali nurodyti išmokos sumą arba kontaktus, kurie atitinka plano tipą. Pavyzdžiui, jei kontakto tipas yra gavėjas, padengimo parinktis turi apibrėžti sąlygas, nurodančias, ką gavėjas turi teisę gauti, kai išmoka išnaudota. Jei kontakto tipas yra priklausomasis, padengimo parinktis turi apibrėžti ryšį tarp priklausomojo ir darbuotojo. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Planų tipai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Plano tipas** | Unikalus pavadinimas, nurodantis plano tipą. |
   | **Aprašas** | Plano tipo aprašas. |
   | **Plano tipo kodas** | Iš išplečiamojo sąrašo reikšmių pasirinkite plano tipo kodą. Plano tipo kodų sąraše išvardijami visi plano tipai, palaikomi dabartinėje versijoje. |
   | **Registravimas tuo pačiu metu** | Nurodo, ar darbuotojas gali registruoti keliems to paties plano tipo išmokų planams, ar tik vienam plano tipo išmokų planui. |
   | **Kontakto tipas** | Nurodo asmeninio kontakto vaidmenį. Vertės yra tokios: tuščia, priklausomasis ir gavėjas. Galite palikti tuščią **kontakto tipo** lauką, jei plano tipo nereikalaujama įtraukti priklausomąjį ar gavėją, atsižvelgiant į padengimo parinktį. |

4. Norėdami konfigūruoti gyvybės įvykio parinktis, pasirinkite **Veiksmai**, tada pasirinkite **Gyvenimo įvykio parinktys**. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Plano tipas** | Plano tipas, dėl kurio konfigūruojamos gyvenimo įvykio parinktys. |
   | **Gyvenimo įvykio tipo ID** | Gyvenimo įvykio tipo ID. |
   | **Leisti atšaukti** | Nurodo, ar darbuotojas gali atšaukti išmokų planą gyvenimo įvykio metu. |
   | **Keisti padengimo parinktį** | Nurodo, ar darbuotojas gali keisti padengimo parinktis gyvenimo įvykio metu. |
   | **Keisti į naują planą** | Nurodo, ar darbuotojas gali keisti planus gyvenimo įvykio metu. |
   | **Planą atšaukti automatiškai** | Nurodo, ar planas automatiškai atšaukiamas gyvenimo įvykio metu. |
   | **Automatiškai pakartotinai atidaryti tinkamumo patikrą** | Nurodo, ar gyvenimo įvykio metu automatiškai pakartotinai atidaryti registracijos išmokoms gauti tinkamumo patikrą. |
   | **Ataskaitų teikimo langas** | Nurodo gyvenimo įvykio ataskaitų teikimo langą dienomis. **Pastaba**. Jei neįvesite reikšmės, sistema laikys, kad ataskaitų lango reikšmė yra nulis ir gyvenimo įvykio neapdoros. |

5. Pasirinkite **Įrašyti**. 
