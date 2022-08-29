---
title: Elektroninių ataskaitų konfigūracijų tinkinimas elektroniniam dokumentui generuoti
description: Šiame straipsnyje paaiškinama, kaip pritaikyti "Microsoft" elektroninių ataskaitų (ER) konfigūracijas, naudojamas norint sugeneruoti pasirinktinį elektroninį dokumentą.
author: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: cd3200bea07d622632dc5781638ec825c21233e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278953"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Elektroninių ataskaitų konfigūracijų tinkinimas elektroniniam dokumentui generuoti

[!include[banner](../includes/banner.md)]

Elektroninių [ataskaitų (ER) sistema leidžia](general-electronic-reporting.md) įkelti ER [konfigūracijas](general-electronic-reporting.md#Configuration), kurias Microsoft teikia į Microsoft Dynamics savo 365 finansų egzempliorių. Tokiu būdu „Microsoft” pateiktos konfigūracijos gali veikti kaip ER sprendimas, naudojamas elektroninėms kliento SF (el. SF) generuoti. Ši ER sprendimą galite naudoti jūsų pasirinktiniam ER sprendimui konfigūruoti, norėdami pasiekti jūsų pasirinktinius duomenų bazės laukus ir sugeneruoti el. SF, atitinkančias jūsų konkrečius reikalavimus, neredaguodami šaltinio kodo.

## <a name="overview"></a>Apžvalga

Pavyzdžiui, šiame straipsnyje kaip kiekvieno kliento, kuriam išrašote sąskaitą faktūrą, federalinių mokesčių identifikavimo kodą turite nurodyti kaip naują pasirinktinį atributą. Todėl turite tinkinti dabar naudojamos SF struktūrą įtraukdami naują elementą, kuris kiekvienoje sugeneruotoje el. SF turi būti užpildytas mokesčio kodu.

Šio straipsnio procedūros paaiškina, kaip sistemos administratoriaus, elektroninių ataskaitų kūrėjo arba elektroninio ataskaitų funkcinės konsultanto vaidmens vartotojas gali atlikti šias užduotis jūsų finansų egzemplioriuje:

- [Konfigūruoti minimalų ER parametrų, kurių reikia norint pradėti naudoti ER sistemą, rinkinį](#ConfigureER).
- [Importuoti pradines standartinių ER konfigūracijų versijas, pateiktas el. SF generuoti](#ImportERConfigurations1).
- [Konfigūruoti gautinų sumų parametrus norint pradėti naudoti standartines ER konfigūracijas](#ConfigureAR1).
- [Konfigūruoti juridinio subjekto parametrus norint išrašyti SF klientams](#ConfigureLE).
- [Paruošti kliento įrašą elektroninių SF išrašymui](#ConfigureCustomer1).
- [Įtraukti, registruoti ir siųsti kliento SF naudojant standartines ER konfigūracijas](#ProcessInvoice1).
- [Įtraukti pasirinktinį duomenų bazės lauką norint valdyti klientų federalinių mokesčių identifikavimo kodą](#AddCustomField).
- [Atnaujinti ER metaduomenis norint įgalinti ER modelio susiejimo dizaino įrankio duomenų bazės keitimus](#RefreshERMetadata).
- [Kurti pasirinktines ER konfigūracijas norint generuoti el. SF, kuriose yra naujas mokesčio kodas](#DesignCustomERConfigurations).
- [Konfigūruoti gautinų sumų parametrus norint pradėti naudoti pasirinktines ER konfigūracijas](#ConfigureAR2).
- [Atnaujinti kliento įrašą elektroninių SF išrašymui](#ConfigureCustomer2).
- [Įtraukti, registruoti ir siųsti kliento SF naudojant pasirinktines ER konfigūracijas](#ProcessInvoice2).
- [Importuoti naujas standartinių ER konfigūracijų versijas, pateiktas el. SF generuoti](#ImportERConfigurations2).
- [Patvirtinti naujų standartinių ER konfigūracijų versijų keitimus jūsų pasirinktinėse ER konfigūracijose](#RebaseCustomERConfigurations).
- [Įtraukti, registruoti ir siųsti kliento SF naudojant naujas pasirinktinių ER konfigūracijų versijas](#ProcessInvoice3).

Visas šias procedūras galima užbaigti **DEMF** įmonėje.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>ER sistemos konfigūracija

Jei esate elektroninių ataskaitų funkcinio konsultanto ar elektroninių ataskaitų kūrėjo vaidmens vartotojas, turite sukonfigūruoti minimalų ER parametrų rinkinį. Tada galėsite pradėti naudoti ER sistemą, norėdami kurti pasirinktines standartinių ER sprendimo, naudojamo el. SF generuoti, konfigūracijų versijas.

### <a name="configure-er-parameters"></a>ER parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Skirtuko Lokalizavimas mėlyno **spausdinimo puslapyje, skyriuje Susiję** saitai **, pasirinkite Elektroninių** ataskaitų parametrus **.**
3. **Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.
4. Skirtuko **Priedai** lauke **Konfigūracijos** pasirinkite **Failas**.
5. **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.

Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>ER konfigūracijos tiekėjo aktyvavimas

Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui. ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui. Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.

> [!NOTE]
> Tik ER konfigūracijos savininkas gali redaguoti. Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.

#### <a name="review-the-list-of-er-configuration-providers"></a>ER konfigūracijos teikėjų sąrašo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Lokalizavimo **mėlyno spausdinimo** puslapio skyriuje Susiję **saitai** pasirinkite Konfigūracijos **teikėjai**.
3. **Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį. Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Pridėkite naują ER konfigūracijos tiekėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Lokalizavimo **mėlyno spausdinimo** puslapio skyriuje Susiję **saitai** pasirinkite Konfigūracijos **teikėjai**.
3. **Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.
4. Lauke **Pavadinimas** įveskite **Litware, Inc.**
5. **Internetinis adresas** lauke įveskite `https://www.litware.com`.
6. Pasirinkite **Įrašyti**.

#### <a name="activate-an-er-configuration-provider"></a>ER konfigūracijos tiekėjo aktyvavimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Konfigūracijos teikėjų **skyriaus lokalizavimo** mėlyno **atspaudo** puslapyje pasirinkite Litware, **Inc.** išklotinė dalį, tada pasirinkite **Nustatyti aktyvų**.

Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Pradinių standartinių ER konfigūracijų versijų importavimas

Norėdami įtraukti standartines ER konfigūracijas į dabartinį „Finance” egzempliorių, turite importuoti jas iš ER [saugyklos](general-electronic-reporting.md#Repository), sukonfigūruotos tam egzemplioriui.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Puslapyje Lokalizavimas **,** **konfigūracijos** teikėjų skyriuje, **pasirinkite "Microsoft**" išklotąją dalį, tada pasirinkite Saugyklos, **kad** būtų rodomas "Microsoft" teikėjo saugyklų sąrašas.
3. Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**. Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.
4. Puslapio **Konfigūracijos saugykla** kairiosios srities konfigūracijos medyje pasirinkite formato konfigūraciją **PEPPOL pardavimo SF**.
5. Sparčiajame skirtuke **Versijos** paspauskite **11.2.2**.
6. Pasirinkite **Importuoti**, norėdami atsisiųsti pasirinktą versiją iš bendrosios saugyklos.

![Konfigūracijos saugyklos puslapis.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Jei kyla problemų prisijungiant prie [Bendrosios saugyklos ](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš „Microsoft Dynamics Lifecycle Services (LCS)”.

### <a name="review-the-imported-er-configurations"></a>Importuotų ER konfigūracijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Konfigūracijos skyriaus lokalizavimo** mėlyno **spausdinimo puslapyje** pasirinkite ataskaitų konfigūracijų **išklotines** dalis.
3. Puslapyje **Konfigūracijos** išplėskite „FastTab” **Konfigūracijos komponentai**.
4. Kairiosios srities konfigūracijos medyje išplėskite **SF modelis**, tada – **UBL pardavimo SF**.

Atkreipkite dėmesį, kad kartu su pasirinktu ER formatu **PEPPOL pardavimo SF** buvo importuotos kitos būtinos ER konfigūracijos. Kadangi naujos ER konfigūracijų versijos nuolat publikuojamos bendrojoje saugykloje ir LCS, kad atitinkami sprendimai atitiktų naujus reikalavimus, buvo importuotos naujausios reikiamo duomenų modelio konfigūracijos versijos ir jo modelio susiejimo konfigūracijos.

![Puslapis Konfigūracijos.](./media/er-quick-start3-imported-solution1a.png)

Norėdami modeliuoti būseną, kurią turėtų ER konfigūracijos dabartiniame „Finance” egzemplioriuje, jei importavote ER formato **PEPPOL pardavimo SF** **11.2.2** versiją anksčiau (pavyzdžiui, 2019 m. rugpjūčio 7 d.), atlikite toliau pateiktus veiksmus.

- Veiksmų srityje pasirinkite **Naikinti**, norėdami panaikinti visas ER konfigūracijas, publikuotas po 2019 m. rugpjūčio 7 d. Turi būti paliktos tik konfigūracijos **SF modelis**, **SF modelio susiejimas** (iš pradžių pavadinta **Kliento SF modelio susiejimas**), **UBL pardavimo SF** and **PEPPOL pardavimo SF**.
- Likusių konfigūracijų „FastTab” **Versijos** pasirinkite **Naikinti**, norėdami panaikinti visas ER konfigūracijų, publikuotų po 2019 m. rugpjūčio 7 d., versijas.

Tada patikrinkite, ar toliau pateiktos konfigūracijos prieinamos konfigūracijos medyje.

- ER duomenų modelio konfigūracija **SF modelis** (iš pradžių pavadinta **Kliento SF modelis**):

    - 11 versijoje yra duomenų modelio ER komponento 10 versija, nurodanti SF išrašymo verslo domeno duomenų struktūrą. Ši ER konfigūracija buvo importuota kaip importuoti pasirinkto ER formato **PEPPOL pardavimo SF** aukštesnio lygmens elementas.
    - 50 versijoje yra duomenų modelio ER komponento 31 versija. Ši ER konfigūracija buvo importuota kaip ER modelio susiejimo konfigūracijos **SF modelio susiejimas** 2019 m. rugpjūčio 7 d. versijos aukštesnio lygmens elementas.

    ![ER duomenų modelio konfigūracija SF modelis puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Jei nematote šio duomenų modelio 50 versijos, atidarykite bendrąją saugyklą ir importuokite ER konfigūracijos **SF modelio susiejimas** 50.19 versiją.

- ER modelio konfigūracija **SF modelio susiejimas** (iš pradžių pavadinta **Kliento SF modelio susiejimas**):

    - 50.19 versija buvo importuota kaip naujausias ER duomenų modelio konfigūracijos **SF modelis** 50 versijos diegimas. Joje yra du modelio susiejimo ER komponentai, aprašantys, kaip duomenų modelis užpildomas programos duomenimis vykdymo metu.

    ![ER modelio susiejimo konfigūracija SF modelio susiejimas puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Jei nematote šio modelio susiejimo 50.19 versijos, atidarykite bendrąją saugyklą ir importuokite ER konfigūracijos **SF modelio susiejimas** 50.19 versiją.

- ER formato konfigūracija **UBL pardavimo SF**:

    - 11.2 versijoje yra formato ir formato susiejimo ER komponentai. Formato komponentas nurodo ataskaitos maketą. Formato susiejimo komponentas apima modelio duomenų šaltinį ir nurodo, kaip šis duomenų šaltinis naudojamas ataskaitos maketui užpildyti vykdymo metu. Šis ER formatas buvo sukonfigūruotas generuoti el. SF universaliosios verslo kalbos (UBL) formatu. Jis buvo importuotas kaip importuoti pasirinkto ER formato **PEPPOL pardavimo SF** pirminis elementas.

- ER formato konfigūracija **PEPPOL pardavimo SF**:

    - 11.2.2 versijoje yra formato ir formato susiejimo ER komponentai, kurie buvo sukonfigūruoti el. SF generuoti „Pan-European Public Procurement OnLine” (PEPPOL) formatu.

    ![ER formato konfigūracija PEPPOL pardavimo SF puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Gautinų sumų parametrų konfigūravimas

1. Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.
2. Skirtuko **Elektroniniai dokumentai** „FastTab” **Elektroninės ataskaitos** lauke **Pardavimas ir laisvos formos SF** pasirinkite **PEPPOL pardavimo SF**.
3. Pasirinkite **Įrašyti**.

![Skirtukas Elektroniniai dokumentai gautinų sumų parametrų puslapyje.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Juridinio subjekto parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Organizacijos** \> **Juridiniai subjektai**.
2. Pasirinktos **DEMF** įmonės „FastTab” **Banko sąskaitos informacija** lauke **Banko kodas** įveskite **1234**.
3. Pasirinkite **Įrašyti**.
4. Uždarykite puslapį **Juridiniai subjektai**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Kliento įrašo paruošimas

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. Puslapyje **Visi klientai** pasirinkite kliento sąskaitos saitą **DE-014**.

### <a name="add-a-customer-contact"></a>Kliento kontakto įtraukimas

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. Veiksmų srities skirtuko **Klientas** grupėje **Sąskaitos** pasirinkite **Kontaktai**.
3. Pasirinkite **Įtraukti kontaktų**.
4. Puslapio **Kontaktai** lauke **Vardas** atidarykite peržvalgą, pasirinkite **Adam Carter**, tada pasirinkite **Pasirinkti**, norėdami uždaryti peržvalgą.
5. Pasirinkite **Įrašyti**.
6. Uždarykite puslapį **Kontaktai**.

### <a name="define-a-primary-contact"></a>Pirminio kontakto nustatymas

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. „FastTab” **Pardavimo demografiniai duomenys** lauke **Pirminis kontaktas** pasirinkite **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>El. SF išrašymo parinkties nustatymas

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. „FastTab” **SF ir pristatymas** nustatykite parinktį **El. SF** į **Taip**.
3. Pasirinkite **Įrašyti**.
4. Uždarykite puslapį **Visi klientai**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Kliento SF apdorojimas naudojant standartines ER konfigūracijas

Dabar galite naudoti standartines ER konfigūracijas, kurias importavote, kad galėtumėte klientui elektroniniu būdu siųsti laisvos formos SF.

### <a name="add-a-new-invoice"></a>Naujos SF įtraukimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapyje **Laisvos formos SF** pasirinkite **Naujas**.
3. „FastTab” **Laisvos formos SF antraštė** lauke **Kliento sąskaita** pasirinkite **DE-014**.
4. „FastTab” **SF eilutės** automatiškai įtraukiama SF eilutė. Šioje eilutėje nustatykite toliau pateiktus laukus.

    - Lauke **Aprašas** įveskite **Bloknotas**.
    - Lauke **Pagrindinė sąskaita** įveskite **401100**.
    - Lauke **Vieneto kaina** įveskite **1000**.

5. Pasirinkite **Įrašyti**.

![Laisvos formos SF puslapis.](./media/er-quick-start3-add-invoice.png)

Daugiau informacijos žr. [Laisvos formos SF kūrimas](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Naujos SF registravimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapio **Laisvos formos SF** veiksmų srityje pasirinkite **Registruoti**.
3. Dialogo lange **Registruoti laisvos formos SF** pasirinkite **Gerai**.

![Laisvos formos SF informacijos puslapis.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Užregistruotos SF siuntimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapio **Laisvos formos SF** veiksmų srities grupėje **Dokumentas** pasirinkite **Siųsti** \> **Originalus**.

    ![Pradinės SF peržiūra.](./media/er-quick-start3-send-invoice.png)

3. Uždarykite puslapį **Laisvos formos SF**.

### <a name="analyze-a-generated-e-invoice"></a>Sugeneruotos el. SF analizavimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninės ataskaitos užduotys**.
2. Puslapyje **Elektroninės ataskaitos užduotys** pasirinkite pradinį įrašą, kurio užduoties aprašas yra **Siųsti el. SF XML**.
3. Pasirinkite **Rodyti failus**, norėdami pasiekti sugeneruotų failų sąrašą.

    ![Elektroninių ataskaitų užduočių puslapis.](./media/er-quick-start3-jobs-list.png)

4. Pasirinkite **Atidaryti**, norėdami atsisiųsti sugeneruotą el. SF XML failą.
5. Analizuokite el. SF XML failą. Atkreipkite dėmesį, kad kliento mokesčių schemą šiuo metu nurodo XML atributai **schemeID** ir **schemeAgencyID**. Taip pat atkreipkite dėmesį, kad XML elemente **cbc:CustomizationID** šiuo metu yra toliau pateiktas tekstas: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Sugeneruoto elektroninės SF XML failo peržiūra.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Pasirinktinio duomenų bazės lauko įtraukimas

Galite naudoti funkciją [Pasirinktinis laukas](../../fin-ops/get-started/user-defined-fields.md), norėdami atlikti toliau pateiktus tinkinimo veiksmus dabartiniame „Finance” egzemplioriuje.

- Tinkinkite duomenų bazės struktūrą įtraukdami naują pasirinktinį duomenų bazės lauką, kuriame saugomas kiekvieno kliento federalinių mokesčių identifikavimo kodas.
- Tinkinkite puslapį **Klientas** įtraukdami naują duomenų įrašo lauką, kurį galima naudoti norint įvesti mokesčio kodo vertę naujame pasirinktiniame duomenų bazės lauke.

Atlikite toliau pateiktus veiksmus, norėdami atlikti tinkinimą.

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. Puslapyje **Visi klientai** pasirinkite kliento sąskaitos saitą **DE-014**.
3. „FastTab” **Bendra** dešiniuoju pelės mygtuku spustelėkite bet kurią tuščią sritį po lauku **Kalba** ir pasirinkite **Personalizavimas: UpperGroup**.

    „FastTab” **Bendra** turinys yra paryškintas ir pasirodo meniu **Personalizavimas**.

4. Meniu **Personalizavimas** pasirinkite **Įtraukti lauką**.
5. Dialogo lange **Įtraukti stulpelius** pasirinkite **Kurti naują lauką**.
6. Dialogo lango **Kurti naują lauką** lauke **Lentelės pavadinimas** pasirinkite **Klientai**.
7. Lauke **Pavadinimo prefiksas** įveskite **FederalTaxID**.

    > [!NOTE]
    > Visas lauko pavadinimas automatiškai nustatomas į **FederalTaxID\_Custom**.

8. Lauke **Žyma** įveskite **Federalinių mokesčių ID**.
9. Lauke **Tipas** pasirinkite **Tekstas**.
10. Lauke **Ilgis** įveskite **20**.
11. Pasirinkite **Įrašyti**.
12. Atsiradusiame pranešimo lange pasirinkite **Taip**, norėdami patvirtinti, kad norite sukurti naują lentelės **Klientai** lauko **FederalTaxID** įrašą.
13. Pasirinkite **Įterpti**, norėdami <a name="insert_custom_field"></a>įtraukti lauką **FederalTaxID\_Custom** į dabartinį puslapį.

    ![Puslapis Visi klientai.](./media/er-quick-start3-create-new-field.gif)

14. Uždarykite puslapį **Visi klientai**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>ER metaduomenų atnaujinimas

Norėdami, kad jūsų įtrauktas pasirinktinis laukas būtų [matomas](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) ER modelio susiejimo dizaino įrankyje, turite atnaujinti ER metaduomenis.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Lentelės nuorodų perkūrimas**.
2. Dialogo lange **Atnaujinti duomenų modelį** pasirinkite **Gerai**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Pasirinktinių ER konfigūracijų kūrimas

Galite naudoti „Microsoft” pateiktas ER konfigūracijas, norėdami kurti pasirinktines ER konfigūracijas, kad jos generuotų el. SF, kuriose yra naujas mokesčio kodas.

### <a name="customize-the-data-model-configuration"></a>Duomenų modelio konfigūracijos tinkinimas

Jei esate elektroninių ataskaitų funkcinio konsultanto vaidmens vartotojas, galite kurti jūsų pasirinktinį ER duomenų modelį.

#### <a name="add-a-custom-data-model-configuration"></a>Pasirinktinio duomenų modelio konfigūracijos įtraukimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje pasirinkite **Kliento SF modelis**.
3. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
4. Išplečiamojo dialogo lango lauke **Naujas** pasirinkite **Kildinti iš pavadinimo: kliento SF modelis, „Microsoft”**, norėdami nurodyti, kad nauja jūsų pasirinktinio ER duomenų modelio konfigūracija turi būti pagrįsta ER duomenų modelio konfigūracija.
5. Lauke **Pavadinimas** įveskite **SF modelis („Litware”)**.
6. Pasirinkite **Kurti konfigūraciją**, norėdami įtraukti naują ER konfigūraciją.

Dabar galite naudoti ER duomenų modelio konstruktorių, norėdami redaguoti SF modelio (Litware) **ER** **konfigūracijos Juodraštis 50.1** versiją.

![ER konfigūracijos 50.1 versija puslapyje Konfigūracijos.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Pasirinktinio duomenų modelio konfigūravimas

Turite modifikuoti jūsų pasirinktinį duomenų modelį įtraukdami naują lauką, kad būtų suteikta federalinių mokesčių identifikavimo kodo vertė. Šis kodas yra kiekvieno kliento duomenų ER formato, kuris naudos šį duomenų modelį kaip duomenų šaltinį, dalis.

1. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje pasirinkite **SF modelis („Litware”)**.
2. „FastTab” **Versijos** pasirinkite pasirinktos ER duomenų modelio konfigūracijos, kurios būsena yra **Juodraštis**, **50.1** versiją.
3. Veiksmų srityje pasirinkite pasirinktos konfigūracijos versijos **dizaino įrankį**.
4. Puslapio **Duomenų modelio dizaino įrankis** duomenų modelio medyje pasirinkite **Kliento informacija (klientas)**.
5. Pasirinkite **Naujas**.
6. Išplečiamojo dialogo lango lauke **Naujas mazgas kaip** priimkite numatytąją vertę **Aktyvaus mazgo antrinis elementas**.
7. Lauke **Pavadinimas** įveskite **FederalTaxID\_Litware**.
8. Lauke **Elemento tipas** priimkite numatytąją vertę **Eilutė**.
9. Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti**.

    ![Duomenų modelio dizaino įrankio puslapis.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Laukai **Žyma** ir **Aprašas** apibūdina naujo lauko paskirtį. Šiuos laukus galima užpildyti keliomis kalbomis. Daugiau informacijos žr. [Elektroninių ataskaitų keliomis kalbomis kūrimas](er-design-multilingual-reports.md).

10. Uždarykite **Duomenų modelio kūrimo** puslapį.

#### <a name="complete-a-custom-data-model-configuration"></a>Pasirinktinio duomenų modelio konfigūracijos užbaigimas

Turite užbaigti jūsų darbą naudodami jūsų pasirinktinio ER duomenų modelio konfigūracijos 50.1 versiją, kad jis būtų pasiekiamas ir būtų galima įtraukti kitas pasirinktines ER konfigūracijas.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **SF modelis**, tada pasirinkite **SF modelis („Litware”)**.
3. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 50.1 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 50.2 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinio ER duomenų modelio konfigūracijoje.

![50.1 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos tinkinimas

Jei esate elektroninių ataskaitų kūrėjo vaidmens vartotojas, galite kurti jūsų pasirinktinio ER modelio susiejimą.

#### <a name="add-a-custom-model-mapping-configuration"></a>Pasirinktinio ER modelio susiejimo konfigūracijos įtraukimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis**, tada pasirinkite **Kliento SF modelio susiejimas**.
3. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
4. Išplečiamojo dialogo lango lauke **Naujas** pasirinkite **Kildinti iš pavadinimo: kliento SF modelio susiejimas, „Microsoft”**, norėdami nurodyti, kad nauja jūsų pasirinktinio ER modelio susiejimo konfigūracija turi būti pagrįsta ER modelio susiejimo konfigūracija.
5. Lauke **Pavadinimas** įveskite **SF modelio susiejimas („Litware”)**.
6. Lauke **Paskirties modelis** pasirinkite **SF modelis („Litware”)**.

    > [!IMPORTANT]
    > Šis veiksmas yra labai svarbus. Jei jį praleisite, negalėsite naudoti jūsų pasirinktinio duomenų modelio sukonfigūruotame modelio susiejime.

7. Pasirinkite **Kurti konfigūraciją**, norėdami įtraukti naują ER konfigūraciją.

![Pasirinktinio modelio susiejimo konfigūracijos įtraukimas puslapyje Konfigūracijos.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Pasirinktinio modelio susiejimo konfigūravimas

Turite modifikuoti jūsų pasirinktinio modelio susiejimą ir nurodyti, kaip pasirinktinis pasirinktinio duomenų modelio laukas **FederalTaxID\_Litware** turi būti užpildytas programos duomenimis vykdymo metu.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis** \> **Kliento SF modelio susiejimas**, tada pasirinkite **SF modelio susiejimas („Litware”)**.
3. Veiksmų srityje pasirinkite **Dizaino įrankis**.
4. Puslapyje **Duomenų šaltinio susiejimo modelis** pasirinkite susiejimą **Kliento SF**.

    ![Puslapis Duomenų šaltinio susiejimo modelis.](./media/er-quick-start3-select-customer-mapping.png)

5. Pasirinkite **Dizaino įrankis**.
6. Puslapio **Modelio susiejimo dizaino įrankis** srityje **Duomenų šaltiniai** išplėskite duomenų šaltinį **CustInvoiceJour**, nurodantį programos lentelę **CustInvoiceJour**.
7. Dalyje **CustInvoiceJour** išplėskite **Ryšiai**, norėdami peržiūrėti lentelės **CustInvoiceJour** ryšių, kurių tipas „daugelis su vienu“ (N:1), sąrašą.
8. Dalyje **CustInvoiceJour** \> **Ryšiai** išplėskite **Klientai (CustTable)**, norėdami pasiekti lentelės **Klientai (CustTable)** laukus ir ryšius.
9. Pasirinkite duomenų šaltinio lauką **FederalTaxID\_Custom**, kurį įdiegėte [anksčiau](#insert_custom_field).
10. Srityje **Duomenų modelis** išplėskite **Kliento informacija (klientas)** ir pasirinkite duomenų modelio lauką **FederalTaxID\_Litware**.
11. Pasirinkite **Susieti**.

    ![Modelio susiejimo dizaino įrankio puslapis.](./media/er-quick-start3-customize-model-mapping.gif)

12. Pasirinkite **Įrašyti**.
13. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
14. Uždarykite puslapį **Duomenų šaltinio susiejimo modelis**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Pasirinktinio modelio susiejimo konfigūracijos užbaigimas

Turite užbaigti jūsų darbą naudodami jūsų pasirinktinio ER modelio susiejimo konfigūracijos 50.19.1 versiją, kad jis būtų pasiekiamas.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis** \> **Kliento SF modelio susiejimas**, tada pasirinkite **SF modelio susiejimas („Litware”)**.
3. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 50.19.1 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 50.19.2 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinio ER modelio susiejimo konfigūracijoje.

![50.19.1 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Palaikomas konfigūracijos [ciklas](general-electronic-reporting-manage-configuration-lifecycle.md) neapima duomenų bazės keitimų ciklo. Jei eksportuojate konfigūracijos **SF modelio susiejimas („Litware”)** 50.19.1 versiją iš dabartinio „Finance” egzemplioriaus ir bandote importuoti ją į kitą egzempliorių, kurio lentelėje **CustTable** nėra pasirinktinio lauko **FederalTaxID\_Custom**, įvyks išimtis. Išimtis nurodys, kad importuota ER konfigūracija nesuderinama su „Finance” paskirties egzemplioriaus metaduomenimis.

### <a name="customize-the-format-configuration"></a>Formato konfigūracijos tinkinimas

Jei esate elektroninių ataskaitų funkcinio konsultanto vaidmens vartotojas, galite kurti jūsų pasirinktinį ER formatą.

#### <a name="add-a-custom-format-configuration"></a>Pasirinktinės formato konfigūracijos įtraukimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis** \> **UBL pardavimo SF**, tada pasirinkite **PEPPOL pardavimo SF**.
3. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
4. Išplečiamojo dialogo lango lauke **Naujas** pasirinkite **Kildinti iš pavadinimo: PEPPOL pardavimo SF, „Microsoft”**, norėdami nurodyti, kad jūsų pasirinktinė ER formato konfigūracija turi būti pagrįsta ER formato konfigūracija.
5. Lauke **Pavadinimas** įveskite **PEPPOL pardavimo SF („Litware”)**.
6. Lauke **Duomenų modelis** pasirinkite **SF modelis („Litware”)**, norėdami naudoti jūsų pasirinktinį duomenų modelį ir modelio susiejimo komponentus.

    > [!NOTE]
    > Šis veiksmas yra labai svarbus. Jei jį praleisite, negalėsite naudoti jūsų pasirinktinio duomenų modelio sukonfigūruotame formate.

7. Lauke **Duomenų modelis** pasirinkite šaknies sąvoką **InvoiceCustomer**.
8. Pasirinkite **Kurti konfigūraciją**, norėdami įtraukti naują ER konfigūraciją.

![Pasirinktinės formato konfigūracijos įtraukimas puslapyje Konfigūracijos.](./media/er-quick-start3-adding-custom-format.png)

Dabar galite naudoti ER operacijų konstruktorių, kad galėtumėte redaguoti 11.2.2.1 **Sf (litware)** ER **konfigūracijos** versiją Juodraštis.

![ER konfigūracijos 11.2.2.1 versija puslapyje Konfigūracijos.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Pasirinktinio formato konfigūravimas

Turite modifikuoti jūsų pasirinktinį formatą įtraukdami naują formato elementą, kad būtų užpildyta kliento, kurio SF išrašyta, federalinių mokesčių identifikavimo kodo vertė.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis** \> **UBL pardavimo SF** \> **PEPPOL pardavimo SF**, tada pasirinkite **PEPPOL pardavimo SF („Litware”)**.
3. Veiksmų srityje pasirinkite **Dizaino įrankis**.
4. Formato medyje išplėskite **XMLHeader** \> **SF** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**, tada pasirinkite **cbc:ID**.
5. Pasirinkite **Įtraukti**, tada pasirinkite **XML** \> **Atributas**.
6. Dialogo lango **Komponento ypatybė** lauke **Pavadinimas** įveskite **FederalTaxID**.
7. Pasirinkite **Gerai**, norėdami įtraukti naują formato elementą, kad sukurtumėte naują XML atributą **FederalTaxID** sugeneruotame XML faile.
8. Formato medžio dalyje **XMLHeader** \> **SF** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** pasirinkite **FederalTaxID**.
9. Pasirinkite **Perkelti aukštyn**.

![Naujas formato elementas puslapyje Formato dizaino įrankis.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Pasirinktinio formato susiejimo konfigūravimas

1. Puslapio **Formato dizaino įrankis** skirtuke **Susiejimas** išplėskite duomenų šaltinį **SF**, kurio tipas **Modelis**.
2. Dalyje **SF** išplėskite **Kliento informacija (klientas)** ir pasirinkite **FederalTaxID\_Litware**.
3. Pasirinkite **Susieti**.

    ![Formato dizaino įrankio puslapis.](./media/er-quick-start3-customized-format-mapping.png)

4. Pasirinkite duomenų šaltinį **SF**, kurio tipas **Modelis**, tada pasirinkite **Redaguoti**.
5. Lauke **Versija** pasirinkite **1** jūsų pasirinktinio duomenų modelio versiją, tada pasirinkite **Gerai**.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį **Formato dizaino įrankis**.

#### <a name="complete-a-custom-format-configuration"></a>Pasirinktinės formato konfigūracijos užbaigimas

Norėdami naudoti, turite užbaigti darbo su 11.2.2.1 versijos ER formato konfigūracijos versija.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **Kliento SF modelis** \> **UBL pardavimo SF** \> **PEPPOL pardavimo SF**, tada pasirinkite **PEPPOL pardavimo SF („Litware”)**.
3. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 11.2.2.1 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 11.2.2.2 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinėje ER formato konfigūracijoje.

![11.2.2.1 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Gautinų sumų parametrų konfigūravimas norint pradėti naudoti pasirinktines ER konfigūracijas

1. Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.
2. Skirtuko **Elektroniniai dokumentai** „FastTab” **Elektroninės ataskaitos** lauke **Pardavimas ir laisvos formos SF** pasirinkite **PEPPOL pardavimo SF („Litware”)**.
3. Pasirinkite **Įrašyti**.

![Gautinų sumų parametrų puslapis, skirtukas Elektroniniai dokumentai, „FastTab” Elektroninės ataskaitos.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Kliento įrašo atnaujinimas įtraukiant federalinių mokesčių identifikavimo kodą

1. Eikite į **Gautinos sumos** \> **Klientai** \> **Visi klientai**.
2. Puslapyje **Visi klientai** pasirinkite kliento sąskaitos saitą **DE-014**.
3. „FastTab” **Bendra** lauke **Federalinių mokesčių ID** įveskite **LITWARE-6789**.
4. Pasirinkite **Įrašyti**.

    ![DE-014 kliento informacijos puslapis.](./media/er-quick-start3-added-tax-id-value.png)

5. Uždarykite puslapį **Visi klientai**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Kliento SF apdorojimas naudojant pasirinktines ER konfigūracijas

### <a name="select-and-send-a-posted-invoice"></a>Užregistruotos SF pasirinkimas ir siuntimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapyje **Laisvos formos SF** pasirinkite SF, kurią anksčiau įtraukėte ir užregistravote.
3. Veiksmų srities grupėje **Dokumentas** pasirinkite **Siųsti** \> **Originalus**.
4. Uždarykite puslapį **Laisvos formos SF**.

### <a name="analyze-a-generated-e-invoice"></a>Sugeneruotos el. SF analizavimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninės ataskaitos užduotys**.
2. Puslapyje **Elektroninės ataskaitos užduotys** pasirinkite naujausią įrašą, kurio užduoties aprašas yra **Siųsti el. SF XML**.
3. Pasirinkite **Rodyti failus**, norėdami pasiekti sugeneruotų failų sąrašą.
4. Pasirinkite **Atidaryti**, norėdami atsisiųsti sugeneruotą el. SF XML failą.
5. Analizuokite el. SF XML failą. Atkreipkite dėmesį, kad jūsų tinkinimą atitinkanti kliento mokesčių schema apima pasirinktinį XML atributą **FederalTaxID** ir XML atributus **schemeID** ir **schemeAgencyID**. Šio naujo XML atributo vertę nurodo **LITWARE-6789** federalinių mokesčių ID, įvestas klientui, kurio SF išrašyta.

    ![Sugeneruoto elektroninės SF XML failo, kuriame yra jūsų tinkinimai, peržiūra.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Naujausių standartinių ER konfigūracijų versijų importavimas

Norėdami [atnaujinti](general-electronic-reporting-manage-configuration-lifecycle.md) standartinių ER konfigūracijų rinkinį jūsų „Finance” egzemplioriuje, turite importuoti naujas jų versijas, kada jos pasiekiamos to egzemplioriaus sukonfigūruotoje ER [saugykloje](general-electronic-reporting.md#Repository).

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę ir pasirinkite **Saugyklos**, kad peržiūrėtumėte „Microsoft” tiekėjo saugyklų sąrašą.
3. Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**. Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.
4. Puslapio **Konfigūracijos saugykla** kairiosios srities konfigūracijos medyje pasirinkite formato konfigūraciją **PEPPOL pardavimo SF**.
5. „FastTab” **Versijos** pasirinkite **32.6.7** pasirinktos ER formato konfigūracijos, kuri buvo išleista, kad palaikytų kliento elektronines SF PEPPOL BIS 3 formatu, versiją. Daugiau informacijos rasite [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.

![32.6.7 versija, pasirinkta saugyklos puslapyje Konfigūracija.](./media/er-quick-start3-import-solution2.png)

Informacijos apie tai, kaip šis procesas gali būti automatizuotas, žr. [Atnaujintų ER konfigūracijų versijų importavimas](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Importuotų ER konfigūracijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Išplėskite „FastTab“ **Konfigūracijos komponentai**.
4. Kairiosios srities konfigūracijos medyje išplėskite **SF modelis**. Atkreipkite dėmesį, kad pavadinimas **Kliento SF modelis** buvo pakeistas į **SF modelis** vienoje iš importuotų ER duomenų modelio konfigūracijų.
5. Kairiosios srities konfigūracijos medyje išplėskite **SF modelio susiejimas**. Atkreipkite dėmesį, kad pavadinimas **Kliento SF modelio susiejimas** buvo pakeistas į **SF modelio susiejimas** vienoje iš importuotų ER modelio susiejimo konfigūracijų.
6. Išplėskite **UBL pardavimo SF** \> **PEPPOL pardavimo SF**.

Atkreipkite dėmesį, kad kartu su pasirinktu ER formatu **PEPPOL pardavimo SF** buvo importuotos kitų būtinų ER konfigūracijų naujausios versijos. Kadangi naujos ER konfigūracijų versijos nuolat publikuojamos bendrojoje saugykloje ir LCS, kad atitinkami ER sprendimai atitiktų naujus reikalavimus, buvo importuotos naujausios reikiamo duomenų modelio konfigūracijos versijos ir jo modelio susiejimo konfigūracijos.

Įsitikinkite, kad toliau pateiktos ER konfigūracijos galiausiai bus prieinamos konfigūracijos medyje.

- ER duomenų modelio konfigūracija **SF modelis**:

    - 206 versijoje (arba naujesnėje) yra duomenų modelio ER komponento 24 versija (arba naujesnė), nurodanti SF išrašymo verslo domeno duomenų struktūrą. Ši ER konfigūracija buvo importuota kaip naujausios pasiekiamos ER modelio susiejimo konfigūracijos **SF modelio susiejimas** aukštesnio lygmens elementas.

    ![206 versija puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution2b1.png)

- ER modelio susiejimo konfigūracija **SF modelio susiejimas**:

    - 206.132 versija (arba naujesnė) buvo importuota kaip naujausias ER duomenų modelio konfigūracijos **SF modelis** 206 versijos diegimas. Joje yra keli modelio susiejimo ER komponentai, aprašantys, kaip duomenų modelis užpildomas programos duomenimis vykdymo metu.

    ![206.132 versija puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution2b2.png)

- ER formato konfigūracija **UBL pardavimo SF**:

    - 32.6 versijoje yra formato ir formato susiejimo ER komponentai. Formato komponentas nurodo ataskaitos maketą. Formato susiejimo komponentas apima modelio duomenų šaltinį ir nurodo, kaip šis duomenų šaltinis naudojamas ataskaitos maketui užpildyti vykdymo metu. Šis ER formatas buvo sukonfigūruotas generuoti el. SF UBL formatu. Jis buvo importuotas kaip importuoti pasirinkto ER formato **PEPPOL pardavimo SF** pirminis elementas.

- ER formato konfigūracija **PEPPOL pardavimo SF**:

    - 32.6.7 versijoje yra formato ir formato susiejimo ER komponentai, kurie buvo sukonfigūruoti el. SF generuoti PEPPOL formatu.

    ![32.6.7 versija puslapyje Konfigūracijos.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Naujų standartinių ER konfigūracijų versijų keitimų tvirtinimas jūsų pasirinktinėse ER konfigūracijose

### <a name="adopt-your-custom-er-data-model"></a>Jūsų pasirinktinio ER duomenų modelio tvirtinimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **SF modelis**, tada pasirinkite **SF modelis („Litware”)**.
3. „FastTab” **Versijos** pasirinkite pasirinktos duomenų modelio konfigūracijos **50.2** juodraščio versijos parinktį **Pritaikyti kitoje vietoje**.
4. Lauke **Paskirties versija** patvirtinkite pagrindinio ER duomenų modelio konfigūracijos **206** versijos pasirinkimą ir pasirinkite **Gerai**.

    Jūsų pasirinktinės ER duomenų modelio konfigūracijos juodraščio versijos numeris pakeičiamas iš **50.2** į **206.2** siekiant nurodyti, jog joje dabar yra jūsų tinkinimas, sulietas su pagrindinio ER duomenų modelio konfigūracijos naujausios versijos (206) keitimais.

    > [!NOTE]
    > Pritaikymo kitoje vietoje veiksmas nėra grįžtamas. Norėdami atšaukti šį pritaikymą kitoje vietoje, „FastTab” **Versijos** pasirinkite **50.1** modelio **SF modelis („Litware”)** versiją ir pasirinkite **Gauti šią versiją**. 206.2 versija bus pernumeruota atgal į **50.2**, o juodraštinės versijos 50.2 turinys atitiks 50.1 versijos turinį.

5. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 206.2 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 206.3 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinio ER duomenų modelio konfigūracijoje.

![206.2 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Jūsų pasirinktinio ER modelio susiejimo tvirtinimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **SF modelis** \> **SF modelio susiejimas**, tada pasirinkite **SF modelio susiejimas („Litware”)**.
3. „FastTab” **Versijos** pasirinkite pasirinktos modelio susiejimo konfigūracijos **50.19.2** juodraščio versijos parinktį **Pritaikyti kitoje vietoje**.
4. Lauke **Paskirties versija** patvirtinkite pagrindinio ER modelio susiejimo konfigūracijos **206.132** versijos pasirinkimą ir pasirinkite **Gerai**.

    Jūsų pasirinktinės ER modelio susiejimo konfigūracijos juodraščio versijos numeris pakeičiamas iš **50.19.2** į **206.132.2** siekiant nurodyti, jog joje dabar yra jūsų tinkinimas, sulietas su pagrindinio ER modelio susiejimo konfigūracijos naujausios versijos (206.132) keitimais.

    Atkreipkite dėmesį, kad aptikta pritaikymo kitoje vietoje nesuderinamumų. Dabar turite išspręsti šiuos nesuderinamumus neautomatiniu būdu.

    ![Pritaikymo kitoje vietoje nesuderinamumų pranešimas puslapyje Konfigūracijos.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Veiksmų srityje pasirinkite **Dizaino įrankis**, tada susiejimų sąraše pasirinkite **Kliento SF**.
6. Pasirinkite kiekvieno pritaikymo kitoje vietoje nesuderinamumo parinktį **Išlaikyti vertę**, nes turite išsaugoti kiekvieno paminėto komponento pasirinktinio duomenų modelio versijos numerį.

    ![Pritaikymo kitoje vietoje nesuderinamumai puslapyje Modelio susiejimo dizaino įrankis.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Pasirinkite **Įrašyti** ir uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
8. Susiejimų sąraše pasirinkite **Projekto SF**.
9. Pasirinkite kiekvieno pritaikymo kitoje vietoje nesuderinamumo parinktį **Išlaikyti vertę**, nes turite išsaugoti kiekvieno paminėto komponento pasirinktinio duomenų modelio versijos numerį.
10. Pasirinkite **Įrašyti** ir uždarykite puslapį **Modelio susiejimai**.

    > [!NOTE]
    > Pritaikymo kitoje vietoje veiksmas nėra grįžtamas. Norėdami atšaukti šį pritaikymą kitoje vietoje, „FastTab” **Versijos** pasirinkite **50.19.1** modelio susiejimo **SF modelio susiejimas („Litware”)** versiją ir pasirinkite **Gauti šią versiją**. 206.132.2 versija bus pernumeruota atgal į **50.19.2**, o juodraštinės versijos 50.19.2 turinys atitiks 50.19.1 versijos turinį.

11. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 206.132.2 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 206.132.3 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinio ER modelio susiejimo konfigūracijoje.

![206.132.2 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Jūsų pasirinktinio ER formato tvirtinimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** kairiosios srities konfigūracijos medyje išplėskite **SF modelis** \> **UBL pardavimo SF** \> **PEPPOL pardavimo SF**, tada pasirinkite **PEPPOL pardavimo SF („Litware”)**.
3. „FastTab” **Versijos** pasirinkite pasirinktos formato konfigūracijos **11.2.2.2** juodraščio versijos parinktį **Pritaikyti kitoje vietoje**.
4. Versijos lauke **Paskirtis** patvirtinkite pagrindinio ER formato konfigūracijos **32.6.7** versijos pasirinkimą ir pasirinkite **Gerai**.

    Jūsų pasirinktinės ER formato konfigūracijos juodraščio versijos numeris pakeičiamas iš **11.2.2.2** į **32.6.7.2** siekiant nurodyti, jog joje dabar yra jūsų tinkinimas, sulietas su pagrindinio ER formato konfigūracijos naujausios versijos (32.6.7) keitimais.

    Atkreipkite dėmesį, kad aptikta pritaikymo kitoje vietoje nesuderinamumų. Dabar turite išspręsti šiuos nesuderinamumus neautomatiniu būdu.

5. Veiksmų srityje pasirinkite **Dizaino įrankis**.
6. Pasirinkite kiekvieno pritaikymo kitoje vietoje nesuderinamumo parinktį **Išlaikyti vertę**, nes turite išsaugoti kiekvieno paminėto komponento pasirinktinio duomenų modelio versijos numerį.
7. Pasirinkite **Įrašyti**.
8. Skirtuke **Susiejimas** pasirinkite duomenų šaltinį **SF**, kurio tipas **Modelis**, tada pasirinkite **Redaguoti**.
9. Lauke **Versija** pasirinkite **2** jūsų pasirinktinio duomenų modelio versiją, tada pasirinkite **Gerai**.
10. Pasirinkite **Įrašyti**.

    > [!NOTE]
    > Pritaikymo kitoje vietoje veiksmas nėra grįžtamas. Norėdami atšaukti šį pritaikymą kitoje vietoje, „FastTab” **Versijos** pasirinkite **11.2.2.1** formato **PEPPOL pardavimo SF („Litware”)** versiją ir pasirinkite **Gauti šią versiją**. 32.6.7.2 versija bus pernumeruota atgal į **11.2.2.2**, o juodraštinės versijos 11.2.2.2 turinys atitiks 11.2.2.1 versijos turinį.

11. Uždarykite puslapį **Formato dizaino įrankis**.
12. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 32.6.7.2 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Įtraukta nauja redaguojama 32.6.7.3 versija ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus jūsų pasirinktinėje ER formato konfigūracijoje.

![32.6.7.2 versija užbaigta puslapyje Konfigūracijos.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Kliento SF apdorojimas naudojant naujas pasirinktinių ER konfigūracijų versijas

### <a name="select-and-send-a-posted-invoice"></a>Užregistruotos SF pasirinkimas ir siuntimas

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Puslapyje **Laisvos formos SF** pasirinkite SF, kurią anksčiau įtraukėte ir užregistravote.
3. Veiksmų srities grupėje **Dokumentas** pasirinkite **Siųsti** \> **Originalus**.

    > [!NOTE] 
    > Todėl, **kad dabar turite dvi Jav pardavimo SF (litware)** ER formato konfigūracijos versijas, todėl nė viena versija neturi galiojainės datos reikšmės, naujausia versija naudojama el. SF generuoti.

4. Uždarykite puslapį **Laisvos formos SF**.

### <a name="analyze-a-generated-e-invoice"></a>Sugeneruotos el. SF analizavimas

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninės ataskaitos užduotys**.
2. Puslapyje **Elektroninės ataskaitos užduotys** pasirinkite naujausią įrašą, kurio užduoties aprašas yra **Siųsti el. SF XML**.
3. Pasirinkite **Rodyti failus**, norėdami pasiekti sugeneruotų failų sąrašą.
4. Pasirinkite **Atidaryti**, norėdami atsisiųsti sugeneruotą el. SF XML failą.
5. Analizuokite el. SF XML failą. Atkreipkite dėmesį, kad jūsų tinkinimą atitinkanti kliento mokesčių schema vis dar apima pasirinktinį XML atributą **FederalTaxID** ir XML atributus **schemeID** ir **schemeAgencyID**. Be to, dėl naujos pagrindinio formato **UBL pardavimo SF** versijos keitimų suliejimo su jūsų tinkinimu, XML elemento **cbc:CustomizationID** tekstas buvo pakeistas iš `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` į `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Sugeneruoto elektroninės SF XML failo, kuriame yra tinkinimų, peržiūra.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [ER konfigūracijų atsisiuntimas iš „Lifecycle Services“](download-electronic-reporting-configuration-lcs.md)
- [ER konfigūracijų atsisiuntimas iš „Configuration service” Bendrosios saugyklos](er-download-configurations-global-repo.md)
- [Kurti laisvos formos SF](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Pasirinktinių laukų kūrimas ir naudojimas](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
