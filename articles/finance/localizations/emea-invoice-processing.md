---
title: SF apdorojimas
description: Šioje temoje pateikiama informacijos apie sąskaitų faktūrų apdorojimą Rytų Europoje.
author: v-kikozl
manager: AnnBe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia, Italy
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 87a06e1b17e9c0bdb4147f49b2dacb74236360fa
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039809"
---
# <a name="invoice-processing"></a>SF apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje trumpai aprašomi keli konkrečių šalių scenarijai, pvz., ES vidaus pridėtinės vertės mokestis (PVM) ir atidėtas mokestis. Sąskaitų faktūrų išrašymo procesui taikomi kai kurių Europos šalių teisiniai reikalavimai. Šioje temoje taip pat pateikiama informacijos apie tai, kaip šiose šalyse apdorojamos klientų ir tiekėjų sąskaitos faktūros. 
<table>
<thead>
<tr>
<th>Scenarijus</th>
<th>Šalys</th>
<th>Funkcijų pakeitimų aprašas</th>
</tr>
</thead>
<tbody>
<tr>
<td>PVM gautinų sumų ir mokėtinų sumų datos</td>
<td>Čekija, Lenkija</td>
<td>
<p>Prekes perkant iš Europos Sąjungos (ES) šalių, taikomas įsipareigojimas PVM įvertinti patiems.</p>
<ul>
<li>Mokėtiną PVM reikia sumokėti per PVM laikotarpį, kuriuo išduota sąskaita faktūra (dokumento data).</li>
<li>Gautino PVM negalima atskaityti prieš gaunant dokumentą (PVM registro data).</li>
</ul>
<p>Kad būtų galima taikyti šį scenarijų, reikia sukonfigūruoti tolesnius parametrus.</p>
<ul>
<li>Puslapyje <strong>Mokėtinų sumų parametrai</strong> įjunkite parametrus <strong>ES vidaus PVM</strong> ir <strong>ES vidaus PVM dokumento data</strong>.</li>
<li>Nustatykite du PVM kodus, vieną – su teigiamu PVM procentu ir vieną – su neigiamu.</li>
<li>Nustatykite PVM grupę, kurioje būtų tiek teigiami, tiek neigiami PVM kodai. Neigiamo PVM kodo parametrą <strong>ES vidaus PVM</strong> nustatykite kaip <strong>Taip</strong>.</li>
</ul>
<p>Sėkmingai tai nustačius, perkant bus registruojamos dvi tolesnės PVM operacijos.</p>
<ul>
<li>Teigiama operacija su <strong>gautino PVM</strong> kryptimi ir PVM registro data, lygia sąskaitos faktūros registravimo puslapyje nurodytai datai.</li>
<li>Neigiama operacija su <strong>mokėtino PVM</strong> kryptimi ir PVM registro data, lygia dokumento datai.</li>
</ul>
</td>
</tr>
<tr>
<td>Modifikuokite pardavimo dokumento datą.</td>
<td>Visos Rytų Europos šalys</td>
<td><p>Galite modifikuoti projekto sąskaitos faktūros lauką <strong>Dokumento data</strong>. Ši data rodoma išspausdintoje sąskaitoje faktūroje.</p>
<p>Laukas <strong>Dokumento data</strong> taip pat yra puslapiuose <strong>Registravimo sąskaita faktūra</strong> ir <strong>Laisvos formos sąskaita faktūra</strong>. Užregistravus sąskaitą faktūrą, dokumento data rodoma jos antraštėje.</p>
</td>
</tr>
<tr>
<td>Valiutų kursų dokumento data</td>
<td>Lenkija, Vengrija, Čekijos Respublika, Italija</td>
<td>
<p>Teisės aktuose nurodytos skirtingos taisyklės, taikomos renkantis verslo operacijoms tinkamus valiutų kursus. Puslapiuose <strong>Gautinų sumų parametrai</strong> ir <strong>Mokėtinų sumų parametrai</strong> esančiame lauke <strong>Valiutos kurso data</strong> galite pasirinkti datą, kurią reikia naudoti su sumomis skaičiuojant apskaitos valiutą pirkimo ir pardavimo dokumentuose. Kai įvedami duomenys, sistema pagal šį parametrą gauna operacijos valiutos kursą.</p>
<blockquote>[!NOTE]<br>Italijoje ši funkcija taikoma tik modulyje Mokėtinos sumos. Mokėtinų sumų parametruose vartotojas gali pasirinkti <strong>registravimo datą</strong> arba <strong>dokumento datą</strong> lauke <strong>Valiutos kurso data</strong>.   </blockquote>
<blockquote>[!NOTE]<br>Kai lauką <strong>Valiutos kurso data</strong> nustatote kaip <strong>Dokumento data (tik ES prekybai)</strong>, sistema naudoja PVM grupę. PVM grupės skirtuke <strong>Bendra</strong> yra parametras <strong>ES prekyba</strong>. Jei PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Taip</strong> ir jei ši PVM grupė nurodyta dokumento antraštėje, sistema valiutos kursą gauna pagal dokumento datą. Jei šios PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Ne</strong>, sistema valiutos kursą gauna pagal dokumento registravimo datą.</blockquote>
</td>
</tr>
<tr>
<td>Prekybos datų, PVM registro datų ir dokumentų bei PVM datų valdymas</td>
<td>Lenkija, Vengrija, Čekija</td>
<td>
<p>Pardavimo datą ir dokumento gavimo datą būtina nurodyti teikiant PVM ataskaitas.</p>
<ul>
<li>Pardavimo data – tai operacijos įvykdymo data modulyje Gautinos sumos.</li>
<li>Dokumento gavimo data – tai data, kuri parodo teisę reikalauti PVM atskaitymo modulyje Mokėtinos sumos. Kiekviename gautame dokumente audito tikslais nurodyta data.</li>
</ul>
<p>Į Vengrijos datų terminų funkcijas, Čekijos įvykdymo datų funkcijas ir Lenkijos PVM registravimo datų funkcijas įtrauktas mokesčių informacijos ataskaitų reikalavimas, paremtas data, kuri skiriasi nuo registravimo datos.</p>
<p>Laukas <strong>PVM registro data</strong> palaiko šį reikalavimą ir yra rodomas daugiau nei 20-yje puslapių. Šie puslapiai – tai žurnalai, pardavimo užsakymai, pirkimo užsakymai, laisvos formos sąskaitos faktūros, tiekėjų sąskaitų faktūrų žurnalai ir projektų sąskaitos faktūros. Kai atnaujinate ar registruojate dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data įtraukiama į puslapius, pvz., klientų ir tiekėjų sąskaitų faktūrų žurnalų puslapius.</p>
<p>Konkrečiai Čekijoje, jei PVM registravimas atidedamas, registravimo metu laukas <strong>PVM registro data</strong> gali būti tuščias. Kitu atveju laukas yra privalomas ir jį reikia užpildyti.</p>
<p>Datos tikrinimo parametrus galima nustatyti puslapyje <strong>PVM grupės</strong>.</p>
<ul>
<li>Parametrai <strong>PVM registro pildymo data</strong> ir <strong>Pardavimo datos pildymas</strong> naudojami kaip numatytasis atitinkamų datų pildymo būdas. Taip pat galima naudoti rankinės įvesties ir kelis automatinės įvesties būdus.</li>
<li>Laukas <strong>Privaloma pardavimo data</strong> nurodo, ar, prieš registruojant pardavimo sąskaitą faktūrą, reikia įvesti pardavimo datą.</li>
</ul>
<p>Puslapyje <strong>PVM registro operacijos</strong> galite užpildyti tuščius registruotų mokesčių operacijų PVM registro datų laukus.</p>
</td>
</tr>
<tr>
<td>PVM registravimo datos, į kurias įtraukti atidėti mokesčiai</td>
<td>Vengrija</td>
<td>
<p>Pagal Vengrijos mokesčių įstatymų reikalavimus sąskaitas faktūras reikia sukurti jų įvykdymo metu arba ne vėliau kaip per 15 dienų po įvykdymo.</p>
<p>Įvykdymo data yra užsakytų paslaugų suteikimo data arba užsakytų prekių pristatymo data. Atnaujinant ar registruojant dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data rodoma atitinkamuose puslapiuose. Be to, pagal reikalavimus, nuolat teikiant paslaugas, pvz., nuomos, konsultavimo ar šildymo, PVM turi atitikti tolesnius kriterijus.</p>
<ul>
<li>PVM sąskaitos faktūros dieną turi būti registruojamas paskirtoje DK sąskaitoje.</li>
<li>PVM termino dieną turi būti perkeltas iš specialių sąskaitų į gautino arba mokėtino PVM sąskaitą ir jį reikia įtraukti į PVM ataskaitą.</li>
</ul>
<p>Kad galėtumėte įvykdyti šiuos reikalavimus, didžiosios knygos registravimus galite perkelti į atidėtų gaunamų mokesčių sąskaitą ir atidėtų išmokamų mokesčių sąskaitą. Tačiau pirmiausia turite įvykdyti tolesnes būtinąsias sąlygas.</p>
<ul>
<li>Didžiosios knygos registravimo grupėse nustatyti atidėto mokėtino PVM ir atidėto gautino PVM DK sąskaitas.</li>
<li>Įjungti prekių PVM grupių parametrą <strong>Atidėtas PVM</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>Privaloma PVM data</td>
<td>Lenkija</td>
<td>
<p>Galite reikalauti, kad PVM registro data būtų įtraukta į pirkimo ir pardavimo operacijų įrašus. Todėl PVM registro datą galima užfiksuoti prieš užregistruojant operaciją. Naudojant šią funkciją galima išvengti situacijos, kai laikotarpio pabaigoje reikia tvarkyti kelias operacijas.</p>
<p>Lauką <strong>PVM registro data</strong> galite padaryti privalomą registruojant klientų ar tiekėjų operacijas. Norėdami šį lauką padaryti privalomą, įjunkite susijusios kliento ar tiekėjo sąskaitos parinktį <strong>Būtina nurodyti PVM datą</strong>.</p>
</td>
</tr>
</tbody>
</table>
