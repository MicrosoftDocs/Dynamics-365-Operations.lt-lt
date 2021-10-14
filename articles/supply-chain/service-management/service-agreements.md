---
title: Aptarnavimo sutarčių kūrimo ir nustatymo apžvalga
description: Aptarnavimo sutartys leidžia nustatyti išteklius, kurie bus naudojami įprasto aptarnavimo vizito metu, ir kaip už šiuos išteklius bus išrašoma sąskaita klientui.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54a3612d11976c86ec1412bb0a599c772d7edeb5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573254"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Aptarnavimo sutarčių kūrimo ir nustatymo apžvalga

[!include [banner](../includes/banner.md)]

Aptarnavimo sutartys leidžia nustatyti išteklius, kurie bus naudojami įprasto aptarnavimo vizito metu, ir kaip už šiuos išteklius bus išrašoma sąskaita klientui.

Kiekviena aptarnavimo sutartis yra pridėta prie projekto, kurio operacijos registruojamos ir už jas išrašomos sąskaitos. Tačiau sąskaitas už aptarnavimo užsakymo operacijas galima išrašyti ir tiesiogiai per projektą – ir tam nereikės iš pradžių prijungti aptarnavimo užsakymo prie aptarnavimo sutarties. Galite nuspręsti taip daryti, jei aptarnavimo užsakymas yra sukurtas tik vienkartiniam aptarnavimo vizitui, o poreikis greitai apdoroti aptarnavimo operacijas yra svarbesnis už poreikį prižiūrėti, kad aptarnavimo sutarties informacija apie klientą per tam tikrą laikotarpį būtų išsami.

## <a name="service-agreement"></a>Aptarnavimo sutartis

Kiekvienoje aptarnavimo sutartyje reikia nustatyti projektą, aptarnavimo sutarties ID ir aptarnavimo sutarčių grupę. Aptarnavimo sutarčių grupė gali būti naudojama aptarnavimo sutartims rūšiuoti ir organizuoti.

Aptarnavimo sutarties antraštėje yra parametrai, taikomi visoms pridėtoms sutarties eilutėms:

-  Ar aptarnavimo sutartis yra sustabdyta. Jei aptarnavimo sutartis yra sustabdyta, iš jos negalima generuoti aptarnavimo užsakymų.
-  Aptarnavimo sutarties trukmė.
-  Kaip aptarnavimo užsakymo eilutės jungiamos į aptarnavimo užsakymus.
-  Ar aptarnavimo sutartis yra šablonas.

Aptarnavimo sutarties antraštėje taip pat galite nustatyti visus aptarnavimo objektus ir aptarnavimo užduotis, kuriuos bus galima naudoti su aptarnavimo sutartimi, įvedę konkrečias aptarnavimo užduotis ar aptarnavimo objektus, kurie turi būti pridėti prie įvairių sutarties eilučių.

Iš aptarnavimo sutarties antraštės taip pat galima nukopijuoti aptarnavimo sutarties eilutes arba aptarnavimo šablono eilutes į dabartinę aptarnavimo sutartį.

Galima laikinai sustabdyti aptarnavimo sutartis ir sustabdyti atskiras aptarnavimo sutarties eilutes.

Aptarnavimo sutartyje pažymėję žymės langelį **Laikinai sustabdyta**, negalėsite:

-    Iš aptarnavimo sutarties automatiškai arba rankiniu būdu sukurti aptarnavimo užsakymų.

Aptarnavimo sutarties eilutėje pažymėję žymės langelį **Sustabdyta**, negalėsite:

-    Iš aptarnavimo sutarties eilutės automatiškai arba rankiniu būdu sukurti aptarnavimo užsakymų.
-    Nukopijuoti aptarnavimo sutarties eilutę į kitą aptarnavimo sutartį arba aptarnavimo užsakymą.


> [!NOTE]
> Jei aptarnavimo sutartis laikinai sustabdoma, visos pridėtos eilutės sustabdomos, neatsižvelgiant į jų būseną.

## <a name="service-agreement-lines"></a>Aptarnavimo sutarties eilutės

Kiekviena aptarnavimo sutarties eilutė išsamiai aprašo siūlomo aptarnavimo darbo turinį. Eilutėse yra tokie parametrai:

-  Operacijos tipas ir operacijos tipo aprašymas.
-  Aptarnavimo darbą atliekantis darbuotojas.
-  Objektai, kuriems turi būti atliekamas aptarnavimas pagal aptarnavimo sutartį.
-  Užregistruojamas dažnumas, kuriuo atliekamas darbas, ir užregistruojamos susijusios prekės, išlaidų ir mokesčių operacijos.
-  Laiko langas, per kurį aptarnavimo užsakymo eilutės gali būti sugrupuotos į aptarnavimo užsakymą.
-  Aptarnavimo užduotys, naudojamos sutarties eilučių rinkiniams į darbo užduotis grupuoti ir pateikti aptarnavimo technikams bei klientams apibendrintą informaciją, kokia aptarnavimo užduotis turi būti atlikta.
-  Ar eilutė sustabdyta. Jei eilutė sustabdyta, negalima sukurti aptarnavimo užsakymų tai atskirai eilutei.
-  Projekto parametrai, pvz., kategorija ir eilutės ypatybė.

## <a name="related-topics"></a>Susijusios temos

[Aptarnavimo sutarčių kūrimas](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]