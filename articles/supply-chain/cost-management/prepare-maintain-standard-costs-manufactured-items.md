---
title: Pagamintų prekių standartinių savikainų paruošimas priežiūrai
description: Šioje temoje aprašomi pasiruošimo tvarkyti pagamintų prekių išlaidas veiksmai.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 866da2ce58e33676c2fa4bb2d6abfde891a5d021
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433630"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Pagamintų prekių standartinių savikainų paruošimas priežiūrai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi pasiruošimo tvarkyti pagamintų prekių išlaidas veiksmai. Pagamintų prekių veiksmai šiek tiek skiriasi nuo įsigytų prekių veiksmų.

Strategijos, priskirtos pagamintoms prekėms, gali paveikti pirminių pagamintų prekių išlaidų skaičiavimą. Norėdami pasiruošti tvarkyti pagamintų prekių išlaidas, atlikite tolesnius veiksmus.

1. Pagamintai prekei priskirkite prekių modelio grupę. 

   Prekių modelio grupė nustato, kad bus naudojamos standartinės išlaidos.

2. Pagamintai prekei priskirkite prekių grupę. 

   Prekių grupėje yra DK sąskaitos, taikomos pagamintai prekei. DK sąskaitose pagamintai prekei su standartinių išlaidų atsargų modeliu yra keletas gamybos nuokrypių, išlaidų pokyčio nuokrypis ir atsargų išlaidų perkainojimas.

3. Prekei priskirti atsargų matavimo vienetą. 

   Prekės išlaidos visada išreiškiamos prekės atsargų matavimo vienetu.

4. Pagamintai prekei nepriskirkite išlaidų grupės, nebent prekė bus laikoma įsigyta preke.

5. Pagamintai prekei priskirkite komplektavimo specifikacijos (KS) skaičiavimo grupę. 

   Prekės KS skaičiavimo grupė apibrėžia taikomas įspėjimo sąlygas. Taip, skaičiuojant KS, gali būti generuojami perspėjimo pranešimai apie galimus skaičiavimo klaidų šaltinius. Pavyzdžiui, perspėjimo pranešimas gali nustatyti, kada aktyvios KS ar maršruto nėra. KS skaičiavimo grupėje yra išskleidimo stabdymo strategija, nurodanti, kada pagamintą prekę reikia laikyti įsigyta preke.

6. Jei pagamintos prekės išlaidos yra pastovios, jai priskirkite standartinį užsakymo kiekį. 

   Standartinis užsakymo kiekis yra apskaitos partijos dydis pastovioms išlaidoms amortizuoti. Pastovių išlaidų pavyzdžiai – nukreipimo operacijų nustatymo laikas ir pastovus komponentų kiekis komplektavimo specifikacijoje.

7. Apibrėžkite pagamintos prekės KS. 

   Viena ar daugiau KS versijų gali būti apibrėžta pagamintai prekei. Patikrinkite, ar jūsų pageidaujamos versijos yra pažymėtos kaip patvirtintos ir aktyvios bei kad jų įsigaliojimo datos yra tokios, kokių pageidaujate. KS versija gali būti skirta visai įmonei arba konkrečiai teritorijai.

8. Apibrėžkite pagamintos prekės nukreipimą. 

   Viena ar daugiau maršrutų versijų gali būti apibrėžta pagamintai prekei. Patikrinkite, ar jūsų pageidaujamos versijos yra pažymėtos kaip patvirtintos ir aktyvios bei kad jų įsigaliojimo datos yra tokios, kokių pageidaujate. Maršruto versija turi būti skirta konkrečiai teritorijai.

Jei norite įkainodami naudoti nukreipimo informaciją, reikia atlikti papildomus paruošiamuosius veiksmus. Pavyzdžiui, išlaidų kategorijos, priskirtos nukreipimo operacijoms, turi būti teisingos ir baigtos.

<a name="related-topics"></a>Susijusios temos
--------

[Pastovių pagamintos prekės išlaidų amortizavimas](amortize-constant-costs-manufactured-item.md)

[Produktų, kuriuos galima gaminti arba įsigyti, nustatymas](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]