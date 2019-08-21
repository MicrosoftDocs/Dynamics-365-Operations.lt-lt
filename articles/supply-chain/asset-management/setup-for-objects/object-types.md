---
title: Turto tipai
description: Šioje temoje paaiškinta, kaip kurti turto tipus turto valdyme. Jame taip pat aprašomi elementai, susiję su turto tipais.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783466"
---
# <a name="asset-types"></a>Turto tipai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aiškinama, kaip sukurti turto tipus. Jame taip pat aprašomi elementai, susiję su turto tipais. Turto tipai naudojami kaip bendrosios turto kategorijos. Pavyzdžiai apima CNC mašinas, matavimo įrangą ir sunkvežimių variklius. Turto tipai naudojami valdyti užduočių tipus (priežiūros užduotis), turto ciklo būsenas, turto matus, turto atributus, sąlygų vertinimo šablonus ir turto modelius, kuriuos galima pasirinkti turtui. Kuriant turtą būtina nurodyti turto tipą.

Kiekvienam turto tipui galima sukurti turto tipo nustatymų variantus. Pavyzdžiui, jei turite turto tipą, pavadintą **Sunkvežimiai**, galite kurti to turto tipo variantus skirtingiems turto gamintojams ir turto modeliams. į kiekvieno turto tipo nustatymą galite įtraukti reikiamas atsargines dalis ir priežiūros planus.

Pirmiausia nustatykite būtinus turto tipus. Tada sukurkite turto modelius, kurie turėtų būti susiję su turto tipais. Galiausiai puslapyje **Turto tipo numatytosios reikšmės** sukurkite visus jūsų įrangai būtinų turto tipų variantus.

## <a name="create-an-asset-type"></a>Turto tipo kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto tipai** \> **Turto tipai**.
2. Pasirinkite **Naujas**, kad sukurtumėte turto tipą.
3. Lauke **Turto tipas** įveskite turto tipo ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.
5. Lauke **Turto ciklo modelis** pasirinkite turto ciklo modelį. Daugiau informacijos apie turto ciklo būsenas ir turto ciklo modelius žr. [Turto ciklo būsenos](object-stages.md).
6. Nustatykite parinktį **Bendra** į **Taip**, jei suvestinio pagrindinio efektyvumo indikatoriaus (KPI) reikšmės turi būti apskaičiuojamos šį turto tipą turinčiam turtui.
7. Pasirinkite **Įrašyti**.
8. „FastTab“ **Užduočių tipai** pasirinkite užduočių tipus, kurie turėtų būti susieti su turto tipu:

    - Norėdami pasirinkti užduoties tipą, pasirinkite jį lauke **Likę užduočių tipai**, tada pasirinkite rodyklės dešinėn mygtuką ![Rodyklės dešinėn mygtukas](media/29-setup-for-objects.png), kad perkeltumėte jį į skyrių **Pasirinkti užduočių tipai**.
    - Norėdami pasirinkti visus galimus užduočių tipus, pasirinkite mygtuką ![Rodyklė Persiųsti viską](media/30-setup-for-objects.png). Visi užduočių tipai perkeliami iš lauko **Likę užduočių tipai** į lauką **Pasirinkti užduočių tipai**.
    - Norėdami atšaukti užduoties tipo pasirinkimą, pasirinkite jį lauke **Pasirinkti užduočių tipai**, tada pasirinkite rodyklės kairėn mygtuką ![Rodyklės kairėn mygtukas](media/31-setup-for-objects.png), kad perkeltumėte jį į lauką **Likę užduočių tipai**.

9. Taip pat galima pasirinkti turto matus, kurie turėtų būti susieti su turto tipu. „FastTab“ **Turto matai** atlikite pasirinkimą naudodami metodus, aprašytus užduočių tipams atliekant 8 veiksmą. Daugiau informacijos apie turto matų nustatymą žr. [Prižiūrimo turto matai](counters.md).
10. Taip pat galima pasirinkti atributų tipus, kurie turėtų būti susieti su turto tipu. „FastTab“ **Atributų tipai** atlikite pasirinkimą naudodami metodus, aprašytus užduočių tipams atliekant 8 veiksmą. Tada, norėdami kurti pageidaujamą atributų tipų seką, pasirinkite atributo tipą lauke **Pasirinkti atributų tipai** ir perkelkite juos naudodami rodyklių aukštyn ir žemyn mygtukus. Atributų tipų seka bus rodoma turtui, kuris naudoja šį turto tipą. Daugiau informacijos apie turto atributus žr. [Priežiūros atributų tipai](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > „FastTab“ **Atributų tipai** įtraukus naujų atributų tipų, esamas turtas automatiškai atnaujinamas naudojant tą informaciją.

11. Taip pat galima pasirinkti sąlygų vertinimo šablonus, kurie turėtų būti susieti su turto tipu. „FastTab“ **Sąlygų vertinimai** atlikite pasirinkimą naudodami metodus, aprašytus užduočių tipams atliekant 8 veiksmą. Daugiau informacijos apie sąlygų vertinimo šablonus ir registracijas žr. [Sąlygų vertinimas](../setup-for-objects/condition-assessment.md).
12. „FastTab“ **Turto modelis** rodomi visi turto gamintojų ir modelių deriniai, nustatyti pasirinktam turto tipui. Norėdami peržiūrėti derinius, suskirstytų pagal gamintoją, pasirinkite **Turto modelis**, kad atidarytumėte puslapį **Turto modelis**.

    Puslapyje **Turto modelis** galite įtraukti turto modelio-turto tipo ryšius. Be to, puslapyje **Turto tipai** galite įtraukti turto gamintojo-turto modelio ryšius tiesiogiai su turto tipu. Galiausiai puslapyje **Turto modelis** (**Turto valdymas** \> **Sąranka** \> **Turtas** \> **Turto modelis**) galima sukurti naujus turo gamintojo-turto modelio-turto tipo ryšius. Yra trys būdai, kaip galima nustatyti ir redaguoti turto gamintojo-turto modelio-turto tipo ryšius. Visi galimi deriniai rodomi iš skirtingų perspektyvų ir galima pasirinkti pageidaujamą įvedimo tašką, kai dirbate su sąranka.

> [!NOTE]
> - Jei turto tipui pasirinksite turto matus, pasirinkimai automatiškai atnaujinami puslapyje **Turto matai** (**Turto valdymas** \> **Sąranka** \> **Turtas** \> **Turto tipai** \> **Turto matai**).
> - Dalies **Informacija** laukuose „FastTab“ **Bendra** pateiktas pasirinktam turto tipui nustatytų užduočių tipų, turto matų, atributų ir pan. skaičius.

Paprastai rankiniu būdų sukurti darbo užsakymai yra susiję su koreguojamąja priežiūra, o automatiškai sukurti darbo užsakymai yra susiję su prevencine priežiūra. Rankiniu būdu kuriant darbo užsakymus gali būti naudojami tik puslapio **Turto tipai** „FastTab“ **Užduočių tipai** pasirinkti užduočių tipai. Tačiau automatiškai sukurti darbo užsakymai gali naudoti visus užduočių tipus, kuriuos sukuriate puslapyje **Užduočių tipai** (**Turto valdymas** \> **Sąranka** \> **Užduotys** \> **Užduočių tipai**).

## <a name="create-asset-type-setup-lines"></a>Turto tipo nustatymo eilučių kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Turto tipai** \> **Turto tipo nustatymas**. Taip pat galima pasirinkti **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Turto tipai** \> **Turto tipai**, pasirinkti turto tipą, tada pasirinkti **Turto tipo nustatymas**.
2. Pirmą kartą naudojant puslapį **Turto tipo nustatymas** gali būti naudingas mygtukas **Kurti derinius**. Naudodami šį mygtuką galite greitai sukurti visus turto tipo turto modelio derinius. Pasirinkite **Kurti derinius**, pasirinkite turto tipą, kad galėtumėte kurti jo derinius, tada pasirinkite **Gerai**.

    > [!NOTE]
    > Jei nenaudosite visų automatiškai sukurtų turto tipų nustatymo derinių, galite panaikinti sąranką ją pasirinkdami, tada pasirinkdami **Naikinti**.

3. Pasirinkite **Naujas**, kad sukurtumėte turto tipo nustatymą rankiniu būdu.
4. Atsižvelgiant į tai, kiek konkretus turėtų būti turto tipo nustatymas, atlikite pasirinkimus laukuose **Turto tipas**, **Gamintojas** ir **Modelis**.
5. Jei garantinė sutartis susijusi su turto tipu, pasirinkite sutartį laukuose **Tiekėjo garantija** ir **Kliento garantija**. 
6. „FastTab“ **Atsarginės dalys** pasirinkite **Įtraukti**, kad įtrauktumėte atsarginių dalių į pasirinkto turto tipo nustatymą.
7. Norėdami patvirtinti atsarginę dalį, pasirinkite atsarginių dalių eilutę, tada pasirinkite **Tvirtinti**. Tvirtinimui galima pasirinkti kelias eilutes.
8. Norėdami peržiūrėti, ar atsarginė dalis naudojama kur nors kitur turto valdyme (pvz., turto ir darbo užsakymų atžvilgiu), pasirinkite atsarginių dalių eilutę, tada pasirinkite **Elementas, kuris naudojamas**, kad atidarytumėte puslapį **Elementas, kuris naudojamas**. Norėdami pamatyti sąraše visas aktyvias atsargines dalis, pažymėkite žymės langelį **Aktyvios**. Jei norite matyti tik patvirtintas atsargines dalis, pažymėkite žymės langelį **Patvirtintos**.
9. „FastTab“ **Priežiūros planai** pasirinkite **Įtraukti**, kad įtrauktumėte priežiūros planus į pasirinkto turto tipo nustatymą.
10. Norėdami kopijuoti turto tipo sąranką į kitą sąranką, galite naudoti funkciją Kopijuoti. Pasirinkite turto tipo sąranką, kad nukopijuotumėte sąranką, pasirinkite **Kopijuoti sąranką**, tada pasirinkite turto tipo sąranką, iš kurios bus kopijuojama sąranka. Įvairių parinkčių parametrai lemia, kiek informacijos bus įtraukta. Baigę pasirinkite **Gerai**, kad nukopijuotumėte sąranką.

> [!NOTE]
> Jei turite daug atsarginių dalių eilučių ir priežiūros plano eilučių, kurias pakartotinai naudosite, funkcija Kopijuoti suteikia galimybę greitai ir lengvai nustatyti daugelio turto tipų nustatymo duomenų derinius.

## <a name="spare-parts-on-the-asset-type-setup"></a>Atsarginės dalys turto tipo nustatyme

Kaip aprašyta skyriuje „Turto tipo nustatymo eilučių kūrimas“, atsarginės dalys nustatomos turto modeliuose puslapyje **Turto tipo nustatymas**. Atidarius puslapį **Turto tipo nustatymas** matysite tik tas atsargines dalis, kurios yra susijusios su pasirinktu turto tipo, turto gamintojo ir turto modelio deriniu. Norėdami peržiūrėti visų atsarginių dalių įrašų sąrašą, atidarykite puslapį **Atsarginės dalys** (**Turto valdymas** \> **Užklausos** \> **Atsarginės dalys**).

Puslapyje **Atsarginės dalys** taip pat galite kurti naujas atsargines dalis esamiems turto tipo, turto gamintojo ir turto modelio deriniams. Galite nuspręsti, ar norite kurti atsarginių dalių įrašus puslapyje **Turto tipo nustatymas**, ar puslapyje **Atsarginės dalys**. Puslapyje **Turto tipo nustatymas** teikiama pasirinkto turto tipo, turto gamintojo ir turto modelio derinio duomenų apžvalga, o puslapyje **Atsarginės dalys** teikiama išsami visų turto tipo nustatymo eilučių apžvalga. Jei puslapyje **Atsarginės dalys** yra daug įrašų, puslapyje **Turto tipo nustatymas** gali būti pateikiama geresnė apžvalga.

Norėdami peržiūrėti, ar atsarginė dalis pasirinktoje eilutėje naudojama kur nors kitur turto valdyme (pvz., turto ir darbo užsakymų atžvilgiu), pasirinkite **Elementas, kuris naudojamas**, kad atidarytumėte puslapį **Elementas, kuris naudojamas**. 

