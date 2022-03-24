---
title: Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas
description: Šioje temoje aprašoma, kaip įgalinti rankinį įvertinimų ir peržiūros paskelbimą režimo vadovo ir kaip rankiniu būdu skelbti „Microsoft Dynamics 365 Commerce“ įvertinimus ir įvertinimus.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2b4ba835ff4540b63f6fe49cc847286f8c2a3bcf
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407824"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įgalinti rankinį įvertinimų ir peržiūros paskelbimą režimo vadovo ir kaip rankiniu būdu skelbti „Microsoft Dynamics 365 Commerce“ įvertinimus ir įvertinimus.

„Dynamics 365 Commerce“ pagal vertinimą ir peržiūrimas sprendimas naudoja „Azure Cognitive Services" virtualiosios paslaugos automatiškai persvarsto peržiūros pavadinimus ir turinį bei skelbia vertinimus ir peržiūras. Todėl neautomatinis veiksmai nėra būtini norint peržiūrėti ir paskelbti įvertinimus ir peržiūras jūsų el. komercijos svetainėje.

Tačiau kai kurios įmonės gali pasirinkti, kad moderatoriai peržiūrėtų ir patvirtintų peržiūras prieš jas publikuodami. Jei norite įgalinti automatinį įvertinimų ir peržiūros skelbimą režimo vadovo, turite įgalinti „Commerce" svetainių generatoriaus priemonę **Reikalauti moderatoriaus, kad ji galėtų naudoti vertinimo** peržiūros funkciją.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Įjungti reikalauti moderatoriaus įvertinimų ir peržiūros funkciją „Commerce" svetainės generatoriuje

Norėdami įjungti **reikalauti moderatoriaus įvertinimų ir peržiūros** funkciją „Commerce“ svetainės generatoriuje, imkitės tokių veiksmų.

1. Eikite į **Pagrindinis \>Apžvalgos \> Sąranka**.
1. Nustatykite **įvertinimų ir peržiūros parinkties Reikalauti moderatoriaus** parinktį **Įjungta**.

> [!NOTE]
> Įgalindami **įvertinimų ir peržiūros funkcijų reikalauti moderatorių** sustabdote automatinį įvertinimų ir peržiūrint publikavimą, kad dabar būtų reikalingas neautomatinis publikavimas. Tačiau „Azure Cognitive Services" ir toliau iš naujo tęs peržiūrą pagal pavadinimus ir turinį.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Publikavimo ir apžvalgų reitingai

Jei norite įgalinti **Reikalauti moderatoriaus reitingams ir peržiūroms** funkciją, moderatoriui reikia rankiniu būdu peržiūrėti ir publikuoti reitingus bei peržiūrėti siekiant juos parodyti jūsų el. komercijos saite.

Norėdami peržiūrėti ir publikuoti įvertinimų ir atsiliepimų tendencijas „Commerce“ svetainių daryklėje, atlikite šiuos veiksmus.

1. Eikite į **Apžvalgos \> Moderavimas**.
1. Tinklelyje, jei eilutės laukas **Būsena** nustatytas kaip **Nepaskelbtas**, tos eilutės vertinimas ir peržiūra dar nepublikuoti. Norėdami peržiūrėti tik nepaskelbtas įvertinimus ir peržiūras, pasirinkite **Būsena: reikia peržiūrėti** būsenos filtrą virš tinklelio.
1. Pasirinkite vieną ar daugiau įvertinimų ir peržiūros, kurių būsena yra **Nepaskelbta**, ir tada rinkitės **Publikuoti** komandų juostoje. Pasirinkti įvertinimai ir peržiūros įtraukiami į publikavimo eilę ir bus rodomi el. komercijos svetainėje po to, kai jie bus publikuoti.

> [!NOTE]
> - Kai įvertinimas ir peržiūra paskelbiami, būsenos reikšmė pasikeičia iš nepaskelbta į nulinę **vertę** (tuščias laukas).
> - Jei pasirenkate kelis įvertinimus ir peržiūros, kurių būsenos yra mišrios, tada pasirenkate Skelbti, vertinimai ir peržiūros, kurios dar nebuvo **publikuojamos**, bus publikuojamos. Tačiau jau publikuotų įvertinimų ir peržiūros nebus publikuojami dar kartą.

Šiame pavyzdyje pateikiamas pavyzdys, kuriame yra pasirinkti trys nepaskelbtai įvertinimai ir peržiūros Komercijos svetainės generatoriaus puslapyje **Moderavimas**.

![„Commerce" svetainės generatoriaus puslapyje moderavimas pasirinkti trys nepaskelbtai įvertinimai ir peržiūros.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas](sync-product-ratings.md)

[Įvertinimų ir atsiliepimų importavimas ir eksportavimas](import-export-reviews.md)

[Ryšių tarp tarnybų autentifikavimo konfigūravimas](service-to-service-auth.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md)
