---
title: Išlaidų pokyčio modeliavimas naudojant suplanuotų išlaidų įkainojimo versiją
description: Šiame straipsnyje paaiškinta, kaip modeliuoti išlaidų pokyčio poveikį pagamintos prekės apskaičiuotoms išlaidoms naudojant atskirą suplanuotų išlaidų įkainojimo versiją.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 627c45a6cd7b647c0cb11ad4a4470bf143fff6cd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821470"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a>Išlaidų pokyčio modeliavimas naudojant suplanuotų išlaidų įkainojimo versiją

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip modeliuoti išlaidų pokyčio poveikį pagamintos prekės apskaičiuotoms išlaidoms naudojant atskirą suplanuotų išlaidų įkainojimo versiją.

Išlaidų pokyčio poveikį apskaičiuotoms pagamintų prekių išlaidoms galite modeliuoti naudodami atskirą suplanuotų išlaidų įkainojimo versiją. Norėdami įvesti laukiamų išlaidų įrašus, atspindinčius didėjančius išlaidų pokyčius ir apskaičiuoti išlaidų poveikį pagamintoms prekėms, naudokite šią atskirą įkainojimo versiją. Kadangi skaičiuojant KS bus naudojamas atsarginis Aktyvių išlaidų principas, reikės įvesti tik didėjančius išlaidų pokyčius.

## <a name="guidelines-for-defining-the-simulation-costing-version"></a>Įkainojimo modeliavimo versijos apibrėžimo nuorodos
Apibrėždami įkainojimo modeliavimo versiją, vadovaukitės šiais nurodymais:

-   Priskirkite įkainojimo tipą **Suplanuotos išlaidos**.
-   Priskirkite prasmingą įkainojimo versijos identifikatorių, pvz., **Modeliavimas**.
-   Įsitikinkite, kad turinyje yra išlaidų įrašai.
-   Leiskite išlaidų įrašų įrašą. Neužblokuokite laukiamų išlaidų įrašo.
-   Leiskite išlaidų įrašų įrašą visose svetainėse. Priskyrę vieną svetainę, išlaidų įrašų įrašą apribosite į tą svetainę.
-   Apsaugoti laukiančių išlaidų aktyvinimą. Įkainojimo modeliavimo versijoje kaip išlaidų įrašai turi būti įvestos tik laukiančios išlaidos.
-   Neįveskite datos „Nuo“. Skaičiavimo data bus įvesta kiekvienam KS skaičiavimui, naudojančiam įkainojimo modeliavimo versiją.
-   Nurodykite atsarginį principą **Dabartinis aktyvus**. Atsarginis principas leidžia įvesti didėjančius išlaidų pokyčius modeliavimui, dabartines aktyvias išlaidas naudojant kaip visų kitų išlaidų įrašų šaltinį. Laikome, kad visiems kitiems išlaidų įrašams yra dabartinės aktyvios išlaidos.
-   Nurodykite **Versijos savikainos modelis**, bet neapribokite skaičiavimų. Pvz., siekiant nurodyti išlaidų poveikio nupirktoms prekėms duomenų šaltinį, modeliuojant taip pat gali būti naudojamas savikainos modelis **KS skaičiavimo grupė**.
-   Nurodykite **Kelių lygių** išskleidimo režimą, bet neapribokite skaičiavimų. Modeliuojant gali būti naudojami kiti išskleidimo režimai.

## <a name="costing-versions"></a>Įkainojimo versijos
Toliau pateiktais scenarijais iliustruojama, kaip įkainojimo modeliavimo versijos naudojamos, modeliuojant išlaidų pokyčių poveikį. Prieš įvesdami sumodeliuotą išlaidų pokytį, panaikinkite įkainojimo modeliavimo versijos laukiančių išlaidų įrašus, kad pradėtumėte nuo nulio. Norėdami peržiūrėti ir panaikinti laukiančių išlaidų įrašus, susijusius su prekių kainomis ir išlaidų kategorijos kainomis, naudokite puslapį **Prekės kaina**.

-   Sumodeliuokite nupirktos prekės išlaidų pokytį. Pvz., išlaidų pokytis gali atspindėti numatomą kritinių nupirktų medžiagų išlaidų padidėjimą ar sumažėjimą. Norėdami nurodyti skirtingas nupirktos prekės išlaidas, naudodami puslapį **Prekės kaina** įkainojimo modeliavimo versijoje įveskite laukiančių išlaidų įrašą.
-   Sumodeliuokite išlaidų kategorijos išlaidų pokytį. Pvz., išlaidų pokytis gali atspindėti numatomą darbo tarifų ar operacijų išteklių valandinių tarifų padidėjimą ar sumažėjimą. Norėdami nurodyti skirtingas išlaidų kategorijos išlaidas, naudodami puslapį **Išlaidų kategorijos kaina** įkainojimo modeliavimo versijoje įveskite laukiančių išlaidų įrašą.
-   Netiesioginių išlaidų skaičiavimo formulėje sumodeliuokite išlaidų pokytį. Pvz., išlaidų pokytis gali atspindėti numatomą gamybos pridėtinių išlaidų padidėjimą ar sumažėjimą. Norėdami nurodyti netiesioginių išlaidų skaičiavimo formulės pokytį, naudodami puslapį **Įkainojimo lapo nustatymas** įkainojimo modeliavimo versijoje įveskite įrašą apie laukiančias išlaidas, patikrinkite ir įrašykite keitimą.

Įvedę sumodeliuotus išlaidų pokyčius, apskaičiuokite pagamintų prekių, kurias paveikė išlaidų pokyčiai, išlaidas. Įkainojimo modeliavimo versijai naudodami puslapį **Skaičiavimas** nustatykite pasirinktas pagamintas prekes, kurioms turės įtakos išlaidų pokyčiai. KS skaičiavimai taikomi visoms pagamintoms prekėms, nebent jūs pasirenkate konkrečias prekes. Taip pat galite naudoti KS skaičiavimo pasirinktį, skirtą duomenų apie naudojimą atnaujinimams. Norėdami analizuoti, kaip modeliuojami išlaidų pokyčiai veikia pasirinktų pagamintų prekių išlaidas, peržiūrėkite prekės išlaidų įrašus įkainojimo modeliavimo versijoje. Norėdami peržiūrėti ir analizuoti išlaidas naudokite puslapius **Prekės kaina** ir **Skaičiuoti prekės savikainą**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]