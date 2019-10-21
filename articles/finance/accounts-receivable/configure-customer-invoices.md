---
title: Kliento SF kūrimas
description: '**Kliento SF pardavimo užsakymui** yra sąskaita, susijusi su pardavimu ir kurią organizacija pateikia klientui.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa49b70b07ac3dc6cbc5989b11981098f22be89c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189159"
---
# <a name="create-a-customer-invoice"></a>Kliento SF kūrimas

[!include [banner](../includes/banner.md)]

**Kliento SF pardavimo užsakymui** yra sąskaita, susijusi su pardavimu ir kurią organizacija pateikia klientui. Šis kliento SF tipas kuriamas remiantis pardavimo užsakymu, į kurį įeina užsakymo eilutės ir prekių numeriai. Prekių numeriai yra nurodyti ir užregistruoti didžiojoje knygoje. Kliento SF pardavimo užsakymui skirtų papildomos knygos žurnalo įrašų nėra. Daugiau informacijos žr. [Kurti pardavimo užsakymų sąskaitas faktūras](tasks/create-sales-order-invoices.md).

**Laisvos formos SF** nėra susijusi su pardavimo užsakymu. Joje pateikiamos užsakymo eilutės, kuriose yra DK sąskaitos, laisvo pobūdžio aprašai ir pardavimo suma, kuriuos įvedate. Į šios rūšies SF prekės numerio įvesti negalite. Turite įvesti atitinkamą PVM informaciją. Pagrindinė pardavimo sąskaita nurodoma kiekvienoje SF eilutėje, kurią paskirstyti į kelias DK sąskaitas galite **Laisvos formos SF** puslapyje spustelėdami **Paskirstyti sumas**. Be to, kliento balansas suminėje sąskaitoje regisruojamas iš naudojamo laisvos formos SF registravimo profilio.

Norėdami gauti daugiau informacijos, žr. 

[Kurti laisvos formos SF](../accounts-receivable/create-free-text-invoice-new.md)

[Kurti laisvos formos šabloną](../accounts-receivable/create-free-text-invoice-template-new.md)

[Priskirti klientui laisvos formos SF šabloną](tasks/assign-free-text-invoice-template-customer.md)

[Generuoti ir registruoti pasikartojančias laisvos formos SF](tasks/post-recurring-free-text-invoices.md)


**Išankstinė SF** yra tokia sąskaita, kuri parengiama kaip faktinių sąskaitos sumų įvertinimas, prieš užregistruojant sąskaitą faktūrą. Galite išspausdinti arba kliento SF pardavimo užsakymui, arba laisvos formos sąskaitos faktūros išankstinę sąskaitą faktūrą.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Registruoti ir spausdinti atskiras kliento SF, kurios paremtos pardavimo užsakymais
Naudodami šį procesą galite sukurti sąskaitą faktūrą, grindžiamą pardavimo užsakymu. To gali prireikti, jei nuspręsite išrašyti klientui sąskaitą faktūrą prieš pristatydami prekes arba suteikdami paslaugas. 

Kai registruojate sąskaitą faktūrą, **SF likučio** kiekis kiekvienai prekei atnaujinamas nurodant bendruosius SF kiekius iš pasirinkto pardavimo užsakymo. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.

Peržiūrėti pardavimo užsakymų būseną galite sąrašo puslapyje **Visi pardavimo užsakymai**. Sąrašo puslapyje **Atidarytos klientų SF** galite peržiūrėti savo registruotas sąskaitas faktūras.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Registruoti ir spausdinti atskiras klientų SF, kurios paremtos važtaraščiais ir data
Šią procedūrą naudokite, kai užregistruotas vienas ar keli pardavimo užsakymo važtaraščiai. Kliento SF grindžiama šiais važtaraščiais ir atspindi juose nurodytus kiekius. SF finansinė informacija yra paremta informacija, įvesta jums registruojant SF. 

Galima sukurti kliento SF, kuri paremta važtaraščio eilutės prekėmis, išsiųstomis iki dabar, net jei dar ne visos konkretaus pardavimo užsakymo prekės yra išsiųstos. Tai galite atlikti jei, pavyzdžiui, jūsų juridinis subjektas per mėnesį vienam klientui išduoda vieną SF, kurioje pateikiama informacija apie visus siuntinius, išsiųstus tą mėnesį. Kiekvienas važtaraštis reiškia iš dalies arba visiškai atliktą pardavimo užsakymo prekių pristatymą. 

Jums užregistravus SF, **SF likučio** kiekis kiekvienai prekei yra atnaujinamas bendra pristatytų kiekių iš pasirinktų važtaraščių suma. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF. 

Atsargų operacijos yra atnaujinamos SF numeriu, o būsena pardavimo užsakymo lauke **Eilutės būsena** pakeičiama į **SF išrašyta**. 

Pardavimo užsakymų būseną peržiūrėkite sąrašo puslapyje **Visi pardavimo užsakymai**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsoliduoti pardavimo užsakymus arba važtaraščius, norint juos registruoti
Šį procesą naudokite, kai vienam ar keliems pardavimo užsakymams galima išrašyti SF, ir norite juos konsoliduoti į vieną SF. 

**Pardavimo užsakymo** sąrašo puslapyje galite pasirinkti kelias SF ir tada joms konsoliduoti naudoti **Generuoti SF**. Puslapyje **SF registravimas** galite pakeisti **Suminio užsakymo** nustatymą, kad būtų sumuojama pagal užsakymo numerį (kai yra keli vieno pardavimo užsakymo važtaraščiai) arba pagal SF sąskaitą (kai yra keli vienos SF sąskaitos pardavimo užsakymai). Naudokite mygtuką **Išdėstyti**, kad pardavimo užsakymus pagal **Suminio užsakymo** parametrus konsoliduotumėte į vieną SF.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Papildomos nuostatos, keičiančios registravimo veikseną
Toliau nurodyti laukai keičia registravimo proceso veikseną.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Laukas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kiekis</td>
<td>Pasirinkite kiekius, kuriais grindžiamas dokumentų registravimas. Prieinamos parinktys skiriasi – jos priklauso nuo registruojamo dokumento tipo, pvz., važtaraščio ar SF.
<ul>
<li><strong>Pristatyti dabar</strong> – pasirinkti visus kiekius, kurie įvesti į lauką <strong>Pristatyti dabar</strong>. Naudokite šią parinktį, jei norite patvirtinti ar pristatyti dalinį užsakymą.</li>
<li><strong>Paimti</strong> – pasirinkti visus kiekius, kurie paimti.</li>
<li><strong>Visi</strong> – pasirinkti visus pardavimo užsakymų kiekius, kurie dar neatnaujinti pagal dabartinio dokumento tipą.</li>
<li><strong>Važtaraštis</strong> – pasirinkti visus kiekius, kurie atnaujinti pagal važtaraštį.</li>
<li><strong>Paimtas kiekis ir atsargose nelaikomi produktai</strong> – pasirinkti visus kiekius, kurie paimti ir visus produktų kiekius, kurie nelaikomi atsargose.</li>
</ul></td>
</tr>
<tr class="even">
<td>Registravimas</td>
<td><ul>
<li>Norėdami į žurnalą įtraukti pardavimo užsakymą, pasirinkite šią parinktį.</li>
<li>Norėdami spausdinti išankstinį pardavimo užsakymą, panaikinkite šios parinkties žymėjimą. <strong>Pastaba.</strong> Jei susitarėte dėl mokėjimo grafiko, išankstiniame pardavimo užsakyme mokėjimo grafikas nerodomas. Mokėjimo grafikai rodomi tik faktiniuose pardavimo užsakymuose.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vėlesnis pasirinkimas</td>
<td>Pažymėkite šią parinktį, jei norite pasirinktą užklausą taikyti vėliau. Ši pasirinktis naudojama su paketinėmis užduotimis. Užklausa vykdoma paleidus paketinę užduotį.</td>
</tr>
<tr class="even">
<td>Mažinti kiekį</td>
<td>Pasirinkite šią parinktį, kad užregistravus dokumentą būtų automatiškai sumažinamas pristatytas kiekis – tuomet pristatytas kiekis bus lygus turimoms atsargoms.</td>
</tr>
<tr class="odd">
<td>Spausdinti</td>
<td>Pasirinkite, kada reikia spausdinti dokumentus.
<ul>
<li><strong>Dabart.</strong> – dokumentus spausdinti atnaujinus kiekvieną SF.</li>
<li><strong>Vėliau</strong> – dokumentus spausdinti, kai atnaujinamos visos SF.</li>
</ul>
<strong>Pastaba.</strong> Lauką <strong>Spausdinti</strong> galėsite naudoti tik pasirinkę parinktį <strong>Spausdinti SF</strong>, <strong>Spausdinti patvirtinimą</strong>, <strong>Spausdinti išrinkimo dokumentą</strong> arba <strong>Spausdinti važtaraštį</strong>. Pavyzdžiui, puslapyje <strong>Rūšiavimas pagal formas</strong> turite nustatyti sistemą, kad informacija būtų rūšiuojama pagal SF sąskaitą. Tada galite pasirinkti parinktį <strong>Vėliau</strong>, kad būtų spausdinami pagal SF sąskaitą surūšiuotame pakete esantys dokumentai. Kitu atveju dokumentai spausdinami neužbaigus apdorojimo proceso ir nėra surūšiuojami puslapyje <strong>Rūšiavimas pagal formas</strong> nurodyta tvarka.</td>
</tr>
<tr class="even">
<td>Spausdinti SF</td>
<td>Pažymėkite šią parinktį, kad būtų spausdinama SF. Jei ši parinktis yra išjungta, spausdinti SF galite jos neregistravę.</td>
</tr>
<tr class="odd">
<td>Siųsti el. laišką</td>
<td>Pasirinkite šią parinktį, norėdami klientui pardavimo užsakymo SF siųsti kaip el. laiško priedą, ją užregistravus. Priedai siunčiami kaip PDF ir XML failai. Ši parinktis galima tik tada, jei <strong>Elektroninių SF parametrų</strong> puslapyje pasirenkate parinktį <strong>Įgalinti CFD (elektronines SF)</strong>. <strong>Pastaba.</strong> (MEX) Šis valdiklis pasiekiamas tik juridiniams subjektams, kurių pagrindinis adresas yra Meksikoje.</td>
</tr>
<tr class="even">
<td>Naudoti spausdinimo valdymo paskirtį</td>
<td>Pasirinkite šią parinktį, norėdami naudoti operacijos, dokumento ar modulio spausdinimo nuostatas, nurodytas <strong>Spausdinimo valdymo sąrankos</strong> puslapyje.</td>
</tr>
<tr class="odd">
<td>Tikrinti kredito limitą</td>
<td>Pasirinkite informaciją, kuri turėtų būti analizuojama tikrinant kredito limitą.
<ul>
<li><strong>Nėra</strong> – nereikalaujama tikrinti kredito limito.</li>
<li><strong>Balansas</strong> – kredito limitas tikrinamas pagal kliento balansą.</li>
<li><strong>Balansas + važtaraštis arba produkto gavimo kvitas</strong> – kredito limitas tikrinamas pagal kliento balansą ir pristatymus.</li>
<li><strong>Balansas + visi</strong> – Kredito limitas tikrinamas pagal kliento balansą, pristatymus ir atvirus užsakymus.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kredito koregavimas</td>
<td>Pasirinkite šią parinktį, kad kvitų operacijose kredito pažyma būtų rodoma kaip debetas.</td>
</tr>
<tr class="odd">
<td>Kredituoti likusį kiekį</td>
<td>Pasirinkite šią parinktį, jei registruojant kredito pažymą norite palikti likusį užsakymo kiekį. Jei šios parinkties žymės langelis išvalomas, likęs kiekis nustatomas 0 (nuliu).</td>
</tr>
<tr class="even">
<td>Suminis atnaujinimas</td>
<td>Pasirinkite, kaip turėtų būti apibendrinami keli pardavimo užsakymai.
<ul>
<li><strong>Niekaip</strong> – pardavimo užsakymų neapibendrinti. Pavyzdžiui, bus sukurta atskira kiekvieno pardavimo užsakymo SF.</li>
<li><strong>SF sąskaita</strong> – visus pasirinktus užsakymus apibendrinti pagal kriterijus, nustatytus puslapyje <strong>Suminio atnaujinimo parametrai</strong>.</li>
<li><strong>Užsakymas</strong> – pasirinktą užsakymų intervalą apibendrinti į vieną jūsų nurodytą užsakymą. Užsakymai apibendrinami pagal kriterijus, nustatytus puslapyje <strong>Suminio atnaujinimo parametrai</strong>. Jei pasirenkate šią parinktį, lauke <strong>Pardavimo užsakymas</strong> turite pasirinkti reikšmę.</li>
<li><strong>Automatinis sumavimas</strong> – jei <strong>Suminio atnaujinimo</strong> puslapyje nurodyti suminiai atnaujinimai, visus pasirinktus užsakymus sumuoti pagal kriterijus, nustatytus <strong>Suminio atnaujinimo parametrų</strong> puslapyje. Jei suminiai atnaujinimai nenurodyti, užsakymas registruojamas atskirai.</li>
<li><strong>Važtaraštis</strong> – pasirinktą užsakymų intervalą sumuoti į vieną kiekvieno važtaraščio SF. Šią parinktį galima naudoti, tik jei lauke <strong>Kiekis</strong> pasirinkta <strong>Važtaraštis</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>





