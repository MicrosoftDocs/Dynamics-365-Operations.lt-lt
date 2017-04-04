---
title: Registracijos ID
description: "Šioje temoje pateikta informacija apie kuriant ir naudojant registracijos ID."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registracijos ID

Šioje temoje pateikta informacija apie kuriant ir naudojant registracijos ID.

Daugelyje šalių ir regionų turi skirtingų teisės aktų ir reikalavimų registracijos numerius ar ID registruoti. Šioje temoje pateikta reikiamus parametrus ir perdirbimo palaikomos registravimo tipų apžvalga šalims skirtingose Europos šalyse/regionuose. Visose šalyse/regionuose turite savo poreikį remti įvairias konkrečioms funkcijas, susijusias su registracijos numerius gautus iš įvairių valstybės tarnybų. Registracijos numerių pavyzdžiai, socialinio draudimo numerį (SSN), mokesčių identifikavimo numerį (TIN) ir Europos PVM mokėtojo kodas (ES PVM ID). Ši priemonė suteikia vieningą sistemą visoms šalims atsižvelgiant į konkrečios šalies reikalavimus, kai kuriose Europos šalyse visuose regionuose. Šiuose skyriuose aprašoma apie bendrą informaciją, kuri yra naudojama steigimo ir registravimo ID apdorojimo srautą.

## <a name="registration-type-creation"></a>Registracijos tipo kūrimas
Prieš įvesdami registracijos ID, turite nustatyti registravimo tipus registracijos numerius, kad kiekviena šalis yra atsižvelgiant į skirtingų tipų. Eikite į **organizacijos administracijos**&gt;**adresų knyga**&gt;**registracijos tipai**&gt;**registracijos tipai** puslapis kurti ir tvarkyti registracijos tipai, tiekėjai, Klientai, darbuotojai ir juridinių asmenų skirtingose šalyse/regionuose.

|Laukas                 |aprašymas      |
|------------------------------|----------------------------|                                                                           
| Vardas                | Registracijos tipo pavadinimas. |                                                                           
| aprašymas         | Registracijos tipo aprašymas. |
| Šalis/regionas      | Unikalusis atstovo, šalis/regionas.|
| Mokesčių inspekcija       | Mokesčių administratorius, kuris yra susietas su registravimo tipu.|
| Apribota iki       | Natūra, apribojimas, taikomas mokesčių registracijos tipas: nėra, asmuo, organizacija.|
| Formatuoti              | Registracijos tipo patvirtinimo formatą.|
| Galima naujinti      | Nustatoma registracijos numeris registracijos tipo galima atnaujinti po to, kai jis yra įrašytas.|
| Unikalus              | Nustatoma pagal registracijos numerį, registracijos tipas yra unikalus. |
| Pagrindinis šalies | Jei šalis yra susijęs su viena ar daugiau adresų, ypač šalies ir registracijos ID galioja visi šie adresai, privalo paskirti vieną adresą kaip pirminis šalyje. Jūs galite registruotis tik vieną ID kaip pagrindinę. Nustatoma registracijos numeris gali būti įrašytas tik į šalies adreso. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Priskirti registravimo tipą registravimo kategorija
Registravimo kategorija yra šalies/regiono registracijos identifikatorius aprobuotas naudojant šalį/regioną, mokesčių, muitinės ir kitiems tikslams. Ši kategorija apibrėžia tikrinimo taisykles, ypač registracijos ID (įskaitant tikrinimo skaitmenų ir kt.) ir integracijos registracijos ID įvairias ataskaitas. Naudokite puslapį **organizacijos administracijos**&gt;**adresų knyga**&gt;**registracijos tipai**&gt;**registracijos kategorijos** priskirti registracijos tipas tam tikros šalies palaikomos registravimo kategorija.

| Laukas            | aprašymas|
|-----------------------|----------------|
| Registracijos tipas     | Registracijos tipo ypač šalis/regionas.|
| Apribota iki         | Apribojimas taikomas mokesčių registracijos tipas: nėra, asmuo, organizacija.|
| Registracijos kategorija | Aprobuotas naudoti šalyje unikalų registracijos identifikatorius. Visas sąrašas, kuriam AX7.1 kategorijos yra žemiau. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Įveskite registracijos ID adresų knygos įrašus
Adresų knygelės (GAB) Microsoft Dynamics 365 operacijoms yra konsoliduota adreso informacija pirkėjams, tiekėjams, kontaktai, verslo ryšius ir juridiniai asmenys. Daugiau informacijos ieškokite [adresų knygų apžvalga](/dynamics365/operations/organization-administration/overview-global-address-book). Šalies įrašai, kurie saugomi Visuotiniame adresų knygoje gali būti vienas ar daugiau adresų įrašų. Šie adresai naudojami įvairiems tikslams, pvz., atsiskaitymo arba pristatymo. Jums nustatyti registracijos ID adreso informacija pirkėjams, tiekėjams, darbuotojams, ir juridiniai asmenys. Rasti asmens (juridinio asmens, tiekėjų, klientų, darbuotojas) įrašo, kurį norite įvesti registro ID, ir tada spustelėkite **registracijos ID.** formų, susijusių su šalies, juridinis asmuo, tiekėjų, klientų, darbuotojas atidaryti su **tvarkyti adresų** puslapis. Dėl to **mokesčių registracijos** skirtuką, spustelėkite **pridėti**, ir įveskite šią informaciją apie registracijos ID.

|Laukas                |aprašymas                                                |
|---------------------|-----------------------------------------------------------|
| Registracijos tipas   | Registracijos tipo pasirinktos šalies/regiono.     |
| Įmonės įreg. Nr. | Šalis registracijos ID.                                |
| aprašymas         | Įmonės apibūdinimas.               |
| Skyrius             | Papildomos informacijos apie registracijos numerį. |
| Išduodanti agentūra      | Institucijai, kuri išdavė registracijos numerį.        |
| Išdavimo data         | Išduotas data, registracijos numeris.              |
| Galioja           | Įsigaliojimo data, registracijos numeris.           |
| Galiojimo pabaiga          | Galiojimo pabaigos data, registracijos numeris.          |

> [!NOTE]
> Mokesčių mokėtojo teisės subjektas, tiekėjų, klientų galima pasirinkti registracijos ID susiję su PVM mokėtojo kodas ir įrašytas šalies.

## <a name="search-for-records-by-registration-id"></a>Ieškoti įrašų pagal registracijos ID
Ieškoti pagal ID galima rasti susijusiose šaliai, juridinio asmens, tiekėjų, klientų ir darbuotojų registracijos šalies įrašų. Spustelėkite **registracijos ID paieškos** atidaryti, **registracijos ID paieškos kriterijus** puslapis. Nurodykite paieškos kriterijus ir spauskite **rasti**. Sistema parodys pažymėtus įrašus iš adresų knygos ir susijusios šalies įrašų tipų.

## <a name="supported-registration-categories"></a>Palaikomos registracijos kategorijos
Šioje lentelėje pateikiami palaikomi registracijos tipus dinamika 365 operacijoms. Jei esate susipažinę su Microsoft Dynamics AX 2012 laukuose registravimo ID, šioje lentelėje taip pat žemėlapiai tose srityse Dynamics 365 operacijų registracijos kategorijoms.

| Dinamika 365 operacijų registravimo kategorija         |Šalis/regionas  | Dinamika AX 2012/lauką|
|---------------------------------------------------------------|---------------------|---------------------------------|
| PVM ID                                                        | Visose šalyse Europos Sąjungos (ES)|  PVM mokėtojo kodas (TAX ID, AX2012 R3 teisėkūros tipas)|
| Įmonės ID (COID)                                          | Belgija Čekija Estija Vengrija Latvija Lietuva Lenkija Šveicarija | Įmonių skaičius (EnterpriseNumber) registracijos numeris (RegNum\_W) registracijos numeris (RegNum\_W) registracijos numeris (RegNum\_W) registracijos numeris (RegNum\_W) įmonės kodas (EnterpriseCode) registracijos numeris (RegNum\_W) UID (teisėkūros rūšis UID, AX2012 R3) |
| Filialo ID                                                     | Belgija            | Filialo numeris (BranchNumber)|
| Spisová značka (registracijos numeris, išdavusi agentūra, skyrius) | Čekijos Respublika     | Potinkinis numeris (CommercialRegisterInsetNumber) Kept prekybos užsiregistruoti komerciniame registre (CommercialRegisterSection) skyrių (CommercialRegister)|
| Muitinės kliento ID                                           | Suomija | Muitinės klientų skaičių (CustomsCustomerNumber\_internetu)|
| INN                                                           | Rusijos Federacija| INN (teisėkūros rūšis INN, AX2012 R3)|
| RPK                                                           | Rusijos Federacija| Registravimo priežasties kodas (RPK, AX2012 R3 teisėkūros rūšis)|
| EVPK                                                          | Rusijos Federacija| EVPK (teisėkūros rūšis EVPK AX2012 R3)|
| OKPO                                                          | Rusijos Federacija| OKPO (teisėkūros rūšis OKPO AX2012 R3)|
| RAPOK                                                         | Rusijos Federacija| RAPOK (RAPOK, AX2012 R3 teisėkūros rūšis)|
| OGRN                                                          | Rusijos Federacija| OGRN (OGRN, AX2012 R3 teisėkūros rūšis) |
| SNILS                                                         | Rusijos Federacija| SNILS (SNILS, AX2012 R3 teisėkūros rūšis)|
| CIFTS                                                         | Rusijos Federacija| CIFTS (CIFTS, AX2012 R3 teisėkūros rūšis)|

Daugiau informacijos apie registravimo ID, apdorojimas, įskaitant būtinąsias sąlygas, šios užduoties įrašų ieškokite PVM ID gyvavimo ciklo paslaugų (LCS):

-   PVM ID nustatymas
-   Tiekėjo PVM mokėtojo kodas registracijos
-   : šalies ieška naudojant PVM ID



