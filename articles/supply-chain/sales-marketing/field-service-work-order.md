---
title: „Field Service“ darbo užsakymų sinchronizavimas su „Supply Chain Management“ pardavimo užsakymais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Field Service“ darbo užsakymus su „Supply Chain Management“ pardavimo užsakymais.
author: Henrikan
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c54f5eaec1ae453ba9e55ef54d47c8591276ec89
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568380"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>„Field Service“ darbo užsakymų sinchronizavimas su „Supply Chain Management“ pardavimo užsakymais

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Field Service“ darbo užsakymus su „Dynamics 365 Supply Chain Management“ pardavimo užsakymus.

[![„Supply Chain Management“ ir „Field Service“ verslo procesų sinchronizavimas.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau nurodyti šablonai ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ darbo užsakymus su „Supply Chain Management“ pardavimo užsakymais.

### <a name="names-of-the-templates-in-data-integration"></a>Šablonų pavadinimai naudojant funkciją Duomenų integravimas

Sinchronizuojant naudojamas šablonas **Darbo užsakymai į pardavimo užsakymus („Field Service“ į „Supply Chain Management“)**.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Užduočių pavadinimai projekte Duomenų integravimas

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Prieš sinchronizuojant pardavimo užsakymo antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- „Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)
- Sąskaitos (iš „Sales” į „Supply Chain Management”) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| **„Field service“** | **„Supply Chain Management”** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse pardavimo užsakymo antraštės |
| msdyn_workorderservices | Dataverse pardavimo užsakymo eilutės   |
| msdyn_workorderproducts | Dataverse pardavimo užsakymo eilutės   |

## <a name="entity-flow"></a>Objekto srautas

Darbo užsakymai kuriami „Field Service“. Jei darbo užsakymai apima tik išoriškai tvarkomus produktus, o reikšmė **Darbo užsakymo būsena** nėra **Atidarytas – nesuplanuotas** arba **Uždarytas – atšauktas**, darbo užsakymus galima sinchronizuoti su „Supply Chain Management“ naudojant „Microsoft Dataverse“ duomenų integravimo projektą. Darbo užsakymų naujinimai bus sinchronizuojami kaip „Supply Chain Management“ pardavimo užsakymai. Šie naujinimai apima informaciją apie pradinį tipą ir būseną.

## <a name="estimated-versus-used"></a>Numatoma ir naudojama

„Field Service“ darbo užsakymų produktų ir paslaugų kiekiams bei sumoms priskiriamos reikšmės **Numatoma** ir **Naudojama**. Tačiau „Supply Chain Management“ pardavimo užsakymuose nėra naudojamos tokio pačio tipo reikšmės **Numatoma** ir **Naudojama**. Du užduočių rinkiniai sinchronizuoja darbo užsakymo produktus ir paslaugas, kad būtų palaikomas produktų paskirstymas, kuris naudoja numatomą kiekį „Supply Chain Management“ pardavimo užsakyme, bet kad būtų išlaikytas naudojamas kiekis, kuris turėtų būti vartojamas ir už kurį turėtų būti išrašyta SF. Vienas užduočių rinkinys skirtas tipo **Numatoma** reikšmėms, o kitas užduočių rinkinys skirtas tipo **Naudojama** reikšmėms.

Dėl šios elgsenos galimi atvejai, kai numatomos reikšmės naudojamos „Supply Chain Management“ paskirstant arba rezervuojant, o naudojamos reikšmės naudojamos vartojant ir išrašant SF.

### <a name="estimated"></a>Įvertinta

Sinchronizuojant produkto eilutes, tipo **Numatoma** reikšmės naudojamos, kai parinkties **Eilutės būsena** reikšmė yra **Numatoma**, nustatyta parinkties **Paskirstyta** reikšmė **Taip**, o parinkties **Sistemos būsena** reikšmė nėra **Uždarytas – užregistruotas**.

Sinchronizuojant paslaugos eilutes, tipo **Numatoma** reikšmės naudojamos, kai parinkties **Eilutės būsena** reikšmė yra **Numatoma**, o parinkties **Sistemos būsena** reikšmė nėra **Uždarytas – užregistruotas**.

### <a name="used"></a>Naudota

Tipo **Naudojama** reikšmės naudojamos vartojant ir išrašant SF. Tokiais atvejais tipo **Naudojama** reikšmės yra sinchronizuojamos.

Tolesnėje lentelėje pateikiama įvairių produkto eilučių derinių apžvalga.

| Sistemos būsena <br>(„Field Service”) | Eilutės būsena <br>(„Field Service”) | Paskirstytas <br>(„Field Service”) |Sinchronizuojama reikšmė <br>(„Supply Chain Management“) |
|--------------------|-------------|-----------|---------------------------------|
| Atidarytas – suplanuotas   | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – suplanuotas   | Įvertinta   | Ne        | Naudota                            |
| Atidarytas – suplanuotas   | Naudota        | Taip       | Naudota                            |
| Atidarytas – suplanuotas   | Naudota        | Ne        | Naudota                            |
| Atidarytas – vykdomas | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – vykdomas | Įvertinta   | Ne        | Naudota                            |
| Atidarytas – vykdomas | Naudota        | Taip       | Naudota                            |
| Atidarytas – vykdomas | Naudota        | Ne        | Naudota                            |
| Atidarytas – baigtas   | Įvertinta   | Taip       | Įvertinta                       |
| Atidarytas – baigtas   | Įvertinta   | Ne        | Naudota                            |
| Atidarytas – baigtas   | Naudota        | Taip       | Naudota                            |
| Atidarytas – baigtas   | Naudota        | Ne        | Naudota                            |
| Uždarytas – užregistruotas    | Įvertinta   | Taip       | Naudota                            |
| Uždarytas – užregistruotas    | Įvertinta   | Ne        | Naudota                            |
| Uždarytas – užregistruotas    | Naudota        | Taip       | Naudota                            |
| Uždarytas – užregistruotas    | Naudota        | Ne        | Naudota                            |

Tolesnėje lentelėje pateikiama įvairių paslaugos eilučių derinių apžvalga.

| Sistemos būsena <br>(„Field Service”) | Eilutės būsena <br>(„Field Service”) | Sinchronizuojama reikšmė <br>(„Supply Chain Management“) |
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

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **0** (nulis) ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Supply Chain Management“.

2. Produktai paskirstomi „Field Service“.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – suplanuotas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 0 vnt., eilutės būsena = numatoma, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 0 h, eilutės būsena = numatoma

    Šiame pavyzdyje produkto lauko **Numatomas kiekis** reikšmė **5 vnt.** ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Supply Chain Management“.

3. Paslaugos technikas pradeda dirbti su darbo užsakymu ir užregistruoja medžiagų naudojimą, nurodydamas kiekį 6.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – vykdomas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 6 vnt., eilutės būsena = naudojama, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 0 h, eilutės būsena = numatoma

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **6** ir paslaugos lauko **Numatomas kiekis** reikšmė **2 h** sinchronizuojamos su „Supply Chain Management“.

4. Paslaugos technikas baigia darbo užsakymą ir užregistruoja 1,5 valandos naudojimo laiką.

    Parinkties **Sistemos būsena** reikšmė yra **Atidarytas – baigtas**.

    - **Produkto eilutė:** numatomas kiekis = 5 vnt., naudojamas kiekis = 6 vnt., eilutės būsena = naudojama, paskirstyta = ne
    - **Paslaugos eilutė:** numatomas kiekis = 2 h, naudojamas kiekis = 1,5 h, eilutės būsena = naudojama

    Šiame pavyzdyje produkto lauko **Naudojamas kiekis** reikšmė **6** ir paslaugos lauko **Naudojamas kiekis** reikšmė **1,5 h** sinchronizuojamos su „Supply Chain Management“.

## <a name="sales-order-origin-and-status"></a>Pardavimo užsakymo kilmė ir būsena

### <a name="sales-origin"></a>Pardavimo šaltinis

Norėdami sekti pardavimo užsakymus, kurie sukurti iš darbo užsakymų, galite kurti pardavimo kilmę, kai nustatyta parinkties **Kilmės tipo priskyrimas** reikšmė **Taip** ir nustatyta lauko **Pardavimo šaltinio tipas** reikšmė **Darbo užsakymo integravimas**.

Pagal numatytuosius parametrus susiejant pasirenkama visų pardavimo užsakymų, kurie sukurti iš darbo užsakymų, pardavimo kilmės tipo **Darbo užsakymo integravimas** pardavimo kilmė. Tai gali būti naudinga, kai dirbate su pardavimo užsakymu „Supply Chain Management“. Turite įsitikinti, kad pardavimo užsakymai, kilę iš darbo užsakymų, nėra atgaliniu ryšiu sinchronizuojami su „Field Service“ kaip darbo užsakymai.

Informacijos apie tai, kaip kurti teisingą pardavimo kilmės sąranką „Supply Chain Management“, žr. šios temos dalyje „Išankstinės sąlygos ir susiejimo nustatymas“.

### <a name="status"></a>Būsena

Kai pardavimo užsakymas sukuriamas iš darbo užsakymo, laukas **Išorinė darbo užsakymo būsena** rodomas pardavimo užsakymo antraštės skirtuke **Sąranka**. Šiame lauke rodoma „Field Service“ darbo užsakymo sistemos būsena, kad „Supply Chain Management“ būtų lengviau sekti pardavimo užsakymų sinchronizuojamų darbo užsakymų būseną. Šis laukas taip pat gali padėti vartotojui nustatyti, kada pardavimo užsakymas turėtų būti išsiųstas arba kada turėtų būti išrašyta jo SF.

Lauke **Išorinė darbo užsakymo būsena** naudojamos toliau nurodytos reikšmės.

- Atidarytas – suplanuotas
- Atidarytas – vykdomas
- Atidarytas – baigtas
- Uždarytas – užregistruotas

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas

Reikalinga papildoma „Field Service“ CRM sprendimo funkcija, kad būtų palaikomas „Field Service“ ir „Supply Chain Management“ integravimas. Sprendimas apima toliau nurodytus keitimus.

### <a name="work-order-entity"></a>Objektas Darbo užsakymas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymą sudaro tik išoriškai tvarkomi produktai. Darbo užsakymą sudaro tik išoriškai tvarkomi produktai, o visus susijusius produktus tvarko „Supply Chain Management“. Šis laukas padeda užtikrinti, kad vartotojai nesinchronizuotų darbo užsakymų, kuriuose pateikti neatpažįstami produktai.

### <a name="work-order-product-entity"></a>Objektas Darbo užsakymo produktas

- Laukas **Užsakymą sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymo produktas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymo produktas tvarkomas „Supply Chain Management“. Šis laukas padeda užtikrinti, kad vartotojai nesinchronizuotų darbo užsakymų produktų, kurių „Supply Chain Management“ neatpažįsta.
- Laukas **Antraštės sistemos būsena** įtrauktas į objektą **Darbo užsakymo produktas** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti darbo užsakymo sistemos būseną, ir padeda užtikrinti teisingą filtravimą, kai darbo užsakymo produktai sinchronizuojami su „Supply Chain Management“. Kai filtrai nustatyti integravimo užduotyse, lauko **Antraštės sistemos būsena** informacija taip pat naudojama siekiant nustatyti, ar sinchronizuoti numatomas reikšmes, ar naudojamas reikšmes.
- Lauke **SF vieneto suma** rodoma SF suma už faktinį naudojamą vienetą. Reikšmė apskaičiuojama kaip lauko **Bendra suma** reikšmė, padalyta iš lauko **Faktinis kiekis** reikšmės. Laukas naudojamas integruojant su sistemomis, kurios nepalaiko skirtingų naudojamo kiekio ir kiekio, kurio SF išrašyta, reikšmių. Šis laukas nerodomas vartotojo sąsajoje. 
- Lauko **SF nuolaidos suma** reikšmė apskaičiuojama kaip lauko **Nuolaidos sumos** reikšmės ir suapvalintos apskaičiuotos lauko **SF vieneto suma** reikšmės suma. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **Dešimtainis kiekis** saugoma reikšmė iš lauko **Kiekis**, pateikiama kaip dešimtainis skaičius. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas. 
- Laukų **Naudojama** reikšmė atkuriama į **0** (nulis), jei darbo užsakymo produkto lauko **Eilutės būsena** reikšmė pakeičiama iš **Naudojama** į **Numatoma**. Šis pakeitimas padeda išvengti situacijų, kuriose klaidingai įvestas naudojamas kiekis yra naudojamas sinchronizuojant, kai lauko **Eilutės būsena** reikšmė yra **Numatoma** ir nustatyta parinkties **Paskirstyta** reikšmė **Ne**.

### <a name="work-order-service-entity"></a>Objektas Darbo užsakymo paslauga

- Laukas **Užsakymą sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Darbo užsakymo paslauga** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti, ar darbo užsakymo paslauga tvarkoma „Supply Chain Management“. Šis laukas padeda užtikrinti, kad vartotojai nesinchronizuotų darbo užsakymų paslaugų, kurių „Supply Chain Management“ neatpažįsta.
- Laukas **Antraštės sistemos būsena** įtrauktas į objektą **Darbo užsakymo paslauga** ir yra rodomas puslapyje. Jis naudojamas, kad būtų galima nuosekliai sekti darbo užsakymo sistemos būseną, ir padeda užtikrinti teisingą filtravimą, kai darbo užsakymo paslaugos sinchronizuojamos su „Supply Chain Management“. Kai filtrai nustatyti integravimo užduotyse, lauko **Antraštės sistemos būsena** informacija taip pat naudojama siekiant nustatyti, ar sinchronizuoti numatomas reikšmes, ar naudojamas reikšmes.
- Lauke **Trukmė valandomis** saugoma reikšmė iš lauko **Trukmė**, paversta iš minučių į valandas. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **Numatoma trukmė valandomis** saugoma reikšmė iš lauko **Numatoma trukmė**, paversta iš minučių į valandas. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauke **SF vieneto suma** rodoma SF suma už faktinį naudojamą vienetą. Reikšmė apskaičiuojama kaip lauko **Bendra suma** reikšmė, padalyta iš lauko **Faktinis kiekis** reikšmės. Šis laukas naudojamas integruojant su sistemomis, kurios nepalaiko skirtingų naudojamo kiekio ir kiekio, kurio SF išrašyta, reikšmių. Laukas nerodomas vartotojo sąsajoje.
- Lauko **SF nuolaidos suma** reikšmė apskaičiuojama kaip lauko **Nuolaidos sumos** reikšmės ir suapvalintos apskaičiuotos lauko **SF vieneto suma** reikšmės suma. Šis laukas naudojamas integruojant ir vartotojo sąsajoje nerodomas.
- Lauko **Išorinės eilutės užsakymas** reikšmė yra apskaičiuotas neigiamas eilutės užsakymo numeris, kurį galima naudoti išorinėse sistemose, kuriose darbo užsakymo ir paslaugos eilutės yra sujungtos. Šis laukas suteikia galimybę rodyti įterptų darbo užsakymo produktų teigiamus eilučių numerius ir darbo užsakymo paslaugų neigiamus eilučių numerius. Šio lauko reikšmė apskaičiuojama kaip laiko **Eilutės užsakymas** reikšmė, padauginta iš –1. Šis laukas nerodomas vartotojo sąsajoje.
- Laukų **Naudojama** reikšmė atkuriama į **0** (nulis), jei darbo užsakymo paslaugos lauko **Eilutės būsena** reikšmė dėl tam tikros priežasties pakeičiama iš **Naudojama** į **Numatoma**. Šis pakeitimas padeda išvengti situacijų, kuriose klaidingai įvestas naudojamas kiekis yra naudojamas sinchronizuojant, kai lauko **Eilutės būsena** reikšmė yra **Numatoma** ir nustatyta parinkties **Antraštės sistemos būsena** reikšmė **Uždarytas – užregistruotas**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant darbo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-field-service"></a>„Field Service“ sąranka

- Įsitikinkite, kad numerių serija, naudojama „Field Service“ darbo užsakymams, nesutampa su numeracija, naudojama „Supply Chain Management“ pardavimo užsakymams. Kitu atveju esami pardavimo užsakymai gali būti neteisingai atnaujinti „Field Service“ arba „Supply Chain Management“.
- Turi būti nustatyta lauko **Darbo užsakymo SF kūrimas** reikšmė **Niekada**, nes SF bus išrašoma iš „Supply Chain Management“. Pasirinkite **„Field Service”** \> **Parametrai** \> **Administravimas** \> **„Field Service“ parametrai** ir įsitikinkite, kad nustatyta lauko **Darbo užsakymo SF kūrimas** reikšmė **Niekada**.

### <a name="setup-in-supply-chain-management"></a>„Supply Chain Management“ nustatymas

Norint integruoti darbo užsakymus reikia nustatyti pardavimo kilmę. Pardavimo kilmė naudojama siekiant atskirti sukurtus „Supply Chain Management“ pardavimo užsakymus nuo „Field Service“ darbo užsakymų. Kai pardavimo užsakymo pardavimo kilmės tipas yra **Darbo užsakymo integravimas**, laukas **Išorinė darbo užsakymo būsena** rodomas pardavimo užsakymo antraštėje. Be to, pardavimo kilmė padeda užtikrinti, kad pardavimo užsakymai, sukurti iš „Field Service“ darbo užsakymų, būtų pašalinami naudojant filtrą, kai pardavimo užsakymai sinchronizuojami iš „Supply Chain Management“ į „Field Service“.

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

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Darbo užsakymai į pradavimo užsakymus („Field Service“ į „Supply Chain Management“): WorkOrderHeader

Filtras: (msdyn_systemstatus ne 690970005) ir (msdyn_systemstatus ne 690970000) ir (msdynce_hasexternallymaintainedproductsonly lygtis teisinga)

[![Šablono susiejimas integruojant darbo užsakymų duomenis su pardavimo užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderHeader.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Darbo užsakymai į pradavimo užsakymus („Field Service“ į „Supply Chain Management“): WorkOrderServiceLineEstimate

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir (msdyn_linestatus lygtis 690970000) ir (msdynce_headersystemstatus ne 690970004)

[![Šablono susiejimas integruojant darbo užsakymų duomenis su pardavimo užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderServiceLineEstimate.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Darbo užsakymai į pradavimo užsakymus („Field Service“ į „Supply Chain Management“): WorkOrderServiceLineUsed

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir ((msdyn_linestatus lygtis 690970001) arba (msdynce_headersystemstatus lygtis 690970004))

[![Šablono susiejimas integruojant darbo užsakymų duomenis su pardavimo užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderServiceLineUsed.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Darbo užsakymai į pradavimo užsakymus („Field Service“ į „Supply Chain Management“): WorkOrderProductLineEstimate

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir (msdyn_linestatus eq 690970000) ir (msdynce_headersystemstatus ne 690970004) ir (msdyn_allocated lygtis teisinga)

[![Šablono susiejimas integruojant darbo užsakymų duomenis su pardavimo užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderProductLineEstimate.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Darbo užsakymai į pradavimo užsakymus („Field Service“ į „Supply Chain Management“): WorkOrderProductLineUsed

Filtras: (msdynce_headersystemstatus ne 690970005) ir (msdynce_headersystemstatus ne 690970000) ir (msdynce_orderhasexternalmaintainedproductsonly lygtis teisinga) ir ((msdyn_linestatus lygtis 690970001) arba (msdynce_headersystemstatus lygtis 690970004) arba (msdyn_allocated ne teisinga))

[![Šablono susiejimas integruojant darbo užsakymų duomenis su pardavimo užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderProductLineUsed.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]