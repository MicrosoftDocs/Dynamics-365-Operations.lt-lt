---
title: Pirkimo paraiškos apžvalga
description: Šioje temoje aprašoma pirkimo paraiškos darbo eiga ir skirtingos galimos pirkimo paraiškos būsenos.
author: kamaybac
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0fc2f6104bc8a79ea4e8b6d0061f4b135026de0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825259"
---
# <a name="purchase-requisition-overview"></a>Pirkimo paraiškos apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma pirkimo paraiškos darbo eiga ir skirtingos galimos pirkimo paraiškos būsenos.

Atsižvelgdami į jūsų organizacijos nustatymą, galite sukurti pirkimo paraiškas produktams, kuriuos naudoja jūsų organizacija. Pirkimo paraiška yra vidinis dokumentas, įgaliojantis Pirkimo skyrių pirkti prekes arba paslaugas.  

Kai pirkimo paraiška patvirtinta, ją galima naudoti pirkimo užsakymui generuoti. Pirkimo užsakymai yra išoriniai dokumentai, kuriuos Pirkimo skyrius pateikia tiekėjams.

## <a name="creating-purchase-requisitions"></a>Pirkimo paraiškų kūrimas
Galite sukurti pirkimo paraišką puslapyje **Mano pirkimo paraiškos** ir pasirinkti reikiamas prekes ir paslaugas. Galite pasirinkti prekes iš jūsų organizacijos sukurto įsigijimo katalogo arba prašyti prekių, kurių nepavyko rasti kataloge, pasirinkę įsigijimo kategoriją ir įvedę produkto informaciją.  

Prieš pateikiant peržiūrėti pirkimo paraišką, reikia sukonfigūruoti darbo eigas. Darbo eigą naudokite pirkimo paraiškai perkelti peržiūros proceso metu nuo pirminės būklės **Juodraštis** iki galutinės būklės **Patvirtinta**.

### <a name="purchase-requisition-statuses"></a>Pirkimo paraiškų būsenos

Sukūrus naują pirkimo paraišką, jai priskiriama būsena. Būsena priskiriama ir kiekvienai eilutei, kurią galite įtraukti į pirkimo paraišką. Pateikus pirkimo paraišką darbo eigai peržiūrėti, pirkimo paraiškos būsena ir kiekvienos eilutės būsena atnaujinamos eilutes perkeliant darbo eigos proceso metu.  

Pirkimo paraiškos darbo eigos procesą galite konfigūruoti ir nukreipti pirkimo paraišką peržiūros proceso metu kaip vieną dokumentą. Arba pirkimo paraiškos eilutės gali būti atskirai nukreipiamos atitinkamiems peržiūrėtojams. Jei pirkimo paraiškos eilutės peržiūrimos atskirai, kiekvienos pirkimo paraiškos eilutės būseną galima atnaujinti, eilutei judant per peržiūros procesą. Kai visų eilučių peržiūros procesas baigtas ir nebeliko jokių pirkimo paraiškos peržiūros proceso veiksmų, atnaujinama visos pirkimo paraiškos būsena.

### <a name="purchase-requisition-workflow"></a>Pirkimo paraiškos darbo eiga

Pateiktoje diagramoje rodomos pirkimo paraiškai ir pirkimo paraiškos eilutei priskirtos būsenos, kai šios perkeliamos darbo eigos proceso metu.  

[![Pirkimo paraiškos antraštės ir eilutės būsenos](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Pirkimo paraiškos antraštės ir eilutės būsenų ryšys

Bendrąją pirkimo paraiškos būseną nustato pirkimo paraiškos eilučių būsena. Todėl visų pirkimo paraiškos eilučių peržiūros procesas turi būti baigtas prieš užbaigiant visos pirkimo paraiškos peržiūros procesą. Pateiktoje lentelėje apibūdinamos pirkimo paraiškos antraštei ir eilutėms priskirtos būsenos, kai pirkimo paraiška perkeliama darbo eigos proceso metu.

<table>
<thead>
<tr class="header">
<th>Pirkimo paraiškos būsena</th>
<th>Pirkimo paraiškos eilutės būsena</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Juodraštis</td>
<td>Juodraštis</td>
<td>Pirkimo paraiška bei pirkimo paraiškos eilutė buvo sukurtos, bet jos dar nebuvo&#39; pateiktos peržiūrėti. Pirkimo paraišką ir pirkimo paraiškos eilutes, kurių būsena <strong>Juodraštis</strong>, galima modifikuoti. Pirkimo paraiškos arba pirkimo paraiškos eilutės, kuri buvo atšaukta, bet dar nėra&#39; pateikta peržiūrėti, būsena irgi yra <strong>Juodraštis</strong>. <strong>Pastaba:</strong> pirkimo paraišką galite pateikti arba atšaukti dokumento lygiu. Tačiau negalima&#39; pateikti arba atšaukti vienos pirkimo paraiškos eilutės.</td>
</tr>
<tr class="even">
<td>Peržiūrima</td>
<td><ul>
<li>Peržiūrima</li>
<li>Atmesta</li>
</ul></td>
<td>Jei darbo eiga buvo sukonfigūruota nukreipti pirkimo paraiškos eilutes atskiriems redaktoriams, kiekvienos eilutės būsena gali būti <strong>Peržiūrima</strong> arba <strong>Atmesta</strong>. Kai visų pirkimo paraiškos eilučių peržiūros procesas baigtas ir nebeliko jokių pirkimo paraiškos peržiūros proceso veiksmų, atnaujinama pirkimo paraiškos būsena.
<ul>
<li><strong>Peržiūrima</strong> – pirkimo paraiškos eilutės pateiktos peržiūrėti. Kai pirkimo paraiškos eilutės darbo eigos procesas yra baigtas, tos eilutės būsena lieka <strong>Peržiūrima</strong> tol, kol bus peržiūrėtos visos likusios pirkimo paraiškos eilutės.</li>
<li><strong>Atmesta</strong> – pirkimo paraiškos eilutė atmesta. Pirkimo paraiškos eilutes, kurios buvo atmestos, galima pakeisti ir pateikti iš naujo.</li>
</ul>
Jei iš naujo pateikiate pirkimo paraiškos eilutę, kuri buvo atmesta, peržiūros procesas prasideda visoms pirkimo paraiškos eilutėms, kurios vis dar peržiūrimos. </br><strong>Pastaba:</strong> galima atšaukti jau pateiktą pirkimo paraišką. Atšaukus pirkimo paraišką, taip pat atšaukiamos visos kitos pirkimo paraiškos eilutės. Galima panaikinti pirkimo paraiškos eilutes, kurios buvo atšauktos.</td>
</tr>
<tr class="odd">
<td>Atmesta</td>
<td>Atmesta</td>
<td>Pirkimo paraiška ir visos pirkimo paraiškos eilutės atmestos. Pirkimo paraišką ir pirkimo paraiškos eilutes, kurios buvo atmestos, galima pateikti iš naujo.</td>
</tr>
<tr class="even">
<td>Patvirtinta</td>
<td><ul>
<li>Patvirtinta</li>
<li>Atšaukta</li>
<li>Uždaryta</li>
</ul></td>
<td>Visų pirkimo paraiškos eilučių peržiūros procesas baigtas ir nebeliko jokių šios pirkimo paraiškos peržiūros proceso veiksmų.
<ul>
<li><strong>Patvirtinta</strong> – pirkimo paraiškos eilutės peržiūros procesas baigtas, eilutė yra patvirtinta.</li>
<li><strong>Atšaukta</strong> – pirkimo paraiškos eilutė buvo patvirtinta, bet ji buvo atšaukta, nes ji&#39; nebebus reikalinga. Galima atšaukti tik tas pirkimo paraiškos eilutes, kurios buvo patvirtintos.</li>
<li><strong>Uždaryta</strong> – pirkimo paraiškos eilutė buvo patvirtinta ir dokumentai buvo sugeneruoti atsižvelgiant į paraiškos paskirtį.
<ul>
<li>Jei paraiškos paskirtis yra suvartojimas, sugeneruojamas pirkimo paraiškos eilutės pirkimo užsakymas.</li>
<li>Jei paraiškos paskirtis yra papildymas, sugeneruojami vienas ar keli įvykdymo dokumentai.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Atšaukta</td>
<td>Atšaukta</td>
<td>Pirkimo paraiška ir visos pirkimo paraiškos eilutės atšauktos.</br> <strong>Pastaba:</strong> jei jums nebereikia pirkimo paraiškos eilutėje nurodytos prekės, turite atšaukti pirkimo paraiškos eilutę, jeigu ji jau buvo patvirtinta. Galima atšaukti tik tas pirkimo paraiškos eilutes, kurios buvo patvirtintos. Jei kuri nors pirkimo paraiškos eilutė peržiūrima, pirkimo paraiškos būsena yra <strong>Peržiūrima</strong>. Tokiu atveju galite atšaukti pirkimo paraišką ir panaikinti atitinkamą pirkimo paraiškos eilutę.</td>
</tr>
<tr class="even">
<td>Uždaryta</td>
<td><ul>
<li>Uždaryta</li>
<li>Atšaukta</li>
</ul></td>
<td>Pirkimo paraiška uždaryta, sugeneruoti vienas ar keli įvykdymo dokumentai.
<ul>
<li><strong>Uždaryta</strong> – pirkimo paraiškos eilutė buvo patvirtinta ir dokumentai buvo sugeneruoti atsižvelgiant į paraiškos paskirtį.
<ul>
<li>Jei paraiškos paskirtis yra suvartojimas, sugeneruojamas pirkimo paraiškos eilutės pirkimo užsakymas.</li>
<li>Jei paraiškos paskirtis yra papildymas, sugeneruojami vienas ar keli įvykdymo dokumentai.</li>
</ul></li>
<li><strong>Atšaukta</strong> – pirkimo paraiškos eilutė buvo patvirtinta, bet ji buvo atšaukta, nes ji&#39; nebebus reikalinga. Galima atšaukti tik tas pirkimo paraiškos eilutes, kurios buvo patvirtintos.</li>
</ul>
<strong>Pastaba:</strong> jei jums nebereikia prekės, nurodytos uždarytoje pirkimo paraiškos eilutėje, turite atšaukti eilutę įvykdymo dokumente, kuris buvo sugeneruotas pirkimo paraiškos eilutei.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Išlaidų paskirstymas į keletą finansinių sąskaitų
Galite paskirstyti produktų išlaidas, kurios pirkimo paraiškoje yra įtrauktos į keletą finansinių ataskaitų. Jei jūsų organizacija naudoja dimensijas, pavyzdžiui, išlaidų centrams ir padaliniams, galite paskirstyti produkto savikainą dimensijoms finansinėms ataskaitoms.

## <a name="requisition-purposes"></a>Paraiškos paskirtys
Dėl paraiškos paskirčių paraiškos poreikio įvykdymo procesas yra lankstesnis. Kurdami paraišką galite priskirti jai vieną iš dviejų paskirčių: vartojimas arba papildymas. Priklausomai nuo paraiškos paskirties ir jūsų organizacijos nustatymo, paraiškos poreikį galima tenkinti pirkimo užsakymu, perkėlimo užsakymu, gamybos užsakymu arba „kanban“.  

Įsigijimo strategijose galite valdyti paraiškos paskirtis, kurios galimos tuo metu, kai jūsų organizacijai sukuriama paraiška.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Paraiškos, kurių paskirtis yra vartojimas

Paraiška, kurios paskirtis yra suvartojimas, rodo jūsų organizacijos viduje naudojamų prekių ar paslaugų paklausą. Paklausa, kurią kuria tokios paraiškos visuomet patenkinama pirkimo užsakymu. Jei Tiekimo grandinės valdyme yra nustatyta automatiškai generuoti pirkimo užsakymus, pirkimo užsakymai bus sukurti po to, kai pirkimo paraiška bus patvirtinta.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Paraiškos, kurių paskirtis yra papildymas

Paraiška, kurios paskirtis yra papildymas, atspindi poreikį papildyti atsargas. Pvz., sukuriate paraišką prekėms papildyti, kad jas būtų galima parduoti konkrečioje mažmeninės prekybos vietoje konkrečiu metu. Tokia paraiška sukurtą poreikį galima patenkinti pirkimo užsakymu, perkėlimo užsakymu, gamybos užsakymu arba „kanban“.  

Jei paraiškos paskirtis yra papildymas, poreikis išreiškiamas kaip kiekis, o ne kaip piniginė suma. Todėl biudžeto rezervavimo paraiška, biudžeto kontrolė, ilgalaikio turto nustatymo verslo taisyklės (BRAD), projekto apskaita ir susijusios taisyklės netaikomos. Tenkinti papildymo paraiškos poreikį gali tik produktai, laikomi ir išleidžiami nurodytam juridiniam subjektui. Norėdami nustatyti produktus, kurie yra prieinami, kai paraiškos paskirtis yra papildymas, naudokite puslapį **Papildymo kategorijos prieigos strategijos taisyklė**.  

Norint naudoti pirkimo paraiškas, kurių paskirtis yra papildymas, turite nustatyti, kad į bendrąjį planavimą būtų įtrauktas paraiškos poreikis. Pagal šios rūšies paraišką sukurto poreikio patenkinimo būdas automatiškai nustatomas pagal jūsų organizacijos prekėms sukurtą ir naudojant bendrąjį planavimą suplanuotą tiekimo strategiją.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Pirkimo paraiškos ir pasiūlymo reikalavimai
Kai kuriais atvejais, galite pradėti pasiūlymo patvirtinimo (RFQ) procesą, norėdami identifikuoti pirkimo paraiškoje nurodytų produktų tiekėją ir kainą. RFQ galima generuoti, kai pirkimo paraiška yra peržiūrima. Priėmus pasiūlymą, informacija apie tiekėją, kainą ir kt. perkeliama į paraišką.  

Galite sulaikyti pirkimo paraišką puslapyje **Pirkimo paraiškos informacija** pažymėdami žymės langelį **Sulaikyta**. Pirkimo paraiškos apdorojimą galite tęsti tik pašalinę sulaikymą panaikindami žymės langelio žymėjimą.  

> [!NOTE]
> El. pirkime, jūsų pirkimo paraiškos RFQ gali leisti tiekėjams pridėti alternatyvių eilučių. Tokiu atveju, jūsų pirkimo paraiškoje bus nurodyti patvirtinti pakeitimai.

## <a name="demand-consolidation"></a>Poreikio konsolidacija
Konsolidavę pirkimo paraiškos eilutes iš kelių pirkimo paraiškų, galite efektyviau derėtis su tiekėjais dėl geresnių kainų, mažesnių siuntimo ir tvarkymo išlaidų ir mažesnių pridėtinių išlaidų.  

Pirkimo paraiškos eilutės tinka poreikio konsolidavimui atlikti tik tada, jei šie teiginiai yra teisingi:

-   Pirkimo paraiška yra patvirtinta.
-   Pirkimo paraiška atitinka pirkimo strategijos taisyklės kriterijus, taikomus apdorojimui rankiniu būdu ir poreikio konsolidavimui.

Patvirtintos pirkimo paraiškos eilutės, kurios atitinka neautomatinio apdorojimo kriterijus, yra įtrauktos į puslapį **Išleisti patvirtintas pirkimo paraiškas**. Jei pirkimo paraiškos eilutė taip pat atitinka poreikio konsolidavimo kriterijus, eilutę galima įtraukti į konsolidavimo galimybę.  

Konsolidavimo galimybė yra rinkinys pirkimo paraiškos eilučių, kurios yra sugrupuotos taip, kad pirkimo specialistas galėtų derėtis su tiekėjais dėl geriausio pasiūlymo. Pirkimo paraiškos eilutės, kurias pasirinkote konsolidavimo galimybei, rodomos puslapyje **Pirkimo paraiškos konsolidavimas**. Jei reikia atlikti pakeitimų, galite modifikuoti eilutes šiame puslapyje. Be to, į konsolidavimo galimybę galite įtraukti naujų eilučių arba pašalinti esamas eilutes.  

Įtraukę paraiškos eilutes į konsolidavimo galimybę ir atlikę reikiamus pakeitimus, galite sukurti pirkimo užsakymą pagal konsoliduotas pirkimo paraiškos eilutes.  

> [!NOTE]
> Pakeitimai, atlikti pirkimo paraiškos eilutėje, puslapyje **Pirkimo paraiškos konsolidacija**, matomi jūsų sukurtame pirkimo užsakyme. Tačiau pirkimo paraiškoje eilutė lieka nepakeista, kad būtų galima peržiūrėti retrospektyvos informaciją.  

Norėdami sukurti pirkimo užsakymą pagal pirkimo paraiškos eilutes, kurios neatitinka poreikio konsolidavimo arba kurios nepasirinktos įtraukti į konsolidavimo galimybę, turite šias eilutes apdoroti neautomatiniu būdu.

### <a name="consolidating-purchase-requisition-lines"></a>Pirkimo paraiškos eilučių konsolidavimas

Poreikio konsolidavimo procesas prasideda darbo eigoje patvirtinus pirkimo paraišką ir įrašius biudžeto rezervavimus ir preliminarius biudžeto rezervavimus, jei jūsų organizacijoje sukonfigūruota biudžeto kontrolė. Šioje diagramoje pavaizduota poreikio konsolidavimo proceso eiga.  

[![Poreikio konsolidavimo proceso eiga](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Norėdami konsoliduoti patvirtintas pirkimo paraiškos eilutes, atlikite toliau nurodytus veiksmus.

1.  Peržiūrėkite patvirtintas paraiškos eilutes, kurias reikia apdoroti rankiniu būdu ir kurios atitinka poreikio konsolidavimo kriterijus.
2.  Pasirinkite eilutes įtraukti į konsolidacijos galimybę.
3.  Sukurkite naują konsolidavimo galimybę arba įtraukite paraiškos eilutes į esamą konsolidavimo galimybę.
4.  Atlikite atitinkamus pakeitimus paraiškos eilutėse ir pašalinkite paraiškos eilučių elementus, kurių nebenorite įtraukti į konsolidavimo galimybę.
5.  Kurkite pirkimo užsakymus pagal konsoliduotas paraiškos eilutes arba pagal konsolidavimo galimybės pirkimo paraiškos eilutes.


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Vartojimo paraiškos kūrimas](tasks/create-requisition-consumption.md)

[Pirkimo paraiškos darbo eiga](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]