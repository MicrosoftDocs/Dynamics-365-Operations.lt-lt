---
title: Variacijos skatinimas ir eksperimento užbaigimas
description: Šioje temoje aprašoma, kaip skatinti sėkmingą variaciją ir užbaigti eksperimentą „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
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
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930248"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variacijos skatinimas ir eksperimento užbaigimas

Šioje temoje aprašoma, kaip skatinti variacijas, pateikusias geriausius rezultatus jūsų eksperimento metu, ir kaip užbaigti eksperimentą. Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose.

[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir užbaigimas](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

[Įvykdę eksperimentą](experimentation-run-monitor.md) ir surinkę pakankamai duomenų, kad nustatytumėte, kurią variaciją naudosite jūsų aktyvioje svetainėje, skatinsite variaciją ir užbaigsite eksperimentą.

## <a name="promote-a-variation"></a>Variacijos skatinimas
Norėdami nuspręsti, kuri variacija pateikė geriausius rezultatus, naudokite duomenis ir analizę, susijusius su trečiosios šalies paslaugos eksperimentu. Norėdami pakeisti dabartinį aktyvios svetainės turinį laimėjusia variacija, kad ji būtų pasiekiama visiems jūsų svetainės vartotojams, atlikite toliau pateiktus veiksmus. 

1. Eikite į svetainių daryklės skirtuką **Eksperimentai** ir pasirinkite eksperimentą.
1. Viršutinėje juostoje pasirinkite **Užbaigti eksperimentą**.
1. Dialogo meniu **Užbaigti eksperimentą** pasirinkite **Peržiūrėti eksperimento duomenis**. Atidaroma trečiosios šalies paslauga, kurioje galite patvirtinti metriką ir nustatyti, kuri variacija pateikė geriausius duomenis.
1. Svetainių daryklės dialogo meniu **Užbaigti eksperimentą** pasirinkite laimėjusią variaciją ir pasirinkite **Pirmyn**.
1. Atidarykite trečiosios šalies paslaugą ir sustabdykite eksperimentą.
1. Svetainių daryklėje pasirinkite **Baigti**, norėdami perrašyti pradinį aktyvų puslapį ir publikuoti laimėjusią variaciją, kad jis būtų pasiekiama visiems jūsų svetainės vartotojams. 

> [!NOTE]
> Jei pasirinksite palikti dabartinį aktyvų puslapį ir nepublikuoti variacijos, pasirinkite **Publikuoti pradinį puslapį iš naujo**.

## <a name="delete-your-experiment"></a>Eksperimento naikinimas
Nors nėra būtina panaikinti baigtą eksperimentą „Commerce”, galite jį panaikinti, norėdami taupyti vietą arba išvalyti jūsų darbo sritį. Norėdami panaikinti eksperimentą, atlikite toliau pateiktus veiksmus.

1. Eikite į svetainių daryklės skirtuką **Eksperimentai** ir pasirinkite eksperimentą. 
    > [!NOTE]
    > Jei eksperimentas vis dar aktyvus, prieš tęsdami, sustabdykite eksperimentą trečiosios šalies paslaugoje.
1. Norėdami pašalinti variacijos turinį iš aktyvios svetainės, komandų juostoje pasirinkite **Panaikinti publikavimą**.
1. Norėdami panaikinti eksperimentą, komandų juostoje pasirinkite **Naikinti**.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento vykdymas ir stebėjimas](experimentation-run-monitor.md)
