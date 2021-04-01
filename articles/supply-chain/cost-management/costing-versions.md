---
title: Įkainojimo versijų apžvalga
description: Šiame straipsnyje pateikta informacija apie įkainojimo versijas, kaip jas prižiūrėti, ir duomenų, kuriuos į jas galima įtraukti, tipus. Pirminė įkainojimo versijos paskirtis yra saugoti išlaidų įrašus apie prekes, išlaidų kategorijas ir netiesioginių išlaidų apskaičiavimo formules.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4375c088e0872f6f75ee83b288c41e80ea4dcb34
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232355"
---
# <a name="costing-versions-overview"></a>Įkainojimo versijų apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie įkainojimo versijas, kaip jas prižiūrėti, ir duomenų, kuriuos į jas galima įtraukti, tipus. Pirminė įkainojimo versijos paskirtis yra saugoti išlaidų įrašus apie prekes, išlaidų kategorijas ir netiesioginių išlaidų apskaičiavimo formules.

Įkainojimo versija gali turėti vieną ar daugiau paskirčių, jos priklauso nuo duomenų, esančių įkainojimo versijoje. Pirminė įkainojimo versijos paskirtis yra saugoti išlaidų įrašus apie prekes, išlaidų kategorijas ir netiesioginių išlaidų apskaičiavimo formules. Įkainojimo versiją gali sudaryti standartinių išlaidų įrašų rinkinys arba suplanuotų išlaidų įrašų rinkinys paremtas įkainojimo tipu, kuris priskirtas įkainojimo versijai.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Standartinių ar suplanuotų išlaidų įkainojimo versijos
### <a name="standard-costs"></a>Standartinės išlaidos

Įkainojimo versija palaiko standartinį atsargų išlaidų modelį prekėms, kurių įkainojimo versijas sudaro standartinių išlaidų įrašų rinkinys apie prekes ir gamybos procesus. Išlaidų duomenys apie gamybos procesus išreikšti išlaidų kategorijomis maršruto operacijoms ir papildomomis gamybos duomenų apskaičiavimo formulėmis.

### <a name="planned-costs"></a>Suplanuotos išlaidos

Įkainojimo versija gali būti sudaryta iš suplanuotų išlaidų rinkinio apie prekes ir gamybos procesus. Įkainojimo versija su suplanuotomis išlaidomis dažnai naudojama palaikyti išlaidų apskaičiavimo modeliavimams, pavyzdžiui, poveikio, kurį turi nupirktoms medžiagoms arba gaminamų prekių gamybos procesams apskaičiuotų išlaidų pokytis, modeliavimui. Prekės išlaidų įrašai suplanuotoms išlaidoms taip pat gali būtu naudojami faktiniam išlaidų atsargoms modeliui palaikyti. Į šias reikšmes įtrauktas suplanuotų pagamintų prekių išlaidų skaičiavimas.

## <a name="entering-costs"></a>Išlaidų įvedimas
Išlaidų įrašų įkainojimo versijoje duomenų tvarkymas apima išlaidų nupirktoms prekėms ir prekėms, kurios perkeliamos iš vienos teritorijos į kitą, įvedimą. Papildomų duomenų tvarkymas gamintojams apima išlaidų įvedimą į išlaidų kategorijas, kurios susijusios su maršruto operacijomis, apskaičiavimo formulių netiesioginėms išlaidoms įvedimą, suteikiantį papildomų duomenų apie gamybą, ir gaminamų prekių išlaidų apskaičiavimą. 

Prekių išlaidų duomenis įkainojimo versijoje sudaro vienas ar keli kiekvienos prekės išlaidų įrašai. Kai pirmą kartą įvedamas prekės išlaidų įrašas, jo būsena yra **Laukiantis** ir jis turi numatomą įsigaliojimo datą. Kai prekės išlaidų įrašą suaktyvinate, būsena atnaujinama į **Aktyvus**, o įsigaliojimo data atnaujinama į aktyvavimo datą. Skirtingi prekių išlaidų įrašai gali atspindėti skirtingas teritorijas, galiojimo datas ar būsenas. Kai skaičiuojate būsimos datos pagamintų prekių išlaidas, skaičiuojant komplektavimo specifikaciją (KS), naudojami išlaidų įrašai su aktualia galiojimo data, nesvarbu, ar būsena yra **Laukiantis**, ar **Aktyvus**. Prekės dabartinis aktyvus išlaidų įrašas naudojamas gamybos užsakymo išlaidoms įvertinti ir pagal standartinį atsargų įkainojimo modelį nustatyti atsargų operacijų vertei. Išlaidų kategorijų išlaidų įrašų tvarkymas ir netiesioginių išlaidų apskaičiavimo formulių tvarkymas primena prekės išlaidų įrašų tvarkymą. 

Dvi išlaidų versijos blokavimo strategijos nustato, ar laukiančios išlaidos gali būti tvarkomos ir ar galima suaktyvinti laukiančias išlaidas. Naudokite blokavimo strategijas, norėdami leisti duomenų tvarkymą ir taip pat jas naudokite norėdami uždrausti išlaidų įrašų duomenų tvarkymą įkainojimo versijoje. 

Įkainojimo versiją taip pat sudaro duomenys apie prekės pardavimo ar pirkimo kainas KS apskaičiavimo tikslams.

## <a name="item-sales-prices-for-bom-calculations"></a>Prekių pardavimo kainos skaičiuojant KS
Pagrindinė priežastis įtraukti duomenims apie pardavimo kainas yra išlaikyti apskaičiuotą pagamintos prekės pardavimo kainą. Tada apskaičiuotą pardavimo kainą galima analizuoti, siekiant nustatyti, kaip komponentai, nukreipimo operacijos ir papildomos išlaidos prisideda prie savikainos ir pardavimo kainos. 

Antrinė priežastis įtraukti duomenims apie pardavimo kainas yra apibrėžti sudedamųjų prekių pardavimo kainų įrašus. Šiuos įrašus tada galima naudoti norint apskaičiuoti pagamintų prekių pardavimo kainą. Pirmiausia apibrėžiate pardavimo kainos modelį, įdėtą į KS skaičiavimo grupę, ir ją priskiriate nupirktoms prekėms. Tada, atlikdami KS skaičiavimus, kurie naudoja suplanuotas išlaidas, pasirenkate KS skaičiavimo grupės savikainos modelį. 

Kitu atveju prekių pardavimo kainos įrašai naudojami tik kaip nuorodos informacija, nesvarbu, ar įrašai įvesti rankiniu būdu, ar apskaičiuoti. Suaktyvinę prekės pardavimo kainos įrašą, galite atnaujinti prekės bazinę pardavimo kainą. Tačiau bazinė pardavimo kaina nepriklauso nuo teritorijos, ir ją galima rankiniu būdu perrašyti. Prekės bazinė pardavimo kaina naudojama kaip numatytoji pardavimo kaina pardavimo užsakymuose ir pardavimo pasiūlymuose.

## <a name="item-purchase-prices-for-bom-calculations"></a>Prekių pirkimo kainos skaičiuojant KS
Pagrindinė pirkimo kainos duomenų įgalinimo priežastis yra apibrėžti sudedamųjų prekių pirkimo kainos įrašus, kad juos būtų galima naudoti apskaičiuojant pagamintų prekių išlaidas. Prekės pirkimo kainos įrašai privalo būti įvedami rankiniu būdu. 

Norėdami įgalinti pirkimo kainos turinį, pirmiausia apibrėžiate KS skaičiavimo grupę, kurioje yra prekės pirkimo kainos savikainos modelis, ir KS skaičiavimo grupę priskiriate nupirktoms prekėms. Tada, atlikdami KS skaičiavimus, kurie naudoja suplanuotas išlaidas, kad apskaičiuotumėte pagamintų prekių pardavimo kainą, naudojate KS skaičiavimo grupės savikainos modelį. 

Prekių pirkimo kainos įrašai taip pat naudojami kaip nuorodos informacija. Prekės pirkimo kainos įrašo būseną pakeitę iš **Laukiantis** į **Aktyvus**, galite atnaujinti prekės bazinę pirkimo kainą. Tačiau bazinė pirkimo kaina nepriklauso nuo teritorijos, ir ją galima rankiniu būdu perrašyti. Prekės bazinė pirkimo kaina naudojama kaip numatytoji pirkimo užsakymų pirkimo kaina.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]