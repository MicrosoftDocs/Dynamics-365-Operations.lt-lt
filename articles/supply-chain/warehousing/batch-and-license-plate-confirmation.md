---
title: Paketo ir numerio lentelės patvirtinimas
description: Šiame straipsnyje aprašoma, kaip nustatyti ir taikyti paketo ir numerio lentelės patvirtinimą iš mobiliojo įrenginio.
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
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903730"
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
