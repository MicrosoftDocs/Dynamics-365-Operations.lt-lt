---
title: Įdiegti SF fiksavimo sprendimą
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įdiegti SF fiksavimo sprendimą ir integruoti jį su Microsoft Dynamics "365 Finance".
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691008"
---
# <a name="install-the-invoice-capture-solution"></a>Įdiegti SF fiksavimo sprendimą

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Jei sprendimas įdiegtas privačioje peržiūroje, prieš tęsdami turite pašalinti seną sprendimą.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš diegdami SF fiksavimo sprendimą turite užbaigti šiuos būtinuosius komponentus:

1. Užregistruokite programą ir pridėkite kliento slaptažodį "Microsoft Azure Active Directory " (Azure AD) naudodami "Azure" abonementą. Daugiau informacijos ieškokite Registruoti [interneto programą naudojant AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Pasižymykite programos **(kliento) ID**, **kliento slapto** ir **nuomininko ID** vertes, nes jų reikės vėliau.

2. Užregistruokite "Azure" programą "Dynamics 365" finansų aplinkoje. Norėdami gauti daugiau informacijos, užregistruokite [savo išorinę programą](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Įdiegti ir nustatyti sprendimą

Norėdami įdiegti SF fiksavimo sprendimą, AppSource eikite į ir [pasirinkite "Dynamics 365" SF fiksavimo peržiūros versijos saitą](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Užbaigę diegimą, matysite sprendimą, įdiegtą pasirinktoje aplinkoje Power Apps.

Norėdami užbaigti nustatymą, atlikite šiuos veiksmus.

1. Atsisiųskite [asistento](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) sprendimą, kad būtų nustatyta ši informacija:

    - Finansų aplinkos Microsoft Power Platform ryšys
    - Ryšio nuoroda, skirta ir Dataverse Office 365 "Outlook", kurią naudoja kanalas

2. Įeikite Power Apps į aplinką ir pasirinkite Importuoti **sprendimą**.
3. Pasirinkite **Naršyti**, pasirinkite atsisiųstą asistento sprendimo paketą, tada pasirinkite **Pirmyn**.
4. Pasirinkite **Toliau**.
5. Priskirkite esamą ryšį arba sukurkite naują, pasirinkdami **Naujas ryšys**.
6. Po to, kai paketas sėkmingai importuotas, atidarykite " **Dynamics 365" SF fiksavimas – diegimo įrankiai**.
7. Paleiskite debesies srautą, kad būtų nustatytas ryšys tarp SF fiksavimo sprendimo ir Microsoft Power Platform finansų.
8. Pasirinkite **Vykdyti** ir nurodykite šiuos parametrus:

    - **"Dynamics 365** " finansų URL – finansinės aplinkos, su kurią norite integruoti, URL.
    - **Nuomininko ID – finansinės aplinkos nuomininko ID**.
    - **Kliento ID** – užregistruotas "Azure" programos ID.
    - **Kliento slapyme** – kliento slapyme, sugeneruotas "Azure" programai.
