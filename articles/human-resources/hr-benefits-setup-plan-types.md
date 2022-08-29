---
title: Plano tipų apžvalga
description: Plano tipas programoje „Microsoft Dynamics 365 Human Resources“ yra konkrečių išmokų tipų aukščiausio lygio grupavimas.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ca14156c165ca3f536fc0120ebd03883284eb18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337332"
---
# <a name="plan-type-overview"></a>Plano tipo peržiūra

[!include [banner](../includes/preview-banner.md)]

Plano tipas yra konkrečių išmokų tipų aukščiausio lygio grupavimas. Kiekvienam plano tipui taikomas plano tipo kodas, kuriuo nustatomos plano tipo taisykles. Pavyzdžiui, **Pagrindiniam gyvybės** plano tipui bus priskiriamas **Gyvybės** plano tipo kodas, nes tai yra gyvybės draudimo plano rūšis ir turi atitikti taisykles, nustatytas **Gyvybės** plano tipo kodui. Kitas plano tipas gali būti **Papildomas gyvybės**. Šis plano tipas taip pat turės **Gyvybės** plano tipo kodą.

Kiekvienas plano tipas nurodo, keliems planams darbuotojas gali užsiregistruoti – vienam ar keletui. Pavyzdžiui, galbūt darbuotojas galės užsiregistruoti abiems **Basic life** ir **Supplemental life** abiems plano „Life“ polisams. Greičiausiai darbuotojui bus leista užsiregistruoti tik vienam medicinos draudimo tipo polisui gauti.

Jei plano tipas apima kontaktus, plano tipas nurodo, kad yra kontaktai – gavėjai ar priklausomieji. Pavyzdžiui, į plano tipą **Basic life** būtų įtraukiami gavėjai, o į plano tipą „Basic Medical“ būtų įtraukiami priklausomieji. Kai kuriais atvejais į planą gali būti neįtraukta asmeninių kontaktų. Pavyzdžiui, lanksčiųjų išlaidų sąskaita arba automobilių stovėjimo nuolaida.


Plano tipas gali nurodyti padengimo pasirinktis. Padengimo parinktys nustatytos **padengimo parinkčių** puslapyje. Padengimo parinktis gali nurodyti išmokos sumą arba kontaktus, kurie atitinka plano tipą. Pavyzdžiui, jei kontakto tipas yra **gavėjas**, padengimo parinktis turi apibrėžti sąlygas, nurodančias, ką gavėjas turi teisę gauti, kai išmoka išnaudota. Jei kontakto tipas yra **priklausomasis**, padengimo parinktis turi apibrėžti ryšį tarp priklausomojo ir darbuotojo. 

> [!IMPORTANT]
> Puslapyje **Plano tipai** yra pagrindiniai duomenys, kurie turi įtakos parinktims, galimoms kuriant naują išmokų planą:
>
> - **Plano tipo kodas** – šis laukas turi įtakos tam, kas rodoma skirtuke **Konfigūracija**, kai nustatoma faktinė nauda.  
> - **Lygiagreti registracija** – šis laukas nustato, ar leidžiamos kelios registracijos. (Medicininiam planui šis laukas įprastai nustatomas kaip **Viena registracija** .)
> - **Kontakto tipas** – šis laukas leidžia į planą įtraukti priklausomuosius arba gavėjus. Jei jis nustatytas į **Nėra**, į išmokų planus įtraukti darbuotojai neturės galimybės pasirinkti nei gavėjo, nei priklausomo asmens.
> - **Padengimo parinktys** – naudokite šį lauką, jei norite susieti padengimo parinktis su plano tipais. Jame apibrėžiami asmenys, kuriems bus taikomas šis plano tipas arba padengimo sumos, galimos šiam plano tipui. Pavyzdžiui, galite nurodyti, kad medicininio plano tipo aprėptis būtų prieinama tik darbuotojui, darbuotojui ir kitam vienam asmeniui arba darbuotojui ir jo šeimai.

## <a name="create-plan-types"></a>Planų tipų kūrimas

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
   | **Keisti padengimo parinktį** | Nurodo, ar darbuotojas gali keisti padengimo parinktis gyvenimo įvykio metu. |
   | **Keisti į naują planą** | Nurodo, ar darbuotojas gali keisti planus gyvenimo įvykio metu. |
   | **Automatiškai pakartotinai atidaryti tinkamumo patikrą** | Nurodo, ar gyvenimo įvykio metu automatiškai pakartotinai atidaryti registracijos išmokoms gauti tinkamumo patikrą. |
   | **Galiojimo įvykio registracijos laikotarpis** | Nurodo gyvenimo įvykio ataskaitų teikimo langą dienomis. **Pastaba**. Jei neįvesite reikšmės, sistema laikys, kad ataskaitų lango reikšmė yra nulis ir gyvenimo įvykio neapdoros. |
   | **Redaguoja tik administratoriai** | Nurodo, ar administratoriai gali atšaukti ar redaguoti planą per visą gyvenimo įvykį. Darbuotojas negali atlikti jokių keitimų darbuotojų savitarnos **darbo** srityje. |
   | **Planą atšaukti automatiškai** | Nurodo, ar planas turi būti automatiškai atšauktas per gyvenimo įvykį. Apdorous visą įvykį, automatinio atšaukimo **plano parinktis** išlaikys plano pasirinkimą. Bus pašalinta **tik** būsena **Patvirtinta arba** Išregistruota. Planas lieka pasirinktas. Todėl darbuotojai, kurie neatims plano pasirinkimų galiojimo įvykio registracijos laikotarpiu, neprarasite plano pasirinkimo. 

5. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
