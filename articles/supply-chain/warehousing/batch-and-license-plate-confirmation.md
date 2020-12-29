---
title: Paketo ir numerio lentelės patvirtinimas
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti paketo ir numerio lentelės patvirtinimą iš mobiliojo įrenginio.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a953b677b1188750241772d7ae966a1dba77b92e
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514307"
---
# <a name="batch-and-license-plate-confirmation"></a>Paketo ir numerio lentelės patvirtinimas

[!include [banner](../includes/banner.md)]

Atlikdami paketo patvirtinimą galite patvirtinti kad iš mobiliojo įrenginio paimamas teisingas paketas. Taikoma tik pradiniam virš paketo esančių elementų darbo paėmimui, kai parinktimi virš paketo nurodoma, kad ieškos hierarchijoje paketo intervalas yra aukščiau negu vietos intervalas, ir turite patikrinti, ar paimtas paketas atitinka darbo eilutėje nurodytą paketą.

Naudodami numerio lentelės patvirtinimą galite patvirtinti, kad iš mobiliojo įrenginio paimta teisinga numerio lentelė. Rinkdamiesi darbą iš etapo vietos turite patikrinti, ar pasirinkta numerio lentelė atitinka su darbu susietą numerio lentelę. Jei darbas pradedamas nuskaitant numerio lentelę, šis patvirtinimo veiksmas praleidžiamas.

## <a name="where-it-applies"></a>Kai taikoma

Patvirtinimas taikomas šiais atvejais:

- Paketo patvirtinimas taikomas pradiniam virš paketo esančių elementų darbo paėmimui.
- Numerio lentelės patvirtinimas taikomas paėmimams iš etapo vietos.

> [!IMPORTANT]
> Papildymas nėra palaikomoas licencijos lentelės patvirtinimui. Atliekand papildymo darbą nėra sukuriamas joks lentelės patvirtinimo žingsnis.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Paketo ir numerio lentelės patvirtinimo nustatymas

Paketo ir numerio lentelės patvirtinimą galite konfigūruoti pagal mobiliojo įrenginio meniu elementus.

1. Mobiliojo įrenginio meniu elementuose įveskite darbo patvirtinimo sąranką.  
1. Pasirinkite paketo arba numerio lentelės patvirtinimo parinktį. Abi parinktys taikomos darbo tipo paėmimams, kuriems neįgalinta automatinio patvirtinimo funkcija.  
