---
title: „ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas
description: Šioje temoje aprašoma, kaip įgalinti „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9910ee48a0792c89a4e04ec8685fd02484e45575d70b06454dea56a89ee8c914
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775343"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>„ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įgalinti „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.

Norėdami sukonfigūruoti „Teams” su informacija iš „Dynamics 365 Commerce” ir sinchronizuoti užduočių valdymo funkcijas tarp „Teams” ir elektroninio kasos aparato (EKA) programos, turite įgalinti integravimo funkcijas „Commerce” būstinėje.

> [!NOTE]
> Kai įgalinate „Teams” integravimą, sutinkate su „Teams” bendrinti savo duomenis. Su „Teams” bendrinami duomenys gali priklausyti kitai šaliai nei jūsų „Commerce” duomenys ir jiems gali būti taikomi skirtingi atitikties standartai. Daugiau informacijos rasite [„Microsoft” patikimumo centras](https://www.microsoft.com/trust-center). Daugiau informacijos apie „Microsoft” privatumo politikas rasite [„Microsoft” privatumo nuostatos](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>„Teams” integravimo įgalinimas

Prieš įgalindami „Microsoft Teams” integravimą su „Commerce”, turite užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.

Norėdami užregistruoti „Teams” programą savo nuomotojui „Azure” portale, atlikite šiuos veiksmus.

1. Atlikite skyriuje [Greitas pasirengimas darbui: Registruoti programą „Microsoft” tapatybės platformoje](/azure/active-directory/develop/quickstart-register-app) pateiktus veiksmus, norėdami užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.
1. Nukopijuokite **Programos (kliento) ID** reikšmę iš **Apžvalgos** puslapio užregistruotai programai. Šią reikšmę naudosite „Teams” integravimo įgalinimui „Commerce” būstinėje.
1. Nukopijuokite sertifikato reikšmę, kuri buvo įvesta, kai [įtraukėte sertifikatą](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) 1 veiksme. Sertifikatas taip pat vadinamas viešuoju raktu arba programos raktu. Šią reikšmę naudosite „Teams” integravimo įgalinimui „Commerce” būstinėje.

Norėdami įgalinti „Teams” integravimą „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūracija**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Nustatykite parinktį **Įgalinti „Microsoft Teams” integravimą** į **Taip**.
1. Laukuose **Programos ID** ir **Programos raktas** įveskite reikšmes, gautas registruojant „Teams” programą „Azure” portale.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Šioje iliustracijoje pateikiamas „Teams” integravimo „Commerce” būstinėje konfigūracijos pavyzdys.

![„Teams” integravimo konfigūracija „Commerce” būstinėje.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>„Teams” integravimo išjungimas

Norėdami išjungti „Microsoft Teams” integravimą „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūravimas**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
3. Nustatykite parinktį **Įgalinti „Microsoft Teams” integravimą** į **Ne**.
4. Išvalykite laukų **Programos ID** ir **Programos raktas** reikšmes.
1. Veiksmų srityje pasirinkite **Įrašyti**.

> [!NOTE]
> Išjungus „Teams” integravimą su „Commerce”, EKA terminalai neberodys užduočių, publikuotų iš „Teams” programos.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga](commerce-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA](synchronize-tasks-teams-pos.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)