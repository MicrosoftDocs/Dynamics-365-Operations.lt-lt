---
title: Variacijos skatinimas ir eksperimento užbaigimas
description: Šiame straipsnyje aprašoma, kaip skatina sėkmingą variaciją ir baigia anumentuoti Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942748"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variacijos skatinimas ir eksperimento užbaigimas

Šiame straipsnyje aprašoma, kaip skatina variacijų, kurios atliko geriausią rezultatą jūsų pabaigoje, ir kaip užbaigti pabaigą. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai įtraukti atskiruose straipsnius.

[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir užbaigimas.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

[Įvykdę eksperimentą](experimentation-run-monitor.md) ir surinkę pakankamai duomenų, kad nustatytumėte, kurią variaciją naudosite jūsų aktyvioje svetainėje, skatinsite variaciją ir užbaigsite eksperimentą.

## <a name="promote-a-variation"></a>Variacijos skatinimas
Norėdami nuspręsti, kuri variacija pateikė geriausius rezultatus, naudokite duomenis ir analizę, susijusius su trečiosios šalies paslaugos eksperimentu. Tada galite jį skatinti pakeisdami dabartinį aktyvios svetainės turinį laimėjusia variacija, kad ji būtų pasiekiama visiems jūsų svetainės vartotojams.

Norėdami skatinti laimėjusią variaciją, atlikite toliau pateiktus veiksmus. 

1. „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą.
1. Komandų juostoje pasirinkite **Užbaigti eksperimentą**.
1. Dialogo lange **Užbaigti eksperimentą** pasirinkite **Peržiūrėti eksperimento duomenis**. Atidaroma trečiosios šalies paslauga, kurioje galite patvirtinti metriką ir nustatyti, kuri variacija pateikė geriausius duomenis.
1. Dialogo lange **Užbaigti eksperimentą** pasirinkite laimėjusią variaciją ir pasirinkite **Pirmyn**.
1. Atidarykite trečiosios šalies paslaugą ir sustabdykite eksperimentą.
1. Svetainių daryklėje pasirinkite **Baigti**, norėdami perrašyti pradinį aktyvų puslapį ir publikuoti laimėjusią variaciją, kad jis būtų pasiekiama visiems jūsų svetainės vartotojams. 

> [!NOTE]
> Jei pasirinksite palikti dabartinį aktyvų puslapį ir nepublikuoti variacijos, pasirinkite **Publikuoti pradinį puslapį iš naujo**.

## <a name="delete-your-experiment"></a>Eksperimento naikinimas
Nors nėra būtina panaikinti baigtą eksperimentą „Commerce”, galite jį panaikinti, norėdami taupyti vietą arba išvalyti jūsų darbo sritį. 

Norėdami panaikinti užbaigtą "Commerce" svetainės generatoriaus seką, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą. 
    > [!NOTE]
    > Jei eksperimentas vis dar aktyvus, prieš tęsdami, sustabdykite eksperimentą trečiosios šalies paslaugoje.
1. Norėdami pašalinti variacijos turinį iš aktyvios svetainės, komandų juostoje pasirinkite **Panaikinti publikavimą**.
1. Norėdami panaikinti eksperimentą, pasirinkite **Naikinti**.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento vykdymas ir stebėjimas](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
