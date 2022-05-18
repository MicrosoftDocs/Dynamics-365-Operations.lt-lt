---
title: Savikainos objekto dimensijos
description: Analizuodami išlaidas ir norėdami nustatyti, kur nukreiptas išlaidų srautas, naudojate išlaidų elemento dimensijas. Išlaidų objekto dimensijas naudojate tada, kai norite nustatyti, kur reikia priskirti išlaidas. Šioje temoje pateikiama informacijos apie išlaidų objekto dimensijas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cf9ebda3ab362112c9354595b7d554355b30f118
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734023"
---
# <a name="cost-object-dimensions"></a>Savikainos objekto dimensijos

[!include [banner](../includes/banner.md)]

Analizuodami išlaidas ir norėdami nustatyti, kur nukreiptas išlaidų srautas, naudojate išlaidų elemento dimensijas. Išlaidų objekto dimensijas naudojate tada, kai norite nustatyti, kur reikia priskirti išlaidas. Šioje temoje pateikiama informacijos apie išlaidų objekto dimensijas.

Išlaidų objektas gali būti bet kokio tipo objektas, kurį norite įvertinti, kuriam norite paskirstyti išlaidas arba kurį norite tiesiogiai išmatuoti. Dažniausiai pasitaikantys išlaidų objektai yra produktai, projektai, ištekliai, padaliniai, išlaidų centrai ir geografiniai regionai. Valdyba naudoja išlaidų objektus norėdama apskaičiuoti išlaidas ir atlikti pelningumo analizę.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Išlaidų objekto dimensijos ir išlaidų objekto dimensijos nariai
Išlaidų objektai vadinami *išlaidų objekto dimensijos*. Po to, kai nuspręsite, kurį objektą turėtų nurodyti išlaidų objekto dimensija, turite nurodyti atskiras dimensijos vertes arba importuoti jas į išlaidų apskaitą iš kitų išteklių sistemų. Šios atskiros dimensijos vertės vadinamos *išlaidų objekto dimensijos nariai*. Pavyzdžiui, norite naudoti finansinę dimensiją, kurios pavadinimas Išlaidų centras, kaip išlaidų objekto dimensiją. Norėdami pamatyti išlaidų srautą į atskirus išlaidų centrus, turite importuoti išlaidų objekto dimensijos narius. Šiuo atveju išlaidų objekto dimensijos nariai yra faktinių išlaidų centrai, pavyzdžiui, pardavimai, gamyba, administravimas ir geografinės vietos. Toliau pateikiamoje ekrano nuotraukoje pavaizduotas išlaidų centrų pavyzdys, kai išlaidų centrai yra išlaidų objekto dimensija su savo faktinių išlaidų centrais, kurie yra išlaidų objekto dimensijos nariai. 

[![Ekrano kopija, kurioje rodomas išlaidų centras kaip išlaidų objekto dimensija.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Išlaidų objekto dimensijos narių importavimas naudojant duomenų jungtis
Siekdami palengvinti išlaidų objekto dimensijos narių importavimą ir gauti vertes iš objektų, kuriuos norite naudoti kaip išlaidų objekto dimensijas, naudojate duomenų jungtis. Galite naudoti iš anksto paruoštas duomenų jungtis arba savo sukurtas pasirinktines duomenų jungtis.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
