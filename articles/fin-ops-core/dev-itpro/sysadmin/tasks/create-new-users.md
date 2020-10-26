---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982507"
---
# <a name="create-new-users"></a>Naujų vartotojų kūrimas

[!include [banner](../../includes/banner.md)]

Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Susiekite vartotoją su licencija (tik naujų licencijų tipais)
Klientams, kurių licencija yra viena iš naujų licencijų tipų, įtrauktų 2019 m. spalio mėn., vartotojai turi būti susieti su licencija. Vartotojai, kurie susieti su licencija, automatiškai pridedami kaip sistemos vartotojai, kurie neturi vaidmenų pirmą kartą prisiregistravus.

Sistemos administratoriai gali [priskirti licencijas vartotojams](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [„Microsoft 365” administravimo centre](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Išorinio vartotojo susiejimas su licencija (tik su naujais licencijų tipais)
Vartotojai, nepriklausantys nuomotojui, kuriame buvo įdiegta aplinka, turi būti pateikiami pagrindinio nuomotojo kataloge („Azure Active Directory“ („Azure AD“)), kad jiems būtų galima priskirti licencijas. Minėtus išorinius vartotojus reikia įtraukti į „Azure AD“ esantį nuomotoją kaip vartotojus svečius ir priskirti jiems atitinkamas licencijas. Norėdami gauti daugiau informacijos, žr. [„Azure Active Directory“ B2B bendradarbiavimo vartotojų įtraukimas „Azure“ portale](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Naujo vartotojo įtraukimas
1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Vartotojo ID** įveskite vartotojo unikalųjį identifikatorių (ID). Reikės vartotojo ID.  
4. Lauke **Vartotojo vardas** įveskite vartotojo vardą.  
5. Lauke **Domenas** įveskite vartotojo domeną.  
6. Lauke **Pseudonimas** įveskite vartotojo pseudonimą.  
7. Lauke **Įmonė** pasirinkite norimą įmonę. 
8. „FastTab” **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**, kad priskirtumėte vartotojams saugos vaidmenis. Norėdami gauti daugiau informacijos, žr. [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md).
9. Pasirinkite **Gerai**.
10. Pasirinkite **Įrašyti**.

## <a name="import-users"></a>Importuoti vartotojus
1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
2. Veiksmų srityje pasirinkite **Importuoti vartotojus**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Pasirinkite **Importuoti vartotojus**.
5. Pasirinkite **Uždaryti**.

