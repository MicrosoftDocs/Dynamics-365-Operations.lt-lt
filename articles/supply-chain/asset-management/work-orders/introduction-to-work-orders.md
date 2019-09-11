---
title: Įvadas į darbo užsakymus
description: Šioje temoje pateikiama darbo užsakymų modulyje Turto valdymas apžvalga.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875806"
---
# <a name="introduction-to-work-orders"></a>Įvadas į darbo užsakymus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Darbo užsakymai naudojami priežiūros užduotims tvarkyti, pateikti joms būtiną informaciją ir priežiūros užduočių suvartojimui registruoti. Darbo užsakyme gali būti viena arba keletas darbo užsakymo užduočių; su darbo užsakymu galima susieti vieną arba daugiau turto vienetų. Kiekvienoje darbo užsakymo eilutėje apibrėžiama turtui suplanuota priežiūros užduotis.

Darbo užsakymus galima kurti automatiškai arba rankiniu būdu.

- Automatiškai jie kuriami naudojant formą **Priežiūros planų planavimas**, kai pagal kalendorių vykdomuose priežiūros planuose nustatyta „Automatinis kūrimas“.  

- Automatiškai jie kuriami naudojant formą **Priežiūros ciklų planavimas**, kai pagal kalendorių vykdomuose priežiūros cikluose nustatyta „Automatinis kūrimas“.  

- Kūrimas pagal priežiūros grafiką: galima kurti prevencinės priežiūros užduotis arba priežiūros užklausas.  

- Darbo užsakymo kūrimas rankiniu būdu.  

- Darbo užsakymo kūrimas naudojant **Visos priežiūros užklausos**, **Aktyviosios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**.

>[!NOTE]
>Darbo užsakymų užduotys, susijusios su tuo pačiu turtu, yra susijusios su tuo pačiu projekto ID.

## <a name="all-work-orders"></a>Visi darbo užsakymai

Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai**, kad atidarytumėte sąrašą. Pasirinkus **Visi darbo užsakymai**, pateikiamas visų darbo užsakymų sąrašas ir rodoma dalis informacijos, susijusios su darbo užsakymu.

![1 pav.](media/01-work-orders.png)

- Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Aktyvieji darbo užsakymai**, kad pamatytumėte aktyviųjų darbo užsakymų sąrašą.

- Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Mano funkcinės vietos darbo užsakymų priežiūros užduotys**, kad pamatytumėte darbo užsakymų užduočių, susijusių su turtu, įdiegtu funkcinėse vietose, kuriose jūs esate darbuotojas (kaip nustatyta skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md)), sąrašą.

- Sąraše **Visi darbo užsakymai** (nustatę tinklelio rodinį), spustelėkite nuorodą stulpelyje **Darbo užsakymas**, kad įjungtumėte pasirinkto įrašo rodinį Informacija. Spustelėkite mygtuką **Redaguoti**, kad atidarytumėte įrašą norėdami jį redaguoti.  

- Rodinyje Informacija matote išsamia informaciją apie darbo užsakymą.  

- Rodinyje Informacija pasirinkite nuorodą **Eilutės**, kad pamatytumėte išsamią informaciją apie darbo užsakymo užduotį, arba pasirinkite nuorodą **Antraštė**, kad pamatytumėte išsamią informaciją apie darbo užsakymą.  

- Ekrano dešinėje esančioje vertikalioje srityje **Susijusi informacija** pateikiama papildoma su darbo užsakymu susijusi informacija. Išplėskite sritį, kad pamatytumėte su pasirinktu darbo užsakymu susijusią informaciją.  


![2 paveikslėlis](media/02-work-orders.png)


Veiksmų srities mygtukai suskirstyti į skirtukus veiksmų srityje. Toliau pateikiamas trumpas su įmonių turto valdymu susijusių mygtukų aprašas.



| Mygtuko pavadinimas                     | Aprašymas                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redagavimas                            | Pasirinkto darbo užsakymo redagavimas.                                                                                                                                                                                                                                           |
| Naujos                             | Naujo darbo užsakymo kūrimas.                                                                                                                                                                                                                                                  |
| Naikinti                          | Pasirinkto darbo užsakymo naikinimas.                                                                                                                                                                                                                                         |
| Darbo užsakymų telkinys                 | Pasirinkto darbo užsakymo įtraukimas į darbo užsakymų telkinį arba jo pašalinimas iš darbo užsakymų telkinio.                                                                                                                                                                                           |
| Koreguoti                          | Informacijos apie pasirinktų darbo užsakymų numatomą pradžią ir pabaigą, aptarnavimo lygį, atsakingą priežiūros darbuotoją arba atsakingą priežiūros darbuotojų grupę koregavimas.                                                                                                                                     |
| Susijęs darbo užsakymas              | Naujo darbo užsakymo, susijusio su pasirinkta darbo užsakymo užduotimi, kūrimas. Naudinga, jei norite registruoti pirminius ir antrinius darbo užsakymus.                                                                                                                              |
| Kopijuoti darbo užsakymą                 | Naujo darbo užsakymo kūrimas pagal esamą darbo užsakymą.                                                                                                                                                                                                                |
| Įvykių retrospektyva                   | Darbo užsakymo registravimo retrospektyvos peržiūra.                                                                                                                                                                                                                |
| Darbo užsakymo priežiūros užduočių pastabos                           | Darbo užsakymo aprašo arba pastabų kūrimas. Pradėkite, spustelėdami mygtuką **Įtraukti lako žymą**, kad į pastabą įtrauktumėte savo vartotojo vardą ir laiko žymą. Pastabos rodomos formoje **Darbo užsakymas** > FastTab **Eilutės informacija** > skirtuke **Aprašas**. |
| Įrankiai                           | Būtinų darbo užsakymo įrankių kūrimas. Įrankiai pateikiami kaip ištekliai, pasirinkus **Organizacijos administravimas** > **Bendra** > **Ištekliai** > **Ištekliai**.                                                                                                      |
| Prižiūrimo turto kontrolinis sąrašas           | Su darbo užsakymu susijusio turto kontrolinio sąrašo peržiūra.                                                                                                                                                                                                              |
| Turto gedimas                     | Turto gedimo informacijos, kuri bus naudojama valdant gedimus, peržiūra arba registravimas.                                                                                                                                                                                        |
| Prižiūrimo turto prastova            | Darbo užsakymo prižiūrimo turto prastovos nurodymas.                                                                                                                                                                                                                               |
| Sąlygos įvertinimas            | Darbo užsakymo sąlygos įvertinimo matmenų registravimas.                                                                                                                                                                                                             |
| Turto skaitikliai                 | Turto skaitiklio registracijų kūrimas arba peržiūra.                                                                                                                                                                                                                     |
| Prognozė                        | Darbo užsakymo prognozių kūrimas arba peržiūra.                                                                                                                                                                                                                               |
| Žurnalai                        | Darbo užsakymo žurnalų kūrimas arba peržiūra. Žurnalo eilutes galimo nukopijuoti iš prognozių.                                                                                                                                                                                         |
| Projekto operacijos            | Visų su turto darbo užsakymais susijusių užregistruotų operacijų peržiūra.                                                                                                                                                                                             |
| Darbo užsakymo būsenos naujinimas                | Darbo užsakymo ciklo būsenos naujinimas.                                                                                                                                                                                                                                                |
| Ciklo būsenos žurnalas                       | Pasirinkto darbo užsakymo ciklo būsenų žurnalas.                                                                                                                                                                                                                   |
| Turto dokumentai                | Su darbo užsakymu susijusio turto dokumentų sąrašo peržiūra. Šie dokumentai pateikiami pasirinkus **Turto valdymas** > **Sąranka** > **Turto dokumentai**.                                                                                                 |
| Grafikas                        | Pasirinktų darbo užsakymų planavimas.                                                                                                                                                                                                                                      |
| Išsiųsti            | Pasirinkto darbo užsakymo planavimas vienam darbuotojui.                                                                                                                                                                                                                        |
| Naikinti grafiką                 | Pasirinkto darbo užsakymo grafiko naikinimas.                                                                                                                                                                                                                          |
| Suplanuotos darbo užsakymo priežiūros užduotys             | Sąrašo puslapio **Suplanuotos darbo užsakymo priežiūros užduotys** atidarymas.                                                                                                                                                                                                                             |
| Darbo užsakymo pirkimo paraiška | Sąrašo puslapio **Darbo užsakymo pirkimo paraiška** atidarymas.                                                                                                                                                                                                                 |
| Darbo užsakymo pirkimas             | Sąrašo puslapio **Darbo užsakymo pirkimas** atidarymas.                                                                                                                                                                                                                             |
| Išlaidų kontrolė                    | Darbo užsakymo biudžeto išlaidų ir faktinių išlaidų palyginimas.                                                                                                                                                                                                                |
| Valandų kontrolė                    | Darbo užsakymo prognozuotų valandų ir faktinių valandų palyginimas.                                                                                                                                                                                                                |
| Darbo užsakymo ataskaita               | Darbo užsakymo ataskaitos spausdinimas.                                                                                                                                                                                                                                                |
| Darbo užsakymo suvartojimas          | Suvartojimo ataskaitos spausdinimas.                                                                                                                                                                                                                                               |


Mygtukai skirtuke **Darbo užsakymas** > grupėje **Projektas** yra susiję su modulio **Projektų valdymas ir apskaita** funkcija, susijusia su prognozėmis, žurnalais ir sąskaitų išrašymu.

>[!NOTE]
>Sukurtas darbo užsakymo prognozes galima įtraukti, vykdant bendrąjį planavimą ir naudojant prognozės modelį, pasirinktą formoje **Turto valdymo parametrai**.

