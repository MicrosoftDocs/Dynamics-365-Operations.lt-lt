---
title: Ryšių tarp tarnybų autentifikavimo konfigūravimas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti paslaugos teikimo autentifikavimą, Microsoft Dynamics 365 Commerce kad būtų galima saugiai iškviesti vertinimo ir peržiūros paslaugų API.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3134d4ddb2e4f3d260e51d49e7399ff84e0d74a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279454"
---
# <a name="configure-service-to-service-authentication"></a>Ryšių tarp tarnybų autentifikavimo konfigūravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukonfigūruoti paslaugų tarnybos (S2S) Microsoft Dynamics 365 Commerce autentifikavimą siekiant saugiai iškviesti paslaugų programos programavimo sąsajas (API) dėl įvertinimų ir apžvalgos.

Dynamics 365 Commerce siūlo [vertinimus ir peržiūros](ratings-reviews-overview.md) kaip kanalų sprendimą. Šis sprendimas leidžia pasiekti paslaugų API ne iš "Commerce", kad būtų galima atlikti įvairias užduotis. Šios užduotys apima įvertinimų ir peržiūros importavimą iš jūsų išorinės sistemos į Komercijos ir vertinimų eksportavimą iš Komercijos. Kad "Commerce" galėtų saugiai iškviesti įvertinimus ir peržiūrėti paslaugų API, pirmiausia, atlikdami šiame straipsnyje nurodytas procedūras, turite sukonfigūruoti S2S autentifikavimą.

## <a name="add-a-new-app-registration"></a>Įtraukti naują programos registraciją

Prieš įtraukdami naują programos registraciją, turite sukurti programą naudodami "Azure" [portalą](https://portal.azure.com). Norėdami užregistruoti programą () ir Azure Active Directory Azure AD įgalinti autentifikavimą, atlikite veiksmus, kuriuos [atlikite naudodami Azure Active Directory pasirinktinę jungtį dalyje Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Rinkti šiuos YS iš "Azure" portalo. Atlikite šiuos veiksmus, kad jums reikės šių JAV duomenų.

- Kliento taikomosios programos ID
- Klientų katalogo (nuomininko) ID

Norėdami įtraukti naują programos registraciją į "Commerce" svetainės generatorių, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \>Apžvalgos \> Sąranka**.
1. Dalyje **Paslaugos paslauga (S2S) autentifikavimas** pasirinkite **Valdyti**.

    !["Commerce" svetainių generatoriaus skyriuje "Paslauga paslauga (S2S) autentifikavimas" valdyti mygtuką.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Dešinėje pusėje **esančioje S2S** programų įrašų srityje pasirinkite **Įtraukti naują S2S programos registraciją**.
1. Dialogo lange **Įtraukti S2S programos** įrašą įveskite toliau nurodytą reikiamą informaciją. Naudokite vertes iš "Azure" programos registracijos.

    - **Pavadinimas** – įveskite savo programos pavadinimą (pvz., **Fabrikam App**).
    - **Kliento programos ID** – įveskite programos ID (pvz. **00000000-0000-0000-0000-000000000000**).
    - **Katalogo (nuomininko) ID** – įveskite katalogo ID (pvz.). **00000000-0000-0000-0000-000000000000**

    ![Įtraukti S2S programos įrašo dialogo langą "Commerce" svetainės generatoriuje.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Pasirinkite **Pateikti**. Jūsų programos pavadinimas turėtų būti rodomas **S2S programos įrašų srities** sąraše.
1. Uždarykite **S2S programos įrašų** sritį.
1. Pasirinkite **Įrašyti**.

## <a name="edit-an-existing-app-registration"></a>Esamos programos registracijos redagavimas

Norėdami redaguoti esamą programos registraciją "Commerce" svetainės generatoriuje, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \>Apžvalgos \> Sąranka**.
1. Dalyje **Paslaugos paslauga (S2S) autentifikavimas** pasirinkite **Valdyti**.
1. **Srityje S2S programų** įrašai pasirinkite simbolią, esantį šalia norimo redaguoti įrašo.
1. Jei reikia, atnaujinkite **vertes** **laukuose Pavadinimas, Kliento programos** ID **ir Katalogo (nuomininkų) ID**.
1. Pasirinkite **Pateikti**.
1. Uždarykite **S2S programos įrašų** sritį.
1. Pasirinkite **Įrašyti**.

## <a name="remove-an-existing-app-registration"></a>Esamos programos registracijos pašalinimas

Norėdami pašalinti esamą programos registraciją "Commerce" svetainių generatoriuje, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis \>Apžvalgos \> Sąranka**.
1. Dalyje **Paslaugos paslauga (S2S) autentifikavimas** pasirinkite **Valdyti**.
1. **Srityje S2S programų** įrašai pasirinkite simbolią, esantį šalia įrašo, kurį norite pašalinti. Įrašas pašalinamas iš sąrašo.
1. Uždarykite **S2S programos įrašų** sritį.
1. Pasirinkite **Įrašyti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas](sync-product-ratings.md)

[Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas](manual-publish-rating-reviews.md)

[Įvertinimų ir atsiliepimų importavimas ir eksportavimas](import-export-reviews.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md) 
