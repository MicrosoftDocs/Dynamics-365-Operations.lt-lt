---
title: Atvirkštinio mokesčio PVM
description: Šioje temoje paaiškinama, kaip nustatyti atvirkštinio mokesčio pridėtinės vertės mokestį (PVM) Europos šalyse ir Saudo Arabijoje.
author: epodkolz
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 530ff52abb1dd36c473ae436d61ea925c5696a30
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183769"
---
# <a name="reverse-charge-vat"></a>Atvirkštinio mokesčio PVM


[!include [banner](../includes/banner.md)]


Šioje temoje aprašomas bendrasis atvirkštinio apmokestinimo pridėtinės vertės mokesčiu (PVM) nustatymo metodas Saudo Arabijoje ir Europos šalyse.

Atvirkštinis apmokestinimas yra mokesčio schema, kuri atsakomybę už apskaitą ir PVM ataskaitas perkelia nuo pardavėjo prekių ir (arba) paslaugų pirkėjui. Todėl savo PVM išraše prekių ir (arba) paslaugų gavėjai praneša ir mokėtiną PVM (atlikdami pardavėjo vaidmenį), ir gautiną PVM (atlikdami pirkėjo vaidmenį).

Kai kuriose šalyse ar regionuose atvirkštinio apmokestinimo schema taikoma tik tam tikroms prekėms ir (arba) paslaugoms ir yra papildomų sąlygų arba pardavimo sumų ribinių verčių. Kitose šalyse ar regionuose PVM mokėjimo atsakomybė priklauso nuo tiekėjo ir pirkėjo būsenos. Jei pirkėjas turi sumokėti PVM, tai turi būti aiškiai pažymėta tiekėjo išduotoje SF. Pvz., SF turi būti žodžiai „atvirkštinis mokestis“ ir turi būti nurodyta, kurios pareigos apmokestinamos pagal atvirkštinio mokesčio schemą. 

Norėdami taikyti atvirkštinį mokestį, turite atlikti toliau nurodytą sąranką.

## <a name="set-up-sales-tax-codes"></a>Nustatyti PVM kodus
Pardavimo ir pirkimo operacijoms rekomenduojame naudoti atskirus PVM kodus.

<table>
<body>
<tr>
<td><strong>Pardavimo PVM kodas</strong></td>
<td>Sukurkite atvirkštinio mokesčio pardavimo operacijų PVM kodą (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM kodai</strong>).
</td>
</tr>
<tr>
<td><strong>Pirkimo PVM kodas</strong></td>
<td><p>Sukurkite teigiamus ir neigiamus pirkimo atvirkštinio mokesčio PVM kodus (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM kodai</strong>).</p>
<ol>
<li>Sukurkite teigiamos reikšmės PVM kodą.</li>
<li>Sukurkite neigiamos reikšmės PVM kodą. Nustatykite funkcijos <strong>Leisti neigiamą PVM procentą</strong> parinktį <strong>Taip</strong>.
Turite priskirti neigiamą PVM kodą prekės PVM grupei, o po to tą PVM grupę priskirti prekėms, kurios yra atvirkštinio PVM subjektas.</li>
</ol>
<p>Daugiau informacijos ieškokite kitame skyriuje &quot;PVM grupių ir prekių PVM grupių nustatymas&quot;.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Nustatyti PVM grupes ir prekių PVM grupes
Pardavimo ir pirkimo operacijoms rekomenduojame naudoti atskiras PVM grupes.

<table>
<tr>
<td><strong>Pardavimo PVM grupės</strong></td>
<td>Sukurkite atvirkštinio mokesčio pardavimo operacijų PVM grupę (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM grupės</strong>). Šios grupės skirtuke <strong>Sąranka</strong> įtraukite atvirkštinio mokesčio PVM kodą. Pažymėkite PVM kodo žymės langelius <strong>Neapmokestinama</strong> ir <strong>Atvirkštinis mokestis</strong>.</td>
</tr>
<tr>
<td><strong>Pirkimo PVM grupės</strong></td>
<td>Sukurkite atvirkštinio mokesčio pirkimo operacijų PVM grupę (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM grupės</strong>). Skirtuke <strong>Sąranka</strong> į šią grupę įtraukite ir teigiamus, ir neigiamus PVM kodus. Pažymėkite neigiamos reikšmės PVM kodo žymės langelį <strong>Atvirkštinis mokestis</strong>.</td>
</tr>
<tr>
<td><strong>Prekės PVM grupės</strong></td>
<td>Sukurkite arba atnaujinkite prekės PVM grupę, kuriai priskirtas neigiamos reikšmės PVM kodas (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>Prekės PVM grupės</strong>). Numatytąją prekės PVM grupę turite priskirti tiems produktams ir kategorijoms, kurioms taikomas atvirkštinis mokestis.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Atvirkštinio apmokestinimo grupių nustatymas
Puslapyje **Atvirkštinio apmokestinimo prekių grupės** (**Mokestis** &gt; **Sąranka** &gt; **PVM** &gt; **Atvirkštinio apmokestinimo prekių grupės**) galite nurodyti produktų, paslaugų arba atskirų prekių, paslaugų, kurioms gali būti taikomas atvirkštinis apmokestinimas, grupes. Nurodykite kiekvienos atvirkštinio apmokestinimo prekių grupės prekių, prekių grupių bei pardavimų ir (arba) pirkimų kategorijų sąrašą.

## <a name="set-up-reverse-charge-rules"></a>Atvirkštinio apmokestinimo taisyklių nustatymas
Puslapyje **Atvirkštinio apmokestinimo taisyklės** (**Mokestis** &gt; **Sąranka** &gt; **PVM** &gt; **Atvirkštinio apmokestinimo taisyklės**) galite nustatyti pirkimo ir pardavimo tikslais naudojamas tinkamumo taisykles. Galite sukonfigūruoti atvirkštinio mokesčio taikymo taisyklių rinkinį. Nustatykite šiuos kiekvienos taisyklės laukus:

- **Dokumento tipas** – pasirinkite **Pirkimo užsakymas**, **Tiekėjo SF žurnalas**, **Pardavimo užsakymas**, **Laisvos formos SF**, **Kliento SF žurnalas** ir (arba) **Tiekėjo SF**.
- **Partnerio šalies / regiono tipas** – pasirinkite **Vietinis**, **ES** arba **Užsienio**. Arba, jeigu taisyklė gali būti taikoma visiems prekybos partneriams, nepriklausomai nuo jų šalies ar regiono adreso, pasirinkite **Visi**.
- **Vietinis pristatymo adresas** – pažymėkite šį žymės langelį, jei norite taikyti taisyklę visoms į tą pačią šalį ar regioną pristatomoms prekėms. Pasirinkus dokumentų tipus **Tiekėjo SF žurnalas** ir **Kliento SF žurnalas** šio žymės langelio pažymėti negalima.
- **Atvirkštinio apmokestinimo prekių grupė** – pasirinkite grupę, kuriai gali būti taikoma taisyklė.
- **Ribinės vertės suma** – SF atvirkštinio apmokestinimo schema taikoma tik tada, jei prekių ir (arba) paslaugų, kurios įtrauktos į atvirkštinio apmokestinimo prekių grupę vertė viršija limitą, kurį nurodote čia.

Laukus **Galioja nuo** ir **Galiojimo data** taip pat galite naudoti norėdami nurodyti laikotarpį, kada galioja taisyklė.

Be to, galite nurodyti, ar, jei bus patenkinta tos dokumento eilutės sąlyga, bus rodomas pranešimas ir ar bus atnaujinta dokumento eilutėje nurodyta numatytoji atvirkštinio apmokestinimo PVM grupė. Galimos toliau nurodytos pasirinktys:

- **Nė vienas iš atvejų** – dokumento eilutė neatnaujinama.
- **Raginti** – rodomas pranešimas, raginantis patvirtinti, kad galima taikyti atvirkštinio apmokestinimo mokestį.
- **Nustatyti** – dokumento eilutė atnaujinama be papildomų pranešimų.

## <a name="set-up-default-parameters"></a>Numatytųjų parametrų nustatymas
Norėdami įgalinti atvirkštinio mokesčio PVM funkciją, puslapio **DK parametrai** skirtuke **Atvirkštinis apmokestinimas** nustatykite funkcijos **Įgalinti atvirkštinį apmokestinimą** parinktį **Taip**. Laukuose **Pirkimo užsakymų PVM grupė** ir **Pardavimo užsakymų PVM grupė** pasirinkite numatytąsias PVM grupes. Kai patenkinama atvirkštinio mokesčio taikymo sąlyga, pardavimo arba pirkimo užsakymo eilutės atnaujinamos nurodant šias PVM grupes.

## <a name="reverse-charge-on-a-sales-invoice"></a>Pardavimo SF atvirkštinis apmokestinimas
Pagal atvirkštinio apmokestinimo schemą atliekamiems pardavimamas pardavėjas PVM mokesčio netaiko. Tačiau SF nurodomos abi prekės, kurioms taikytinas atvirkštinio apmokestinimo PVM, bei bendra atvirkštinio PVM suma.

Užregistravus atvirkštinio apmokestinimo pardavimo SF, PVM operacijos pažymimos mokesčių nuoroda **Mokėtinas PVM** bei nulinio PVM mokesčio nuoroda ir pažymimas žymės langelis **Atvirkštinis apmokestinimas**.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Pirkimo SF atvirkštinis apmokestinimas
Kai pirkimai atliekami pagal atvirkštinio apmokestinimo schemą, atvirkštinio apmokestinimo SF gavęs pirkėjas PVM apskaitos tikslais yra ir pirkėjas, ir pardavėjas.

Užregistravus atvirkštinio apmokestinimo pirkimo SF sukuriamos dvi PVM operacijos. Viena operacija pažymėta mokesčių nuoroda **Gautinas PVM**. Kita operacija pažymėta mokesčių nuoroda **Mokėtinas PVM** ir pažymėtas žymės langelis **Atvirkštinis apmokestinimas**.

Toliau pateiktoje ekrano kopijoje vienos operacijos kryptis yra **Gautinas PVM**, o kitos – **mokėtinas PVM**. 

![Užregistruotas PVM](media/apac-sau-posted-sales-tax.png)
