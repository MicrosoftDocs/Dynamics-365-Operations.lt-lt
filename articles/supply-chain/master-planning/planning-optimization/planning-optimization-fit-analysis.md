---
title: Planavimo optimizavimo tinkamumo analizė
description: Šioje temoje paaiškinama, kaip patikrinti dabartinę sąranką ir duomenis, atsižvelgiant į „Planning Optimization“ funkcijos galimybes.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 04605370cbcc7b8c13552ae7f999212a1efabfab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967075"
---
# <a name="planning-optimization-fit-analysis"></a>Planavimo optimizavimo tinkamumo analizė

[!include [banner](../../includes/banner.md)]

Kaip perkėlimo proceso dalį turite analizuoti planavimo optimizavimo tinkamumo analizės rezultatą. Atkreipkite dėmesį, kad planavimo optimizavimo aprėptis nesutampa su dabartine integruota bendrojo planavimo funkcija. Ruošiantis perkėlimui, rekomenduojame tai aptarti kartu su partneriu ir perskaityti dokumentus. 

Planavimo optimizavimo tinkamumo analizė padeda nustatyti atvejus, kai integruotos bendrojo planavimo funkcijos ir „Planning Optimization“ rezultatas gali skirtis. Ši analizė atliekama remiantis dabartine jūsų sąranka ir duomenimis. 

Norėdami peržiūrėti planavimo optimizavimo tinkamumo analizės rezultatą, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo tinkamumo analizė** ir pasirinkite **Atlikti analizę**. Jei atlikus analizę randama neatitikimų, jie pateikiami tame pačiame puslapyje. (Analizė gali užtrukti kelias minutes.)

> [!NOTE]
> Jei randama neatitikimų, vis tiek galite naudoti „Planning Optimization“ funkciją. Tinkamumo analizės rezultatai rodo tik tas vietas, kuriose planavimo paslauga neatsižvelgs į dabartinę sąranką. Kitaip tariant, rodomos vietos, kuriose gali būti nepaisoma kai kurių procesų arba jie gali būti nepalaikomi.

## <a name="analysis-results-example-1"></a>Analizės rezultatai: 1 pavyzdys

- **Funkcija:** gamyba
- **Problema:** prekės, kurių KS lygis didesnis nei nulis: 56
- **Paaiškinimas:** tinkamumo analizė rado 56 prekes, kurios turi KS nustatymus gamybai. Kadangi dabartinė „Planning Optimization“ versija nepalaiko gamybos, „Planning Optimization“ sugeneruos suplanuotus pirkimo užsakymus, ne suplanuotus gamybos užsakymus. Taip pat bus rodomas įspėjimas, kuriame išvardijamos paveiktos prekės.

## <a name="analysis-results-example-2"></a>Analizės rezultatai: 2 pavyzdys

- **Funkcija:** veiksmai
- **Išdavimas:** padengimo grupės su įjungtu veiksmų skaičiavimu: 6
- **Paaiškinimas:** tinkamumo analizė rado šešias padengimo grupes, kuriose veiksmų skaičiavimas įjungtas. Kadangi dabartinė „Planning Optimization“ versija nepalaiko veiksmų, bendrojo planavimo metu jokie veiksmai nebus generuojami.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Galimų tinkamumo analizės rezultatų peržiūra

Tolesnėje lentelėje pateikiami skirtingi rezultatai, rodomi po tinkamumo analizės. Skaičių ženklai (_\#_) bus pakeisti skaičiumi, nurodančiu įrašų, kuriuose yra nurodyta problema, skaičių. Palaikomos arba peržiūrimos funkcijos yra prieinamos 10.0.9 arba naujesnėje versijoje (nebent stulpelyje „Numatomas pasiekiamumas” yra nurodytas didesnis versijos numeris).

| Funkcija | Nurodyta problema | Paaiškinimas | Numatomas prieinamumas |
| --- | --- | --- | --- |
| Veiksmai | Padengimo grupės su įjungtu veiksmų skaičiavimu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu atliekant bendrąjį planavimą veiksmai negeneruojami, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. Pagrindinis veiksmų tikslas yra siūlyti pakeitimus esamiems užsakymams. Įvertinkite, ar veiksmai yra aktyviai taikomi kaip jūsų verslo procesų dalis, arba, jei vėlavimo informacijos, susijusios su užsakymais, pakanka. | 2021 spalio mėn. |
| Pagrindiniai kalendoriai | Kalendoriai, naudojantys pagrindinį kalendorių: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu pagrindinio kalendoriaus nepaisoma, kai įjungtas planavimo optimizavimas. Įvertinkite, ar jūsų verslo procesams yra reikalingas pagrindinis kalendorius, ar pakanka tiesiogiai sukonfigūruoti kalendorių. | 2021 m. balandžio mėn. | 
| Paketo perdavimo kodai | Neaktyvaus pagrindinio paketo perdavimas: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu paketų perdavimo kodai nepaisomi, kai įjungtas planavimo optimizavimas. | 2021 m. spalio mėn. |
| Galimos pateikti atsargos (CTP) | Numatytieji užsakymo parametrai su pristatymo datos valdymu, nustatytu į CTP: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu CTP nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |
| Kopijuoti statinį į dinaminį planą | Kopijavimas statinio į dinaminį planą yra įjungtas bendrojo planavimo parametruose. | Planavimo optimizavimas nekopijuoja statinio plano į dinaminį planą, neatsižvelgiant į šį parametrą. Paprastai ši koncepcija yra mažiau aktuali dėl planavimo optimizavimo teikiamo greičio ir visiško regeneravimo. Jei naudojami du ar daugiau planų, turėtų būti suaktyvintas kiekvieno plano bendrasis planavimas. | Spalio 2021 d. |
| Patvirtinimas | Padengimo grupės su nustatyta automatinio patvirtinimo laiko riba: _\#_ | 10.0.7 ar vėlesnėje versijoje patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija _Automatinis planavimo optimizavimo patvirtinimas_). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| Patvirtinimas | Prekės padengimo įrašai su nustatytu automatiniu patvirtinimu: _\#_ | 10.0.7 ar vėlesnėje versijoje automatinis patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija _Automatinis planavimo optimizavimo patvirtinimas_). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| Patvirtinimas | Bendrieji planai su nustatytu automatiniu patvirtinimu: _\#_ | 10.0.7 ar vėlesnėje versijoje automatinis patvirtinimas palaikomas kaip atskira patvirtinimo paketinė užduotis po to, kai bendrasis planavimas yra baigtas (jei [funkcijų valdyme](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjungta funkcija _Automatinis planavimo optimizavimo patvirtinimas_). Atkreipkite dėmesį, kad automatinis planavimo optimizavimo patvirtinimas yra pagrįstas užsakymo data (pradžios data), o ne poreikio data (pabaigos data). Taip užtikrinama, kad suplanuotų užsakymų patvirtinimas įvyktų laiku, tačiau į patvirtinimo laiko ribą nereikia įterpti gamybos laiko. | Palaikoma |
| FitAnalysisPlanningItems | Planuojamos prekės: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu planuojamos prekės yra tvarkomos kaip įprastos prekės, kai įjungtas planavimo optimizavimas. | Spalio 2021 d. |
| Prognozė | Padengimo grupės su įjungta funkcija „Įtraukti vidinės įmonės užsakymus”: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu į bendrąjį planavimą neįtraukiamas proceso pabaigos suplanuotas poreikis, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. Atkreipkite dėmesį, kad išleisti / patvirtinti užsakymai vis dar veikia su įprastomis vidinės įmonės funkcijomis ir apima daugelį scenarijų. | Peržiūros režimu |
| Prognozė | Padengimo grupės, kurių parametras „Prognozę sumažina” nustatytas į reikšmę, kuri skiriasi nuo reikšmės „Užsakymai”: _\#_ | Pagal numatytuosius parametrus planavimo optimizavimas naudoja parametrą „Prognozę sumažina” užsakymams, neatsižvelgiant į šį nustatymą. | Palaikoma |
| Prognozė | Prognozės modeliai su antriniais modeliais: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu prognozės, naudojančios antrinius modelius, nepalaikomos, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2021 m. balandžio mėn. |
| Prognozė | Bendrieji planai su įjungta funkcija „Įtraukti tiekimo prognozę”: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu tiekimo prognozės nepalaikomos, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | Spalio 2021 d. |
| Blokavimo laiko ribos | Padengimo grupės su nustatyta blokavimo laiko riba: _\#_ | Blokavimo laiko riba nėra dažnai naudojama, o šiuo metu nėra planų, į kuriuos būtų galima ją įtraukti planavimo optimizavimui. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Netaikoma |
| Blokavimo laiko ribos | Prekių aprėpties įrašai su nustatyta blokavimo laiko riba: _\#_ | Blokavimo laiko riba nėra dažnai naudojama, o šiuo metu nėra planų, į kuriuos būtų galima ją įtraukti planavimo optimizavimui. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Netaikoma |
| Blokavimo laiko ribos | Bendrieji planai su nustatyta blokavimo laiko riba: _\#_ | Blokavimo laiko riba nėra dažnai naudojama, o šiuo metu nėra planų, į kuriuos būtų galima ją įtraukti planavimo optimizavimui. Šiuo metu blokavimo laiko ribos nustatymo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Netaikoma |
| Vidinė įmonė | Bendrieji planai, įskaitant proceso pabaigoje suplanuotą poreikį: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu į bendrąjį planavimą neįtraukiamas proceso pabaigos suplanuotas poreikis, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. Atkreipkite dėmesį, kad išleisti/patvirtinti užsakymai vis dar veikia su įprastomis vidinės įmonės funkcijomis ir apima daugelį scenarijų. | Peržiūros režimu |
| Kanban | Prekės padengimo įrašai su suplanuoto užsakymo tipu „kanban“: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu prekės padengimo, nustatyto į „kanban”, bus nepaisoma, kai įjungtas planavimo optimizavimas. Suplanuoto užsakymo tipas „kanban” bendrojo planavimo metu sukurs įspėjimą, o suplanuoti pirkimo užsakymai bus sukurti padengti susijusį poreikį. | Spalio 2021 d. |
| Kanban | Prekės su numatytojo užsakymo tipu „kanban“: _\#_ | Šiuo metu numatytojo užsakymo tipo, nustatyto į „kanban”, bus nepaisoma, kai įjungtas planavimo optimizavimas. Numatytojo užsakymo tipas „kanban” bendrojo planavimo metu sukurs įspėjimą, o suplanuoti pirkimo užsakymai bus sukurti padengti susijusį poreikį. | Spalio 2021 d. |
| Produkto ciklo būsena   | Produkto ciklų būsenos nesuaktyvintos planavimui: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu produkto ciklo būsenos nepaisoma, kai įjungtas planavimo optimizavimas. Galite koreguoti plano lygio produkto filtrą, kad nereikėtų įtraukti produktų, kuriuose išjungta planavimo produkto ciklo būsena. | Palaikoma |
| Gamyba | KS eilutės su apvalinimu arba keliais nustatymais: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS eilutėse esančio apvalinimo ir kelių nustatymų nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | 2021 m. balandžio mėn. |
| Gamyba | KS / formulės eilutės su formulės matavimo vienetu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilutėse esančio formulės matavimo vieneto nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |
| Gamyba | KS / formulės eilutės su prekės pakeitimu (planavimo grupės): _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilutėse esančio prekės pakeitimo (planavimo grupių) nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |
| Gamyba | KS / formulės eilutės su neigiamu kiekiu: _\#_ | Ši funkcija laukia patvirtinimo. KS ir formulės eilutės, kuriose yra neigiamas kiekis, bus įtrauktos su kiekiu, lygiu 0 (nuliui), ir bus pateiktas įspėjimas, kai įjungtas planavimo optimizavimas. Atnaujinti bendruosius duomenis, kad būtų išvengta įspėjimų. | 2021 spalio mėn. |
| Gamyba | KS / formulės eilutės su išteklių sąnaudomis: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilučių, kuriose yra išteklių sąnaudos, nepaisoma, kai įjungtas planavimo optimizavimas. Kai ši funkcija palaikoma, medžiagų reikalavimas bus nustatytas kaip gamybos pradžios data. Kol ši funkcija bus palaikoma, nebus sugeneruoti medžiagų, pažymėtų išteklių suvartojimo vėliavėle, reikalavimai. | 2021 m. balandžio mėn. |
| Gamyba | KS / formulės eilutės su žingsnių sąnaudomis: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS ir formulės eilučių, kuriose yra žingsnių sąnaudos, nepaisoma, kai įjungtas planavimo optimizavimas. | Spalio 2021 d. |
| Gamyba | KS su apibrėžtu nuolatiniu arba kintamu nurašymu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu nuolatinio arba kintamo nurašymo, apibrėžto KS, nepaisoma, kai įjungtas planavimo optimizavimas. | Spalio 2021 d. |
| Gamyba | KS su subranga: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu subrangos nustatymo KS nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |
| Gamyba | KS be svetainės: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu KS be svetainės nepaisoma, kai įjungtas planavimo optimizavimas. | Palaikoma |
| Gamyba | Poreikis su apibrėžtomis konkrečiomis KS ar maršruto reikalavimais: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu konkrečių KS ar maršruto reikalavimų, apibrėžtų pagal poreikį (pvz., KS arba maršrutas pardavimo užsakyme), nepaisoma, kai įjungtas planavimo optimizavimas. Bus naudojama standartinė KS arba maršrutas, neatsižvelgiant į šį nustatymą. | Spalio 2021 d. |
| Gamyba | Formulės versijos su sudėtiniais / šalutiniais produktais: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu sudėtinių ir šalutinių produktų, susietų su formulės versija, nepaisoma, kai įjungtas planavimo optimizavimas. | Spalio 2021 d. |
| Gamyba | Formulės versijos su išeiga: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu išeigos, susietos su formulės versija, nepaisoma, kai įjungtas planavimo optimizavimas. | Spalio 2021 d. |
| Gamyba | Planai su seka: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu sekos nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |
| Gamyba | Paleisti gamybos užsakymai, kurie nepradėti, buvo suplanuoti pradėti anksčiau nei šiandien: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu, jei gamybos užsakymas vėluoja, bendrojo planavimo metu bus laikoma, kad jis bus baigtas šiandien. Tai aktualu išleistiems gamybos užsakymais, kurių pristatymo data yra praėjusi, tačiau užsakymai dar nėra baigti. | 2021 m. spalio mėn. |
| Gamyba | Ištekliai, suplanuoti esant ribotam pajėgumui: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu išteklių, suplanuotų esant ribotam pajėgumui, nepaisoma, kai įjungtas planavimo optimizavimas. Planavimas atliekamas pagal numatytąjį produkto gamybos laiką. | 2021 m. balandžio mėn. |
| Gamyba | Maršrutai, naudojami planuojant: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu maršrutų nepaisoma, kai įjungtas planavimo optimizavimas. Naudojamas numatytasis produkto gamybos laikas. | 2021 m. balandžio mėn. |
| Gamyba | Pardavimo eilutės rezervavimas, naudojantis išskleidimą: _\#_ | Pardavimo eilutės rezervavimas, naudojantis išskleidimą, nepalaikomas, kai įjungtas planavimo optimizavimas. | 2021 m. spalio mėn. |
| Gamyba | Planavimas išskleidžiant gamybos užsakymus: _\#_ | Planavimas, naudojantis gamybos užsakymų išskleidimą, nepalaikomas, kai įjungtas planavimo optimizavimas. Gamybos užsakymai gali būti suplanuoti atskirai. | Spalio 2021 d. |
| Pasiūlymo patvirtinimai | Bendrieji planai su įgalintu pasiūlymo patvirtinimu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu pasiūlymo patvirtinimai (RFQ) nėra laikomi poreikiu, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2021 m. spalio mėn. |
| Paraiškos | Bendrieji planai su įgalintomis paraiškomis: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu į paraiškas neatsižvelgiama, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | Spalio 2021 d. |
| Laiko rezervai | Padengimo grupės su laiko rezervu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu laiko rezervo nepaisoma, kai įjungtas planavimo optimizavimas. Norėdami kompensuoti šią problemą, galite padidinti gamybos laiką, kad būtų įtrauktas laiko rezervas. | Gavimo laiko rezervas: Palaikoma. Užsakymo laiko rezervas ir išdavimo laiko rezervas: 2021 m. balandžio mėn |
| Laiko rezervai | Bendrieji planai su laiko rezervu: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu laiko rezervo nepaisoma, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. Norėdami kompensuoti šią problemą, galite padidinti gamybos laiką, kad būtų įtrauktas laiko rezervas. | Gavimo laiko rezervas: Palaikoma. Užsakymo laiko rezervas ir išdavimo laiko rezervas: 2021 m. balandžio mėn |
| Saugos atsargų pildymas | Prekės padengimo įrašai, kurių parametras „Išpildyti minimumą” skiriasi nuo „Šiandienos data + įsigijimo laikas”: _\#_ | Planavimo optimizavimas visada naudoja *Šiandienos data + įsigijimo laikas*. Šis pakeitimas sukurtas pasirengti supaprastintam planavimo nustatymui ateityje ir pateikti įgyvendinamą rezultatą. Jei įsigijimo laikas neįtrauktas į pakankamas atsargas, suplanuoti užsakymai, sukurti dabartinėms mažoms turimoms atsargos, visada bus atidėti dėl gamybos laiko. Tai gali sukelti daug triukšmo ir nepageidaujamų suplanuotų užsakymų. Geriausia yra pakeisti parametrą, kad būtų naudojama *Šiandienos data + įsigijimo laikas*. Atnaujinti bendruosius duomenis, kad būtų išvengta įspėjimų. | Netaikoma |
| Pardavimo pasiūlymai | Bendrieji planai su įgalintais pardavimo pasiūlymais: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu į pasiūlymus neatsižvelgiama, kai įjungtas planavimo optimizavimas. Jų bus nepaisoma, neatsižvelgiant į šį nustatymą. | 2021 m. spalio mėn. |
| Laikymo trukmė | Bendrieji planai su įgalinta laikymo trukme: _\#_ | Ši funkcija laukia patvirtinimo. Šiuo metu į laikymo trukmę neatsižvelgiama, kai įjungtas planavimo optimizavimas, neatsižvelgiant į šį parametrą. | Spalio 2021 d. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Darbo su planavimo optimizavimu pradžia](get-started.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
