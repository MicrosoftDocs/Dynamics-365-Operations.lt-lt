---
title: Duomenų integravimo technologijos pasirinkimas
description: Šioje temoje pateikiama informacija apie integravus personalo valdomus duomenis.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 98c1c56b445ae426103d19f96cbf1a77891221ef
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717145"
---
# <a name="choose-a-data-integration-technology"></a>Duomenų integravimo technologijos pasirinkimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šioje temoje pateikiama informacija, kaip integruoti su duomenimis, valdomais "Dynamics 365" personalo. Jame aprašomos įvairios integravimo technologijos, kad apsispręstumėte, kurios technologijos labiausiai atitinka jūsų poreikius.

## <a name="data-integration-background"></a>Duomenų integravimo fonas

Verslo duomenys yra pagrindinis turtas, dėl kurio jūsų įmonė yra unikali. Jūsų verslo duomenys labai vertingi. Galite naudoti ryšius tarp savo verslo duomenų, kad galėtumėte pagerinti savo organizacijos verslo procesus ir įžvalgas. Siekiame suteikti paprastą, saugią ir stabilią prieigą prie jūsų verslo duomenų, nepriklausomai nuo sistemos, kurioje jie yra.

Istoriniu požiūriu duomenų integravimas tarp kelių sistemų buvo sudėtingas. „Microsoft“ imasi veiksmų, kad būtų lengviau integruoti duomenis, ir sparčiai artėja šio tikslo link, kai jis realizuojamas pasitelkiant [„Dataverse“](/powerapps/maker/common-data-service/data-platform-intro).

Dėl „Human Resources“ programos „Dataverse“ tampa pageidaujama „Human Resources“ duomenų viešoji sąsaja. Ilgainiui mes tikimės, kad visi svarbiausi duomenys, valdomi „Human Resources“ programos, bus išstatyti „Dataverse“. Rekomenduojame „Dataverse“ kaip rinktinę technologiją daugeliui integravimo taikymų.

Mes suprantame, kad „Dataverse” dar gali būti ne visi jūsų programai reikalingi duomenys. Taip pat suprantame, kad jūsų projektų laiko planavimo juostai gali prireikti alternatyvių technologijų. Praneškite mums, kai „Dataverse” neatitinka jūsų integravimo poreikių.

## <a name="integration-technologies"></a>Integravimo technologijos

Tolesniuose skyriuose aprašomos įvairios duomenų integravimo technologijos, kurias galima naudoti su „Human Resources“.

### <a name="dataverse-tables"></a>„Dataverse“ lentelės

„Dataverse“ yra pageidaujama „Human Resources“ viešoji duomenų sąsaja. Ji atsirado iš „Dynamics 365” XRM platformos, kurią naudoja [„Dynamics 365 Customer Engagement”](/dynamics365/?panel=customer-engagement#pivot=business-apps) sprendimai.

„Dataverse“ suteikia platformą ir API duomenų lentelėms. Kai diegiate „Human Resources”, ji prijungiama prie „Dataverse” egzemplioriaus. „Human Resources” duomenų objektai įdiegiami tame „Dataverse” egzemplioriuje. Lentelės ir jų duomenys yra prieinami bet kuriai programai, kuri gali susijungti su „Dataverse“ elementu. „Human Resources“ sinchronizuoja duomenis į ir iš „Dataverse“ lentelių.

> [!NOTE]
> „Human Resources“ objektai atitinka „Dataverse“ lenteles. Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)

Kai duomenų lentelių prašo integruojanti programa ir jos yra „Dataverse“, galite iki galo naudoti [„Dataverse“ ir API, kurios ją palaiko](/powerapps/?panel=developer#pivot=home). Tarp palaikomų API yra [„Dynamics 365“ žiniatinklio API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), kuri pateikia prieigos prie „Dataverse“ duomenų „OData“ diegimą.

„Dataverse“ lentelės ir su jomis susijusios API yra geriausias sprendimas prieigai prie „Human Resources“ duomenų iš žiniatinklio programų, tinklo paslaugų/API ir kitų programų, kurios sujungia „OData“ srautus.

> [!NOTE]
> Kadangi sprendimas teikti „Dataverse“ pirmenybę kaip „Human Resources“ duomenų sąsajai priimtas gana neseniai, galite pastebėti, kad „Human Resources“ duomenų objektai, kuriuos reikia įtraukti į savo integraciją, dar nėra teikiami „Dataverse“.
> </br>
> Norėdami gauti „Human Resources“ objektų, pasiekiamų „Dataverse“ sąrašą, žr. [„Human Resources“ ir „Dataverse”](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Jei jūsų integracijai reikalingų „Human Resources“objektai dar nėra pasiekiami, turite palaukti, kol duomenų objektai bus prieinami, arba turite naudoti vieną iš toliau aprašytų integravimo technologijų.
> </br>
> Pagal numatytuosius parametrus naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Dataverse“ integravimas yra išjungtas. Jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenys aplinkose pradedami sinchronizuoti tada, kai jie yra parengti. Kai jūsų aplinka paruošta sinchronizuoti duomenis, galite įjungti integravimą.

### <a name="dmfdixf-entities"></a>DMF / DIXF objektai

Personalo valdymo sistema, sukurta toje pačioje platformoje kaip ir finansų ir operacijų programos, pateikia [duomenų valdymo sistemą (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF taip pat žinomas kaip Duomenų importavimo / eksportavimo sistema (DIXF). „Human Resources” suteikia duomenų objektų, kuriuos galite naudoti norėdami importuoti ir eksportuoti „Human Resources” duomenis, rinkinį. Kol „Dataverse“ lentelės yra rekomenduojama duomenų integravimo sąsaja „Human Resources“, DMF objektai vis dar naudingi kai kuriomis sąlygomis, tokiomis kaip:

- „Dataverse“ lentelės nėra dar prieinamos.

- Integruojant reikia didelio našumo masinio duomenų importavimo / eksportavimo galimybių.

> [!NOTE]
> „Human Resources“ objektai atitinka „Dataverse“ lenteles. Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)

DMF objektai šiuo metu pateikia pilniausią duomenų aprėptį „Human Resource“ duomenims.

DMF yra netinkama realiojo laiko integracijoms, pvz., kai reikia nedelsiant pateikti vartotojo atsiliepimų vartotojo sąsajoje. Paketinės operacijos yra suplanuotos paketinės užduotys ir dažnai turi mažiausiai 1–2 minučių gaištį, kol paketinė tarnyba pradeda užduoties vykdymą, bei importavimo / eksportavimo operacijai atlikti gali prireikti laiko tiek, kiek tai bus vykdoma.

DMF gali būti geriausia išeitis, kai reikalingas didelis pralaidumas (pvz., naktį suplanuotam daugiatūkstantinių įrašų importavimui / eksportavimui).

> [!NOTE]
> DMF nepasiekiamas programose „Attract“ ir „Onboard“.

### <a name="dmf-package-rest-api"></a>DMF paketo REST API

DMF teikia [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api)manipuliuoti duomenų paketus. Šis API gali būti naudojamas programiškai sąveikauti su DMF, tad galima atlikti tokius veiksmus:

- Importuoti duomenų paketą.

- Eksportuoti duomenų paketą.

- Tikrinti importavimo / eksportavimo operacijos būsena.

DMF paketas REST API yra visiškai palaikomas „Human Resource“.

### <a name="azure-sql-db-byod"></a>„Azure SQL“ DB (BYOD)

DMF papildomai suteikia galingą funkciją (žinomą kaip [Savo duomenų bazės naudojimas](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)arba BYOD), kuri leidžia „Human Resources“ eksportuoti duomenis į savo „Microsoft Azure“ SQL duomenų bazę. Ši galimybė suteikia didžiulį dinamiškumą. Kai duomenys yra jūsų SQL duomenų bazėje, galite naudoti bet kurias programas arba tarpinę programinę įrangą, kurios gali jungtis prie SQL duomenų saugyklos.

BYOD dažniausiai yra tik skaityti skirtas sprendimas. Nors jūs galite manipuliuoti ir saugoti visus duomenis, kuriuos norite „Azure SQ“ duomenų bazėje (pvz., duomenų mišinius), duomenų, saugomų „Azure SQL“ duomenų bazėje, negalima sinchronizuoti į „Human Resources“.

BYOD tinka ataskaitoms apie sprendimus, duomenų integravimus, duomenų mišinius, kaip duomenų šaltinis, skirtas srautui [„Azure Data Factory“](/azure/data-factory/).

> [!NOTE]
> BYOD nepasiekiamas programose „Attract“ ir „Onboard“.

### <a name="odata-enabled-entities"></a>„OData“ palaikomi objektai

Dauguma DMF objektų yra įgalinami prieigai per „Human Resources“ duomenų tarnybą („OData“). Dokumentai, pateikti finansų ir [operacijų OData](/dynamics365/unified-operations/dev-itpro/data-entities/odata) tarnybai, taikomi Personalo tarnybai, išskyrus tai, kaip kurti savo OData rodyti objektus.

Nors ir „Dataverse“ ir „OData” diegimas, pateikiamas „Dataverse“ (per [„Dynamics 365“ žiniatinklio API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))), yra pageidaujamas naudojant „Human Resources“ duomenų tarnybą, „Human Resources“ duomenų tarnyba šiuo metu turi didesnę objektų sudėties aprėptį, skirtą „Human Resources“ duomenims.

### <a name="excel-add-in"></a>„Excel“ priedas

Su [„Excel“ priedu](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) galėsite plačiau naudoti „OData” palaikomus objektus. Jis suteikia patogų būdą galutiniam vartotojui gauti ir modifikuoti „Human Resources“ duomenis per pažįstamą „Excel“ vartotojo sąsają (UI).

„Excel“ papildinys tinkamas verslo srities ekspertams importuoti / eksportuoti ad hoc duomenis. Pasikartojančių duomenų integravimui, kuriam reikia programinės automatizacijos, kita integravimo technologija bus tinkamesnė.

### <a name="data-integrator"></a>Duomenų integratorius

Norėdami integruoti duomenis į ir iš „Dataverse”, galite naudoti [tarnybą „Data Integrator“](/powerapps/administrator/data-integrator). Tarnyba „Data Integrator“ leidžia apibrėžti integravimo projektus, dažnai pagrįstus iš anksto nustatytais šablonais, kuriuos programos kūrėjai pritaikė konkretiems integravimams. Integravimo projektus galite planuoti vykdyti automatiškai pasikartojančiu grafiku arba vykdyti rankiniu būdu.

„Data Integrator“ projektai yra tinkami „Dataverse” paketų integravimams. Jie yra puikus pasirinkimas integravimams tarp „Dynamics 365“ programų šeimos. Pavyzdžiui, Microsoft pateikia duomenų integratoriaus šabloną, leidžiaį integruoti duomenis iš personalo į Dynamics 365 finansus. Daugiau informacijos apie integravimo šabloną galite sužinoti iš [" Dynamics 365 Human Resources Dynamics 365 Finance"](hr-admin-integration-finance.md).

### <a name="power-query"></a>„Power Query“

Duomenų integratorius palaiko per [Power Query](/power-query/power-query-what-is-power-query) išplėstinės [užklausos funkciją](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query suteikia galinga, lanksti duomenų filtravimą ir transformaciją, įskaitant raiškiojo M formulės kalbą. Power Query tikriausiai bus žinoma, jei sukūrėte Power BI ataskaitas.

## <a name="deciding-on-an-integration-technology"></a>Integravimo technologijos pasirinkimas

Naudojant tiek daug skirtingų integravimo technologijų, sprendžiant, kurį integravimo metodą rinktis, kartais gali pasirodyti keblu. Kai „Dataverse“ duomenų aprėptis auga, sprendimas tampa lengvesnis, nes dauguma atvejų „Dataverse“ bus pageidaujama duomenų sąsaja. Tačiau iki tol jūs galite pastebėti, kad „Dataverse“ dar negali patenkinti jūsų poreikių. Toliau pateikiamoje lentelėje pateikiama kelių pagrindinių integravimo technologijos parinkčių charakteristikų suvestinė.

| Technologija / Įrankis / API    | Pasikartojančios integracijos                   | Sinchroninė / asinchroninė                    | Programinė prieiga naudojant API        | Atitinkami duomenų tomai                                   | Duomenų aprėptis                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| „Dataverse“ lentelės           | Taip, naudojant duomenų integratorių arba tarpinę programinę įrangą | „Sync“, „Async“, „Batch“ (naudojant duomenų integratorių) | Taip, naudojant „Dynamics 365“ žiniatinklio API („OData“) | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Tobulinimas<sup>2</sup>                       |
| DMF objektai           | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip, naudojant DMF paketo REST API         | Didelis (šimtai tūkstančių įrašų)                    | Aukštas                                |
| DMF paketo REST API   | Taip, suplanuota naudojant tarpinę programinę įrangą        | „Async“, „Batch“                                | Taip                                       | Didelis (šimtai tūkstančių įrašų)                    | API palaiko visus DMF objektus       |
| BYOD                   | Taip, suplanuota administratoriaus programoje „Human Resources“        | „Async“, „Batch“                                | Ne<sup>3</sup>                                    | Didelis (šimtai tūkstančių įrašų)                    | Palaiko visus DMF objektus           |
| „OData“ palaikomi objektai | Taip, naudojant tarpinę programinę įrangą                    | Sinchronizuoti                                        | Taip, naudojant „Human Resources“ duomenų tarnybą („OData“)  | Skiriasi pagal naudojimo atvejį (palaikomos puslapių kaitos interaktyviajam naudojimui) | Aukštas                                |
| „Excel“ priedas           | Ne                                       | Sinchronizuoti                                        | Ne                                        | Vidutinis (dešimtys tūkstančių įrašų)                      | Palaiko visus „OData“ palaikomus objektus |
| Duomenų integratorius        | Taip, suplanuota duomenų Integratoriuje        | „Async“, „Batch“                                | Ne                                        | Skiriasi pagal naudojimo atvejį                                       | Palaiko visas „Dataverse“ lenteles           |

<sup>2</sup>„Microsoft“ daug investuoja į didėjančią duomenų aprėptį „Dataverse“ lentelėms. Rekomenduojame naudoti „Dataverse”, kai aprėptis yra prieinama. Šiuo metu „Dataverse“ duomenų aprėptis yra maža, palyginus su DMF ir „OData“ palaikomais objektais.

<sup>3</sup>SQL duomenų bazė gali būti prieinama programiškai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
