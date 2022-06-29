---
title: Atšaukti aptarnavimo užsakymus
description: Galite atšaukti aptarnavimo užsakymą arba aptarnavimo užsakymo eilutę arba galite atšaukti kelis aptarnavimo užsakymus vykdydami periodinę užduotį.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228b76d6f6f0bb048662c8e82df76f51b7cb3652
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017382"
---
# <a name="cancel-service-orders"></a>Atšaukti aptarnavimo užsakymus   

[!include [banner](../includes/banner.md)]


Galite atšaukti aptarnavimo užsakymą arba aptarnavimo užsakymo eilutę arba galite atšaukti kelis aptarnavimo užsakymus vykdydami periodinę užduotį.


> [!NOTE]
> <P>Aptarnavimo užsakymai negali būti atšaukti, jei aptarnavimo užsakymo etapas neleidžia atšaukti, jei aptarnavimo užsakymas turi prekių poreikį arba jei aptarnavimo užsakymas jau užregistruotas.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Aptarnavimo užsakymų formoje esančių aptarnavimo užsakymų atšaukimas

1.  Spustelėkite Aptarnavimo **valdymo paslaugos** \> **užsakymai** \> **Aptarnavimo užsakymai**. Pasirinkite aptarnavimo užsakymą ir veiksmų srityje spustelėkite **Atšaukti užsakymą**.

## <a name="cancel-a-service-order-line"></a>Aptarnavimo užsakymo eilutės atšaukimas

1.  Spustelėkite Aptarnavimo **valdymo paslaugos** \> **užsakymai** \> **Aptarnavimo užsakymai**. Dukart spustelėkite aptarnavimo užsakymą, kuriame yra eilutė, kurią norite atšaukti.

2.  Pasirinkite aptarnavimo užsakymo eilutę, kurią norite atšaukti, tada spustelėję **Atšaukti užsakymo eilutę** pakeisite eilutės būseną į **Atšaukta**.


> [!TIP]
> <P>Norėdami panaikinti aptarnavimo užsakymo eilutės atšaukimą ir pakeisti būseną atgal į <STRONG>Sukurta</STRONG>, spustelėkite <STRONG> anuliuoti atšaukimą</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Kelių aptarnavimo užsakymų atšaukimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Periodinis** \> **Aptarnavimo užsakymai** \> **Atšaukti aptarnavimo užsakymus**.

2.  Spustelėkite mygtuką **Pasirinkti**.

3.  Formos **Užklausa** stulpelyje **Kriterijai** pasirinkite aptarnavimo užsakymus, kuriuos norite atšaukti.

4.  Spustelėję **Gerai** uždarykite formą **Užklausa**.

5.  Pažymėkite žymės langelį **Rodyti sistemos pranešimą** norėdami sugeneruoti sistemos pranešimą, kuriame būtų nurodyti atšaukti aptarnavimo užsakymai.

6.  Pažymėkite žymės langelį **Anuliuoti atšaukimą**, jei norite panaikinti aptarnavimo užsakymo būseną **Atšaukta**.

7.  Spustelėkite **Gerai**.

Pasirinkti aptarnavimo užsakymai yra arba atšaukti, arba jų eigos būsena **Atšaukta** buvo pakeista į **Vykdoma**.


> [!NOTE]
> <P>Jei pažymėjote žymės langelį <STRONG>Anuliuoti atšaukimą</STRONG>, aptarnavimo užsakymai, kurių eigos būsena yra <STRONG>Atšaukta</STRONG>, yra pakeičiami ir jokie aptarnavimo užsakymų, kurių eigos būsena yra <STRONG>Vykdoma</STRONG>, atšaukimai nevykdomi.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]