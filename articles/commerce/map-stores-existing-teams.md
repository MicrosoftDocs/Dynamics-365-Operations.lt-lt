---
title: Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje
description: Šiame straipsnyje aprašoma, kaip susieti parduotuves ir atitinkamas komandas Dynamics 365 Commerce būstinėje, jei jūsų organizacija jau sukūrė komandas Microsoft Teams prieš "Commerce" integravimą.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 67a1a79dd74d411aa7e21000c8baaa8a069cede7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279125"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip susieti parduotuves ir atitinkamas komandas Dynamics 365 Commerce būstinėje, jei jūsų organizacija jau sukūrė komandas Microsoft Teams prieš "Commerce" integravimą.

Gali būti, jog jūsų organizacija sukūrė komandas kai kurioms arba visoms jūsų parduotuvėms dar prieš „Dynamics 365 Commerce” ir „Microsoft Teams” integravimą. Tokiu atveju, norėdami nustatyti užduočių sinchronizavimą tarp „Commerce” EKA ir „Microsoft Teams”, turite susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Parduotuvių ir atitinkamų komandų susiejimas „Commerce” būstinėje 

Norėdami susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje, atlikite šiuos veiksmus.

1. Eikite į **Sistemos Administravimas \> Darbo sritis \> Duomenų valdymas**.
1. Pasirinkite **Eksportuoti**. 
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dalyje **Grupės pavadinimas** įveskite „Eksportuoti „Teams” susiejimą”.
1. „FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti objektą**. Atsiranda dialogo langas **Įtraukti objektą**.  
1. Išplečiamajame sąraše **Objekto pavadinimas** pasirinkite **„Teams” susiejimas tarp šaltinio ir komandos**.
1. Išplečiamajame sąraše **Paskirties duomenų formatas** pasirinkite **„CSV”**.
1. Pasirinkite **Įtraukti**, o tada pasirinkite **Uždaryti**.
1. Veiksmų srities viršutinėje kairėje pusėje, pasirinkite **Eksportuoti dabar**.
1. Dalyje **Objekto apdorojimo būsena** pasirinkite **Atsisiųsti failą**.
1. Eksportuotame CSV failuose į laukus **ŠALTINIO TIPAS**, **ŠALTINIO ID** ir **KOMANDOS ID** įveskite tokias reikšmes:
    - Į **ŠALTINIO TIPAS** įveskite „Mažmeninės prekybos parduotuvė”. 
    - Į **ŠALTINIO ID** įveskite parduotuvės numerį (pavyzdžiui, „000135” San Fransisko parduotuvei). Parduotuvių numerius galite rasti **Mažmeninė prekyba ir komercija \> Kanalai \> Parduotuvės**.
    - Į **KOMANDOS ID** įveskite atitinkamos komandos ID iš „Microsoft Teams” (pavyzdžiui, „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c”). Komandos ID informaciją galite rasti [svetainėje admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Įrašykite CSV failą į savo vietinį kompiuterį.
1. Eikite į **Sistemos Administravimas \> Darbo sritis \> Duomenų valdymas**, o tada pasirinkite **Importuoti**.
1. „FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti failą**. Atsiranda dialogo langas **Įtraukti failą**.
1. Išplečiamajame sąraše **Objekto pavadinimas** pasirinkite **„Teams” susiejimas tarp šaltinio ir komandos**.
1. Išplečiamajame sąraše **Šaltinio duomenų formatas** pasirinkite **„CSV”**.
1. Pasirinkite **Įkelti ir įtraukti**, tada pasirinkite anksčiau įrašytą CSV failą ir **Atidaryti**.
1. Dialogo lange **Įtraukti failą** pasirinkite **Uždaryti**.
1. Veiksmų srityje pasirinkite **Įrašyti**, o tada pasirinkite **Importuoti**.

Šiame pavyzdyje rodoma „Commerce” esanti **Komandų susiejimo eksportavimo** grupė su **Įtraukti objektą** elementais ir išryškintomis CSV failo antraštėmis.

![Komandų susiejimo eksportavimo grupė su objekto įtraukimo elementais ir išryškintomis CSV failo antraštėmis.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Atlikę ankstesnius veiksmus, atlikite skyriuje [Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir EKA](synchronize-tasks-teams-pos.md) nurodytus veiksmus, jei norite sinchronizuoti užduočių valdymą. 

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA](synchronize-tasks-teams-pos.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)
