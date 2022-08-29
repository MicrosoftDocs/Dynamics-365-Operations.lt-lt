---
title: Mobiliojo įrenginio meniu elementų aplinkinių veiksmų konfigūravimas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti meniu elementų elementus, kad darbuotojai galėtų dirbti su dabartine užduotimi, atlikti kitą užduotį, o tada grįžti prie pradinės užduoties neprarasdami jokios informacijos.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 50f899cd7f28a4b7fd23db5f049de02896e8d8e9
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336132"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementų aplinkinių veiksmų konfigūravimas

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šiame straipsnyje aprašytos funkcijos taikomos tik naujai sandėlio valdymo mobiliąją programai. Jie neturi įtakos senai sandėlio programai, kuri dabar pasenusi.

Šiame straipsnyje aprašoma, kaip konfigūruoti meniu elementų elementus, kad darbuotojai galėtų "iš" atlikti dabartinę užduotį, atlikti kitą užduotį, tada grįžti prie pradinės užduoties neprarasdami jokios informacijos.

Apylanka yra atskiras meniu elementas, kurį galima atidaryti iš pagrindinės užduoties veiksmo. Apylankos pabaigoje darbuotojas yra grąžinamas į vietą, kur paliko pagrindinę užduotį. Konfigūracijos metu nurodote meniu elementą, kuris turėtų veikti kaip apylanka. Taip pat galite pasirinkti, kurios pagrindinės užduoties laukų vertės turi būti automatiškai persiunčiamos (kopijuojamos) į apylanką ir ten įvedamos. Todėl turite suprasti, kurioje užduočių srauto vietoje norite, kad darbuotojai galėtų naudotis apylanka. Taip pat turite užtikrinti, kad informacija, kurią reikia nukopijuoti į apylanką, bus prieinama naudoti šiame užduočių srauto etape.

## <a name="enable-detours-in-your-system"></a>Įgalinkite apylankas savo sistemoje

Kad būtų galima konfigūruoti veiksmų apylankas mobiliojo įrenginio meniu elementuose, turite atlikti toliau nurodytą procedūrą, kad įgalintumėte reikiamas funkcijas ir sugeneruotumėte reikiamų laukų pavadinimus Warehouse Management mobilių įrenginių programoje.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
1. Įsitikinkite, kad *sandėlio programos veiksmo* instrukcijų funkcija jūsų sistemai įjungta. Kaip ir tiekimo grandinės valdymo versija 10.0.29 ši funkcija įjungiama pagal numatytąjį nustatymą. Daugiau informacijos apie *Warehouse programos veiksmų instrukcijų* funkciją žr. [Warehouse Management mobiliosios programos veiksmų pavadinimų ir instrukcijų pritaikymas](mobile-app-titles-instructions.md). Ši funkcija yra būtina *Warehouse Management programos apylankos* sąlyga.
1. Įjungti sandėlio *valdymo programos de informacijos* funkciją. Ši funkcija yra tokia, kuri aprašyta šiame straipsnyje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ji įjungta pagal numatytąjį nustatymą.
1. Jei sandėlio *valdymo programos funkcijų funkcija nebuvo įjungta,* **\>\>\>** **atnaujinkite laukų pavadinimus sandėlio valdymo mobiliųjų įrenginių programoje, nuėję į Sandėlio valdymo nustatymo mobiliojo įrenginio programos laukų pavadinimus** ir pasirinkdami Kurti numatytąjį nustatymą. Pakartokite šį veiksmą su kiekvienu juridiniu subjektu (įmone), kuriame naudojate sandėlio valdymo mobiliąją programą. Daugiau informacijos rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigūruoti apylanką iš meniu specifinio keitimo

Norėdami nustatyti apylanką iš meniu konkretaus keitimo, naudokite nurodytą procedūrą.

1. Sukurkite meniu specifinį atnaujinimą, skirtą atitinkamo meniu ir atlikite veiksmus, kaip aprašyta [Warehouse Management mobiliosios programos veiksmų pavadinimų ir instrukcijų pritaikymas](mobile-app-titles-instructions.md).
1. Raskite veiksmo **Veiksmo ID** ir **Menu prekės pavadinimas** vertės, kurias norite redaguoti ir tada pasirinkite vertę **Veiksmo ID** stulpelyje.
1. Puslapyje, kuris rodomas **Galimos apylankos (meniu elementai)** "FastTab" laukuose galite nurodyti meniu elementą, kuris turėtų veikti kaip apylanka. Taip pat galite pasirinkti, kurios pagrindinės užduoties laukų vertės turi būti automatiškai kopijuojamos į apylanką ir iš jos. Pavyzdžių, kurie parodo, kaip naudoti šiuos parametrus, ieškokite toliau šiame straipsnyje pateikti scenarijai.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>1 pavyzdinis scenarijus: pardavimo paėmimas, kur vietos užklausa veikia kaip apylanka

Šis scenarijus rodo, kaip konfigūruoti vietos užklausą kaip apylanką darbuotojo pardavimo išrinkimo užduočių sraute. Ši apylanka leis darbuotojams peržiūrėti visas licencijoslenteles toje vietoje, iš kurios jie išrinkti, ir pasirinkti licencijos lentelę, kurią jie nori naudoti pasirinkimui užbaigti. Šis apylankos tipas gali būti naudingas, jei brūkšninis kodas yra pažeistas ir skaitytuvo įrenginys jo nenuskaito. Taip pat gali būti naudinga, jei darbuotojas turi sužinoti, kas iš tikrųjų yra pateikta sistemoje. Įsidėmėkite, kad šis scenarijus veikia tik tada, kai renkatės tik iš pagal licencijos lentelę kontroliuojamų vietų.

### <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami naudoti nurodytus pavyzdinius įrašus ir reikšmes, norėdami dirbti naudodami šį scenarijų, turite naudoti sistemą, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys. Prieš pradėdami turite pasirinkti juridinį subjektą **USMF**.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Kurkite meniu specifinius keitimus ir konfigūruoti apylankas 1 scenarijui.

Šios procedūros metu sukonfigūruosite **Pardavimo pasirinkimo** meniu elemento apylanką licencijos lentelės veiksme.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.
1. Raskite veiksmo ID, kuris vadinamas *LicensePlateId* ir pasirinkite jį.
1. Veiksmų srityje pasirinkite **Įtraukti veiksmo konfigūraciją**.
1. Iššokančiame dialogo lange naudokite **Meniu elemento** lauką, kad rastumėte ir pasirinktumėte *Pardavimų pasirinkimą*.
1. Pasirinkite **Gerai**.
1. Rodomas ką tik sukurto pakeistos informacijos puslapis. **Galimios apylankos (meniu elementai)** FastTab skirtuke pasirinkite **Įtraukti** į įrankių juostą.
1. Dialogo lange **Įtraukti apylanką** pasirinkite **Vietos užklausą** kaip apylanką, kuri bus prieinama Warehouse Management mobilioje programoje.
1. Pasirinkite **Gerai**.
1. "FastTab" skirtuke **Galimos apylankos (meniu elementai)** pasirinkite ką tik pridėtą apylanką, tada pasirinkite įrankių juostoje **Pasrinkite laukus, kurie bus siunčiami**.
1. Dialogo lange **Pasirinkti laukus, kurie bus siunčiami** nurodykite informaciją, kuri turėtų būti siunčiama į apylanką ir iš jos. Tokiu atveju įgalinate darbuotojus naudoti vietą, iš kurios jie turėtų pasirinkti, kaip įvestį vietos užklausos apylankai. Todėl skyriuje **Siųsti iš pardavimo pasirinkimo** įrankių juostoje pasirinkite **Įtraukti**, kad įtraukumėte eilutę į tinklelį. Tada nustatykite šias vertes naujai eilutei:

    - **Kopijuoti iš Pardavimo pasirinkimo:** *Vieta*
    - **Įklijuoti į Vietos užklausą:** *Vieta*

1. Kadangi šiame scenarijuje ši apylanka sukonfigūruota licencijos lentelės žingsnyje, tai bus naudinga, jei darbuotojai gali perkelti licencijos lentelę iš užklausos atgal į pagrindinį srautą. Todėl skyriuje **Grąžinti atgal iš vietos užklausos** įrankių juostoje pasirinkite **Įtraukti**, kad įtraukumėte eilutę į tinklelį. Tada nustatykite šias vertes naujai eilutei:

    - **Kopijuoti iš Vietos Užklausos:** *Licencijos lentelė*
    - **Įklijuoti į Pardavimo pasirinkimą:** *Licencijos lentelė*

1. Pasirinkite **Gerai**.

Apylanka dabar yra visiškai sukonfigūruota. Mygtukas pradėti **Vietos užklausos** apylanką dabar bus rodomas licencijos lentelėje **Pardavimo išsirinkimo** meniu elemente.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Užbaikite pardavimo pasirinkimą mobiliajame įrenginyje ir naudokite apylanką

Šios procedūros metu užbaigsite pardavimo pasirinkimą naudodami Warehouse Management mobiliąją programą. Naudosite ką tik sukonfigūruotą apylanką, norėdami rasti licencijos lentelę, kurią naudosite pasirinkimo veiksmui atlikti.

1. Microsoft Dynamics 365 Supply Chain Management sukurkite pardavimo užsakymą, kuriame reikės atlikti pasirinkimo veiksmą, kad būtų paimta iš vietos, kuri yra sekama pagal licencijos lentelę. Tada išleiskite pardavimo užsakymą į sandėlį. Pasižymėkite rodomo darbo ID, kuris yra generuojamas.
1. Atidarykite Warehouse Management mobiliųjų įrenginių programėlę ir prisiregistruokite sandėlyje 24. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami *24*, o kaip slaptažodį – *1*.)
1. Pasirinkite **Išsiuntimo** meniu ir tada pasirinkite **Pardavimo pasirinkimas** meniu elementą.
1. Norėdami įvesti darbo ID, kuris buvo sugeneruotas 1 veiksmu, vadovaukitės ekrane pateikiamomis duomenų įvedimo instrukcijomis.
1. Žingsnyje, kuriame yra tekstas **Nuskaityti licencijos lentelę** atidarykite veiksmų meniu. Turėtumėte matyti naują mygtuką, kuris pažymėtas **Vietos užklausa**. Viršutiniame kairiajame kampe nurodyta rodyklė nurodo, kad mygtukas pradės apylanką. Pasirinkite **Vietos užklausa**.
1. Apylanka pradedama. Kitame puslapyje patvirtinkite vietą, kuri buvo nukopijuota iš pagrindinio srauto.
1. Galimų licencijų lentelių vietų sąraše, pažymėkite licencijos lentelę, kurią norite nukopijuoti atgal į pagrindinį srautą. Tada pasirinkite **Atgal** mygtuką.
1. Busite grąžintas į pardavimo pasirinkimo pagrindinį srautą, o licencijos lentelė buvo nukopijuota atgal į ją iš apylankos. Patvirtinkite vertę, kad eitumėte prie kito veiksmo.
1. Dabar galite užbaigti likusį standartinį srautą įvesdami pageidaujamas duomenų įvedimo instrukcijas.

Sandėlio darbas dabar baigtas. Darbuotojas sėkmingai atidarė apylanką kad atliktų antrinę (vietos užklausos) užduotį, neprarasdamas savo vietos pagrindinėje užduotyje ir pervedė informaciją, kuri buvo reikalinga atlikti pagrindinę užduotį.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>2 pavyzdžio scenarijus: elemento užklausa su judėjimo ir koregavimo apylankomis

Šis scenarijus rodo, kaip konfigūruoti judėjimą ir koregavimus kaip kelias apylankas vietos užklausos užduočių sraute. Ši galimybė gali būti naudinga situacijose, kai darbuotojas atvyksta į vietą, nustato, kad atsargos vietoje skiriasi nuo to, kas užregistruota sistemoje, todėl turi koreguoti arba perkelti prekes.

Jei reikia, vietos užklausą galite pakeisti licencijos lentelės užklausa arba prekės užklausa.

### <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami naudoti nurodytus pavyzdinius įrašus ir reikšmes, norėdami dirbti naudodami šį scenarijų, turite naudoti sistemą, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys. Prieš pradėdami turite pasirinkti juridinį subjektą **USMF**.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Sukurkite meniu specifinius keitimus ir konfigūruoti apylankas 2 scenarijui.

Šios procedūros metu sukonfigūruosite **Pardavimo pasirinkimo** meniu elemento apylanką licencijos lentelės veiksme.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.
1. Raskite ir pasirinkite veiksmo ID, kuris vadinamas *LocationInquiryList*.

    > [!NOTE]
    > Norėdami vietoj vietos užklausos naudoti prekės užklausą, pasirinkite eilutę, kurioje veiksmo ID pavadintas *ItemInquiryList*. Norėdami naudoti licencijos lentelės užklausą pasirinkite eilutę, kurioje veiksmo ID pavadintas *LPInquiryList*.

1. Veiksmų srityje pasirinkite **Įtraukti veiksmo konfigūraciją**.
1. Iššokančiame dialogo lange naudokite **Meniu elemento** lauką, kad rastumėte ir pasirinktumėte *Vietos užklausą*.
1. Pasirinkite **Gerai**.
1. Rodomas ką tik sukurto pakeistos informacijos puslapis. **Galimios apylankos (meniu elementai)** FastTab skirtuke pasirinkite **Įtraukti** į įrankių juostą.
1. Dialogo lange **Įtraukti apylanką** pasirinkite **Judėjimas** kaip apylanką, kuri bus prieinama Warehouse Management mobilioje programoje.
1. Pasirinkite **Gerai**.
1. "FastTab" skirtuke **Galimos apylankos (meniu elementai)** pasirinkite ką tik pridėtą apylanką, tada pasirinkite įrankių juostoje **Pasrinkite laukus, kurie bus siunčiami**.
1. Dialogo lange **Pasirinkti laukus, kurie bus siunčiami** nurodykite informaciją, kuri turėtų būti siunčiama į apylanką ir iš jos. Šiame scenarijuje tikitės, kad darbuotojai ieškos pagal licencijos lentelę kontroliuojamų vietų. Todėl, būtų naudinga nukopijuoti licencijos lentelę iš užklausos į **Judėjimo** apylanką. Skyriuje **Siųsti iš pardavimo pasirinkimo** įrankių juostoje pasirinkite **Įtraukti**, kad įtraukumėte eilutę į tinklelį. Tada nustatykite šias vertes naujai eilutei:

    - **Nukopijuokite iš Vietos užklausos:** *Vieta*
    - **Įklijuokite į Judėjimą:** *Vieta/ LP*

    Šioje apylankoje nesitikite, kad kokia nors informacija bus nukopijuota atgal, nes pagrindinis srautas buvo užklausa, kurioje nereikia atlikti jokių papildomų veiksmų.

1. Pasirinkite **Gerai**.

Apylanka dabar yra visiškai sukonfigūruota. Mygtukas pradėti **Judėjimo** apylanką dabar bus rodomas licencijos lentelėje **Vietos užklausos** meniu elemente.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Atlikite vietos užklausą mobiliajame įrenginyje ir naudokite apylanką

Šios procedūros metu atliksite vietos užklausą naudodami Warehouse Management mobiliąją programą. Tada prekių judėjimui užbaigti naudosite apylanką.

1. Atidarykite Warehouse Management mobiliųjų įrenginių programėlę ir prisiregistruokite sandėlyje 24. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami *24*, o kaip slaptažodį – *1*.)
1. Pasirinkite meniu **Atsargos** ir pasirinkite **Vietos užklausos** meniu elementą.
1. Įveskite vietą, kurios užklausą norite pateikti, pvz., *FL-001*.
1. Kai pasirodo sąrašas, spustelėkite ir laikykite vieną iš joje kortelių, kad būtų parodytos galimos apylankos.
1. Pasirinkite **Judėjimas**.
1. Atkreipkite dėmesį, kad licencijos lentelė buvo nukopijuota iš pasirinktos kortelės. Patvirtinkite vertę.
1. Dabar, norėdami baigti judėjimą, galite vadovautis standartiniu užduočių srautu. Kai darbas baigtas, atidarykite veiksmų meniu ir pasirinkite **Atšaukti**.
1. Jūs būsite grąžintas į **Vietos užklausos** puslapį. Atkreipkite dėmesį, kad vertės nėra atnaujinamos automatiškai. Todėl turite rankiniu būdu atnaujinti puslapį, kad pamatytumėte perkėlimo pakeitimus.
