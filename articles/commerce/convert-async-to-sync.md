---
title: Asinchroninių klientų konvertavimas į sinchroninius klientus
description: Šiame straipsnyje paaiškinama, kaip konvertuoti asinchronius klientus į sinchronius klientus Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278198"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asinchroninių klientų konvertavimas į sinchroninius klientus

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip konvertuoti asinchronius klientus į sinchronius klientus Microsoft Dynamics 365 Commerce.

Norėdami konvertuoti asinchroniniai klientus į sinchroniniai klientai, atlikite šiuos žingsnius.

1. Paleiskite "Commerce Headquarters" **P užduotį, norėdami** asinchroninių klientų siuntinį į "Commerce Headquarters".
1. Paleiskite **klientų sinchronizavimo ir verslo partnerių iš "Async" režimo** užduoties, kad sukurtumėte kliento sąskaitų DK. (Ši užduotis anksčiau buvo pavadinta **Sinchronizuokite klientus ir verslo partnerius naudojant "Async" režimą**.)
1. Vykdykite **1010** užduotį, norėdami sinchronizuoti naujų kliento sąskaitų NUMERIUS su kanalais.

Jei užsakymas nurodo nesinchroninį klientą arba adresą, kuris dar nesinchronizuotas su "Commerce Headquarters", **klientas arba adresas bus sinchronizuojami kaip užsakymų sinchronizavimo paketinės užduoties** dalis. Jei grynųjų pinigų ir carry operacija nurodo nesinchroninį klientą arba adresą, klientas arba adresas bus sinchronizuojami prieš dienos pabaigos (EOD) registravimą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Klientų valdymas parduotuvėse](customer-mgmt-stores.md)

[Asinchroninis kliento kūrimo režimas](async-customer-mode.md)

[Kliento atributai](dev-itpro/customer-attributes.md)

[Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
