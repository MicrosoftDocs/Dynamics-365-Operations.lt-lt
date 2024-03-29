---
title: Pristatymo alternatyvos
description: Pardavimo užsakymų priėmėjai gali naudoti puslapį Pristatymo alternatyvos, norėdami sužinoti alternatyvias užsakymo įvykdymo parinktis.
author: Henrikan
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f58f7923d82f3aa371ba916352211195870f9a75
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572630"
---
# <a name="delivery-alternatives"></a>Pristatymo alternatyvos

[!include [banner](../includes/banner.md)]

Pardavimo užsakymų priėmėjai gali naudoti puslapį **Pristatymo alternatyvos**, norėdami sužinoti alternatyvias užsakymo įvykdymo parinktis.

Puslapio maketas **Pristatymo alternatyvos** suteikia visų alternatyvių parinkčių apžvalgą. Tai taip užsakymų priėmėjams jis suteikia galimybę įvykdymo galimybių už dabartinės įmonės ribų. Dabar jie gali peržiūrėti tiek vidinės įmonės galimybes, tiek išorinių tiekėjų galimybes. Rūšiuodami parinktis pagal pristatymo datą, pardavimo užsakymų priėmėjai gali peržiūrėti išmanų pristatymo alternatyvų sąrašą. Be to, parametrai jiems suteikia galimybę geriau valdyti siūlomas pristatymo parinktis. Kadangi transportavimo laikas gali paveikti pristatymo datas, pardavimo užsakymų priėmėjai gali palyginti įvairias vežėjų siūlomas transportavimo galimybes. Kadangi rodoma išsami kiekvieno pasiūlymo informacija, užsakymų priėmėjai gali priimti kompetentingus sprendimus tiesiogiai iš **Pristatymo alternatyvos**.

## <a name="open-the-delivery-alternatives-page"></a>Puslapio Pristatymo alternatyvos atidarymas

Puslapį **Pristatymo alternatyvos** galite atidaryti iš pardavimo užsakymo eilutės.

1. Pasirinkite **Produktai ir tiekimas \> Pristatymo alternatyvos**.
1. Pasirinkite **Eilutės informacija \> Pristatymas \> Pristatymo alternatyvos.**

Taip pat galite atidaryti **Pristatymo alternatyvos** puslapį atidarydami darbo sritį **Pardavimo užsakymo apdorojimas ir užklausa** ir tada pasirinkę **Užsakymai ir parankiniai \> Atidėto užsakymo eilutės \> Pristatymo alternatyvos** **Pastaba:** Puslapį **Pristatymo alternatyvos** galite atidaryti tik jei tenkinamos abi tolesnės sąlygos:

- Užpildyta visa privaloma pardavimo eilutės informacija.
- Nustatyta lauko **Pristatymo datos valdymas** reikšmė nėra **Nėra**.

## <a name="delivery-date-control-methods"></a>Pristatymo datos valdymo metodai

Pristatymo datos valdymo metodas nurodo tai, kaip sistema nustato pristatymo datas, kaip pristatymo alternatyvas galima apskaičiuoti ir kokia informacija rodoma. Atkreipkite dėmesį į tai, kad naudojant pristatymo datos valdymo funkciją atsižvelgiama į kalendorius. Todėl šie kalendoriai gali paveikti siūlomą gavimo datą: sandėlio kalendorius, transportavimo kalendorius, tiekėjo kalendorius ir kliento kalendorius. Toliau pateikiamoje lentelėje aprašomas kiekvienas pristatymo datos valdymo metodas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Metodas</strong></td>
<td><strong>Aprašas</strong></td>
</tr>
<tr class="even">
<td><strong>Nėra</strong></td>
<td><ul>
<li>Pardavimo eilučių pristatymo alternatyvos nėra palaikomos. Ši parinktis išjungia pristatymo datos valdiklį.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Pardavimo vykdymo laikas</strong></td>
<td><ul>
<li>Pristatymo alternatyvos apskaičiuojamos pagal iš anksto nustatytą pardavimo vykdymo laiką. Transportavimo dienos skaičiuojamos pagal pristatymo būdą.</li>
<li>Pristatymo alternatyvos apima sandėlius, kurie turi atsargų, ir tiekimo / poreikio užsakymus.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Pristatymo alternatyvos apskaičiuojamos pagal prieinamų atsargų (ATP) logika. Atsižvelgiama į esamą prieinamumą ir numatomą prieinamumą ateityje. Transportavimo dienos skaičiuojamos pagal pristatymo būdą.</li>
<li>Pristatymo alternatyvos apima sandėlius, kurie turi atsargų, ir tiekimo / poreikio užsakymus.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP ir išdavimo laiko rezervas</strong></td>
<td><ul>
<li>Pristatymo alternatyvos apskaičiuojamos taip, kaip taikant ATP metodą, bet į skaičiavimą įtraukiama išdavimo laiko rezervas.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Pristatymo alternatyvos apskaičiuojamos pagal galimų pateikti atsargų (CTP) logiką. MRP išskleidimas naudojamas prieinamumui nustatyti. Atminkite, kad CTP visada bent paslenka pristatymo datas į pardavimo vykdymo laiką. Transportavimo dienos skaičiuojamos pagal pristatymo būdą.</li>
<li>Pristatymo alternatyvos apima toliau nurodytų sandėlių pasiūlymus.
<ul>
<li>Dabartinis sandėlis</li>
<li>Numatytasis sandėlis</li>
<li>Visi sandėliai, kuriuose yra turimų atsargų</li>
<li>Visi sandėliai, kuriuose yra tiekimo užsakymų</li>
<li>Visi sandėliai, kuriuose yra aktyvių komplektavimo specifikacijos (KS) versijų</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Informacijos apie pristatymo alternatyvas peržiūra

Šiame skyriuje aprašoma informacija apie pristatymo alternatyvas, pateikiama kiekviename puslapio **Pristatymo alternatyvos** „FastTab”.

### <a name="the-product-fasttab"></a>Produkto „FastTab“

Šiame „FastTab” rodoma produkto suvestinė ir dabartinės pardavimo eilutės informacija.

### <a name="the-delivery-alternatives-fasttab"></a>Pristatymo alternatyvų „FasTab”

Šiame „FastTab” rodomas pristatymo alternatyvų, išrūšiuotų pagal gavimo datą, sąrašas. Virš sąrašo galite pasirinkti, kuriomis parinktimis turi būti pagrįsti pasiūlymai. Taip pat galite pasirinkti pristatymo būdą, kuris nustato transportavimo dienas. Galimos toliau nurodytos pasirinktys:

- **Įtraukti kitus produkto variantus** – šią pasirinktį galima naudoti, jei produktas turi produkto variantų. Bus įtrauktos kitų produkto variantų pristatymo alternatyvos. Šios parinkties negalima naudoti su CTP.
- **Įtraukti dalinį kiekį** – pagal numatytuosius parametrus įtraukiami tik pasiūlymai, kurie atitinka visą pardavimo eilutės kiekį. Pasirinkite šią pasirinktį, norėdami įtraukti pasiūlymus, kurie atitinka tik užsakymo eilutės kiekio dalį. Ši pasirinktis yra naudinga, kai klientas pageidauja ankstesnės pristatymo datos ir pristatymą sutinka priimti dalimis.
- **Įtraukti vėlesnes datas** – pagal numatytuosius parametrus rodomi tik pasiūlymai, kurie yra geresni (ankstesni) nei dabartinės pardavimo eilutės datos. Pasirinkite šią parinktį, norėdami įtraukti vėlesnes datas. Ši parinktis gali būti naudinga situacijose, kai prioritetas teikiamas ne datos parametrui. Pvz., konkretus tiekėjas arba sandėlis gali būti pageidaujamas.
- **Pristatymo būdas** – pasirinkite norimą pristatymo būdą, kad optimizuotumėte transportavimo laiką ir išlaidas. Iš karto pamatysite pasikeitusį siūlomų pristatymo alternatyvų rodinį. Todėl lengva palyginti alternatyvas.
- **Įtraukti įsigijimą** – pasirinkus įsigijimą, siūlomos pristatymo alternatyvos apima pasirinktis pirkti iš išorinių tiekėjų ir kitų įmonės įmonių (vidinių įmonių). Parinktis **Įtraukti įsigijimą** palaikoma naudojant pristatymo datos valdymo metodą ATP bei ATP ir išdavimo laiko rezervas. Įtraukiamos parinktys pirkti iš produkto numatytojo pirkimo tiekėjo ir produkto visų patvirtintų tiekėjų.
- Naudojant išorinius tiekėjus, skaičiavimas yra pagrįstas pirkimo vykdymo laiku.
- Naudojant vidinę įmonę, skaičiavimas pagrįstas išteklių tiekimo įmonės turimomis atsargomis, atsižvelgiant į išteklių tiekimo įmonės pristatymo datos valdymą.
- **Pristatymo tipas** (aktualu perkant)
  - **Atsargos** – produktai siunčiami iš išteklių tiekimo sandėlio į pardavimo eilutės teritoriją / sandėlį. Tada jie iš to sandėlio siunčiami klientui.
  - **Tiesioginis pristatymas** – produktai iš išteklių tiekimo sandėlio siunčiami tiesiogiai klientui.

### <a name="the-availability-information-fasttab"></a>Pasiekiamumo informacijos „FastTab”

Šio „FastTab” informacija yra susijusi su pasirinkta pristatymo alternatyvos eilute. Priklausomai nuo pardavimo eilutės pristatymo datos valdymo, rodoma tolesnė informacija.

- **Pardavimo vykdymo laikas**
  - **Turima šiandien** – rodomos faktinės turimos, faktiškai rezervuotos ir turimos faktinės atsargos.
  - **Parametrai** – rodomas atsargų vienetas ir pardavimo vykdymo laikas.

- **ATP bei ATP ir išdavimo laiko rezervas**
  - **Turima šiandien** – rodomos faktinės turimos, faktiškai rezervuotos ir turimos faktinės atsargos.
  - **Parametrai** – rodomas atsargų vienetas ir pardavimo vykdymo laikas.
  - **Prieinamumas ateityje** – rodomas teritorijos ir sandėlio, pasirinktų dalyje **Pristatymo alternatyvos**, dabartinio ir būsimo prieinamumo grafinis vaizdas. Galite pasirinkti diagramos stulpelius norėdami peržiūrėti išsamios informacijos apie būsimą produkto pasiekiamumą. Slankiklis rodo atitinkamų poreikio ir tiekimo užsakymų, patenkančių į ATP laiko ribą, sąrašą.

- **CTP**
  - **Turima šiandien** – rodomos faktinės turimos, faktiškai rezervuotos ir turimos faktinės atsargos.
  - **Parametrai** – rodomas atsargų vienetas ir pardavimo vykdymo laikas.
  - **Išskleidimas** – rodomas pasirinktos pristatymo alternatyvos tiekimo išskleidimas. Galite naudoti parinktį **Sąranka**, norėdami keisti išskleidime rodomus laukus ir atsargų dimensijas.

### <a name="the-impact-of-selected-alternative-fasttab"></a>Pasirinktos alternatyvos „FastTab” poveikis

Šis „FastTab” išryškina pasirinktos pristatymo alternatyvos poveikį. Jei pasirinksite **Gerai**, pardavimo eilutė atnaujinama paryškintomis reikšmėmis PASIRINKTUOSE stulpeliuose. Atminkite, jei pasirinktos pristatymo alternatyvos kiekis yra mažesnis nei pardavimo eilutės kiekis, sukuriamas pristatymo grafikas ir užsakymo eilutė išskaidoma į dvi eilutes: vieną eilutę, skirtą pasirinktam kiekiui, ir vieną eilutę, skirtą likusiam kiekiui. Taip pat galite atnaujinti prekybos eilutę, kad ji atitiktų grafiko eilutes ir turėtų įtakos kainai.

## <a name="additional-resources"></a>Papildomi ištekliai

[Užsakymų vykdymo perspektyva](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]