---
title: Registracijos ID
description: Šiame straipsnyje pateikiama informacija, kaip nustatyti ir naudoti registracijos PVM.
author: kfend
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264824
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
ms.openlocfilehash: 380cb1d2b52d5d0debffdbe73183be2f5e783f21
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274558"
---
# <a name="registration-ids"></a>Registracijos ID

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija, kaip nustatyti ir naudoti registracijos PVM.

Daugelyje šalių ir regionų galioja skirtingi registracijos numerių arba ID įrašymo reikalavimai ir nuostatos. Šiame straipsnyje pateikiama reikalaujama parametrų peržiūra ir šalių ( regionų) palaikomų registracijos tipų apdorojimo apžvalga. Visose šalyse / regionuose galioja vietos reikalavimai, reguliuojantys įvairių konkrečiai šaliai skirtų funkcijų, susijusių registracijos numeriais, kuriuos teikia skirtingos valstybinės agentūros, palaikymą. Registracijos numerių pavyzdžiai: socialinis draudimo numeris (SSN), mokesčių identifikavimo numeris (TIN) ir Europos PVM identifikacija (ES PVM ID). Ši funkcija pateikia visiems regionams ir šalims skirtą suvienodintą sistemą, kurioje atsižvelgiama į kai kurioms konkrečioms Europos šalims taikomus reikalavimus. Toliau pateikiamuose skyriuose aprašomas bendras informacijos, kuri naudojama nustatant ir apdorojant registracijos ID, srautas.

## <a name="registration-type-creation"></a>Registracijos tipo kūrimas
Norėdami įvesti registracijos ID, turite nustatyti įvairių rūšių registravimo numerių, kurie taikomi kiekvienai šaliai, registracijos tipus. Atidarykite puslapį **Organizacijos administravimas** &gt; **Visuotinė adresų knygelė** &gt; **Registracijos tipai** &gt; **Registracijos tipai**, kad sukurtumėte ir valdytumėte skirtingų šalių / regionų tiekėjų, klientų, darbuotojų ir juridinių subjektų registracijos tipus.

|Laukas                 |aprašymas      |
|------------------------------|----------------------------|                                                                           
| Vardas                | Registracijos tipo pavadinimas. |                                                                           
| aprašymas         | Registracijos tipo aprašas. |
| Šalis/regionas      | Unikalus šalies / regiono identifikatorius.|
| Mokesčių inspekcija       | Mokesčių inspekcija, susieta su registracijos tipu.|
| Apribota iki       | Mokesčių registracijos tipui taikomo apribojimo rūšis: Nėra, Asmuo, Organizacija.|
| Formatuoti              | Registracijos tipo tikrinimo formatas.|
| Galima naujinti      | Nurodo, ar įvestą registracijos tipo registracijos numerį galima naujinti.|
| Unikalus              | Nurodo, ar registracijos tipo registracijos numeris yra unikalus. |
| Pagrindinis šalies | Jei šalis yra susijusi su vienu ar daugiau adresų konkrečioje šalyje ir registracijos ID taikomas visiems šiems adresams, vieną adresą turite nustatyti kaip pagrindinį adresą toje šalyje. Tik vieną ID galite užregistruoti kaip pagrindinį. Nurodo, ar galima įvesti tik pagrindinio adreso šalyje registracijos numerį. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Registracijos tipo priskyrimas registracijos kategorijai
Registracijos kategorija yra šalies / regiono registracijos identifikatorius, kuris patvirtintas naudoti konkrečioje šalyje / regione mokesčių, muitų tvarkymo ir kitais tikslais. Kategorija nurodo konkretaus registracijos ID tikrinimo taisykles (įskaitant kontrolinius skaitmenis ir t. t.) ir registracijos ID įtraukimą į įvairias ataskaitas. Naudokite puslapį **Organizacijos administravimas** &gt; **Visuotinė adresų knygelė** &gt; **Registracijos tipai** &gt; **Registracijos tipai**, kad konkrečios šalies registracijos tipą priskirtumėte registracijos kategorijai.

| Laukas            | aprašymas|
|-----------------------|----------------|
| Registracijos tipas     | Registracijos tipas konkrečioje šalyje / regione.|
| Apribota iki         | Mokesčių registracijos tipui taikomo apribojimo rūšis: Nėra, Asmuo, Organizacija.|
| Registracijos kategorija | Unikalus registracijos identifikatorius, patvirtintas naudoti šalyje. Toliau šiame straipsnyje rodomas visas palaikomų kategorijų sąrašas. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Visuotinės adresų knygelės įrašų registracijos ID įvedimas

Visuotinė adresų knygelė (GAB) pateikia konsoliduotą klientų, tiekėjų, kontaktų, verslo ryšių ir juridinių subjektų adresų informaciją. Išsamesnės informacijos žr. [Visuotinės adresų knygelės apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-global-address-book.md). Šalies įrašuose, kurie yra saugomi visuotinėje adresų knygelėje, gali būti vienas ar daugiau adresų įrašų. Šie adresai naudojami įvairiems tikslams, pvz., atsiskaitymo arba pristatymo. Galite nustatyti klientų, tiekėjų, darbuotojų ir juridinių subjektų adresų informacijos registracijos ID. Raskite šalies (juridinio subjekto, tiekėjo, kliento, darbuotojo) įrašą, kurio registracijos ID norite įvesti, o tada spustelėkite **Registracijos ID** formose, susijusiose su šalimi, juridiniu subjektu, tiekėju, klientu, darbuotoju, kad atidarytumėte puslapį **Tvarkyti adresus**. Skirtuke **Mokesčių registracija** spustelėkite **Įtraukti** ir įveskite tolesnė registracijos ID informaciją.


|Laukas                |aprašymas                                                |
|---------------------|-----------------------------------------------------------|
| Registracijos tipas   | Registracijos tipas pasirinktoje šalyje / regione.     |
| Įmonės įreg. Nr. | Šalies registracijos ID.                                |
| aprašymas         | Registracijos numerio aprašas.               |
| Skyrius             | Papildoma registracijos numerio informacija. |
| Išduodanti agentūra      | Institucija, kuri išdavė registracijos numerį.        |
| Išdavimo data         | Registracijos numerio išdavimo data.              |
| Galioja           | Registracijos numerio įsigaliojimo data.           |
| Galiojimo pabaiga          | Registracijos numerio galiojimo data.          |

> [!NOTE]
> Juridinio subjekto, tiekėjo, kliento šalies mokesčių lengvatos numeris, kurį galima pasirinkti iš registracijos ID, susijusių su PVM ID, ir įvesti.

## <a name="search-for-records-by-registration-id"></a>Įrašų ieška pagal registracijos ID
Ieškokite šalies įrašų pagal registracijos ID, pateikiamą formose, susijusiose su šalimi, juridiniu subjektu, tiekėju, klientu arba darbuotoju. Spustelėkite **Registracijos ID ieška**, kad atidarytumėte puslapį **Registracijos ID ieškos kriterijai**. Nurodykite ieškos kriterijus ir spustelėkite **Rasti**. Sistema rodys pasirinktus įrašus iš visuotinės adresų knygelės ir susijusius šalies įrašo tipus.

## <a name="supported-registration-categories"></a>Palaikomos registracijos kategorijos
Toliau esančioje lentelėje pateiktas palaikomų registracijos tipų sąrašas. Jei esate susipažinę su Microsoft Dynamics AX 2012 m. registracijos PVM laukais, ši lentelė taip pat susies tuos laukus su "Dynamics 365" finansinės registracijos kategorijomis.

| „Finance“ registracijos kategorija         |Šalis/regionas  | „Dynamics AX 2012“ terminas / laukas|
|---------------------------------------------------------------|---------------------|---------------------------------|
| PVM ID                                                        | Visos Europos Sąjungos (ES) šalys|  Mokesčių lengvatos numeris (įstatymuose nustatyto tipo mokesčio ID programoje AX 2012 R3)|
| Įmonės ID (COID)                                          | Belgija Čekijos Respublika Estija Vengrija Latvija Lietuva Lenkija Šveicarija | Įmonės numeris (EnterpriseNumber) Registracijos numeris (RegNum\_W) Registracijos numeris (RegNum\_W) Registracijos numeris (RegNum\_W) Registracijos numeris (RegNum\_W) Įmonės kodas (EnterpriseCode) Registracijos numeris (RegNum\_W) UID (įstatymuose nustatyto tipo mokesčio ID programoje AX 2012 R3) |
| Filialo ID                                                     | Belgija            | Šakos numeris (BranchNumber)|
| Spisová značka (Registracijos numeris, Išduodanti agentūra, Skyrius) | Čekijos Respublika     | Įklijos numeris (CommercialRegisterInsetNumber) Saugoma komercijos registre (CommercialRegister) Komercijos registro skyrius (CommercialRegisterSection)|
| Muitinės kliento ID                                           | Suomija | Muitinės kliento numeris (CustomsCustomerNumber\_FI)|
| INN                                                           | Rusijos Federacija| INN (įstatymuose nustatyto tipo INN programoje AX 2012 R3)|
| RPK                                                           | Rusijos Federacija| RRC (įstatymuose nustatyto tipo RRC programoje AX 2012 R3)|
| OKDP                                                          | Rusijos Federacija| OKDP (įstatymuose nustatyto tipo OKDP programoje AX 2012 R3)|
| OKPO                                                          | Rusijos Federacija| OKPO (įstatymuose nustatyto tipo OKPO programoje AX 2012 R3)|
| RCOAD                                                         | Rusijos Federacija| RCOAD (įstatymuose nustatyto tipo RCOAD programoje AX 2012 R3)|
| OGRN                                                          | Rusijos Federacija| OGRN (įstatymuose nustatyto tipo OGRN programoje AX 2012 R3) |
| SNILS                                                         | Rusijos Federacija| SNILS (įstatymuose nustatyto tipo SNILS programoje AX 2012 R3)|
| CIFTS                                                         | Rusijos Federacija| CIFTS (įstatymuose nustatyto tipo CIFTS programoje AX 2012 R3)|
| Pasas                                                      | Ispanija             | Pasas|
| Oficialus identifikavimo dokumentas                              | Ispanija             | Oficialus identifikavimo dokumentas|
| Pažyma apie gyvenamąją vietą                                         | Ispanija             | Pažyma apie gyvenamąją vietą|
| Kitas identifikavimo dokumentas                                 | Ispanija             | Kitas identifikavimo dokumentas|
| Nesurašyta                                                  | Ispanija             | Negalima AX 2012 R3|


Norėdami daugiau informacijos apie registracijos ID apdorojimą, įskaitant būtinąsias sąlygas, žr. toliau nurodytus PVM ID užduočių įrašus „Lifecycle Services“ (LCS).

-   PVM ID nustatymas
-   Tiekėjo PVM ID registracija
-   : šalies ieška naudojant PVM ID






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
