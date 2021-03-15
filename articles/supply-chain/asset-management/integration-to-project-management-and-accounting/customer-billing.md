---
title: Kliento turto priežiūros sąskaitos pateikimas
description: Šioje temoje paaiškinama, kaip kurti, apdoroti ir išrašyti priežiūros darbo, atliekamam su jūsų klientų turtu, sąskaitą.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131846"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Kliento turto priežiūros sąskaitos pateikimas

[!include [banner](../../includes/banner.md)]

Funkcija *Darbo užsakymo sąskaitos pateikimas* leidžia kurti, apdoroti ir pateikti priežiūros darbo, atliekamam su jūsų klientų turtu, sąskaitą. Ši funkcija jums leidžia atlikti tolesnes užduotis:

- Susieti klientus su jų turimu turtu.
- Pasirinkti klientą ir peržiūrėti jam priklausantį turtą, kai kuriate darbo užsakymą.
- Nustatyti pirminį projektą kiekvienam klientui.
- Registruoti valandas, prekes, išlaidas ir mokesčius pagal darbo užsakymą ir tada vėliau sukurti sąskaitos faktūros pasiūlymą klientui.

Papildomai funkcija suteikia šias funkcijas:

- Projekto sutartis automatiškai kopijuojama iš kliento pirminio projekto į atitinkamą darbo užsakymo projektą.
- Turto valdymas dabar gali naudoti projekto operacijos tipą *mokestis* tiek darbo užsakymo prognozėse, tiek darbo užsakymų žurnaluose.

## <a name="turn-on-the-customer-billing-feature"></a>Funkcijos Kliento sąskaitos pateikimas įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Projektų valdymas ir apskaita*
- **Funkcijos pavadinimas:** *Darbo užsakymo sąskaitos pateikimas*

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Norėdami sužinoti, kaip veikia ši funkcija, dirbkite naudodami šį pavyzdinį scenarijų.

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Prieš pradėdami turite pasirinkti **„USMF”** juridinį subjektą.

Taip pat galite naudoti šią scenarijų kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje. Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>1 žingsnis: Sukurkite naują projekto sutartį klientui

1. Eikite į **Projektų valdymas ir apskaita \> Projektai \> Projekto sutartys**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Nauja projekto sutartis** nustatykite šias reikšmes:

    - **Pavadinimas:** *„Pelican” didmeninė prekyba*
    - **Lėšų skyrimo tipas:** *Klientas*
    - **Lėšų skyrimo šaltinis:** *„US-013”* (*„Pelican” didmeninė prekyba)*

1. Pasirinkite **Gerai**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>2 žingsnis: Sukurkite pirminį projektą klientui

Čia sukurtas pirminis projektas bus naudojamas kuriant darbo užsakymus klientui.

1. Eikite į **Projektų valdymas ir apskaita \> Projektai \> Visi projektai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Naujas projektas** nustatykite šias reikšmes:

    - **Projekto tipas:** *Laikas ir medžiaga*
    - **Projekto pavadinimas:** *„Pelican” didmeninės prekybos darbo užsakymai*
    - **Projekto grupė:** *„TM”*
    - **Projekto sutarties ID:** *„Pelican” didmeninė prekyba* (anksčiau sukurta sutartis)
    - **Pradžios data:** Pasirinkite šiandienos datą.

1. Pasirinkite **Kurti projektą**.
1. Atidaromas naujas projektas. Pasižymėkite **Projekto ID** reikšmę. Turėsite ją įvesti vėliau.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>3 žingsnis: Naujo darbo užsakymo tipo kūrimas turto valdyme

1. Eikite į **Turto valdymas \> Sąranka \> Darbo užsakymas \> Darbo užsakymų tipai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujas įrašas įtraukiamas į sąrašą. Nustatykite tokias šio įrašo reikšmes:

    - **Darbo užsakymo tipas:** *Paslauga*
    - **Pavadinimas:** *Paslaugos darbo užsakymai*
    - **Darbo užsakymo ciklo būsena:** *Standartinė*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>4 žingsnis: Susiekite kliento paskyrą su pirminiu projektu

Dabar turite susieti kliento paskyrą su pirminiu projektu Turto valdymo projektų sąrankoje.

1. Eikite į **Turto valdymas \> Sąranka \> Darbo užsakymai \> Projekto sąranka**.
1. Skirtuke **Pirminis projektas** pasirinkite **Pridėti** naujai eilutei pridėti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Kliento paskyra:** *„US-013”* (*„Pelican” didmeninė prekyba*)
    - **Projekto ID:** Įveskite anksčiau pasižymėtą projekto ID.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>5 žingsnis: Susiekite projektų grupę ir tipą su darbo užsakymo projektu

Jūs turite likti **Projekto sąrankos** puslapyje (**Turto valdymas \> Sąranka \> Darbo užsakymai \> Projekto sąranka**).

1. Skirtuke **Projekto grupė** pasirinkite **Pridėti** naujai eilutei pridėti.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Darbo užsakymo tipas:** *Paslauga* (anksčiau sukurtas darbo užsakymo tipas)
    - **Projekto grupė:** *„TM”*

> [!NOTE]
> Projekto sutartis darbo užsakymo projekte yra visada perimama iš pirminio projekto.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>6 žingsnis: Susiekite turtą su kliento ID

1. Eikite į **Turto valdymas \> Turtas \> Aktyvus turtas**.
1. Lauke **Filtruoti** įveskite *„VE-102”* ir pasirinkite filtruoti pagal **Turtą**.
1. Pasirinkite turtą jo parametrams atidaryti.
1. „FastTab” skirtuke **Klientas** nustatykite lauką **Kliento paskyra** į *„US-013”* (*„Pelican”didmeninė prekyba*).

    Laukas **Pavadinimas** automatiškai atnaujinamas į *„Pelican” didmeninė prekyba*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>7 žingsnis: Sukurkite naują turto darbo užsakymą

1. Eikite į **Turto valdymas \> Darbo užsakymai \> Aktyvūs darbo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti darbo užsakymą** nustatykite šias vertes:

    - **Darbo užsakymo tipas:** *Paslauga*
    - **Aprašas:** *Remonto sunkvežimis*
    - **Kliento paskyra:** *„US-013”* (*„Pelican” didmeninė prekyba*)
    - **Turtas:** *„VE-102”*

        > [!NOTE]
        > Peržvalgoje rodomas tik su pasirinkta kliento paskyra susietas turtas.

    - **Priežiūros užduoties tipas:** *Remontas*
    - **Prekyba:** *Mechanika*
    - **Paslaugos lygis:** *4'*

1. Pasirinkite **Gerai**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>8 žingsnis: Peržiūrėkite darbo užsakymą ir pradėkite su juo dirbti

Šiame skyriuje dirbsite su ankstesniame skyriuje sukurtu darbo užsakymu.

1. Norėdami patikrinti, ar pirminis projektas yra *„Pelican” didmeninės prekybos darbo užsakymo* projektas, atlikite šiuos veiksmus:

    1. Skyriuje **Darbo užsakymo priežiūros užduotys** pasirinkite eilutę.
    1. „FastTab” skirtuke **Eilutės informacija** patikrinkite **Projekto ID** reikšmę. Ji turėtų būti brūkšninis skaičius forma *\<Parent-Project-ID\>-\<Project-ID\>*. Ši reikšmė yra saitas.
    1. Pasirinkite projekto ID saitą atidaryti puslapiui, kuriame galite peržiūrėti pirminio projekto ir projekto pavadinimus.

1. Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Ciklo būsena** pasirinkite **Atnaujinti darbo užsakymo būseną**.
1. Dialogo lango **Atnaujinti darbo užsakymo būseną** stulpelyje **Pasirinkti** pasirinkite žymės langelį eilutei, kurioje laukas **Ciklo būsena** yra nustatytas į *Vykdoma*.
1. Pasirinkite **Gerai**.
1. Dialogo lange **Ciklo būsena: Vykdoma** pasirinkite **Gerai**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>9 žingsnis: Registruoti darbo užsakymo kūrimo valandas ir sukurti naują sąskaitos faktūros pasiūlymą

Šiame skyriuje ir toliau dirbsite su tuo darbo užsakymu, su kuriuo dirbote ankstesniame skyriuje.

1. Veiksmų srities skirtuko **Darbo užsakymas** grupėje **Projektas** pasirinkite **Žurnalai**.

    Rodomas **Darbo užsakymų žurnalai** puslapis. Čia galite registruoti laiką, kurį paskyrėte darbo užsakymui.

1. „FastTab“ **Valandos** pasirinkite **Įtraukti eilutę**.
1. Naujoje eilutėje nustatykite lauką **Valandos** į *4'*.
1. Veiksmų srityje pasirinkite **Registruoti žurnalus**.
1. Uždarykite puslapį **Darbo užsakymų žurnalai** tam, kad sugrįžtumėte prie darbo užsakymo.
1. Veiksmų srities skirtuke **Sąskaitų faktūrų išrašymas** pasirinkite **Naujas sąskaitos faktūros pasiūlymas**.
1. Dialogo lango **Kurti sąskaitos faktūros pasiūlymą** skyriuje **Projekto operacijos** pasirinkite žymės langelį **Pasirinkti** kiekvienai eilutei, kuriai norite sukurti sąskaitą faktūrą.
1. Pasirinkite **Gerai** tam, kad uždarytumėte dialogo langą ir peržiūrėtumėte naują sąskaitos faktūros pasiūlymą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]