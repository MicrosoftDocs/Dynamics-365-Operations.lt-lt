---
title: Eksperimento nustatymas
description: Šiame straipsnyje aprašoma, kaip nustatyti šios trečiosios šalies tarnybos animentavimą.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946171"
---
# <a name="set-up-an-experiment"></a>Eksperimento nustatymas

[Nustatę hipotezę ir sėkmės metriką, kurią norite naudoti](experimentation-identify.md), turite nustatyti jūsų eksperimentą trečiosios šalies paslaugoje. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai įtraukti atskiruose straipsnius.

[ ![Vartotojo eksperimentavimo kelionė – nustatymas.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimento nustatymas trečiosios šalies paslaugoje
Jau turėjote pasirinkti trečiosios šalies paslaugą, kuri vykdys ir stebės jūsų eksperimentą, ir nustatyti eksperimento jungtį. Šios būtinosios sąlygos išvardytos [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).

Atlikite veiksmus, reikalingus eksperimentui sukurti trečiosios šalies paslaugoje. Jei jungtis tinkamai sukonfigūruota, visas eksperimentų, kuriuos nustatysite trečiosios šalies paslaugoje, sąrašas atsiras „Commerce” svetainių daryklėje per maždaug 5 minutes.

## <a name="set-up-your-success-metrics"></a>Jūsų sėkmės metrikos nustatymas
Kiekvienam eksperimentui reikia metrikos, kad būtų galima įvertinti variacijų poveikį ir patvirtinti hipotezę. Atlikite toliau nurodytus veiksmus, norėdami įgalinti metrikos skaičiavimą trečiosios šalies paslaugoje naudojant aktyvius „Dynamics 365 Commerce” telemetrijos įvykius.

Norėdami nustatyti sėkmingą "out-of-the box" modulių metriką, atlikite šiuos veiksmus.

1. „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Puslapiai** ir pasirinkite puslapį, kurio metriką norite rinkti. 
1. Eikite į puslapio ar modulio, kurį norite sekti, dešinėje esančios ypatybių srities sekciją **Įvykių ID, kurie bus sekami**.
1. Pasirinkite **Peržiūrėti**. Visų spusteltų įvykių ID sąrašas. Nukopijuokite įvykį, kurį norite sekti, ir įklijuokite įvykio raktą į trečiosios šalies aptarnavimo nustatytą vietą. Jei reikia daugiau nei vieno įvykio, vienu metu kopijuokite po vieną raktą. 
1. Jei naudojate puslapių rodinius, SHA-256 prie svetainės generatoriaus pridėtas puslapio pavadinimo hash vertė `.PageView`. Pvz., įvykio ID būtų `Homepage.PageView``e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Atlikite kitus reikalingus metrikos sekimo veiksmus trečiosios šalies paslaugoje.

Jei norite naudoti pasirinktinį modulį, spustelėkite šiuos veiksmus, kad būtų galima priemonėje spustelėti įvykius:

1. Paruoškite **telemetryContent** objektą moduliui naudojant toliau pateiktą funkciją. Ši funkcija kaip įvestis perima puslapio pavadinimą, modulio pavadinimą ir SDK pateiktą numatytąjį telemetrinį objektą.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Toliau pateikiamas pavyzdys: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Sukurkite algalapio duomenis, kuriuose yra informacijos apie tai, ką reikia užfiksuoti. Mygtukų ir kitų statinių valdiklių atveju galite įtraukti **etext**, pvz., "Pirkti dabar" arba "Ieškoti". Komponentų su spustelėjimu, pvz., spustelėjus produkto kortelę, galima siųsti įrašo ID, **kuris** yra produkto arba produkto ID įrašo ID.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Kaip statinių valdiklių pavyzdį perduoti mygtuko teksto eilutę, kaip parodyta toliau:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Kaip produkto spustelėjimus, produkto įrašo ID perdavimas, kaip parodyta žemiau:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Iškviesti **OnClick** funkciją įvykiui užregistruoti.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Toliau pateikiamas pavyzdys:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento hipotezės ir metrikos nustatymas](experimentation-identify.md) 


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento prijungimas ir redagavimas](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
