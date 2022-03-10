---
title: Šalies / regiono išrinkiklio modulis
description: Ši tema paaiškina siuntimo šalies/regiono parinkėjo modulį ir aprašo, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 1a8eebb589372051272573895a0ae5b4203eef62
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109786"
---
# <a name="countryregion-picker-module"></a>Šalies / regiono išrinkiklio modulis

[!include [banner](includes/banner.md)]

Ši tema paaiškina siuntimo šalies/regiono parinkėjo modulį ir aprašo, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

Šalies / regiono išrinkiklio modulis naudoja [geografinio aptikimo ir nukreipimo](geo-detection-redirection.md) funkciją „Dynamics 365 Commerce“ tam, kad parodytų rekomenduojamus URL klientams, kurie prašo el. komercijos svetainės URL, kuris nėra susietas su jų šalimi ar regionu.

Pavyzdžiui, Kanados klientas prašo svetainės URL, kuris nėra susietas su Kanada. Šiuo atveju šalies / regiono išrinkiklio modulyje rodomas dialogo langas, kuriame rekomenduojama su Kanada susieti svetainės URL. Šiame paveikslėlyje rodomas dialogo lango šalies/regiono parinkėjo užduotis pavyzdys.

![Šalies / regiono išrinkiklio dialogo lango pavyzdys pagrindiniame puslapyje.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Šalies / regiono išrinkiklio modulio ypatybės

| Ypatybės pavadinimas              | Reikšmė       | Aprašas |
| -------------------------- | ----------- | ----------- |
| Antraštė                    | Tekstas        | Antraštė, rodoma dialogo lango viršuje. |
| Subantraštė                 | Tekstas        | Paantraštė, rodoma po antrašte. |
| Šalis: rodoma eilutė    | Tekstas        | Rodomas URL pasirinkties pavadinimas (pvz., „Kanada"). |
| Šalis: rodoma papildoma eilutė | Tekstas        | Pasirenkama URL pasirinkties rodymo antrinė funkcija (pvz., „Anglų" arba „Prancūzų"). |
| Šalis: šalies vaizdas     | Medijų turtas | Pasirenkamas vaizdas, susietas su URL pasirinktimi (pavyzdžiui, Kanados vėliavėlės vaizdas). |
| Šalis: šalies URL       | Tekstas        | URL, atitinkantis kanalą ir vietą, sukonfigūruotą šaliai arba regionui ar šaliai, kurie konfigūruojami **Kanalų** puslapyje „Commerce“ svetainės kūrimo (**Svetainės nustatymai \> Kanalai**). Šis URL turi tiksliai atitikti URL, kuris sukonfigūruotas **kanalų** puslapyje. |
| Veiksmo saitas                | Veiksmo saitas | Pasirinktinis saitas, rodomas dialogo lango apačioje. Pavyzdžiui, šis saitas gali nurodyti vidinį puslapį, kuriame pateikiamas visų šios svetainės palaikomų šalių ir regionų sąrašas. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Įtraukti šalies / regiono parinkimo modulį į puslapį

Šalies / regiono išrinkiklio modulį galima pridėti prie antraštės modulio tiesiogiai arba naudojant bendrą fragmentą. Daugiau informacijos apie antraščių fragmentus ir modulius žr. [Antraštės modulis](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigūruoti šalies / regiono išrinkiklio modulį „Commerce" svetainės generatoriuje

> [!NOTE]
> URL, kuriuos rekomenduojate savo klientams, turi būti sukonfigūruoti kaip šalies objektai šalies / regiono parinkiklio modulyje.

Kiekvieno URL, kurį norite rodyti ir rekomenduoti klientams, atveju atlikite šiuos „Commerce" svetainių generatoriaus veiksmus.

1. Rinktis šalies / regiono parinkiklio modulio vietą.
1. Ypatybės srities dalyje **Šalių sąrašas** pasirinkite **Įtraukti šalį**.
1. Pasirinkite naują **šalies** langelį.
1. Rodymo **eilutės lauke** įveskite rodomą pavadinimą (pvz., **Kanada**).
1. Pasirinktinai: lauke **Rodyti papildomą eilutės** laukelį, įveskite rodymo papildomą eiltuę (pavyzdžiui, **prancūzų** ar **fr-ca**).
1. Pasirinktinai: pasirinkite vaizdą iš laikmenų bibliotekos.
1. Lauke **Šalies URL** įveskite URL. Šis URL turi tiksliai atitikti URL, kuris rodomas **kanalų** puslapyje ir yra susietas su kanalu, įskaitant su šalimi arba regionu susietą vietą.
1. Pasirinkite **Gerai**.
1. Pakartokite šiuos veiksmus visų kitų šalių URL, kuriuos norite, kad rodytų šalies / regiono parinkiklio modulis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Geografinės srities aptikimo ir peradresavimo nustatymas](geo-detection-redirection.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md)

[Svetainės išrinkiklio modulis](site-selector.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
