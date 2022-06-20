---
title: „Dataverse“ integravimo konfigūravimas
description: Šiame straipsnyje aprašomas integravimas tarp Microsoft Dataverse ir Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fdc8d15138904336ce7e7b85fe286c815f0743f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869929"
---
# <a name="configure-dataverse-integration"></a>„Dataverse“ integravimo konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite įjungti arba išjungti integravimą tarp „Microsoft Dataverse“ ir „Dynamics 365 Human Resources“. Galite taip pat peržiūrėti sinchronizavimo išsamią informaciją, panaikinti sekimo duomenis ir iš naujo sinchronizuoti lentelę, kad padėtumėte šalinti duomenų problemas tarp dviejų aplinkų.

> [!NOTE]
> Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)

Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Dataverse“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.

Pagal numatytuosius parametrus duomenų integravimas tarp „Human Resources“ ir „Dataverse“ yra išjungtas.

Galbūt norėsite išjungti integravimą šiais atvejais:

- Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.

- Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Dataverse”. Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje. Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas. Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Dataverse“ integravimo praleistų užklausų sinchronizavimas**.

> [!WARNING]
> Kai išjungiate duomenų integravimą, įsitikinkite, kad neredaguojate to paties įrašo abiejose aplinkose. Kai vėl įjungsite integravimą, paskutinis redaguotas įrašas bus sinchronizuojamas. Todėl, jei abiejose aplinkose neatliekate tų pačių keitimų, gali būti prarasti duomenys.

## <a name="access-the-dataverse-integration-page"></a>Prieiga prie „Dataverse“ integravimo puslapio

1. „Human Resources“ egzemplioriuje, kur norite peržiūrėti arba konfigūruoti parametrus integravimui su „Dataverse“, pasirinkite plytelę **Sistemos administravimas**.

    [![Plytelė Sistemos administravimas.](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Pasirinkite skirtuką **Saitai**.

    [![Saitų skirtukas.](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Dalyje **Integravimai** pasirinkite **„Dataverse“ konfigūravimas**.

    [![„Dataverse“ konfigūracijos saitas.](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Duomenų integravimo tarp „Human Resources“ ir „Dataverse“ įjungimas ir išjungimas

- Norėdami įjungti integravimą, nustatykite **Įjungti „Dataverse“ integravimo** parinktį į **Taip** **„Microsoft Dataverse“ integravimo** puslapyje.

    > [!NOTE]
    > Kai įjungiate integravimą, duomenys bus sinchronizuojami kitą kartą, kai vykdoma paketinė užduotis **„Dataverse“ integravimo praleistų užklausų sinchronizavimas**. Po to, kai paketinė užduotis bus baigta, visi duomenys turėtų būti pasiekiami.

- Norėdami išjungti integravimą, nustatykite parinktį į **Ne**.

[![„Dataverse“ integravimo įjungimas arba išjungimas.](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Primygtinai rekomenduojame išjungti „Dataverse“ integravimą atliekant duomenų perkėlimo užduotis. Dideli duomenų įkėlimai gali reikšmingai pabloginti veikimą. Pavyzdžiui, 2000 darbuotojų atnaujinimas gali užimti kelias valandas, kol integravimas bus įjungtas ir mažiau nei valandą jo išjungimui. Šiame pavyzdyje pateikti skaičiai yra tik demonstracijos tikslais. Tikslus laiko kiekis įrašų importavimui gali labai skirtis priklausomai nuo daugybės faktorių.

## <a name="view-data-integration-details"></a>Duomenų integravimo išsamios informacijos apžvalga

**Administravimo** „FastTab“ **„Microsoft Dataverse“ integravimo** puslapyje galite matyti, kaip eilutės yra susietas kartu tarp „Human Resources“ ir „Dataverse“.

- Norėdami peržiūrėti eilutes, rinkitės lentelę **„Dataverse“ lentelės** laukelyje. Tinklelis rodo visas eilutes, kurios yra siejamos su pasirinkta lentele.

> [!NOTE]
> Ne visos „Dataverse“ lentelės dabar yra įtrauktos į sąrašą. Tik lentelės, kurios palaiko tinkintų laukelių naudojimą pasirodys tinklelyje. Naujos lentelės taps prieinamos per nuolatinius „Human Resources“ leidimus.

Tinklelyje yra šie laukai:

- **„Dataverse“ lentelė** – Lentelės pavadinimas „Dataverse“.
- **„Dataverse“ nuoroda į lentelę** – Identifikatorius, kurį „Dataverse“ naudoja idenfitikuoti įrašą. Ši vertė atitinka „Human Resources“ vertę **RecId**. Galite rasti identifikatorių, kai atversite „Dataverse“ lentelę „Microsoft Excel“.
- **„Human Resources“ objekto pavadinimas** – „Human Resources“ objektas, kuris paskutinis sinchronizavimo duomenis į „Dataverse“. Objektas gali būti arba „Dataverse“ priešvardis, arba kitas priešvardis.
- **„Human Resources“ nuoroda** – **RecId** vertė, susieta su „Human Resources“ įrašu.
- **Pašalintas iš „Dataverse“** – Vertė, kuri identifikuoja, ar eilutė buvo pašalinta iš „Dataverse“.

> [!NOTE]
> Įrašai „Human Resources“ atitinka eilutes „Dataverse“.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Pašalinkite „Human Resources“ sąsajos įrašą iš „Dataverse“ eilutės

Jei jums kyla problemų sinchronizuojant duomenis tarp „Human Resources“ ir „Dataverse”, galite jas išspręsti išvalydami sekimą ir leisdami iš naujo nustatyti sekimo lentelę. Jei pašalinsite sąsają ir tada keisite ar naikinsite eilutę „Dataverse“, keitimai nebus sinchronizuojami „Human Resources“. Jei darote keitimus „Human Resources“, naujas sekimo įrašas yra kuriamas ir eilutė yra naujinama „Dataverse“.

- Pašalinkite „Human Resources“ sąsajos įrašą ir „Dataverse“eilutes pasirinkdami lentelę **„Dataverse“ lentelės** laukelyje ir tada rinkitės **Naikinti sekimo informaciją**.

[![Sekimo informacijos valymas.](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Norėdami vykdyti visą sinchronizavimą lentelėje, kai ištrinsite sekimą, žr. kitą procedūrą.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Sinchronizuoti lentelę tarp „Human Resources“ ir „Dataverse“

Naudokite šią procedūrą, kai:

- „Dataverse” keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“.

- Išvalę sekimą turite atnaujinti sekimo lentelę.

Norėdami vykdyti visą sinchronizavimą lentelėje tarp „Human Resources“ ir „Dataverse“:

1. Rinkitės lentelę **„Dataverse“ lentelės** laukelyje.

2. Pasirinkite **Sinchronizuoti dabar**.

[![Visiško sinchronizavimo paleidimas.](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[„Dataverse“ lentelės](hr-developer-entities.md)<br>
[Konfigūruokite „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[„Human Resources“ virtualiųjų lentelių DUK](hr-admin-virtual-entity-faq.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologijos naujinimai](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
