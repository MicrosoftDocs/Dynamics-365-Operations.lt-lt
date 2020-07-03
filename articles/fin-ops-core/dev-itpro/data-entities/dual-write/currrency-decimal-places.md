---
title: Valiutos duomenų tipo perkėlimas dvigubui rašymui
description: Šioje temoje aprašoma, kaip pakeisti dešimtainių skaičius, kurie dvigubu rašymu palaiko valiutą.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456819"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valiutos duomenų tipo perkėlimas dvigubui rašymui

[!include [banner](../../includes/banner.md)]

Galite padidinti dešimtainių skaičių, palaikomų daugiausiai iki 10 valiutoms vertėms, kiekį. Numatytoji riba yra keturi dešimtainiai skaičiai. Padidinę dešimtainių skaičių kiekį, padėsite išvengti duomenų praradimo, kai naudosite dvigubo rašymo funkciją sinchronizuodami duomenis. Dešimtainių skaičių padidinimas yra pasirenkamas pakeitimas. Norėdami jį įgyvendinti, turite paprašyti pagalbos iš „Microsoft”.

Norėdami pakeisti dešimtainių skaičių kiekį, turite atlikti du žingsnius:

1. Perkėlimo užklausa iš „Microsoft”.
2. Dešimtainių skaičių kiekio pakeitimas „Common Data Service”.

„Finance and Operations” programėlė ir „Common Data Service” turi palaikyti tą patį dešimtainių skaičių kiekį valiutos vertėse. Priešingu atveju, kai ši informacija sinchronizuojama tarp programėlių, gali dingti duomenys. Perkėlimo procesas perkonfigūruoja, kaip saugomos valiutos ir valiutos kurso vertės, bet jokie duomenys nesikeičia. Baigus perkėlimą, valiutų kodų ir kainų dešimtainių skaičių kiekis gali būti padidintas, o vartotojų įvesti ir peržiūrėti duomenys gali būti tikslesni dešimtainių tikslumu.

Perkėlimas yra neprivalomas. Jei didesnio dešimtainių skaičių kiekio palaikymas jums naudingas, rekomenduojame apsvarstyti perkėlimą. Organizacijoms, kurioms nereikia jokių verčių, kuriose yra daugiau nei keturi dešimtainiai skaičiai, perkėlimas nebūtinas.

## <a name="requesting-migration-from-microsoft"></a>Perkėlimo užklausos siuntimas „Microsoft”

Saugojimas esamiems valiutos laukams „Common Data Service” negali palaikyti daugiau nei keturių dešimtainių skaičių. Todėl perkėlimo metu valiutos vertės nukopijuojamos į naujus duomenų bazės vidinius laukus. Šis procesas vyksta nuolatos, kol bus perkelti visi duomenys. Viduje perkėlimo pabaigoje, naujieji saugojimo tipai pakeičia senus saugojimo tipus, tačiau duomenų vertės lieka nepakitusios. Valiutos laukai gali palaikyti iki 10 dešimtainių skaičių. Perkėlimo metu „Common Data Service” gali būti toliau naudojama be pertraukos.

Tuo pačiu metu keitimo kursai modifikuojami taip, kad jie palaikytų iki 12 dešimtainių skaičių, o ne dabartinę 10 limitą. Šis pakeitimas būtinas, kad dešimtainių skaičių kiekis būtų toks „Finance and Operations” programėlėje ir „Common Data Service”.

Perkėlimas nekeičia jokių duomenų. Kai valiutos ir keitimo kurso laukai konvertuoti, administratoriai gali konfigūruoti sistemą, kad būtų galima naudoti iki 10 dešimtainių skaičių valiutos laukas nurodant kiekvienos operacijos valiutos ir kainos dešimtainių skaičių kiekį. 

### <a name="request-a-migration"></a>Perkėlimo užklausa

Norėdami įjungti šią funkciją, susiekite el. paštu **CDSExpandDecimal@microsoft.com** ir nurodykite šią informaciją:

+ **Tema:** Užklausa įgalinti išplėstinį dešimtainių skaičių palaikymą, skirtą \<organizationID\>
+ **Pagrindinė dalis:** Norėčiau įgalinti išplėstinį dešimtainių skaičių palaikymą mano org. \<organizationID\>.

„Microsoft” atstovas susisieks su jumis per dvi ar tris darbo dienas dėl tolesnių veiksmų.

Kai prašote perkelti, turite žinoti apie šiuos dalykus ir pasiruošti jiems atitinkamai:

+ Laikas, skirtas perkelti duomenis, priklauso nuo duomenų kiekio sistemoje. Didelių duomenų bazių perkėlimas gali užtrukti kelias dienas.
+ Perkėlimo metu duomenų bazės dydis laikinai padidėja, nes indeksuose reikia papildomos vietos. Kai perkėlimas baigtas, dauguma papildomos vietos atlaisvinama.
+ Perkėlimo proceso metu įvykus klaidai, neleidžiančios užbaigti perkėlimo, sistema parodo įspėjimus „Microsoft Support”, kad „Support” personalas galėtų įsikišti. Tačiau, net jei vykdant perkėlimą įvyksta klaidų, „Common Data Service” tolesnis naudojimas nesutrinka.
+ Perkėlimo procesas nėra grįžtamas.

## <a name="changing-the-number-of-decimal-places"></a>Dešimtainių skaičių kiekio keitimas

Baigus perkėlimą, „Common Data Service” gali būti saugomi skaičiai, turintys daugiau dešimtainių skaičių. Administratoriai gali pasirinkti, kiek dešimtainių skaičių naudojama konkretiems valiutos kodams ir kainoms. „Microsoft Power Apps” „Power BI”, ir „Power Automate” vartotojai gali tada peržiūrėti ir naudoti skaičius, turinčius daugiau dešimtainių skaičių.

Norėdami atlikti šį keitimą, turite atnaujinti šiuos parametrus „Power Apps”:

+ **Sistemos parametrai: kainos valiutos tikslumas** – **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** lauke, nustatoma, kaip valiuta veiks organizacijoje, kai **Kainos tikslumas** pasirenkamas.
+ **Verslo valdymas: valiutos** – **Valiutos tikslumas** laukas leidžia nurodyti pasirinktinį dešimtainių skaičių kiekį konkrečiai valiutai. Yra atsarginis visai organizacijai taikomas parametras.

Yra keletas apribojimų:

+ Negalite sukonfigūruoti objekto valiutos lauko.
+ Galite nurodyti daugiau nei keturis dešimtainius skaičius **Kaina** ir **Operacijos valiuta** lygiuose.

### <a name="system-settings-currency-precision-for-pricing"></a>Sistemos parametrai: valiutos kainos tikslumas

Baigus perkėlimą, administratoriai gali nustatyti valiutos tikslumą. Eikite į **Parametrai \> Administravimas** ir pasirinkite **Sistemos parametrai**. Tada **Bendra** skirtuke pakeiskite **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** lauko vertę, kaip parodyta šioje iliustracijoje.

![Valiutos sistemos parametrai](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Verslo valdymas: valiutos

Jei jums reikia, kad valiutos tikslumas konkrečiai valiutai skirtųsi nuo valiutos tikslumo, naudojamo kainai, galite jį pakeisti. Eikite į **Parametrai \> Verslo valdymas**, pasirinkite **Valiutos** ir pasirinkite valiutą, kurią norite pakeisti. Tada nustatykite **Valiutos tikslumas** lauką pagal dešimtainių skaičių kiekį, kaip parodyta šioje iliustracijoje.

![Konkrečios lokalės valiutos parametrai](media/specific-currency.png)

### <a name="entities-currency-field"></a>Objektai: valiutos laukas

Galima tik keturis kartus koreguoti dešimtainių skaičių, skirtų konkrečios valiutos laukams, kiekius.
