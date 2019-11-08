---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570526"
---
# <a name="create-new-users"></a>Naujų vartotojų kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Susiekite vartotoją su licencija (tik naujų licencijų tipais)
Klientams, kurių licencija yra viena iš naujų licencijų tipų, įtrauktų 2019 m. spalio mėn., vartotojai turi būti susieti su licencija. Vartotojai, kurie susieti su licencija, automatiškai pridedami kaip sistemos vartotojai, kurie neturi vaidmenų pirmą kartą prisiregistravus. Vartotojai, kurie nesusieti su licencija, gauna įspėjamąjį pranešimą.

Sistemos administratoriai gali [priskirti licencijas vartotojams](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [„Microsoft 365” administravimo centre](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Naujo vartotojo įtraukimas
1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Vartotojo ID** įveskite vartotojo unikalųjį identifikatorių (ID). Reikės vartotojo ID.  
4. Lauke **Vartotojo vardas** įveskite vartotojo vardą.  
5. Lauke **Domenas** įveskite vartotojo domeną.  
6. Lauke **Pseudonimas** įveskite vartotojo pseudonimą.  
7. Lauke **Įmonė** pasirinkite norimą įmonę. 
8. „FastTab” konteineryje **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**, kad [priskirtumėte vartotojams saugos vaidmenis](assign-users-security-roles.md).
9. Pasirinkite **Gerai**.
10. Pasirinkite **Įrašyti**.

## <a name="import-users"></a>Importuoti vartotojus
1. Veiksmų srityje pasirinkite **Importuoti vartotojus**.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Pasirinkite **Importuoti vartotojus**.
4. Pasirinkite **Uždaryti**.

