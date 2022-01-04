---
title: Norvegijos grynųjų pinigų registrų diegimo rekomendacijos
description: Šioje temoje pateikiama informacija apie tai, kaip įgalinti grynųjų pinigų registro funkciją Microsoft Dynamics 365 Commerce Norvegijos lokalizavimui.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c7e64dbfe6a300c097b5b3711ac4310f3386df11
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944745"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norvegijos grynųjų pinigų registrų diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip įgalinti grynųjų pinigų registro funkciją Microsoft Dynamics 365 Commerce Norvegijos lokalizavimui. Lokalizavimą sudaro keli komponentų plėtiniai. Šie plėtiniai leidžia atlikti tokius veiksmus, kaip pasirinktinių laukų spausdinimas kvituose, papildomų audito įvykių registravimas, pardavimo operacijos ir mokėjimo operacijos elektroniniame kasos aparate (EKA), skaitmeniniu būdu pasirašant pardavimo operacijas ir ataskaitų spausdinimas vietiniu formatu. Daugiau informacijos apie Norvegijos lokalizavimą ieškokite Norvegijos [grynųjų pinigų registro funkcija](./emea-nor-cash-registers.md). Norėdami gauti daugiau informacijos apie "Commerce for Norway" konfigūravimą, [žr. "Commerce for Norway" nustatykite](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų, šiuo metu jo [negalima](../dev-itpro/build-pipeline.md) naudoti šiai lokalizavimo funkcijai. Turite naudoti Norvegijos skaitmeninio pasirašymo pavyzdžio versiją ankstesnėje "Retail" programinės įrangos kūrimo rinkinio (SDK) versijoje, kūrėjų virtualiojoje kompiuteryje (VM) ciklo tarnybose Microsoft Dynamics (LCS). Daugiau informacijos rasite Norvegijos [(senesnės programos) grynųjų pinigų registrų diegimo](./emea-nor-loc-deployment-guidelines.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

## <a name="set-up-fiscal-registration-for-norway"></a>Nustatyti Norvegijos finansų registraciją

Norvegijos finansinio registracijos pavyzdys pagrįstas finansinio [integravimo funkcija ir yra](fiscal-integration-for-retail-channel.md) "Retail" SDK dalis. Pavyzdys yra sprendimų saugyklos **src \\ FiscalIntegration \\ SequentialSitctureNorway aplanke**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (pvz., paleidimo [/ 9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway) pavyzdys). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas ir fiskalinė jungtis, kuri yra "Commerce runtime" () CRT plėtiniai. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

Atlikite finansinio registravimo nustatymo veiksmus, kurie aprašyti [nustatyti "Commerce" kanalų fiskalinę](./setting-up-fiscal-integration-for-retail-channel.md) integraciją:

1. [Nustatykite finansinio registravimo](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) procesą. Įsitikinkite, kad užsirašykite finansinių registracijų proceso parametrų, [kurie yra specifiniai](#configure-the-fiscal-registration-process) Norvegijai.
1. [Nustatyti klaidų tvarkymo](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) parametrus.
1. [Įgalinkite atidėtos finansinio registravimo vykdymą rankiniu](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) būdu.
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="configure-the-fiscal-registration-process"></a>Konfigūruoti finansinio registravimo procesą

Vadovaukitės šiais veiksmais Norvegijos finansinio registravimo procesui "Commerce Headquarters" įgalinti.

1. Atsisiųskite finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus iš "Commerce SDK":

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Atidarykite paskutinę galima paleidimo šaką (pvz., **[paleidimas / 9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Atidarykite **src \> FiscalIntegration \> SequentialSi sunorway \> CommerceRuntime.**
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą, kurį sudaro **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSinorwaySample.xml** (pvz., paleidimo [failas/9.34).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)
    1. Atsisiųskite finansinio jungties konfigūracijos failą, nurodytą **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSi parametrųNorwaySample.xml** (pvz., [leidimo/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml) failas).

1. Eikite į **"Retail" ir \> "Commerce Headquarters" nustatymo \>\> parametrų bendrai naudojamus parametrus**. Skirtuke **Bendra** nustatykite **pasirinktį Įgalinti** fiskalinį integravimą kaip **Taip**.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" jungtis ir įkelkite anksčiau **\>\>\>** atsisiųstą "Fiscal Connector" konfigūracijos failą.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" dokumentų teikėjai ir įkelkite anksčiau **\>\>\>** atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir \> "Commerce" kanalo nustatymo \> "Fiscal integration \> Connector" funkcinius** profilius. Sukurkite naują jungties funkcinį profilį ir pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį.
1. Eikite į **"Retail" ir \> "Commerce \> Channel" nustatymo "Fiscal \> integration Connector" techninius profilius.** Sukurkite naują jungties techninio profilio ir pasirinkite jungtį, kurią įkeliate anksčiau. Nustatyti jungties tipą **Vidinis**.
1. Eikite į "Retail" ir "Commerce Channel" nustatymo "Fiscal integration Fiscal Connector" grupes ir sukurkite naują anksčiau sukurto jungties funkcinio profilio **\>\>\>** "Fiscal Connector" grupę.
1. Eikite į **"Retail" ir "Commerce \>\> Channel" nustatymo "Fiscal integration \> Fiscal" registracijos** procesus. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso** "FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą. Finansinių **paslaugų** "FastTab" pasirinkite senesnę jungties techninio profilio versiją, kurią sukūrėte anksčiau. 
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**. Atidaryti paskirstymo grafiką ir pasirinkti užduotis **1070** ir **1090** duomenims perkelti į kanalo duomenų bazę.

### <a name="configure-the-digital-signature-parameters"></a>Skaitmeninio parašo parametrų konfigūravimas

Turite sukonfigūruoti sertifikatus, kurie bus naudojami pardavimo operacijoms skaitmeniniu būdu pasirašyti parduotuvėje. Skaitmeninis sertifikatas, saugomas "Azure" rakto "Vault", naudojamas pasirašymui atlikti. "Modern POS" autonominiam režimui pasirašant galima naudoti skaitmeninį sertifikatą, kuris saugomas vietiniame kompiuterio, kuriame įdiegta "Modern POS", saugykloje.

Kad būtų galima naudoti skaitmeninį sertifikatą, kuris saugomas "Key Vault" saugykloje, reikia atlikti šiuos veiksmus.

1. Būtina sukurti "Key Vault" saugyklą. Rekomenduojame saugyklą diegti tame pačiame geografiniame regione kaip ir "Commerce Scale Unit".
1. Sertifikatas turi būti įkeltas į rakto Vault saugyklą kaip base64 eilutės slaptą.
1. Programos objektų serverio (AOS) programa turi būti įgaliota skaityti paslapius iš rakto Vault saugyklos.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su "Key Vault", žr.["Pradėkite naudodami "Azure Key](/azure/key-vault/key-vault-get-started) Vault".

Tada, **"Key Vault" parametrų puslapyje, turite nurodyti parametrus, kad būtų galima** pasiekti "Key Vault" saugyklą:

- **Pavadinimas** ir aprašymas – **·** "Key Vault" saugyklos pavadinimas ir aprašas.
- **Rakto "Vault"** URL – "Key Vault" saugyklos URL.
- **Kodo Vault klientas – interaktyvus () programos, susietos su rakto Vault saugykla,** Azure Active Directory Azure AD autentifikavimo tikslais, interaktyvios kliento ID. Šis klientas turi turėti prieigą skaityti iš saugyklos slapymetes.
- **Rakto Vault slapyvo raktas – slaptasis raktas, susietas su** Azure AD programa, kuri naudojama autentifikuoti "Key Vault" saugykloje.
- **Pavadinimas,** **aprašymas ir** **slapti nuoroda –** sertifikato pavadinimas, aprašymas ir slapti nuoroda.

Po to turite sukonfigūruoti savo sertifikatų, saugomų rakto Vault arba vietinio sertifikato saugykloje, jungtį. Ši jungtis naudojama norint pasirašyti kanalo pusėje.

1. Eikite į **"Retail" ir \> "Commerce \> Channel" nustatymo "Fiscal \> integration Connector" techninius profilius.**
1. Parametrų **·** "FastTab" nurodykite šiuos skaitmeninių parašų parametrus:

    - **Slapto** vardo – pasirinkite slaptą pavadinimą, kurį anksčiau konfigūravote **"Key Vault" parametrų** puslapyje.
    - **Vietinis sertifikato** nykščio atspaudas – pateikti vietoje saugomo sertifikato nykščio atspaudą.
    - **Maišos** algoritmas – nurodyti vieną iš kriptografijos maišos algoritmų, kuriuos Microsoft .NET palaiko, pvz., **SHA1**.
    - **Sertifikato saugyklos** pavadinimas – šis laukas nėra būtinas. Naudokite jį, norėdami nurodyti numatytąjį saugyklos pavadinimą, kurį reikia naudoti ieškant vietinių sertifikatų.
    - **Sertifikato saugyklos** vieta – šis laukas nėra būtinas. Naudokite jį, norėdami nurodyti numatytąją saugojimo vietą, kurią reikia naudoti ieškant vietinių sertifikatų.
    - **Iš pradžių pabandykite vietinį sertifikatą – pasirinkite šią pasirinktį, norėdami naudoti vietinės parduotuvės sertifikatą pagal numatytuosius nustatymus pasirašymo duomenims, o ne iš** rakto Vault.
    - **Aktyvinti sveikatos** tikrinkite – daugiau informacijos apie sveikatos tikrinimo funkciją žr. [iždo registracijos sveikatos](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check) tikrinimas.

> [!NOTE]
> - Norvegijai **šiuo metu priimtinas tik SHA1** kriptografijos maišos algoritmas.
> - Numatytasis parduotuvės pavadinimas ir parduotuvės vieta įtraukiami, kad būtų paprasčiau ieškoti vietinių CRT sertifikatų. X509StoreProvider yra aplankų, kuriuose saugomi sertifikatai, sąrašas. Jei nenurodytas numatytasis parduotuvės pavadinimas ir numatytoji parduotuvės vieta, X509StoreProvider bando rasti sertifikatą visuose jos sąrašo aplankuose.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

### <a name="development-environment"></a>Talpinimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Dalyje **·** **Dynamics365Commerce.Solutions \\ FiscalIntegration \\ SequentialSi siuntiniųnorway atidarykite sprendimą SequentialSi siuntiniųnorway ir sukurkite** jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit": aplanke** **SequentialSi pradūrūrojeNorway \\\\ ScaleUnit.SequentialSignNorway.Installer talpyklos \\\\ debug \\ net461** raskite **aplanką ScaleUnit.SequentialSignNorway.Installer diegimo** kūrėjas.
        - **Vietinė CRT "Modern POS": aplanke** **SequentialSi \\ installertureNorway \\ ModernPOS ModernPos.SequentialSignNorway.Installer talpyklos \\\\ debug \\ net461** raskite **ModernPos.SequentialSignNorway.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **"Modern CRT POS" vieta:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **SequentialSi katalogeNorway build-pipeline.jaml šablono FAILĄ JAML galima rasti sprendimų saugyklos YAML_Files pardavimo** **galimybių \\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>"Modern POS" skaitmeninio parašo įgalinimas neprisijungus

Norėdami įjungti skaitmeninį parašą "Modern POS" neprisijungus, turite atlikti šiuos veiksmus, kai naujame įrenginyje suaktyvinsite "Modern POS".

1. Prisijunkite prie POS.
1. Duomenų bazės **ryšio būsenos** puslapyje įsitikinkite, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių **atsisiuntimų lauko vertė** yra **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Atsijungti nuo EKA.
1. Palaukite, kol autonominė duomenų bazė bus visiškai sinchronizuojama.
1. Prisijunkite prie POS.
1. Duomenų bazės **ryšio būsenos** puslapyje įsitikinkite, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių operacijų **vertė autonominės duomenų bazės lauke** yra **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Iš naujo atidarykite modernų EKA.
