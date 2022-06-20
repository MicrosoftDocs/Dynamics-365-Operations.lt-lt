---
title: Atsakingi priežiūros darbuotojai
description: Šiame straipsnyje paaiškinama, kaip nustatyti atsakingo priežiūros darbuotojus turto valdymo dalyje.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9535be3161253e88083b5add7ac55c12364aa383
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875598"
---
# <a name="responsible-maintenance-workers"></a>Už priežiūrą atsakingi darbuotojai

[!include [banner](../../includes/banner.md)]

 

Už priežiūrą atsakingi darbuotojai gali būti susiję su turto tipais, turtu, funkcinėmis vietovėmis, priežiūros užduoties tipo kategorijomis, priežiūros užduočių tipais, priežiūros užduoties tipo variantais ir prekyba. Jie gali būti naudojami darbo užsakymuose ir priežiūros užklausose, siekiant nurodyti nuostatą, kurie priežiūros darbuotojai turėtų būti atsakingi už darbo užsakymą. (Tačiau šie techninės priežiūros darbuotojai nebūtinai yra tie patys darbuotojai, kuriems numatyta atlikti darbų užsakymą.) Šios funkcijos naudojimas yra neprivalomas. Pavyzdžiui, ji gali būti naudojama norint pasirinkti atsakingus darbuotojus arba darbuotojų grupes konkretiems darbo tipams arba darbo sritims.

Darbo užsakymo ciklo arba priežiūros užklausos ciklo metu, už priežiūrą atsakingi darbuotojai gali būti keičiami arba atnaujinami. Šis pakeitimas arba atnaujinimas gali būti susijęs, pavyzdžiui, su priežiūros užklausos ciklo būsenos arba darbo užsakymo ciklo būsenos pasikeitimu.

Puslapio **Už priežiūrą atsakingi darbuotojai** konfigūracija *nėra* naudojama darbo užsakymo planavimo metu.

> [!NOTE]
> Modulyje „Turto valdymas“ taip pat galite pasirinkti *pageidaujamus* priežiūros darbuotojus, kurie gali būti priskirti darbo užsakymams darbo užsakymo planavimo metu.

Kad galėtumėte nustatyti už priežiūrą atsakingus darbuotojus, turite nustatyti darbuotojų ir priežiūros darbuotojų grupes, kurias būtų galima pasirinkti. Informacijos apie tai, kaip nustatyti darbuotojus ir priežiūros darbuotojų grupes, rasite temoje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Už priežiūrą atsakingų darbuotojų nustatymas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Atsakingi priežiūros darbuotojai**.
2. Pasirinkite **Naujas** pranešimui sukurti.
3. Visų pirma sukurkite numatytąjį už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupės konfigūraciją, kurioje nustatysite tik lauką **Už priežiūrą atsakingų darbuotojų grupė** ir (arba) lauką **Atsakingas darbuotojas**. Likusius laukus palikite tuščius. Ši numatytoji konfigūracija bus naudojama darbo užsakymų planavimo metu, jei nebus rasta jokia kita, konkrečiau darbo užsakymo turinį atitinkanti kombinacija.

    > [!NOTE]
    > Kuriant priežiūros užklausą, puslapyje **Visos priežiūros užklausos** aktyvavus galimybę pasirinkti už priežiūrą atsakingą darbuotoją arba už priežiūrą atsakingų darbuotojų grupę, modulyje „Turto valdymas“ peržiūrimi visi už priežiūrą atsakingų darbuotojų įrašai, siekiant surasti galimą atitiktį. Jis visada pirmiausiai tikrina konkrečiausius derinius. Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Prekyba** atitikties. Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipo variantas** atitikties. Jei atitiktis nerasta, ieškoma lauko **Priežiūros užduoties tipas** atitikties ir t.t. Kaip matote pagal puslapio išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti pačią konkrečiausią kombinaciją, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę (iš pradžių **Prekyba**, tada **Priežiūros užduočių tipo variantas**, tada **Priežiūros užduoties tipas**, tada **Priežiūros užduoties tipo kategorija**, tada **Funkcinė vietovė**, tada **Turtas** ir galiausiai **Turto tipas**). Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuriame šie septyni laukai yra tušti.

Paveikslėlyje pavaizduotas puslapio **Už priežiūrą atsakingi darbuotojai** pavyzdys.

![Už priežiūrą atsakingų darbuotojų puslapis.](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]