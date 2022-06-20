---
title: Eksperimento prijungimas ir variacijų redagavimas
description: Šiame straipsnyje aprašoma, kaip susieti jav ir trečiosios šalies tarnybos an elimisiją Dynamics 365 Commerce su failo variantu ir kaip redaguoti jo variantus.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942827"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimento prijungimas ir variacijų redagavimas

Šiame straipsnyje aprašoma, kaip susieti savo antensiją komercijoje ir atlikti pakeitimus, kad jos sutaptumėte su jūsų maketacija. 

Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai įtraukti atskiruose straipsnius.

[ ![Vartotojo eksperimentavimo kelionė – prijungimas ir redagavimas.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

[Nustatę jūsų eksperimentą](experimentation-setup.md) trečiosios šalies paslaugoje, prijungsite eksperimentą „Dynamics 365 Commerce” ir redaguosite eksperimento variacijas.

## <a name="connect-your-experiment"></a>Jūsų eksperimento prijungimas
Norėdami prijungti eksperimentą, paleiskite vedlį **Eksperimento prijungimas**. Vedlys padeda atlikti veiksmus, reikalingus norint prijungti jūsų eksperimentą. Kai baigsite naudotis vedliu, jūsų eksperimentas bus prijungtas, o variacijos sukurtos ir paruoštos redaguoti.

Norėdami pradėti jūsų eksperimento prijungimą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Norėdami paleisti vedlį **Prijungti eksperimentą**, kairiojoje naršymo srityje pasirinkite **Eksperimentai**, tada pasirinkite **Prijungti**. Taip pat galite pasiekti vedlį iš puslapio arba fragmento rengyklės redaguodami eksperimentą ir komandų juostoje pasirinkdami **Prijungti eksperimentą**.

    > [!NOTE]
    > - Puslapį galima prijungti tik prie vieno eksperimento vienu metu. Norėdami prijungti puslapį prie kito eksperimento, pirmiausia panaikinkite eksperimentą, prie kurio puslapis šiuo metu prijungtas.
    > - Galite tik naudoti tinklapius naudodami pasirinktinį maketą. Jei jūsų puslapyje yra iš anksto nustatytas maketas, pirmiausia konvertuokite jį į pasirinktinį maketą. Tai galite atlikti pereidami į puslapį ir komandų juostoje **pasirinkdami Konvertuoti** į pasirinktinį maketą. Daugiau informacijos apie maketus ieškokite Iš anksto nustatyti [ir pasirinktiniai maketai](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Jei jungiatės prie anuliacijos **iš kairės** naršymo srities skirtuko Lapo, iš rodomą sąrašą pasirinkite dialogo lango pavadinimą.
1. Pasirinkite puslapį ar fragmentą, kurį norite vykdyti savo kadaise.
1. Paskutinio vedlio veiksmo metu pasirinkite **Generuoti variacijas ir išjungti vedlį**. Sukuriamos eksperimento variacijos. 

> [!NOTE]
> Jei norite suplanuoti, kada publikuoti eksperimentą jūsų aktyvioje svetainėje, įsitikinkite, kad turinys, kurį norite susieti su eksperimentu, yra publikavimo grupėje *prieš* eksperimento prijungimą. Daugiau informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).

## <a name="edit-your-variations"></a>Jūsų variacijų redagavimas

Išeidami iš **"Connect"** vedlio, sukuriate jums variacijas. Norėdami redaguoti variacijas, kad jie atspindėtų pasirinktis, kurias turite patikrinti naujame ekrane, atlikite toliau aprašytus veiksmus.

1. Rengyklės rodinyje naudokite variacijų išplečiamąjį meniu, esantį po komandų juosta, norėdami redaguoti kiekvieną variaciją pagal jūsų pradinę hipotezę. Taip pat galite nustatyti kontrolinę arba bazinę variaciją, palikdami vieną iš variacijų nepakeistą.
1. Pasirinkite modulį, su kuriuo bus eksperimentuojama, pasirinkite elipsę (...) ir tada pasirinkite **Įtraukti į eksperimentą**.

> [!NOTE]
> Apsvarstykite galimybę sukurti valdiklį arba pagrindinį nuovariaciją, vieną iš variantų palikdami nepakeistą.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento nustatymas](experimentation-setup.md) 


## <a name="next-step"></a>Kitas veiksmas
[Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
