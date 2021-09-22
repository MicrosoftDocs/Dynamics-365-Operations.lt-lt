---
title: Nerasite atsargų žurnalų išplečiamojo dialogo lango „Darbo eiga”
description: Nerandate išplečiamojo dialogo lango Darbo eiga žurnalo puslapyje arba susijusios „darbo eigos“ operacijos negalimos.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477074"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nerasite atsargų žurnalų išplečiamojo dialogo lango „Darbo eiga”

## <a name="symptoms"></a>Požymiai

Nerandate išplečiamojo dialogo lango **Darbo eiga** žurnalo puslapyje arba susijusios darbo eigos operacijos negalimos.

Ši problema gali atsirasti dėl trijų priežasčių, pateikiamų šiuose skyriuose.

## <a name="resolution-1"></a>Sprendimas 1

Jei su problema susiduria visi vartotojai, tikėtina, kad ji kartojasi, nes darbo eigos patvirtinimas nebuvo priskirtas žurnalo pavadinime. Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Atsargų valdymas &gt; Sąranka &gt; Žurnalo pavadinimai &gt; Atsargos**.
1. Sąrašo srityje pasirinkite žurnalo pavadinimą, kad atidarytumėte nustatymus.
1. **Bendras** „FastTab“ skirtuke nustatykite **Patvirtinimo darbo eiga** parinktį į *Taip*. Jei atsirado pranešimas, raginantis patvirtinti pakeitimą, pasirinkite **Taip**.
1. Lauke **Darbo eiga** lauke pasirinkite darbo eigą, kurią norite naudoti pasirinktam žurnalo pavadinimui.

## <a name="resolution-2"></a>Sprendimas 2

Jei jūsų darbo eigoje naudojamas pritaikytas kodas, atnaujinus sistemą, gali kilti problemų. Pavyzdžiui, žurnalo darbo eigoje mygtukas **Pateikti** gali būti neaktyvus, kad negalėtumėte jo paspausti pateikimui patvirtinti.

Jeigu mygtukas **Pateikti** neaktyvus, jūsų darbo eiga gali būti tinkinta, vadinasi, darbo eigos metodas `canSubmitToWorkflow()`  `FormDataUtil`buvo praplėstas. Norėdami išspręsti šią problemą, pakeiskite būdą, kuriuo praplečiate `canSubmitToWorkflow()`metodą, kad naudotumėte struktūrą pagal šį pavyzdį.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Sprendimas 3

Jei su problema susiduria tik keli konkretūs vartotojai, tie vartotojai gali neturėti saugos teisių, kurių reikia norint vykdyti darbo eigos operacijas atsargų žurnaluose. Patikrinkite, ar kiekvienas su problema susidūręs vartotojas turi *Tvarkyti atsargų žurnalo darbo eigą* saugos teisę. Pagal numatytuosius nustatymus, ši teisė priskiriama pareigai, užvadintai tuo pačiu pavadinimu, ir ši pareiga taikoma *Sandėlio darbuotojas* ir *Sandėlio vadovas* vaidmenims.
