---
title: Kurti pirkimo sutartį
description: Šis straipsnis padės jums sukurti pirkimo sutartį.
author: GalynaFedorova
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 108c3a47132b262ebe2e15f00d26191b75469959
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877572"
---
# <a name="create-a-purchase-agreement"></a>Kurti pirkimo sutartį

[!include [banner](../../includes/banner.md)]

Šis straipsnis padės jums sukurti pirkimo sutartį. Paprastai tai atlieka pirkimo vadybininkas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami turite nustatyti pirkimo sutarčių klasifikacijas. Sukūrę sutartį, galėsite ją naudoti, kai sukursite PU – pirkimo sutarties sąlygos bus nukopijuotos į antraštę ir į visas užsakymo eilutes, susijusias su šia sutartimi.


## <a name="create-a-new-purchase-agreement"></a>Kurti naują pirkimo sutartį
1. Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir išteklių paskirstymas > Pirkimo sutartys > Pirkimo sutartys**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo klientas** pažymėkite išskleidžiamąjį meniu, tada pažymėkite pageidaujamo įrašo eilutę.
4. Lauke **Pirkimo sutarčių klasifikacija** pažymėkite išskleidžiamąjį meniu, tada pažymėkite pageidaujamo įrašo eilutę.
5. Išplėskite **Bendra** FastTab.
6. Lauke **Galiojimo data** įveskite datą.

    - Ši galiojimo data bus numatytoji visose įsipareigojimų eilutėse ir nulems, kiek laiko galios kiekvienas konkretus įsipareigojimas.  

7. Lauke **Dokumento pavadinimas** įveskite savo pirkimo sutarties pavadinimą.

    - Palikite lauką **Numatytasis įsipareigojimas** nustatytą kaip **Produkto kiekio įsipareigojimas** (arba pakeiskite, jei nustatyta kitaip).  
    - Numatytoji įsipareigojimo reikšmė nurodo jūsų parinktis sutarties eilutėse. Jei jums reikia naujo įsipareigojimo tipo kuriant sutarties eilutes, turite pakeisti numatytąjį įsipareigojimą antraštėje. Yra 4 tipų įsipareigojimai: **Produkto kiekio įsipareigojimas** – skirta konkrečiam produkto kiekiui, **Produkto vertės įsipareigojimas** – skirta konkrečiai produkto sumos valiutai, **Produkto kategorijos įsipareigojimas** – skirta konkrečios valiutos sumai įsigijimo kategorijoje, kurioje suma gali būti skirta katalogo elementui arba ne katalogo elementui, **Vertės įsipareigojimas** – skirta konkrečios valiutos sumai, kurią galima užpildyti naudojant produktą arba įsigijimo kategoriją.  

8. Pasirinkite **Gerai**.

## <a name="add-a-commitment"></a>Įtraukti įsipareigojimą
1. Pasirinkite **Pridėti eilutę**.
2. Lauke **Elemento numeris** išplečiamajame meniu pasirinkite norimą įrašą.
3. Lauke **Kiekis** įveskite skaičių. Tai yra bendras kiekis, kurį susitarėte pirkti iš tiekėjo.  
4. Lauke **Vieneto kaina** įveskite skaičių.
5. Išplėskite skyrių **Eilutės informacija** section.
6. Parinktį **Maksimaliai vykdoma** nustatykite į **Taip**. Parinktis **Maksimaliai vykdoma** apriboja įsipareigojimų naudojimą. Galite pirkti iki kiekio, kuris nurodytas eilutės lauke **Kiekis**.  

## <a name="add-header-conditions"></a>Įtraukti antraštės sąlygas
1. Veiksmų srityje pasirinkite **Parinktys**.
2. Pasirinkite **Keisti rodinį**.
3. Pasirinkite **Antraštės rodinys**.
4. Išplėskite skyrių **Sąlygos**.
5. Lauke **Mokėjimo metodas** išplečiamajame meniu pažymėkite pageidaujamą įrašą. Čia pagal numatytuosius nustatymus rodomos mokėjimo sąlygos iš tiekėjo sąskaitos.  
6. Lauke **Pristatymo režimas** išplečiamajame meniu pažymėkite pageidaujamą įrašą.
7. Lauke **Pristatymo sąlygos** pažymėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.

## <a name="confirm-and-activate-the-agreement"></a>Patvirtinti ir aktyvinti sutartį
1. Veiksmų srityje pasirinkite **Pirkimo sutartis**.
2. Pasirinkite **Patvirtinimas**. Nustatykite parinktį **Pažymėti sutartį kaip galiojančią** į **Taip**.  
3. Pasirinkite **Gerai**.
4. Veiksmų srityje pasirinkite **Pirkimo sutartis**.
5. Pasirinkite **Pirkimo sutarties patvirtinimai**. Parinktis **Peržiūrėti / spausdinti** leidžia generuoti pirkimo sutarties dokumentą, kurį galite spausdinti arba siųsti tiekėjui. Jei vėliau sutartį atnaujinsite ir iš naujo patvirtinsite, abi jos versijos bus rodomas čia.  
6. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]