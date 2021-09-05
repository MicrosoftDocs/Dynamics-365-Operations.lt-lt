---
title: Atsargų matomumo programa
description: Šioje temoje aprašoma, kaip naudoti atsargų matomumo programą.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345007"
---
# <a name="inventory-visibility-app"></a>Atsargų matomumo programa

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šioje temoje aprašoma, kaip naudoti atsargų matomumo programą.

Atsargų matomumas suteikia modeliu pagrįstą programą vizualizacijai. Programą sudaro trys puslapiai: **Konfigūracija**, **Veiklos matomumas** ir **Atsargų suvestinė**. Jam būdingos šios funkcijos:

- Ji suteikia turimos konfigūracijos ir švelniai rezervavimo konfigūracijos vartotojo sąsają (UI).
- Jis palaiko realiuoju laiku turimų atsargų užklausas įvairiuose dimensijų deriniaie.
- Joje pateikiama vartotojo sąsajos, skirtos UI užklausoms registruoti.
- Ji pateikia pritaikytą turimų produktų atsargų rodinį kartu su visomis dimensijomis

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta [Nustatyti atsargų matomumą](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Konfigūravimas

**Konfigūracijos** puslapis padeda nustatyti turimos konfigūracijos ir soft reservation konfigūraciją. Įdiegus papildinį, numatytoji konfigūracija įtraukia „Microsoft Dynamics 365 Supply Chain Management“ (duomenų `fno` šaltinio vertę). Galite peržiūrėti numatytuosius nustatymus. Be to, atsižvelgdami į savo verslo poreikius ir išorinės sistemos atsargų registravimo reikalavimus, galite modifikuoti konfigūraciją, kad būtų galima standartizuoti būdą, kuriuo atsargų pakeitimai gali būti registruojami, tvarkomi keliose sistemose ir jų bus [„Dataverse“](/powerapps/maker/common-data-service/data-platform-intro) užklausta.

### <a name="define-data-sources"></a>Nustatyti duomenų šaltinius

Apibrėžiate kiekvieną *duomenų šaltinį*, kurį norite integruoti su atsargų matomumu. Atsargų matomumas palaiko integravimą su įvairiais duomenų šaltiniais, pavyzdžiui, jūsų point of sale (POS) sistema, „Supply Chain Management“ ir kitomis išorinėmis sistemomis. Pagal numatytuosius nustatymus „Supply Chain Management“ nustatomas kaip numatytasis duomenų šaltinis (`fno`) atsargų matomumo atveju.

Norėdami įtraukti duomenų šaltinį, atlikite nurodytus veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Norėdami įtraukti **duomenų šaltinį**, skirtuke **Naujas duomenų šaltinis** pasirinkite Naujas duomenų šaltinis.

> [!NOTE]
> Kai pridedate duomenų šaltinį, prieš atnaujindami atsargų matomumo tarnybos konfigūraciją būtinai patikrinkite duomenų šaltinio pavadinimą, faktinius matus ir dimensijų susiejimus. Pasirinkę Naujinti konfigūraciją šių parametrų **modifikuoti negalėsite**.

### <a name="set-up-dimension-mappings"></a>Dimensijų žemėlapių nustatymas

Atsargų matomumas pateikia bazinių dimensijų, kurias galima susieti pagal jūsų duomenų šaltinio dimensijas, sąrašą. Per daug tris dimensijas galima susieti.

- Pagal numatytuosius nustatymus, jeigu naudojate tiekimo grandinės valdymą kaip vieną iš duomenų šaltinių, 13 dimensijų yra susietos su „Supply Chain Management“ standartinėmis dimensijomis. Per daug kitų (`inventDimension1` dimensijų per `inventDimension12`) yra susietos su pasirinktomis „Supply Chain Management“ dimensijomis. Likusios aštuonios dimensijos yra išplėstinės dimensijos, kurias galite susieti su išoriniais duomenų šaltiniais.
- Jei negalite naudoti „Supply Chain Management“ kaip vieno iš savo duomenų šaltinių, galite laisvai susieti dimensijas. Šioje lentelėje rodomas visas galimų dimensijų sąrašas.

> [!NOTE]
> Jei jūsų dimensija nėra numatytajame dimensijų sąraše ir naudojate išorinį duomenų šaltinį, rekomenduojame naudoti `ExtendedDimension1` per `ExtendedDimension8` susiejimui atlikti.

| Dimensijos tipas | Dimensijos pavadinimas |
|---|---|
| Produktas | `ColorId` |
| Produktas | `SizeId` |
| Produktas | `StyleId` |
| Produktas | `ConfigId` |
| Sekimas | `BatchId` |
| Sekimas | `SerialId` |
| Buvimo vieta | `LocationId` |
| Buvimo vieta | `SiteId` |
| Inventoriaus būsena | `StatusId` |
| Sandėliui konkretus | `WMSLocationId` |
| Sandėliui konkretus | `WMSPalletId` |
| Sandėliui konkretus | `LicensePlateId` |
| Kitas | `VersionId` |
| Atsargos (tinkintas) | `InventDimension1` per `InventDimension12` |
| Kitas | `ExtendedDimension1` per `ExtendedDimension8` |

Norėdami dimensijų žemėlapius, atlikite nurodytus veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuko **Duomenų šaltinis** skyriuje **Dimensijų susiejimai** pasirinkite **Įtraukti** įtraukumėte dimensijų susiejimus.
1. Lauke **Dimensijos pavadinimas** nurodykite šaltinio dimensiją.
1. Lauke **Į bazinę dimensiją** pasirinkite dimensiją iš Atsargų matomumo, kurį norite susieti.
1. Pasirinkite **Įrašyti**.

![Dimensijų žemėlapių įtraukimas](media/inventory-visibility-dimension-mapping.png "Dimensijų žemėlapių įtraukimas")

Pavyzdžiui, jei jūsų duomenų šaltinyje yra produkto spalvos dimensija, galite susieti ją su bazine dimensija `ColorId` norėdami `ProductColor` pasirinktinė dimensija būtų įtraukta į `exterchannel` duomenų šaltinį. Tada ji bus susietas su bazine `ColorId` dimensija.

## <a name="create-a-physical-measure"></a>Kurti fizinį vienetą

Kai duomenų šaltinis užregistruoja atsargų pakeitimą į Atsargų matomumą, jis užregistruoja jį naudodamas *faktinius duomenis*. Faktiniai duomenys yra modifikatoriai, kurie atspindi apibendrintas atsargų operacijų būsenas. Užklausos gali būti pagrįstos faktiniais išmes taisyme.

Atsargų matomumas turi numatytųjų fizinių priemonių sąrašą. Šie numatytieji faktiniai duomenys imami iš atsargų operacijų būsenų, esančių tiekimo grandinės valdymo sąrašo puslapyje **Turimos atsargos** puslapyje „Supply Chain Management“ (**Atsargų valdymas \> Užklausos ir ataskaita \> Turimas sąrašas**).

| Keitikas | Pavadinimas / vardas ir (arba) pavardė |
|---|---|
| `PhysicalInvent` | Faktinės atsargos |
| `ReservPhysical` | Fiziškai rezervuota |
| `AvailPhysical` | Faktiškai turima |
| `ReservOrdered` | Užsakytas rezervuotas kiekis |
| `PostedQty` | Publikuotas kiekis |
| `Deducted` | Išskaičiuota |
| `Picked` | Paimta |
| `Received` | Gauta |
| `Registered` | Užregistruota |
| `Arrived` | Pristatyta |
| `Ordered` | Užsakyta |
| `OnOrder` | Užsakymas |
| `QuotationReceipt` | Pasiūlymo kvitas |
| `QuotationIssue` | Pasiūlyta išleisti |

Jei duomenų šaltinis yra „Supply Chain Management“, nereikia iš naujo kurti numatytųjų faktinių priemonių. Tačiau šiems išoriniams duomenų šaltiniams galite sukurti naujus fizinius veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skyriuje **Duomenų šaltinis** skirtuke **Faktiniai matai** rinkitės **Įtraukti**, nurodykite šaltinio matavimo pavadinimą ir įrašykite savo keitimus.

## <a name="define-the-product-hierarchy-index"></a>Nurodyti produktų hierarchijos indeksą

Nustatydami su suvestinių dimensijų grupes, galite naudoti atsargų matomumo užklausą apie turimų atsargų būseną. Atsargų matomume kiekviena dimensijų grupė yra žinoma kaip *indeksas*. Kiekvienas indeksas atitinka nustatytą numerį. Galite nuspręsti, kurios dimensijos bus naudojamos indeksuoti nustatyti remiantis tuo, kaip užklaussite apie atsargų matomumą.

Norėdami nustatyti savo produkto hierarchijos indeksą, atlikite šiuos žingsnius.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuko **Produkto hierarchijos indeksas** skyriuje **Dimensijų susiejimai** pasirinkite **Įtraukti** įtraukumėte dimensijų susiejimus.
1. Numatyta, kad pateikiamas indeksų sąrašas. Norėdami modifikuoti esamą indeksą, atitinkamo **Redaguoti** ar **Įtraukti** skyriuje pasirinkite Redaguoti arba Įtraukti. Norėdami sukurti naują indeksų rinkinį, pasirinkite **Naujas indeksų rinkinys**. Kiekvienai eilutei iš kiekvieno indeksų rinkinio **dimensijos** lauke pasirinkite iš pagrindinės dimensijos sąrašo. Automatiškai generuojamos šių laukų vertės:

    - **Nustatyti numerį** – Dimensijos, priklausančios tam pačiam grupės (indeksui), bus sugrupuotos ir joms bus priskirtas tas pats rinkinio numeris.
    - **Hierarchija** – Hierarchija naudojama apibrėžti palaikomas dimensijų kombinacijas, kurių galima užklausti dimensijos grupėje (indeksas). Pavyzdžiui, jei nustatote dimensijų grupę, kuri turi *stiliaus*, *spalvos*, ir *dydžio*, hierarchijos seką, sistema palaiko trijų užklausų grupių rezultatą. Pirmoji grupė yra tik stilius. Antroji grupė yra stiliaus ir spalvos derinys. O trečioji grupė yra stiliaus, spalvos ir dydžio kombinacija. Nepalaikomos kitos kombinacijos.

Daugiau informacijos, žr. [Produkto indekso hierarchijos konfigūracija](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Pavyzdys

Šiame skyriuje pateikiamas pavyzdys, kuriame parodyta, kaip veikia hierarchija. Šioje lentelėje šiame pavyzdyje pateikiamas galimų atsargų sąrašas.

| Produktas | Stilius | Spalva | Dydis | Kiekis |
|---|---|---|---|---|
| I0001 | Plati | Juoda | Mažas | 1 |
| I0001 | Plati | Juoda | Dideli | 2 |
| I0001 | Plati | Raudona | Mažas | 3 |
| I0001 | Reguliarus | Juoda | Mažas | 4 |
| I0001 | Reguliarus | Juoda | Dideli | 5 |
| I0001 | Reguliarus | Raudona | Mažas | 6 |
| I0001 | Reguliarus | Raudona | Dideli | 7 |

Tolesnėje lentelėje parodyta, kaip nustatoma indekso hierarchijos grupė.

| Raktas | Nustatyti numerį | Hierarchija |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Pagal ankstesnius parametrus, atsargų matomumo užklausos dimensijų derinys yra *Stilius*, *Spalva* ir *Dydis*. Hierarchijos nustatymas įgalina išorines sistemas pateikti užklausą apie turimų atsargų atsargas šiais būdais:

- `()`– sugrupuota pagal visus. Čia yra išorės rezultatai:

    - I0001, 28

- `(StyleId)` – Grupės pagal stilių. Čia yra išorės rezultatai:

    - I0001, Plotis, 6
    - I0001, Reguliarus, 22

- `(StyleId, ColorId)` – Grupuojama pagal stiliaus ir spalvos kombinaciją. Čia yra išorės rezultatai:

    - I0001, platus, juoda, 3
    - I0001, platus, raudona, 3
    - I0001, Reguliarus, Juoda, 9
    - I0001, reguliarus, raudona, 13

- `(StyleId, ColorId, SizeId)` – Grupuojama pagal stiliaus ir spalvos bei dydžio kombinaciją. Čia yra išorės rezultatai:

    - I0001, platus, juoda, mažas, 1
    - I0001, platus, juoda, didelis, 2
    - I0001, platus, raudona, mažas, 3
    - I0001, Reguliarus, Juoda, mažas, 4
    - I0001, Reguliarus, Juoda, didelis, 5
    - I0001, reguliarus, raudona, mažas, 6
    - I0001, reguliarus, raudona, didelis, 7

## <a name="set-up-a-custom-calculated-measure"></a>Pasirinktinio apskaičiuoto matavimo nustatykite

Atsargų matomumo užklausą galite naudoti ir atsargų faktiniams priemonėms, ir *pasirinktiniams apskaičiuoties priemonėms*.

Konfigūracija leidžia apibrėžti modifikatorių rinkinį, kuris pridedamas ar atimamas, kad būtų gauti bendras suvestinis išeigos kiekis.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Apskaičiuotas matas** pasirinkite **Naujas skaičiavimo matas,** kad pridėtumėte apskaičiuotą matą. Tada nustatykite laukus, kaip aprašoma tolesnėje lentelėje.

    | Laukas | Reikšmė |
    |---|---|
    | Naujo apskaičiuoto mato pavadinimas | Įveskite apskaičiuoto mato pavadinimą. |
    | Duomenų šaltinis | Užklausų sistema yra duomenų šaltinis. |
    | Modifikatoriaus duomenų šaltinis | Įveskite keitimo duomenų šaltinį. |
    | Keitikas | Įveskite keitimo vardą. |
    | Modifikatoriaus tipas | Pasirinkite modifikatoriaus tipą (*pridėjimas* ar *atimtis*). |

Toliau pateikiamoje lentelėje nurodyti pagrindiniai apskaičiuoti „`MyCustomAvailableforReservation`“ tinkintas apskaičiuotas matavimas. Daugiau informacijos apie šį pavyzdį ieškokite [duomenų šaltinio konfigūracijoje](inventory-visibility-configuration.md#data-source-configuration).

| Suskaičiuotas matavimo duomenų šaltinis | Apskaičiuotas matas | Modifikatoriaus duomenų šaltinis | Keitikas | Modifikatoriaus tipas |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Nustatyti švelnų rezervavimo susiejimą

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tam, kad galėtumėte redaguoti skirtuką **Švelniai rezervavimas** turite įjungti funkciją *OnHandReservation* skirtuke **Funkcijų valdymas**.

Nustatydami faktinio mato susiejimą su apskaičiuotu matu įgalinate atsargų matomumo tarnybą, kad remiantis faktiniu matu būtų automatiškai tikrinamas rezervavimas.

Prieš pradedant nustatyti šį susiejimą konfigūracijos puslapio skirtukuose **Duomenų šaltinis** ir **Apskaičiuotas matas** skirtuke **Konfigūravimas** puslapyje „Power Apps“ (kaip aprašyta anksčiau šioje temoje).

Norėdami nustatyti švelniai rezervavimo susiejimą, atlikite šiuos veiksmus.

1. Nurodyti fizinį matą, kuris naudojamas kaip švelniai rezervavimo matas (pvz., `softreservordered`).
1. Puslapio skirtuke **Apskaičiuotas matas** nustatykite **Konfigūracija** ir *prieinamą rezervuoti*, kuriame yra AFR skaičiavimo formulė, kurią norite susieti su faktini matu. Pavyzdžiui, galite nustatyti (galima rezervuoti), kad jis būtų susietas su `availforreserv` anksčiau apibrėžtu `softreservordered` faktiniu matais. Tokiu būdu galite rasti, kuriuos kiekius, kurių `softreservordered` atsargų būsena yra galima rezervuoti. Toliau pateikiamoje lentelėje rodoma AFR skaičiavimo formulė.

    | Keitikas | Duomenų šaltinis | Mato vnt. |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Švelnus rezervavimo susiejimas** nustatykite susiejimą su fiziniu matmeniu siekiant apskaičiuoti matą. Ankstesniame pavyzdyje galite naudoti šiuos parametrus, norėdami susieti su `availforreserv` anksčiau apibrėžtu `softreservordered` fiziniu matais.

    | Faktinio matavimo duomenų šaltinis | Fizinis matas | Galimas rezervavimo duomenų šaltinis | Galimas rezervuoti apskaičiuotas matas |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Nustatyti švelnų rezervavimo hierarchiją

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tam, kad galėtumėte redaguoti skirtuką **Švelnaus rezervavimo hierarchija** turite įjungti funkciją *OnHandReservation* skirtuke **Funkcijų valdymas**.

Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Tai veikia tuo pačiu būdu, kaip produkto hierarchija veikia turimose užklausose.

Rezervavimo hierarchija gali skirtis nuo turimos indeksų hierarchijos. Šis nepriklausomumas leidžia įgyvendinti kategorijų valdymą, kur vartotojai gali suskaidyti dimensijas į išsamią informaciją, kad nustatytų tikslesnių rezervavimų reikalavimus.

#### <a name="example"></a>Pavyzdys

Jūsų sistemoje nustatoma ši rezervavimo hierarchija.

| Dimensija | Hierarchija |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Pagal šią rezervavimo hierarchiją, galite rezervuoti šias dimensijų tvarką:

- `()`– nenurodyta jokia dimensija.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Tinkama dimensijų seka turi griežtai laikytis rezervavimo hierarchijos sekos dimensijos pagal dimensiją. Pvz., šiame pavyzdyje rezervacijos nebus leidžiamos, nes ši seka `(ColorId, StyleId)` nėra nustatyta rezervavimo hierarchijoje.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Valdymo funkcijų valdymas

Atsargų matomumo priedas suteikia tokias funkcijas, kaip *OnHandReservation* ir *OnHandMostSpecificBackgroundService*. Pagal numatytuosius nustatymus šios funkcijos yra išjungtos. Norėdami juos naudoti, **atidarykite** puslapį Power Apps konfigūravimo puslapį dalyje ir funkcijų **valdymo skirtuke** įjunkite jas.

### <a name="complete-and-update-the-configuration"></a>Baigti ir atnaujinti konfigūraciją

Baigę konfigūruoti turite įvykdyti visus atsargų matomumo keitimus. Norėdami atlikti keitimus, rinkitės **viršutiniame dešiniajame** konfigūracijos puslapio kampe ir rinkitės **Naujinti** puslapyje „Power Apps“.

Pirmą kartą, kai **pasirenkate Naujinti** konfigūraciją, sistema reikalauja savo kredencialų.

- **Kliento ID** – „Azure" programos ID, kurį sukūrėte atsargų matomumui.
- **Nuomininko ID** – jūsų „Azure" nuomininko ID.
- **Kliento raktas** – „Azure" programos raktą, kurį sukūrėte atsargų matomumui.

Kai prisiregistruojate, konfigūracija atnaujinama atsargų matomumo paslaugoje.

> [!NOTE]
> Kai pridedate duomenų šaltinį, prieš atnaujindami atsargų matomumo tarnybos konfigūraciją būtinai patikrinkite duomenų šaltinio pavadinimą, faktinius matus ir dimensijų susiejimus. Pasirinkę Naujinti konfigūraciją šių parametrų **modifikuoti negalėsite**.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Paslaugos galinio punkto radimas

Jei nežinote tinkamo atsargų matomumo tarnybos galinio punkto, atidarykite **konfigūracijos** puslapį „Power Apps“ ir tada rinkitės **Rodyti paslaugos galinį punktą** dešiniajame viršutiniame kampe. Puslapyje bus rodomas tinkamas tarnybos galinis punktas.

## <a name="operational-visibility"></a>Veikimo matomumas

Veiklos **matomumo puslapis** pateikia realiuoju laiku turimų atsargų užklausos rezultatus, paremtus įvairiomis dimensijų kombinacijomis. Kai *OnHandReservation* funkcija įjungta, taip pat galite registruoti rezervavimo užklausas iš **veiklos matomumo** puslapio.

### <a name="on-hand-query"></a>Turimos užklausos

Skirtuke **Turimų atsargų** užklausa rodomi turimų atsargų realiuoju laiku užklausos rezultatai.

Kai pasirenkate skirtuką **Turimų atsargų** užklausa, sistema reikalauja jūsų kredencialų, kad ji galėtų gauti paženklą, kuris būtinas norint pateikti užklausą dėl atsargų matomumo tarnybos. Galite tiesiog įklijuoti ypatybės atpažinimo ženklą į lauką **BearerToken** ir uždaryti dialogo langą. Tada galite registruoti turimos informacijos užklausą.

Jei pateikėjas atpažinimo ženklas netinkamas arba jei jis baigė galioti, lauke **BearerToken** turite įklijuoti naują ženklą. Įveskite teisingą **kliento ID**, **nuomininko ID**, **Kliento rakto** naujinimo reikšmes ir pasirinkite **Atnaujinti**. Sistema automatiškai gaus naują, galiojantį paerio atpažinimo ženklą.

Norėdami užregistruoti turimos informacijos užklausą, įveskite užklausą užklausos tekstą. Naudokite šabloną, kuris aprašytas [Užklausoje, naudodami skelbimo metodą](inventory-visibility-api.md#query-with-post-method).

![Turimos užklausos nustatymai](media/inventory-visibility-query-settings.png "Turimos užklausos nustatymai")

### <a name="reservation-posting"></a>Rezervavimo publikavimas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Norėdami **užregistruoti rezervavimo** užklausą, naudokite skirtuką Rezervavimo registravimas. Kad būtų galima užregistruoti rezervavimo užklausą, reikia įjungti funkciją *OnHandReservation*. Dėl daugiau informacijos apie šią funkciją, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

Norėdami registruoti rezervavimo užklausą, turite įvesti vertę užklausos tekstą. Naudokite trafaretą, kuris aprašytas [kurti vieną rezervavimo įvykį](inventory-visibility-api.md#create-one-reservation-event). Tada rinkitės **Publikuoti**. Norėdami peržiūrėti užklausos atsakymo informaciją, pasirinkite **Rodyti išsamią informaciją**. Taip pat galite gauti **reservationId** vertę iš atsakymo informacijos.

## <a name="inventory-summary"></a>Atsargų suvestinė

**Atsargų suvestinė** yra pritaikytas atsargų atsargų *sumos objekto rodinys*. Joje pateikiama produktų atsargų suvestinė kartu su visomis dimensijomis. Naudodami **išplėstinį filtrą**, kuris suteikia „Dataverse“, galite sukurti asmeninį rodinį, kuriame būtų rodomos jums svarbios eilutės. Išplėstinės filtro pasirinktys leidžia jums sukurti platų rodinių diapazoną – nuo paprasto iki kompleksinio. Jos taip pat leidžia į filtrus įtraukti sugrupuotas ir įdėtąsias sąlygas.

Norėdami sužinoti daugiau apie tai, kaip naudoti **išplėstinį filtrą**, žr. [Redaguoti arba kurti asmeninius rodinius naudojant išplėstinius tinklelių filtrus](/powerapps/user/grid-filters-advanced)

Pritaikyto rodinio viršuje pateikiami trys laukai: **Numatytoji dimensija**, **Pasirinktinė dimensija** ir **Matas**. Šiuos laukus galite naudoti, kad kontroliuojate, kurie stulpeliai yra matomi.

Norėdami filtruoti arba rūšiuoti esamus rezultatus, galite pasirinkti stulpelio antraštę.

Tinkinimo rodinio apačioje rodoma tokia informacija: „50 įrašų (pasirinkta 29)" arba „50 įrašų". Ši informacija nurodo šiuo metu įkeltus įrašus iš **išplėsto filtro** rezultato. Tekstas „29 pasirinktas" nurodo įrašų, kurie buvo pasirinkti naudojant įkeltų įrašų stulpelio antraštės filtrą, skaičių.

Rodinio apačioje yra mygtukas **Įkelti daugiau**, kurį galite naudoti norėdami įkelti daugiau įrašų iš „Dataverse“. Numatytasis įkeltų įrašų skaičius yra 50. Pasirinkus **Įkelti daugiau**, į rodinį įkeliama kita 1000 galimų įrašų. Mygtuko Įkelti **daugiau numeris** nurodo šiuo metu įkeltus įrašus ir bendrą išplėstinio filtro **rezultato įrašų** skaičių.

![Atsargų suvestinė](media/inventory-visibility-onhand-list.png "Atsargų suvestinė")
