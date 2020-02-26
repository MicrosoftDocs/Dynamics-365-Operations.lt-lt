---
title: Duomenų integravimo technologijos pasirinkimas
description: Šiame straipsnyje pateikiami nurodymai dėl įvairių integravimo su „Human Resources“ valdomais duomenimis parinkčių, aprašomi įvairių integravimo technologijų ypatumai, kad integratoriai galėtų priimti pagrįstus sprendimus dėl tinkamiausių technologijų jų poreikiams.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029893"
---
# <a name="choose-a-data-integration-technology"></a>Duomenų integravimo technologijos pasirinkimas

Programa „Dynamics 365 Human Resources“ valdomi verslo duomenis, kurie naudingi įvairiuose verslo procesuose. Šiame straipsnyje pateikiami nurodymai dėl įvairių integravimo su „Human Resources“ valdomais duomenimis parinkčių, aprašomi įvairių integravimo technologijų ypatumai, kad integratoriai galėtų priimti pagrįstus sprendimus dėl tinkamiausių technologijų jų poreikiams.

## <a name="data-integration-vision"></a>Duomenų integravimo vizija

„Microsoft“ suvokia verslo duomenis kaip pagrindinį turtą, dėl kurio jūsų įmonė yra unikali. Jūsų verslo duomenys labai vertingi. Duomenys, surinkti ir tvarkomi viena verslo dalimi, yra susiję su duomenimis, kuriuos surinko kita verslo dalis, o šie ryšiai gali būti naudojami verslo procesams ir verslo įžvalgoms savo organizacijoje gerinti. Užtikrinti paprastą, saugią ir stabilią prieiga prie jūsų verslo duomenų, neatsižvelgiant į tai, kuriai sistemai duomenys „priklauso“, – pagrindinis principas mūsų vizijos dėl duomenų integravimo su „Human Resources“.

Istoriniu požiūriu duomenų integravimas tarp kelių sistemų buvo sudėtingas.
„Microsoft“ imasi veiksmų, kad būtų lengviau integruoti duomenis, ir sparčiai artėja šio tikslo link, kai jis realizuojamas pasitelkiant [„Common Data Service“](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Žvelgiant į ateitį, dėl „Human Resources“ programos „Common Data Service“ tampa pageidaujama „Human Resources“ duomenų viešoji sąsaja. Ilgainiui mes tikimės, kad visi svarbiausi duomenys, valdomi „Human Resources“ programos, bus išstatyti „Common Data Service“. Rekomenduojame „Common Data Service“ kaip rinktinę technologiją daugeliui integravimo taikymų. Nors mes suprantame, kad šiuo metu galbūt nėra visų jūsų programai reikiamų duomenų platformoje „Common Data Service“, o jūsų projektų laiko planavimo juostoms gali prireikti alternatyvių technologijų, prašome mums pranešti, kai „Common Data Service“ neatitinka jūsų integravimo poreikių.

## <a name="integration-technologies"></a>Integravimo technologijos

Tolesniuose skyriuose aprašomos įvairios duomenų integravimo technologijos, kurias galima naudoti su „Human Resources“.

### <a name="common-data-service-entities"></a>„Common Data Service“ objektai

„Common Data Service“ yra pageidaujama „Human Resources“ viešoji duomenų sąsaja. „Common Data Service“ yra sukurta išbandytos platformos pagrindu, išvystyta iš „Dynamics 365“ „XRM“ platformos, pagal kurią [„Dynamics 365 Customer Engagement“](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) sprendimai yra sukurti.

„Common Data Service“ teikia duomenų objektų platformą ir API, kad būtų galima pasiekti šiuos objektus. Kai „Human Resources“ yra diegiamas jūsų organizacijoje, „Human Resources“ yra susiejamas su „Common Data Service“ egzemplioriumi, o objektai, kuriais tvarkomi„Human Resources“ duomenys, yra diegiami į tą patį „Common Data Service“ egzempliorių, todėl objektai ir jų duomenys prieinami bet kuriai programai, kuri gali jungtis prie „Common Data Service“ egzemplioriaus. Atsižvelgiant į tai, kokias „Human Resources“ programas naudojate, „Human Resources“ atlieka duomenų operacijas tiesiogiai su „Common Data Service“ objektais (tai taikoma su „Attract“ ir Onboard“) arba sinchronizuoja duomenis su „Common Data Service“ objektais.

Kai duomenų objektai, kurie pateikia duomenis, reikiamų jūsų integravimo programoms, yra įtraukti į „Common Data Service“, galite visapusiškai naudotis [„Common Data Service“ ir jos palaikomas API](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Tarp palaikomų API yra [„Dynamics 365“ žiniatinklio API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kuri pateikia prieigos prie „Common Data Service“ duomenų „OData“ diegimą.

„Common Data Service“ objektai ir susiję API yra geriausias pasirinkimas pasiekti „Human Resources“ duomenis iš žiniatinklio programų, tinklo tarnybų / API ir bet kurios kitos programos, kuri jungiasi prie „OData“ sklaidos kanalų.

> [!NOTE]
> Kadangi sprendimas teikti „Common Data Service“ pirmenybę kaip „Human Resources“ duomenų sąsajai priimtas gana neseniai, galite pastebėti, kad „Human Resources“ duomenų objektai, kuriuos reikia įtraukti į savo integraciją, dar nėra teikiami „Common Data Service“<sup>1</sup>. Jei jūsų integracijai reikalingų „Human Resources“objektai dar nėra pasiekiami, turite palaukti, kol duomenų objektai bus prieinami, arba turite naudoti vieną iš toliau aprašytų integravimo technologijų.
> 
> Pagal numatytuosius parametrus naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Common Data Service“ integravimas yra išjungtas. Jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenys aplinkose pradedami sinchronizuoti tada, kai jie yra parengti. Kai jūsų aplinka paruošta sinchronizuoti duomenis, galite įjungti integravimą.

<sup>1</sup>Norėdami gauti „Human Resources“ objektų, pasiekiamų „Common Data Service“ sąrašą, žr. [„Human Resources“ ir „Common Data Service”](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Programose „Attract“ ir „Onboard“ visi objektai pasiekiami „Common Data Service“.

### <a name="dmfdixf-entities"></a>DMF / DIXF objektai

„Human Resources“, sukurta tos pačios platformos kaip ir „Finance and Operations“ programos pagrindu, teikia [duomenų tvarkymo sistemą (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), kartais dar vadinamą duomenų importavimo / eksportavimo sistema arba DIXF, ir duomenų objektų, kuriuos galima naudoti importuojant / eksportuojant duomenis į / iš „Human Resources“, rinkinį. Nors „Common Data Service“ objektai yra pageidaujama „Human Resources“ duomenų integravimo sąsaja, DMF objektai vis dar naudingi tam tikromis aplinkybėmis, pvz.:

- „Common Data Service“ objektai dar nepasiekiami.

- Integruojant reikia didelio našumo masinio duomenų importavimo / eksportavimo gebų.

DMF objektai šiuo metu teikia Išsamiausių duomenų aprėptį „Human Resources“ duomenims.

DMF yra netinkama realiojo laiko integracijoms (pvz., kai reikia nedelsiant pateikti vartotojo atsiliepimų vartotojo sąsajoje), nes paketinės operacijos yra suplanuotos paketinės užduotys, ir dažnai turi mažiausiai 1–2 minučių gaištį, kol paketinė tarnyba pradės užduoties vykdymą, bei importavimo/eksportavimo operacijai atlikti gali prireikti laiko tiek, kiek tai bus vykdoma.

DMF gali būti geriausia išeitis, kai reikalingas didelis pralaidumas (pvz., naktį suplanuotam daugiatūkstantinių įrašų importavimui / eksportavimui).

> [!NOTE]
> DMF nepasiekiamas programose „Attract“ ir „Onboard“.

### <a name="dmf-package-rest-api"></a>DMF paketo REST API

DMF teikia [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api)manipuliuoti duomenų paketus. Šis API gali būti naudojamas programiškai sąveikauti su DMF, tad galima atlikti tokius veiksmus:

- Importuoti duomenų paketą.

- Eksportuoti duomenų paketą.

- Tikrinti importavimo / eksportavimo operacijos būsena.

DMF paketo REST API yra visiškai palaikoma „Human Resources: Core HR“.

### <a name="azure-sql-db-byod"></a>„Azure SQL“ DB (BYOD)

DMF papildomai suteikia galingą funkciją (paprastai žinomą kaip [Savo duomenų bazės naudojimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)arba BYOD), kuri leidžia „Human Resources“ eksportuoti duomenis į savo „Microsoft Azure“ SQL duomenų bazę. Tai suteikia didžiulį dinamiškumą, nes kai duomenys yra jūsų SQL duomenų bazėje, galite naudoti bet kurias programas arba tarpinę programinę įrangą, kurios gali jungtis prie SQL duomenų saugyklos.

BYOD paprastai turėtų būti laikoma tik skaityti skirtu sprendimu. Nors jūs galite manipuliuoti ir saugoti visus duomenis, kuriuos norite „Azure SQ“ duomenų bazėje (pvz., duomenų mišinius), duomenų, saugomų „Azure SQL“ duomenų bazėje, nebus galima sinchronizuoti atgal į „Human Resources“.

BYOD tinka ataskaitoms apie sprendimus, duomenų integravimus, duomenų mišinius, kaip duomenų šaltinis, skirtas srautui [„Azure Data Factory“](https://docs.microsoft.com/azure/data-factory/).

> [!NOTE]
> BYOD nepasiekiamas programose „Attract“ ir „Onboard“.

### <a name="odata-enabled-entities"></a>„OData“ palaikomi objektai

Dauguma DMF objektų yra įgalinami prieigai per „Human Resources“ duomenų tarnybą („OData“). Pateikta [„Finance and Operations“ „OData“ tarnybos](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) dokumentacija paprastai taikoma ir programai „Human Resources“, nors dokumentacija apie savo „OData“ rodomų objektų kūrimą nebus taikoma.

Nors ir „Common Data Service“ ir „OData” diegimas, patekiamas „Common Data Service“ (per [„Dynamics 365“ žiniatinklio API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), yra pageidaujamas naudojant „Human Resources“ duomenų tarnybą, „Human Resources“ duomenų tarnyba šiuo metu turi didesnę objektų sudėties aprėptį, skirtą „Human Resources“ duomenims.

### <a name="excel-add-in"></a>„Excel“ priedas

Su [„Excel“ priedu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) galėsite plačiau naudoti „OData” palaikomus objektus. Jis suteikia patogų būdą galutiniam vartotojui gauti ir modifikuoti „Human Resources“ duomenis per pažįstamą „Excel“ vartotojo sąsają (UI).

„Excel“ papildinys tinkamas verslo srities ekspertams importuoti / eksportuoti ad hoc duomenis. Pasikartojančių duomenų integravimui, kuriam reikia programinės automatizacijos, kita integravimo technologija bus tinkamesnė.

### <a name="data-integrator"></a>Duomenų integratorius

„Common Data Service“ administratoriaus funkcijos suteikia [duomenų integratoriaus tarnybą](https://docs.microsoft.com/powerapps/administrator/data-integrator), kuri gali būti naudojama duomenų integravimams į / iš „Common Data Service“. Duomenų integratorius gali būti naudojamas integravimo projektams apibrėžti (dažnai yra pagrįstas iš anksto nustatytais šablonais, kuriuos programos kūrėjai pritaikė konkretiems integravimams). Integravimo projektus galima planuoti vykdyti automatiškai pasikartojančiu grafiku arba vykdyti rankiniu būdu.

Duomenų integratoriaus projektai yra tinkami „Common Data Service“ paketų integravimams ir yra puikus pasirinkimas integravimams tarp „Dynamics 365“ programų šeimos. Pavyzdžiui, „Microsoft“ pateikia iš anksto paruoštą duomenų integratoriaus šabloną, kuris gali būti naudojamas integruojant duomenis iš „Human Resources“ į „Dynamics 365 Finance“. Daugiau informacijos žr. [Integravimas iš „Dynamics 365 Human Resources“ į „Dynamics 365 Finance“](hr-admin-integration-finance.md).

### <a name="power-query"></a>„Power Query“

Duomenų integratorius taip pat palaiko [„Power Query“](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (naudodamas savo [išplėstinės užklausos funkciją](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
„Power Query“ suteikia galingą, lankstų duomenų filtravimą ir transformavimą, įskaitant raiškiąją M formulės kalbą, ir gali būti pažįstama tiems, kurie turi patirties kuriant „Power BI“ ataskaitas.

## <a name="deciding-on-an-integration-technology"></a>Integravimo technologijos pasirinkimas

Naudojant tiek daug skirtingų integravimo technologijų, sprendžiant, kurį integravimo metodą rinktis, kartais gali pasirodyti keblu. Ilgainiui ir ypač kai „Common Data Service“ duomenų aprėptis auga, sprendimas taps lengvesnis, nes dauguma atvejų „Common Data Service“ bus pageidaujama duomenų sąsaja. Tačiau iki tol jūs galite pastebėti, kad „Common Data Service“ dar negali patenkinti jūsų poreikių. Toliau pateikiamoje lentelėje pateikiama kelių pagrindinių įvairių integravimo technologijos parinkčių charakteristikų suvestinė.

| Technologija / Įrankis / API    | Pasikartojančios integracijos                   | Sinchroninė / asinchroninė                    | Programinė prieiga naudojant API        | Atitinkami duomenų tomai                                   | Duomenų aprėptis                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| „Common Data Service“ objektai           | Taip, naudojant duomenų integratorių arba tarpinę programinę įrangą | „Sync“, „Async“, „Batch“ (naudojant duomenų integratorių) | Taip, naudojant „Dynamics 365“ žiniatinklio API („OData“) | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Tobulinimas<sup>2</sup>                       |
| DMF objektai           | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip, naudojant DMF paketo REST API         | Didelis (šimtai tūkstančių įrašų)                    | Aukštas                                |
| DMF paketo REST API   | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip                                       | Didelis (šimtai tūkstančių įrašų)                    | API palaiko visus DMF objektus       |
| BYOD                   | Taip, suplanuota administratoriaus programoje „Human Resources“        | „Async“, „Batch“                                | Ne<sup>3</sup>                                    | Didelis (šimtai tūkstančių įrašų)                    | Palaiko visus DMF objektus           |
| „OData“ palaikomi objektai | Taip, naudojant tarpinę programinę įrangą                    | Sinchronizuoti                                        | Taip, naudojant „Human Resources“ duomenų tarnybą („OData“)  | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Aukštas                                |
| „Excel“ priedas           | Ne                                       | Sinchronizuoti                                        | Ne                                        | Vidutinis (dešimtys tūkstančių įrašų)                      | Palaiko visus „OData“ palaikomus objektus |
| Duomenų integratorius        | Taip, suplanuota duomenų Integratoriuje        | „Async“, „Batch“                                | Ne                                        | Skiriasi pagal naudojimo atvejį                                       | Palaiko visus „Common Data Service“ objektus           |

<sup>2</sup>„Microsoft“ daug investuoja, kad išplėstų „Common Data Service“ objektų duomenų aprėptį, bei rekomenduoja „Common Data Service“ kaip pageidaujamą duomenų sąsają, kai aprėptis yra prieinama. Šiuo metu „Common Data Service“ duomenų aprėptis yra maža, palyginus su DMF ir „OData“ palaikomais objektais.

<sup>3</sup>SQL duomenų bazė gali būti prieinama programiškai.

## <a name="summary"></a>Suvestinė

Jūsų verslo duomenys yra vertingas turtas, bet jo vertė gali būti labai sumažinta, jei sunku naudoti duomenis konkretiems tikslams (pvz., ataskaitų, duomenų mišinius ar pasirinktines programas). „Dynamics 365 Human Resources“ suteikia kelias technologijas, skirtas dirbti su duomenimis, kurie nepriklauso „Human Resources“ programos vartotojo sąsajai (UI), todėl leidžiama programų prieigos prie duomenų integracija. Šioje temoje aprašomos galimos integravimo technologijos ir kai kurios jų pagrindinės charakteristikos. Ši informacija turėtų padėti priimti geresnius sprendimus, kokiais būdais naudoti jūsų integravimo projektus.

