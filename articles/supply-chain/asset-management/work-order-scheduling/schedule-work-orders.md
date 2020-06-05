---
title: Planuoti darbo užsakymus
description: Šioje temoje paaiškinta, kaip planuoti darbo užsakymus modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e98a30a03856f5532d420e516cb35d66acffb278
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383494"
---
# <a name="schedule-work-orders"></a>Planuoti darbo užsakymus

[!include [banner](../../includes/banner.md)]

 

Šioje temoje paaiškinta, kaip planuoti darbo užsakymus modulyje Turto valdymas. 

Darbo užsakymui reikalingas valandų skaičius nustatomas iš prognozuojamų valandų sumos atėmus paskelbtas valandas. Jei reikia daugiau laiko, reikia atitinkamai koreguoti prognozę. Srityje **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai** galite peržiūrėti arba redaguoti prognozes apie darbo užsakymą pasirinkdami darbo užsakymą ir skirtuke **Darbo užsakymas** spustelėję **Prognozė**. Sukūrus ir įvertinus darbo užsakymus, kitas veiksmas užbaigiant darbo užsakymus yra paskirti reikalingus priežiūros darbuotojus ir įrankius.

Galima planuoti tik darbo užsakymus, kurių darbo užsakymo ciklo būsena leidžia planavimą. Planavimo leidimas nustatomas srityje **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Ciklo būsenos** > **„FastTab“ Bendra** > perjungimo mygtukas **Leisti planavimą**.

1. Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai**.

2. Sąraše pažymėkite darbo užsakymus, kuriuos norite planuoti. Pavyzdžiui, sąrašą galite rikiuoti pagal **Dabartinę ciklo būseną**.

3. Skirtuke **Bendra** spustelėkite **Grafikas**.

4. Dialogo lange **Planuoti darbo užsakymus**, jei reikia, galite pasirinkti parametrus, susijusius su numatoma pradžios data ir aptarnavimo lygiu. Jei planavimo proceso metu reikia atsižvelgti į pajėgumo apribojimus, susijusius su jau suplanuotais kitų užduočių ištekliais, įsitikinkite, kad perjungimo mygtukai **Turtas**, **Įrankis** ir **Darbuotojas** yra nustatyti į „Taip“.

    [!NOTE]
    Jei perjungimo mygtukus **Turtas**, **Įrankis** ir **Darbuotojas** nustatysite į „Ne“, bus nepaisoma esamų rezervavimų. Sistemos pranešime bus rodomas persidengiančių darbo užsakymų grafikų sąrašas ir, jei reikia, galite spustelėti pranešimus, kad atidarytumėte darbo užsakymą ir jį suplanuotumėte iš naujo.

5. Norėdami peržiūrėti išsamią informaciją apie planavimo procesą, perjungimo mygtuke **Daugiažodis** pasirinkite „Taip“. Tai reiškia, kad išsami informacija apie darbo užsakymų ir priežiūros darbuotojų apskaičiuotus rezultatus bus rodoma sistemos pranešime.

6. Spustelėkite **Gerai**, kad pradėtumėte planavimo procesą.

7. Baigus planavimą sistemos pranešime rodomas suplanuotų darbo užsakymų skaičius bei išsamesnė informacija, jei perjungimo mygtukas **Daugiažodis** buvo nustatytas į „Taip“.

>[!NOTE]
>Darbo užsakymai planuojami per vieną ciklą vienam darbo užsakymui, o ne per darbo užsakymo užduotį. Taip pat galite atidaryti dialogo langą **Planuoti darbo užsakymus** tiesiogiai srityje **Turto valdymas** > **Periodinis** > **Darbo užsakymai** > **Planuoti darbo užsakymus**. Pažymėkite reikiamas parinktis ir spustelėkite **Gerai**, kad pradėtumėte darbo užsakymo planavimą. Darbo užsakymo planavimą galima nustatyti kaip paketinę užduotį dialogo lange **Planuoti darbo užsakymus** > „FastTab“ **Vykdyti fone**.

*Pavyzdys:* toliau pateiktame paveikslėlyje lauke **Numatoma pradžia** įvesta formulė generuos visų darbo užsakymų, kurių numatyta pradžios data už savaitės nuo dabar ir vėliau, grafikus. Ši formulė gali praversti, jei nuolat vykdote darbo užsakymų planavimą, tačiau norite užtikrinti, kad ateinančioms 5–6 dienoms suplanuoti darbo užsakymai nebūtų suplanuoti iš naujo.

![1 pav.](media/03-work-order-scheduling.png)

Pagal darbo užsakymo tipą, susijusį su darbo užsakymais, gali būti nustatomas vieno priežiūros darbuotojo planavimas (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Darbo užsakymų tipai** > perjungimo mygtuką **Vienas priežiūros darbuotojas** nustačius į „Taip“). Tai reiškia, kad, jei darbo užsakyme naudojamas darbo užsakymo tipas, perjungimo mygtukas **Vienas priežiūros darbuotojas** yra automatiškai nustatomas į „Taip“ išsamios informacijos puslapyje **Visi darbo užsakymai** > rodinyje **Antraštė** > „FastTab“ **Planuoti**. Planuojant darbo užsakymą visos jame sukurtos darbo užsakymo užduotys vėliau bus suplanuotos tam pačiam priežiūros darbuotojui. Jei reikia, galite redaguoti pasirinkimą perjungimo mygtuke **Vienas priežiūros darbuotojas** puslapyje **Visi darbo užsakymai**, kad darbo užsakymo užduotyse būtų galima planuoti kelis darbuotojus arba vieną darbuotoją.

Planavimo procese naudojant modulį Turto valdymas apskaičiuojant grafiką naudojami keli veiksniai.

- Skaičiuojami ir darbo užsakymų, ir priežiūros darbuotojų rezultatai. Darbo užsakymų ir priežiūros darbuotojų rezultatai nustatomi **Turto valdymo parametruose**. 
- Tikrinama, ar yra užduočiai atlikti reikalingos sutampančios kompetencijos, t. y., įgūdžiai ir pažymėjimai. Priežiūros darbuotojų įgūdžiai ir liudijimai nustatomi modulyje **Žmogiškieji ištekliai** (**Žmogiškieji ištekliai** > **Darbuotojai** > **Darbuotojai** > sąraše pasirinkite darbuotoją > skirtukas **Darbuotojas** > skyrius **Kompetencijos** > mygtukai **Įgūdžiai** ir **Liudijimai**). Be to, įgūdžius ir liudijimas galima įtraukti į priežiūros užduočių tipus ir priežiūros užduočių profesijas. Norėdami gauti daugiau informacijos apie kompetencijas ir priežiūros užduočių tipus žr. [Priežiūros užduočių tipų kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipų variantai, priežiūros užduočių profesijos ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Planuojant darbo užsakymus naudojami rezultatai

Darbo užsakymo užduoties rezultatai apskaičiuojami pagal darbo užsakymo numatomą pradžios datą ir aptarnavimo lygį.

**Pradžios datos** apskaičiavimas: iš kiekvienos ateities datos, apskaičiuotos pagal numatomą pradžios datą, atimamas pradžios datos rezultatas ir padauginamas iš rezultato, kuris toliau pateiktuose pavyzdžiuose yra „10“.

**Svarbos** apskaičiavimas: svarbos rezultatas padaugintas iš darbo užsakymo svarbos.

**Aptarnavimo lygio** apskaičiavimas: aptarnavimo lygio rezultatas padalytas iš darbo užsakymo aptarnavimo lygio.

Toliau pateiktuose pavyzdžiuose svarbos rezultatas yra „2“, o aptarnavimo lygio rezultatai yra „5“ ir „100“.

**1 pavyzdys:**

| Darbo užsakymo ID | Numatoma pradžios data | Darbo užsakymo svarba | Darbo užsakymo paslaugos lygis | Skaičiavimas               | Rezultatas      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Rytoj            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | „\- 5.75“    |
| WO-00010817   | Dvi dienos nuo dabar   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | „\- 15.75“   |
| WO-00010818   | Dvi dienos nuo dabar   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | „\- 13“      |

Darbo užsakymai bus suplanuoti šia tvarka: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**2 pavyzdys:**

| Darbo užsakymo ID | Numatoma pradžios data | Darbo užsakymo svarba | Darbo užsakymo paslaugos lygis | Skaičiavimas                 | Rezultatas    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Rytoj            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | „\- 1“     |
| WO-00010817   | Dvi dienos nuo dabar   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | „\- 11“    |
| WO-00010818   | Dvi dienos nuo dabar   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Jei aptarnavimo lygio rezultatas padidinamas iki „100“ vietoje „5“, planavimo tvarka bus: WO-000108**18**, WO-000108**16**, WO-000108**17**.

Vertinimo rezultatai, susiję su apskaičiavimu, kurie priežiūros darbuotojai turėtų dirbti vykdant darbo užsakymus, yra nustatyti kaip skaičiai, kurie įtraukiami į kiekvieną priežiūros darbuotojo skaičiavimą planuojant darbo užsakymą. Darbo užsakyme pasirenkamas priežiūros darbuotojas, kurio rezultatas yra didžiausias. Toliau pateiktas trumpas priežiūros darbuotojo rezultatų aprašas.

| Priežiūros darbuotojo rezultatas| Aprašymas |
|---|---|
| Atsakingas darbininkas | Jei priežiūros darbuotojas yra pasirinktas kaip darbo užsakymo atsakingas darbuotojas, rezultatas pridedamas. |
| Atsakinga priežiūros darbuotojų grupė | Jei priežiūros darbuotojas priklauso darbo užsakymo atsakingai priežiūros darbuotojų grupei, rezultatas pridedamas. |
| Pageidaujamas priežiūros darbuotojas         | Jei darbuotojas yra pasirinktas kaip pageidaujamas turto priežiūros darbuotojas, rezultatas pridedamas. |
| Pageidaujama priežiūros darbuotojų grupė   | Jei darbuotojas priklauso pageidaujamai turto priežiūros darbuotojų grupei, rezultatas pridedamas.  |
| Vieta  | Jei jūsų įmonėje naudojamos funkcinės vietos, priežiūros darbuotojai gauna visą rezultatą, jei jie yra su turtu susijusioje funkcinėje vietoje. Jei yra turto funkcinės vietos pirminė vieta, priežiūros darbuotojai toje funkcinėje vietoje gaus 1/2 rezultato. Jei ta vieta taip pat turi pirminę vietą, priežiūros darbuotojai toje funkcinėje vietoje gaus 1/3 rezultato. Jei ta vieta taip pat turi pirminę vietą, priežiūros darbuotojai toje funkcinėje vietoje gaus 1/4 rezultato, ir t. t. Jei jūsų įmonėje naudojama turto vieta (nerekomenduojame to daryti), apskaičiuojant vietos rezultatus naudojama vieta, sritis ir zona. Darbuotojai gauna visą balą, jei jie yra su turtu susietoje vietoje, srityje ir zonoje. Jei darbuotojo vieta atitinka tik vietą ir sritį, priežiūros darbuotojo vertinimo rezultatas yra 2/3 viso rezultato. Jei priežiūros darbuotojo vieta atitinka tik vietą, priežiūros darbuotojo vertinimo rezultatas yra 1/3 viso rezultato. |
| Darbininko darbo pradžios data  | Dėl kiekvienos datos, kai suplanuota pradžios data yra vėlesnė už numatytą pradžios datą, rezultatas atimamas.  |

>[!NOTE]
>Jei rezultatas nustatytas kaip „0“, tas rezultatas neskaičiuojamas. Tai naudinga, jei, pavyzdžiui, planuodami nenorite įtraukti atsakingo darbuotojo.

## <a name="competencies-used-in-work-order-scheduling"></a>Planuojant darbo užsakymus naudojamos kompetencijos

Galima nustatyti priežiūros užduočių tipų (**Išteklių valdymas** > **Sąranka** > **Užduotys** > **Priežiūros užduočių tipai**) ir priežiūros užduočių profesijų (**Turto valdymas** > **Sąranka** > **Užduotys** > **Priežiūros užduoties profesija**) įgūdžių ir liudijimų reikalavimus. 

Priežiūros užduočių tipai ir priežiūros užduočių profesijos pasirenkamos darbo užsakymo užduotyse. Jei buvo pasirinkti priežiūros užduoties tipo ar priežiūros užduoties profesijos įgūdžiai ar liudijimai, o tas priežiūros užduoties tipas ar priežiūros užduoties profesija naudojama darbo užsakymo užduotyje, tame darbo užsakyme suplanuojami dirbti tik priežiūros darbuotojai su atitinkančiais įgūdžiais ir liudijimais.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Darbas su suplanuotais darbo užsakymais naudojant Ganto diagramą

**Suplanuotų darbo užsakymų Ganto diagrama** pateikiama grafinė sąsaja, kur galite peržiūrėti ir perplanuoti savo darbo užsakymus.

Norėdami peržiūrėti Ganto diagramą ir su ja dirbti, atlikite toliau nurodytus veiksmus.

1. Eikite į **Turto valdymas > Darbo užsakymai > Suplanuotų darbo užsakymų Ganto diagrama**.

1. Norėdami nustatyti, kuri funkcinė vieta, trukmė ir laiko skalė turėtų būti rodoma Ganto diagramoje, naudokite dalyje **Parametrai** esančius išplečiamuosius sąrašus ir laukus.

1. Pasirinkite **Taikyti**.

    - Ganto diagrama atnaujinama, kad būtų rodomi jūsų nustatymus atitinkantys suplanuoti darbo užsakymai. Kiekvieną darbo užsakymą vaizduoja mėlynas stačiakampis.
    - Norėdami perplanuoti rodomą darbo užsakymą, pasirinkite ir nuvilkite jį į norimą naują datą ir laiką.

1. Jei atlikote pakeitimus, veiksmų srityje pasirinkite **Įrašyti**, kad juos įrašytumėte.
