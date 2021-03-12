---
title: Kokybės patikra
description: Šioje temoje pateikiama informacija apie kokybės tikrinimo funkciją. Ši funkcija leidžia sandėlio darbuotojams atlikti greitą vietos kokybės tikrinimą, jiems gaunant prekes vidaus doko vietoje.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 585ca933726cb932290f8abf8504aeb13848a0e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996257"
---
# <a name="quality-check"></a>Kokybės patikra

[!include [banner](../includes/banner.md)]

*Kokybės tikrinimo* funkcija leidžia sandėlio darbuotojams greitai tikrinti vietą dėl kokybės, jiems gaunant prekes vidaus doko vietoje. Šios vietos patikros yra naudingos, kai darbuotojai tikrina pakuotę arba lengvai atpažįsta prekės dalis. Funkcijas veda darbuotojus tam, kad jie greitai peržiūrėtų, ar esama akivaizdžių klaidų ar pažeidimų prieš tai, kai jie deda atsargas atidėjimo vietoje.

Ši funkcija yra alternatyvi funkcija standartiniam kokybės patikros procesui. Ji siūlo daugiau lankstuma ir greitesnį apdorojimą.

Naudojant šią funkciją atvykimo ir kokybės kontrolė vyksta tokiu būdu:

1. Kroviniui atvykus sandėlio darbuotojas užregistruoja atvykimą. Darbuotojas taip pat nuskaito licencijos numerį tam, kad užregistruotų vietą.
1. Darbuotojas atlieka greitą kokybės patikrą ir įrašo rezultatus (atitiko ar neatitiko) licencijos numeriui.
1. Įvyksta vienas iš toliau nurodytų veiksmų.

    - Jei kokybės tikrinimas atitiko, licencijos numeris priimtas ir vedamas į gavimo vietą, kaip įprasta.
    - Jei kokybės patikra nepavyko, licencijos numeris yra atmetamas ir esantis atidėjimo darbas jai yra nukreipiamas į alternatyvią vietą tolesniam tyrimui. Sukuriamas naujas kokybės užsakymas. Tam, kad peržiūrėtumėte kokybės užsakymą, kuris yra sukurtas dėl nepavykusio kokybės patikrinimo, eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.

Šis procesas taip pat gali būti nustatytas taip, kad visi nuskaityti licencijos numeriai būtų nedelsiant nukreipti į kokybės tikrinimo vietą.

## <a name="turn-on-the-quality-check-feature"></a>Įjunkite kokybės tikrinimo funkciją

Prieš tai kai galite naudoti *Kokybės tikrinimo* funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Kokybės tikrinimas*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Nustatykite funkciją pavyzdiniam scenarijui

Šis skyrius aprašo gaires ir pavyzdį, kuris rodo, kaip nustatyti *Kokybės tikrinimo* funkciją ir paruošti pavyzdinius duomenis pavyzdiniam scenarijui, kuris pateiktas vėliau šiame skyriuje.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

### <a name="quality-check-template"></a><a name="quality-template"></a>Kokybės patikrinimo šablonas

Kokybės tikrinimo šablonas nustato taisykles dėl greitos taško kokybės patikros gavimo metu.

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Darbas \> Kokybės tikrinimo šablonas**.
1. Pasirinkite **Naujas** tam, kad įtrauktumėte šabloną į tinklelį.
1. Nustatykite tolesnes vertes tam, kad nustatytumėte naują šabloną:

    - **Kokybės tikrinimo šablono pavadinimas:** *Doko tikrinimas*

        Įveskite pavadinimą, kuris nustato politikas taikomas šiam šablonui.

    - **Priėmimo politika:** *Vartotojo skatinimas*

        Nurodykite, ar vartotojai turi būti skatinami priimti ar atsisakyti atsargų kokybės darbo apdorojimo metu, ar kokybės turi būti automatiškai atsisakoma. Šios prieinamos parinktys yra *Automatinis atsisakymas* ir *Vartotojo skatinimas*.

    - **Kokybės apdorojimo politika:** *Sukurkite kokybės užsakymą*

        Pasirinkite politiką, kuri turi būti naudojama, kai kokybės inventoriaus yra atsisakoma. Galimos toliau nurodytos parinktys.

        - *Sukurti tik darbą* – Tik sukurkite darbą, kad palengvintumėte inventoriaus judėjimą.
        - *Sukurkite kokybės užsakymą* – Sukurkite kokybės užsakymą, kad palengvintumėte kokybės testus.

    - **Bandymų grupė:** *Priedas*

        Nurodykite testo grupę, kuri turi būti naudojama sukurtame kokybės užsakyme. Testo grupės yra nustatytos **Atsargų valdymo** modulyje.

        Palikite **Destrukcinio teksto** parinktį išjungtą testinei grupei. Ši parinktis nustato, ar pavyzdys bus sunaikinamas kaip dalis testo testinėje grupėje. Jei destruukcinis testas yra naudojamas, sistema generuoja atsargų perlaidą, kai kokybės užsakymas yra sukurtas elementui. Nauja atsargų operacija numato tikrinimo kiekio atsargų sumažėjimą. Atsargų sumažinimas atsitinka, kai kokybės užsakymas yra pabaigiamas per patvirtinimo žingsnį. Atsargų operacija nurodoma kaip kokybės užsakymas.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Darbo klasė - Kokybės tikrinimas

Darbo klasės yra naudojamos valdyti ir (arba) apriboti darbo tvarkos tipo eilutes, kurias sandėlio darbuotojai gali apdoroti mobiliame prietaise.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.
1. Pasirinkite **Naujas**, kad sukurtumėte darbo klasę.
1. Antraštėje nustatykite šias vertes:

    - **Darbo klasės ID:** *QC patikra*

        Įveskite pavadinimą, kuris nustato darbo klasę.

    - **Aprašas:** *QC tikrinimas*

        Įveskite trumpą aprašą, kuris nurodo, kokia darbo klasė jam naudojama.

    - **Darbo užsakymo tipas:** *Kokybė kokybės patikroje*

        Pasirinkite darbo užsakymo tipą, kuris kuriamas pagal darbo klasę. Jums nustatant kokybės patikrinimo darbą, visuomet pasirinkite *Kokybė kokybės patikroje*.

1. **Tvirtinimo įdėjimo vietos tipas** „FastTab“, palikite **Vietos tipo** laukelį tuščią.

    Jei pasirinkote vietos tipą, apribojote vietas, kuriose elementai gali būti padedami po jų paėmimo. Šis laukelis naudojamas, kai vietos direktyva bando išspręsti vietą arba kai sandėlio darbuotojas rankiniu būdu nustato vietą mobilaus prietaiso meniu elementui.

Dėl išsamesnės informacijos apie darbo klases ir kaip jas sukurti, žr. [Sukurti darbo klasę](tasks/create-work-class.md).

### <a name="work-template"></a>Darbo šablonas

Darbo šablonai leidžia jums nustatyti darbo operacijas, kurios turi būti atliekamos sandėlyje. Dažniausiai sandėlio darbo operacijas sudaro pora veiksmų: sandėlio darbuotojas paima turimas atsargas aukštyn į vietą vietą ir tuomet padeda paimtas atsargas žemyn į kitą vietą. Darbo šablonas kokybės kontrolei nustato darbo operacijas kokybės patikrų atlikimui.

#### <a name="purchase-orders"></a>Pirkimo užsakymai

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Antraštėje nustatykite **Darbo užsakymo tipo** laukelį į *Įsigijimo užsakymai*.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Pasirinkite darbo šabloną, kuris turi apimti kokybės tikrinimo žingsnį. **Peržiūros** skyriuje, **Darbo šablonas** laukelyje pasirinkite *51 PO kvitas*.
1. **Darbo šablono išsami informacija** skyriuje, atkreipkite dėmesį, kad tinklelis turi dvi egzistuojančias eilutes: vieną *Paėmimui* ir kitą *Padėjimui*.
1. **Darbo šablono išsami informacijos** skyriuje pasirinkite **Naujas** tam, kad įtrauktumėte eilutę kokybės kontrolei tinklelyje. Atkrepkite dėmesį, kad **Eilutės numeris** laukelis yra naujai eilutei nustatytai į *3*.
1. Naujoje eilutėje nustatykite šias reikšmes: Priimkite nustatytąsias vertes likusiems laukeliams.

    - **Darbo tipas:** *Kokybės patikra*
    - **Darbo klasės ID:** *Įsigijimas*
    - **Kokybės tikrinimo šablono pavadinimas:** *Doko tikrinimas*

        Pasirinkite unikalųjį darbo klasės ID. Galite naudodami šią reikšmę konfigūruoti meniu elementus mobiliajame įrenginyje ir darbų, kuriuos tie meniu elementai gali apdoroti, tipus.

1. Veiksmų juostoje pasirinkite **Įrašyti**, kad įrašytumėte savo darbą iki dabar.

    Gausite informacinį pranešimą sakantį „Negalima - kokybės patikra turi eiti iškart po paėmimo.“ Dėl to, privalote pakeisti **Eilutės numerio** vertę eilutei, kuri buvo kątik įtraukta.

1. Atlikite šiuos žingsnius, kad pakeistumėte **Eilutės numerio** vertę naujai eilutei:

    1. **Darbo šablono išsamios informacijos** skyriuje pasirinkite eilutę, kurioje **Darbo tipo** laukelis yra nustatytas į *Kokybės patikrinimas*.
    2. Pasirinkite **Eiti aukštyn** ar **Eiti žemyn** mygtuką, kad judintumėte *Kokybės tikrinimo* eilutę taip, kad ji būtų po *Paėmimo* eilute.

1. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="quality-in-quality-check"></a>Kokybė kokybės patikrinime

Po to, sukurkite darbo šabloną kokybės patikrai.

1. **Darbo šablono** puslapio antraštėje, pakeiskite **Darbo užsakumo tipo** vertęs laukelį į *Kiekis kiekio tikrinime*.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad įtrauktumėte eilutę tinklelyje **Peržiūros** skyriuje.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Darbo šablonas:** *51 kokybės patikra*

        Įveskite šablono pavadinimą.

    - **Darbo šablono aprašas:** *51 kokybės patikra*

1. Veiksmų juostoje pasirinkite **Įrašyti** tam, kad padarytumėte **Darbo šablono išsamios informacijos** skyrių prieinamą.
1. Kai naujas šablonas vis dar yra pasirinktas **Peržiūros** skyriuje, pasirinkite **Naujas** **Išsamiso darbo šablono informacijos** skyriuje, kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Darbo tipas:** *Paėmimas*
    - **Darbo klasės ID:** *QC patikra*

        Pasirinkite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.

1. **Darbo šablono išsamios informacijos** skyriuje pasirinkite **Naujas** dar kartą, kad įtrauktumėte kitą eilutę.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Darbo tipas:** *Padėjimas*
    - **Darbo klasės ID:** *QC patikra*

        Pasirinkite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.

1. Veiksmų srityje pasirinkite **Įrašyti**.

Dėl išsamesnės informacijos apie darbo šablonus,, žr. [Sandėlio darbo valdymas naudojant darbo šablonus ir vietos direktyvas](control-warehouse-location-directives.md).

### <a name="location-directive--quality-failures"></a>Vietos direktyva - Kokybės klaidos

Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas. Pavyzdžiui, prekybos užsakymo perlaidoje, vietos direktyva nulemia, ar elementai bus paimami ir, kur paimti elementai turi būti padėti. Privalote konfigūruoti vietos direktyvos taisyklę, kad nustatytumėte, kaip nepavykusios kokybės patikros bus valdomos.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairiojoje juostoje, nustatykite **Darbo užsakymo tipo** laukelį į *Įsigijimo užsakymai* tam, kad dirbtumėte su to tipo vietos direktyvomis.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte vietos direktyvą kokybės patikroms.
1. Antraštėje nustatykite šias vertes:

    - **Sekos numeris:** Priimkite numatytąją vertę.
    - **Pavadinimas:** *51 į kokybę*

1. „FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes: Priimkite nustatytąsias vertes likusiems laukeliams.

    - **Darbo tipas:** *Padėjimas*
    - **Vieta:** *5*
    - **Sandėlis:** *51*

1. Veiksmų juostoje pasirinkite **Įrašyti** tam, kad įrašytumėte savo direktyvą ir padarytumėte **Eilutes** „FastTab“ prieinamą.
1. „FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes: Priimkite nustatytąsias vertes likusiems laukeliams.

    - **Pradinis kiekis:** *1*
    - **Galutinis kiekis:** *1000000*

1. Veiksmų juostoje pasirinkite **Įrašyti** tam, kad įrašytumėte naują eilutę ir padarytumėte **Vietos direktyvos veiksmą** „FastTab“ prieinamą.
1. Kol nauja eilutę yra dar pasirinkta **Eilutės** „FastTab“, pasirinkite **Naujas** skyriuje **Vietos direktyvos veiksmai** „FastTab“ tam, kad įtrauktumėte eilutę į tinklelį taip, kad galėtumėte nustatyti veiksmą eilutei.
1. Naujoje eilutėje, nustatykite **Pavadinimas** laukelį į *Kokybę*. Priimkite nustatytąsias vertes likusiems laukeliams.
1. Veiksmų juostoje pasirinkite **Įrašyti** tam, kad padarytumėte **Redaguoti užklausą** mygtuką **Vietos direktyvos veiksmų** „FastTab“ prieinamą.
1. Kol jūsų kątik įtraukta eilutė vis dar yra pasirinkta **Vietos direktyvos veiksmuose** „FastTab“, pasirinkite **Redaguoti užklausą** tam, kad atidarytumėte teksto laukelį, kuriame galite redaguoti užklausą veiksmui.
1. **Intervalas** skirtuke, pasirinkite **Įtraukti** tam, kad įtrauktumėte eilutę į užklausą.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Vieta*
    - **Kriterijai:** *QMS*

    *QMS* vieta yra sandėlio vietoje kokybei.

1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Privalote pakeisti įsigijimo užsakymo vietos seką sandėlio direktyvoms *51*. Pasirinkite naują *51 į kokybę* vietos direktyvą, atnaujinkite puslapį ir tuomet pasirinkite vietos direktyvą sąraše. Tuomet naudokite **Judinimo aukštyn** ir **Judinimo žemyn** mygtukus veiksmų juostoje, kad padėtumėte vietos direktyvą sandėliui *51* tokia tvarka. (Prieš pasirinkdami **Judėjimą aukštyn** ar **Judėjimą žemyn**, privalote pasirinkti vietos direktyvą sąraše.)

    1. 51 į kokybę
    2. 51 PO Direct
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Mobiliojo įrenginio meniu elementai

Konfigūruokite meniu elementą taip, kad mobilsu prietaisas galėtų atlikti **Kokybės tikrinimo** funkciją.

#### <a name="purchase-putaway"></a>Įsigijimo atidėjimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sąraše pasirinkite **Įsigijimo atidėjimo** meniu elementą.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Darbo klasės** skyriuje pasirinkite **Naujas** tam, kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Darbo klasės ID:** *QC patikra*

        Įveskite [darbo klasės](#work-class) pavadinimą, kurį sukūrėte anksčiau kokybės kontrolės darbui.

    - **Darbo užsakymo tipas:** *Kokybė kokybės patikroje*

1. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="purchase-order-line-receiving"></a>Gaunama pirkimo užsakymo eilutė

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Meniu elemento pavadinimas:** *PU eilutės gavimas*
    - **Pavadinimas:** *PU eilutės gavimas*
    - **Režimas:** *Darbas*
    - **Naudoti sukurtą darbą:** *Ne*

1. Skirtuke **Bendra** „FastTab“, nustatykite tolesnes reikšmes. Priimkite nustatytąsias vertes likusiems laukeliams.

    - **Darbo sukūrimo procesas:** *Įsigijimo užsakymo linijos gavimas ir atidėjimas*
    - **Generuoti numerio lentelę:** *Taip*
    - **Darbo šablonas:** *51 PO kvitas*

1. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Meniu elemento įtraukimas į mobiliojo įrenginio meniu

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Kairiojoje juostoje, pasirinkite esamą **Vidaus** meniu.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Esami meniu ar meniu elementai** stulpelyje pasirinkite naują **PO eilutės gavimo** meniu elementą.
1. Pasirinkite dešinę rodyklės mygtuką, kad judintumėte **PO leilutės gavimą** į **Meniu struktūros** stulpelį.
1. **Meniu struktūros** stulpelyje pasirinkite **PO eilutės gavimą** ir tuomet pasirinkite rodyklę aukštyn ar žemyn mygtuką tam, kad judintumėte meniu elemntus į norimą padėtį mobilaus prietaiso meniu.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Pavyzdinis scenarijus

Po to, kai atliksite visus anksčiau aprašytus pavyzdžio duomenis esančius ir nustatytus, galite dirbti su šiuo scenarijumis tam, kad bandytumėte *Kokybės tikrinimo* funkciją. Šiame scenarijuje rodomos vertės apima tai, kad jūs dirbate su standartiniais demonstraciniais duomenimis, kuriuos pasirinkote **USMF** teisiniame subjekte ir tai, kad rengiate pavyzdžio įrašus, kurie yra aprašyti anksčiau šiame skyriuje. Scenarijus taip pat naudingas kaip pavyzdys rodantis, kaip funkcija gali būti naudojama gamybos parametruose.

### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:

    - **Tiekėjo paskyra:** *104*
    - **Sandėlis:** *51*

1. Pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį ir atidarytumėte naują įsigijimo užsakymą.
1. **Įsigijimo užsakymo linijos** „FastTab“ tinklelis turi naują, tuščią liniją. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *M9203*
    - **Kiekis:** *3*
    - **Vienetas:** *PL*

1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="process-quality-check-receiving"></a>Proceso kokybės tikrinimo gavimas

Po to, kai įsigijimo užsakymas buvo sukurtas, jis gali būti gaunamas naudojant **PO eilutės gavimo** meniu elementą ir *Kokybės tikrinimo* funkciją.

#### <a name="receive-pallet-1"></a>Gauti padėklą 1

1. Prisijungti prie sandėlio programos kaip sandėlio naudotojas *51*. (Įveskite *51* kaip vartotojo ID ir *1* slaptažodį.)
1. Eikite į **Vidaus \> PO linijos gavimas**.
1. **PONUM** laukelį, įveskite įsigijimo užsakymo numerį.
1. Patvirtinkite įsigijimo užsakymo numerį.
1. **LINENUM** laukelyje įveskite įsigijimo užsakymo eilutės numerį, kuris yra gaunamas. Kadangi užsakymas turi tik vieną eilutę šiame scenarijuje, jūs taip pat įvesite *1* **LINENUM** laukelyje kiekvienam gavimo žingsniui.
1. Patvirtinkite eilutės numerį.
1. **QTY** laukelyje įveskite gaunamą kiekį. Kadangi įsigijimo užsakymas yra trims padėklams (*PL*) šiame scenarijuje ir esama trijų gavimo žingsnių, įvesite *1* **QTY** laukelyje kiekvienam gavimo žingsniui.
1. Patvirtinkite kiekį.

    **Kokybės tikrinimo** puslapis pasirodo neturintis jokių įrašų laukelių. Jis turi tik patvirtinimą (žymimos žymės) mygtuką meniu mygtuko apačioje (**≡**) viršuje. (Meniu mygtukas kartais vadinamas mėsainiu ar mėsainio mygtuku.) Jis skirtas tirti kokybės tikrinimo procesą, kai padėklai praeina kokybės tikrinimą, vartotojas tik patvirtina **Kokybės tikrinimo** puslapį.

    ![Kokybės patikros puslapis](media/quality-check.png "Kokybės patikros puslapis")

1. Pasirinkite patvirtinimo mygtuką, kad jis praeitų kokybės tikrinimą padėklui 1 eilutėje 1.

    **Įsigijimo užsakymai: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:

    - **LOC:** Sistemos nustatyta vieta

        Ši vieta yra nustatyta gaunamo įsigijimo užsakymo atidėjimo vietai.

    - **LP:** Sistema kuria licencijos numerio ID
    - **Prekė:** *M9203*
    - **Kiekis:** *1 PL: 100 ea*

    Rodomas ir elemento aprašas.

1. Patvirtinkite atidėjimo darbą.

    **Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą. **LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.

#### <a name="receive-pallet-2"></a>Gauti padėklą 2

Šiame scenarijuje antras padėklas bus atmestas.

1. **LINENUM** laukelyje, įveskite *1* ir patvirtinkite eilutės numerį.
1. **QTY** laukelis dabar prieinamas. Įveskite *1* ir patvirinkite kiekį.

    **Kokybės patikra** puslapis pasirodo. Dėl šio kvito, padėklas bus atmestas dėl kokybės ir bus padėtas į *QMS* kokybės vietą.

1. Pasirinkite meniu mygtuką (**≡**) puslapio viršuje ir tuomet meniu pasirinkite **Atsisakyti** grįžimui į meniu.
1. **Užduoties** pasirodančiame puslapyje įveskite **QMS** kaip *Padėta* vietoje tam, kad siųstumėte padėklą tolesnei patikrai.

    **Kokybė kokybės patikroje: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:

    - **LOC:** *QMS*

        Ši vieta yra nustatyta gaunamo įsigijamo užsakymo atšauktos kokybės gavimui.

    - **LP:** Sistema kuria licencijos numerio ID
    - **Prekė:** *M9203*
    - **Kiekis:** *1 PL: 100 ea*

    Rodomas ir elemento aprašas.

1. Patvirtinkite atidėjimo darbą.

    **Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą. **LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.

Dabar baigėte kokybės tikrinimą ir sukūrėte kokybės užsakymą atsisakytam padėklui. Tam, kad peržiūrėtumėte sukurtą užsakymą, eikite į **Atsargų valymdas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.

Kokybės užsakymo testavimas dabar gali būti pradėtas. Kokybės testavimas nėra aptariamas šioje temoje.

Dėl išsamesnės informacijos apie kokybės valdymą, žr. [Kokybės valdymo peržiūra](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Gauti padėklą 3

Šiame scenarijuje trečias padėklas bus priimtas.

1. **LINENUM** laukelyje, įveskite *1* ir patvirtinkite eilutės numerį.
1. **QTY** laukelis dabar prieinamas. Įveskite *1* ir patvirinkite kiekį.

    **Kokybės patikra** puslapis pasirodo. Dėl šio kvito, padėklas bus priimtas dėl kokybės ir bus padėtas į nesupakuotų krovinių atidėjimo vietą.

1. Pasirinkite patvirtinimo mygtuką, kad jis praeitų kokybės patikrą.

    **Įsigijimo užsakymai: Padėti** puslapis, kuris rodo informaciją apie paėjimo darbą:

    - **LOC:** Sistemos nustatyta vieta

        Ši vieta yra nustatyta gaunamo įsigijimo užsakymo atidėjimo vietai.

    - **LP:** Sistema kuria licencijos numerio ID
    - **Prekė:** *M9203*
    - **Kiekis:** *1 PL: 100 ea*

    Rodomas ir elemento aprašas.

1. Patvirtinkite atidėjimo darbą.

    **Užduoties** puslapyje įsigijimo užsakymo linijos gavime, matysite „Darbas užbaigtas“ pranešimą. **LINENUM** laukelis yra prieinamas, todėl galite pradėti gauti kitą padėklą.

1. Pasirinkite meniu mygtuką (**≡**) puslapio viršuje ir tuomet meniu pasirinkite **Atšaukti** grįžimui į meniu.

Dabar galite uždaryti mobiliąją programą.
