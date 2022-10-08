---
title: Norvegijos grynųjų pinigų registrų diegimo rekomendacijos
description: Šiame straipsnyje pateikta informacija apie tai, kaip įgalinti kasos aparato funkcijas Microsoft Dynamics 365 Commerce Norvegijos lokalizavimui.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 0e66ef93e65fecaca23f0434c386507a0672d251
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631321"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norvegijos grynųjų pinigų registrų diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Veiksmus, aprašytus šiame straipsnyje, turite atlikti tik tada, jei naudojate Microsoft Dynamics 365 Commerce 10.0.29 arba vėlesnę versiją. Naudojant "Commerce" 10.0.28 arba senesnę versiją, reikia naudoti ankstesnę "Retail" programinės įrangos kūrimo rinkinio (SDK) versiją programavimo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Norėdami gauti daugiau informacijos, žr. [Norvegijos grynųjų pinigų registrų diegimo gaires (iš ankstesnės programos)](./emea-nor-loc-deployment-guidelines.md). Jei naudojate "Commerce" 10.0.28 ar naujesnę versiją ir pereinate prie "Commerce" versijos 10.0.29 ar vėlesnės versijos, [turite atlikti veiksmus, nurodytus Norvegijos senesnėje "Commerce" versijoje](./emea-nor-fi-migration.md).

Šiame straipsnyje pateikta informacija apie tai, kaip įgalinti grynųjų pinigų registro funkciją Norvegijos komercijos lokalizavimui. Lokalizavimą sudaro keli komponentų plėtiniai, kurie leidžia atlikti tokius veiksmus, kaip pasirinktinių laukų spausdinimas kvituose, papildomų audito įvykių registravimas, pardavimo operacijos ir elektroninio kasos aparato (EKA) mokėjimo operacijos, skaitmeniniu būdu pasirašant pardavimo operacijas ir ataskaitų spausdinimas vietiniu formatu. Daugiau informacijos apie Norvegijos lokalizavimą ieškokite Norvegijos grynųjų [pinigų registro funkcija](./emea-nor-cash-registers.md). Norėdami gauti daugiau informacijos apie "Commerce for Norway" konfigūravimą, žr [. "Commerce for Norway" nustatykite](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

## <a name="set-up-fiscal-registration-for-norway"></a>Nustatyti Norvegijos finansų registraciją

Norvegijos finansinio registracijos pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ SequentialSikcijosnorway**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas ir fiskalinė jungtis, kuri yra "Commerce runtime" () plėtiniai CRT. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

Atlikite finansinio registravimo nustatymo veiksmus, kurie aprašyti [nustatyti "Commerce" kanalų fiskalinę integraciją](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite finansinio registravimo procesą](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Įsitikinkite, kad užsirašykite finansinių registracijų proceso parametrų, kurie [yra specifiniai Norvegijai](#configure-the-fiscal-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinkite atidėtų finansinių duomenų registravimą neautomatiniu būdu](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigūruoti finansinio registravimo procesą

Vadovaukitės šiais veiksmais Norvegijos finansinio registravimo procesui "Commerce Headquarters" įgalinti.

1. Atsisiųskite finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus iš "Commerce SDK":

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Atidaryti paskutinę galimas paleidimo šakas.
    1. Atidarykite **src \> FiscalIntegration \> SequentialSi sunorway \> CommerceRuntime**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą **, kurį sudaro DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSinorwaySample.xml**.
    1. Atsisiųskite finansinio jungties konfigūracijos failą, kurį reikia **atidaryti per Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSi parametrųNorwaySample.xml**.

1. Eikite į " **Retail" ir "Commerce \> Headquarters" nustatymo \> parametrų bendrai \> naudojamus parametrus**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurkite naują jungties funkcinį profilį ir pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite jungtį, kurią įkeliate anksčiau. Nustatyti jungties tipą **Vidinis**.
1. Eikite į **"Retail" ir "Commerce \> Channel \> " nustatymo "Fiscal integration \> Fiscal Connector" grupes ir sukurkite naują anksčiau sukurto jungties funkcinio profilio "Fiscal Connector**" grupę.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą. Finansinių paslaugų **"** FastTab" pasirinkite senesnę jungties techninio profilio versiją, kurią sukūrėte anksčiau. 
1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**. Atidaryti paskirstymo grafiką ir pasirinkti užduotis **1070** ir **1090** duomenims perkelti į kanalo duomenų bazę.

### <a name="configure-the-digital-signature-parameters"></a>Skaitmeninio parašo parametrų konfigūravimas

Turite sukonfigūruoti sertifikatus, kurie bus naudojami pardavimo operacijoms skaitmeniniu būdu pasirašyti parduotuvėje. Skaitmeninis sertifikatas, saugomas "Azure" rakto "Vault", naudojamas pasirašymui atlikti. "Modern POS" autonominiam režimui pasirašant galima naudoti skaitmeninį sertifikatą, kuris saugomas vietiniame kompiuterio, kuriame įdiegta "Modern POS", saugykloje.

Kad būtų galima naudoti skaitmeninį sertifikatą, kuris saugomas "Key Vault" saugykloje, reikia atlikti šiuos veiksmus.

1. Būtina sukurti "Key Vault" saugyklą. Rekomenduojame saugyklą diegti tame pačiame geografiniame regione kaip ir "Commerce Scale Unit".
1. Sertifikatas turi būti įkeltas į rakto Vault saugyklą kaip base64 eilutės slaptą.
1. Programos objektų serverio (AOS) programa turi būti įgaliota skaityti paslapius iš rakto Vault saugyklos.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su "Key Vault", žr [. "Pradėkite naudodami "Azure Key Vault"](/azure/key-vault/key-vault-get-started).

Tada, " **Key Vault" parametrų** puslapyje, turite nurodyti parametrus, kad būtų galima pasiekti "Key Vault" saugyklą:

- **Pavadinimas** ir **aprašymas** – "Key Vault" saugyklos pavadinimas ir aprašas.
- **Rakto "Vault" URL – "Key Vault" saugyklos URL**.
- **Kodo Vault klientas** – autentifikavimo tikslais Azure Active Directory interaktyvios programos,Azure AD susietos su "Key Vault" saugykla, interaktyvios kliento ID. Šis klientas turi turėti prieigą skaityti iš saugyklos slapymetes.
- **Rakto Vault slapyvo** raktas – slaptasis Azure AD raktas, susietas su programa, kuri naudojama autentifikuoti "Key Vault" saugykloje.
- **Pavadinimas**, **aprašymas** ir slapti **nuoroda** – sertifikato pavadinimas, aprašymas ir slapti nuoroda.

Po to turite sukonfigūruoti savo sertifikatų, saugomų rakto Vault arba vietinio sertifikato saugykloje, jungtį. Ši jungtis naudojama norint pasirašyti kanalo pusėje.

1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**.
1. Parametrų **"** FastTab" nurodykite šiuos skaitmeninių parašų parametrus:

    - **Slapto** vardo – pasirinkite slaptą pavadinimą, kurį anksčiau konfigūravote " **Key Vault" parametrų** puslapyje.
    - **Vietinis sertifikato nykščio** atspaudas – pateikti vietoje saugomo sertifikato nykščio atspaudą.
    - **Maišos algoritmas** – nurodyti vieną iš kriptografijos maišos algoritmų, kuriuos palaiko Microsoft .NET, pvz., **SHA1**.
    - **Sertifikato saugyklos pavadinimas** – šis laukas nėra būtinas. Naudokite jį, norėdami nurodyti numatytąjį saugyklos pavadinimą, kurį reikia naudoti ieškant vietinių sertifikatų.
    - **Sertifikato saugyklos vieta** – šis laukas nėra būtinas. Naudokite jį, norėdami nurodyti numatytąją saugojimo vietą, kurią reikia naudoti ieškant vietinių sertifikatų.
    - **Iš pradžių pabandykite vietinį** sertifikatą – pasirinkite šią pasirinktį, norėdami naudoti vietinės parduotuvės sertifikatą pagal numatytuosius nustatymus pasirašymo duomenims, o ne iš rakto Vault.
    - **Aktyvinti sveikatos** tikrinkite – daugiau informacijos apie sveikatos tikrinimo funkciją žr. iždo [registracijos sveikatos tikrinimas](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Norvegijai šiuo **metu priimtinas tik SHA1** kriptografijos maišos algoritmas.
> - Numatytasis parduotuvės pavadinimas ir parduotuvės vieta įtraukiami, kad būtų paprasčiau ieškoti vietinių sertifikatų CRT. X509StoreProvider yra aplankų, kuriuose saugomi sertifikatai, sąrašas. Jei nenurodytas numatytasis parduotuvės pavadinimas ir numatytoji parduotuvės vieta, X509StoreProvider bando rasti sertifikatą visuose jos sąrašo aplankuose.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

#### <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dalyje Dynamics365Commerce.Solutions** **\\ FiscalIntegration\\ SequentialSi siuntiniųnorway atidarykite sprendimą SequentialSi siuntiniųnorway** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** aplanke SequentialSi pradūrūrojeNorway **ScaleUnit.SequentialSignNorway.Installer\\ talpyklos debug\\ net461\\\\ raskite aplanką ScaleUnit.SequentialSignNorway.Installer\\** diegimo **kūrėjas.**
        - **Vietinė CRT "Modern POS":** **aplanke SequentialSi installertureNorway\\ ModernPOS\\ ModernPos.SequentialSignNorway.Installer\\\\ talpyklos debug\\ net461** raskite **ModernPos.SequentialSignNorway.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. SequentialSi katalogeNorway build-pipeline.jaml **šablono FAILĄ JAML** **galima rasti sprendimų saugyklos YAML_Files\\**[Dynamics 365 Commerce pardavimo galimybių aplanke.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>"Modern POS" skaitmeninio parašo įgalinimas neprisijungus

Norėdami įjungti skaitmeninį parašą "Modern POS" neprisijungus, turite atlikti šiuos veiksmus, kai naujame įrenginyje suaktyvinsite "Modern POS".

1. Prisijunkite prie POS.
1. Duomenų bazės **ryšio būsenos puslapyje įsitikinkite**, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių atsisiuntimų **lauko vertė yra** **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Atsijungti nuo EKA.
1. Palaukite, kol autonominė duomenų bazė bus visiškai sinchronizuojama.
1. Prisijunkite prie POS.
1. Duomenų bazės **ryšio būsenos puslapyje įsitikinkite**, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių operacijų vertė **autonominės duomenų bazės lauke yra** **0** (nulis), duomenų bazė visiškai sinchronizuojama.
1. Iš naujo atidarykite modernų EKA.
