---
title: Patobulintas pagal paketą sekamų prekių tvarkymas
description: Šioje temoje aprašoma, kaip patobulintas pagal paketą sekamų prekių paketų tvarkymas atliekant išrašo registravimo procesą.
author: josaw1
ms.date: 11/04/2019
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
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799714"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Patobulintas pagal paketą sekamų prekių tvarkymas


[!include [banner](includes/banner.md)]


Elektroniniame kasos aparate (EKA) parduodant pagal paketą sekamas prekes jų paketų numerių užfiksuoti negalima. Tačiau, naudojant tam tikras konfigūracijas, kai pardavimai būstinėje registruojami per klientų užsakymus arba registruojant išrašus, „Microsoft Dynamics“ sistema tikisi, kad egzistuoja galiojantys pagal paketą sekamų prekių paketų numeriai ir kad jie bus naudojami atliekant SF išrašymo procesą.

Jei egzistuoja galiojantys produktų paketų numeriai, jie naudojami atliekant klientų užsakymų SF išrašymo procesą ir pardavimo užsakymų SF išrašymo procesą, kai registruojami išrašai. Kitu atveju atliekant klientų užsakymų SF išrašymo procesą negalima registruoti, o EKA vartotojas gauna klaidos pranešimą. Išrašų registravimas tada tampa klaidos būsenos. Ši klaidos būsena atsiranda net tada, kai įjungtos produktų neigiamos atsargos.

„Retail“ 10.0.4 ir naujesnėse versijose atlikti patobulinimai padeda užtikrinti, kad, kai yra įjungtos pagal paketą sekamų prekių neigiamos atsargos, toms prekėms klientų užsakymų SF išrašymas ir pardavimo užsakymų SF išrašymas registruojant išrašus nebūtų blokuojamas, jei atsargos yra 0 (nulis) arba nėra paketo numerio. Kai nėra paketų numerių, naujoji funkcija pardavimo eilutėms naudoja numatytąjį paketo ID.

Norėdami nustatyti numatytąjį paketo ID, naudojamą klientų užsakymuose, puslapio **Prekybos parametrai** skirtuko **Klientų užsakymai** „FastTab“ konteineryje **Užsakymas** nustatykite lauką **Numatytasis paketo ID**.

Norėdami nustatyti numatytąjį paketo ID, kuris yra naudojamas, kai registruojant išrašus išrašomos pardavimo užsakymų sąskaitos faktūros, puslapio **Prekybos parametrai** skirtuko **Registravimas** „FastTab“ konteineryje **Atsargų atnaujinimas** nustatykite lauką **Numatytasis paketo ID**.

> [!NOTE]
> Šią funkciją galima naudoti tik tada, kai konkrečiam parduotuvės sandėliui ir prekėms įjungtas pažangus sandėliavimas. Naujesniame leidime ši funkcija taip pat bus palaikoma situacijose, kai pažangus sandėlių valdymas nenaudojamas.

> [!NOTE]
> „Retail” 10.0.5 versijoje įvestas patobulinto pagal paketą sekamų prekių tvarkymo palaikymas atliekant neišplėstinių sandėlių valdymo scenarijų išrašų tvarkymą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]