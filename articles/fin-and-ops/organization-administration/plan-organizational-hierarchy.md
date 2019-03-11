---
title: Organizacijos hierarchijos planavimas
description: Prieš nustatydami organizacijas ir hierarchijas įsitikinkite, kad suprantate, kaip geriausia modeliuoti savo verslą.
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 633d85333a510cec9cee2721e6e2330a47b6c78c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "331994"
---
# <a name="plan-your-organizational-hierarchy"></a>Organizacijos hierarchijos planavimas

[!include [banner](../includes/banner.md)]

Prieš nustatydami organizacijas ir hierarchijas programoje „Microsoft Dynamics 365 for Finance and Operations“, būtinai suplanuokite, kaip bus modeliuojamas jūsų verslas. Organizacijos modelis turi didelės įtakos „Finance and Operations“ diegimui ir verslo procesams.

Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro verslą. Todėl modeliuojant organizacijas svarbiausias aspektas yra jūsų verslo struktūra. Rekomenduojame organizacijos struktūras apibrėžti naudojantis atsiliepimais, gautais iš vadovų ir vyresniųjų vadybininkų, dirbančių įvairiose veiklos srityse, pvz., finansų ir apskaitos, personalo, pagrindinės veiklos, pirkimo ir pardavimo bei rinkodaros.

Planuojant hierarchijas taip pat svarbu atsižvelgti į ryšį tarp organizacijos hierarchijos ir finansinių dimensijų. Galite nustatyti kelias organizacijos hierarchijas, kurios atspindės skirtingus jūsų verslo aspektus. Naudodami finansines dimensijas galite kurti ataskaitas pagal šiuos aspektus. Dirbdami su savo „Microsoft Dynamics 365 for Finance and Operations“ partneriu kurkite hierarchijas, skirtas tiek organizacinio, tiek įstatymuose numatyto ataskaitų teikimo poreikiams.

> [!NOTE]
> Nors juridinius subjektus atstovaujančias finansines dimensijas galite naudoti programoje „Finance and Operations“ nesukurdami juridinių subjektų, finansinės dimensijos nėra skirtos juridinių subjektų veiklos ar verslo poreikiams. Susijusių vienetų apskaitos funkcija programoje „Finance and Operations“ yra skirta tik apskaitos įrašams, kuriuos sukuria kiekviena operacija.

> [!IMPORTANT]
> Neturėtumėte priimti sprendimų dėl organizacijų modeliavimo remdamiesi vien šiame straipsnyje pateikta informacija. Šis dokumentas yra tik vadovas. Papildomų rekomendacijų galite gauti dirbdami su savo „Finance and Operations“ partneriu. Jūsų „Finance and Operations“ partneris turi darbo įvairiuose sektoriuose ir su įvairiais klientais patirties.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Sprendimas, ar vidinės organizacijos bus modeliuojamos kaip juridiniai subjektai, ar kaip valdymo vienetai

Privalote turėti bent vieną programoje „Finance and Operations“ jūsų verslą atstovaujantį juridinį subjektą. Juridinis subjektas gali sudaryti teisines sutartis ir privalo rengti finansines savo veiklos ataskaitas.

Programoje „Finance and Operations“ juridinius subjektus galima naudoti operacijų verslui arba konsolidavimui. Tai reiškia, kad juridinis subjektas programoje „Finance and Operations” nebūtinai atspindi tikrą jūsų verslo subjektą. Pavyzdžiui, operacijose dalyvaujanti įmonė gali turėti pavaldžių juridinių subjektų. Tokiame scenarijuje juridinio subjekto reikia operacijoms, o virtualus juridinis subjektas privalo konsoliduoti pavaldžių juridinių subjektų rezultatus ir balansus.

Vidinės jūsų verslo organizacijos, pvz., regioniniai biurai, gali būti atspindimi kaip papildomi juridiniai subjektai arba kaip pagrindinio juridinio subjekto valdymo vienetai. Valdymo vienetas neprivalo būti teisiškai apibrėžta organizacija. Valdymo vienetai naudojami ekonominiams ištekliams ir veiklos procesams kontroliuoti versle. Valdymo vienetų pavyzdžiai yra skyriai ir išlaidų centrai.

Tam tikros „Finance and Operations“ funkcijos veikia skirtingai priklausomai nuo to, ar organizacija yra juridinis subjektas, ar valdymo vienetas. Priiminėdami sprendimą atidžiai apsvarstykite toliau aprašytas funkcijas.

### <a name="master-data"></a>Bendrieji duomenys

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Tam tikrus pagrindinius duomenis, pvz., klientus, mokėjimo sąlygas, mokesčių įstaigas ir atsargų užsakymą konkrečioje teritorijoje, reikia nustatyti kiekvienam juridiniam subjektui. Tam tikri bendrieji duomenys, pvz., vartotojai, produktai ir didžioji dalis personalo duomenų, yra bendri visiems juridiniams subjektams.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Bendrieji duomenys yra bendri valdymo vienetuose.

### <a name="module-parameters"></a>Modulio parametrai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Moduliams skirti parametrai, pavyzdžiui, gautinų sumų parametrai, mokėtinų sumų parametrai ir grynųjų pinigų ir banko valdymo parametrai turi būti nustatomi kiekvienam juridiniam subjektui. Juridinių subjektų modulių nustatymas atliekamas atskirai, todėl kiekvienas filialas gali laikytis įstatymų reikalavimų ir verslo praktikos. Pavyzdžiui, profesionalių paslaugų juridinis subjektas ir gamybos juridinis subjektas gali turėti skirtingus modulių parametrus, net jei jie atsiskaito tai pačiai pirminei įmonei.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Modulių parametrai yra bendri valdymo vienetuose.

### <a name="data-security"></a>Duomenų sauga

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Daugelis duomenų automatiškai saugomi pagal įmonės ID. Įmonės ID yra unikalus duomenų, susietų su juridiniu subjektu, identifikatorius. Įmonė gali būti susijusi su tik vienu juridiniu subjektu ir juridinis subjektas gali būti susijęs su tik viena įmone. Vartotojai gali pasiekti tik tų įmonių, kurių prieiga jiems suteikta, duomenis. Jums nereikia tinkinti „Finance and Operations“ norint apsaugoti duomenis pagal įmonės ID.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Duomenis galima apsaugoti pagal valdymo vienetą kuriant pritaikytas duomenų saugos strategijas. Duomenų apsaugos strategijos naudojamos prieigai prie duomenų riboti. Pavyzdžiui, tarkime, kad vartotojui leidžiama kurti pirkimo užsakymus tik tam tikrame valdymo vienete. Duomenų apsaugos strategijas galima kurti, kad vartotojas negalėtų pasiekti pirkimo užsakymo duomenų iš jokio kito valdymo vieneto. Operacijų kiekis ir apsaugos strategijų skaičius gali turėti įtakos efektyvumui. Kurdami apsaugos strategijas nepamirškite efektyvumo reikalavimų.

### <a name="ledgers"></a>Didžiosios knygos

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Kiekvienam juridiniam subjektui reikia didžiosios knygos, kurioje yra sąskaitų planas, apskaitos valiuta, ataskaitų valiuta ir finansinis kalendorius. Balansą galima kurti tik juridiniam subjektui. Pagrindines sąskaitas, dimensijas, sąskaitų struktūras, sąskaitų planus ir apskaitos taisykles gali naudoti keli juridiniai subjektai.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Valdymo vienetas negali turėti nuosavos didžiosios knygos informacijos. Jei jūsų vidinėms organizacijoms nereikia unikalių didžiųjų knygų, galite jas modeliuoti kaip valdymo vienetus. Didžiosios knygos informacija bus nustatyta pirminiam juridiniam subjektui hierarchijoje. Pajamų išrašus galima kurti valdymo vienetams, priklausantiems juridiniam subjektui arba pirminiam juridiniam subjektui.

### <a name="fiscal-calendars"></a>Finansiniai kalendoriai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Kiekvienas juridinis subjektas turi nuosavą finansinį kalendorių. Jei jūsų vidinės organizacijos naudoja kitokius finansinius metus ir finansinius kalendorius, organizacijas reikia modeliuoti kaip juridinius subjektus.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Valdymo vienetai turi turėti bendrą finansinį kalendorių. Jei jūsų vidinės organizacijos gali naudoti tuos pačius finansinius metus ir finansinius kalendorius, organizacijas galite modeliuoti kaip valdymo vienetus.

### <a name="consolidation"></a>Konsolidacija

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Norėdami parengti finansines ataskaitas, turite konsoliduoti regioninių biurų finansinius rezultatus į vieną konsoliduotą įmonę.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Konsolidavimas nėra būtinas, nes duomenys jau yra bendrai naudojami valdymo vienetų.

### <a name="centralized-payments"></a>Centralizuoti mokėjimai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Kad visų antrinių juridinių subjektų sąskaitos faktūros galėtų būti apmokamos į vieną pirminį juridinį subjektą arba iš jo, reikia nustatyti centralizuotus mokėjimus.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Centralizuoti mokėjimai nebūtini, nes visos sąskaitos faktūros įrašomos viename juridiniame subjekte.

### <a name="intercompany-transactions"></a>Vidinės įmonės operacijos

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Vidinės įmonės pardavimo užsakymai, pirkimo užsakymai, mokėjimai arba gavimai gali būti taikomi vieni kitiems. Nebūtina naudoti žurnalų kvitų. Vidinės įmonės operacijas galite peržiūrėti antrinės didžiosios knygos lygiu (gautinos sumos, mokėtinos sumos). Toliau pateiktuose pavyzdžiuose parodyta, kaip tvarkomos vidinės įmonės operacijos.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>1 pavyzdys: pagrindinė buveinė teikia paslaugas regioniniams biurams ir turi atgauti tokių paslaugų išlaidas iš regioninių biurų

Jei regioninį biurą modeliuojate kaip juridinį subjektą, turite toliau nurodytas galimybes.

- Pagrindinė buveinė sukuria žurnalo įrašą siekdama atgauti išlaidas iš regioninio biuro. Operacijų negalima skirstyti pagal terminus.
- Pagrindinė buveinė siunčia paslaugų pirkimo užsakymą regioniniam biurui. Regioninio biuro juridiniame subjekte automatiškai sukuriamas pardavimo užsakymas su vidinės įmonės antrinės didžiosios knygos operacijomis.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>2 pavyzdys: pagrindinė buveinė perka paslaugą, kuri suteikiama regioniniam biurui, ir už ją sumoka

Jei regioninį biurą modeliuojate kaip juridinį subjektą, turite toliau nurodytas galimybes.

- Sąskaita faktūra ir mokėjimas atitinka pagrindinei buveinei taikomus įstatyminius reikalavimus. Pagrindinė buveinė gali sukurti žurnalo įrašą siekdama atgauti išlaidas iš regioninio biuro. Operacijų negalima skirstyti pagal terminus.
- Sąskaita faktūra ir mokėjimas atitinka pagrindinei buveinei taikomus įstatyminius reikalavimus. Pagrindinė buveinė gali sukurti vidinės įmonės antrinės didžiosios knygos operaciją.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Vidinės įmonės operacijos tarp valdymo vienetų palaikomos tik naudojant žurnalo kvitus. Valdymo vienetas negali išduoti arba gauti pirkimo užsakymo, pardavimo užsakymo arba sąskaitos faktūros iš kito valdymo vieneto, priklausančio tam pačiam juridiniam subjektui. Negalite peržiūrėti vidinės įmonės operacijų antrinės didžiosios knygos lygiu (gautinos sumos, mokėtinos sumos). Toliau pateiktuose pavyzdžiuose parodyta, kaip tvarkomos vidinės įmonės operacijos.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>1 pavyzdys: pagrindinė buveinė teikia paslaugas regioniniams biurams ir turi atgauti tokių paslaugų išlaidas iš regioninių biurų

Jei regioninį biurą modeliuojate kaip valdymo vienetą, pagrindinė buveinė įveda išlaidų operaciją ir perduoda ją regioniniam biurui.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>2 pavyzdys: pagrindinė buveinė perka paslaugą, kuri suteikiama regioniniam biurui, ir už ją sumoka

Jei modeliuojate regioninį biurą kaip valdymo vienetą, sąskaita faktūra ir mokėjimas turi atitikti pagrindinei buveinei taikomus įstatymų reikalavimus. Sąskaitą faktūrą galima perduoti regioniniam biurui. Pajamų išraše nurodykite regioninio biuro sąnaudas naudodami balansavimo finansinę dimensiją.

### <a name="local-tax-requirements"></a>Vietiniai mokestiniai reikalavimai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Juridiniam subjektui taikomi šalies / regiono, kuriame registruotas juridinis subjektas, mokesčių įstaigos mokesčių įstatymai. Pavyzdžiui, jei juridinis subjektas registruotas Danijoje, jam taikomi Danijos mokesčių įstatymai ir taisyklės. Programoje „Finance and Operations“ juridinis subjektas gali priklausyti tik vienai šaliai / regionui. Šalis / regionas, kurį pasirenkate kaip juridinio subjekto pirminį adresą, kontroliuoja konkrečios šalies / regiono funkcijas, kurios yra prieinamos tam juridiniam subjektui. Pavyzdžiui, jei juridinio subjekto pagrindinis adresas yra Danijoje, įgalinamos funkcijos, susijusios su Danijos mokesčių įstatymais ir taisyklėmis. Tad jei jūsų organizacijos įsikūrusios skirtingose šalyse / regionuose ir joms reikia skirtingų vietinių mokesčių parinkčių, turite nustatyti organizacijas kaip atskirus juridinius subjektus.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Valdymo vienetai naudoja pirminio juridinio subjekto šalies aplinką. Tam pačiam juridiniam subjektui priklausantys valdymo vienetai negali turėti skirtingų šaliai / regionui būdingų reikalavimų. Jei jūsų organizacijos yra toje pačioje šalyje / regione ir naudoja tas pačias mokesčių parinktis, galite nustatyti jas kaip valdymo vienetus.

### <a name="statutory-reporting-for-a-countryregion"></a>Šalies / regiono privalomosios ataskaitos

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Šalims / regionams, kuriuos palaiko „Finance and Operations“, galima sukurti daugumą privalomųjų ataskaitų. Informacijos apie tai, kokios ataskaitos prieinamos kiekvienoje šalyje / regione, ieškokite [„Microsoft Dynamics“ lokalizavimo portale, skirtame „Finance and Operations“](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC). (Reikia „CustomerSource“ prisijungimo.)

> [!NOTE]
> Sprendime „Finance and Operations“ didžiosios knygos registravimo sluoksnis suteikia galimybę atlikti koregavimo įrašus pirminei įmonei, naudojančiai kitą apskaitos standartą nei antrinė įmonė. Pavyzdžiui, įmonėje, kuri naudoja Jungtinės Karalystės visuotinai priimtą apskaitos praktiką (UK GAAP), galite atlikti koregavimo įrašus registravimo sluoksnyje. Šiuos įrašus galima konsoliduoti į pirminę įmonę, kuri naudoja JAV visuotinai priimtus apskaitos principus (GAAP). Koregavimo įrašai neturi įtakos UK GAAP ataskaitoms.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Privalomąsias ataskaitas reikia kurti naudojantis kita programa. Turite užtikrinti, kad „Finance and Operations“ duomenys būtų fiksuojami tenkinant kiekvieno valdymo vieneto reikalavimus, jei jie skiriasi nuo pagrindinės buveinės reikalavimų.

### <a name="currency"></a>Valiuta

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Jei jūsų organizacijos privalo naudoti kitokias funkcines valiutas, jas reikia modeliuoti kaip juridinius subjektus. Funkcinės valiutos nustatomos kiekvienam juridiniam subjektui. Bet galite įvesti operacijas keliomis valiutomis.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Jei jūsų organizacijos gali naudoti vieną funkcinę valiutą, galite modeliuoti organizacijas kaip valdymo vienetus. Valdymo vienetai turi turėti bendrą funkcinę valiutą. Bet galite įvesti operacijas ir kurti ataskaitas keliomis valiutomis.

### <a name="year-end-closing"></a>Uždarymas metų pabaigoje

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Jei skiriasi šalių, kuriose įsikūrusios jūsų organizacijos, įstatymai ir apskaitos praktikos, jums gali reikėti skirtingų metų pabaigos procedūrų kiekvienoje organizacijoje. Tai reiškia, kad turite modeliuoti organizacijas kaip juridinius subjektus. Kiekvienas juridinis subjektas turi nuosavas metų pabaigos procedūras.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Jei šalių, kuriose įsikūrusios jūsų organizacijos, įstatymai ir apskaitos praktikos sutampa, galite naudoti vieną metų pabaigos procedūrų rinkinį. Tai reiškia, kad galite modeliuoti organizacijas kaip valdymo vienetus. Visi valdymo vienetai turi naudoti tą pačią uždarymo metų pabaigoje procedūrą.

### <a name="number-sequences"></a>Numeravimai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Tam tikrų nuorodų numeracijas galima atskirai nustatyti kiekviename juridiniame subjekte. Tam tikros numeracijos gali būti bendros.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Tam tikrų nuorodų numeracijas galima atskirai nustatyti kiekviename valdymo vienete. Tam tikros numeracijos gali būti bendros.

### <a name="products"></a>Produktai

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Produktų apibrėžimai yra bendri, be to, norint įtraukti juos į operacijas, juos reikia patvirtinti konkretiems juridiniams subjektams. Kiekvienas juridinis asmuo turi nuosavą patvirtintų produktų rinkinį, kurį galima įtraukti į operacijų dokumentus. Jei jūsų vidinės organizacijos privalo naudoti skirtingus produktų rinkinius, jas reikia modeliuoti kaip juridinius subjektus.

> [!NOTE]
> Net jei produktų apibrėžimai naudojami bendrai, kiekviename juridiniame subjekte, kuriame buvo patvirtintas produktas, galite nurodyti skirtingus prekės pardavimo, pirkimo ir sandėliavimo parametrus kiekvienoje atsargų teritorijoje.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Visi valdymo vienetai bendrai naudoja tą patį produktų rinkinį. Jei jūsų vidinės organizacijos gali bendrai naudoti tą patį produktų rinkinį, organizacijas galite modeliuoti kaip valdymo vienetus.

### <a name="inquiry-and-reporting"></a>Užklausos ir ataskaitos

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ar organizacija modeliuojama kaip juridinis subjektas

Norėdami įvesti operacijas ir atlikti užklausas keliuose juridiniuose subjektuose, turite pakeisti įmones neautomatiniu būdu. Dėl duomenų saugos apribojimų, konsoliduotos užklausos ir ataskaitos gali reikalauti daug išteklių ir užimti daug laiko.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ar organizacija modeliuojama kaip valdymo vienetas

Keisti įmonių nereikia norint pasiekti duomenis iš kelių valdymo vienetų. Konsoliduotos užklausos ir ataskaitos bei atskira regioninė užklausa atliekama lengviau ir greičiau.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Geriausia organizacijų ir hierarchijų modeliavimo praktika

Įgyvendindami organizacijos hierarchiją, atsižvelkite į šiuos geriausios praktikos pavyzdžius:

- Norėdami modeliuoti juridinio subjekto ir verslo struktūros vieneto sankirtą, sukurkite skyrių. Tada galite pridėti duomenis iš skyriaus prie juridinio subjekto privalomosioms ataskaitoms ir iš skyriaus prie verslo struktūros vieneto vidinėms ataskaitoms. Skyriai gali veikti kaip pelno centrai. Jei naudojate skyrius, neprivalote naudoti juridinių subjektų ir verslo struktūros vienetų kai dimensijų sąskaitos struktūroje. Kaip dimensiją galite naudoti tik skyrius. Bet privalote naudoti išlaidų centrus ir skyrius kaip dimensijas sąskaitos struktūroje, jei išlaidų centrai naudojami tik kaip išlaidų kaupimo vienetai, o skyriai naudojami įplaukų pripažinimui.
- Jei taikote sudėtingus reikalavimus pelno ir nuostolio nurodymui ataskaitose, modeliuokite kelias hierarchijas valdymo vienetams.
- Viename juridiniame subjekte nemodeliuokite kelių hierarchijų tam pačiam hierarchijos tikslui.
- Nekurkite hierarchijos kiekvienam tikslui. Paprastai vieną hierarchiją galite naudoti keliems tikslams. Pavyzdžiui, vieną valdymo vienetų hierarchiją galima priskirti visiems su strategija susijusiems tikslams.
- Kurkite subalansuotas hierarchijas. Hierarchijoje visi mazgai, esantys tokiu pačiu atstumu nuo šakninio mazgo, apibrėžiami kaip lygis. Subalansuotoje hierarchijoje kiekviename lygyje gali būti tik vieno tipo valdymo vienetas, o atstumas nuo šakninio mazgo iki kiekvieno lygio yra nuoseklus. Jei tarp skyriaus ir juridinio subjekto arba verslo struktūros vieneto yra tarpinių lygių, norint sukurti subalansuotą hierarchiją gali reikėti organizacijų-rezervavimo ženklų.
- Nemodeliuokite atskiros valdymo vienetų hierarchijos, jei juridinių subjektų struktūra yra ir jūsų valdymo struktūra. Mišri juridinių subjektų ir valdymo vienetų hierarchija gali tarnauti abiem tikslams.
- Prieš modeliuodami pagrindinius pertvarkymo scenarijus, poveikio analizei ir tikrinimo bandymui atlikti naudokite hierarchijos įsigaliojimo datas.
- Naudodami juodraščio režimą pakeiskite hierarchiją prieš publikuodami naują versiją gamybos aplinkoje.
- Ribokite skaičių žmonių, turinčių teisę įtraukti organizacijos į hierarchiją arba šalinti iš jos gamybos aplinkoje. Mažesnis skaičius sumažina brangių klaidų ir reikalingų taisymų pavojų.
