---
title: USMCA kilmės sertifikatas
description: Ši funkcija leidžia jums spausdinti kilmės dokumentų sertifikatą, kurio reikia pagal JAV-Meksikos-Kanados sutartį (USMCA).
author: Henrikan
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: e479c7686ab9445b012d335ddc9fc4cdc6b2275c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807709"
---
# <a name="usmca-certification-of-origin"></a>USMCA kilmės sertifikatas

[!include [banner](../includes/banner.md)]

Ši funkcija leidžia jums spausdinti kilmės dokumentų sertifikatą, kurio reikia pagal JAV-Meksikos-Kanados sutartį (USMCA).

*USMCA dokumento kilmės sertifikate* yra mažiausių duomenų elementai, kurių reikia deklaracijai. Kai kurie duomenų elementai gali būti filtruoti iš anksto spausdinant, kai kiti turi būti užpildyti rankiniu būdu po spausdinimo. Norėdami gauti pirmenybinį tarifo tvarkymą, dokumentas turi būti užpildytas ir jį turėti importuotas deklaracijos padarymo metu. Dokumentą gali užbaigti importuotojas, eksportuotojas ar gamintojas.

Galite spausdinti dokumentą vienam siuntimui iš **Visų siuntimų** sąrašo puslapio arba iš **Siuntimo išsamios informacijos** puslapio.

Prie dokumento galima prieiti tik, kai šalis pirminiame adrese juridiniame asmenyje yra JAV.

Priklausomai nuo dokumento spausdinimo pasirinkimo, dokumentą galima iš anksto užpildyti jūsų sistemos duomenimis. Galima keisti ar įtraukti duomenis į spausdintą dokumentą eksportuojant spausdintą dokumentą redaguojamu formatu, tokiu kaip „Microsoft Word“. Po eksportavimo, galite taikyti visus būtinus pakeitimus prieš deklaraciją.

## <a name="turn-on-the-usmca-feature"></a>Įjunkite USMCA funkciją

Prieš jums naudojant USMCA funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Gabenimo valdymas*
- **Funkcijos pavadinimas:** *USMCA kilmės sertifikato dokumentas*

## <a name="document-content"></a>Dokumento turinys

USMCA dokumento kilmės sertifikate yra mažiausių tolesnių duomenų elementai:

- Adreso elementai
- Sertifikuojančios šalies vaidmuo
- Vienas siuntimas
- Sąskaitos faktūros
- Bendras laikotarpis
- Prekės duomenys
- Parašo sertifikuotojas
- Puslapių skaičius

Daugiau informacijos apie kiekvieną iš šių elementų ir jų verčių rasite tolesniuose šios temos skyriuose.

## <a name="print-a-usmca-certification-of-origin-document"></a>Spausdinkite USMCA kilmės sertifikato dokumentą

Norėdami atspausdinti USMCA dokumento kilmės sertifikatą siuntimui, darykite taip:

1. Atlikite vieną iš toliau nurodytų veiksmų.
    - Eikite į **Gabenimo valdymas > Siuntimai > Visi siuntimai** ir pasirinkite siuntimą, kuriam norite spausdinti dokumentą.
    - Atverkite **Siuntimo išsami informacija** puslapį siuntimui, kuriam norite spausdinti dokumentą (yra keli būdai ten patekti, įskaitant **Visi siuntimai** puslapį).
1. Veiksmų juostoje atverkite **Siuntimų** skirtuką esantį grupėje **Spausdinti** ir rinkitės **USMCA kilmės sertifikatas**.
1. Teksto laukelis **Kilmės sertifikatas** atidaromas. Nustatykite kaip aprašyta tolesniuose poskyriuose ir tada rinkitės **Gerai**, kad sukurtumėte dokumentą.
1. Dokumento peržiūra atsidaro. Naudokite komandas veiksmų juostoje, kad spausdintumėte ar eksportuotumėte dokumentą, kaip būtina.

### <a name="certifying-party"></a>Tvirtinanti šalis

Naudokite **Sertifikuojanti šalis** iškrentantį meniu, kad identifikuotumėte šalį, kuri spausdina dokumentą. Nurodykite, ar sertifikuojanti šalis *Eksportuotojas*, *Eksportuotojas ar gamintojas*, *gamintojas* ar *Importuotojas*; arba palikite tuščią, jei sertifikuojanti šalis yra kita. Jūsų pasirinkta parinktis nustato, kas yra spausdinama dokumento adreso skyriuose.

**Sertifikuojanti šalis**, kurią pasirinkote bus įtraukta į spausdinamą dokumentą.

Dokumentą galima spausdinti tiek įvesties, tiek išvesties siuntimuose. Rinkitės *Importuotoją* kaip **Sertifikuojanti šalis** įvesties siuntimams.

Tolesnėje lentelėje aprašyti informacijos tipai, kurie yra įtraukti į dokumentą pagal jūsų pasirinktą **Sertifikuojančią šalį**.

| Sertifikuojanti&nbsp;šalis | aprašymas |
|---|---|
| *\[Tuščias\]* | Įtraukite tolesnę išsamią informaciją į dokumentą:<ul><li>**Sertifikuotojo išsami informacija**: Naudoja adreso informaciją siuntimo sandėliui, jei prieinama; kitu būdu, naudoja siuntimo saito adresą, jei prieinamas; kitu atveju, naudoja juridinio asmens adresą (įmonės) pasirinktą „Supply Chain Management“.</li><li>**Eksportuotojo išsami informacija**: Tuščia</li><li>**Gamintojo išsami informacija**: Tuščia</li><li>**Importuotojo išsami informacija**: Tuščia</li><ul>|
| *Eksportuotojas* | Įtraukite tolesnę išsamią informaciją į dokumentą:<ul><li>**Sertifikuotojo išsami informacija**: Naudoja adreso informaciją siuntimo sandėliui, jei prieinama; kitu būdu, naudoja siuntimo saito adresą, jei prieinamas; kitu atveju, naudoja juridinio asmens adresą (įmonės) pasirinktą „Supply Chain Management“.</li><li>**Eksportuotojo išsami informacija**: Naudoja adreso informaciją juridiniam asmeniui.</li><li>**Gamintojo išsami informacija**: Tuščia</li><li>**Importuotojo išsami informacija**: Naudoja sąskaitą susijusiam prekybos užsakymui.</li><ul>|
| *Eksportuotojas ir gamintojas* | Įtraukite tolesnę išsamią informaciją į dokumentą:<ul><li>**Sertifikuotojo išsami informacija**: Naudoja adreso informaciją siuntimo sandėliui, jei prieinama; kitu būdu, naudoja siuntimo saito adresą, jei prieinamas; kitu atveju, naudoja juridinio asmens adresą (įmonės) pasirinktą „Supply Chain Management“.</li><li>**Eksportuotojo išsami informacija**: Naudoja adreso informaciją juridiniam asmeniui.</li><li>**Gamintojo išsami informacija**: Naudoja adreso informaciją juridiniam asmeniui.</li><li>**Importuotojo išsami informacija**: Naudoja sąskaitą susijusiam prekybos užsakymui.</li><ul>|
| *Importuotojas* | Įtraukite tolesnę išsamią informaciją į dokumentą:<ul><li>**Sertifikuotojo išsami informacija**: Naudoja adreso informaciją siuntimo sandėliui, jei prieinama; kitu būdu, naudoja siuntimo saito adresą, jei prieinamas; kitu atveju, naudoja juridinio asmens adresą (įmonės) pasirinktą „Supply Chain Management“.</li><li>**Eksportuotojo išsami informacija**: Tuščia</li><li>**Gamintojo išsami informacija**: Tuščia</li><li>**Importuotojo išsami informacija**: Naudoja adreso informaciją juridiniam asmeniui.</li><ul>|
| *Gamintojas* | Įtraukite tolesnę išsamią informaciją į dokumentą:<ul><li>**Sertifikuotojo išsami informacija**: Naudoja adreso informaciją siuntimo sandėliui, jei prieinama; kitu būdu, naudoja siuntimo saito adresą, jei prieinamas; kitu atveju, naudoja juridinio asmens adresą (įmonės) pasirinktą „Supply Chain Management“.</li><li>**Eksportuotojo išsami informacija**: Tuščia</li><li>**Gamintojo išsami informacija**: Naudoja adreso informaciją juridiniam asmeniui.</li><li>**Importuotojo išsami informacija**: Tuščia</li><ul>|

### <a name="has-various-producers"></a>Yra įvairių gamintojų

**Sertifikuojanti šalis** iškrentantis sąrašas valdo tekstą naudojamą gamintojo išsamioje informacijoje dokumente. Pasirinkite vieną iš šių parinkčių:

- *Įvairūs gamintojai* - Spausdina tekstą „Įvairūs“ gamintojo išsamioje informacijoje.
- *Prieinamas pagal užklausą* - Spausdina tekstą „Prieinama pagal importuojančių įstaigų užklausą“ gamintojo išsamioje informacijoje.

Kai **Sertifikuojanti šalis** nustatyta į *Eksportuotojo ir gamintojo* ar *Gamintojo* laukelius kai **Turi įvairius gamintojus** nustatymai viršijami ir gamintojo adreso išsami informacija bus tokia pati kaip sertifikuotojo.

### <a name="blanket-period"></a>Bendras laikotarpis

Naudokite **Bendro laikotarpio formą** ir **Bendras laikotarpis į** nustatymus, kad sukurtumėte bendrą laikotarpį, per kurį dokumentas apims keletą identiškų prekių siuntimų, net jei dokumentas spausdinamas vienam siuntimui. Galite nustatyti bendro laikotarpio datas be jokių apribojimų ir jos bus įtrauktos į dokumentą. Taip pat galite palikti šiuos nustatymus tuščius ar nustatyti juos anksčiau.

### <a name="is-single-shipment"></a>Vieno siuntimo metu

Teksto laukelyje **Kilmės sertifikatas** nustatykite **Vienas siuntimas** tokią vertę:

- *Taip* - Įtraukite „Vienas siuntimas Taip“ šalia sąskaitos numerio.
- *Ne* - Nieko neįtraukia.

## <a name="other-information-included-in-the-document"></a>Kita informacija įtraukta į dokumentą

Kartu su pasirinktinais elementais, kuriuos pasirenkate naudodami **Sertifikatą ar kilmę** teksto laukelį, USMCA kilmės sertifikato dokumentas apims informaciją ir tinkintus laukelius apibendrintus tolesniuose poskyriuose. Šios informacijos dalis turi būti įvedama rankiniu būdu jums sukūrus dokumentą.

### <a name="invoice-number"></a>SF numeris

Prekybos sąskaitų ID susiję su siuntimais yra spausdinami dokumente nepriklausomai nuo bendro laikotarpio. Sąskaitos numeriai spausdinami nepriklausomai nuo **Vienas siuntimas** pasirinkimo.

### <a name="item-details"></a>Prekės duomenys

Dokumente pateikti keli skyriai, kuriuose nurodyta informacija apie prekę, kuri yra:

- **SKU numeris**: Spausdina išleisto produkto prekės numerį.

- **Aprašas**: Spausdina aprašą ar išleisto produkto vardą. Jei aprašas vartotojo kalba egzistuoja, jis ir spausdinamas. Jei nėra tokio aprašo, tuomet pavadinimas spausdinamas vartotojo kalba. Jei tokio vardo nėra, prekės vardas spausdinamas.

- **Harmonizuota sistema (HS) tarifo klasifikavimas**: Spausdina „Harmonized Tariff Schedule“ susietą su produktu. Galite nustatyti šiuos grafikus patekę į **Gabenimo valdymas \> Nustatymai \> Standartinis gabenimas \> Harmonized Tariff Schedules**.

- **Kilmės kriterijai:** Turite rankiniu būdu įvesti duomenis į šį skyrių pirmą kartą išleisdami dokumentą.

- **Kilmės šalis:** Spausdina kilmės šalį, kuriai taikote patekę į **Produkto informacijos valdymas \> Nustatymai \> Produkto atitiktis \> Kilmės šalis** (taip pat žr.[Kilmės šalis](../pim/country-of-origin.md)). ISO šalies kilmės kodas yra spausdinamas priklausomai nuo paskirties šalies ar regiono siuntimo pristatymo adrese ir ant prekės. Jei nėra jokių kilmės šalies duomenų nustatytų, tuomet ši vertė grįžta atgal į nustatymus rastus **Išleistas produktas \> Užsienio prekyba \> Kilmė**. Jei vis dar nerandami jokie kilmės duomenys, tuomet turite rankiniu būtu įvesti kilmės šalį sukūrę dokumentą.

### <a name="certifier-signature-and-date"></a>Parašo sertifikuotojas ir data

Privalote įvesti rankiniu būdu sukūrę dokumentą.

### <a name="consists-of-number-of-pages"></a>Jį sudaro puslapių skaičius

Vartotojas pasirašydamas sertifikatą turi rankiniu būvu įvesti puslapių skaičių (patvirtinimui) sukūręs dokumentą.

### <a name="page-numbers"></a>Puslapių numeriai

Esamas puslapis ir puslapių skaičius spausdinamas dokumento apačioje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]