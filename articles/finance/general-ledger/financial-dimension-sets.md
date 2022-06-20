---
title: Finansinių dimensijų rinkiniai
description: Šiame straipsnyje aprašomi finansinių dimensijų rinkiniai ir pateikiami patarimai, kaip optimizuoti jų naudojimą.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3d4c15504b2ad128493e1bafa36aed271c2ab6dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864287"
---
# <a name="financial-dimension-sets"></a>Finansinių dimensijų rinkiniai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi finansinių dimensijų rinkiniai ir pateikiami patarimai, kaip optimizuoti jų naudojimą.

Dimensijų rinkinys yra surikiuotas finansinių dimensijų sąrašas, kurį galima naudoti Didžiosios knygos duomenims apibendrinti vartotojo apibrėžtu būdu. Pirminis dimensijų rinkinių naudojimas yra apibrėžti bandomąjį balansą.

Vienintelis standartinis dimensijų rinkinys yra tas dimensijų rinkinys, kuriame yra tik pagrindinė sąskaita.

Naudokite puslapį **Finansinių dimensijų rinkiniai** kurti ir valdyti finansinių dimensijų rinkinius.

## <a name="dimension-set-balances"></a>Dimensijų rinkinio balansai

Dimensijų rinkinys gali turėti balansus, pagrįstus jo finansinėmis dimensijomis. Balansai yra Didžiojoje knygoje ir yra pagrįsti dimensijų rinkinio apibrėžimu. Balansai yra apibendrinami iš Didžiosios knygos duomenų, kad būtų pagerintas operacijų efektyvumas, kai jos nuskaitomos (pavyzdžiui, kai generuojamas bandomasis balansas).

## <a name="create-balances"></a>Balansų kūrimas

Naudokite mygtuką **Kurti balansus** norėdami inicijuoti dimensijų rinkinio, kuris šiuo metu neturi balansų, balansus.

> [!NOTE]
> Rekomenduojame riboti balansus turinčių dimensijų rinkinių skaičių, nes balanso atnaujinimai paveikia visas Didžiosios knygos registravimo veiklas.

## <a name="update-balances"></a>Atnaujinti balansus

Naudokite mygtuką **Atnaujinti balansus** norėdami į balansus įtraukti naujausią Didžiosios knygos registravimo veiklą. Balanso atnaujinimai yra lengvos operacijos. Jie turi apdoroti tik Didžiosios knygos registravimo veiklą, kuri įvyko po paskutinio atnaujinimo.

> [!NOTE]
> Bandomojo balanso rodymas sukelia atnaujinimą, siekiant užtikrinti, kad rodomi balansai yra dabartiniai. Apsvarstykite galimybę naudoti pasikartojančią paketinę užduotį, kad dažniausiai naudojamų dimensijų rinkinių naujinimai būtų spartieji. Tokiu būdu galite sumažinti bandomojo balanso vartotojų laukimo laiką.

## <a name="rebuild-balances"></a>Perkurti balansus

Naudokite mygtuką **Perkurti balansus**, kad iš naujo sukurtumėte balansus nuo pradžių. Tokiu būdu galite užtikrinti, kad jie atitinka Didžiosios knygos duomenis. Balansų perkūrimui reikia daug apdorojimo ir paprastai jis neturėtų būti reikalaujamas.

> [!NOTE]
> Jei naudojate scenarijų, kuriame reguliariai reikalaujama perkurti balansus, rekomenduojame kreiptis į klientų aptarnavimo tarnybą. Klientų aptarnavimo tarnyba gali padėti nustatyti, kodėl balansai neatitinka Didžiosios knygos duomenų.

## <a name="clear-balances"></a>Valyti balansus

Naudokite mygtuką **Valyti balansus**, kad pašalintumėte balansus ir sustabdytumėte bet kokius tolesnius atnaujinimus. Dimensijų rinkinys nebeturės įtakos Didžiosios knygos registravimo veikloms.

## <a name="delete-a-dimension-set"></a>Dimensijų rinkinio naikinimas

Nenaikite **ir iš naujo sukurkite dimensijų** rinkinius kaip bet kokios formos problemos, kad išspręskite potencialias problemas, susijusias su konkretaus dimensijų rinkinio balanso duomenimis. Dimensijų rinkinio perkūrimas yra įkainotas. Jei reikia pagalbos dėl problemų, susisiekite su klientų aptarnavimo tarnyba. 


Daugiau informacijos rasite [Finansinės dimensijos](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
