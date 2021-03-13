---
title: Formulės ir formulių versijos
description: Šioje temoje pateikiama informacijos apie formules ir formulių versijas. Formule apibrėžiamos konkretaus proceso gamybos proceso medžiagos, ingredientai ir rezultatai. Proceso gamyboje formulės naudojamos produktams planuoti ir gaminti.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e5ff5916366f968cbf8dc9a5614466ef89faa92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007168"
---
# <a name="formulas-and-formula-versions"></a>Formulės ir formulių versijos

[!include [banner](../includes/banner.md)]

Formule apibrėžiamos konkretaus proceso gamybos proceso medžiagos, ingredientai ir rezultatai. Su atitinkamu maršrutu formulė proceso gamyboje apibrėžia visą procesą. Proceso gamyboje formulės naudojamos produktams planuoti ir gaminti.

Formulę sudaro ingredientai ir kiekiai, kurių reikia norint pagaminti konkretų sudėtinės prekės kiekį. Atsižvelgiant į atliekamą užduotį, formulių funkcijas galite pasiekti dalyse Atsargų ir sandėlio valdymas arba Produktų informacijos valdymas.

## <a name="formulas-and-formula-lines"></a>Formulės ir formulių eilutės
Formulę sudaro viena arba kelios formulės eilutės, identifikuojančios formulę sudarančius ingredientus ar prekes. Formulės eilutėje gali būti komplektavimo specifikacijos (KS) prekių, sudėtinių prekių, esamo svorio prekių, įsigytų prekių, sudėtinių produktų arba šalutinių produktų. Kadangi daug prekių yra naudojamos keliuose produktuose, prekę galima naudoti daugiau nei vienoje formulėje.

Formulės pavyzdys yra sausainio su šokolado drožlėmis formulė. Šios formulės ingredientams naudojamos kelios eilutės, pvz., miltai, cukrus, kiaušiniai, sviestas ir šokolado drožlės. Sausainio su šokolado drožlėmis formulėje yra ingredientų, kurie greičiausiai naudojami ir kitose formulėse. Gaminant sausainius su šokolado drožlėmis, gali likti likučių, pvz., trupinių, arba kai kurie sausainiai gali būti per daug iškepę ar iškepti nepakankamai gerai. Atsižvelgiant į gamybos operacijas, šiuos elementus galima nustatyti kaip sudėtinius produktus arba šalutinius produktus.

Kurdami formulės eilutę, naudojate eilutės tipą, kad nurodytumėte, kaip sistema eilutę turi tvarkyti jums vykdant bendrąjį planavimą ir gaminant paketinius užsakymus. Kiekviena eilutė pateikia skirtingą rezultatą. Toliau pateikiamoje lentelėje aprašomi eilučių tipai, kuriuos galite pasirinkti. 

| Eilutės tipas     | aprašymas  |
|---------------|--------------|
| Produktas          | Pasirinkite **Prekė**, kai prekė yra žaliava arba pusiau pabaigta prekė, paimta iš atsargų, arba kai prekė yra paslauga. |
| Fiktyvus       | Pasirinkite **Fiktyvus**, norėdami išskleisti bet kurias žemesniojo lygio sudėtines prekes, esančias formulės eilutėse. Kai numatote paketinį užsakymą ir sudėtinės prekės yra išskleidžiamos, sudėtinės prekės surašomos kaip formulės eilutės paketiniame užsakyme. Be to, prie gamybos maršruto pridedami atitinkami maršrutai. Sudėtinės prekės išskleidžiamos naudojant dabartinę konfigūraciją. Naudodami eilutės tipą **Fiktyvus**, galite tvarkyti gamybos ir matavimo konfigūracijas, esančias skirtinguose formulės lygiuose. Jei puslapio **Išleisto produkto informacija** „FastTab“ skirtuke **Konfigūruoti** prie produkto pasirenkate **Fiktyvus** ir tada šį produktą naudojate formulėje, formulės eilutės tipas pakeičiamas į **Fiktyvus**. Tipo **Fiktyvus** negalima parinkti esamo svorio prekei arba prekėms, kurių gamybos tipas yra **Sudėtinis produktas**, **Šalutinis produktas** arba **Planavimo prekė**. |
| Iškviestas tiekimas | Pasirinkite **Iškviestas tiekimas**, kad sukurtumėte formulės eilutės ingrediento paketinį užsakymą, gamybos užsakymą, kanban, perkėlimo užsakymą arba pirkimo užsakymą. Susijęs užsakymas nustatomas pagal numatytuosius užsakymo parametrus bei ingrediento gamybos tipą ir sukuriamas jums numatant paketinį užsakymą. Reikiami ingredientų kiekiai rezervuojami paketiniam užsakymui. |
| Tiekėjas        | Pasirinkite **Tiekėjas**, jei gamybos procese dalyvauja subrangovas ir norite sukurti tarpinę gamybą arba pirkimo užsakymą subrangovui. Subrangovo atliekamą paslaugą ar darbą reikia sukurti naudojant sudėtinę prekę arba aptarnavimo prekę. Prekę galite pridėti prie pirminės prekės kaip formulės eilutę. Maršrute turi būti operacija, priskirta subrangovo operacijų ištekliui. Ši operacija prie formulės eilutės pridedama naudojant **Oper. nr.** nurodytas operacijos numeris. |

## <a name="formula-versions"></a>Formulės versijos
Kurdami naują formulę, pirmiausia turite sukurti formulės versiją, o tada įtraukti formulės eilučių prekių ir jų konkrečių charakteristikų. Kiekviena formulė turi turėti bent vieną versiją. Formulės versijoje mygtuką **Patvirtinta** galima naudoti tik sėkmingai įrašius versijos įrašą. Kiekvienas formulės versijos įrašas yra susietas su vienu ar keliais sudėtiniais produktais ir šalutiniais produktais, kuriuos galima gaminti gaminant baigtą produktą. Daugelį produktų galima gaminti iš tų pačių ingredientų ir skirtingais paketo dydžiais, pakartotinai arba naudojant skirtingas išeigas. Galite kurti tiek formulės versijų, kiek reikia.

Norėdami valdyti kelias aktyvias formulės versijas, naudokite įsigaliojimo datų intervalus arba kiekio laukus „nuo“. Kelios aktyvios formulės versijos gali egzistuoti, tik jei nepersidengia datų intervalas ir kiekis „nuo“.

Skirtingai nuo komplektavimo specifikacijų, kurių viena dažnai susiejama su daug KS versijų, paprastai egzistuoja tik viena formulės versija. Atminkite, kad galima suaktyvinti tik vieną konkretaus produkto padengimo dimensijų ir kiekio formulės versiją. Tačiau dėl kitų priežasčių gali egzistuoti daug formulės versijų ir, kurdami paketinį užsakymą, jas galite pasirinkti rankiniu būdu.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Formulių bei formulių versijų tvirtinimas ir aktyvinimas
Kad formules ir formulių versijas būtų galima naudoti vykdant planavimą ir gamybą, jas reikia patvirtinti. Formulės paprastai suaktyvinamos prieš jas naudojant. Tačiau, vykdydami gamybą, galite pasirinkti patvirtintą, tačiau nesuaktyvintą formulę.

Norėdami padėti apsaugoti formulę ar formulės versiją, puslapyje **Gamybos valdymo parametrai** galite nustatyti parametrus **Blokuoti redagavimą** ir **Blokuoti patvirtinimo pašalinimą**.

Jei pasirenkate **Blokuoti redagavimą** ir formulė yra patvirtinta, negalima panaikinti ar redaguoti jokių formulės eilučių laukų. Tačiau, jei pašalinate formulės patvirtinimą, formulės eilutes galite panaikinti ir modifikuoti. Taip pat galite kurti naujas formules ir naujas formulių versijas.

Jei pasirenkate **Blokuoti patvirtinimo pašalinimą**, negalite pašalinti patvirtintos formulės ar formulės versijos patvirtinimo. Tačiau galite kurti naujas formules bei naujas formulių versijas ir galite pašalinti formulės versijos suaktyvinimą.

Naudodami elektroninio parašo funkcijas galite įtraukti daugiau valdymo lygių. Kai nustatyta, kad, vartotojui tvirtinant formulę, reikia naudoti elektroninį parašą, suaktyvinus formulę rodomas puslapis **Parašas**. Vartotojas turi būti įgaliotas pasirašyti elektroniniu būdu ir, kad būtų galima atlikti keitimą, sertifikatas turi būti sėkmingai patikrintas. Jei parašo autentifikuoti nepavyksta, patvirtinimo tvirtinimas ar šalinimas atmetamas, o patvirtinimo tvirtinimą ar šalinimą inicijavęs keitimas grąžinamas į pradinę būseną.

## <a name="use-the-scalable-feature"></a>Funkcijos Keičiama naudojimas
Funkciją Keičiama galima naudoti, tik jei visi formulės elementų komponentai nustatyti kaip **Kintamas suvartojimas**. Jei elementų komponentai nustatyti kaip **Fiksuotas vartojimas** arba **Pakopinis vartojimas**, funkcijos naudoti negalima. Kai naudojama funkcija Keičiama, pakeitus formulės ingredientą, pakoreguojamas kitų jūsų pasirinktų ingredientų kiekis. Koreguojamas ir formulės dydis. Taip pat, pakeitus formulės dydį, pakeičiamas visų keičiamo dydžio ingredientų kiekis. Ši funkcija konkrečiai skirta formulėms kurti ir prižiūrėti. Ji nenurodo, ar ingrediento kiekis paketiniame užsakyme bus padidintas, ar sumažintas.

## <a name="use-step-consumption"></a>Funkcijos Pakopinis vartojimas naudojimas
Naudojant funkciją Pakopinis vartojimas, ingrediento skirtuke **Formulės eilutė** nebereikia įvesti kiekio. Todėl funkcija Pakopinis vartojimas sukonfigūruota taip, kad joje būtų reikšmės **Iš serijos** ir **Kiekis**. Pasirenkama informacija iš įrašo Pakopinis serijos vartojimas, atitinkanti paketinio užsakymo kiekį. Funkcija Pakopinis vartojimas naudinga, kai suvartojimo rodiklis paketinio užsakymo dydžio atžvilgiu nėra linijinis ir, pasiekus konkrečią kiekio ribą, tik padidina poreikį. Norėdami šią funkciją įjungti naujai formulei, grupėje **Suvartojimo skaičiavimas** taikytino ingrediento formulės parametrą iš **Standartinis** pakeiskite į **Pakopinis**. Šis suvartojimo metodas nurodomas puslapio **Formulės eilutė** skirtuke **Sąranka**.
