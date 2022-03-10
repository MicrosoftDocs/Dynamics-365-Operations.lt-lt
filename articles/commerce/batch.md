---
title: Patobulintas pagal paketą sekamų prekių tvarkymas
description: Šioje temoje aprašomas patobulintas pagal paketą sekamų priekių tvarkymas atliekant išrašo registravimo procesą „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485788"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Patobulintas pagal paketą sekamų prekių tvarkymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomas patobulintas pagal paketą sekamų priekių tvarkymas atliekant išrašo registravimo procesą „Microsoft Dynamics 365 Commerce“.

„Dynamics 365 Commerce“ elektroniniame kasos aparate (EKA) parduodant pagal paketą sekamas prekes jų paketų numerių užfiksuoti negalima. Tačiau, naudojant tam tikras konfigūracijas, kai pardavimai „Commerce“ būstinėje registruojami per klientų užsakymus arba registruojant išrašus, „Commerce“ tikisi, kad egzistuoja galiojantys pagal paketą sekamų prekių paketų numeriai ir kad jie bus naudojami atliekant SF išrašymo procesą.

Jei egzistuoja galiojantys produktų paketų numeriai, jie naudojami atliekant tiek klientų užsakymų SF išrašymo procesą, tiek pardavimo užsakymų SF išrašymo procesą, kai registruojami išrašai. Jei nėra galiojančių produktų paketų numerių, atliekant klientų užsakymų SF išrašymo procesą registruoti negalima ir EKA vartotojas gauna klaidos pranešimą. Išrašų registravimas tada tampa klaidos būsenos, net jei įjungtos produktų neigiamos atsargos.

„Commerce“ atlikti patobulinimai padeda užtikrinti, kad, kai yra įjungtos pagal paketą sekamų prekių neigiamos atsargos, toms prekėms klientų užsakymų SF išrašymas ir pardavimo užsakymų SF išrašymas registruojant išrašus nebūtų blokuojamas, jei atsargos yra 0 (nulis) arba nėra paketo numerio. Kai nėra paketų numerių, patobulinta funkcija pardavimo eilutėms naudoja numatytąjį paketo ID.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Numatytojo paketo ID, naudojamo kliento užsakymams, nustatymas

Norėdami nustatyti numatytojo paketo ID, naudojamo kliento užsakymams, atlikite toliau pateikiamus veiksmus.

1. „Commerce“ būstinėje eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai**.
1. Skirtuke **Kliento užsakymai** „FastTab“ **Užsakymas** įveskite reikšmę lauke **Numatytasis paketo ID**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Numatytojo paketo ID, kuris yra naudojamas, kai registruojant išrašus išrašomos pardavimo užsakymų SF, nustatymas

Norėdami nustatyti numatytojo paketo ID, kuris yra naudojamas, kai registruojant išrašus išrašomos pardavimo užsakymų SF, atlikite toliau nurodytus veiksmus.

1. „Commerce“ būstinėje eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> „Commerce“ parametrai**.
1. Skirtuke **Registravimas** „FastTab“ **Atsargų atnaujinimas** įveskite reikšmę lauke **Numatytasis paketo ID**.

> [!NOTE]
> - Numatytojo paketo ID funkciją galima naudoti tik tada, kai konkrečiam parduotuvės sandėliui ir prekėms įjungtas pažangus sandėliavimas. Būsimame leidime numatytojo paketo ID funkcija taip pat bus palaikoma situacijose, kai pažangus sandėlių valdymas neįjungtas.
> - „Commerce” 10.0.5 versijos leidime įvestas patobulinto pagal paketą sekamų prekių tvarkymo palaikymas atliekant neišplėstinių sandėlių valdymo scenarijų išrašų tvarkymą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
