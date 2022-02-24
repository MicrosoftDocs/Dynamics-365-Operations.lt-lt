---
title: Įsigijimo katalogo kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo eigą.
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaf8b8d8b369aa704344d6984a0f111af6e4285b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016482"
---
# <a name="create-a-procurement-catalog"></a>Įsigijimo katalogo kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti darbo eigą. Šią užduotį paprastai atlieka įsigijimo specialistas. Taip pat sužinosite, kaip kurdami paraišką darbuotojai gali naudoti katalogą. Prieš kuriant katalogą, sistemoje turi būti nustatyta įsigijimo kategorijų hierarchija. Naujas katalogas perima hierarchiją ir visus hierarchijos produktus. Šį vedlį galite naudoti demonstracinių duomenų įmonėje USMF, kurioje įgalinta įsigijimo kategorijų hierarchija, taip pat procedūros veiksmų pavyzdžiuose.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Įsitikinkite, kad įsigijimo kategorijų hierarchija nustatyta
1. Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir šaltiniai > Įsigijimo kategorijos**. Demonstracinių duomenų įmonėje USMF galima naudoti įsigijimo kategorijų hierarchiją, be to, produktai yra įtraukti į kategoriją **Biuro mašinos arba kompiuteriai**. Jei šią procedūrą vykdote kaip užduočių vedlį, turėsite jį atrakinti, kad galėtumėte naršyti kategoriją. Jei hierarchija nesukurta, galite ją kurti spustelėdami **Nauja**. Tai galima atlikti tik vieną kartą.  
2. Uždarykite puslapį.

## <a name="create-a-catalog"></a>Katalogo kūrimas
1. Pasirinkite **Naršymo sritis > Moduliai > įsigijimas ir šaltinio pasirinkimas > Katalogai > Įsigijimo katalogai**.
2. Spustelėdami **Naujas įsigijimo katalogas** atidarykite išplečiamąjį dialogo langą.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Pasirinkite **Gerai**.
5. Medyje išplėskite **CORP ĮSIGIJIMO KATEGORIJOS**.
6. Medyje išplėskite **BIURO MAŠINOS**.
7. Medyje pasirinkite **Kompiuteriai**.

  - Sąraše rodomi įsigijimo kategorijos produktai. Jei į kategoriją norite įtraukti produktą, tai turite atlikti puslapyje **Įsigijimo kategorijų hierarchija** arba puslapyje **Prekės informacija**.  
  - **Numatytasis** naujinimo tipas nustato, ar nauji į įsigijimo kategorijų hierarchiją įtraukti produktai yra iš karto matomi kataloge. Jei naujinimo tipas nustatytas kaip **Dinamiškas**, keitimai matomi iš karto. Jei naujinimo tipas nustatytas kaip **Statinis**, katalogą naudojantys asmenys naujus produktus matys tik tada, kai katalogas bus iš naujo publikuotas. Veiksmas **Publikuoti** pateikiamas puslapio viršuje esančioje veiksmų srityje. Jei produktai pašalinami iš įsigijimo kategorijų hierarchijos, pakeitimas matomas iš karto, neatsižvelgiant į lauko **Numatytasis** naujinimo tipas reikšmę.  

8. Veiksmų srityje pasirinkite **Kategorijos naršymas** ir įsitikinkite, kad pasirinkta parinktis **Įjungti**.
9. Pasirinkite **Suaktyvinti katalogą**.
10. Uždarykite puslapį.

## <a name="make-the-catalog-visible"></a>Nustatyti katalogą kaip matomą
1. Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos**.
2. Pasirinkite **Įsigijimo strategijos USMF**. Turite pasirinkti juridinio subjekto pirkimo strategiją, pagal kurią su jūsų vartotojo profilių susietas darbuotojas gali užsakyti produktus. USMF demonstraciniuose duomenyse vartotojas administratorius yra susietas su darbuotoja, vardu **Julia Funderburk**, ir ji USMF produktus užsako pagal numatytuosius parametrus.  
3. Pasirinkite katalogą, kurį ką tik sukūrėte.
4. Pasirinkite **Gerai**.

## <a name="use-the-catalog"></a>Naudoti katalogą
1. Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo paraiškos > Visos pirkimo paraiškos**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Pasirinkite **Gerai**.
5. Pasirinkite **Įtraukti produktus**.
6. Sąraše raskite ir pasirinkite norimą įrašą. Norėdami filtruoti produktus, galite naudoti kategorijų hierarchiją sąrašo kairėje pusėje arba filtrą sąrašo viršuje.  
7. Pasirinkite **Įtraukti į eilutes**.
8. Pasirinkite **Gerai**.

