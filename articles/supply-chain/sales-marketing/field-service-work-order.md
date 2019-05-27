---
title: „Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ pardavimo užsakymais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 49cb5942532e4feab64aa271ebfecf5cb60b1c61
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562723"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ pardavimo užsakymais

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su „Microsoft Dynamics 365 for Finance and Operations“ pardavimo užsakymus.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/field-service-integration.png)](./media/field-service-integration.png)

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau nurodyti šablonai ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais.

### <a name="names-of-the-templates-in-data-integration"></a>Šablonų pavadinimai naudojant funkciją Duomenų integravimas

Sinchronizuojant naudojamas šablonas **Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“)**.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Užduočių pavadinimai projekte Duomenų integravimas

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Prieš sinchronizuojant pardavimo užsakymo antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- „Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)
- Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| **Field Service** | **„Finance and Operations”** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS pardavimo užsakymų antraštės |
| msdyn_workorderservices | CDS pardavimo užsakymo eilutės   |
| msdyn_workorderproducts | CDS pardavimo užsakymo eilutės   |

## <a name="entity-flow"></a>Objekto srautas

Darbo užsakymai kuriami „Field Service“. Jei darbo užsakymai apima tik išoriškai tvarkomus produktus, o parinkties **Darbo užsakymo būsena** reikšmė nėra **Atidarytas – nesuplanuotas** arba **Uždarytas – atšauktas**, darbo užsakymus galima sinchronizuoti su „Finance and Operations“ naudojant CDS duomenų integravimo projektą. Darbo užsakymų naujinimai bus sinchronizuojami kaip „Finance and Operations“ pardavimo užsakymai. Šie naujinimai apima informaciją apie pradinį tipą ir būseną.

## <a name="estimated-versus-used"></a>Numatoma ir naudojama

„Field Service“ darbo užsakymų produktų ir paslaugų kiekiams bei sumoms priskiriamos reikšmės **Numatoma** ir **Naudojama**. Tačiau „Finance and Operations“ pardavimo užsakymuose tokio pačio tipo reikšmės **Numatoma** ir **Naudojama** nenaudojamos. Du užduočių rinkiniai sinchronizuoja darbo užsakymo produktus ir paslaugas, kad būtų palaikomas produktų paskirstymas, kuris naudoja numatomą kiekį „Finance and Operations“ pardavimo užsakyme, bet kad būtų išlaikytas naudojamas kiekis, kuris turėtų būti vartojamas ir už kurį turėtų būti išrašyta SF. Vienas užduočių rinkinys skirtas tipo **Numatoma** reikšmėms, o kitas užduočių rinkinys skirtas tipo **Naudojama** reikšmėms.

Dėl šios elgsenos galimi atvejai, kai numatomos reikšmės naudojamos „Finance and Operations“ paskirstant arba rezervuojant, o naudojamos reikšmės naudojamos vartojant ir išrašant SF.

### <a name="estimated"></a>Įvertinta

Sinchronizuojant produkto eilutes, tipo **Numatoma** reikšmės naudojamos, kai parinkties **Eilutės būsena** reikšmė yra **Numatoma**, nustatyta parinkties **Paskirstyta** reikšmė **Taip**, o parinkties **Sistemos būsena** reikšmė nėra **Uždarytas – užregistruotas**.

Sinchronizuojant paslaugos eilutes, tipo **Numatoma** reikšmės naudojamos, kai parinkties **Eilutės būsena** reikšmė yra **Numatoma**, o parinkties **Sistemos būsena** reikšmė nėra **Uždarytas – užregistruotas**.

### <a name="used"></a>Naudota

Tipo **Naudojama** reikšmės naudojamos vartojant ir išrašant SF. Tokiais atvejais tipo **Naudojama** reikšmės yra sinchronizuojamos.

Tolesnėje lentelėje pateikiama įvairių produkto eilučių derinių apžvalga.

| Sistemos būsena <br>(Field Service) | Eilutės būsena <br>(Field Service) | Paskirstytas <br>(Field Service) |Sinchronizuojama reikšmė <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Atidarytas – suplanuotas   | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – suplanuotas   | Įvertinta   | Nr.        | Naudota                            |
| Atidarytas – suplanuotas   | Naudota        | Taip       | Naudota                            |
| Atidarytas – suplanuotas   | Naudota        | Nr.        | Naudota                            |
| Atidarytas – vykdomas | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – vykdomas | Įvertinta   | Nr.        | Naudota                            |
| Atidarytas – vykdomas | Naudota        | Taip       | Naudota                            |
| Atidarytas – vykdomas | Naudota        | Nr.        | Naudota                            |
| Atidarytas – baigtas   | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – baigtas   | Įvertinta   | Nr.        | Naudota                            |
| Atidarytas – baigtas   | Naudota        | Taip       | Naudota                            |
| Atidarytas – baigtas   | Naudota        | Nr.        | Naudota                            |
| Uždarytas – užregistruotas    | Įvertinta   | Taip       | Naudota                            |
| Uždarytas – užregistruotas    | Įvertinta   | Nr.        | Naudota                            |
| Uždarytas – užregistruotas    | Naudota        | Taip       | Naudota                            |
| Uždarytas – užregistruotas    | Naudota        | Nr.        | Naudota                            |

Tolesnėje lentelėje pateikiama įvairių paslaugos eilučių derinių apžvalga.

| Sistemos būsena <br>(Field Service) | Eilutės būsena <br>(Field Service) | Sinchronizuojama reikšmė <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Atidarytas – suplanuotas   | Įvertinta   | Įvertinta |
| Atidarytas – suplanuotas   | Naudota        | Naudota      |
| Atidarytas – vykdomas | Įvertinta   | Įvertinta |
| Atidarytas – vykdomas | Naudota        | Naudota      |
| Atidarytas – baigtas   | Įvertinta   | Įvertinta |
| Atidarytas – baigtas   | Naudota        | Naudota      |
| Uždarytas – užregistruotas    | Įvertinta   | Naudota      |
| Uždarytas – užregistruotas    | Naudota        | Naudota      |

Tipo **Numatoma** reikšmių sinchronizavimas, lyginant su tipo **Naudojama** reikšmėmis, valdomas naudojant du produkto eilučių ir paslaugos eilučių užduočių rinkinius. Iš anksto nustatyti filtrai suaktyvina teisingą užduotį, o pagrindinis susiejimas padeda užtikrinti, kad sinchronizuojamos tinkamos tipo **Numatoma** lyginant su tipu **Naudojama** reikšmės.

### <a name="example"></a>Pavyzdys

1. „Field Service“ sukuriamas ir suplanuojamas darbo užsakymas.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – suplanuotas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 0 vnt., eilutės būsena = numatoma, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 0 h, eilutės būsena = numatoma

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **0** (nulis) ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Finance and Operations“.

2. Produktai paskirstomi „Field Service“.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – suplanuotas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 0 vnt., eilutės būsena = numatoma, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 0 h, eilutės būsena = numatoma

    Šiame pavyzdyje produkto lauko **Numatomas kiekis** reikšmė **5 vnt.** ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Finance and Operations“.

3. Paslaugos technikas pradeda dirbti su darbo užsakymu ir užregistruoja medžiagų naudojimą, nurodydamas kiekį 6.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – vykdomas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 6 vnt., eilutės būsena = naudojama, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 0 h, eilutės būsena = numatoma

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **6** ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Finance and Operations“.

4. Paslaugos technikas baigia darbo užsakymą ir užregistruoja 1,5 valandos naudojimo laiką.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – baigtas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 6 vnt., eilutės būsena = naudojama, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 1,5 h, eilutės būsena = naudojama

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **6** ir paslaugos lauko **Naudojamas kiekis** reikšmė **1,5 h** sinchronizuojamos su „Finance and Operations“.

## <a name="sales-order-origin-and-status"></a>Pardavimo užsakymo kilmė ir būsena

### <a name="sales-origin"></a>Pard. šaltinis

Norėdami sekti „Finance and Operations“ pardavimo užsakymus, kurie sukurti iš darbo užsakymų, galite kurti pardavimo kilmę, kai nustatyta parinkties **Kilmės tipo priskyrimas** reikšmė **Taip** ir nustatyta lauko **Pardavimo kilmės tipas** reikšmė **Darbo užsakymo integravimas**.

Pagal numatytuosius parametrus susiejant pasirenkama visų pardavimo užsakymų, kurie sukurti iš darbo užsakymų, pardavimo kilmės tipo **Darbo užsakymo integravimas** pardavimo kilmė. Tai gali būti naudinga, kai dirbate su pardavimo užsakymu „Finance and Operations“. Turite įsitikinti, kad pardavimo užsakymai, kilę iš darbo užsakymų, nėra atgaliniu ryšiu sinchronizuojami su „Field Service“ kaip darbo užsakymai.

Informacijos apie tai, kaip kurti teisingą pardavimo kilmės sąranką „Finance and Operations“, žr. temoje „Išankstinės sąlygos ir susiejimo sąranka“.

### <a name="status"></a>Būsena

Kai pardavimo užsakymas sukuriamas iš darbo užsakymo, laukas **Išorinė darbo užsakymo būsena** rodomas pardavimo užsakymo antraštės skirtuke **Sąranka**. Šiame lauke rodoma „Field Service“ darbo užsakymo sistemos būsena, kad „Finance and Operations“ būtų lengviau sekti pardavimo užsakymų sinchronizuojamų darbo užsakymų būseną. Šis laukas taip pat gali padėti „Finance and Operations“ vartotojui nustatyti, kada pardavimo užsakymas turėtų būti išsiųstas arba kada turėtų būti išrašyta jo SF.

Lauke **Išorinė darbo užsakymo būsena** naudojamos toliau nurodytos reikšmės.

- Atidarytas – suplanuotas
- Atidarytas – vykdomas
- Atidarytas – baigtas
- Uždarytas – užregistruotas

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas

Reikalinga papildoma funkcija iš „Field Service“ CRM sprendimo, kad būtų palaikomas „Field Service ir „Finance and Operations“ integravimas. Sprendimas apima toliau nurodytus keitimus.

### <a name="work-order-entity"></a>Objektas Darbo užsakymas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymą sudaro tik išoriškai tvarkomi produktai. Darbo užsakymą sudaro tik išoriškai tvarkomi produktai, kai visi susiję produktai tvarkomi „Finance and Operations“. Šis laukas padeda užtikrinti, kad vartotojai sinchronizuotų darbo užsakymus, kuriuose pateikti „Finance and Operations“ neatpažįstami produktai.

### <a name="work-order-product-entity"></a>Objektas Darbo užsakymo produktas

- Laukas **Užsakymą sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymo produktas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymo produktas tvarkomas „Finance and Operations“. Šis laukas padeda užtikrinti, kad vartotojai sinchronizuotų darbo užsakymų produktus, kurių „Finance and Operations“ neatpažįsta.
- Laukas **Antraštės sistemos būsena** įtrauktas į objektą **Darbo užsakymo produktas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti darbo užsakymo sistemos būseną, ir jis padeda užtikrinti teisingą filtravimą, kai darbo užsakymo produktai sinchronizuojami su „Finance and Operations“. Kai filtrai nustatyti integravimo užduotyse, lauko **Antraštės sistemos būsena** informacija taip pat naudojama siekiant nustatyti, ar sinchronizuoti numatomas reikšmes, ar naudojamas reikšmes.
- Lauke **SF vieneto suma** rodoma SF suma už faktinį naudojamą vienetą. Reikšmė apskaičiuojama kaip lauko **Bendra suma** reikšmė, padalyta iš lauko **Faktinis kiekis** reikšmės. Laukas naudojamas integruojant su sistemomis, kurios nepalaiko skirtingų naudojamo kiekio ir kiekio, kurio SF išrašyta, reikšmių. Šis laukas nerodomas vartotojo sąsajoje. 
- Lauko **SF nuolaidos suma** reikšmė apskaičiuojama kaip lauko **Nuolaidos sumos** reikšmės ir suapvalintos apskaičiuotos lauko **SF vieneto suma** reikšmės suma. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **Dešimtainis kiekis** saugoma reikšmė iš lauko **Kiekis**, pateikiama kaip dešimtainis skaičius. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas. 
- Laukų **Naudojama** reikšmė atkuriama į **0** (nulis), jei darbo užsakymo produkto lauko **Eilutės būsena** reikšmė pakeičiama iš **Naudojama** į **Numatoma**. Šis pakeitimas padeda išvengti situacijų, kuriose klaidingai įvestas naudojamas kiekis yra naudojamas sinchronizuojant, kai lauko **Eilutės būsena** reikšmė yra **Numatoma** ir nustatyta parinkties **Paskirstyta** reikšmė **Ne**.

### <a name="work-order-service-entity"></a>Objektas Darbo užsakymo paslauga

- Laukas **Užsakymą sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymo paslauga** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymo paslauga tvarkoma „Finance and Operations“. Šis laukas padeda užtikrinti, kad vartotojai sinchronizuotų darbo užsakymų paslaugas, kurių „Finance and Operations“ neatpažįsta.
- Laukas **Antraštės sistemos būsena** įtrauktas į objektą **Darbo užsakymo paslauga** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti darbo užsakymo sistemos būseną, ir jis padeda užtikrinti teisingą filtravimą, kai darbo užsakymo paslaugos sinchronizuojamos su „Finance and Operations“. Kai filtrai nustatyti integravimo užduotyse, lauko **Antraštės sistemos būsena** informacija taip pat naudojama siekiant nustatyti, ar sinchronizuoti numatomas reikšmes, ar naudojamas reikšmes.
- Lauke **Trukmė valandomis** saugoma reikšmė iš lauko **Trukmė**, paversta iš minučių į valandas. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **Numatoma trukmė valandomis** saugoma reikšmė iš lauko **Numatoma trukmė**, paversta iš minučių į valandas. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **SF vieneto suma** rodoma SF suma už faktinį naudojamą vienetą. Reikšmė apskaičiuojama kaip lauko **Bendra suma** reikšmė, padalyta iš lauko **Faktinis kiekis** reikšmės. Šis laukas naudojamas integruojant su sistemomis, kurios nepalaiko skirtingų naudojamo kiekio ir kiekio, kurio SF išrašyta, reikšmių. Laukas nerodomas vartotojo sąsajoje.
- Lauko **SF nuolaidos suma** reikšmė apskaičiuojama kaip lauko **Nuolaidos sumos** reikšmės ir suapvalintos apskaičiuotos lauko **SF vieneto suma** reikšmės suma. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauko **Išorinės eilutės užsakymas** reikšmė yra apskaičiuotas neigiamas eilutės užsakymo numeris, kurį galima naudoti išorinėse sistemose, kuriose darbo užsakymo ir paslaugos eilutės yra sujungtos. Šis laukas suteikia galimybę rodyti įterptų darbo užsakymo produktų teigiamus eilučių numerius ir darbo užsakymo paslaugų neigiamus eilučių numerius. Šio lauko reikšmė apskaičiuojama kaip laiko **Eilutės užsakymas** reikšmė, padauginta iš –1. Šis laukas nerodomas vartotojo sąsajoje.
- Laukų **Naudojama** reikšmė atkuriama į **0** (nulis), jei darbo užsakymo paslaugos lauko **Eilutės būsena** reikšmė dėl tam tikros priežasties pakeičiama iš **Naudojama** į **Numatoma**. Šis pakeitimas padeda išvengti situacijų, kuriose klaidingai įvestas naudojamas kiekis yra naudojamas sinchronizuojant, kai lauko **Eilutės būsena** reikšmė yra **Numatoma** ir nustatyta parinkties **Antraštės sistemos būsena** reikšmė **Uždarytas – užregistruotas**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant darbo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-field-service"></a>„Field Service“ sąranka

- Įsitikinkite, kad numerių serija, naudojama „Field Service“ darbo užsakymuose, nesutampa su numeracija, naudojama „Finance and Operations“ pardavimo užsakymuose. Kitu atveju esami pardavimo užsakymai gali būti neteisingai atnaujinti „Field Service“ arba „Finance and Operations“.
- Turi būti nustatyta lauko **Darbo užsakymo SF kūrimas** reikšmė **Niekada**, nes SF bus išrašoma iš „Finance and Operations“. Pasirinkite **Field Service** \> **Parametrai** \> **Administravimas** \> **„Field Service“ parametrai** ir įsitikinkite, kad nustatyta lauko **Darbo užsakymo SF kūrimas** reikšmė **Niekada**.

### <a name="setup-in-finance-and-operations"></a>Sąranka sprendime „Finance and Operations“

Norint integruoti darbo užsakymus reikia nustatyti pardavimo kilmę. Pardavimo kilmė naudojama siekiant atskirti sukurtus „Finance and Operations“ pardavimo užsakymus nuo „Field Service“ darbo užsakymų. Kai pardavimo užsakymo pardavimo kilmės tipas yra **Darbo užsakymo integravimas**, laukas **Išorinė darbo užsakymo būsena** rodomas pardavimo užsakymo antraštėje. Be to, pardavimo kilmė padeda užtikrinti, kad pardavimo užsakymai, sukurti iš „Field Service“ darbo užsakymų, būtų pašalinami naudojant filtrą, kai pardavimo užsakymai sinchronizuojami iš „Finance and Operations“ į „Field Service“.

1. Pasirinkite **Pardavimas ir rinkodara** \> **Sąranka** \> **Pardavimo užsakymai** \> **Pardavimo kilmė**.
2. Norėdami kurti naują pardavimo kilmę, pasirinkite **Nauja**.
3. Lauke **Pardavimo kilmė** įveskite pardavimo kilmės pavadinimą, pavyzdžiui, **WorkOrder**.
4. Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ darbo užsakymas**.
5. Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.
6. Nustatykite lauko **Pardavimo kilmės tipas** reikšmę **Darbo užsakymo integravimas**.
7. Pasirinkite **Įrašyti**.


### <a name="setup-in-data-integration"></a>Duomenų integravimo sąranka

Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_workorders**
1. Eikite į Duomenų integravimas
2. Pasirinkite skirtuką **Ryšio rinkinys**
3. Pasirinkite Ryšio rinkinys, naudojamą Darbo užsakymui sinchronizuoti
4. Pasirinkite skirtuką **Integravimo raktas**
5. Raskite msdyn_workorders ir patikrinkite, ar pridėtas raktas **msdyn_name (Darbo užsakymo numeris)**. Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“): WorkOrderHeader

Filtras: (msdyn_systemstatus ne 690970005) ir (msdyn_systemstatus ne 690970000) ir (msdynce_hasexternallymaintainedproductsonly lygtis teisinga)

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“): WorkOrderServiceLineEstimate

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir (msdyn_linestatus lygtis 690970000) ir (msdynce_headersystemstatus ne 690970004)

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“): WorkOrderServiceLineUsed

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir ((msdyn_linestatus lygtis 690970001) arba (msdynce_headersystemstatus lygtis 690970004))

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“): WorkOrderProductLineEstimate

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir (msdyn_linestatus eq 690970000) ir (msdynce_headersystemstatus ne 690970004) ir (msdyn_allocated lygtis teisinga)

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Finance and Operations“): WorkOrderProductLineUsed

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir ((msdyn_linestatus lygtis 690970001) arba (msdynce_headersystemstatus lygtis 690970004) arba (msdyn_allocated ne teisinga))

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)
