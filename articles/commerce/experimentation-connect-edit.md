---
title: Eksperimento prijungimas ir variacijų redagavimas
description: Šioje temoje aprašoma, kaip prijungti eksperimentą prie „Dynamics 365 Commerce” trečiosios šalies paslaugoje ir kaip redaguoti eksperimento variacijas.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d3b1a099e29073e82e2118f9e43441a9068a4d10f0ea9f79123b97d2b7d5c419
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773038"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimento prijungimas ir variacijų redagavimas

Šioje temoje aprašoma, kaip prijungti jūsų eksperimentą „Commerce” ir atlikti variacijų keitimus, kad jos sutaptų su jūsų hipoteze. 

Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose.

[ ![Vartotojo eksperimentavimo kelionė – prijungimas ir redagavimas.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

[Nustatę jūsų eksperimentą](experimentation-setup.md) trečiosios šalies paslaugoje, prijungsite eksperimentą „Dynamics 365 Commerce” ir redaguosite eksperimento variacijas.

## <a name="planning-considerations"></a>Planavimo aplinkybės

Prieš prijungdami jūsų eksperimentą „Commerce”, turite priimti tam tikrus sprendimus, kurie turi įtakos tam, kaip „Commerce” valdo jūsų turinį.

### <a name="determine-the-scope-of-your-experiment"></a>Jūsų eksperimento aprėpties nustatymas
Kai prijungiate eksperimentą, esate raginami nustatyti eksperimento aprėptį. Eksperimentai nustatomi kaip **dalinės** aprėpties arba **visos** aprėpties.
- Pasirinkite **dalinę**, jei norite atlikti konkrečios puslapio dalies eksperimentą. Jei pasirinksite šią parinktį, turite nurodyti, kurie moduliai yra įtraukti į eksperimentą. Keitimai, atliekami numatytojo puslapio arba fragmento dalims, kurios nėra susijusios su eksperimentu, automatiškai sinchronizuojami skirtingose variacijose.
- Pasirinkite **visą** aprėptį, jei norite atlikti viso puslapio ar fragmento eksperimentą. Sukuriamos atskiros numatytojo puslapio arba fragmento kopijos. Jums nereikės pasirinkti, kuriuos modulius įtraukti į eksperimentą, nes galima keisti visą redagavimo paviršių. Jei reikia, galite įtraukti, naikinti arba pertvarkyti modulius. Tačiau, jei atliekami bet kokie numatytojo puslapio arba fragmento, su kuriuo susietas eksperimentas, keitimai, šiuos keitimus reikia sinchronizuoti neautomatiniu būdu visose variacijose.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Jei susiejate jūsų eksperimentą su puslapiu, naudojančiu maketą, galite nurodyti tik **visą** eksperimento aprėptį.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Nuspręskite, ar norite suplanuoti, kada publikuoti eksperimentą
Jei norite suplanuoti, kada publikuoti eksperimentą jūsų aktyvioje svetainėje, įsitikinkite, kad turinys, kurį norite susieti su eksperimentu, yra publikavimo grupėje *prieš* eksperimento prijungimą. 

Daugiau informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).


## <a name="connect-your-experiment"></a>Jūsų eksperimento prijungimas
Norėdami prijungti eksperimentą, paleiskite vedlį **Eksperimento prijungimas**. Vedlys padeda atlikti veiksmus, reikalingus norint prijungti jūsų eksperimentą. Kai baigsite naudotis vedliu, jūsų eksperimentas bus prijungtas, o variacijos sukurtos ir paruoštos redaguoti.

Norėdami pradėti jūsų eksperimento prijungimą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Norėdami paleisti vedlį **Prijungti eksperimentą**, kairiojoje naršymo srityje pasirinkite **Eksperimentai**, tada pasirinkite **Prijungti**. Taip pat galite pasiekti vedlį iš puslapio arba fragmento rengyklės redaguodami eksperimentą ir komandų juostoje pasirinkdami **Prijungti eksperimentą**.

    > [!NOTE]
    > Puslapį galima prijungti tik prie vieno eksperimento vienu metu. Norėdami prijungti puslapį prie kito eksperimento, pirmiausia panaikinkite eksperimentą, prie kurio puslapis šiuo metu prijungtas.

1. Pasirinkite puslapį arba fragmentą, kurio eksperimentą norite vykdyti.
1. Nustatykite eksperimento aprėptį į **dalinę** arba **visą**, atsižvelgdami į pasirinkimą, kurį atlikote pirmesniame skyriuje [Jūsų eksperimento aprėpties nustatymas](#determine-the-scope-of-your-experiment).
    > [!NOTE]
    > Jei norite vykdyti viso puslapio ar fragmento eksperimentą, turite įjungti funkcijos vėliavėlę **Puslapių ar fragmentų eksperimentų vykdymas**. Daugiau informacijos ieškokite temoje [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).
    
1. Paskutinio vedlio veiksmo metu pasirinkite **Generuoti variacijas ir išjungti vedlį**. Sukuriamos eksperimento variacijos. 

## <a name="edit-your-variations"></a>Jūsų variacijų redagavimas
Išjungus vedlį, sukuriamos variacijos. 

Redaguokite variacijas, kad jos atitiktų eksperimento hipotezės pasirinkimus, kuriuos turite patvirtinti. Pasirinkite vieną iš toliau pateiktų procedūrų, atitinkančių jūsų eksperimento aprėptį, kurią pasirinkote pirmesniame skyriuje [Jūsų eksperimento aprėpties nustatymas](#determine-the-scope-of-your-experiment).

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Eksperimentų, kurių aprėptis dalinė, variacijų redagavimas
Atlikite toliau pateiktus veiksmus, jei nurodėte **dalinę** jūsų eksperimento aprėptį vedlyje **Eksperimento prijungimas**.

1. Rengyklės rodinyje naudokite variacijų išplečiamąjį meniu, esantį po komandų juosta, norėdami redaguoti kiekvieną variaciją pagal jūsų pradinę hipotezę. Taip pat galite nustatyti kontrolinę arba bazinę variaciją, palikdami vieną iš variacijų nepakeistą.
1. Pasirinkite modulį, su kuriuo bus eksperimentuojama, pasirinkite elipsę (...) ir tada pasirinkite **Įtraukti į eksperimentą**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Eksperimentų, kurių aprėptis visa, variacijų redagavimas
Jei nurodėte **visą** jūsų eksperimento aprėptį vedlyje **Eksperimento prijungimas**, rengyklės rodinyje naudokite variacijų išplečiamąjį meniu, esantį po komandų juosta, norėdami redaguoti kiekvieną variaciją pagal jūsų pradinę hipotezę. 

> [!NOTE]
> Bet kuriuo atveju galite nustatyti kontrolinę arba bazinę variaciją, palikdami vieną iš variacijų nepakeistą.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento nustatymas](experimentation-setup.md) 


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]