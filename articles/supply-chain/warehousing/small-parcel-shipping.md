---
title: Mažų siuntinių siuntimas
description: Šioje temoje pateikiama informacija apie mažų siuntinių siuntimo (angl. SPS) funkciją. Ši funkcija leidžia „Microsoft Dynamics 365 Supply Chain Management” pateikti informaciją apie supakuotą konteinerį vežėjui ir gauti siuntimo žymę, siuntimo įkainį ir vežėjo pateiktą sekimo numerį.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e8e2bda39b9de241d17fcf3cb9acce2b8015efd2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687622"
---
# <a name="small-parcel-shipping"></a>Mažų siuntinių siuntimas

[!include [banner](../../includes/banner.md)]

Mažų siuntinių siuntimo (SPS) funkcija leidžia „Microsoft Dynamics 365 Supply Chain Management” sąveikauti su siuntimo vežėjais per vežėjų API susisiekimo sistemą. Ši funkcija naudinga, kai pavienius pardavimo užsakymus siųsite per komercinius vežėjus, o ne rinksitės konteinerio siuntimą, ar ne viso pakrovimo (LTL) siuntimą.

SPS funkcija sąveikauja su jūsų siuntinio vežėju per skirtą *Tarifų mechanizmas*. Jūsų organizacija turi sukurti šį tarifo mechanizmą bendradarbiaujant su jūsų vežėju arba vežėjų centrų tarnyba. Šis tarifų mechanizmas leidžia „Supply Chain Management” pateikti informaciją apie supakuotą konteinerį jūsų vežėjui ir gauti siuntimo etiketę, siuntimo įkainį ir vežėjo pateiktą sekimo numerį.

Grąžintas siuntimo tarifas įtraukiamas į susietą pardavimo užsakymą kaip papildomas mokestis. Grąžintą siuntimo žymę galima automatiškai išspausdinti naudojant „Zebra” programavimo kalbos (ZPK) spausdintuvą ir pritaikyti siuntai. Vežėjas nuskaitys šią siuntimo žymą, kai paima paketus iš jūsų sandėlio.

## <a name="prepare-your-system-to-support-sps"></a>Paruoškite sistemą palaikyti SPS

Prieš pradedant naudotis SPS funkcija, turite įjungti SPS funkciją Funkcijų valdymo dalyje, pridėkite tarifų variklį, ir nustatykite **Transportavimo valdymas** ir **Sandėlio valdymas** modulius jam palaikyti.

### <a name="turn-on-the-sps-feature"></a>SPS funkcijos įjungimas

Prieš naudodami SPS funkciją, turite ją įjungti savo sistemoje. Administratoriai gali naudoti [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną, ir jei būtina, ją įjungtų. Ten ši funkcija pateikiama taip:

- **Modulis:** *Gabenimo valdymas*
- **Funkcijos pavadinimas:** *Mažų siuntinių siuntimas*

### <a name="deploy-and-set-up-rate-engines"></a>Tarifų mechanizmo įdiegimas ir konfigūravimas

„Supply Chain Management” neapima jokių tarifų mechanizmų. Turite įsigyti arba sukurti bet kuriuos tarifų modulius, kurių jums reikia, ir įtraukti juos į savo sistemą. Tačiau „Microsoft” suteikia demonstracinę tarifų mechanizmo versiją, kurią galite naudoti testavimui.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Demonstracinės tarifų mechanizmo versijos atsisiuntimas ir įdiegimas

Norėdami gauti demonstracinę tarifų mechanizmo versiją, atlikite šiuos veiksmus.

1. „GitHub” atsisiųskite [dinaminę saitų biblioteką (angl. DLL), skirtą demonstracinei tarifų mechanizmo versijai](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. „Supply Chain Management” serveryje įrašykite DLL aplanke **\\AOSService\\ PackagesLocalDirectory\\ Application Dll\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Funkcinių tarifų mechanizmų kūrimas ir diegimas

Informacijos apie tai, kaip sukurti ir įdiegti funkcinių tarifų mechanizmus, kad juos būtų galima naudoti gamybos arba tikrinimo aplinkoje, ieškokite šiose temose:

- [Naujo transportavimo valdymo mechanizmo kūrimas](../transportation/create-new-transportation-management-engine.md)
- [Transportavimo valdymo mechanizmų konfigūravimas](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Daugiau informacijos apie tai, kaip sukurti SPS tarifų mechanizmą, rasite šiame tinklaraščio įraše: [Mažų siuntinių siuntimas: kaip pagerinti mažų siuntinių siuntimo funkciją „Microsoft Dynamics 365”](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Tarifų mechanizmo konfigūravimas „Supply Chain Management”

Sukūrę ir įdiegę SPS tarifų mechanizmą, atlikite šiuos veiksmus, norėdami jį nustatyti.

1. Eikite į **Transportavimo valdymas \> Sąranka \> Mechanizmai \> Tarifo mechanizmas**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šiuos laukus:

    - **Vertinimo mechanizmas** – įveskite unikalų tarifo mechanizmo pavadinimą. Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *Demonstracinė tarifo mechanizmo versija*.
    - **Pavadinimas** – įveskite trumpą tarifo mechanizmo aprašą. Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *Demonstracinė tarifo mechanizmo versija*.
    - **Vertinimo metaduomenų ID** – pasirinkite pagrindą, kuris turėtų būti naudojamas skaičiuojant tarifą. Pavyzdžiui, jūsų tarifas gali būti apskaičiuojamas pagal atstumą. Jei naudojate demonstracine tarifo mechanizmo versija, galite palikti šį lauką tuščią.
    - **Mechanizmo rinkinys** – įveskite įdiegto DLL paketo failo pavadinimą. Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *TMSSmallParcelShippingEngine.dll*.
    - **Mechanizmo klasė** – įveskite klasės pavadinimą, kuri buvo sukurta jūsų jūsų tarifo mechanizmui. Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šis pavyzdys rodo, kaip nustatyti ir naudoti SPS, kai jau paruošėte savo sistemą, kaip aprašyta anksčiau šioje temoje. Šiame scenarijuje naudojamas anksčiau minėta demonstracinės tarifo mechanizmo versija.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Norėdami dirbti pagal šį scenarijų, naudojant čia nurodytus demonstracinius įrašus ir vertes, turite būti sistemoje, kurioje įdiegti standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

### <a name="set-up-the-scenario"></a>Scenarijaus nustatymas

Šiame pavyzdyje scenarijuje turite turėti demonstracinį vežėją, vežėjų grupę, pakavimo strategiją ir pakavimo profilį. Šiuose poskyriuose paaiškinama, kaip paruošti įrašus, reikalingus scenarijui. Gamybos scenarijuje nustatymo procesas paprastai yra panašus į čia apibūdintą procesą. Tačiau jūs nustatote skirtingas vertes.

#### <a name="set-up-carriers"></a>Siuntų vežėjų nustatymas

Atlikite šiuos veiksmus vežėjui nustatyti.

1. Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.
1. Veiksmų srityje pasirinkite **Nauja**, norėdami vežėją.
1. Antraštėje nustatykite šias vertes:

    - **Siuntimo vežėjas:** *Demonstracinis vežėjas*
    - **Pavadinimas:** *Demonstracinis vežėjas*
    - **Režimas:** *Žeme*

1. **Peržiūros** „FastTab“, nustatykite šias vertes:

    - **Aktyvuoti siuntimo vežėją:** *Taip*
    - **Aktyvuoti siuntimo vertinimą:** *Taip*

1. „FastTab“ skirtuke **Paslaugos** pasirinkite **Nauja**, kad pridėtumėte paslaugą į tinklelį.
1. Nustatykite šias naujos paslaugos vertes:

    - **Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*
    - **Pavadinimas:** *Demonstracinio vežėjo paslauga*
    - **Transportavimo būdas:** *Žeme*

    Jei reikia, įveskite visų kitų laukų sutartines vertes. (Kai įrašote naują siuntimo vežėjo įrašą, bus sukurtas naujas pristatymo būdas ir **Pristatymo režimas** laukas bus nustatytas automatiškai.)

1. „FastTab“ skirtuke **Vertinimo profiliai** rinkitės **Naujas**, kad sukurtumėte įvertinimų profilį tinkleliui.
1. Nustatykite šias naujo profilio vertes:

    - **Įvertinimo šablonas:** *Demonstracinių vežėjų paslauga*
    - **Pavadinimas:** *Demonstracinio vežėjo paslauga*
    - **Tarifo mechanizmas** *Demonstracinis tarifų mechanizmas*

    Jei reikia, įveskite visų kitų laukų sutartines vertes.

1. Veiksmų srityje pasirinkite **Įrašyti**.

Daugiau informacijos apie tai, kaip nustatyti vežėjus, ieškokite [Siuntimo vežėjų nustatymas](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Vežėjų paslaugų sąskaitų nustatymas

Atlikite šiuos veiksmus, kad sukonfigūruotumėte vežėjo paslaugos sąskaitą.

1. Eikite į **Transportavimo valdymas \> Sąranka \> Įvertinimas \> Vežėjų paslaugos sąskaita**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte vežėjo paslaugos sąskaitą.
1. Nustatykite šias naujos sąskaitos vertes:

    - **Siuntimo vežėjas:** *Demonstracinis vežėjas*
    - **Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*
    - **Vežėjo kliento sąskaitos numeris:** Vežėjo kliento sąskaitos numeris, naudojamas patikrinti ir autentifikuoti ryšį su siuntos vežėju. Jūsų vežėjas teiks šią vertę. Jei naudojate demonstracinę paslaugą, galite įvesti sutartinę vertę.
    - **Vieta:** *6*
    - **Sandėlis:** *62*

    > [!NOTE]
    > Dažnai **Vežėjo kliento sąskaitos numeris** yra vienintelė vertė, reikalinga autentifikuoti ryšį. Tačiau jei jūsų vežėjui reikia papildomų autentifikavimo parametrų, jūsų organizacija turi pritaikyti šį puslapį, kad būtų atitinkamai pridėti papildomi laukai.

#### <a name="set-up-a-container-packing-policy"></a>Konteinerio pakavimo strategijos nustatymas

Norėdami nustatyti konteinerio pakavimo strategiją, atlikite toliau nurodytus veiksmus.

1. Jei dar nenustatėte ZPL spausdintuvo apibrėžimo, norėdami jį nustatyti, naudokite Dokumento maršruto agento programą. Daugiau informacijos žr. [Dokumentų spausdinimo apžvalga](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ir susijusiose temose.
1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Konteineriai \> Konteinerių pakavimo strategijos**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte konteinerio pakavimo strategiją.
1. Naujosios strategijos antraštėje, nustatykite šias vertes:

    - **Konteinerio pakavimo strategija:** *Demonstracinė pakavimo strategija*
    - **Aprašas:** Strategijos aprašas

1. **Peržiūros** „FastTab“, nustatykite šias vertes:

    - **Sandėlis:** *62*
    - **Numatytoji galutinės siuntos vieta:** *Įlankos vartai*
    - **Svorio vienetas:** *kg*
    - **Talpyklos uždarymo politika:** *Automatinis išleidimas*
    - **Konteinerio išleidimo strategija:** *Pasiekiama galutinėje siuntimo vietoje*

1. „FastTab“ **Konteinerio deklaracija** nustatykite šias vertes.

    - **Automatinė deklaracija uždarius konteinerį:** *Taip*
    - **Konteinerio deklaracijos reikalavimai:** *Transportavimo valdymas*
    - **Spausdinti konteinerių turinį:** *Ne*

1. „FastTab“ **Siuntėjo žymos spausdinimas** nustatykite šias vertes.

    - **Spausdinti konteinerio siuntimo žymą:** *Visada*
    - **Spausdintuvo pavadinimas:** ZPL spausdintuvo, kuris turėtų spausdinti siuntimo žymas, pavadinimas

#### <a name="set-up-a-packing-profile"></a>Pakavimo šablono nustatymas

Norėdami nustatyti pakavimo profilį, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte pakavimo profilį į tinklelį.
1. Nustatykite šias naujo profilio vertes:

    - **Pakavimo profilio ID:** *Demonstracinis pakavimo profilis*
    - **Aprašas:** Profilio aprašas
    - **Konteinerio pakavimo strategija:** *Demonstracinė pakavimo strategija*
    - **Talpyklos identifikavimo numerio režimas:** *Automatinis*
    - **Konteinerio tipas:** *Maža dėžutė*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Nustatykite klientą, kad pasirinktumėte SPS vežėją

Norėdami nustatyti klientą, kad jis galėtų pasirinkti jūsų sukurtą vežėją, atlikite šiuos veiksmus.

1. Eikite į **Gautos sąskaitos \> klientai \> Visi klientai**.
1. Tinklelyje suraskite ir pasirinkite *US-027*.
1. Veiksmų srities skirtuko **Bendra** **Nustatyti** pasirinkite **Vežėjo klientų sąskaitos**.
1. Vežėjo **Vežėjo klientų sąskaitos** puslapyje, veiksmų srityje, pasirinkite **Nauja**, kad pridėtumėte sąskaitą tinklelyje.
1. Nustatykite šias naujos sąskaitos vertes:

    - **Siuntimo vežėjas:** *Demonstracinis vežėjas*
    - **Vežėjo kliento sąskaitos numeris:** *12345* (vertė šiame scenarijuje nėra svarbi, tačiau ji bus reikalinga kitame skyriuje.)

### <a name="go-through-the-example-scenario"></a>Pereikite per scenarijaus pavyzdį

Nustatę visus duomenų pavyzdžius, kaip aprašyta ankstesniame skyriuje, esate pasiruošę naudoti pavyzdinį scenarijų.

#### <a name="create-a-sales-order-and-process-the-work"></a>Pardavimo užsakymo sukūrimas ir darbo apdorojimas

Norėdami sukurti pardavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lango **Kurti pardavimo užsakymą** lauke nustatykite **Kliento paskyra** lauką į *US-027*.
1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. „FastTab” skirtuke **Pardavimo užsakymo antraštė** nustatykite lauke **Vežėjo kliento sąskaitos numeris** jūsų anksčiau šiam klientui (*12345*) pasirinktą vertę.
1. Dalyje **Pardavimo užsakymo eilutės** pridėkite pardavimų eilutę ir nustatykite šias vertes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *1*
    - **Vieta:** *6*
    - **Sandėlis:** *62*

1. Perjunkite **Antraštės** rodinį.
1. „FastTab” skirtuke **Pristatymas** nustatykite šias vertes:

    - **Siuntimo vežėjas:** *Demonstracinis vežėjas*
    - **Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*

1. Grįžkite į **Eilučių** rodinį. Jei būsite paraginti atnaujinti pardavimo eilučių pristatymo būdą, pasirinkite **Taip**.
1. Dalyje **Pardavimų užsakymų eilutės** pasirinkite jūsų anksčiau nustatytą užsakymo eilutę ir pasirinkite **Atsargos \> Rezervavimas**.
1. Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Sukurtas darbas, skirtas prekėms iš paėmimo vietos į pakavimo stotį perkelti.

1. Dalyje **Pardavimų užsakymų eilutės** pasirinkite **Sandėlis \> Siuntimo informacija**.
1. **Siuntimo informacija** puslapyje pateikite pastabą apie siuntos ID. Jums jos prireiks, kai pakuosite siuntinį pakavimo stotyje.
1. Uždarykite **Siuntimo informacija** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Pasižymėkite pardavimo užsakymo numerį, tada eikite į **Sandėlio valdymas \>Darbas \> Visi darbai**.
1. Pardavimo užsakymo numerį naudokite surasti ir pasirinkti užsakymui sukurtą darbą.
1. Veiksmų srityje, **Darbas** skirtuke, pasirinkite **Visas darbas**.
1. **Darbo užbaigimas** puslapyje **Vartotojo ID** pasirinkite vartotojo ID. Tada veiksmų srityje pasirinkite **Patvirtinti darbą**.
1. Jei darbas patvirtinamas, veiksmų srityje pasirinkite **Baigti darbą**.

    Darbas pažymimas kaip baigtas, modeliuojant prekių judėjimą į pakavimo stotį.

#### <a name="pack-the-shipment"></a>Siuntos pakavimas

Norėdami supakuoti siuntą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbuotojas** ir įsitikinkite, kad sandėlio valdymui vartotojo paskyra yra susieta su darbuotojo paskyra.
1. Eikite į **Sandėlio valdymas \> Atsiėmimas ir talpinimas į konteinerį \> Pakuoti**.
1. Dialogo lange **Pasirinkite pakavimo stotį** nustatykite šias vertes:

    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Vieta:** *Pakavimas*
    - **Pakavimo profilio ID:** *Demonstracinis pakavimo profilis*

1. Pasirinkite **Gerai**.
1. Pasirodo puslapis **Pakuoti**. Gamybos scenarijuje darbuotojas nuskaitys numerio lentelę arba siuntos ID. Tačiau šiam scenarijui atidarykite **Visos siuntos** puslapį ir suraskite jūsų sukurtos siuntos numerį. Tada įveskite šią vertę lauke **Numerio lentelė arba siunta** **Pakuoti** puslapyje. Kitu atveju įveskite anksčiau pasižymėtos siuntos ID.
1. Veiksmų juostoje pasirinkite **Naujas talpykla**.
1. Dialogo lange rodoma išsami informacija apie naują konteinerį. Palikite numatytąsias reikšmes, tada pasirinkite **Gerai**.
1. **Pakuoti** puslapyje **Prekės pakavimas** „FastTab” skirtuke pasirinkite **Identifikatorius** lauką, pasirinkite *A0002*, kad supakuotumėte prekę. Prekė pridėta į konteinerį.
1. Veiksmų srityje pasirinkite **Konteineriai siuntai**.

    Pasirodžiusiame **Konteineriai siuntai** puslapyje pateikiama jūsų sukurta eilutė. Tačiau **Konteinerių deklaracijos ID** laukas eilutėje šiuo metu yra tuščias, nes negavote siuntimo žymos ir sekimo numerio iš vežėjo.

1. Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.
1. Dialogo lange **Uždaryti konteinerį** nustatykite **Bruto svoris** lauką į *1 kg* ir pasirinkite **Gerai**.

    Siuntimo žymė dabar turi būti išspausdinta ant anksčiau pasirinkto ZPL spausdintuvo. Ji turi atitikti šį pavyzdį.

    ![Siuntimo žymės pavyzdys.](media/sps-label-example.png "Siuntimo žymės pavyzdys")

1. Atkreipkite dėmesį, kad **Konteinerio deklaracijos ID** ir **Bendras krovinys** vertės pridėtos tokios, kokios gautos iš vežėjo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]