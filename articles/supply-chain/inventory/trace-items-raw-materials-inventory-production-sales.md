---
title: Prekių ir žaliavų sekimas atsargose, gamyboje ir pardavimuose
description: Šioje temoje aprašoma, kaip galite naudoti prekės sekimą norėdami nustatyti, kur prekės arba žaliavos buvo naudojami, naudojami arba bus naudojami gamybos ir pardavimo procesuose.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9293578144c51baef34204a2b592d517baa3b0dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967185"
---
# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Prekių ir žaliavų sekimas atsargose, gamyboje ir pardavimuose

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip galite naudoti prekės sekimą norėdami nustatyti, kur prekės arba žaliavos buvo naudojami, naudojami arba bus naudojami gamybos ir pardavimo procesuose.

Prekių sekimo funkcijos prieinamos puslapyje **Prekių sekimas**. Toliau pateikiamuose skyriuose aprašoma, kaip galima naudoti prekių sekimą ir kokios jo parinktys bei apribojimai.

## <a name="what-is-item-tracing"></a>Kas yra prekės sekimas?
Prekių sekimas yra verslo tyrimų (BI) įrankis, kuris užtikrina prekių ir žaliavų šaltinio ir paskirties matomumą tiekimo grandinėje. Gamintojai gali sekti prekes, žaliavas arba ingredientus atgal iki tiekėjo ir toliau gamybos procesą bei galutinio produkto pardavimą. Prekių sekimas padeda gamintojams atitikti reglamentų reikalavimus bei padeda kokybės pareigūnams ir gamybos vadovams analizuoti ir imtis veiksmų, kad nebūtų produktų ir medžiagų kokybės nuokrypių. Toliau pateikti keli pavyzdžiai, kaip gamintojai gali naudoti prekių sekimą.

-   Nustatyti atsargose esančių prekių ar žaliavų kiekį ir vietą, kur jos saugomos.
-   Nustatyti, kiek prekės arba žaliavos buvo išsiųsta ir kuriems klientams jos išsiųstos.
-   Nustatyti visas suplanuotas siuntas, kuriose yra tos prekės arba žaliavos.
-   Rasti gamybos užsakymus, kuriuose naudojama prekė arba žaliava, ir kurie yra suplanuoti, vykdomi arba paskelbti įvykdytais.
-   Sužinoti, kur buvo įsigyta prekė arba žaliava.
-   Ištirti, kur prekė arba žaliava buvo panaudota kitos prekės gamybai.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Ką galima sekti ir ar yra apribojimų?
Galite sekti retrospektyvines prekių ir žaliavų atsargų operacijas pagal prekės numerį ir sekimo dimensiją, pvz., serijos numerį, paketo numerį arba tiekėjo paketo numerį. Prekę ar žaliavą sekti galite tik jei jai priskirta sekimo dimensija. Kadangi sekimo pagrindas yra atsargų operacijos, yra tam tikrų prekių sekimo apribojimų. Pavyzdžiui, yra apribojimų, susijusių su projektų, ilgalaikio turto ir prekybos operacijomis. Be to, sekimo duomenyse rodomi sudėtiniai produktai, bet neįtraukiami šalutiniai produktai. Sekimas apima visas sandėlio operacijas iš vienos vietos į kitą. Todėl vartotojams tiek informacijos gali būti per daug. Vienu metu rodomas vieno juridinio subjekto sekimas. Vidinės įmonės kontekste visoms įmonėms taikomų galimybių nėra. Turite pradėti naują kiekvienos įmonės, kurioje gaunama ar išduodama prekė, sekimą.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Kokius prekės sekimo kriterijus galiu nurodyti?
Kriterijai, kurių reikia norint sekti prekę, yra prekės numeris, sekimo dimensija (pvz., paketo numeris arba serijos numeris) ir kryptis. Šioje lentelėje aprašomi kriterijai, kuriuose galite naudoti sekdami prekę.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauko grupė</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prekės numeris</td>
<td>Įveskite sekamos prekės arba žaliavos identifikatorių.</td>
</tr>
<tr class="even">
<td>Produktų dimensijos</td>
<td>Pasirinktinai: sekite tam tikrus produkto aspektus, pvz., konfigūraciją, dydį, spalvą arba stilių.</td>
</tr>
<tr class="odd">
<td>Sekimo dimensijos</td>
<td>Įveskite paketo numerio, tiekėjo paketo numerio arba serijos numerio sekimo dimensiją. Kai paketo numerį naudojate kaip kriterijų, bus rodomas tiekėjo paketo numeris, jei įrašėte šią informaciją.</td>
</tr>
<tr class="even">
<td>Saugojimo dimensijos</td>
<td>Pasirinktinai: sekite prekes, kurios saugomos tam tikroje vietoje.</td>
</tr>
<tr class="odd">
<td>Laikotarpis</td>
<td>Pasirinktinai: įveskite datas, norėdami vykdyti sekimą tam tikrą laikotarpį. Sekimo duomenyse bus rodomi tik dokumentai ir operacijos, kurios buvo sukurtos šiuo laikotarpiu.</td>
</tr>
<tr class="even">
<td>Pirmyn arba atgal</td>
<td>Pasirinkite sekimo kryptį. Galite sekti pirmyn arba atgal:
<ul>
<li><strong>Atgal</strong> – sekite atgal, norėdami nustatyti šaltinį, dar turimą kiekį ir gamybos užsakymus, kurie yra paskelbti bent iš dalies baigtais.</li>
<li><strong>Pirmyn</strong> – sekite pirmyn, norėdami nustatyti paskirties vietą. Galite rasti pardavimo užsakymus ir klientus, kuriems sekama prekė arba žaliava bent iš dalies išsiųsta.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Kokia informacija yra sekimo duomenyse?
Sekimo rezultatai rodomi medyje chronologine tvarka puslapio **Prekių sekimas** „FastTab“ skirtuke **Išsami informacija**. Užsakymas skiriasi priklausomai nuo sekimo krypties. Informacija apima visas operacijas nuo prekės pirkimo iš tiekėjo iki jos pardavimo klientui. Sekimo rezultatuose taip yra informacija apie tarpinius produktus, susijusius su preke arba sekimo dimensija, nurodyta sekimo kriterijuose. Aukščiausias mazgas rodo atsargose turimą prekės kiekį pagal saugojimo dimensijas, nurodytas sekimo kriterijuose. **Pastaba.** Sekimo duomenys greitai perteikia informaciją, kuri buvo prieinama atliekant sekimą. Sekimo duomenys nėra atnaujinami, jei atlikus sekimą pasikeičia informacija.

## <a name="why-dont-some-nodes-contain-any-details"></a>Kodėl kai kuriuose mazguose nėra jokios informacijos?
Kad sekimo duomenyse būtų mažiau informacijos, informacija pateikiama tik pirmojo prekės ar žaliavos egzemplioriaus mazge. Jei pažymėtame mazge nėra informacijos, mazgą, kuriame informacijos yra, galite peržiūrėti spustelėdami **Pereiti prie sekamos eilutės**. Tada galite grįžti į mazgą, iš kurio išėjote, spustelėdami **Grįžti atgal**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Ar galiu peržiūrėti tik tam tikro tipo dokumentą? Pavyzdžiui, galiu peržiūrėti tik gamybos užsakymus, klientus ar tiekėjus?
Taip, iš išsamios sekimo informacijos srities galite atidaryti sąrašo puslapius, kuriuose yra tik tam tikro tipo dokumentas ar operacija. Šiuos puslapius galite pasiekti iš veiksmų srities meniu elemento **Sekimas**, grupėse **Prekė**, **Pardavimas**, **Pirkimas**, **Gamyba** ir **Kokybė**. Pavyzdžiui, norėdami peržiūrėti tiekėjų sąrašą sekimo duomenyse, spustelėkite **Sekimas** &gt; **Pirkimas** &gt; **Tiekėjai**. Sąrašo puslapiuose apibendrinami sekimo duomenų dokumentai ar operacijos. Sąrašų puslapiuose **Laukiančios operacijos**, **Laukiantys užsakymai** ir **Neišsiųsti pardavimo užsakymai** taip pat pateikiama kita informacija, neįtraukta į sekimo duomenis. Be to, juose visada rodomi esamos datos rezultatai, net jei buvo nurodytas datų intervalas. Toliau pateikiamoje lentelėje aprašomi papildomi duomenys, kurie gali būti pateikti šiuose puslapiuose.

| Sąrašai                    | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Neišsiųsti pardavimo užsakymai | Peržiūrėkite pardavimo užsakymo eilutes, kurios nebuvo įtrauktos ir todėl nerodomos sekimo duomenyse.                                                                                                                                                                                                                        |
| Laukiantys užsakymai           | Peržiūrėkite visus laukiančius sekamos prekės gamybos užsakymus, nesvarbu, kokios sekimo dimensijos buvo naudojamos sekimo kriterijuose. Taip pat galite peržiūrėti laukiančius gamybos užsakymus, kur sekama prekė yra ingredientas, ir kur nebuvo atlikta jokių registracijų bei nėra baigtomis paskelbtų užsakymo operacijų. |
| Laukiančios operacijos     | Peržiūrėkite sekamos prekės, kurioje yra nurodytos sekimo dimensijos arba tuščia sekimo dimensija, laukiančias atsargų operacijas. Taip pat sekimo duomenyse galite peržiūrėti laukiančias prekių ir sekimo dimensijų kombinacijų ar tuščios vertės atsargų operacijas.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Kiek lygių galiu atsekti aukštyn arba žemyn KS arba formulėje?
Komplektavimo specifikacijoje (KS) arba formulėje galite atsekti vieną lygį aukštyn arba žemyn. Pavyzdžiui, jei sekate žaliavas, galite matyti galutinį produktą ir sudėtinius produktus. Tačiau, jei sekate sudėtinį produktą, sekimo duomenyse nebus galutinio produkto.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Kaip peržiūrėti išsamesnę informaciją apie dokumentą arba operaciją sekimo duomenyse?
„FastTab“ skirtuke **Išsami informacija** peržiūrėti daugiau informacijos apie pasirinktą dokumentą arba operaciją sekimo duomenyse galite tolesniais dviem būdais.

-   Kai pasirenkate mazgą sekimo duomenyse „FastTab“ skirtuke **Išsami informacija**, kituose puslapio „FastTab“ skirtukuose rodoma informacija apie dokumentą arba operaciją mazge.
-   Pasirinkto mazgo dokumento informacijos puslapį galite atidaryti spustelėdami **Peržiūrėti informaciją**. Pavyzdžiui, jei pasirinksite mazgą, kuriame aprašomas gamybos užsakymas, ir spustelėsite **Peržiūrėti informaciją**, bus rodomas puslapis **Gamybos užsakymų informacija**.

Kai kurie „FastTab“ skirtukai suteikia prieigą prie papildomos informacijos apie pasirinktą mazgą. Pavyzdžiui, „FastTab“ skirtuke **Neatitiktys** galite spustelėti **Užklausos** ir ištirti, ar anksčiau buvo neatitikčių. „FastTab“ skirtuke **Paketas** galite spustelėti **Turimų atsargų sąrašas** ir peržiūrėti šiuo metu turimas faktines atsargas ir su paketu susijusias atsargų operacijas.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Ar galiu vykdyti daugiau nei vieną sekimą, o vėliau palyginti informaciją?
Po to, kai pradedate sekimą, galite naudoti tolesnes mygtuko **Sekti nuo mazgo** parinktis, kad pradėtumėte naują pasirinkto mazgo operacijos sekimą.

-   **Atgal** arba **Pirmyn** – pradėkite naują pasirinkto mazgo sekimą ir perrašykite dabartinio sekimo informaciją.
-   **Naujas atgalinis sekimas** arba **Naujas sekimas į priekį** – pradėkite naują sekimą naujame lange ir pasilikite dabartinio sekimo informaciją.

Jei norite naudoti parinktį **Naujas atgalinis sekimas** arba **Naujas sekimas į priekį**, turite naudoti funkciją **Atidaryti naujame lange**, kad naujas sekimas būtų rodomas naujame lange.

## <a name="can-i-save-the-trace-details"></a>Ar galiu įrašyti sekimo duomenis?
Informaciją skirtuke <strong>Išsami informacija</strong> galite įrašyti kaip XML failą – veiksmų srityje po veiksmu *<strong><em>Sekimas</em></strong>* spustelėkite <strong>Eksportuoti</strong>. Be sekimo duomenų XML faile pateikiami ir sekimo kriterijai, pirminis mazgas ir turimas kiekis. Galimybė įrašyti sekimo duomenis yra naudinga, jei, pavyzdžiui, norite pridėti informacijos prie kokybės užsakymo arba kitų atitikties dokumentų. Galite nurodyti, kur failas bus išsaugotas. Norėdami failą peržiūrėti iš karto, pasirinkite parinktį <strong>Rodyti dokumentą</strong>. <strong>Pastaba.</strong> Failas visada įrašomas, net ir tuo atveju, jei norite jį tik peržiūrėti. Pagal numatytuosius nustatymus XML failas atidaromas naršyklės lange. Tačiau failą galite spustelėti dešiniuoju pelės mygtuku, pasirinkti <strong>Atidaryti naudojant</strong> ir pasirinkti programą turiniui rodyti.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Ar galiu apskaičiuoti konkrečios prekės ar ingrediento balansą?
Informaciją iš suvestinės puslapių galite eksportuoti į „Microsoft Excel“. Atidarykite aktualų puslapį, spustelėkite piktogramą **Atidaryti naudojant „Microsoft Office“** ir pasirinkite **Eksportuoti į „Microsoft Excel“**. Ši funkcija ypač naudinga, kai norite apskaičiuoti prekės ar ingrediento masės balansą iš puslapio **Operacijų suvestinė**. Puslapyje **Operacijų suvestinė** galite filtruoti pagal prekę arba ingredientą ir, jei reikia, pagal paketą, ir tada eksportuoti informaciją į „Excel“. Programoje „Excel“ galite atskirti, pavyzdžiui, turimą kiekį, parduotą kiekį ir kiekį, panaudotą gamyboje.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Ar galiu ištirti, ar yra problemų su prekėmis arba žaliavomis retrospektyva?
Sekimo duomenyse pateikiama informacija apie kokybės užsakymus ir neatitiktis, susijusius su prekėmis arba žaliavomis. Norėdami peržiūrėti kokybės užsakymų ir neatitikčių suvestinę, veiksmų srityje spustelėkite **Kokybės užsakymai** arba **Neatitiktys**. **Pastaba.** Ardomieji kokybės užsakymai sekimo duomenyse gali būti rodomi daugiau nei vieną kartą. Jei dokumente sukuriamas ardomasis kokybės užsakymas, pvz., pirkimo užsakymas, jis rodomas prie visų šio dokumento operacijų.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Ar yra su prekės sekimu susijusių ataskaitų teikimo galimybių?
Galite generuoti ataskaitą **Išsiųsta klientams**, norėdami nustatyti, koks prekės arba žaliavos kiekis buvo išsiųstas ir kuriems klientams jis buvo išsiųstas. Ataskaitą dėl užklausos, susijusios su atitiktimi, galite generuoti visiems klientams. Ataskaitą dėl užklausos, susijusios su klientų aptarnavimu, galite generuoti pasirinktam klientui. Jei produktas buvo žaliava, panaudota užbaigtos prekės gamyboje, užbaigta prekė taip pat bus įtraukta. **Pastaba.** Jei naudojate pardavimo užsakymų naikinimo ar archyvavimo funkcijas, ataskaitos rezultatuose taip pat bus visi pardavimo užsakymai, kurie buvo panaikinti arba suarchyvuoti.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Ar galiu sekti sudėtinius produktus ir šalutinius produktus?
Galite sekti sudėtinius produktus, tačiau negalite sekti šalutinių produktų, nes sekimo dimensijos paprastai nėra priskirtos šalutiniams produktams. Kai sekate prekę, sekimo duomenys apima visus susijusius sudėtinius produktus. Mazgo, kuriame yra sudėtinis produktas, informacijoje nurodomi žodžiai „sudėtinis produktas“. Taip pat galite peržiūrėti išsamią informaciją apie sudėtinį produktą, sekimo duomenyse pasirinkdami mazgą ir spustelėdami „FastTab“ skirtuką **Gamyba**.
