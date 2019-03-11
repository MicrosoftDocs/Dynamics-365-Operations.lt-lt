---
title: Vartotojas nerastas žmonių parinkiklyje naudojant „Attract“ arba „Onboard“
description: Šioje temoje paaiškinama, ką daryti, kai įmonės nuomotojo vartotojai nerodomi žmonių parinkiklyje naudojant „Dynamics 365 for Talent“ „Attract“ arba „Onboard“ programas.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305534"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>„Azure Active Directory“ vartotojų žmonių parinkiklyje nerasta

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Išduoti

Tam tikri tinkami „Microsoft Azure Active Directory“ („Azure AD“) nuomotojo vartotojai nerodomi, kai ieškoma vardų žmonių parinkiklyje naudojant „Dynamics 365 for Talent“ „Attract“ arba „Onboard“ programas.

## <a name="cause"></a>Priežastis

Šiuo metu tam tikrų tipų vartotojai nepalaikomi „Attract“ ir „Onboard“ programose. Patikrinkite, ar vartotojas nėra „Azure AD“ įmonių (B2B) vartotojas svečias. Vartotojo tipo informaciją galima rasti „Azure“ portalo mentėje „Azure Active Directory“.

Daugiau informacijos apie „Azure B2B“ rasite [Kas yra vartotojo svečio prieiga „Azure Active Directory B2B“](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Ne B2B vartotojai, tam tikrų vartotojų ypatybė Vartotojo tipas gali būti neišsami objekte **Vartotojas**. Tai galima patikrinti ir ištaisyti naudojant „Azure AD PowerShell“ modulį. Daugiau informacijos rasite [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

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
