---
title: Valiutos duomenų tipo perkėlimas dvigubui rašymui
description: Šioje temoje aprašoma, kaip pakeisti dešimtainių skaičius, kurie dvigubu rašymu palaiko valiutą.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 073f89b5ae44e20d1d2e854341afaa176f9b6280
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350940"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Valiutos duomenų tipo perkėlimas dvigubui rašymui

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Galite padidinti dešimtainių skaičių, palaikomų daugiausiai iki 10 valiutoms vertėms, kiekį. Numatytoji riba yra keturi dešimtainiai skaičiai. Padidinę dešimtainių skaičių kiekį, padėsite išvengti duomenų praradimo, kai naudosite dvigubo rašymo funkciją sinchronizuodami duomenis. Dešimtainių skaičių padidinimas yra pasirenkamas pakeitimas. Norėdami jį įgyvendinti, turite paprašyti pagalbos iš „Microsoft”.

Norėdami pakeisti dešimtainių skaičių kiekį, turite atlikti du žingsnius:

1. Perkėlimo užklausa iš „Microsoft”.
2. Dešimtainių skaičių kiekio pakeitimas „Dataverse”.

„Finance and Operations” programėlė ir „Dataverse” turi palaikyti tą patį dešimtainių skaičių kiekį valiutos vertėse. Priešingu atveju, kai ši informacija sinchronizuojama tarp programėlių, gali dingti duomenys. Perkėlimo procesas perkonfigūruoja, kaip saugomos valiutos ir valiutos kurso vertės, bet jokie duomenys nesikeičia. Baigus perkėlimą, valiutų kodų ir kainų dešimtainių skaičių kiekis gali būti padidintas, o vartotojų įvesti ir peržiūrėti duomenys gali būti tikslesni dešimtainių tikslumu.

Perkėlimas yra neprivalomas. Jei didesnio dešimtainių skaičių kiekio palaikymas jums naudingas, rekomenduojame apsvarstyti perkėlimą. Organizacijoms, kurioms nereikia jokių verčių, kuriose yra daugiau nei keturi dešimtainiai skaičiai, perkėlimas nebūtinas.

## <a name="requesting-migration-from-microsoft"></a>Perkėlimo užklausos siuntimas „Microsoft”

Saugojimas esamiems valiutos stulpeliams „Dataverse” negali palaikyti daugiau nei keturių dešimtainių skaičių. Todėl perkėlimo metu valiutos vertės nukopijuojamos į naujus duomenų bazės vidinius stulpelius. Šis procesas vyksta nuolatos, kol bus perkelti visi duomenys. Viduje perkėlimo pabaigoje, naujieji saugojimo tipai pakeičia senus saugojimo tipus, tačiau duomenų vertės lieka nepakitusios. Valiutos stulpeliai gali palaikyti iki 10 dešimtainių skaičių. Perkėlimo metu „Dataverse” gali būti toliau naudojama be pertraukos.

Tuo pačiu metu keitimo kursai modifikuojami taip, kad jie palaikytų iki 12 dešimtainių skaičių, o ne dabartinę 10 limitą. Šis pakeitimas būtinas, kad dešimtainių skaičių kiekis būtų toks „Finance and Operations” programėlėje ir „Dataverse”.

Perkėlimas nekeičia jokių duomenų. Kai valiutos ir keitimo kurso stulpeliai konvertuoti, administratoriai gali konfigūruoti sistemą, kad būtų galima naudoti iki 10 dešimtainių skaičių valiutos stulpeliams, nurodydami kiekvienos operacijos valiutos ir kainos dešimtainių skaičių kiekį.

### <a name="request-a-migration"></a>Perkėlimo užklausa

Norėdami įjungti šią funkciją, susiekite el. paštu **CDSExpandDecimal@microsoft.com** ir nurodykite šią informaciją:

+ **Tema:** Užklausa įgalinti išplėstinį dešimtainių skaičių palaikymą, skirtą \<organizationID\>
+ **Pagrindinė dalis:** Norėčiau įgalinti išplėstinį dešimtainių skaičių palaikymą mano org. \<organizationID\>.

„Microsoft” atstovas susisieks su jumis per dvi ar tris darbo dienas dėl tolesnių veiksmų.

Kai prašote perkelti, turite žinoti apie šiuos dalykus ir pasiruošti jiems atitinkamai:

+ Laikas, skirtas perkelti duomenis, priklauso nuo duomenų kiekio sistemoje. Didelių duomenų bazių perkėlimas gali užtrukti kelias dienas.
+ Perkėlimo metu duomenų bazės dydis laikinai padidėja, nes indeksuose reikia papildomos vietos. Kai perkėlimas baigtas, dauguma papildomos vietos atlaisvinama.
+ Perkėlimo proceso metu įvykus klaidai, neleidžiančios užbaigti perkėlimo, sistema parodo įspėjimus „Microsoft Support”, kad „Support” personalas galėtų įsikišti. Tačiau, net jei vykdant perkėlimą įvyksta klaidų, „Dataverse” tolesnis naudojimas nesutrinka.
+ Perkėlimo procesas nėra grįžtamas.

## <a name="changing-the-number-of-decimal-places"></a>Dešimtainių skaičių kiekio keitimas

Baigus perkėlimą, „Dataverse” gali būti saugomi skaičiai, turintys daugiau dešimtainių skaičių. Administratoriai gali pasirinkti, kiek dešimtainių skaičių naudojama konkretiems valiutos kodams ir kainoms. „Microsoft Power Apps” „Power BI”, ir „Power Automate” vartotojai gali tada peržiūrėti ir naudoti skaičius, turinčius daugiau dešimtainių skaičių.

Norėdami atlikti šį keitimą, turite atnaujinti šiuos parametrus „Power Apps”:

+ **Sistemos parametrai: kainos valiutos tikslumas** – **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** stulpelyje nustatoma, kaip valiuta veiks organizacijoje, kai **Kainos tikslumas** yra pasirinktas.
+ **Verslo valdymas: valiutos** – **Valiutos tikslumas** stulpelis leidžia nurodyti pasirinktinį dešimtainių skaičių kiekį konkrečiai valiutai. Yra atsarginis visai organizacijai taikomas parametras.

Yra keletas apribojimų:

+ Negalite sukonfigūruoti valiutos stulpelio lentelėje.
+ Galite nurodyti daugiau nei keturis dešimtainius skaičius **Kaina** ir **Operacijos valiuta** lygiuose.

### <a name="system-settings-currency-precision-for-pricing"></a>Sistemos parametrai: valiutos kainos tikslumas

Baigus perkėlimą, administratoriai gali nustatyti valiutos tikslumą. Eikite į **Parametrai \> Administravimas** ir pasirinkite **Sistemos parametrai**. Tada skirtuke **Bendra** pakeiskite **Nustatyti valiutos tikslumą, naudojamą kainai visoje sistemoje** stulpelio vertę, kaip parodyta šioje iliustracijoje.

![Valiutos sistemos parametrai.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Verslo valdymas: valiutos

Jei jums reikia, kad valiutos tikslumas konkrečiai valiutai skirtųsi nuo valiutos tikslumo, naudojamo kainai, galite jį pakeisti. Eikite į **Parametrai \> Verslo valdymas**, pasirinkite **Valiutos** ir pasirinkite valiutą, kurią norite pakeisti. Tada nustatykite **Valiutos tikslumas** stulpelį pagal dešimtainių skaičių kiekį, kaip parodyta šioje iliustracijoje.

![Konkrečios lokalės valiutos parametrai.](media/specific-currency.png)

### <a name="tables-currency-column"></a>lentelės: stulpelis Valiuta

Galima tik keturis kartus koreguoti dešimtainių skaičių, skirtų konkrečios valiutos stulpeliams, kiekius.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]