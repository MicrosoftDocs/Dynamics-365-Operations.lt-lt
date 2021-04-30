---
title: „Dynamics 365 Commerce“ ir „Microsoft Teams“ integravimo DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie„ Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908861"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>„Dynamics 365 Commerce“ ir „Microsoft Teams“ integravimo DUK

[!include [banner](includes/banner.md)]

Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie„ Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Kas parduotuvėje tampa komandos savininku, kol „Teams” parengiama iš „Commerce”? 

Visi parduotuvių vadovai automatiškai įtraukiami kaip savininkai į atitinkamą komandos grupę, kad jie galėtų atlikti operacijas, pavyzdžiui, įtraukti privatų kanalą ir įtraukti ar panaikinti narius. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Kaip priskirti „komunikacijos vadovo” vaidmenį darbuotojui „Commerce” būstinėje? 

Komunikacijos vadovai „Microsoft Teams” platformoje turi galimybę kurti ir publikuoti užduočių sąrašus. Organizacijos darbuotojams, kurie turėtų tapti komunikacijos vadovais, turi būti priskirtas „mažmeninės prekybos užduočių vadovo” vaidmuo „Commerce” būstinėje.

Norėdami darbuotojui priskirti mažmeninės prekybos užduočių vadovo vaidmenį, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Darbuotojai \> Vartotojai**.
1. Pasirinkite darbuotoją.
1. „FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**.
1. Dialogo lange **Priskirti vaidmenis vartotojui** pasirinkite vaidmenį **Mažmeninės prekybos užduočių vadovas**, tada pasirinkite **Gerai**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Kaip padaryti, kad būtų galima įkelti konkrečią organizacijos hierarchiją į „Microsoft Teams”?

„Commerce” būstinėje kiekviena organizacijos hierarchija yra susieta su vienu arba daugiau tikslų. Įsitikinkite, kad hierarchijoje, kurią norite parengti į „Microsoft Teams”, yra su ja susietas **Mažmeninės prekybos ataskaitų** tikslas, kaip parodyta toliau pateiktame pavyzdyje. 

![Organizacijos hierarchijos tikslo pavyzdys „Commerce” būstinėje](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Kaip įgalinti mažmeninės prekybos parduotuvės darbuotojus prisijungti prie „Commerce” elektroninio kasos aparato (EKA) naudojant „Azure Active Directory” („Azure AD”)?

Informaciją apie tai, kaip sukonfigūruoti „Commerce” EKA prisijungimo patirtį, kad būtų naudojamas „Azure AD” autentifikavimas, rasite [„Azure Active Directory” autentifikavimo įgalinimas EKA prisijungimui](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Kaip susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje, jei mano organizacija jau sukūrė komandas „Microsoft Teams” platformoje?

Informaciją apie tai, kaip susieti parduotuves ir komandas, jeigu yra išankstinių komandų, rasite [Susiekite parduotuves ir atitinkamas komandas, jeigu jūsų organizacija turi išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Kaip išvalyti „Microsoft Graph API” atpažinimo ženklą, saugomą seanso saugykloje?

Vartotojas, prisijungęs prie elektroninio kasos aparato (EKA) su „Azure Active Directory” („Azure AD”) abonementu, turi atsijungti nuo EKA arba uždaryti programą, kad išvalytų seanso saugyklą. 

> [!TIP]
> Rekomenduojama geriausia praktika yra ta, kad darbuotojai visada užrakintų EKA terminalą arba atsijungtų nuo seanso, kai nenaudoja terminalo. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Kas atsitinka, jei parduotuvėje neturi parduotuvės vadovų?

Jei parduotuvėje nėra vadovų, komandos grupė nebus sukurta parduotuvei ar „Teams” platformoje. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Kas atsitinka, jeigu parduotuvės vadovas išeina iš įmonės?

Kiekvienas asmuo, turintis savininko vaidmenį, gali įtraukti naują parduotuvės vadovą „Commerce” būstinėje ir iš naujo parengti „Teams” tam, kad naujas vadovas turėtų reikiamas grupės teises „Teams” platformoje. 

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA](synchronize-tasks-teams-pos.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)
