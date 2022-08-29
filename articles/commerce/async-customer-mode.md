---
title: Asinchroninis kliento kūrimo režimas
description: Šiame straipsnyje aprašomas asinchroninis kliento kūrimo režimas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 1ac1bc842d5d12ece8951ffed18157e6f9b50d14
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228729"
---
# <a name="asynchronous-customer-creation-mode"></a>Asinchroninis kliento kūrimo režimas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomas asinchroninis kliento kūrimo režimas Microsoft Dynamics 365 Commerce.

Komercijoje naudojami du klientų kūrimo būdai: sinchroninis (arba sinchronizavimas) ir asinchroninis (arba "async"). Numatyta, kad klientai sukuriami sinchroniškai. Kitaip tariant, jos realiuoju laiku sukuriamos "Commerce Headquarters". Sinchronizavimo kliento kūrimo režimas pagal reikalavimus, nes nauji klientai nedelsdami ieškomi kanaluose. Tačiau yra ir trūkumų. Kadangi ši funkcija generuoja [Commerce Data Exchange: realaus laiko paslaugos](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) skambučius į „Commerce“ valdymo sritį, veiksmingumui tai gali daryti įtakos, jei vienu metu atliekami keli kliento kūrimo skambučiai.

Jei parinktis **Kurti klientą asinchroniniu režimu** nustatyta kaip **Taip** parduotuvės funkcijų profilyje (**Mažmeninė prekyba ir komercija \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcijų profiliai**), realiu laiku atliekami skambučiai nenaudojami klientų įrašams kurti kanalo duomenų bazėje. "Async" kliento kūrimo režimas "Commerce Headquarters" našumui įtakos neturi. Laikinas visuotinis unikalus identifikatorius (GUID) priskiriamas kiekvienam naujam "async" kliento įrašui ir naudojamas kaip kliento kodo ID. Šis GUID nerodomas point sale (EKA) vartotojams. Vietoje to, kaip kliento paskyros ID šie naudotojai matys **Laukiama sinchronizavimo**.

> [!IMPORTANT]
> Kai EKA atsijungiama nuo tinklo, sistema automatiškai sukuria klientus asinchroniškai, net jei "async" kliento kūrimo režimas išjungtas. Todėl, neatsižvelgiant į jūsų pasirinkimą sinchronizuoti ir "async" kliento kūrimą, "Commerce Headquarters" administratoriai turi sukurti ir suplanuoti pasikartojančią P **užduoties paketinę užduotį,** sinchronizuoti klientus ir verslo partnerius **iš "Async** **" režimo užduoties ir 1010** užduoties, kad visi "async" klientai būtų konvertuoti į sinchronizavimo klientus "Commerce Headquarters".

## <a name="async-customer-limitations"></a>„Async“ kliento apribojimai

"Async" kliento funkcija šiuo metu turi šį apribojimą:

- Lojalumo kortelių negalima išduoti "async" klientams, nebent naujas kliento sąskaitos ID buvo sinchronizuotas atgal į kanalą.

## <a name="async-customer-enhancements"></a>"Async" kliento patobulinimai

Siekiant padėti organizacijoms naudoti "Async" klientų kūrimo režimą ir valdyti klientus bei padėti realiuoju laiku sumažinti ryšį su "Commerce Headquarters", įdiegti šie patobulinimai, siekiant suderinti sinchronizavimo ir "async" režimus kanaluose. 

| Funkcijos patobulinimas | "Commerce" versija | Išsami informacija apie funkciją |
|---|---|---|
| Efektyvumo patobulinimai, kai iš kanalų duomenų bazės nuskaitoma kliento informacija | 10.0.20 ir vėliau | Kad būtų pagerintas našumas, kliento objektas padalintas į mažesnius objektus. Tada sistema nuskaito tik reikiamą informaciją iš kanalo duomenų bazės. |
| Galimybė sukurti adresą asinchroniškai atliekant registraciją | 10.0.22 ir vėliau | <p>Priemonės raktas: **įgalinti asinchroninį klientų adresų kūrimą**</p><p>Priemonės informacija:</p><ul><li>Galimybė įtraukti adresus neįrašant "Real-time Service" skambučių į "Commerce Headquarters"</li><li>Galimybė unikaliai identifikuoti adresus kanalo duomenų bazėje nenaudojant įrašo ID (**RecId** vertės)</li><li>Adreso kūrimo sekimo laiko žymos</li><li>Adresų sinchronizavimas "Commerce Headquarters"</li></ul><p>Ši funkcija veikia ir sinchronizavimo klientus, ir "async" klientus. Norėdami redaguoti adresus asinchroniškai be jų kūrimo asinchroniškai, **turite įgalinti klientų redagavimą asinchroninio režimo funkcija**.</p> |
| Įgalinti sinchroninio ir asinchroninio kliento kūrimo lygumą. | 10.0.24 ir vėliau | <p>Funkcijos perjungimas: įgalinti **patobulintą "async" kliento kūrimą**</p><p>Funkcijos informacija: gebėjimas fiksuoti papildomą informaciją, pvz., pareigas, priskyrimus iš numatytojo kliento ir antrinę kontaktinę informaciją (telefono numerį ir el. pašto adresą), o tada kurti klientus asinchroniškai</p> |
| Vartotojui patogus klaidų pranešimas | 10.0.28 ir vėliau | Šie patobulinimai padeda pagerinti vartotojui patogius klaidų pranešimus, jei vartotojas negali iš karto redaguoti informacijos, kol vyksta sinchronizavimas. Šiuos patobulinimus įgalinate naudodami **funkciją Leisti, kad tam tikri vartotojo sąsajos elementai būtų nemodifikuojami "Async** **\>**" kliento parametru "Commerce" svetainės parametrų plėtinių generatoriuje. |
| Galimybė redaguoti kliento informaciją asinchroniškai | 10.0.29 ir vėliau | <p>Funkcijos perjungimas: **įgalinti klientų redagavimą asinchroniškai režimu**</p><p>Funkcijos informacija: galimybė redaguoti kliento duomenis asinchroniškai</p><p>Norėdami gauti atsakymų į bendrus klausimus apie problemas, susijusias su kliento informacijos redagavimas asinchroniškai, [žr. asinchroninio kliento kūrimo režimo DUK](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Priemonių perjungimo hierarchija

Dėl priemonių raktų hierarchijos prieš **įjungdami funkciją Įgalinti klientų redagavimą asinchroninio** režimo režimu turite įgalinti šias funkcijas: 

- **Klientų užsakymų ir klientų operacijų našumo patobulinimai** – ši funkcija yra privaloma nuo "Commerce" 10.0.28 versijos leidimo. 
- **Įgalinti patobulintą "async" kliento kūrimą**
- **Įjungti asinchroninį klientų adresų kūrimą**

Atsakymus į bendruosius trikčių diagnostikos klausimus rasite asinchroninio [kliento kūrimo režimo DUK](async-customer-mode-faq.md). 

Įjungę anksčiau nurodytas funkcijas, **turite suplanuoti pasikartojanti P** užduoties paketinę užduotį, **sinchronizuoti klientus ir verslo partnerius iš "Async** **" režimo užduoties ir 1010** užduoties, kad visi "Async" klientai būtų konvertuoti į sinchronizavimo klientus "Commerce Headquarters".

### <a name="customer-creation-in-pos-offline-mode"></a>Kliento kūrimas EKA autonominiu režimu

Kaip buvo nurodyta anksčiau, kai EKA atsijungiama nuo tinklo, sistema automatiškai sukuria klientus asinchroniškai, net jei "async" kliento kūrimo režimas išjungtas. Todėl "Commerce Headquarters" administratoriai turi sukurti ir suplanuoti pasikartojanti P **užduoties paketinę užduotį,** sinchronizuoti klientus ir verslo partnerius **iš "Async** **" režimo užduoties ir 1010** užduoties, kad visi "Async" klientai būtų konvertuoti į sinchronizavimo klientus "Commerce Headquarters".

> [!NOTE]
> Jei parinktis **Filtruoti bendrinamas kliento duomenų lenteles** nustatoma kaip **Taip** puslapyje **„Commerce“ kanalo schema** (**Mažmeninės prekybos ir komercijos sąranka \> Valdymo srities sąranka \> „Commerce“ planuoklis \> Kanalo duomenų bazės grupė**), kliento įrašai nesukuriami EKA, veikiant autonominiu režimu. Daugiau informacijos žr. skyriuje [Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildomi ištekliai

[Klientų valdymas parduotuvėse](customer-mgmt-stores.md)

[Asinchroninių klientų konvertavimas į sinchroninius klientus](convert-async-to-sync.md)

[Kliento atributai](dev-itpro/customer-attributes.md)

[Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
