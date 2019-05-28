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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514444"
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

# <a name="policy-tips"></a>Strategijos patarimai
Pateikiame kelis pasiūlymus, kurie gali padėti sukurti naujas išlaidų valdymo strategijas. 
* Strategijos įsigalioja nuo nurodytos datos ir neturi įtakos, jei strategija sukurta po patirtų išlaidų. Pavyzdžiui, jei šiandien kuriate naują strategiją, kad išlaidos maistui neviršytų 50 USD, bet kurios esamos išlaidos, įvestos vakar, nebus tikrinamos pagal šią strategiją.
* Kuriant išlaidų kategorijos strategiją, kurią galima detaliai išvardyti eilutėmis, siūlome pridėti sąlygą dėl išlaidų eilutės tipo. Kai kurios strategijos, pvz., kvito reikalavimas, gali netikti detaliam išvardijimui eilutėmis ir turėtų būti taikomas tik antraštės eilutei arba nedetaliai eilutei. 

# <a name="when-to-evaluate-policies"></a>Kada vertinti strategijas

Išlaidų valdymo parametruose yra parinktis vertinti išlaidų valdymo strategijas, kai eilutė įrašoma, arba kai pateikiama išlaidų ataskaita. Jei pasirinksite įvertinti, kai eilutė įrašoma, užtikrinsite, kad vartotojai iš anksto matys, ką reikia padaryti, kad iš karto užbaigtų savo išlaidų ataskaitą. Kitu atveju, galite atidėti strategijos vertinimą ir sutaupyti laiko, jei patikrinimas atliekamas pabaigoje, pateikimo į darbo eigą metu.
