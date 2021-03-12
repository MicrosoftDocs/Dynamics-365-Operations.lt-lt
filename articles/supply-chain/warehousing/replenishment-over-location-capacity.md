---
title: Papildymas pagal vietos erdvę
description: Šioje temoje pateikiama informacija apie vietos pajėgumo papildymo funkciją. Ši funkcija įjungia visus papildymo darbus, kurių bus reikalaujama kūrimo dieną ir valdo papildymo darbo prieinamumą siekiant užtikrinti, kad paėmimo vieta neišeis iš atsargų ir neviršys pajėgumo.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3f94053920b475ef9190b5ac65a5f9ca01dcd4a1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996128"
---
# <a name="replenishment-over-location-capacity"></a>Papildymas pagal vietos erdvę

[!include [banner](../includes/banner.md)]

Kai kurie didelės apimties ar erdvėje apriboti sandėliai privalo išsiųsti daugiau elemento kiekio per dieną nei telpa paėmimo vietoje. *Vietos pajėgumo papildymo* funkcija įjungia visus papildymo darbus, kurių bus reikalaujama kūrimo dieną ir valdo papildymo darbo prieinamumą siekiant užtikrinti, kad paėmimo vieta neišeis iš atsargų ir neviršys pajėgumo.

Ši funkcija įjungia daugiau papildymo darbo, kuris bus sukuriamas nei telpa vietoje ir užblokuoja papildymo darbą nuo jo pabaigos, kai vieta yra pilna. Kadangi atsargos paėmimo vietoje nukrenta žemiau konfigūruojamo slenksčio, didesnis papildymo darbas yra prieinamas.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Įjungti vietos pajėgumo papildymo darbo funkciją

Tam, kad šioje temoje aprašyta funkcija būtų prieinama jūsų sistemoje, įjunkite tolesnes funkcijas [Funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)(tokia tvarka):

1. Darbo blokavimas organizacijos mastu
1. Papildymas pagal vietos erdvę

## <a name="set-up-the-feature-for-the-example-scenario"></a>Nustatykite funkciją pavyzdiniam scenarijui

Šis skyrius aprašo gaires ir pavyzdį, kuris rodo, kaip nustatyti šią funkciją ir paruošti pavyzdinius duomenis pavyzdiniam scenarijui, kuris pateiktas vėliau šiame skyriuje.

### <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Tam, kad dirbtumėte su [pavyzdiniu scenarijumi](#example-scenario) naudodami pavyzdinius įrašus ir vertes nurodytas čia, turite būti sistemoje, kurioje standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yra įdiegti. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

### <a name="location-profile"></a>Vietos profilis

Įjungti vietos pajėgumo papildymo funkciją vietos profilyje.

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Sandėlis \> Vietos profiliai**.
1. Kairėje juostoje, pasirinkite **PICK-06**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Skirtuke **Papildymas** „FastTab“, nustatykite tolesnes reikšmes:

    - **Viršytas vietos pajėgumas:** *Taip*

        Įjungus papildymo darbui leidžiama viršyti maksimalius vietos pajėgumus. Tai taip pat įjungia kitus laukelius **Papildymo** „FastTab“.

    - **Darbo prieinamumo slenksčio tipas:** *Kiekis*

        Šis laukelis nustato metodą, kuris naudojamas nustatyti, kai daugiau darbo turi būti paleidžiama. Galite paleisti bet kurį kiekį ar procentą:

        - *Procentas* – Pasirinkite šią parinktį tam, kad naudotumėte procentų pajėgumą pagrįstą atsargų limitais ir apimtimis. Pasirenkant šią parinktį įjungiamas **Per didelio srauto procentai** laukelis ir išjungiami du su kiekiai susiję laukeliai  **Per didelio srauto kiekis** ir **Per didelio srauto padalinys**.

            Galite naudoti šią parinktį, jei paėmimo vietos naudoja apimtis.

            Jei ši parinktis yra pasirinkta, nustatykite **Per didelio srauto procento** laukelį į procentą, kuriame daugiau papildomo darbo yra prieinama.

        - *Kokybė* – Pasirinkite šią parinktį, kad naudotumėte konkrečią kiekio vertę. Pasirenkant šią parinktį išjungiamas **Per didelio srauto procentai** laukelis ir įjungiami **Per didelis kiekis** ir **Per didelio srauto padalinys** laukeliai.

            Naudokite šią parinktį, kai nenaudojate tūrio vietose, kurios yra papildomos arba kai turite nuolatinius kiekius, kuriuose norite, kad daugiau atsargų būtų atvesta į vietą.

           Jei ši parinktis pasirinkta, nustatykite **Per didelio srauto kiekį** ir **Per didelio srauto padalinio** laukelius ir padalinį, kuriame daugiau papildomo darbo yra prieinama.

    - **Perpildos kiekis:** *0.65*

        Šis laukelis nustato kiekį, kuriuo vieta yra perpildyta.

        Darbas bus prieinamas bet kada, kai turimo kiekio suma vietoje ir darbo kiekis yra žemesnis nei ši vertė. Visi darbo papildymai viršijantys šią vertę bus blokuojami ir turės būti atblokuojami rankiniu būdu.

        Vietos laikymo limitai yra vertinami, kai darbo kiekis yra apskaičiuojamas.

    - **Perpildos padalinys:** *PL*

        Šis laukelis nustato padalinį, kuris yra susietas su perpildos kiekiu.

        Tokiu atveju, daugiau papildomo darbo bus prieinama, kai vieta sumažėja iki 0,65 padėklo (PL).

    - **Perpildos procentas**

        Šis laukelis nustato procentą, kuriuo vieta yra perpildyta.

        Darbas bus prieinamas bet kada, kai turimo kiekio suma vietoje ir darbo kiekis yra žemesnis nei šis procentas. Visi darbo kiekio procento papildymai viršijantys šią vertę bus blokuojami ir turės būti atblokuojami rankiniu būdu.

        Vietos laikymo limitai yra vertinami, kai darbo kiekio procentas yra apskaičiuojamas. Jei nėra nustatytų jokių vietos talpinimo limitų, darbo kiekio procentas bus skaičiuojamas pagal pajėgumą, jei pajėgumo apribojimai yra nustatyti vietos profilyje.

> [!IMPORTANT]
> Jei naudojate demonstracinius duomenis **USMF** teisinis subjektas ir anksčiau įjungta *Vietos licencijos ženklo padėties* funkcija, turite būti išjungę **Įjungto licencijos ženklo vietos** nustatymus **BULK-06** vietos profiliui tam, kad būtų užbaigti mobilūs žingsniai šiame pavyzdiniame scenarijuje.

### <a name="wave-step-code"></a>Bangos veiksmo kodas

> [!NOTE]
> Tam, kad nustatytumėte čia aprašytą bangos žingsnio kodą, pirmiausia jums reikia naudoti [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte funkciją pavadintą *Organizacijos pločio bangos žingsnio kodas*.

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Bangos \> Bangos žingsnio kodas**.
1. Pasirinkite **Naujas** ir nustatykite tolesnes reikšmes:

    - **Bangos veiksmo kodai:** *Papildyti*
    - **Bangos žingsnio aprašas:** *Papildymas*
    - **Bangos žingsnio tipas:** *Papildymas*

1. Pasirinkite **Įrašyti**.

### <a name="replenishment-template"></a>Papildymo šablonas

Papildymo šablonai yra taisyklių rinkiniai, valdantys kada ir kaip vieta yra papildoma.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Peržiūros** skyriuje pasirinkite eilutę, kurioje **Papildymo šablono** laukelis yra nustatytas į *Papildymo poreikis*.
1. Nustatykite toliau nurodytas reikšmes.

    - **Bangos veiksmo kodai:** *Papildyti*
    - **Leisti bangai reikalauti naudoti nerezervuotus kiekius:** *Taip*

1. Pasirinkite **Įrašyti**.

### <a name="wave-template"></a>Bangos šablonas

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Kairiojoje juostoje nustatykite **Bangos šablono tipo** laukelį į *Siuntimas*.
1. Pasirinkite šabloną **61 siuntimas** sąraše.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. **Bendras** „FastTab“, nustatykite **Automatizuoti papildymo darbo leidimo** parinktį į *Taip*.

    Nustatykite šią parinktį į *Taip* tam, kad sukurtumėte užklausa pagrįstą papildymo darbą ir automatiškai jį išleistumėte. Privalote įtraukti papildymo bangos metodą į bangos šabloną ir sukurti **Bangos poreikio** papildymo šablono tipą. Nustatykite papildymo šabloną **Papildymo šablonų** puslapyje. Tam, kad nustatytumėte papildymo šabloną, privalote įtraukti papildymo metodą į bangos šabloną.

1. **Metodai** „FastTab“ **Pasirinkti metodai** stulpelyje suraskite šią eilutę:

    - **Metodo pavadinimas** *papildymas*
    - **Pavadinimas** *Papildymas*

1. Nustatykite **Bangos žingsnio kodo** laukelį šiai linijai į *Pildyti*.
1. Pasirinkite **Įrašyti**.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Po to, kai atliksite visus anksčiau aprašytus pavyzdžio duomenis esančius ir nustatytus, galite dirbti su šiuo scenarijumis tam, kad bandytumėte *Vietos pajėgumo papildymo* funkciją. Šiame scenarijuje rodomos vertės apima tai, kad jūs dirbate su standartiniais demonstraciniais duomenimis, kuriuos pasirinkote **USMF** teisiniame subjekte ir tai, kad rengiate pavyzdžio įrašus, kurie yra aprašyti anksčiau šiame skyriuje. Scenarijus taip pat naudingas kaip pavyzdys rodantis, kaip funkcija gali būti naudojama gamybos parametruose.

### <a name="create-replenishment-work"></a>Kurti papildymo darbą

#### <a name="create-sales-order-1"></a>Pardavimo užsakymo 1 sukūrimas

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.
1. Dialogo lange nustatykite šias vertes:

    - **Kliento sąskaita:** *US-007*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *T0100*
    - **Kiekis:** *40*

1. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.
1. Uždarykite puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti. Sukuriama ir papildymo banga.

    Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“

#### <a name="create-sales-order-2"></a>Pardavimo užsakymo 2 sukūrimas

1. **Visų prekybos užsakymų** lange, veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.
1. Teksto laukelyje nustatykite šią vertę:

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *T0100*
    - **Kiekis:** *60*

1. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.
1. Uždarykite puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti. Sukuriama ir papildymo banga.

    Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“

#### <a name="create-sales-order-3"></a>Pardavimo užsakymo 3 sukūrimas

1. **Visų prekybos užsakymų** puslapyje, veiksmų juostoje pasirinkite **Naujas** tam, kad atidarytumėte teksto laukelį naujo prekybos užsakymo sukūrimui.
1. Dialogo lange nustatykite šias vertes:

    - **Kliento sąskaita:** *US-004*
    - **Sandėlis:** *61*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima naują, tuščią liniją **Prekybos užsakymo eilučių** „FastTab“. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *T0100*
    - **Kiekis:** *30*

1. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.
1. Uždarykite puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Gausite informacinį pranešimą, kuris rodo, kad bangos ir siuntimo ID buvo sukurti. Sukuriama ir papildymo banga.

    Taip pat gausite įspėjimą, kuris sako „Darbo ID XXX negali būti atblokuotas, nes nepabaigtas papildymo darbas.“

#### <a name="view-work-details"></a>Peržiūrėti išsamią darbo informaciją

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. **Peržiūros** skyriuje filtruokite **Sandėlio** stulpelį sandėliui *61*.
1. Turėtumėte matyti, kad septynių darbų ID buvo sukurti trims prekybos užsakymų reikalavimams.

    - Tris iš septynių darbo ID turi **Darbo užsakymo tipo** vertę *Papildymas*, o keturi turi **Darbo užsakymo tipo** vertę *Prekybos užsakymai*.
    - Visi trys darbo ID turintys **Darbo užsakymo tipo** vertę *Papildymas* turi tas pačias *Paėmimo* ir *Padėjimo* vietas **Eilučių** skyriuje:

        - **Paimti:** *02A01R5S1B*
        - **Padėti:** *06A01R2S1B*

    - Du darbo ID buso sukurti prekybos užsakymui 1.

1. Atkreipkite dėmesį į darbo ID prekybos užsakymuose.

Priklausomai nuo turimų kiekių, sukurti darbo kiekiai gali nežymiai skiris. Nepaisant to, bendros sukurtos darbo antraštės turėtų atitikti šį scenarijaus pavyzdį.

#### <a name="on-hand-inventory-license-plate-id"></a>Turimų atsargų licencijos numerio ID

Vėliau šiame scenarijuje naudosite sandėlio programą (ar emuliatorių), kuriame turėsite nustatyti licencijos numerį tam, kad pabaigtumėte paėmimą ir papildymo scenarijus.

Tam, kad rastumėte vėliau jums reikalingų licencijos numerių ID, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas**.
1. Pasirinkite **Rodyti filtrus** mygtuką, kad atidarytumėte filtro juostą,
1. Įveskite tolesnius filtravimo kriterijus, kad gautumėte licencijos numerius šiam scenarijui. Naudokite *pradžias su* filtru.

    - **Prekės numeris:** *T0100*
    - **Sandėlis:** *61*

1. Pasirinkite **Taikyti**.
1. Veiksmų juostoje, pasirinkite **Dimensijos**.
1. **Dimensijos rodymo** teksto laukelyje,**Saugojimo dimensijos** skyriuje pasirinkite visas vertes.
1. **Perlaidos** skyriuje pasirinkite **Elemento numerį** ir **Kiekį \<\> 0**.
1. Kai pabaigsite pasirinkite **Gerai** tam, kad uždarytumėte teksto laukelį.
1. **Turimas** tinklelis rodo licencijos numerio numerius elementui *T0100* kiekvienoje vietoje. Atkreipkite dėmesį į licencijos numerį esantį kiekvienoje vietoje, nes jums šios informacijos reikės vėliau.
1. Uždarykite puslapį.

### <a name="process-steps"></a>Proceso veiksmai

Atliksite sandėlio vietos papildymą pirmiems dviems darbo ID. Dirbas su trečiuoju papildymo darbu bus užblokuotas, kol atsargų lygis paėmimo vietoje nukris žemiau slenksčio.

#### <a name="replenishment"></a>Papildymas

1. Prisijungti prie sandėlio programos kaip naudotojas sandėlyje *61*. (Įveskite *61* kaip vartotojo ID ir *1* slaptažodį.)
1. Eikite į **Atsargos \> Papildymas**.

    Esate paskatintas pabaigti pirmąjį papildymo darbą. Rodomi elemento numeris, kiekis ir paėmimo vieta.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.
1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).

    Sistema sukuria licencijos numerio numerį paimto elemento naujam licencijos numeriui.

1. Pasirinkite **Gerai** vertės patvirtinimui.

    Rodomas paėmimo darbas, kuris naudotojui rodo padėti galutinį licencijos numerį į papildymo vietą. *Padėjimo* vieta turi būti **06A01R2S1B**.

1. Patvirtinkite padėjimo informaciją ir pasirinkite **Gerai**.

    Gausite „Darbas baigtas“ pranešimą ir yra rodoma informacija apie kitą paėmimo papildymo darbą: elemento numeris, kiekis ir vieta, iš kurios paimama. Paėmimo vieta bus ta pati, kaip pirmoji papildymo vieta. Dėl to, licencijos numeris turės tą patį licencijos numerio ID, kuris buvo naudojamas pirmajai papildymo darbo užduočiai.

1. Pakartokite ankstesnius žingsnius tam, kad užbaigtumėte papildymo darbą antrajai darbo užduočiai. Kiekio ir gaultinis licencijos numeris skirsis nuo kiekio ir galutinio licencijos numerio pirmajai darbo užduočiai.

Pabaigus antrąjį papildymo darbą, gausite „Darbas baigtas“ pranešimą. Mobilus prietaisas taip pat informuos, kad nėra jokio prieinamo darbo, nors keletas papildomų darbų išliks. Tokia seka atsitinka, nes papildymo darbas turi prieinamumo *Sulaikymo* statusą ir yra pažymėtas kaip **Blokuojamas**.

*Laikomas* statusas buvo paleistas, nes vietos profilis paėmimo vietoje, kurioje darbas buvo priskirtas, turi **Kiekio perviršio** vertę *0,65 PL*. Dvi ankstesnės papildymo darbo užduotys užpildytos vietoje beveiki iki perviršio limito elementui *T0100*. (Padalinio pavertimas elementui *1 PL = 100 ea*.) Dėl to, likęs papildymo darbas viršys vietos perviršio limitą.

Kol pakankamai atsargų yra paimta iš vietos tam, kad būtų pristatytas tolesnis darbo paleidimo slenkstis mobilaus prietaiso meniu elemente, šis papildymo darbas liks užblokuotas.

#### <a name="sales-order-pick"></a>Prekybos užsakymo paėmimas

Prieš likusios papildymo darbo užduoties užbaigimą, paėmimo vieta turi būti atsargoms priskirta lygmeniu, kuriame likęs papildymo darbas gali būti atblokuotas. Kitaip tariant, turimų atsargų suma vietoje ir papildymo kiekis negali viršyti **Perviršio kiekio** vertės. Kai suma yra mažesnė nei perviršio kiekis, likęs papildymo darbas bus atblokuotas.

1. Prisijungti prie sandėlio programos kaip naudotojas sandėlyje *61*. (Įveskite *61* kaip vartotojo ID ir *1* slaptažodį.)
1. Eikite į **Išorė \> Prekybos paėmimas**.
1. Įveskite pirmojo darbo ID prekybos užsakymui 1.

    Žiūrėkite darbo ID prekybos užsakymuose, kuriuos anksčiau užsirašėte **Darbo informacijos** puslapyje. Darbo ID, kurį įvedėte čia, sukurs 10 ea kiekio paėmimo darbą iš dviejų atskirų vietų.

1. Pasirinkite **Gerai**.

    **Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą pirmajai vietai.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.
1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).

    **Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.
1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).

    **Prekybos užsakymai: Padėjimas** puslapis rodo jums, kad turite atidėti abu pabaigtus paėmimo darbus į išorės etapo vietą.

1. Pasirinkite **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

1. Įveskite antrojo darbo ID prekybos užsakymui 1.

    Yra tik viena paėmimo užduotis šio darbo ID.

1. Pasirinkite **Gerai**.

    **Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.

    Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduočių. Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.

1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).
1. Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.
1. Pasirinkite **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

Prekybos užsakymas 2 yra užblokuotas dėl paėmimo, nes su juo susieta papildymo užduotis nėra baigta. Šiuo metu dar nėra 30 ea kiekio paėmimo vietoje ir papildymo kiekis prekybos užsakymui 2 yra 60 ea. Turimų atsargų suma ir papildymo atsargos (90 ea) viršija perviršio kiekį 0,65 PL (arba 65 ea). Prieš tai, kai papildymo darbas bus užbaigtas, prekybos užsakymas 3 turi būti paimtas.

1. Įveskite pirmojo darbo ID prekybos užsakymui 3.

    Yra tik viena paėmimo užduotis šio darbo ID.

1. Pasirinkite **Gerai**.

    **Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.

    Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduočių. Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.

1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).
1. Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.
1. Pasirinkite **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

Kai tik turimų atsargų kiekio paėmimo vietoje ir papildymo suma yra žemiau slenksčio, jūs galėsite apdoroti likusį papildymo darbą.

Grįžkite į **Darbo išsamios informacijos** puslapį ir atkreipkite dėmesį, kad papildymo darbo prieinamumas galutinei papildymo daliai (prekybos užsakymui 2) yra *Atviras*, nes dabar yra pakankamai vietos vietoje, kad ji priimtų papildymą.

Galite apdoroti šį papildymo darbą per mobilųjį įrenginį.

1. Eikite į **Atsargos \> Papildymas**.

    Esate paskatintas pabaigti likusį papildymo darbą. Rodomi elemento numeris, kiekis ir paėmimo vieta.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.
1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).

    Sistema sukuria licencijos numerio numerį paimto elemento naujam licencijos numeriui.

1. Pasirinkite **Gerai** vertės patvirtinimui.

    Rodomas paėmimo darbas, kuris naudotojui rodo padėti galutinį licencijos numerį į papildymo vietą. *Padėjimo* vieta turi būti **06A01R2S1B**.

1. Patvirtinkite padėjimo informaciją ir pasirinkite **Gerai**.

    Gausite „Darbas baigtas“ ir „Nėra esamo darbo“ pranešimus.

Dabar galite paimti prekybos užsakymą 2. Jis taps atblokuotas, kai papildymo darbas bus susietas su pabaigtu prekybos užsakymu.

1. Įveskite pirmojo darbo ID prekybos užsakymui 2.

    Yra tik viena paėmimo užduotis šio darbo ID.

1. Pasirinkite **Gerai**.

    **Prekybos užsakymai: Paėmimas** užduoties puslapis rodo elemento numerį, kiekį ir paėmimo vietą kitai vietai.

1. **LP** laukelyje įveskite licencijos numerį elementui vietoje, kuris yra rodomas.

    Licencijos numeris, kurį nurodėte bus sistemos sukurtas licencijos numeris iš papildymo darbo užduoties. Tam, kad įsitikintumėte, jog apėmėte tinkamą licencijos numerio ID, patikrinkite inventorių **Turimo sąrašo** puslapyje elementui, vietai ir kiekiui.

1. Pasirinkite **Gerai** mygtuką (pažymint simbolį).
1. Patvirtinkite instrukcija dėl padėjimo užduoties į išorės etapo vietą.
1. Pasirinkite **Gerai**.

    Gaunate Pabaigtas darbas pranešimą.

## <a name="notes-and-tips"></a>Pastabos ir patarimai

- Ši funkcija veikia su visais papildymo tipais: bangos poreikiu, min./maks., apkrovos poreikiu ir vietos priskyrimu.
- Galite rankiniu būdu viršyti papildymo darbo prieinamumą kiekvienai darbo antraštei iš norimo **Darbo informacijos** puslapio.
- Kai sistema nustato papildymo darbo prieinamumą, ji svarsto visas atsargas, kurios jau yra vietoje prieš pabaigiant darbą
- Kiekvienas prekybos užsakymo elementas yra susiejamas su konkrečiu papildymo darbu. Nėra jokių atitinkamų prekybos užsakymo darbo prieinamumo funkcijų.
