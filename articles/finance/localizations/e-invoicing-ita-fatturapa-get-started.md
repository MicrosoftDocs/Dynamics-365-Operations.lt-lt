---
title: Nustatyti tiesioginį ItalijosturaPA integravimą su SDI
description: Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Italijos elektroninių SF išrašymo ir nustatyti tiesioginį Italijos AsturaPA integravimą su exchange sistema (SDI).
author: gionoder
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e050d3896b2ba10433e166995d6fc405996cf0b2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267164"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Nustatyti tiesioginį ItalijosturaPA integravimą su SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Italijos elektroninių SF išrašymas šiuo metu gali nepatebėti visų funkcijų, galimų elektroninėms Microsoft Dynamics SF 365 finansuose ir Dynamics 365 Supply Chain Management.

Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti naudoti Italijos finansų ir tiekimo grandinės valdymo elektroninių SF išrašymą. Tai padės jums atlikti konfigūravimo veiksmus, kurie priklauso nuo šalies / regiono kontrolės konfigūracijos tarnybose (RCS). Šie veiksmai papildo veiksmus, aprašytus skyriuje Darbo pradžia [naudojant elektroninių SF išrašymą](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami šiame straipsnyje nurodytus veiksmus, turite įvykdyti šiuos būtinuosius komponentus:

- Atlikite veiksmus darbo su [elektroninių SF išrašymu pradžia](e-invoicing-get-started.md).
- Importuoti Italijos **EsturaPA (IT) elektroninių** SF išrašymo priemonę į RCS iš visuotinės saugyklos. Norėdami gauti daugiau informacijos, žr [...](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider). anksčiau paminėtos "Darbo su elektroninių SF išrašymu" skyriaus "Pradėti naudojant elektroninių SF išrašymą" skyrių Importuokite elektroninių SF išrašymo funkciją.
- Įtraukite saitus iš reikalingų sertifikatų į aptarnavimo aplinką. Reikiami sertifikatai apima skaitmeninio parašo sertifikatą, sertifikatų tarnybos (CA) sertifikatą ir kliento programų sertifikatą. Daugiau informacijos ieškokite straipsnio " [Darbo su elektroninio SF išrašymo](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) paslauga" skaitmeninio sertifikato slapto skyriaus kūrimas.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Šaliai skirta Italijos parametrųturaPA (IT) elektroninių SF išrašymo priemonės konfigūracija

Prieš diegdami programos nustatymą prie prijungtų finansų arba tiekimo grandinės valdymo programos atlikite šias procedūras.

Šiame skyriuje papildoma " [Darbo su elektroninio SF išrašymo](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) " straipsnio konkrečios šalies konfigūravimo programos nustatymo sekcija.

### <a name="create-a-new-feature"></a>Kurti naują funkciją

1. Prisijunkite prie RCS.
2. Elektroninių ataskaitų **darbo** srityje konfigūracijos **teikėjų skyriuje** pažymėkite savo įmonės konfigūracijos teikėją kaip aktyvų.
3. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
4. Elektroninių SF **išrašymo priemonių puslapyje** pasirinkite **Įtraukti** \> **pagal esamą priemonę.**
5. Prie **Microsoft konfigūravimo** teikėjo kaip **pagrindinę priemonę pasirinkite ItalijosturaPA (IT**), įveskite pavadinimą, tada pasirinkite Kurti **funkciją**.

### <a name="set-up-application-specific-parameters"></a>Konkrečios programos parametrų nustatymas

1. Elektroninio **SF išrašymo priemonių** puslapyje pasirinkite norimą redaguoti priemonę.
2. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
3. Skirtuke **Konfigūracijos** pasirinkite konfigūraciją, tada pasirinkite nuo programos **priklausomi parametrai**.
4. Peržvalgos skyriuje **įsitikinkite**, kad pasirinktas **Atšauktų išlaidų subkategorijų** sąrašas.
5. **Skyriuje Sąlygos** pasirinkite **Įtraukti**.
6. Kiekvienai subkategorijai, kuri nustatyta sistemoje, pridėkite tam tikras sąlygas, tada įrašykite pakeitimus.

    > [!NOTE]
    > Stulpelyje **Pavadinimas** galite vietoj konkrečios **\* vertės pasirinkti tuščią\*** arba **\* neužpildyti\*** vietos rezervavimo ženklo vertę.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigūruoti eksportuojamų pardavimo galimybių apdorojimą

1. Elektroninio **SF išrašymo priemonių** puslapyje pasirinkite norimą redaguoti priemonę.
2. Skirtuke **Nustatymai** pasirinkite **Pardavimo SF** ir pasirinkite **Redaguoti**.
3. Pardavimo galimybių **apdorojimo** skyriuje eikite per veiksmus ir nustatykite visus būtinus laukus:

    - Dokumento ženklo **veiksmo** lauke Sertifikato pavadinimas **nurodykite** skaitmeninio parašo sertifikatą.
    - Norėdami pateikti **veiksmą** nustatykite URL adreso **ir** **sertifikatų** laukus. Lauko Sertifikatai vertė **yra** sertifikatų grandinė, iš kurių pirmasis yra šakninis CA sertifikatas (caentrate.cer), o antrasis – kliento sertifikatas.

4. Skyriuje Pritaikymo **taisyklės** eikite per sąlygas ir peržiūrėkite arba nustatykite būtinus laukus:
    - Peržiūrėkite sąlygą **LegalEntityID** ir atnaujinkite savo juridinio subjekto tinkama reikšme.

5. Pasirinkite **Tikrinti,** jei norite užtikrinti, kad visi privalomi laukai yra nustatyti.
6. Įrašykite keitimus ir uždarykite puslapį.
7. Skirtuke **Nustatymai** pasirinkite **Projekto SF**, tada – **Redaguoti**.
8. Pakartokite 3–6 žingsnius projekto SF.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigūruoti importo apdorojimo pardavimo galimybes

1. Elektroninio **SF išrašymo priemonių** puslapyje pasirinkite norimą redaguoti priemonę.
2. Skirtuke **Nustatymai** pasirinkite Importuoti **SF**, tada – **Redaguoti**.
3. **Duomenų kanalo skyriuje**, skirtuke **Parametrai**, duomenų kanalo **lauke**, įveskite eilutės vertę.
4. Skirtuke **Taikymo** taisyklės nustatykite nustatymo laukus. Numatytąją sąlygą **Channel** galite naudoti **perd** kursite ankstesniame veiksme nustatytą lauko Duomenų kanalas vertę į lauką **Vertė**.

    ![Taikomumo taisyklių nustatymą;](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Pasirinkite **Tikrinti,** jei norite užtikrinti, kad visi privalomi laukai yra nustatyti.

### <a name="deploy-the-feature"></a>Diegti funkciją

1. Užbaikite, publikuokite ir įdiekite funkciją tarnybos aplinkoje. Norėdami gauti daugiau informacijos, žr. straipsnio ["Pradėti naudojant elektroninio](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) SF išrašymą" skyriuje Elektroninių SF išrašymo funkcija paslaugų aplinkoje.
2. Įdiekite funkciją į prijungtą programą. Norėdami gauti daugiau informacijos, žr. straipsnio ["Pradėti naudoti elektronines](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) SF išrašymą" skyriuje "Pradėta naudojant elektroninių SF išrašymą" skyrių Elektroninio SF išrašymo funkcija.

### <a name="set-up-finance"></a>Nustatyti finansus

1. Prisiregistruokite prie savo finansų aplinkos.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.
3. Pasirinkite saugyklose **atidarytas** \> **visuotines** \> **saugyklas.**
4. Pasirinkite ir importuokite **kliento SF konteksto modelį** ir **tiekėjo SF importavimo (IT)** konfigūracijas.
5. Eikite į **Organizacijos administravimas** \> **Nustatymas** \> **Elektroninio dokumento parametrai**.
6. Skirtuke **Priemonės** raskite ir pasirinkite Italijos **elektroninės SF** priemonę, tada pažymėkite žymės langelį **Įgalinti**.
7. Skirtuke **Elektroninis** dokumentas įsitikinkite **, kad kliento SF** **·**[žurnalo ir projekto SF laukai nustatyti pagal programos nustatymo konfigūravimo informaciją.](e-invoicing-get-started.md#configure-the-application-setup)

### <a name="set-up-vendor-invoice-import"></a>Nustatyti tiekėjo SF importavimą 

1. Elektroninių ataskaitų darbo srities **finansų** skyriuje **Konfigūracijos teikėjai** pažymėkite savo įmonės konfigūracijos teikėją kaip aktyvų.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Pasirinkite **Kliento SF konteksto** modelį, tada – **Kurti konfigūraciją**.
4. Pasirinkite **Išvesti iš pavadinimo: kliento SF kontekstas, Microsoft, norėdami** sukurti išvestinį konfigūravimą.
5. Juodraščio **versijoje pasirinkite Konstruktorius** **.**
6. Duomenų modelio **medyje** pasirinkite Susieti **modelį su duomenų šaltiniu**.
7. Aprašų **medyje** pasirinkite **DataChannel ir** pasirinkite **Konstruktorius**.
8. Duomenų šaltinių **medyje** išplėskite kontekstinio kanalo **\$ konteinerį\_**.
9. **Vertės lauke** pasirinkite **Redaguoti**. 
10. Įveskite duomenų kanalo pavadinimą. Pavadinime turi būti ne daugiau kaip 10 simbolių. Jis turėtų sutapti su **RCS** elektroninių SF išrašymo funkcijos duomenų kanalo parametro reikšme.
11. Įrašykite keitimus, o tada pereikite į **Ataskaitų konfigūracijos** \> **baigtos konfigūracijos versiją.**
12. Išorinių **kanalų** skirtuko skyriuje Kanalai **pasirinkite** Įtraukti **·**.
13. Lauke Kanalas **įveskite** Konteksto **\$ kanalo** reikšmę.
14. Laukuose Aprašymas ir **Įmonė** **įveskite** vertes.
15. Dokumento konteksto **lauke** pasirinkite naują konfigūraciją, kurią išvedami iš kliento **SF konteksto modelio**. Susiejimo aprašas turi būti **duomenų kanalo kontekstas**.
16. Skirtuke **Importuoti šaltinius** pasirinkite **Įtraukti**, tada nustatykite šias vertes:

    - **Pavadinimas:** OutputFile
    - **Duomenų objekto pavadinimas:** tiekėjo SF antraštė (duomenų **objektas:** VendorInvoiceHeaderEntity)
    - **Modelio susiejimas:** tiekėjo SF importavimas (IT)

> [!NOTE]
> Jei importuojate tiekėjo SF iš skirtingų šaltinių, galite sukurti kelis išorinius kanalus ir keletą išvestinių konfigūracijų, kurios turi skirtingas konteksto **\$ kanalo** vertes. Pavyzdžiui, galite norėti importuoti tiekėjų SF skirtingiems juridiniams subjektams.

## <a name="proxy-server-setup"></a>Tarpinio serverio nustatymas

Šiame skyriuje pateikiama informacija, kuri padės nustatyti ir konfigūruoti tarpinę tarnybą, kad būtų galima naudoti exchange sistemos (SDI) ir elektroninių SF išrašymo tarnybos ryšį.

### <a name="create-an-app-registration"></a>Sukurti programos registraciją

1. Norėdami sukurti pasirašytą sertifikatą paslaugai paslaugai (S2S) autentifikuoti, naudokite toliau nurodytą "Windows PowerShell" scenarijų.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Įrašykite .pfx sertifikato failą į rakto saugyklą, tada panaikinkite vietinę kopiją.
3. Prisiregistruokite prie " [Azure" portalo](https://portal.azure.com) kaip administratorius.
4. Sukurkite SDI tarpinio serverio tarnybos programos registraciją.

    1. Eikite **į programos registracijas**, sukurkite registraciją ir tada nustatykite šias jos vertes:

        - **Pavadinimas:** SDI tarpinis klientas
        - **Palaikomi sąskaitų tipai:** sąskaitos tik šiame organizacijos kataloge (vienas nuomininkas)

    2. Pasirinkite **Registruoti**, tada pasirinkite ką tik sukurtą programos registraciją.
    3. Eikite į **API teises** ir pasirinkite Subsidijos **administratoriaus sutikimas**.
    4. Pereikite prie **sertifikatų > paslapčių**, **pasirinkite** Įkelti sertifikatą ir įkelkite .cer sertifikato failą, kad jį būtų galima naudoti S2S autentifikavimui.
    5. Eikite **į įmonės** programas ir pasirinkite sukurtą programą.
    6. Įrašykite **programos ID** (kliento ID) ir **objekto ID** vertes, skirtas programai.
    7. SF išrašymo paslaugų komanda turi suteikti programai prieigą prie paslaugos. Siųsti šių parametrų vertes į <D365EInvoiceSupport@microsoft.com>:

        - AAD nuomininko ID
        - LCS aplinkos ID
        - Programos ID
        - Objekto ID

5. RCS įtraukite programą į programų sąrašą, skirtą jūsų aptarnavimo aplinkai.

    1. Eikite **į globalizavimo funkcijų** \> **aplinkas** \> **– elektroninių SF** \> **išrašymo tarnybos aplinkas** ir pasirinkite savo aplinką.
    2. **Programų skyriuje**, pridėkite eilutę prie tinklelio ir įveskite programos pavadinimą ir objekto ID.

        ![Programa pridedama prie tarnybos aplinkos.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Pasirinkite **Įrašyti**, tada pasirinkite **Publikuoti**.

### <a name="create-an-azure-virtual-machine"></a>"Azure" virtualiosios mašinos kūrimas

1. ["Azure" portale](https://portal.azure.com) eikite į **virtualias mašinas** ir pasirinkite **Kurti naują**.
2. Skirtuke **Pagrindiniai pasirinkite** abonementą ir išteklių grupę. Vertės turi būti abonementas ir išteklių grupė, kurioje yra jūsų kodo saugyklos ir BLOB saugykla.
3. Pasirinkite regioną. Ši vertė turėtų būti regionas, kuriame įdiegta jūsų finansinė aplinka.
4. Įtraukite administratoriaus vartotojo vardą ir slaptažodį, tada įrašykite juos į rakto saugyklą.
5. Lauke Pasirinkti **gaunamų užklausų prievadus** pasirinkite **HTTPS (443)** ir **RPD (3389)**.

    > [!NOTE]
    > Patariame išjungti **RDP (3389)** prievadą, kai sistema pereina prie gamybos. Jei trikčių šalinimo tikslais turite prisijungti prie virtualiosios mašinos (VM), galite ją vėl įjungti.

    ![Kad būtų sukurta "Azure VM", skirtuko Lape Pagrindiniai parametrai nustatomi laukai.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Skirtuke **Diskai**, išplėstiniam **"** FastTab", pažymėkite žymės langelį **Naudoti valdomus** diskus. Palikite **Epliekijos OS disko** žymės langelį išvalytą.

    ![Norint sukurti "Azure" VM, skirtuke Diskai nustatomi laukai.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Skirtuko Tamsoje **, po viešu** IP **lauku, pasirinkite** Kurti naują **.**

    ![Norint sukurti "Azure" VM, skirtuko "Azure" laukų nustatymas.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Sku laukų **grupės dialogo lange** Kurti viešąjį **IP** adresą pasirinkite standartinę **pasirinktį**. Laukų grupėje **Priskyrimas** pasirinkite pasirinktį **Statinis**.

    ![Viešo IP adreso kūrimas.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Skirtuke Valdymas **panaikinkite** žymės langelio Automatinis **išjungimas žymėjimą**, kad išjungtumėte automatinį išjungimą.
10. Nustatykite svečio **OS atnaujinimų** lauką **kaip Rankinis**, tada nustatykite visas kitas strategijas.
11. Peržiūrėkite ir sukurkite VM.
12. Naujame VM eikite į Priskirtą **tapatybės** \> **sistemą** ir nustatykite būsenos **parinktį** Į.**·**
13. Suteikti VM prieigą prie rakto saugyklos.

    1. Rakto "Vault" eikite į prieigos **valdymo (IAM) vaidmenų** \> **priskyrimus.**
    2. Pasirinkite **Įtraukti vaidmens priskyrimą**, tada nustatykite šiuos laukus:

        1. Lauke Vaidmuo **nurodykite** rakto **Vault Secrets vartotoją**.
        2. Lauke Priskirti **prieigą prie** nurodykite virtualiąją **mašiną**.
        3. Lauke Abonementas **nurodykite** savo abonementą.
        4. **Lauke Pasirinkti** nurodykite savo VM.

    3. Eikite į Prieigos **strategijas**.
    4. Pasirinkite **Įtraukti prieigos strategiją** ir nustatykite šiuos laukus:

        1. Pasirinktame **pasirinktame** lauke pasirinkite savo VM.
        2. Skyriuje Sertifikatas **pasirinkite** Sąrašas **ir** Gauti **teises**.

14. ["Azure" portale](https://portal.azure.com) eikite **į viešus** IP adresus ir pasirinkite VM sukurtą IP adresą.
15. Eikite **į konfigūraciją** ir nustatykite domeno vardų sistemos (DNS) pavadinimą.

### <a name="prepare-the-proxy-service-environment"></a>Paruošti tarpinio serverio tarnybos aplinką

Atlikite šiuos veiksmus kompiuteryje, kuriame yra tarpinis serveris.

1. Prisijunkite prie VM naudodami nuotolinio darbalaukio ryšį.
2. Atidarykite vietinio kompiuterio sertifikato įfiksavimo įrankį. Norėdami gauti daugiau informacijos, žr [. Kaip: peržiūrėti sertifikatus, kai galima prispausti](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) MMC.
3. Importuokite **caentrate.cer gamybos** sertifikatą **ir CAEntratetest.cer**[, kad jį būtų galima patikrinti patikimos šakninio sertifikavimo institucijos parduotuvėje](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** yra šakninis CA sertifikatas, kurį pateikė institucija.)
4. Valdymo skyde atidarykite **Įjungti arba išjungti "Windows** **·** \> **·**" funkcijas arba pereikite į serverio operacinės sistemos (OS) serverio tvarkytuvo įtraukti vaidmenis ir funkcijas ir įjunkite informacinių interneto paslaugų (IIS) funkcijas:

    - Tinklo valdymo įrankiai
        - IIS valdymo suliejus
    - Interneto tinklo tarnybos
        - Programos programavimo priemonės
            - .NET Extensibility 4.7 (arba 4.8)
            - Asp
            - ASP.NET 4.7 (arba 4.8)
            - Cgi
            - ISAPI plėtiniai
            - ISAPI filtrai
        - Bendrosios HTTP funkcijos
            - Numatytasis dokumentas
            - Katalogo naršymas
            - HTTP klaidos
            - Statinis turinys
        - Sveikatos ir diagnozė
            - HTTP registravimas
            - Sekimas
        - Našumo funkcijos
            - Statinio turinio glaudinimas
        - Sauga
            - Užklausų filtravimas

    ![IIS funkcijų įjungimas.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>SDI tarpinio serverio tarnybos konfigūravimas IIS

1. Ciklo Microsoft Dynamics tarnybose (LCS) eikite į bendrai naudojamų turtų biblioteką ir pasirinkite **duomenų paketą** kaip turto tipą.
2. Suraskite **elektroninių SF išrašymo tarnybos Sdi** tarpinį serverį ir atsisiųskite jį į VM.
3. Sukonfigūruokite tarnybą.

    1. Išskraskite elektroninį **SF išrašymo tarnybos Sdi tarpinio serverio** archyvo aplanką, kurį jūs atsisiuntėte.
    2. **Aplanke src\\ JartureService** atidarykite **appsettings.json** failą ir nustatykite šiuos parametrus:

        - **KeyVaultUri** – nurodyti rakto saugyklos, kurioje saugomas SF išrašymo paslaugos kliento sertifikatas, adresą.
        - **TenantId** – nurodykite kliento nuomininko visuotinį unikalų identifikatorių (GUID).
        - **EnvironmentId** – nurodykite LCS aplinkos ID.
        - **Kliento ID** – nurodykite tarpinių paslaugų programos registracijos kliento nuomininke programos ID.
        - **ClientCertificateName** – nurodykite S2S sertifikato pavadinimą "key vault".
        - **SecurityServiceClientOptions.Endpoint** – nurodykite saugos tarnybos URL.
        - **SecurityServiceClientOptions.Resource** – nurodykite aprėptį, kurios atpažinimo ženklą norite gauti.
        - **SFingServiceClientOptions.Endpoint** – nurodyti SF išrašymo paslaugos galinį punktą. Ši vertė turi būti tas pats galinis punktas, kuris naudojamas RCS ir finansuose.
        - **SFingServiceClientOptions.ServiceEnvironmentId** – nurodykite aptarnavimo aplinkos pavadinimą. Ši vertė turi būti jūsų finansų aplinkos pavadinimas.
        - **NotificationsFolder** – nurodyti aplanką, kuriame bus įrašomi gaunami pranešimų failai.

    3. **Faile web.config suraskite** šią eilutę ir pridėkite tarpinio serverio sertifikato nykščio atspaudą.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Sistemai perėjus į gamybą, galite pakeisti rinkmenos web.config vertes, kad būtų sumažintas surinktos žurnalo informacijos kiekis ir diske būtų vietos diske. Mazge **\<system.diagnostics\>\<source\>** pakeiskite switchValue vertę į **Kritinė** **, Klaida**. Daugiau informacijos rasite MS [Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Atidarykite IIS tvarkytuvą. Kairėje medžio pusėje, liko šakniniame mazge. Dešinėje pasirinkite Serverio **sertifikatai**.

    ![Tarnybos sertifikatų pasirinkimas IIS tvarkytuve.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Atidarykite meniu ir pasirinkite **Importuoti**.
6. Dialogo lango **Importuoti sertifikatą** lauke **Sertifikato failas (.pfx)** nurodykite tarpinio serverio sertifikato .pfx failo maršrutą.

    ![Nurodomas tarpinio serverio tarnybos sertifikato failas.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) **"Sites**", tada pasirinkite **Įtraukti svetainę**.
8. **Dialogo lango Įtraukti** svetainę lauke **Svetainės pavadinimas** įveskite svetainės pavadinimą.
9. Lauke Fizinis **maršrutas** nurodo **src Turinotarninės\\ tarnybos** aplanką.
10. Lauke Susiejimo **tipas** pasirinkite **https**.
11. Lauke Pagrindinio **kompiuterio vardas** nurodykite pagrindinio kompiuterio pavadinimą.
12. Palikti nustatytus **IP adreso** ir **prievado** laukų numatytąsias vertes.
13. Įsitikinkite, kad **žymės langelis Reikalauti** serverio pavadinimo nurodymo yra išvalytas, nes SDI nepalaiko šios technologijos.
14. SSL sertifikato **lauke** pasirinkite importuotą tarpinio serverio sertifikatą.
15. Programų telkinio **lauke** nurodykite svetainės telkinį ir pasižymkite jos pavadinimą (pvz., **SdiAppPool**).

    ![Žiniatinklio svetainės įtraukimas.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Baigę kurti svetainę, atidarykite SSL parametrų **meniu**.

    ![Atidaromas SSL parametrų meniu.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Pažymėkite žymės **langelį Reikalauti SSL**, tada laukų grupėje **Kliento** sertifikatai pažymėkite parinktį **Reikalauti**.

    ![Ssl parametrų konfigūravimas.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Atidarykite **katalogo naršymą** ir pasirinkite **Įgalinti**.
19. Bet kurioje interneto naršyklėje eikite į **serverDNS/TrasmissioneFatture.svc**. Turi pasirodyti standartinis aptarnavimo puslapis.

    ![Tikrinama paslauga naršyklėje.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Norėdami saugoti žurnalus ir failus, kurkite šiuos aplankus:

    - **C:\\ Žurnalai\\** – parduotuvės žurnalo failai čia. Šiuos failus galite peržiūrėti MS [service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\ Files\\** – čia saugoti visus atsakymo failus.

21. Failų naršyklėje suteikite TINKLO TARNYBAI **ir** IIS AppPool **SdiAppPool (\\ arba IIS AppPool** DefaultAppPool **\\,** jei naudojate numatytąjį telkinį) **·** **prie žurnalų ir failų** aplankų.

    1. Pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) vieną iš aplankų, tada pasirinkite **Ypatybės**.
    2. **Skirtuko Sauga** dialogo lange Ypatybės **pasirinkite** **Redaguoti**.
    3. Pridėkite vartotojus, jei jų nėra sąraše.
    4. Kito aplanko atvejais pakartokite 1–3 veiksmus.

    ![Teisių įtraukimas į aptarnavimo vartotoją.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Privatumo pranešimas 

Įgalinus **Italijos elektroninės SF** priemonę, gali reikėti siųsti ribotą duomenų apdorojimą. Šie duomenys apima organizacijos mokesčių registracijos ID. Administratorius gali įjungti ir išjungti Italijos elektroninės SF funkciją. Norėdami išjungti funkciją, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Nustatymas** \> **Elektroninio dokumento parametrai**.
2. Skirtuke **Priemonės** pasirinkite eilutes, kuriose yra Italijos elektroninės **SF priemonė**, ir pasirinkite Išjungti **dabar**.

Iš šių išorinių sistemų importuojami duomenys į šią "Dynamics 365" interneto paslaugą priklauso nuo mūsų privatumo [patvirtinimo](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite šaliai/regionui brangesnių priemonių dokumentuose skyriuje "Privatumo pranešimas".

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
