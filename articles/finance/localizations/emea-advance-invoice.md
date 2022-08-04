---
title: Išankstinės SF, skirtos Rytų Europai
description: Šiame straipsnyje pateikiama informacija apie išankstines SF Rytų Europai. Išankstinė SF yra dokumentas, kurį galite kurti klientui arba tiekėjui. Ji nurodo pardavimo užsakymo sumą, kurią reikia apmokėti iš anksto.
author: EvgenyPopovMBS
ms.date: 07/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bcf8424b311b595a114d3429fa7a3252e47e643d
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135929"
---
# <a name="advance-invoices-for-eastern-europe"></a>Išankstinės SF, skirtos Rytų Europai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie išankstines SF Rytų Europai. Išankstinė SF yra dokumentas, kurį galite kurti klientui arba tiekėjui. Ji nurodo pardavimo užsakymo sumą, kurią reikia apmokėti iš anksto. 

> [!NOTE]
> Kita pasirinktis – naudoti išankstinio mokėjimo SF funkciją. Microsoft Dynamics Nuo 365 10.0.28 finansinės versijos šią funkciją galite naudoti **nustatę** &gt; **·** &gt; **·** &gt; **·** **mokėtinų sumų nustatymo parametrus DK ir PVM ir nustatydami parinktį Naudoti išankstinio apmokėjimo SF** **parinktį** Išankstinio mokėjimo SF "FastTab" kaip **Taip.** Daugiau informacijos rasite Išankstinio apmokėjimo [SF ir išankstinių apmokėjimų atveju](../accounts-payable/prepayments-invoices-vs-prepayments.md).

Išankstinės SF funkcija suteikia galimybę atlikti tolesnes užduotis.

- Išduoti išankstines SF klientams ir sekti tų išankstinių SF būseną (**Atvira**, **Iš dalies apmokėta** arba **Uždaryta**).
- *Tik Lenkijai: registruoti* išankstinės SF operacijas ir pridėtinės vertės mokesčio (PVM) operacijas.
- Automatiškai generuoti mokėjimų žurnalo eilutes, remiantis išankstine SF.
- Susieti išankstinius mokėjimus, gautus iš klientų, su išankstinėmis SF (prieš registruojant išankstinį mokėjimą arba po to).
- Keisti užregistruotų išankstinių apmokėjimų PVM registravimą (t. y. konvertuoti išankstinį mokėjimą į mokėjimą ar mokėjimą į išankstinį apmokėjimą arba keisti registravimo datą, mokesčio tarifą ar sumą).
- *Tik Čekijos Respublika: sukurkite* mokesčių dokumentą, apmokestinamo PVM pristatymui.

Straipsnyje yra tokie skyriai:

- [Išankstinės SF, skirtos Lenkijai](#advance-invoices-for-poland)
- [Išankstinių SF gautinų sumų nustatymas](#set-up-accounts-receivable-for-advance-invoices)
- [Kliento išankstinės SF kūrimas](#create-a-customer-advance-invoice)
- [Išankstinių SF PVM](#vat-on-advance-invoices)
- [Išankstinės SF susiejimas su pardavimo užsakymu arba laisvos formos SF](#link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice)
- [Kliento išankstinės SF kūrimas iš pardavimo užsakymo](#create-a-customer-advance-invoice-from-a-sales-order)
- [Kliento išankstinės SF kūrimas naudojant laisvos formos SF](#create-a-customer-advance-invoice-from-a-free-text-invoice)
- [Išankstinės SF spausdinimas](#print-an-advance-invoice)
- [Mokėjimo pasiūlymo kūrimas naudojant išankstinę SF](#create-a-payment-proposal-from-an-advance-invoice)
- [Išankstinio mokėjimo susiejimas su išankstine SF](#link-a-prepayment-to-an-advance-invoice)
- [Išankstinės SF susiejimas su išankstiniu mokėjimu](#link-an-advance-invoice-to-a-prepayment)
- [Išankstinės SF kredito pažymos](#advance-invoice-credit-notes)
- [Čekijos mokesčių dokumentai](#tax-documents-for-the-czech-republic)
- [Išankstinių SF mokėtinų sumų nustatymas](#set-up-accounts-payable-for-advance-invoices)
- [Tiekėjo išankstinės SF kūrimas](#create-a-vendor-advance-invoice)
- [Naudoti išankstinės SF ir išankstinio apmokėjimo tvarkymo funkciją](#use-the-advance-invoice-and-prepayment-handling-functionality)
- [Čekijos PVM sumų atšaukimas](#reversing-sales-tax-amounts-for-czech-republic)

## <a name="advance-invoices-for-poland"></a>Išankstinės SF, skirtos Lenkijai

Išankstinius mokėjimus gaunančios Lenkijos įmonės turi sukurti išankstinių mokėjimų klientui SF. Ši išankstinė SF užregistruojama DK ir ji yra privalomas dokumentas, naudojamas PVM mokesčių tikslais. Išankstinėje SF apskaičiuotas mokestis turi būti pateiktas mokesčių rinkėjui.

Įvykdžius galutinį prekių pardavimą, išankstinė SF turėtų būti nurodyta pardavimo SF. Bendra pardavimo suma turi apimti išankstinius mokėjimus.

Užregistrus pardavimo SF, sudengta išankstinė SF atšaukiama. Pradinė išankstinė SF sudengiama su išankstinės SF atšaukimas.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Išankstinių SF gautinų sumų nustatymas

1. Gautinų **sumų parametrų** puslapio skirtuke **Atnaujinimai**, **Išankstinės SF** "FastTab", nustatykite šiuos laukus.

    | Laukas | Aprašymas |
    |-------|-------------|
    | Registravimo profilis | <p>*Tik Lenkijai: pasirinkite* registravimo šabloną, kurį reikia naudoti su išankstinėmis SF išrašymu.</p><p>**Svarbu:** Čekijos Respublikoje ir Vengrijoje išankstinės SF nėra laikomos apskaitos arba mokesčių dokumentais ir nėra registruojamos DK. Todėl turite palikti šį lauką tuščią šioms šalims, kad išankstinės SF nebūtų registruojamos DK.</p> |
    | Korespondentinė sąskaita | Pasirinkti korespondentinę sąskaitą. |
    | PVM grupė | Pasirinkite PVM grupę, naudotiną skaičiuojant išankstinių SF PVM. |
    | Atšaukimas kaip koregavimas | Pažymėti šį žymės langelį, jei išankstinės SF atšaukimas turi būti laikomas pataisymu. |
    | Atšaukti datą | Pažymėti šį žymės langelį norint atšaukti išankstinį apmokėjimą SF registravimo datą. |

1. Mokėjimo "**FastTab**" nustatykite šiuos laukus.

    | Laukas | Aprašymas |
    |-------|-------------|
    | Kelios išankstinio apmokėjimo datos | Pasirinkite **Priimti**, **Įspėjimas** arba **Klaida**. |
    | Datos nesutapimas | Pasirinkite **Priimti**, **Įspėjimas** arba **Klaida**. |
    | Sumos nesutapimas | Pasirinkite **Priimti**, **Įspėjimas** arba **Klaida**. |
    | Susiejimas su užregistruota išankstine SF | Pasirinkite **Priimti**, **Įspėjimas** arba **Klaida**. |
    | (CZE), (POL) Išankstinio mokėjimo tvarkymas | Pasirinkite **Išankstinis**. |

1. Skirtuke **Numeracijos** nustatykite tolesnių nuorodų numeracijas.

    - Mokesčio dokumentas
    - Mokesčių kredito pažyma
    - Išankstinė SF
    - Išankstinės SF kredito pažyma
    - Išankstinės SF atšaukimas
    - Išankstinės SF kvitas
    - Išankstinės SF kredito pažymos kvitas
    - Išankstinės SF atšaukimo kvitas

## <a name="create-a-customer-advance-invoice"></a>Kliento išankstinės SF kūrimas

1. Eiti į gautinų **sumų** &gt; **bendrąsias** &gt; **išankstines SF** &gt; **visas išankstines SF.**
1. Veiksmų srities skirtuke Išankstinė SF **pasirinkite Išankstinė** SF, norėdami **sukurti** išankstinę SF.
1. Įveskite reikiamą informaciją ir pasirinkite Registruoti, norėdami **registruoti** išankstinę SF.

Išankstinės SF būsena gali būti tokia: **Atvira**, **Iš dalies apmokėta** arba **Uždaryta**. Galite neautomatiniu būdu keisti užregistruotos išankstinės SF būseną. Pasirinkite **Būsena**, tada, **išankstinės** SF puslapio būsenos keitimas lauke **Nauja būsena**, pasirinkite naują išankstinės SF būseną.

> [!NOTE]
> Išankstinės SF būseną galite bet kada pakeisti. Negalima apdoroti uždarytų išankstinių SF operacijose.
> 
> *Tik Lenkijai: išankstinės* SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną gautinų sumų parametruose. Norėdami peržiūrėti užregistruotas operacijas, išankstinės **SF** puslapyje pasirinkite **kvitą**.

## <a name="vat-on-advance-invoices"></a>Išankstinių SF PVM

Įmonės turi įrašyti klientų išankstinių mokėjimų PVM, net jei pardavimas nebuvo baigtas. Norėdami registruoti išankstinio mokėjimo PVM, į išankstinę SF galite įtraukti eilutę, kurioje yra PVM specifikacija. Išankstinėje SF gali būti kelios eilutės, o tose eilutėse gali būti PVM specifikacijų, kurios paimtos iš pardavimo užsakymo eilučių. Todėl PVM iš išankstinio apmokėjimo galite registruoti griežtai pagal pardavimo užsakymo eilutes.

> [!NOTE]
> PVM specifikacijos kopijuojamos į **išankstinės** **·** **SF eilutes tik tada, jei mokesčio lauko tipas PVM kodų puslapyje nustatytas į Standartinis PVM** arba Sumažintas **PVM.** Kitu atveju jos kopijuojamos į išankstinės SF eilutes taip, tarsi PVM suma būtų 0 (nulis).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Išankstinės SF susiejimas su pardavimo užsakymu arba laisvos formos SF

Kiekvieną išankstinę SF galima susieti tik su vienu pardavimo užsakymu arba laisvos formos SF. Esamą išankstinę SF galite perskirti kitam pardavimo užsakymui arba laisvos formos SF, jei su išankstine SF nesusieta jokių išankstinių mokėjimų.

Norėdami susieti išankstinę SF su pardavimo užsakymu, atlikite šiuos veiksmus.

1. Puslapyje Visos **išankstinės SF** pasirinkite išankstinę SF.
1. Veiksmų srityje pasirinkite Išankstinė **SF, tada** pasirinkite **Pardavimo užsakymas**.
1. Pasirinkite pardavimo užsakymą, norimą susieti su išankstine SF, tada pasirinkite **Gerai**.

Norėdami susieti išankstinę SF su laisvos formos SF, atlikite šiuos veiksmus.

1. Puslapyje Visos **išankstinės SF** pasirinkite išankstinę SF.
1. Veiksmų srityje pasirinkite Išankstinė **SF, tada** pasirinkite Laisvos **formos SF**.
1. Pasirinkite laisvos formos SF, norėdami susieti su išankstine SF, tada pasirinkite **Gerai**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Kliento išankstinės SF kūrimas iš pardavimo užsakymo

1. Sukurkite pardavimo užsakymą arba pasirinkite esamą.
1. Pasirinkite **SF**, tada pasirinkite Generuoti **išankstinę** &gt; **SF.**
1. Puslapyje Kurti **išankstinę SF** nustatykite šiuos laukus.

    | Laukas | Aprašymas |
    |-------|-------------|
    | Procentas | Nurodykite pardavimo užsakymo išankstinio mokėjimo procentą. |
    | Korespondentinė sąskaita | Pasirinkti numatytąją korespondentinę sąskaitą, naudotimą su išankstinėmis SF išrašymu. |
    | Užsakymo naujinimas | Pasirinkite **Visi**, **Pristatyti dabar**, **Paimtas**, **Važtaraštis** arba Paimtas **kiekis ir Atsargose neesantys produktai**. Išankstinės SF suma bus apskaičiuota remiantis prekių pardavimo užsakymo sumomis. |
    | Registruoti PVM | Nurodykite, ar PVM turi būti registruojamas išankstinės SF registravimo metu. |
    | PVM registravimo data | Nurodykite datą, kada turi būti užregistruotas PVM. |
    | Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu | Nurodykite išankstinio mokėjimo registravimo šabloną. |
    | Kurti mokesčio dokumentą | Nurodykite, ar turi būti sukurtas mokesčių dokumentas. |

> [!NOTE]
> *Tik Lenkijai: išankstinės* SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną gautinų sumų parametruose.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Kliento išankstinės SF kūrimas naudojant laisvos formos SF

1. Sukurkite laisvos formos SF arba pasirinkite esamą laisvos formos SF.
1. Skirtuko SF **skyriuje** Naujas **pasirinkite** Išankstinę **SF**.

    Dabar galite sukurti naują išankstinę SF, kuri bus susieta su laisvos formos SF.

> [!NOTE]
> *Tik Lenkijai: išankstinės* SF operacijos generuojamos, jei nustatote išankstinių SF registravimo šabloną gautinų sumų parametruose.

## <a name="print-an-advance-invoice"></a>Išankstinės SF spausdinimas

- Išankstinės **SF puslapyje** pasirinkite **Spausdinti**. 

*Tik Lenkijai:* galite išspausdinti finansinio dokumento išankstinės SF dokumentą. Pasirinkite parinktį išankstinės SF registravimo metu.

*Tik Lenkijai:* pardavimo SF makete ir laisvos formos SF dokumentuose turėtų būti ši informacija apie sudengtą išankstinę SF:

- Išankstinės SF numeris
- Išankstinės SF data
- Suma be PVM, PVM suma, suma su PVM ir valiuta
- Mokesčio procentas

PVM sumų suvestinėje turi būti mokestis iš **išankstinės SF** lauko. Apmokėtiną sumą turėtų sumažinti išankstinės SF suma.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Mokėjimo pasiūlymo kūrimas naudojant išankstinę SF

Kai sukuriate naują mokėjimų žurnalą, galite automatiškai generuoti mokėjimo žurnalo eilutes pagal išankstinę SF.

1. Puslapyje Mokėjimų žurnalas **pasirinkite** išankstinio mokėjimo žurnalo **kvito** pasirinktį, tada pasirinkite **Eilutės**.
1. Žurnalo **kvito puslapyje** pasirinkite mokėjimo **pasiūlymą** &gt; **Mokėjimo pasiūlymas iš išankstinės SF**, kad sukurtumėte mokėjimo pasiūlymą iš išankstinių SF. Iš išankstinės SF paimama informacija, pvz., registravimo šablonas ir PVM grupės.

> [!NOTE]
> Nauji išankstiniai apmokėjimai bus automatiškai **susieti** **·** **su išankstinėmis SF, jei puslapio Kurti mokėjimo pasiūlymą pasirinktį Susieti išankstinius apmokėjimus ir Keisti būseną.**

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Išankstinio mokėjimo susiejimas su išankstine SF

Norėdami susieti išankstinį apmokėjimą su išankstine SF iš mokėjimo žurnalo, atlikite šiuos veiksmus.

- Atidarykite mokėjimo žurnalą, pasirinkite eilutę su išankstiniu apmokėjimu, tada pasirinkite Funkcijų **saitas** &gt; **, kad būtų išrašytos išankstinės SF.**

Norėdami susieti išankstinį apmokėjimą su išankstine SF iš **kliento operacijų puslapio**, atlikite šiuos veiksmus.

1. Pasirinkti visas **klientų** &gt; **klientų operacijas.** &gt; **·**
1. Pasirinkite mokėjimo žurnalą, pasirinkite eilutę, į kurią yra išankstinis apmokėjimas, tada pasirinkite Funkcijų **saitas** &gt; **, kad būtų išrašytos išankstinės SF.**

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Išankstinės SF susiejimas su išankstiniu mokėjimu

Norėdami susieti išankstinę SF su išankstinio apmokėjimo eilute, atlikite šiuos veiksmus.

1. Puslapyje Visos **išankstinės SF** pasirinkite išankstinę SF.
1. Veiksmų srityje pasirinkite Išankstinė SF **ir pasirinkite** Išankstinis **apmokėjimas**.
1. Pasirinkite išankstinio apmokėjimo eilutę, norimą susieti su išankstine SF, tada pasirinkite **Gerai**.

## <a name="advance-invoice-credit-notes"></a>Išankstinės SF kredito pažymos

- *Tik Lenkijai:* norėdami atšaukti išankstinę SF, galite sukurti išankstinės SF kredito pažymą ir registruoti ją DK.
- Norėdami sukurti kredito pažymą, galite sukurti naują išankstinę SF ir pasirinkti kredito **pažymą**. Tada galite pasirinkti atšauktiną išankstinę SF.
- Taip pat galite sukurti pardavimo SF, kuri turi išankstinės SF sudengimą, kredito pažymą.
- Išankstinės SF kredito pažymos SF makete pateikiama informacija apie eilutes prieš ir po koregavimo.
- *Tik Lenkijai:* DK operacijos sukuriamos užregistrus išankstinės SF kredito pažymą.

## <a name="tax-documents-for-the-czech-republic"></a>Čekijos mokesčių dokumentai

Čekijos Respublikoje galite kurti mokesčių dokumentą, pagrįstą PVM apmokestinamo pristatymo išankstinio mokėjimo informacija. Galite kurti, kurti ir rodyti, **ar kurti ir spausdinti mokesčių dokumentą išankstinio mokėjimo puslapyje, pasirinkdami Funkcijos** &gt; **mokesčių** dokumentą, o tada pasirinkdami vieną iš pasirinkčių. Mokesčių dokumente pateikiama išsami informacija apie PVM, pvz., PVM tipas, vertė ir pagrindinė suma apskaitos valiuta bei operacijos valiuta.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Išankstinių SF mokėtinų sumų nustatymas

- Puslapio **Mokėtinų sumų parametrai** skirtuke **Numeracijos** nurodykite išankstinių SF numeraciją.

## <a name="create-a-vendor-advance-invoice"></a>Tiekėjo išankstinės SF kūrimas

Galite neautomatiniu būdu kurti išankstinę SF. Be to, nauja išankstinė SF gali būti pagrįsta esamu pirkimo užsakymu.

### <a name="manually-create-a-vendor-advance-invoice"></a>Tiekėjo išankstinės SF neautomatinis kūrimas

1. Eiti į mokėtinų **sumų** &gt; **bendrąsias išankstines** &gt; **SF** &gt; **visas išankstines SF.**
1. Veiksmų srities skirtuke Išankstinė SF **pasirinkite Išankstinė** SF, norėdami **sukurti** išankstinę SF.
1. Įveskite reikiamą informaciją ir pasirinkite Registruoti, norėdami **registruoti** išankstinę SF.

Išankstinės SF būsena gali būti tokia: **Atvira**, **Iš dalies apmokėta** arba **Uždaryta**. Galite neautomatiniu būdu keisti užregistruotos išankstinės SF būseną. Pasirinkite **Būsena**, tada, **išankstinės** SF puslapio būsenos keitimas lauke **Nauja būsena**, pasirinkite naują išankstinės SF būseną.

> [!NOTE]
> Išankstinės SF būseną galite bet kada pakeisti. Negalima apdoroti uždarytų išankstinių SF operacijose.
>
> PVM specifikacijos kopijuojamos į **išankstinės** **·** **SF eilutes tik tada, jei mokesčio lauko tipas PVM kodų puslapyje nustatytas į Standartinis PVM** arba Sumažintas **PVM.** Kitu atveju jos kopijuojamos į išankstinės SF eilutes taip, tarsi PVM suma būtų 0 (nulis).

### <a name="link-an-advance-invoice-to-a-purchase-order"></a>Išankstinės SF susiejimas su pirkimo užsakymu

Kiekvieną išankstinę SF galima susieti tik su vienu pirkimo užsakymu. Esamą išankstinę SF galite perskirti kitam pirkimo užsakymui, jei su išankstine SF nesusieta jokių išankstinių mokėjimų.

Norėdami susieti išankstinę SF su pirkimo užsakymu, atlikite šiuos veiksmus.

1. Puslapyje Visos **išankstinės SF** pasirinkite išankstinę SF.
1. Veiksmų srityje pasirinkite Išankstinė **SF, tada** pasirinkite **Pirkimo užsakymas**.
1. Pasirinkite pirkimo užsakymą, norimą susieti su išankstine SF, tada pasirinkite **Gerai**.

### <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Tiekėjo išankstinės SF kūrimas naudojant pirkimo užsakymą

1. Sukurkite pirkimo užsakymą arba pasirinkite esamą.
1. Pasirinkite **SF**, tada pasirinkite Generuoti **išankstinę** &gt; **SF.**
1. Puslapyje Kurti **išankstinę SF** nustatykite šiuos laukus.

    | Laukas | Aprašymas |
    |-------|-------------|
    | Procentas | Nurodykite pirkimo užsakymo išankstinio mokėjimo procentą. |
    | Atnaujinti pirkimą | Pasirinkite pasirinktį. Išankstinės SF suma bus apskaičiuota remiantis prekių pirkimo užsakymo suma. |
    | Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu | Nurodykite išankstinio mokėjimo registravimo šabloną. |

## <a name="use-the-advance-invoice-and-prepayment-handling-functionality"></a>Naudoti išankstinės SF ir išankstinio apmokėjimo tvarkymo funkciją

Verslo procese galite naudoti **išankstinės SF** **ir** išankstinio apmokėjimo tvarkymo funkciją. Toliau pateikiamas pavyzdys.

1. Vartotojas pateikia išankstinę SF su PVM klientui išankstiniam apmokėjimui. Išankstinė SF neužregistruota DK.
2. Vartotojas sukuria ir registruoja išankstinį apmokėjimą be PVM.
3. Vartotojas sukuria išankstinio apmokėjimo tvarkymą ir susies jį su išankstine SF. Tada vartotojas registruoja išankstinio apmokėjimo tvarkymą ir sukuria mokesčio dokumentą. Sistema užregistruoja PVM DK ir sieja PVM su išankstiniu apmokėjimu.

> [!NOTE]
> Išvalykite lauko Registravimo šablonas **, esančio išankstinės** **SF "FastTab"**, esančio gautinų **sumų** parametrų skirtuke **Atnaujinimas, reikšmę**. Kai kuriate išankstinę SF, nustatykite parinktį **Registruoti mokestį** kaip **Taip**.

Norėdami sukurti išankstinio apmokėjimo tvarkymą ir susieti jį su išankstine SF, atlikite šiuos veiksmus.

1. Eikite **į gautinų** \> **sumų** klientus ir suraskite bei atidarykite kliento įrašą.
2. Veiksmų srityje pasirinkite Kliento operacijos **, pasirinkite išankstinio** \> **mokėjimo** operaciją, tada pasirinkite Išankstinio apmokėjimo **tvarkymas.**
3. Nustatykite parinktį **Transformuoti į mokėjimą** kaip **Ne**.
4. Pasirinkti **išankstinę SF** išankstinio apmokėjimo tvarkymui susieti su išankstine SF. Sistema automatiškai sukuria PVM eilutes iš išankstinės SF.
5. Užregistruokite išankstinio apmokėjimo tvarkymą. Sistema automatiškai sukuria išankstinio apmokėjimo PVM operacijas.

## <a name="reversing-sales-tax-amounts-for-czech-republic"></a>Čekijos PVM sumų atšaukimas

Norėdami rankiniu būdu nustatyti PVM sumų atšaukimo, paremto išankstinio apmokėjimo apdorojimu, **įgalinkite (Čekija) Įgalinti rankinio įvesties PVM sumų** funkciją. Informacijos apie tai, kaip įgalinti funkcijas, žr. [Funkcijų valdymo peržiūrą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

> [!NOTE]
> Ši funkcija galima tik mokėtinoms su sąskaitoms.

Kai pažymite SF operaciją sudengti pagal mokėjimą, **·** **galite atnaujinti atšaukimų PVM sumas skirtuke Atšaukti PVM sumas, skirtuke Sudengti operacijos** puslapį. Jei reikia, galite atnaujinti mokesčių sumas sudengimo **mokesčio sumos** lauke.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
