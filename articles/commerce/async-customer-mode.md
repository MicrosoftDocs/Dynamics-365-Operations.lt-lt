---
title: Asinchroninis kliento kūrimo režimas
description: Šioje temoje aprašomas asinchroninis kliento kūrimo režimas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 43418b61778d187364d4d52a05178078a37623eb
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984275"
---
# <a name="asynchronous-customer-creation-mode"></a>Asinchroninis kliento kūrimo režimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomas asinchroninis kliento kūrimo režimas Microsoft Dynamics 365 Commerce.

Komercijoje naudojami du klientų kūrimo būdai: sinchroninis (arba sinchronizavimas) ir asinchroninis (arba "async"). Numatyta, kad klientai sukuriami sinchroniškai. Kitaip tariant, jie kuriami realiuoju laiku „Commerce“ valdymo srityje. Sinchronizavimo kliento kūrimo režimas pagal reikalavimus, nes nauji klientai nedelsdami ieškomi kanaluose. Tačiau yra ir trūkumų. Kadangi ši funkcija generuoja [Commerce Data Exchange: realaus laiko paslaugos](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) skambučius į „Commerce“ valdymo sritį, veiksmingumui tai gali daryti įtakos, jei vienu metu atliekami keli kliento kūrimo skambučiai.

Jei parinktis **Kurti klientą asinchroniniu režimu** nustatyta kaip **Taip** parduotuvės funkcijų profilyje (**Mažmeninė prekyba ir komercija \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcijų profiliai**), realiu laiku atliekami skambučiai nenaudojami klientų įrašams kurti kanalo duomenų bazėje. "Async" kliento kūrimo režimas "Commerce Headquarters" našumui įtakos neturi. Laikinas visuotinis unikalus identifikatorius (GUID) priskiriamas kiekvienam naujam "async" kliento įrašui ir naudojamas kaip kliento kodo ID. Šis GUID nerodomas point sale (EKA) vartotojams. Vietoje to, kaip kliento paskyros ID šie naudotojai matys **Laukiama sinchronizavimo**.

> [!IMPORTANT]
> Kai EKA atsijungiama nuo tinklo, sistema automatiškai sukuria klientus asinchroniškai, net jei "async" kliento kūrimo režimas išjungtas. Todėl, neatsižvelgiant į jūsų pasirinkimą sinchronizuoti ir "async" kliento kūrimą, "Commerce Headquarters" administratoriai turi sukurti ir suplanuoti pasikartojanti P užduoties paketinę užduotį, sinchronizuoti klientus ir verslo partnerius iš "Async" režimo užduoties (anksčiau vadinama Sinchronizuoti klientus ir verslo partnerius iš "async" režimo) ir 1010 užduoties, kad visi "async" klientai būtų konvertuoti į **sinchronizavimo** **·** **·** **klientus**" "Commerce Headquarters".

## <a name="async-customer-limitations"></a>„Async“ kliento apribojimai

"Async" kliento funkcijai šiuo metu taikomi šie apribojimai:

- „Async“ kliento įrašų redaguoti negalima, nebent „Commerce“ valdymo srityje buvo sukurtas klientas, o naujo kliento paskyros ID sinchronizuotas atgal į kanalą.
- Lojalumo kortelių negalima išduoti "async" klientams, nebent naujas kliento sąskaitos ID buvo sinchronizuotas atgal į kanalą.

## <a name="async-customer-enhancements"></a>"Async" kliento patobulinimai

Kaip ir "Commerce" 10.0.24 versijos leidimą funkcijų valdymo darbo srityje galite įgalinti funkciją Įgalinti patobulintą **"async"** **kliento** kūrimą. Ši funkcija jungia tarpą tarp "async" ir sinchronizavimo kliento kūrimo režimų EKA ir el. prekyboje šiais būdais:

- Priskyrimus galima susieti su "Async" klientais.
- Pavadinimus galima įtraukti į "Async" klientus.
- Antriniai el. pašto adresai ir telefono numeriai gali būti užfiksuoti "Async" klientams.

Kaip ir "Commerce" 10.0.22 versiją, funkcijų valdymo darbo srityje galite įgalinti asinchroninį klientų adresų **kūrimo** **funkciją**. Ši funkcija leidžia naujai sukurti klientų adresus asinchroniškai įrašyti ir sinchronizavimo klientams, ir "async" klientams.

Įjungę anksčiau nurodytas funkcijas, turite suplanuoti pasikartojanti P užduoties paketinę užduotį, sinchronizuoti klientus ir verslo partnerius iš "Async" režimo užduoties ir 1010 užduoties, kad visi "Async" klientai būtų konvertuoti į **sinchronizavimo** **·** **klientus** "Commerce Headquarters".

### <a name="customer-creation-in-pos-offline-mode"></a>Kliento kūrimas EKA autonominiu režimu

Kaip buvo nurodyta anksčiau, kai EKA atsijungiama nuo tinklo, sistema automatiškai sukuria klientus asinchroniškai, net jei "async" kliento kūrimo režimas išjungtas. Todėl "Commerce Headquarters" administratoriai turi sukurti ir suplanuoti pasikartojanti P užduoties paketinę užduotį, sinchronizuoti klientus ir verslo partnerius iš "Async" režimo užduoties ir 1010 užduoties, kad visi "Async" klientai būtų konvertuoti į **sinchronizavimo** **·** **klientus** "Commerce Headquarters".

> [!NOTE]
> Jei parinktis **Filtruoti bendrinamas kliento duomenų lenteles** nustatoma kaip **Taip** puslapyje **„Commerce“ kanalo schema** (**Mažmeninės prekybos ir komercijos sąranka \> Valdymo srities sąranka \> „Commerce“ planuoklis \> Kanalo duomenų bazės grupė**), kliento įrašai nesukuriami EKA, veikiant autonominiu režimu. Daugiau informacijos žr. skyriuje [Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildomi ištekliai

[Klientų valdymas parduotuvėse](customer-mgmt-stores.md)

[Asinchroninių klientų konvertavimas į sinchroninius klientus](convert-async-to-sync.md)

[Kliento atributai](dev-itpro/customer-attributes.md)

[Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
