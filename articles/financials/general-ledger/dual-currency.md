---
title: Dvi valiutos
description: Šioje temoje pateikiama informacija apie dvi valiutas, kai ataskaitų valiuta naudojama kaip antroji „Microsoft Dynamics 365 for Finance and Operations“ apskaitos valiuta.
author: kweekley
manager: AnnBe
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dfd4c116552510ee42cd2f3e8a0f31100826b9d2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839407"
---
# <a name="dual-currency"></a>Dvi valiutos

[!include [banner](../includes/banner.md)]

Naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versijoje 8.1 (2018 m. spalis) įdiegta funkcija galima iš naujo nurodyti ataskaitų valiutos paskirtį ir šią valiutą naudoti kaip antrąją apskaitos valiutą. Ši funkcija vadinama *dvi valiutos*. Dviejų valiutų pakeitimų nepavyks išjungti naudojantis konfigūracijos raktu arba parametru. Kadangi ataskaitų valiuta naudojama kaip antroji apskaitos valiuta, pasikeitė ataskaitų valiutos apskaičiavimo registravimo logikoje tvarka.

Be to, patobulinti įvairūs sekimui, ataskaitų rengimui ir ataskaitų valiutos naudojimui įvairiuose procesuose skirti moduliai. Patobulinti tokie moduliai kaip **Didžioji knyga**, **Finansinės ataskaitos**, **Mokėtinos sumos**, **Gautinos sumos**, **Grynųjų pinigų ir banko valdymas** ir **Ilgalaikis turtas**. Po atnaujinimo turite atlikti tam tikrus grynųjų pinigų ir banko valdymo ir ilgalaikio turto veiksmus. Todėl būtinai atidžiai perskaitykite atitinkamus šios temos skyrius.

## <a name="posting-process"></a>Registravimo procesas

Pakeista visų operacijų, kurių metu didžiojoje knygoje kuriamas apskaitos įrašas, registravimo logika. Toliau nurodyta, kaip anksčiau buvo skaičiuojama ataskaitų valiuta.

Suma operacijos valiuta \> Suma apskaitos valiuta \> Suma ataskaitų valiuta

Pavyzdžiui, valiuta, kuria įvedama operacija yra Kanados doleris (CAD). CAD suma konvertuojama į apskaitos valiutą, kuri yra JAV doleris (USD). Paskui USD suma konvertuojama į ataskaitų valiutą, kuri yra euras (EUR). Todėl turi būti nurodyti valiutos kursai tarp CAD ir USD ir tarp USD ir EUR.

Toliau pateiktas naujas skaičiavimas.

Suma operacijos valiuta \> Suma apskaitos valiuta

Suma operacijos valiuta \> Suma ataskaitų valiuta

Kadangi atliktas šis pakeitimas, turi būti nurodyti valiutos kursai tarp CAD ir USD ir tarp CAD ir EUR.

## <a name="reports-and-inquiries"></a>Ataskaitos ir užklausos

Įvairiose ataskaitose ir užklausose dabar nurodomos sumos ne tik ataskaitų valiuta, bet ir apskaitos valiuta. Atnaujintos ne visos ataskaitos ir užklausos. Pavyzdžiui, ataskaitos, kuriose nurodytos tik sumos operacijos valiuta, nepakeistos.

Keitimai atliekami pagal vieną iš dviejų modelių.

- Jei ataskaitoje arba užklausoje buvo pakankamai vietos, kad sumas būtų galima nurodyti ne tik apskaitos valiuta, bet ir ataskaitų valiuta, įtrauktos sumos ataskaitų valiuta.
- Jei ataskaitoje arba užklausoje nebuvo pakankamai vietos, kad sumas būtų galima nurodyti abiejomis valiutomis, įtraukta parinktis, kad vartotojai galėtų pasirinkti, kuria valiuta nurodomos sumos.

Į įvairias ataskaitas ir užklausas taip pat buvo įtraukta logika nebesiųsti sumų ataskaitų valiuta, jei ataskaitų valiuta yra tokia pati kaip apskaitos valiuta, arba jei juridinio subjekto didžiojoje knygoje nebuvo nurodyta ataskaitų valiuta.

## <a name="financial-journals"></a>Finansiniai žurnalai

Atnaujinti finansiniai žurnalai (pvz., pagrindinis žurnalas ir tiekėjo SF žurnalas), kad juose būtų įtraukta papildoma informacija apie ataskaitų valiutą. Dabar bendrosios kvito ir žurnalo sumos nurodomos ataskaitų valiuta. Be to, dabar žurnalo eilučių skirtuke **Bendra** rodoma informacija apie ataskaitų valiutos keitimo kursą. Todėl įvesdami operacijas galite nepaisyti ataskaitų valiutos keitimo kurso.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Tiekėjo SF, pardavimo užsakymai ir pardavimo sutartys
Buvo atnaujintos tiekėjo SF, pardavimo užsakymai ir pardavimo sutartys, kad būtų įtrauktas fiksuotas valiutos kursas, skirtas ataskaitai. Fiksuotas valiutos kursas gali būti nustatytas tiek apskaitos valiuta, tiek ataskaitų valiuta, kai skiriasi operacijos valiuta. Kai apskaitos valiuta ir ataskaitų valiuta sutampa, fiksuotas valiutos kursas bus sinchronizuojamas naudojant apskaitos valiutos fiksuotą tarifą kaip ataskaitų valiutos fiksuotas kursas. Šios konfigūracijos ataskaitos valiutos fiksuoto valiutos kurso keisti negalima. Kai apskaitos valiuta ir ataskaitos valiuta skiriasi, fiksuotas valiutos kursas gali būti nustatytas tiek apskaitos valiuta, tiek ataskaitų valiuta įvedant operacijas. Jei ataskaitos valiuta nebuvo nurodyta didžiojoje knygoje, laukas **Ataskaitų valiutos fiksuotas valiutos kursas** lieka neįgalintas, o ataskaitos valiutos suma neapskaičiuojama.

## <a name="module-changes"></a>Modulių pakeitimai

Toliau išvardyti moduliai ataskaitų valiutą naudoja kaip antrąją apskaitos valiutą.

- [Didžioji knyga](#general-ledger)
- [Finansinės ataskaitos](#financial-reporting)
- [Mokėtinos sumos](#accounts-payable-and-accounts-receivable)
- [Gautinos sumos](#accounts-payable-and-accounts-receivable)
- [Grynųjų pinigų ir banko valdymas](#cash-and-bank-management)
- [Ilgalaikis turtas](#fixed-assets)

### <a name="general-ledger"></a>DK

Jei ataskaitų valiuta buvo nurodyta DK, DK jau buvo sekamos ataskaitų valiuta pateiktos kiekvieno apskaitos įrašo sumos. Tačiau dabar šios sumos konvertuojamos iš operacijos valiuta pateiktų sumų.

Atlikti toliau nurodyti modulio **Didžioji knyga** pakeitimai.

- DK galima nurodyti atskirą ataskaitų valiutos kurso tipą. Jei organizacija nenori naudoti kito valiutos kurso tipo, lauką, kuriame nurodomas ataskaitų valiutos kurso tipas, galite palikti tuščią. Taip pat galite pasirinkti tą patį valiutos kurso tipą, kuris naudojamas apskaitos valiutai. Jei laukas paliekamas tuščias, sistema naudoja apskaitos valiutos kurso tipą.
- Naudojant naują žurnalą (ataskaitų valiutos koregavimo žurnalą) atliktus koregavimus DK sąskaitose galima registruoti tik ataskaitų valiuta. Naudojantis šiuo žurnalu galima registruoti tik DK sąskaitose. Jis nepalaiko vidinės įmonės ir valiuta turi būti juridinio subjekto, kuriame žurnalas registruojamas, ataskaitų valiuta. Užregistravus žurnalą, operacijos valiuta ir apskaitos valiuta pateiktos sumos yra 0 (nulis), o ataskaitų valiuta pateikta suma registruojama nurodant tokią sumą, kuri buvo įvesta operacijoje. Kadangi pasikeitė ataskaitų valiutos naudojimo moduliuose **Mokėtinos sumos**, **Gautinos sumos** ir **Ilgalaikis turtas** pobūdis, šis žurnalas gali būti naudojamas po atnaujinimo atliekamiems koregavimams. Pavyzdžių, kuriuose vaizduojama, kaip naudoti šį žurnalą, ieškokite tiems moduliams skirtuose skyriuose.
- Laikotarpio paskirstymo procesas atnaujintas taip, kad būtų paskirstomos operacijos, apskaitos ir ataskaitų valiutomis nurodytos sumos. Anksčiau buvo skirstomos operacijos ir apskaitos valiuta nurodytos sumos, paskui suma apskaitos valiuta būdavo konvertuojama į sumą ataskaitų valiuta. Todėl DK sąskaitos balansas gali likti nurodytas ataskaitų valiuta. Dabar, kai sumos apskaičiuojamos ir naudojamos apskaitos įraše, konvertavimas nevyksta.
- Įvykus užsienio valiutos kurso pasikeitimo procesui jau pakeistos ataskaitų valiuta nurodytos sumos. Tačiau suma ataskaitų valiuta dabar apskaičiuojama naudojant sumą operacijos valiuta, kaip aprašyta ankstesniame šios temos skyriuje [Registravimo procesas](#posting-process).
- Daugumoje DK ataskaitų ir užklausų jau buvo nurodyta ataskaitų valiuta, bet keliose ji nebuvo nurodyta. Vienas pavyzdys – sąrašo puslapis **Bandomasis balansas**. Šiame sąrašo puslapyje dabar pateikiami stulpeliai, skirti sumoms apskaitos valiuta ir ataskaitų valiuta. Atkreipkite dėmesį į tai, kad jei apskaitos valiuta ir ataskaitų valiuta sutampa arba jei DK ataskaitų valiuta nenurodyta, stulpeliai, kuriuose nurodomos sumos ataskaitų valiuta, paslėpti.

### <a name="financial-reporting"></a>Finansinės ataskaitos

Naudodamiesi patobulintu moduliu **Finansinės ataskaitos** sumas ataskaitų valiuta į finansinę ataskaitą galite įtraukti dviem būdais. Stulpelio apraše galite pateikti tiesioginę ataskaitą dėl DK registruotų sumų ataskaitų valiuta (nauja funkcija). Arba galite ir toliau konvertuoti apskaitos valiuta nurodytas sumas į sumas ataskaitų valiuta (esama funkcija).

Šis pakeitimas prieinamas naudojantis stulpelio aprašo nustatymu **Valiutos rodinys**. Jei pasirinksite **Ataskaitų valiuta iš DK**, stulpelyje esančios sumos nekonvertuojamos. Ataskaitos apie jas parengiamos tiesiogiai iš DK. Jeigu norite, kad stulpelyje būtų rodomos konvertuotos sumos, pasirinkite parinktį **Konvertuoti į XXXX**, kai *XXXX* yra stulpelyje turima nurodyti ataskaitų valiuta. Šiuo atveju, naudojantis esama konvertavimo funkcija, apskaitos valiuta nurodytos sumos bus konvertuojamos į pasirinktą valiutą.

### <a name="accounts-payable-and-accounts-receivable"></a>Mokėtinos sumos ir gautinos sumos

Moduliai **Mokėtinos sumos** ir **Gautinos sumos** jau sekė sumas ataskaitų valiuta. Tačiau sumos nebuvo rodomas arba naudojamos įvairiems procesams. Atlikti toliau nurodyti pakeitimai.

- Sumos ataskaitų valiuta dabar rodomos klientų ir tiekėjų operacijose. Taip pat rodomos kiekvienos operacijos atviro balanso sumos ataskaitų valiuta.
- Atnaujintas skirstymo pagal terminus procesas, kad organizacija skirstymo pagal terminus rinkinius galėtų peržiūrėti apskaitos valiuta arba ataskaitų valiuta.
- Atnaujintos įvairios užklausos ir ataskaitos, kad jose būtų nurodomos sumos ataskaitų valiuta. Pavyzdžiai – ataskaitos **Kliento ir DK suderinimas** ir **Tiekėjo ir DK suderinimas**.
- Įvykus užsienio valiutos kurso pasikeitimo procesui jau pakeistos ataskaitų valiuta nurodytos sumos. Tačiau suma ataskaitų valiuta dabar apskaičiuojama naudojant sumą operacijos valiuta, kaip aprašyta skyriuje [Registravimo procesas](#posting-process).
- **Atnaujinimo aplinkybės.** Prieš atnaujinimą dokumentuose (sąskaitose faktūrose, mokėjimuose ir pan.) nurodomos sumos ataskaitų valiuta apskaičiuojamos naudojant apskaitos valiutą. Pavyzdžiui, SF užregistruojama prieš organizacijos atnaujinimus ir neapmokama. Vykdant atnaujinimą SF apskaitos įrašas nekeičiamas. Tačiau po atnaujinimo galioja dviejų valiutų pakeitimai. Todėl apmokėjus SF mokėjime ataskaitų valiuta nurodoma suma dabar apskaičiuojama naudojant sumą operacijos valiuta. Sudengus mokėjimą ir SF, gali būti apskaičiuota nežymių gauto pelno / nuostolių sumos skirtumų, nes sumos ataskaitų valiuta dabar skaičiuojamos kitaip. Jei manoma, kad apskaičiuotas skirtumas didelis, naudojantis naujoju ataskaitų valiutos koregavimo žurnalu galima pakoreguoti tik ataskaitų valiuta nurodytą gauto pelno / nuostolio ir DK sąskaitų mokėtinų sumų / gautinų sumų balansą.

### <a name="cash-and-bank-management"></a>Grynųjų pinigų ir banko valdymas

Anksčiau modulis **Ilgalaikis turtas** nesekdavo kiekvienoje ilgalaikio turto knygoje registruotoms operacijoms skirtų ataskaitų valiuta nurodytų sumų. Po atnaujinimo automatiškai sekamos visų užregistruotų naujų operacijų ataskaitų valiuta nurodytos sumos. Tačiau sumas ataskaitų valiuta būtina įtraukti į pirmiau užregistruotas papildomos knygos operacijas.

- **Atnaujinimo aplinkybės.** Kadangi ilgalaikio turto knygos operacijos anksčiau nesekė ataskaitų valiutos, pridėtas vedlys, kad į ilgalaikio turto knygos operacijas galėtumėte įtraukti sumas ataskaitų valiuta. Šis vedlys **neatlieka** pakartotinio registravimo didžiojoje knygoje. Jis atnaujina iš didžiosios knygos gautas ataskaitų valiuta nurodytas sumas pagalbinės knygos lentelėse.

    - Norėdami paleisti vedlį, paspauskite **Grynųjų pinigų ir banko valdymas** \> **Sąranka** \> **Įtraukti sumas ataskaitų valiuta į banko sąskaitos operacijas**.
    - Vedlys rodo visų dabartinės bendrovės ilgalaikio turto knygų operacijas, kurių suma ataskaitų valiuta yra 0 (nulis). Įtraukiamos tik prieš atnaujinimą užregistruotos operacijos.
    - Vedlys didžiojoje knygoje suranda atitinkamus kiekvienos banko sąskaitos operacijos apskaitos įrašus ir įveda numatytąją ataskaitų valiuta nurodytą sumą. Nors sumas galima redaguoti, rekomenduojame jų **neredaguoti**. Priešingu atveju gali nepavykti banko sąskaitų balansų suderinti su DK. Sumą galite redaguoti tik tuo atveju, jei ataskaitų valiuta nurodytos sumos nėra didžiojoje knygoje. Tokiu atveju vedlio rodoma ataskaitų valiuta išreikšta suma bus 0 (nulis).
    - Jei vedlyje paspausite **Atšaukti**, banko sąskaitos operacijos ir visi ataskaitų valiuta nurodytų sumų pakeitimai saugomi tol, kol kitą kartą paleisite vedlį. Tačiau banko sąskaitos operacijoms skirtos sumos ataskaitų valiuta neatnaujinamos. Šis atnaujinimas atliekamas tik vedlyje paspaudus **Baigti**. Vedlį galite paleisti kelis kartus. Todėl suklydę galite pataisyti visas neteisingai įvestas ataskaitų valiuta nurodytas sumas.

- Nėra pakeistų grynųjų pinigų ir banko valdymo procesų, tačiau atnaujintos įvairios ataskaitos ir užklausos, kad jose būtų rodomos sumos ataskaitų valiuta. Grynųjų pinigų srautų prognozės ataskaitos yra išimtis. Jos nebuvo atnaujintos, kad būtų įtrauktos ataskaitų valiuta nurodytos sumos.

### <a name="fixed-assets"></a>Ilgalaikis turtas

Anksčiau modulis **Ilgalaikis turtas** nesekdavo kiekvienoje ilgalaikio turto knygoje registruotoms operacijoms skirtų ataskaitų valiuta nurodytų sumų. Po atnaujinimo automatiškai sekamos visų užregistruotų naujų operacijų ataskaitų valiuta nurodytos sumos. Tačiau sumas ataskaitų valiuta būtina įtraukti į pirmiau užregistruotas papildomos knygos operacijas.

Be to, atlikti dideli nusidėvėjimo proceso pakeitimai. Atlikus šiuos pakeitimus po atnaujinimo būtini vartotojo veiksmai. Svarbu perskaityti ir suprasti toliau išvardytus pakeitimus, net jei dar nenaudojate ilgalaikio turto.

- Pasikeitė tai, kaip nusidėvėjimo procesas nustato sumą ataskaitų valiuta. Toliau minimu atveju palyginama, kaip nusidėvėjimas nustatydavo sumą ataskaitų valiuta anksčiau ir kaip nustato šią sumą dabar.

    **Nusidėvėjimo scenarijus**

    Turtas įsigyjamas ir užregistruojamas nurodant toliau pateiktas sumas. Atkreipkite dėmesį į tai, kad ataskaitų valiuta nurodyta suma registruojama DK, bet nėra saugoma ilgalaikio turto papildomos knygos lentelėse.

    | Operacijos tipas | Operacijos suma | Valiutos kursas | Suma apskaitos valiuta | Valiutos kursas | Suma ataskaitų valiuta |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Įsigijimas      | 1,000,000 DKK      | 2,0           | 500,000 USD                | 2,5           | 200,000 EUR               |

    **Ankstesnis ataskaitų valiutos nusidėvėjimas**

    Metų gale vykdomas nusidėvėjimo pasiūlymas ir apskaičiavus gaunamos toliau nurodytos sumos.

    | Operacijos tipas | Operacijos suma | Valiutos kursas | Suma apskaitos valiuta | Valiutos kursas | Suma ataskaitų valiuta |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Nusidėvėjimas     | 50,000 USD         | 1,0           | 50,000 USD                 | 2,6           | 19,230.77 EUR             |

    Vykdant nusidėvėjimo pasiūlymą jis, panaudodamas nusidėvėjimo metodą, apskaičiuoja sumą apskaitos valiuta. Paskui, panaudojant dabartinį valiutos kursą tarp USD ir EUR, ta suma konvertuojama į ataskaitų valiuta išreikštą sumą. Dėl šio konvertavimo kyla problemų, kadangi, naudojant momentinį kursą, ataskaitų valiuta išreikštas turtas negali būti visiškai nusidėvėjęs.

    **Naujas ataskaitų valiutos nusidėvėjimas**

    Pakeistas nusidėvėjimo procesas, kad ataskaitų valiuta išreikšta suma taip pat būtų apskaičiuojama naudojant nusidėvėjimo metodą. Toliau pateikiami rezultatai, gauti tuo atveju, kai vykdomas turto nusidėvėjimas.

    | Operacijos tipas | Operacijos suma | Valiutos kursas | Suma apskaitos valiuta | Valiutos kursas                                                       | Suma ataskaitų valiuta |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Nusidėvėjimas     | 50,000 USD         | 1,0           | 50,000 USD                 | 2,5<blockquote>[!NOTE] Nors rodomas šis valiutos kursas, jis nenaudojamas konvertuojant į ataskaitų valiutą.</blockquote> | 20,000 EUR                |

    Vykdant nusidėvėjimo pasiūlymą, jis, naudodamas nusidėvėjimo metodą, apskaičiuoja sumą apskaitos valiuta ir sumą ataskaitų valiuta. Paskui sumos naudojamos DK apskaitos įraše. Konvertavimas, siekiant nustatyti sumą ataskaitų valiuta, neatliekamas.

- **Atnaujinimo aplinkybės.** Kadangi ilgalaikio turto knygos operacijos anksčiau nesekė ataskaitų valiutos, pridėtas vedlys, kad į ilgalaikio turto knygos operacijas galėtumėte įtraukti sumas ataskaitų valiuta. Šis vedlys **neatlieka** pakartotinio registravimo didžiojoje knygoje. Kadangi nusidėvėjimo pasiūlymas sumą ataskaitų valiuta dabar apskaičiuoja kitaip, norint, kad organizacija galėtų įvesti bet kokias nusidėvėjimo operacijas, **būtina** paleisti ir atlikti kiekvienos bendrovės vedlio veiksmus.

    - Norėdami paleisti vedlį, paspauskite **Ilgalaikis turtas** \> **Sąranka** \> **Įtraukti sumas ataskaitų valiuta į ilgalaikio turto knygas**.
    - Vedlys rodo visų dabartinės bendrovės ilgalaikio turto knygų operacijas, kurių suma ataskaitų valiuta yra 0 (nulis). Įtraukiamos tik prieš atnaujinimą užregistruotos operacijos.
    - Vedlys ataskaitų valiuta išreikštas sumas gauna **ne** iš didžiosios knygos. Kaip aprašyta ankstesniame scenarijuje, pirmiausia DK užregistruotos sumos ataskaitų valiuta netinkamai panaudojo momentinį kursą. Šios sumos neturėtų būti rodomos ilgalaikio turto papildomoje knygoje, kadangi atlilekant kitą nusidėvėjimo skaičiavimą bus naudojamos netinkamos sumos. Todėl vedlys nustato pirmojo įsigijimo dienos valiutos kursą. Paskui jis naudoja tą valiutos kursą rekomenduodamas ataskaitų valiuta išreikštą sumą, kuri turėtų būti registruojama papildomoje knygoje. Pavyzdžiui, toliau pateikiami galimi ankstesnio scenarijaus vedlio rodmenys.

        | Ilgalaikis turtas | Rezervuoti      | Operacijos tipas | Operacijos data | Valiuta | Suma operacijos valiuta | Suma  | Valiutos kursas | Suma ataskaitų valiuta |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Įsigijimas      | 6/3/2016         | DKK      | 1 000 000                      | 500,000 | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Nusidėvėjimas     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Nusidėvėjimas     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Nusidėvėjimas     | 6/3/2016         | DKK      | 50 000                         | 50 000  | 2,5       | 250,000                   |

    - Daugelis klientų sekė savo turto operacijų duomenis pasižymėdami juos darbaknygėse. Prie šių duomenų priskiriami valiutos kursai ir sumos. Jei turite šiuos duomenis darbaknygėje, galite sukurti pasirinktinį valiutos kurso tipą ir jį atnaujinti, pasinaudodami darbaknygėje nurodytais valiutos kursais. Tada šis valiutos kurso tipas bus naudojamas įvedant numatytąjį valiutos kursą įsigijimo dieną ir apskaičiuojant sumą ataskaitų valiuta. Jeigu valiutos kurso tipas nepasirinktas, vedlys naudoja didžiojoje knygoje nurodytą valiutos kurso tipą.
    - Valiutos kursą ir sumas ataskaitų valiuta galima pakeisti. Pasikeitus valiutos kursui, ataskaitų valiuta nurodyta suma perskaičiuojama naudojant naują kursą.
    - Jei vedlyje paspausite **Atšaukti**, ilgalaikio turto knygos operacijos ir visi valiutos kurso ar ataskaitų valiuta nurodytų sumų pakeitimai saugomi tol, kol kitą kartą paleisite vedlį. Tačiau ilgalaikio turto knygos operacijoms skirtos sumos ataskaitų valiuta neatnaujinamos. Šis atnaujinimas atliekamas tik vedlyje paspaudus **Baigti**. Vedlį galite paleisti kelis kartus. Todėl suklydę galite pataisyti visas neteisingai įvestas ataskaitų valiuta nurodytas sumas.
    - Visiškai atnaujinus papildomoje knygoje pateikiamas sumas ataskaitų valiuta, **būtina** nustatyti klausimo **Ar atnaujinote visas ataskaitų valiuta nurodytas ilgalaikio turto knygos operacijų sumas?** parinktį **Taip**, o paskui paspausti **Baigti**. Nenustačius klausimo **Ar atnaujinote visas ataskaitų valiuta nurodytas ilgalaikio turto knygos operacijų sumas?** parinkties **Taip** nusidėvėjimo skaičiavimų užbaigti nepavyks. Nustačius parinktį **Taip**, vedliu naudotis nebegalima.
    - Atnaujinus papildomos knygos ilgalaikio turto operacijas nurodant sumas ataskaitų valiuta, šios sumos nesutaps su iš pradžių didžiojoje knygoje užregistruotomis sumomis. Tačiau norint atnaujinti DK nusidėvėjimo knygos sąskaitų balansus, kad jie atitiktų iš pradžių užregistruotas sumas, galima naudoti ataskaitų valiutos koregavimo žurnalą.
    - Naudodamiesi nauju į darbo sritį **Duomenų valdymas** įtrauktu objektu **Turto operacijoms skirtos sumos ataskaitų valiuta** galite eksportuoti vedlio duomenis. Paskui, naudodamiesi šiais duomenimis, galite nustatyti ilgalaikio turto nusidėvėjimo operacijų papildomos knygos balansą. Tada šį balansą galima panaudoti nustatant DK ataskaitų valiutos koregavimo sumą.

- **Atnaujinimo aplinkybės.** Įtraukta naujų ilgalaikio turto sąrankos laukų, kurie naudojami apskaičiuojant nusidėvėjimą. Prieš atliekant kitą nusidėvėjimo skaičiavimą šiuos laukus gali tekti atnaujinti.

    - Ilgalaikio turto knygoje (**Ilgalaikis turtas** \> **Knygos**), atsirado naujas „FastTab“ skirtuko **Bendra** laukas **Įsigijimo kaina ataskaitų valiuta**.
    - Ilgalaikio turto knygoje (**Ilgalaikis turtas** \> **Knygos**), atsirado naujas „FastTab“ skirtuko **Nusidėvėjimas** laukas **Numatoma likvidacinė vertė ataskaitų valiuta**.
    - Ilgalaikio turto parametruose (**Ilgalaikis turtas** \> **Sąranka** \> **Ilgalaikio turto parametrai**) atsirado naujas „FastTab“ skirtuko **Bendra** laukas **Minimali nusidėvėjimo suma ataskaitų valiuta**.
    - Knygose (**Ilgalaikis turtas** \> **Sąranka** \> **Knygos**) atsirado du nauji „FastTab“ skirtuko **Bendra** laukai: **Suapvalinti nusidėvėjimą ataskaitų valiuta** ir **Balansinę vertę palikti ataskaitų valiuta**.

- Kadangi nusidėvėjimo pasiūlymas sumas dabar skaičiuoja apskaitos valiuta ir ataskaitų valiuta, atnaujintas ilgalaikio turto žurnalas, kad jame būtų rodomos ataskaitų valiuta išreikštos nusidėvėjimo sumos. Nusidėvėjimo operacijoms visada naudojama apskaitos valiuta. Todėl šios sumos ir toliau bus rodomos stulpeliuose **Debetas** ir **Kreditas**. Tinklelyje įtraukti du nauji stulpeliai: **Debetas ataskaitų valiuta** ir **Kreditas ataskaitų valiuta**.

    - Naujais laukais galima naudotis tik tada, kai naudojamas vienas iš šių keturių nusidėvėjimo operacijos tipų: **Nusidėvėjimas**, **Nusidėvėjimo koregavimas**, **Visiškas nusidėvėjimas** arba **Specialioji nusidėvėjimo nuolaida**.
    - Jei nusidėvėjimo operacijos tipas įvedamas ilgalaikio turto žurnale, sumos ataskaitų valiuta rodomos naujuose stulpeliuose. Šias sumas galima pakeisti.
    - Jei DK apskaitos valiuta ir ataskaitų valiuta sutampa, sumos sinchronizuojamos. Pakeitus sumą **Kreditas** automatiškai pakeičiama suma **Kreditas ataskaitų valiuta**, kad jos sutaptų.
    - Ilgalaikio turto žurnale įvedus bet kokį kitą operacijos tipą, sumos **Debetas ataskaitų valiuta** ir **Kreditas ataskaitų valiuta** nerodomos nei prieš registravimą, nei po jo. Sumos apskaitos valiuta ir ataskaitų valiuta vis dar matomos DK registruojamame kvite.
