---
title: Išlaidų strategijų apibrėžimas
description: Galite apibrėžti išlaidų strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
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
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840894"
---
# <a name="expense-policies"></a>Išlaidų strategija

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
Pateikiame kelis pasiūlymus, kurie gali padėti sukurti naujas išlaidų valdymo strategijas. 
* Strategijos įsigalioja nuo nurodytos datos ir neturi įtakos, jei strategija sukurta po patirtų išlaidų. Pavyzdžiui, jei šiandien kuriate naują strategiją, kad išlaidos maistui neviršytų 50 USD, bet kurios esamos išlaidos, įvestos vakar, nebus tikrinamos pagal šią strategiją.
* Kuriant išlaidų kategorijos strategiją, kurią galima detaliai išvardyti eilutėmis, siūlome pridėti sąlygą dėl išlaidų eilutės tipo. Kai kurios strategijos, pvz., kvito reikalavimas, gali netikti detaliam išvardijimui eilutėmis ir turėtų būti taikomas tik antraštės eilutei arba nedetaliai eilutei. 

## <a name="when-to-evaluate-policies"></a>Kada vertinti strategijas

Išlaidų valdymo parametruose yra parinktis vertinti išlaidų valdymo strategijas, kai eilutė įrašoma, arba kai pateikiama išlaidų ataskaita. Jei pasirinksite įvertinti, kai eilutė įrašoma, užtikrinsite, kad vartotojai iš anksto matys, ką reikia padaryti, kad iš karto užbaigtų savo išlaidų ataskaitą. Kitu atveju, galite atidėti strategijos vertinimą ir sutaupyti laiko, jei patikrinimas atliekamas pabaigoje, pateikimo į darbo eigą metu.
