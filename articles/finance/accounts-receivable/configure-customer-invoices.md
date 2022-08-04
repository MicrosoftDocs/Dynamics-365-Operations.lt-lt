---
title: Kliento SF kūrimas
description: Kliento SF pardavimo užsakymui yra sąskaita, susijusi su pardavimu ir kurią organizacija pateikia klientui.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04c26eec8be61d60908bef67c75958287e7e1a01
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129519"
---
# <a name="create-a-customer-invoice"></a>Kliento SF kūrimas

[!include [banner](../includes/banner.md)]

Pardavimo **užsakymo kliento SF yra** sąskaita, susijusi su pardavimu ir kurią organizacija pateikia klientui. Šis kliento SF tipas kuriamas remiantis pardavimo užsakymu, į kurį įeina užsakymo eilutės ir prekių numeriai. Prekių numeriai yra nurodyti ir užregistruoti didžiojoje knygoje. Kliento SF pardavimo užsakymui skirtų papildomos knygos žurnalo įrašų nėra. Daugiau informacijos žr. [Kurti pardavimo užsakymų sąskaitas faktūras](tasks/create-sales-order-invoices.md).

Laisvos **formos SF** nėra susijusi su pardavimo užsakymu. Joje pateikiamos užsakymo eilutės, kuriose yra DK sąskaitos, laisvo pobūdžio aprašai ir pardavimo suma, kuriuos įvedate. Į šios rūšies SF prekės numerio įvesti negalite. Turite įvesti atitinkamą PVM informaciją. Pagrindinė pardavimo sąskaita nurodoma kiekvienoje SF eilutėje, kurią paskirstyti į kelias DK sąskaitas galite **Laisvos formos SF** puslapyje spustelėdami **Paskirstyti sumas**. Be to, kliento balansas suminėje sąskaitoje regisruojamas iš naudojamo laisvos formos SF registravimo profilio.

Daugiau informacijos, žr.:

[Kurti laisvos formos SF](../accounts-receivable/create-free-text-invoice-new.md)[
 kurti laisvos formos SF
](../accounts-receivable/create-free-text-invoice-template-new.md)[šabloną laisvos formos SF šablonui](tasks/assign-free-text-invoice-template-customer.md)
[klientui priskirti ir užregistruoti pasikartojančias laisvos formos SF](tasks/post-recurring-free-text-invoices.md)


Išankstinė **SF yra** sąskaita, kuri parengiama kaip faktinių sąskaitos sumų įvertinimas prieš užregistruojant sąskaitą faktūrą. Galite išspausdinti **arba kliento** pardavimo užsakymo išankstinės SF, arba laisvos formos sąskaitos faktūros išankstinę sąskaitą faktūrą. 

>[!NOTE]
> Sistemos trukdžių pardavimo išankstinės SF proceso metu atveju išankstinė SF gali būti vieniša. Vieniša išankstinė SF gali būti panaikinta rankiniu būdu paleidus **periodinę užduotį Naikinti** išankstines SF. Eikite **į pardavimo ir rinkodaros > periodines užduotis > Valyti > išankstinės SF panaikinkite rankiniu būdu**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Pardavimo užsakymo kliento SF duomenų objektų naudojimas
Galite naudoti duomenų objektus pardavimo užsakymo informacijai apie kliento SF importuoti ir eksportuoti. Pardavimo SF antraštėje ir pardavimo SF eilutėse yra skirtingų objektų.

Pardavimo SF antraštėje gali būti naudojami šie objektai:

- **Pardavimo SF žurnalo antraštės** objektas (SalesInvoiceJournalHeaderEntity)
- **Pardavimo SF antraštės V2 objektas** (SalesInvoiceHeaderV2Entity)

Rekomenduojame naudoti pardavimo SF žurnalo **antraštės objektą**, nes jis teikia daugiau patirties pardavimo antraštės importavimui ir eksportavimui. Šiame subjekte nėra PVM **sumos** (INVOICEHEADERTAMOUNT) stulpelio, kuris nurodo PVM vertę pardavimo SF antraštėje. Jei jūsų verslo scenarijus reikalauja šios informacijos, naudokite objektą **Pardavimo SF V2**, kad importuokite ir eksportuokite pardavimo SF antraštės informaciją.

Pardavimo SF eilutėse pateikiama informacija galima šiais objektais:

- **Kliento SF eilučių** objektas (BusinessDocumentSalesInvoiceLineItemEntity)
- **Pardavimo SF eilučių V3 objektas** (SalesInvoiceLineV3Entity)

Kai nustatote, kurį eilutės objektą naudoti eksportuojant, apsvarstykite, ar bus naudojamas visiškas stūmimas, ar visiškas stūmimas. Be to, atsižvelkite į duomenų sudėtį. Pardavimo **SF eilučių V3 objektas** palaiko sudėtingesnius scenarijus (pavyzdžiui, konvertavimas į atsargų laukus). Taip pat ji palaiko viso stūmimo eksporto scenarijus. Dėl didėjančio stūmimo rekomenduojame naudoti kliento **SF eilučių objektą**. Šis objektas yra daug paprastesnė **duomenų struktūra nei pardavimo SF eilučių V3** objektas ir jis yra pageidautinas, ypač jei atsargų lauko integravimas nėra būtinas. Dėl eilučių objektų susiejimo palaikymo skirtumų **kliento** **SF eilučių objektas paprastai būna greitesnis nei pardavimo SF eilučių V3 objektas.**

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Registruoti ir spausdinti atskiras kliento SF, kurios paremtos pardavimo užsakymais
Naudodami šį procesą galite sukurti sąskaitą faktūrą, grindžiamą pardavimo užsakymu. To gali prireikti, jei nuspręsite išrašyti klientui sąskaitą faktūrą prieš pristatydami prekes arba suteikdami paslaugas. 

Kai registruojate sąskaitą faktūrą, **SF likučio** kiekis kiekvienai prekei atnaujinamas nurodant bendruosius SF kiekius iš pasirinkto pardavimo užsakymo. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.

Peržiūrėti pardavimo užsakymų būseną galite sąrašo puslapyje **Visi pardavimo užsakymai**. Sąrašo puslapyje **Atidarytos klientų SF** galite peržiūrėti savo registruotas sąskaitas faktūras.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Registruoti ir spausdinti atskiras klientų SF, kurios paremtos važtaraščiais ir data
Šią procedūrą naudokite, kai užregistruotas vienas ar keli pardavimo užsakymo važtaraščiai. Kliento SF grindžiama šiais važtaraščiais ir atspindi juose nurodytus kiekius. SF finansinė informacija yra paremta informacija, įvesta jums registruojant SF. 

Galite sukurti kliento SF, pagrįstą prekių, išsiųstų iki dabar, važtaraščio eilute, net jei nebuvo išsiųstos visos konkretaus pardavimo užsakymo prekės. Tai galite atlikti jei, pavyzdžiui, jūsų juridinis subjektas per mėnesį vienam klientui išduoda vieną SF, kurioje pateikiama informacija apie visus siuntinius, išsiųstus tą mėnesį. Kiekvienas važtaraštis reiškia iš dalies arba visiškai atliktą pardavimo užsakymo prekių pristatymą. 

Jums užregistravus SF, **SF likučio** kiekis kiekvienai prekei yra atnaujinamas bendra pristatytų kiekių iš pasirinktų važtaraščių suma. Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF. 

Atsargų operacijos yra atnaujinamos SF numeriu, o būsena pardavimo užsakymo lauke **Eilutės būsena** pakeičiama į **SF išrašyta**. 

Peržiūrėkite pardavimo užsakymų būseną visų **pardavimo užsakymų** sąrašo puslapyje.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Konsoliduoti pardavimo užsakymus arba važtaraščius, norint juos registruoti
Šį procesą naudokite, kai vienam ar keliems pardavimo užsakymams galima išrašyti SF, ir norite juos konsoliduoti į vieną SF. 

**Pardavimo užsakymo** sąrašo puslapyje galite pasirinkti kelias SF ir tada joms konsoliduoti naudoti **Generuoti SF**. Puslapyje **SF registravimas** galite pakeisti **Suminio užsakymo** nustatymą, kad būtų sumuojama pagal užsakymo numerį (kai yra keli vieno pardavimo užsakymo važtaraščiai) arba pagal SF sąskaitą (kai yra keli vienos SF sąskaitos pardavimo užsakymai). Naudokite mygtuką **Išdėstyti**, kad pardavimo užsakymus pagal **Suminio užsakymo** parametrus konsoliduotumėte į vieną SF.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Skaidyti pardavimo užsakymo SF pagal vietą ir pristatymo informaciją
Pardavimo užsakymo kliento SF skaidymas pagal vietą arba pristatymo adresą galima **konfigūruoti** **gautinų sumų parametrų puslapio skirtuke Sumavimas.** 
 - Pasirinkite parinktį **Skaidymo metu, remiantis SF vieta**, registruodami kiekvienai svetainei sukurkite vieną SF. 
 - Pasirinkite skaidymo **remiantis SF pristatymo informacija parinktį,** norėdami registruojant sukurti vieną SF kiekvienam pardavimo užsakymo eilutės pristatymo adresui. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Registruoti pardavimo užsakymo eilučių be kainos ir išlaidų įplaukų sąskaitoje
Turite parinktį DK atnaujinti pardavimo užsakymo **eilučių,** kuriose **nėra** kainos ir nėra išlaidų, įplaukų sąskaitą. Norėdami nustatyti arba peržiūrėti šią informaciją, **·** **·** **eikite į gautinų sumų parametrų puslapio DK ir PVM skirtuko lape parametrą Registruoti įplaukų sąskaitoje dėl nulinių kainų ir nulinių išlaidų pardavimo užsakymo SF eilučių** parametrų. (**Gautinų sumų > gautinų sumų > parametrus**). Pasirinkite **Taip,** jei norite atnaujinti **pardavimo** užsakymo SF eilučių, kuriose nėra kainos ir išlaidų, sąskaitą Įplaukos. Jei ši pasirinktis pasirinkta, kvite bus 0,00 įrašų kliento **balanse ir įplaukų** **registravimo** tipuose. Įplaukų sąskaita yra apibrėžta atsargų registravimo **parametrų** puslapyje, pardavimo užsakymo **sąskaitos** apibrėžimo skirtuke. Jei ši pasirinktis nepasirinkta, eilutės, kuriose nėra kainos arba išlaidų informacijos, nebus registruojamos Įplaukų **sąskaitoje**. Vietoj to kvite bus kliento balanso registravimo tipo 0,00 **įrašas**.

## <a name="line-creation-sequence-number-information"></a>Eilutės kūrimo eilės numerio informacija
Kai registruojate kliento SF eilutes, galite pasirinkti nuoseklius eilučių kūrimo eilės numerius. Eilutės kūrimo eilės numeriai priskiriami registravimo proceso metu. Leisdami ne nuoseklią numeraciją, galite pagerinti kliento SF registravimo našumą. Eilutės kūrimo eilės numerius gali naudoti trečiosios šalies integravimas, kuris laukia nuoseklios eilės. Dėl plėtinių, kurie gali būti integruoti su eilutės kūrimo eilės numeriais, kreipkitės į IT padalinį.

Norėdami nustatyti ar peržiūrėti šią informaciją, **skirtuko** Gautinos sumos parametrų puslapyje, **·** **skirtuke Atnaujinimai nustatykite pasirinktį Priskirti nuoseklius eilučių numerius registruodami kliento SF** eilutes:

- Nustatykite pasirinktį **Ne**, jei norite naudoti nuoseklų eilučių kūrimo sekos numerių numeravimą.
- Norėdami naudoti nuoseklų **numeravimą**, nustatykite pasirinktį Taip. Turite nustatyti pasirinktį Taip juridiniams **subjektams**, kurių adresas yra Italija. Taip pat turite nustatyti jį kaip **Taip**, jei **išjungtas CustInvoiceTransCreationSeqNumFlight** skrydis.

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
<li><strong>Nėra</strong> – kredito limito tikrinimas nėra reikalaujamas.</li>
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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
