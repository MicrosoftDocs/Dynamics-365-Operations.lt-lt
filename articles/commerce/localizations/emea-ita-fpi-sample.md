---
title: Fiskalinio spausdintuvo integracijos pavyzdys (Italija)
description: Šioje temoje pateikiama Italijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 02226fd9f2c92db2518ca48baefb680a3d2f0ac1
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076908"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskalinio spausdintuvo integracijos pavyzdys (Italija)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama Italijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

Italijos komercijos funkcija apima pavyzdinį pardavimo vietos (POS) integravimą su mokesčių spausdintuvu. Mėginys pratęsia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) kad jis veiktų su [Epson FP-90III serija](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) „Epson“ spausdintuvai ir įgalina ryšį su fiskaliniu spausdintuvu žiniatinklio serverio režimu per „EpsonFPMate“ žiniatinklio paslaugą naudojant „Fiscal ePOS-Print“ API. Pavyzdys palaiko tik Registratore Telematico (RT) režimą. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų iš „Epson“. Norėdami gauti informacijos apie fiskalinio spausdintuvo įsigijimą ir naudojimą, susisiekite su [Epson Italia SpA](https://www.epson.it)

## <a name="scenarios"></a>Scenarijai

Italijos fiskalinio spausdintuvo integravimo pavyzdys apima šiuos scenarijus:

- Pardavimo scenarijai:

    - Atsispausdinkite grynųjų pinigų pardavimo ir grąžinimo mokesčių kvitą.
    - Užfiksuokite atsakymą iš fiskalinio spausdintuvo ir išsaugokite jį kanalų duomenų bazėje.
    - Mokesčiai:

        - Susiekite su fiskalinio spausdintuvo mokesčių kodais (skyriais).
        - Perkelkite susietus mokesčių duomenis į fiskalinį spausdintuvą.
        - Išspausdinkite mokesčius fiskaliniame kvite.

    - Mokėjimai:

        - Susiekite su fiskalinio spausdintuvo mokėjimo būdais.
        - Atsispausdinkite mokėjimus fiskaliniame kvite.
        - Spausdinti pakeitimo informaciją.

    - Spausdinimo linijų nuolaidos.
    - Dovanų kortelės:

        - Išskirkite išduotą / papildytą dovanų kortelių eilutę iš pardavimo fiskalinio kvito.
        - Atspausdinkite mokėjimą, kai kaip įprastas mokėjimo būdas naudojamas dovanų kortelė.

    - Spausdinkite klientų užsakymo operacijų fiskalinius kvitus:

        - Kliento užsakymo indėlio fiskalinis kvitas nespausdinamas.
        - Išspausdinkite fiskalinį kvitą hibridinio kliento užsakymo vykdymo eilėms.
        - Išspausdinkite fiskalinį kliento užsakymo atsiėmimo operacijos kvitą.
        - Atsispausdinkite grąžinimo užsakymo fiskalinį kvitą.

    - Išspausdinkite kvito numerio brūkšninį kodą fiskaliniame kvite.
    - Spausdinkite [klientų informacija](emea-ita-customer-information.md) kuris nurodytas pardavimo sandoriui fiskaliniame kvite. Šios informacijos pavyzdys yra kliento loterijos kodas. 

- Dienos pabaigos ataskaitos (fiskalinės X ir fiskalinės Z ataskaitos).
- Klaidų apdorojimas, pvz., šios parinktys:

    - Bandykite dar kartą registruoti fiskalinę informaciją, jei įmanoma pakartotinai, pvz., jei mokesčių spausdintuvas neprijungtas, nėra paruoštas arba nereaguoja, spausdintuve baigėsi popierius arba įstrigo popierius.
    - Atidėti fiskalinę registraciją.
    - Praleiskite fiskalinę registraciją arba pažymėkite operaciją kaip registruotą ir įtraukite informacinius kodus, kad užfiksuotumėte gedimo priežastį ir papildomą informaciją.
    - Patikrinkite fiskalinio spausdintuvo prieinamumą prieš atidarydami naują pardavimo operaciją arba užbaigdami pardavimo operaciją.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinio spausdintuvo integravimo pavyzdys įgyvendina šias taisykles, susijusias su dovanų kortelėmis:

- Išskirkite pardavimo eilutes, kurios yra susijusios su *Išduoti dovanų kortelę* ir *Pridėti prie dovanų kortelės* operacijos iš fiskalinio kvito.
- Nespausdinkite fiskalinio kvito, jei jį sudaro tik dovanų kortelės eilutės.
- Iš fiskalinio kvito mokėjimo eilučių atimkite visą dovanų kortelių, kurios išduodamos arba apmokestinamos atliekant operaciją, sumą.
- Išsaugokite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Apmokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klientų indėliai ir klientų užsakymų indėliai

Fiskalinio spausdintuvo integravimo pavyzdys įgyvendina šias taisykles, susijusias su klientų indėliais ir klientų užsakymų įnašais:

- Nespausdinkite fiskalinio kvito, jei operacija yra kliento indėlis.
- Nespausdinkite fiskalinio kvito, jei operaciją sudaro tik kliento užsakymo užstatas arba kliento užsakymo užstato grąžinimas.
- Išspausdinkite anksčiau sumokėto užstato sumą ant kliento užsakymo atsiėmimo operacijos fiskalinio kvito.
- Sukūrę hibridinį kliento užsakymą, iš mokėjimo eilučių išskaičiuokite kliento užsakymo įmokos sumą.
- Išsaugokite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į fiskalinę operaciją hibridiniam kliento užsakymui.

### <a name="limitations-of-the-sample"></a>Mėginio apribojimai

- Fiskalinis spausdintuvas palaiko tik tuos atvejus, kai pardavimo mokestis yra įtrauktas į kainą. Todėl, **Kaina su pardavimo mokesčiu** parinktis turi būti nustatyta į **Taip** tiek parduotuvėms, tiek pirkėjams.
- Kasdienės ataskaitos (fiskalinės X ir fiskalinės Z) spausdinamos naudojant formatą, kuris yra įdėtas į fiskalinio spausdintuvo programinę įrangą.
- Fiskalinis spausdintuvas nepalaiko mišrių operacijų. The **Uždrausti maišyti pardavimus ir grąžinimus viename kvite** parinktis turi būti nustatyta į **Taip** POS funkcijų profiliuose.
- Pavyzdys palaiko integravimą tik su fiskaliniu spausdintuvu, kuris veikia Registratore Telematico (RT)) režimu.

## <a name="set-up-fiscal-integration-for-italy"></a>Nustatyti fiskalinę Italijos integraciją

Fiskalinio spausdintuvo integravimo pavyzdys Italijoje yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ EpsonFP90III pavyzdys** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Italijoje skirto fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senas)](emea-ita-fpi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

Atlikite fiskalinės integracijos sąrankos veiksmus, kaip aprašyta [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas šiam fiskalinio spausdintuvo integravimo pavyzdžiui](#set-up-the-registration-process).
1. [Nustatykite nuolaidų fiskalinius tekstus](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Nustatykite klaidų tvarkymo nustatymus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Nustatykite fiskalines X/Z ataskaitas iš POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Nustatykite klientų informacijos valdymo POS funkciją](emea-ita-customer-information.md#setup).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatykite registracijos procesą

Norėdami įjungti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte „Commerce“ būstinę. Daugiau informacijos žr [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją (pvz.,**[išleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atviras **src \> Fiskalinė integracija \> EpsonFP90III pavyzdys**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Konfigūracija \> DocumentProviderEpsonFP90IIISample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Konfigūracija \> JungtisEpsonFP90IIISample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinio dokumento teikėjo konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extension.DocumentProvider.EpsonFP90IIISample\\ Konfigūracija\\ DocumentProviderEpsonFP90IIISample.xml
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ HardwareStation\\ Plėtinys.EpsonFP90IIIFiscalDeviceSample\\ Konfigūracija\\ JungtisEpsonFP90IIISample.xml
    > 
    > Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Ant **Generolas** skirtuką, nustatykite **Įgalinti fiskalinę integraciją** galimybė į **Taip**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite fiskalinio dokumento teikėjo konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys** ir įkelkite fiskalinės jungties konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**. Sukurkite naują jungties funkcinį profilį. Pasirinkite dokumento teikėją ir jungtį, kurią įkėlėte anksčiau. Atnaujinkite [duomenų atvaizdavimo nustatymus](#default-data-mapping) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**. Sukurkite naują jungties techninį profilį ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Atnaujinkite [jungties nustatymai](#fiscal-connector-settings) kaip reikalaujama.
6. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės**. Sukurkite naują fiskalinių jungčių grupę jungties funkciniam profiliui, kurį sukūrėte anksčiau.
7. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**. Sukurkite naują fiskalinės registracijos procesą ir fiskalinės registracijos proceso veiksmą ir pasirinkite anksčiau sukurtą fiskalinių jungčių grupę.
8. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų profilį, susietą su parduotuve, kurioje turėtų būti suaktyvintas registracijos procesas. Ant **Fiskalinės registracijos procesas** FastTab, pasirinkite fiskalinės registracijos procesą, kurį sukūrėte anksčiau.
9. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros profilį, susietą su aparatūros stotimi, prie kurios bus prijungtas fiskalinis spausdintuvas. Ant **Fiskaliniai periferiniai įrenginiai** FastTab, pasirinkite jungties techninį profilį, kurį sukūrėte anksčiau.
10. Atidarykite platinimo tvarkaraštį (**Mažmeninė prekyba ir prekyba \> Mažmeninė prekyba ir IT \> Platinimo grafikas**) ir pasirinkite darbus **1070** ir **1090** perkelti duomenis į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytasis duomenų atvaizdavimas

Šis numatytasis duomenų atvaizdavimas įtrauktas į fiskalinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Konkurso tipo kartografavimas** – Mokėjimo metodų, sukonfigūruotų parduotuvei, susiejimas su mokėjimų tipais, kuriuos palaiko fiskalinis spausdintuvas. Toliau pateiktame pavyzdyje parodytas numatytasis susiejimas.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Štai šio žemėlapio atributų paaiškinimas:

    - **Parduotuvės mokėjimo metodas** yra mokėjimo būdas, nustatytas parduotuvėje adresu **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Mokėjimo metodai \> Mokėjimo metodai**.
    - **Spausdintuvo mokėjimo tipas** ir **PrinterPaymentIndex** yra atitinkamas mokėjimo tipas ir indeksas, apibrėžti „Epson“ fiskalinio spausdintuvo dokumentacijoje.
    - **Indėlio mokėjimo būdas** naudojamas norint nurodyti spausdintuvo mokėjimo tipą ir indeksą, skirtą kliento užsakymo atsiėmimo sumos daliai, kuri apmokama kliento užsakymo depozitu.

    Šioje lentelėje parodyta, kaip pavyzdinis mokėjimo metodų susiejimas atitinka parduotuvės mokėjimo metodus, sukonfigūruotus standartiniuose demonstraciniuose duomenyse.

    | Mokėjimo būdas | Mokėjimo būdo pavadinimas |
    |----------------|---------------------|
    | 1              | Grynieji pinigai                |
    | 3              | Kortelė                |
    | 4              | Kliento kodas    |
    | 6              | Valiuta            |
    | 8              | Dovanų kortelė           |

    Turite modifikuoti pavyzdinį susiejimą pagal mokėjimo metodus, sukonfigūruotus jūsų programoje.

- **Kvito numerio brūkšninio kodo tipas** – Brūkšninio kodo tipas, naudojamas kvito numeriui rodyti fiskaliniame kvite. Numatytasis atvaizdavimas yra **KODAS 128**.
- **Spausdinkite fiskalinius duomenis kvito antraštėje** – Jei šis parametras įjungtas, parduotuvės informacija bus atspausdinta fiskaliniame kvite. Ši informacija apima parduotuvės pavadinimą, adresą ir mokesčių mokėtojo numerį bei kasininko vardą.
- **Fiskalinio spausdintuvo skyriaus žemėlapis** – Fiskalinio spausdintuvo skyrių susiejimas su pridėtinės vertės mokesčio (PVM) tarifais, PVM neapmokestinamomis rūšimis ir produktų tipais. Toliau pateiktame pavyzdyje parodytas numatytasis susiejimas.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Štai šio žemėlapio atributų paaiškinimas:

    - **VATRAte** yra palaikomas PVM tarifas, sukonfigūruotas kaip pardavimo mokesčio kodas. Susiejimo reikšmė turi du skaitmenis po kablelio, bet be kablelio skyriklio. Pavyzdžiui, **2200** sudaro 22 proc., ir **1000** sudaro 10 proc.
    - **VATExemptNature** taikomas tik tais atvejais, kai PVM tarifas yra 0 (nulis), įskaitant atvejus, kai mokesčio nėra. Šiuo metu, **VATExemptNature** palaikoma tik dovanų kortelėms, o reikšmė atvaizde turi atitikti vertę **VATExemptNatureForGiftCard** ypatybę XML konfigūracijos faile.
    - **Produkto tipas** yra produkto tipas. Vertė **0** reiškia prekes ir vertę **1** atstovauja paslaugas.
    - **Skyriaus numeris** yra skyriaus, kuris sukonfigūruotas spausdintuve ir atitinkantis tris ankstesnius atributus, numeris.

    Turite modifikuoti pavyzdinį susiejimą pagal PVM tarifus, kurie sukonfigūruoti jūsų programoje ir atitinkamuose skyriuose, sukonfigūruotuose jūsų mokesčių spausdintuve.

- **PVM neapmokestinamas gamtos dovanų kuponas** – PVM neapmokestinamasis pobūdis, kuris turėtų būti taikomas išduodant ar pildant dovanų kortelę. Reikšmė turėtų atitikti tam tikrą įrašą fiskalinio spausdintuvo skyriaus atvaizde. Numatytasis atvaizdavimas yra **NS**.
- **Įgalinti nemokamus elementus** – Jei šis parametras įjungtas, specialus *omaggio* įjungtas nuolaidos koregavimo tipas prekėms, kurioms taikoma 100 procentų nuolaida.
- **Grąžinimo kilmės informacijos kodas** – Informacijos kodas, naudojamas grąžinimo operacijos kilmei užfiksuoti, jei nepateikiamas originalus pardavimo kvitas. Šis parametras naudojamas kartu su **Pradinės pardavimo datos informacijos kodas** ir **Grąžinimo kilmės žemėlapis** parametrus, kad sugeneruotų teisingą pranešimą fiskaliniame kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos. 

    Šis informacijos kodas turi būti sukonfigūruotas taip, kad vartotojas galėtų pasirinkti arba įvesti vieną iš galimų grąžinimo šaltinių jūsų parduotuvėse. Pavyzdžiui, jis gali būti sukonfigūruotas kaip subkodų sąrašas (pvz., **iš svetainės** arba **Grįžimas iš kiosko**). The **Grąžinimo kilmės žemėlapis** Tada parametras naudojamas informacijos kodo reikšmei paversti fiskalinio spausdintuvo komanda.

    Informacijos kodas, kuriam pasirinktas **Grąžinimo kilmės informacijos kodas** turėtų būti sukonfigūruotas kaip privalomas informacijos kodas, kuris suaktyvinamas vieną kartą per vieną pardavimo operaciją. Jis turėtų būti priskirtas kaip **Grąžinti prekę** informacijos kodas POS funkcijų profilyje, kad jis būtų paleistas, kai **Grąžinti prekę** operacija vykdoma.

    Šiam susiejimui nenurodyta numatytoji vertė. Turite pasirinkti informacijos kodą, kuris sukonfigūruotas jūsų programoje.

- **Pradinės pardavimo datos informacijos kodas** – Informacijos kodas, naudojamas grąžinimo operacijos pradinei pardavimo datai užfiksuoti, jei nepateikiamas originalus pardavimo kvitas. Šis parametras naudojamas kartu su **Grąžinimo kilmės informacijos kodas** ir **Grąžinimo kilmės žemėlapis** parametrus, kad sugeneruotų teisingą pranešimą fiskaliniame kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos.

    Informacijos kodas turi būti sukonfigūruotas taip, kad **Įvesties tipas** laukas nustatytas į **Data**. Jis turėtų būti sukonfigūruotas kaip privalomas informacijos kodas, kuris suaktyvinamas vieną kartą per vieną pardavimo operaciją. Jis taip pat turėtų būti priskirtas kaip **Susietas informacijos kodas** informacijos kodui, kuris pasirinktas **Grąžinimo kilmės informacijos kodas** parametrą, kad du informacijos kodai būtų suaktyvinti vienas po kito.

    Šiam susiejimui nenurodyta numatytoji vertė. Turite pasirinkti informacijos kodą, kuris sukonfigūruotas jūsų programoje.

- **Grąžinimo kilmės žemėlapis** – Grąžinimo pradžios atvaizdavimas, naudojamas grąžinimo operacijos kilmei spausdinti, jei nepateikiamas originalus pardavimo kvitas. Šis parametras naudojamas kartu su **Grąžinimo kilmės informacijos kodas** ir **Pradinės pardavimo datos informacijos kodas** parametrus, kad sugeneruotų teisingą pranešimą fiskaliniame kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos. Toliau pateiktame pavyzdyje parodytas numatytasis susiejimas.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Štai šio žemėlapio atributų paaiškinimas:

    - **ReturnOrigin** yra viena iš galimų grąžinimo šaltinių jūsų parduotuvėse. Vertė turi atitikti reikšmę **Grąžinimo kilmės informacijos kodas** parametras.
    - **Spausdintuvo grąžinimas** yra viena iš grąžinimo šaltinių, kurią priima fiskalinis spausdintuvas (**POS**, **·**, arba **ND**).
    - **PrinterReturnOriginWithoutFiscalData** yra grąžinimo kilmė, kurią priima fiskalinis spausdintuvas ir kuri atitinka grąžinimo operaciją, susietą su pradine pardavimo operacija, kurioje nėra susietų fiskalinių duomenų, nes ji nebuvo užregistruota naudojant fiskalinį spausdintuvą. Tokiu atveju pradinė pardavimo data nurodoma kaip pradinės pardavimo operacijos data.

Šie numatytieji duomenų atvaizdai yra pasenę ir saugomi tik atgaliniam suderinamumui:

- Pridėtinės vertės mokesčio (PVM) kodų atvaizdavimas
- Įmokos mokėjimo tipas

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Galinio taško adresas** – Spausdintuvo URL.
- **Datos ir laiko sinchronizavimas** – Reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuojami su prijungta aparatūros stotimi.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Italijoje skirto fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senas)](emea-ita-fpi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

#### <a name="set-up-the-development-environment"></a>Nustatykite kūrimo aplinką

Norėdami nustatyti kūrimo aplinką pavyzdžiui išbandyti ir išplėsti, atlikite šiuos veiksmus.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite fiskalinio spausdintuvo integravimo sprendimą adresu **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ EpsonFP90III pavyzdys\\ EpsonFP90IIISample.sln**, ir pastatyti jį.
1. Diegti CRT plėtiniai:

    1. Surask CRT plėtinio diegimo programa:

        - **Prekybos masto vienetas:** Viduje konors **EpsonFP90III pavyzdys\\ ScaleUnit\\ ScaleUnit.EpsonFP90III.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ScaleUnit.EpsonFP90III.Installer** montuotojas.
        - **Vietinis CRT Šiuolaikinėje POS:** Viduje konors **EpsonFP90III pavyzdys\\ Šiuolaikinis POS\\ ModernPOS.EpsonFP90III.Įdiegimo programa\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ModernPOS.EpsonFP90III.Įdiegimo programa** montuotojas.

    1. Pradėkite CRT plėtinio diegimo programa iš komandinės eilutės:

        - **Prekybos masto vienetas:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Vietinis CRT Šiuolaikinėje POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatinės įrangos stoties plėtinius:

    1. Viduje konors **EpsonFP90III pavyzdys\\ HardwareStation\\ HardwareStation.EpsonFP90III.Įdiegimo programa\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **HardwareStation.EpsonFP90III.Įdiegimo programa** montuotojas.
    1. Paleiskite plėtinio diegimo programą iš komandinės eilutės:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **EpsonFP90III build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-extensions"></a>Priestatų projektavimas

Fiskalinio spausdintuvo integravimo pavyzdys Italijoje yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ EpsonFP90III pavyzdys** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Italijoje skirto fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senas)](emea-ita-fpi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra mokesčių dokumentų teikėjas, tikslas yra generuoti konkretiems spausdintuvams skirtus dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **Document ProviderEpsonFP90III** užklausų tvarkytojas yra užklausos generuoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkretaus spausdintuvo dokumentą, kuris turėtų būti užregistruotas mokesčių spausdintuve.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ EpsonFP90III pavyzdys\\ CommerceRuntime\\ DocumentProvider.EpsonFP90IIISample\\ Konfigūracija\\ DocumentProviderEpsonFP90IIISample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – įgalinti dokumentų teikėjo nustatymus konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių spausdintuvu. Šis plėtinys naudoja HTTP protokolą, kad pateiktų dokumentus, kuriuos CRT plėtinys sugeneruoja mokesčių spausdintuvą. Ji taip pat tvarko atsakymus, gautus iš mokesčių spausdintuvo.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EpsonFP90III pavyzdys** užklausų tvarkytuvas yra įvesties taškas, skirtas apdoroti užklausą į fiskalinį periferinį įrenginį.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į spausdintuvus ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama prietaiso sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama spausdintuvo inicijavimui.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ EpsonFP90III pavyzdys\\ HardwareStation\\ EpsonFP90IIIFiscalDeviceSample\\ Konfigūracija\\ JungtisEpsonFP90IIISample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – įgalinti jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
