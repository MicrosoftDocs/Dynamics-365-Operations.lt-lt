---
title: Atsargų blokavimas
description: Šioje temoje apžvelgiamas atsargų blokavimas, kuris yra „Supply Chain Management‟ kokybės tikrinimo proceso dalis. Naudodami atsargų blokavimą galite neleisti apdoroti ar vartoti prekių.
author: perlynne
manager: tfehr
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 646ddc231b1ee25b13fdeb779b2bbeae6dd8c2a9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011602"
---
# <a name="inventory-blocking"></a>Atsargų blokavimas

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas atsargų blokavimas, kuris yra „Supply Chain Management‟ kokybės tikrinimo proceso dalis. Naudodami atsargų blokavimą galite neleisti apdoroti ar vartoti prekių.

Atsargų prekes blokuoti galite toliau nurodytais būdais.
-   Rankiniu būdu
-   Sukurdami kokybės užsakymą
-   Naudodami procesą, kuris generuoja kokybės užsakymą
-   Naudodami atsargų būsenos blokavimo funkciją

## <a name="blocking-items-manually"></a>Blokuodami prekes rankiniu būdu
Galite blokuoti prekės kiekį, sukurdami operaciją puslapyje **Atsargų blokavimas**. Rankiniu būdu galima blokuoti tik atsargose esančias prekes. Jei kiekius užblokuojate rankiniu būdu, turite nuspręsti, ar į veiklos planavimą kaip numatomas turimas kiekis įtrauktini numatomi gavimai. Numanomi gavimai yra užblokuotos prekės, kurios, tikimasi, baigus patikrinimą bus tarp turimų atsargų. Numatomą datą galima išlaikyti. Pagal numatytuosius nustatymus prekėms, užblokuotoms naudojant kokybės užsakymą, pasirinkta pasirinktis **Numatomi gavimai**. Galite atšaukti kiekio rankinį blokavimą panaikindami operaciją puslapyje **Atsargų blokavimas**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Prekių blokavimas sukuriant kokybės užsakymą
Galite nurodyti prekes, kurias reikia patikrinti, kurdami kokybės užsakymą puslapyje **Kokybės užsakymai**. Sukūrus kokybės užsakymą, nurodytas prekės kiekis yra užblokuojamas. Pavyzdžių ėmimo planas, susietas su kokybės užsakymu, valdo tik prekių, kurias reikia patikrinti, kiekį, o ne kiekį, kuris yra užblokuotas. Užblokuojamas tas prekės kiekis, kuris įvestas kokybės užsakyme, neatsižvelgiant į pavyzdžių ėmimo plane nurodytą kaip siųstiną tikrinti kiekį.

> [!NOTE]
> Bendrasis planavimas nepalaiko nei paketo galiojimo datos, nei atsargų būsenos blokavimo funkcijų, kai jos naudojamos kartu. Tai gali lemti dvigubą turimų atsargų neįtraukimą, kuris gali įvykti per bendrąjį planavimą. Norėdami blokuoti nebegaliojančius paketus, naudokite paketo perdavimo kodus, o ne atsargų būseną.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Prekių blokavimas naudojant procesą, kuris generuoja kokybės užsakymą
Jei kokybės procese nurodyta, kad prekę reikia patikrinti, prekių kiekis blokuojamas automatiškai. Todėl, kai automatiškai sugeneruojamas kokybės užsakymas, prekių tikrinimo planas, susijęs su kokybės užsakymu, kontroliuoja ir blokuojamų prekių kiekį, ir prekių, kurias reikia patikrinti, kiekį. Jei puslapyje **Prekės pavyzdžio ėmimas** pasirinkta parinktis **Visiškas blokavimas**, per patikrinimą blokuojamas visas kiekis, pvz., pirkimo užsakymo eilutė, nepaisant prekės tikrinimo kiekio.
### <a name="example"></a>Pavyzdys

Šiame pavyzdyje kokybės užsakymas yra generuojamas užregistravus pirkimo užsakymo važtaraštį. Puslapyje **Kokybės susiejimai** nurodėte, kad pirkimo užsakymo važtaraščio registravimas yra procesas, kuris suaktyvina kokybės užsakymą.

|Sąranka                                                                     |Vartotojo veiksmas                 |Rezultatas             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Kokybės susiejimas nurodo, kad reikia sugeneruoti kokybės užsakymą, kai registruojamas pirkimo užsakymo važtaraštis. Kokybės užsakymo prekių pavyzdžių ėmimo nustatymas nurodo, kad turi būti tikrinama 10 procentų pirkimo užsakymo eilutės kiekio. Be to, kadangi pavyzdžių ėmimo nustatyme pasirinkta parinktis **Visiškas blokavimas**, per patikrinimą turi būti užblokuotas visas pirkimo užsakymo eilutės kiekis, neatsižvelgiant į tikrinimui siunčiamą kiekį. | Važtaraštis užregistruotas. | Sugeneruotas kokybės užsakymas. Dešimt procentų pirkimo užsakymo prekės kiekio siunčiama tikrinti. Visas pirkimo užsakymo eilutės kiekis yra užblokuotas. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Prekių blokavimas naudojant atsargų būsenos blokavimo funkciją
Galite nurodyti, kurių atsargų būsenos yra blokavimo būsenos, naudodami parametrą **Atsargų blokavimas**, esantį puslapyje **Atsargų būsenos**. Negalite naudoti atsargų būsenų kaip gamybos užsakymų, pardavimo užsakymų, perkėlimo užsakymų, siuntimo operacijų arba projekto integravimų blokavimo būsenų. Atlikdami siuntimo darbus naudokite prekes, kurių atsargų būsena yra „pasiekiama“. Jei prekių būsena yra **Sugadinta** ir su tomis prekėmis atliekamas bendrasis planavimas, prekės laikomos trūkstamomis ir atsargos automatiškai papildomos.



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Kurti ir tvarkyti atsargų blokavimą](tasks/create-maintain-inventory-blocking.md)

[Kokybės valdymo procesai](quality-management-processes.md)

[Tikrinti prekių kokybę](tasks/inspect-quality-goods.md)
