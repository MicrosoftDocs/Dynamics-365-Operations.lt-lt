---
title: GS1 brūkšniniai kodai ir QR kodai
description: Šioje temoje aprašoma, kaip nustatyti GS1 brūkšninius kodus ir QR kodus, kad etiketės galėtų būti nuskaitomos sandėlyje.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 702985ef9726690829e35e43d270477be318fc41
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075219"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1 brūkšniniai kodai ir QR kodai

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- Preview until 10.0.25 GA -->

Sandėlio darbuotojai dažnai turi atlikti keletą užduočių, kai, naudodami mobilųjį skaitytuvą, registruoja prekės, padėklo ar konteinerio judėjimą. Šios užduotys gali apimti ir brūkšninių kodų nuskaitymą, ir rankinį informacijos įvedimą mobiliajame įrenginyje. Brūkšniniams kodams naudojamas konkrečios įmonės formatas, kurį nustatote ir tvarkote naudodami „Microsoft Dynamics 365 Supply Chain Management“.

Siekiant užtikrinti visuotinį įmonių duomenų mainų standartą, buvo sukurti siuntimo etikečių GS1 brūkšninių kodų ir QR kodų formatai. GS1 formatai ne tik užkoduoja duomenis, bet ir leidžia naudoti iš anksto apibrėžtą *programos identifikatorių* sąrašą duomenų reikšmei nustatyti. GS1 standartas apibrėžia duomenų formatą ir įvairius duomenis, kuriuos galima naudoti norint kažką užkoduoti. Skirtingai nei senesniuose brūkšniniuose koduose, GS1 brūkšniniuose koduose gali būti keletas duomenų elementų. Todėl, vieną kartą nuskaičius brūkšninį kodą, galima užfiksuoti kelių tipų produkto informaciją, pvz., paketą ir galiojimo datą.

GS1 palaikymas sprendime „Supply Chain Management“ itin supaprastina nuskaitymo procesą sandėliuose, kuriuose padėklai ir konteineriai žymimi naudojant kodus GS1 formatu. Sandėlio darbuotojai visą reikiamą informaciją gali gauti vieną kartą nuskaitę GS1 brūkšninį kodą. Kadangi nebereikia kelis kartus nuskaityti ir (arba) rankiniu būdu įvesti informacijos, GS1 brūkšniniai kodai padeda sumažinti užduotims atlikti reikiamą laiką. Taip pat jie padeda padidinti tikslumą.

Logistikos vadovai turi nustatyti reikiamą programos identifikatorių sąrašą ir kiekvieną iš jų susieti su atitinkamais mobiliojo įrenginio meniu elementais. Tada programos identifikatorius sandėliuose galima naudoti kaip visuotinį perkėlimo ir pakavimo parametrą. Todėl visos siuntimo etiketės bus vienodo formato.

Jei nenurodyta kitaip, šioje temoje naudojamas terminas *brūkšninis kodas* reiškia ir brūkšninius kodus, ir QR kodus.

## <a name="turn-on-the-gs1-feature"></a>GS1 funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *GS1 brūkšninių kodų nuskaitymas*

## <a name="set-up-global-gs1-options"></a>Visuotinių GS1 parinkčių nustatymas

Puslapyje **Sandėlio valdymo parametrai** pateikiami keli parametrai, kuriais nustatomos visuotinės GS1 parinktys.

Norėdami nustatyti visuotines GS1 parinktis, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. „FastTab“ skirtuke **Brūkšniniai kodai** nustatykite toliau nurodytus laukus.

    - **FNC1 simbolis** – nurodykite simbolius, kurie turi būti suprantami kaip prefiksas, kai analizuojamas brūkšninis kodas.
    - **Duomenų matricos simbolis** – nurodykite simbolius, kurie turi būti suprantami kaip prefiksas, kai analizuojama duomenų matrica.
    - **QR kodo simbolis** – nurodykite simbolius, kurie turi būti suprantami kaip prefiksas, kai analizuojamas QR kodas.
    - **Grupių skyriklis** – nurodykite simbolį, kuris identifikuoja atskiras brūkšninio kodo arba QR kodo dalis.
    - **Maksimalus identifikatoriaus ilgis** – nurodykite maksimalų leidžiamą programos identifikatoriaus simbolių skaičių.

> [!NOTE]
> Prefiksai sistemai nurodo, kad brūkšninis kodas užšifruotas pagal GS1 standartą. Vienu metu įvairiais tikslais galima naudoti iki trijų prefiksų (**FNC1 simbolis**, **Duomenų matricos simbolis** ir **QR kodo simbolis**).

## <a name="gs1-application-identifiers"></a>GS1 prašymo identifikatoriai

GS1 formatai ne tik užkoduoja duomenis, bet ir leidžia naudoti iš anksto apibrėžtą programos identifikatorių sąrašą duomenų reikšmei nustatyti. Logistikos vadovai turi nustatyti reikiamą programos identifikatorių sąrašą ir kiekvieną iš jų susieti su atitinkamais mobiliojo įrenginio meniu elementais. Tada identifikatorius sandėliuose galima naudoti kaip visuotinį perkėlimo ir pakavimo parametrą. Todėl visos siuntimo etiketės bus vienodo formato.

Sistema naudoja duomenis, ypač iš anksto nustatytus programos identifikatorius, taisyklėms, kurios turi būti taikomos atitinkamai nuskaitytai informacijai, nustatyti.

Kiekvienas programos identifikatorius sistemai nurodo, kad vėlesni nuskaityto brūkšninio kodo simboliai turi būti laikomi užšifruotos informacijos bloku. Programos identifikatorių nustatymas apibrėžia, kaip sistema turi interpretuoti brūkšninį kodą ir jį įrašyti kaip reikšmę sistemoje.

Logistikos vadovai gali naudoti standartinius tarptautinius programos identifikatorius ir (arba) sukurti savus.

### <a name="load-the-standard-application-identifiers"></a>Standartinių programos identifikatorių įkėlimas

Norėdami greitai pradėti darbą, galite įkelti įprastų tarptautinių programos identifikatorių sąrašą. Jei reikia, sąrašą galite išplėsti arba redaguoti vėliau.

Norėdami įkelti standartinius programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 programos identifikatoriai**.
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**.

> [!WARNING]
> Komanda **Kurti numatytąją sąranką** panaikina visus šiuo metu nustatytus programos identifikatorius ir pakeičia juos standartiniu sąrašu. Tačiau įkėlę numatytąją sąranką, jei reikia, galite sąrašą tinkinti.

### <a name="set-up-custom-application-identifiers"></a>Pasirinktinių programos identifikatorių nustatymas

Jei kai kurie arba visi programos identifikatoriai, kuriuos naudoja jūsų įmonė, skiriasi nuo standartinio rinkinio, galite kurti savo kodus nuo pradžių arba tinkinti standartinį rinkinį taip, kaip jums reikia.

Norėdami nustatyti ir tinkinti savo GS1 programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 programos identifikatoriai**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują identifikatorių, veiksmų srityje pasirinkite **Naujas**.
    - Norėdami redaguoti esamą identifikatorių, pasirinkite identifikatorių, tada veiksmų srityje pasirinkite **Redaguoti**.

1. Nustatykite tolesnius naujo arba pasirinkto identifikatoriaus laukus.

    - **Programos identifikatorius** – įveskite programos identifikatoriaus identifikavimo kodą. Paprastai šis kodas yra dviejų skaitmenų sveikasis skaičius, tačiau jis gali būti ilgesnis. Paskutinis dešimtainių verčių skaitmuo nurodo skaitmenų po kablelio skaičių. Daugiau informacijos rasite toliau šiame sąraše pateiktame žymės langelio **Dešimtainė dalis** apraše.
    - **Aprašas** – įveskite trumpą identifikatoriaus aprašą.
    - **Fiksuotas ilgis** – pažymėkite šį žymės langelį, jei naudojant šį programos identifikatorių nuskaitomų verčių simbolių skaičius yra fiksuotas. Jei verčių ilgis kintamas, šį žymės langelį išvalykite. Tokiu atveju, naudodami grupių skyriklio simbolį, kurį nurodėte puslapyje **Sandėlio valdymo parametrai**, turite nurodyti vertės pabaigą.
    - **Ilgis** – įveskite maksimalų simbolių, kurie gali būti rodomi vertėse, nuskaitomose naudojant šį programos identifikatorių, skaičių. Jei pažymėtas žymės langelis **Fiksuotas ilgis**, numatomas tiksliai toks simbolių skaičius.
    - **Tipas** – pasirinkite vertės, nuskaitomos naudojant šį programos identifikatorių, tipą (*Skaitinė*, *Raidinė-skaitinė* arba *Data*). Numatomas datų formatas yra mmMMDD (be tarpų ir brūkšnelių).
    - **Dešimtainė dalis** – pažymėkite šį žymės langelį, jei vertėje yra numanomas dešimtainis skyriklis. Jei šis langelis pažymėtas, sistema paskutinį programos identifikatoriaus skaitmenį naudos tam, kad nustatytų skaitmenų po kablelio skaičių. Pavyzdžiui, jei programos identifikatorius yra *3205*, dešinieji penki vertės skaitmenys bus suprantami kaip esantys po dešimtainio skyriklio.

> [!NOTE]
> Puslapyje **Sandėlio valdymo parametrai** nurodomas grupių skyriklis nėra privalomas, jei vertė, po kurios seka programos identifikatorius, yra fiksuoto ilgio arba jei jo ilgis yra maksimalus (t. y., jei ilgis lygus nustatytai programos identifikatoriaus vertei **Ilgis**).

## <a name="establish-the-generic-gs1-setup"></a>Bendrosios GS1 sąrankos nustatymas

Bendroji GS1 sąranka nustato bendrų susiejimų rinkinį. Šie susiejimai kiekvieną atitinkamą mobiliųjų įrenginių programėlės įvesties lauką sutapdina su programos identifikatoriumi, kuris valdo, kaip nuskaitytų brūkšninių kodų vertės turi būti interpretuotos ir saugomos šiame lauke. Numatyta, kad šie parametrai taikomi visiems visų mobiliojo įrenginio meniu elementų nuskaitymams. Tačiau juos viename ar daugiau konkrečių laukų gali pakeisti GS1 strategija, priskirta konkrečiam meniu elementui.

Naudojant bendrąją GS1 sąranką, vienu metu galima nuskaityti tik vieną vertę. Todėl, jei iš vieno nuskaitymo norite įkelti keletą laukų verčių, turite nustatyti atitinkamų meniu elementų GS1 strategiją.

Daugiau informacijos apie GS1 strategijas rasite kitame skyriuje.

### <a name="load-the-standard-generic-gs1-setup"></a>Standartinės bendrosios GS1 sąrankos įkėlimas

Puslapyje **Bendroji GS1 sąranka** galima įkelti standartinį mobiliojo įrenginio laukų ir standartinių programos identifikatorių susiejimų, sukurtų pagal numatytąją sąranką, rinkinį.

Norėdami nustatyti bendrąją GS1 sąranką, eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> Bendroji GS1 sąranka**. Tada pasirinkite **Kurti numatytąją sąranką**, kad kiekvienam laukui, kuris paprastai naudojamas mobiliojo įrenginio meniu elementuose, būtų automatiškai priskirtas tinkamas programos identifikatorius.

> [!WARNING]
> Jei jau yra bet kokia bendroji GS1 sąranka, komanda **Kurti numatytąją sąranką** visiškai ją panaikina ir įkelia standartinę sąranką.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standartinės bendrosios GS1 sąrankos tinkinimas

Norėdami tinkinti bendrąją GS1 sąranką, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> Bendroji GS1 sąranka**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują susiejimą, veiksmų srityje pasirinkite **Naujas**.
    - Norėdami redaguoti esamą susiejimą, pasirinkite susiejimą, tada veiksmų srityje pasirinkite **Redaguoti**.

1. Nustatykite tolesnius naujo arba pasirinkto susiejimo laukus.

    - **Laukas** – pasirinkite arba įveskite mobiliųjų įrenginių programėlės įvesties lauką, kuriam turi būti priskirta gaunama vertė. Ši vertė nėra rodomas pavadinimas, kurį mato darbuotojai. Tai yra rakto pavadinimas, priskirtas pagrindinio kodo laukui. Numatytoji sąranka pateikia laukų, kurie gali būti naudingi, rinkinį ir kiekvieno lauko bei sutampančių užprogramuotų funkcijų intuityvių raktų pavadinimų. Tačiau, norint nustatyti tinkamas pasirinktis savo įdiegčiai, gali reikėti pasitarti su programavimo partneriais.
    - **Programos identifikatorius** – pasirinkite taikytiną programos identifikatorių, kaip nurodyta puslapyje **GS1 programos identifikatoriai**. Identifikatorius nustato, kaip brūkšninis kodas bus interpretuojamas ir saugomas kaip įvardytojo lauko vertė. Kai pasirenkate programos identifikatorių, lauke **Aprašas** rodomas jo aprašas.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>GS1 strategijų, kurias galima priskirti mobiliojo įrenginio meniu elementams, nustatymas

GS1 standarto paskirtis – leisti darbuotojams įkelti keletą verčių, vieną kartą nuskaičius vieną brūkšninį kodą. Siekdami šio tikslo logistikos vadovai turi nustatyti GS1 strategijas, kurios sistemai nurodo, kaip interpretuoti kelių verčių brūkšninius kodus. Vėliau galite priskirti strategijas mobiliojo įrenginio meniu elementams, kad galėtumėte valdyti, kaip brūkšninis kodas bus interpretuojamas, kai darbuotojai jį nuskaito naudodami konkretų meniu elementą.

Jei meniu elementui nepriskirta jokia GS1 strategija, sistema gali fiksuoti tik vieną vertę. Ši vertė taikoma mobiliųjų įrenginių programėlės įvesčiai, kuri pasirenkama darbuotojui atlikus nuskaitymą, kaip nurodyta bendrojoje GS1 sąrankoje. Jei GS1 strategija priskirta meniu elementui, sistema vis tiek naudoja bendrąją GS1 sąranką, kad pirmą brūkšninio kodo vertę susietų su pasirinktu lauku. Tačiau tada ji gali fiksuoti papildomas lauko vertes, kaip nurodyta taikomoje strategijoje.

### <a name="load-the-standard-specific-gs1-policies"></a>Standartinių konkrečių GS1 strategijų įkėlimas

Norėdami greitai pradėti darbą, galite įkelti GS1 strategijų rinkinį. Jei reikia, strategijas galite išplėsti arba redaguoti vėliau.

Norėdami įkelti standartinius programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 strategija**.
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**.

> [!WARNING]
> Komanda **Kurti numatytąją sąranką** panaikina visas šiuo metu nustatytas strategijas ir pakeičia jas standartiniu strategijų rinkiniu. Tačiau įkėlę numatytąją sąranką, jei reikia, galite strategijas tinkinti.

### <a name="set-up-custom-specific-gs1-policies"></a>Pasirinktinių konkrečių GS1 strategijų nustatymas

Norėdami nustatyti ir tinkinti savo GS1 strategijas, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 strategija**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują strategiją, veiksmų srityje pasirinkite **Nauja**.
    - Norėdami redaguoti esamą strategiją, pasirinkite ją sąrašo srityje.

1. Naujos arba pasirinktos strategijos antraštėje nustatykite tolesnius laukus.

    - **Strategijos pavadinimas** – įveskite strategijos pavadinimą.
    - **Aprašas** – įveskite trumpą strategijos aprašą.

1. Po antrašte esančiame „FastTab“ skirtuke susiekite laukų pavadinimus su programos identifikatoriais, kaip reikalauja dabartinė strategija. Naudokite mygtukus įrankių juostoje, kad pagal poreikį įtrauktumėte ar pašalintumėte eilutes. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Laukas** – pasirinkite arba įveskite mobiliųjų įrenginių programėlės įvesties lauką, kuriam turi būti priskirta gaunama vertė. Ši vertė nėra rodomas pavadinimas, kurį mato darbuotojai. Tai yra rakto pavadinimas, priskirtas pagrindinio kodo laukui. Numatytoji sąranka pateikia laukų, kurie gali būti naudingi, rinkinį ir kiekvieno lauko bei sutampančių užprogramuotų funkcijų intuityvių raktų pavadinimų. Tačiau, norint nustatyti tinkamas pasirinktis savo įdiegčiai, gali reikėti pasitarti su programavimo partneriais.
    - **Programos identifikatorius** – pasirinkite taikytiną programos identifikatorių, kaip nurodyta puslapyje **GS1 programos identifikatoriai**. Identifikatorius nustato, kaip brūkšninis kodas bus interpretuojamas ir saugomas kaip įvardytojo lauko vertė. Kai pasirenkate programos identifikatorių, lauke **Aprašas** rodomas jo aprašas.
    - **Rikiavimas** – kiekvienas kelių verčių brūkšninis kodas apima programos identifikatorių, po kiekvieno iš kurių nurodyta vertė, seką. Taikoma GS1 strategija nustato, kuris programos identifikatorius susiejamas su kiekvienu duomenų bazės lauku. Tačiau, jei brūkšninis kodas tą patį programos identifikatorių naudoja daugiau nei vieną kartą, sistema naudoja tvarką, kuria programos identifikatoriai rodomi kode, kad susietų juos su laukais. Eilučių, kuriose programos identifikatorius sutampa su vienos ar kelių kitų eilučių identifikatoriumi, atveju naudokite šį lauką, kad nustatytumėte tvarką, kuria apdorojamos sutampančios eilutės. Eilutė, kurios rūšiavimo vertė mažiausia, bus apdorota pirmiausia.

> [!NOTE]
> Norėdami nustatyti laukų tvarką brūkšniniams kodams, kuriuose yra daugiau nei vienas identiškas programos identifikatorius, *privalote* naudoti lauką **Rūšiavimas**.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 strategijų priskyrimas mobiliojo įrenginio meniu elementams

Pagal numatytuosius parametrus visuose mobiliojo įrenginio meniu elementuose yra įvesties laukai, kuriuose darbuotojai gali nuskaityti vieną vertę pagal bendrąją GS1 sąranką. Jei norite, kad darbuotojai galėtų nuskaityti daugiau nei vieną mobiliojo įrenginio meniu elemento lauko vertę vienu nuskaitymu, turite priskirti GS1 strategiją, atlikdami šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sukurkite arba atidarykite meniu elementą.
1. „FastTab“ skirtuke **Bendra** lauką **GS1 strategija** nustatykite kaip strategiją, taikomą meniu elementui.

## <a name="gs1-setup-example"></a>GS1 sąrankos pavyzdys

Šis pavyzdys taikomas sistemai, kurioje GS1 parinktys yra nustatytos taip, kaip nurodyta toliau.

- Puslapyje **Sandėlio valdymo parametrai** nustatomi tolesni visuotiniai parametrai.

  - **FNC1 simbolis:** *\]C1*
  - **Grupių skyriklis:** *\~*

- Puslapyje **GS1 programos identifikatoriai** šiam pavyzdžiui aktualūs tolesni programos identifikatoriai.

    | Programos identifikatorius | Aprašas | Fiksuotas ilgis | Ilgis | Tipas | Dešimtainis |
    |---|---|---|---|---|---|
    | 01 | GTIN | Pasirinkta | 14 | Skaitinis | Apmokėta |
    | 10 | Paketo numeris | Apmokėta | 20 | Raidinis ir skaitinis | Apmokėta |
    | 17 | Galiojimo data | Pasirinkta | 6 | Data | Apmokėta |
    | 30 | Gaunamas kiekis | Apmokėta | 8 | Skaitinis | Apmokėta |

- Puslapyje **Bendroji GS1 sąranka** šiam pavyzdžiui aktualūs tolesni bendrosios GS1 strategijos parametrai.

    | Laukas | Programos identifikatorius | Aprašas |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Puslapyje **GS1 strategija** yra strategija, kurios laukas **Strategijos pavadinimas** nustatytas kaip *Pirkimo gavimas*. Šioje strategijoje yra toliau nurodytos eilutės.

    | Laukas | Programos identifikatorius | Aprašas | Rūšiavimas |
    |---|---|---|---|
    | „ExpDate” | 17 | Galiojimo data | 0 |
    | „InventBatchId” | 10 | Paketo numeris | 0 |
    | Kiekis | 30 | Gaunamas kiekis | 0 |

- Puslapyje **Mobiliojo įrenginio meniu elementai** yra meniu elementas, pavadintas *Pirkimo gavimas*. Jo laukas **GS1 strategija** nustatytas kaip *Pirkimo gavimas*.

Kai pirkimo užsakymo prekės pristatomos į sandėlį, darbuotojas atlieka šiuos veiksmus.

1. Mobiliajame įrenginyje pasirinkite meniu elementą **Pirkimo gavimas**.
1. Įveskite pirkimo užsakymo numerį.
1. Pasirinkite lauką **Prekė** ir nuskaitykite šį brūkšninį kodą: *\]C10100000012345678\~3030\~10b1\~17220215*.

Dėl parametrų, kurie nustatyti šiame pavyzdyje, sistema nuskaitytą brūkšninį kodą nuskaito taip, kaip nurodyta toliau.

| Lauko raktas | Programos ID | Reikšmė | Banknotas |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Kadangi darbuotojas nuskaitė į lauką **Prekė**, pirmoji brūkšninio kodo vertė susiejama su tuo lauku. Susiejimas paimamas iš bendrosios GS1 sąrankos. |
| Kiekis | 30 | 30 | Kadangi vienu nuskaitymu fiksuojamos kelios laukų vertės, šis susiejimas ir visi likę susiejimai paimami iš GS1 strategijos, priskirtos meniu elementui **Pirkimo gavimas**. Ši vertė yra gautas kiekis. |
| „InventBatchId” | 10 | b1 | Ši vertė yra paketo ID. |
| „ExpDate” | 17 | 220215 | Datos formatas yra mmMMDD. Todėl galiojimo data yra 2022 m. vasario 15 d. |

Tada užregistruojamas gavimas, o po vieno nuskaitymo įvedamos atitinkamos duomenų bazės vertės.
