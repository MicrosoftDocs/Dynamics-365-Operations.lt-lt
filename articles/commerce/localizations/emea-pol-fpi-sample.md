---
title: Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)
description: Šioje temoje pateikiama Lenkijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076841"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama Lenkijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

The Dynamics 365 Commerce Lenkijos funkcionalumas apima pavyzdinį pardavimo vietos (POS) integravimą su mokesčių spausdintuvu. Mėginys pratęsia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir palaiko POSNET THERMAL HD 2.02 protokolą fiskaliniams spausdintuvams iš [Posnet Polska SA](https://www.posnet.com.pl) Pavyzdys leidžia palaikyti ryšį su mokesčių spausdintuvu, kuris yra prijungtas per COM prievadą naudojant vietinę programinės įrangos tvarkyklę. Jis buvo įdiegtas ir išbandytas naudojant programinės įrangos emuliatorių, kurį „Posnet“ suteikė „Posnet Thermal HD FV EJ“ fiskaliniam spausdintuvui. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ iš „Posnet“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų. Norėdami gauti informacijos apie fiskalinio spausdintuvo įsigijimą ir naudojimą, susisiekite su [Posnet Polska SA](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenarijai

Lenkijos mokesčių spausdintuvo integravimo pavyzdys apima šiuos scenarijus:

- Pardavimo scenarijai:

    - Atsispausdinkite grynųjų pinigų pardavimo ir grąžinimo mokesčių kvitą.
    - Užfiksuokite atsakymą iš fiskalinio spausdintuvo ir išsaugokite jį kanalų duomenų bazėje.
    - Mokesčiai:

        - Susiekite su fiskalinio spausdintuvo mokesčių kodais (skyriais).
        - Perkelkite susietus mokesčių duomenis į fiskalinį spausdintuvą.

    - Mokėjimai:

        - Susiekite su fiskalinio spausdintuvo mokėjimo būdais.
        - Atsispausdinkite mokėjimus fiskaliniame kvite.
        - Spausdinti pakeitimo informaciją.

    - Spausdinimo linijų nuolaidos.
    - Dovanų kortelės:

        - Išskirkite išduotą / pakartotinai apmokestintą dovanų kortelės eilutę iš pardavimo mokesčių kvito.
        - Atspausdinkite mokėjimą, kai kaip įprastas mokėjimo būdas naudojamas dovanų kortelė.

    - Spausdinkite klientų užsakymo operacijų fiskalinius kvitus:

        - Kliento užsakymo indėlio fiskalinis kvitas nespausdinamas.
        - Išspausdinkite fiskalinį kvitą hibridinio kliento užsakymo vykdymo eilėms.
        - Išspausdinkite fiskalinį kliento užsakymo atsiėmimo operacijos kvitą.
        - Atsispausdinkite grąžinimo užsakymo fiskalinį kvitą.

    - Spausdinkite [klientų informacija](emea-pol-customer-information.md) kuris nurodytas pardavimo sandoriui fiskaliniame kvite. Šios informacijos pavyzdys yra kliento PVM mokėtojo kodas.

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
- Iš fiskalinio kvito mokėjimo eilučių atimkite visą dovanų kortelių, kurios išduodamos arba iš naujo apmokestinamos atliekant operaciją, sumą.
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
- Kasdienės ataskaitos (fiskalinės X ir fiskalinės Z) spausdinamos naudojant įdėtąjį *Pamainos ataskaita* formatu.
- Brūkšninio kodo spausdinimas ant fiskalinių kvitų laikomas galimu pritaikymu, nes ši funkcija nepalaikoma įterptuose formatuose ir gali būti įdiegta tik naudojant tinkinamą **Super formatas** ataskaita.
- Fiskalinis spausdintuvas nepalaiko mišrių operacijų. The **Uždrausti maišyti pardavimus ir grąžinimus viename kvite** parinktis turi būti nustatyta į **Taip** POS funkcijų profiliuose.

## <a name="set-up-fiscal-integration-for-poland"></a>Nustatyti fiskalinę Lenkijos integraciją

Fiskalinio spausdintuvo integravimo pavyzdys Lenkijai yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Posnet** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Fiskalinio spausdintuvo integravimo Lenkijoje pavyzdžio diegimo gairės (senas)](emea-pol-fpi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

Atlikite fiskalinės integracijos sąrankos veiksmus, kaip aprašyta [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas šiam fiskalinio spausdintuvo integravimo pavyzdžiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo nustatymus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Nustatykite fiskalines X/Z ataskaitas iš POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatykite registracijos procesą

Norėdami įjungti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte „Commerce“ būstinę. Daugiau informacijos žr [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją (pvz.,**[išleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atviras **src \> Fiskalinė integracija \> Posnet**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **CommerceRuntime \> DocumentProvider.PosnetSample \> Konfigūracija \> DocumentProviderPosnetSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **HardwareStation \> ThermalDeviceSample \> Konfigūracija \> JungtisPosnetThermalFVEJ.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinio dokumento teikėjo konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extension.DocumentProvider.PosnetSample\\ Konfigūracija\\ DocumentProviderPosnetSample.xml
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ HardwareStation\\ Extension.Posnet.ThermalDeviceSample\\ Konfigūracija\\ JungtisPosnetThermalFVEJ.xml
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

- **Pridėtinės vertės mokesčio (PVM) tarifų kartografavimas** – Mokesčių procentinių verčių, nustatytų pardavimo mokesčių kodams, susiejimas su fiskaliniam spausdintuvui būdingais PVM tarifais. Čia yra numatytasis atvaizdavimas:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Pirmasis kiekvienos poros komponentas reiškia PVM tarifo numerį, sukonfigūruotą fiskaliniame spausdintuve. Antrasis komponentas reiškia atitinkamą PVM tarifą. Daugiau informacijos apie fiskalinio spausdintuvo PVM tarifo konfigūraciją rasite POSNET tvarkyklės dokumentacijoje.

- **Konkurso tipo kartografavimas** – Mokėjimo metodų, sukonfigūruotų parduotuvei, susiejimas su mokėjimo formomis, kurias palaiko fiskalinis spausdintuvas. Čia yra numatytasis atvaizdavimas:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Pirmasis kiekvienos poros komponentas reiškia mokėjimo metodą, kuris yra nustatytas parduotuvėje. Antrasis komponentas reiškia atitinkamą mokėjimo formą, kurią palaiko fiskalinis spausdintuvas. Daugiau informacijos apie mokėjimo formas, kurias palaiko fiskalinis spausdintuvas, rasite POSNET tvarkyklės dokumentacijoje. Turite modifikuoti pavyzdinį susiejimą pagal mokėjimo metodus, sukonfigūruotus jūsų programoje.

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Ryšio eilutė** – Eilutę, apibūdinančią išsamią ryšio su įrenginiu informaciją formatu, kurį palaiko tvarkyklė. Daugiau informacijos rasite POSNET tvarkyklės dokumentacijoje.
- **Datos ir laiko sinchronizavimas** – Reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuojami su prijungta aparatūros stotimi.
- **Įrenginio skirtasis laikas** – Laikas milisekundėmis, per kurį vairuotojas lauks atsakymo iš įrenginio. Daugiau informacijos rasite POSNET tvarkyklės dokumentacijoje.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Fiskalinio spausdintuvo integravimo Lenkijoje pavyzdžio diegimo gairės (senas)](emea-pol-fpi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

#### <a name="set-up-the-development-environment"></a>Nustatykite kūrimo aplinką

Norėdami nustatyti kūrimo aplinką pavyzdžiui išbandyti ir išplėsti, atlikite šiuos veiksmus.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite fiskalinio spausdintuvo integravimo sprendimą adresu **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ Posnet\\ Posnet.sln**, ir pastatyti jį.
1. Diegti CRT plėtiniai:

    1. Surask CRT plėtinio diegimo programa:

        - **Prekybos masto vienetas:** Viduje konors **Posnet\\ ScaleUnit\\ ScaleUnit.Posnet.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ScaleUnit.Posnet.Installer** montuotojas.
        - **Vietinis CRT Šiuolaikinėje POS:** Viduje konors **Posnet\\ Šiuolaikinis POS\\ ModernPOS.Posnet.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ModernPOS.Posnet.Installer** montuotojas.

    1. Pradėkite CRT plėtinio diegimo programa iš komandinės eilutės:

        - **Prekybos masto vienetas:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Vietinis CRT Šiuolaikinėje POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatinės įrangos stoties plėtinius:

    1. Viduje konors **Posnet\\ HardwareStation\\ HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** montuotojas.
    1. Paleiskite plėtinio diegimo programą iš komandinės eilutės:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **Posnet build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-extensions"></a>Priestatų projektavimas

Fiskalinio spausdintuvo integravimo pavyzdys Lenkijai yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ Posnet** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Fiskalinio spausdintuvo integravimo Lenkijoje pavyzdžio diegimo gairės (senas)](emea-pol-fpi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra mokesčių dokumentų teikėjas, tikslas yra generuoti konkretiems spausdintuvams skirtus dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo. Šis plėtinys generuoja spausdintuvui būdingų komandų rinkinį JavaScript Object Notation (JSON) formatu, apibrėžtą POSNET specifikacijoje 19-3678.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **DocumentProviderPosnetProtocol** užklausų tvarkytojas yra užklausos generuoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkretaus spausdintuvo dokumentą, kuris turėtų būti užregistruotas mokesčių spausdintuve.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample\\ Konfigūracija\\ DocumentProviderPosnetSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinių dokumentų teikėjo nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių spausdintuvu. Šis plėtinys iškviečia POSNET tvarkyklės funkcijas, kad pateiktų komandas, kurias CRT plėtinys sugeneruoja mokesčių spausdintuvą. Jis taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **FiscalPrinterHandler** užklausų tvarkytojas yra įvesties taškas, skirtas apdoroti užklausą į fiskalinį periferinį įrenginį.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į spausdintuvus ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama prietaiso sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama spausdintuvo inicijavimui.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ Posnet\\ HardwareStation\\ ThermalDeviceSample\\ Konfigūracija\\ JungtisPosnetThermalFVEJ.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – leisti fiskalinės jungties nustatymus konfigūruoti iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
