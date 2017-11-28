---
title: Gamybos nustatymo reikalavimai
description: "Šiame straipsnyje pateikiama informacija apie nustatymo reikalavimus prieš dirbant su Gamybos kontrole."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a>Gamybos nustatymo reikalavimai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie nustatymo reikalavimus prieš dirbant su Gamybos kontrole. 

Gamybos kontrolė yra integruota su kitų modulių funkcijomis. Šis tarpusavio ryšys leidžia pakeisti gamybos užsakymus ir užtikrinti, kad jie būtų automatiškai atnaujinami visuose kituose susijusiuose sistemos procesuose ir skaičiavimuose. Toliau nurodyti sąrankos procesai išvardyti tokia tvarka, kokia juos turėtumėte atlikti.

## <a name="required-baseline-setup-in-other-modules"></a>Kituose modeliuose būtinas pradinis nustatymas
Prieš dirbant su Gamybos kontrole, turi būti nustatyta informacija kituose moduliuose. Ši sąranka apima toliau nurodytas užduotis.

-   Nustatyti bendrą įmonės informaciją.
-   Nustatyti DK.
-   Apibrėžti prekių grupes.
-   Prekių grupėms nustatyti DK sąskaitas.
-   Srityje Atsargų valdymas nustatyti atsargų prekių lentelę.
-   Srityje Atsargų valdymas sukurti komplektavimo specifikacijas (KS) ir KS versijas.

## <a name="required-calendar-and-resource-setup"></a>Būtina kalendoriaus ir išteklių sąranka
Prieš naudodami Gamybos kontrolę, atidarykite modulį Organizacijos administravimas ir toliau nurodyta tvarka sukurkite bei apibrėžkite kalendorių ir operacijų išteklius.

1.  **Darbo laiko šablonai** – nustatyti darbo laiko šablonus, siekiant apibrėžti laiką, kuris galimas gamybai planuoti.
2.  **Kalendoriai** – nustatyti darbo valandų kalendorius, siekiant apibrėžti, kurios metų dienos galimos gamybai planuoti.
3.  **Išteklių grupės** – nustatyti išteklių grupes, siekiant grupuoti operacijų išteklius, kad, vykdant planavimą, būtų galima matyti visų laisvų pajėgumų apžvalgą. Prieš nustatant operacijų išteklius, nustatyti išteklių grupių nereikia. Tačiau rekomenduojame žinoti, kaip, nustatant gamybos kontrolę, grupuoti išteklius.
4.  **Ištekliai** – nustatyti operacijų išteklius, siekiant apibrėžti skirtingus išteklius, naudojamus gamybos procesui užbaigti ir pajėgumams planuoti.

## <a name="required-production-parameters-setup"></a>Būtinas gamybos parametrų nustatymas
**Gamybos kontrolės parametrai** – nustatyti pagrindinius gamybos parametrus, siekiant apibrėžti, kaip sistema tvarko ir apdoroja gamybos užsakymus. Apibrėžti, kaip gamybos užsakymai kuriami, vertinami, planuojami ir naudojami. Taip pat galima pasirinkti norimą grįžtamojo ryšio rūšį ir kaip turėtų būti atliekama išlaidų apskaita.

## <a name="required-journal-name-identification"></a>Būtinas žurnalo pavadinimo identifikavimas
**Gamybos žurnalų pavadinimai** – nurodyti gamybos žurnalų pavadinimus, kurie naudojami įrašyti ir registruoti operacijoms.

## <a name="setup-if-you-use-operations"></a>Nustatyti, jei naudojamos operacijos
Operacijos rodo tam tikrą veiklą, atliekamą siekiant pagaminti galutinį produktą. **Pastaba:** norėdami pagaminti prekę, turite žinoti reikiamų veiklų tipus ir tvarką bei prioritetus. Taip pat turite žinoti, kurie ištekliai naudojami, ir kiek.

1.  **Operacijos** – nustatyti operacijas, rodančias užduotis, kurios turi būti atliktos galutinei prekei pagaminti.
2.  **Ryšiai** – nustatyti operacijų ryšius, siekiant nustatyti tikslias ypatybes. Norėdami nustatyti operacijų ryšius, puslapyje **Operacijos** spustelėkite **Ryšiai**.

## <a name="setup-if-you-use-routes"></a>Nustatyti, jei naudojami maršrutai
Jei naudojate maršrutus, operacijos turi būti apibrėžtos kiekvienam nustatytam gamybos maršrutui. Maršrutas rodo kelią, kurį prekė įveikia nuo operacijos iki operacijos, nuo gamybos proceso pradžios iki pabaigos.

1.  **Išlaidų kategorijos** – nustatyti išlaidų kategorijas, siekiant apibrėžti nustatytų procesų valandines išlaidas ir sąrankos laiką.
2.  **Išlaidų grupės** – nustatyti išlaidų grupes, siekiant sukurti ir prižiūrėti skirtingus išlaidų tipus.
3.  **Maršrutų grupės** – nustatyti maršrutų grupes, siekiant apibrėžti parametrus, kurie yra susiję su maršrutų grupėmis. Prieš kuriant gamybos maršrutus, reikia nustatyti maršrutų grupes.
4.  **Maršrtai** – nustatyti gamybos maršrutus ir apibrėžti numatytąsias nuostatas, siekiant kontroliuoti maršruto operacijų planavimą, įkainojimą ir kainodarą bei kontroliuoti eigos ataskaitas.
5.  **Maršrutai** – nustatyti maršrutų versijas, siekiant įgalinti prekių nuokrypius gamyboje.

## <a name="optional-advanced-settings"></a>Neprivalomos išplėstinės nuostatos
1.  **Gamybos grupės** – nustatyti gamybos grupes, siekiant nustatyti gamybos užsakymo ir DK sąskaitų ryšius. DK sąskaitos naudojamos registruoti arba grupuoti ataskaitų užsakymams.
2.  **Gamybos telkiniai** – sukurti gamybos telkinius, siekiant sugrupuoti gamybos užsakymus, kad būtų galima apdoroti skubius gamybos užsakymus arba panaikinti ir registruoti užsakymų grupes.
3.  **Ypatybės** – apibrėžti ypatybes, siekiant sukurti specialius atributus, kuriuos būtų galima priskirti savo ištekliams ir taip kontroliuoti gamybos tvarką. Šie atributai yra sujungti su darbo laiko šablonu.





