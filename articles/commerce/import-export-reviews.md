---
title: Įvertinimų ir atsiliepimų importavimas ir eksportavimas
description: Šiame straipsnyje aprašoma, kaip importuoti ir eksportuoti produktų įvertinimus ir apžvalgas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271941"
---
# <a name="import-and-export-ratings-and-reviews"></a>Įvertinimų ir atsiliepimų importavimas ir eksportavimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip importuoti ir eksportuoti produktų įvertinimus ir apžvalgas Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce siūlo [vertinimus ir peržiūros](ratings-reviews-overview.md) kaip kanalų sprendimą. Pereidami Dynamics 365 Commerce prie įvertinimų ir peržiūros sprendimų, galbūt norėsite perkelti savo esamus įvertinimus ir peržiūros duomenis į komercijos platformą. Taip pat galite norėti eksportuoti įvertinimus ir peržiūrėti duomenis iš "Commerce", atsižvelgdami į verslo poreikius. Jungtis Power Automate leidžia importuoti įvertinimus ir apžvalgas į Commerce ir eksportuoti juos iš Komercijos.

> [!NOTE]
> Informacijos, kaip pradėti naudojant logikos srautus, ieškokite Power Automate daugiau informacijos apie [debesies srautą Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš importuodami ir eksportuodami įvertinimus ir peržiūrint, turite įvykdyti šiuos būtinuosius komponentus:

- Turi būti įgalinti jūsų el. komercijos svetainės vertinimai ir peržiūros sprendimas "Commerce platform". Norėdami gauti daugiau informacijos, peržiūrėkite ["Opt", norėdami naudoti vertinimus ir apžvalgas](opt-in-ratings-reviews.md).
- "Dynamics 365" įvertinimai ir peržiūros "Power App Connector" turi būti sukonfigūruoti, kad įgalintumėte "pateikti apžvalgas" arba "eksporto peržiūros" veiksmus.Power Automate Daugiau informacijos rasite - [Dynamics 365 Commerce vertinimai ir peržiūros (peržiūra)](/connectors/dynamics365ratingsre/).
- Norint saugiai iškviesti įvertinimus ir peržiūrėti ne komercijos programų programavimo sąsają (API), turi būti sukonfigūruotas "Service-to Service" (S2S) autentifikavimas. Daugiau informacijos rasite Konfigūravimas [paslaugai-paslaugai autentifikavimas](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Importuoti įvertinimus ir apžvalgas

Norėdami importuoti įvertinimus ir peržiūrėti duomenis iš jūsų esamos sistemos į Komercijos, turite įtraukti "Dynamics 365" vertinimus Power Automate Power Automate ir peržiūros jungtį į esamą srautą arba naują. Daugiau informacijos rasite - [Dynamics 365 Commerce vertinimai ir peržiūros (peržiūra)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Prieš procedūros pabaigą turite sukonfigūruoti [S2S autentifikavimą](service-to-service-auth.md).

Norėdami importuoti vertinimus ir peržiūrimi į Komercijos naudojant jungtį "Dynamics 365" vertinimas ir Power Automate apžvalgos, atlikite šiuos veiksmus.

1. Pasirinkite veiksmą **Pateikti vartotojo** peržiūrą.
1. Užmezkite ryšį naudodami Azure Active Directory (Azure AD) programos informaciją, kuri buvo sukurta konfigūruotame S2S autentifikavime. Daugiau informacijos rasite Konfigūravimas [paslaugai-paslaugai autentifikavimas](service-to-service-auth.md).
1. Veiksmas **Pateikti vartotojo peržiūrą** vienu metu yra peržiūrias vieną kartą. Todėl pakartokite veiksmą. Norėdami pateikti masinius peržiūrimų prekių peržiūros duomenis, naudokite šaltinio peržiūros sąrašą.
    
## <a name="export-ratings-and-reviews"></a>Eksporto vertinimai ir peržiūros

Norėdami eksportuoti vertinimus ir peržiūrų duomenis iš "Commerce", turite įtraukti "Dynamics 365 Power Automate Power Automate " įvertinimą ir peržiūros jungtį į esamą srautą arba naują. Daugiau informacijos rasite - [Dynamics 365 Commerce vertinimai ir peržiūros (peržiūra)](/connectors/dynamics365ratingsre/).

Norėdami eksportuoti "Commerce" vertinimus ir apžvalgas naudojant jungtį "Dynamics 365" vertinimas ir Power Automate apžvalgos, atlikite šiuos veiksmus.

1. Pasirinkite veiksmą **Eksportuoti visas peržiūros** priemones.
1. Baigti veiksmą. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas](sync-product-ratings.md)

[Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas](manual-publish-rating-reviews.md)

[Ryšių tarp tarnybų autentifikavimo konfigūravimas](service-to-service-auth.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md)
