---
title: Pavojingų medžiagų nustatymas
description: Šioje temoje paaiškinama kaip nustatyti duomenis, reikalingus klasifikuoti prekes kaip pavojingas medžiagas. Kai kuriate pardavimo užsakymą, kuriame yra prekė, klasifikuojama kaip pavojinga medžiaga, sistema sugeneruoja pavojingos prekės dokumentaciją tam pardavimo užsakymui, kai jis yra išsiunčiamas.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ac6a9b4316fa260a86c124f86d04645625e9b808
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577437"
---
# <a name="set-up-hazardous-materials"></a>Pavojingų medžiagų nustatymas

[!include [banner](../includes/banner.md)]

Kad galėtumėte naudoti pavojingų medžiagų funkciją, pirma turite nustatyti duomenis, reikalingus klasifikuoti prekes kaip pavojingas medžiagas. Tada, kai kuriate pardavimo užsakymą, kuriame yra prekė, klasifikuojama kaip pavojinga medžiaga, sistema sugeneruoja pavojingos prekės dokumentaciją tam pardavimo užsakymui, kai jis yra išsiunčiamas.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Pavojingų medžiagų funkcijos įjungimas Jūsų sistemoje

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Produkto informacijos valdymas*
- **Funkcijos pavadinimas:** *Pavojingų medžiagų produkto informacija ir siuntimo dokumentacija*

## <a name="hazardous-material-regulations"></a>Pavojingų medžiagų nuostatos

Norėdami naudoti pavojingų medžiagų procesus, pirma turite sukurti nuostatą. Nuostatos apibrėžia, kaip spausdintas siuntimo tekstas yra kuriamas prekei. Jos taip pat apibrėžia susijusius pristatymo būdus.

Kai kurios bendrosios nuostatos:

- **ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais
- **CFR 49** – pavojingų krovinių gabenimo Jungtinėse Valstijose nuostatos
- **IMDG** – Tarptautinis jūra gabenamų pavojingų krovinių (IMDG) kodeksas
- **IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos

Šios nuostatos padeda nuspręsti kokia informacija turi būti rodoma, kuomet spausdinate prekės siuntimo tekstą. Galite apibrėžti tiek nuostatų, kiek jų turite atitikti.

> [!IMPORTANT]
> Informacijos kodų, susijusių su pavojingomis medžiagomis, nustatymo funkcija nepadaro taip, kad Jūsų įmonė atitiktų nuostatas. Tai tik įrankis, padedantis sukurti Jūsų kompanijos procesus.

Įprastai, nuostata yra prieinama tam tikram transportavimo būdui, pavyzdžiui jūros, sausumos ar oro transportui. Taigi, galite susieti kiekvieną nuostatą su pristatymo būdu. Pristatymo būdas bus naudojamas, kai tam tikri dokumentui bus spausdinami sandėlio valdyme. Sandėlio valdyme kiekviena siunta yra susieta su siuntos vežėju ir vežėjo tarnyba, kurie yra nustatomi **Transportavimas** modulyje. Pristatymo būdas yra susietas su siuntos vežėju ir vežėjo tarnyba. Kai paleidžiate ataskaitą, pristatymo būdas naudojamas surasti siuntimo spausdintą tekstą, susietą su išleista preke.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui (įmonei). Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Kiekvienai nuostatai galite apibrėžti medžiagų sąrašą ir naudoti jį kaip šablonų sąrašą, siejamą su išleistomis prekėmis. Kiekvienai nuostatai taip pat galite apibrėžti spausdinimo nustatymus. Spausdinimo nustatymai leidžia Jums nuspręsti kaip konstruojamas prekės siuntimo tekstas. Spausdinimo nustatymai naudojami konstruoti siuntimo spausdinimo tekstą išleistai prekei.

Norėdami nustatyti pavojingų medžiagų nuostatas, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų nuostatos**. Puslapyje **Pavojingų medžiagų nuostatos** galite sukurti kiek norite nuostatų ir jas konfigūruoti, naudodami laukus, aprašomus tolesniuose poskyriuose.

### <a name="hazardous-material-regulation-header"></a>Pavojingų medžiagų nuostatos antraštė

Kiekviena nuostata turi kodą ir aprašą. Šioje lentelėje apibūdinami laukai, galimi antraštėje.

| Laukas | Aprašas |
|---|---|
| Nuostatos kodas | Įveskite kodą pavojingų medžiagų nuostatos įrašo identifikacijai. |
| Aprašas | Įveskite pavojingų medžiagų nuostatos aprašą. |

### <a name="print-setup-fasttab"></a>Spausdinimo nustatymas „FastTab”

Kiekviena nuostata gali turėti neribotą spausdinimo nustatymų skaičių. Jūs apibrėžiate spausdinimo nustatymus **Spausdinimo nustatymai** „FastTab”. Šioje lentelėje apibūdinami laukai, galimi kiekvienam spausdinimo nustatymui.

| Laukas | Aprašas |
|---|---|
| Seka | Apibrėžkite seką, kuria laukai bus nurodomi spausdinimo tekste. |
| Lauko spausdinimas | Pasirinkite lauką, kurį norite įtraukti į siuntimo tekstą. Ne visus pavojingų medžiagų laukus bus galima spausdinti. Bus galimi tik bendri laukai, naudojami apibrėžti įvairių nuostatų siuntimo tekstui. Jūs turite apibrėžti pirmąjį spausdinimo lauką kaip laukų skyriklį, kurio reikšmė **Seka** yra *0* (nulis), kad jį būtų galima naudoti kaip skyriklį tarp kitų laukų. Reikia tik vienos nuorodos į laukų skyriklį.<p>Galimos šios vertės:</p><ul></li><li>**Laukų skyriklis** – šis spausdinimo laukas naudojamas kaip laukų skyriklis tekstui. Sekai reikalingas tik vienas laukų skyriklis. Įprastai turite nustatyti reikšmę **Seka** šiam spausdinimo laukui į *0* (nulis). Sistema ieškos laukų skyriklio ir naudos pirmąjį, rastą sąraše. Teksto reikšmė, naudojama eilutėje, ateis iš **Spausdinti po** lauko.</li><li>**Identifikacija** – šis spausdinimo laukas įdeda [identifikavimo kodą ir (arba) aprašą](#identification) į spausdinimo tekstą.</li><li>**Klasė** – šis spausdinimo laukas įdeda [klasės kodą ir (arba) aprašą](#classes) į spausdinimo tekstą.</li><li>**Padalinys** – šis spausdinimo laukas įdeda [padalinio kodą ir (arba) aprašą](#divisions) į spausdinimo tekstą.</li><li>**Pakavimo grupė** – šis spausdinimo laukas įdeda [pakavimo grupės kodą ir (arba) aprašą](#packing-group) į spausdinimo tekstą.</li><li>**Tunelio kodas ir (arba) aprašas** – šis spausdinimo laukas įdeda [tunelio kodą ir (arba) aprašą](#tunnel) į spausdinimo tekstą.</li><li>**Tinkamas siuntimo pavadinimas** – šis spausdinimo laukas įdeda [tinkamą siuntimo pavadinimą](hazmat-items.md#hazmat-description) į spausdinimo tekstą.</li><li>**Techninis pavadinimas** – šis spausdinimo laukas įdeda [techninį pavadinimą ir (arba) aprašą](#technical-name) į spausdinimo tekstą.</li><li>**Transportavimo kategorija** – šis spausdinimo laukas įdeda [transportavimo kategorijos kodą ir (arba) aprašą](#transport-category) į spausdinimo tekstą.</li><li>**Laikymas** – šis spausdinimo laukas įdeda [laikymo kodą ir (arba) aprašą](#stowage) į spausdinimo tekstą.</li><li>**Fiksuotas tekstas** – šis spausdinimo laukas įveda tekstą, apibrėžtą **Fiksuotas tekstas** lauke šiai eilutei.</li><li>**Etiketės kodas ir (arba) aprašas** – šis spausdinimo laukas įdeda [etiketės kodą ir (arba) aprašą](#label) į spausdinimo tekstą.</li><li>**Orlaivio pakavimas** – šis spausdinimo laukas įdeda [orlaivio pakavimo instrukcijų kodą ir (arba) aprašą](#packing-instruction) į spausdinimo tekstą.</li><li>**Ribotas kiekis** – šis spausdinimo laukas patikrina ar prekė yra pažymėta kaip [riboto kiekio prekė](hazmat-items.md#material-management) ir, jeigu taip, įveda tekstą, apibrėžtą **Fiksuotas tekstas** lauke šiai eilutei.</li><li>**Pakavimo aprašas** – šis spausdinimo laukas įdeda [pakavimo aprašą](#packing-description) į spausdinimo tekstą.</li></ul> |
| Spausdinti prieš | Įveskite tekstą, kuris turi būti atspausdintas prieš turinį, apibrėžtą **Spausdinimo lauko** nustatymo. |
| Spausdinti po | Įveskite tekstą, kuris turi būti atspausdintas po turinio, apibrėžto **Spausdinimo lauko** nustatymo. |
| Spausdinti su ankstesniu | Pasirinkite šį žymės langelį, kad neleistumėte atspausdinti laukų skyriklio tarp ankstesnio ir šio lauko. Naudokite šį žymės langelį spausdinimo laukams, kurie yra arba pasirinktiniai arba įtraukti į kitą spausdinimo lauką. |
| Fiksuotas tekstas | Jei nustatote lauką **Spausdinimo laukas** į **Fiksuotas tekstas** ar **Ribotas kiekis**, įveskite tekstą, kuris turi būti atspausdintas. |
| Įtraukti į spausdinimą | Pasirinkite reikšmę arba reikšmes, kurios turi būti atspausdintos šiai eilutei, iš pasirinkto spausdinimo lauko. Galite atspausdinti kodą, aprašą arba kodą ir aprašą. |

### <a name="mode-of-delivery-fasttab"></a>Pristatymo būdas „FastTab”

Nuostata yra bendrinama lentelė ir nėra specifinė kiekvienam juridiniam subjektui. Tačiau pristatymo būdai yra specifiniai juridiniam subjektui. Tačiau, kai nustatote pristatymo būdą, privalote pasirinkti santykius tarp nuostatos, juridinio subjekto ir pristatymo būdo.

Ši lentelė apibūdina laukus, kurie galimi **Pristatymo būdas** „FastTab”.

| Laukas | Aprašas |
|---|---|
| Įmonė | Pasirinkite juridinį subjektą susieti su šia nuostata. |
| Pristatymo būdas | Pagal Jūsų pasirinktą juridinį subjektą, pasirinkite pristatymo būdą, kuris turi būti susietas su nuostata. |

### <a name="country-fasttab"></a>Šalies „FastTab”

Nuorodos tikslais, galite išvardyti šalis arba regionus, kuriuose galioja nuostata. Tačiau, kai vykdomos siuntimo ataskaitos, nuostatai nuspręsti naudojamas tik pristatymo būdas. Kai peržiūrite sandėlio siuntą, nėra tiesioginio saito į pristatymo būdą. Siunta gali būti susieta su siuntos vežėju ir vežėjo paslauga. Kai apibrėžiate vežėjo paslaugą, privalote susieti ją su pristatymo būdu. Šis santykis bus naudojamas siuntimo ataskaitoms, tokioms kaip važtaraštis, surasti siuntimo spausdinimo tekstą prekei.

Ši lentelė apibūdina lauką, galimą **Šalis** „FastTab”.

| Laukas | Aprašas |
|---|---|
| Šalis/regionas | Pasirinkite šalį/regioną susieti su nuostata. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Medžiagų kodai

Medžiagų kodai sukuria nustatymus, susijusius su tam tikru pavojingu komponentu, galimai įtrauktu į išleistą produktą. Kiekvienas medžiagos kodas priklauso tam tikros pavojingos medžiagos nuostatai ir jos apibrėžtis turi atitikti tą nuostatą. Kai pritaikote medžiagos kodą išleistam produktui, naudodami **Medžiagos kodas** lauką, visi medžiagos kodo pavojingų medžiagų nustatymai yra automatiškai pritaikomi tam produktui. Todėl išleistų išleistų produktų nustatymo procesas yra greitesnis ir mažiau linkęs į klaidas.

Norėdami tvarkyti Jūsų pavojingų medžiagų apibrėžtis, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų nuostatos**.
2. Pasirinkite nuostatą, kuriai norite nustatyti pavojingos medžiagos apibrėžtį.
3. Veiksmų srities skirtuke **Sąranka** pasirinkite **Pavojingos medžiagos**.
4. Lauke **Medžiagos kodas** įveskite kodą pavojingos medžiagos apibrėžčiai. Jūs pasirinksite šią reikšmę, kai pritaikysite medžiagos kodą išleistam produktui.

    Laukas **Nuostatos kodas** yra tik skaitomas ir rodo nuostatą, kurią pasirinkote 2 veiksme.

5. Naudokite likusius laukus šiame puslapyje kiekvienos pavojingos medžiagos, taikomos Jūsų pasirinktai nuostatai, kūrimui ir nustatymui. Laukai, kurie yra galimi, yra pavojingų medžiagų laukų, galimų atskiriems išleistiems produktams, pogrupis. Norėdami gauti daugiau informacijos žr. [Pavojingos medžiagos produktuose, užsakymuose, siuntose ir kroviniuose](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Pavojingų medžiagų klasifikavimo grupės

Kiekviena pavojingų medžiagų klasifikavimo grupė apibrėžia lauko reikšmių, sukuriančių šabloną, grupę. Šį šabloną galėsite naudoti vėliau, kuomet nustatysite pavojingų medžiagų informaciją išleistai prekei.

Kai priskiriate pavojingų medžiagų klasifikavimo grupės kodą išleistai prekei, informacija, susieta su ta klasifikavimo grupe bus nukopijuota į atitinkamus prekės laukus. Todėl galite supaprastinti nustatymo procesus sukurdami susijusių laukų reikšmių, kurias dažnai naudojate kartu, rinkinį.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Norėdami nustatyti pavojingų medžiagų klasifikavimo grupes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų klasifikavimo grupė**. Puslapyje **Pavojingų medžiagų klasifikavimo grupė** galite sukurti tiek grupių, kiek norite ir konfigūruoti kiekvieną naudodami laukus, apibūdintus šioje lentelėje.

| Laukas | Aprašas |
|---|---|
| Grupės kodas | Įveskite kodą grupės identifikavimui. |
| Aprašas | Įveskite grupės aprašą. |
| Klasės kodas | Susiekite pavojingos medžiagos [klasės kodą](#classes) su grupe. |
| Padalinio kodas | Susiekite pavojingos medžiagos [padalinio kodą](#divisions) su grupe. |
| Pakavimo grupės kodas | Susiekite [pakavimo grupės kodą](#packing-group) su grupe. |
| Transportavimo kategorijos kodas | Susiekite [transportavimo kategorijos kodą](#transport-category) su grupe. |
| Daugiklis | Įveskite pavojingų medžiagų daugiklį, taikomą pasirinktai pavojingų medžiagų klasei ir padaliniui, remiantis taikytina nuostata. Šis daugiklis naudojamas kaip dalis formulės, apskaičiuojančios bendrus *pavojingų medžiagų taškus,* kurie yra įtraukti į krovinį arba siuntą. Norėdami gauti daugiau informacijos apie pavojingų medžiagų taškus ir šį daugiklį, žr. [Medžiagų valdymo „FastTab”](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Pavojingų medžiagų klasės

Pavojingų medžiagų klasė įprastai yra susieta su klasių, pateikiamų nuostatoje, kurią stengiatės atitikti, sąrašu. Pavyzdžiui, pagal JAV nuostatą CFR 49 „3 klasė” yra degūs skysčiai. Galite nustatyti klases, susijusias su medžiagomis, kurias privalote suklasifikuoti.

Kiekviena klasė bus priskirta sąrankai medžiagos sąraše, susijusiame su nuostata. Jūs priskirsite klasę kiekvienai išleistai prekei, kaip privaloma, jog apibūdintumėte pavojingą produkto pobūdį.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Pavojingų medžiagų klasės bendradarbiauja su padaliniais, grupėmis ir suderinamumo grupėmis šiuo būdu:

- Kai priskiriate pavojingų medžiagų klasę išleistai prekei, Jūs taip pat privalote priskirti [pavojingų medžiagų padalinį](#divisions).
- Galite naudoti pavojingų medžiagų klases kartu su [pavojingų medžiagų klasifikavimo grupėmis](#classification-groups) sukurti kodų šabloną prekių nustatymui.
- Galite naudoti [pavojingų medžiagų suderinamumo grupes](#compatibility-groups) nustatyti, kurios pavojingų medžiagų klasės ir padaliniai gali būti gabenami kartu.

Norėdami nustatyti pavojingų medžiagų klases, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų klasės**. Puslapyje **Pavojingų medžiagų klasė** galite sukurti tiek klasių, kiek norite ir konfigūruoti kiekvieną jų naudodami laukus, apibūdintus šioje lentelėje.

| Laukas | Aprašas |
|---|---|
| Klasės kodas | Įveskite kodą šios klasės identifikavimui. Jūs apibrėžiate kodą šiai prekei. Tai bus naudojama peržvalgos sąraše, kai priskirsite pavojingų medžiagų klasę išleistai prekei. |
| Aprašas | Įveskite klasės aprašą. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Pavojingų medžiagų padaliniai

Pavojingų medžiagų padalinys yra pavojingų medžiagų grupės pogrupis. Turite priskirti ir padalinį, ir klasę kiekvienam produktui, kuriame yra pavojingų medžiagų.

Klasėms, kurios neturi jokių padalinių, sukurkite padalinį su kodu *0*. Pavyzdžiui, IATA nuostatoje 7 klasės radioaktyviosios medžiagos neturi padalinių. Šiuo atveju sukursite *0* padalinį, kurį galėsite susieti su išleistu produktu, kai priskirsite klasę.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Pavojingų medžiagų klasės bendradarbiauja su klasėmis, grupėmis ir suderinamumo grupėmis šiais būdais:

- Kai priskiriate pavojingų medžiagų padalinį išleistai prekei, taip pat privalote priskirti [pavojingų medžiagų klasę](#classes).
- Galite naudoti pavojingų medžiagų padalinius kartu su [pavojingų medžiagų klasifikavimo grupėmis](#classification-groups) sukurti kodų šabloną prekių nustatymui.
- Galite naudoti [pavojingų medžiagų suderinamumo grupes](#compatibility-groups) nustatyti, kurios pavojingų medžiagų klasės ir padaliniai gali būti gabenami kartu.

Norėdami nustatyti pavojingų medžiagų klases, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų padalinys**. Puslapyje **Pavojingų medžiagų padalinys** galite sukurti tiek padalinių, kiek norite ir konfigūruoti kiekvieną jų naudodami laukus, apibūdintus šioje lentelėje.

| Laukas | Aprašas |
|---|---|
| Padalinys | Įveskite kodą, naudojamą kaip padalinio nuorodos numerį. |
| Aprašas | Įveskite padalinio aprašą. |
| Klasė | Peržiūrėkite ir priskirkite klasę, kuriai padalinys priklauso. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Pavojingų medžiagų suderinamumo grupės

Pavojingų medžiagų suderinamumo grupės nustato, kurios pavojingų medžiagų klasės ir padaliniai gali būti gabenami kartu. Kai operatoriai kuria sandėlio krovinius ar siuntas, jie gali paleisti suderinamumo patikrą, kuri pateiks įspėjimą, jeigu krovinyje arba siuntoje bus prekių, kurios nepriklauso tai pačiai suderinamumo grupei.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Norėdami nustatyti pavojingų medžiagų suderinamumo grupes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų suderinamumo grupės**. Puslapyje **Pavojingų medžiagų suderinamumo grupė** galite sukurti tiek suderinamumo grupių, kiek norite ir konfigūruoti kiekvieną jų naudodami laukus, apibūdintus šioje lentelėje.

### <a name="hazardous-material-compatibility-group-header"></a>Pavojingų medžiagų suderinamumo grupės antraštė

Kiekviena pavojingų medžiagų suderinamumo grupė turi kodą ir aprašą. Šioje lentelėje apibūdinami laukai, galimi antraštėje.

| Laukas | Aprašas |
|---|---|
| Suderinamumo grupė | Įveskite kodą suderinamumo grupei identifikuoti |
| Aprašas | Įveskite suderinamumo grupės aprašą. |

### <a name="compatibility-group-details"></a>Suderinamumo grupės išsami informacija

Kiekviena suderinamumo grupė nustato pavojingų medžiagų, kurias galima gabenti kartu, klasių ir padalinių sąrašą.

| Laukas | Aprašas |
|---|---|
| Klasė | Pasirinkite pavojingų medžiagų klasę, kuri yra suderinama su visomis kitomis grupės klasėmis. |
| Padalinys | Pasirinkite pavojingų medžiagų padalinį, priklausantį pasirinktai klasei. |

## <a name="hazardous-material-specification-values"></a>Pavojingų medžiagų specifikacijos reikšmės

„Microsoft Dynamics 365 Supply Chain Management” pateikia kelis pavojingų medžiagų specifikacijos tipus. Kiekvienam tipui turite sukurti centralizuotą reikšmių rinkinį kiekviename svarbiame lauke. Vartotojai gali pasirinkti iš šių reikšmių, kai jie konfigūruoja pavojingų medžiagų apibrėžtis arba išleistus produktus. Supply Chain Management pateikia puslapių, kuriuose galite nustatyti reikšmes, kolekciją. Kiekvienas puslapis yra skirtas vienam specifikacijos tipui. Norėdami gauti kiekvienos galimos specifikacijos aprašą ir informaciją, kaip sukurti jos galimas reikšmes, žr. tolesnius poskyrius.

Pavojingų medžiagų specifikacijos pavyzdys – _laikymo kodas_, nurodantis kaip medžiaga gali būti laikoma transportavimo metu. Naudodamiesi šio skyriaus informacija, sukursite laikymo kodų centrinę kolekciją. Tada ši kolekcija bus pristatyta vartotojams išplečiamajame sąraše, kai jie nustatys išleisto produkto laikymo kodą.

Šie nustatymo duomenys nėra specifiniai kiekvienam juridiniam subjektui. Todėl galite turėti bendrą pavojingų medžiagų informacijos rinkinį, bendrinamą su visais Jūsų juridiniais subjektais.

Naudosite [medžiagų kodus](#hazmat-codes) sukurti kiekvienos specifikacijos, taikomos pasirinktai nuostatai, nustatymų bendrą kolekciją. Tada galite taikyti atitinkamą kodą kiekvienam išleistam produktui, kaip privaloma. Norėdami gauti daugiau informacijos apie tai, kaip pritaikyti pavojingų medžiagų kodą tam tikram išleistam produktui ir kaip konfigūruoti asmeninius to produkto nustatymus bet kuriai čia apibūdintai specifikacijai, žr. [Pavojingos medžiagos produktuose, užsakymuose, siuntose ir kroviniuose](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Reagavimas į ekstremalias situacijas dėl pavojingos medžiagos

Specifikacija *Reagavimas į ekstremalias situacijas dėl pavojingos medžiagos* nurodo, kas turi būti padaryta, jeigu įvyksta kažkas blogo, transportuojant produktą, kuriame yra tam tikra pavojinga medžiaga.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų suderinamumo grupės**. Puslapyje **Reagavimas į ekstremalias situacijas dėl pavojingos medžiagos** galite sukurti tiek reikšmių, kiek norite ir konfigūruoti kiekvieną jų su klasifikacijos kodu ir trumpu aprašu.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Pavojingos medžiagos identifikacija

Specifikacija *Pavojingos medžiagos identifikacija* nustato pavojingos medžiagos klasę arba būseną. Reikšmė įprastai yra kodas, paremtas Jungtinių Tautų (JT) standartu. Kiekviena klasė yra identifikuojama kodu ir aprašu ir ji gali nustatyti transportavimo metodų apribojimus. Pavyzdžiui, degios prekės arba medžiagos identifikavimui, sukuriate pavojingų medžiagų klasę, naudojančią kodą *FL* ir aprašą *Degi*. Taip pat nurodote klasę, kuri negali būti transportuojama oru.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos identifikacija**. Puslapyje **Pavojingos medžiagos identifikacija** galite sukurti tiek reikšmių, kiek norite ir konfigūruoti kiekvieną jų naudodami laukus, apibūdintus šioje lentelėje.

| Laukas | Aprašas |
|---|---|
| Identifikacija | Įveskite kodą, kurį naudosite kaip nuorodos numerį, identifikuojantį šią pavojingos medžiagos klasę. |
| Aprašas | Įveskite šios klasės aprašą. |
| Apriboti nuo oro transporto | Pasirinkite šį žymės langelį norėdami nurodyti, kad ši pavojingos medžiagos klasė neturėtų būti transportuojama oru. |
| Apriboti nuo jūros transporto | Pasirinkite šį žymės langelį norėdami nurodyti, kad ši pavojingos medžiagos klasė neturėtų būti transportuojama jūra. |

### <a name="hazardous-material-label"></a><a name="label"></a>Pavojingos medžiagos etiketė

Specifikacija *Pavojingos medžiagos etiketė* nustato pavojingų prekių etiketę, kuri turi būti pritaikyta susijusiems išleistiems produktams. Etiketėse bus apibūdinta kaip produktas turi būti tvarkomas. Pavyzdžiui, turite produktą, kuriame yra nuodingų dujų. Šiuo atveju, nustatote etiketės kodą, atitinkantį nuodingų dujų etiketę. Taip pat sukuriate Jūsų verslo procesą, kad jis peržiūrėtų šią reikšmę gabenant produktus.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos etiketė**. Puslapyje **Pavojingos medžiagos etiketė** galite sukurti tiek etikečių, kiek norite ir konfigūruoti kiekvieną su identifikacijos kodu ir trumpu aprašu.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Pavojingos medžiagos pakavimo aprašai

Specifikacija *Pavojingos medžiagos pakavimo aprašai* nustato kaip pavojinga prekė turi būti pakuojama. Pavyzdžiui, ji gali būti pakuojama tam tikro tipo plieno statinėje arba kitokio tipo specialioje pakuotėje.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos pakavimo aprašai**. Puslapyje **Pavojingos medžiagos pakavimo aprašai** galite sukurti tiek pakavimo aprašų, kiek norite ir konfigūruoti kiekvieną jų su identifikavimo kodu ir trumpu aprašu.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Pavojingos medžiagos pakavimo grupė

Specifikacija *Pavojingos medžiagos pakavimo grupė* nustato pavojingos prekės pakavimo grupę. Pakavimo grupė leidžia Jums apibrėžti kodą ir aprašą, nustatančius kaip pavojingos medžiagos prekė turi būti supakuota transportavimo arba siuntimo metu. Pakavimo grupė yra priskiriama prekei per **Pavojingų medžiagų prekė** puslapį.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos pakavimo grupė**. Puslapyje **Pavojingos medžiagos pakavimo grupė** galite sukurti tiek pakavimo grupių, kiek norite ir konfigūruoti kiekvieną jų su identifikavimo kodu ir trumpu aprašu.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Pavojingos medžiagos pakavimo instrukcija

Specifikacija *Pavojingos medžiagos pakavimo instrukcija* nustato pakavimo instrukcijos, kurių reikia laikytis, kai tam tikra pavojinga prekė ruošiama transportavimui oru.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos pakavimo instrukcija**. Puslapyje **Pavojingos medžiagos pakavimo instrukcija** galite sukurti tiek pakavimo instrukcijos identifikatorių, kiek norite ir konfigūruoti kiekvieną jų su identifikavimo kodu ir trumpu aprašu.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Pavojingos medžiagos laikymas

Specifikacija *Pavojingos medžiagos laikymas* nustato kaip produktas turi būti laikomas laive, kai jis transportuojamas jūros transportu.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos laikymas**. Puslapyje **Pavojingos medžiagos laikymas** galite sukurti tiek laikymo identifikatorių, kiek norite ir konfigūruoti kiekvieną jų su identifikavimo kodu ir trumpu aprašu.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Pavojingų medžiagų transportavimo kategorija

Specifikacija *Pavojingų medžiagų transportavimo kategorija* įprastai naudojama panašių pavojingų produktų grupavimui ataskaitose. Pavyzdžiui, transportavimo kategorijos yra naudojamos **Siuntos suvestinė** ataskaitoje, kurią galite atsispausdinti iš sandėlio siuntos ataskaitos.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų transportavimo kategorija**. Puslapyje **Pavojingų medžiagų transportavimo kategorija** galite sukurti tiek transportavimo kategorijų, kiek norite ir konfigūruoti kiekvieną jų su rodomu pavadinimu ir trumpu aprašu.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Pavojingos medžiagos techninis pavadinimas

Specifikacija *Pavojingos medžiagos techninis pavadinimas* gali būti naudojama pateikti bendrai naudojamą arba vidinį įmonės pavadinimą, apibūdinantį kiekvieną medžiagą.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos techninis pavadinimas**. Puslapyje **Pavojingos medžiagos techninis pavadinimas** galite sukurti tiek techninių pavadinimų, kiek norite ir konfigūruoti kiekvieną jų su rodomu pavadinimu ir trumpu aprašu.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Pavojingos medžiagos tunelis

Specifikacija *Pavojingos medžiagos tunelis* apriboja tunelių, kuriais pavojingos medžiagos gali būti transportuojamos, tipus nustatydami tunelių, kurie turi būti naudojami, tipus. Tunelio kategorijos yra nustatomos pagal taikomas pavojingų medžiagų transportavimo nuostatas. Ši specifikacija įprastai taikoma tik sausumos transportui.

Norėdami nustatyti šios specifikacijos reikšmes, eikite į **Produkto informacijos valdymas \> Sąranka \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos tunelis**. Puslapyje **Pavojingos medžiagos tunelis** galite sukurti tiek tunelio identifikatorių, kiek norite ir konfigūruoti kiekvieną jų su identifikacijos kodu ir trumpu aprašu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]