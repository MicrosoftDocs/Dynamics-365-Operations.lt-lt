---
title: "\"Commerce\" katalogų išorinis poveikis B2B tinkinimais"
description: Šioje temoje aprašomas prekybos katalogų poveikis B2B funkcijai Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: aff333bfe8003233dd5d8181aa8c5dd7eaeffcd0
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2022
ms.locfileid: "8657199"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>"Commerce" katalogų išorinis poveikis B2B tinkinimais

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašomas prekybos katalogų **poveikis B2B funkcijai** Microsoft Dynamics 365 Commerce.

Jei norite išplėsti katalogo kontekstą iki pasirinktinių scenarijų, gali tekti atnaujinti savo pritaikymus. Šis naujinimas atliekamas pagal standartinį procesą, kurį turi atlikti klientai, nes jų tinkinimai gali automatiškai nepaveikti naujausių funkcijų atlikus atnaujinimus. Jei jūsų pritaikymai apima visas naujas savo patirties funkcijas ar klaidų pataisymus, rekomenduojame pagal tai atnaujinti pritaikymo kodą. Šis naujinimas panašus į keitimus, kuriuos "Microsoft" galėjo atlikti su pagrindiniu kodu.

Norėdami nustatyti, ar jūsų pritaikymai turi būti atnaujinti, peržiūrėkite pritaikymo atvejus.

> [!NOTE]
> - Visos prekybos programų programavimo sąsajos (API) turėtų būti atsiejamos nuo katalogo. Todėl labai svarbu, kad išlaikyti CatalogID **parametrą**.
> - Numatytasis katalogas (**CatalogID0**=**·**) nėra tinkamas katalogas, skirtas prisiregistravę verslo (B2B) vartotojams. Todėl visi API iškvietimai, kurie pereina "0" arba naudoja numatytąją vertę, nepavyks, nes svetainės vartotojai neturi prieigos prie katalogo 0. Norint gauti teisingą patirtį, kliento API iškvietimai turi būti atnaujinti, kad jie būtų perduoti katalogo parinkiklio pasirinkto katalogo ID. Jei naudojate numatytąją vertę, o vartotojas perjungia katalogus, svetainė turi pateikti pasirinkto katalogo duomenis. Todėl norint suderinti API, kurie paleisti iš pagrindinio "Commerce" kodo, pritaikyti API turi atitikti pasirinktą katalogą.

Šiuos pritaikymo atvejus reikia atnaujinti:

- **1 atvejis:** klientas pristato savo duomenų veiksmą [, kuris](e-commerce-extensibility/data-actions.md) iškmes su produktu susijusią API arba duomenų veiksmą. Būtini šie atnaujinimo veiksmai:

    1. Jei duomenų veiksmas naudoja tiesioginį API iškvietimą, atnaujinkite duomenų veiksmą taip, kad jis išlaiko katalogo ID, kaip parodyta toliau pateiktame pavyzdyje.

        ![Atnaujintas duomenų veiksmas, kuris išlaiko katalogo ID.](./media/customization1_a.png)

    1. Jei duomenų veiksmas išk taigi kitas su produktu susijęs duomenų veiksmas tinkinimo viduje, kodas turi būti atnaujintas taip, kad jis pereina prie kai kurių naujų parametrų, pvz **., requestContext**. Parametras **requestContext** naudojamas dabartinio katalogo ID nuskaityti, kaip parodyta pateiktoje pavyzdyje.

        ![Atnaujintas duomenų veiksmas, kuris išlaiko naują parametrą.](./media/customization1_b.png)

- **2 atvejis:** klientas turi nepaisomas [duomenų veiksmą](e-commerce-extensibility/data-action-overrides.md). Būtinas šis atnaujinimo veiksmas:

    - Atnaujinkite duomenų veiksmą 1 atvejui.

- **3 atvejis:** klientas turi rodinio plėtinį, scenarijaus dėsčių modulį arba išplėstą modulį, [į](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) kurį įeina API arba duomenų veiksmų kvietimai. Būtinas šis atnaujinimo veiksmas:

    - Atnaujinkite 1 atvejo kodą, kaip parodyta toliau pateiktame pavyzdyje.

       ![Atnaujintas kodas, kuris pereina naują parametrą.](./media/customization3.png)

- **4 atvejis:** klientas naudoja **getById API iškvietimą**. Būtinas šis atnaujinimo veiksmas:

    - Pereikite prie **api iškvietimo getByIds**, nes **iškvietime getById** YRA keletas apribojimų ir nepalaiko katalogo supratimo.

- **5 atvejis:** klientas turi duomenų veiksmą, kuris nuskaito informaciją apie kelis produktus, kurie gali būti iš skirtingų katalogų. Būtinas šis atnaujinimo veiksmas:

    - Skaidyti API iškvietimus pagal katalogo ID. Pavyzdžiui, krepšelio API krepšelyje gali būti produktų iš skirtingų katalogų. Produktų eilutės turi būti sugrupuotos pagal katalogo ID, o kiekvieno katalogo API turėtų būti iškviestos atskirai, kaip parodyta toliau pateiktame pavyzdyje.

        ![Atnaujintas duomenų veiksmas, pagal kurį produktų eilutės sus grupės pagal katalogo ID.](./media/customization5.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kurti B2B svetainių "Commerce" katalogus](catalogs-b2b-sites.md)

[DUK B2B komercijos katalogai](catalogs-b2b-sites-FAQ.md)
