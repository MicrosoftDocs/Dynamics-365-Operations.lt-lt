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
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762706"
---
# <a name="use-the-inventory-visibility-app"></a>Naudokite programą „Inventory Visibility“

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti programą Atsargų matomumas.

Atsargų matomumas suteikia modeliu pagrįstą programą vizualizacijai. Programą sudaro trys puslapiai: **Konfigūracija**, **Veiklos matomumas** ir **Atsargų suvestinė**. Jam būdingos šios funkcijos:

- Ji suteikia turimos konfigūracijos ir švelniai rezervavimo konfigūracijos vartotojo sąsają (UI).
- Jis palaiko realiuoju laiku turimų atsargų užklausas įvairiuose dimensijų deriniaie.
- Joje pateikiama vartotojo sąsajos, skirtos UI užklausoms registruoti.
- Jame pateikiamas turimų produktų atsargų ir visų dimensijų rodinys.
- Joje pateikiamas turimų produktų atsargų sąrašas kartu su iš anksto nustatytomis dimensijomis. Turimos informacijos sąrašo rodinys gali būti arba visa suvestinė, arba iš anksto įkeltas turimos užklausos rezultatas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta [įdiegti ir nustatyti atsargų matomumą](inventory-visibility-setup.md).

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a> Atidaryti ir autentifikuoti atsargų matomumo programą

Norėdami atidaryti ir autentifikuoti atsargų matomumo programą, atlikite šiuos veiksmus.

1. Prisiregistruokite savo aplinkoje Power Apps.
1. Atidarykite **atsargų matomumo** programą.
1. Atidaryti veiklos **matomumo** puslapį iš kairiosios srities.
1. Pasirinkite nustatymų **mygtuką** (pavarų simbolį) puslapio viršuje.
1. Parametrų dialogo **lange įveskite kliento ID**, nuomininko **ID** **·** **ir kliento slaptojo failo vertes,** kurias pažymėjote įdiegdami ir nustatę atsargų matomumą.[...](inventory-visibility-setup.md)
1. Pasirinkite atnaujinimo **mygtuką**, esantį šalia simbolių **atpažinimo ženklo** lauko. Sistema sugeneruoja naują pateikia ženklo ženklą, remdamasi jūsų įvesta informacija.

    ![Turimos užklausos parametrai.](media/inventory-visibility-query-settings.png "Turimos užklausos nustatymai")

1. Kai gaunate tinkamą meškinėlyje atpažinimo ženklą, uždarykite dialogo langą. Pačio atpažinimo ženklo galiojimas baigsis po tam tikros laiko. Todėl, kartais turite ją atnaujinti, kai reikia atnaujinti konfigūraciją, registruoti duomenis arba užklausos duomenis.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a> Atsargų matomumo programos konfigūravimas

**Atsargų** matomumo programos konfigūracijos puslapis padeda nustatyti bendrą duomenų valdymo konfigūraciją ir funkcijų konfigūraciją. Įdiegus papildinį, numatytoji konfigūracija įtraukia „Microsoft Dynamics 365 Supply Chain Management“ (duomenų `fno` šaltinio vertę). Galite peržiūrėti numatytuosius nustatymus. Tai atlikus, atsižvelgdami į jūsų verslo poreikius ir išorinės sistemos atsargų registravimo reikalavimus, galite modifikuoti konfigūraciją, kad būtų standartinis būdas, kuriuo atsargų pakeitimai gali būti registruojami, sutvarkyti ir užklausti keliose sistemose.

Išsami informacija apie sprendimo konfigūravimą pateikta [Atsargų matomumo konfigūravimas](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Veikimo matomumas

Veiklos **matomumo** puslapis pateikia realiuoju laiku turimų atsargų užklausos, rezervavimo registravimo ir paskirstymo rezultatus, paremtus įvairiomis dimensijų kombinacijomis. Kai OnHandReservation *funkcija* įjungta [, taip pat](inventory-visibility-configuration.md) galite registruoti rezervavimo užklausas iš veiklos matomumo **puslapio**.

### <a name="on-hand-query"></a>Turimos užklausos

Turimų **atsargų realiuoju** laiku **turimų atsargų užklausas** galite pateikti užklausą naudojimo matomumo puslapio skirtuke. Norėdami nustatyti ir vykdyti užklausą, atlikite šiuos veiksmus.

1. Atidarykite **atsargų matomumo** programą.
1. Atidaryti veiklos **matomumo** puslapį iš kairiosios srities.
1. Skirtuke **Turimos užklausos** įveskite organizacijos **ID**, svetainės **ID ir vietos** ID **vertes**, kurias norite pateikti užklausoje.
1. Norėdami gauti **tikslų užklausos atitikimą, lauke Produkto ID** įveskite vieną ar daugiau produkto ID. Jei produkto **ID laukas** paliekamas tuščias, į rezultatus bus įtraukti visi produktai iš nurodytos vietos ir vietos.
1. Norėdami gauti išsamesnį rezultatą (pavyzdžiui, peržiūrėti pagal dimensijų vertes, pvz., spalvą ir dydį), **lauke Grupuoti pagal dimensijas pasirinkite Grupavimo rezultatai** pagal.
1. Norėdami rasti prekes, kurios turi konkrečią dimensijos vertę (pvz., spalva = raudona), **lauke** Filtruoti dimensijas pasirinkite dimensiją ir įveskite dimensijos vertę.
1. Pasirinkti **užklausą**. Gausite sėkmingą (žalia) pranešimą arba nepavykusį (raudoną) pranešimą. Jei užklausa nepavyksta, patikrinkite savo užklausos kriterijus ir įsitikinkite, [kad savo pateikėjo](#open-authenticate) atpažinimo ženklo galiojimas nepasibaigė.

Kitas būdas, kaip sukurti turimos informacijos užklausą, yra pateikti tiesiogines API užklausas. Galite naudoti arba `/api/environment/{environmentId}/onhand/indexquery``/api/environment/{environmentId}/onhand`. Norėdami gauti daugiau informacijos, žr. [atsargų matomumo viešas API](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Rezervavimo publikavimas

Norėdami užregistruoti **rezervavimo užklausą**, naudokite puslapio **Veiklos** matomumas rezervavimo registravimas skirtuką. Kad būtų galima užregistruoti rezervavimo užklausą, reikia įjungti funkciją *OnHandReservation*. Daugiau informacijos apie šią funkciją ir jos įjungus ieškokite atsargų [matomumo rezervavimuose](inventory-visibility-reservations.md).

> [!NOTE]
> Galimybė šiek tiek rezervuoti naudojant vartotojo sąsają yra skirta tam, kad jūs galite patikrinti šią funkciją. Kiekviena soft rezervavimo užklausa turi būti susieta su operacijos užsakymo eilutės keitimą (kūrimas, modifikavimas, naikinimas ir pan.). Todėl rekomenduojame atlikti tik švelniai rezervavimus, kurie yra susieti su atgalinis užsakymas. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

Norėdami, naudodami vartotojo sąsają, užregistruoti šiek tiek rezervavimo užklausą, atlikite šiuos veiksmus.

1. Atidarykite **atsargų matomumo** programą.
1. Atidaryti veiklos **matomumo** puslapį iš kairiosios srities.
1. Skirtuko Rezervavimo **registravimas** lauke **Kiekis nurodykite** kiekį, kurį norite rezervuoti švelniai.
1. Išvalykite **žymės langelį Įgalinti neigiamas atsargas, kad** būtų galima perrašyti atsargas, kad jos nebūtų per daug ar per daug rezervuotos.
1. Lauke Operatorius **pasirinkite** duomenų šaltinį ir fizinį matą, kurie bus taikomi iš dalies rezervuotame kiekyje.
1. Įveskite organizacijos **ID**, svetainės **ID**, **vietos ID** ir produkto **ID** vertes, kurias norite pateikti užklausoje.
1. Norėdami gauti išsamesnį rezultatą, pasirinkite duomenų šaltinį, dimensijas ir dimensijų vertes.

Kitas būdas užregistruoti švelniai rezervavimą – pateikti tiesiogines API užklausas. Naudokite trafaretą, kuris aprašytas [kurti vieną rezervavimo įvykį](inventory-visibility-api.md#create-one-reservation-event). Tada rinkitės **Publikuoti**. Norėdami peržiūrėti užklausos atsakymo informaciją, pasirinkite **Rodyti išsamią informaciją**. Taip pat galite gauti  `reservationId` vertę iš atsakymo informacijos.

### <a name="allocation"></a>Paskirstymas

Informacijos apie tai, kaip valdyti paskirstymus iš vartotojo sąsajos ir API, ieškokite [atsargų matomumo atsargų paskirstyme](inventory-visibility-allocation.md).

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

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a> Iš anksto įkelti supaprastintą turimos informacijos užklausą

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Tiekimo grandinės valdymas saugo daug informacijos apie dabartines turimas atsargas ir tampa pasiekiamas įvairiais tikslais. Tačiau daugeliui kasdienių operacijų ir trečiųjų šalių integravimui reikia tik mažo šios informacijos subrinkinio, o visos sistemos užklausa gali vesti didelius duomenų rinkinius, kurių prireiks norint surinkti ir perkelti. Todėl atsargų matomumo tarnyba gali periodiškai surasti ir saugoti supaprastintą turimų atsargų duomenų rinkinį, kad optimizuota informacija būtų nuolat pasiekiama. Saugoma turimų atsargų informacija filtruojama pagal konfigūruojamus verslo kriterijus, siekiant užtikrinti, kad būtų įtraukta tik tinkamiausia informacija. Kadangi filtruoti turimų atsargų sąrašai saugomi vietoje atsargų matomumo paslaugoje ir yra reguliariai atnaujinami, jie palaiko greitą prieigą, duomenų eksportą pagal poreikį ir supaprastintą integravimą su išorinėmis sistemomis.

Iš **anksto įkelkite atsargų matomumo suvestinės** puslapį, kad būtų galima peržiūrėti turimos indekso *užklausos iš anksto įkelti rezultatų objektą*. Skirtingai nei *atsargų suvestinės objektas*, *turimų* atsargų indekso užklausos išankstinio įkėliaus rezultatų objektas pateikia produktų su pasirinktomis dimensijomis turimų atsargų sąrašą. Atsargų matomumas sinchronizuoja iš anksto įkeltus suvestinės duomenis kas 15 minučių.

Norėdami peržiūrėti duomenis skirtuke Iš anksto įkelti atsargų matomumo suvestinę, **turite įjungti konfigūravimo puslapio funkcijų valdymo skirtuko funkciją OnHandIndexQueryPreloadBackgroundService** *·* **·** **ir** pasirinkti Naujinti konfigūraciją (**taip** pat žr. atsargų matomumą).[...](inventory-visibility-configuration.md)

> [!NOTE]
> *Kaip ir naudojant funkciją OnhandMostSpecificBackgroudService*, Funkcija OnHandIndexQueryPreloadBackgroundService *seka tik turimų atsargų keitimus,* kurie įvyko įjungtas dėl funkcijos. Produktų, kurie nebuvo pakeisti nuo tada, kai įjungta funkcija, duomenys nebus sinchronizuoti iš atsargų tarnybos talpyklos į aplinką Dataverse. Jei jūsų **atsargų** suvestinės puslapis nerodo visos turimos informacijos, kurios tikitės, **eikite į Atsargų valdymo > Periodinės užduotys > Atsargų matomumo integravimas**, uždrauskite paketinę užduotį ir vėl ją įjunkite. Taip bus inicijuotas stūmimas *, o visi duomenys bus sinchronizuoti su turimo indekso užklausos išankstinio* įkėliaus rezultatų objektu per kitas 15 minučių. Jei norite naudoti šią priemonę, **rekomenduojame ją įjungti prieš kuriant turimų atsargų pakeitimus ir įgalinti atsargų matomumo integravimo paketinę** užduotį.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a> Filtruoti ir naršyti atsargų suvestines

Naudodami **išplėstinį filtrą**, kuris suteikia „Dataverse“, galite sukurti asmeninį rodinį, kuriame būtų rodomos jums svarbios eilutės. Išplėstinės filtro pasirinktys leidžia jums sukurti platų rodinių diapazoną – nuo paprasto iki kompleksinio. Jos taip pat leidžia į filtrus įtraukti sugrupuotas ir įdėtąsias sąlygas. Norėdami sužinoti daugiau apie tai, kaip naudoti išplėstinį filtrą, žr. Redaguoti arba [kurti asmeninius rodinius naudojant išplėstinius tinklelių filtrus](/powerapps/user/grid-filters-advanced).

Atsargų **suvestinės puslapyje yra** trys laukai virš tinklelio (**Numatytoji** dimensija, **·** **Pasirinktinė** dimensija ir Matas), kuriuos galite naudoti, norėdami valdyti, kurie stulpeliai yra matomi. Taip pat galite pasirinkti bet kurią stulpelio antraštę, pagal kurią norite filtruoti arba rūšiuoti dabartinius rezultatus pagal tą stulpelį. Toliau pateiktoje ekrano nuotrauka aprašo dimensijas, filtravimą, rezultatų skaičių ir įkėlimą **daugiau, esančius atsargų suvestinės** puslapyje.

![Atsargų suvestinės puslapis.](media/inventory-visibility-onhand-list.png "Atsargų suvestinės puslapis")

Kadangi jūs turite iš anksto nustatyti dimensijas, kurios naudojamos suvestinės duomenims įkelti iš anksto, **atsargų** matomumo suvestinės puslapyje bus rodomi su dimensija susiję stulpeliai. *Dimensijas sistema gali tinkinti tik pagal&mdash; iš anksto įkeltų turimo sąrašo svetainės ir vietos dimensijas.* Iš **anksto įkelti atsargų matomumo suvestinės** puslapį **pateikiami** filtrai, kurie yra panašūs į atsargų suvestinės puslapį, išskyrus tas dimensijas, kurios jau pasirinktos. Toliau pateiktoje ekrano nuotrauka aprašo galimų filtravimo laukus, esančius **puslapyje Iš anksto įkelti atsargų matomumo suvestinės** puslapį.

![Iš anksto įkelti atsargų matomumo suvestinės puslapį.](media/inventory-visibility-preload-onhand-list.png "Iš anksto įkelti atsargų matomumo suvestinės puslapį")

Iš **anksto** **įkelkite** atsargų matomumo suvestinės ir atsargų suvestinės puslapių apačią, rasite informacijos, pvz., "50 įrašų (pasirinkta 29)" arba "50 įrašų". Ši informacija nurodo šiuo metu įkeltus įrašus iš **išplėsto filtro** rezultato. Tekstas „29 pasirinktas" nurodo įrašų, kurie buvo pasirinkti naudojant įkeltų įrašų stulpelio antraštės filtrą, skaičių. Taip pat yra mygtukas Įkelti **daugiau,** kurį galite naudoti norėdami įkelti daugiau įrašų iš Dataverse. Numatytasis įkeltų įrašų skaičius yra 50. Pasirinkus Įkelti **daugiau**, į rodinį bus įkelta kita 1000 galimų įrašų. Mygtuko Įkelti **daugiau mygtukas** nurodo šiuo metu įkeltus įrašus ir bendrą išplėstinio filtro **rezultato įrašų** skaičių.
