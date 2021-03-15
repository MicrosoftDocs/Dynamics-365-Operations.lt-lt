---
title: Importuoti papildomus duomenis iš failų
description: Šioje temoje paaiškinta, kaip paruošti duomenis iš išorės sistemų, kad juos būtų galima importuoti į „Microsoft Dynamics 365 Finance“.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7ced1b970aefa20a27ab16e005dff8fabace78d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988830"
---
# <a name="import-subsidiary-data-from-files"></a>Importuoti papildomus duomenis iš failų

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinta, kaip paruošti duomenis iš išorės sistemų, kad juos būtų galima importuoti į „Microsoft Dynamics 365 Finance“. Galite naudoti **Konsoliduoti su impotavimu** puslapį (**Konsolidavimai \> Konsoliduoti su importavimu**) siekiant parengti papildomų duomenų perdavimą iš išorės sistemų.

1. Sukurti papildomą asmenį konsolidavimo procesui. Dėl informacijos apie tai, kaip sukurti juridinius asmenis, žr. [Kurti juridinius asmenis](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Dėl daugiau informacijos, žr. [Parengti juridinį asmenį naudojimui konsolidavimo procese](prepare-company-for-consolidation.md) ir [Nustatyti papildomą juridinį asmenį konsolidavimui](set-up-subsidiary-company-for-consolidation.md).

2. Parenkite failą, kuriame yra importuojami duomenys. Dėl daugiau informacijos apie importavimo procesą, žr. [Duomenų importavimo ir eksportavimo darbų peržiūra](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Eksportuoti duomenis į failą pagal šiuos veiksmus „Duomenų importavimas/eksportavimo procesai“ procedūrą [Duomenų importavimo ir eksportavimo darbų peržiūra](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Galite naudoti procedūrą siekiant konsoliduoti duomenis iš kito elemento „Dynamics 365 Finance“ arba iš „Dynamics 365 Business Central“. Jei importuojate duomenis iš išorės sistemų, duomenys turi būti aprašytu formatu [Eksportuoti papildomus duomenis į failus](export-subsidiary-data-to-file.md).
4. Eiktie į **Konsolidavimai \> Konsoliduoti su importavimu**. Puslapyje **Konsoliduoti su importavimu**, skirtuke **Kriterijai** nurodykite išsamią ataskaitų ir (ar) importavimo informaciją nustatydami tolesnius laukelius.

    | Laukas                                 | Ataskaitos vertė | Importavimo vertė |
    |---------------------------------------|----------------------|----------------------|
    | aprašymas                           | Netaikoma | Įveskite aprašą skirtą importavimą identifikuoti. |
    | Korespondentinė sąskaita, subsąskaita                          | Nustatykite sąskaitų intervalą, kurį turi apimti ataskaita. Jei nenustatėte intervalo, visos sąskaitos bus apimtos. | Nustatykite sąskaitų intervalą, kurį turi apimti importavimas. Jei nenustatėte intervalo, visos sąskaitos bus apimtos. |
    | Konsolidacijos laikotarpis                  | Nustatykite datų intervalą konsolidavimui. | Nustatykite datų intervalą konsolidavimui. |
    | Įtraukti faktines sumas                | Nustatykite parinktį į **Taip** norėdami įtraukti esamas vertes. | Nustatykite parinktį į **Taip** norėdami įtraukti esamas vertes. |
    | Įtraukti biudžeto sumas                | Nustatykite parinktį į **Taip** norėdami įtraukti biudžeto sumas konsolidavimuose. | Nustatykite parinktį į **Taip** norėdami įtraukti biudžeto sumas konsolidavimuose. |
    | Naujas balansų sukūrimas konsoliduojant | Nustatykite šią parinktį į **Taip** jei papildomo kūrimo procesas turi visiškai panaikinti balanso ir naujus įrašus ir sukurkite iš naujo balansą nuo laiko pradžios. | Nustatykite šią parinktį į **Taip** jei papildomo kūrimo procesas turi visiškai panaikinti balanso ir naujus įrašus ir sukurkite iš naujo balansą nuo laiko pradžios. |
    | Biudžeto modeliai                         | Netaikoma | Jei renkatės importuoti biudžeto sumas, įveskite biudžeto modelius konsilidavimui. |
    | Biudžeto kurso tipas                      | Netaikoma | Įveskite keitimo kurso biudžeto tipą. |

6. Jei turite kitas apskaitos valiutas, naudokite laukelius **Esamas vertimas** skirtuke, kad konfigūruotumėte vertimą, kuris atliekamas konsolidavimo metu.

    | Laukas                      | aprašymas |
    |----------------------------|-------------|
    | Šaltinio juridinis subjektas        | Rinkitės juridinį objektą, iš kurio importuojate. |
    | Šaltinio apskaitos valiuta | Numatytoji valiuta yra valiuta susieta su šaltinio juridinu asmeniu, kurį pasirinkote **Šaltinio juridinis asmuo** laukelyje. |
    | Nuo iki sąskaitos       | Nustatykite sąskaitų intervalą, kurais importuosite iš šaltinio juridinio asmens. |
    | Valiutos kurso tipas         | Rinkitės keitimo kurso biudžeto tipą. Keitimo kursai yra būtini ir turi būti priskirti jums kuriant pagrindinę sąskaitą. Daugiau informacijos žr. [Kurti pagrindinę sąskaitą](tasks/create-main-account.md). |
    | Taikyti valiutos kursą nuo   | Įveskite datą taikomą keitimo kursui, kuris įsigalioja tą dieną. Kitu atveju, įveskite vertę, kuri turi būti naudojama kaip keitimo kursas. |
    | Valiutos kursas              | Numatyta vertė priklauso nuo keitimo kurso, kurį rinkotės **Keitimo kurso tipas** laukelyje. Jei įvedėte, vartotojo nustatytą keitimo kursą, galtie nustatyti intervalą. |

7. Nustatykite **Vykdyti fone** parintkį į **Taip** siekiant įjungti importavimo procesą vykdomą fone.
8. Nustatykite **Paketo tvarkymo** parinktį į **Taip** tam, kad vykdytumėte konsolidavimą kaip paketo darbą konkrečiu laiku. Norėdami vykdyti konsolidavimą nedelsiant, rinkitės **Gerai**. 

Perlaidos ir balansai nurodyti konsolidavimui papildomose įmonėse yra įtraukiami į atitinkamas sąskaitas konsoliduojamame juridiniame asmenyje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]