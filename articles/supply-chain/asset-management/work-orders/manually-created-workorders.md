---
title: Neautomatiniu būdu sukurti darbo užsakymai
description: Šioje temoje paaiškinta, kaip kurti darbo užsakymą rankiniu būdu skiltyje Turto valdymas.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875797"
---
# <a name="manually-created-work-orders"></a>Neautomatiniu būdu sukurti darbo užsakymai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Galite kurti darbo užsakymus rankiniu būdu dviem būdais:

- Skiltyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**  
- Skiltyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**, arba **Mano funkcinės vietos priežiūros užklausos**  

## <a name="create-work-order"></a>Kurti darbo užsakymą

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Spustelėkite mygtuką **Naujas**.

3. Išplečiamajame meniu **Sukurti darbo užsakymą** pasirinkite darbo užsakymo tipą.

4. Jei reikia, pasirinkite aprašą.

5. Pasirinkite darbo užsakymo turtą bei priežiūros užduoties tipą.

>[!NOTE]
>Pasirinkus turtą galimi trys skirtukai: skirtuke **Mano turtas** nurodomas turtas, susijęs su funkcine vieta, į kurią jūs (prisijungęs į sistemą darbuotojas) galite būti paskirtas (sąranka aprašoma [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md)). Jei darbuotojui nėra nurodyta funkcinė vieta skiltyje [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md), skirtukas **Mano turtas** nebus rodomas. Skirtuke **Aktyvus turtas** yra viso turto, kurio turto ciklo būsena „Aktyvi“, sąrašas. Skirtuke **Turto rodinys** rodomas funkcinių vietų ir tose vietose įdiegto turto medžio rodinys.

6. Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.

7. Jei reikia, galite keisti darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.

8. Susijusiuose laukuose pasirinkite numatomas pradžios ir pabaigos datas.

9. Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.

10. Redaguokite, jei reikia, darbo užsakymą, pasirinkę **Visi darbo užsakymai**.

- Pasirinkę **Visi darbo užsakymai** galite pridėti prie darbo užsakymo kelis turtus Išsamios informacijos rodinyje įterpdami eilutes į „FastTab“ **Darbo užsakymų priežiūros užduotys**. Turtui galite pasirinkti tik tuos priežiūros užduoties tipus, kurie yra nurodyti turto tipe konkrečiam turtui.  
- Jei pakeitėte turto aptarnavimo lygį arba turto kritiškumą, po to, kai panaudojote jį darbo užsakyme (žr. [Turto aptarnavimo lygiai](../setup-for-objects/object-priorities.md) ir [Turto kritiškumas](../setup-for-objects/object-criticalities.md)), darbo užsakymo aptarnavimo lygis arba kritiškumas atitinkamai nėra naujinami.
- Darbo užsakymo kritiškumas yra perskaičiuojamas kiekvienąkart, kai darbo užsakymo eilutė yra įterpiama arba pašalinama tame darbo užsakyme.
- Išsamios informacijos rodinyje **Visi darbo užsakymai** > rodinyje **Antraštė** > „FastTab“ **Grafikas** galite pasirinkti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją laukuose **Atsakinga grupė** arba **Atsakingas**. Šie parametrai gali būti keičiami tol, kol darbo užsakymas yra aktyvus, pavyzdžiui, kai darbo užsakymo ciklo būsena pakinta. Automatinė atranka, vykdoma kuriant darbo užsakymą, yra grindžiama sąranka, esančia **Atsakingi priežiūros darbuotojai**. Jei pridėsite arba pašalinsite darbo užsakymo užduotis po to, kai sukūrėte darbo užsakymą, o atnaujinus darbo užsakymą laukai **Atsakinga grupė** ir **Atsakingas**, Turto valdyme bus ieškomos galimos atitiktys sąrankos formoje, skirtoje nurodyti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją. Jei atnaujinus darbo užsakymą laukas **Atsakinga grupė** arba laukas **Atsakingas** jau yra užpildyti, pakeitimai nėra vykdomi. 

- Skiltyje **Priežiūros būsena** galite vykdyti skaičiavimus, kuriuos atlikus bus suformuojama darbo krūvio, susijusio su gaunamais ir baigtais darbo užsakymais, apžvalga.  

- „FastTab“ **Eilutės išsami informacija** naudokite laukus **Platuma** ir **Ilguma** įterpti geografines koordinates turtui, pasirinktam darbo užsakymo užduočiai.  

## <a name="create-related-work-order"></a>Kurti susijusį darbo užsakymą

Galite sukurti susijusį darbo užsakymą esamam darbo užsakymui, pavyzdžiui, jei norite dirbti su pagrindiniais ir antriniais darbo užsakymais. Naujas darbo užsakymas yra kuriamas pagal darbo užsakymo užduotį iš esamo darbo užsakymo.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pažymėkite darbo užsakymą, kuriam norite sukurti susijusį darbo užsakymą.

3. Spustelėkite **Susijęs darbo užsakymas**.

4. Išplečiamajame dialogo lange **Sukurti susijusį darbo užsakymą** pasirinkite darbo užsakymo užduotį, kuriai norite sukurti susijusį darbo užsakymą lauke **Darbo užsakymo užduotis**.

5. Pasirinkite priežiūros užduoties tipą lauke **Priežiūros užduoties tipas** ir, jei reikia, susijusį priežiūros užduoties tipo variantą ir prekybos šaką laukuose **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.

6. Jei tai pirmas susijęs darbo užsakymas, kurį kursite, spustelėkite išrinkimo mygtuką **Naujas darbo užsakymas**.

7. Susijusiuose laukuose pasirinkite **Darbo užsakymo tipas** ir **Aprašas**.

8. Prireikus keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.

9. Įterpkite numatomas pradžios ir pabaigos datas susijusiuose laukuose.

10. Spustelėkite **Gerai**. Naujai sukurtas susijęs darbo užsakymas bus rodomas sąraše **Visi darbo užsakymai**.

11. Jei kursite susijusį darbo užsakymą darbo užsakymui, kuris jau turi susijusių darbo užsakymų, galėsite įterpti darbo užsakymo užduotį jau esančiam susijusiam darbo užsakymui. Tai galite atlikti spustelėjus išrinkimo mygtuką **Pridėti prie darbo užsakymo** 6 etape. Tada pažymėkite susijusį darbo užsakymą, kuriam norite pridėti naują darbo užsakymo užduotį. Redaguokite kiek reikia laukus **Aptarnavimo lygis**, **Numatoma pradžia** ir **Numatoma pabaiga**, ir spustelėkite **Gerai**. Darbo užsakymo užduotis pridedama prie esamo susijusio darbo užsakymo.


![1 pav.](media/03-work-orders.png)

**Pastaba.** Jei nustatėte susijusio darbo šabloną **Turto valdymo parametrai** > **Darbo užsakymai** nuorodoje > **Susijusio darbo užsakymo šablonas** lauke, darbo užsakymo ID bus sukuriami pagal šablono sąranką. Jei nėra nurodytas joks susijusio darbo užsakymo šablonas, kitas pasiekiamas darbo užsakymo ID bus naudojamas susijusiems darbo užsakymams.

## <a name="copy-work-order"></a>Kopijuoti darbo užsakymą

Galima greitai sukurti naują darbo užsakymą iš esamo darbo užsakymo. Toks darbo užsakymų tvarkymas skiriasi nuo darbo užsakymų kūrimo pagal priežiūros planus. Tai naudinga, pavyzdžiui, jei turite darbo užsakymą, kuriame yra daug darbo užsakymo užduočių su skirtingomis užduotimis, skirtomis skirtingam turtui, ir jos turi būti atliktos reguliariais intervalais.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, iš kurio norite nukopijuoti turinį.

3. Spustelėkite **Kopijuoti darbo užsakymą**. Rodoma darbo užsakymo sąranka iš pasirinkto darbo užsakymo. Prireikus galite redaguoti kai kuriuos laukus.

4. Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.

5. Redaguokite, jei reikia, darbo užsakymą, pasirinkę **Visi darbo užsakymai**.

>[!NOTE]
>Kai sukuriamas naujas darbo užsakymas, dalis informacijos yra nukopijuojama tiesiai iš esamo darbo užsakymo. Tokia informacija kaip prognozės, įrankiai, priežiūros kontroliniai sąrašai, funkcinė vieta, adresai ir planavimas nėra kopijuojama, bet pradedama kurti iš esamos sąrankos Turto valdyme. Tai reiškia, jog, jei buvo įvykdyti pakeitimai tuose duomenyse sukūrus pirmą darbo užsakymą ir, iki kol padarėte darbo užsakymo kopiją, tie pakeitimai išliks naujai sukurtame darbo užsakyme. Pavyzdžiai – prognozių arba atnaujintų prižiūrimo turto kontrolinių sąrašų pakeitimai.


![2 paveikslėlis](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Sukurkite darbo užsakymą pagal priežiūros užklausą

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros užklausos** > **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**.

2. Pasirinkite priežiūros užklausą, kuriai norite sukurti darbo užsakymą, ir spustelėkite **Redaguoti**.

3. Skiltyje **Visos užklausos** spustelėkite **Darbo užsakymas**.

4. Užpildykite išplečiamąjį sąrašą **Darbo užsakymas**. Jei priežiūros užduoties tipas buvo pasirinktas priežiūros užklausoje, jei pageidaujate, galite pasirinkti kitą priežiūros užduoties tipą, kai kuriate darbo užsakymą.

5. Spustelėkite **Gerai**. Bus rodomas pranešimas, kuriame informuojama apie sukurtą darbo užsakymą.

6. Jei norite matyti, kurie darbo užsakymai yra susieti su priežiūros užklausa, pasirinkite priežiūros užklausą iš sąrašų **Visos priežiūros užklausos** arba**Aktyvios priežiūros užklausos** ir spustelėkite mygtuką **Darbo užsakymai**.


![3 paveikslėlis](media/05-work-orders.png)


>[!NOTE]
>Darbo užsakymai gali būti sukurti automatiškai, planuojant priežiūros planų užduotis arba nustatant turtui „Kurti automatiškai“ priežiūros planus arba priežiūros ciklus. Darbo užsakymai, sukurti pagal priežiūros užklausas ir nurodomi skiltyje**Priežiūros grafikas**, kuriami nurodant priežiūros užduoties tipus, pasirinktus priežiūros užklausose.

