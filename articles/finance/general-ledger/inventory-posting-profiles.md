---
title: Atsargų registravimo šablonai
description: Šioje temoje pateikta atsargų registravimo šablonų apžvalga.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28e3a3051978f921e01a929496e96909e6c32429
ms.sourcegitcommit: 00b39900d3cbdbc9ca1ab3145265007f5dc98a3f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/25/2022
ms.locfileid: "8806389"
---
# <a name="inventory-posting-profiles"></a>Atsargų registravimo šablonai

[!include [banner](../includes/banner.md)]

Atsargų registravimo šablonai valdo atsargų papildomos knygos operacijų registravimą DK. Atsargų papildomos knygos operacijos gali būti generuojamos iš daugelio **modulių**, įskaitant pardavimą ir rinkodarą, **įsigijimą** ir atsargas, **gamybos valdiklį** ir kt. Atsargų papildomos knygos operacijos gali būti registruojamos bet kada, kai prekė naudojama pardavimo užsakyme arba pirkimo užsakyme. 

Papildomos atsargų papildomos knygos operacijos gali būti užregistruotos:
- Kiekvieną kartą atnaujinus dokumentą.
- Kai registruojamas pardavimo užsakymo važtaraštis arba SF.
- Kai generuojamas pirkimo užsakymo produkto gavimo kvitas arba SF.

Norėdami gauti daugiau informacijos, eikite į atsargų papildomos knygos operacijas.

## <a name="inventory-transaction-overview"></a>Atsargų operacijų peržiūra

Kiekvienos atsargų papildomos knygos operacijos apima:
 - Kiekis 
 - Kaina 
 - Svetainė 
 - Sandėlis 
 - Vieta 

Atsargų papildomos knygos operacijos sukuria du įrašus DK faktinio registravimo ir finansinio registravimo metu. Norėdami gauti daugiau informacijos, eikite į Faktiniai [ir Finansiniai atnaujinimai](/supply-chain/cost-management/physical-financial-updates.md).
Toliau pateiktas pavyzdys yra pirkimo užsakymas su trimis eilutėmis. Pavyzdžiui, tarkime, kad visas užsakymas yra skirtas viena vietai ir sandėliui. Kiekviena pirkimo užsakymo eilutė turi vieną susijusį InventTrans įrašą, taip pat vadinamą atsargų operacija, ir kiekviena eilutė skirta kiekiui, kuris yra 10. Šioje diagramoje parodytas ryšys tarp vienos pirkimo užsakymo antraštės ir trijų pirkimo užsakymo eilučių, kiekvienoje iš kurių yra vienas InventTrans įrašas.

![Pirkimo užsakymo ryšio diagrama, kurios kiekviena su trimis eilutėmis yra su vienu InventTrans įrašu.](./media/InventTransRelationship.PNG)

Kiekis, kuris yra 5, gaunamas pirmoje pirkimo užsakymo eilutėje. Visas antrosios eilutės kiekis ir kiekis, gautas trečioje pirkimo užsakymo eilutėje. Dabar yra antroji atsargų operacija, susijusi su pirmą pirkimo užsakymo eilute. Antrosios pirkimo užsakymo eilutės operacija bus atnaujinta į **Gauta**, o trečioji operacija liks ta pati. Šioje diagramoje parodytas ryšys su papildomais InventTrans 1 eilutės įrašais.

![Pirkimo užsakymo su trimis eilutėmis ryšio diagrama. Viena eilutė yra iš dalies gauta ir rodomi du InventTrans įrašai.](./media/InventTransRelationshipPartialReceipt.PNG)

Šiame pavyzdyje kvitas bus registruojamas DK; tai faktinis kvitas. Prekių modelių grupė sukonfigūruota taip, kad būtų galima registruoti faktines atsargas, o visos prekės naudoja tą pačią prekės modelių grupę. Atsargų registravimo šablonas naudoja vieną pagrindinių sąskaitų rinkinį. Bus sukurtas vienas kvitas, o InventTrans įrašas su tuo pačiu kvitu bus susieti ir InventTrans 1, ir InventTrans 2.

Tada gauta sf už kiekį, gautą pagal 1 ir 2 eilutes. DK sukuriamas kitas kvitas; tai yra finansinis kvitas. Prekių modelių grupė sukonfigūruota registruoti finansines atsargas. Naujas antras kvitas susijęs su InventTrans 1 ir InventTrans 2.

Priklausomai nuo įkainojimo modelio, jūsų atsargų papildomos knygos operacijoms, susijusioms su atsargų uždarymu ir sudengavimu, gali būti trečiasis DK registravimas. Norėdami gauti daugiau informacijos, eikite į [Atsargų uždarymas](/supply-chain/cost-management/inventory-close.md). Galite peržiūrėti visų atsargų operacijų informaciją, nueiti į **Atsargų valdymo užklausas** > **ir ataskaitas** > **Operacijos**.

>[!Important]
> Atsargų operacijos bus padalinti kiekvienai unikaliai atsargų dimensijų kombinacijai ir kiekvienam daliniam atnaujinimą. Tai buvo parodyta ankstesniame dalinių atnaujinimų pavyzdyje.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Skaidyti atsargas pagal atsargų dimensijų pavyzdį

Pavyzdžio pirkimo užsakymo eilutė yra 3 eilutė yra eilutėmis išdėstyti prekė. Gavimo proceso metu pirkimo užsakymui užregistruojami dešimt serijos numerių. Atsargų operacija bus padalinta į 10 atsargų operacijų. Toliau pateiktoje diagramoje parodytas ryšys ir papildomos atsargų operacijos, kurių kiekviena turi savo serijos numerį susijusį su 3 pirkimo užsakymo eilute.

![Pirkimo užsakymo su trimis eilutėmis ryšio diagrama. Viena eilutė yra išdėstyti eilutėmis ir rodomi papildomi InventTrans įrašai](./media/InventTransRelationshipSerialNumber.PNG)

Anksčiau pateiktame pavyzdyje, jei kiekvienas serijos numeris gaunamas pagal vieną produkto gavimo kvitą, bus sukurtas vienas papildomas kvitas. Faktinio kvito laukas bus susietas su kiekvienu serijos numeriu. Tas pats taikoma ir finansinio atnaujinimo metu, kai išrašote pirkimo užsakymo SF.

## <a name="inventory-transactions"></a>Atsargų operacijos

Atsargų operacijas galite peržiūrėti atsargų operacijų **puslapyje, atsargų** ir **sandėlio valdymo arba** išlaidų **valdymo puslapyje**. Taip pat galite peržiūrėti atsargų operacijas, susijusias su konkrečia šaltinio dokumento eilute, pvz., pirkimo užsakymo eilute arba pardavimo užsakymo eilute, **pasirinkdami** Atsargos ir pasirinkdami **Operacijos**. 

Atsargų **operacijų puslapyje** yra šie laukai.

| Laukas            | Aprašymas                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Prekės numeris      | Su operacija susijęs prekės numeris.                                                                  |
| Faktinė data    | Atsargų pristatymo į sandėlį data, paliekama sandėlio vieta, sunaudojama gamyboje arba gaminama. Pavyzdžiui, registravimo data
Pardavimo užsakymo važtaraščio registravimą arba pirkimo užsakymo gavimo dokumento registravimą.                             |
| Finansinė data   | Data, kai atsargų operacija yra uždaryta ir išlaidos įrašomos į DK. Pavyzdžiui, registravimo data SF 
Pardavimo arba pirkimo užsakymo generavimas. Nuorodos dokumento atnaujinimai yra neleistinai po to, kai užpildoma finansinė data. |
| Nuoroda        | Nurodomas operacijos šaltinis ir dokumento tipas, rodomas lauke **Skaičius**. Pavyzdžiui, pardavimo užsakymas, pirkimo užsakymas arba perkėlimo užsakymo gavimas.                                                 |
| Skaičius           | Nurodo operacijos nuorodos ID. Pavyzdžiui, jei lauke **Nuoroda** nurodomas pardavimo užsakymas, lauke **Numeris** nurodomas pardavimo užsakymo numeris.                                                       |
| Gavimas (būsena) | Šis laukas rodo gavimų atsargų operacijų gavimo būseną. Pavyzdžiui, pirkimo užsakymas yra gavimas, o būsena gali būti Užsakyta **arba** **Nupirkta**.                                                            |
| Išdavimas (būsena)   | Išdavimą kurios yra atsargų operacijos, šis laukas nurodo išdavimo būseną. Pvz., pardavimo užsakymas yra išdavimas, o būsena gali būti Užsakyta **arba** **Parduota**.                         |
| Kiekis         | Atsargų operacijos kiekis. Teigiami skaičiai naudojami gavimų į atsargas metu, o neigiami skaičiai naudojami iš atsargų išduodant.                                                                                                                          |
| Vienetas             | Matavimo vienetas, išreikštas kiekiu.                                                                                   |
| Svėrimo kiekis      | Operacijos esamo svorio kiekis. Daugiau informacijos rasite apie esamo [svorio prekes](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Svėrimo vnt.          | Esamo svorio matavimo vienetas, išreikštas esamo svorio kiekiu.                                                         |
| Išlaidų suma      | Galutinės atsargų operacijos išlaidos. Šis laukas užpildomas finansiškai atnaujinus operaciją. Atsižvelgiant į įkainojimo metodologiją, atsargų uždarymo ir koregavimo procesas gali atnaujinti šį lauką.                            |

## <a name="inventory-status"></a>Atsargų būsena

Kiekviena atsargų operacija turi būseną, kuri rodoma lauke Gavimas **arba** **Išdavimas**. Naudojamas laukas priklauso nuo atsargų operacijų tipo. Gavimų operacijos, kurios padidina atsargas. Pavyzdžiui, pirkimo užsakymas, kurio kiekis teigiamas, arba pardavimo užsakymo grąžinimas su neigiamu kiekiu. Problemos yra atsargų operacijos, kurios sumažino atsargas. Pavyzdžiui, pardavimo užsakymas, kurio kiekis teigiamas, arba pirkimo užsakymo grąžinimas su neigiamu kiekiu.

### <a name="receipt-status"></a>Gavimo būsena

Šioje lentelėje aprašoma gavimo **būsena**.

| **Gavimo būsena** | **Aprašas**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Užsakyta            | Bet kurios atsargų operacijos, vaizduojamos gavimu, pradinė būsena. Tai apima pirkimo užsakymus, kurių kiekis teigiamas, gamybos užsakymai arba pardavimo užsakymų grąžinimai, kurių kiekis neigiamas.                                                   |
| Užregistruota         | Ši būsena naudojama, kai vyksta dviejų veiksmų gavimo procesas arba kai prekės gavimas naudojamas nurodyti, kad produktas pristatytas. Jis naudojamas, kai paketo arba serijos numeriai yra "priskirti" arba užregistruoti užsakyme. Norėdami gauti daugiau informacijos apie prekių g atvykimą, eikite į [Gavimų apžvalgą](/supply-chain/inventory/arrival-overview.md). |
| Gauta           | Ši būsena naudojama, kai operacija faktiškai atnaujinama. Pirkimo užsakymo atveju, tai yra, kai užregistruojamas produkto gavimo kvitas. Pardavimo užsakymo grąžinimo atveju tai yra, kai užregistruojamas važtaraštis.                                                                            |
| Nupirkta          | Ši būsena naudojama finansiškai atnaujinus operaciją. Kai pirkimo užsakymas arba pardavimo užsakymas grąžinamas, SF sugeneruojama.                                                                                             |

### <a name="issue-status"></a>Išdavimo būsena

Šioje lentelėje aprašoma išdavimo **būsena**.

| **Išdavimo būsena**  | **Aprašas**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Užsakyta          | Pradinė bet kurios atsargų operacijos, kuri susijusi su išdavimu, būsena. Tai taikoma pardavimo užsakymams su teigiamu kiekiu, gamybos užsakymų KS ar formulės eilutėmis arba pirkimo užsakymų grąžinimai su neigiamu kiekiu.                                             |
| Rezervuota užsakytų  | Ši atsargų būsena nurodo, kad atsargos rezervuojamos pagal sukurtą užsakymą, tačiau dar faktiškai neį gautos į atsargas. Kai atsargos gautos, būsena bus automatiškai atnaujinta į Faktiškai **rezervuota**. Norėdami gauti daugiau informacijos apie rezervavimus, eikite į [Rezervuoti atsargų kiekius](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Rezervuota faktiškai | Ši būsena nurodo, kad atsargos buvo paskirstytos arba rezervuotos pagal konkretų užsakymą. Kai atsargos rezervuojamos, kitų užsakymų atveju jos faktiškai negalimos.                                 |
| Paimta         | Tai nurodo, kad atsargos paimtos iš sandėlio. Atsargos faktiškai sandėlyje nėra pašalintos, bet negalimos kitiems užsakymams.  |
| Išskaičiuota          | Ši būsena naudojama, kai operacija faktiškai atnaujinama. Pardavimo užsakymui – tai yra užregistravimas pagal važtaraštį; pirkimo užsakymo grąžinimui – tai, kai užregistruojamas produkto gavimo kvitas.                                                                      |
| Parduota              | Tai yra būsena, naudojama finansiškai atnaujinus operaciją. Pirkimo užsakymui arba pardavimo užsakymui sf sugeneruojama.|

Norėdami gauti daugiau informacijos apie atsargų operacijas, eikite į [Atsargų operacijų informaciją](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Atsargų registravimo šablono konfigūravimas

Norėdami konfigūruoti atsargų registravimo šabloną, atlikite šiuos veiksmus:

1.  Atidarykite **atsargų valdymo nustatymo** > **registravimą** > **·** > **·**.
2.  Pasirinkite operacijos tipo skirtuką. Pvz., pasirinkite **Pirkimo užsakymas**.
3.  Pasirinkite registravimo tipo radijo mygtuką. Pvz., pasirinkite **Išlaidų pirkimo išlaidas**.
4.  Pasirinkite **Nauja**.
5.  Lauke Prekės **kodas pasirinkite** pasirinktį Lentelė **, Grupė** **·**, Visi **arba** **Kategorija.** Pavyzdžiui, norėdami konfigūruoti registravimo šabloną konkrečiai prekių grupei, pasirinkite **Grupė**.
     - **Jei 5 žingsnyje** pasirinkote Lentelė, lauke Prekės ryšys pasirinkite konkretų registravimo šablono **prekės** numerį.
     - **Jei 5 žingsnyje** pasirinkote Grupė, **prekės ryšių** lauke pasirinkite registravimo šablono **prekių** grupę.
     - **Jei 5 veiksme** pasirinkote Visi **, prekės ryšio** laukas bus tuščias.
     - **Jei 5 žingsnyje** pasirinkote Kategorija, **prekės ryšio** laukas bus tuščias. Naudokite lauką **Kategorijos** ryšys, kad pasirinktumėte kategoriją, kuri taikoma registravimo šablonui.

6.  Lauke Sąskaitos **kodas pasirinkite** pasirinktį Lentelė **, Grupė** **arba** **Visi.** Pavyzdžiui, norėdami registravimo šabloną taikyti visiems tiekėjams, pasirinkite **Visi**.
     - **Jei 5 žingsnyje** pasirinkote Lentelė, lauke Sąskaitos ryšys pasirinkite konkretų tiekėjo numerį, kuris bus skirtas **registravimo šablonui**.
     - **Jei 5 žingsnyje** pasirinkote Grupė, lauke Sąskaitos ryšys pasirinkite registravimo šablono **tiekėjų** grupę.
     - **Jei 5 veiksme** pasirinkote Visi **, sąskaitos ryšio** laukas bus tuščias.

7.  Norėdami susieti tam tikrą pvm grupę, kurios registravimo tipas pasirinktas, pasirinkite **PVM grupę**. Jei šis laukas tuščias, registravimo tipas taikomas visoms esamoms mokesčių grupėms. Registravimas, nurodytas mokesčių grupėse, taikomas tik pardavimo ir pirkimo operacijoms.
8.  Nurodykite sąskaitos numerį, kad pagrindinės sąskaitos lauke būtų galima **registruoti sąskaitos** tipą. Jei sąskaitos numeris nesukurtas naudoti kaip apskaitos tipas, galite sukurti naują sąskaitą. Naują sąskaitą sukuriate DK **informacijos puslapyje** Pagrindinės sąskaitos informacija.

## <a name="additional-resources"></a>Papildomi ištekliai

Kiekvienas atsargų registravimo **šablono puslapio skirtukas** yra susijęs su papildomos knygos lapu Dynamics 365 Supply Chain Management. Norėdami gauti daugiau informacijos, eikite į:
-   [Pardavimo užsakymo registravimas](sales-order-posting.md)
-   [Pirkimo užsakymo registravimas](purchase-order-posting.md)
-   [Atsargų registravimas](inventory-posting.md)
-   [Gamybos kontrolės registravimas](production-posting.md)
-   [Standartinių išlaidų nuokrypio registravimas](standard-cost-variance-posting.md)
