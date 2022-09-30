---
title: Masinis patvirtintų „Commerce“ savitarnos komponentų diegimas
description: Šiame straipsnyje paaiškinama, kaip naudoti savitarnos komponentų diegimo sistemą, kad jos automatiškai įdiegtų ir įdiegtų paslaugas.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 426473c14cdf9e171810aafd97dbb1afd5988b2f
ms.sourcegitcommit: 24673493d14f2045a08fe7240689bee34e099cb5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2022
ms.locfileid: "9589095"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Masinis patvirtintų „Commerce“ savitarnos komponentų diegimas

[!include [banner](../includes/banner.md)]

Šis straipsnis taikomas užantspauduotai sistemai, komponentų diegimo tarnyboms, kurios paleidžiamos kas mėnesį, pradedant nuo 10.0.18 versijos ir Microsoft Dynamics prieinamoms ciklo tarnybų (LCS) bendrai naudojamų turtų bibliotekoje. Nepamirškite, kad pirmieji keli šių naujų diegimo priemonių paleidimai yra pažymėti kaip **(Peržiūra)**. Tačiau vienintelis šio paskyrimo tikslas yra atskirti naujas diegimo įdiegtis, o Microsoft nustato, ar yra kokių nors papildomų funkcijų reikalavimų, kuriuos būtų galima naudoti. Tai nereiškia, kad diegimo programos nėra tinkamos gamybai. Remiantis šių naujų diegimo programų paleidimu Microsoft planuoja nusidėvinti senus (senesnius) diegimo planus 2023 m. spalio mėn. arba maždaug. 

Šiame straipsnyje paaiškinama, kaip naudoti naujas diegimo programas, norint atlikti automatinis diegimą ir atnaujinimų aptarnavimas naudojant komandų eilutės argumentus. Šie argumentai leidžia atlikti masinę diegimą keliais skirtingais būdais.

> [!NOTE]
> Nauja savitarnos paslauga, užantspauduotos diegimo programos nebus galimos programoje "Headquarters" ir jos bus galima atsisiųsti tik naudojant LCS.

## <a name="delimiters-for-mass-deployment"></a>Masinio diegimo skyrikliai

Šioje lentelėje rodomi skyrikliai, kuriuos galima naudoti vykdant komandų eilutę.


| Skyriklis                 | Aprašymas |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | "Microsoft" () atpažinimo ženklo Azure Active Directory išdavėjo Azure AD prefiksas. |
| -AsyncClientAadClientId | Kliento Azure AD ID, kurį turi naudoti "Async" klientas ryšio su "Headquarters" metu. |
| -AsyncClientAppInsclientsInstrumentationKey | "Async" kliento AppInsights instrumentavimo raktas. |
| -AsyncClientCertFullPath | Visiškai suformatuotas URN maršrutas, naudojantis nykščio atspaudą kaip "Async Azure AD " kliento tapatybės sertifikato vietos ieškos metriką, kuri turi būti naudojama autentifikuoti ryšiui su "Headquarters". Pavyzdžiui, yra `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` teisingai suformatuotas URL. Reikšmė bus **\<MyThumbprint\>** pakeista sertifikato nykščio atspaudu, kuris turi būti naudojamas. Nenaudokite šio parametro kartu su parametru **-AsyncClientCertThumbprint**. |
| -AsyncClientCertThumbprint | "Async" kliento tapatybės sertifikato, kurį reikia naudoti ryšio su " Azure AD Headquarters" nykščio atspaudas, kuris turi būti naudojamas autentifikuoti. Šis nykščio atspaudas bus **naudojamas ieškoti LocalMachine / Mano** parduotuvės vietoje ir siekiant rasti tinkamą naudotiną sertifikatą. Nenaudokite šio parametro kartu su parametru **-AsyncClientCertFullPath**. |
| -ClientAppIns turi būtiInstrumentationKey | AppInsights Kliento instrumentavimo raktas. |
| – CloudPosAppInsprogramsInstrumentationKey | Debesies EKA AppInsights instrumento raktas. |
| -Config | Konfigūracijos failas, kuris turėtų būti naudojamas diegiant. Failo vardo pavyzdys yra **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | Kliento Azure AD ID, kurį turi naudoti "Cloud POS" aktyvinant įrenginį. Šio parametro nereikia norint įdiegti vietiniame kompiuteryje. |
| -Įrenginio | Įrenginio ID, kaip parodyta programos **Headquarters** puslapyje Įrenginiai. |
| –EnvironmentId | Aplinkos ID. |
| -HardwareStationAppInsininkaisInstrumentationKey | Aparatūros stoties AppInsights instrumentinės įrangos raktas. |
| Diegti | Parametras, nurodantis, ar turi būti įdiegtas šios diegimo programos komponentas. Šio parametro reikia norint atlikti diegimą, jis neturi būti priekinio brūkšnio simbolio. |
| -InstallOffline | Naudojant "Modern POS" šis parametras nurodo, kad autonominė duomenų bazė taip pat turi būti įdiegta ir sukonfigūruota. Taip pat **naudokite parametrą -SQLServerName**. Kitu atveju diegimo programa bandys rasti numatytąjį egzempliorių, kuris atitiktų būtinuosius komponentus. Naudojant (Azure Active Directory) autentifikavimą Azure AD EKA ne tinkle funkcija neveikia, nes interneto ryšys reikalingas visada. |
| -Uosto | Prievadas, kurį reikia susieti su virtualiojo katalogo "Retail Server" ir naudoti. Jei prievadas nustatytas, bus naudojamas numatytasis prievadas 443. |
| -Užsiregistruok | Registro ID, kaip parodyta kasos **aparatų puslapyje**, būstinėje. |
| -RetailServerAadClientId | Kliento Azure AD ID, kurį turi naudoti "Retail Server" ryšio su "Headquarters" metu. |
| -RetailServerAadResourceId | "Retail Server" Azure AD programos išteklių ID, kuris turi būti naudojamas aktyvinant įrenginį. Šio parametro nereikia norint įdiegti vietiniame kompiuteryje. |
| –RetailServerCertFullPath | Visiškai suformatuotas URN maršrutas, naudojantis nykščio atspaudą kaip "Retail Server Azure AD " tapatybės sertifikato ieškos metriką, kurią reikia naudoti norint autentifikuoti ryšiui su "Headquarters". Pavyzdžiui, teisingai `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` suformatuotas URLN, kur vertė bus **\<MyThumbprint\>** pakeista sertifikato nykščio atspaudu, kuris turi būti naudojamas. Nenaudokite šio parametro kartu su parametru **-RetailServerCertThumbprint**. |
| –RetailServerCertThumbprint | "Retail Server" tapatybės sertifikato nykščio atspaudas, kurį reikia naudoti norint autentifikuoti Azure AD ryšį su "Headquarters". Šis nykščio atspaudas bus **naudojamas ieškoti LocalMachine / Mano** parduotuvės vietoje ir siekiant rasti tinkamą naudotiną sertifikatą. Nenaudokite šio parametro kartu su parametru **-RetailServerCertFullPath**. |
| -RetailServerURL | "Retail Server" URL, kurį turi naudoti diegimo programa. (Šis URL taip pat vadinamas "Commerce Scale Unit" \[CSU\] URL.) "Modern POS" ši vertė bus naudojama aktyvinant įrenginį. |
| -SkipAadCredentialsCheck| Switch, kuris nurodo, ar Azure AD reikia praleisti kredencialų būtinųjų komponentų tikrinimus. Numatytoji reikšmė yra **klaidinga**. |
| –SkipCertCheck | Raktas, nurodantis, ar reikia praleisti sertifikato būtinųjų komponentų tikrinimus. Numatytoji reikšmė yra **klaidinga**. |
| -SkipIisCheck | Switch, kuris nurodo, ar turi būti praleisti informacinių interneto paslaugų (IIS) būtinųjų komponentų tikrinimai. Numatytoji reikšmė yra **klaidinga**. |
| -SkipNetFrameworkCheck | Switch, kuris nurodo, ar reikia praleisti ".NET Framework" būtinųjų komponentų tikrinimus. Numatytoji reikšmė yra **klaidinga**. |
| -SkipScaleUnit Turi būti tikrinta | Perjungimo raktas, nurodantis, ar turi būti praleistas įdiegtų komponentų sveikatos tikrinimas. Numatytoji reikšmė yra **klaidinga**. |
| -SkipsChannelCheck | Switch, kuris nurodo, ar reikia praleisti saugius kanalo būtinuosius tikrinimus. Numatytoji reikšmė yra **klaidinga**. |
| -SkipSqlFullTextCheck | Raktas, nurodantis, ar reikia praleisti SQL serverio būtinojo komponento, kuriam reikia viso teksto ieškos, tikrinimą. Numatytoji reikšmė yra **klaidinga**. |
| -SkipSqlServerCheck | Raktas, nurodantis, ar turi būti praleisti SQL serverio būtinųjų komponentų tikrinimai. Numatytoji reikšmė yra **klaidinga**. |
| -SqlServerName | SQL serverio pavadinimas. Jei pavadinimas nenurodytas, diegimo programa bandys rasti numatytąjį egzempliorių. |
| -SslcertFullPath | Visiškai suformatuotas URN maršrutas, naudojantis nykščio atspaudą kaip sertifikato vietos paieškos metriką, kurią reikia naudoti HTTP srautui į svarstyklių vienetą šifruoti. Pavyzdžiui, teisingai `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` suformatuotas URLN, kur vertė bus **\<MyThumbprint\>** pakeista sertifikato nykščio atspaudu, kuris turi būti naudojamas. Nenaudokite šio parametro kartu su parametru **-SslCertThumbprint**. |
| -SslCertThumbprint | Sertifikato, kurį naudojant reikia šifruoti HTTP srautą iki svarstyklių vieneto, nykščio atspaudas. Šis nykščio atspaudas bus **naudojamas ieškoti LocalMachine / Mano** parduotuvės vietoje ir siekiant rasti tinkamą naudotiną sertifikatą. Nenaudokite šio parametro kartu su parametru **-SslCertFullPath**. |
| -StoreSystemAosUrl | Būstinės (AOS) URL. |
| -StoreSystemChannelDatabaseId | Kanalo duomenų bazės ID (pavadinimas). |
| -TenantId | Nuomininko Azure AD ID. |
| -TransactionServiceAzureAuthority | "Transaction Service" Azure AD institucija. |
| -TransactionServiceAzureResource | "Transaction Service" Azure AD išteklius. |
| -TrustSqlServerCertificate | Raktas, nurodantis, ar užmegzti ryšį su SQL serveriu reikia pasitikima serverio sertifikatu. Siekiant išvengti saugos rizikos, diegiant gamybą čia niekada neturėtų būti tiek vertė, kuri **yra teisinga**. Numatytoji reikšmė yra **klaidinga**. |
| -Daugiažodis | Registravimosi lygis, reikalaujamas diegiant. Paprastai ši vertė neturi būti naudojama. |
| -WindowsPhoneAppInsprogramsInstrumentationKey | Aparatūros stoties AppInsights instrumentinės įrangos raktas. |

## <a name="general-overview"></a>Bendroji peržiūra

Nauja savitarnos diegimo diegimo priemonių sistema turi įvairių funkcijų ir patobulinimų. Nauja sistema šiuo metu sugeneruoja tik "Modern POS", aparatūros stoties ir CSU (savitarnos), diegimo programa. Svarbu suprasti, kad užantspauduotos diegimo programos naudoja pagrindinę komandų eilutę, kuri turėtų atrodyti panašiai kaip pateikta toliau pateiktame pavyzdyje. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Diegimo programai reikia parametrų **diegimo** (arba **šalinimo**, norint pašalinti įdiegtį) ir bet kokius to diegimo parametrus. **Parametro** pavadinime turi būti visi reikalingi parametrai, pvz., registras, CSU URL ar sertifikato informacija. **Parametrų** informacija turi apimti bet kokią papildomą informaciją apie parametrus.

Užantspauduota sistema sukurta tam, kad būtų leidžiama atlikti šiuos pakeitimus:
- **Užantspauduota** – naujos diegimo programos sistema visiškai atskiria Microsoft paskirstytų pagrindinio komponento diegimo komponentus nuo extensibility pagrįstų tinkinimų. Tinkinimai bus įdiegti vėliau, bet bus toliau diegiami atnaujinimų atžvilgiu (kad naujinimai būtų leidžiami tik "Microsoft" pagrindinio komponento, tik pritaikymams arba abiems).
- **GUI-mažiau** – nebėra vartotojo sąsajos (vartotojo sąsajos). Todėl yra visiškai komandinės eilutės vykdomasis failas, skirtas kiekvienai komponentų diegimo programai. Šis pakeitimas yra vienas iš kelių pagrindinių keitimų arba priemonių, kurios naudojamos naujos diegimo programos sistemai sutelkti, kad būtų galima naudoti masiniam diegimui.
- **Išplėstinės** diegimo programos registravimas – išplėstiniai diegimo programos žurnalai leidžia geriau patikrinti diegimo užbaigimą arba triktį, atlikti veiksmai ir sugeneruoti įspėjimai ar klaidos.
- **Valymas** – naujoje sistemoje komponentų diegimo programos diegimo programos veikia daug toliau, kad galėtų palaikyti diegimo katalogų valymo procesą, išvalydami visą komponentų aplanko turinį prieš diegdami naujesnius komponentus. Šis valymas užtikrina, kad nėra jokių palikti failų, kurie gali sukelti problemų ir neleidžia sėkmingai įdiegti.

Į naują sistemą nebuvo perkelti trys komponentai: virtualusis išorinis simuliatorius, "Async Server Connector" paslauga (naudojama "Dynamics AX 2012 R3" palaikymas) ir "Real-time Service" pakeitimas (naudojama "Dynamics AX 2012 R3" palaikyme).

> [!NOTE]
> Diegimo programos saugomos vietoje ir užlaikomos.  Laikui bėgant svarbu valdyti arba panaikinti išlaikytus diegimo įrašus, kad diske nebūtų vietos. Rekomenduojama palikti dabartinę pagrindinių komponentų diegimo tarpiklį ir visas naujausių versijų plėtinių diegimo versijas, kad būtų galima atsikurti iš ypač situacijų.

## <a name="migration"></a>Migracijos

Norint perkelti iš senų savitarnos sistemos komponentų diegimo programų į naujas sistemos komponentų diegimo tarnybas, reikia pašalinti senus komponentus.

- **"Modern POS** " – naujos diegimo programos sistema lėmė, kad programa gaus naują programos parašo ID. Todėl prieš įdiegiant naują "Modern POS" komponentą būtina pašalinti visus senus komponentus. Dėl visiško pašalinimo reikalavimo įrenginio aktyvinimas bus reikalingas dar kartą. (Šis įrenginio suaktyvinimas iš naujo yra vienkartis reikalavimas, jei šalinimo laikas nesikartoja.)
- **Aparatūros** stotis – kaip IIS svetainė, naujo diegimo programos sistemai reikia iš naujo atlikti pagrindinio aplanko struktūrą. Todėl prieš įdiegiant naują aparatūros stoties komponentą būtina pašalinti visus senus komponentus.
- **"Commerce Scale Unit" (CSU, self-hosted)** – kaip IIS žiniatinklio svetainių serija, nauja diegimo programos sistema reikalauja iš naujo atlikti pagrindinio aplanko struktūrą.  Todėl prieš įdiegiant naują CSU (savitarnos nuomojamą) komponentą būtina pašalinti visus senus komponentus.

## <a name="modern-pos"></a>„Modern POS“

### <a name="before-you-begin"></a>Prieš pradedant

Svarbu pašalinti seną savitarnos "Modern POS" komponentą. Norėdami gauti daugiau informacijos, peržiūrėkite anksčiau šiame straipsnyje nurodytus perkėlimo veiksmus.

> [!NOTE]
> Viename kompiuteryje, pvz., programavimo topologijoje ar demonstracinę aplinką, arba kai "Commerce Scale Unit" ir "Modern POS" yra įdiegti tame pačiame kompiuteryje, galima nustatyti, kad "Store Commerce" nebegalės baigti aktyvinti įrenginio. Ši problema kyla dėl to, kad "Store Commerce" negali iš naujo skambinti tam pačiam kompiuteriui (t.vz., išk ryšys su tuo pačiu kompiuteriu). Kol tai niekada neturėtų būti gamybos parametrų scenarijus, problema gali būti sumažinta įgalinant AppContainer ciklo atšaukimo išimtį, kad būtų galimi ryšiai su tuo pačiu kompiuteriu. Įvairios programos yra viešai prieinamos, kad padėtų įgalinti šį ciklo atjungią. Daugiau informacijos apie ciklo atsarginį ryšį žr. Kaip įgalinti [loopback ir šalinti tinklo atskyrimo triktis](/previous-versions/windows/apps/hh780593(v=win.10)). Svarbu suprasti, kad loopback gali būti saugos rizika, todėl nerekomenduojama naudoti loopback, nebent to reikia.

### <a name="examples-of-silent-deployment"></a>Tyliojo diegimo pavyzdžiai

Šiame skyriuje pateikiami komandų, kurios naudojamos "Modern POS" įdiegti, pavyzdžiai.

#### <a name="silently-install-modern-pos"></a>Automatiškai diegti "Modern POS"

Ši komanda tyliuoju būdu įdiegia (arba atnaujina) "Modern POS". Ji turi standartinę komandų struktūrą, kuri naudojama automatiškai aptarnauti šiuo metu įdiegtus komponentus. Struktūra naudoja pagrindines **&lt; InstallerName.exe&gt; reikšmes**.

Šioje pagrindinei komandai rodoma galimų pasirinkčių, jei reikia įdiegti, atveju. Rekomenduojama šią komandą naudoti pirmą kartą tikrinant arba naudojant diegimo programą.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> "Modern POS" konfigūracijos failo nereikia. Diegimo programa dabar turi įvairių verčių, naudojamų aktyvinant įrenginį, parametrus (parodyta anksčiau šiame straipsnyje).

Toliau pateikta komanda nurodo visus parametrus, kurie turi būti naudojami įrenginio aktyvinimo metu įdiegus "Modern POS" programą. Šiame pavyzdyje naudojamasĖs-3 **registras**, kuris paprastai naudojamas demonstracinių Dynamics 365 Commerce duomenų vertė.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Toliau nurodyta komanda nurodo parametrus, kuriuos reikia naudoti norint įdiegti ir konfigūruoti autonominę duomenų bazę. SQL serveris nurodomas kartu su konfigūracijos failu, kuris turi būti naudojamas.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Norint pasiekti norimus diegimo rezultatus, galima maišyti ir suderinti šias sąvokas.

## <a name="hardware-station"></a>Aparatūros stotis

### <a name="before-you-begin"></a>Prieš pradedant

Svarbu pašalinti seną savitarnos aparatūros stoties komponentą. Norėdami gauti daugiau informacijos, peržiūrėkite anksčiau šiame straipsnyje nurodytus perkėlimo veiksmus. Nebėra prekybininko sąskaitos informacijos įrankio. Prekybininko sąskaitos informacija įdiegiama, kai EKA terminalas yra susietas su aparatūros stotyje. Tikrinant šią diegimo programą pirmą kartą, labai rekomenduojama vykdyti šią komandą:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Tyliojo diegimo pavyzdžiai

Šiame skyriuje pateikiami komandų, kurios naudojamos aparatūros stotis įdiegti, pavyzdžiai.

#### <a name="silently-install-hardware-station"></a>Automatiškai diegti aparatūros stotį

Ši komanda automatiškai įdiegia (arba atnaujina) aparatūros stotį. Ji turi standartinę komandų struktūrą, naudojamą šiuo metu įdiegtims aptarnavimo komponentams. Struktūra naudoja pagrindines **&lt; InstallerName.exe&gt; reikšmes**.

Toliau nurodyta pagrindinė komanda vykdo vykdomųjų failų diegimo programą.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Aparatūros stotis konfigūracijos failo nereikia. Diegimo programa dabar turi įvairių verčių, kurios reikalingos, parametrus (parodyta anksčiau šiame straipsnyje).

Toliau pateikiama komanda nurodo visus parametrus, kurių reikia norint praleisti būtinųjų komponentų tikrinimus standartinio diegimo metu. 

> [!NOTE]
> Nerekomenduojama praleisti tikrinimų nepatarus iš anksto arba programavimo situacijose.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Kaip įprasta, norint pasiekti norimus diegimo rezultatus, įprasta maišyti ir atitikti šias sąvokas.

## <a name="commerce-scale-unit-self-hosted"></a>„Commerce Scale Unit“ (savarankiškai nuomojamas)

Tikrinant šią diegimo programą pirmą kartą, labai rekomenduojama vykdyti šią komandą:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Prieš pradedant

Yra labai svarbu pašalinti seną savitarnos CSU (savitarnos) komponentą. Norėdami gauti daugiau informacijos, peržiūrėkite anksčiau šiame straipsnyje nurodytus perkėlimo veiksmus.

### <a name="examples-of-silent-deployment"></a>Tyliojo diegimo pavyzdžiai

Šiame skyriuje pateikiami komandų, kurios naudojamos CSU įdiegti (savitarnos), pavyzdžiai.

#### <a name="silently-install-csu-self-hosted"></a>Automatiškai diegti CSU (savitarnos),

Ši komanda automatiškai įdiegia (arba atnaujina) CSU (savitarnos). Ji turi standartinę komandų struktūrą, kuri naudojama automatiškai aptarnauti šiuo metu įdiegtus komponentus. Struktūra naudoja pagrindines **&lt; InstallerName.exe&gt; reikšmes**.

Lyginant su kitomis savitarnos įdiegtimis, "Commerce Scale Unit" (CSU) yra sudėtingesnė ir tam reikia daug papildomos informacijos. Toliau nurodyta komanda yra minimali komanda (su parametrais), reikalinga vykdomai failų diegimo programai paleisti, kai nėra konfigūracijos failo.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Konfigūracijos failas vis dar reikalingas CSU (savitarnos).

Toliau pateikta komanda yra išsamesnė komanda, kuri vykdo vykdomojo failo diegimo programą su kai kuriais alternatyviais parametrais.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Toliau pateikta komanda nurodo parametrus, būtinus norint praleisti būtinųjų komponentų tikrinimus atliekant standartinį diegimą. 

> [!NOTE]
> Nerekomenduojama praleisti tikrinimų nepatarus iš anksto arba programavimo situacijose.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Norint pasiekti norimus diegimo rezultatus, galima maišyti ir suderinti šias sąvokas.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
