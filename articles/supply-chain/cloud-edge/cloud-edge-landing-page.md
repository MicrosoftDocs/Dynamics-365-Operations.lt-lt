---
title: Skalės vienetai paskirstytoje topologijoje
description: Šioje temoje pateikiama informacija apie debesies ir briaunos skalės vienetų gamybos ir sandėlio valdymo darbo krūvius.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3111de1f9862cbf926e763f963c86059f4121fc0
ms.sourcegitcommit: 4b7e9d074e368a08d2f75482b722dce0c69a4bbd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/02/2021
ms.locfileid: "7733444"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Skalės vienetai paskirstytoje topologijoje

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> „Microsoft Dynamics 365 Supply Chain Management” skalės vieneto pajėgumas dabar jums prieinamas pagal sąlygas, prižiūrinčias paslaugos naudojimą. Daugiau informacijos rasite [„Microsoft Dynamics“ teisinė informacija](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Kai įgalinsite debesies ir briaunos skalės vienetus, būsite paprašyti patvirtinti, kad suprantate, jog kai kurie duomenys yra susieti su konfigūravimu ir debesies ir briaunos skalės vienetų, kurie gali būti laikomi Jungtinėse Valstijose esančiame duomenų centre, konfigūravimu ir apdorojimu. Norėdami sužinoti daugiau apie debesies ir briaunos skalės vienetų duomenų apdorojimą, skaitykite skyriuje [Duomenų apdorojimą skalės vienetų valdymo metu](#data-processing-management), pateiktame toliau šioje temoje.

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Paskirstytos topologijos pagrindinės vertės pasiūlymas

Įmonės, dirbančios su gamyba ir platinimu, privalo vykdyti pagrindinius verslo procesus 7 dienas per savaitę, 24 valandas per parą be pertrūkių ir laipsniškai. Paskirstyta hibridinė topologija leidžia įmonėms vykdyti pagrindinius kritines misijos gamybos ir sandėlio procesus be pertrūkio, net jei jos susiduria su kartais pasireiškiančiomis tinklo ryšio ar vėlavimo problemomis.

Paskirstytoje pagal topologiją pristatyta skalės vienetų koncepcija, kuri įgalina darbo laiko ir *sandėlio vykdymo* darbo krūvį paskirstyti skirtingose aplinkose. Ši funkcija gali padėti pagerinti efektyvumą, apsaugoti nuo paslaugų pertrūkių ir maksimalizuoti veikimo laiką. Skalės vienetai pateikiami šiais jūsų „Supply Chain Management” prenumeratos priedais:

- „Cloud Scale Unit“ papildinys „Dynamics 365 Supply Chain Management“
- „Edge Scale Unit“ papildinys „Dynamics 365 Supply Chain Management“

Darbo krūvio galimybės yra leidžiamos nepertraukiamai didėjančiais patobulinimais.

## <a name="scale-units-and-dedicated-workloads"></a>Skalės vienetai ir paskirti darbo krūviai

Skalės vienetai išplečia jūsų centrinę „Supply Chain Management“ telkinio aplinką įtraukdami paskirtąjį apdorojimo pajėgumą. Skalės vienetai gali vykti debesyje. Kitu atveju jie gali vykti briaunoje, vietoje, jūsų vietinėse patalpose.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 su skalės vienetais.":::

Skalės vienetai suteikia atsparumą, patikimumą ir skalę paskirtiems darbo krūviams. Briaunos skalės vienetus galima laikinai atjungti nuo debesies telkinio aplinkos, o darbuotojai gali toliau dirbti su priskirtais darbo krūviais briaunoje.

*Darbo krūvis* yra nustatytas verslo funkcijų rinkinys, kuris gali veikti su faktoriais ir būti priskirtas skalės vienetui. Nors sandėlio valdymo darbo krūvis yra išleistas, gamybos vykdymo darbo krūvis vis dar peržiūrimas.

Galite konfigūruoti savo telkinio aplinką ir pasirinktų darbo krūvių debesies skalės vienetus naudodami [Skalės vieneto valdymo portalą](https://sum.dynamics.com). Taip pat galite priskirti kelis darbo krūvius vienam skalės vienetui. Informacijos apie dabartinio leidimo debesies skalės vienetų būtinuosius komponentus ir apribojimus rasite skyriuje [Debesies skalės vienetų būtinieji komponentai ir apribojimai](#cloud-scale-unit-prerequisites), esančiame toliau šioje temoje.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Priskirto sandėlio valdymo darbo krūvio pajėgumai skalės vienete

Sandėlio valdymo darbo krūvis leidžia paleisti sandėlio valdymo procesus diegiant atskirtą sistemą.
Daugiau informacijos rasite [Sandėlio valdymo darbo krūviai debesies ir briaunos skalės vienetams](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Priskirto gamybos vykdymo darbo krūvio pajėgumai skalės vienete

Gamybos darbo krūvis suteikia šias galimybes:

- Mašinos operatoriai ir parduotuvės aukšto vadovai gali prieiti prie operacijos gamybos plano.
- Mašinos operatoriai gali vis atnaujintą planą diskretiškam vykdymui ir proceso gamybos darbams.
- Parduotuvės aukšto vadovas gali keisti operacijos planą.
- Darbuotojai gali prieiti prie atėjimo į darbą ir išėjimo iš darbo laiko ir dalyvavimo briaunoje, siekiant užtikrinti teisingą darbuotojo užmokesčio apskaičiavimą.

Daugiau informacijos rasite [Gamybos vykdymo darbo krūviai debesies ir briaunos skalės vienetams](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Aspektai prieš įjungiant paskirstytąją, hibridinę „Supply Chain Management” topologiją

Įgalindami paskirstytą, hibridinę topologiją, jūs pereinate savo „Supply Chain Management” debesies aplinką, kad ji veiktų kaip telkinys. Taip pat galite susieti papildomas aplinkas, kurios sukonfigūruotos kaip skalės vienetai debesyje arba briaunoje.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a> Debesies skalės vienetų būtinieji komponentai ir apribojimai

Dabartiniame skalės vienetų leidime kai kurios galimybės dar nėra pasiekiamos, bet laikui bėgant, jos gali būti įtrauktos į vėlesnius leidimus.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Jūs turite būti licencijuotas „Supply Chain Management” klientas

Norėdami naudoti paskirstytą topologiją, privalote turėti „Supply Chain Management” licenciją. Jūsų esama debesies aplinka taps telkiniu jūsų hibridinėje topologijoje. Galite deklaruoti tiek smėlio dėžės, tiek gamybos aplinkas kaip telkinio aplinkas ir galite pridėti skalės vienetus pagal jūsų įgytus papildinius.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Jūsų esamą projektą būtina administruoti naudojant visuotinę, komercinę LCS versiją

Jūsų esamas „Microsoft Dynamics Lifecyle Services” (LCS) projektas turi atitikti šiuos versijos reikalavimus:

- Projektą būtina administruoti naudojant visuotinę, komercinę LCS versiją adresu [„lcs.dynamics.com”](https://lcs.dynamics.com).
- Vietinės LCS versijos (pavyzdžiui, [„eu.lcs.dynamics.com”](https://eu.lcs.dynamics.com) ir [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) nėra palaikomos.
- Vyriausybės debesies LCS versijos nėra palaikomos.
- LCS „Mooncake” versija nėra palaikoma.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Jūsų dabartinė gamybos aplinka turi būti Savitarnos tipo LCS sistemoje

Jūsų dabartinė gamybos aplinka turi būti pažymėta kaip **Savitarnos tipo** LCS sistemoje. Šis tipas nurodo, kad jūsų LCS projekto nuomotojas jau buvo konvertuotas taip, kad palaikytų „Azure Service Fabric” išteklių nuomos modelį.

> [!IMPORTANT]
> Aplinkos tipai, kurie veikia kaip infrastruktūros nuomos paslauga (IaaS), nėra palaikomi. Šios aplinkos įprastai žymimos kaip **Valdoma „Microsoft”** tipo LCS sistemoje. Jei turite šio tipo aplinkų, dirbkite kartu su jūsų „Microsoft” kontaktu, kad suprastumėte perkėlimo į **Savitarnos** tipą laiko juostą.

„Microsoft” vykdo visų „Supply Chain Management” debesies aplinkų perėjimą iš „IaaS” modelio į topologiją, nuomojamą „Service Fabric”. Šis perkėlimas suteikia geresnį išplečiamumą ir palengvina paslaugų valdymą. Todėl diegimo ir priežiūros operacijos yra greitesnės. Taip pat, paslaugų komponentai yra perkeliami į mikropaslaugų sąvoką, o paslaugų nuomos modelis [pereis](/virtualization/windowscontainers/about/containers-vs-vm) iš virtualiosios mašinos (VM) modelio į supaprastintą konteinerizuotą architektūrą.

Galiausiai ta pati „Service Fabric” pagrįsta konteinerizuota paslaugų infrastruktūra maitins paslaugos tiek debesies, tiek briaunos egzempliorius, priklausomai nuo to, ar egzempliorius yra telkinys debesyje, ar skalės vienetas debesyje arba briaunoje.

Prieš galėdami naudoti hibridinę topologiją, palaikančią skalės vienetus, jūsų projekto nuomotojas turi pereiti prie modelio, nuomojamo „Service Fabric”. Taip pat, turi būti konvertuojama bet kokia aplinka, kuri veiks kaip centras.

> [!TIP]
> Norėdami pateikti jūsų LCS projekto nuomotojo būsenos užklausą, peržiūrėkite savo aplinkos tipą [LCS sistemoje](https://lcs.dynamics.com/) arba kreipkitės į savo partnerį arba „Microsoft” kontaktą.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Vietos verslo duomenų (vietinės) aplinkos nepalaikomos kaip telkiniai skalės vienetams

Vietinės aplinkos negali veikti kaip telkiniai skalės vienetams. Telkinio aplinkos visada turi būti nuomojamos debesyje.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Skalės vieneto valdymo pajėgumai yra riboti

Valdymo galimybės, galinčios padėti valdyti darbo krūvių judėjimą, yra ribotos. Kai kurios valdymo operacijos nepalaikomos savitarnos būdu, todėl gali prireikti paprašyti pagalbos per savo partnerį arba „Microsoft” kontaktą. Pavyzdžiai apima kai kuriuos darbo krūvių perkėlimus tarp skalės vienetų ir laikinus „ad-hoc” perkėlimus nesėkminguose scenarijuose.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Metrika ir matavimai dar nėra palaikomi

Metrikos ir matavimai, galintys padėti pasirinkti geriausią programą jūsų skalės vienetams, dar nėra prieinami. Dirbkite su savo „Microsoft” kontaktu ar diegimo partneriu, kad pasirinktumėte naudingiausią programą.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a> Duomenų apdorojimas skalės vienetų valdymo metu

Kai įgalinsite „Dynamics 365” aplinką palaikyti paskirstytą, hibridinę topologiją debesies ir briaunos skalės vienetams, kai kurios valdymo paslaugos bus nuomojamos tik Jungtinėse Amerikos Valstijose, kaip ir LCS. Tai daro įtaką kai kurios administravimo ir konfigūravimo informacijos, kurią naudoja [Skalės vienetų valdymo portalas](https://sum.dynamics.com), perkėlimą ir saugojimą. Štai keletas pavyzdžių:

- Jūsų nuomotojo pavadinimai ir ID
- Jūsų LCS projekto ID
- Administratoriaus ir projekto savininko el. pašto adresai, naudojami prisijungimui
- Aplinkos ID telkinio ir skalės vienetams
- Darbo krūvio konfigūracijos, įskaitant juridinių subjektų ir įstaigų pavadinimus bei fizinius adresus, kad jūsų topologija būtų rodoma geografiniame žemėlapyje
- Surinktos metrikos (pavyzdžiui, gaištis ir našumas), kurios bus rodomos žemėlapio analizės puslapyje, kad padėtų jums pasirinkti naudingiausią skalės vienetų naudojimą

Duomenys, perkeliami į ir saugomi JAV duomenų centruose, bus panaikinti pagal „Microsoft” duomenų saugojimo strategijas. „Microsoft“ yra svarbus jūsų privatumas. Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboarding-in-two-stages"></a>Naudojimosi pradžia dvejais etapais

Pasirengimo darbui su paskirstytąja, hibridine topologija procesas turi du etapus. Pirmojo etapo metu turite patikrinti tinkinimus, kad užtikrintumėte, jog jie veikia paskirstytoje topologijoje, turinčioje skalės vienetus. Smėlio dėžės ir gamybos aplinkos yra perkeliamos tik antrajame etape.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>1 etapas: Tinkinimų vieno bloko programavimo aplinkose įvertinimas

Prieš pradedant pasirengimą darbui su jūsų smėlio dėžės arba gamybos aplinkomis, rekomenduojame, kad vystymo nustatyme patyrinėtumėte skalės vienetus, tokius kaip vieno bloko aplinka (taip pat žinoma kaip 1 pakopos aplinka), kad jūs galėtumėte patikrinti procesus, tinkinimus ir sprendimus. Šio etapo metu duomenys ir tinkinimai bus taikomi vieno bloko aplinkoms. Viena aplinka atlieka telkinio vaidmenį, o kita – skalės vieneto. Šis nustatymas suteikia geriausią būdą identifikuoti ir išspręsti problemas. Naujausia ankstyvos prieigos (PEAP) komponavimo versija taip pat gali būti naudojama šiam etapui užbaigti.

1 etapui turėtumėte naudoti [skalės vieneto diegimo įrankius, skirtus vieno bloko vystymo aplinkoms](https://github.com/microsoft/SCMScaleUnitDevTools). Šie įrankiai leidžia jums konfigūruoti telkinio ir skalės vienetus vienoje arba dviejose atskirose vieno bloko aplinkose. Įrankiai yra pateikiami kaip dvejetainis leidimas ir šaltinio kodu „GitHub” platformoje. Skaitykite projekto „wiki”, kuri apima [Išsamų naudojimo vadovą](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), aprašantį, kaip naudojami įrankiai.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>2 etapas: Papildinių įsigijimas ir diegimas jūsų smėlio dėžės ir gamybos aplinkos

Norėdami parengti vieną iš jūsų smėlio dėžės arba gamybos aplinkų į naują topologiją, turite įsigyti papildinius vienam ar daugiau debesies skalės vienetų (o ateityje – ir briaunos skalės vienetams). Papildiniai suteiks atitinkamus projekto ir aplinkos intervalus [„LCS”](https://lcs.dynamics.com/) sistemoje, kad būtų galima diegti skalės vieneto aplinkas.

> [!NOTE]
> Skalės vieneto papildiniai nėra priskirti ribotam vartotojų skaičiumi, ir juos gali naudoti bet kuris esamos prenumeratos vartotojas, remdamasis vaidmenimis, kuriuos priskiria administratorius.

Skalės vienetai yra siūlomi keliuose sandėliavimo vienetuose (SKU) ir kainų parinktyse. Todėl galite pasirinkti tai, kas geriausiai atitinka jūsų suplanuotų mėnesinių operacijų apimtį ir efektyvumo reikalavimus.

Įrašo lygio SKU žinomas kaip *Paprastasis*, o efektyvesnis SKU žinomas kaip *Standartinis*. Kiekvienas SKU yra iš anksto įkeliamas su konkrečiu mėnesinių operacijų skaičiumi. Tačiau galite padidinti mėnesinių operacijų biudžetą įtraukdami pertekliaus papildinius kiekvienam SKU.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Papildiniai debesies skalės vienetams.":::

> [!TIP]
> Norėdami nustatyti geriausiai jūsų poreikius atitinkantį dydį, bendradarbiaukite su savo partneriu ir „Microsoft”, kad suprastumėte kokio mėnesinio operacijų dydžio jums reikia.

Kiekvienas skalės vieneto priedo pirkimas ne tik suteikia mėnesinę operacijų apimtį, bet ir suteikia jums teisę į konkretų aplinkos intervalų skaičių LCS sistemoje. Kiekvienam debesies skalės vieneto papildiniui turite teisę į vieną naują gamybos aplinkos intervalą ir vieną naują smėlio dėžės intervalą. Pasirengimo darbui proceso metu bus įtrauktas naujas LCS projektas, kuriame yra šie intervalai. Intervalų naudojimo teisės yra apribotos, jog intervalai privalo būti naudojami kaip skalės vienetai, turintys debesies telkinį.

Pertekliaus papildiniai nesuteikia jums teisės į naujus aplinkos intervalus.

Jei norite įsigyti daugiau smėlio dėžės aplinkų, galite nusipirkti papildomų įprastinių smėlio dėžės intervalų. Tada „Microsoft” gali padėti jums įgalinti šiuos intervalus kaip smėlio dėžės skalės vienetus, skirtus hibridinei topologijai.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Pasirengimas darbui su paskirstyta, hibridine topologiją, skirta „Supply Chain Management”

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Jūsų LCS projekto nuomotojo ir išsamaus pasirengimo proceso pasirinkimas

Baigę planuoti, kaip jūs pasirengsite darbui su paskirstytąja, hibridine topologija, skirta „Supply Chain Management”, naudosite [Skalės vieneto valdymo portalą](https://aka.ms/SCMSUM) pasirengimo procesui pradėti. Portale pasirinkite skirtuką **„Dynamics 365“ nuomotojai** Jame rodomas nuomotojų sąrašą, kurio dalis yra jūsų paskyra, ir kuriame esate LCS projekto savininkas arba aplinkos administratorius.

Jei nuomotojo, kurio ieškote nėra sąraše, eikite į [„LCS”](https://lcs.dynamics.com/v2) ir užtikrinkite, kad esate aplinkos administratorius ar LCS projekto tam nuomotojui projekto savininkas. Tik „Azure Active Directory“ („Azure AD“) paskyros iš pasirinkto nuomotojo yra įgaliotos užbaigti prisijungimo patirtį.

> [!NOTE]
> Jums pritaikius pakeitimus LCS, gali užtrukti iki 30 minučių, kol nuomotojų sąrašas atspindės pakeitimus.

Kiekvienam nuomotojui sąrašas rodo pasirengimo darbui būseną.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Nuomotojų sąrašas Dynamics 365 nuomotojų skirtuke.":::

Pasirinkite **Paspauskite čia norėdami pradėti**, kad pateiktumėte pasirengimo darbui užklausą LCS nuomotojui. Turite priimti sąlygas. Taip pat turite pateikti verslo el. pašto adresą, į kurį „Microsoft“ gali siųsti pranešimus, susijusius su pasirengimo darbui procesu.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Prisijungimo pateikimas nuomotojui.":::

„Microsoft“ peržiūrės jūsų užklausą ir informuos jus apie kitus žingsnius nusiųsdama el. laišką tuo adresu, kurį pateikėte prisijungimo formoje. „Microsoft” glaudžiai bendradarbiaus su jumis, kad jūsų verslo scenarijui įjungtų skalės vienetus hibridinėje topologijoje.

Kai pasirengimas yra baigtas, galite naudoti prievadą skalės vienetams ir darbo krūviams konfigūruoti.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a> Valdyti skalės vienetus ir darbo krūvius naudojant skalės vieneto tvarkytuvo portalą

Eikite į [Skalės vieneto valdymo portalą](https://aka.ms/SCMSUM) ir prisijunkite naudodami savo nuomotojo paskyrą. Puslapyje **Konfigūruoti skalės vienetus** galite įtraukti telkinio aplinką, jei jos dar nėra. Tada galite rinktis telkinį, kurį norite konfigūruoti su skalės vienetais ir darbo krūviais.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Skalės vieneto tvarkytuvo portalas, sukonfigūruokite skalės vienetų puslapį.":::

Norėdami įtraukti vieną ar keletą skalės vienetų, galimų jūsų prenumeratose, pasirinkite **Įtraukti skalės vienetus**.

Skirtuke **Nustatyti darbo krūviai** naudokite **Sukurti darbo krūvį** mygtuką, kad įtrauktumėte sandėlio valdymo darbo krūvį į vieną iš jūsų skalės vienetų. Kiekvienam darbo krūviui turite nurodyti procesų kontekstą, kurį valdys darbo krūvis. Sandėlio valdymo darbo krūviams kontekstas turi konkretų sandėlį konkrečioje vietoje ir juridinį asmenį.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Apibrėžti darbo krūvių dialogo langą.":::

#### <a name="manage-workloads"></a>Valdyti darbo krūvius

Įgalinę vieną ar daugiau darbo krūvių, naudodami parinktį Tvarkyti darbo krūvius galite inicijuoti ir valdyti procesus, pavyzdžiui, **išvardytus** šioje lentelėje.

| Apdorojimas | Aprašymas |
|---|---|
| Pristabdyti skalės vieneto ryšį | Pristabdyti pardavimo galimybių pranešimus tarp centro ir svarstyklių vieneto. Šio proceso metu bus sustabdytas ryšys ir išeikvotos duomenų galimybės tarp centro ir svarstyklių vienetų. Turite paleisti šį procesą prieš paleisdami tiekimo grandinės valdymo aptarnavimo operaciją centro arba svarstyklių vienetais, tačiau galite tai naudoti ir kitose situacijose. |
| Tęsti skalės vieneto ryšį | Tęsti pardavimo galimybių pranešimus tarp centro ir svarstyklių vieneto. Jums gali reikėti naudoti šį procesą, pvz., po tiekimo grandinės valdymo aptarnavimo operacijos paleidimo ant centro arba svarstyklių vieneto. |
| Naujinti darbo krūvius | Sinchronizuoti naujas funkcijas tarp centro ir skalės vieneto darbo krūvių. Jums gali reikėti naudoti šį procesą, pavyzdžiui, kai aptarnavimas lėmė duomenų mainų užklausų pasikeitimą ir (arba) prie darbo krūvio pridėjote naujas lenteles ar laukus. |
| Perkelti darbo krūvius į svarstyklių vienetą | Suplanuoti darbo krūvį, kuris šiuo metu vykdomas ant svarstyklių vieneto, kad būtų perkeltas į svarstyklių vienetą. Kai vykdomas šis procesas, duomenų sinchronizavimas bus vykdomas, o ir centras, ir skalės vienetas bus nustatyti pakeisti darbo krūvio nuosavybę. |
| Perkelti skalės vienetą į centrą | Planuoti darbo krūvį, kuris šiuo metu vykdomas svarstyklių vienetu, kad būtų perkeltas į centrą. Kai vykdomas šis procesas, duomenų sinchronizavimas bus vykdomas, o ir centras, ir skalės vienetas bus nustatyti pakeisti darbo krūvio nuosavybę.
| Perėjimas nelaimės atveju į centrą | <p>Nedelsiant perkelkite esamą darbo krūvį į centrą. *Šio proceso metu bus pakeisti tik šiuo metu hube galimų duomenų nuosavybės teisės.*</p><p><strong></strong> Perspėjimas: dėl šio proceso gali būti prarasti nesinchronizuoti duomenys ir nepavykęs verslo apdorojimas. Todėl jis turėtų būti naudojamas tik pagal regionus, kur verslo procesai turi būti apdorojami centre, nes svarstyklių vienetas turi panaudą, kurios negalima apriboti per pagrįstą laiką.</p> |
| Perdkirstyta topologija | Pašalinkite skalės vieneto diegimą ir paleiskite tik ant centro, neišsiųsdami darbo krūvio. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Skalės vienetas ir darbo apkrovos valdymo patirtis.":::

> [!TIP]
> Laikui bėgant didėjantys patobulinimai bus įtraukti į Skalės vienetų valdymo patirtį, kad būtų lengviau atlikti ciklo valdymo operacijas. Konkretūs dabartinio leidimo pajėgumai yra dokumentuojami supažindinimo vadove, prieinamu tiems klientams, kurie šiuo metu susipažįsta su paskirstytąja, hibridine „Supply Chain Management” topologija. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
