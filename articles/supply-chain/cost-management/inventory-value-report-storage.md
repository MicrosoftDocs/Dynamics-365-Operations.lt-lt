---
title: Atsargų vertės saugyklos ataskaita
description: Šioje temoje paaiškinama, kaip vykdyti atsargų vertės saugyklos ataskaitą ir nustatyti, kad rezultatas būtų prieinamas skaitmeniniu būdu kaip interaktyvus puslapis „Microsoft Dynamics 365 Supply Chain Management“ arba kaip eksportuojamas dokumentas bet kuriuo iš kelių formatų.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1946ca72aa92b644e15e8a625577bdf4ef1506ff
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577749"
---
# <a name="inventory-value-storage-report"></a>Atsargų vertės saugyklos ataskaita

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip vykdyti **atsargų vertės saugyklos** ataskaitą ir nustatyti, kad rezultatas būtų prieinamas skaitmeniniu būdu kaip interaktyvus puslapis „Microsoft Dynamics 365 Supply Chain Management“ arba kaip eksportuojamas dokumentas bet kuriuo iš kelių formatų.

Kai ataskaitą peržiūrite naršyklėje, stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į jūsų sukonfigūruotą maketą. Galite surikiuoti rezultatus, filtruoti juos, detalizuoti duomenis ir daugiau.

Ataskaitų rezultatai saugomi duomenų objekte **Atsargų vertė**. Todėl rezultatus galite filtruoti ir eksportuoti formatu, pvz., kableliais atskirtų reikšmių (CSV) arba „Microsoft Excel” formatu.

**Atsargų vertės saugyklos** ataskaita naudinga, kai išvestyje yra daug eilučių. Pavyzdžiui, jūs turite 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai. Tokiu atveju, pateikus atsargų pabaigos balansų užklausą pagal prekę, svetainę ir sandėlį, išvestyje bus daug eilučių.

> [!NOTE]
> Ataskaitoje nebus įtrauktos tarpinės sumos, kurios nurodytos ataskaitos makete. Joje taip pat nebus DK balansų, net jei jie nurodyti ataskaitos makete. Derinimas su DK turi būti atliekamas naudojant bandomuosius balansus.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Atsargų vertės saugyklos funkcijos įjungimas

Kad galėtumėte generuoti **atsargų vertės saugyklos** ataskaitą, turite įjungti funkciją jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis** – kaštų valdymas
- **Funkcijos pavadinimas** – Atsargų vertės saugykla

## <a name="generate-an-inventory-value-storage-report"></a>Atsargų vertės saugyklos ataskaitos generavimas

Atlikite šiuos veiksmus, norėdami sugeneruoti ir išsaugoti **atsargų vertės saugyklos** ataskaitą.

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų vertės ataskaitų saugykla**.
1. Pasirinkite **Naujas**.
1. Pasirodžiusiame dialogo lange **Atsargų vertė** nustatykite tolesnes reikšmes, kad nurodytumėte, kurie įrašai įtraukti jūsų ataskaitoje.

    - „FastTab” **Parametrai** įveskite unikalų ataskaitos pavadinimą ir naudokite laukus, esančius skyriuje **Datos intervalas**, kad nurodytumėte, kurie įrašai įtraukti ataskaitoje. Norėdami nustatyti datos intervalą, lauke **Datos intervalo kodas** pasirinkite iš anksto nustatytą intervalą (susijusį su ataskaitos generavimo data) arba laukuose **Nuo datos** ir **Iki datos** įveskite konkrečias datas.
    - „FastTab“ **Įtrauktini įrašai** nustatykite filtrus ir apribojimus, kad apibrėžtumėte, kurie duomenys įtraukti į ataskaitą.
    - „FastTab” **Vykdyti fone** nurodykite, kaip, kada ir kokiu dažnumu ataskaita generuojama.

    > [!NOTE]
    > Ši ataskaita visada vykdoma kaip paketinės užduoties dalis.

1. Norėdami pritaikyti nustatymus ir uždaryti dialogo langą, pasirinkite **Gerai**.

Po to, kai paketinė užduotis baigiama, ataskaita bus įtraukta į puslapį **Atsargų vertės ataskaitų saugykla**. Gali reikėti atnaujinti puslapį, kad pamatytumėte ataskaitą.

## <a name="explore-an-inventory-value-storage-report"></a>Atsargų vertės saugyklos ataskaitos nagrinėjimas

Sukūrę ataskaitą galite ją peržiūrėti ir naršyti bet kuriuo metu atlikdami tolesnius veiksmus.

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų vertės ataskaitų saugykla**.
1. Sąraše pasirinkite ataskaitą.
1. Pasirinkite **Peržiūrėti informaciją**, kad būtų rodomas ataskaitos turinys.
1. Susipažinkite su ataskaita atlikdami bet kurį iš tolesnių veiksmų.

    - Galite pasirinkti beveik bet kurio stulpelio antraštę, kad galėtumėte rūšiuoti arba filtruoti tinklelį pagal stulpelio reikšmes, kaip tai darote su dauguma standartinių „Supply Chain Management“ puslapių.
    - Norėdami filtruoti ataskaitą pagal bet kurią kelių galimų stulpelių reikšmę, naudokite lauką **Filtruoti**.
    - Naudokite rodymo meniu (virš lauko **Filtruoti**), kad įrašytumėte ir įkeltumėte mėgstamiausius rūšiavimo ir filtravimo parinkčių derinius.

## <a name="export-an-inventory-value-storage-report"></a>Atsargų vertės saugyklos ataskaitos eksportavimas

Kiekviena sugeneruota ataskaita saugoma duomenų objekte **Atsargų vertė**. Norėdami eksportuoti duomenis iš šio objekto bet kokiu palaikomu duomenų formatu, pvz., CSV arba „Excel“ formatu, galite naudoti standartines „Supply Chain Management“ duomenų tvarkymo funkcijas.

Toliau pateiktame pavyzdyje parodyta, kaip eksportuoti ataskaitą **Atsargų vertės ataskaita**.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Duomenų valdymas**.
1. Skyriuje **Importavimas / eksportavimas** pasirinkite plytelę **Eksportavimas**. 
1. Pasirodžiusiame puslapyje **Eksportavimas** nustatysite eksportavimo užduotį. Pirmiausia įveskite užduoties grupės pavadinimą.
1. Skyriuje **Pasirinkti objektai** pasirinkite **Įtraukti objektą**.
1. Pasirodžiusiame dialogo lange nustatykite tolesnius laukus.

    - **Objekto pavadinimas** – pasirinkite **Atsargų vertė**.
    - **Paskirties duomenų formatas** – pasirinkite formatą, kuriuo bus eksportuojami duomenys.

1. Norėdami pridėti naują eilutę pasirinkite **Įtraukti**, tada pasirinkite **Uždaryti**, kad uždarytumėte dialogo langą.
1. Paprastai vienu metu eksportuojate vieną ataskaitą. Norėdami eksportuoti vieną ataskaitą, nustatykite eilutės, kurią ką tik įtraukėte į dialogo langą **Užklausa**, filtrą. Tokiu būdu galite nurodyti, kuri objekto **Atsargų vertė** ataskaita yra įtraukiama į eksportavimą. Atlikite tolesnius veiksmus, norėdami nustatyti šias filtro pasirinktis vienai ataskaitai eksportuoti.

    1. Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte eilutę.
    2. Nustatykite lauką **Lentelė** į **Atsargų vertė**.
    3. Nustatykite lauką **Išvestinė lentelė** į **Atsargų vertė**.
    4. Nustatykite lauko **Laukas** reikšmę kaip lauką, pagal kurį norite filtruoti. Paprastai naudosite lauką **Vykdymo pavadinimas** ir / arba lauką **Vykdymo laikas**.
    5. Lauką **Kriterijai** nustatykite į reikšmę, kurios norite ieškoti pasirinktame lauke. (Jei ankstesniame veiksme pasirinkote lauką **Vykdymo pavadinimas**, ši reikšmė bus ataskaitos pavadinimas. Jei pasirinkote lauką **Vykdymo laikas**, reikšmė bus laikas, kada buvo sugeneruota ataskaita.)
    6. Jei reikia, įtraukite daugiau eilučių į lentelę **Diapazonas**, kol gausite tiksliai tokią unikalią ataskaitą, kokios reikėjo.

1. Norėdami įrašyti parametrus ir uždaryti dialogo langą, pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, kad įrašytumėte eksporto sąranką.
1. Skirtuke **Eksportavimo parinktys** pasirinkite **Eksportuoti dabar**, kad būtų sugeneruotas eksportavimo failas.
1. Pasirodžiusiame puslapyje **Vykdymo suvestinė**, galite peržiūrėti eksportavimo užduoties būseną ir eksportuotų objektų sąrašą. Skyriaus **Objekto apdorojimo būsena** sąraše pasirinkite objektą **Atsargų vertė**, tada pasirinkite **Atsisiųsti failą**, kad atsisiųstumėte iš to objekto eksportuotus duomenis.

Norėdami gauti daugiau informacijos apie tai, kaip naudoti duomenų valdymo funkciją duomenims eksportuoti, žr. [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]