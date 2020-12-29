---
title: Duomenų integravimo technologijos pasirinkimas
description: Šiame straipsnyje pateikiama informacija apie integravimą su „Human Resources” valdomais duomenimis. Jame aprašomos įvairios integravimo technologijos, kad apsispręstumėte, kurios technologijos labiausiai atitinka jūsų poreikius.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
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
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528346"
---
# <a name="choose-a-data-integration-technology"></a>Duomenų integravimo technologijos pasirinkimas

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje pateikiama informacija apie integravimą su „Dynamics 365 Human Resources” valdomais duomenimis. Jame aprašomos įvairios integravimo technologijos, kad apsispręstumėte, kurios technologijos labiausiai atitinka jūsų poreikius.

## <a name="data-integration-background"></a>Duomenų integravimo fonas

Verslo duomenys yra pagrindinis turtas, dėl kurio jūsų įmonė yra unikali. Jūsų verslo duomenys labai vertingi. Galite naudoti ryšius tarp savo verslo duomenų, kad galėtumėte pagerinti savo organizacijos verslo procesus ir įžvalgas. Siekiame suteikti paprastą, saugią ir stabilią prieigą prie jūsų verslo duomenų, nepriklausomai nuo sistemos, kurioje jie yra.

Istoriniu požiūriu duomenų integravimas tarp kelių sistemų buvo sudėtingas.
„Microsoft“ imasi veiksmų, kad būtų lengviau integruoti duomenis, ir sparčiai artėja šio tikslo link, kai jis realizuojamas pasitelkiant [„Common Data Service“](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Dėl „Human Resources“ programos „Common Data Service“ tampa pageidaujama „Human Resources“ duomenų viešoji sąsaja. Ilgainiui mes tikimės, kad visi svarbiausi duomenys, valdomi „Human Resources“ programos, bus išstatyti „Common Data Service“. Rekomenduojame „Common Data Service“ kaip rinktinę technologiją daugeliui integravimo taikymų.

Mes suprantame, kad „Common Data Service” dar gali būti ne visi jūsų programai reikalingi duomenys. Taip pat suprantame, kad jūsų projektų laiko planavimo juostai gali prireikti alternatyvių technologijų. Praneškite mums, kai „Common Data Service” neatitinka jūsų integravimo poreikių.

## <a name="integration-technologies"></a>Integravimo technologijos

Tolesniuose skyriuose aprašomos įvairios duomenų integravimo technologijos, kurias galima naudoti su „Human Resources“.

### <a name="common-data-service-entities"></a>„Common Data Service“ objektai

„Common Data Service“ yra pageidaujama „Human Resources“ viešoji duomenų sąsaja. Ji atsirado iš „Dynamics 365” „XRM” platformos, kurią naudoja [„Dynamics 365 Customer Engagement”](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) sprendimai.

„Common Data Service” pateikiama duomenų objektų platforma ir API. Kai diegiate „Human Resources”, ji prijungiama prie „Common Data Service” egzemplioriaus. „Human Resources” duomenų objektai įdiegiami tame „Common Data Service” egzemplioriuje. Objektai ir jų duomenys prieinami bet kuriai programai, kuri gali prisijungti prie „Common Data Service” egzemplioriaus. „Human Resources” sinchronizuoja duomenis su „Common Data Service” objektais ir iš jų.

Kai duomenų objektai, reikalingi jūsų integravimo programoms, yra „Common Data Service”, galite išnaudoti visas [„Common Data Service” ir API, kurias ji palaiko](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer), galimybes. Tarp palaikomų API yra [„Dynamics 365“ žiniatinklio API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kuri pateikia prieigos prie „Common Data Service“ duomenų „OData“ diegimą.

„Common Data Service“ objektai ir su jais susiję API yra geriausias pasirinkimas pasiekti „Human Resources“ duomenis iš žiniatinklio programų, tinklo tarnybų / API ir bet kurios kitos programos, kuri jungiasi prie „OData“ sklaidos kanalų.

> [!NOTE]
> Kadangi sprendimas teikti „Common Data Service“ pirmenybę kaip „Human Resources“ duomenų sąsajai priimtas gana neseniai, galite pastebėti, kad „Human Resources“ duomenų objektai, kuriuos reikia įtraukti į savo integraciją, dar nėra teikiami „Common Data Service“.
</br>
> Norėdami gauti „Human Resources“ objektų, pasiekiamų „Common Data Service“ sąrašą, žr. [„Human Resources“ ir „Common Data Service”](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Jei jūsų integracijai reikalingų „Human Resources“objektai dar nėra pasiekiami, turite palaukti, kol duomenų objektai bus prieinami, arba turite naudoti vieną iš toliau aprašytų integravimo technologijų.
> </br>
> Pagal numatytuosius parametrus naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Common Data Service“ integravimas yra išjungtas. Jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenys aplinkose pradedami sinchronizuoti tada, kai jie yra parengti. Kai jūsų aplinka paruošta sinchronizuoti duomenis, galite įjungti integravimą.

### <a name="dmfdixf-entities"></a>DMF / DIXF objektai

„Human Resources“, sukurta tos pačios platformos kaip ir „Finance and Operations“ programos pagrindu, teikia [duomenų tvarkymo sistemą (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). DMF taip pat žinomas kaip Duomenų importavimo / eksportavimo sistema (DIXF). „Human Resources” suteikia duomenų objektų, kuriuos galite naudoti norėdami importuoti ir eksportuoti „Human Resources” duomenis, rinkinį. Nors „Common Data Service“ objektai yra pageidaujama „Human Resources“ duomenų integravimo sąsaja, DMF objektai vis dar naudingi tam tikromis aplinkybėmis, pvz.:

- „Common Data Service“ objektai dar nepasiekiami.

- Integruojant reikia didelio našumo masinio duomenų importavimo / eksportavimo galimybių.

DMF objektai šiuo metu teikia Išsamiausių duomenų aprėptį „Human Resources“ duomenims.

DMF yra netinkama realiojo laiko integracijoms, pvz., kai reikia nedelsiant pateikti vartotojo atsiliepimų vartotojo sąsajoje. Paketinės operacijos yra suplanuotos paketinės užduotys ir dažnai turi mažiausiai 1–2 minučių gaištį, kol paketinė tarnyba pradeda užduoties vykdymą, bei importavimo / eksportavimo operacijai atlikti gali prireikti laiko tiek, kiek tai bus vykdoma.

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

DMF papildomai suteikia galingą funkciją (žinomą kaip [Savo duomenų bazės naudojimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)arba BYOD), kuri leidžia „Human Resources“ eksportuoti duomenis į savo „Microsoft Azure“ SQL duomenų bazę. Ši galimybė suteikia didžiulį dinamiškumą. Kai duomenys yra jūsų SQL duomenų bazėje, galite naudoti bet kurias programas arba tarpinę programinę įrangą, kurios gali jungtis prie SQL duomenų saugyklos.

BYOD dažniausiai yra tik skaityti skirtas sprendimas. Nors jūs galite manipuliuoti ir saugoti visus duomenis, kuriuos norite „Azure SQ“ duomenų bazėje (pvz., duomenų mišinius), duomenų, saugomų „Azure SQL“ duomenų bazėje, negalima sinchronizuoti į „Human Resources“.

BYOD tinka ataskaitoms apie sprendimus, duomenų integravimus, duomenų mišinius, kaip duomenų šaltinis, skirtas srautui [„Azure Data Factory“](https://docs.microsoft.com/azure/data-factory/).

> [!NOTE]
> BYOD nepasiekiamas programose „Attract“ ir „Onboard“.

### <a name="odata-enabled-entities"></a>„OData“ palaikomi objektai

Dauguma DMF objektų yra įgalinami prieigai per „Human Resources“ duomenų tarnybą („OData“). Pateikta [„Finance and Operations“ „OData“ tarnybos](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) dokumentacija taikoma „Human Resources“, išskyrus savo „OData“ rodomų objektų kūrimą.

Nors ir „Common Data Service“ ir „OData” diegimas, patekiamas „Common Data Service“ (per [„Dynamics 365“ žiniatinklio API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), yra pageidaujamas naudojant „Human Resources“ duomenų tarnybą, „Human Resources“ duomenų tarnyba šiuo metu turi didesnę objektų sudėties aprėptį, skirtą „Human Resources“ duomenims.

### <a name="excel-add-in"></a>„Excel“ priedas

Su [„Excel“ priedu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) galėsite plačiau naudoti „OData” palaikomus objektus. Jis suteikia patogų būdą galutiniam vartotojui gauti ir modifikuoti „Human Resources“ duomenis per pažįstamą „Excel“ vartotojo sąsają (UI).

„Excel“ papildinys tinkamas verslo srities ekspertams importuoti / eksportuoti ad hoc duomenis. Pasikartojančių duomenų integravimui, kuriam reikia programinės automatizacijos, kita integravimo technologija bus tinkamesnė.

### <a name="data-integrator"></a>Duomenų integratorius

Norėdami integruoti duomenis į ir iš „Common Data Service”, galite naudoti [tarnybą „Data Integrator“](https://docs.microsoft.com/powerapps/administrator/data-integrator). Tarnyba „Data Integrator“ leidžia apibrėžti integravimo projektus, dažnai pagrįstus iš anksto nustatytais šablonais, kuriuos programos kūrėjai pritaikė konkretiems integravimams. Integravimo projektus galite planuoti vykdyti automatiškai pasikartojančiu grafiku arba vykdyti rankiniu būdu.

„Data Integrator“ projektai yra tinkami „Common Data Service” paketų integravimams. Jie yra puikus pasirinkimas integravimams tarp „Dynamics 365“ programų šeimos. Pavyzdžiui, „Microsoft“ pateikia „Data Integrator“ šabloną, skirtą integruoti duomenis iš „Human Resources“ į „Dynamics 365 Finance“. Daugiau informacijos apie šabloną žr. [Integravimas iš „Dynamics 365 Human Resources” į „Dynamics 365 Finance”](hr-admin-integration-finance.md).

### <a name="power-query"></a>„Power Query“

„Data Integrator“ palaiko [„Power Query“](https://docs.microsoft.com/power-query/power-query-what-is-power-query) naudodamas savo [išplėstinės užklausos funkciją](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). „Power Query“ suteikia galingą, lankstų duomenų filtravimą ir transformavimą, įskaitant raiškiąją M formulės kalbą. „Power Query” jums gali būti pažįstama, jei esate kūrę „Power BI“ ataskaitas.

## <a name="deciding-on-an-integration-technology"></a>Integravimo technologijos pasirinkimas

Naudojant tiek daug skirtingų integravimo technologijų, sprendžiant, kurį integravimo metodą rinktis, kartais gali pasirodyti keblu. Kai „Common Data Service“ duomenų aprėptis auga, sprendimas tampa lengvesnis, nes dauguma atvejų „Common Data Service“ bus pageidaujama duomenų sąsaja. Tačiau iki tol jūs galite pastebėti, kad „Common Data Service“ dar negali patenkinti jūsų poreikių. Toliau pateikiamoje lentelėje pateikiama kelių pagrindinių integravimo technologijos parinkčių charakteristikų suvestinė.

| Technologija / Įrankis / API    | Pasikartojančios integracijos                   | Sinchroninė / asinchroninė                    | Programinė prieiga naudojant API        | Atitinkami duomenų tomai                                   | Duomenų aprėptis                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| „Common Data Service“ objektai           | Taip, naudojant duomenų integratorių arba tarpinę programinę įrangą | „Sync“, „Async“, „Batch“ (naudojant duomenų integratorių) | Taip, naudojant „Dynamics 365“ žiniatinklio API („OData“) | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Tobulinimas<sup>2</sup>                       |
| DMF objektai           | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip, naudojant DMF paketo REST API         | Didelis (šimtai tūkstančių įrašų)                    | Aukštas                                |
| DMF paketo REST API   | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip                                       | Didelis (šimtai tūkstančių įrašų)                    | API palaiko visus DMF objektus       |
| BYOD                   | Taip, suplanuota administratoriaus programoje „Human Resources“        | „Async“, „Batch“                                | Ne<sup>3</sup>                                    | Didelis (šimtai tūkstančių įrašų)                    | Palaiko visus DMF objektus           |
| „OData“ palaikomi objektai | Taip, naudojant tarpinę programinę įrangą                    | Sinchronizuoti                                        | Taip, naudojant „Human Resources“ duomenų tarnybą („OData“)  | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Aukštas                                |
| „Excel“ priedas           | Ne                                       | Sinchronizuoti                                        | Ne                                        | Vidutinis (dešimtys tūkstančių įrašų)                      | Palaiko visus „OData“ palaikomus objektus |
| Duomenų integratorius        | Taip, suplanuota duomenų Integratoriuje        | „Async“, „Batch“                                | Ne                                        | Skiriasi pagal naudojimo atvejį                                       | Palaiko visus „Common Data Service“ objektus           |

<sup>2</sup>„Microsoft“ daug investuoja, kad išplėstų „Common Data Service“ objektų duomenų aprėptį. Rekomenduojame naudoti „Common Data Service”, kai aprėptis yra prieinama. Šiuo metu „Common Data Service“ duomenų aprėptis yra maža, palyginus su DMF ir „OData“ palaikomais objektais.

<sup>3</sup>SQL duomenų bazė gali būti prieinama programiškai.
