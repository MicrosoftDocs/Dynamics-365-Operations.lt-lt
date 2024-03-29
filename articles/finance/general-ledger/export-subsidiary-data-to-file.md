---
title: Eksportuoti papildomus duomenis į failus
description: Šiame straipsnyje paaiškinama, kaip pasiruošti eksportuoti duomenis iš " Microsoft Dynamics 365 Finance" ir importuoti juos į konsoliduotą juridinį subjektą.
author: jinniew
ms.date: 11/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 30d69f9a2813621df410a29568644f264392fb49
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779967"
---
# <a name="export-subsidiary-data-to-files"></a>Eksportuoti papildomus duomenis į failus

[!include [banner](../includes/banner.md)]

Naudojate **Eksportuoti** puslapį (**Sistemos administravimas \> Darbo aplinkos \> Importuoti/Eksportuoti**) tam, kad parengtumėte eksportuoti papildomus duomenis į failus, kurie tuomet gali būti importuoti į konsoliduotą juridinį asmenį. Dėl daugiau informacijos apie importavimo ir eksportavimo procesus, žr. [Duomenų importavimo ir eksportavimo darbų peržiūra](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Sukurti juridinį asmenį konsolidavimo procesui. Dėl informacijos apie tai, kaip sukurti juridinius asmenis, žr. [Kurti juridinius asmenis](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Dėl daugiau informacijos, žr. [Parengti juridinį asmenį naudojimui konsolidavimo procese](prepare-company-for-consolidation.md) ir [Nustatyti papildomą juridinį asmenį konsolidavimui](set-up-subsidiary-company-for-consolidation.md). 

2. Eiktie į **Konsolidavimai \> Eksportuoti įmonių balansus**. Puslapyje **Eksportuoti įmonių balansus** skirtuke **Kriterijai** nurodykite išsamią konsolidavimo informaciją nustatydami tolesnius laukelius.

    | Laukas                             | aprašymas |
    |-----------------------------------|-------|
    | **Pagrindinė sąskaita**                      | Nustatykite konsoliduotinas sąskaitas. Norėdami įtraukti visas sąskaitas, palikite laukelį tuščią. |
    | **Naudokite konsolidavimo sąskaitą**         | Jei nustatėte konsolidavimo sąskaitas, nustatykite parinktį į **Taip**. |
    | **Pasirinkti konsolidacijos sąskaitą iš** | Rinkitės **Pagrindinę sąskaitą** ar **Konsoliduotos sąskaitos grupę**. |
    | **Konsolidacijos sąskaitų grupė**       | Rinkitės konsolidavimo sąskaitos grupę jūsų pasirinktai konsolidavimo sąskaitai. |
    | **Konsolidacijos laikotarpis**              | Nurodykite „nuo“ ir „iki“ datas konsolidavimui. |
    | **Įtraukti faktines sumas**            | Nustatykite parinktį į **Taip** norėdami įtraukti esamas sumas. |
    | **Įtraukti biudžeto sumas**            | Nustatykite parinktį į **Taip** norėdami įtraukti biudžeto sumas konsolidavimuose. |
    | **Biudžeto modeliai**                     | Nurodykite įtraukiamą biudežto modelį. |

3. Skirtuke **Finansinės dimensijos**, nurodykite išsamią konsolidavimo informaciją:

    - Nurodykite finansinės dimensijos informaciją, kuri turi būti perduodamas iš transakcijos į papildomas sąskaitas į transakcijas konsoliduotame juridiniame asmenyje.
    - Rinkitės finansines dimensijas sąraše.
    - Nurodykite tinkamą specifikaciją kiekvienai konsoliduotai finansinei dimensijai. Esamos parinktys apima **Dimensiją**, **Grupės dimensiją**, **Kompanijos sąskaitas** ir **Paskyrą**.

        > [!NOTE]
        > Parinktis **Grupės dimensija** leidžia jums nustatyti dimensijos vertę, kurią naudoja konsoliduojama įmonių grupė.

    - Nurodykite segmento užsakymą, kuriame konsoliduojate.

4. Skirtuke **Juridiniai asmenys**, atlikite šiuos žingsnius, kad nurodytumėte juridinį asmenį, kurį eksportuojate:

    1. Pasirinkite **Naujas**.
    2. Laukelyje **Šaltinio juridinis asmuo**, įveskite juridinį asmenį.

        Jei tie patys kriterijai taikomi keliems papildiniams, kurie yra toje pačioje duomenų bazėje, galite perduoti duomenis iš tų papildinių į atskirus eksportuojamus failus viena operacija:

        1. Sukurkite kiekvienam papildomam juridiniam asmeniui eilutę, kuriam sąskaitos turi būti eksportuojamos į failus. Šie failai bus importuojami į konsoliduotą juridinį asmenį vėliau.
        2. Kiekvienam papildiniui įveskite papildinio pavadinimą ir eksportuojamo failo pavadinimą, kuris bus sukuriamas eksportavimo darbo metu.

    3. Laukelyje **Konvertuojamų skirtumų sąskaitos tipas** laukelyje, rinkitės **Pelnas ir nuostoliai** ar **Balansas**.
    4. Įveskite pavadinimą eksportuojamam failui, kuris bus sukurtas.

5. Rinkitės **Gerai** tam, kad vykdytumėte eksportavimą.

Užbaigus eksportavimą, gausite pranešimą, kuriame bus rodomas įrašų skaičius, įrašytas į kiekvieną failą. Tuomet galite importuoti failus į konsoliduotą juridinį asmenį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
