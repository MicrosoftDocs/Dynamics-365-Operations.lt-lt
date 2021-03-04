---
title: „Common Data Service“ integravimo konfigūravimas
description: Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Dynamics 365 Human Resources“. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527934"
---
# <a name="configure-common-data-service-integration"></a>„Common Data Service“ integravimo konfigūravimas

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Dynamics 365 Human Resources“. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.

Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Common Data Service“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.

Pagal numatytuosius parametrus duomenų integravimas tarp „Human Resources“ ir „Common Data Service“ yra išjungtas.

Galbūt norėsite išjungti integravimą šiais atvejais:

- Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.

- Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Common Data Service”. Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje. Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas. Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.

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

> [!WARNING]
> Primygtinai rekomenduojame išjungti „Common Data Service“ integravimą atliekant duomenų perkėlimo užduotis. Dideli duomenų įkėlimai gali reikšmingai pabloginti veikimą. Pavyzdžiui, 2000 darbuotojų atnaujinimas gali užimti kelias valandas, kol integravimas bus įjungtas ir mažiau nei valandą jo išjungimui.  Šiame pavyzdyje pateikti skaičiai yra tik demonstracijos tikslais. Tikslus laiko kiekis įrašų importavimui gali labai skirtis priklausomai nuo daugybės faktorių. 

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

Naudokite šią procedūrą, kai:

- „Common Data Service” keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“.

- Išvalę sekimą turite atnaujinti sekimo lentelę.

Norėdami vykdyti visišką objekto sinchronizavimą tarp „Human Resources“ ir „Common Data Service”, atlikite toliau pateiktus veiksmus.

1. Lauke **CDS objekto pavadinimas** pasirinkite objektą.

2. Pasirinkite **Sinchronizuoti dabar**.

[![Visiško sinchronizavimo paleidimas](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]