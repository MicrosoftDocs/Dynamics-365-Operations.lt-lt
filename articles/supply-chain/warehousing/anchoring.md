---
title: Fiksavimas
description: Šioje temoje paaiškinama, kaip įgalinti ir naudoti fiksavimą.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505589"
---
# <a name="anchoring"></a>Fiksavimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama išsami informacija apie fiksavimo procesą. Joje aprašoma reikiama konfigūracija ir logika, vykdoma sandėlio darbuotojui pakeitus padėjimo vietą arba iškrovimo vietą.

Fiksavimo funkcija leidžia nepaisyti paėmimo arba iškrovimo vietos. Tada visi atviri padėjimai bus nukreipti į naują jūsų nurodytą paėmimo arba iškrovimo vietą.

Ši funkcija gali padėti darbuotojams efektyviau siųsti prekes. Štai keletas pavyzdžių:

- Darbuotojas, kuris turi padėti 1 užsakymo prekes į išdėstymo vietą prie 1 rampos, negali to atlikti, nes iš tos vietos dar nepašalintas pirmesnis krovinys. Užuot laukęs, kol atsilaisvins paėmimo vieta 1 rampoje, darbuotojas nusprendžia naudoti išdėstymo vietą 2 rampoje. Todėl darbuotojas pakeičia siūlomą išdėstymo vietą. Visų likusių darbo prekių padėjimo vieta tada pakeičiama į 2 rampos išdėstymo vietą.
- Darbuotojas, kuris turi atlikti keletą to paties pristatymo paėmimų, gali būti tikras, kad visos padėjimo prekės yra surinktos toje pačioje vietoje. Todėl reikia mažiau laiko prekėms įkelti į sunkvežimį.

Jūs konfigūruojate mobiliojo įrenginio meniu elementų fiksavimą naudodami **Fiksavimo** parinktį. Jei nustatote ši parinktį į *Taip*, galite naudoti **Fiksuoti pagal** lauką nurodyti, ar norite fiksuoti pagal siuntą, ar pagal krovinį. Jei lauką **Fiksuoti pagal** nustatote į *Siunta*, vėlesni atviri padėjimai bus pakeisti į naują tos siuntos vietą. Jei jį nustatote kaip *Įkelti*, vėlesni atviri padėjimai bus pakeisti į naują to krovinio vietą.

> [!IMPORTANT]
> Vėlesnių atvirų padėjimų vieta bus pakeista tik darbo eilutėse, kurios yra generuojamos iš tos pačios darbo šablono eilutės. Kitaip tariant, sistema užfiksuos padėjimo eilutes iš tos pačios darbo šablono eilutės.

Šioje temoje pateikiamas scenarijus, parodantis, kaip veikia fiksavimas. Scenarijaus metu sukursite pardavimo užsakymų rinkinį ir juos išleisite į sandėlį. Tada pakeisite siūlomą paėmimo vietą ir patikrinsite, ar visas likęs padėjimo darbas yra nukreiptas į naują vietą.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Būtina scenarijaus sąlyga: padaryti pasiekiamas demonstracinius duomenis

Šioje temoje esantis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis. Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į *USMF*.

## <a name="scenario-setup"></a>Scenarijaus nustatymas

Prieš naudodami pavyzdinį scenarijų turite įgalinti fiksavimą atitinkamam mobiliojo įrenginio meniu elementui.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Mobiliojo įrenginio meniu elemento nustatymas fiksavimo įgalinimui

Jei norite įgalinti mobiliojo įrenginio meniu elemento fiksavimą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sąrašo srityje pasirinkite įrašą, pavadintą *Pardavimų surinkimas*. Jei joks esamas įrašas neturi šio pavadinimo, sukurkite jį. Patvirtinkite arba nustatykite šias įrašo vertes:

    - **Meniu elemento pavadinimas:** *Pardavimų surinkimas*
    - **Pavadinimas:** *Pardavimų surinkimas*
    - **Režimas:** *Darbas*
    - **Naudoti esamą darbą:** *Taip*
    - **Vadovas:** *Vartotojui nurodyta*
    - **Fiksavimas:** *Taip*

        Dėl šio parametro sistema pardavimų paėmimo metu sujungia kelias darbo užsakymo eilutes.

    - **Fiksuoti pagal:** *Krovinį*

        Dėl šio parametro sistema fiksuoja pagal krovinį.

    - **Nepaisyti paskirties numerio lentelės:** *Taip*
    - **Nepaisyti numerio lentelės padavimo metu:** *Taip*
    - **Palikti vartotojo užrakintą darbą:** *Taip*
    - **Leisti surinkimo perviršį:** *Taip*

### <a name="set-up-a-work-template-to-enable-staging"></a>Darbo šablono nustatymas siekiant įgalinti išdėstymą

Norėdami sukonfigūruoti darbo šabloną siekiant įgalinti išdėstymą, atlikite šiuos veiksmus. Ši konfigūracija palaikys scenarijų, pagal kurį darbuotojas pateikia prekei užsakymui į išdėstymo vietą.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.
1. Tinklelyje pasirinkite **61 SO Etapas** darbo šabloną.
1. Skyriuje **Išsami darbo šablono informacija** įsitikinkite, kad yra toliau nurodytos eilutės ir kad jos yra sukonfigūruotos, kaip parodyta čia:

    - Eilutė 1:

        - **Darbo tipas:** *Paėmimas*
        - **Privaloma:** Pasirinkite (= *Taip*)
        - **Darbo klasės ID:** *SO paėmimas*

    - Eilutė 2:

        - **Darbo tipas:** *Padėjimas*
        - **Privaloma:** Pasirinkite (= *Taip*)
        - **Direktyvos kodas:** *Etapas*
        - **Darbo klasės ID:** *SO paėmimas*

    - Eilutė 3:

        - **Darbo tipas:** *Paėmimas*
        - **Privaloma:** Pasirinkite (= *Taip*)
        - **Sustabdyti darbą:** *Taip*
        - **Darbo klasės ID:** *SO iškrovimas*

    - Eilutė 4:

        - **Darbo tipas:** *Padėjimas*
        - **Privaloma:** Pasirinkite (= *Taip*)
        - **Direktyvos kodas** *Įlankos durys*
        - **Darbo klasės ID:** *SO iškrovimas*

1. Veiksmų srityje pasirinkite **Redaguoti užklausą,** kad atidarytumėte užklausų rengyklę.
1. Skirtuke **Diapazonas** įsitikinkite, kad yra ši eilutė:

    - **Lentelė:** *Laikinos darbo operacijos*
    - **Išvestinė Lentelė:** *Laikinos darbo operacijos*
    - **Laukas:** *Sandėlis*
    - **Kriterijai:** *61*

1. Skirtuke **Rūšiavimas** įsitikinkite, kad yra ši eilutė:

    - **Lentelė:** *Laikinos darbo operacijos*
    - **Išvestinė Lentelė:** *Laikinos darbo operacijos*
    - **Laukas:** *Siuntos ID*
    - **Paieškos kryptis:** *Didėjanti*

1. Pasirinkite **GERAI** tam, kad taikytumėte savo nustatymus ir uždarytumėte užklausų rengyklę. Priimkite pakeitimus, jei būsite paraginti.
1. Veiksmų juostoje pasirinkite **Darbo antraštės lūžiai**.
1. Eilutėje, kurioje **Lauko pavadinimas** laukas nustatytas į *Siuntos ID*, įsitikinkite, kad pasirinktas **Grupuoti pagal šį lauką** žymės laukelis.

### <a name="set-up-license-plates-locations-and-inventory"></a>Numerio lentelės, vietų ir atsargų nustatymas

Prieš kurdami pardavimo užsakymus ir siuntas, turite užtikrinti, kad yra reikiamos vietos, numerio lentelės ir atsargos.

1. Eikite į **„Warehouse management” \> Nustatymas \> Sandėlis \> Numerio lentelės** ir sukurkite dvi numerio lenteles:

    - „MyLP1”
    - „MyLP2”

1. Eikite į **„Warehouse management” \> Nustatymas \> Sandėlis \> Vietos** ir sukurkite toliau nurodytas vietas, jei jos dar nėra sukurtos.

    | Sandėlis | Buvimo vieta   | Vietos šablono ID | Zonos ID   |
    |-----------|------------|---------------------|-----------|
    | 61        | „06A01R2S1B” | „PICK-06”             | AUKŠTAS     |
    | 61        | „06A01R3S1B” | „PICK-06”             | AUKŠTAS     |
    | 61        | „STAGE01”    | ETAPAS               | *(tuščia)* |
    | 61        | „STAGE02”    | ETAPAS               | *(tuščia)* |
    | 61        | „STAGE03”    | ETAPAS               | *(tuščia)* |
    | 61        | „STAGE04”    | ETAPAS               | *(tuščia)* |

1. Įsitikinkite, kad toliau nurodytos atsargos yra pasiekiamos. Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba bet kokį kitą srautą.

    | Prekės Nr. | Kiekis | Sandėlis | Buvimo vieta   | Numerio lentelė |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | „06A01R2S1B” | „MyLP1”         |
    | A0002       | 100      | 61        | „06A01R3S1B” | „MyLP2”         |

### <a name="create-demand"></a>Kurti paklausą

Prieš galėdami išbandyti fiksavimo funkciją, privalote sukurti šiek tiek poreikio. Šiuo scenarijumi sukursite tris to paties kliento pardavimo užsakymus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas** pirmam pardavimo užsakymui sukurti.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“. Nustatykite tokias šios eilutės reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *1*

1. Įrankių juostoje pasirinkite **Pridėti eilutę** antram pardavimo užsakymui pridėti ir nustatykite šias jo reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *1*

1. Vadovaukitės šiais veiksmais kiekvienai prekybos eilutei užsakyme tam, kad rezervuotumėte jam inventorių:

    1. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite pardavimo užsakymo eilutę.
    1. Įrankių juostoje pasirinkite **Atsargos \> Rezervavimas**.
    1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.
    1. Veiksmų srityje pasirinkite **Įrašyti**.

1. Norėdami sukurti antrą pardavimo užsakymą, pakartokite 2–6 veiksmus. Nustatykite tokias šio įrašo reikšmes:

    - **Kurti pardavimo užsakymą** dialogo lange:

        - **Kliento sąskaita:** *US-001*
        - **Sandėlis:** *61*

    - 1 pardavimo užsakymo eilutėje:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *2*

    - 2 pardavimo užsakymo eilutėje:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *2*

1. Jei norite rezervuoti kiekvieną 2 pardavimo užsakymo eilutę, pakartokite 7 veiksmą.
1. Norėdami sukurti trečią pardavimo užsakymą, pakartokite 2–6 veiksmus. Nustatykite tokias šio įrašo reikšmes:

    - **Kurti pardavimo užsakymą** dialogo lange:

        - **Kliento sąskaita:** *US-001*
        - **Sandėlis:** *61*

    - 1 pardavimo užsakymo eilutėje:

        - **Prekės numeris:** *A0001*
        - **Kiekis:** *3*

    - 2 pardavimo užsakymo eilutėje:

        - **Prekės numeris:** *A0002*
        - **Kiekis:** *3*

1. Jei norite rezervuoti kiekvieną 3 pardavimo užsakymo eilutę, pakartokite 7 veiksmą.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Krovinio planavimo darbo srities naudojimas kroviniui kurti ir paleisti į sandėlį

Atlikite tolesnius veiksmus, jei norite sukurti krovinį šiame scenarijuje sukurtiems užsakymams ir tada išleisti jį į sandėlį.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas 1 ir 2 pardavimo užsakymų eilutes.
1. Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**.
1. Dialogo lango **Krovinio šablono priskyrimas** lauke **Krovinio šablono ID** pasirinkite krovinio šabloną, pvz., *Stnd krovinio šablonas*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Dalyje **Kroviniai** raskite ir pasirinkite savo sukurtą krovinį.
1. Įrankių juostoje pasirinkite **Išleisti \> Išleisti į sandėlį**.
1. Dialogo lange **Išleisti krovinį į sandėlį** pasirinkite **GERAI**, kad išleistumėte pasirinktą krovinį į sandėlį.
1. Eikite į **Sandėlio valdymas \> Darbas \> Visas darbas** sukurtam darbui peržiūrėti. Turėtumėte rasti du naujus darbo ID – po vieną kiekvienai siuntai. Kiekviena darbo ID turi paėmimo ir padėjimo eilutes, kuriose atsargos atvežamos į paėmimo vietą ir iš jos – į užsakymo vietą. Pasižymėkite pirmosios siuntos **Darbo ID** reikšmę, nes ji bus reikalinga kitoje procedūroje.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Pardavimo užsakymo paėmimas į pirmosios siuntos paėmimo vietą

1. Prisijunkite prie „Warehouse Management” mobiliųjų įrenginių programėlės kaip darbuotojas sandėlyje *„61”*. (Standartiniuose demonstracijos duomenyse galite prisijungti naudodami vartotojo ID _„61”_ ir _„1”_ kaip slaptažodį.)
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Prekybos paėmimas**.
1. Pasirinkite **identifikavimo kodo** laukelį ir tuomet įveskite pirmosios siuntos darbo ID.
1. Patvirtinkite savo įrašą.
1. Lauke **„LP”** įveskite pirmosios prekės numerio lentelės numerį (*„MyLP1”*).
1. Patvirtinkite savo įrašą.
1. Lauke **Paskirties LP** įveskite bet kokį numerį (paskirties numerio lentelė neprivalo jau būti sukurta).

    Paimsite visas eilutes, kurios buvo sukurtos iš apdorotos bangos į tą patį galutinį licencijos numerį.

1. Patvirtinkite savo įrašą.
1. Lauke **„LP”** įveskite antrosios prekės numerio lentelės numerį (*„MyLP2”*).
1. Patvirtinkite savo įrašą.

    Įsivaizduokite, kad darbuotojas dabar surinko užsakymą, tačiau nuėjęs į darbe nurodytą paėmimo vietą sužino, kad vieta jau užimta. Tačiau darbuotojas gali matyti, kad kita artima vieta (*ETAPAS03*) yra galima. Todėl jis paprašys pakeisti išdėstymo vietą. Kadangi fiksavimo funkcija yra įgalinta, tada sistema automatiškai atnaujins šio ir viso susijusio darbo paėmimo vietą.

1. Pasirinkite **Nepaisyti vietos**, kad būtų nepaisoma siūlomos išdėstymo vietos.
1. Lauke **Darbo išimtys** nurodykite *Pakeistą išdėstymo juostą*.
1. Lauke **Vieta** įveskite naują išdėstymo vietą (*ETAPAS03*).
1. Patvirtinkite savo įrašą. Matysite „Darbas baigtas“ pranešimą.
1. Pasirinkite **Sandėlio valdymas \> Darbas \> Visi darbai**.
1. Atidarykite pirmosios siuntos darbo ID. Patikrinkite, ar paėmimo vieta buvo atnaujinta į naują vietą (*ETAPAS03*), kuri buvo apibrėžta naudojant mobilųjį įrenginį.
1. Atidarykite antrosios siuntos darbo ID. Patikrinkite, ar paėmimo vieta buvo atnaujinta į naują išdėstymo vietą (*ETAPAS03*) dėl fiksavimo nustatymo.

> [!NOTE]
> Visų likusių atvirų atidavimo darbo eilučių, kuriose yra ta pati paėmimo vieta ir kurios buvo sugeneruotos iš tos pačios darbo šablono eilutės, vieta bus atnaujinta į naują vietą.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Krovinio planavimo darbo srities naudojimas naujo pardavimo užsakymo įtraukimui į esamą krovinį

Jei norite įtraukti užsakymą į krovinį ir tada išleisti jį į sandėlį, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas 3 pardavimo užsakymo eilutes.
1. Veiksmų srities skirtuko **Tiekimas ir poreikis** grupėje **Įtraukti** pasirinkite **Į esamą krovinį**, kad įtrauktumėte pasirinktas užsakymo eilutes į esamą krovinį.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Dalyje **Kroviniai** raskite ir pasirinkite krovinį iš ankstesnių veiksmų.
1. Pasirinkite **Išleisti \> Išleisti į sandėlį**.
1. Dialogo lange **Išleisti krovinį į sandėlį** pasirinkite **GERAI**, kad išleistumėte pasirinktą krovinį į sandėlį.
1. Eikite į **Sandėlio valdymas \> Darbas \> Visas darbas** sukurtam darbui peržiūrėti. Pasižymėkite **Darbo ID** reikšmę, nes ji bus reikalinga kitoje procedūroje.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Pardavimo užsakymo paėmimas į trečiosios siuntos paėmimo vietą

1. Prisijunkite prie mobilios programos kaip darbuotojas sandėlyje *61*.
1. Pagrindiniame meniu pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **Prekybos paėmimas**.
1. Pasirinkite **identifikavimo kodo** laukelį ir tuomet įveskite trečiosios siuntos darbo ID.
1. Patvirtinkite savo įrašą.
1. Lauke **„LP”** įveskite pirmosios prekės numerio lentelės numerį (*„MyLP1”*).
1. Patvirtinkite savo įrašą.
1. Lauke **Paskirties LP** įveskite bet kokį numerį (paskirties numerio lentelė neprivalo jau būti sukurta).
1. Patvirtinkite savo įrašą.
1. Lauke **„LP”** įveskite antrosios prekės numerio lentelės numerį (*„MyLP2”*).
1. Patvirtinkite savo įrašą.

    Pirmajam kroviniui įsivaizduokite, kad darbuotojas sužino, jog nurodyta paėmimo vieta negalima. Todėl jie nori naudoti kitą išdėstymo vietą (*ETAPAS04*).

1. Pasirinkite **Nepaisyti vietos**, kad būtų nepaisoma siūlomos išdėstymo vietos.
1. Lauke **Darbo išimtys** nurodykite *Pakeistą išdėstymo juostą*.
1. Lauke **Vieta** įveskite naują paėmimo vietą (*ETAPAS04*).
1. Patvirtinkite savo įrašą. Matysite „Darbas baigtas“ pranešimą.
1. Pasirinkite **Sandėlio valdymas \> Darbas \> Visi darbai**.
1. Atidarykite pirmosios siuntos darbo ID. Patikrinkite, ar paėmimo vieta nebuvo atnaujinta į naują paėmimo vietą (*ETAPAS04*), nes likusi atvira padėjimo eilutė neatitinka užbaigtos padėjimo eilutės darbo šablono eilutės.
1. Atidarykite antrosios siuntos darbo ID. Patikrinkite, ar paėmimo vieta nebuvo atnaujinta į naują paėmimo vietą (*ETAPAS04*), nes paėmimo vieta neatitinka užbaigtos padėjimo eilutės paėmimo vietos. Kitaip tariant, užbaigta padėjimo darbo eilutė ir likusi atvira darbo eilutė turi skirtingas paėmimo vietas ir, šiuo atveju, atnaujinamos tik tos eilutės, kurių paėmimo vietos yra vienodos.
1. Atidarykite trečiosios siuntos darbo ID. Patikrinkite, ar paėmimo vieta buvo atnaujinta į naują išdėstymo vietą (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
