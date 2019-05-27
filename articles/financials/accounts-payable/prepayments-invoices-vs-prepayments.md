---
title: Išankstinio mokėjimo SF ir išankstiniai mokėjimai
description: Šioje temoje aprašomi ir priešpriešinami du išankstinių mokėjimų būdai, kuriuos gali naudoti organizacijos. Naudojant vieną būdą, sukuriama išankstinio mokėjimo SF, susieta su pirkimo užsakymu. Naudojant kitą būdą, išankstinio mokėjimo žurnalo kvitai kuriami sukuriant žurnalo įrašus ir pažymint juos kaip išankstinio mokėjimo žurnalo kvitus.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f97eba8831e96b43f7fe7d5ea58359cab47315c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506947"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Išankstinio mokėjimo SF ir išankstiniai mokėjimai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi ir priešpriešinami du išankstinių mokėjimų būdai, kuriuos gali naudoti organizacijos. Naudojant vieną būdą, sukuriama išankstinio mokėjimo SF, susieta su pirkimo užsakymu. Naudojant kitą būdą, išankstinio mokėjimo žurnalo kvitai kuriami sukuriant žurnalo įrašus ir pažymint juos kaip išankstinio mokėjimo žurnalo kvitus.

Organizacijos gali tiekėjams išduoti išankstinius mokėjimus (mokėjimus iš anksto) už prekes arba paslaugas prieš šių prekių ar paslaugų užsakymų įvykdymą. Tiekėjams galima išduoti išankstinius mokėjimus dviem būdais. Siekdami sumažinti riziką, išankstinius mokėjimus galite sekti, išankstinį mokėjimą nurodydami pirkimo užsakyme. Naudodami šį būdą turite sukurti išankstinio mokėjimo SF, susietą su pirkimo užsakymu. Šis būdas vadinamas išankstinio mokėjimo SF išrašymu. Organizacijos, kurios nenori išankstinių mokėjimų sekti taip atidžiai arba negauna išankstinio mokėjimo SF iš savo tiekėjo, gali naudoti išankstinio mokėjimo žurnalo kvitus, o ne išankstinio mokėjimo SF išrašymo būdą. Išankstinio mokėjimo žurnalo kvitus galite kurti, sukurdami žurnalo įrašus ir pažymėdami juos kaip išankstinio mokėjimo žurnalo kvitus. Naudodami šį būdą negalite sekti, kurie kurių pirkimo užsakymų išankstiniai mokėjimai tiekėjui yra atliekami. Tačiau galite pažymėti užregistruotą išankstinį mokėjimą sudengti pagal pirkimo užsakymą.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Kada naudoti išankstinio mokėjimo SF išrašymo būdą ir išankstinius mokėjimus

| Išankstinio mokėjimo SF išrašymas                                                                | Išankstiniai mokėjimai                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Nurodykite išankstinio mokėjimo vertę pirkimo užsakyme.                                    | Pirkimo užsakyme išankstinio mokėjimo vertė nenurodyta.                    |
| Raktas: išankstinio mokėjimo SF ir paskutinė SF turi būti užregistruotos.                       | Išankstinio apmokėjimo SF registruoti nereikia.                                    |
| Išankstinio mokėjimo įsipareigojimai saugomi išankstinio mokėjimo sąskaitoje, o ne AP sąskaitoje. | Išankstinio mokėjimo įsipareigojimai saugomi AP sąskaitoje.                  |
| Tiekėjo balansas neatspindi išankstinio mokėjimo vertės visos proceso metu.     | Tiekėjo balansas atspindi išankstinio mokėjimo vertę visos proceso metu. |
| Išankstinio mokėjimo SF išrašyti galima tik naudojant mokėtinas sumas.                         | Išankstinius mokėjimus atlikti galima naudojant mokėtinas sumas ir gautinas sumas.    |

## <a name="overview-of-the-prepayment-process"></a>Išankstinio mokėjimo proceso apžvalga
Daugelyje šalių/regionų norint atlikti apskaitą, reikia, kad išankstiniai apmokėjimai iš kliento arba tiekėjui nebūtų registruojami į įprastas sumines kliento ar tiekėjo sąskaitas. Vietoj to šie išankstiniai apmokėjimai registruojami į specialias DK sąskaitas, skirtas išankstiniams apmokėjimams. Kai sukuriamas pardavimo arba pirkimo užsakymas, išrašoma SF klientui arba iš tiekėjo. Apmokant SF, išankstinis apmokėjimas ir PVM išankstinio mokėjimo kvitas, esantys išankstinių apmokėjimų DK sąskaitoje, atšaukiami, o SF sumos automatiškai užregistruojamos įprastose suminėse sąskaitose. Atlikite toliau nurodytus veiksmus, norėdami sukurti išankstinį mokėjimą.

1.  Nustatykite išankstinių mokėjimų registravimo šablonus.
2.  Puslapiuose Gautinų sumų parametrai ir Mokėtinų sumų parametrai, esančiuose dalyje **DK ir PVM**, pasirinkite naują registravimo šabloną naudodami parametrą **Registravimo šablonas, skirtas mokėjimo žurnalui, su išankstiniu mokėjimu**.
3.  Sukurkite mokėjimo žurnalą, o tada sukurkite naują mokėjimą.
4.  Mokėjimą galite pažymėti kaip išankstinį mokėjimą. Jei mokėjimas pažymėtas kaip išankstinis mokėjimas, mokėjimas užregistruojamas DK sąskaitose, nurodytose registravimo šablone, kurį nustatėte atlikdami 1 ir 2 veiksmus. Be to, jei mokėjimas pažymėtas kaip išankstinis mokėjimas, skaičiuojami mokesčiai. Kai kurios vyriausybės reikalauja, kad mokesčiai būtų sumokami, kai įrašomas išankstinis apmokėjimas, net jei SF nėra.
5.  Užregistruokite išankstinį apmokėjimą.
6.  Pasirinktinai: išankstinį mokėjimą galite sudengti pagal pirkimo arba pardavimo užsakymą prieš kurdami SF.Pardavimo užsakymo arba pirkimo užsakymo puslapio veiksmų srityje pasirinkite **Sudengti operacijas**.
7.  Po to, kai tiekėjas pristato prekes arba paslaugas, įrašykite SF. Jei išankstinį mokėjimą sudengiate pagal pirkimo arba pardavimo užsakymą (6 veiksmas), išankstinis mokėjimas yra automatiškai sudengiamas pagal jūsų sukurtą SF. Jei išankstinio mokėjimo pagal pirkimo arba pardavimo užsakymą nesudengėte, galite jį neautomatiškai sudengti pagal SF, kliento arba tiekėjo puslapyje pasirinkdami **Sudengti operacijas**. Tada išankstinio mokėjimo suma yra atšaukiama iš laikinos AP/AR DK sąskaitos. Be to, jei buvo apskaičiuoti mokesčiai, jie bus atšaukti, nes SF pateikiami faktiniai mokesčiai.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Išankstinio mokėjimo SF išrašymo proceso apžvalga
Išankstinio mokėjimo SF versle yra įprastos. Tiekėjas išduoda išankstinio mokėjimo SF, reikalaudamas pirkimo depozito prieš pirkimo užsakymo vykdymą. Pvz., kai kurie tiekėjai gali prašyti iš anksto sumokėti už tam tikras prekes arba paslaugas. Jei tiekėjas išduoda SF, pagal kurią reikalingas išankstinis mokėjimas, galite naudoti išankstinio mokėjimo SF išrašymo funkciją. Išankstinio mokėjimo vertę galima nurodyti pirkimo užsakyme, išankstinio apmokėjimo SF yra užregistruojama ir apmokama, o tada išankstinio mokėjimo SF taikoma paskutinei SF. Atlikite toliau nurodytus veiksmus, norėdami sukurti išankstinį mokėjimą.

1.  Pirkimo agentas kuria, tvirtina ir tada pateikia pirkimo užsakymą, už kurį tiekėjas prašė išankstinio mokėjimo. Išankstinio mokėjimo vertė pirkimo užsakyme nurodoma kaip sutarties dalis.
2.  Tiekėjas pateikia išankstinio mokėjimo SF.
3.  Mokėtinų sumų koordinatorius užregistruoja išankstinio mokėjimo SF pagal pirkimo užsakymą, o tada išankstinio mokėjimo SF yra apmokama.
4.  Po to, kai tiekėjas pristato prekes arba paslaugas, o susijusios tiekėjo SF yra gautos, mokėtinų sumų koordinatorius taiko išankstinio mokėjimo sumą, kuri jau buvo sudengta pagal SF.
5.  Mokėtinų sumų koordinatorius moka ir sudengia likusią SF sumą.




