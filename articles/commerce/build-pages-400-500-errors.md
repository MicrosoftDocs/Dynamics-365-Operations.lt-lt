---
title: Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius
description: Šiame straipsnyje aprašoma, kaip kurti pasirinktinius 4xx ir 5xx būsenos kodų klaidų atsakymo puslapius naudojant kūrimo įrankius,tus meniu Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276406"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kurti pasirinktinius 4xx ir 5xx būsenos kodų klaidų atsakymo puslapius naudojant kūrimo įrankius,tus meniu Microsoft Dynamics 365 Commerce.

Jei užklausa nėra sėkminga, serveris pateikia HTTP būsenos kodo klaidų atsakus. Būsenos kodas 404 užfiksuojamas ir pateikiamas neradus puslapio, o būsenos kodas 500 – įvykus serverio klaidai. Programos „Dynamics 365 Commerce“ vartotojai gali kurti pasirinktinius būsenos kodo klaidų atsako puslapių, kurie rodomi vartotojams dėl tokių būsenos kodo klaidų atsako.

## <a name="build-a-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio kūrimas

Norėdami pradėti kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.

1. Savo pageidaujamoje žiniatinklio naršyklėje prisijunkite prie „Dynamics 365 Commerce“. 
1. Pasirinkite svetainę, kuriai norite sukurti 4xx / 5xx būsenos kodo klaidų atsako puslapį.

### <a name="build-the-template"></a>Šablono kūrimas

Norėdami sukurti būsenos kodo klaidų atsako puslapio šabloną, atlikite tolesnius veiksmus.

1. Eikite į parinktį **Šablonai**.
1. Pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite naujo šablono pavadinimą ir pasirinkite **Gerai**.
1. Sukurkite šabloną su norima būsenos kodo klaidų atsako puslapio struktūra.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 

### <a name="build-the-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio kūrimas

Norėdami kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.

1. Eiti į **Puslapiai**.
1. Pasirinkite **Naujas**, kad sukurtumėte puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite šabloną, tada dalyje **Puslapio pavadinimas** įveskite būsenos kodo klaidų atsako puslapio pavadinimą. Lauką **Puslapio URL** palikite tuščią.
1. Sukurkite puslapį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

> [!NOTE]
> Galite sukurti atskirus būsenos kodo klaidų atsako puslapius, skirtus 4xx ir 5xx būsenos kodo klaidoms. Taip pat galite naudoti tą patį bendrą būsenos kodo klaidų atsako puslapį abiem klaidų kategorijoms.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio peradresavimo nustatymas

Norėdami nustatyti būsenos kodo klaidų atsako puslapio peradresavimą, atlikite tolesnius veiksmus.

1. Nueikite į **URL \> Naujas \> Naujas pseudonimas** ir pasirinkite anksčiau sukurtą būsenos kodo klaidų atsako puslapį.
1. Lauke **Pseudonimas** įveskite **numatytasis-4xx** arba **numatytasis-5xx**, atsižvelgdami į būsenos kodo klaidų atsako puslapį, kurio peradresavimą nustatote. Šiuos pseudonimus reikia publikuoti. Kitu atveju peradresavimas neveiks.
1. Pasirinkite **Gerai**, kad patvirtintumėte susiejimą.

> [!NOTE]
> Jei abiem klaidų kategorijoms naudojate vieną būsenos kodo klaidų atsako puslapį, pakartokite šią procedūrą, kad kitos klaidų kategorijos pseudonimą susietumėte su tuo pačiu puslapiu.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbas su šablonais](work-with-templates.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Kurti puslapio URL](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
