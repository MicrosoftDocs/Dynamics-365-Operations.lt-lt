---
title: Šalies / regiono išrinkiklio modulis
description: Ši tema paaiškina siuntimo šalies/regiono parinkėjo modulį ir aprašo, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551675"
---
# <a name="countryregion-picker-module"></a>Šalies / regiono išrinkiklio modulis

[!include [banner](includes/banner.md)]

Ši tema paaiškina siuntimo šalies/regiono parinkėjo modulį ir aprašo, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.

Šalies / regiono [...](geo-detection-redirection.md)Dynamics 365 Commerce išrinkiklio modulis naudoja geografinio aptikimo ir nukreipimo funkciją, kad rodytų rekomenduojamas svetaines klientams, kurie prašo el. komercijos svetainės URL, kuris nėra susietas su jų šalimi ar regionu.

Pavyzdžiui, kanados klientas prašo svetainės URL, kuris susietas su kita nei Kanada. Šiuo atveju šalies / regiono išrinkiklio modulyje rodomas dialogo langas, kuriame rekomenduojama su Kanada susieti svetainės URL. 

## <a name="how-it-works"></a>Kaip tai veikia

Kai įgalintas svetainės geografinis aptikimas ir nukreipimas, o klientas paprašo svetainės URL, aptikta kliento šalis ir URL, kurių prašo, naudojami siekiant nustatyti, ar URL yra susietas su šalimi, kurioje yra klientas. URL ir šalių susiejimas apibrėžtas " **Commerce" svetainės generatoriaus** **svetainės parametrų** puslapyje Kanalai. 

Jei užklausos URL nesutampa su bet kokiu URL, susietu su kliento šalimi, vieno ar daugiau URL, kurie susieti su ta šalimi, sąrašas grąžinamas atsakant. Šalies / regiono parinkiklis palygina kiekvieną to sąrašo URL su URL, kurie buvo sukonfigūruoti šalies / regiono modulyje. Kiekvieno tikslaus sugretinto atitikmens atveju, šalies / regiono parinkiklis atvaizduos to URL ekrano antraštę, paantraštes ir paveikslėlį, o hipersaitus – naudodamas URL.

Klientui pasirinkus pasirinktį šalies/regiono parinkiklis, jie nukreipiami į hipersaitu nukreipiamas URL. Kad URL būtų naudojamas kaip **\_ kliento svetainės nuostata, jis būtų naudojamas mslit365site\_\_\_\_** cookies. Tada, kitą kartą, kai klientas pageidauja URL, kuris nėra susietas su jų šalimi ar regionu, jis automatiškai peradresuojamas į pageidaujamą šalį. Todėl rekomenduojame ir [savo](site-selector.md) el. komercijos svetainėje naudoti svetainių išrinkiklio modulį, kad klientai galėtų nepaisyti arba atnaujinti savo svetainės nuostatą. 

Jei klientas uždaro šalies/regiono išrinkiklio dialogo langą, neįrašomas joks dk ir klientas lieka dabartinėje teritorijoje. 

Šiame paveikslėlyje rodomas dialogo lango šalies/regiono parinkėjo užduotis pavyzdys.

![Šalies / regiono išrinkiklio dialogo lango pavyzdys pagrindiniame puslapyje.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Šalies / regiono išrinkiklio modulio ypatybės

| Ypatybės pavadinimas              | Reikšmė       | Aprašas                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Antraštė                    | Tekstas        | Antraštė, rodoma dialogo lango viršuje.       |
| Subantraštė                 | Tekstas        | Paantraštė, rodoma po antrašte.               |
| Šalis: rodoma eilutė    | Tekstas        | Rodomas URL pasirinkties pavadinimas (pvz., „Kanada").   |
| Šalis: rodoma papildoma eilutė | Tekstas        | Pasirenkama URL pasirinkties rodymo antrinė funkcija (pvz., „Anglų" arba „Prancūzų"). |
| Šalis: šalies vaizdas     | Medijų turtas | Pasirenkamas vaizdas, susietas su URL pasirinktimi (pavyzdžiui, Kanados vėliavėlės vaizdas). |
| Šalis: šalies URL       | Tekstas        | Konfigūruojamos šalies / regiono svetainės URL. Šis URL turi tiksliai atitikti URL, kurį nurodėte šiai šaliai / regionui **"Commerce" svetainės** generatoriaus **svetainės parametrų** puslapyje Kanalai. Be to, URL **·** **domenas** turi būti pasirinktinis domenas, nurodytas skirtuko Kanalai lauke Suderinti domeną, o ne svetainės, kurią "Commerce" pateikia kurdami savo el. komercijos aplinką, darbo adresas (pvz., URL).`https://<yourcompany>.commerce.dynamics.com/` |
| Veiksmo saitas                | Veiksmo saitas | Pasirinktinis saitas, rodomas dialogo lango apačioje. Pavyzdžiui, šis saitas gali nurodyti vidinį puslapį, kuriame pateikiamas visų šios svetainės palaikomų šalių ir regionų sąrašas. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Įtraukti šalies / regiono parinkimo modulį į puslapį

Šalies / regiono išrinkiklio modulį galima pridėti prie antraštės modulio tiesiogiai arba naudojant bendrą fragmentą. Daugiau informacijos apie antraščių fragmentus ir modulius žr. [Antraštės modulis](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigūruoti šalies / regiono išrinkiklio modulį „Commerce" svetainės generatoriuje

> [!NOTE]
> URL, kuriuos rekomenduojate savo klientams, turi būti sukonfigūruoti kaip šalies objektai šalies / regiono parinkiklio modulyje.

Kiekvienos svetainės URL, kurį norite rodyti ir rekomenduoti klientams, "Commerce" svetainių generatoriuje atlikite šiuos veiksmus.

1. Rinktis šalies / regiono parinkiklio modulio vietą.
1. Ypatybės srities dalyje **Šalių sąrašas** pasirinkite **Įtraukti šalį**.
1. Pasirinkite naują **šalies** langelį.
1. Rodymo **eilutės lauke** įveskite rodomą pavadinimą (pvz., **Kanada**).
1. Pasirinktinai: lauke **Rodyti papildomą eilutės** laukelį, įveskite rodymo papildomą eiltuę (pavyzdžiui, **prancūzų** ar **fr-ca**).
1. Pasirinktinai: pasirinkite vaizdą iš laikmenų bibliotekos.
1. Lauke **Šalies URL** įveskite URL. Šis URL turi tiksliai atitikti **URL**, kuris rodomas kanalų puslapyje ir susietas su kanalu, įskaitant su šalimi arba regionu susietą vietą. 
1. Pasirinkite **Gerai**.
1. Pakartokite šiuos veiksmus visų kitų šalių URL, kuriuos norite, kad rodytų šalies / regiono parinkiklio modulis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Geografinės srities aptikimo ir peradresavimo nustatymas](geo-detection-redirection.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md)

[Svetainės išrinkiklio modulis](site-selector.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
