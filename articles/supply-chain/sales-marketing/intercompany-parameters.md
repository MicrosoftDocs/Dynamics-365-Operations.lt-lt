---
title: Vidinės įmonės parametrai
description: Šiame straipsnyje paaiškinami vidinės įmonės parametrai
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7a9b921c7db47fe99981438932e5587f9a18f018
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850531"
---
# <a name="intercompany-parameters"></a>Vidinės įmonės parametrai

[!include [banner](../../includes/banner.md)]

Vidinės įmonės organizacijoje galite nustatyti parametrus, apibrėžiaius, kaip prekiauti tarp skirtingų juridinių subjektų. Šie parametrai nustatomi jūsų pasirinktuose laukuose. Norėdami atspindėti skirtingus prekybos scenarijus, galite pasirinkti skirtingas kombinacijas.

Toliau pateikti du pavyzdžiai aprašo scenarijus vidinės įmonės organizacijose, vienas lygis su dviem lygiais ir vienas su trim lygiais.

## <a name="example-1-two-level-intercompany-chain"></a>1 pavyzdys: Dviejų lygių vidinės įmonės grandinė

Vidinės įmonės organizacija apima šiuos juridinius subjektus:

- Juridinis subjektas A – parduoda išoriniams klientams, bet neturi atsargų. Šis juridinis subjektas perka iš juridinio subjekto B.
- Juridinis subjektas B – parduoda tik juridiniam subjektui A.

Abu juridiniai subjektai gali parduoti ir pirkti vieną iš kitų.

Pagal šį pavyzdį pradinio pardavimo užsakymo, kuris perduodamas išoriniam klientui, kaina visada yra paremta pardavimo kaina. Vidinės įmonės pardavimo užsakymo ir vidinės įmonės pirkimo užsakymo kainas kontroliuoja pardavimo įmonės (B) vidinės įmonės užsakyme nurodyta vidinė pardavimo Juridiniame asmenyje B.

Užsakymo antraštės informacija valdoma naudojant išorės klientui skirtą pradinį pardavimo užsakymą. Vidinės įmonės pardavimo užsakymo pakeitimai nesinchronizuoti su pradiniu pardavimo užsakymu.

Juridinio subjekto A tiekėjų **vidinės įmonės** puslapyje pasirinkite **pirkimo užsakymo strategijas**. Laukų grupėje **Pradinis pardavimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **Spausdinti važtaraštį automatiškai**
- **SF registruoti automatiškai**
- **SF spausdinti automatiškai**

Laukų grupėje **Vidinės įmonės pirkimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **SF registruoti automatiškai**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pirkimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pardavimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**
- **Paketo numeris**
- **Serijos nr.**

Juridinio subjekto B klientų **vidinės įmonės** puslapyje pasirinkite **Pardavimo užsakymo strategijas**. Laukų grupėje **Vidinės įmonės pardavimo užsakymo kūrimas** pasirinkite šiuos laukus:

- **Pardavimo užsakymo numeravimas** : **įmonė + pradinis numeris**
- **Leisti atlikti pradinio kliento dokumentų suvestinės atnaujinimą**

Laukų grupėje **Vidinės įmonės pardavimo užsakymo kūrimas** pasirinkite tolesnius laukus:

- **Kainos ir nuolaidos ieška**
- **Leisti redaguoti kainą**
- **Leisti redaguoti nuolaidą**

Laukų grupėje **Vidinės įmonės pardavimo užsakymo \> Vidinės įmonės pardavimo užsakymas** lauko grupėje, rinkitės tolesnius laukus:

- **Paketo numeris**
- **Serijos nr.**

## <a name="example-2-three-level-intercompany-chain"></a>2 pavyzdys: Trijų lygių vidinės įmonės grandinė

Vidinės įmonės organizacija apima šiuos juridinius subjektus:

- Juridinis subjektas A – pardavimo juridinis subjektas, kuris parduoda išoriniams klientams ir perka iš juridinio subjekto B.
- Juridinis subjektas B – gamybos ar paskirstymo juridinis subjektas, kuris negali pristatyti produktų ir perka iš juridinio subjekto C.
- Juridinis subjektas C – gamybos ar paskirstymo juridinis subjektas, kuris negali pristatyti produktų ir perka iš juridinio subjekto B.

Vidinio perkėlimo tarp juridinių subjektų B ir C kaina iš parduodančių juridinių subjektų grandinės pradžioje. Ji taip pat kainuoja juridiniam subjektui A, kuris parduoda išoriniams klientams. Pradinio pardavimo užsakymo kaina, taikoma išoriniam klientui, visuomet yra paremta pardavimo kaina.

Visų vidinės įmonės pardavimo užsakymų ir vidinės įmonės pirkimo užsakymų kaina kontroliuojama pagal vidinės įmonės pardavimo užsakymą. Jis valdomas grandinės pradžioje. Todėl juridinis subjektas C, kuris parduoda juridiniam subjektui B, kontroliuoja kainą. Vidinės įmonės pardavimo užsakymo kaina yra paremta vidine pardavimo ar perkėlimo kaina, kuris yra nustatyta juridiniame objekte C.

Užsakymo antraštės informacija valdoma naudojant išorės klientui skirtą pradinį pardavimo užsakymą. Vidinės įmonės užsakymų pakeitimai nesinchronizuojami su pradiniu pardavimo užsakymu.

Reikia pasirinkti šiuos parametrus:

Juridinio subjekto A tiekėjų **vidinės įmonės** puslapyje pasirinkite **pirkimo užsakymo strategijas**. Laukų grupėje **Pradinis pardavimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **Spausdinti važtaraštį automatiškai**
- **SF registruoti automatiškai**
- **SF spausdinti automatiškai**

Laukų grupėje **Vidinės įmonės pirkimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **SF registruoti automatiškai**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pirkimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pardavimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**
- **Paketo numeris**
- **Serijos nr.**

Juridinio subjekto B klientų **vidinės įmonės** puslapyje pasirinkite **Pardavimo užsakymo strategijas**. Laukų grupėje **Vidinės įmonės pardavimo užsakymo kūrimas** pasirinkite šiuos laukus:

- **Pardavimo užsakymo numeravimas** : **įmonė + pradinis numeris**
- **Leisti atlikti pradinio kliento dokumentų suvestinės atnaujinimą**

Laukų grupėje **Vidinės įmonės pardavimo užsakymo \> Vidinės įmonės pardavimo užsakymas** lauko grupėje, rinkitės tolesnius laukus:

- **Paketo numeris**
- **Serijos nr.**

Laukų grupėje **Vidinės įmonės kliento SF publikavimas** pasirinkite tolesnius laukus:

- **Vieneto kaina lygi savikainai**
- **Inicijuoti pradinio kliento SF registravimą**

Juridinio subjekto B tiekėjų **vidinės įmonės** puslapyje pasirinkite **pirkimo užsakymo strategijas**. Laukų grupėje **Pradinis pardavimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **Spausdinti važtaraštį automatiškai**
- **SF registruoti automatiškai**
- **SF spausdinti automatiškai**

Laukų grupėje **Vidinės įmonės pirkimo užsakymas (tiesioginis pristatymas)** pasirinkite šiuos laukus:

- **SF registruoti automatiškai**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pirkimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**
- **Kaina ir nuolaida**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pardavimo užsakymas** pasirinkite šiuos laukus:

- **Kliento informacija**
- **RMA numeris**
- **Paketo numeris**
- **Serijos nr.**

Juridinio subjekto C klientų **vidinės įmonės** puslapyje pasirinkite **Pardavimo užsakymo strategijas**. Laukų grupėje **Vidinės įmonės pardavimo užsakymo kūrimas** pasirinkite šiuos laukus:

- **Pardavimo užsakymo numeravimas**: **numeracijos kodas**
- **Leisti atlikti pradinio kliento dokumentų suvestinės atnaujinimą**

Laukų grupėje **Vidinės įmonės pardavimo užsakymo kūrimas** pasirinkite tolesnius laukus:

- **Kainos ir nuolaidos ieška**

Laukų grupėje **Vidinės įmonės kliento SF publikavimas** pasirinkite tolesnius laukus:

- **Vieneto kaina lygi savikainai**
- **Inicijuoti pradinio kliento SF registravimą**

Laukų grupėje **Originalių pardavimų užsakymas <-> Vidinės įmonės pirkimo užsakymas** pasirinkite šiuos laukus:

- **Paketo numeris**
- **Serijos nr.**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
