---
title: Eksperimento peržiūra ir publikavimas
description: Šioje temoje aprašoma, kaip peržiūrėti ir publikuoti eksperimentą iš „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414485"
---
# <a name="preview-and-publish-an-experiment"></a>Eksperimento peržiūra ir publikavimas

Šioje temoje aprašoma, kaip peržiūrėti ir publikuoti jūsų eksperimentą „Dynamics 365 Commerce” po to, kai [prijungėte eksperimentą ir redagavote variacijas](experimentation-connect-edit.md). Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”. Papildomi veiksmai aprašomi kitose temose.

[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir publikavimas](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Jūsų eksperimento variacijų peržiūra
Galite peržiūrėti jūsų variacijas ir jas redaguoti, kad jos atrodytų taip, kaip norite.

Norėdami peržiūrėti jūsų eksperimento variacijas „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Po komandų juosta esančiame išplečiamajame variacijų meniu pasirinkite turinį, kurį norite peržiūrėti. 
1. Komandų juostoje pasirinkite **Peržiūrėti**. Rodoma peržiūra, kaip turinys atrodys, kai jis bus publikuotas.
1. Norėdami peržiūrėti kitą variaciją, pasirinkite ją iš variacijų išplečiamojo meniu ir pasirinkite **Peržiūra** dar kartą.

## <a name="publish-your-experiment"></a>Jūsų eksperimento publikavimas
Jei nenaudojate publikavimo grupės, kad suplanuotumėte, kada eksperimentas bus publikuotas, o norite publikuoti iš karto, komandų juostoje pasirinkite **Publikuoti**. Bus publikuotos visos eksperimentui priklausančios variacijos.
    
> [!IMPORTANT]
> Jei puslapyje yra nepublikuotas URL, pirmiausia turite publikuoti URL, kitaip jis nebus matomas jūsų svetainės vartotojams. Daugiau informacijos žr. [Puslapio įrašymas, peržiūra ir publikavimas](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Publikavimo grupių naudojimas suplanuoti, kada eksperimentas bus publikuotas
Galima suplanuoti variacijų, sukurtų svetainių daryklėje, publikavimą naudojant publikavimo grupę. Publikavimo grupėje galite prijungti puslapį ar fragmentą prie jūsų eksperimento, kairiojoje naršymo srityje pasirinkdami **Eksperimentai**. Taip pat galite tai atlikti pasirinkdami **Puslapiai** arba **Fragmentai** ir vadovaudamiesi instrukcijomis, pateiktomis [Eksperimento prijungimas ir variacijų redagavimas](experimentation-connect-edit.md). Informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).

Naudojant publikavimo grupes su eksperimentais, yra svarbių dalykų, kuriuos reikia žinoti.
- Kai įtraukiate puslapį ar fragmentą, kuriame vykdomas eksperimentas, į publikavimo grupę, eksperimentas bus pašalintas iš puslapio ar fragmento publikavimo grupėje.
- Eksperimentai, prijungti prie aktyvios svetainės svetainės puslapių, nėra pasiekiami publikavimo grupių puslapiuose (ir atvirkščiai). Be to, aktyvios svetainės puslapiai, kuriuose vykdomi eksperimentai, nėra pasiekiami kituose publikavimo grupių eksperimentuose (ir atvirkščiai).
- Publikuojant arba planuojant publikavimo grupę, visas publikavimo grupės turinys publikuojamas, neatsižvelgiant į tai, ar yra eksperimentas, susietas su publikavimo grupe.
- Kadangi publikavimo grupė ir toliau išlieka po to, kai ji publikuojama aktyvioje svetainėje, eksperimentai publikavimo grupėje taip pat išlieka. Todėl negalėsite susieti kitų eksperimentų su tuo pačiu puslapiu ar fragmentu. Norėdami išvengti šio apribojimo, panaikinkite visas publikavimo grupes, kuriose yra išlikusių eksperimentų. Taip pat, jei norite panaikinti aktyvios svetainės eksperimentą, kuris taip pat yra publikavimo grupėje, pirmiausia panaikinkite jį iš publikavimo grupės.

## <a name="previous-step"></a>Ankstesnis veiksmas
[Eksperimento prijungimas ir redagavimas](experimentation-connect-edit.md)

## <a name="next-step"></a>Kitas veiksmas
[Eksperimento vykdymas ir stebėjimas](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]