---
title: Patobulintas pagal paketą sekamų prekių tvarkymas
description: Šioje temoje aprašoma, kaip patobulintas pagal paketą sekamų prekių paketų tvarkymas atliekant procesą Mažmeninės prekybos išrašo registravimas.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617394"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Patobulintas pagal paketą sekamų prekių tvarkymas

„Microsoft Dynamics 365 for Retail“ elektroniniame kasos aparate (EKA) parduodant pagal paketą sekamas prekes jų paketų numerių užfiksuoti negalima. Tačiau, naudojant tam tikras konfigūracijas, kai pardavimai būstinėje registruojami per klientų užsakymus arba registruojant išrašus, „Microsoft Dynamics“ sistema tikisi, kad egzistuoja galiojantys pagal paketą sekamų prekių paketų numeriai ir kad jie bus naudojami atliekant SF išrašymo procesą.

Jei egzistuoja galiojantys produktų paketų numeriai, jie naudojami atliekant klientų užsakymų SF išrašymo procesą ir pardavimo užsakymų SF išrašymo procesą, kai registruojami išrašai. Kitu atveju atliekant klientų užsakymų SF išrašymo procesą negalima registruoti, o EKA vartotojas gauna klaidos pranešimą. Išrašų registravimas tada tampa klaidos būsenos. Ši klaidos būsena atsiranda net tada, kai įjungtos produktų neigiamos atsargos.

„Microsoft Dynamics for Retail“ 10.0.4 ir naujesnėse versijose atlikti patobulinimai padeda užtikrinti, kad, kai yra įjungtos pagal paketą sekamų prekių neigiamos atsargos, toms prekėms klientų užsakymų SF išrašymas ir pardavimo užsakymų SF išrašymas registruojant išrašus nėra blokuojamas, jei atsargos yra 0 (nulis) arba nėra paketo numerio. Kai nėra paketų numerių, naujoji funkcija pardavimo eilutėms naudoja numatytąjį paketo ID.

Norėdami nustatyti numatytąjį paketo ID, naudojamą klientų užsakymuose, puslapio **Mažmeninės prekybos parametrai** skirtuko **Klientų užsakymai** „FastTab“ konteineryje **Užsakymas** nustatykite lauką **Numatytasis paketo ID**.

Norėdami nustatyti numatytąjį paketo ID, kuris yra naudojamas, kai registruojant išrašus išrašomos pardavimo užsakymų SF, puslapio **Mažmeninės prekybos parametrai** skirtuko **Registravimas** „FastTab“ konteineryje **Atsargų atnaujinimas** nustatykite lauką **Numatytasis paketo ID**.

> [!NOTE]
> Šią funkciją galima naudoti tik tada, kai konkrečiam parduotuvės sandėliui ir prekėms įjungtas pažangus sandėliavimas. Naujesniame leidime ši funkcija taip pat bus palaikoma situacijose, kai pažangus sandėlių valdymas nenaudojamas.
