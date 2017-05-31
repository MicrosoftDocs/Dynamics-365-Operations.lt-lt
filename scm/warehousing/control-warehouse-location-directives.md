---
title: "Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus"
description: "Šiame straipsnyje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje darbas yra atliekamas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9d0ad4f64ee84da4e90dfa1525ebb5ff9fec4063
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašoma, kaip naudoti darbo šablonus ir vietos nurodymus, siekiant nustatyti, kaip ir kur sandėlyje darbas yra atliekamas.

Instrukcijos, kurias sandėlio darbuotojai gauna mobiliajame įrenginyje, yra nustatomos pagal darbo šablonus, nustatytus „Microsoft Dynamics 365 for Operations“ siekiant apibrėžti įvairius sandėlio procesus ir užduotis. Darbo šablonai nurodo, kaip darbas atliekamas kiekvieno sandėlio proceso metu. Vietos nurodymą susiedami su darbo šablonais galite užtikrinti, kad darbas bus vykdomas konkrečiose faktinėse sandėlių vietose.

## <a name="work-templates"></a>Darbo šablonai
Puslapyje **Darbo šablonai** galima apibrėžti darbo operacijas, kurį reikia atlikti sandėlyje. Paprastai sandėlio darbo operacijas sudaro du veiksmai: sandėlio darbuotojas paima turimas atsargas vienoje vietoje ir tada padeda paimtas atsargas kitoje vietoje. 

Darbo šablonus sudaro antraštė ir susietos eilutės. Kiekvienas darbo šablonas yra skirtas konkrečiam *darbo užsakymo tipui*. Daugelis darbo užsakymų tipų yra susieti su šaltinio dokumentais, pvz., pirkimo arba pardavimo užsakymais. Tačiau kiti darbo užsakymų tipai nurodo atskirus sandėlio procesus, pavyzdžiui, ciklo skaičiavimą. *Darbo telkinio ID* leidžia skirstyti darbą į grupes. 

Darbo antraštės aprašo parametrus galima naudoti norint nustatyti, kada turi būti sukurtas naujas darbas. Pavyzdžiui, galite nustatyti didžiausią paėmimo eilučių skaičių ir didžiausią numatomą paėmimo laiką. Tada, jei pardavimo užsakymo išrinkimo proceso darbas viršija vieną iš šių reikšmių, tas darbas yra padalijamas į du darbus. 

Darbo eilutės nurodo faktines užduotis, kurių reikia norint vykdyti darbą. Pvz., viena siuntimo sandėlio proceso darbo eilutė gali būti skirta prekes paimti sandėlyje, o kita eilutė – tas prekes padėti į išdėstymo sritį. Taip pat gali būti papildoma eilutė prekėms iš išdėstymo srities paimti ir dar viena eilutė prekėms į sunkvežimį pakrauti (tai yra krovimo proceso dalis). *Krypties kodas * gali būti nustatytas darbo šablono eilutėse. Krypties kodas yra susietas su vietos nurodymu ir todėl padeda užtikrinti, kad sandėlio darbas yra vykdomas tinkamoje sandėlio vietoje. 

Galite nustatyti užklausą, norėdami kontroliuoti, kada konkretus darbo šablonas naudojamas. Pavyzdžiui, galite nustatyti apribojimą, kad konkretus šablonas būtų naudojamas tik atliekant darbą konkrečiame sandėlyje. Taip pat galite nustatyti kelis šablonus, kurie būtų naudojami siuntimo pardavimo užsakymo apdorojimo darbui kurti, atsižvelgiant į pardavimo šaltinį. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų darbo šablonų vertinimo tvarką. Todėl, jei turite labai konkrečią užklausą dėl konkretaus darbo šablono, turėtumėte jai priskirti žemą sekos numerį. Tada ta užklausa bus vertinama anksčiau nei kitos, bendresnės užklausos. 

Norėdami darbo procesą sustabdyti arba pristabdyti, galite naudoti darbo eilutės parametrą **Stabdyti darbą**. Tokiu atveju darbą atliekančio darbuotojo nebus prašoma atlikti kitą darbo eilutės veiksmą. Norėdamas pereiti prie kito veiksmo, tas arba kitas darbuotojas turi pasirinkti darbą dar kartą. Taip pat galite atskirti darbo užduotis, darbo šablono eilutėse naudodami kitą *darbo klasės ID*.

## <a name="location-directives"></a>Vietos nurodymai
Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas. Pvz., pardavimo užsakymo operacijoje vietos nurodymas nustato, kur prekės bus paimtos ir kur bus padėtos. Vietos nurodymus sudaro antraštė ir susietos eilutės, o jie kuriami puslapyje **Vietos nurodymai**. 

Kiekvienas antraštės vietos nurodymas turi būti susietas su *darbo užsakymo tipu*, nurodančiu, kuriam atsargų operacijos tipui nurodymas bus skirtas, pvz., pardavimo užsakymas, papildymas arba žaliavų paėmimas. *Darbo tipas *nurodo, ar vietos nurodymas bus skirtas išrinkimo darbui, padėjimo darbui, ar kažkuriam kitam sandėlio procesui, pvz., skaičiavimui arba atsargų būsenos keitimams. Taip pat turi būti nurodyta *teritorija *ir *sandėlis*. Antraštėje nurodytas *krypties kodas * gali būti naudojamas vietos nurodymui su vienu ar daugiau darbo šablonų susieti. 

Kalbant apie darbo šablonus, nustatydami užklausą galite nurodyti, kada naudojamas konkretus vietos nurodymas. Pavyzdžiui, galite nurodyti, kad kai pardavimo užsakymo šaltinis yra e. prekyba, atsargas reikia paimti iš paskirtos sandėlio vietos. Sistema naudoja lauką **Sekos numeris**, kad nustatytų galimų vietos nurodymų vertinimo tvarką. 

Vietos nurodymo eilutės nustato papildomus vietos ieškos taisyklių taikymo apribojimus. Galite nurodyti mažiausią ir didžiausią kiekius, kuriems nurodymas būtų taikomas, taip pat galite nurodyti, kad nurodymas yra skirtas konkrečiam atsargų vienetui. Pavyzdžiui, jei matavimo vienetas yra padėklai, padėklų prekes galima padėti konkrečioje vietoje. Taip pat galite nurodyti, ar kiekis gali būti suskaidytas keliose vietose. Kaip ir vietos nurodymo antraštė, kiekviena vietos nurodymo eilutė turi sekos numerį, pagal kurį nustatoma eilučių vertinimo tvarka. 

Vietos nurodymams priskiriamas vienas papildomas informacijos lygis: *vietos nurodymo veiksmai*. Galite nurodyti kelis kiekvienos eilutės vietos nurodymo veiksmus. Primename, kad sekos numeris yra naudojamas veiksmų vertinimo tvarkai nustatyti. Šiame lygyje galite nustatyti užklausą, norėdami nurodyti, kaip rasti geriausią vietą sandėlyje. Taip pat galite naudoti iš anksto nustatytus **strategijos** parametrus optimaliausiai vietai rasti.

### <a name="example-of-the-use-of-location-directives"></a>Vietos nurodymų naudojimo pavyzdys

Šiame pavyzdyje apsvarstysime pirkimo užsakymo procesą, kai vietos nurodymas turi sandėlyje rasti laisvos vietos atsargų prekėms, kurios buvo ką tik užregistruotos gavimo rampoje. Pirmiausia pabandysime sandėlyje rasti laisvos vietos, konsoliduodami esamas atsargas. Jei konsoliduoti negalima, tada turime rasti tuščią vietą. 

Šiame scenarijuje turime nustatyti du vietos nurodymo veiksmus. Pirmasis sekos veiksmas turi naudoti strategiją **Konsoliduoti**, o antrasis – strategiją **Tuščia vieta, kurioje negaunama darbo**. Jei nenustatysite trečio veiksmo, skirto perpildos scenarijui tvarkyti, kai sandėlyje nėra vietos, galimi du rezultatai: darbą galima kurti net jei nėra nurodytų vietų arba darbo kūrimo procesas gali nepavykti. Rezultatas nustatomas pagal sąranką puslapyje **Vietos nurodymo klaidos**, kuriame galite nuspręsti, ar norite kiekvienam darbo užsakymų tipui nustatyti parinktį **Stabdyti darbą esant vietos nurodymo klaidai**.




