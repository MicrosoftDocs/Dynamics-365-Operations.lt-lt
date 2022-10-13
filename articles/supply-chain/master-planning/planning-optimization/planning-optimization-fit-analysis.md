---
title: Planavimo optimizavimo tinkamumo analizė
description: Šiame straipsnyje paaiškinama, kaip patikrinti dabartinį nustatymą ir duomenis pagal planavimo optimizavimo funkcijų galimybes.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c160a6477dd41fac0f15f57bb0f46def500f4589
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643746"
---
# <a name="planning-optimization-fit-analysis"></a>Planavimo optimizavimo tinkamumo analizė

[!include [banner](../../includes/banner.md)]

Kaip perkėlimo proceso dalį turite analizuoti planavimo optimizavimo tinkamumo analizės rezultatą. Atkreipkite dėmesį, kad planavimo optimizavimo aprėptis nesutampa su dabartine integruota bendrojo planavimo funkcija. Ruošiantis perkėlimui, rekomenduojame tai aptarti kartu su partneriu ir perskaityti dokumentus. 

Planavimo optimizavimo tinkamumo analizė padeda nustatyti atvejus, kai integruotos bendrojo planavimo funkcijos ir „Planning Optimization“ rezultatas gali skirtis. Ši analizė atliekama remiantis dabartine jūsų sąranka ir duomenimis. 

Norėdami peržiūrėti planavimo optimizavimo tinkamumo analizės rezultatą, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo tinkamumo analizė** ir pasirinkite **Atlikti analizę**. Jei atlikus analizę randama neatitikimų, jie pateikiami tame pačiame puslapyje. (Analizė gali užtrukti kelias minutes.)

> [!NOTE]
>
> - Kai kurių nenuoseklumų negalima nustatyti „Planning Optimization“ pritaikymo analizėje. Dėl daugiau informacijos, žr. [Skirtumas tarp įtaisytojo bendrojo planavimo ir „Planning Optimization“](planning-optimization-differences-with-built-in.md).
>
> - Jei randama neatitikimų, vis tiek galite naudoti „Planning Optimization“ funkciją. Tinkamumo analizės rezultatai rodo tik tas vietas, kuriose planavimo paslauga neatsižvelgs į dabartinę sąranką. Kitaip tariant, rodomos vietos, kuriose gali būti nepaisoma kai kurių procesų arba jie gali būti nepalaikomi.

## <a name="analysis-results-example-1"></a>Analizės rezultatai: 1 pavyzdys

- **Funkcija:** gamyba
- **Problema:** prekės, kurių KS lygis didesnis nei nulis: 56
- **Paaiškinimas:** tinkamumo analizė rado 56 prekes, kurios turi KS nustatymus gamybai. Kadangi dabartinė „Planning Optimization“ versija nepalaiko gamybos, „Planning Optimization“ sugeneruos suplanuotus pirkimo užsakymus, ne suplanuotus gamybos užsakymus. Taip pat bus rodomas įspėjimas, kuriame išvardijamos paveiktos prekės.

## <a name="analysis-results-example-2"></a>Analizės rezultatai: 2 pavyzdys

- **Funkcija:** veiksmai
- **Išdavimas:** padengimo grupės su įjungtu veiksmų skaičiavimu: 6
- **Paaiškinimas:** tinkamumo analizė rado šešias padengimo grupes, kuriose veiksmų skaičiavimas įjungtas. Kadangi dabartinė „Planning Optimization“ versija nepalaiko veiksmų, bendrojo planavimo metu jokie veiksmai nebus generuojami.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Galimų tinkamumo analizės rezultatų peržiūra

Tolesnėje lentelėje pateikiami skirtingi rezultatai, rodomi po tinkamumo analizės. Skaičių ženklai (*\#*) bus pakeisti skaičiumi, nurodančiu įrašų, kuriuose yra nurodyta problema, skaičių.

> [!IMPORTANT]
> Dar nepalaikomų priemonių atveju toliau pateikiamoje lentelėje pateikiama tikėtina pasiekiamumo informacija, kuri įvertinta pagal dabartinę sistemos programą. Šie įvertinimai gali būti pakeisti iš anksto neįrašant.

| Funkcija | Nurodyta problema | Paaiškinimas | Numatomas prieinamumas |
| --- | --- | --- | --- |
| Veiksmai | Padengimo grupės su veiksmų skaičiavimu įjungtos: *\#* | Dabar ši funkcija yra palaikoma. | Palaikoma |
| Pagrindiniai kalendoriai | Kalendoriai, naudojantys pagrindinį kalendorių: *\#* | Dabar ši funkcija yra palaikoma. | Palaikoma | 
| Paketo perdavimo kodai | Neaktyvaus pagrindinio paketo perdavimas:*\#* | Ši funkcija laukia patvirtinimo. Šiuo metu paketo perdavimo kodai nepaisomi, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 <!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> |
| Galimos pateikti atsargos (CTP) | Numatytieji užsakymo parametrai su pristatymo datos valdymu, nustatytu į CTP: *\#* | Tiekimo grandinės valdymo 10.0.28 ir naujesnio proceso, kuris vadinamas CTP *planavimo optimizavimui,* leidžia patvirtinti siuntimo ir gavimo datas po dinaminio plano vykdymo. Senesnių tiekimo grandinės valdymo versijų senesnio CTP parametro nepaisoma, kai įgalintas planavimo optimizavimas. | Palaikoma |
| Kopijuoti statinį į dinaminį planą | Kopijavimas statinio į dinaminį planą yra įjungtas bendrojo planavimo parametruose. | Planavimo optimizavimas nekopijuoja statinio plano į dinaminį planą, neatsižvelgiant į šį parametrą. Paprastai ši koncepcija yra mažiau aktuali dėl planavimo optimizavimo teikiamo greičio ir visiško regeneravimo. Jei naudojami du ar daugiau planų, turėtų būti suaktyvintas kiekvieno plano bendrasis planavimas. | Netaikoma |
| Patvirtinimas | Padengimo grupės su nustatyta automatinio patvirtinimo laiko riba:*\#* | 10.0.7 ar vėlesnėje versijoje patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija *Automatinis planavimo optimizavimo patvirtinimas*). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| Patvirtinimas | Prekės padengimo įrašai su nustatytu automatiniu patvirtinimu: *\#* | 10.0.7 ar vėlesnėje versijoje automatinis patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija *Automatinis planavimo optimizavimo patvirtinimas*). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| Patvirtinimas | Bendrieji planai su nustatytu automatiniu patvirtinimu: *\#* | 10.0.7 ar vėlesnėje versijoje automatinis patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija *Automatinis planavimo optimizavimo patvirtinimas*). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| FitAnalysisPlanningItems | Planuojamos prekės: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu planuojamos prekės yra tvarkomos kaip įprastos prekės, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 arba naujesnė versija |
| Prognozė | Padengimo grupės su įjungta funkcija „Įtraukti vidinės įmonės užsakymus”: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Vidinės įmonės planavimas](Intercompany-planning.md) | Palaikoma |
| Prognozė | Padengimo grupės, kurių parametras „Prognozę sumažina” nustatytas į reikšmę, kuri skiriasi nuo reikšmės „Užsakymai”: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Bendrasis planavimas su poreikio prognozėmis](demand-forecast.md) | Palaikoma |
| Prognozė | Prognozės modeliai su antriniais modeliais: *\#* |  Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Bendrasis planavimas su poreikio prognozėmis](demand-forecast.md) | Palaikoma |
| Prognozė | Bendrieji planai su įjungta funkcija „Įtraukti tiekimo prognozę”: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu tiekimo prognozės nepalaikomos, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2022 išleidimo banga 2 arba naujesnė versija |
| Blokavimo laiko ribos | Padengimo grupės su nustatyta blokavimo laiko riba:*\#* | Ši funkcija laukia patvirtinimo. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Blokavimo laiko ribos | Prekių aprėpties įrašai su nustatyta blokavimo laiko riba:*\#* | Ši funkcija laukia patvirtinimo. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Blokavimo laiko ribos | Bendrieji planai su nustatyta blokavimo laiko riba:*\#* | Ši funkcija laukia patvirtinimo. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Vidinė įmonė | Bendrieji planai, įskaitant proceso pabaigoje suplanuotą poreikį: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Vidinės įmonės planavimas](Intercompany-planning.md) | Palaikoma |
| Kanban | Prekės padengimo įrašai su suplanuoto užsakymo tipu „kanban“: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu prekės padengimo, nustatyto į „kanban”, bus nepaisoma, kai įjungtas planavimo optimizavimas. Suplanuoto užsakymo tipas „kanban” bendrojo planavimo metu sukurs įspėjimą, o suplanuoti pirkimo užsakymai bus sukurti padengti susijusį poreikį. | Būsima banga |
| Kanban | Prekės su numatytojo užsakymo tipo „kanban“: *\#* | Šiuo metu numatytojo užsakymo tipo, nustatyto į „kanban”, bus nepaisoma, kai įjungtas planavimo optimizavimas. Numatytojo užsakymo tipas „kanban” bendrojo planavimo metu sukurs įspėjimą, o suplanuoti pirkimo užsakymai bus sukurti padengti susijusį poreikį. | Būsima banga |
| Produkto ciklo būsena | Produkto ciklo būsenos nesuaktyvintos planavimui: *\#* | Dabar ši funkcija yra palaikoma. Papildomos informacijos rasite [Neįtraukti produktų, turinčių konkrečias produkto ciklo būsenas](product-lifecycle-state.md) | Palaikoma |
| Gamyba | KS eilutės su apvalinimu arba keliais nustatymais: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu KS eilutėse esančio apvalinimo ir kelių nustatymų nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Būsima banga|
| Gamyba | KS / formulės eilutės su formulės matavimo vienetu: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilutėse esančio formulės matavimo vieneto nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Gamyba | KS / formulės eilutės su prekės pakeitimu (plano grupės): *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilutėse esančio prekės pakeitimo (planavimo grupių) nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Gamyba | KS / formulės eilutės su neigiamu kiekiu: *\#* | Ši funkcija laukia patvirtinimo. KS ir formulės eilutės, kuriose yra neigiamas kiekis, bus įtrauktos su kiekiu, lygiu 0 (nuliui), ir bus pateiktas įspėjimas, kai įjungtas planavimo optimizavimas. Atnaujinti bendruosius duomenis, kad būtų išvengta įspėjimų. | 2022 išleidimo banga 2 |
| Gamyba | KS / formulės eilutės su išteklių sąnaudomis: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilučių, kuriose yra išteklių sąnaudos, nepaisoma, kai įjungtas planavimo optimizavimas. Kai ši funkcija palaikoma, medžiagų reikalavimas bus nustatytas kaip gamybos pradžios data. Kol ši funkcija bus palaikoma, nebus sugeneruoti medžiagų, pažymėtų išteklių suvartojimo vėliavėle, reikalavimai. | 2022 išleidimo banga 2 |
| Gamyba | KS / formulės eilutės su žingsnių sąnaudomis: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilučių, kuriose yra žingsnių sąnaudos, nepaisoma, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 |
| Gamyba | KS su apibrėžtu nuolatiniu arba kintamu nurašymu: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu nuolatinio arba kintamo nurašymo, apibrėžto KS, nepaisoma, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 |
| Gamyba | KS su subranga: *\#* | Dabar ši funkcija yra palaikoma. | Palaikoma |
| Gamyba | KS be svetainės: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Gamybos planavimas](production-planning.md) | Palaikoma |
| Gamyba | Poreikis su apibrėžtomis konkrečiomis KS ar maršruto reikalavimais: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu konkrečių KS ar maršruto reikalavimų, apibrėžtų pagal poreikį (pvz., KS arba maršrutas pardavimo užsakyme), nepaisoma, kai įjungtas planavimo optimizavimas. Bus naudojama standartinė KS arba maršrutas, neatsižvelgiant į šį nustatymą. | 2022 išleidimo banga 2 |
| Gamyba | Formulės versijos su sudėtiniai / šalutiniais produktais: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu sudėtinių ir šalutinių produktų, susietų su formulės versija, nepaisoma, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 |
| Gamyba | Formulės versijos su išeiga: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu išeigos, susietos su formulės versija, nepaisoma, kai įjungtas planavimo optimizavimas. | 2022 išleidimo banga 2 |
| Gamyba | Planai su sekomis: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu sekos nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2022 išleidimo banga 2 |
| Gamyba | Paleisti gamybos užsakymai, kurie nepradėti, buvo suplanuoti pradėti anksčiau nei šiandien: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu, jei gamybos užsakymas vėluoja, bendrojo planavimo metu bus laikoma, kad jis bus baigtas šiandien. Tai aktualu išleistiems gamybos užsakymais, kurių pristatymo data yra praėjusi, tačiau užsakymai dar nėra baigti. | Būsima banga |
| Gamyba | Ištekliai numatyti esant ribotai talpai: *\#* | Dabar ši funkcija yra palaikoma.| Palaikoma |
| Gamyba | Maršrutai, naudojami planuojant: *\#* | Ši funkcija palaikoma. | Palaikoma |
| Gamyba | Pardavimo linijos rezervavimas naudojant išskleidimą: *\#* | Pardavimo eilutės rezervavimas, naudojantis išskleidimą, nepalaikomas, kai įjungtas planavimo optimizavimas. | Būsima banga |
| Gamyba | Planavimas išskleidžiant gamybos užsakymus: *\#* | Planavimas, naudojantis gamybos užsakymų išskleidimą, nepalaikomas, kai įjungtas planavimo optimizavimas. Gamybos užsakymai gali būti suplanuoti atskirai. | Būsima banga |
| Pasiūlymo patvirtinimai | Bendrieji planai su įgalintu pasiūlymo patvirtinimu: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu pasiūlymo patvirtinimai (RFQ) nėra laikomi poreikiu, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2022 išleidimo banga 2 |
| Paraiškos | Bendrieji planai su įgalintomis paraiškomis: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Pirkimo paraiškos](purchase-requisitions.md) | Palaikoma |
| Laiko rezervai | Padengimo grupės su laiko rezervu:*\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Laiko rezervai](safety-margins.md) | Palaikoma |
| Laiko rezervai | Bendrieji planai su laiko rezervu: *\#* | Dabar ši funkcija yra palaikoma. Papildomą informaciją rasite [Laiko rezervai](safety-margins.md) |  Palaikoma |
| Saugos atsargų pildymas | Prekės padengimo įrašai, kurių parametras „Išpildyti minimumą” skiriasi nuo „Šiandienos data + įsigijimo laikas”: *\#* | Planavimo optimizavimas visada naudoja *Šiandienos data + įsigijimo laikas*. Šis pakeitimas sukurtas pasirengti supaprastintam planavimo nustatymui ateityje ir pateikti įgyvendinamą rezultatą. Jei įsigijimo laikas neįtrauktas į pakankamas atsargas, suplanuoti užsakymai, sukurti dabartinėms mažoms turimoms atsargos, visada bus atidėti dėl gamybos laiko. Tai gali sukelti daug triukšmo ir nepageidaujamų suplanuotų užsakymų. Geriausia yra pakeisti parametrą, kad būtų naudojama *Šiandienos data + įsigijimo laikas*. Atnaujinti bendruosius duomenis, kad būtų išvengta įspėjimų. | Netaikoma |
| Pardavimo pasiūlymai | Bendrieji planai su įgalintais pardavimo pasiūlymais: *\#* | Ši funkcija laukia patvirtinimo. Šiuo metu į pasiūlymus neatsižvelgiama, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2022 išleidimo banga 2 arba naujesnė versija |
| Laikymo trukmė | Bendrieji planai su įgalinta laikymo trukme: *\#* | Dabar ši funkcija yra palaikoma. | Palaikoma |

## <a name="additional-resources"></a>Papildomi ištekliai

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Darbo su planavimo optimizavimu pradžia](get-started.md)

[Skirtumas tarp įtaisytojo bendrojo planavimo ir „Planning Optimization“](planning-optimization-differences-with-built-in.md)

[Planavimo optimizavimo nenaudojami parametrai](not-used-parameters.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
