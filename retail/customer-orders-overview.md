---
title: "Klientų užsakymų apžvalga"
description: "Šioje temoje pateikta informacija apie klientų užsakymus iš mažmeninės prekybos šiuolaikinės POS (MPOS). Klientų užsakymus yra taip pat žinomas kaip specialūs užsakymai. Tema yra susiję parametrai ir sandorių srautų."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Klientų užsakymų apžvalga

Šioje temoje pateikta informacija apie klientų užsakymus iš mažmeninės prekybos šiuolaikinės POS (MPOS). Klientų užsakymus yra taip pat žinomas kaip specialūs užsakymai. Tema yra susiję parametrai ir sandorių srautų.

Omni-kanalo mažmeninės prekybos pasaulyje, daugelis mažmenininkų suteikti klientui galimybę užsakymus arba specialius užsakymus, įvairių produktų ir vykdymo reikalavimus. Štai keletas tipiškų scenarijai:

-   Klientas nori produktai pristatomi konkretų adresą tam tikrą dieną.
-   Klientas nori pasiimti produktų iš parduotuvės arba vietą, kuris skiriasi nuo parduotuvėje arba vieta, kur klientas įsigyti šiuos produktus.
-   Klientas nori kažkas pasiimti produktus, klientas įsigijo.

Mažmenininkams taip pat naudoti klientų užsakymus iki minimumo sumažinti prarastus pardavimus, kad atsargų tiekimo pertrūkių gali kitaip sukelti, nes prekes gali pristatyti arba skirtingu laiku arba vietos pakėlė.

## <a name="set-up-customer-orders"></a>Nustatyti klientų užsakymus
Štai keletas parametrų, kurie gali būti nustatyti į **mažmeninė parametrai** puslapį ir nustatyti, kaip laikomasi klientų užsakymus:

-   **Numatytasis indėlių procentais** – nurodykite suma, kurią klientas privalo sumokėti kaip užstatą kol galima patvirtinti užsakymą. Numatytasis indėlio suma apskaičiuojama kaip procentinė dalis nuo užsakymo sumos. Priklausomai nuo to, privilegijos, parduotuvėje bendradarbis galėtų nepaisyti suma naudojant **deponuoti nepaisyti**.
-   **Atšaukimo mokestis procentais** – jei mokestis bus taikomas, kai kliento užsakymas atšaukiamas, nurodyti, kad mokesčio dydis.
-   **Atšaukimo mokestis kodą** -jei mokestis bus taikomas kai kliento užsakymas atšaukiamas, kad nemokamai atspindės pagal mokesčio kodas pardavimo užsakymo, Microsoft Dynamics AX. Naudokite šį parametrą norėdami nurodyti atšaukimo mokesčio kodas.
-   **Laivybos PAP** – mažmenininkai gali imti papildomą mokestį už laivybos prekes pirkėjui. Kad siuntimo mokesčio suma atsispindės delspinigių kodu Dynamics AX pardavimo užsakyme. Naudokite šį parametrą norėdami siuntimo mokesčio kodas su pristatymo išlaidos pagal kliento užsakymą.
-   **Grąžina siuntimo mokesčiai** – nurodyti, ar gabenimo mokesčius, susijusius su kliento užsakymas grąžinamas.
-   **Didžiausia suma be patvirtinimo** – jei siuntimo mokesčiai yra grąžintini, nurodyti didžiausią sumą pristatymas nemokamai grąžinamosios išmokos visoje grąžinimo užsakymus. Jeigu ši suma viršijama, vadovas nepaisyti reikalingas siekiant toliau grąžinamąją išmoką. Prisitaikyti prie šių scenarijų, grąžinamosios išmokos, pristatymo išlaidos gali viršyti sumos, kurią iš pradžių mokėjo:
    -   Taikomi mokesčiai pardavimo užsakymo antraštėje, ir kai nors kiekis produkto linija grąžinama, maksimalus grąžinimo pristatymo išlaidos leistiną produktų ir kiekio negalima nustatyti tokiu būdu, kuris dirba už visus mažmeninius klientus.
    -   Prie kiekvieno krovinio patiriamos gabenimo mokesčius. Jei pirkėjas grąžina produktų kelis kartus, ir pardavėjo strategija nurodo, kad agentas bus padengia grįžimo siuntimo mokesčiai, grąžinimo siuntimo mokesčiai bus daugiau nei faktinis gabenimo mokesčius.

## <a name="transaction-flow-for-customer-orders"></a>Sandorio srautas, klientų užsakymų
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Sukurti klientų aptarnavimo užsakymo mažmeninės prekybos Šiuolaikinės pos

1.  Įtraukite į operaciją klientą.
2.  Pridėti prekių į krepšelį.
3.  Spustelėkite **sukurti kliento užsakymas**, ir tada pasirinkite užsakymo tipas. Užsakymo tipą galima bet **klientų užsakymų** ar **citata**.
4.  Spustelėkite **laivas pasirinktas** ar **visi laivo** išsiųsti produktus į adresą į kliento sąskaitą, nurodykite kreipiamasi pristatymo datą ir nurodyti gabenimo mokesčius.
5.  Spustelėkite **pasiimti pasirinktas** ar **rinktuvo visus** rinktis produktus, kurie bus būti įlaipinami iš dabartinės parduotuvės ar kitoje parduotuvėje konkrečią datą.
6.  Rinkti indėlio suma, jei užstatą.

### <a name="edit-an-existing-customer-order"></a>Redaguoti esamą kliento užsakymas

1.  Pagrindiniame puslapyje, spustelėkite **rasti užsakymą**.
2.  Raskite ir pasirinkite Redaguoti. Puslapio apačioje spustelėkite į **redaguoti**.

### <a name="pick-up-an-order"></a>Pasiimti vykdomąjį raštą

1.  Pagrindiniame puslapyje, spustelėkite **rasti užsakymą**.
2.  Pasirinkite užsakymą pasiimti. Puslapio apačioje spustelėkite **surinkimo bei pakavimo operacija**.
3.  Spustelėkite **pasiimti**.

### <a name="cancel-an-order"></a>Atšaukti užsakymą

1.  Pagrindiniame puslapyje, spustelėkite **rasti užsakymą**.
2.  Pasirinkite atšaukti užsakymą. Puslapio apačioje spustelėkite **atšaukti**.

#### <a name="create-a-return-order"></a>Grąžinimo užsakymo kūrimas

1.  Pagrindiniame puslapyje, spustelėkite **rasti užsakymą**.
2.  Pasirinkite užsakymą grįžti, pasirinkite užsakymo SF, ir tada pasirinkite produktų liniją, skirtą grąžinti prekes.
3.  Puslapio apačioje spustelėkite į **grąžinimo užsakymui**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asinchroninis sandorio srautas, klientų užsakymų
Klientų užsakymus galima sukurti pardavimo (PV) kliento požiūriu arba Sinchroninis arba asinchroninis režimu.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Įgalinti klientų užsakymus, turi būti sukurta asinchroniniu režimu

1.  Dynamics AX, spustelėkite **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS profilis**&gt;**funkcijų šablonų**.
2.  Dėl į **bendrojo** FastTab, nustatyti su **sukurti kliento užsakymo async režimu** galimybę **taip**.

Kai į **sukurti kliento užsakymo async režimu** parinktis nustatyta **taip**, klientų užsakymus visada sukuriamos asinchroniniu režimu, net jei mažmeninės prekybos operacijų paslaugos (RTS). Jei nustatote šią pasirinktį kaip **Nr**, klientų užsakymus visada sukurtų Sinchroninis režimu naudojant RTS. Sukūrus klientų užsakymus asinchroniniu režimu, jie ištrauktas ir įtrauktas į Dynamics AX iš traukti (P) užduotys. Atitinkamus pardavimo užsakymų yra sukurta Dynamics AX kai **sinchronizuoti užsakymų** yra valdoma rankiniu būdu ar partija apdoroti.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Hibridinis klientų užsakymus](hybrid-customer-orders.md)


