---
title: Transportavimo valdymo mechanizmai
description: Transportavimo valdymo mechanizmai apibrėžia logiką, naudojamą generuojant ir apdorojant transportavimo tarifus modulyje Transportavimo valdymas.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a49ed7a91ec9a1b89564d40bef38cc4ea45532
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669606"
---
# <a name="transportation-management-engines"></a>Transportavimo valdymo mechanizmai

[!include [banner](../includes/banner.md)]

Transportavimo valdymo mechanizmai apibrėžia logiką, naudojamą generuojant ir apdorojant transportavimo tarifus modulyje Transportavimo valdymas. 

Transportavimo valdymo mechanizmas apskaičiuoja užduotis, pvz., vežėjo transportavimo tarifą. Mechanizmo sistema leidžia keisti skaičiavimo strategijas apdorojimo metu, atsižvelgiant į Tiekimo grandinės valdyme esančius duomenis. Transportavimo valdymo mechanizmas panašus į priedą, susijusį su tam tikra vežėjo sutartimi.

## <a name="what-engines-are-available"></a>Kokie yra galimi mechanizmai?
Toliau pateiktoje lentelėje parodyti galimi transportavimo valdymo mechanizmai.

| Transportavimo valdymo mechanizmas | Aprašymas                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tarifo nustatymo mechanizmas**                  | Apskaičiuojami tarifai.                                                                                                                                                                                                                                                                                                           |
| **Bendrasis mechanizmas**               | Paprasti pagalbiniai mechanizmai, naudojami kitų mechanizmų ir nereikalaujantys duomenų iš Tiekimo grandinės valdymo, pavyzdžiui, paskirstymo mechanizmas. Paskirstymo mechanizmai naudojami siekiant sumažinti galutines transportavimo išlaidas iki konkrečių užsakymų ir eilučių, atsižvelgiant į dimensijas, pvz., tūrį ir svorį. |
| **Kilometražo mechanizmas**               | Apskaičiuojamas transportavimo atstumas.                                                                                                                                                                                                                                                                                     |
| **Tranzito laiko mechanizmas**          | Apskaičiuojamas laikas, kurio reikia nukeliauti nuo pradinės iki galutinės paskirties vietos.                                                                                                                                                                                                                                       |
| **Zonos mechanizmas**                  | Apskaičiuojama zona pagal dabartinį adresą ir skaičius zonų, kurias reikia kirsti norint nukeliauti nuo adreso A iki adreso B.                                                                                                                                                                    |
| **Transportavimo sąskaitos tipas**            | Standartizuojama transportavimo sąskaita faktūra bei transportavimo sąskaitos eilutės ir yra naudojamas automatiniam transportavimo sąskaitos gretinimui atlikti.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Kokie mechanizmai turi būti sukonfigūruoti norint vertinti siuntą?

Norėdami vertinti siuntą naudodami konkretų vežėją, turite sukonfigūruoti kelis transportavimo valdymo mechanizmus. **Tarifo nustatymo mechanizmas** yra būtinas, bet gali reikėti ir kitų transportavimo valdymo mechanizmų, kad būtų palaikomas **Tarifo nustatymo mechanizmas**. Pavyzdžiui, **Tarifo nustatymo mechanizmas** galima naudoti duomenims iš **Kilometražo mechanizmas** nuskaityti norint apskaičiuoti tarifą pagal kilometražą tarp šaltinio ir paskirties vietos.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Ko reikia norint inicijuoti transportavimo valdymo mechanizmą?
Norėdami naudoti transportavimo valdymo mechanizmą, turite nustatyti inicijavimo duomenis, kad mechanizmas veiktų konkrečiu būdu. Nustatymas gali apimti toliau nurodytus duomenų tipus.
-   Nuorodos į kitus transportavimo valdymo mechanizmus. Išsamią informaciją žr. šiame skyriuje pateiktame konfigūracijos pavyzdyje.
-   Nuorodos į .NET tipus, kuriuos naudoja transportavimo valdymo mechanizmas.
-   Paprasti konfigūracijos duomenys.

Daugeliu atvejų inicijavimo duomenis galite konfigūruoti spustelėdami transportavimo valdymo mechanizmo nustatymo formose esantį mygtuką **Parametrai**. **Kilometražo mechanizmą nurodančio tarifų mechanizmo konfigūracijos pavyzdys** Toliau pateiktame pavyzdyje parodytas būtinas tarifų mechanizmo, pagrįsto .NET mechanizmo tipu Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine ir nurodančio kilometražo mechanizmą, nustatymas.

|          Parametras           |                                                                                  Aprašymas                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET tipas, interpretuojantis tam tikros schemos tarifo pagrindo priskyrimo duomenis. Parametro reikšmės sintaksę sudaro du segmentai, atskirti vertikaliu brūkšniu ( |
|  <em>MileageEngineCode</em>  |                       Kilometražo mechanizmo kodas, identifikuojantis kilometražo mechanizmo įrašą duomenų bazėje.                        |
| <em>ApportionmentEngine</em> |                        Išlaidų mechanizmo kodas, identifikuojantis paskirstymo mechanizmą duomenų bazėje.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Kaip transportavimo valdymo mechanizmuose naudojami metaduomenys?

Transportavimo valdymo mechanizmai, priklausantys nuo Tiekimo grandinės valdyme apibrėžtų duomenų, gali naudoti skirtingas duomenų schemas. Transportavimo valdymo sistema leidžia įvairiems transportavimo valdymo mechanizmams naudoti tas pačias bendrąsias fizinės duomenų bazės lenteles. Norėdami įsitikinti, kad mechanizmo duomenų apdorojimo laiko interpretavimas yra teisingas, galite apibrėžti duomenų bazės lentelių metaduomenis. Tai sumažina naujų transportavimo valdymo mechanizmų kūrimo išlaidas, nes papildomos lentelių ir formų struktūros programoje „Operations“ nėra privalomos.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Ką galima naudoti kaip ieškos duomenis tarifų skaičiavimuose?
Duomenis, kuriuos naudojate skaičiuodami tarifus, valdo metaduomenų konfigūracija. Pavyzdžiui, jei norite ieškoti tarifų pagal pašto indeksus, turite nustatyti metaduomenis, atsižvelgdami į peržvalgos tipą ir pašto indeksą.

## <a name="do-all-engine-configurations-require-metadata"></a>Ar visoms mechanizmų konfigūracijoms būtini metaduomenys?
Ne. Transportavimo valdymo mechanizmams, naudojamiems nuskaityti duomenis, kurių reikia tarifų skaičiavimui iš išorinių sistemų atlikti, metaduomenys nereikalingi. Šių mechanizmų tarifų duomenis galima nuskaityti iš išorinių transportavimo vežėjo sistemų, paprastai naudojantis žiniatinklio tarnyba. Pavyzdžiui, galite naudoti kilometražo mechanizmą, kuris nuskaito duomenis tiesiogiai iš „Bing“ žemėlapių, kad šiam mechanizmui nereikėtų naudoti metaduomenų.

| **Pastaba.**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transportavimo valdymo mechanizmai, gauti naudojant Tiekimo grandinės valdymą, naudoja duomenis, nuskaitomus iš programos. Mechanizmai, kurie jungiasi prie išorinių sistemų, į programą „Operations“ neįtraukti. Tačiau mechanizmo pagrindu veikiantis išplėtimo modelis leidžia kurti plėtinius naudojant „Visual Studio“ įrankius. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Kaip sukonfigūruoti transportavimo valdymo mechanizmo metaduomenis?
Transportavimo valdymo mechanizmų metaduomenys skirtingų tipų mechanizmams konfigūruojami skirtingai.

| Transportavimo valdymo mechanizmas               | Metaduomenų konfigūracija                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tarifo nustatymo mechanizmas**                                | Reikalingas **Tarifo pagrindo tipas**. Tarifo pagrindo tipe yra tarifo pagrindo duomenų ir tarifo pagrindo priskyrimo duomenų metaduomenų. Tarifo pagrindo metaduomenų struktūrą nurodo tarifų mechanizmo tipas. Tarifo bazės priskyrimo metaduomenų struktūrą nurodo tarifo bazės priskyriklio, susieto su tuo tarifų mechanizmu, tipas. Tarifų mechanizmo tarifo bazės tipas nustatomas puslapiuose **Tarifo nustatymo mechanizmas** ir **Pagrindinis tarifas**. |
| **Zonos mechanizmas**                                | Metaduomenys turi būti nustatyti tiesiogiai pagrindinėje zonoje.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Tranzito laiko mechanizmas** ir **Kilometražo mechanizmas** | Metaduomenys nuskaitomi tiesiogiai iš kilometražo mechanizmo konfigūracijos nustatymo formos.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Tarifų mechanizmo metaduomenų pavyzdys** Transportavimo valdymo mechanizmui reikia nurodyti pradinį adresą, paskirties apskritį ir šalį / regioną bei siuntos pradžios ir pabaigos taškus. Naudojant šiuos reikalavimus, metaduomenys atrodys taip, kaip duomenys toliau pateiktoje lentelėje. Lentelėje taip pat pateikiama informacija, kokio tipo įvesties duomenys yra būtini.
-   Šią informaciją apibrėžkite puslapio **Tarifo pagrindo tipas** dalyje **Transportavimo valdymas** &gt; **Sąranka**.

| Seka | Vardas                          | Lauko tipas | Duomenų tipas | Peržvalgos tipas    | Privaloma |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Pradinis pašto indeksas            | Priskyrimas | Eilutė    | Pašto indeksas    | Pasirinkta  |
| 2        | Paskirties apskritis             | Priskyrimas | Eilutė    | Valstija          |           |
| 3        | Pradinis paskirties vietos pašto indeksas | Priskyrimas | Eilutė    | Pašto indeksas    | Pasirinkta  |
| 4        | Galutinis paskirties pašto indeksas   | Priskyrimas | Eilutė    | Pašto indeksas    | Pasirinkta  |
| 5        | Paskirties šalis           | Priskyrimas | Eilutė    | Šalis/regionas |           |

### <a name="whitepaper"></a>Techninė Dokumentacija

Norėdami gauti daugiau informacijos, atsisiųskite šią techninę dokumentaciją (sukurtą AX2012 palaikymui, tačiau vis dar taikoma „Dynamics 365 Supply Chain Management”)

- [Transportavimo valdymo mechanizmai](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]