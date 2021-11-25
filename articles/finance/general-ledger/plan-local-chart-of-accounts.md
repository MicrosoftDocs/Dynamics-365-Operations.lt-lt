---
title: Vietinių sąskaitų plano rengimas
description: Šioje temoje pateikiama informacija, kuri padės jums suplanuoti sąskaitų planą, kai jūsų organizacijai reikės privalomos/ vietinės reikalavimų.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798301"
---
# <a name="plan-your-local-chart-of-accounts"></a>Vietinių sąskaitų plano rengimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums suplanuoti sąskaitų planą, kai jūsų organizacijoje yra juridinių subjektų, kurie turi atitikti reikalavimus konkrečioms vietos, kurioje jie turi verslo veiklą. Šioje temoje aprašomi sąskaitų plano terminai:

- **Visuotinis** – sąskaitų planas, kurį organizacija naudoja visuotinai. Dažniausiai, jūs konsoliduojate šį sąskaitų planą.
- **Vietinis** – sąskaitų planas, kurį naudoja juridiniai subjektai tam tikroje šalyje arba regione.
- **Bendrai** – naudojamas sąskaitų planas, kurį gali naudoti daugiau nei vienas juridinis subjektas. Galima bendrai naudoti ir visuotinį sąskaitų planą, ir vietines sąskaitų diagramas.

Galite kurti ir bendrai naudoti kelias sąskaitų diagramas. Bendrai naudojamą sąskaitų planą gali naudoti daugiau nei vienas juridinis subjektas, tačiau kiekvienam juridiniam subjektui galima priskirti tik vieną sąskaitų planą. Sąskaitų planas, kurį naudoja juridinis subjektas naudoja, nurodomas puslapyje **Didžioji knyga**.

Kai jos sudaro sąskaitų planą, daugelis organizacijų siekia sukurti visuotinį sąskaitų planą. Bendrai naudojamas sąskaitų plano pajėgumas leidžia sukurti visuotinį sąskaitų planą. Yra naudinga kurti ir naudoti vieną sąskaitų planą. Pavyzdžiui, geriau kontroliuoti, tvarkyti ir tvarkyti bei tvarkyti ataskaitas.

Dauguma organizacijų pasirenka visuotinį sąskaitų planą, todėl paprasčiausias tipas yra įgyvendinti. Nepaisant to, kai kurie juridiniai subjektai reikalauja vietinio sąskaitų plano dėl šių priežasčių:

- Vietiniai privalomi reikalavimai
- Vietinių apskaitos standartų reikalavimai
- Pramonės reikalavimai
- Įmonei keliami ataskaitų ir analizės reikalavimai

Jeigu jūsų organizacija reikalauja, kad juridinis subjektas naudoja vietinį sąskaitų planą, galima naudoti dvi jo vykdymo pasirinktis:

- Priskirkite visuotinį sąskaitų planą ir nustatykite kitas priemones, kurios atitiktų vietinius reikalavimus.
- Juridiniam subjektui priskirkite vietinį sąskaitų planą ir apibrėžkite ryšius su visuotiniu sąskaitų planas.

Organizacijos struktūra ir ataskaitų struktūra lemia naudojamą pasirinktį.

[![ Diagrama, kurioje parodyta, kaip organizacijos struktūra apibrėžia, ar naudoti visuotinį, ar vietinį sąskaitų planą](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Jei visuotinis sąskaitų planas priskirtas juridiniam subjektui, galimos šios vietinių ataskaitų reikalavimų pateikimo pasirinktys:

- Vietinis konsolidavimas.
- Norėdami sekti vietinį sąskaitų planą, naudokite finansinę dimensiją.
- Visuotinio sąskaitų plano kurkite vietines pagrindines sąskaitas.
- Atlikite išorinį susiejimą su vietiniu sąskaitų grafiku.

Jei vietinis visuotinis sąskaitų planas priskirtas juridiniam subjektui, tik parinktis šiuo metu yra šios vietinių ataskaitų reikalavimų pateikimo pasirinktys kaip visuotinis konsolidavimas.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Visuotinis sąskaitų planas, priskirtas juridiniam subjektui

Jei visuotinį sąskaitų planą turite priskirti juridiniam subjektui, galite naudoti keturias sistemos konfigūravimo pasirinktis, kaip aprašyta anksčiau. Visoms keturioms pasirinktims, sukonfigūruojamas vienas sąskaitų planas ir susiejamas su kiekvienu **DK** puslapyje esamu juridiniu subjektu. Kiekviena pasirinktis naudoja skirtingą būdą, kad atitiktų lokalizavimo reikalavimus. Toliau pateikti skyriai apibūdina aukšto lygio veiksmus, kad būtų galima konfigūruoti sistemą pagal lokalizavimo reikalavimus. Jie taip pat apibūdina kiekvienos pasirinkties pranašumas ir pereis.

### <a name="do-local-consolidation"></a>Vietinis konsolidavimas

Vietinis konsolidavimas yra rekomenduojamas būdas atitikti vietines sąskaitų plano reikalavimus ir pasinaudoti tuo tikslu sukurta sistemos funkcija.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Nustatyti vietinio sąskaitų plano konsolidavimą

1. Sukurkite vieną visuotinį sąskaitų planą, kuriame būtų visos būtinos pagrindinės sąskaitos.
2. Kiekviename juridiniame subjekte puslapyje priskirkite visuotinį **DK** planą.
3. Sukurkite konsolidavimo juridinį subjektą kiekvienai reikalingai lokalizacijai.
4. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei reikalinga tik viena lokalizacija, sukonfigūruokite konsolidavimo sąskaitą **Pagrindinės sąskaitos** puslapyje, naudokite **Konsolidavimo grupes** ir **Papildomas konsolidavimos sąskaitas** puslapius.
    - Jei reikalinga daugiau nei viena lokalizacija arba jei sąskaitos numerį ir sąskaitos pavadinimą reikia versti, naudokite **konsolidavimo grupes** ir **papildomų konsolidavimo sąskaitų** puslapius, kad vaizduotumėte lokalizavimo reikalavimus.

5. Vykdykite konsolidavimo procesą, norėdami pakeisti vertę iš šaltinio juridinio subjekto, kuris naudoja visuotinį sąskaitų planą, į konsoliduotą įmonę, kuri naudoja vietinį sąskaitų planą.

#### <a name="advantages"></a>Privalumai

- Šis būdas suteikia nuoseklų darbo organizacijoje būdą.
- Atliekamas vienas vietinių pareigų vertimas.
- Šis būdas palaiko ir pagrindinės sąskaitos ID, ir kiekvienos pagrindinės sąskaitos pavadinimo vertimą.
- Jis palaiko kelias lokalizacijas.

#### <a name="disadvantages"></a>Trūkumai

- Sukuriama papildoma konsolidavimo įmonė.
- Papildomas konsolidavimo procesas yra baigtas.
- Šis būdas gali pateikti ataskaitą lokalizuotoje diagramoje tik baigus konsolidavimo procesą.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Norėdami sekti vietinį sąskaitų planą, naudokite finansinę dimensiją

Šis būdas naudoja finansinę dimensiją, kurioje finansinės dimensijos reikšmės nurodo vietines pagrindines sąskaitas, reikalingas lokalizavimui. Tai veikia gerai, jei reikia tik vienos vietos. Tačiau, jis tampa mažiau naudojamas, kai pridedate daugiau lokalizacijų ir finansinių dimensijų.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Nustatykite finansinę dimensiją vietiniam sąskaitų planui

1. Sukurkite vieną visuotinį sąskaitų planą, kuriame būtų visos būtinos pagrindinės sąskaitos.
2. Kiekviename juridiniame subjekte puslapyje priskirkite visuotinį **DK** planą.
3. Sukurti finansinę dimensiją, vaizduojančią vietinį sąskaitų planą.
4. Sukurti finansinę dimensiją, vertės, vaizduojančius pagrindines vietinių sąskaitų plano pagrindines sąskaitas.
5. Atnaujinkite sąskaitos struktūrą, kad joje būtų finansinė dimensija „vietinė sąskaitų planas".
6. Įsitikinkite, kad „vietinė sąskaitų plano" finansinė dimensija visada turi reikšmę ir kad ji neleidžia tuščios vertės. Naudokite išvestas dimensijas arba fiksuotas dimensijas.
7. Sukurkite finansinių dimensijų rinkinį, kuriame „vietinė sąskaitų plano" finansinė dimensija yra pirmoji pasirinkta finansinė dimensija. Finansinių dimensijų rinkinys gali būti naudojamas generuojant bandomąjį balansą.

#### <a name="advantages"></a>Privalumai

- Pagrindinės visuotinių ir vietinių sąskaitų sąskaitos yra operacijų lygyje. Pagrindinė sąskaita yra visuotinė, o finansinės dimensijos reikšmė yra vietinė.
- Šis būdas pateikia ataskaitas realiuoju laiku ir visuotinių finansų pareigų bei vietos finansų pareigų rodinius.

#### <a name="disadvantages"></a>Trūkumai

- DK parametruose, jei suminės sąskaitos lauke naudojamos **vertės yra nustatytos laukelis** kaip **Apskaitos paskirstymai**, finansinės dimensijos, kurios nurodo pagrindinę išlaidų / turto / įplaukų sąskaitą, bus netinkamai naudojamos gautinų sumų ir mokėtinų sumų suminės sąskaitose. Mes rekomenduojame, kad jūs norėtumėte nustatyti lauką kaip šaltinio dokumentą, o ne užtikrinti, kad būtų naudojamos teisingos finansinės dimensijos vertės.
- Jei reikia daug vietinių sąskaitų plano ir visoms iš jų naudojama viena finansinė dimensija, naudojamų finansinių dimensijų verčių sąrašas gali tapti ilgas ir sunku dirbti.
- Jei reikia daug vietinių sąskaitų plano ir kiekvienam iš jų rodyti naudojama atskira finansinė dimensija, sistemos tinkamumo naudoti ir našumo tai gali būti paveikta, kai yra pridėtos finansinės dimensijos ir finansinių dimensijų rinkiniai.
- Rekomenduojame atidžiai apsvarstyti finansinių dimensijų skaičių, kuris jums reikalingas, verčių skaičių kiekvienoje ir finansinių dimensijų rinkinių skaičių, nes visi šie faktoriai gali paveikti sistemos našumą.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Visuotinio sąskaitų plano kurkite vietines pagrindines sąskaitas

*Apie ką buvo paklausta kopijos doroklis:* šiuo požiūriu visuotinės sąskaitų plano vietinės pagrindinės sąskaitos apima pagrindines sąskaitas iš vietinio sąskaitų plano į visuotinį sąskaitų planą.

*Originali versija:* vietinės pagrindinės sąskaitos pagal visuotinio CoA būdą yra ta, kad vietinės CoA pagrindinės sąskaitos yra įtrauktos į visuotinį CoA.

*Ar tai turėtų būti pateikta:* tokiu atveju vietinės pagrindinės vietinio sąskaitų plano sąskaitos įtraukiamos į visuotinį sąskaitų planą.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Visuotinio sąskaitų plano nustatymas vietinėse pagrindinėse sąskaitose

1. Sukurkite vieną sąskaitų planą, kuriame būtų pagrindinės visuotinės sąskaitų plano ir vietinio sąskaitų plano sąskaitos.
2. Kiekviename juridiniame subjekte puslapyje priskirkite visuotinį **DK** planą.
3. Sąskaitų lentelėje sukurkite bendrųjų sąskaitų, kad susumumėte pagrindines sąskaitas, kurios atitinka tą patį tikslą.
4. Sukurkite juridinių subjektų nepaisymus kiekvienoje vietinėje sąskaitoje, kad išvengtumėte operacijų iš kitų juridinių subjektų, kuriems nesukurta vietinė sąskaita.
5. Sukurkite juridinio subjekto nepaisymus kiekvienoje visuotinoje sąskaitoje, kad išvengtumėte operacijų iš lokalizavimo juridinių subjektų.

#### <a name="advantages"></a>Privalumai

- Realiuoju laiku galima peržiūrėti visuotines finansų pareigas ir vietines finansines pareigas konkrečiose ataskaitose ir konkrečiuose sistemos rodiniuose, pvz., balanso finansinėje ataskaitoje. Jį taip pat galima pasiekti bendrosios **sąskaitos** mygtuku Laikotarpis.
- DK sąskaitoje neturite papildomo segmento.

#### <a name="disadvantages"></a>Trūkumai

- Bendrosios sąskaitos naudojimas ir matomumas ribojami. Pavyzdžiui, bendrosios sąskaitos nematomos **Bandomojo balanso** sąrašo puslapyje.
- Priežiūrai reikia papildomų pastangų.
- Finansinių ataskaitų kūrimui reikia papildomų neautomatinių pastangų.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Atlikite išorinį susiejimą su vietiniu sąskaitų grafiku

Visuotinio sąskaitų plano perteikimas reiškia, kad jūs valdote susiejimą ir lokalizavimą už sistemos ribų. Tokiu atveju tik sukurkite vieną visuotinę sąskaitų planą ir „Microsoft Dynamics 365 Finance“ tvarkysite poreikius ne sistemoje.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Nustatykite išorinį susiejimą su vietiniu sąskaitų grafiku

1. Sukurkite vieną visuotinį sąskaitų planą, kuriame būtų visos būtinos pagrindinės sąskaitos.
2. Kiekviename juridiniame subjekte puslapyje priskirkite visuotinį **DK** planą.
3. Atlikite išorinį susiejimą su vietiniu sąskaitų grafiku ne „Finance“.

#### <a name="advantages"></a>Privalumai

- Šis būdas suteikia vieningus būdus dirbti pagal organizacijos būdą.

#### <a name="disadvantages"></a>Trūkumai

- Iš sistemos nėra vietinių ataskaitų.
- Šis būdas yra po klaidos kuriant finansines ataskaitas.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Vietinis sąskaitų planas, priskirtas juridiniam subjektui

Jeigu jūsų organizacija nusprendžia nenaudoti visuotinių sąskaitų plano tarp juridinių subjektų, sukuriamas atskiras kiekvieno unikalaus vietinio sąskaitų plano sąskaitų planas. Tada kiekvienas juridinis subjektas susiejamas su atitinkamu sąskaitų grafiku **DK** puslapyje.

### <a name="do-global-consolidation"></a>Bendrasis konsolidavimas

Tokiu atveju konsoliduota įmonė naudojama konsoliduotoms sąskaitoms iš kiekvienos šaltinio vietinės įmonės į konsoliduotą visuotinę sąskaitų planą konsoliduotoje įmonėje sujungti. Naudojant šį būdą reikia išlaikyti kiekvieno vietinio sąskaitų plano susiejimą su konsoliduotoje įmonėje esamu visuotiniu sąskaitų grafiku.

#### <a name="set-up-global-consolidation"></a>Nustatyti bendrąjį konsolidavimą

1. Sukurkite atskirą kiekvieno juridinio subjekto, kuris turi skirtingą vietinį sąskaitų planą, sąskaitų planą. Jei kurie juridiniai subjektai turi tą patį vietinį sąskaitų planą, reikia tik vieno vietinio sąskaitų plano ir jis gali būti bendrai naudojamas.
2. Kiekviename juridiniame subjekte puslapyje priskirkite atitinkamą visuotinį **DK** planą.
3. Nebūtina: sukurkite kiekvienos konsoliduotos įmonės, kuri turi skirtingą visuotinį sąskaitų planą, sąskaitų planą, visuotinei sąskaitų diagramai.
4. Sukurkite konsolidavimo juridinį subjektą kiekvienam konsolidavimo lygiui, kuris reikalingas, ir **DK** puslapyje atitinkamą sąskaitų priskirkite planą.
5. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei reikalingas tik vienas konsolidavimas, konsolidavimo sąskaitą sukonfigūruokite **pagrindinės sąskaitos** puslapyje.
    - Jei reikalinga daugiau nei viena konsolidacija arba jei sąskaitos numerį ir sąskaitos pavadinimą reikia versti, naudokite **konsolidavimo grupes** ir **papildomų konsolidavimo sąskaitų** puslapius, kad vaizduotumėte lokalizavimo reikalavimus bendrame sąskaitų plane.

6. Vykdykite konsolidavimo procesą, norėdami perkelti balansus iš vietinių juridinių subjektų į konsoliduotąjį juridinį subjektą. Šis konsoliduotas juridinis subjektas naudoja konsolidavimo sąskaitas, kurias apibrėžiate 5 žingsniu.

#### <a name="advantages"></a>Privalumai

- Vietinis apskaitos standartų formatas taikomas vietiniu būdu.
- Tokiu būdu vietinė finansų komandai bus lengviau dirbti.

#### <a name="disadvantages"></a>Trūkumai

- Visuotinių pareigų realiuoju laiku peržiūrėti negalima.
- Konsolidavimo procesas gali būti vykdomas dažniausiai.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Sąskaitų plano rengimas](plan-chart-of-accounts.md)
- [Didžiųjų knygų konfigūravimas](configure-ledger.md)
- [Finansinės dimensijos ir registravimas](Default-dimensions.md#balancing-dimension)
- [Finansinių dimensijų rinkiniai](financial-dimension-sets.md)
- [Konsolidavimo ir šalinimo apžvalga](../budgeting/consolidation-elimination-overview.md)
- [Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
