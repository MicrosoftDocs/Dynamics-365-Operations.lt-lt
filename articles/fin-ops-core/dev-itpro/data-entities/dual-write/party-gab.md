---
title: Šalies ir bendros knygelės nustatymas
description: Šioje temoje aprašomos dvigubo rašymo šalies ir visuotinės adresų knygelės funkcijos.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750793"
---
# <a name="party-and-global-address-book"></a>Šalies ir bendros knygelės nustatymas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šalis ir visuotinė adresų knygelė yra programų „Finance and Operations“ sąvokos. Šalis gali būti organizacija ar asmuo. Tai patogu visuotinai saugoti ir tvarkyti šalies **ypatybių** pavadinimą, kalbą, kontaktus ir adresus. Kai ypatybės vertė pasikeičia vienoje vietoje, ji atspindi visas šalies **vietas**.

## <a name="party"></a>Įrašas

Šalis *yra* asmuo arba organizacija, įtraukta į verslą. Naudodamas šalies koncepciją asmuo arba organizacija gali atlikti daugiau nei vieną vaidmenį įmonėje (darbuotojas, klientas, tiekėjas arba kontaktas). Vaidmuo remiasi kontekstu ir tikslu. Štai keletas iš fiktyvių įmonių „Contoso“ ir „Fabrikam“ pavyzdžių.

+ **Darbuotojas**: darbuotojas. Pavyzdžiui, „Contoso“ darbuotojas.
+ Terminas **tiekėjas**: reiškia tiekėjų organizaciją arba individualų savininką, kuris tiekia prekes ar teikia paslaugas verslui. Pavyzdžiui, jei „Fabrikam“ parduoda atsargas „Contoso“, „Fabrikam“ atlieka tiekėjo vaidmenį.
+ **Kontaktas**: asmuo, kurį reikia susisiekti. Pavyzdžiui, jei „Contoso" perka atsargas iš „Fabrikam“, „Contoso" darbuotojas susisiektų su kontaktiniu darbuotoju „Fabrikam“.
+ **Klientas**: klientas yra asmuo arba įmonė, kuri perka dalykus iš įmonės. Pavyzdžiui, jei „Contoso“ perka atsargas iš „Fabrikam“, „Contoso“ yra „Fabrikam“ klientas.

Šalies modelis dažnai naudojamas siekiant pateikti tarpinių ir kompleksinių ryšių tarp organizacijų ir žmonių ryšius, ypač kai šalis atlieka daugiau nei vieną vaidmenį. Štai keletas bendrų pavyzdžių:

+ Šalis gali būti ir klientas, ir tiekėjas. Pavyzdžiui, Šiaurės Amerikoje „Fabrikam“ parduoda elektros iš „Contoso“ ir pirkimus surinkus iš „Contoso“. Europoje „Fabrikam“ parduoda dalis „Contoso", tačiau „Contoso" nieko neparduos.
+ Šalis gali būti ir darbuotojas, ir klientas. Pavyzdžiui, „Contoso" darbuotojas iš „Contoso" perka elektronines įrangas asmeniniam naudojimui.
+ Tarp asmens ir organizacijos gali būti įvairiais ryšiais. Pavyzdžiui, „Fabrikam“ tiekia aptarnavimo specialistams ir naudoja išdėstymo koordinates. Koordinatorius suderina kelių „Fabrikam“ klientų darbo užklausų aptarnavimo specialistus. „Contoso" yra viena iš kliento sąskaitų. Kai „Contoso" reikia specialistų, „Contoso" susisieks su koordinatoriumi, kuris palengvina užklausą. Koordinatorius tvarko visų klientų užklausas, kurs ryšį daugelis su daugeliais.

Toliau pateiktame vaizde rodomas šalies duomenų modelis:

![Duomenų modelis šaliai](media/party-gab-image1.png)

> [!Tip]
> Kai bandote sukurti naują sąskaitos įrašą, norėdami ieškoti įrašo pagal pavadinimą, naudokite lauką „Šalis“. Jei įrašą surandate, jums reikia tik pasirinkti įrašą. Sistema automatiškai užpildo visus šalies duomenis. Nereikia neautomatiniu būdu įvesti visų reikalingų laukų. Šį elgseną galima rasti sąskaitos, kontakto ir tiekėjo formose, kurios išsiųstos šiame langelyje.

Ne visi programėlių šalių „Finance and Operations“ vaidmenys palaikomi naudojant dvigubo rašymo funkciją. Visą šalies vaidmenų sąrašą rasite visuotinės adresų [knygelės](../../../fin-ops/organization-administration/overview-global-address-book.md) apžvalga.

### <a name="global-address-book"></a>Visuotinė adresų knygelė

Visuotinė adresų knygelė yra verslo organizacijų ir asmenų pašto ir elektroninių adresų katalogas.

Visuotinė adresų knygelė saugomi ir tvarko tiek pašto adresų, tiek elektroninių adresų, kiek reikia. Pavyzdžiui, tarkime, kad „Fabrikam“ turi dujų stotis 50 vietų. Kiekviena vieta turi skirtingą pašto adresą, el. pašto adresą ir telefono numerį. Visiems verslo užsakymams sąskaita išsakoma į pagrindinę dujų stotį, bet pirkimas siunčiamas tiesiai į konkrečią dujų stotį, kuri reikalauja pirkimo. Visuotinė adresų knygelėje pagrindinė dujų stotis yra sąskaitų siuntimo adresas, o kiekviena dujų stotis – kaip „Fabrikam“ siuntimo adresas. Jei reikia, pasiūlymus ir užsakymus adresai gali būti saugomi ir nuskaitomi.

Asmuo arba organizacija gali atlikti daugiau nei vieną vaidmenį verslo kontekste. Kai taip, jų pašto adresai ir elektroniniai adresai gali būti tokie patys. Šiuo atveju, adreso pakeitimas viename vaidmenyse turėtų pasirodyti ant kito vaidmens ir atvirkščiai. Visuotinė adresų knygelė saugoma ir tvarko adresus visuotinai.

![Visuotinės bendros adresų knygelės duomenų modelis](media/party-gab-image2.png)

## <a name="contacts"></a>Kontaktai

Klientų įsipareigojimo programose *kontaktinis* asmuo yra asmuo. Tačiau kontaktų lentelė buvo perkrauta siekiant atstovauti **asmenį**, portalo vartotoją, B2C klientą arba tiekėją. Vaizdas yra netiesiogiai ir jūs negalite pranešti apie skirtumą, jei nepasteėmėte susijusių operacijų. Kontaktų **lentelėje** ribojamas ryšys su sąskaitų **lentele** 1:1. Kaip šalies ir visuotinės adresų knygelės modelio dalis, dvigubo rašymo funkcija pristato tikslias klasifikavimo ir dvigubo rašymo ypatybes, leidžia N:N ryšius tarp kontaktinio asmens ir organizacijos (sąskaitos objektas arba **tiekėjo** objektas).

Yra du tipai **Kontaktų** eilučių:

+ Atskirtas kontaktas – kontakto eilutė su privaloma verte **įmonės** laukelyje.
+ Neperduotas kontaktas – kontakto eilutė, kurios laukas **Įmonė** tuščias.

Kontaktų **lentelėje gali būti šių tipų** eilutės:

Eilutės tipas | Aprašas
---|---
Asmuo, kuris yra klientas, pavyzdžiui, parduotinas kontaktinis asmuo ar B2C klientas. | Atskirtas kontakto įrašas, kur **įmonės laukas nėra tuščias ir** lauke **klientas** nustatyta reikšmė **Taip**.
Asmuo, kuris yra tiekėjas, pavyzdžiui, ind. įmonės savininkas kaip tiekėjas. | Atskirtas kontakto įrašas, kur **įmonės laukas nėra tuščias ir** lauke **Tiekėjas** nustatyta reikšmė **Taip**.
Asmuo, kuris yra klientas ir tiekėjas. | Atskirtas kontakto įrašas, kur **įmonės** laukas nėra tuščias ir **yra kleintas** nustatytas į **Taip**, o **yra tiekėjo** laukelyje nustatytas į **Taip**. Asmuo gali būti ir vieno produkto gamintojas, ir kito produkto vartotojas. Ir „Finance and Operations“ programėlės, ir dvigubo rašymo palaikymas palaiko šį ryšį.
Asmuo, kuris yra organizacijos kontaktinis asmuo, bet nėra klientas ir ne tiekėjas. | Atskirtas kontakto įrašas, kur **įmonės** laukas nėra tuščias ir **yra kleintas** nustatytas į **Ne**, o **yra tiekėjo** laukelyje nustatytas į **Ne**.

## <a name="contact-for-party"></a>Šalies kontaktas

**Šaliesk ontaktas** kontaktas ir tvarko N:N ryšius tarp **sąskaitos eilučių ir** kontaktų **eilučių**. Taip galima filtruoti atskirtas kontaktinių eilučių eilutes iš nenusidėlintose eilutėse ir susieti tik nesuslenktas kontaktų eilutes **su sąskaitos** **arba** **tiekėjo** **eilutėmis**.

Pavyzdžiui, Nataša Džauns ir Migelis Rejes yra veterinarai, kurie rūpinasi fermomis savo teritorijoje. Nataša dirba Sietlo srityje, o Migelis Kento. Klientų įsipareigojimo programoje, ūkiai yra vaizduojami klientais, o veterinarai kontaktiniais asmenimis. Vienas **Susieto** kontakto įrašas yra susietas su visais Nataša su tais pačiais ūkiais, kuriuose ji dirba. Panašiai, atskiras **Kontakto** įrašas Migeliui yra susietas su ūkiais, su kuriais jis dirba.

Šie ryšiai saugomi šalies **kontaktų** lentelėje. Informaciją galima rasti formose, kurių kodas neįeis į langelį:

+ Kai esate sąskaitos **formoje**, yra skirtukas Susietas **kontaktas**. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau kontaktų su **sąskaitos** eilute. Šioje formoje kontaktiniam asmeniui priskiriate organizacijai. Kai priskiriate kontaktus, galite pasirinkti vieną iš pagrindinių tos sąskaitos kontaktų. Naudodami **sparčiojo** kūrimo formą galite pasirinkti tik kontaktinį asmenį. Jei naudojate formą Tiekėjas, o įrašo tipas yra **Organizacija**, veikimo būdas yra **tas** pats.
+ Kai esate kontaktinio asmens formoje, o eilutė yra klientas, tiekėjas arba abu (tam tikrą kontaktą), tai yra **skirtukas** Susieti **kontaktai**. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau kontaktų su sąskaitos eilute. Šioje formoje kontaktiniam asmeniui, skirtam B2C klientui ar tiekėjui. Kai priskiriate kontaktus, galite pasirinkti vieną iš pagrindinių tos sąskaitos kontaktų. Naudodami **sparčiojo** kūrimo formą galite pasirinkti tik kontaktinį asmenį.
+ Kai esate kontaktinėje **formoje**, o eilutė yra kontaktinis asmuo (tam tikrą kontaktą), tai yra skirtukas **Susietos organizacijos**. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau klientų ar tiekėjų. Šioje formoje priskiriate klientą ar tiekėją su esančiu kontaktiniu asmeniu. Klientas arba tiekėjas gali būti organizacija, asmuo arba abu. Vienu metu galite pasirinkti tik vieną reikšmę iš keturių laukų.

    ![Skirtukas Susietos organizacijos](media/party-gab-image3.png)

    + Jei **pasirenkate įrašo** ID, pagrindinis kontaktas priskiriamas visiems pasirinktos šalies vaidmenims.
    + Jei pasirenkate **Susietas** kontaktas, tada pasirenkate atskirtą kontaktą, kurio tipas yra asmuo.
    + Jei **pasirenkate Susieta** sąskaita arba **Tiekėjas**, tada pasirenkate organizaciją.

    Nepriklausomai nuo jūsų pasirinkimo, susiejimas sukuriamas šalies lygiu ir taikomas visiems šalies vaidmenims ir saugomas objekto „Šalies kontaktas".

> [!Note]
> Klientų įsipareigojimų programoje rodomas šalies lentelės kontaktas pavadinimas yra Kliento / **tiekėjo** **kontaktas**.

Atidaryę kontakto eilutę, kurioje yra klientas ne ir tiekėjas yra Ne, matysite skirtuką Susietos organizacijos. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau **kliento** **arba** **tiekėjo** **organizacijų** **su** **kontaktu**.

Atidaryę kontakto eilutę, kurioje yra klientas ne ir tiekėjas yra nustatytas į Taip ir matysite skirtuką Susieti kontaktai. Naudokite šį skirtuką, kad susietumėte vieną ar daugiau **kliento** **arba** **tiekėjo** **organizacijų** **su** **kontaktai**.

## <a name="postal-address"></a>Pašto adresas

Sąskaitoje, **kontakte** ir tiekėjo formose **įvestas naujas** **skirtukas pavadinimu** **Adresai**. Adresai, **skirti** N adresams naudoti tinklelyje, kaip parodyta šiame paveikslėlyje:

![Pašto adreso tinklelis](media/party-gab-image4.png)

+ Stulpelis **Pašto** adreso vaidmenys išvardija adreso paskirtį.
+ Stulpelyje **Yra** pirminis sąrašas pirminio adreso.
+ **Stulpelis** Adreso numeris išvardija adreso užsakymą.
+ Mygtukas **+ naujas adresas leidžia sukurti naują** adresą. Galite sukurti tiek adresų, kiek norite.

Laukai **1 adresas ir 2 adresas, esantys sąskaitos formos skirtuke Suvestinė**, **atitinka** **pristatymo** **ir** **SF** **adresus**.

![Pašto adreso suvestinės skirtukas](media/party-gab-image5.png)

Laukeliai **Adresas 1**, **Adresas 2** ir **Adresas 3** skirtuke **Santrauka** formoje **Kontaktas** atitinka **Verslo**, **Pristatymo** bei **SF** adresus.

## <a name="electronic-address"></a>Elektroninio pašto adresas

Sąskaitoje, **Kontakto** ir tiekėjo formose **įvestas naujas** **skirtukas pavadinimu** **Elektroniani adresai**. Adresai, **skirti** N adresams naudoti tinklelyje, kaip parodyta šiame paveikslėlyje:

![Elektroninio adreso tinklelis](media/party-gab-image6.png)

+ Stulpelis **Tipas** išvardija adreso tipą.
+ Stulpelyje **Yra** pirminis sąrašas pirminio adreso.
+ Stulpelis **Tikslo** adreso vaidmenys išvardija elektroninio adreso paskirtį.
+ Mygtukas **+ naujas elektroninis adresas leidžia sukurti naują** adresą. Galite sukurti tiek adresų, kiek norite.

Elektroniniai adresai galimi tik šiame tinklelyje. Būsimuose leidimuose visi elektroninio ir pašto adreso laukai bus pašalinti iš kitų skirtukų, pvz., **skirtukų** Suvestinė ir **informacija**.

## <a name="setup-instructions"></a>Sąrankos instrukcijos

Jei esate dvigubo rašymo klientas, reikia pateikti šias nustatymo instrukcijas. Kitu atveju šį skyrių galite praleisti.

1. Sustabdykite toliau nurodytas schemas, nes jų nebereikia. Paleiskite schemą Kontaktai V2 (msdyn_contactforparties).

    + CDS kontaktai V2 ir kontaktai (nurodo klientų kontaktus)
    + CDS kontaktai V2 ir kontaktai (nurodo tiekėjo kontaktus)

2. Atnaujinami šie šalies funkcijų objektų susiejimai, todėl šiems susiejimams turi būti taikoma naujausia versija.

Schema | Atnaujinti į šią versiją | Pakeitimai
---|---|---
Klientai V3 (sąskaitos) | 1.0.0.5 |Pašalintas Šalies numeris ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
Klientas V3 (kontaktai) | 1.0.0.5 | Pašalintas Šalies numeris ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
Tiekėjai V2 (msdyn_vendors) | 1.0.0.6 | Pašalintas Šalies numeris ir kiti su šalimi susiję laukai, pvz., vardas, asmeninė informacija, pašto adreso laukai, elektroninio kontakto adreso laukai ir kt.
CDS pardavimo kainų antraštės (siūlymai) | 1.0.0.6 | Pakeitė kontaktinį asmenį ContactforParty nuoroda.
SF antraštės V2 (sąskaitos) | 1.0.0.4 | Pakeitė kontaktinį asmenį ContactforParty nuoroda.
CDS prekybos užsakymo antraštės (prekybos užsakymai) | 1.0.0.5 | Pakeitė kontaktinį asmenį ContactforParty nuoroda.
Kontaktai V2 (msdyn_contactforparties) | 1.0.0.2 | Tai yra nauja schema. Jei turite ankstesnę šalies sprendimo versiją, įsitikinkite, kad atnaujinsite šią schemą su naujausia versija, kaip nurodyta.
CDS įrašo pašto adreso vietos (msdyn_partypostaladdresses) | 1.0.0.1  | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
CDS pašto adreso retrospektyva V2 (msdyn_postaladdresses) | | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
CDS įrašo pašto adreso vietos (msdyn_postaladdresscollections) | | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.
Šalies kontaktų V3 (msdyn_partyelectronicaddresses) | | Tai nauja schema, pridėta kaip ankstesnio šalies peržiūros leidimo dalis.

## <a name="templates"></a>Šablonai

Lentelių schemų rinkinys veikia kartu interaktyviai naudojant šalies ir bendros adresų knygelės duomenis, kaip parodyta tolesnėje lentelėje.

„Finance and Operations“ programa | „Customer engagement“ programa     | Aprašas
----------------------------|-----------------------------|------------
[Kontaktinio asmens pareigos](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Klientai V3](mapping-reference.md#101) | sąskaitos |
[Klientai V3](mapping-reference.md#116) | kontaktai |
[CDS šalys](mapping-reference.md#220) | msdyn_parties |
[CDS šalies pašto adreso vietos.](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS pašto adreso istorija V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS pašto adreso vietos](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS pardavimo pasiūlymo antraštė](mapping-reference.md#215) | pasiūlymai |
[CDS pardavimo užsakymų antraštės](mapping-reference.md#217) | salesorders |
[Baigiamosios mandagumo frazės](mapping-reference.md#222) | msdyn_complimentaryclosings |
[V2 kontaktai](mapping-reference.md#221) | msdyn_contactforparties |
[Sprendimų priėmimo vaidmenys](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Įdarbinimo užduočių funkcijos](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Lojalumo lygiai](mapping-reference.md#226) | msdyn_loyaltylevels |
[Šalies kontaktai V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Asmeninių savybių tipai](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Pardavimo SF antraštės V2](mapping-reference.md#118) | SF |
[Pasisveikinimai](mapping-reference.md#228) | msdyn_salutations |
[Tiekėjai V2](mapping-reference.md#202) | msdyn_vendors |

Daugiau informacijos žr. [Dvigubo rašymo susiejimo nuoroda](mapping-reference.md)
