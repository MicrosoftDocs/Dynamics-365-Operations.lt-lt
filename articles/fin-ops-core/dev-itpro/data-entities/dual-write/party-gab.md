---
title: Šalies ir bendros knygelės nustatymas
description: Šioje temoje aprašomos dvigubo rašymo šalies ir visuotinės adresų knygelės funkcijos.
author: RamaKrishnamoorthy
ms.date: 08/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: da5ca16ed87108f8046348c831d37085f6f780d7
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386690"
---
# <a name="party-and-global-address-book"></a>Šalies ir bendros knygelės nustatymas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*Šalis* ir *visuotinė adresų knygelė* yra sąvokos „Finance and Operations“ programose. Šalis gali būti organizacija ar asmuo. Tai patogu visuotinai saugoti ir tvarkyti šalies ypatybių pavadinimą, tokių kaip kalbą, kontaktus ir adresus. Tada, kai ypatybės vertė pasikeičia vienoje vietoje, pakeitimas atsispindi visose vietose, kuriose dalyvauja šalis.

## <a name="party"></a>Įrašas

Šalis yra asmuo arba organizacija, įtraukta į verslą. Naudojant šalies sąvoką, asmuo ar organizacija gali vaidinti daugiau nei vieną vaidmenį veikloje (pavyzdžiui, darbuotojo, kliento, tiekėjo ar kontakto). Vaidmuo remiasi kontekstu ir tikslu. Štai keletas iš vaidmenų pavyzdžių iš dviejų fiktivių įmonių „Contoso“ ir „Fabrikam“:

+ **Darbuotojas**: darbuotojas. Pavyzdys yra „Contoso“ darbuotojas.
+ Terminas **tiekėjas**: reiškia tiekėjų organizaciją arba individualų savininką, kuris tiekia prekes ar teikia paslaugas verslui. Pavyzdžiui, jei „Fabrikam“ parduoda „Contoso“ atsargas, „Fabrikam“ yra „Contoso“ tiekėjas.
+ **Kontaktas**: asmuo, kurį reikia susisiekti. Pavyzdžiui, jei „Contoso“ perka atsargas iš „Fabrikam“, „Contoso“ darbuotojas susisiektų su kontaktiniu darbuotoju „Fabrikam“.
+ **Klientas**: klientas yra asmuo arba įmonė, kuri perka dalykus iš įmonės. Pavyzdžiui, jei „Contoso“ perka atsargas iš „Fabrikam“, „Contoso“ yra „Fabrikam“ klientas.

Šalies modelis dažnai naudojamas siekiant pateikti tarpinių ir kompleksinių ryšių tarp organizacijų ir žmonių ryšius, ypač kai šalis atlieka daugiau nei vieną vaidmenį. Štai keletas bendrų pavyzdžių:

+ Šalis gali būti ir klientas, ir tiekėjas. Pavyzdžiui, Šiaurės Amerikoje „Fabrikam“ parduoda elektros iš „Contoso“ ir pirkimus surinkus iš „Contoso“. Europoje „Fabrikam“ parduoda dalis „Contoso“, tačiau nieko neperka iš „Contoso“.
+ Šalis gali būti ir darbuotojas, ir klientas. Pavyzdžiui, „Contoso“ darbuotojas perka elektroninę įrangą iš „Contoso“ asmeniniams tikslams.
+ Tarp asmens ir organizacijos gali būti įvairiais ryšiais (N:N). Pavyzdžiui, „Fabrikam“ tiekia aptarnavimo specialistams ir naudoja išdėstymo koordinates. Koordinatorius suderina kelių „Fabrikam“ klientų darbo užklausų aptarnavimo specialistus. „Contoso“ yra vienas iš „Fabrikam“ klientų. Kai „Contoso“ reikia specialistų, ji susisieks su įdarbinimo koordinatoriumi, kuris palengvina užklausą. Kadangi išdėstymo koordinatorius tvarko visų klientų užklausas, naudojamas ryšys N:N.

Toliau pateiktame vaizde rodomas šalies duomenų modelis.

![Duomenų modelis šaliai.](media/party-gab-image1.png)

> [!TIP]
> Kai bandote sukurti naują sąskaitos įrašą, norėdami ieškoti įrašo pagal pavadinimą, naudokite lauką **Šalis**. Tokiu būdu, jei rasite įrašą, jums tiesiog reikia jį pasirinkti. Sistema tada automatiškai užpildo visus šalies duomenis. Nereikia neautomatiniu būdu įvesti visų reikalingų laukų. Šį elgseną galima rasti sąskaitos nestandartiniuose **Sąskaitos**, **Kontakto** ir **Tiekėjo** puslapiuose.

Ne visi programėlių šalių „Finance and Operations“ vaidmenys palaikomi naudojant dvigubo rašymo funkciją. Visą šalies vaidmenų sąrašą rasite visuotinės adresų [knygelės](../../../fin-ops/organization-administration/overview-global-address-book.md) apžvalga.

### <a name="global-address-book"></a>Visuotinė adresų knygelė

Visuotinė adresų knygelė yra dalyvaujančių verslo organizacijų ir asmenų pašto ir elektroninių adresų katalogas.

Visuotinė adresų knygelė saugomi ir tvarko tiek pašto adresų, tiek elektroninių adresų, kiek reikia. Pavyzdžiui, tarkime, kad „Fabrikam“ turi dujų stotis 50 vietų. Kiekviena vieta turi skirtingą pašto adresą, el. pašto adresą ir telefono numerį. Visiems verslo užsakymams sąskaita išsakoma į pagrindinę dujų stotį, bet pirkimas siunčiamas tiesiai į konkrečią dujų stotį, kuri reikalauja pirkimo. Visuotinė adresų knygelėje pagrindinė dujų stotis yra sąskaitų siuntimo adresas, o kiekviena dujų stotis – kaip „Fabrikam“ siuntimo adresas. Jei reikia, pasiūlymus ir užsakymus adresai gali būti saugomi ir nuskaitomi.

Atsižvelgiant į verslo kontekstą asmuo arba organizacija gali atlikti daugiau nei vieną vaidmenį, o tas pats pašto adresas ir elektroninis adresas gali būti naudojami visiems vaidmenims. Šiuo atveju, adreso pakeitimas viename vaidmenyse turėtų pasirodyti ant kito vaidmens ir atvirkščiai. Visuotinė adresų knygelė saugoma ir tvarko adresus visuotinai.

Toliau pateiktame paveikslėlyje parodytas produkto spalvos dimensijos duomenų modelis.

![Visuotinės bendros adresų knygelės duomenų modelis.](media/party-gab-image2.png)

## <a name="contact"></a>Kontaktas

Klientų įsipareigojimo programose kontaktinis asmuo yra asmuo. Tačiau kontaktų lentelė buvo perkrauta siekiant atstovauti **asmenį**, portalo vartotoją, verslo su klientu B2C klientą arba tiekėją. Vaizdas yra netiesiogiai ir jūs negalite pranešti apie skirtumą, jei nebent tirsite susijusias operacijas. Kontaktų **lentelėje** ribojamas ryšys su sąskaitų **lentele** vienas su vienu 1:1. Kaip šalies ir visuotinės adresų knygelės modelio dalis, dvigubo rašymo funkcija pristato tikslias klasifikavimo ir dvigubo rašymo ypatybes, leidžia N:N ryšius tarp kontaktinio asmens ir organizacijos (**Sąskaitos** ar **Tiekėjo** objekto).

Yra du tipai **Kontaktų** eilučių:

+ **Atskirtas kontaktas** – A **Kontakto** eilutė, kurioje **įmonės** laukelis yra privaloma vertė.
+ **Neperduotas kontaktas** – A **kontakto** eilutė, kurioje **Įmonė** laukelis yra tuščias.

Kontaktų **lentelėje gali būti tolesnių tipų** eilutės.

| Eilutės tipas | Aprašas |
|----------|-------------|
| Asmuo, kuris yra klientas, (pavyzdžiui, parduotinas kontaktinis asmuo ar B2C klientas). | Atskirtas kontakto įrašas, kur **įmonės laukas nėra tuščias ir** lauke **klientas** nustatyta reikšmė **Taip**. |
| Asmuo, kuris yra tiekėjas, pavyzdžiui, ind. įmonės savininkas kaip tiekėjas. | Atskirtas kontakto įrašas, kur **įmonės laukas nėra tuščias ir** lauke **Tiekėjas** nustatyta reikšmė **Taip**. |
| Asmuo, kuris yra klientas ir tiekėjas | Atskirtas kontakto įrašas, kur **įmonės** laukas nėra tuščias ir **yra kleintas** nustatytas į **Taip**, o **yra tiekėjo** laukelyje nustatytas į **Taip**. Asmuo gali būti ir vieno produkto gamintojas, ir kito produkto vartotojas. Ir „Finance and Operations“ programėlės, ir dvigubo rašymo palaikymas palaiko šį ryšį. |
| Asmuo, kuris yra organizacijos kontaktinis asmuo, bet nėra klientas ir ne tiekėjas. | Atskirtas kontakto įrašas, kur **įmonės** laukas nėra tuščias ir **yra kleintas** nustatytas į **Ne**, o **yra tiekėjo** laukelyje nustatytas į **Ne**. |

## <a name="contact-for-party-table"></a>Šalies kontakto lentelė

**Šalies kontaktas** lentelė laiko ir tvarko N:N ryšius tarp **sąskaitos eilučių ir** kontaktų **eilučių**. Taip galima filtruoti atskirtas kontaktinių eilučių eilutes iš nenusidėlintose eilutėse ir susieti tik nesuslenktas kontaktų eilutes **su sąskaitos** **arba** **tiekėjo** **eilutėmis**.

Pavyzdžiui, Nataša Džauns ir Migelis Rejes yra veterinarai, kurie rūpinasi fermomis savo teritorijoje. Nataša dirba Sietlo srityje, o Migelis Kento. Klientų įsipareigojimo programoje, ūkiai yra vaizduojami klientais, o veterinarai kontaktiniais asmenimis. Vienas **Susieto** kontakto įrašas yra susietas su visais Nataša su tais pačiais ūkiais, kuriuose ji dirba. Panašiai, atskiras **Kontakto** įrašas Migeliui yra susietas su ūkiais, su kuriais jis dirba.

Šie ryšiai saugomi šalies **kontaktų** lentelėje. Šį elgseną galite rasti sąskaitos nestandartiniuose **Sąskaitos**, **Kontakto** ir **Tiekėjo** puslapiuose:

+ Sąskaitos puslapyje **galite naudoti skirtuką Susieti kontaktai vienam ar daugiau** **kontaktų** susieti su sąskaitos **eilute**. Tokiu būdu, priskirsite kontakto asmenis organizacijai. Tada galite pasirinkti vieną kontaktą kaip pagrindinį sąskaitos kontaktą. Jei naudojate **sparčiojo kūrimo** puslapį, galite pasirinkti tik kontaktinį asmenį. Jei naudojate formą Tiekėjas, o įrašo tipas yra **Organizacija**, veikimo būdas yra **tas** pats.
+ Kontaktinio asmens puslapyje, kai eilutė yra klientas, tiekėjas arba abu (atskirtas kontaktas), galite naudoti skirtuką Susieti kontaktai, kad susietumėte **vieną** ar daugiau **kontaktų**. Tokiu būdu, priskirsite kontaktinius asmenis B2C klientui ar tiekėjui. Tada galite pasirinkti vieną kontaktą kaip pagrindinį sąskaitos kontaktą. Jei naudojate **sparčiojo kūrimo** puslapį, galite pasirinkti tik kontaktinį asmenį.
+ Kontaktinio asmens puslapyje, kai eilutė yra kontaktinis asmuo (atskirtas kontaktas), galite naudoti skirtuką Susietos organizacijos, kad susietumėte **vieną** ar daugiau **klientų ar tiekėjų**. Tokiu būdu, priskirsite klientus ar tiekėjus kitams kontaktiniam asmeniui. Klientas arba tiekėjas gali būti organizacija, asmuo arba abu. Vienu metu galite pasirinkti tik vieną reikšmę iš keturių laukų:

    + Jei **pasirenkate įrašo** ID laukelį, pagrindinis kontaktas priskiriamas visiems pasirinktos šalies vaidmenims.
    + Jei pasirenkate Susietas kontaktas **laukelį**, tada pasirenkate atskirtą kontaktą, kurio tipas yra **asmuo**.
    + Jei lauke Susieta sąskaita **arba** Susietas **tiekėjas pasirinksite** vertę, pasirinkite organizaciją.

    ![Skirtukas Susietos organizacijos kontakto puslapyje.](media/party-gab-image3.png)

    Nepriklausomai nuo jūsų pasirinkimo, susiejimas sukuriamas šalies lygiu ir taikomas visiems šalies vaidmenims ir saugomas objekto **Šalies kontaktas**.

> [!NOTE]
> Klientų įsipareigojimų programoje rodomas šalies lentelės kontaktas pavadinimas yra Kliento / **tiekėjo** **kontaktas**.

Atidarius kontakto **eilutę, kurioje nustatytas ir kliento, ir tiekėjo** **nr.**,  **rodomas** **skirtukas** **Susietos** organizacijos. Naudokite šį skirtuką norėdami susieti vieną ar daugiau kliento arba tiekėjo organizacijų su kontaktu.

Atidarius kontakto **eilutę, kurioje nustatytas ir kliento, ir tiekėjo** **nr.**,  **rodomas** **Taip** **Susieti** kontakai. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau kontaktų su sąskaitos eilute.

## <a name="postal-addresses"></a>Pašto adresai

Sąskaitoje, **kontakte** ir tiekėjo formose **įvestas naujas** **skirtukas pavadinimu** **Adresai**. Šis skirtukas palaiko kelis pašto adresus, naudodamas tinklelį, kaip parodyta šioje iliustracijoje.

![Pašto adresų tinklelis.](media/party-gab-image4.png)

Tinklelyje yra šie stulpeliai:

+ Stulpelis **Pašto** adreso vaidmenys išvardija adreso paskirtį.
+ **Yra** pirminis – vertė, nurodanti, ar adresas yra pagrindinis adresas.
+ **Adreso** numeris – adreso užsakymas.

Galite naudoti mygtuką **Naujas adresas** virš tinklelio, kad sukurtumėte tiek pašto adresų, kiek norite.

Laukai **1 adresas ir 2 adresas, esantys sąskaitos formos skirtuke Suvestinė**, **atitinka** **pristatymo** **ir** **SF** **adresus**.

![Pašto adresų suvestinės skirtukas.](media/party-gab-image5.png)

Laukeliai **Adresas 1**, **Adresas 2** ir **Adresas 3** skirtuke **Santrauka** formoje **Kontaktas** atitinka **Verslo**, **Pristatymo** bei **SF** adresus.

## <a name="electronic-addresses"></a>Elektroninio pašto adresai

Sąskaitoje, **kontakte** ir tiekėjo formose **įvestas naujas** **skirtukas pavadinimu** **Elektroniniai adresai**. Šis skirtukas palaiko kelis elektroninius adresus, naudodamas tinklelį, kaip parodyta šioje iliustracijoje.

![Elektroninių adresų tinklelis.](media/party-gab-image6.png)

Tinklelyje yra šie stulpeliai:

+ **Tipas** – elektroninio adreso tipas.
+ **Yra** pirminis – vertė, nurodanti, ar adresas yra pagrindinis adresas.
+ Stulpelis **Tikslo** adreso vaidmenys išvardija elektroninio adreso paskirtį.

Galite naudoti mygtuką **Naujas elektroninis adresas** virš tinklelio, kad sukurtumėte tiek pašto adresų, kiek norite.

Elektroniniai adresai galimi tik šiame tinklelyje. Būsimuose leidimuose visi elektroninio ir pašto adresų laukai bus pašalinti iš kitų skirtukų, pvz., **skirtukų** Suvestinė ir **informacija**. Kontaktinė informacija, rodoma skirtuko lape Išsamiai, yra tik skaitomos pirminio elektroninio adreso kopijos, pvz., pagrindinis telefonas, pagrindinis el. paštas, pagrindinis telefonas, pagrindinis faksas ir **pagrindinis** „Twitter" ID. Galimo kliento kvalifikacijos proceso metu galite pateikti ir verslo telefono numerį, ir mobiliojo telefono numerį. Darbo telefono numeris laikomas pirminiu telefono numeriu, jei **IsMobile=Ne** o mobiliojo telefono numeris laikomas antriniu telefonu, jei **IsMobile=Taip**.

> [!TIP]
> Naudokite **adresų** ir **elektroninių adresų** skirtukus **sąskaitų** ir **kontaktų** formose pašto ir elektroniniams adresams valdyti. Taip užtikrinama, kad adreso duomenys bus sinchronizuojami su „Finance and Operations“ programėle.

## <a name="setup"></a>Sąranka

1. Atidarykite savo klientų įdarbinimo programos aplinką.

2. Įdiekite dvigubo rašymo (2.2.2.60 programos) instrumentavimo sprendimo [naujausią versiją](https://aka.ms/dual-write-app).

3. Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelės prendimus](https://aka.ms/dual-write-gab).

4. Atidarykite „Finance and Operations” programą. Eiti į „Data Management“ modulį ir pasirinkti dvigubo rašymo skirtuką. Atidaroma dvigubo rašymo administravimo puslapis.

5. Pritaikykite abu 2 ir 3 veiksmais įdiegtus sprendimus naudodami [sprendimo funkcijos taikykite](link-your-environment.md).

6. Sustabdykite toliau nurodytas schemas, nes jų nebereikia. Paleiskite `Contacts V2 (msdyn_contactforparties)` schemą.

    + CDS kontaktai V2 ir kontaktai (nurodo klientų kontaktus)
    + CDS kontaktai V2 ir kontaktai (nurodo tiekėjo kontaktus)

7. Atnaujinami šie šalies funkcijų objektų susiejimai, todėl šiems susiejimams turi būti taikoma naujausia versija.

    Schema | Atnaujinti į šią versiją | Pakeitimai
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Customers V3 (accounts)` | 1.0.0.5 |Pašalintas `PartyNumber` ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
    `Customer V3 (contacts)` | 1.0.0.5 | Pašalintas `PartyNumber` ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Pašalintas `PartyNumber` ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Pakeitė kontaktinį asmenį `ContactforParty` nuoroda.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Pakeitė kontaktinį asmenį `ContactforParty` nuoroda.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Pakeitė kontaktinį asmenį `ContactforParty` nuoroda.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.

8. Prieš paleisdami pirmiau pateiktas schemas, turite atnaujinti integravimo raktus rankiniu būdu, kaip aprašyta toliau aprašytus veiksmus. Tada pasirinkite **Įrašyti**.

    | Schema | Raktai |
    |-----|------|
    | Paskyra |  accountnumber [Sąskaitos numeris]<br>msdyn_company.cdm_companycode [Įmonė (įmonės kodas)] |
    | Kontaktas | msdyn_contactpersonid [sąskaitos numeris/kontaktinio asmens ID]<br>msdyn_company.cdm_companycode [Įmonė (įmonės kodas)] |
    | Kliento/tiekėjo kontaktas | msdyn_contactforpartynumber [šalies numerio kontaktas]<br>msdyn_associatedcompanyid.cdm_companycode [Susieta įmonė (Įmonės kodas)] |
    | Tiekėjas | msdyn_vendoraccountnumber [Tiekėjo sąskaitos numeris]<br>msdyn_company.cdm_companycode [Įmonė (įmonės kodas)]|

9. „Dataverse“, dublikatų aptikimo taisyklių simbolių limitas padidėjo nuo 450 iki 700 simbolių. Ši riba leidžia prie dublikatų aptikimo taisyklių pridėti vieną ar daugiau raktų. Išplėskite dublikatų aptikimo taisyklę **sąskaitų** lentelei, nustatydami šiuos laukus.

    | Laukas | Reikšmė |
    |-------|-------|
    | Pavadinimas / vardas ir (arba) pavardė | Sąskaitos tokiu pačiu sąskaitos pavadinimu. |
    | Aprašas | Aptinka sąskaitos įrašus, kurie turi tą pačią vertę atribute Sąskaitos pavadinimas. |
    | Pagrindinio įrašo tipas | Paskyra |
    | Įrašo tipo sugretinimas | Paskyra |
    | Sąskaitos pavadinimas (laukas) | Tikslus atitikimas |
    | Įmonė (laukas) | Tikslus atitikimas |
    | Ryšių tipas (laukelis) | Tikslus atitikimas |
    | Šalies ID (laukas) | Tikslus atitikimas |
    | Pasirinkti (lauką) | (tuščia) |

    ![Dubliuoti sąskaitų taisyklę.](media/duplicate-rule-1.PNG)

10. Išplėskite dublikatų aptikimo taisyklę **Kontaktų** lentelei, nustatydami šiuos laukus.

    | Laukas | Reikšmė |
    |-------|-------|
    | Pavadinimas / vardas ir (arba) pavardė | Kontaktai tokiu pačiu vardu ir pavardę. |
    | Aprašas | Aptinka kontaktų įrašus, kurių vertės lauke Vardas ir Pavardė yra tokios pačios. |
    | Pagrindinio įrašo tipas | Kontaktas |
    | Įrašo tipo sugretinimas | Kontaktas |
    | Vardas (laukas) | Tikslus atitikimas |
    | Pavardė (laukas) | Tikslus atitikimas |
    | Įmonė (laukas) | Tikslus atitikimas |
    | Šalies ID (laukas) | Tikslus atitikimas |
    | Pasirinkti (lauką) | (tuščia) |

    ![Dubliuoti kontaktų taisyklę.](media/duplicate-rule-2.PNG)

11. Jei esate esamas dvigubo rašymo vartotojas, vadovaukitės šalies ir visuotinės adresų knygelės modelio atnaujinimo instrukcijomis [ir](upgrade-party-gab.md) atnaujinkite savo duomenis.

12. Vykdykite žemėlapius tokia tvarka. Jei gaunate klaidą, kuri reiškia, kad „Projekto tikrinimas nepavyko. Trūksta paskirties lauko...", tada atidarykite schemą ir pasirinkite **Atnaujinti** lenteles. Tada paleiskite schemą.

    „Finance and Operations“ programa | „Customer engagement“ programa  
    ----------------------------|------------------------
    [CDS šalys](mapping-reference.md#220) | msdyn_parties
    [CDS pašto adreso vietos](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS pašto adreso istorija V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS šalies pašto adreso vietos.](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Šalies kontaktai V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Klientai V3](mapping-reference.md#101) | sąskaitos
    [Klientai V3](mapping-reference.md#116) | kontaktai
    [Tiekėjai V2](mapping-reference.md#202) | msdyn_vendors
    [Kontaktinio asmens pareigos](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Baigiamosios mandagumo frazės](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Pasisveikinimai](mapping-reference.md#228) | msdyn_salutations
    [Sprendimų priėmimo vaidmenys](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Įdarbinimo užduočių funkcijos](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Lojalumo lygiai](mapping-reference.md#226) | msdyn_loyaltylevels
    [Asmeninių savybių tipai](mapping-reference.md#227) | msdyn_personalcharactertypes
    [V2 kontaktai](mapping-reference.md#221) | msdyn_contactforparties
    [CDS pardavimo pasiūlymo antraštė](mapping-reference.md#215) | pasiūlymai
    [CDS pardavimo užsakymų antraštės](mapping-reference.md#217) | salesorders
    [Pardavimo SF antraštės V2](mapping-reference.md#118) | SF

> [!NOTE]
> Schema `CDS Contacts V2 (contacts)` yra schema, kurią sustabdėte 1 žingsnyje. Kai bandote paleisti kitas schemas, šios 2 schemos gali būti rodomos priklausomųjų sąraše. Neį paleiskite šių žemėlapių.
>
> Jei šalies ir visuotinės adresų knygelės sprendimas įdiegtas, turite išjungti prijungimą, `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` pavadintą. Jei šalies ir visuotinės adresų knygelės sprendimas yra išdiegtas, tada turite iš naujo įjungti priedą.
>
> Laukas `msdyn_*partynumber` (vienos eilutės teksto laukelis), įtrauktas į **Sąskaita**, **Kontaktai** ir **Tiekėjo** lenteles turi būti naudojamas einant toliau. Žymės pavadinimas turi prefiksą **(pasenusią)** už imo. Geriau naudokite msdyn_partyid **lauką**. Laukas yra lentelės msdyn_party **peržvalga**.

> Lentelės pavadinimas | Senas laukas | Naujas laukas
> --------|-------|--------
> Paskyra | `msdyn_partynumber` | `msdyn_partyid`
> Kontaktas | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Šablonai

Lentelių schemų rinkinys veikia kartu interaktyviai naudojant šalies ir bendros adresų knygelės duomenis, kaip parodyta tolesnėje lentelėje.

| „Finance and Operations“ programa | „Customer engagement“ programa | Aprašas |
|----------------------------|-------------------------|-------------|
| [Kontaktinio asmens pareigos](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Klientai V3](mapping-reference.md#101) | sąskaitos |
| [Klientai V3](mapping-reference.md#116) | kontaktai |
| [CDS šalys](mapping-reference.md#220) | msdyn\_parties |
| [CDS šalies pašto adreso vietos.](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS pašto adreso istorija V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS pašto adreso vietos](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS pardavimo pasiūlymo antraštė](mapping-reference.md#215) | pasiūlymai |
| [CDS pardavimo užsakymų antraštės](mapping-reference.md#217) | salesorders |
| [Baigiamosios mandagumo frazės](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [V2 kontaktai](mapping-reference.md#221) | msdyn\_contactforparties |
| [Sprendimų priėmimo vaidmenys](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Įdarbinimo užduočių funkcijos](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Lojalumo lygiai](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Šalies kontaktai V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Asmeninių savybių tipai](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Pardavimo SF antraštės V2](mapping-reference.md#118) | SF |
| [Pasisveikinimai](mapping-reference.md#228) | msdyn\_salutations |
| [Tiekėjai V2](mapping-reference.md#202) | msdyn\_vendors |

Daugiau informacijos žr. [Dvigubo rašymo susiejimo nuoroda](mapping-reference.md)

## <a name="known-issues-and-limitations"></a>Žinomos problemos ir apribojimai

+ „Finance and Operations“ Programėlėse, kai kartu su adresu sukuriate klientą ir jį įrašote, adresas gali būti nesinchronizuotas su **adresų** lentele. Taip yra dėl dvigubo rašymo platformos sekos išdavimo. Pirmiausia sukurkite klientą ir įrašykite jį kaip problemos sprendimą. Tada pridėti adresą.
+ Jei programėlių atveju, kai kliento įrašas turi pagrindinį adresą ir sukuriate naują to kliento kontaktą, tada kontakto įrašas perima pagrindinį adresą iš „Finance and Operations“ susieto kliento įrašo. Taip atsitinka ir tiekėjo kontaktui. „Dataverse“ šiuo metu nepalaiko šio veikimo būdo. Jei įgalintas dvigubas rašymas, kliento kontaktai, kurie paveldėti pirminiu programos adresu, sinchronizuojami kartu „Finance and Operations“ ir „Dataverse“ su jų adresu.
+ Elektroniniai adresai nustatyti elektroninių adresų skirtuke **Sąskaita**, **Kontaktas** ir **Tiekėjo** formose ateina iš `msdyn_partyelectronicaddress` lentelės. Ši informacija nėra susijusi su jos operacijomis, pvz., pardavimo užsakymu, pasiūlymu ir pirkimo užsakymu. Planuojame išspręsti šią problemą didėjančia versija. Sąskaitų ir kontaktų įrašų elektroninio adreso laukuose esantys duomenys ir toliau bus dirba su operacijomis, pvz., pardavimo užsakymu, pasiūlymu ir pirkimo užsakymu.
+ „Finance and Operations“ Programėlėse galite sukurti kontakto įrašą iš formos Įtraukti **kontaktą**. Kai formoje Peržiūrėti kontaktą bandote sukurti **naują** kontaktą, veiksmas nepavyksta. Tai yra žinoma problema.

    ![Žinomas problemos su įtraukti kontaktą.](media/party-gab-contact-issue.png)

+ **Pradinis sinchronizavimas nepalaiko Laukų Galima nuo ir**  Galimas **iki** **laiko** **, esančius ContactForParty, nes DIXF vertę konvertuoja į eilutę, o ne** į svertą. Konvertavimas suaktyvina klaidą `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32`.
+ Kai pašto adresas naudojamas dėl daugiau nei vienos priežasties, pavyzdžiui, verslo ryšio adreso ir sąskaitų siuntimo adreso, jis turėtų būti toks, kaip parodyta `Business;Invoice` toliau pateiktame paveikslėlyje. Jei tarp verčių įtrauksite tarpą, gausite klaidą.

    ![Žinomas problemos su adresu.](media/party-gab-address-issue.png)

+ Negalite įvesti pašto adreso į priekį naudodami programą, turiinę „Finance and Operations“ dvigubo rašymo datą,„ Dataverse“, nes datos poveikis nepalaikomas. Jei įvesite būsimą pašto adresą naudodami programą, jis bus visiškai sinchronizuotas ir iš karto matysite „Finance and Operations“ ir „Dataverse“ adresą vartotojo sąsajoje. Atnaujinus šį įrašą, bus klaida, nes ji yra būsima ir ne dabartine Finance and Operations programoje.
