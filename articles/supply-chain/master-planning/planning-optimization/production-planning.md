---
title: Gamybos planavimas
description: Šiame straipsnyje aprašomas gamybos planavimas ir paaiškinama, kaip modifikuoti suplanuotus gamybos užsakymus naudojant planavimo optimizavimą.
author: t-benebo
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 151aa3688c570ea6ec282c297ed18288dd886131
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873788"
---
# <a name="production-planning"></a>Gamybos planavimas

[!include [banner](../../includes/banner.md)]

Planavimo optimizavimas palaiko kelis gamybos scenarijus. Jei pereinate iš esamo, įtaisyto bendrojo planavimo mechanizmo, svarbu žinoti apie pasikeitusį veikimo būdą.

Toliau pateiktame vaizdo įraše pateikiamas trumpas įžanga apie kai kurias šiame straipsnyje aptartas sąvokas: [Dynamics 365 Supply Chain Management optimizavimo patobulinimų planavimas](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Šios funkcijos įjungimas sistemoje

Jei jūsų sistema dar neapima šiame straipsnyje aprašytų priemonių, [...](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*eikite į funkcijų valdymą ir įjunkite planavimo optimizavimo funkcijos suplanuotos gamybos užsakymus.*

## <a name="planned-production-orders"></a>Suplanuoti gamybos užsakymai

Kai bendrasis planavimas sukuria suplanuotus užsakymus reikalavimų įgyvendinimui, užsakymo tipas nustatomas pagal lauko **Suplanuoto užsakymo tipas** reikšmę. Jei lauke **Suplanuoto užsakymo tipas** nustatyta *Gamyba*, kuriami suplanuoti gamybos užsakymai. Į šiuos suplanuotus gamybos užsakymus įtraukta informacija apie aktyvias komplektavimo specifikacijas (KS) ir maršruto ID iš susijusios gamybos sąrankos.

## <a name="requirements-from-boms"></a>KS reikalavimai

Bendrojo planavimo metu atsižvelgiama į KS informaciją. Plano išeiga apima medžiagų tiekimą, padengiantį susijusią medžiagų paklausą gamybai.

Bendrojo planavimo metu dabartinė ir aktyvi KS naudojama nustatyti gamybai reikalingas medžiagas. Šis veiksmas atliekamas visuose KS struktūros lygiuose, susijusiuose su reikalaujamu gamybos užsakymu. Medžiagų poreikis įvykdomas naudojant turimas atsargas, esamą tiekimą pagal užsakymą ir patvirtintus suplanuotus užsakymus. Jei bet kurioje vietoje reikia papildomos medžiagos, sukuriamas suplanuotas užsakymas poreikiui patenkinti.

## <a name="scheduling-during-firming"></a>Planavimas patvirtinimo metu

Suplanuoti gamybos užsakymai apima maršruto ID, kuris būtinas gamybai planavimui. Tačiau planavimo vykdymo metu laukiama planavimo palaikymo patvirtinimo. Maršruto ID yra naudojamas gamybos užsakymams planuoti patvirtinimo metu. Todėl suplanuotų gamybos užsakymų gamybos laikas gali skirtis nuo iš jų sugeneruojamų, susijusių suplanuotų ar patvirtintų gamybos užsakymų, gamybos laiko, kaip aprašyta čia:

- **Suplanuotas gamybos užsakymas** – gamybos laikas paremtas statiniu išleisto produkto gamybos laiku.
- **Patvirtintas gamybos užsakymas** – gamybos laikas paremtas planavimu, naudojančiu maršruto informaciją ir susijusius išteklių apribojimus.

Norėdami gauti daugiau informacijos apie numatomą funkcijos prieinamumą, žiūrėkite [Planavimo optimizavimo pritaikymo analizė](planning-optimization-fit-analysis.md).

Jei jums reikalingos gamybos funkcijos, kurios dar nėra prieinamos planavimo optimizavime, galite toliau naudoti įtaisytąjį bendrojo planavimo mechanizmą. Išimtis nebūtina.

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

Norėdami užtikrinti, kad planavimo optimizavimas turi teisingam rezultatui apskaičiuoti reikalingą informaciją, turite įtraukti visus produktus, kurie turi bet kokį ryšį su produktais visoje suplanuoto užsakymo KS struktūroje. Planavimo scenarijuose, apimančiuose gamybą, mes rekomenduojame vengti vykdyti filtruotą bendrąjį planavimą.

Nors priklausomos antrinės prekės yra automatiškai aptinkamos ir įtraukiamos į bendrojo planavimo vykdymą, kai naudojamas įtaisytasis bendrojo planavimo mechanizmas, planavimo optimizavimas šiuo metu neatlieka šio veiksmo.

Pavyzdžiui, jei vienas varžtas iš produkto A KS struktūros taip pat naudojamas produktui B gaminti, visi A ir B produktų KS struktūros produktai turi būti įtraukti į filtrą. Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai. Kitu atveju bendrasis planavimas pateiks be jūsų besidėtingų rezultatų.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Priežastys, kodėl išvengti filtruotus bendrojo planavimo avimus

Kai vykdote filtruotus bendrojo produkto planus, „Planning Optimization“ (skirtingai nuo įtaisytojo bendrojo planavimo modulio) neaptinka visų tarpinės gamybos ir žaliavų to produkto KS struktūroje, todėl jo neįeis į bendrojo planavimo procesą. Nors „Planning Optimization“ identifikuoja pirmąjį produkto KS struktūros lygį, jo metu iš duomenų bazės nėra įkeliami produkto parametrai (pvz., numatytasis užsakymo tipas arba prekės padengimas).

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
