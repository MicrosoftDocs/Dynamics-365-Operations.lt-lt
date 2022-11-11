---
title: Nustatyti užduotis užduočių valdymo dalyje
description: Šiame straipsnyje paaiškinama, kaip nustatyti "Microsoft" užduočių valdymo užduotis Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745423"
---
# <a name="set-up-tasks-in-task-management"></a>Nustatyti užduotis užduočių valdymo dalyje

[!INCLUDE [PEAP](../includes/peap-1.md)]

Programos Microsoft Dynamics 365 Human Resources versijose iki versijos 10.0.30 vartotojai, norintys redaguoti užduotį, turi atskirai redaguoti tą užduotį kiekviename kontroliniame sąraše, kuriame ji yra. Tačiau, kaip personalo 10.0.30 versija, vartotojai gali pasirinkti, kaip tvarkomos redaguotos užduotys. Jei redaguojama užduotis yra kontroliniame sąraše, personalo bendrinamų parametrų puslapio užduočių valdymo skirtuke reikia pasirinkti parinktį Įgalinti užduočių valdymo atnaujinimą, **·** **·** **kad** kontroliniame sąraše būtų galima naudoti redaguotą užduotį.

[![Įgalinkite užduočių valdymo atnaujinimo parinktį personalo bendrinamų parametrų puslapyje.](./media/task-update.png)](./media/task-update.png)

Jei užduočių redagavimai turi būti taikomi visoms susijusioms kontrolinio sąrašo užduotims, jau turi būti ryšys tarp užduoties užduočių bibliotekoje ir kontrolinio sąrašo užduoties. Pasirinktis buvo pridėta, kad būtų sukurtas ryšys tarp bibliotekos užduoties ir kontrolinio sąrašo užduoties.

Galite sukurti užduotis atskirai ir pakartotinai naudoti jas keliuose kontroliniuose sąraše. Norėdami sukurti užduotį, puslapio **Inboarding setup** skirtuke **Užduotys** pasirinkite **Nauja**.

## <a name="set-up-tasks"></a>Nustatyti užduotis

Norėdami sukurtą užduotį priskirti keliems kontroliniams sąrašui, pasirinkite užduotį ir **meniu kontroliniams sąrašui** pasirinkite Taikyti.

Taip pat galite pridėti užduotis tiesiogiai į kontrolinį sąrašą. Norėdami įtraukti užduotį į kontrolinį sąrašą, **skirtuko Kontrolinio sąrašo puslapyje Inboarding setup** **sukurkite** naują kontrolinį sąrašą, kad įtraukumėte užduotį, arba įtraukite užduotį į esamą kontrolinį sąrašą.

Norėdami redaguoti bibliotekos užduotį, užduočių **bibliotekos** meniu pasirinkite Redaguoti. Jei užduotis susieta su bet kuriuo kontroliniu sąrašu, tie kontroliniai sąrašai bus rodomi užduoties **redagavimo** puslapyje. Jei norite, kad bet kurio kontrolinio sąrašo užduotys būtų atnaujintos naudojant redagavimus, **pasirinkite tuos kontrolinius sąrašus skyriuje Taikyti kontroliniams sąrašas**.

Norėdami panaikinti užduotis iš užduočių bibliotekos, pasirinkite **Naikinti**. Jei užduotis susieta su kontroliniu sąrašu, šis veiksmas nebus panaikintas užduoties iš kontrolinio sąrašo. Norint pašalinti užduotį iš kontrolinio sąrašo, reikia atskiro veiksmo.

### <a name="set-up-checklists"></a>Nustatyti kontrolinius sąrašus

Kontrolinis sąrašas yra užduočių grupė. Galite sukurti tiek kontrolinių sąrašų, kiek jums reikia, ir tas pačias užduotis galite priskirti keliems kontroliniams sąrašui. Kai kuriate kontrolinį sąrašą, nurodote savininką ir kalendorių.

Norėdami kontroliniame sąraše sukurti naują užduotį, užduočių **meniu** juostoje pasirinkite Nauja. Kai kuriate naują užduotį, galite pasirinktinai įtraukti užduotį į užduočių biblioteką, kad ją būtų galima bendrai naudoti keliuose kontroliniuose sąraše. Norėdami įtraukti užduotį į užduočių biblioteką, turite nustatyti parinktį **Taikyti užduotį bibliotekai** kaip **Taip**. Jei pasirinksite įtraukti užduotį į užduočių biblioteką, **ją į kitus kontrolinius sąrašus taip pat galėsite įtraukti vienu metu pasirinkdami tuos kontrolinius sąrašus skyriuje Taikyti kontroliniams sąrašas**. Jei pasirinksite jos neįtraukti į užduočių biblioteką, užduotis bus tik kontroliniame sąraše, kuriame ją sukursite.

Norėdami kontroliniame sąraše redaguoti užduotį, užduočių **meniu** pasirinkite Redaguoti. Jei užduotis susieta su bet kuriuo kontroliniu sąrašu, tie kontroliniai sąrašai bus rodomi užduoties **redagavimo** puslapyje. Jei norite, kad užduotys bet kuriame iš kitų kontrolinių sąrašų būtų atnaujintos naudojant redagavimus, **pasirinkite tuos kontrolinius sąrašus skyriuje Taikyti kontroliniams sąrašai**.

Norėdami pašalinti užduotis iš kontrolinio sąrašo, pasirinkite **Pašalinti**. Šis veiksmas pašalins užduotis iš kontrolinio sąrašo. Tačiau užduočių biblioteka užduočių nepanaikins. Norėdami panaikinti užduotis iš užduočių bibliotekos, atidarykite užduočių **bibliotekos** puslapį ir pasirinkite **Naikinti**.
