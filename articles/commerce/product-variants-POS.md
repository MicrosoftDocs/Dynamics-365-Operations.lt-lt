---
title: Atsargų peržvalga elektroniniame kasos aparate (EKA)
description: Šioje temoje aprašomos parinktys, kuriomis galima peržiūrėti atsargų informaciją elektroniniame kasos aparate (EKA).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 1d6133d80d7674a1d896bc19a743a6bd4d0fb40f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023461"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Atsargų peržvalga elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Atsargų peržvalga elektroniniame kasos aparate (EKA) padeda mažmenininkams realiuoju laiku gerinti veiklos efektyvumą ir gauti įžvalgų, sujungus parduotuves, EKA ir tarnybinį biurą. Ši funkcija leidžia tiksliai realiuoju laiku stebėti produkto atsargas visose parduotuvėse ir platinimo centruose. Ji taip pat padeda mažmenininkams pasiekti papildomo efektyvumo ir sumažinti išlaidas tobulinant atsargų planavimą realiuoju laiku.

Tikslus visos organizacijos atsargų vaizdas realiuoju laiku parduotuvių atstovams padeda teikti savalaikį aukščiausios kokybės klientų aptarnavimą. Svarbiausias yra tas momentas, kai klientas yra pasirengęs priimti pirkimo sprendimą. Parduotuvių kasininkams svarbu po ranka turėti realiuoju laiku matomą atsargų informaciją, kad galėtų tiksliai planuoti produktų pristatymą ir paėmimą.

Galite atidaryti puslapį **Atsargų peržvalga** iš darbo srities **Retail Modern POS** arba darbo srities **Retail Cloud POS**.

![Atsargų peržvalgos dalis EKA pagrindiniame puslapyje](media/POSHomepage.png)

Puslapyje **Atsargų peržvalga** galite skaičių klaviatūra įvesti produkto numerį. Galite peržiūrėti turimus kiekius įvairiose parduotuvėse ir sandėliuose.

![Standartinis atsargų peržvalgos puslapis](media/InventoryLookUp.png)

Taip pat rodomi kiekvienos vietos **Rezervuoti** ir **Užsakyti** kiekiai.

- **Rezervuotas** – šis kiekis rodo pasirinkto vietos produkto numerio **Faktiškai rezervuotą** kiekį tarnybiniame biure.
- **Užsakytas** – šis kiekis rodo pasirinkto vietos produkto numerio **Iš viso užsakytą** kiekį tarnybiniame biure.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Vietos, kurių atsargų likučių informacija rodoma

Vietų sąrašas apima dviejų tipų objektus:

- **Parduotuvės** – sąraše pateikiamos parduotuvės, kurios sukonfigūruotos naudojant dabartinės parduotuvės, esančios būstinėje, parduotuvių lokatorių grupę.
- **Paskirstymo centrai** – „Commerce“ galima konfigūruoti įvairių tipų paskirstymo centrus (pvz., sandėlius). Tačiau sąraše rodoma informacija apie atsargų likučius tik **Standartinio** numatytojo tipo platinimo centruose.

    > [!NOTE]
    > EKA nerodoma informacija apie atsargų likučius **Tranzito**, **Sulaikymo** ir **Išsiųstų prekių** tipų sandėliuose.

Puslapyje **Atsargų peržvalga** galite peržiūrėti prieinamų atsargų (ATP) kiekį kiekvienoje parduotuvėj, o taip pat ir dabar turimą kiekį, rezervuotą kiekį ir užsakytą kiekį. Pasirinkite parduotuvę, kurios ATP informaciją norite peržiūrėti, tada pasirinkite **Rodyti parduotuvės pasiekiamumą**.

![ATP kiekiai](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Dimensijų matricos rodinio atidarymas, kad būtų rodomi visi variantai

Bendrojo produkto puslapyje **Produkto informacija** arba puslapyje **Atsargų peržvalga** pasirinkite **Peržiūrėti visus variantus** iš programos juostos puslapio apačioje. **Dimensijų matricos** rodinys, skirtas pirminiam paleidimui iš šių puslapių, rodo informaciją apie visų produkto variantų atsargų likučius dabartinėje parduotuvėje.

> [!NOTE]
> Mygtuką **Peržiūrėti visus variantus** galima naudoti tik tame bendrojo produkto elemente, kuriame yra produkto variantų. Jo nėra atskiruose produktuose ar rinkiniuose.

![Mygtukas „Peržiūrėti visus variantus“ puslapyje „Atsargų peržvalga“](media/StandardToMatrix.png)

Bendrojo produkto puslapyje **Produkto informacija** arba puslapyje **Atsargų peržvalga** pasirinkite **Peržiūrėti visus variantus** nepasirinkdami vietos, kad patektumėte į rodinį **Dimensijų matrica** ir matytumėte informaciją apie visų produkto variantų atsargų likučius dabartinėje parduotuvėje.

![Dimensijų matricos rodinys puslapyje „Atsargų peržvalga“](media/Matrix.png)

> [!NOTE]
> Ankstesnėje iliustracijoje dimensijos rodomos abėcėlės tvarka, nes pasirinkto produkto dimensijų rodymo tvarka nebuvo sukonfigūruota.

Rodinyje **Dimensijų matrica** produkto variantų langeliuose apatiniame dešiniajame kampe rodoma turimų atsargų vertė. Įvairių verčių reikšmė yra paaiškinta toliau pateiktoje lentelėje.

| Turima vertė                            | aprašymas |
|------------------------------------------|-------------|
| Skaitinė vertė, didesnė už 0 (nulį) | Variantas išleistas pasirinktoje vietoje, langelyje galite atlikti papildomus veiksmus. (Šie veiksmai bus išsamiau aprašyti vėlesniuose šios temos skyriuose.) |
| **0** (nulis)                             | Variantas išleistas pasirinktoje vietoje, bet pasirinktos vietoje šios prekės nėra. Tačiau langelyje galite atlikti papildomus veiksmus. (Šie veiksmai bus išsamiau aprašyti vėlesniuose šios temos skyriuose.) |
| **netaikoma** arba neaktyvus langelis              | Variantas nebuvo išleistas pasirinktoje vietoje, papildomų veiksmų langelyje atlikti negalite. |

Taip pat galite keisti dimensijų suvestinę pasirinkdami naudoti naują dimensiją.

![Suvestinės keitimas](media/ChangePivot.png)

![Suvestinė pakeista](media/PivotChanged.png)

> [!NOTE]
> Ankstesnėse iliustracijose pasirinkto produkto dimensijų rodymo tvarka yra pasirinktinė (ne pagal abėcėlę). Ji paremta dimensijų rodymo tvarka, nustatyta tarnybiniame biure.

Be to, rodinyje **Dimensijų matrica** galima atlikti daugiau veiksmų ir tokiu būdu padėti padidinti parduotuvės atstovo produktyvumą. Štai keletas pavyzdžių:

- Pakeiskite parduotuvės vietą, kad peržvelgtumėte visų produkto variantų atsargų likučius kitose vietose. Šios vietos apima kitas parduotuves parduotuvių lokatorių grupėje ir **Standartinio** numatytojo tipo platinimo centrus.
- Parduokite individualų produkto variantą klientui, taikydami atsiskaitymą grynaisiais, prekių atsiėmimą parduotuvėje arba prekių siuntimą nurodytu adresu.
- Pateikite klientui ATP informaciją apie individualų produkto variantą tam tikroje vietoje.

![Papildomi veiksmai variantų dalyse](media/VariantActions.png)

> [!NOTE]
> Ankstesnėje iliustracijoje dimensijos rodomos abėcėlės tvarka, nes pasirinkto produkto dimensijų rodymo tvarka nebuvo sukonfigūruota.

Šioje lentelėje pateikiama daugiau informacijos apie galimus papildomus veiksmus.

| Veiksmas               | aprašymas |
|----------------------|-------------|
| Parduoti dabar             | Įtraukite pasirinktą prekės variantą į operaciją ir nukreipkite vartotoją į operacijos ekraną. (Šis veiksmas nėra galimas, kai pasirinkta vieta yra platinimo centras.) |
| Paimti parduotuvėje     | Sukurkite kliento užsakymą, skirtą produkto variantui, kuris bus paimtas iš pasirinktos vietos, ir nukreipkite vartotoją į operacijos ekraną. (Šis veiksmas nėra galimas, kai pasirinkta vieta yra platinimo centras.) |
| Siųsti produktą         | Sukurkite kliento užsakymą, skirtą produkto variantui, kuris bus išsiųstas iš pasirinktos vietos, ir nukreipkite vartotoją į operacijos ekraną. |
| Prieinamumas         | Rodykite ATP informaciją apie pasirinktą variantų derinį pasirinktoje vietoje. |
| Visų vietų rodymas   | Pereikite į standartinį atsargų peržvalgos rodinį ir pažymėkite informaciją apie prekės varianto atsargų likučius visose parduotuvėse parduotuvių lokatorių grupėje, taip pat **Standartinio / Numatytojo** tipo platinimo centruose. |
| Peržiūrėti produkto informaciją | Nukreipkite vartotoją į susieto bendrojo produkto puslapį **Produkto informacija**. |
