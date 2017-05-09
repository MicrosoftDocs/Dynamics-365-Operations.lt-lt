---
title: "Visuotinių adresų knygelių konfigūravimas"
description: "Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles programoje „Microsoft Dynamics 365 for Operations“. Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: abd9ec44530522657f758b35e8f987aa92c3b0e3
ms.lasthandoff: 03/31/2017


---

# <a name="configure-global-address-books"></a>Visuotinių adresų knygelių konfigūravimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles programoje „Microsoft Dynamics 365 for Operations“. Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje.

<a name="global-address-book"></a>Visuotinė adresų knygelė
-------------------

Prieš pradėdami dirbti su visuotine adresų knygele, turite nustatyti numatytąsias jos reikšmes. Šios numatytosios reikšmės tada naudojamos bet kokioms papildomoms jūsų sukurtoms adresų knygelėms. **Sprendimai:**

-   Kokia seka turėtų būti rodomi **Asmens** tipo šalių įrašų vardai ir pavardės? Pavyzdžiui, viena seka yra pavardė, antras vardas, vardas.
-   Ar, panaikinus vaidmens įrašą, iš adresų knygelės turėtų būti panaikinti šalių įrašai? Pavyzdžiui, jei panaikinamas kliento įrašas, ar taip pat turėtų būti panaikintas šalies įrašas?
-   Ar, kuriant naują įrašą, naudotojams turėtų būti pranešama, jei visuotinėje adresų knygelėje aptinkamas besidubliuojantis įrašas?
-   Ar į šalies įrašo informaciją turėtų būti įtrauktas Duomenų universaliosios numeravimo sistemos (DUNS) numeris?
-   Jei DUNS numeris įtraukiamas į šalies įrašą, ar turėtų būti tikrinamas numerio unikalumas?
-   Kai visuotinėje adresų knygelėje kuriamas šalies įrašas, ar norite nustatyti numatytąjį įrašo tipą, asmens arba organizacijos?
-   Kokie naudotojo vaidmenys turėtų turėti prieigą prie šalių įrašų privačios adresų ir kontaktinės informacijos?

## <a name="additional-address-books"></a>Papildomos adresų knygelės
Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai. Pavyzdžiui, „Fabrikam‟ yra tarptautinė organizacija, kuri turi kelias įmones ir dalyvauja keliose verslo šakose. „Fabrikam‟ planuoja sukurti kiekvienos verslo šakos adresų knygelę. Tų verslo šakų, kurių veikla vykdoma daugiau nei vienoje vietoje, pvz., pneumatinių įrankių verslo, „Fabrikam‟ planuoja sukurti kiekvienos vietos adresų knygelę. Chrisas, „Fabrikam‟ IT vadovas, sukūrė toliau pateiktą reikiamų adresų knygelių sąrašą. Šiame sąraše taip pat aprašomi šalių įrašai, kurie turi būti kiekvienoje adresų knygelėje.

-   **Viešojo sektoriaus sutartys (PubSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis viešojo sektoriaus sutartimis, įrašai.
-   **Privačiojo sektoriaus sutartys (PriSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis privačiojo sektoriaus sutartimis, įrašai.
-   **Elektroniniai įrankiai (ET)** – visų šalių, dalyvaujančių perkant ar parduodant elektroninius įrankius, ar kitaip sąveikaujančių su elektroniniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.
-   **Pneumatiniai įrankiai (PTJPN)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.
-   **Pneumatiniai įrankiai (PTUSA)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-US‟ įmonėje, arba kurie jai nuperkami, įrašai.

**Sprendimas:**

-   Kiek sukursite papildomų adresų knygelių?

### <a name="address-book-security"></a>Adresų knygelių sauga

Kurti adresų knygeles galite bet kuriuo metu ir taip pat bet kuriuo metu galite nustatyti adresų knygelių saugos parametrus. Nebūtina nustatyti adresų knygelės saugos teisių, tačiau, jei to nepadarysite, visi jūsų organizacijos darbuotojai galės peržiūrėti visus tos adresų knygelės šalių įrašus. Saugos teises į šalių įrašus galite nustatyti adresų knygelėse. Saugos teisės paremtos komandomis. Šiuo būdu garantuojama, kad adresų knygelės šalių įrašus galėtų peržiūrėti tik tie darbuotojai, kurie priskirti komandai, turinčiai prieigą prie tos adresų knygelės. Turite pasirinkti komandas, turinčias prieigą prie kiekvienos adresų knygelės. Galite nustatyti kiekvienos adresų knygelės saugos teises, leidžiančias arba draudžiančias konkrečių komandų prieigą. Jei komandai suteikiate adresų knygelės teises, visi tos komandos nariai gali peržiūrėti adresų knygelės įrašus. Jei komandai prieigos prie adresų knygelės nesuteikiate, tos komandos nariai peržiūrėti adresų knygelės ar jos turinio negali. **Sprendimas:**

-   Kurios komandos turėtų turėti prieigą prie kiekvienos naujos jūsų sukurtos adresų knygelės?





