---
title: Išlaidų strategijų apibrėžimas
description: Galite apibrėžti išlaidų strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas programoje „Microsoft“ „Dynamics 365 Finance“.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389720"
---
# <a name="define-expense-policies"></a>Išlaidų strategijų apibrėžimas

[!include [banner](../includes/banner.md)]

Galite apibrėžti strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas.         
Išlaidų strategijos įgyvendinimas gali padėti veiksmingai valdyti išlaidas.         

Pavyzdžiui, galite nustatyti viešbučio išlaidų Niujorke strategiją, kad išlaidos viešbučiui vienai parai negali viršyti 250 USD.       
Jei darbuotojas pateikia išlaidų ataskaitą ar kelionės paraišką, kurioje kambario tarifas viršija šią sumą, sistema praneš        
kad pagal išlaidų strategiją suma yra viršyta. Sukonfigūruoti pranešimą, kurį gaus darbuotojas, galite        
apibrėždami strategiją.      
        
Galite apibrėžti trijų tolesnių tipų strategijas.         
        
- Įspėjimas – darbuotojui leidžia pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir        
  vėlesnėms ataskaitoms.        

- Klaida – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką, darbuotojas pagal strategiją peržiūrėtų išlaidas.       
 
 - Pateisinimas – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą ar kelionės paraišką, darbuotojas ar vadovas įvestų viršytos strategijos sumos pateisinimą.        

## <a name="policy-tips"></a>Strategijos patarimai
Pateikiame kelis pasiūlymus, kurie gali padėti kuriant naujas išlaidų valdymo strategijas. 
* Strategijos įsigalioja nuo nurodytos datos ir neturi įtakos, jei strategija sukurta po patirtų išlaidų. Pavyzdžiui, jei šiandien kuriate naują strategiją, kad išlaidos maistui neviršytų 50 USD, bet kurios esamos išlaidos, įvestos vakar, nebus tikrinamos pagal šią strategiją.
* Kuriant išlaidų kategorijos strategiją, kurią galima detaliai išvardyti eilutėmis, siūlome pridėti sąlygą dėl išlaidų eilutės tipo. Kai kurios strategijos, pvz., kvito reikalavimas, gali netikti detaliam išvardijimui eilutėmis ir turėtų būti taikomas tik antraštės eilutei arba nedetaliai eilutei. 
* Išlaidų valdymo strategijos pagal numatytuosius nustatymus vertinamos pagal šaltinio objektą. Vidinės įmonės scenarijuose galite nustatyti strategiją, kuri bus vertinama pagal paskirties objektą (besiskolinantį objektą). Norėdami vykdyti strategijas pagal paskirties objektą, įjunkite funkciją „Vertinti išlaidų strategiją pagal besiskolinantį juridinį subjektą“, esančią darbo srityje **Funkcijų valdymas**.

## <a name="when-to-evaluate-policies"></a>Kada vertinti strategijas

Išlaidų valdymo parametruose yra parinktis vertinti išlaidų valdymo strategijas, kai eilutė įrašoma, arba kai pateikiama išlaidų ataskaita. Jei pasirinksite įvertinti, kai eilutė įrašoma, užtikrinsite, kad vartotojai iš anksto matys, ką reikia padaryti, kad iš karto užbaigtų savo išlaidų ataskaitą. Kitu atveju, galite atidėti strategijos vertinimą ir sutaupyti laiko, jei patikrinimas atliekamas pabaigoje, pateikimo į darbo eigą metu.
