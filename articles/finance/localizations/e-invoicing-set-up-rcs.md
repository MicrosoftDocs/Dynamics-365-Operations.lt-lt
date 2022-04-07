---
title: Nustatyti reguliavimo konfigūracijos tarnybą (RCS)
description: Šioje temoje paaiškinama, kaip nustatyti reguliavimo konfigūracijos tarnybą (RCS).
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6aed74656ceb8edd0e88adf53b61fcae81241f54
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470183"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Nustatyti reguliavimo konfigūracijos tarnybą (RCS)

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti reguliavimo konfigūracijos tarnybą (RCS).

## <a name="turn-on-globalization-features"></a>Įjungti globalizavimo funkcijas

1. Prisijunkite prie jūsų RCS abonemento.
2. Pasirinkite plytelę **Funkcijų valdymas**.
3. **Funkcijų valdymo** darbo srityje sąraše pasirinkite **Globalizacijos funkcijos** ir pasirinkite **Įjungti dabar**.

Dabar globalizavimo funkcijų **darbo srities išklotinė** vieta dabar turi būti pagrindinėje RCS skelbimų srityje.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu

1. Darbo srities **Globalizacijos funkcijos** dalyje **Susiję parametrai** pasirinkite saitą **Elektroninių ataskaitų parametrai**.
2. Aptarnavimo **galinio punkto** **URI lauke skirtuke Elektroninis SF** išrašymas Microsoft Azure įveskite atitinkamą geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.

    | Duomenų centras „Azure" geografijoje | Paslaugos galinio punkto URI |
    |----------------------------|----------------------|
    | Jungtinės Valstijos              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Jungtinė Karalystė             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japonija                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Šveicarija                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brazilija                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Jungtiniai Arabų Emyratai       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australija                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Prancūzija                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Indija                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Patvirtinkite, kad **Programos ID** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Ši vertė yra fiksuota vertė. Įsitikinkite, kad įvestas tik globalus unikalus identifikatorius (GUID) ir kad į reikšmę nėra jokių kitų simbolių, pvz., tarpų, kablelių, periodų ar kabučių.
4. **Lauke LCS aplinkos ID** įveskite savo ciklo Microsoft Dynamics tarnybų (LCS) aplinkos ID. Ši vertė yra nuoroda į finansų arba tiekimo grandinės valdymo aplinką, kurią naudosite su elektroninių SF išrašymo paslauga. Norėdami gauti savo ID, [prisijunkite prie LCS](https://lcs.dynamics.com/), atidarykite projektą, **·** **·** **tada skirtuko Aplinkos valdymas skyriuje Aplinkos informacija žiūrėkite lauke Aplinkos ID.**

    > [!IMPORTANT]
    > Jei elektroninių SF išrašymo priedas įdiegtas keliose finansų arba tiekimo grandinės valdymo aplinkose LCS, visada naudokite pastaruoju metu įdiegtos aplinkos ID. Jei nuspręsite įdiegti priedą naujoje aplinkoje Po to, kai nustatėte ir dirbote su elektroninių SF išrašymo funkcija, **atnaujinkite LCS aplinkos ID** lauką RCS į naujausią reikšmę.

5. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="configuration-providers"></a>Konfigūracijos teikėjai

Naudodami konfigūracijos teikėjus galite atskirti elektroninių ataskaitų (ER) konfigūracijų, kurios naudojamos elektroninio SF išrašymo procesuose, savininkus ir savininkų globalizavimo funkcijas. Visoms globalizavimo funkcijoms, kurias teikia "Microsoft" ir kurios publikuojamos visuotinoje saugykloje, konfigūracijos teikėjas nustatomas kaip **"Microsoft** " (`http://microsoft.com`).

Galite koreguoti tik ER konfigūracijas ir globalizavimo funkcijas, kurios priklauso aktyviam konfigūracijos tiekėjui. Šias konfigūracijas ir priemones galite naudoti kaip šablonus, jei norite kurti konfigūracijas ir priemones, priklausančias aktyviam konfigūracijos teikėjui, kad jas būtų galima koreguoti.

Pirma, sukurkite konfigūracijos teikėjus. Tada nustatykite vieną iš jų kaip aktyvią. Nustatyti "Microsoft **" konfigūracijos teikėjo** kaip aktyvaus negalima.

### <a name="create-a-configuration-provider"></a>Konfigūracijos teikėjo kūrimas

1. **Elektroninės ataskaitos** darbo srityje, **Susijusios nuorodos** skyriuje, pasirinkite **Konfigūravimo tiekėjai**.
2. Pasirinkite **Nauja**.
3. **Lauke Pavadinimas** įveskite unikalų konfigūracijos teikėjo pavadinimą.
4. **Interneto adreso** lauke įveskite unikalų konfigūracijos teikėjo URL.
5. Pasirinkite **Įrašyti** ir uždarykite puslapį.

### <a name="select-a-configuration-provider-as-active"></a>Pasirinkti konfigūracijos teikėją kaip aktyvų

1. Konfigūracijos teikėjų sąraše pasirinkite konfigūracijos teikėją, kurį norite nustatyti kaip aktyvų.
2. Pasirinkite **Nustatyti kaip aktyvų**.

## <a name="import-er-configurations-from-the-global-repository"></a>Importuoti ER konfigūracijas iš visuotinės saugyklos

1. **Elektroninės ataskaitos** darbo srityje, **Susijusios nuorodos** skyriuje, pasirinkite **Konfigūravimo tiekėjai**.
2. Konfigūracijos teikėjų sąraše pasirinkite " **Microsoft"**, tada pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotinis**, tada veiksmų srityje pasirinkite **Atidaryti**.
4. Importuokite šiuos ER modelius:

    - **Kliento SF konteksto modelis**
    - **Sąskaitos faktūros modelis**
    - **Iždo dokumentai** (Brazilijos scenarijams, jei reikia)
    - **Atsakymo pranešimo modelis**

5. Jei **SF modelio susiejimas** nebuvo importuotas automatiškai, importuokite jį.
6. Uždarykite puslapį.
