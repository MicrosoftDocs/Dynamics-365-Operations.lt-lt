---
title: Finansinių dimensijų rinkiniai
description: Šioje temoje aprašomi finansinių dimensijų rinkiniai ir pateikiami jų naudojimo optimizavimo patarimai.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 415a41100cc5be740f064d52598cd256c0aa2ae1d45473c8039bdc6e22381b3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739983"
---
# <a name="financial-dimension-sets"></a>Finansinių dimensijų rinkiniai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi finansinių dimensijų rinkiniai ir pateikiami jų naudojimo optimizavimo patarimai.

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

Daugiau informacijos rasite [Finansinės dimensijos](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
