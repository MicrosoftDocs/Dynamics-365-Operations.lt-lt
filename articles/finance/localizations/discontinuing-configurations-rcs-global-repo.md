---
title: Nebenaudokite konfigūracijų RCS visuotinėje saugykloje
description: Šioje temoje aprašoma, kaip nutraukti konfigūracijų naudojimą RCS visuotinėje saugykloje.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 340fc96e7dfe56da9ee8d4831a5980e3e96ec3ee0f2f5a8fb2ab72f713de9737
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712175"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Nebenaudokite konfigūracijų RCS visuotinėje saugykloje

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip nutraukti konfigūracijos naudojimą RCS visuotinėje saugykloje. Anksčiau buvo galima panaikinti tik tas konfigūracijas, kurių nebereikia. Tačiau dabar išleistą konfigūraciją galima pažymėti kaip **Nebenaudojamą** RCS visuotinėje saugykloje. Naudojant šią funkciją taip pat galima atlikti nurodytus veiksmus. 
 
 - Pateikite išankstinius pranešimus, kai konfigūracijos planuojama nebenaudoti.
 - Įtraukite taikomą informaciją apie pakeitimo konfigūraciją.
 - Konkrečiai konfigūracijai datą nustatykite kaip **Palaikoma iki**, kad praneštumėte naudotojui, jog ji nebebus tęsiama.

Kai nebenaudosite konfigūracijos versijos, galėsite nurodyti toliau nurodytą pasirenkamą informaciją.

  - **Pakaitinė konfigūracija**
  - **Pakeitimo konfigūracijos versija**
  - **Laisvos formos pastaba**: šį laukelį naudokite dokumentacijos saitams ar nuorodoms pateikti
  - **Palaikoma iki**: šiame laukelyje pateikiama siūloma data, iki kurios bus palaikoma dabartinė konfigūracija / versija. Šią datą reikia atnaujinti neautomatiniu būdu.
  
Jei norite nutraukti konfigūravimą, atlikite nurodytus veiksmus. 

1. Pasirinkite, ar norite nutraukti vienos ar visų versijų, kurių vienos operacijos parametrai tokie patys, naudojimą, parinktį **Visos versijos** nustatydami kaip **Taip**. 
2. Parametrą **Nebenaudoti** nustatykite kaip **Taip**.
3. Pasirinkite **Gerai**, jei konfigūracijų naudoti nebenorite. Laukelis **Nebenaudojimo data** pasirodys išsaugojus pakeitimus.

![Konfigūracijos informacijos nebenaudojimas.](media/Discontinue-details-2.png)
  
Konfigūraciją galima vėl pakeisti į **Bendrinama** arba bet kuriuo metu sureguliuoti nebenaudojimo informaciją. Jei bendrinate konfigūraciją, nurodykite datą **Palaikoma iki** ir visą kitą informaciją, susijusią su nebenaudojimu, kad nurodytumėte savo planus tolesniam nebenaudojimui.

Jei norite bendrinti informaciją apie planuojamą nebenaudojimą, prieš nutraukdamas konfigūravimą, naudotojas gali iš anksto užpildyti visus laukelius, susijusius su pakeitimu, tačiau parametrą **Nebenaudoti** turi nustatyti kaip **Ne**.

> [!NOTE]
> Nebenaudojimas neriboja operacijų su konfigūracijomis. Galite toliau importuoti, vykdyti arba išvesti konfigūracijas. Šie laukeliai pateikiami tik informacijos tikslais.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finansų srityje šios informacijos rodymas palaikomas, pradedant 10.0.14 versija

Pradedant nuo 10.0.14 versijos, „Dynamics 365 Finance“ palaiko nebenaudojimo informacijos rodymą. Puslapyje **Visuotinė saugykla** galima peržiūrėti naujausią su nebenaudojimu susijusią informaciją. Numatyta, kad nebenaudojamos konfigūracijos bus išfiltruojamos.
  
Puslapyje **Importuotos konfigūracijos** („ERSolutionTable“) rodomos konfigūracijos, kurios jau nebebuvo naudojamos jas importavus. Toms konfigūracijoms, kurios buvo nebenaudojamos po importavimo, nebenaudojimo informaciją galima sinchronizuoti vykdant užduotį **Konfigūracijų atnaujinimų importavimas**.


