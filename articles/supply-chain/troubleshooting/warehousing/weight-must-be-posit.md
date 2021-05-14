---
title: Svoris turi būti teigiamas
description: Svoris turi būti teigiamas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924308"
---
# <a name="weight-must-be-positive"></a>Svoris turi būti teigiamas

Klaidos kodas: WeightMustBePositive

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Svoris turi būti teigiamas.

## <a name="cause"></a>Priežastis

Lauke **Bruto** svoris nustatytas *0* (nulis) arba neigiama vertė.

## <a name="resolution"></a>Skiriamoji geba

Norėdami nustatyti svorį, atlikite vieną iš toliau nurodytų veiksmų.

- Lauke **Bruto** svoris nustatykite vertę. Tada pasirinkite vienetą iš išplečiamojo sąrašo.
- Pasirinkite **Gauti sistemos svorį, kad būtų skaičiuojama** bruto **svorio** vertė.
