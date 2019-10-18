---
title: Vartotojas nerastas žmonių parinkiklyje naudojant „Attract“ arba „Onboard“
description: Šioje temoje paaiškinama, ką daryti, kai įmonės nuomotojo vartotojai nerodomi žmonių parinkiklyje naudojant „Dynamics 365 Talent“ „Attract“ arba „Onboard“ programas.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2a3c83fcc3f48aa235ffb2db2dc492b34a306c4c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024199"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>„Azure Active Directory“ vartotojų žmonių parinkiklyje nerasta

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Išduoti

Tam tikri tinkami „Microsoft Azure Active Directory“ („Azure AD“) nuomotojo vartotojai nerodomi, kai ieškoma vardų žmonių parinkiklyje naudojant „Dynamics 365 Talent: Attract“ „Dynamics 365 Talent: Onboard“ programas.

## <a name="cause"></a>Priežastis

Šiuo metu tam tikrų tipų vartotojai „Attract“ ir „Onboard“ nepalaikomi. Patikrinkite, ar vartotojas nėra „Azure AD“ įmonių (B2B) vartotojas svečias. Vartotojo tipo informaciją galima rasti „Azure“ portalo mentėje „Azure Active Directory“.

Daugiau informacijos apie „Azure B2B“ rasite [Kas yra vartotojo svečio prieiga „Azure Active Directory B2B“](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

Ne B2B vartotojai, tam tikrų vartotojų ypatybė Vartotojo tipas gali būti neišsami objekte **Vartotojas**. Tai galima patikrinti ir ištaisyti naudojant „Azure AD PowerShell“ modulį. Daugiau informacijos rasite [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Nutarimas

Norint atlikti tolesnius veiksmus ir išspręsti problemą, jums reikia turėti tipo Visuotinis administratorius teises „Azure Active Directory“ nuomotojuje arba tipo **User.ReadWrite.All** teises.

Kaip patikrinti paveikto vartotojo ypatybę Vartotojo"tipas.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Komanda pateikia toliau nurodytą informaciją.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Įsidėmėkite vartotojo ypatybę **UserType**. Jei laukas **UserType** yra tuščias, pavyzdžiui ne Narys arba Svečias, atnaujinkite lauką **UserType**naudodami toliau nurodytą komandą.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
