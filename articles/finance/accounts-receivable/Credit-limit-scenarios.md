---
title: Kredito limito scenarijai
description: Šiame straipsnyje aprašoma, kaip tikrinamas kliento kredito limitas, kai klientas priklauso klientų kredito limitų grupei.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130275"
---
# <a name="credit-limit-scenarios"></a>Kredito limito scenarijai

Kredito valdymo srityje kredito limitas gali būti priskirtas klientams kliento lygiu. Kiekvienas klientas gali būti priskirtas *kliento kredito limito grupei*, o kiekviena grupė turi kredito limitą. Todėl kredito limitą galima priskirti ir klientams grupės lygyje. Visi klientai, priskirti tai pačiai klientų kredito grupei, turi tą patį kredito limitą.

Apskritai, grupės kredito limitai tikrinami prieš atskirus kredito limitus. Atskiras kredito limitas ne visada panaikina grupės kredito limitą.

Šiame straipsnyje aprašomi penki scenarijai, susiję su kliento kredito grupėmis ir atskirais kredito limitais.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Klientų grupės kredito limitas didesnis už atskirą kredito limitą

Pavyzdžiui, klientui nustatytas individualus kliento kredito $10,000. Klientas priskiriamas klientų kredito grupei, o grupės kredito limitas $15,000. Šiuo atveju kliento "veiksmingas kredito limitas" yra $10,000, nes ši suma yra mažesnė nei grupės limitas. Blokavimo taisyklės pirmiausia patikrinkite grupės limitą. Tada jos patikrina atskirą limitą. Bet koks pardavimo užsakymas$10,000 šis kiekis bus užblokuotas.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Atskiras kredito limitas didesnis už klientų grupės kredito limitą

Pavyzdžiui, klientas turi atskirą kredito limitą arba $20,000. Klientas priskiriamas klientų kredito grupei, o grupės kredito limitas $15,000. Šiuo atveju galiojantis kliento kredito limitas yra $15,000, kadangi blokavimo taisyklės visada pirmiausia patikrina grupės limitą. Visi daugiau nei $15,000 pardavimo užsakymai bus užblokuoti.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Nustatytas atskiras kredito limitas 0,00, o privalomas kredito limitas nustatytas kaip Taip

Jei klientui nustatytas individualus kredito limitas **, nustatytas 0,00**, **o parinktis Privalomas kredito limitas** **yra nustatyta kaip Taip**, galioja toks kliento kredito $0.00, net jei klientas priskirtas klientų kredito grupei. Tokiu būdu klientas gali būti grupės dalis, tačiau visuose užsakymuose bus kredito valdymas.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Atskiras kredito limitas nustatytas kaip 0,00, o neribotas kredito limitas nustatytas kaip Taip

Jei klientui nustatytas individualus kredito limitas **, nustatytas 0,00**, **bet nustatyta parinktis Neribotas kredito limitas** **yra Nustatyta Taip**, klientas turės neribotą kreditą, net jei jis priskirtas klientų kredito grupei.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Nustatytas atskiras kredito limitas 0,00, o klientas yra klientų kredito grupės dalis

Pavyzdžiui, klientui nustatytas individualus kredito limitas **, nustatytas 0,00**,**·** **parinktis Neribotas kreditas yra nustatyta kaip Ne**, **o privaloma kredito limito** parinktis nustatyta kaip **Ne.** Klientas priskiriamas klientų kredito grupei, o grupės kredito limitas $15,000. Šiuo atveju veiksmingas kliento kredito limitas yra grupės, arba grupės $15,000. Todėl bet kokie pardavimo užsakymai, esantys ta suma, bus užblokuoti. Taip galima valdyti kredito limitą klientų kredito grupės lygyje, o ne atskirų klientų lygyje. Visi tai pačiai grupei priskirti klientai turi tą patį kredito limitą.
