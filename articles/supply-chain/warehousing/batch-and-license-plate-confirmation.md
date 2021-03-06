---
title: Paketo ir numerio lentelės patvirtinimas
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti paketo ir numerio lentelės patvirtinimą iš mobiliojo įrenginio.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c588e6ed11d275b75133e2824f3d385048050426
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837542"
---
# <a name="batch-and-license-plate-confirmation"></a>Paketo ir numerio lentelės patvirtinimas

[!include [banner](../includes/banner.md)]

Atlikdami paketo patvirtinimą galite patvirtinti kad iš mobiliojo įrenginio paimamas teisingas paketas. Pradiniame tik *Virš paketo\[vieta\]* elementų darbo paėmime, kai „virš paketo” reiškia, kad paketas yra aukščiau nei vieta ieškos hierarchijoje, turite patikrinti, ar paimtas paketas atitinka darbo eilutėje nurodytą paketą.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
