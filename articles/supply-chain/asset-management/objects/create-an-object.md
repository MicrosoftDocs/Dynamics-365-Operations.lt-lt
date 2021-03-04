---
title: Turto kūrimas
description: Šioje temoje paaiškinta, kaip kurti turtą turto valdyme.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 045bb59642d766ac23939dee0900ea6911fe50fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433372"
---
# <a name="create-an-asset"></a>Turto kūrimas

[!include [banner](../../includes/banner.md)]

 

Šioje temoje paaiškinta, kaip kurti turtą turto valdyme.

1. Spustelėkite **Turto valdymas** > **Bendras** > **turtas** > **Visas turtas** arba **Aktyvus turtas**.
2. Spustelėkite mygtuką **Naujas**.
3. Dialogo lange **Kurti turtą** įterpkite duomenis apie **Turtą** (turto ID) ir turto pavadinimą. Pasirinkite turto datą ir laiką lauke **Galioja**. Nuo tos datos bus galima diegti turtą funkcinėje vietoje, taip pat perkelti ir pakeisti turtą turto struktūroje.
4. Lauke **Turto tipas** pasirinkite turto tipą (privalomas laukas). Jei reikia, pasirinkite informaciją **Turto gamintojas** ir **Turto modelis**. Jei nustatytas tik vienas produktas, tas produktas automatiškai parenkamas lauke **Turto gamintojas**. Laukeliuose **Turto gamintojas** ir **Turto modelis** galimi pasirinkimai priklauso nuo nustatymų [Turto gamintojai ir modeliai](../setup-for-objects/product-and-model.md).
5. Grupėje **Pagrindinis turtas** laukas **Turtas** paliktas tuščias kaip numatytasis. Jei reikia, galite pasirinkti pagrindinį turtą, tada visi laukai grupėje **Pagrindinis turtas** bus automatiškai užpildyti.
    >[!NOTE]  
    >Pasirinkus pagrindinį turtą teikiami du arba trys skirtukai: skirtuke **Mano turtas** yra turtas, susijęs su funkcinėmis vietomis, į kurias galite būti priskirtas (sistemoje užregistruotas priežiūros darbuotojas). Jei formoje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md) nėra nustatyta jokia priežiūros darbuotojo funkcinė vieta, skirtukas **Mano turtas** nerodomas. Skirtuke **Aktyvus turtas** yra viso turto, kurio turto ciklo būsena „Aktyvi“, sąrašas. Skirtuke **Turto rodinys** rodomas funkcinių vietų ir tose vietose įdiegto turto medžio rodinys.

6. Nustatyta numatytoji funkcinė vieta siūloma turtui grupės **Turtas** > lauke **Funkcinė vieta**. Jei reikia, pasirinkite kitą funkcinę vietą.

    >[!NOTE]
    >Sukūrus turtą jį galima diegti kitoje funkcinėje vietoje. Funkcinėje vietoje galima diegti tik aukščiausio lygio turtą (turtą be esamo pagrindinio turto). Tai reiškia, kad pasirinktoje funkcinėje vietoje diegiamas aukščiausio lygio turtas ir visi antriniai turtai. Daugiau informacijos apie turto diegimą funkcinėse vietose rasite skyriuje [Funkcinių vietų pristatymas](../functional-locations/introduction-to-functional-locations.md).

7. Spustelėkite **Gerai**.
8. Sąraše **Visas turtas** pasirinkite turtą, tada spustelėkite mygtuką **Redaguoti**, kad įtrauktumėte papildomos turto informacijos.

## <a name="general-information"></a>Bendroji informacija

Funkcinė vieta, su kuria susijęs turtas, rodoma lauke **Funkcinė vieta**. Jei turtas yra pagrindinis turtas, su turtu susijusių antrinių elementų skaičius rodomas lauke **Antriniai elementai**. Jei turtas yra antrinis esamo turto turtas, lauke **Pagrindinis elementas** rodomas pagrindinio turto ID.

Galite redaguoti **Turto gamintojo** ir **Turto modelio** informaciją apie turtą, kuris naudojamas atsarginėms dalims, alternatyvioms atsarginėms dalims ir užduoties tipo numatytosioms reikšmėms valdyti. Daugiau informacijos rasite [Turto gamintojai ir modeliai](../setup-for-objects/product-and-model.md). Taip pat galite įtraukti informacijos apie **Modelio metus** ir **Serijos numerį**.

**Dabartinė ciklo būsena** naudojama nustatyti, ar turtas aktyvus, ar neaktyvus. Kuriant turtą etapas visada nustatomas kaip pirmasis turto etapų grupės etapas. Kai esate pasirengę aktyvinti turtą, spustelėkite **Naujinti turto būseną**, tada pasirinkite ciklo būseną, kurią apibrėžėte kaip „aktyvus turtas“, ir spustelėkite **Gerai**.

**Pastaba:** kai turtas nustatytas kaip „neaktyvus“, nebegalima kurti turto darbo užsakymų. Be to, negalima planuoti prevencinių priežiūros užduočių neaktyviam turtui.

Laukai **Aptarnavimo lygis** ir **Kritiškumas** susiję su sukurtais turto darbo užsakymais. Laukuose rodomi turto dabartinės sąrankos **Aptarnavimo lygio** ir **Kritiškumo** duomenys. Informacijos apie tų reikšmių nustatymą rasite [Turto aptarnavimo lygiai](../setup-for-objects/object-priorities.md) ir [Turto kritiškumo tipai](../setup-for-objects/object-criticalities.md).

## <a name="asset"></a>Ilgalaikio turto

Galite pasirinkti turto **Išteklius**. Išteklių pasirinkimas nustato, kuris kalendorius naudojamas darbo užsakymo tvarkaraščiams. Išteklių pasirinkimas dažnai naudojamas ilgalaikiam turtui. Ištekliai ir išteklių grupės nustatomi srityje **Organizacijos administravimas** > **Ištekliai** > **Išteklių grupės** arba **Ištekliai**.

Lauke **Ilgalaikio turto skaičius** galite pasirinkti ilgalaikį turtą, kuris bus susietas su turtu. Tai aktualu, jei turtas susijęs su investicijų projektu.

- Jei turtas susijęs su ilgalaikiu turtu, galite kurti darbo užsakymo tipą, kuris bus naudojamas darbo užsakymams, susijusiems su investicijų projektu. 
- Informacija apie turto ilgalaikį turtą susijusi su moduliu **Ilgalaikis turtas** Dynamics 365 Supply Chain Management. Tai reiškia, kad dalyse **Ilgalaikis turtas** > **Ilgalaikis turtas** > **Ilgalaikis turtas** galite gauti turto valdymo projektų, kurie gali būti susiję su ilgalaikiu turtu, apžvalgą pasirinkdami turtą sąraše ir peržiūrėdami turinį srities **Susijusi informacija** > dalyje **Susiję projektai**.


## <a name="details"></a>Išsami informacija

Lauke **Aktyvusis nuo** rodoma data, kai turto ciklo būsena buvo atnaujinta į aktyvią būseną (žr. [Turto ciklo būsenos](../setup-for-objects/object-stages.md), kur pateikta informacija apie turto ciklo būsenų nustatymą). Jei turtas nebeaktyvus ir atnaujinome turto ciklo būseną į neaktyvią ciklo būseną, data, nuo kurios turtas yra neaktyvus, rodoma lauke **Aktyvus iki**. Prireikus datas galima keisti rankiniu būdu.

Jei reikia, lauke **Pakeitimo data** galite įterpti numatomą turto pakeitimo datą. Numatomą turto pakeitimo reikšmę galima įterpti lauke **Pakeitimo reikšmė**. Pavyzdys: galite naudoti pakeitimo informaciją, kad palygintumėte ją su turto išlaikymo išlaidomis ir vėliau priimtumėte sprendimą dėl naujo turto įsigijimo, jei esamo turto priežiūros išlaidos sparčiai padidėja.

## <a name="notes"></a>Pastabos

„FastTab“ skirtuke **Pastabos** galima įtraukti su turtu susijusių pastabų. Prieš įvesdami pastabą spustelėkite mygtuką **Įtraukti laiko žymę**, jeigu norite įtraukti į pastabą vartotojo informaciją ir datos / laiko žymę.

## <a name="attributes"></a>Atributai

Šiame „FastTab“ galite nustatyti turto atributų reikšmes. Šie atributai gali būti naudojami siekiant apibūdinti su turtu susijusias savybes arba ypatybes, pvz., dydį, svorį arba mašinos konfigūraciją.

Spustelėkite **Įtraukti eilutę**, tada pasirinkite atributo tipą. Tada įterpkite **Reikšmę**, susijusią su atributo tipu, ir išsaugokite įrašą.

>[!NOTE] 
>Galite gauti turto atributų tipų apžvalgą ir jų ryšį su turtu dalyse **Turto atributas** ir **Turto atributų apžvalga**. Daugiau informacijos žr. [Turto atributų apžvalga](../objects/object-specification-overview.md).

## <a name="vendor"></a>Tiekėjas

„FastTab“ **Tiekėjas** pasirinkite turto tiekėjo sąskaitą. Be to, jei buvo suteikta tiekėjo garantija, galite čia įterpti garantijos informaciją.

## <a name="address"></a>Adresas 

„FastTab“ **Adresas** galite įterpti įrangos adresą. Jei į turtą neįtraukiamas joks adresas, turtas naudoja pagrindinio turto adresą, jei pagrindinis turtas turi adresą. Jei turto hierarchijoje adresas nėra susietas su turtu arba pagrindiniais elementais, gali būti naudojamas funkcinės vietos, kurioje įdiegtas turtas, adresas. Jei ta funkcinė vieta neturi su juos susieto adreso, turtui naudojamas pagrindinės funkcinės vietos adresas.

## <a name="asset-management-plans"></a>Turto valdymo planai

Priežiūros planai naudojami turto prevencinės priežiūros darbų reguliariais intervalais planavimui. Šiame „FastTab“ galima nustatyti pasirinkto turto priežiūros plano eilutes. Galima nustatyti įvairaus turto priežiūros ciklus, kuriais būtina atlikti panašią užduotį reguliariais intervalais. Skirtuke **Funkcinės vietos priežiūros planai** pateikti priežiūros planai, susiję su funkcine vieta, kurioje įdiegtas turtas.

>[!NOTE]
>Jei panaikinsite priežiūros plano eilutę arba priežiūros ciklą, susijusį su turtu, srityje **Visas turtas**, bus automatiškai panaikinti visi priežiūros grafikai, kurių būsena „Sukurtas“ ir kurie buvo sukurti atsižvelgiant į tą priežiūros planą ar priežiūros ciklą.

## <a name="functional-location-maintenance-plans"></a>Funkcinės vietos priežiūros planai

Šiame „FastTab“ pateikta priežiūros planų, susijusių su funkcine vieta, kurioje buvo įdiegtas turtas, apžvalga.

## <a name="maintenance-rounds"></a>Priežiūros ciklai

Šiame „FastTab“ galite įtraukti arba šalinti priežiūros ciklus, kurie yra susiję su turtu.

## <a name="financial-dimensions"></a>Finansinės dimensijos

Turtui galima pasirinkti finansines dimensijas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]