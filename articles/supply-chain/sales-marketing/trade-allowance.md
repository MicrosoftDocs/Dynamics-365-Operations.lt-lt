---
title: Prekybos nuolaidų valdymas
description: Šioje temoje aprašomas „Dynamics 365 Supply Chain Management“ prekybos nuolaidų valdymas.
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: MCRBrokerClaims, MCRBrokerWriteOffReasonPrompt, MCRRoyaltyVendTable, MCRRoyaltyVendTrans, PdsCustRebateGroup, PdsRebateAgreement, TAMCopyTradePromotions, TAMDeduction, TAMDeductionCreate, TAMDeductionDenyReason, TAMDeductionParmDeny, TAMDeductionParmMassUpdate, TAMDeductionParmMatch, TAMDeductionParmSplit, TAMDeductionParmWriteOff, TAMDeductionType, TAMDeductionWriteOffReason, TAMFundManagement, TAMFundUsage, TAMListPage, TAMMarketingObjective, TAMMerchEventType, TAMOneTimePromotion, TAMPromoCompareGraph, TAMPromoStatistic, TAMPromotionAnalysisSummary, TAMPromotionParameters, TAMPromotionPeriod, TAMTemplateListPage, TAMTradePromotionAnalysis, TAMTradePromotions, TAMWhatIfPromotionAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 15f324f66240380f698dbc67b95f3bea19314a18
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974915"
---
# <a name="trade-allowance-management"></a>Prekybos nuolaidų valdymas

[!include [banner](../includes/banner.md)]

Prekybos nuolaidų valdymas suteikia galimybę įmonėms valdyti pardavimo akcijų programas, kuriomis siūlomi „užmokesčio už veiklą“ piniginiai atlygiai klientams, kurie pasiekia apimties ir elgsenos tikslų. Funkcijos galimybės yra skirtos įmonėms, kurios vykdo išsamius skatinimo siekiant padidinti pelną procesus – nuo skatinimo lėšų biudžeto sudarymo ir paskirstymo iki nuolaidų sutarčių nustatymo, paraiškos kūrimo ir tvarkymo, mokėjimų apdorojimo, akcijų nuolaidos efektyvumo analizės.


Šiame straipsnyje pateikiama plati prekybos nuolaidų valdymo funkcijų apžvalga ir supažindinama su įprastu užduočių, kurios susijusios su pardavimo akcijų programos valdymu, rinkiniu. Kelių tipų vartotojai, turintys veiklos ir sprendimų priėmimo atsakomybę, turėtų naudoti šią funkciją norėdami pasiekti atitinkamų tikslų.

- Lėšų paskirstymas į pasirinktas sąskaitas savo nuožiūra ir prekybos nuolaidų sutarčių nustatymas, atsižvelgiant į vėliau pateikiamas sąskaitas ir vienkartines fiksuotų sumų išmokas (už sutartą paslaugą)
- Sutartų skatinimo sutarčių vykdymas vykdant nuolatinį pardavimą ir generuojant vėliau pritaikomas paraiškas
- Sugeneruotų paraiškų skaičiavimas, patvirtinimas bei apdorojimas ir jų kaip mokėjimų sudengimo atskaitymų perdavimas į gautinas sumas (A/R)
- Kliento trumpo mokėjimo suderinimas su atskaitymu, kurį reikia atlikti
- Akcijų lėšų naudojimo sekimas ir programos pelningumo bei efektyvumo vertinimas

## <a name="audience-and-purpose"></a>Auditorija ir tikslas

Šiame dokumente pateikta informacija skirta įmonių verslo sprendimus priimantiems asmenims, užimantiems tokias pareigas kaip pirkimo vadovas, vyriausiasis finansininkas (CFO) ir apskaitos vadovas, bei kurie atsakingi už tolesnes sritis.

- Aukšto lygio biudžetai ir lėšų paskirstymas
- Pardavimo akcijų planavimas ir analizavimas
- Darbuotojų, kurie apdoroja vėliau pritaikomas paraiškas, atlieka mokėjimus pagal prekybos įvykius ir sudengia trumpus mokėjimus bei atskaitymus, valdymas

Žmonės, kuriems priskirti šie vaidmenys, ieško būdų, kaip pasiekti šių tikslų.

- Geriau naudoti rinkodaros akcijų lėšas.
- Lanksčiai pritaikyti skirtingų tipų akcijų programas ir nuolaidas.
- Sumažinti administracinę naštą ir klaidas, susijusias su reklamų rezultatų stebėjimu ir paraiškų apdorojimu.
- Gerinti pinigų srautų prognozes kaupiant ateities įsipareigojimams vykdyti.
- Kiekybiškai pagrįsti vykstančias ir būsimas derybas su klientais dėl akcijų.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Akcijų lėšų ir prekybos nuolaidų sutartis

Prekybos nuolaidų sutartis yra skatinimo programa, kurioje mokėjimo už rezultatus piniginiai atlygiai siūlomi klientams, kurie pasiekia konkrečių apimties ir (arba) elgsenos tikslų. Akcijų lėšos yra biudžeto išlaidas. Tokiu būdu akcijų kampanijas gali įrašyti.

### <a name="promotional-fund"></a>Akcijos lėšos

Lėšos, kurios paskirstomos prekybos nuolaidų sutartims, įrašomos puslapyje **Lėšos**. Norėdami atidaryti puslapį **Lėšos** pasirinkite **Pardavimas ir rinkodara** \> **Prekybos nuolaidos** \> **Lėšos** \> **Lėšos**.

![Lėšų puslapis](./media/trade-allowance-management-funds-page.png "Lėšų puslapis")

Puslapyje **Lėšos** galite peržiūrėti išsamią informaciją apie akcijų lėšas.

„FastTab“ **Bendra** rodomas lėšų galiojimo laikotarpis ir jų biudžeto suma. Tam, kad lėšos būtų paskirstytos į akcijų sutartį, turi būti nustatyta lauko **Būsena** reikšmė **Patvirtinta**.

„FastTab“ **Klientai** rodo klientų hierarchiją. Norėdami pasirinkti klientus, kuriems lėšos skiriamos, nuvilkite juos į skiltį **Lėšų klientai**. Šiame „FastTab“ taip pat rodoma, kaip paskirstoma bendra lėšų suma.

„FastTab“ **Prekės** rodomos prekės, kurios įtrauktos į akciją.

### <a name="trade-allowance-agreement"></a>Prekybos nuolaidų sutartis

Kai lėšų aprašas nustatytas, kitas akcijos planavimo veiksmas yra akcijų sutarčių (kurios vadinamos prekybos nuolaidų sutartimis) užregistravimas, lėšų paskirstymas ir kiekvieno pardavimo įvykio našumo tikslų apibrėžimas.

Prekybos nuolaidų sutartys įrašomos puslapyje **Prekybos nuolaidų sutartys**. Norėdami atidaryti puslapį **Prekybos nuolaidų sutartys** pasirinkite **Pardavimo ir rinkodara** \> **Prekybos nuolaidos** \> **Prekybos nuolaidų sutartys**.

![Prekybos nuolaidų sutarčių puslapis](./media/trade-allowance-management-agreements-page.png "Prekybos nuolaidų sutarčių puslapis")

#### <a name="header"></a>Antraštė

Pasirinkite **Antraštė**, kad perjungtumėte rodinį Antraštė.

„FastTab“ **Bendra** laukai **Užsakymas iki** ir **Užsakymas nuo** nurodo sutarties galiojimo laikotarpį. Sutarties patvirtinimo būsena **Patvirtinta viduje** nurodo, kad sutartis dar negalioja ir negali būti taikoma apdorojant pardavimo užsakymą.

„FastTab“ **Bendra** skiltyje **Analizė** pateikiami svarbūs laukai, kurie nurodo išlaidas ir kiekius, naudojamus vertinant akciją.

- Laukas **Pagrindiniai vienetai** nurodytas produktų kiekis, kurį reikia parduoti pasirinktiems klientams prieš taikant akciją.
- Lauko **Apskaičiuotas siuntimo kiekis** reikšmė apskaičiuojama pagal lauko **Padidėjimo procentas** reikšmę, kuri yra tikslinis padidėjimas, planuojamas šioje akcijoje.
- Laukas **Prekybos nuolaidos išlaidos** apskaičiuojamas pagal įvairių įvykių kiekius prekybos nuolaidos sutartyje.

„FastTab“ **Klientai** kairėje pateiktame sąraše galite pasirinkti ir peržiūrėti klientų grupes, kurios sukonfigūruotos kaip iš anksto nustatytos hierarchijos. Tada visą hierarchiją arba konkrečias sąskaitas galite pasirinkti kaip nuolaidos sutarties paskirties vietas.

„FastTab“ **Prekės** (kaip ir puslapio **Lėšos** „FastTab“ **Prekės**) produktai įtraukiami į sutartį, kad jų pardavimas būtų susietas būtų susietas su sutarta nuolaida.

„FastTab“ **Lėšos** galite peržiūrėti akcijos lėšas, kurios yra susietos su šia sutartimi. Taip pat galite peržiūrėti sutarties įvykio išlaidų paskirstymą. 100 procentų įvykio išlaidų paskirstymas nurodo, kad ši akcija bus finansuojama tik iš vieno fondo. Be to, akcijos sutarties gali būti susieta su keliais fondais, taip pat galima taikyti lygaus arba skirtingo procento paskirstymą.

#### <a name="lines"></a>Eilutės

Tada pasirinkite **Eilutės**, kad perjungtumėte rodinį Eilutės.

Skirtuke **Prekybos įvykiai** rodomi įvykių, kuriems taikoma sutartis, tipai. Įvykiai gali būti trijų tipų: vėliau pateikiama SF, fiksuota suma ir į SF neįtraukta suma.

Kai pasirenkate prekybos įvykį ir tada pasirinkate skirtuką **Sumos**, surandama įvykio informacija.

![Prekybos nuolaidų sutarties eilutės](./media/trade-allowance-management-agreements-lines.png "Prekybos nuolaidų sutarties eilutės")

Skiltyje **Prekybos nuolaidos eilutės** nurodykite kiekio arba sumos diapazoną, kurį klientas turi pasiekti, kad gautų atlygius.

Jei prekybos įvykio tipas yra **Vėliau pateikiama SF**, viršutinėje skirtuko **Sumos** dalyje rodomos taisyklės, pagal kurias vėliau pateikiama SF bus taikoma, generuojama ir apmokama. Pvz., taisyklės gali nurodyti toliau pateiktas vėliau pateikiamos SF paraiškos sąlygas.

- Skaičiavimas paremtas pardavimo užsakymo sukūrimo data (lauko **Skaičiavimo datos tipas** reikšmė yra **Sukurta**).
- Skaičiavimas paremtas pardavimo užsakymo eilutės suma prieš taikant nuolaidas, o ne grynąja suma, kuri apima nuolaidas (lauko **Paimta nuo** reikšmė yra **Bendroji suma**).
- Skaičiavimas paremtas parduotų produktų kiekiu, o ne suma (lauko **Grąžinimo eilutės lūžio tipas** reikšmė yra **Kiekis**).
- Skaičiuojama pagal mėnesio laikotarpį (lauko **Kaupti pardavimą iki** reikšmė yra **Mėnuo**). 
- Padengiama kaip atskaitymas, o ne naudojant mokėtinas sumas (lauko **Mokėjimo tipas** reikšmė yra **Kliento atskaitymai**).

Jei prekybos įvykio tipas **Fiksuota suma**, skirtuke **Sumos** rodomas kiekis, kuris bus klientui sumokėtas atskaitymo būdu, kai klientas pasieks konkretų efektyvumo lygį. Patvirtinimo būsena **Atvira** nurodo, kad fiksuota suma nebuvo neapmokėta.

Jei norite taikyti sutartį pardavimo užsakymams, kurie atitinka su sutarties sąlygas, sutarties būsena turi būti **Patvirtinta**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Suplanuoto prekybos įvykio pardavimo vykdymas ir vėliau pateikiamos SF paraiškų generavimas

Kai kuriate pardavimo užsakymą, kuriame yra eilučių, atitinkančių sutarties reikalavimus, galite peržiūrėti susijusią informaciją puslapyje **Pardavimo užsakymas** pasirinkdami **Pardavimo užsakymo eilutė** \> **Peržiūra** \> **Kainos informacija**.

Puslapio **Kainos informacija** „FastTab“ **Grąžinimai** pardavimo klerkas gali peržiūrėti vėliau pateikiamą SF iš tinkamos prekybos nuolaidos sutarties (rodomas grąžinimo programos ID) ir bendrą sumą, kuri taikoma eilutei. Ši suma taip pat rodoma puslapio **Kainos informacija** skilties **Maržos įvertinimas** lauke **Grąžinimo suma**.

Užregistravus pardavimo SF, sugeneruojama atitinkama kiekvienos SF eilutės vėliau pateikiamos SF paraiška.

> [!NOTE]
> Norėdami peržiūrėti puslapį **Kainos informacija**, puslapio **Gautinų sumų parametrai** skirtuke **Kainos** pasirinkite žymės langelį **Įjungti kainų informaciją**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Paraiškų apdorojimas ir jų konvertavimas į gautinų sumų atskaitymus

Kitas vėliau pateikiamų SF apdorojimo proceso veiksmas yra paraiškų peržiūra, skaičiavimas ir tvirtinimas, o tada – jų konvertavimas į atskaitymus.

Vėliau pateikiamų SF darbo srityje akcijos sutarties savininkas gali reguliariai peržiūrėti ir apdoroti sugeneruotas paraiškas. Be to, joje gautinų sumų administratorius konvertuoja patvirtintas paraiškas į atskaitymus arba įprastinius mokėjimus, atsižvelgiant į paraiškos mokėjimo būdą.

Puslapyje **Vėliau pateikiamų SF darbo sritis** galite peržiūrėti paraiškos eilutes. Jei paraiškų būsena **Reikia perskaičiuoti**, jas reikia perskaičiuoti, kad būtų gautas kaupiamasis poveikis.

### <a name="recalculate-claims"></a>Paraiškų perskaičiavimas

Norėdami perskaičiuoti paraiškas, veiksmų srityje pasirinkite **Kaupti**. Tada dialogo lange **Grąžinimų kaupimas** pasirinkite klientą.

Perskaičiavus programa sugeneruoja naujas sumų paraiškas, kad būtų pakoreguotos pradinės paraiškos nurodant reikalavimus atitinkančią sumą pagal vienetą. Viena koregavimo paraiška sugeneruojama ir priskiriama deriniui, kurį sudaro klientas, prekė, valiuta, matavimo vienetas, atsargų dimensijos, finansinės dimensijos ir PVM grupė. Šios koregavimo paraiškos turi tą pačią nuorodą į pardavimo užsakymo ir SF numerį kaip ir paraiškos, kurios yra koreguojamos (t. y. pradinės paraiškos, sukurtos iš pardavimo dokumento). Skirtingai nuo pradinės paraiškos, koregavimo paraiška neturi reikšmių laukuose, kurie nurodo pradinės pardavimo užsakymo eilutės sumas ir kiekį.

Perskaičiavus būsena pakeičiama į **Apskaičiuota**. Norėdami patvirtinti paraiškas, veiksmų srityje pasirinkite **Tvirtinti**.

### <a name="process-claims-and-pass-them-to-ar"></a>Paraiškų apdorojimas ir jų konvertavimas į gautinas sumas

Dabar paraiškas galima apdoroti kaip gautinas sumas. Norėdami jas apdoroti, veiksmų srityje pasirinkite **Apdoroti**. 

Apdorojus paraiškas, būsena pasikeitė į **Pažymėta** ir ji nurodo, kad žurnalo registravimas (užregistruotas žurnalas grąžinimų kaupimo žurnalas, kaip nurodyta gautinų sumų parametruose) suaktyvino toliau nurodytus įvykius. 

- Paraiškos buvo perkeltos į laikiną kliento balansą kaip atskaitymai.
- Iš grąžinimo kaupimo sąskaitos atskaitytos lėšos siekiant nurodyti būsimų įsipareigojimų klientui sąskaitą.
- Iš grąžinimo išlaidų sąskaitos atskaitytos lėšos siekiant nurodyti išlaidas, kurios buvo patirtos parduodant.

Norėdamas baigti procesą, dabar gautinų sumų klerkas turi tvarkyti kaupimo atskaitymus perkeldamas juos į klientų balansą kaip kredito pažymą (įsipareigojimą). 

Norėdami pradėti užduotį, puslapio **Klientas** veiksmų srityje pasirinkite **Rinkti** \> **Sudengti operacijas**. Tada puslapyje **Operacijų sudengimas** pasirinkite **Funkcijos** \> **Vėliau pateikiamų SF programa**. Šiame grąžinimo puslapyje rodomos visos vėliau pateikimų SF paraiškos, apdorotos anksčiau.

Jei norite kurti kredito pažymą, visose eilutėse pasirinkite žymės langelį **Pažymėta**, o tada pasirinkite **Funkcijos** \> **Kurti kredito pažymą**.

Sukūrus kredito pažymą, užregistruojamas žurnalas. (Užregistruotas žurnalas yra gautinų sumų sunaudojimo žurnalas, kaip nurodyta gautinų sumų parametruose). Todėl realaus įsipareigojimo (kredito) suma buvo perkelta į kliento balansą. Finansiškai ši situacija nurodo, kad įvyko toliau nurodyti įvykiai.

- Lėšos pervestos į kliento gautinų sumų sąskaitą.
- Lėšos atskaitytos nuo grąžinimo kaupimo sąskaitos.

Norėdami patvirtinti prekybos įvykį, kurio tipas **Fiksuota suma**, pasirinkite įvykį puslapyje **Prekybos nuolaidų sutartys**, tada skirtuke **Suma** pasirinkite **Tvirtinti**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Mokėtino atskaitymo sudengimas ir kliento trumpas mokėjimas naudojant atskaitymo darbo sritį

Dažnai tikėdamiesi vėliau pateikiamų SF klientai pasirenka trumpo mokėjimo SF. Siekdamas išvengti mokėjimo suderinimo problemų ateityje, gautinų sumų klerkas užregistruoja tuos trumpus mokėjimus kaip atskaitymus, kai jis įrašo faktinius kliento mokėjimus. Tada atskaitymo darbo srityje tuos kliento atskaitymus galima lengvai sudengti pagal paraiškų sumas, kurias įmonė turi sumokėti.

Norėdami registruoti kliento trumpą mokėjimą mokėjimo žurnale, pasirinkite **Gautinos sumos** \> **Mokėjimai** \> **Mokėjimo žurnalas** ir sukurkite naują mokėjimo žurnalą. Veiksmų srityje pasirinkite **Atskaitymai**. Puslapyje **Atskaitymas** galite kurti ir sekti trumpo mokėjimo sumą.

Surinkimo vadovas dabar yra atsakingas už atviros kredito pažymos operacijos ir trumpo mokėjimo operacijos sudengimą atskaitymo darbo srityje.

Norėdami valdyti atskaitymus, pasirinkite **Pardavimas ir rinkodara** \> **Prekybos nuolaidos** \> **Atskaitymai** \> **Atskaitymo darbo sritis**. Viršutinėje puslapio srityje pateikiamos eilutės, kurios nurodo trumpus mokėjimus iš kliento. Apatinėje puslapio srityje pateikiamos klientų atviros kredito operacijos. 

Norėdami sudengti atskaitymą pagal atvirą operaciją, pažymėkite atskaitymo eilutę ir tada skirtuke Atviros operacijos pažymėkite eilutę. Veiksmų srityje spustelėkite Tvarkyti > Gretinti.

Dabar pradinių paraiškų būsena nustatyta į parinktį **Baigta**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Akcijos ir lėšų sunaudojimo efektyvumo analizavimas

Norėdami peržiūrėti pagrindinę programos statistiką ir lėšų sunaudojimo informaciją, galite naudoti kelias ataskaitas ir analizės rodinius, kurie pateikiami prekybos nuolaidų valdymo puslapyje.

Puslapio **Prekybos nuolaidų veikla** skirtuke **Apžvalga** rodoma pagrindinė informacija apie prekybos nuolaidos sutartį. Kituose skirtukuose rodoma konkretesnė informacija apie susietus dokumentus, mokėjimus ir kitus įvykius, kurie yra susiję su programa.

Skirtuke **Suvestinė** rodoma informacija apie bendrą parduotų akcijos produktų kiekį, pardavimo sumą, kurios SF išrašyta, ir apmokėtas vėliau pateikiamas SF bei fiksuotas sumas.

Skirtuke **Vėliau pateikiamų SF kreditai** pateikiama informacija apie atskiras vėliau pateikiamas SF, kurios buvo išduotos klientui.

Norėdami išsamiau išanalizuoti įvairius akcijos efektyvumo rodiklius, galite naudoti rodinį Analizė. Norėdami atidaryti rodinį Analizė, spustelėkite **Pardavimas ir rinkodara** \> **Prekybos nuolaidos** \> **Prekybos nuolaidų sutartys**. Veiksmų srityje spustelėkite **Analizė**.  

Norėdami išsamiau išanalizuoti įvairius akcijos efektyvumo rodiklius, galite naudoti rodinį Analizė. Norėdami atidaryti rodinį Analizė, spustelėkite **Pardavimas ir rinkodara** \> **Prekybos nuolaidos** \> **Prekybos nuolaidų sutartys**. Veiksmų srityje spustelėkite **Analizė**. 

