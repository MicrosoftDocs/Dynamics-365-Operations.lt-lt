---
title: Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus
description: Šiame straipsnyje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje darbas yra atliekamas.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65675d8a99d023176e3e66e92cd3d634750bdb0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877427"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje darbas yra atliekamas.

Instrukcijos, kurias sandėlio darbuotojai gauna mobiliajame įrenginyje, yra nustatomos pagal darbo šablonus, nustatytus „Dynamics 365 Supply Chain Management“ siekiant apibrėžti įvairius sandėlio procesus ir užduotis. Darbo šablonai nurodo, kaip darbas atliekamas kiekvieno sandėlio proceso metu. Vietos nurodymą susiedami su darbo šablonais galite užtikrinti, kad darbas bus vykdomas konkrečiose faktinėse sandėlių vietose.

## <a name="work-templates"></a>Darbo šablonai

Puslapyje **Darbo šablonai** galima apibrėžti darbo operacijas, kurį reikia atlikti sandėlyje. Paprastai sandėlio darbo operacijas sudaro du veiksmai: sandėlio darbuotojas paima turimas atsargas vienoje vietoje ir tada padeda paimtas atsargas kitoje vietoje. 

Darbo šablonus sudaro antraštė ir susietos eilutės. Kiekvienas darbo šablonas yra skirtas konkrečiam *darbo užsakymo tipui*. Daugelis darbo užsakymų tipų yra susieti su šaltinio dokumentais, pvz., pirkimo arba pardavimo užsakymais. Tačiau kiti darbo užsakymų tipai nurodo atskirus sandėlio procesus, pavyzdžiui, ciklo skaičiavimą. *Darbo telkinio ID* leidžia skirstyti darbą į grupes. 

Naudokite nustatymus darbo antraštės sąvokoje siekiant nustatyti, kai nauja darbo dalis turi būti sukurta. Pavyzdžiui, galite nustatyti didžiausią paėmimo eilučių skaičių ir didžiausią numatomą paėmimo laiką. Tada, jei pardavimo užsakymo išrinkimo proceso darbas viršija vieną iš šių reikšmių, tas darbas yra padalijamas į du darbus.

Naudokite **Darbo antraštės pertrūkiai** mygtuką, kad nustatytumėte, kada sistema turi sukurti naują darbo antraštę. Pavyzdžiui, norėdami sukurti darbo antraštę kiekvienam _užsakymo numeriui_, pasirinkite **Redaguoti užklausą** veiksmų juostoje ir tada įtraukite **Užsakymo numerį** laukelį į **Rūšiavimo** skirtuką užklausos redaktoriuje. Laukeliai yra įtraukti į **Rūšiavimo** skirtuką ir yra prieinami pasirinkimui kaip *laukelių grupavimas*. Norėdami nustatyti savo grupavimo laukelius rinkitės **Darbo antraštės pertraukimas** veiksmų juostoje ir tada kiekvienam laukeliui, kurį norite naudoti kaip laukelių grupavimą, pasirinkite žymės laukelį, esantį **Grupuoti šį laukelį** stulpelyje.

Darbo eilutės rodo fizines užduotis, kurių reikia darbo procesui. Pavyzdžiui, išvesties sandėlio procesui gali būti viena paėmimo eilutę prekėms sandėlyje ir kita eilutę padėjimui šių prekių parengimo srityje. Gali tuomet būti papildoma eilutė prekių paėmimui iš parengimo vietos ir kita eilutė prekių padėjimui ant sunkvežimio kaip krovinio proceso dalis. *Krypties kodas* gali būti nustatytas darbo šablono eilutėse. Krypties kodas yra susiejamas su vietos kryptimi ir dėl to padeda užtikrinti, kad sandėlio darbas yra apdorojamas tinkamoje vietoje sandėlyje.

Galite nustatyti užklausą, norėdami kontroliuoti, kada konkretus darbo šablonas naudojamas. Pavyzdžiui, galite nustatyti apribojimą, kad konkretus šablonas būtų naudojamas tik atliekant darbą konkrečiame sandėlyje. Kitu atveju, jums gali reikėti kelių šablonų, kad sukurtumėte darbą pardavimo užsakymo apdorojimui, priklausomai nuo pardavimo kilmės. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų darbo šablonų vertinimo tvarką. Todėl, jei turite labai konkrečią užklausą dėl konkretaus darbo šablono, turėtumėte jai priskirti žemą sekos numerį. Ta užklausa tuomet bus vertinama prieš kitą, bendresnę užklausą.

> [!NOTE]
> Siekiant apsaugoti sistemą nuo automatinio užrašymo darbo šablone *sekos skaičiai* po to, kai šablonas buvo panaikintas, įjunkite *Išsaugoti darbo šablono sekos skaičius naikinimui* funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Norėdami darbo procesą sustabdyti arba pristabdyti, galite naudoti darbo eilutės parametrą **Stabdyti darbą**. Tokiu atveju darbą atliekančio darbuotojo nebus prašoma atlikti kitą darbo eilutės veiksmą. Norėdamas pereiti prie kito veiksmo, tas arba kitas darbuotojas turi pasirinkti darbą dar kartą. Taip pat galite atskirti darbo užduotis, darbo šablono eilutėse naudodami kitą *darbo klasės ID*.

## <a name="location-directives"></a>Vietos nurodymai

Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas. Pvz., pardavimo užsakymo operacijoje vietos nurodymas nustato, kur prekės bus paimtos ir kur bus padėtos. Vietos nurodymus sudaro antraštė ir susietos eilutės, o jie kuriami puslapyje **Vietos nurodymai**.

Kiekvienas antraštės vietos nurodymas turi būti susietas su *darbo užsakymo tipu*, nurodančiu, kuriam atsargų operacijos tipui nurodymas bus skirtas, pvz., pardavimo užsakymas, papildymas arba žaliavų paėmimas. *Darbo tipas* nurodo, ar vietos nurodymas bus skirtas išrinkimo darbui, padėjimo darbui, ar kažkuriam kitam sandėlio procesui, pvz., skaičiavimui arba atsargų būsenos keitimams. Taip pat turi būti nurodyta *teritorija* ir *sandėlis*. Antraštėje nurodytas *krypties kodas* gali būti naudojamas vietos nurodymui su vienu ar daugiau darbo šablonų susieti. 

Kalbant apie darbo šablonus, nustatydami užklausą galite nurodyti, kada naudojamas konkretus vietos nurodymas. Pavyzdžiui, galite nurodyti, kad kai pardavimo užsakymo šaltinis yra e. prekyba, atsargas reikia paimti iš paskirtos sandėlio vietos. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų vietos nurodymų vertinimo tvarką.

Vietos nurodymo eilutės nustato papildomus vietos ieškos taisyklių taikymo apribojimus. Galite nurodyti mažiausią ir didžiausią kiekius, kuriems nurodymas būtų taikomas, taip pat galite nurodyti, kad nurodymas yra skirtas konkrečiam atsargų vienetui. Pavyzdžiui, jei matavimo vienetas yra padėklai, padėklų prekes galima padėti konkrečioje vietoje. Taip pat galite nurodyti, ar kiekis gali būti suskaidytas keliose vietose. Kaip ir vietos nurodymo antraštė, kiekviena vietos nurodymo eilutė turi sekos numerį, pagal kurį nustatoma eilučių vertinimo tvarka.

Vietos nurodymams priskiriamas vienas papildomas informacijos lygis: *vietos nurodymo veiksmai*. Galite nurodyti kelis kiekvienos eilutės vietos nurodymo veiksmus. Primename, kad sekos numeris yra naudojamas veiksmų vertinimo tvarkai nustatyti. Šiame lygyje galite nustatyti užklausą, norėdami nurodyti, kaip rasti geriausią vietą sandėlyje. Taip pat galite naudoti iš anksto nustatytus **strategijos** parametrus optimaliausiai vietai rasti.

Dėl daugiau informacijos, kaip sukurti ir konfigūruoti direktyvas, žr. [Sukurti vietos direktyvą](create-location-directive.md).

### <a name="how-location-directives-work"></a>Kaip vietos kryptys veikia

Vietos kryptys nustato *ar* prekės turi būti paimamos ir *kur* jos turi būti padėtos. Sistema įvertina vietos kryptį lyginant su kiekvieno darbo eilute ir tada pasirenka vietą priklausomai nuo darbo eilutės išsamios informacijos. Sistema pirmiausia suranda visas vietos kryptis, kurios atitinka konkrečią darbo eilutę (pavyzdžiui, jos yra tinkamam sandėliui ir atitinka užklausą). Ji vėliau įvertina rastą kryptį.

> [!NOTE]
> Esama konkrečių atvejų, kai paėmimo vieta ar padėjimo vieta pasirenkama iš anksto. Pavyzdžiui, _įsigijimo registracija_, pirmasis paėmimas visada yra iš vietos, kurioje registracija įvyksta. Kitas pavyzdys yra *inventoriaus judėjimas pagal šabloną*, kai sandėlio darbuotojas pasirenka paėmimo vietą ir tik padėjimo vietos yra randamos per vietos kryptis.

## <a name="additional-resources"></a>Papildomi ištekliai

- Vaizdo įrašas: [Sandėlio valdymo konfigūravimo gili analizė](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Žinyno straipsnis: [Darbas su vietos nurodymais](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]