---
title: Egipto PVM deklaracija
description: Šioje temoje paaiškinama, kaip sukonfigūruoti ir sugeneruoti Egipto PVM grąžinimo formą.
author: sndray
manager: AnnBe
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7859d5a5e3273cd6e55edd1c1ce9fc4699d7ab33
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574339"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Egipto PVM deklaracija (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti ir sugeneruoti PVM grąžinimo formą bei pardavimo ir pirkimo knygas juridiniams subjektams Egipte.

Egipto PVM grąžinimo forma yra oficialus dokumentas, kuriame apibendrinama bendroji mokėtina išeigos PVM suma, visa susigrąžinama įvesties PVM mokesčio suma ir susiję PVM mokesčio sumos įsipareigojimai. Forma naudojama visų tipų mokesčių mokėtojams ir turi būti užpildyta neautomatiniu būdu mokesčių inspekcijos portale. PVM grąžinimo forma paprastai vadinama PVM grąžinimo užklausa.

PVM grąžinimo formoje, esančioje „Dynamics 365 Finance“ yra tokios ataskaitos:

- PVM grąžinimo forma Nr. 10, kuri teikia eilutės elemento sumų, koregavimų ir PVM sumos paskirstymą PVM grąžinimo formoje, kaip aprašyta teisės aktuose.
- Pardavimo operacijų knyga
- Pirkimo operacijų knyga

## <a name="prerequisites"></a>Būtinieji komponentai
Pagrindinis juridinio subjekto adresas turi būti Egipte.
Darbo srityje **Funkcijų valdymas** įjunkite toliau pateikiamą funkciją.

   - (Egiptas) Pardavimo ir pirkimo mokesčių ataskaitos kategorijų hierarchija.

Daugiau informacijos apie tai, kaip įjungti naujas funkcijas, žr. temoje [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Darbo srityje **Elektroninių ataskaitų teikimas** importuokite šį elektroninių ataskaitų teikimo formatą iš saugyklos:

- PVM deklaravimas „Excel“ faile (EG)

> [!NOTE]
> Šis formatas grindžiamas **Mokesčių deklaracijos modeliu** ir naudoja **Mokesčių deklaracijos modelio susiejimą**. Papildomos konfigūracijos bus importuojamos automatiškai.

Daugiau informacijos apie elektroninių ataskaitų teikimo konfigūracijų importavimą, žr. [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektroninių ataskaitų konfigūracijų atsisiuntimas

Egipto PVM grąžinimo formos diegimas grindžiamas elektroninės ataskaitos (ER) konfigūracijomis. Daugiau informacijos apie galimybes ir konfigūruojamų ataskaitų sąvokas žr. [Elektroninių ataskaitų teikimas](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Norėdami rasti gamybos ir naudotojo priėmimo tikrinimo (UAT) aplinkas, žr. [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Norėdami sugeneruoti PVM grąžinimo formą ir susijusias ataskaitas Egipto juridiniame subjekte, įkelkite šias konfigūracijas:

- Mokesčių deklaracija model.version.70.xml arba naujesnė versija
- Mokesčių deklaracija model.mapping.version.70.120.xml arba naujesnė versija
- PVM deklaracijos „Excel“ (EG).version.70.32 ar naujesnė versija

Parsisiuntę ER konfigūracijas iš „Lifecycle Services“ (LCS) arba visuotinės saugyklos, atlikite nurodytus veiksmus.

1. Eikite į darbo sritį **Elektroninės ataskaitos** ir pasirinkite plytelę **Ataskaitų konfigūracijos**.
1. Puslapyje **Konfigūracijos**, veiksmų srityje pasirinkite **Keisti** > **Įkelti iš XML failo**.
1. Įkelkite failus tokia tvarka, kokie jie išvardyti pirmiau. Įkėlus visas konfigūracijas, srityje „Finansai“ turėtų būti konfigūracijos medis.

## <a name="set-up-application-specific-parameters"></a>Konkrečios programos parametrų nustatymas

Konkrečios programos parametrai leidžia nustatyti kriterijus, kaip mokesčių operacijos bus klasifikuojamos ir apskaičiuojamos kiekvienoje eilutėje, kai generuojama ataskaita. Nustatymas paremtas prekės PVM grupės, PVM grupės, PVM kodo ir kitų kriterijų, kurie nustatyti peržvalgos apibrėžime, konfigūracija.

Egipto pardavimo ir pirkimo knygų ataskaitose yra stulpelių rinkinys, atitinkantis konkrečias operacijų klasifikacijas: operacijų tipus, produktus ir dokumentus, būdingus Egiptui. Užuot šias naujas klasifikacijas įtraukus kaip naujus įvesties duomenis, kai paskeliami sandoriai, klasifikacijos apibrėžiamos pagal skirtingas peržvalgas, kurios buvo įvestos pasirinkus **Konfigūracijos** > **Konkrečios programos parametrų nustatymas** > **Sąranka**, atsižvelgiant į Egipto PVM ataskaitų reikalavimus. 

![Konkrečios programos parametrų puslapis](media/egypt-vat-declaration-setup1.png)

Šios peržvalgos konfigūracijos naudojamos klasifikuojant pirkimo ir pardavimo PVM knygų ataskaitų operacijas:

- **PurchaseItemTypeLookup** > O stulpelis: elemento tipas
- **VATRateTypeLookup** > B stulpelis: mokesčio tipas
- **VATRateTypeLookup** > C stulpelis: mokesčio elemento tipas
- **PurchaseOperationTypeLookup** > A stulpelis: dokumento tipas
- **SalesOperationTypeLookup** > N stulpelis: operacijos tipas
- **SalesItemTypeLookup** > O stulpelis: elemento tipas

Norėdami nustatyti skirtingas peržvalgas, naudojamas PVM deklaravimo ir susijusių knygų ataskaitoms generuoti, atlikite nurodytus veiksmus. 

1. Darbo srityje **Elektroninės ataskaitos** pasirinkite **Konfigūracijos** > **Sąranka**, kad nustatytumėte taisykles, skirtas mokesčių operacijai atitinkamame PVM grąžinimo formos laukelyje nustatyti.
2. Pasirinkite dabartinę versiją ir „FastTab“ skirtuke **Peržvalgos** pasirinkite peržvalgos pavadinimą. Pavyzdžiui, **SalesItemTypeLookup**. Ši peržvalga nustato PVM institucijos reikalaujamų klasifikacijų sąrašą pardavimo PVM knygoje.
3. „FastTab“ skirtuke **Sąlygos** pasirinkite **Pridėti** ir naujoje eilutėje, stulpelyje **Peržvalgos rezultatas** pasirinkite susijusią eilutę, kuri vaizduoja klasifikaciją **O stulpelyje**.
4. Stulpelyje **Pardavimų mokesčių grupė** pasirinkite pardavimų mokesčių grupę, kuri naudojama klasifikacijai nustatyti. Pavyzdžiui, **Vidaus SF**. Taip pat galite naudoti prekės PVM grupę, mokesčio kodą arba medžio atributų derinį, jei konfigūracija apibrėžiama kitu būdu. 
5. Stulpelyje **Pavadinimas** pasirinkite mokesčių operacijos klasifikaciją.
6. Visoms galimoms peržvalgoms pakartokite 3–5 veiksmus.
7. Pasirinkite **Pridėti**, jei norite įtraukti paskutinio įrašo eilutę, o stulpelyje **Peržvalgos rezultatas** pasirinkite **Netaikoma**. 
8. Likusiuose stulpeliuose pasirinkite **Ne tuščia**. 

> [!NOTE]
> Pridėję paskutinį įrašą, **Netaikoma**, apibrėžiate tokią taisyklę: kai pardavimų mokesčių grupė, prekių pardavimų mokesčių grupė, mokesčio kodas ir pavadinimas, perduotas kaip argumentas, neatitinka jokių ankstesnių taisyklių, operacijos neįtraukiamos į pardavimų PVM knygą. Nors ši taisyklė naudojama generuojant ataskaitą, taisyklė padeda išvengti ataskaitos generavimo klaidų, kai trūksta taisyklės konfigūracijos.

Toliau pateikiamose lentelėse pateikiamas pavyzdinis aprašytų peržvalgos konfigūracijų siūlomas konfigūravimas. 

**SalesItemTypeLookup**

| Paieškos rezultatas         | Eilutė | PVM grupė    | Prekės PVM grupė    | Mokesčio kodas (kodas) | Pavadinimas / vardas ir (arba) pavardė                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Vietinė              | 1    | VAT_LOCAL          | *Užpildytas*             | *Užpildytas*     | Pardavimas                 |
| Vietinė              | 2    | VAT_LOCAL          | *Užpildytas*             | *Užpildytas*     | Pardavimo kredito pažyma       |
| Vietinė              | 3    | VAT_FINALC         | *Užpildytas*             | *Užpildytas*     | Pardavimas                 |
| Vietinė              | 4    | VAT_FINALC         | *Užpildytas*             | *Užpildytas*     | Pardavimo kredito pažyma       |
| Vietinė              | 5    | VAT_PUBLIO         | *Užpildytas*             | *Užpildytas*     | Pardavimas                 |
| Vietinė              | 6    | VAT_PUBLIO         | *Užpildytas*             | *Užpildytas*     | Pardavimo kredito pažyma       |
| Eksportavimas                | 7    | VAT_EXPORT         | *Užpildytas*             | *Užpildytas*     | Pardavimas                 |
| Eksportavimas                | 8    | VAT_EXPORT         | *Užpildytas*             | *Užpildytas*     | Pardavimo kredito pažyma       |
| Mašina ir įranga | 9    | *Užpildytas*        | VAT_M&E                 | *Užpildytas*     | Pardavimas                 |
| Mašina ir įranga | 10   | *Užpildytas*        | VAT_M&E                 | *Užpildytas*     | Pardavimo kredito pažyma       |
| Dalių mašinos        | 11   | *Užpildytas*        | VAT_PARTS               | *Užpildytas*     | Pardavimas                 |
| Dalių mašinos        | 12   | *Užpildytas*        | VAT_PARTS               | *Užpildytas*     | Pardavimo kredito pažyma       |
| Lengvatos            | 13   | VAT_EXE            | *Užpildytas*           | *Užpildytas*     | SaleExempt            |
| Lengvatos            | 14   | VAT_EXE            | *Užpildytas*           | *Užpildytas*     | SalesExemptCreditNote |
| Netaikoma        | 15   | *Tuščias*            | *Tuščias*                 | VAT_ADJ         | *Užpildytas*           |
| Netaikoma        | 16   | *Užpildytas*        | *Užpildytas*             | *Užpildytas*     | *Užpildytas*           |

 **SalesOperationTypeLookup**

| Paieškos rezultatas  | Eilutė | Prekės PVM grupė    | Mokesčio kodas    | Pavadinimas / vardas ir (arba) pavardė                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Prekės          | 1    | VAT_GOODS               | *Užpildytas* | Pardavimas                 |
| Prekės          | 2    | VAT_GOODS               | *Užpildytas* | Pardavimo kredito pažyma       |
| Prekės          | 3    | VAT_GOODS               | *Užpildytas* | SaleExempt            |
| Prekės          | 4    | VAT_GOODS               | *Užpildytas* | SalesExemptCreditNote |
| Paslaugos       | 5    | VAT_SERV                | *Užpildytas* | Pardavimas                 |
| Paslaugos       | 6    | VAT_SERV                | *Užpildytas* | Pardavimo kredito pažyma       |
| Paslaugos       | 7    | VAT_SERV                | *Užpildytas* | SaleExempt            |
| Paslaugos       | 8    | VAT_SERV                | *Užpildytas* | SalesExemptCreditNote |
| Koregavimai    | 9    | *Tuščias*                 | VAT_ADJ     | Pardavimas                 |
| Koregavimai    | 10   | *Tuščias*                 | VAT_ADJ     | Pirkimas              |
| Netaikoma | 11   | *Užpildytas*             | *Užpildytas* | *Užpildytas*           |

**PurchaseItemTypeLookup**

| Paieškos rezultatas          | Eilutė | Prekės PVM grupė    | Mokesčio kodas    | Pavadinimas / vardas ir (arba) pavardė                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Prekės                  | 1    | VAT_GOODS               | *Užpildytas* | Pirkimas                 |
| Prekės                  | 2    | VAT_GOODS               | *Užpildytas* | PurchaseCreditNote       |
| Paslaugos               | 3    | VAT_SERV                | *Užpildytas* | Pirkimas                 |
| Paslaugos               | 4    | VAT_SERV                | *Užpildytas*  | PurchaseCreditNote       |
| Mašina ir įranga  | 5    | VAT_M&E                 | *Užpildytas* | Pirkimas                 |
| Mašina ir įranga  | 6    | VAT_M&E                 | *Užpildytas* | PurchaseCreditNote       |
| Dalių mašinos         | 7    | VAT_PARTS               | *Užpildytas* | Pirkimas                 |
| Dalių mašinos         | 8    | VAT_PARTS               | *Užpildytas* | PurchaseCreditNote       |
| Lengvatos             | 9    | VAT_EXE                 | *Ne bankas*  | PurchaseExempt           |
| Lengvatos             | 10   | VAT_EXE                 | *Užpildytas* | PurchaseExemptCreditNote |
| Netaikoma         | 11   | *Tuščias*                 | VAT_ADJ     | *Užpildytas*              |
| Netaikoma         | 12   | *Užpildytas*             | *Užpildytas* | *Užpildytas*              |
| Netaikoma         | 13   | *Tuščias*                 | *Užpildytas* | *Užpildytas*              |

**PurchaseOperationTypeLookup**

| Paieškos rezultatas  | Eilutė | PVM grupė  | Mokesčio kodas    | Pavadinimas / vardas ir (arba) pavardė                     |
|----------------|------|------------------|-------------|--------------------------|
| Vietinė       | 1    | VAT_LOCAL        | *Užpildytas* | Pirkimas                 |
| Vietinė       | 2    | VAT_LOCAL        | *Užpildytas* | PurchaseCreditNote       |
| Vietinė       | 3    | VAT_LOCAL        | *Užpildytas* | PurchaseExempt           |
| Vietinė       | 4    | VAT_LOCAL        | *Užpildytas* | PurchaseExemptCreditNote |
| Importuota       | 5    | VAT_IMPORT       | *Užpildytas* | Pirkimas                 |
| Importuota       | 6    | VAT_IMPORT       | *Užpildytas* | PurchaseCreditNote       |
| Importuota       | 7    | VAT_IMPORT       | *Užpildytas* | PurchaseExempt           |
| Importuota       | 8    | VAT_IMPORT       | *Užpildytas* | PurchaseExemptCreditNote |
| Koregavimai    | 9    | *Tuščias*          | VAT_ADJ     | PurchaseCreditNote       |
| Koregavimai    | 10   | *Tuščias*          | VAT_ADJ     | Pirkimas                 |
| Netaikoma | 11   | *Užpildytas*      | *Užpildytas* | *Užpildytas*              |

**VATRateTypeLookup**

| Paieškos rezultatas  | Eilutė | Mokesčio kodas (kodas) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Užpildytas*     |
| SecondTable    | 4    | *Užpildytas*     |
| Netaikoma | 5    | *Užpildytas*     |


## <a name="set-up-general-ledger-parameters"></a>Didžiosios knygos parametrų sąranka

Jei norite generuoti PVM grąžinimo formos ataskaitą „Microsoft Excel“ formatu, apibrėžkite ER formatą puslapyje **Didžiosios knygos parametrai**.

1. Eikite į **Mokesčiai** > **Sąranka** > **Didžiosios knygos parametrai**.
2. Skirtuke **Pardavimų mokestis**, dalyje **Mokesčių parinktys**, laukelyje **PVM išrašo formato išdėstymas** pasirinkite **PVM „Excel“ deklaracija (EG)**. Jei laukelį paliekate tuščią, standartinė pardavimų mokesčių ataskaita bus generuojama SSRS formatu.
3. Pasirinkite **Kategorijų hierarchija**. Ši kategorija įgalina prekių kodą užsienio prekybos skirtuko operacijose, kad naudotojai galėtų pasirinkti ir klasifikuoti prekes ir paslaugas. Šios klasifikacijos aprašas išsamiai aprašytas pardavimo ir pirkimo operacijų ataskaitose. Ši konfigūracija yra pasirenkama.

![Deklaracijos forma](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Generuoti PVM grąžinimo ataskaitą
Laikotarpio PVM grąžinimo ataskaitos paruošimo ir pateikimo procesas yra pagrįstas PVM mokėjimo operacijomis, kurios buvo užregistruotos atliekant sudengimo ir registravimo PVM užduotį. Daugiau informacijos apie pardavimų mokesčio pareiškimą ir ataskaitas žr. skyriuje [Pardavimų mokesčio apžvalga](../general-ledger/indirect-taxes-overview.md).

Atlikite šiuos veiksmus, kad sugeneruotumėte mokesčių deklaracijos ataskaitą.

1. Eikite į **Mokesčiai** > **Deklaracijos** > **Pardavimų mokestis** > **Pardavimų mokesčio ataskaita atsiskaitymo laikotarpiui** arba **Nustatyti ir paskelbti pardavimų mokestį**.
2. Pasirinkite **Atsiskaitymo laikotarpis**.
3. Pasirinkite pradžios datą, tada pasirinkite pardavimų mokesčio mokėjimo versiją.
5. Pasirinkite **Gerai**. 
6. Jei taikoma, įveskite ankstesnio laikotarpio kredito sumą arba palikite sumą kaip nulį.
7. Laukelyje **Ataskaitų duomenys** pasirinkite vieną iš toliau pateiktų parinkčių. 
   - **Pirkimo PVM knyga**: generuoti pirkimo mokesčio operacijų informacijos ataskaitą.
   - **Pardavimų PVM knyga**: generuoti pardavimų mokesčio operacijų informacijos ataskaitą.
   - **PVM deklaracija**: generuoti tik PVM deklaracijos grąžinimo formą.
8. Įveskite asmens, kuris užsiregistravo priskirti formą, vardą ir pavardę.
9. Pasirinkti kalbą. Visos ataskaitos yra verčiamos į **en-us** ir **ar-eg** kalbas.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


