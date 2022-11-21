---
title: „Inventory Visibility“ rezervavimai
description: Šiame straipsnyje aprašoma, kaip nustatyti rezervavimo priemonę, kad būtų galima kurti rezervavimus, naudoti rezervavimus ir (arba) nerealizuoti nurodytų atsargų kiekių naudojant atsargų matomumą.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762747"
---
# <a name="inventory-visibility-reservations"></a>„Inventory Visibility“ rezervavimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas įprastas šiek tiek rezervų naudojimo atvejis ir paaiškinama, kaip juos nustatyti naudojant atsargų matomumą. Čia pateikiama informacija apie tai, kaip kurti soft rezervavimus, koresponduoti juos su faktiniu suvartojimu ir koreguoti arba nerealizuoti nurodytų atsargų kiekius.

## <a name="sample-use-case-for-soft-reservation"></a>Pavyzdžio naudojimo atvejis, skirtas švelniai rezervavimui

Švelniai rezervavimai padeda organizacijoms pasiekti vieną galimų atsargų teisingų šaltinį, ypač užsakymo įvykdymo proceso metu. Šis funkcionalumas naudingas organizacijose, kuriose yra šios sąlygos:

- Organizacija turi bent dvi skirtingas sistemas, kurios tiesiogiai priima siunčiamus užsakymus.
- Organizacija yra labai griežta ir nori išvengti dvigubo produktų atsargų rezervavimo, kuris gali įvykti jei kelios sistemos gali per daug užsakyti paskutinę atsargų dalį. Ši situacija apsaugoma nuo visų užsakymų sistemų, kurios gali atlikti tiesioginius suminio rezervavimo API iškvietimus į atsargų matomumą, kuris suteikia vieną teisingų atsargų prieinamumo šaltinį.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title=" Atsargų matomumo švelniai rezervavimas" width="720" />](media/inventory-visibility-soft-reservation.png)

Ankstesnis pavyzdys rodo, kaip veikia švelniai rezervavimas, ir išryškina šias operacijas:

- Jūsų pradinis atsargų lygis sinchronizuojamas su "Microsoft" atsargų matomumu Dynamics 365 Supply Chain Management.
- Švelniai rezervavimai registruojami iš kiekvieno užsakymo kanalų ar sistemų į atsargų matomumą. Atsargų matomumas patikrina atsargų prieinamumą ir bando šiek tiek rezervuoti. Jei pavyko šiek tiek rezervuoti, atsargų matomumo įtraukimas į soft rezervuotą kiekį, atima iš galimų rezervuoti (AFR) kiekio ir atsako su soft rezervavimo ID.
- Šiuo metu jūsų faktinių atsargų kiekis lieka toks pat.
- Tada galite sinchronizuoti vieną arba suvestinius iš dalies rezervuotus užsakymus (užsakymo eilutes) su tiekimo grandinės valdymu, norėdami atlikti sąstabų rezervavimą ir išleisti į sandėlį arba atnaujinti galutinį atsargų kiekį.
- Galite nustatyti, kad sistema kompensuotumėte [soft reservations, kai tiekimo grandinės valdymo sistemoje atnaujinamos faktinės](#offset-scm) atsargos.

Paprastai, švelniai rezervavimai kuriami, suvartojami ir atšaukiami naudojant API iškvietimus į atsargų matomumo tarnybą.

> [!NOTE]
> Galite pasirinktinai nustatyti tiekimo grandinės valdymą (ir kitas trečiosios šalies sistemas) automatinei rezervuotam kiekiui kompensuoti naudojant atsargų matomumą. Korespondentinis kiekis panaikinamas iš rezervavimo įrašų atsargų matomumo lauke.
>
> Numatyta, kad korespondentinė funkcija automatiškai įjungiama, kai įgalinate funkciją Švelniai rezervavimas.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Įjungti ir nustatyti rezervavimo funkciją

Norėdami įjungti šią rezervacijos funkciją, atlikite toliau nurodytus veiksmus.

1. Prisiregistruokite prie Power Apps atsargų matomumo **ir jį atidarykite**.
1. Atidarykite **Konfigūravimo** puslapį.
1. **Funkcijų valdymo** skirtuke įjunkite funkciją *OnHandReservation*.
1. Prisiregistruokite savo tiekimo grandinės valdymo aplinkoje.
1. Eikite į **[funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbo sritį ir įjunkite *atsargų matomumo integravimą su rezervavimo kompensavimą* funkciją (reikalinga 10.0.22 ar vėlesnė versija).
1. Eikite į **Atsargų valdymo \> nustatymo \> atsargų matomumo integravimo parametrus**, atidarykite **Rezervavimo kompensavimas** skirtuką ir atlikite šiuos parametrus:

    - **Įgalinti rezervavimo korespondentinę sąskaitą** – nustatykite kaip *Taip*, norėdami įgalinti šią funkciją.
    - **Rezervavimo korespondentinis modifikatorius** – pasirinkite atsargų operacijos būseną, kuri koresponduos rezervavimus, kurie atliekami atsargų matomumo metu. Šis parametras nustato užsakymo apdorojimo etapą, kuris suaktyvina kompensavimus. Etapą seka užsakymo atsargų operacijos būsena. Pasirinkite vieną iš šių reikšmių:

        - *Užsakyta –* užsakymai, kurių būsena *Užsakyta,* sukūrus korespondentinę užklausą nusiųs korespondentinę užklausą. Korespondentinis kiekis bus sukurto užsakymo (eilutės) kiekis.
        - *Rezervuoti* – užsakymai, kurių būsena *Rezervas*, siųs korespondentinę užklausą, kai jie yra rezervuoti arba faktiškai rezervuoti. *Kai* paslinksite būseną Rezervas, užsakymas siųs korespondentinę užklausą apie bet kurią naują atsargų būseną, artimiausią rezervuotam paimtam (pavyzdžiui, paėmimas, užregistruotas važtaraštis arba išrašyta SF). Taip nutinka net jei tiekimo grandinės valdymo dalyje rezervavimą praleisite ir tęsite iki kitos atsargų būsenos (pvz., jei praleisti iš išleidimo į sandėlį ir paimti ir pakuoti). Užklausa bus suaktyvinta tik vieną kartą. Jei jis suaktyvintas paėmimo metu, registruojant važtaraštį korespondentinė sąskaita nebus dubliuota. Korespondentinis kiekis bus toks pat, kaip ir atsargų operacijos būsenos kiekis, kai jis buvo suaktyvintas (kitaip tariant, *·*/*atitinkamoje* užsakymo eilutėje yra rezervuotas užsakytas rezervuotas faktinis rezervas arba vėlesnė būsena).

1. Vėl prisijunkite prie atsargų matomumo programos, **eikite** į konfigūracijos puslapį, **tada** skirtuke Švelniai rezervavimas peržiūrėkite numatytąją soft reservation hierarchiją. Jei reikia, į hierarchiją įtraukti naujas dimensijas.
1. Skyriuje Nustatyti soft **rezervavimo susiejimą** peržiūrėkite numatytuosius parametrus. Pagal numatytuosius nustatymus, iš dalies rezervuotų atsargų kiekiai bus įrašyti pagal `softreservephysical` fizinį duomenų šaltinio matą `iv`. Apskaičiuotas *rezervavimo matas* yra susietas su `availabletoreserve`. Jei norite atnaujinti apskaičiuotą matą`availabletoreserve`, **eikite** į konfigūracijos puslapį ir **skirtuke** Apskaičiuotas matas išplėskite ir modifikuokite apskaičiuotą matą.

Dėl daugiau informacijos, žr. [Inventoriaus matomumo papildinio konfigūravimas](inventory-visibility-configuration.md).

> [!NOTE]
> Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Jis veikia taip pat, kaip indeksų hierarchija veikia turimose užklausose, bet naudojamas nepriklausomai, kad vartotojai galėtų nurodyti dimensijų informaciją ir atlikti tikslesnius rezervavimus.
>
> Jūsų soft rezervavimo hierarchijoje turėtų būti `SiteId` komponentai `LocationId` ir kaip komponentai, nes jie sudaro atsargų matomumo skaidinio konfigūraciją.

Daugiau informacijos apie tai, kaip konfigūruoti rezervavimus, žr. [Rezervavimo konfigūravimas](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Naudoti rezervacijos funkciją atsargų matomume

Kai iškiesite rezervavimo API, sistema pažymi nurodytų prekių ir kiekių rezervavimą.

Čia pateikiamas pavyzdinis scenarijus ir API užklausos lauko pavyzdys. Įmonė Contoso parduoda produktą D0002 (kabinetas) iš savo el. komercijos svetainės. Klientas per svetainę suduos pardavimo užsakymą smulkiai raudonai kabinetui. Contoso nusprendžia įvykdyti šį užsakymą naudodama šias dimensijas:

- Organizacijos ID = usmf
- Vieta = 1
- Sandėlis = 11
- Produktas = D0002
- Spalva = raudona
- Dydis = mažas

"Contoso" jau nustatė API ryšį su atsargų matomumu savo el. komercijos sistemoje. Kai užsakymas gaunamas, sistema iš anksto suaktyvina API iškvietimą atlikti soft rezervavimą atsargų matomumo kabinetui.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Kurti švelniai rezervavimus naudojant rezervavimo API

Rezervavimai atliekami atsargų matomumo paslaugoje, pateikiant post užklausą paslaugos URL, pvz., `/api/environment/{environmentId}/onhand/reserve`.

Rezervuojant užklausos dokumentuose turi būti organizacijos ID, produkto ID, rezervuoti kiekiai ir dimensijos.

Kai iškiesite rezervavimo API, galite valdyti rezervavimo tikrinimą nurodydami parametrą Boolean `ifCheckAvailForReserv` užklausos body. Vertė, `True` kuri reiškia, kad būtinas tikrinimas, o `False` vertė reiškia, kad tikrinimas nebūtinas. Numatytoji vertė yra `True`.

Jei norite atšaukti rezervavimą ar nereservuoti nurodytų atsargų kiekių, nustatykite neigiamą kiekio vertę ir nustatykite parametrą praleisti `ifCheckAvailForReserv` ir `False` tikrinimą.

Tai užklausos lauko, kuris nurodo pardavimo užsakymą ankstesniame kontekste, pavyzdys.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Sėkminga išankstinio rezervavimo užklausa pateikia soft *rezervavimo ID* kiekvienam rezervavimo įrašui. Soft reservation ID nėra unikalus identifikatorius individualiam išankstinio rezervavimo įrašui, tačiau produkto ID ir dimensijų verčių, kurios siejamos su soft reservation request, kombinacija. Galite įrašyti soft rezervavimo ID užsakymo eilutėje, kai sinchronizuojate sėkmingai rezervuotus užsakymus su tiekimo grandinės valdymu arba kita korespondentine ERP sistema.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a> Tiekimo grandinės valdymo korespondentinis švelniai rezervavimas

Galite atskaičiuoti iš dalies rezervuotą kiekį po to, kai užsakymo kiekis faktiškai atimtas tiekimo grandinės valdymo sistemoje arba kitoje ERP sistemoje. Atsargų matomumas siūlo neįmanomą soft rezervavimo korespondentinę integraciją su tiekimo grandinės valdymu.

Norėdami suslinkti šį rezervavimą, atlikite šiuos veiksmus.

1. Prisijunkite prie „Supply Chain Management“.
1. Eiti į Pardavimo **ir rinkodaros pardavimo \> užsakymus visus \> pardavimo užsakymus**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Iš naujo sukurkite išorinį pardavimo užsakymą ir pridėkite pardavimo eilutę, kurioje naudojamos tos pačios produkto ID, organizacijos, vietos, sandėlio ir dimensijų vertės.
1. Pardavimo užsakymo **eilutėse** "FastTab" pasirinkite ką tik įvestą pardavimo eilutę, tada įrankių juostoje pasirinkite **Atsargų rezervavimo \> ID**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Nukopijuokite soft rezervavimo ID savo soft reservation request response ir įklijuokite į lauką **Rezervavimo ID**.
    - Lauką **Rezervavimo ID palikite** tuščią, bet pažymėkite atsargų **tarnybos automatinio korespondentinio** langelio žymės langelį. Sistema automatiškai nustatys, kurias produkto ir produkto dimensijas padengti, remdamasi prekės ID ir dimensijų vertėmis, įvestomis pasirinktoje eilutėje.

1. Pasirinkite **Gerai**.
1. Kol ta pati pardavimo eilutė vis dar pasirinkta, **\>** **faktiškai rezervuoti užs. kiekį pardavimo užsakymo eilučių "FastTab" įrankių juostoje pasirinkus Atsargų rezervavimas.**
1. Jei anksčiau nustatėte **lauką Rezervuoti korespondentinį modifikatorių** kaip *Rezervuota*, korespondentinė sąskaita bus suaktyvinta, *·* *kai užsakymo eilutės būsena yra Rezervuoti faktiškai arba Rezervuoti užsakyta.* Paketinė užduotis paleidžiama vieną kartą per minutę, kad būtų galima sinchronizuoti tiekimo grandinės valdymo ir atsargų matomumo korespondentines užklausas.

> [!NOTE]
> Operacijų būsenose, kurios apima nurodytą rezervo korespondentinį modifikatorių, operacijos atnaujinimas koresponduos atitinkamą rezervavimo įrašą, kai bus įvykdytos visos šios sąlygos:
>
> - Atsargų operacijos rezervavimo ID sutampa su atsargų matomumo rezervavimo įrašo rezervavimo ID.
> - Atsargų operacijos dimensijos atitinka rezervavimo įrašo dimensijas atsargų matomumo lauke.
> - Atsargų operacijos būsenos pakeitimai suaktyvina rezervavimų kompensavimus, kai atsargų operacijos būsena atspindi faktą, kad užsakymo procesas buvo baigtas arba praleistas.

Korespondentiniai kiekiai seka atsargų kiekius, kurie nurodyti atitinkamose atsargų operacijose. Korespondentinė sąskaita įsigalioja tik tuomet, jei rezervuotas kiekis lieka atsargų matomumo lauke.

### <a name="cancel-or-revert-a-soft-reservation"></a>Atšaukti arba sugrąžinti šiek tiek rezervavimą

Jei pradinė užsakymo eilutė atšaukiama arba panaikinama, o jūs turite grąžinti atitinkamą soft rezervavimą, užregistruokite neigiamą kiekį, kuriame yra tokia pati informacija API užklausos eilutėje.
