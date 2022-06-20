---
title: „ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas
description: Šiame straipsnyje aprašoma, kaip įgalinti ir Microsoft Dynamics 365 Commerce Microsoft Teams integruoti.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 505e3854818e4d5b73fc1a22724be16036300c3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872833"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>„ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įgalinti ir Microsoft Dynamics 365 Commerce Microsoft Teams integruoti.

Norėdami sukonfigūruoti „Teams” su informacija iš „Dynamics 365 Commerce” ir sinchronizuoti užduočių valdymo funkcijas tarp „Teams” ir elektroninio kasos aparato (EKA) programos, turite įgalinti integravimo funkcijas „Commerce” būstinėje.

> [!NOTE]
> Kai įgalinate „Teams” integravimą, sutinkate su „Teams” bendrinti savo duomenis. Su „Teams” bendrinami duomenys gali priklausyti kitai šaliai nei jūsų „Commerce” duomenys ir jiems gali būti taikomi skirtingi atitikties standartai. Daugiau informacijos rasite [„Microsoft” patikimumo centras](https://www.microsoft.com/trust-center). Daugiau informacijos apie „Microsoft” privatumo politikas rasite [„Microsoft” privatumo nuostatos](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>„Teams” integravimo įgalinimas

Prieš įgalindami „Microsoft Teams” integravimą su „Commerce”, turite užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.

Norėdami užregistruoti „Teams” programą savo nuomotojui „Azure” portale, atlikite šiuos veiksmus.

1. Atlikite skyriuje [Greitas pasirengimas darbui: Registruoti programą „Microsoft” tapatybės platformoje](/azure/active-directory/develop/quickstart-register-app) pateiktus veiksmus, norėdami užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.
1. Skirtuke **Programos registracija** pasirinkite programą, kurią sukūrėte ankstesniu veiksmu. Tada skirtuke Autentifikavimas **pasirinkite** Įtraukti **platformą**.
1. Dialogo lange pasirinkite **Internetas**. Tada į nukreipimo **URL** lauką įveskite URL formatu / **\<HQUrl\> autorizavimo būdu**. Pakeiskite **\<HQUrl\>** "Commerce Headquarters" URL (pvz., `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Užregistruotos **programos** peržiūros puslapyje nukopijuokite programos **(kliento) ID vertę**. Turite pateikti šią vertę, kad kitame skyriuje būtų galima įgalinti "Teams" integravimą "Commerce Headquarters".
1. Norėdami pridėti kliento slaptą [kliento slaptą, vadovaukitės](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) instrukcijomis, pateikiamomis prie kliento slapto. Tada nukopijuokite **kliento Slaptą** vertę. Turite pateikti šią vertę, kad kitame skyriuje būtų galima įgalinti "Teams" integravimą "Commerce Headquarters".
1. Pasirinkite **API teises**, tada pasirinkite **Įtraukti teisę**.
1. **Užklausos API teisių dialogo** lange pasirinkite "Microsoft Graph **",** **pasirinkite** Perduotas teises, **išplėskite** Grupė, pasirinkite **Group.ReadWrite.Visi**, tada pasirinkite **Įtraukti teises.**
1. Užklausos API teisių dialogo lange pasirinkite Įtraukti teisę, **pasirinkite** "Microsoft Graph **",** pasirinkite Programos teisės, **·** **išplėskite** Grupė, pasirinkite **Group.ReadWrite.All**, tada pasirinkite **Įtraukti teises.** **·**
1. **Užklausos API teisių dialogo** lange pasirinkite **Įtraukti teisę**. Skirtuke **APIs mano organizacija naudoja**, ieškokite " **Microsoft Teams Retail Service"** ir pasirinkite jį.
1. Pasirinkite **perduotas teises**, išplėskite **TaskPublishing**, pasirinkite **TaskPublising.ReadWrite.Visi**, tada pasirinkite **Įtraukti teises**. Norėdami gauti daugiau informacijos, žr. [Kliento programos konfigūravimas, kad būtų galima pasiekti žiniatinklio API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Norėdami įgalinti „Teams” integravimą „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūracija**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Nustatykite parinktį **Įgalinti „Microsoft Teams” integravimą** į **Taip**.
1. **Programos ID lauke įveskite** programos (kliento **) ID** vertę, kurią gavote registravę programą "Teams" "Azure" portale.
1. Programos rakto **lauke įveskite** slaptą **vertę**, kurią gavote į "Azure" portalą įdę kliento slaptažodį.
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
