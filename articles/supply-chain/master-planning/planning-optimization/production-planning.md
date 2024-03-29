---
title: Gamybos planavimas
description: Šiame straipsnyje aprašomas gamybos planavimas ir paaiškinama, kaip modifikuoti suplanuotus gamybos užsakymus naudojant planavimo optimizavimą.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 43da249637c44b3f56e8b5e210a0e44d9ac6cb9d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740555"
---
# <a name="production-planning"></a>Gamybos planavimas

[!include [banner](../../includes/banner.md)]

Toliau pateiktame vaizdo įraše pateikiamas trumpas įžanga apie kai kurias šiame straipsnyje aptartas sąvokas: [Dynamics 365 Supply Chain Management optimizavimo patobulinimų planavimas](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-this-feature-on-or-off-for-your-system"></a>Įjungti arba išjungti šią funkciją jūsų sistemai

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, *·*[tada](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) administratoriai gali įjungti arba išjungti šią funkciją ieškodami funkcijų valdymo darbo srityje funkcijos planavimo optimizavimo funkcijos suplanuotų gamybos užsakymų.

## <a name="planned-production-orders"></a>Suplanuoti gamybos užsakymai

Kai bendrasis planavimas sukuria suplanuotus užsakymus reikalavimų įgyvendinimui, užsakymo tipas nustatomas pagal lauko **Suplanuoto užsakymo tipas** reikšmę. Jei lauke **Suplanuoto užsakymo tipas** nustatyta *Gamyba*, kuriami suplanuoti gamybos užsakymai. Į šiuos suplanuotus gamybos užsakymus įtraukta informacija apie aktyvias komplektavimo specifikacijas (KS) ir maršruto ID iš susijusios gamybos sąrankos.

## <a name="requirements-from-boms"></a>KS reikalavimai

Bendrojo planavimo metu atsižvelgiama į KS informaciją. Plano išeiga apima medžiagų tiekimą, padengiantį susijusią medžiagų paklausą gamybai.

Bendrojo planavimo metu dabartinė ir aktyvi KS naudojama nustatyti gamybai reikalingas medžiagas. Šis veiksmas atliekamas visuose KS struktūros lygiuose, susijusiuose su reikalaujamu gamybos užsakymu. Medžiagų poreikis įvykdomas naudojant turimas atsargas, esamą tiekimą pagal užsakymą ir patvirtintus suplanuotus užsakymus. Jei bet kurioje vietoje reikia papildomos medžiagos, sukuriamas suplanuotas užsakymas poreikiui patenkinti.

## <a name="scheduling-during-firming"></a>Planavimas patvirtinimo metu

Suplanuoti gamybos užsakymai apima maršruto ID, kuris būtinas gamybai planavimui. Tačiau planavimo vykdymo metu laukiama planavimo palaikymo patvirtinimo. Maršruto ID yra naudojamas gamybos užsakymams planuoti patvirtinimo metu. Todėl suplanuotų gamybos užsakymų gamybos laikas gali skirtis nuo iš jų sugeneruojamų, susijusių suplanuotų ar patvirtintų gamybos užsakymų, gamybos laiko, kaip aprašyta čia:

- **Suplanuotas gamybos užsakymas** – gamybos laikas paremtas statiniu išleisto produkto gamybos laiku.
- **Patvirtintas gamybos užsakymas** – gamybos laikas paremtas planavimu, naudojančiu maršruto informaciją ir susijusius išteklių apribojimus.

## <a name="delays"></a>Atidėjimai

Jei reikiamos medžiagos gamybos laikas yra ilgesnis nei laikotarpis nuo šiandienos datos iki medžiagų poreikio datos, suplanuotas reikiamos medžiagos užsakymas ir susijęs gamybos užsakymas bus atidėti. Suplanuotų užsakymų atidėjimas (dienomis) skaičiuojamas pagal išleisto produkto gamybos laiką. Atidėjimo informacija tada bus perduodama per visus KS struktūros lygius. Todėl jūs galite sekti atidėtų žaliavų poveikį iki pat kliento pardavimo užsakymo.

## <a name="modifying-planned-orders"></a>Suplanuotų užsakymų modifikavimas

Keisdami suplanuoto užsakymo informaciją, gausite tokį pranešimą: „Atkreipkite dėmesį, kad neautomatinių pakeitimų poveikis suplanuotiems užsakymams nebus rodomas likusioje plano srityje iki kito bendrojo planavimo vykdymo.”

Jei norite pakeisti suplanuoto užsakymo informaciją ir pamatyti poveikį susijusiems medžiagų reikalavimams, atlikite šiuos veiksmus.

1. Atnaujinkite suplanuotą užsakymą.
2. Patvirtinkite suplanuotą užsakymą.
3. Vykdykite bendrąjį planavimą.

Kai vykdote bendrąjį planavimą, neturėtumėte naudoti filtrų, jeigu įtraukti suplanuoti gamybos užsakymai. Daugiau informacijos ieškokite šio straipsnio [skyriuje](#filters) Filtrai.

> [!NOTE]
> Jei suplanuoto užsakymo pristatymo data pakeičiama į vėlesnę, poreikis gali būti iškviestas naujam suplanuotam užsakymui. Taip nutinka, kai dėl naujos tiekimo datos atidedamas iškviestas poreikis, tačiau atsižvelgiant į gamybos laiko parametrus, atidėjimo galima išvengti.

## <a name="explosion-page"></a>Išskleidimo puslapis

Galite naudoti **Išskleidimo** puslapį analizuoti poreikiui, kuris reikalingas konkrečiam arba suplanuotam gamybos užsakymui, susijusiai aprėpčiai ir iškvietimo informacijai. Informacija **Išskleidimo** puslapyje atnaujinama bendrojo planavimo metu. Negalite atnaujinti informacijos tiesiogiai iš **Išskleidimo** puslapio.

## <a name="filters"></a><a name="filters"></a>Filtrai

Norėdami užtikrinti, kad bendrasis planavimas turi informacijos, kurios reikia norint apskaičiuoti teisingus rezultatus, turite įtraukti visus produktus, kurie turi bet kokį ryšį su produktais, visoje suplanuoto užsakymo KS struktūroje. Planavimo scenarijuose, apimančiuose gamybą, mes rekomenduojame vengti vykdyti filtruotą bendrąjį planavimą.

Nors priklausomos antriniai prekės automatiškai aptinkamos ir įtraukiamos į bendrąjį planavimą, kai naudojamas pasenusias bendrojo planavimo mechanizmas, planavimo optimizavimas šiuo metu neatlika šio veiksmo.

Pavyzdžiui, jei vienas varžtas iš produkto A KS struktūros taip pat naudojamas produktui B gaminti, visi A ir B produktų KS struktūros produktai turi būti įtraukti į filtrą. Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai. Kitu atveju bendrasis planavimas pateiks be jūsų besidėtingų rezultatų.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Priežastys, kodėl išvengti filtruotus bendrojo planavimo avimus

Kai vykdote filtruotą bendrąjį produkto planavimą, planavimo optimizavimas (skirtingai nei pasenęs bendrojo planavimo variklis) neaptinka visų tarpinės gamybos ir žaliavų to produkto KS struktūroje, todėl jo neįeis į bendrojo planavimo procesą. Nors „Planning Optimization“ identifikuoja pirmąjį produkto KS struktūros lygį, jo metu iš duomenų bazės nėra įkeliami produkto parametrai (pvz., numatytasis užsakymo tipas arba prekės padengimas).

„Planning Optimization“ vykdymo duomenys įkeliami iš anksto ir taikomi filtrai. Tai reiškia, kad jei tarpinė gamyba arba žaliavos, įtrauktos į konkretų produktą, nėra filtro dalis, informacija apie ją nebus fiksuojama vykdyti. Be to, jei tarpinė gamyba arba žaliavos taip pat įtraukiamos į kitą produktą, tada filtruotas paleidimas, kuriame įtrauktas tik pradinis produktas ir jo komponentai, pašalintų esamą suplanuotą to kito produkto poreikį.

Dėl šios logikos filtruoti bendrojo planavimo leidžiami rezultatai gali būti netikėti. Toliau pateikti pavyzdžiai iliustruoja netikėtus rezultatus.

### <a name="example-1"></a>1 pavyzdys

Baigtai *FG* sudaro šie komponentai:

- Žaliavos *R*
- Tarpinė gamyba *S1*, kurią sudaro tarpinė gamyba *S2*

Yra turimų atsargų *R*, o atsargose nėra tarpinės *S1* gamybos.

Kai atliekate filtruotą baigtos gamybos FG bendrojo planavimo procesą, pamatysite suplanuotą baigtos gamybos *FG*, bendrojo planavimo procesą, pamatysite suplanuotą gmaybos *FG* užsakymą, suplanuotą žaliavų *R* pirkimo užsakymą ir tarpinės gamybos *S1* suplanuotą pirkimo užsakymą. Tai yra rezultatas, nes planavimo optimizavimas nepaisė esamo žaliavų *R* ir papildomas produktas *S1*, nes planavimo optimizavimas nepaisė easmo žaliavų ir tarpinės gamybos *S2*, o ne tiesiogiai jas užsakė. Taip nutiko, nes „Planning Optimization“ turi tik baigtos gamybos *FG* komponentų sąrašą, kuriame nėra susijusios informacijos, pvz., esamo jo komponentų tiekimo ar jų numatytųjų užsakymo parametrų.

### <a name="example-2"></a>2 pavyzdys

Pagal ankstesnį pavyzdį papildoma baigta įranga *FG2* taip pat naudoja tarpinės gamybos *S1*. Yra baigtų gerų *FG2* suplanuotas užsakymas ir yra suplanuotas visų komponentų poreikis, įskaitant *S1*.

Nusprendėte atnaujinti besibaigias filtruotas bendrojo planavimo rezultatus pagal ankstesnį pavyzdį, įtraukdami į filtrą visą tarpinę gamybą ir žaliavas iš baigtos prekės *FG* KS struktūros į filtrą ir paleisdami visą paleistį.

Paleidus visą išaurinimo procesą, sistema panaikina visus esamus visų įtrauktų produktų rezultatus ir iš naujo sukuria rezultatus remdamasi naujais skaičiavimais. Tai reiškia, kad esamas suplanuotas produkto *S1* poreikis panaikinamas ir tada perkurtas atsižvelgiant į baigtus prekių *FG* reikalavimus, o baigtų gerų *FG2* reikalavimų nepaisoma. Taip nutinka, nes paleidus „Planning Optimization“, į jį neįeis tik planuotas kitų suplanuotų gamybos užsakymų poreikis, o tik planuota paklausa, sugeneruota vykdant&mdash;.

> [!NOTE]
> Jei esamo suplanuoto baigtų prekių *FG2* užsakymo būsena yra *Patvirtinta*, patvirtintas suplanuotas poreikis bus įtrauktas net jei pirminis produktas nėra įtraukiama į filtrą.

Todėl, nebent pridedate visus baigtos prekės FG komponentus, baigtą gera *FG*, baigtos prekės *FG2*, ir visus kitus produktus, kurių dalis yra šie komponentai (kartu su komponentais), filtruotas bendrojo planavimo procesas pateiks rezultatus.

Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
