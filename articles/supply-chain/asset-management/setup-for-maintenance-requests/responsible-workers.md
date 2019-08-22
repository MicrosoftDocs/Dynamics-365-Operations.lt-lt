---
title: Už priežiūrą atsakingi darbuotojai
description: Šiame straipsnyje aprašoma, kaip priskirti už priežiūrą atsakingus darbuotojus modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790520"
---
# <a name="responsible-maintenance-workers"></a>Už priežiūrą atsakingi darbuotojai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Už priežiūrą atsakingi darbuotojai gali būti susiję su turto tipais, turtu, funkcinėmis vietovėmis, priežiūros užduoties tipo kategorijomis, priežiūros užduočių tipais, priežiūros užduoties tipo variantais ir prekyba. Jie gali būti naudojami darbo užsakymuose ir priežiūros užklausose, siekiant nurodyti nuostatą, kurie priežiūros darbuotojai turėtų būti atsakingi už darbo užsakymą. (Tačiau šie techninės priežiūros darbuotojai nebūtinai yra tie patys darbuotojai, kuriems numatyta atlikti darbų užsakymą.) Šios funkcijos naudojimas yra neprivalomas. Pavyzdžiui, ji gali būti naudojama norint pasirinkti atsakingus darbuotojus arba darbuotojų grupes konkretiems darbo tipams arba darbo sritims.

Darbo užsakymo ciklo arba priežiūros užklausos ciklo metu, už priežiūrą atsakingi darbuotojai gali būti keičiami arba atnaujinami. Šis pakeitimas arba atnaujinimas gali būti susijęs, pavyzdžiui, su priežiūros užklausos ciklo būsenos arba darbo užsakymo ciklo būsenos pasikeitimu.

Puslapio **Už priežiūrą atsakingi darbuotojai** konfigūracija *nėra* naudojama darbo užsakymo planavimo metu.

> [!NOTE]
> Modulyje „Turto valdymas“ taip pat galite pasirinkti *pageidaujamus* priežiūros darbuotojus, kurie gali būti priskirti darbo užsakymams darbo užsakymo planavimo metu.

Kad galėtumėte nustatyti už priežiūrą atsakingus darbuotojus, turite nustatyti darbuotojų ir priežiūros darbuotojų grupes, kurias būtų galima pasirinkti. Informacijos apie tai, kaip nustatyti darbuotojus ir priežiūros darbuotojų grupes, rasite temoje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Už priežiūrą atsakingų darbuotojų nustatymas

1. Pasirinkite **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Visų pirma sukurkite numatytąjį už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupės konfigūraciją, kurioje nustatysite tik lauką **Už priežiūrą atsakingų darbuotojų grupė** ir (arba) lauką **Atsakingas darbuotojas**. Likusius laukus palikite tuščius. Ši numatytoji konfigūracija bus naudojama darbo užsakymų planavimo metu, jei nebus rasta jokia kita, konkrečiau darbo užsakymo turinį atitinkanti kombinacija.

    > [!NOTE]
    > Kuriant priežiūros užklausą, puslapyje **Visos priežiūros užklausos** aktyvavus galimybę pasirinkti už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupę, modulyje „Turto valdymas“ peržiūrimi visi už priežiūrą atsakingų darbuotojų įrašai, siekiant surasti galimą atitiktį. Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Prekyba** atitikties. Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipo variantas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipas** atitikties ir t.t. Kaip matote pagal puslapio išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti pačią konkrečiausią kombinaciją, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę (iš pradžių **Prekyba**, tada **Priežiūros užduočių tipo variantas**, tada **Priežiūros užduoties tipas**, tada **Priežiūros užduoties tipo kategorija**, tada **Funkcinė vietovė**, tada **Turtas** ir galiausiai **Turto tipas**). Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuriame šie septyni laukai yra tušti.

Paveikslėlyje pavaizduotas puslapio **Už priežiūrą atsakingi darbuotojai** pavyzdys.

![1 paveikslėlis](media/08-setup-for-requests.png)
