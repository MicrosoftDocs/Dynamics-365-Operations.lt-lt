---
title: Sandėlio programos įvykiai
description: Šiame straipsnyje aprašomas sandėlio programos įvykio apdorojimas, naudojamas sandėlio programos įvykių pranešimui kaip paketinės užduoties daliai apdoroti.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41b9538d3064bad24c4c5c60d401605e47e9c655
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905460"
---
# <a name="warehouse-app-event-processing"></a>Sandėlio programos įvykių apdorojimas

[!include [banner](../includes/banner.md)]

„Supply Chain Management“ vykdomos paketinės užduotys gali naudoti duomenis iš apdorojimo įvykių eilės, kuri yra gaunama iš sandėlio valdymo mobiliųjų įrenginių programėlės tam, kad galėtų reaguoti į pateikiamus įvykius, kaip reikia. Ši funkcija įtraukia atitinkamus įvykius į eilę, reaguodama į tam tikrų tipų veiksmus, kuriuos atlieka darbuotojai naudodami programą. Pavyzdžiui, kai naudojate funkciją *Kurti ir apdoroti perkėlimo užsakymus iš sandėlio programos*, sistemai vykdant paketinę užduotį **Apdoroti sandėlio programos įvykius** fone sukuriama ir atnaujinama perkėlimo užsakymo antraštė bei eilutės.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>Įjungti arba išjungti funkciją Apdoroti sandėlio programos įvykius

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali įjungti arba išjungti šią funkciją, naudodamiesi funkcijų *valdymo* darbo srityje funkcija Apdoroti sandėlio [app events](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Sandėlio programos įvykių apdorojimo paketinės užduoties konfigūravimas

### <a name="process-warehouse-app-events"></a>Apdoroti sandėlio programos įvykius

Sukonfigūruokite suplanuotą paketinę užduotį sandėlio programos įvykių apdorojimui kuriant perkėlimo užsakymą ir atnaujinant eilutes.

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Apdoroti sandėlio programos įvykius**.
1. Atidaromas sandėlio programos įvykių apdorojimo dialogo langas. Išplėskite „FastTab“ **Vykdyti fone** ir nustatykite **Paketinis apdorojimas** reikšmę **Taip**.
1. **Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.
1. **Nustatyti pakartojimą** langas atsidaro. Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.
1. Pasirinkite **Gerai**, kad sugrįžtumėte į dialogo langą **Apdoroti sandėlio programos įvykius**.
1. Dialogo lange **Apdoroti sandėlio programos įvykius** pasirinkite **Gerai**, kad įtrauktumėte paketinę užduotį į paketo eilę.

## <a name="query-warehouse-app-events"></a>Pateikite sandėlio programos įvykių užklausą

Sandėlio valdymo mobiliųjų įrenginių programėlės sugeneruotą įvykių eilę ir įvykių pranešimus galite peržiūrėti nuėję į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.

## <a name="the-standard-event-queue-process"></a>Standartinis įvykių eilės procesas

Sandėlio programos įvykių eilės apdorojimas atliekamas tokia tvarka:

1. Įvykis įtraukiamas į eilę kartu su įvykio pranešimu. Iš pradžių naujo pranešimo įvykio būsena yra **Laukiama**, o tai reiškia, kad paketinė užduotis **Apdoroti sandėlio programos įvykius** šio pranešimo neišrinks ir neapdoros.
1. Iš karto, kai pranešimo būsena atnaujinama į **Eilėje**, įvykių paketinė užduotis **Apdoroti sandėlio programos įvykius** išrinks ir apdoros įvykį.
1. Priklausomai nuo to, ar reikiamą procesą buvo įmanoma atlikti, paketinė užduotis atnaujina įvykių būsenas į **Atlikta** arba **Nepavyko**.
1. Kai visų susijusių įvykio pranešimų būsena yra **Atlikta**, įvykis pašalinamas iš eilės.

 Išsamų pavyzdį žr. [Kurti perkėlimo užsakymą naudojant sandėlio programos procesą](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Įvykio klaidų tvarkymas

Atliekant sandėlio įvykių apdorojimą, reikiamai pranešimo veiklai gali nebūti suteikti paketinės užduoties procesai. Šiuo atveju įvykio pranešimas pasikeis į **Nepavyko**. Norėdami sužinoti priežastį ir imtis reikiamų veiksmų, kad išspręstumėte problemas, galite naudoti **paketo žurnalo** informaciją.

Išsamų pavyzdį žr. [Kurti perkėlimo užsakymą naudojant sandėlio programą](create-transfer-order-from-warehouse-app.md).

Norėdami atkurti nesėkmingo sandėlio programos įvykio pranešimą:

1. Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.
1. „FastTab“ **Sandėlio programos įvykių pranešimai** suraskite ir pasirinkite atitinkamą įvykį, kurio būsena stulpelyje **Įvykio būsena** yra **Nepavyko**.
1. Įrankių juostoje **Sandėlio programos įvykių pranešimai** pasirinkite **Atkurti**.
1. Tęskite darbą, kol atkursite visus susijusius pranešimus.

Įvykio pranešimą **Nepavyko** taip pat galite pašalinti naudodami parinktį **Naikinti**, pasiekiamą įrankių juostoje **Sandėlio programos įvykių pranešimai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]