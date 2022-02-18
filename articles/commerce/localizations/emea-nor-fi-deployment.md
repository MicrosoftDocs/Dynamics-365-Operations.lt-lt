---
title: Kasos aparatų diegimo Norvegijoje gairės
description: Šioje temoje pateikiamos gairės, kaip įjungti kasos aparato funkcijas Microsoft Dynamics 365 Commerce lokalizacija Norvegijai.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f0744b18ed59c692ae336c92e488d339ae158368
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077145"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Kasos aparatų diegimo Norvegijoje gairės

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įjungti kasos aparato funkcijas Microsoft Dynamics 365 Commerce lokalizacija Norvegijai. Lokalizaciją sudaro keli komponentų plėtiniai. Šie plėtiniai leidžia atlikti tokius veiksmus kaip pasirinktinių laukų spausdinimas kvituose, papildomų audito įvykių, pardavimo operacijų ir mokėjimo operacijų registravimas pardavimo vietoje (POS), skaitmeninio pardavimo operacijų pasirašymas ir ataskaitų spausdinimas vietiniais formatais. Norėdami gauti daugiau informacijos apie lokalizaciją Norvegijoje, žr [Kasos aparato funkcionalumas Norvegijai](./emea-nor-cash-registers.md). Norėdami gauti daugiau informacijos apie tai, kaip konfigūruoti „Commerce“ Norvegijai, žr [Nustatyti „Commerce“ Norvegijai](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jis negali būti naudojamas šiai lokalizavimo funkcijai. Turite naudoti Norvegijai skirto skaitmeninio pasirašymo pavyzdžio versiją ankstesnėje mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) versijoje kūrėjo virtualioje mašinoje (VM)Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Kasos aparatų diegimo Norvegijoje gairės (palikimas)](./emea-nor-loc-deployment-guidelines.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

## <a name="set-up-fiscal-registration-for-norway"></a>Nustatykite mokesčių registraciją Norvegijoje

Norvegijos fiskalinės registracijos pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ SequentialSignatureNorway** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo ir fiskalinės jungties, kurios yra „Commerce“ vykdymo laiko plėtiniai (CRT). Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

Atlikite fiskalinės registracijos sąrankos veiksmus, aprašytus [Nustatykite fiskalinį prekybos kanalų integravimą](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite fiskalinės registracijos procesą](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Būtinai atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas Norvegijai](#configure-the-fiscal-registration-process).
1. [Nustatykite klaidų tvarkymo nustatymus](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Sukonfigūruokite fiskalinės registracijos procesą

Atlikite šiuos veiksmus, kad įgalintumėte Norvegijos fiskalinės registracijos procesą „Commerce“ būstinėje.

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus iš „Commerce“ SDK:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Atidarykite paskutinę galimą leidimo šaką (pvz.,**[leidimas/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Atviras **src \> Fiskalinė integracija \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **DocumentProvider.SequentialSignNorway \> Konfigūracija \> DocumentProviderSequentialSignatureNorwaySample.xml** (pavyzdžiui, [išleidimo failas/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **Jungtis.SequentialSignNorway \> Konfigūracija \> ConnectorSequentialSignatureNorwaySample.xml** (pavyzdžiui, [išleidimo failas/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Eiti į **Mažmeninė prekyba ir prekyba \> Būstinės įrengimas \> Parametrai \> Bendrinami parametrai**. Ant **Generolas** skirtuką, nustatykite **Įgalinti fiskalinę integraciją** galimybė į **Taip**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys** ir įkelkite fiskalinės jungties konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite fiskalinio dokumento teikėjo konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**. Sukurkite naują jungties funkcinį profilį ir pasirinkite dokumento teikėją bei anksčiau įkeltą jungtį.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**. Sukurkite naują jungties techninį profilį ir pasirinkite jungtį, kurią įkėlėte anksčiau. Nustatykite jungties tipą į **Vidinis**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės** ir sukurkite naują fiskalinių jungčių grupę jungties funkciniam profiliui, kurį sukūrėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**. Sukurkite naują fiskalinės registracijos procesą ir fiskalinės registracijos proceso veiksmą ir pasirinkite anksčiau sukurtą fiskalinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų profilį, susietą su parduotuve, kurioje turėtų būti suaktyvintas registracijos procesas. Ant **Fiskalinės registracijos procesas** FastTab, pasirinkite fiskalinės registracijos procesą, kurį sukūrėte anksčiau. Ant **Fiskalinės paslaugos** FastTab, pasirinkite jungties techninį profilį, kurį sukūrėte anksčiau. 
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**. Atidarykite paskirstymo grafiką ir pasirinkite darbus **1070** ir **1090** perkelti duomenis į kanalo duomenų bazę.

### <a name="configure-the-digital-signature-parameters"></a>Konfigūruokite skaitmeninio parašo parametrus

Turite sukonfigūruoti sertifikatus, kurie bus naudojami skaitmeniniam pardavimo operacijų pasirašymui parduotuvėje. Pasirašymui naudojamas skaitmeninis sertifikatas, saugomas Azure Key Vault. Modernaus POS režimu neprisijungus pasirašyti taip pat galima naudojant skaitmeninį sertifikatą, kuris saugomas įrenginio, kuriame įdiegtas Modern POS, vietinėje saugykloje.

Kad galėtumėte naudoti skaitmeninį sertifikatą, saugomą Key Vault saugykloje, turite atlikti šiuos veiksmus.

1. „Key Vault“ saugykla turi būti sukurta. Rekomenduojame saugyklą diegti tame pačiame geografiniame regione kaip ir prekybos masto vienetas.
1. Sertifikatas turi būti įkeltas į „Key Vault“ saugyklą kaip „base64“ eilutės paslaptis.
1. „Application Object Server“ (AOS) programa turi būti įgaliota skaityti paslaptis iš „Key Vault“ saugyklos.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su Key Vault, žr [Pradėkite naudotis „Azure Key Vault“](/azure/key-vault/key-vault-get-started).

Toliau, ant **Key Vault parametrai** puslapyje, turite nurodyti parametrus, kad galėtumėte pasiekti „Key Vault“ saugyklą:

- **vardas** ir **apibūdinimas** – „Key Vault“ saugyklos pavadinimas ir aprašymas.
- **Key Vault URL** – „Key Vault“ saugyklos URL.
- **Key Vault klientas** – Interaktyvus kliento ID Azure Active Directory (Azure AD) programa, kuri autentifikavimo tikslais susieta su „Key Vault“ saugykla. Šis klientas turi turėti prieigą, kad galėtų skaityti paslaptis iš saugyklos.
- **Key Vault slaptasis raktas** – Slaptas raktas, susietas su Azure AD programa, kuri naudojama autentifikavimui Key Vault saugykloje.
- **vardas**, **·**, ir **Slapta nuoroda** – Sertifikato pavadinimas, aprašymas ir slapta nuoroda.

Tada turite sukonfigūruoti sertifikatų, saugomų Key Vault arba vietinėje sertifikatų saugykloje, jungtį. Ši jungtis naudojama pasirašymui kanalo pusėje.

1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**.
1. Ant **Nustatymai** FastTab, nurodykite šiuos skaitmeninio parašo parametrus:

    - **Slaptas vardas** – Pasirinkite slaptą pavadinimą, kurį anksčiau sukonfigūravote **Key Vault parametrai** puslapį.
    - **Vietinio sertifikato nykščio atspaudas** – Pateikite vietoje saugomo sertifikato nykščio atspaudą.
    - **Maišos algoritmas** – Nurodykite vieną iš palaikomų kriptografinių maišos algoritmų Microsoft .NET, toks kaip **SHA1**.
    - **Sertifikatų parduotuvės pavadinimas** – Šis laukas yra neprivalomas. Naudokite jį, norėdami nurodyti numatytąjį saugyklos pavadinimą, kurį reikia naudoti ieškant vietinių sertifikatų.
    - **Sertifikatų parduotuvės vieta** – Šis laukas yra neprivalomas. Naudokite jį, norėdami nurodyti numatytąją saugojimo vietą, kurią reikia naudoti ieškant vietinių sertifikatų.
    - **Pirmiausia išbandykite vietinį sertifikatą** – Pasirinkite šią parinktį, kad pagal numatytuosius nustatymus duomenims pasirašyti būtų naudojamas sertifikatas iš vietinės parduotuvės, o ne sertifikatas iš Key Vault.
    - **Suaktyvinkite sveikatos patikrinimą** – Daugiau informacijos apie sveikatos patikrinimo funkciją žr [Fiskalinės registracijos sveikatos patikrinimas](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Tik **SHA1** kriptografinis maišos algoritmas šiuo metu yra priimtinas Norvegijoje.
> - Numatytasis parduotuvės pavadinimas ir parduotuvės vieta pridedami siekiant supaprastinti vietinių sertifikatų paieškos procesą CRT. X509StoreProvider yra aplankų, kuriuose saugomi sertifikatai, sąrašas. Jei numatytasis parduotuvės pavadinimas ir numatytoji parduotuvės vieta nenurodyti, X509StoreProvider bando rasti sertifikatą visuose sąraše esančiuose aplankuose.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

### <a name="development-environment"></a>Talpinimo aplinka

Atlikite šiuos veiksmus, kad nustatytumėte kūrimo aplinką, kad galėtumėte išbandyti ir išplėsti pavyzdį.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidaryk **SequentialSignatureNorway.sln** sprendimas pagal **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ SequentialSignatureNorway**, ir pastatyti jį.
1. Diegti CRT plėtiniai:

    1. Surask CRT plėtinio diegimo programa:

        - **Prekybos masto vienetas:** Viduje konors **SequentialSignatureNorway\\ ScaleUnit\\ ScaleUnit.SequentialSignNorway.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ScaleUnit.SequentialSignNorway.Installer** montuotojas.
        - **Vietinis CRT Šiuolaikinėje POS:** Viduje konors **SequentialSignatureNorway\\ Šiuolaikinis POS\\ ModernPos.SequentialSignNorway.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ModernPos.SequentialSignNorway.Installer** montuotojas.

    1. Pradėkite CRT plėtinio diegimo programa iš komandinės eilutės:

        - **Prekybos masto vienetas:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Vietinis CRT Šiuolaikinėje POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **SequentialSignatureNorway build-pipeline.yaml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Įgalinkite šiuolaikinio POS skaitmeninį parašą neprisijungus

Norėdami įjungti šiuolaikinio POS skaitmeninį parašą neprisijungus, turite atlikti šiuos veiksmus, kai suaktyvinate Modern POS naujame įrenginyje.

1. Prisijunkite prie POS.
1. Ant **Duomenų bazės ryšio būsena** puslapį, įsitikinkite, kad neprisijungus pasiekiama duomenų bazė yra visiškai sinchronizuota. Kai vertė **Laukiantys atsisiuntimai** laukas yra **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Atsijunkite nuo POS.
1. Palaukite, kol neprisijungus pasiekiama duomenų bazė bus visiškai sinchronizuota.
1. Prisijunkite prie POS.
1. Ant **Duomenų bazės ryšio būsena** puslapį, įsitikinkite, kad neprisijungus pasiekiama duomenų bazė yra visiškai sinchronizuota. Kai vertė **Laukiančios operacijos neprisijungus esančioje duomenų bazėje** laukas yra **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Iš naujo atidarykite Modern POS.
