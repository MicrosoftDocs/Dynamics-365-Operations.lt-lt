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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776781"
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
