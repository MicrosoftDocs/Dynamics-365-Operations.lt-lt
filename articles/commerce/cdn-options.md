---
title: Turinio pristatymo tinklo diegimo parinktys
description: Šiame straipsnyje peržiūrimos skirtingos turinio pristatymo tinklo (CDN) diegimo parinktys, kurias galima naudoti su Microsoft Dynamics 365 Commerce aplinka. Šios pasirinktys apima vietinius „Commerce“ pateiktus „Azure Front Door“ egzempliorius ir „Azure Front Door“ egzempliorius, kurie priklauso klientams.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a63751d42ab98610904191f1c09794b2311b0189
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884422"
---
# <a name="content-delivery-network-implementation-options"></a>Turinio pristatymo tinklo diegimo parinktys

[!include [banner](includes/banner.md)]

Šiame straipsnyje peržiūrimos skirtingos turinio pristatymo tinklo (CDN) diegimo parinktys, kurias galima naudoti su Microsoft Dynamics 365 Commerce aplinka. Šios pasirinktys apima vietinius „Commerce“ pateiktus „Azure Front Door“ egzempliorius ir „Azure Front Door“ egzempliorius, kurie priklauso klientams.

„Commerce“ klientai turi kelias parinktis, kai jie atsižvelgia į tai, kurią CDN paslaugą naudoti su savo „Commerce“ aplinka. „Commerce“ išleidžiama su pagrindiniu „Azure Front Door“ palaikymu, kuris apima pagrindinius išteklių nuomos ir pasirinktinio domeno reikalavimus. Įmonėms, kurios nori daugiau kontroliuoti ir trokšta konkretesnių saugos gebėjimų, pvz., interneto programos užkardos (WAF), geriausias pasirinkimas – naudoti kliento „Azure Front Door“ egzempliorių arba išorinę CDN tarnybą.

„Commerce“ aplinkose gali būti naudojamos šios trys CDN diegimo parinktys:

- „Commerce“ pateiktas „Azure Front Door” egzempliorius
- Kliento „Azure Front Door“ egzempliorius (kad būtų padidinta kontrolė ir papildomos saugos funkcijos)
- Išorinė CDN tarnyba

Visos trys CDN diegimo parinktys teikia tik dinaminį HTML turinį iš pasirenkamų domenų. „Commerce“ automatiškai tvarko visus „JavaScript“ pakopinio stiliaus sąrašus (CSS), vaizdus, vaizdo įrašus ir kitą statinį turinį, naudodami „Microsoft“ valdomus CDN. Jūsų parinktis nustato veikimo pajėgumus, valdymo pajėgumus ir papildomas galimas saugos galimybes.

Toliau esančiame paveikslėlyje pateikiama „Commerce“ architektūros apžvalga.

![„Commerce“ architektūros apžvalga.](media/Commerce_CDN-Option_ComparisonModels.png)

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti „Azure Front Door“ egzempliorių savo „Commerce“ svetainei, žr. [Pridėti CDN palaikymą](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>„Commerce“ pateikto „Azure Front Door“ egzemplioriaus naudojimas

Toliau esančioje lentelėje pateikiami privalumai ir trūkumai, susiję su tuo, kaip naudoti „Commerce“ pateiktą „Azure Front Door“ egzempliorių galiniams turinio punktams valdyti.

| Privalumai | Trūkumai |
|------|------|
| <ul><li>Egzempliorius įtraukiamas į „Commerce“ kainą.</li><li>Egzempliorių valdo „Commerce“ komanda, todėl reikia mažiau priežiūros reikia ir yra bendrai naudojamų nustatymo veiksmų.</li><li>„Azure“ palaikoma infrastruktūra yra keičiamo dydžio, saugi ir patikima.</li><li>Saugiųjų jungčių lygmens (SSL) sertifikatui reikia vienkartinio nustatymo ir jis atnaujinamas automatiškai.</li><li>„Commerce“ komanda stebi, ar egzemplioriuje nėra klaidų ir anomalijų.</li></ul> | <ul><li>WAF nėra palaikomas.</li><li>Nėra jokių konkrečių pritaikymų ar nustatymų koregavimų.</li><li>Egzempliorius priklauso nuo „Commerce“ komandos atnaujinimų ar pakeitimų.</li><li>Atskiras „Azure Front Door“ egzempliorius reikalingas „Apex“ domenams, o „Apex“ domenams integruoti su „Azure“ DNS reikalingas papildomas darbas.</li><li>Klientui nepateikiama jokia telemetrijos informacija apie atsakymus per sekundę (RPS) ar klaidų dažnį.</li></ul> |

Šioje iliustracijoje vaizduojama „Commerce“ pateikiamo „Azure Front Door“ egzemplioriaus architektūra.

![„Commerce“ pateiktas „Azure Front Door“ egzempliorius.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Kliento „Azure Front Door“ egzemplioriaus naudojimas

Toliau esančioje lentelėje pateikiami privalumai ir trūkumai, susiję su tuo, kaip naudoti kliento „Azure Front Door“ egzempliorių galiniams turinio punktams valdyti.

| Privalumai | Trūkumai |
|------|------|
| <ul><li>Sąranką valdyti saugu ir paprasta.</li><li>„Azure“ palaikoma infrastruktūra yra keičiamo dydžio, saugi ir patikima.</li><li>Egzempliorius leidžia integruoti WAF ir naudoti detalios taisyklės valdiklius tikslesnei saugai, pritaikytai konkrečiai jūsų svetainei.</li><li>Egzempliorius leidžia tiksliau valdyti SSL sertifikatus (ir priklausantiems klientui, ir valdomiems „Azure Front Door–Managed“) bei domeno susiejimą.</li><li>Egzempliorius siūlo „Apex“ domeno sprendimą, jei jis tiesiogiai susiejamas su „Azure“ DNS.</li><li>Pateikiama telemetrija ir įspėjimai.</li><li>SSL sertifikatui reikia vienkartinio nustatymo ir jis atnaujinamas automatiškai.</li></ul> | <ul><li>Egzempliorius valdomas savarankiškai.</li><li>Būtina nustatyti pradines žinias.</li></ul> |

Toliau pateiktoje iliustracijoje rodoma „Commerce“ infrastruktūra, kuri apima kliento „Azure Front Door“ egzempliorių.

![„Commerce“ infrastruktūra, kuri apima kliento „Azure Front Door“ egzempliorių.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Išorinės CDN tarnybos naudojimas

Šioje lentelėje pateikiami išorinės CDN tarnybos naudojimo, siekiant valdyti turinio galinius punktus, privalumai ir trūkumai.

| Privalumai | Trūkumai |
|------|------|
| <ul><li>Ši parinktis naudinga, kai esamas domenas jau yra išoriniame CDN.</li><li>WAF: Priklauso nuo išorinio teikėjo.</li></ul> | <ul><li>Reikalinga atskira sutartis ir papildomas įkainojimas.</li><li>SSL gali turėti papildomų išlaidų.</li><li>Kadangi paslauga yra atskira nuo „Azure“ debesies struktūros, būtina valdyti papildomą infrastruktūrą.</li><li>Paslauga gali reikalauti ilgalaikių investicijų į galinį punktą ir saugos nustatymo.</li><li>Paslauga valdoma savarankiškai.</li><li>Paslauga stebima savarankiškai.</li></ul> |

Šioje iliustracijoje vaizduojama „Commerce“ infrastruktūra, kurioje yra išorinė CDN paslauga.

![„Commerce“ infrastruktūra, kurioje yra išorinė CDN paslauga.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio pateikimo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)
