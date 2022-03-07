---
title: Ataskaitos kaip baigto publikuto žurnalo klaida
description: Kai registruojate žurnalą Skelbti baigtu, gaunate klaidos pranešimą, kuriame teigiama, kad užsakyto kiekio negalima sumažinti.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750935"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Ataskaitos kaip baigto publikuto žurnalo klaida

KB numeris: 4612891

## <a name="symptoms"></a>Požymiai

Kai registruojate **žurnalą Skelbti baigtu**, įvyksta klaida ir gaunate tokį klaidos pranešimą:

> Užsakyto kiekio mažinti negalima, nes nepakanka atvirų atsargų operacijų, kurių būsena Užsakyta. Prekės yra Nupirktos, Gautos arba Užregistruotos.

Ši klaida įvyksta tik tada, kai laukas **Klaidų kiekis** laukelis yra nustatytas ant pirmosios eiltuės **Pranešti apie baigtą** žurnale, o **Geros kokybės** laukelis yra nustatytas paskutinėje. Jei **Klaidos kiekis** laukelyje nustatytas paskutinėje eilutėje, klaidų nėra.

## <a name="resolution"></a>Skiriamoji geba

Norėdami išvengti šios klaidos, atidarykite **gamybos valdymo parametrų** puslapį ir tada **Bendra** skirtuke, nustatykite **Padidėjimas su klaidų kiekis** parinktį į *Taip*.
