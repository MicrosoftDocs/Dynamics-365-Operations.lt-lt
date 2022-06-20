---
title: Planavimas su neigiamais turimais kiekiais
description: Šiame straipsnyje paaiškinama, kaip tvarkomi neigiami turimi rezultatai naudojant planavimo optimizavimą.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04006bb12142be69c84bc8085dd82fc99280e90b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856141"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planavimas, kai turimi kiekiai neigiami

[!include [banner](../../includes/banner.md)]

Jei sistemoje rodomas neigiamas bendrasis turimas kiekis, planavimo mechanizmas kiekį laiko 0 (nuliu), kad padėtų išvengti tiekimo pertekliaus. Toliau nurodyta, kaip ši funkcija veikia.

1. Planavimo optimizavimo funkcija sujungia turimus kiekius taikydama mažiausią padengimo dimensijų lygį. (Pavyzdžiui, jei *vieta* nėra padengimo dimensija, planavimo optimizavimo funkcija turimus kiekius sujungia *sandėlio* lygiu.)
1. Jei bendrasis turimas kiekis taikant mažiausią padengimo dimensijų lygį yra neigiamas, sistema daro prielaidą, kad turimas kiekis tikrai yra 0 (nulis).

> [!IMPORTANT]
> Planavimo sistema gali būti tik tiek tiksli, kiek tikslūs įvesti duomenys. Jei įvesti duomenys yra netikslūs, neigiamo turimo kiekio įrašai nurodys, kad „Microsoft Dynamics 365 Supply Chain Management“ atsargų informacija nesusinchronizuota su realiu pasauliu. Todėl planavimo rezultatas bus klaidingas. Norėdami gauti tikslų planavimo rezultatą, turite sumažinti įrašų, kuriuose rodomas neigiamas turimas kiekis, skaičių.

## <a name="example-1"></a>1 pavyzdys

13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.

- **Padengimo kodas:** min. / maks.
- **Minimalus** 15 vienetų (vnt.)
- **Maksimalus:** 25 vnt.

Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.

- **1 objektas, 13 sandėlis, 1 vieta:** 20 vnt.
- **1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.

Todėl bendrasis turimas 13 sandėlio kiekis yra 12 vnt. (= 20 vnt. &minus; 8 vnt.).

Šiuo atveju planavimo mechanizmas naudoja 12 vnt. bendrąjį turimą kiekį. 13 sandėlyje.

Rezultatas yra suplanuotas 13 vnt. užsakymas (= 25 vnt. &minus; 12 vnt.), kad 13 sandėlis būtų pripildytas nuo 12 vnt. iki 25 vnt.

## <a name="example-2"></a>2 pavyzdys

13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.

- **Padengimo kodas:** min. / maks.
- **Minimalus:** 15 vnt.
- **Maksimalus:** 25 vnt.

Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.

- **1 objektas, 13 sandėlis, 1 vieta:** 4 vnt.
- **1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.

Todėl bendrasis turimas 13 sandėlio kiekis yra &minus;4 vnt. (= 4 vnt. &minus; 8 vnt.). Kitaip tariant, mažiau nei 0 (nulis).

Šiuo atveju planavimo mechanizmas daro prielaidą, kad turimas 13 sandėlio kiekis yra 0 vnt., o ne &minus;4 vnt.

Rezultatas yra suplanuotas 25 vnt. užsakymas (= 25 vnt. &minus; 0 vnt.), kad 13 sandėlis būtų pripildytas nuo 0 vnt. iki 25 vnt.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Planavimas, kai yra rezervavimas dėl neigiamų turimų atsargų

Jeigu atsargas koreguojate, kai yra faktinių rezervavimų, galite sukelti situaciją, kai užsakymas faktiškai rezervuojamas prieš neigiamas atsargas. Šiuo atveju, kadangi yra faktinis rezervavimas, turite turėti tiekimą, kad būtų galima padengti rezervuotą kiekį. Todėl būtina papildyti, todėl sistema sukurs suplanuotą užsakymą, pagal kurį būtų papildomas kiekis, kurio nepavyko padengti turimos atsargos, arba padengti jį esamu prekės užsakymu.

Toliau pateiktas pavyzdys iliustruoja šį scenarijų.

### <a name="example"></a>Pavyzdys

Sistema konfigūruota tokiu būdu:

- Produktas *FG* yra ir turima *10* vnt. turimų atsargų.
- Produkto konfigūracija leidžia faktines neigiamas atsargas.
- Pardavimo užsakymą sudaro *10* vnt. kiekiui. produkto *FG*.
- Pardavimo užsakymo kiekis faktiškai rezervuojamas pagal esamas turimas atsargas.

Tada koreguojate produkto *FG* kiekį, kad turimos atsargos taptų 5. Kadangi turimos produkto atsargos yra 5, dabar pardavimo užsakymo kiekis rezervuojamas pagal kiekį, kurio nėra turima (būtų panaši į tai, jei turimos atsargos būtų 0, o šiuo atveju pardavimo užsakymas būtų rezervuotas pagal neigiamas atsargas). Jei paleisite bendrąjį planavimą dabar, FG *bus sukurtas suplanuotas 5* kiekio užsakymas, skirtas tiekti pardavimo užsakymą, kadangi planavimo optimizavimas visada naudos esamą tiekimą arba sukurs naują suplanuotą užsakymą faktiniam rezervavimui tiekti.

## <a name="related-resources"></a>Susiję ištekliai

- [Planavimo optimizavimo apžvalga](planning-optimization-overview.md)
- [Darbo su planavimo optimizavimu pradžia](get-started.md)
- [Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)
- [Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)
- [Planavimo užduoties atšaukimas](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
