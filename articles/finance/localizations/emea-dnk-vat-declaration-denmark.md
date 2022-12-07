---
title: PVM deklaracija (Danija)
description: Šiame straipsnyje aprašoma, kaip nustatyti ir sugeneruoti Danijos išankstinę pridėtinės vertės mokesčio (PVM) deklaraciją.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 99c8b7a35258116adfe7433e884564d64dbf140f
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812138"
---
# <a name="vat-declaration-denmark"></a>PVM deklaracija (Danija)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti Danijos pridėtinės vertės mokesčio (PVM) deklaraciją ir ją peržiūrėti Microsoft Excel.

Norėdami automatiškai sugeneruoti ataskaitą, pirmiausia sukurkite pakankamai PVM kodų, kad kiekvienai išankstinės PVM deklaracijos laukui būtų išlaikoma atskira PVM apskaita. Be to, elektroninės ataskaitos (ER) formato konkrečiame programos parametre, skirtame išankstinei PVM deklaracijai, susiekite PVM kodus su PVM deklaracijos langų peržvalgos rezultatu.

Turite sukonfigūruoti Danijos ataskaitos **lauko peržvalgą**. Daugiau informacijos apie tai, kaip nustatyti programai brangius parametrus, [žr](#set-up-application-specific-parameters). toliau šiame straipsnyje skyriuje Nustatyti programai brangius PVM deklaravimo laukų parametrus.

Šioje lentelėje stulpelyje Peržvalgos rezultatas rodomas peržvalgos rezultatas, iš anksto sukonfigūruotas tam tikros PVM deklaracijos eilutei PVM deklaracijos formatu. Naudokite šią informaciją, norėdami teisingai susieti PVM kodus su peržvalgos rezultatu, o tada su PVM deklaracijos eilute.

### <a name="vat-declaration-overview"></a>PVM deklaracijos peržiūra

Pvm deklaracijoje Danijoje pateikiama ši informacija.

**Mokėtinas VAT**

| Aprašymas                                                  | Mokesčio bazinė/mokesčio suma | Peržvalgos rezultatas/suma                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pardavimo PVM                                                   | Mokesčių suma          | **IšeigosVAT**</br> **DomesticVATUseTax** (taip pat pranešta lauke "Įvesties PVM")                                                                                                                                                                                                                                                                       |
| PVM prekėms ir pan. Nupirkta už užsienio                           | Mokesčių suma          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (taip pat pranešta lauke "Įvesties PVM")</br>**PurchaseGoodsEU** (Mokesčių pagrindas paskelbtas "A langelis – prekių įsigijimas").</br>**PurchaseGoodsEUUseTax** (Mokesčių suma taip pat pateikiama langelyje Įvesties PVM). Mokesčio pagrindas paskelbtas "A langelis – prekių įsigijimas").                   |
| Užsienyje įsigytų paslaugų PVM taikomas atvirkštinis mokestis | Mokesčių suma          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (taip pat pranešta lauke "Įvesties PVM")</br>**PurchaseServicesEU** (Mokesčių pagrindas praneštas "A langelis – paslaugų įsigijimas")</br>**PurchaseServicesEUUseTax** (Mokesčių suma taip pat pateikiama langelyje Įvesties PVM). Mokesčių bazė pranešama "A langelis – paslaugų įsigijimas") |
| Iš viso mokėtinų sumų                                                | Mokesčių suma          | Ankstesnių trijų langelių suma                                                                                                                                                                                                                                                                                                            |

**Atskaitymai**

| Aprašymas                                                                               | Mokesčio bazinė/mokesčio suma | Peržvalgos rezultatas/suma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pirkimo PVM                                                                                 | Mokesčių suma          | **ĮvestiesVAT**</br> **DomesticVATUseTax** (taip pat pranešta lauke Išeigos PVM)</br>**PurchaseGoodsAbroadUseTax** (taip pat pateikiama "PVM prekėms ir kt." Nupirkta į užsienį")</br>**PurchaseServicesAbroadUseTax** (taip pat paskelbtas "PVM už užsienio įsigytas paslaugas, kurioms taikomas atvirkštinis mokestis")</br>**PurchaseGoodsEUUseTax** (taip pat pateikiama "PVM prekėms ir kt." Nupirkta į užsienį")</br> **PurchaseServicesEUUseTax** (taip pat paskelbtas "PVM už užsienio įsigytas paslaugas, kurioms taikomas atvirkštinis mokestis") |
| Naftos ir dujų balionų mokestis                                                                  | Mokesčių suma          | **NaftaGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Maitinimo / muito mokestis                                                                    | Mokesčių suma          | **PowerElectricityDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Gamtinių dujų ir miesto dujų mokestis                                                             | Mokesčių suma          | **NaturalGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Anglies mokestis                                                                               | Mokesčių suma          | **Tam, kad būtų galima užeiti**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Mokesčių suma          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vandens mokestis                                                                              | Mokesčių suma          | **Vandenženklis**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Bendroji atskaitymų suma                                                                          | Mokesčių suma          | Ankstesnių šešių langelių suma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Bendra muitų suma (teigiama suma = atlikti mokėjimą, neigiama suma = grąžinami pinigai) | Mokesčių suma          | "Bendroji mokėtina suma" – "Visi atskaitymai"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Papildoma informacija**

| Aprašymas                                                                                                                                                                                                                                | Mokesčio bazinė/mokesčio suma | Peržvalgos rezultatas/suma                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| A langelis – prekių įsigijimas. Vertė be prekių įsigijimo Sąjungos viduje PVM.                                                                                                                                                   | Mokesčių bazė            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| A langelis – paslaugų įsigijimas. Vertė be ES vidaus paslaugų įsigijimo PVM.                                                                                                                                             | Mokesčių bazė            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| B langelis – prekių tiekimas – turi būti pranešta "ES pardavimas be PVM" / DK PREKIŲ tiekimas. Vertė be PREKIŲ tiekimo Sąjungos viduje PVM                                                                                                           | Mokesčių bazė            | **SalesGoodsEU**                                |
| B langelis – atsargos – nereikia pranešti "ES pardavimas be PVM" / DK PREKIŲ. Tam tikrų vidaus tiekimo (pvz., diegimo, surinkimo, atstumo pardavimo ir naujų transporto priemonių neapmokestinamiems asmenims) vertė be PVM. | Mokesčių bazė            | **SalesInstallationAssemblyEtcEU**              |
| B langelis – paslaugų tiekimas. Vertė be JAV vidaus paslaugų, už kurias pirkėjas gali mokėti PVM kaip atvirkštinį mokestį, PVM turi būti paskelbta "ES pardavimas be PVM" / DK VIES.                          | Mokesčių bazė            | **SalesServicesEU**                             |
| C langelis – kiti ištekliai. Kitų prekių ir paslaugų, teikiamų be PVM Danijos teritorijoje, į kitas ES valstybes nares ir į trečiąjas šalis arba trečiąjas teritorijas, tiekimo vertė.                                     | Mokesčių bazė            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Pirkimo atvirkštinio apmokestinimo PVM

Jei konfigūruojate PVM kodus, norėdami registruoti gaunamą atvirkštinį PVM naudodami naudojimo mokestį, **susiekite** savo PVM kodus su ataskaitos lauko peržvalgos rezultatu, kuriame yra "UseTax" pavadinime.

Kitaip, galite konfigūruoti du atskirus PVM kodus: vieną mokėtinam PVM ir kitą PVM atskaitymui. Tada kiekvieną kodą susieti su atitinkamais ataskaitos lauko peržvalgos **rezultatais**.

Pavyzdžiui, **apmokestinamų įsigijimų bendrijos viduje atveju konfigūruojate PVM kodą UT_S_EU**  **naudojimo mokesčiu ir susiejate jį su PurchaseGoodsEUUseTax**  **ataskaitos lauko peržvalgos rezultatu**. Šiuo atveju mokesčių sumos, kurios naudoja **UT_S_EU** PVM kodą, yra rodomos "PREKIŲ PVM ir t. t. Užsienio pirktos prekės" ir "Įvesties PVM". Mokesčių bazės atsispindi "A langelis – prekių įsigijimas".

Taip pat konfigūruojate du PVM kodus:

- **VAT_S_EU**, kurios mokesčių tarifo vertė yra -25 procentai
- **InVAT_S_EU**, kurios mokesčio tarifo vertė yra 25 procentai

Tada kodus su ataskaitos lauko peržvalgos **rezultatais susiejate** tokiu būdu:

- Susieti **VAT_S_EU** su **PurchaseGoodsEU** peržvalgos rezultatu.
- Susieti **InVAT_S_EU** su **InputVAT** peržvalgos rezultatu.

Šiuo atveju sumos, kurios naudoja **VAT_S_EU** PVM kodą, yra rodomos "PREKIŲ PVM ir t. t. Nupirkta užsienyje" ir "A langelis – prekių įsigijimas". Sumos, kurios **InVAT_S_EU** PVM kodą, rodomos lauke Įvesties PVM.

Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti atvirkštinį PVM, žr. Atvirkštinį [apmokestinimą](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigūruoti sistemos parametrus

Norėdami generuoti PVM deklaraciją, turite sukonfigūruoti PVM numerį.

1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
2. Pasirinkite juridinį subjektą, tada **pasirinkite registracijos PVM**.
3. Pasirinkite arba sukurkite adresą Danijoje, tada registracijos **ID** "FastTab" pasirinkite **Įtraukti**.
4.  **Lauke Registracijos tipas** pasirinkite Danijai skirtą registracijos tipą, kuris naudoja **PVM ID registracijos** kategoriją.
5. Į registracijos **numerio** lauką įveskite mokesčio numerį.
6.  **Skirtuko Bendra** lauke **Įsigalioja įveskite** datą, nuo kurios numeris įsigalioja.

Daugiau informacijos apie tai, kaip nustatyti registracijos kategorijas ir registracijos tipus [, ieškokite registracijos ID](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Nustatyti Danijos PVM deklaracijos peržiūrą

### <a name="import-er-configurations"></a>Importuokite ER konfigūracijas

Atidarykite **elektroninės ataskaitos darbo** sritį ir importuokite **PVM deklaracijos Excel (DK)** ER formatą.

Daugiau informacijos žr. [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a> Nustatyti konkrečios programos parametrus PVM deklaracijos laukams

> [!NOTE]
> Rekomenduojame įgalinti funkciją, **Funkcijų valdymo darbo srityje naudokite ankstesnių ER formatų versijų** darbo srityje **Funkcijų valdymas**. Įgalinus šią funkciją, parametrai, kurie sukonfigūruoti naudoti su ankstesne ER formato versija, automatiškai tampa taikoma vėlesnei to paties formato versijai. Jei ši funkcija neįgalinta, turite konkrečiai konfigūruoti kiekvienos formato versijos parametrus, būruojat konkrečius programos parametrus. Rekomenduojame įgalinti funkciją, **Funkcijų valdymo darbo srityje naudokite ankstesnių ER formatų versijų** funkcija yra prieinama darbo srityje **Funkcijų valdymas** „Finance“ 10.0.23 versijoje. Daugiau informacijos apie tai, kaip nustatyti kiekvieno juridinio subjekto ER formato parametrus, ieškokite juridinio [subjekto ER formato parametrų nustatymas](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Norėdami automatiškai sugeneruoti PVM deklaraciją, susiekite PVM kodus programoje ir peržvalgos rezultatus ER konfigūracijoje.

Norėdami nurodyti, kurie PVM kodai generuoja PVM deklaracijos langelius, atlikite šiuos veiksmus.

1. Eikite **į darbo sritis** > **– elektroninės** ataskaitos ir pasirinkite **ataskaitų konfigūracijas**.
2. Pasirinkite PVM **deklaracijos Excel (DK)**  konfigūraciją, tada pasirinkite Konfigūravimų **specialios \> programos parametrų nustatymą**.
3. Konkretaus programos **parametrų puslapio** Peržvalgos **"FastTab"** pasirinkite Ataskaitos **lauko peržvalga**.
4. Sąlygų FastTab **nustatykite** šiuos laukus, norėdami susieti PVM kodus ir ataskaitos laukus.

    | Laukas                  | Aprašymas                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Paieškos rezultatas          | Pasirinkti ataskaitos lauko vertę. Daugiau informacijos apie vertes ir jų priskyrimą PVM deklaracijos eilutėms žr. [anksčiau šiame straipsnyje skyriuje](#vat-declaration-overview) PVM deklaracijos apžvalga.                                                                                               |
    | Mokesčio kodas               | Pasirinkti PVM kodą, kuris bus susietas su ataskaitos lauku. Užregistruotos mokesčių operacijos, kurios naudoja pasirinktą PVM kodą, bus surinktos atitinkamą deklaracijos langelį. Rekomenduojame atskirti PVM kodus taip, kad vienas PVM kodas sugeneruotų sumas tik viename deklaracijos langelyje. |
    | Operacijų klasifikatorius | Jei sukūrėte pakankamai PVM kodų deklaracijos laukui nustatyti, pasirinkite **\*Neužpildyti\***. Jei nesukurėte pakankamai PVM kodų, kad vienas PVM kodas sugeneruotų sumas tik viename deklaravimo langelyje, galite nustatyti operacijų klasifikatorius. Galimos šios operacijų klasės:</br>-   **Pirkimas**</br>-   **PurchaseExempt**  (neapmokestinamas pirkimas)</br>-   **PurchaseReverseCharge**  (gautinas mokestis iš pirkimo atvirkštinio apmokestinimo)</br>-   **Pardavimas**</br>-   **SalesExempt**  (neapmokestinamas pardavimas)</br>-   **SalesReverseCharge**  (mokėtinas mokestis iš pirkimo atvirkštinio mokesčio arba atvirkštinio pardavimo mokesčio)</br>-   **Naudojimo mokestis**. </br>Taip pat galima naudoti kiekvieno operacijų klasifikatorius kredito pažymos klasifikatorius. Pavyzdžiui, vienas iš šių klasių yra **PurchaseCreditNote** (pirkimo kredito pažyma).</br>Įsitikinkite, kad sukurkite dvi eilutes kiekvienam PVM kodui: vieno, kuris turi operacijos klasifikatorius vertę, ir vieno, kuris turi kredito pažymos vertės operacijos klasifikatorius, eilutes. |


    > [!NOTE]
    > Susieti visus PVM kodus su peržvalgos rezultatais. Jei PVM kodai neturi generuoti verčių PVM deklaracijoje, susiekite juos su **kita** peržvalgos rezultatu.

    ![Konkrečios programos parametrų puslapis.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Būsenos lauke **pakeiskite** vertę į **Baigta**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Pvm ataskaitos formato nustatymas "Excel" peržiūrėti sumas

1. Funkcijų valdymo **darbo srityje** raskite ir pasirinkite PVM išrašo **formato ataskaitas.** Sąraše <a0/& pasirinkite Įgalinti **dabar**.
2. Eikite **į DK** > **nustatymo** > **DK parametrus**.
3. Skirtuke **PVM**, **mokesčių** pasirinkčių "FastTab", **PVM** išrašo formato susiejimo lauke, **pasirinkite PVM deklaracijos Excel (DK)** ER formatą.

   Šis formatas spausdinamas, kai paleidžiate sudengimo **laikotarpio ataskaitos PVM** ataskaitą. Jis taip pat spausdinamas PVM mokėjimų **puslapyje** pasirinkus **Spausdinti**.

4. Mokesčių inspekcijos **puslapyje** pasirinkite mokesčių inspekciją, tada lauke Ataskaitos maketas **pasirinkite** Numatytasis **·**.

Jei konfigūruojate PVM deklaraciją juridiniame subjekte, kuriame yra kelios [PVM registracijos](emea-reporting-for-multiple-vat-registrations.md), atlikite šiuos veiksmus.

1. Eikite į **Didžioji knyga** \> **nustatymas** \> **DK parametrai**.
2. Skirtuko PVM **šalių**  **/** regionų "FastTab **" elektroninės ataskaitos DNK** eilutėje pasirinkite **PVM deklaracijos Excel (DK)** ER formatą.

## <a name="set-up-electronic-messages"></a>Nustatyti elektroninius pranešimus

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Atsisiųskite ir importuokite duomenų paketą, kuriame yra elektroninių pranešimų pavyzdinių parametrų

Duomenų pakete yra elektroninio pranešimo parametrai, naudojami PVM deklaracijai peržiūrėti programoje "Excel". Galite išplėsti šiuos parametrus arba sukurti savo. Norėdami gauti daugiau informacijos apie tai, kaip dirbti su elektroniniais pranešimais ir kurti savo parametrus, žr. Elektroninių [pranešimų siuntimo informaciją](../general-ledger/electronic-messaging.md).

1. Ciklo [Microsoft Dynamics tarnybų (LCS)](https://lcs.dynamics.com/v2) bendrai naudojamų turtų bibliotekoje pasirinkite Duomenų paketas kaip turto tipą, **·**  **tada atsisiųskite DK PVM deklaracijos paketą.** Atsisiųstas failas yra pavadintas **DK PVM deklaracijos package.zip**.
2. Duomenų valdymo darbo srityje finansai **pasirinkite** Importuoti **·**.
3.  **Skirtuko Importo** FastTab lauke **Grupės** pavadinimas įveskite užduoties pavadinimą.
4. „FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti failą**.
5. Dialogo lange **Įtraukti failą** patikrinkite, **ar šaltinio duomenų formato**  **laukas** nustatytas kaip Pakuotė, pasirinkite Įkelti ir įtraukti, **tada** pasirinkite anksčiau atsisiųstą pašto failą.
6. Pasirinkite **Uždaryti**.
7. Kai duomenų objektai įkeliami, veiksmų srityje pasirinkite **Importuoti**.
8. Eikite į **mokesčių** > **užklausas ir ataskaitas Elektroniniai** > **pranešimai** > **Elektroniniai** pranešimai ir patikrinkite importuoto elektroninio pranešimo apdorojimą (**DK PVM deklaracija**).

### <a name="configure-electronic-messages"></a>Konfigūruoti elektroninius pranešimus

1. Eikite į **mokesčių** > **nustatymo elektroninius** > **pranešimus** > **užpildyti įrašų veiksmus**.
2. Pasirinkite DK automatiškai įvesti **PVM grąžinimo įrašų eilutę,** tada pasirinkite užklausą **Redaguoti**.
3. Naudodami filtrą nurodykite sudengimo laikotarpius, kurie bus įtraukti į ataskaitą.
4. Jei turite pateikti kitų sudengimo laikotarpių mokesčių operacijas kitoje deklaracijoje, **sukurkite naują veiksmą Automatiškai įvesti įrašus** ir pasirinkite atitinkamus sudengimo laikotarpius.

## <a name="preview-the-vat-declaration-in-excel"></a>Peržiūrėti PVM deklaraciją programoje "Excel"

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a> Peržiūrėti PVM deklaraciją "Excel" iš sudengimo laikotarpio periodinės užduoties ataskaitos PVM

1. Eiti į **Mokesčių periodines** > **užduotis** > **Deklaracijos** > **PVM ataskaita** > **sudengimo laikotarpiui**.
2. Lauke Sudengimo **laikotarpis** pasirinkite vertę.
3.  **PVM mokėjimo versijos lauke pasirinkite** vieną iš šių verčių:

    - **Pradinis**: generuoti pradinio PVM mokėjimo operacijų arba prieš PVM mokėjimą ataskaitą.
    - **Taisy** įrašai: generuoti visų vėlesnių laikotarpio PVM mokėjimų PVM operacijų ataskaitą.
    - **Bendras sąrašas**: sugeneruokite visų laikotarpio PVM operacijų ataskaitą, įskaitant originalius ir visus pataisymus.

4.  **Lauke Pradžios data** pasirinkite ataskaitinio laikotarpio pradžios datą.
5. Pasirinkite **Gerai** ir peržiūrėkite Excel ataskaitą.

### <a name="settle-and-post-sales-tax"></a>Sudengti ir užregistruoti PVM

1. Eiti į mokesčių periodines **užduotis** > **Deklaracijos** > **PVM sudengimas** > **ir registruoti PVM** > **.**
2. Lauke Sudengimo **laikotarpis** pasirinkite vertę.
3.  **PVM mokėjimo versijos lauke pasirinkite** vieną iš šių verčių:

    - **Pradinis**: sugeneruokite pradinį sudengimo laikotarpio PVM mokėjimą.
    - **Naujausi koregavimai: sugeneruokite pataisymų PVM mokėjimą po to, kai buvo sukurtas** pradinis sudengimo laikotarpio PVM mokėjimas.

4.  **Lauke Pradžios data** pasirinkite ataskaitinio laikotarpio pradžios datą.
5. Pasirinkite **Gerai**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Peržiūrėti PVM deklaraciją Programoje "Excel" iš PVM mokėjimo

1. Eikite **·** > **į mokesčių užklausas ir** > **ataskaitas PVM** > **užklausas** PVM mokėjimams ir pasirinkite PVM mokėjimo eilutę.
2. Pasirinkite **Spausdinti ataskaitą** ir tada pasirinkite **Gerai**.
3. Peržiūrėkite "Excel" failą, sugeneruotą pasirinktai PVM mokėjimo eilutei.

> [!NOTE]
> Ataskaita generuojama tik pagal pasirinktą PVM mokėjimo eilutę. Jei turite sugeneruoti, pvz., koreguojamą deklaraciją, kurioje yra visi laikotarpio pataisymai, arba pakeitimo deklaraciją, kurioje yra pradiniai duomenys ir visi pataisymai, **sudengimo** laikotarpio periodinę užduotį naudokite ataskaitą PVM.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generuoti PVM deklaraciją iš elektroninių pranešimų

Kai naudojate elektroninius pranešimus ataskaitai generuoti, galite rinkti mokesčių duomenis iš kelių juridinių subjektų. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr. skyrių Paleisti kelių](#run-vat-declaration) juridinių subjektų PVM deklaraciją.

Toliau pateikta procedūra taikoma elektroninių pranešimų apdorojimo pavyzdžiui, kurį importavote anksčiau iš LCS bendrinamo turto bibliotekos.

1. Eikite į **mokesčių \> užklausas ir ataskaitas Elektroniniai \>  \> pranešimai**.
2. Kairiajame lange pasirinkite **DK PVM deklaraciją**.
3. Pranešimų FastTab **pasirinkite** Naujas **·**, tada dialogo lange **Vykdyti apdorojimą** pasirinkite **Gerai**.
4. Pasirinkite sukurtą pranešimo eilutę, įveskite aprašymą, tada nurodykite deklaracijos pradžios ir pabaigos datas.

   > [!NOTE]
   > 5–7 žingsniai nėra privalomi.

5. Nebūtina: " **FastTab" Pranešimuose** pasirinkite **Rinkti duomenis**, tada pasirinkite **Gerai**. Anksčiau sugeneruoti PVM mokėjimai įtraukiami į pranešimą. Norėdami gauti daugiau informacijos, žr. [anksčiau šiame straipsnyje skyriuje Sudengti](#settle-and-post-sales-tax) ir užregistruoti PVM. Jei praleisite šį veiksmą, vis tiek galėsite **generuoti PVM deklaraciją naudodami mokesčių deklaracijos** versijos lauką, kuris **yra deklaracijos** dialogo lange.
6. Nebūtina: Pranešimo **prekių "** FastTab" peržiūrėkite PVM mokėjimus, kurie perkelti apdoroti. Pagal numatytuosius nustatymus įtraukiami visi pasirinkto laikotarpio PVM mokėjimai, kurie nebuvo įtraukti į kitus to paties apdorojimo pranešimus.
7. Pasirinktinai: pasirinkite **originalų dokumentą**, kad peržiūrėtumėte PVM mokėjimus, **arba pasirinkite Naikinti,** norėdami neįtraukti PVM mokėjimų į apdorojimą. Jei praleisite šį veiksmą, vis tiek galėsite **generuoti PVM deklaraciją naudodami mokesčių deklaracijos** versijos lauką, kuris **yra deklaracijos** dialogo lange.
8. Pranešimų " **FastTab**" pasirinkite Atnaujinimo **būseną**. Būsenos atnaujinimo **dialogo** lange pasirinkite Parengta **generuoti**, tada pasirinkite **Gerai**. Patikrinkite, ar pranešimo būsena pakeista į Parengta **generuoti**.
9. Pasirinkite **Generuoti ataskaitą**. Norėdami peržiūrėti PVM deklaracijos sumas, dialogo **lange Vykdyti** apdorojimą **pasirinkite Peržiūrėti ataskaitą**, tada pasirinkite **Gerai**.
10. Elektroninių ataskaitų **parametrų** dialogo lange nustatykite laukus, [kaip aprašyta PVM deklaracijos "Excel](#preview-vat-excel) " dalyje Iš anksčiau šiame straipsnyje skyriuje "Sudengimo laikotarpio periodinės užduoties ataskaitos PVM" ir pasirinkite **Gerai**.
11. Viršutiniame **dešiniajame** puslapio kampe pasirinkite **mygtuką** Priedai (popieriaus paveikslėlio simbolis), tada pasirinkite Atidaryti, kad atidarytumėte failą. Peržiūrėkite Excel dokumento sumas.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a> Vykdyti PVM deklaraciją keliems juridiniams subjektams

Norėdami naudoti formatus norėdami juridinių subjektų grupei pateikti PVM deklaraciją, pirmiausia turite nustatyti nuo programos konkrečius PVM kodų formato parametrus iš visų reikalaujamo juridinio subjekto.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Nustatyti elektroninius pranešimus siekiant surinkti mokesčių duomenis iš kelių juridinių subjektų

Norėdami nustatyti elektroninius pranešimus duomenims iš kelių juridinių subjektų rinkti, atlikite šiuos veiksmus.

1. Eikite į **darbo sričių** > **funkcijų valdymą**.
2. Raskite ir pasirinkite **visos įmonės užklausas, skirtas automatiškai įvesti įrašų** veiksmų funkciją sąraše, tada pasirinkite Įgalinti **dabar**.
3. Eikite į **mokesčių** > **nustatymo elektroninius** > **pranešimus** > **užpildyti įrašų veiksmus**.
4. Veiksmų puslapyje **Automatiškai įvesti įrašus** pasirinkite DK automatiškai įvesti **PVM grąžinimo įrašų eilutę**.

   Duomenų šaltinių **nustatymo tinklelyje** galimas **naujas** laukas Įmonė. Šiame lauke rodomas esamų juridinių subjektų identifikatorius esamiems įrašams.

5. Duomenų šaltinių **nustatymo tinklelyje** pridėkite kiekvieno papildomo juridinio subjekto, kuris turi būti įtrauktas į ataskaitą, eilutę. Kiekvienai naujai eilutei nustatykite šiuos laukus.

    | Laukas                  | Aprašymas                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Pavadinimas / vardas ir pavardė                   | Įveskite vertę, kuri padės suprasti, iš kur gaunamas šis įrašas. Pavyzdžiui, įveskite filialo **1 PVM mokėjimą**. |
    | Pranešimo prekės tipas      | Pasirinkti **PVM grąžinimą**. Ši vertė yra vienintelė galima visų įrašų vertė.                                    |
    | Kodo tipas           | Žymėti **viską**.                                                                                                               |
    | Pagrindinės lentelės pavadinimas      | Nurodykite **TaxReportVoucher** visiems įrašams.                                                                             |
    | Laukas Dokumento numeris  | Nurodyti **kvitą** visiems įrašams.                                                                                      |
    | Laukas Dokumento data    | Nurodyti **visų įrašų TransDate** .                                                                                    |
    | Laukas Dokumento sąskaita | Nurodyti **TaxPeriod** visiems įrašams.                                                                                    |
    | Įmonė                | Pasirinkite juridinio subjekto ID.                                                                                            |
    | Vartotojo užklausa             | Šis žymės langelis automatiškai pasirenkamas, kai pasirenkate kriterijus pasirinkdami Redaguoti **užklausą**.                                 |

6. Kiekvienoje naujoje eilutėje pasirinkite **Redaguoti užklausą** ir **nurodykite** susijusį juridinio subjekto, nurodyto eilutės lauke Įmonė, sudengimo laikotarpį.

Kai nustatymas baigtas, elektroninių **pranešimų puslapyje**  **nurodyta** duomenų rinkimo funkcija surenka PVM mokėjimus iš visų jūsų nurodytų juridinių subjektų.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
