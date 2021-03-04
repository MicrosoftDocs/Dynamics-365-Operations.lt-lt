---
title: Didžiųjų knygų konfigūravimas
description: Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti kiekvieno juridinio subjekto didžiąsias knygas. Joje pateikiama informacijos apie tai, kaip pasirinkti valiutas, finansinius kalendorius, sąskaitų planą ir sąskaitų struktūras, kurios turėtų būti naudojamos su kiekvienu juridiniu subjektu.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 929ab7ae66a217de836ce49373faed76325c4d3a
ms.sourcegitcommit: ac0a676c91e3053ad7f9432d576c9af3ff98a99a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4446210"
---
# <a name="configure-ledgers"></a>Didžiųjų knygų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti kiekvieno juridinio subjekto didžiąsias knygas. Joje pateikiama informacijos apie tai, kaip pasirinkti valiutas, finansinius kalendorius, sąskaitų planą ir sąskaitų struktūras, kurios turėtų būti naudojamos su kiekvienu juridiniu subjektu.

## <a name="selecting-the-chart-of-accounts"></a>Sąskaitų plano pasirinkimas

Reikia sukonfigūruoti kiekvieno „Microsoft Dynamics 365 Finance“ juridinio subjekto didžiosios knygos informaciją. Puslapyje **Didžioji knyga** galite pasirinkti sąskaitų planą ir sąskaitų struktūras, kurios bus naudojamos su pasirinktu juridiniu subjektu. Sąskaitų planą ir sąskaitų struktūras galite bendrinti sukonfigūruodami kiekvieno juridinio subjekto puslapį **Didžioji knyga**, kad būtų galima naudoti tą patį sąskaitų planą ir sąskaitų struktūras. Taip pat galite bendrinti kiekvieno juridinio subjekto konfigūracijos dalį ir turėti konkrečias konfigūracijas kiekviename juridiniame subjekte.

Jeigu jūsų juridiniai subjektai turi turėti skirtingus sąskaitų planus arba skirtingas sąskaitų struktūras, gali būti naudinga juridinio subjekto keitimo funkcija. Naudojant tą patį sąskaitų planą ir sąskaitų struktūras keliems juridiniams subjektams, o tada tvarkant išimtis keičiant juridinius subjektus, galima supaprastinti priežiūrą per tam tikrą laiką.

Norėdami sukonfigūruoti juridinio subjekto sąskaitų planą, eikite į **Didžioji knyga \> Didžiosios knygos sąranka \> Didžioji knyga**. Puslapyje **Didžioji knyga** pasirinkite **Sąskaitų planas**, tada sąraše pasirinkite naudotiną sąskaitų planą. Atkreipkite dėmesį, kad sąskaitų plano negalima pakeisti pasirinkus reikšmę ir registruojant operacijas juridiniame subjekte.

Norėdami gauti daugiau informacijos apie tai, kaip planuoti ir konfigūruoti sąskaitų planą ir pagrindines sąskaitas, žr. [Sąskaitų plano planavimas](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Sąskaitų struktūrų pasirinkimas

Kiekvienas „Dynamics 365 Finance“ juridinis subjektas gali būti sukonfigūruotas naudoti vieną ar daugiau sąskaitų struktūrų. Kiekviena sąskaitų struktūra apibrėžia finansines dimensijas ir pagrindinių sąskaitų bei finansinių dimensijų derinius, kurie bus leidžiami registruojant operacijas. Tas pačias sąskaitų struktūras galite naudoti daugiau nei viename juridiniame subjekte.

Atkreipkite dėmesį, kad, jei turite kelias sąskaitų struktūras, galite pasirinkti tik tas sąskaitų struktūras, kuriose nėra persidengiančių pagrindinių sąskaitų ir finansinių dimensijų derinių. Pavyzdžiui, viena iš jūsų sąskaitų struktūrų sukonfigūruota įtraukti verslo struktūros vienetą į pagrindines sąskaitas tarp 1000 ir 1999. Kitoje sąskaitų struktūroje į pagrindines sąskaitas, prasidedančias 1, įtraukėte finansinę dimensiją Padalinys. Šiuo atveju tame pačiame juridiniame subjekte galima įtraukti tik vieną iš sąskaitų struktūrų.

Norėdami sukonfigūruoti savo DK sąskaitų struktūras, puslapio **Didžioji knyga**, „FastTab“ **Sąskaitų struktūros** pasirinkite **Įtraukti**, sąraše pasirinkite sąskaitų struktūrą, tada – **Pasirinkti**. Gali užtrukti keletą minučių, kol bus įtrauktos ir įrašytos sąskaitų struktūros. Atkreipkite dėmesį, kad jūsų pasirinktos sąskaitų struktūros turi būti aktyvios. Kitu atveju informacija apie sąskaitų struktūras negalios juridiniuose subjektuose, kuriuose jos yra susietos.

Norėdami pašalinti sąskaitos struktūrą, puslapio **Didžioji knyga** „FastTab“ **Sąskaitų struktūros** pasirinkite **Pašalinti**. Atkreipkite dėmesį, kad, iš savo DK pašalinę sąskaitų struktūrą, nepašalinate jokių operacijų, kurios buvo užregistruotos naudojant tos sąskaitų struktūros konfigūraciją.

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti savo sąskaitų struktūras, žr. [Sąskaitų struktūrų konfigūravimas](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Didžiosios knygos kalendorių konfigūravimas

Dar vienas DK komponentas yra finansinis kalendorius. Turite pasirinkti kiekvieno juridinio subjekto finansinį kalendorių. Tą patį finansinį kalendorių galite naudoti daugiau nei viename juridiniame subjekte. Kai pasirenkate DK finansinį kalendorių, sukuriama kopija. Ši kopija vadinama DK kalendoriumi. DK kalendorius leidžia pasirinkti laikotarpių būseną ir kiekvieno laikotarpio modulius.

Norėdami pasiekti ir atnaujinti pasirinkto juridinio subjekto kalendorių, puslapio **Didžioji knyga** veiksmų srityje pasirinkite **Didžiosios knygos kalendorius**.

Norėdami pasirinkti kalendorių, pasirinkite **Finansiniai kalendoriai** ir sąraše pasirinkite kalendorių. Jei keičiate finansinį kalendorių po to, kai operacijos užregistruotos juridiniame subjekte, turite pasirinkti **Perskaičiuoti didžiosios knygos laikotarpius**. Tada pasirodžiusiame dialogo lange galite atnaujinti savo kalendoriaus laikotarpių DK balansus. Rekomenduojame procesą **Perskaičiuoti didžiosios knygos laikotarpius** paleisti naudojant režimą **Paketinis** ir jį vykdyti, kai sistemoje vyksta neesminiai procesai. Atsižvelgiant į operacijų skaičių ir finansinių dimensijų derinius, šis procesas gali šiek tiek užtrukti.

Jei juridinio subjekto finansinio kalendoriaus nepasirinkta, bandant užregistruoti operaciją šiame juridiniame subjekte bus parodytas klaidos pranešimas.

Daugiau informacijos rasite [Ataskaitiniai kalendoriai, ataskaitiniai metai ir laikotarpiai](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Balansavimo finansinės dimensijos naudojimas

Pasirinkę sąskaitų planą ir įtraukę vieną ar daugiau sąskaitų struktūrų, galite pasirinkti vieną finansinę dimensiją, kuri bus naudojama kaip balansavimo finansinė dimensija. Dimensija, kurią pasirinkote, turi būti visose sąskaitų struktūrose. Ji taip pat turi būti subalansuota visuose apskaitos įrašuose. Kitaip tariant, debetai ir kreditai turi sutapti pagrindinėje sąskaitoje ir balansavimo finansinėje dimensijoje. Sistema automatiškai sukuria operacijas, skirtas įrašams subalansuoti, pagal pagrindines sąskaitas, kurios yra nurodytos puslapio **Automatinės operacijos sąskaitos** laukuose **Susiję vienetai – kreditas** ir **Susiję vienetai – debetas**.

Norėdami gauti daugiau informacijos apie balansavimo įrašus, žr. [Subalansuoti žurnalai susijusių vienetų apskaitai](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Didžiosios knygos valiutų konfigūravimas

Puslapis **Didžioji knyga** taip pat naudojamas valiutoms, kurios bus naudojamos registruojant operacijas didžiojoje knygoje, valdyti ir nurodyti. Turite nurodyti apskaitos valiutą, kuri yra valiuta, naudojama DK visų kvitų stulpelyje **Apskaitos valiuta**. Be to, stulpelyje **Ataskaitų valiuta** galite pasirinkti antrą valiutą. Jei pasirinksite ataskaitų valiutą, visos operacijos visų kvitų DK stulpelyje **Ataskaitų valiuta** bus įrašomos ta valiuta.

Jei operacijos užregistruojamos kita valiuta, sistema automatiškai konvertuoja operacijos sumą iš operacijų valiutos į kvito apskaitos valiutą ir ataskaitų valiutą. Puslapio **Didžioji knyga** lauke **Apskaitos valiutos kurso tipas** pasirinkite valiutos kurso tipą, sukonfigūruotą valiutos kursams, kurie turi būti naudojami norint konvertuoti reikšmes iš operacijų valiutos į apskaitos valiutą kvite. Jei pasirinkote ataskaitų valiutą, taip pat turite nustatyti lauką **Ataskaitų valiutos kurso tipas**, kad nurodytumėte valiutos kursą, kuris turi būti naudojamas konvertuojant reikšmes iš operacijų valiutos į apskaitos valiutą kvite.

Jei naudojate biudžeto sudarymo funkciją, taip pat galite nustatyti lauką **Biudžeto valiutos kurso tipas**, kad nurodytumėte valiutos kursą, kuris turi būti naudojamas konvertuojant biudžeto operacijas iš vienos valiutos į kitą.

Jei naudojate dvi valiutas arba naudojate vieną valiutą, bet operacijos užregistruojamos kita valiuta, turite sukonfigūruoti puslapio **Didžioji knyga** „FastTab“ **Sąskaitos valiutos kursui pakeisti**. Šiame „FastTab“ nurodote numatytąsias gauto ir negauno pelno bei nuostolio sąskaitas, kurios bus naudojamos pagal numatytuosius parametrus, kai bus registruojamos operacijos, jei puslapyje **Valiutos kurso pasikeitimo sąskaitos** nenurodyta jokia sąskaita. (Puslapis **Valiutos kurso pasikeitimo sąskaitos** naudojamas norint konfigūruoti skirtingas gauto ir negauto pelno bei nuostolio sąskaitas kiekviena valiuta.)

Gautas pelnas ir nuostoliai yra pelnas ir nuostoliai, kurie gaunami / patiriami baigus operacijų. Jie įrašomi pelno ir nuostolio išraše. Negautas pelnas ir nuostoliai yra pelnas ir nuostoliai, kurie materializuoti, bet operacija nebaigta. Kitaip tariant, pvz., užregistravote SF, bet ji dar nesudengta ir nesumokėta. Negautas pelnas ir nuostoliai įrašomi balanse.

Daugiau informacijos apie dviejų valiutų naudojimą rasite temoje [Dvi valiutos](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]