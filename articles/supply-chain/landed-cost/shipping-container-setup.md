---
title: Gabenimo konteineriai
description: Šiame straipsnyje aprašoma, kaip nustatyti siuntimo konteinerius įkrautų išlaidų moduliui.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 345f815a4f85db30db18aba3f8a4d41835c2e3f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860848"
---
# <a name="shipping-container-setup"></a>Gabenimo konteinerio nustatymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti siuntimo konteinerius įkrautų **išlaidų moduliui**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Gabenimo konteinerių tipų nustatymas

Gabenimo konteinerių tipai apibrėžia gabenimo konteinerių tipus, kuriuos galima naudoti siuntimų ir reisų metu.

Norėdami dirbti su gabenimo konteinerių tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Gabenimo konteinerių tipai**. Čia galite peržiūrėti, įtraukti ir pašalinti jūsų konteinerių tipų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Gabenimo konteinerio tipas | Įveskite unikalų gabenimo konteinerio tipo identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite gabenimo konteinerio tipo aprašą. |
| Tūris | Įveskite didžiausią tūrį, leidžiamą šio tipo gabenimo konteineriuose. |
| Svarba | Įveskite didžiausią svorį, leidžiamą šio tipo gabenimo konteineriuose. |
| Grąžinama | Nurodykite, ar šio tipo gabenimo konteineriai gali būti grąžinti tiekėjui po to, kai jie buvo naudoti reiso metu. Jei ši parinktis nustatyta į *Taip*, gali būti taikomos papildomos išlaidos grąžinant šio tipo gabenimo konteinerius į kilmės uostą. |

## <a name="set-up-shipping-containers"></a>Gabenimo konteinerių nustatymas

Gabenimo konteinerių įrašus galite naudoti kiekvienam konteineriui, kurį naudojate reiso metu, identifikuoti. Kai sukuriate reisą, galite pasirinkti konkretų konteinerį visų čia apibrėžtų gabenimo konteinerių įrašų sąraše. Ši funkcija ypač naudinga, jei jūsų įmonė turi savo gabenimo konteinerių.

Jums nereikia įvesti gabenimo konteinerių, kurie bus naudojami tik vieną kartą, numerių. Vietoje to galite įtraukti gabenimo konteinerio numerį, kai kuriate reisą.

Gabenimo konteinerių įrašai naudojami tik modulyje Iškrovimo kaina. Jie negalimi standartiniame modulyje **Transportavimo valdymas** (TMS).

Norėdami dirbti su gabenimo konteineriais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Gabenimo konteineriai**. Čia galite peržiūrėti, įtraukti ir pašalinti jūsų gabenimo konteinerių įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Gabenimo konteineris | Įveskite unikalų gabenimo konteinerio identifikavimo pavadinimą / numerį. |
| Gabenimo konteinerio tipas | Pasirinkite gabenimo konteinerio tipą. Norėdami gauti daugiau informacijos, šiame straipsnyje [anksčiau pateiktame skyriuje Nustatyti siuntimo konteinerių](#shipping-container-types) tipus. |

> [!NOTE]
> - Gabenimo konteinerio nustatymas nebūtinas. Paprastai jį naudosite tik tuo atveju, jei jūsų įmonė turi savo gabenimo konteinerių arba dažnai pakartotinai naudoja tuos pačius gabenimo konteinerius.
> - Nėra skaičiuojami gabenimo konteinerių numerių kontroliniai skaitmenys.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Vienetų tipų nustatymas

Vienetų tipai nustato papildomus gabenimo konteinerių grupavimus ir identifikavimo metodus. Vieneto tipas paprastai naudojamas norint identifikuoti konteinerio, kuriame supakuotos prekės, tipą, pvz., padėklai ar statinės. Galite pasirinkti vieneto tipą, kai nustatote konteinerį puslapyje **Visi gabenimo konteineriai**.

Vienetų tipai naudojami tik modulyje Iškrovimo kaina. Jie negalimi TMS.

Norėdami dirbti su vienetų tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Vienetų tipai**. Čia galite peržiūrėti, įtraukti ir pašalinti jūsų vienetų tipų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Vieneto tipas | Įveskite unikalų vieneto tipo identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite vieneto tipo aprašymą. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Šaldymo tipų nustatymas

Šaldymo tipai nustato papildomus gabenimo konteinerių (paprastai šaldymo konteinerių) grupavimus ir identifikavimo metodus. Galite pasirinkti šaldymo tipą, kai nustatote konteinerį puslapyje **Visi gabenimo konteineriai**.

Norėdami dirbti su šaldymo tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Šaldymo tipai**. Čia galite peržiūrėti, įtraukti ir pašalinti jūsų šaldymo tipų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Šaldymo tipas | Įveskite unikalų šaldymo tipo identifikavimo pavadinimą / numerį. |
| aprašymas | Įveskite šaldymo tipo aprašymą. |
