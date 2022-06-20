---
title: Nustatyti pažangų banko suderinimo importavimą naudojant elektronines ataskaitas
description: Šiame straipsnyje paaiškinama, kaip naudoti elektronines ataskaitas išplėstiniam banko suderinimo importavimo procesui nustatyti.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889126"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Nustatyti pažangų banko suderinimo importavimą naudojant elektronines ataskaitas

[!include [banner](../includes/banner.md)]

Išplėstinės banko suderinimo priemonė leidžia importuoti elektroninius banko išrašus ir automatiškai suderinti juos Microsoft Dynamics su banko operacijomis,-365 finansuose. Šiame straipsnyje paaiškinama, kaip nustatyti banko išrašų importavimo funkciją. Banko išrašo importavimo nustatymas priklauso nuo elektroninio banko išrašo formato. Microsoft Dynamics 365 Finansai palaiko tris banko išrašų formatus: ISO20022, MT940 ir BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroninių ataskaitų konfigūracijos parametrai

1. Eikite į **darbo sričių elektronines \> ataskaitas**.
2. "Microsoft" konfigūracijos teikėjo **išklotijoje** pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Jei reikia užmegzti ryšį su saugykla, dialogo lange pasirinkite mėlyną saitą.
5. Konfigūracijos sąraše rasti BAI2 banko **išrašo \> modelio banko išrašo modelį**.
6. **Pasirinkti BAI2** formatą.
7. Skirtuke **Versijos** FastTab pasirinkite naujausią versiją, tada pasirinkite **Importuoti**.

## <a name="set-up-the-bank-statement-format"></a>Banko išrašo formato nustatymas

1. Eikite į **grynųjų pinigų ir banko valdymo \> nustatymą Išplėstinis \> banko suderinimo nustatymo banko išrašo \> formatas**.
2. Pasirinkite **Nauja**.
3. Nustatykite išrašo **formatą** ir **pavadinimo** laukus.
4. Pažymėkite žymės **langelį Bendrasis elektroninio importavimo** formatas.
5. Nustatyti importavimo **formato konfigūracijos** lauką **BAI2** formatu.

## <a name="set-up-the-bank-account"></a>Nustatyti banko sąskaitą

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.
2. Atidarykite banko sąskaitą.
3. Suderinimo "**FastTab**" nustatykite išplėstinio **banko suderinimo pasirinktį** kaip **Taip**.
4. Nustatyti anksčiau **sukurto** BAI2 **formato išrašo** formato lauką.

## <a name="import-the-bank-statement"></a>Importuoti banko išrašą

1. Eiti į grynųjų **pinigų ir banko valdymo banko išrašų \> suderinimo banko išrašus \>**.
2. Banko išrašų puslapio **viršuje pasirinkite** Importuoti **išrašą**.
3. Išraše **nustatykite** banko sąskaitos lauką kaip banko sąskaitą.
4. Nustatyti anksčiau **sukurto** BAI2 **formato išrašo** formato lauką.
5. Pasirinkite **Naršyti** ir pasirinkite **BAI** failą.
6. Pasirinkite **Nusiųsti**.
7. Pasirinkite **Gerai**, jei norite importuoti pasirinktą failą.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banko išrašų formatų ir techninių maketų pavyzdžiai
Toliau pateikiami išplėstinio banko derinimo importavimo failo techninio maketo aprašų pavyzdžiai ir trys susijusių banko išrašo failų pavyzdžiai: [Importavimo failų pavyzdžiai](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Techninio maketo aprašas                             | Banko išrašo failo pavyzdys          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

