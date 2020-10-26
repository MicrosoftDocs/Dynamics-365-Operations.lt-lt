---
title: Grąžintų prekių patikrinimas
description: Grąžintų prekių patikrinimas.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985796"
---
# <a name="take-returned-items-through-inspection"></a>Grąžintų prekių patikrinimas 

[!include [banner](../includes/banner.md)]


1.  Spustelėkite **Atsargų valdymas** \> **Periodinis** \> **Kokybės valdymas** \> **Sulaikymo užsakymai**.

2.  Raskite užsakymo eilutę, atitinkančią tikrinamą grąžintą prekę.

    > [!NOTE]
    > <P>Sulaikymo užsakymą galima susieti tik su vienu prekės numeriu. Jei 10 prekių su skirtingais prekių numeriais grąžinamos viename siuntinyje ir siunčiamos į sulaikymą, bus sukurta 10 atskirų sulaikymo užsakymų.</P>

3.  Patikrinę prekę, lauke **Perdavimo kodas** atlikite pasirinkimą ir nurodykite, kas turėtų būti atliekama su preke ir kaip tvarkyti susijusią finansinę operaciją. Pavyzdžiai apima prekės grąžinimą į atsargas ir pinigų grąžinimą klientui, išmetimą į atliekas ir pakaitalo siuntimą klientui arba prekės grąžinimą klientui be kredito.
    
    > [!NOTE]
    > <P>Jei keleto grąžintų prekių su vienu prekės numeriu paketo negalima priskirti tam pačiam perdavimo kodui, reikia išskaidyti sulaikymo užsakymą (<STRONG>Funkcijos</STRONG> &gt; <STRONG>Skaidyti</STRONG>), kad kiekvienam papildomam paketui būtų priskirtas skirtingas perdavimo kodas.</P>


4.  Baigę tikrinti spustelėkite **Paskelbti baigtu** ir paleiskite grąžintas prekes bei sukurkite prekių atvykimo žurnalo įrašą. Tada prekes gavęs asmuo arba padalinys apdoroja į atsargas grąžintinų prekių žurnalą.
    
    arba,
    
    Pabaikite sulaikymo užsakymą ir naudodami vieną iš mygtuko **Atsargos** funkcijų prekes iš karto perkelkite atgal į atsargas.

5.  Uždarę formą įrašysite savo pakeitimus.

## <a name="see-also"></a>Taip pat žiūrėkite

[Nustatymas, kaip išmesti grąžintas prekes](specify-how-to-dispose-of-returned-items.md)

  


