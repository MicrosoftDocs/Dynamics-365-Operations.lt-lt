---
title: Neautomatiniu būdu sukurti darbo užsakymai
description: Šioje temoje paaiškinta, kaip kurti darbo užsakymą rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017873"
---
# <a name="manually-created-work-orders"></a>Neautomatiniu būdu sukurti darbo užsakymai

[!include [banner](../../includes/banner.md)]


Galite kurti darbo užsakymus rankiniu būdu dviem būdais:

- Puslapyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai** 
- Puslapyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**, arba **Mano funkcinės vietos priežiūros užklausos** 

## <a name="create-work-order"></a>Kurti darbo užsakymą

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite **Naujas**.

3. Dialogo lange **Kurti darbo užsakymą**, lauke **Darbo užsakymo tipas**, pasirinkite darbo užsakymo tipą.

4. Jei reikia, pasirinkite **aprašymą**.

5. Lauke **Turtas** pasirinkite turtą.

>[!NOTE]
>Pasirinkus turtą, išplečiamajame meniu **Turtas** gali būti galimi trys toliau pateikti skirtukai. 

- **Aktyvus turtas**: šiame skirtuke yra viso turto, kurio turto ciklo būsena „Aktyvi“, sąrašas. 
- **Turto rodinys**: šiame skirtuke rodomas funkcinių vietų ir jose įdiegto turto medžio rodinys.
- **Mano turtas**: šiame skirtuke yra turtas, susijęs su funkcinėmis vietomis, į kurias jūs (darbuotojas, prisijungęs prie sistemos) galite būti priskirtas. (Norėdami gauti informacijos apie nustatymą, žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).) Jei darbuotojui nėra priskirtų funkcinių vietų skiltyje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md), skirtukas **Mano turtas** negalimas. 

6. Lauke **Priežiūros užduoties tipas** pasirinkite darbo užsakymo priežiūros užduoties tipą.

7. Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**.

8. Jei reikia, galite keisti darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.

9. Susijusiuose laukuose pasirinkite **numatomas pradžios** ir **numatomas pabaigos** datas.

10. Spustelėkite **Gerai**, kad sukurtumėte darbo užsakymą.

11. Sąrašo puslapyje **Visi darbo užsakymai** galite pagal poreikį redaguoti darbo užsakymą.

Atkreipkite dėmesį į toliau nurodytus punktus.

- Sąrašo puslapio **Visi darbo užsakymai** išsamios informacijos rodinyje galite pridėti kelis turtus prie darbo užsakymo įterpdami eilutes į „FastTab“ **Darbo užsakymų priežiūros užduotys**. Turtui galite pasirinkti tik tuos priežiūros užduoties tipus, kurie yra nurodyti turto tipe konkrečiam turtui.  

- Jei pakeisite turto aptarnavimo lygį ar turto kritiškumą po to, kai naudojote turtą darbo užsakyme, šio darbo užsakymo aptarnavimo lygis ar kritiškumas nebus atitinkamai atnaujintas. Daugiau informacijos apie aptarnavimo lygius ir kritiškumus žr. [Turto aptarnavimo lygiai](../setup-for-objects/object-priorities.md) ir [Turto svarbos tipai](../setup-for-objects/object-criticalities.md).

- Darbo užsakymo kritiškumas iš naujo apskaičiuojamas kaskart, kai prie darbo užsakymo pridedama arba pašalinama darbo užsakymo užduotis.

- Išsamios informacijos rodinyje **Visi darbo užsakymai** > skirtuke **Antraštė** > „FastTab“ **Grafikas**, laukuose **Atsakinga grupė** arba **Atsakingas**, galite pasirinkti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją. Šiuos parametrus galima keisti, kol darbo užsakymas yra aktyvus. Pavyzdžiui, jas galima pakeisti, kai pasikeičia darbo užsakymo ciklo būsena. Automatinė atranka, vykdoma kuriant darbo užsakymą, yra grindžiama sąranka, esančia puslapyje **Atsakingi priežiūros darbuotojai**. Jei pridėsite arba pašalinsite darbo užsakymo užduotis po to, kai sukūrėte darbo užsakymą, o atnaujinus darbo užsakymą laukai **Atsakinga grupė** ir **Atsakingas** yra tušti, turto valdyme bus ieškomos galimos atitiktys sąrankos formoje, skirtoje nurodyti atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją. Jei atnaujinus darbo užsakymą laukai **Atsakinga grupė** arba **Atsakingas** jau yra nustatyti, pakeitimai nėra vykdomi. Daugiau informacijos apie už priežiūrą atsakingus darbuotojus ir darbuotojų grupes, rasite temoje [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).

- Puslapyje [Priežiūros būsena](../controlling-and-reporting/maintenance-status.md) galite vykdyti skaičiavimus, kuriuos atlikus bus suformuojama darbo krūvio, susijusio su gaunamais ir baigtais darbo užsakymais, apžvalga.  

- Puslapio **Visi darbo užsakymai** išsamios informacijos rodinyje, „FastTab” **Eilutės informacija**, galite naudoti laukus **Platuma** ir **Ilguma**, kad būtų galima pridėti darbo užsakymo užduoties pasirinkto turto geografines koordinates.  


## <a name="create-related-work-order"></a>Kurti susijusį darbo užsakymą

Galite sukurti darbo užsakymą, susijusį su esamu darbo užsakymu. Ši galimybė naudinga jei, pavyzdžiui, norite dirbti su pirminiais ir antriniais darbo užsakymais. Naujas darbo užsakymas yra kuriamas pagal darbo užsakymo užduotį iš esamo darbo užsakymo.

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, kuriam kursite susijusį darbo užsakymą.

3. Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Naujas** pasirinkite **Susijęs darbo užsakymas**.

4. Dialogo lange **Kurti susijusį darbo užsakymą**, lauke **Darbo užsakymo užduotis**, pasirinkite darbo užsakymo užduotį, kuriai norite sukurti susijusį darbo užsakymą.

5. Lauke **Priežiūros užduoties tipas** pasirinkite priežiūros užduoties tipą.

6. Laukuose **Priežiūros užduoties tipo variantas** ir **Prekybos šaka** pasirinkite susijusios priežiūros užduoties tipo variantą ir prekybos šaką.

7. Jei šis darbo užsakymas yra pirmas susijęs darbo užsakymas, sukurtas pasirinktam darbo užsakymui, atlikite toliau pateiktus veiksmus.
    1. Pasirinkite parinktį **Naujas darbo užsakymas**.
    2. Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą.
    3. Lauke **Aprašas** įveskite aprašą.
    4. Pagal poreikį keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.
    5. Laukuose **Numatoma pradžia** ir **Numatoma pabaiga** pasirinkite numatomas pradžios bei pabaigos datas.
    6. Pasirinkite **Gerai**. Naujai sukurtas susijęs darbo užsakymas bus rodomas sąrašo puslapyje **Visi darbo užsakymai**.  

8. Jei darbo užsakymas, kuriam kuriate susijusį darbo užsakymą, jau turi susijusių darbo užsakymų, atlikite toliau pateiktus veiksmus, norėdami įtraukti naują darbo užsakymo užduotį į esamą susijusį darbo užsakymą.
    1. Pasirinkite parinktį **Įtraukti į susijusį darbo užsakymą**.
    2. Lauke **Darbo užsakymas** pažymėkite susijusį darbo užsakymą, kuriam norite pridėti naują darbo užsakymo užduotį.
    3. Pagal poreikį keiskite darbo užsakymo aptarnavimo lygį lauke **Aptarnavimo lygis**.
    4. Laukuose **Numatoma pradžia** ir **Numatoma pabaiga** pagal poreikį pakeiskite numatomas pradžios bei pabaigos datas.
    5. Pasirinkite **Gerai**. Darbo užsakymo užduotis pridedama prie esamo susijusio darbo užsakymo.

Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kurti susijusį darbo užsakymą** pavyzdys.

![1 pav.](media/03-work-orders.png)

>[!NOTE]
>Jei nustatėte susijusio darbo šabloną **Turto valdymo parametrai** > skirtuke **Darbo užsakymai** > lauke **Susijusio darbo užsakymo šablonas**, darbo užsakymo ID bus sukuriami pagal šablono sąranką. Jei nėra nurodytas joks susijusio darbo užsakymo šablonas, kitas pasiekiamas darbo užsakymo ID naudojamas susijusiems darbo užsakymams.

## <a name="copy-a-work-order"></a>Kopijuoti darbo užsakymą

Galite greitai sukurti naują darbo užsakymą iš esamo darbo užsakymo. Toks darbo užsakymų tvarkymas skiriasi nuo darbo užsakymų kūrimo pagal [priežiūros planus](../preventive-and-reactive-maintenance/maintenance-plans.md). Tai naudinga, pavyzdžiui, jei darbo užsakyme yra daug darbo užsakymo užduočių ir skirtingos užduotys turi būti atliktos skirtingam turtui ir reguliariais intervalais.

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, iš kurio norite nukopijuoti turinį.

3. Veiksmų srityje > skirtuke **Darbo užsakymas** > grupėje **Naujas**, pasirinkite **Kopijuoti darbo užsakymą**.

4. Rodoma darbo užsakymo sąranka iš pasirinkto darbo užsakymo. Prireikus galite redaguoti kai kuriuos laukus.

5. Spustelėkite **Gerai**, kad sukurtumėte naują darbo užsakymą.

6. Sąrašo puslapyje **Visi darbo užsakymai** galite pagal poreikį redaguoti darbo užsakymą.

>[!NOTE]
>Kai sukuriamas naujas darbo užsakymas, dalis informacijos yra nukopijuojama tiesiai iš esamo darbo užsakymo. Informacija apie prognozes, įrankius, prižiūrimo turto kontrolinius sąrašus, funkcines vietas, adresus ir planavimą nėra kopijuojama. Vietoje to, ji inicijuojama naudojant dabartinį nustatymą turto valdyme. Todėl, jei ši informacija buvo pakeista nuo tada, kai buvo sukurtas pirmas darbo užsakymas, iki tada, kai buvo sukurta darbo užsakymo kopija, pakeitimai įtraukiami į naują darbo užsakymą. Pavyzdžiai: prognozių pakeitimai ir prižiūrimo turto kontrolinių sąrašų naujinimai.

Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kopijuoti darbo užsakymą** pavyzdys.

![2 pav.](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Sukurkite darbo užsakymą pagal priežiūros užklausą

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros užklausos** > **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos**.

2. Pasirinkite priežiūros užklausą, kuriai norite sukurti darbo užsakymą, ir spustelėkite **Redaguoti**.

3. Veiksmų srityje > skirtuke **Priežiūros užklausa** > grupėje **Naujas**, pasirinkite **Darbo užsakymas**.

4. Dialogo lange **Darbo užsakymas** nustatykite laukus. Jei priežiūros užduoties tipas buvo pasirinktas priežiūros užklausoje, jei pageidaujate, galite pasirinkti kitą priežiūros užduoties tipą, kai kuriate darbo užsakymą.

5. Pasirinkite **Gerai**. Pranešimas informuoja, kad darbo užsakymas sukurtas.

6. Jei norite peržiūrėti su priežiūros užklausa susietus darbo užsakymus, pasirinkite priežiūros užklausą sąrašo puslapiuose **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**. Tada, veiksmų srityje, skirtuke **Priežiūros užklausa**, grupėje **Peržiūrėti**, pasirinkite **Darbo užsakymai**.


Toliau pateiktame paveikslėlyje parodytas dialogo lango **Kurti darbo užsakymą** pavyzdys.

![3 pav.](media/05-work-orders.png)


>[!NOTE]
>Jei norite, kad darbo užsakymai būtų sukurti automatiškai, tai galite padaryti planuojant priežiūros planų užduotis arba nustatant turtui „Kurti automatiškai“ [priežiūros planus](../preventive-and-reactive-maintenance/maintenance-plans.md) arba [priežiūros ciklus](../preventive-and-reactive-maintenance/maintenance-rounds.md). Darbo užsakymų, sukurtų pagal priežiūros užklausas sąrašo puslapyje **Visas priežiūros grafikas**, priežiūros užduoties tipai pasirenkami priežiūros užklausose.

