---
title: Bendrasis planavimas su tiekimo prognozėmis
description: Šiame straipsnyje aprašoma, kaip bendrojo planavimo metu atsižvelgiama į tiekimo prognozes.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690164"
---
# <a name="master-planning-with-supply-forecasts"></a>Bendrasis planavimas su tiekimo prognozėmis

[!include [banner](../../includes/banner.md)]

Tiekimo prognozės leidžia nurodyti tiekimą, kuris, jūsų tikimasi, reikalingas tam tikru būsimu laikotarpiu. Paprastai vertinimas bus pagrįstas ankstesnių metų pardavimo retrospektyva ir tada naudosite prognozę biudžeto planavimo tikslais. Taip pat galite nustatyti savo bendrąjį planą, į kurį planuodami atsižvelkite į prognozes.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Nustatyti bendrąjį planą, kad būtų galima atsižvelgti į tiekimo prognozes

Galite nurodyti, ar kiekvienas bendrasis planas turi atsižvelgti į jo vykdomas prognozes. Norėdami nustatyti kiekvieno plano prognozės pasirinktis, naudokite nurodytą procedūrą.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Arba sąrašo srityje pasirinkite esamą bendrąjį planą, arba veiksmų **srityje** pasirinkite Naujas, kad sukurtumėte naują.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Prognozės** modelis – pasirinkite modelį, kuriame yra tiekimo ir (arba) poreikio prognozės, į kurias turi būti atsižvelgiama bendrojo plano metu.
    - **Įtraukti tiekimo prognozę** – nustatykite šią pasirinktį *kaip Taip*, jei į bendrąjį planą reikia atsižvelgti į tiekimo prognozes.
    - **Įtraukti poreikio prognozę** – nustatykite šią pasirinktį *kaip Taip*, jei bendrasis planas turi atsižvelgti į poreikio prognozes. Nors šis parametras nepriklauso nuo **parametro** Įtraukti tiekimo prognozę, kai kurie kiti puslapio parametrai taikomi ir tiekimo prognozėms, ir poreikio prognozėms. Daugiau informacijos apie planavimą, kurį reikia naudoti poreikio prognozėms, rasite bendrojo planavimo [su poreikio prognozėmis.](demand-forecast.md)
    - **Metodas, naudojamas prognozės reikalavimams sumažinti** – pasirinkite metodą, kurį naudosite prognozės reikalavimams sumažinti bendrojo planavimo metu:

        - *Nėra* – prognozės reikalavimai nebus sumažinti bendrojo planavimo metu.
        - *Procentas – mažinimo raktas* – prognozės reikalavimai bus sumažinti pagal procentus ir laikotarpius, kurie nurodyti mažinimo rakte.
        - *Operacijos – mažinimo raktas* – prognozės poreikius sumažins operacijos, kurios įvyksta per laikotarpius, kurie apibrėžti mažinimo rakte.
        - *Operacijos – dinaminis laikotarpis* – prognozės reikalavimus sumažins užsakymo operacijos, kurios įvyksta dinaminį laikotarpį. Dinaminis laikotarpis apima dabartines prognozės datas ir baigiasi kitos prognozės pradžios metu. Operacijos *– dinaminio* laikotarpio metodas netaiko arba reikalauja mažinimo rakto, ir kai jį naudojate, taikomos šios sąlygos:

            - Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).
            - Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.
            - Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.
            - Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.
            - Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.

        > [!NOTE]
        > Metodas **, naudojamas prognozės poreikių** nustatymui sumažinti, taip pat taikomas poreikio prognozėms, jei įgalinote jas bendrojo plano metu ir panašiai veikiate jas. Daugiau informacijos ieškokite Bendrasis planavimas [su poreikio prognozėmis](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Nustatyti padengimo grupių mažinimo parinktis

Norėdami nustatyti pasirinktis, kurios kontroliuoja, kaip padengimo grupė sumažins jos prognozės reikalavimus bendrieji planai, naudojantys operacija pagrįstą mažinimą, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis planavimas \> Nustatymas \> Planai \> Apimties grupės**.
1. Pasirinkite esamą padengimo grupę sąrašo srityje arba veiksmų **srityje** pasirinkite Naujas, kad sukurtumėte naują.
1. **Skirtuke Kita** "FastTab" lauke Sumažinti prognozę pagal **nurodykite,** kaip padengimo grupės prekių tiekimo prognozės reikalavimai turi būti sumažinti, **·** *kai nustatyti metodai prognozės reikalavimams sumažinti nustatyti į Operacijos –* *Mažinimo raktas arba Operacijos – dinaminis laikotarpis.* Pasirinkite vieną iš šių reikšmių:

    - *Visos perlaidos* – Visos perlaidos turi sumažinti prognozę.
    - *Užsakymai* – tik to paties tipo užsakymai turėtų sumažinti prognozę.

    Pavyzdžiui, numatytieji prekės užsakymo parametrai nurodo, kad ji turi būti gaminama. Yra 50 vienetų kiekio tiekimo prognozės eilutė, o esamas pirkimo užsakymas, kurio kiekis yra 20. Jei laukas **Sumažinti prognozę** pagal nustatytas į *Užsakymai*, bus sukurtas suplanuotas gamybos užsakymas, kurio kiekis yra 50. Jei nustatyta kaip Visos *operacijos*, suplanuotas gamybos užsakymas bus sumažintas iki 30 kiekio.

    Šis parametras taip pat taikomas poreikio prognozės mažinimui. Daugiau informacijos ieškokite Bendrasis planavimas [su poreikio prognozėmis](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Įvesti produkto tiekimo prognozę

Norėdami įvesti produkto tiekimo prognozę, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą, kurio prognozę norite įvesti.
1. Veiksmų srities skirtuke Planas **pasirinkite** Tiekimo **prognozė**.
1. Veiksmų srities **puslapyje Tiekimo** prognozė pasirinkite Naujas, kad prognozė **būtų** galima įtraukti į tinklelį.
1. Įveskite reikiamą informaciją naujoje eilutėje, kuri reikalinga prognozei nurodyti.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Prekės su tiekimo prognozės eilutėmis planas

Kai vykdote bendrąjį planą, kuriame yra prekė, kurios tiekimo prognozė yra, sistema sukurs įvestų tiekimo eilučių pirkimo užsakymą. Atsižvelgiama į numatytuosius prekės užsakymo parametrus. Jei šie **numatytieji** *užsakymo* parametrai nurodo pirkimo užsakymo numatytojo užsakymo tipo vertę ir tiekimo prognozės eilutėje nenurodytas joks tiekėjo kodas, sistema prekei naudos numatytąjį tiekėją.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Tikrinti, ar suplanuotas užsakymas yra tiekimo prognozės užsakymas

Norėdami sužinoti, ar pagal tiekimo prognozę sukurtas suplanuotas užsakymas, naudokite nurodytą procedūrą.

1. Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**.
1. Atidarykite suplanuotą užsakymą, kurį norite patikrinti.
1. Bendrajame **"** FastTab" peržiūrėkite tiekimo prognozės **lauko** vertę. Jei užsakymas buvo sukurtas tiekimo prognozei padengti, šis laukas bus nustatytas kaip *Taip*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Bendrojo planavimo su tiekimo prognozėmis pavyzdžiai

Šiame skyriuje pateikiami keli pavyzdžiai, kurie parodo, kaip tiekimo prognozė veikia bendrąjį planavimą.

### <a name="example-1-supply-forecast-for-an-item"></a>1 pavyzdys: Prekės tiekimo prognozė

Turite prekę, kurios numatytasis užsakymo tipas yra *Pirkimo užsakymas,* o numatytasis tiekėjas yra *US-002*. Ji turi šią tiekimo prognozės eilutę.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 |                |              | 35       | vnt.   | 1    | 11        |

Jums paleidus bendrąjį planavimą, suplanuotas pirkimo užsakymas bus sukurtas *35 prekių* iš tiekėjo *JAV-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>2 pavyzdys: Kelios tiekimo prognozės eilutės su tiekėju ir be jo

Turite prekę, kurios numatytasis užsakymo tipas yra *Pirkimo užsakymas,* o numatytasis tiekėjas yra *US-002*. Yra šios tiekimo prognozės eilutės.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 |                |              | 35       | vnt.   | 1    | 11        |
| Dabartinis puslapis | 10/10/22 | US-101         |              | 25       | vnt.   | 1    | 11        |

Šiuo atveju sistema teigia eilutę, kuri nenurodo tiekėjo kaip bendrosios prognozės, ir laikoma, kad eilutė, kurioje nurodomas tiekėjas, turi būti atimta iš bendrosios prognozės. Todėl bendrasis planavimas sukurs šiuos suplanuotus prekės pirkimo užsakymus:

- Suplanuotas pirkimo užsakymas, kurio *kiekis – 25 lt* *, iš tiekėjo US-101* (naudojamas tiekėjas ir kiekis, nurodyti prognozės eilutėje).
- *Suplanuotas pirkimo užsakymas, kurio kiekis yra 10* *prekių, iš tiekėjo US-002* (kadangi kitoje prognozės eilutėje nenurodytas joks tiekėjas, naudojamas numatytasis tiekėjas, o šios prognozės eilutės kiekis sumažinamas tiekėjui brastos prognozės eilutės kiekiu.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>3 pavyzdys: Planai, naudojantys operacijas – dinaminio laikotarpio mažinimo metodą viename prognozės laiko periode

Bendrojo planavimo metu, kurie naudoja *operacijas –* dinaminį laikotarpį kaip prognozės mažinimo metodą, prognozės kiekiai bus sumažinti, jei yra operacijų, kurios atitinka tiekimo charakteristikas.

Pavyzdžiui, turite prekę, kurios numatytasis užsakymo tipas yra *Pirkimo užsakymas*. Ji turi šią tiekimo prognozės eilutę.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 | US-101         |              | 25       | vnt.   | 1    | 11        |

Kadangi yra tik viena tiekimo prognozės eilutė, yra tik vienas prognozės laikotarpis.

Kai vykdote bendrąjį planą, *kuris nustatytas naudoti operacijas –* dinaminis laikotarpis kaip mažinimo metodas, gali būti gauti vienas iš šių rezultatų:

- *Jei yra tiekėjo JAV-101* *pirkimo užsakymas, kurio kiekis – 10*,**·** *o tiekimo prognozės laukas nustatytas kaip Taip*, bendrasis planavimas sukuria naują suplanuotą pirkimo užsakymą, *kurio likęs kiekis yra 10 prekių.* Prognozės eilutė sumažinama, nes tiekėjas atitinka esamą pirkimo užsakymą.
- *Jei yra tiekėjo JAV-102*, 1 svetainės, *11* *sandėlio* ir 10 *vnt. kiekio pirkimo užsakymas,* **·** *o tiekimo prognozės laukas nustatytas kaip Taip*, *bendrasis planavimas sukuria naują suplanuotą pirkimo užsakymą, kurio visas kiekis yra 25 vnt.* Prognozės eilutės sumažinti negalima, nes jos tiekėjas skiriasi nuo esamo pirkimo užsakymo.

> [!NOTE]
> Ši situacija gali atsirasti suplanuotuose pirkimo užsakymuose, nes su juo yra susietas tiekėjas. Tačiau perkėlimo ir gamybos užsakymų tiekimo prognozės sumos visada bus sumažinamos esamais užsakymais, nes nenurodytas nė vienas šių tipų užsakymų tiekėjas.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>4 pavyzdys: Planai, kurie naudoja operacijas – dinaminio laikotarpio mažinimo metodą kelių prognozės laikotarpių metu

Turite prekę, kurios numatytasis užsakymo tipas yra *Pirkimo užsakymas*. Yra šios tiekimo prognozės eilutės.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 | US-101         |              | 25       | vnt.   | 1    | 11        |
| Dabartinis puslapis | 10/15/22 | US-101         |              | 25       | vnt.   | 1    | 11        |

Šiame pavyzdyje yra dvi prognozės eilutės, kurių kiekviena turi kitą datą. Todėl datos nustato prognozės laikotarpių ribas. Pirmasis laikotarpis yra nuo 2022 m. spalio 10 d. iki spalio 14 d. (10/10/22–10/14/22). Antrasis bus 2022 m. spalio 15 d. (10/15/22) toliau.

Yra tiekėjo *JAV-101 pirkimo užsakymas, kiekis – 10* *k.,* *o data – 10/12/22 (2022* m. spalio 12 d.). Kai vykdote bendrąjį planą, kuris nustatytas *naudoti operacijas –* dinaminis laikotarpis kaip mažinimo metodas, jis sukurs šiuos užsakymus:

- Suplanuotas *užsakymas, kurio kiekis yra 15* *prekių, o data 10/10/22* (Kiekis sumažinamas esamu pirkimo užsakymu, kurio data yra tą patį prognozės laikotarpį.)
- Suplanuotas užsakymas, kurio *kiekis yra 25* *m., o data 10/15/22 (Kiekis yra visas* prognozės kiekis).

### <a name="example-5-plans-that-use-no-reduction"></a>5 pavyzdys: Planai, kurie nesumažinimo

Kai vykdote planą, kuriame prognozės sumažinimo metodas *Nėra*, bendrasis planavimas visada sukurs suplanuotą visų tiekimo prognozės eilučių tiekimą. Patvirtinus suplanuotą tiekimą, bus sumažinti būsimi suplanuoti užsakymai. Tačiau pirkimo užsakymai nesumažės tiekimo prognozės eilučių.

Pavyzdžiui, turite prekę, kurios numatytasis užsakymo tipas yra *Pirkimo užsakymas*. Ji turi šią tiekimo prognozės eilutę.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 | US-101         |              | 25       | vnt.   | 1    | 11        |

Yra tiekėjo *JAV-101, 1* svetainės, *11* *sandėlio,* *25* *vnt. kiekio ir datos 10/10/22 pirkimo užsakymas.* 

Kai paleidžiate bendrąjį planą, kuris nustatytas taip, kad kaip mažinimo metodą būtų naudojamas Joks, *bus sukurtas suplanuotas pirkimo užsakymas tiekėjui JAV-101*, *1* vieta, *11* sandėlis, *25 prekių* kiekis ir *data 10/10/22*.*·* Kitaip tariant, esamo pirkimo užsakymo nebus sumažintas, nes prognozės sumažinimo metodas yra *Nėra*.

Dabar redaguojate suplanuotą pirkimo užsakymą, sukurtą po paskutinio planavimo vykdymo, ir pakeiskite kiekį į *15 mėn*. Tada patvirtinate užsakymą. Kai kitą kartą galėsite vykdyti bendrąjį planą, *bus sukurtas suplanuotas pirkimo užsakymas tiekėjui JAV-101*, *1 vieta*, *11* sandėlis, *kiekis* 10 el *. ir data 10/10/22*. Šiuo metu kiekis bus sumažintas, kad atspindėtų esamo patvirtinto užsakymo, kuris buvo nurodytas ankstesniame planavimu, kiekį.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Skirtumai tarp planavimo optimizavimo ir įtaisyto planavimo modulio

Tiekimo prognozės šiek tiek skiriasi, tai priklauso nuo jūsų naudojamas planavimo modulio (įtaisytasis bendrasis planavimas arba planavimo optimizavimas). Šiame skyriuje aprašomi skirtumai.

### <a name="vendor-groups"></a>Tiekėjų grupės

Kai pridedate prognozuojamą eilutę, galite nurodyti tiekėją ir tiekėjų grupę. Įtaisytojo planavimo sistemoje sukurti suplanuoti užsakymai grupuojami pagal tiekėjų ir tiekėjų grupės verčių derinį. Planavimo optimizavime suplanuoti užsakymai grupuojami pagal tiekėją.

Toliau esančioje lentelėje pateikiami prekės tiekimo prognozės eilučių pavyzdžiai.

| Modelis    | Data     | Tiekėjo paskyra | Tiekėjų grupė | Kiekis | Vienetas | Svetainė | Sandėlis |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| Dabartinis puslapis | 10/10/22 |                | Tiekėjų grupė | 5        | vnt.   | 1    | 11        |
| Dabartinis puslapis | 10/10/22 |                | Tiekėjų grupė | 6        | vnt.   | 1    | 11        |
| Dabartinis puslapis | 10/10/22 |                |              | 7        | vnt.   | 1    | 11        |

Tiekėjas *VendorA* yra numatytasis tiekėjų grupės *VendorGroupA tiekėjas*. Tai taip pat numatytasis prekės tiekėjas.

Įtaisytasis planavimo variklis sukurs šiuos užsakymus:

- Suplanuotas tiekėjo Tiekėjo A *, tiekėjų grupės* VendorGroupA *ir* kiekio 11 pirkimo *užsakymas*
- Suplanuotas tiekėjo tiekėjo pirkimo *užsakymas,* kurio kiekis – *7*

Planavimo optimizavimas sukurs tik vieną užsakymą:

- Suplanuotas tiekėjo Tiekėjo A *, tiekėjų grupės* VendorGroupA *pirkimo* užsakymas ir kiekis – *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Bendrųjų prognozių sumažinimas pagal konkrečias prognozes

Įtaisytojo bendrojo planavimo sistemoje rezultatas yra neprognozuojamas, jei kai kurios prognozės turi tiekėją, o kitos – ne.

Planavimo optimizavime bendrosios prognozės visada sumažinamos labiau konkrečiomis prognozėmis, kaip parodyta toliau pateiktame pavyzdyje.

Toliau esančioje lentelėje pateikiami prekės tiekimo prognozės eilučių pavyzdžiai.

| Data       | Kiekis | Tiekėjas   | Tiekėjų grupė  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Tiekėjas – A | VendorGroup-A |
| 02/11/2022 | 6,00     | Tiekėjas – A | VendorGroup-A |
| 02/11/2022 | 15.00    |          |               |

Bendroji prognozė (15,00 vienetų) sumažinama pagal konkrečias prognozes (5,00 + 6,00 = 11,00 vienetų). Likutis priskiriamas numatyta taip pat kaip numatytasis tiekėjas. Toliau pateikiamoje lentelėje rodomi suplanuoti užsakymai.

| Data       | Kiekis | Tiekėjas   | Tiekėjų grupė  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Tiekėjas – A | VendorGroup-A |
| 02/11/2022 | 4.00     | Tiekėjas – A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Numatytųjų užsakymo parametrų vykdymas generuojant suplanuotus užsakymus

Kiekviena prekė gali turėti numatytuosius užsakymo parametrus, pvz., mažiausią pirkimo užsakymo kiekį. Įtaisytasis planavimo modulis nepaiso šių parametrų, todėl prognozės konvertuojamos į suplanuotus užsakymus, kurių kiekis toks pat. Planavimo optimizavimas pagal šiuos parametrus, kai suplanuoti užsakymai generuojami pagal tiekimo prognozes. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Suplanuotų užsakymų sujungimas dėl sumažinimo pagal patvirtintus užsakymus

Įtaisytasis bendrojo planavimo modulis daro prielaidą, kad tik vienas užsakymas sumažins esamą tiekimo prognozę. Todėl jei keli užsakymai atitinka tiekimo prognozės eilutę, tik pirmasis užsakymas ją sumažins. Planavimo optimizavime visi užsakymai, kurie atitinka tiekimo prognozės eilutę, sumažins ją.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Prognozių sumažinimas tik suderinus tiekėjus

Kai įtaisytasis bendrojo planavimo modulis sumažina prognozę pagal esamus išleisti pirkimo užsakymus, programa užtikrina, kad pirkimo užsakymo tiekėjas atitiktų tiekėją pagal prognozę. Planavimo optimizavimas sumažina prognozes tik pagal pirkimo užsakymus, kurių tiekėjo lauke yra atitinkanti vertė.

Perkėlimo ir gamybos užsakymų tiekėjo lauko visada nepaisoma, nes jis yra su šiais užsakymų tipais susijusias.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Prognozių sumažinimas pagal perkėlimo užsakymus

Jei numatytasis prekės užsakymo tipas yra Perkėlimas, prognozes *galima* sumažinti tik esamais suplanuotais perkėlimo užsakymais. Tačiau gamybos užsakymų ir pirkimo užsakymų tiekimo prognozę sumažina tik išleisti užsakymai.

Įtaisytasis planavimo modulis sumažina visų perkėlimo užsakymų būsenų skaičius, o planavimo optimizavimas sumažina prognozes tik pagal perkėlimo užsakymus, kurių būsena *Išleista*.
