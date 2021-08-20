---
title: Interaktyvus funkcijos modulis
description: Šioje temoje aprašomi interaktyvių funkcijų moduliai ir tai, kaip juos įtraukti į „Microsoft Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5b18a29ce43e69ec0578602535f21e52388fe3d04ac14673bbdefed9ec8ea161
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749855"
---
# <a name="interactive-feature-module"></a>Interaktyvus funkcijos modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi interaktyvių funkcijų moduliai ir tai, kaip juos įtraukti į „Microsoft Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Interaktyvūs funkcijų moduliai yra į mozaikas panašūs moduliai, kuriuos galima naudoti norint reklamuoti kelias produktų kategorijas arba produktų prekės ženklus naudojant vaizdų ir teksto derinį. Pavyzdžiui, mažmeninis prekybininkas gali įtraukti interaktyvų funkcijos modulį į pagrindinį elektroninės prekybos svetainės puslapį, kad pareklamuotų geriausiai parduodančias kategorijas. Interaktyvus funkcijos modulis yra panašus į plytelių sąrašo modulį, bet jo maketas ir sąveikos funkcija skiriasi.

Kiekvienas interaktyvus funkcijos modulis yra interaktyvių funkcijų elementų modulių rinkinys. Kiekvienas funkcijos elemento modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS). Jis nepriklauso nuo jokių kitų „Commerce” būstinės modulių ar duomenų. Interaktyvų funkcijos modulį galima įtraukti į bet kurį svetainės puslapį, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, kategorijas ar prekės ženklus).

> [!IMPORTANT]
> - Interaktyvus funkcijos modulis yra prieinamas kaip 10.0.20 „Dynamics 365 Commerce” versijos leidimas.
> - Interaktyvus funkcijos modulis rodomas „Adventure Works” temoje.

Šioje iliustracijoje pateikiamas interaktyvaus funkcijos modulio pavyzdys „Adventure Works” pagrindiniame puslapyje.

![Interaktyvaus funkcijos modulio pavyzdys „Adventure Works” pagrindiniame puslapyje](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktyvus funkcijos modulis ir temos

Interaktyvus funkcijos modulis gali palaikyti įvairius maketus ir stilius, pagrįstus tema. Pavyzdžiui, „Adventure Works” temoje interaktyvus funkcijų modulis turi dviejų stulpelių maketą, kuris rodo animacijos efektus, kai svetainės vartotojas užveda pelę ant kiekvienos prekės. Interaktyvus funkcijos modulis yra optimizuotas lyginiam skaičiui vaizdų, išdėstomų dviejų stulpelių maketu.

## <a name="interactive-feature-module-properties"></a>Interaktyvus funkcijos modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Interaktyvios funkcijos modulio teksto antraštė. |

## <a name="interactive-feature-item-module-properties"></a>Interaktyvus funkcijos elemento modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Nuotrauka         | Vaizdo failas | Vaizdas, atspindintis produktą arba kategoriją. Vaizdą galima įkelti į „Commerce” svetainės generatoriaus medijos biblioteką arba naudoti esamą vaizdą. |
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Numatyta, kad naudojama antraštės žymė **„H2”**, tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa     | Pastraipos tekstas | Modulis palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pavyzdžiui, hipersaitai, paryškintasis, pabrauktasis ir pasvirasis tekstas. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas          | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** parinkiklis | Modulis palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, jog atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Interaktyvaus funkcijos modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti interaktyvų funkcijos modulį ir nustatyti reikiamas ypatybes „Commerce” svetainių daryklėje, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir atidarykite jūsų svetainės pagrindinio puslapio rinkodaros šabloną (arba sukurkite naują rinkodaros šabloną).
1. Nustatytojo puslapio **Pagrindinis** vietoje pasirinkite elipsę (**...**), ir tuomet pasirinkite **Įtraukti modulį**.
1. **Pridėti modulį** dialogo lange pasirinkite **Interaktyvų funkcijos** modulį ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir atidarykite pagrindinį svetainės puslapį (arba sukurkite naują pagrindinį puslapį naudodami rinkodaros šabloną).
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Dialogo lango **Įtraukti modulį** dalyje **Pasirinkti modulius** pasirinkite **Interaktyvų funkcijos** modulį, o tada pasirinkite **GERAI**.
1. Interaktyvaus funkcijos modulio ypatybių srityje įtraukite antraštę.
1. Vietoje **Interaktyvi funkcija** pasirinkite daugtaškio mygtuką (**...**), o tada – **Įtraukti modulį**.
1. **Pridėti modulį** dialogo lange pasirinkite **Interaktyvų funkcijos elemento** modulį ir pasirinkite **Gerai**.
1. Interaktyvaus funkcijos elemento modulio ypatybių srityje įtraukite vaizdą, antraštės tekstą, paragrafo tekstą ir URL.
1. Jei reikia, įtraukite ir sukonfigūruokite papildomus interaktyvius funkcijos elemento modulius.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[„Adventure Works” tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
