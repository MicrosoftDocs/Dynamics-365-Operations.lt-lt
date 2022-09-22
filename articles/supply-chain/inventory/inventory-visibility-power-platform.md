---
title: Atsargų matomumo programa
description: Šiame straipsnyje aprašoma, kaip naudoti programą Atsargų matomumas.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520870"
---
# <a name="use-the-inventory-visibility-app"></a>Naudokite programą „Inventory Visibility“

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti programą Atsargų matomumas.

Atsargų matomumas suteikia modeliu pagrįstą programą vizualizacijai. Programą sudaro trys puslapiai: **Konfigūracija**, **Veiklos matomumas** ir **Atsargų suvestinė**. Jam būdingos šios funkcijos:

- Ji suteikia turimos konfigūracijos ir švelniai rezervavimo konfigūracijos vartotojo sąsają (UI).
- Jis palaiko realiuoju laiku turimų atsargų užklausas įvairiuose dimensijų deriniaie.
- Joje pateikiama vartotojo sąsajos, skirtos UI užklausoms registruoti.
- Jame pateikiamas turimų produktų atsargų ir visų dimensijų rodinys.
- Jame pateikiamas turimų produktų atsargų sąrašo rodinys ir iš anksto nustatytos dimensijos.


## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta [įdiegti ir nustatyti atsargų matomumą](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Atverti atsargų matomumo programą

Norėdami atidaryti atsargų matomumo programą, prisijunkite prie savo „Power Apps“ aplinkos ir atidarykite **Atsargų matomumą**.

## <a name="configuration"></a><a name="configuration"></a>Konfigūravimas

Atsargų matomumo programa **Konfigūracijos** puslapis padeda nustatyti turimos konfigūracijos ir soft reservation konfigūraciją. Įdiegus papildinį, numatytoji konfigūracija įtraukia „Microsoft Dynamics 365 Supply Chain Management“ (duomenų `fno` šaltinio vertę). Galite peržiūrėti numatytuosius nustatymus. Tada, atsižvelgdami į savo verslo poreikius ir išorinės sistemos atsargų registravimo reikalavimus, galite modifikuoti konfigūraciją, kad būtų galima standartizuoti būdą, kuriuo atsargų pakeitimai gali būti registruojami, tvarkomi keliose sistemose ir jų bus užklausta.

Išsami informacija apie sprendimo konfigūravimą pateikta [Atsargų matomumo konfigūravimas](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Veikimo matomumas

Veiklos **matomumo puslapis** pateikia realiuoju laiku turimų atsargų užklausos rezultatus, paremtus įvairiomis dimensijų kombinacijomis. Kai *OnHandReservation* funkcija įjungta, taip pat galite registruoti rezervavimo užklausas iš **veiklos matomumo** puslapio.

### <a name="on-hand-query"></a>Turimos užklausos

Skirtuke **Turimų atsargų** užklausa rodomi turimų atsargų realiuoju laiku užklausos rezultatai.

Kai atidarote **puslapio** **Veiklos** matomumas skirtuką Turimų atsargų užklausa, sistema reikalauja jūsų kredencialų, kad ji galėtų gauti paženklą, kuris būtinas norint pateikti užklausą apie atsargų matomumo tarnybą. Galite tiesiog įklijuoti ypatybės atpažinimo ženklą į lauką **BearerToken** ir uždaryti dialogo langą. Tada galite registruoti turimos informacijos užklausą.

Jei pateikėjas atpažinimo ženklas netinkamas arba jei jis baigė galioti, lauke **BearerToken** turite įklijuoti naują ženklą. Įveskite teisingą **kliento ID**, **nuomininko ID**, **Kliento rakto** naujinimo reikšmes ir pasirinkite **Atnaujinti**. Sistema automatiškai gaus naują, galiojantį paerio atpažinimo ženklą.

Norėdami užregistruoti turimos informacijos užklausą, įveskite užklausą užklausos tekstą. Naudokite šabloną, kuris aprašytas [Užklausoje, naudodami skelbimo metodą](inventory-visibility-api.md#query-with-post-method).

![Turimos užklausos nustatymai](media/inventory-visibility-query-settings.png "Turimos užklausos nustatymai")

### <a name="reservation-posting"></a>Rezervavimo publikavimas

Norėdami užregistruoti **rezervavimo užklausą**, naudokite puslapio **Veiklos** matomumas rezervavimo registravimas skirtuką. Kad būtų galima užregistruoti rezervavimo užklausą, reikia įjungti funkciją *OnHandReservation*. Daugiau informacijos apie šią funkciją ir jos įjungus ieškokite atsargų [matomumo rezervavimuose](inventory-visibility-reservations.md).

Norėdami registruoti rezervavimo užklausą, turite įvesti vertę užklausos tekstą. Naudokite trafaretą, kuris aprašytas [kurti vieną rezervavimo įvykį](inventory-visibility-api.md#create-one-reservation-event). Tada rinkitės **Publikuoti**. Norėdami peržiūrėti užklausos atsakymo informaciją, pasirinkite **Rodyti išsamią informaciją**. Taip pat galite gauti  `reservationId` vertę iš atsakymo informacijos.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Atsargų suvestinė

Atsargų **suvestinės puslapis** pateikia produktų atsargų suvestinę kartu su visomis dimensijomis. Tai pasirinktinis objekto Atsargų *atsargų suma* rodinys. Atsargų suvestinės duomenys periodiškai sinchronizuojami pagal atsargų matomumą.

Norėdami įgalinti atsargų **suvestinės puslapį ir** nustatyti sinchronizavimo dažnumą, atlikite šiuos veiksmus:

1. Atidarykite **Konfigūravimo** puslapį.
1. Atidarykite **skirtuką Priemonių valdymas >** Parametrai.
1. Nustatykite OnHandMostSpecificBackgroundService **funkcijos** perjungimo raktą kaip *Taip*.
1. Įgalinus funkciją, tarnybos **konfigūravimo** **dalis tampa galima, o jos metu konfigūruojama OnHandMostSpecificBackgroundService** funkcija. Šis parametras leidžia pasirinkti dažnumą, kuriuo sinchronizuojami atsargų suvestinės duomenys. Naudokite stulpelio **Vertė** **mygtukus** **Aukštyn ir Žemyn,** norėdami pakeisti laiką tarp sinchronizavimų (kuris gali būti ne mažas kaip 5 minutės). Tada pasirinkite **Įrašyti**.

    ![OnHandMostSpecificBackgroundService parametras](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService parametras")

1. Pasirinkite **Naujinti konfigūraciją,** kad įrašytumėte visus pakeitimus.


> [!NOTE]
> Funkcija *OnHandMostSpecificBackgroundService* seka tik turimų atsargų keitimus, atliktus po to, kai buvo įjungta funkcija. Produktų, kurie nebuvo pakeisti nuo tada, kai įjungta funkcija, duomenys nebus sinchronizuoti iš atsargų tarnybos talpyklos į aplinką Dataverse. Jei jūsų **atsargų** suvestinės puslapis nerodo visos turimos informacijos, kurią tikitės, atidarykite Tiekimo grandinės valdymą, **eikite į Atsargų valdymo > Periodinės užduotys > Atsargų** matomumo integravimas, išjunkite paketinę užduotį ir vėl ją įjunkite. Taip bus inicijuotas stūmiimas *ir visi duomenys bus sinchronizuoti su objektu Atsargų atsargų atsargų suma* per kitas 15 minučių. Jei norite naudoti *Funkciją OnHandMostSpecificBackgroundService*, **rekomenduojame** ją įjungti prieš kuriant bet kokius turimų atsargų pokyčius ir įgalinant atsargų matomumo integravimo paketinę užduotį.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a> Iš anksto įkelti supaprastintą turimos informacijos užklausą

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Tiekimo grandinės valdymas saugo daug informacijos apie dabartines turimas atsargas ir tampa pasiekiamas įvairiais tikslais. Tačiau daugeliui kasdienių operacijų ir trečiųjų šalių integravimui reikia tik mažo šios informacijos subrinkinio, o visos sistemos užklausa gali vesti didelius duomenų rinkinius, kurių prireiks norint surinkti ir perkelti. Todėl atsargų matomumo tarnyba gali periodiškai surasti ir saugoti supaprastintą turimų atsargų duomenų rinkinį, kad optimizuota informacija būtų nuolat pasiekiama. Saugoma turimų atsargų informacija filtruojama pagal konfigūruojamus verslo kriterijus, siekiant užtikrinti, kad būtų įtraukta tik tinkamiausia informacija. Kadangi filtruoti turimų atsargų sąrašai saugomi vietoje atsargų matomumo paslaugoje ir yra reguliariai atnaujinami, jie palaiko greitą prieigą, duomenų eksportą pagal poreikį ir supaprastintą integravimą su išorinėmis sistemomis.

> [!NOTE]
> Dabartinė šios funkcijos peržiūros versija gali pateikti tik iš anksto įkeltus rezultatus, kuriuose yra svetainė ir vieta. Galutinė šios priemonės versija leis pasirinkti kitas dimensijas, kurios bus įkeltos iš anksto kartu su rezultatais.

Iš **anksto įkelkite atsargų matomumo suvestinės** puslapį, kad būtų galima peržiūrėti turimos indekso *užklausos iš anksto įkelti rezultatų objektą*. Skirtingai nei *atsargų suvestinės objektas*, *turimų* atsargų indekso užklausos išankstinio įkėliaus rezultatų objektas pateikia produktų su pasirinktomis dimensijomis turimų atsargų sąrašą. Atsargų matomumas sinchronizuoja iš anksto įkeltus suvestinės duomenis kas 15 minučių.

Norėdami peržiūrėti duomenis skirtuke Iš anksto įkelti atsargų matomumo suvestinę, **turite įjungti konfigūravimo puslapio funkcijų valdymo skirtuko funkciją OnHandIndexQueryPreloadBackgroundService** *·* **·** **ir** pasirinkti Naujinti konfigūraciją (**taip** pat žr. atsargų matomumą).[...](inventory-visibility-configuration.md)

> [!NOTE]
> *Kaip ir naudojant funkciją OnhandMostSpecificBackgroudService*, Funkcija OnHandIndexQueryPreloadBackgroundService *seka tik turimų atsargų keitimus,* kurie įvyko įjungtas dėl funkcijos. Produktų, kurie nebuvo pakeisti nuo tada, kai įjungta funkcija, duomenys nebus sinchronizuoti iš atsargų tarnybos talpyklos į aplinką Dataverse. Jei jūsų **atsargų** suvestinės puslapis nerodo visos turimos informacijos, kurios tikitės, **eikite į Atsargų valdymo > Periodinės užduotys > Atsargų matomumo integravimas**, uždrauskite paketinę užduotį ir vėl ją įjunkite. Taip bus inicijuotas stūmimas *, o visi duomenys bus sinchronizuoti su turimo indekso užklausos išankstinio* įkėliaus rezultatų objektu per kitas 15 minučių. Jei norite naudoti šią priemonę, **rekomenduojame ją įjungti prieš kuriant turimų atsargų pakeitimus ir įgalinti atsargų matomumo integravimo paketinę** užduotį.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Filtruoti ir naršyti atsargų suvestines

Naudodami **išplėstinį filtrą**, kuris suteikia „Dataverse“, galite sukurti asmeninį rodinį, kuriame būtų rodomos jums svarbios eilutės. Išplėstinės filtro pasirinktys leidžia jums sukurti platų rodinių diapazoną – nuo paprasto iki kompleksinio. Jos taip pat leidžia į filtrus įtraukti sugrupuotas ir įdėtąsias sąlygas. Norėdami sužinoti daugiau apie tai, kaip naudoti išplėstinį filtrą, žr. Redaguoti arba [kurti asmeninius rodinius naudojant išplėstinius tinklelių filtrus](/powerapps/user/grid-filters-advanced).

Atsargų **suvestinės puslapyje yra** trys laukai virš tinklelio (**Numatytoji** dimensija, **·** **Pasirinktinė** dimensija ir Matas), kuriuos galite naudoti, norėdami valdyti, kurie stulpeliai yra matomi. Taip pat galite pasirinkti bet kurią stulpelio antraštę, pagal kurią norite filtruoti arba rūšiuoti dabartinius rezultatus pagal tą stulpelį. Toliau pateiktoje ekrano nuotrauka aprašo dimensijas, filtravimą, rezultatų skaičių ir įkėlimą **daugiau, esančius atsargų suvestinės** puslapyje.

![Atsargų suvestinės puslapis.](media/inventory-visibility-onhand-list.png "Atsargų suvestinės puslapis")

Kadangi jūs turėsite iš anksto nustatytas dimensijas, kurios naudojamos suvestinės duomenims įkelti iš anksto, **atsargų** matomumo suvestinės puslapyje bus rodomi su dimensija susiję stulpeliai. *Dimensijas sistema gali tinkinti tik pagal&mdash; iš anksto įkeltų turimo sąrašo svetainės ir vietos dimensijas.* Iš **anksto įkelti atsargų matomumo suvestinės** puslapį **pateikiami** filtrai, kurie yra panašūs į atsargų suvestinės puslapį, išskyrus tas dimensijas, kurios jau pasirinktos. Toliau pateiktoje ekrano nuotrauka aprašo galimų filtravimo laukus, esančius **puslapyje Iš anksto įkelti atsargų matomumo suvestinės** puslapį.

![Iš anksto įkelti atsargų matomumo suvestinės puslapį.](media/inventory-visibility-preload-onhand-list.png "Iš anksto įkelti atsargų matomumo suvestinės puslapį")

Iš **anksto** **įkelkite** atsargų matomumo suvestinės ir atsargų suvestinės puslapių apačią, rasite informacijos, pvz., "50 įrašų (pasirinkta 29)" arba "50 įrašų". Ši informacija nurodo šiuo metu įkeltus įrašus iš **išplėsto filtro** rezultato. Tekstas „29 pasirinktas" nurodo įrašų, kurie buvo pasirinkti naudojant įkeltų įrašų stulpelio antraštės filtrą, skaičių. Taip pat yra mygtukas **Įkelti daugiau**, kurį galite naudoti norėdami įkelti daugiau įrašų iš Dataverse. Numatytasis įkeltų įrašų skaičius yra 50. Pasirinkus Įkelti **daugiau**, į rodinį bus įkelta kita 1000 galimų įrašų. Mygtuko Įkelti **daugiau mygtukas** nurodo šiuo metu įkeltus įrašus ir bendrą išplėstinio filtro **rezultato įrašų** skaičių.
