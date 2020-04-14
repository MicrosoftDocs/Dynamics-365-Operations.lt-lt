---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143586"
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
1. Veiksmų srityje pasirinkite **Importuoti vartotojus**.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Pasirinkite **Importuoti vartotojus**.
4. Pasirinkite **Uždaryti**.

