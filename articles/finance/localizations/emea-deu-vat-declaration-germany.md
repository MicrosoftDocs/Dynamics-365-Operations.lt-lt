---
title: PVM deklaracija (Vokietija)
description: Šiame straipsnyje aprašoma, kaip nustatyti ir generuoti Vokietijos išankstinę pridėtinės vertės mokesčio (PVM) deklaraciją oficialiu XML formatu.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 04c625b554d96f8ed28ceffef9647fe9cbf7fe2f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689466"
---
# <a name="vat-declaration-germany"></a>PVM deklaracija (Vokietija)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti ir generuoti Vokietijos išankstinę pridėtinės vertės mokesčio (PVM) deklaraciją oficialiu XML formatu. Šiame straipsnyje taip pat paaiškinama, kaip peržiūrėti PVM deklaraciją Microsoft Excel.

Norėdami automatiškai sugeneruoti ataskaitą, sukurkite pakankamai PVM kodų, kad kiekvienas išankstinio PVM deklaravimo laukas būtų atskiras PVM apskaita. Be to, elektroninės ataskaitos (ER) formato konkrečiame programos parametre, skirtame išankstinei PVM deklaracijai, susiekite PVM kodus su PVM deklaracijos langų peržvalgos rezultatu.

Vokietijoje turite konfigūruoti lauko **Ataskaitos peržvalgą**. Daugiau informacijos apie tai, kaip nustatyti programai brangius parametrus, [žr](#set-up-application-specific-parameters-for-vat-declaration-fields). toliau šiame straipsnyje skyriuje Nustatyti programai brangius PVM deklaravimo laukų parametrus.

Šioje lentelėje stulpelyje Peržvalgos rezultatas rodomas peržvalgos rezultatas, iš anksto sukonfigūruotas tam tikros PVM deklaracijos eilutei PVM deklaracijos formatu. Naudokite šią informaciją, norėdami teisingai susieti PVM kodus su peržvalgos rezultatu, o tada su PVM deklaracijos eilute.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a> PVM deklaracijos peržiūra

Išankstinėje PVM deklaracijoje Vokietijoje yra ši informacija.

**SKYRIUS – PRISTATYMAI IR KITOS PASLAUGOS**

**Apmokestinami pardavimai**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                                                                                                                      | Paieškos rezultatas                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Be kodo     | Apmokestinami pardavimai, kurių mokesčio tarifas yra 19 procentų.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – su minuso ženklu             |
| 21  | 86             | Be kodo     | Apmokestinami pardavimai, kurių mokesčio tarifas yra 7 procentai.                                                                                                        | 21-TaxableSalesRe su rastos</br>73-BadDebtsWriteOffRepres (86/50) – su minuso ženklu               |
| 22  | 35             | 36               | Apmokestinamas pardavimas pagal kitus mokesčių tarifus.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – su minuso ženklu      |
| 23  | 77             | *Mokesčio sumos nėra*  | Pristatymai iš žemės ūkio ir veiklos pagal Vokietijos PVM akto (UStG) nr. y.24 PVM aktą klientams, kurie turi PVM ID numerį. | 23–EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – su minuso ženklu |
| 24  | 76             | 80               | Pardavimai, už kuriuos turi būti mokamas mokestis pagal UStG (*)24 iš UStG (toliau – "šiuo metu gauti produktai, operacijos ir bazės").                                | 24–SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Neapmokestinami pardavimai su pirkimo mokesčio atskaita**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                                                       | Paieškos rezultatas                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Mokesčio sumos nėra*  | ES vidaus pristatymai klientams, kurie turi PVM ID.                       | 26–EUSales                          |
| 27  | 44             | *Mokesčio sumos nėra*  | Naujų transporto priemonių pristatymas ES vidaus prekybai pirkėjams, neturint PVM ID.    | 27–EUSalesNewVehicles               |
| 28  | 49             | *Mokesčio sumos nėra*  | Naujų transporto priemonių, o ne įmonės vidaus pristatymai.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Mokesčio sumos nėra*  | Kiti neapmokestinami pardavimai, kurių įvesties mokesčio atskaitymai, pvz., eksporto pristatymai. | 29-ExportOtherTaxFreeSales          |

**Neapmokestinami pardavimai be pirkimo mokesčio atskaitos**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                            | Paieškos rezultatas                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Mokesčio sumos nėra*  | Neapmokestinami pardavimai, kurie neturi įvesties mokesčio atskaitymo. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Įsigijimai Bendrijos viduje**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                                                                                                   | Paieškos rezultatas                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Mokesčio sumos nėra*  | Neapmokestinami kai kurių objektų ir investicijų auksinės spalvos įsigijimai ES viduje.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Be kodo     | Apmokestinami įsigijimai bendrijos viduje, kai mokesčio tarifas yra 19 procentų.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Be kodo     | Apmokestinami įsigijimai bendrijos viduje, kai mokesčio tarifas yra 7 procentai.                                                              | 35-EUPurchaseRe sue su retuoju</br>35-UseTaxEUPurchaseRe sue objektų (93/61)          |
| 36  | 95             | 98               | Apmokestinami įsigijimai bendrijos viduje pagal kitus mokesčių tarifus.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Apmokestinami naujų transporto priemonių įsigijimai bendrijos viduje iš tiekėjų, kurie neturi PVM ID numerio, esant bendrajam mokesčių tarifui. | 37–EUPurchaseVehicles</br>37– UseTaxEUPurchaseVehicles (94/96/61)     |

**SKYRIUS – GAVĖJAS KAIP MOKESČIŲ SKOLININKAS**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                                                        | Paieškos rezultatas                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Kitos esamu bendrijos lygiu paremtos paslaugos.        | 40 – BeneficiaryTaxDebtor</br>40- UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Pardavimas, kuris patenka į 13b (2) skyriaus Nr. 3 UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Kitos paslaugos, kurios patenka į 13b (2) skyriaus Nr. Nuo 1, 2 ir 4 iki 12 UStG. | 42–BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**SKYRIUS – PAPILDOMA PARDAVIMO INFORMACIJA**

| Eilutė | Langelis – mokesčių bazė  | Langelis – mokesčio suma | Aprašymas                                                                                                | Paieškos rezultatas                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Mokesčio sumos nėra*  | Pirmojo kliento pristatymai ES vidaus trišalių operacijų atveju.                   | 48 - pristatymaiFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Mokesčio sumos nėra*  | Apmokestinami atlikimo operacijos pardavimai, pagal kuriuos aptarnavimo gavėjas skolingas mokesčius. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Mokesčio sumos nėra*  | Kitos neapmokestinamos paslaugos.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Mokesčio sumos nėra*  | Kitas neapmokestinamas pardavimas, kai našumo vieta nėra Vokietijoje.                                    | 51–OtherSalesNonTaxable                                                                          |
| 52  | *Mokesčio sumos nėra* | *Mokesčio sumos nėra*  | PVM.                                                                                                       | 20 eilutė + 21 eilutė + 22 eilutė + 2 4 eilutė + 34 eilutė + 35 eilutė + 36 eilutė + 37 eilutė + 40 eilutė + 41 eilutė + 42 eilutė |

**SKYRIUS – ATSKAITOMAS ĮVESTIES MOKESTIS**

| Eilutė | Langelis – mokesčio suma | Aprašymas                                                                                                | Paieškos rezultatas                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Įvesties SF mokesčių sumos iš kitų įmonių, paslaugų ir ES vidaus trišalės operacijos.     | 55 – InputTax 40 – UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – su minuso ženklu                                                                   |
| 56  | 61               | Įvesties mokesčio sumos, gautos įsigyjant prekes ES viduje.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseRe sue objektų (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37– UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Patirtų išlaidų importo PVM.                                                                                 | 57– InputTaxImport                                                                                                                                                            |
| 58  | 67               | Įeimo mokesčio sumos iš paslaugų, kaip nurodyta UStG .13b.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Įvesties mokesčio sumos, skaičiuojamos pagal bendrąjį vidurkį.                                  | 59 – InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – su minuso ženklu                                                                                    |
| 60  | 59               | Įvesties mokesčio atskaitymas, taikomas esamam naujų transporto priemonių pristatymui už įmonės ribų ir smulkioms įmonėms. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – su minuso ženklu                                                                  |
| 61  | 64               | Įvesties mokesčio atskaitymo koregavimas.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Likusi suma.                                                                                      | 52 eilutė – 55 eilutė – 56 eilutė – 57 eilutė – 58 eilutė – 50 eilutė – 60 eilutė – 61 eilutė                                                                                                        |

**SKYRIUS – KITOS MOKESČIŲ SUMOS**

| Eilutė | Langelis – mokesčio suma | Aprašymas                                                                                                                                                                                                                                                         | Paieškos rezultatas                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Mokestis dėl apmokestinimo formos pakeitimo ir papildomo apmokestinamų mokėjimus apmokestinamo mokesčio, nes pasikeistų mokesčių tarifas.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Neteisingos arba neteisingos mokesčių sumos, rodomos SF, ir mokesčių sumos, kurias skolingas pagal 6a (4) skyrių 2, 17 (1) skyrius, 7 skyrius arba UStG 25b (2) skyrius arba kurias skolingas užsakomųjų paslaugų įmonė ar sandėlio finansininkas. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Nuolatinio plėtinio fiksuoto specialaus išankstinio mokėjimo atskaitymas. Ši eilutė paprastai užpildoma tik paskutiniu išankstiniu mokesčių laikotarpio pranešimu.                                                                                                  | Vartotojo įvesties parametras ataskaitos dialogo lange |
| 68  | 83               | Likęs išankstinis PVM mokėjimas ir likęs perviršis. Prieš sumą įtraukti minuso žurnalą.                                                                                                                                                          | 62 eilutė + 64 eilutė – 65 eilutė – 66 eilutė             |

**SKYRIUS – PAPILDOMA INFORMACIJA APIE SUMAŽINIMUS**

| Eilutė | Langelis – mokesčių bazė | Langelis – mokesčio suma | Aprašymas                                                            | Paieškos rezultatas                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Mokesčio pagrindo sumažinimas nuo 20 iki 24 eilučių.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffRepres (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Atskaitomų įvesties mokesčių sumų sumažinimas 55, 59 ir 60 eilutėse. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Pirkimo atvirkštinio apmokestinimo PVM

Jei konfigūruojate PVM kodus, norėdami registruoti gaunamą atvirkštinį PVM naudodami naudojimo mokestį, **susiekite** savo PVM kodus su ataskaitos lauko peržvalgos rezultatu, kuriame yra "UseTax" pavadinime.

Kitaip, galite konfigūruoti du atskirus PVM kodus: vieną mokėtinam PVM ir kitą PVM atskaitymui. Tada kiekvieną kodą susieti su atitinkamais ataskaitos lauko peržvalgos **rezultatais**.

Pavyzdžiui, **apmokestinamų įsigijimų bendrijos viduje standartiniu tarifu atveju konfigūruojate PVM kodą UT_S_EU** **naudojimo mokesčiu ir susiejate jį su 34-UseTaxEUPurchaseStandard** **peržvalgos rezultatu Ataskaitos** lauko peržvalga. Šiuo atveju sumos, kurios **naudoja pvm UT_S_EU**, rodomos laukuose 089 ir 061 (34 ir 56 eilutės).

Taip pat konfigūruojate du PVM kodus:

  - **VAT_S_EU**, kurios mokesčio tarifo vertė yra -19 procentų
  - **InVAT_S_EU**, kurios mokesčio tarifo vertė yra 19 procentų

Tada kodus su ataskaitos lauko peržvalgos **rezultatais susiejate** tokiu būdu:

  - Susieti **VAT_S_EU** su **34-EUPurchaseStandard** peržvalgos rezultatu.
  - Susieti **InVAT_S_EU** **56-InputTaxEUPurchase peržvalgos** rezultatu.

Šiuo atveju sumos, kurios naudoja **VAT_S_EU** kodą, rodomos lauke 089 (34 eilutė). Sumos, kurios InVAT_S_EU **PVM** kodą, rodomos 061 langelyje (56 eilutė).

Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti atvirkštinį PVM, žr. Atvirkštinį [apmokestinimą](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigūruoti sistemos parametrus

Norėdami sugeneruoti PVM deklaraciją, turite konfigūruoti savo organizacijos mokesčių numerį (Steuernummer).

1. Pasirinkite **Organizacijos administravimas** > **Organizacijos** > **Juridiniai subjektai**.
2. Pasirinkite juridinį subjektą, tada **pasirinkite registracijos PVM**.
3. Pasirinkite arba sukurkite adresą Vokietijoje, tada registracijos **ID** "FastTab" pasirinkite **Įtraukti**.
4. Lauke Registracijos **tipas** pasirinkite Vokietijai skirtą registracijos tipą, **kuris naudoja įmonės ID (COID) registravimo** kategoriją.
5. Į registracijos **numerio** lauką įveskite mokesčio numerį.
6. **Skirtuko Bendra** lauke **Įsigalioja įveskite** datą, nuo kurios numeris įsigalioja.

Daugiau informacijos apie tai, kaip nustatyti registracijos kategorijas ir registracijos tipus [, ieškokite registracijos ID](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Nustatyti Vokietijos PVM deklaraciją

### <a name="import-er-configurations"></a>Importuokite ER konfigūracijas

Atidarykite **elektroninės ataskaitos darbo** sritį ir importuokite šias ar vėlesnes šių ER formatų versijas:

   - PVM deklaracijos Excel (DE).version.101.16.12.xml
   - PVM deklaracijos XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a> Nustatyti konkrečios programos parametrus PVM deklaracijos laukams

Norėdami automatiškai sugeneruoti PVM deklaraciją, susiekite PVM kodus programoje ir peržvalgos rezultatus ER konfigūracijoje.

> [!NOTE]
> Rekomenduojame įgalinti funkciją, **Funkcijų valdymo darbo srityje naudokite ankstesnių ER formatų versijų** darbo srityje **Funkcijų valdymas**. Įgalinus šią funkciją, parametrai, kurie sukonfigūruoti naudoti su ankstesne ER formato versija, automatiškai tampa taikoma vėlesnei to paties formato versijai. Jei ši funkcija neįgalinta, turite atskirai konfigūruoti kiekvienos formato versijos konkrečius programos parametrus. Rekomenduojame įgalinti funkciją, **Funkcijų valdymo darbo srityje naudokite ankstesnių ER formatų versijų** funkcija yra prieinama darbo srityje **Funkcijų valdymas** „Finance“ 10.0.23 versijoje. Daugiau informacijos apie tai, kaip nustatyti kiekvieno juridinio subjekto ER formato parametrus, ieškokite juridinio [subjekto ER formato parametrų nustatymas](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Norėdami nurodyti, kurie PVM kodai generuoja PVM deklaracijos langelius, atlikite šiuos veiksmus.

1. Eikite **į darbo sritis** > **– elektroninės** ataskaitos ir pasirinkite **ataskaitų konfigūracijas**.
2. Pasirinkite PVM **deklaracijos XML (DE)** konfigūraciją, tada pasirinkite Konkrečių **programos \> parametrų nustatymą**.
3. Konkretaus programos **parametrų puslapio** Peržvalgos **"FastTab"** pasirinkite Ataskaitos **lauko peržvalga**.
4. Sąlygų FastTab **nustatykite** šiuos laukus, norėdami susieti PVM kodus ir ataskaitos laukus.

    | Laukas                  | Aprašymas                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Paieškos rezultatas          | Pasirinkti ataskaitos lauko vertę. Daugiau informacijos apie vertes ir jų priskyrimą PVM deklaracijos eilutėms žr. [anksčiau šiame straipsnyje skyriuje](#vat-declaration-overview) PVM deklaracijos apžvalga.                                                                                               |
    | Mokesčio kodas               | Pasirinkti PVM kodą, kuris bus susietas su ataskaitos lauku. Užregistruotos mokesčių operacijos, kurios naudoja pasirinktą PVM kodą, bus surinktos atitinkamą deklaracijos langelį. Rekomenduojame atskirti PVM kodus taip, kad vienas PVM kodas sugeneruotų sumas tik viename deklaracijos langelyje. |
    | Operacijų klasifikatorius | Jei sukūrėte pakankamai PVM kodų deklaracijos laukui nustatyti, pasirinkite **\*Neužpildyti\***. Jei nesukurėte pakankamai PVM kodų, kad vienas PVM kodas sugeneruotų sumas tik viename deklaravimo langelyje, galite nustatyti operacijų klasifikatorius. Galimos šios operacijų klasės:</br>-   **Pirkimas**</br>-   **PurchaseExempt** (neapmokestinamas pirkimas)</br>-   **PurchaseReverseCharge** (mokesčiai, gautini iš pirkimo atvirkštinio apmokestinimo)</br>-   **Pardavimas**</br>-   **SalesExempt** (neapmokestinamas pardavimas)</br>-   **SalesReverseCharge** (mokestis, mokėtinas iš pirkimo atvirkštinio mokesčio arba atvirkštinio pardavimo mokesčio)</br>-   **Naudojimo mokestis**. </br>Taip pat galima naudoti kiekvieno operacijų klasifikatorius kredito pažymos klasifikatorius. Pavyzdžiui, vienas iš šių klasių yra **PurchaseCreditNote** (pirkimo kredito pažyma).</br>Įsitikinkite, kad sukurkite dvi eilutes kiekvienam PVM kodui: vieno, kuris turi operacijos klasifikatorius vertę, ir vieno, kuris turi kredito pažymos vertės operacijos klasifikatorius, eilutes. |

    > [!NOTE]
    > Susieti visus PVM kodus su peržvalgos rezultatais. Jei PVM kodai neturi generuoti verčių PVM deklaracijoje, susiekite juos su **kita** peržvalgos rezultatu.

    ![Konkrečios programos parametrų puslapis](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Būsenos lauke **pakeiskite** vertę į **Baigta**.
6. Veiksmų srityje pasirinkite Eksportuoti **, kad** eksportuotumėte konkrečių programos parametrų parametrus.
7. Pasirinkite PVM **deklaracijos Excel (DE)** konfigūraciją, tada veiksmų srityje pasirinkite Importuoti, norėdami importuoti parametrus, **·** **kuriuos sukonfigūravote PVM deklaracijos XML (DE)**.
8. Lauke **Būsena** pasirinkite **Baigta**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Pvm ataskaitos formato nustatymas "Excel" peržiūrėti sumas

1. Funkcijų valdymo **darbo srityje** raskite ir įgalinkite PVM išrašo **formato ataskaitų** funkciją.
2. Eikite **į DK** > **nustatymo** > **DK parametrus**.
3. Skirtuke **PVM**, mokesčių **pasirinkčių** "FastTab", **PVM išrašo formato** susiejimo lauke, **pasirinkite PVM deklaracijos Excel (DE)**.

   Šis formatas spausdinamas, kai paleidžiate sudengimo **laikotarpio ataskaitos PVM** ataskaitą. Jis taip pat spausdinamas PVM mokėjimų **puslapyje** pasirinkus **Spausdinti**.

4. Jei turite pranešti apie taisymus, specialios ataskaitos **skyriuje** nustatykite **Įtraukti taisymus kaip** **Taip**.
5. Mokesčių inspekcijos **puslapyje** pasirinkite mokesčių inspekciją, o lauke Ataskaitos maketas **pasirinkite** Numatytasis **·**.

Jei konfigūruojate PVM deklaraciją juridiniame subjekte, kuriame yra kelios [PVM registracijos](emea-reporting-for-multiple-vat-registrations.md), atlikite šiuos veiksmus:

1. Eikite **į DK** > **nustatymo** > **DK parametrus**.
2. Skirtuko PVM **šalių** **/** regionų "FastTab **" elektroninės ataskaitos DEU** eilutėje pasirinkite **PVM deklaracijos Excel (DE)** ER formatą.

## <a name="set-up-electronic-messages"></a>Nustatyti elektroninius pranešimus

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Atsisiųskite ir importuokite duomenų paketą, kuriame yra elektroninių pranešimų pavyzdinių parametrų

Duomenų pakete yra elektroninio pranešimo parametrai, naudojami PVM deklaracijai sugeneruoti XML formatu, o tada peržiūrėti programoje "Excel". Galite išplėsti šiuos parametrus arba sukurti savo. Norėdami gauti daugiau informacijos apie tai, kaip dirbti su elektroniniais pranešimais ir kurti savo parametrus, žr. Elektroninių [pranešimų siuntimo informaciją](../general-ledger/electronic-messaging.md).

1. Ciklo [Microsoft Dynamics tarnybose (LCS)](https://lcs.dynamics.com/v2) bendrai naudojamų turtų bibliotekoje pasirinkite Duomenų paketas kaip **turto** tipą, **tada atsisiųskite DE VAT deklaracijos EM paketą**. Atsisiųsto failo vardas yra **DE VAT deklaracijos EM package.zip**.
2. Duomenų valdymo darbo srityje "Dynamics 365 **Finance"** pasirinkite **Importuoti**.
3. **Skirtuko Importo** FastTab lauke **Grupės** pavadinimas įveskite užduoties pavadinimą.
4. „FastTab” **Pasirinkti objektai** pasirinkite **Įtraukti failą**.
5. Dialogo **lange Įtraukti** failą patikrinkite, **ar šaltinio duomenų formato** **laukas** nustatytas kaip Pakuotė, pasirinkite Įkelti ir įtraukti, **tada** pasirinkite anksčiau atsisiųstą pašto failą.
6. Pasirinkite **Uždaryti**.
7. Kai duomenų objektai įkeliami, veiksmų srityje pasirinkite **Importuoti**.
8. Eikite į **mokesčių** > **užklausas ir ataskaitas Elektroniniai** > **pranešimai** > **Elektroniniai** pranešimai ir patikrinkite importuoto elektroninio pranešimo apdorojimą.

### <a name="configure-electronic-messages"></a>Konfigūruoti elektroninius pranešimus

1. Eikite į **mokesčių** > **nustatymo elektroninius** > **pranešimus** > **užpildyti įrašų veiksmus**.
2. Pasirinkite DE užpildyti PVM **grąžinimo įrašų eilutę, tada** pasirinkite užklausą **Redaguoti**.
3. Naudodami filtrą nurodykite sudengimo laikotarpius, kurie bus įtraukti į ataskaitą.
4. Jei turite pateikti kitų sudengimo laikotarpių mokesčių operacijas kitoje deklaracijoje, **sukurkite naują veiksmą Automatiškai įvesti įrašus** ir pasirinkite atitinkamus sudengimo laikotarpius.

## <a name="preview-the-vat-declaration-in-excel"></a>Peržiūrėti PVM deklaraciją programoje "Excel"

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Peržiūrėti PVM deklaraciją "Excel" iš sudengimo laikotarpio periodinės užduoties ataskaitos PVM

1. Eiti į **Mokesčių periodines** > **užduotis** > **Deklaracijos** > **PVM ataskaita** > **sudengimo laikotarpiui**.
2. Lauke Sudengimo **laikotarpis** pasirinkite vertę.
3. **PVM mokėjimo versijos lauke pasirinkite** vieną iš šių verčių:

    - **Pradinis**: generuoti pradinio PVM mokėjimo operacijų arba prieš PVM mokėjimą ataskaitą.
    - **Taisy** įrašai: generuoti visų vėlesnių laikotarpio PVM mokėjimų PVM operacijų ataskaitą.
    - **Bendras sąrašas**: sugeneruokite visų laikotarpio PVM operacijų ataskaitą, įskaitant originalius ir visus pataisymus.

4. **Lauke Pradžios data** pasirinkite ataskaitinio laikotarpio pradžios datą.
5. Pasirinkite **Gerai** ir peržiūrėkite Excel ataskaitą.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Sudengti ir užregistruoti PVM

1. Eiti į mokesčių periodines **užduotis** > **Deklaracijos** > **PVM sudengimas** > **ir registruoti PVM** > **.**
2. Lauke Sudengimo **laikotarpis** pasirinkite vertę.
3. **PVM mokėjimo versijos lauke pasirinkite** vieną iš šių verčių:

    - **Pradinis**: sugeneruokite pradinį sudengimo laikotarpio PVM mokėjimą.
    - **Naujausi koregavimai: sugeneruokite pataisymų PVM mokėjimą po to, kai buvo sukurtas** pradinis sudengimo laikotarpio PVM mokėjimas.

4. **Lauke Pradžios data** pasirinkite ataskaitinio laikotarpio pradžios datą.
5. Pasirinkite **Gerai**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Peržiūrėti PVM deklaraciją Programoje "Excel" iš PVM mokėjimo

1. Eikite **·** > **į mokesčių užklausas ir** > **ataskaitas PVM** > **užklausas** PVM mokėjimams ir pasirinkite PVM mokėjimo eilutę.
2. Pasirinkite **Spausdinti ataskaitą** ir tada pasirinkite **Gerai**.
3. Peržiūrėkite "Excel" failą, sugeneruotą pasirinktai PVM mokėjimo eilutei.

    > [!NOTE]
    > Ataskaita generuojama tik pagal pasirinktą PVM mokėjimo eilutę. Jei norite generuoti, pvz., koreguojamą deklaraciją, kurioje yra visi laikotarpio taisy įrašai, arba pakeitimo deklaraciją, kurioje yra pradiniai duomenys ir visi pataisymai, **sudengimo** laikotarpio periodinę užduotį naudokite ataskaitą PVM.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generuoti PVM deklaraciją iš elektroninių pranešimų

Kai naudojate elektroninius pranešimus ataskaitai generuoti, galite rinkti mokesčių duomenis iš kelių juridinių subjektų. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr. skyrių Paleisti kelių](#run-a-vat-declaration-for-multiple-legal-entities) juridinių subjektų PVM deklaraciją.

Toliau pateikta procedūra taikoma elektroninių pranešimų apdorojimo atvejui, kurį importavote iš LCS bendrinamo turto bibliotekos.

1. Eikite į **mokesčių** > **užklausas ir ataskaitas Elektroniniai** > **·** > **pranešimai**.
2. Kairiajame lange pasirinkite **DE PVM deklaraciją**.
3. Pranešimų FastTab **pasirinkite** Naujas **·**, tada dialogo lange **Vykdyti apdorojimą** pasirinkite **Gerai**.
4. Pasirinkite sukurtą pranešimo eilutę, įveskite aprašymą, tada nurodykite deklaracijos pradžios ir pabaigos datas.

    > [!NOTE]
    > 5–7 žingsniai nėra privalomi.

5. Nebūtina: " **FastTab" Pranešimuose** pasirinkite **Rinkti duomenis**, tada pasirinkite **Gerai**. Anksčiau sugeneruoti PVM mokėjimai įtraukiami į pranešimą. Norėdami gauti daugiau informacijos, žr. [anksčiau šiame straipsnyje skyriuje Sudengti](#settle-and-post-sales-tax) ir užregistruoti PVM. Jei praleisite šį veiksmą, vis tiek galėsite **generuoti PVM deklaraciją naudodami mokesčių deklaracijos** versijos lauką, kuris **yra deklaracijos** dialogo lange.
6. Nebūtina: Pranešimo **prekių "** FastTab" peržiūrėkite PVM mokėjimus, kurie perkelti apdoroti. Pagal numatytuosius nustatymus įtraukiami visi pasirinkto laikotarpio PVM mokėjimai, kurie nebuvo įtraukti į kitus to paties apdorojimo pranešimus.
7. Pasirinktinai: pasirinkite **originalų** dokumentą, kad peržiūrėtumėte PVM mokėjimus, arba pasirinkite Naikinti **,** norėdami neįtraukti PVM mokėjimų į apdorojimą. Jei praleisite šį veiksmą, vis tiek galėsite **generuoti PVM deklaraciją naudodami mokesčių deklaracijos** versijos lauką, kuris **yra deklaracijos** dialogo lange.
8. Pranešimų "**FastTab**" pasirinkite Atnaujinimo **būseną**. Būsenos atnaujinimo **dialogo** lange pasirinkite Parengta **generuoti**, tada pasirinkite **Gerai**. Patikrinkite, ar pranešimo būsena pakeista į Parengta **generuoti**.
9. Pasirinkite **Generuoti ataskaitą**. Norėdami peržiūrėti PVM deklaracijos sumas, dialogo **lange Vykdyti** apdorojimą **pasirinkite Peržiūrėti ataskaitą**, tada pasirinkite **Gerai**.
10. **Elektroninių ataskaitų parametrų** dialogo lange nustatykite šiuos laukus ir pasirinkite **Gerai**.

    | **Laukai**                                   | **Aprašas**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Sudengimo laikotarpis                           | Pasirinkti sudengimo laikotarpį. **Jei 5 veiksme** pasirinkote Rinkti duomenis, šį lauką galite palikti tuščią. Bus sugeneruota PVM operacijų, įtrauktų į surinktus PVM mokėjimus, ataskaita. |
    | Mokesčių deklaracijos versija                     | Pasirinkite vieną iš šių reikšmių:</br>-   **Originalas** – generuoti pradinio PVM mokėjimo operacijų arba prieš PVM mokėjimą ataskaitą.</br>-   **Taisy** įrašai – generuoti visų vėlesnių laikotarpio PVM mokėjimų PVM operacijų ataskaitą.</br>-   **Bendrasis sąrašas** – generuoti visų laikotarpio PVM operacijų ataskaitą, įskaitant originalius ir visus pataisymus.|
    | Atstovas mokesčių klausimais | Pasirinkite šalį, kuri yra PVM deklaracijos mokesčių atstovas, jei taikoma. Informacija apie pasirinktą šalį eksportuojama į **DatenLieferant** XML elementą. |
    | Kontaktinis asmuo | Pasirinkite organizacijos asmenį, kuris yra duomenų tiekėjas. Informacija apie pasirinktą asmenį eksportuojama į **DatenLieferant** XML elementą. |
    | Korekcinė grąža | Pasirinkite Taip **,** jei tai koreguojamosios PVM deklaracija. Šiuo atveju XML elemento KZ10 vertė bus **1**.|
    | Patvirtinamieji dokumentai | Pasirinkite Taip **,** jei siunčiate ir palaikančius dokumentus. Šiuo atveju XML elemento KZ22 vertė bus **1**.|
    | SEPA tiesioginio debeto įgaliojimas bus atšauktas kaip išimtis| Pasirinkite **Taip**, jei SEPA tiesioginio debeto įgaliojimas bus atšauktas kaip šio išankstinės registracijos laikotarpio išimtis. Pavyzdžiui, dėl kompensavimo užklausų. Bet koks likęs balansas mokamas atskirai. Šiuo atveju XML elemento KZ26 vertė bus **1**. |
    | Norima pakartotinio išmokėjimo sumos korespondavimas | Pasirinkite **Taip**, jei norite suslinkti norimą kompensacijos sumą arba jei kompensacijos suma priskirta. Šiuo atveju XML elemento KZ29 vertė bus **1**. |
    | Specialus nuolatinis išankstinio mokėjimo plėtinys | Įvesti nuolatinio plėtinio fiksuoto specialaus išankstinio mokėjimo atskaitymo sumą. Ši atskaitoma suma paprastai baigiama per paskutinę išankstinę mokesčių laikotarpio registraciją. Suma eksportuojama PVM deklaracijos 67 eilutėje (39 langelis) ir XML elementu KZ39. |

11. Viršutiniame **dešiniajame** puslapio kampe pasirinkite Priedai, tada pasirinkite **Atidaryti**.
12. Peržiūrėkite Sumas Excel dokumente ir pasirinkite Generuoti **ataskaitą**.
13. Norėdami generuoti PVM deklaraciją XML formatu dialogo lange **Vykdyti apdorojimą** pasirinkite **Generuoti ataskaitą**, tada pasirinkite **Gerai**.
14. Elektroninių ataskaitų **parametrų dialogo** lange nustatykite laukus taip, kaip aprašyta 10 veiksme.
15. Viršutiniame **dešiniajame** puslapio kampe pasirinkite Priedus, atsisiųskite failą ir naudokite jį norėdami pateikti mokesčių inspekcijai.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a> Vykdyti PVM deklaraciją keliems juridiniams subjektams

Norėdami naudoti formatus norėdami juridinių subjektų grupei pateikti PVM deklaraciją, pirmiausia turite nustatyti nuo programos konkrečius PVM kodų formato parametrus iš visų reikalaujamo juridinio subjekto.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Nustatyti elektroninius pranešimus siekiant surinkti mokesčių duomenis iš kelių juridinių subjektų

Norėdami nustatyti elektroninius pranešimus, kurie surinks duomenis iš kelių juridinių subjektų, atlikite šiuos veiksmus.

1. Eikite į **darbo sričių** > **funkcijų valdymą**.
2. Raskite ir pasirinkite **visos įmonės užklausas, skirtas automatiškai įvesti įrašų** veiksmų funkciją sąraše, tada pasirinkite Įgalinti **dabar**.
3. Eikite į **mokesčių** > **nustatymo elektroninius** > **pranešimus \> užpildyti įrašų veiksmus**.
4. Veiksmų puslapyje **Automatiškai įvesti įrašus** pasirinkite eilutę, kur bus automatiškai užpildomi **PVM grąžinimo įrašai**.

   Duomenų šaltinių **nustatymo tinklelyje** galimas **naujas** laukas Įmonė. Šiame lauke rodomas esamų juridinių subjektų identifikatorius esamiems įrašams.

5. Duomenų šaltinių **nustatymo tinklelyje** pridėkite kiekvieno papildomo juridinio subjekto, kuris turi būti įtrauktas į ataskaitą, eilutę. Kiekvienai naujai eilutei nustatykite šiuos laukus.

    | Laukas                  | Aprašymas                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Pavadinimas / vardas ir pavardė                   | Įveskite vertę, kuri padės suprasti, iš kur gaunamas šis įrašas. Pavyzdžiui, įveskite filialo **1 PVM mokėjimą**. |
    | Pranešimo prekės tipas      | Pasirinkti **PVM grąžinimą**. Ši vertė yra vienintelė galima visų įrašų vertė.                                    |
    | Kodo tipas           | Žymėti **viską**.                                                                                                               |
    | Pagrindinės lentelės pavadinimas      | Nurodykite **TaxReportVoucher** visiems įrašams.                                                                             |
    | Laukas Dokumento numeris  | Nurodyti **kvitą** visiems įrašams.                                                                                      |
    | Laukas Dokumento data    | Nurodyti **visų įrašų TransDate**.                                                                                    |
    | Laukas Dokumento sąskaita | Nurodyti **TaxPeriod** visiems įrašams.                                                                                    |
    | Įmonė                | Pasirinkite juridinio subjekto ID.                                                                                            |
    | Vartotojo užklausa             | Šis žymės langelis automatiškai pasirenkamas, kai pasirenkate kriterijus pasirinkdami Redaguoti **užklausą**.                                 |

6. Kiekvienoje naujoje eilutėje pasirinkite **Redaguoti užklausą** ir **nurodykite** susijusį juridinio subjekto, nurodyto eilutės lauke Įmonė, sudengimo laikotarpį.

Kai nustatymas baigtas, elektroninių **pranešimų puslapyje** **nurodyta** duomenų rinkimo funkcija surenka PVM mokėjimus iš visų jūsų nurodytų juridinių subjektų.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
