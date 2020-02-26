---
title: Konfigūruoti „Common Data Service“ integravimą
description: Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Microsoft Dynamics 365 Human Resources“ egzemplioriaus. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009912"
---
# <a name="configure-common-data-service-integration"></a>Konfigūruoti „Common Data Service“ integravimą

Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Microsoft Dynamics 365 Human Resources“ egzemplioriaus. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.

Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Common Data Service“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.

Pagal numatytuosius parametrus integravimas tarp „Human Resources“ ir „Common Data Service“ yra arba išjungtas, arba įjungtas, atsižvelgiant į tai, ar aplinkose yra demonstracinių duomenų:

- **Išjungta** naujoms aplinkoms, kuriose nėra demonstracinių duomenų
- **Įjungta** naujoms aplinkoms, kuriose yra demonstracinių duomenų

Naujos aplinkos, kuriose yra demonstracinių duomenų, pradės sinchronizuoti duomenis, kai jie parengiami.

Galbūt norėsite išjungti integravimą šiais atvejais:

- Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.

- Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Common Data Service”. Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje. Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, bus sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas. Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.

> [!WARNING]
> Kai išjungiate duomenų integravimą, įsitikinkite, kad neredaguojate to paties įrašo abiejose aplinkose. Kai vėl įjungsite integravimą, paskutinis redaguotas įrašas bus sinchronizuojamas. Todėl, jei abiejose aplinkose neatliekate tų pačių keitimų, gali būti prarasti duomenys.

## <a name="access-the-common-data-service-integration-page"></a>Prieiga prie „Common Data Service“ integravimo puslapio

1. „Human Resources“ egzemplioriuje, kur norite peržiūrėti arba konfigūruoti parametrus integravimui su „Common Data Service“, pasirinkite plytelę **Sistemos administravimas**.

    [![Plytelė Sistemos administravimas](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Pasirinkite skirtuką **Saitai**.

    [![Saitų skirtukas](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Dalyje **Integravimai** pasirinkite **„Common Data Service“ konfigūravimas**.

    [![„Common Data Service“ konfigūracijos saitas](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Duomenų integravimo tarp „Human Resources“ ir „Common Data Service“ įjungimas ir išjungimas

- Norėdami įjungti integravimą, nustatykite parinktį **Įjungti integravimą į „Common Data Service“** kaip **Taip**.

    > [!NOTE]
    > Kai įjungiate integravimą, duomenys bus sinchronizuojami kitą kartą, kai vykdoma paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**. Po to, kai paketinė užduotis bus baigta, visi duomenys turėtų būti pasiekiami.

- Norėdami išjungti integravimą, nustatykite parinktį į **Ne**.

[![„Common Data Service“ integravimo įjungimas arba išjungimas](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Duomenų integravimo išsamios informacijos apžvalga

„FastTab“ **Administravimas**, esančiame puslapyje **„Common Data Service“ integravimas**, galite matyti, kaip įrašai siejami tarpusavyje tarp „Human Resources” ir „Common Data Service”.

- Norėdami peržiūrėti objekto įrašus, pažymėkite objektą lauke **CDS objekto pavadinimas**. Tinklelyje rodomi visi įrašai, kurie yra siejami su pasirinktu objektu.

[![Objekto įrašų peržiūra](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Šiuo metu nurodyti ne visi „Common Data Service“ objektai. Tinklelyje rodomi tik tie ojektai, kurie palaiko pasirinktinius laukus. Nauji objektai tampa pasiekiami nuolatiniuose „Human Resources“ leidimuose.

Tinklelyje yra šie laukai:

- **CDS objekto pavadinimas** – objekto, esančio „Common Data Service“, pavadinimas.
- **CDS objekto nuoroda** – identifikatorius, kurį „Common Data Service“ naudoja įrašui identifikuoti. Ši vertė atitinka „Human Resources“ vertę **RecId**. Galite rasti identifikatorių, kai atidarote „Common Data Service“objektą, esantį „Microsoft Excel“.
- **„Human Resources“ objekto pavadinimas** – objektas, kuris paskutinį kartą sinchronizavo duomenis į „Common Data Service“. Objektas gali būti arba „Common Data Service“ priešvardis, arba kitas priešvardis.
- **„Human Resources“ nuoroda** – **RecId** vertė, susieta su „Human Resources“ įrašu.
- **Panaikintas iš CDS** – reikšmė, nurodanti, ar įrašas buvo panaikintas iš „Common Data Service“.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Įrašo, esančio „Human Resources“ susiejimo šalinimas iš „Common Data Service“

Jei jums kyla problemų sinchronizuojant duomenis tarp „Human Resources“ ir „Common Data Service”, galite jas išspręsti išvalydami sekimą ir leisdami iš naujo nustatyti sekimo lentelę. Jei pašalinsite susiejimą ir pakeisite arba panaikininsite įrašą, esantį „Common Data Service“, keitimai nebus sinchronizuojami su „Human Resources“. Atlikus keitimų programoje „Human Resources“, sukuriamas naujas sekimo įrašas ir atnaujinamas įrašas, esantis „Common Data Service“.

- Norėdami pašalinti įrašo susiejimą tarp „Human Resources“ ir „Common Data Service“, lauke **CDS objekto pavadinimas** pasirinkite objektą, tada pasirinkite **Valyti sekimo informaciją**.

[![Sekimo informacijos valymas](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Išvalę sekimą, norėdami vykdyti visišką objekto sinchronizavimą, žr. tolesnę procedūrą.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Objekto sinchronizavimas tarp „Human Resources“ ir „Common Data Service“

Naudokite šią procedūrą, jei „Common Data Service“ keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“, arba jei išvalę sekimą turite atnaujinti sekimo lentelę.

- Norėdami vykdyti visišką objekto sinchronizavimą tarp „Human Resources“ ir „Common Data Service“, lauke **CDS objekto pavadinimas** pasirinkite objektą, tada pasirinkite **Sinchronizuoti dabar**.

[![Visiško sinchronizavimo paleidimas](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


