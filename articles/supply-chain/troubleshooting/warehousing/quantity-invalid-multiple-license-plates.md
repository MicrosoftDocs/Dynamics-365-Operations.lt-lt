---
title: Kiekis netinkamas paėmimo darbui su keliais LPs
description: Kiekis negalioja ea vienetui, kai yra paėmimo darbas turintis keletą licencijos lentelių vienoje vietoje. Patikrinkite, ar šie laukai teisingi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477051"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Kiekis netinkamas, kai vienoje vietoje yra paėmimo darbas su keliais LPs

## <a name="symptoms"></a>Požymiai

Kiekis negalioja ea vienetui, kai yra paėmimo darbas turintis keletą licencijos lentelių vienoje vietoje *ea* kiekio ir gaunate tokį klaidos pranešimą:

> Šis kiekis netinka pasirinktam vienetui 1%.

## <a name="resolution"></a>Sprendimas

Patikrinkite, ar **Vieneto sekos grupės ID** ir **Vieneto pavertimų** laukeliai išleistame produkte ar produkto variante yra nustatyti tinkamai.

Atkreipkite dėmesį, kad klaidos pranešimas buvo pagerintas versijoje 10.0.15 siekiant rodyti tikėtiną kiekį (žr. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Naujas klaidos pranešimas:

> Netinkamas kiekis. Tikėtina %1 %2.
