---
title: Norvegijos grynųjų pinigų registrų diegimo gairės (iš senesni)
description: Ši tema yra diegimo vadovas, kuris parodo, kaip Microsoft Dynamics 365 Commerce įgalinti Norvegijos lokalizavimą.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 019bac01abdc0b2e16718c08953b44fbccef83a3
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944793"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Norvegijos grynųjų pinigų registrų diegimo gairės (iš senesni)

[!include [banner](../includes/banner.md)]

Ši tema yra diegimo vadovas, kuris parodo, kaip Microsoft Dynamics 365 Commerce įgalinti Norvegijos lokalizavimą. Lokalizavimą sudaro keletas "Commerce" komponentų plėtinių. Pvz., plėtiniai leidžia kvituose spausdinti pasirinktinius laukus, registruoti papildomus audito įvykius, pardavimo operacijas ir mokėjimo operacijas elektroniniame kasos aparate (EKA), skaitmeniniu būdu pasirašyti pardavimo operacijas ir spausdinti X ir Z ataskaitas vietiniu formatu. Daugiau informacijos apie Norvegijos lokalizavimą ieškokite Norvegijos [grynųjų pinigų registro funkcija](./emea-nor-cash-registers.md).

Šis pavyzdys yra "Retail" programinės įrangos kūrimo rinkinio (SDK) dalis. Informacijos apie SDK žr.["Retail" programinės įrangos kūrimo rinkinio (SDK) architektūrą](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Šį pavyzdį sudaro "Commerce runtime (CRT), "Retail Server" ir EKA plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti CRT "Retail Server" ir EKA projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz., "Microsoft" Visual Studio Online (VSO), kurioje dar nėra pakeistų failų.

> [!NOTE]
> Naudojant "Commerce 10.0.8" ir daugiau, "Retail Server" vadinamas "Commerce Scale Unit". Kadangi ši tema taikoma su keliomis ankstesnėmis programos versijomis, *"Retail* Server" naudojama šioje temoje.
>
> Kai kurie šios temos procedūrų veiksmai skiriasi, atsižvelgiant į jūsų naudojama komercijos versiją. Daugiau informacijos rasite Kas [naujo arba Dynamics 365 Retail](../get-started/whats-new.md) pakeista.

### <a name="using-certificate-profiles-in-commerce-channels"></a>Sertifikatų profilių naudojimas "Commerce" kanaluose

"Commerce" 10.0.15 ir vėlesnėse versijose galite naudoti vartotojo nustatytus sertifikatų šablonus mažmeninės prekybos parduotuvėms funkcijai, kuri palaiko atjungties režimą, kai rakto Vault arba [Commerce](./certificate-profiles-for-retail-stores.md) Headquarters naudoti negalima. Ši funkcija išplečia mažmeninės [prekybos kanalų funkcijos paslapčių](../dev-itpro/manage-secrets.md) valdymas.

Norėdami taikyti šią funkciją CRT plėtinyje, atlikite šiuos veiksmus.

1. Sukurkite naują CRT išplėtimo projektą (C# klasės bibliotekos projekto tipas). Naudokite pavyzdžių šablonus iš "Retail" programinės įrangos kūrimo rinkinio (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).

2. Įtraukite pasirinktinę CertificateSikettureServiceRequest apdorojimo programą į projektą SequentialSibentureRegister.

3. Norėdami perskaityti slaptą skambutį, `GetUserDefinedSecretCertificateServiceRequest` konstruktorių naudodami šablono ID parametrą. Tai pradės funkcijas, kurios veikia su sertifikato profilių nustatymais. Pagal parametrus sertifikatas bus nuskaitomas arba iš "Azure Key Vault", arba iš vietinės mašinos saugyklos.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Nuskaitę sertifikatą, tęskite duomenų pasirašymą.

5. Kurti CRT išplėtimo projektą.

6. Kopijuoti išvesties klasės biblioteką ir įklijuoti ją į ...\RetailServer\webroot\bin\Ext, kad būtų galima tikrinti rankiniu būdu.

7. Faile CommerceRuntime.Ext.config atnaujinkite plėtinio sudėtį, naudodami pasirinktinės bibliotekos informaciją.

## <a name="development-environment"></a>Talpinimo aplinka

Atlikite šias procedūras, norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį.

### <a name="the-crt-extension-components"></a>Plėtinio CRT komponentai

Plėtinio CRT komponentai įtraukiami į CRT pavyzdžius. Norėdami atlikti šias procedūras, atidarykite CRT sprendimą, **CommerceRuntimeSamples.sln, dalyje** **RetailSdk \\ SampleExtensions \\ CommerceRuntime.**

#### <a name="receiptsnorway-component"></a>ReceiptsNorway komponentas

1. Raskite **Runtime.Extensions.ReceiptsNorway** projektą ir sukurkite jį.
2. Aplanke **Extensions.ReceiptsNorway bin Debug raskite \\\\** failą **Contoso.Commerce.Runtime.ReceiptsNorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris: kopijuokite surinkimą į talpyklos išorės aplanką, esantį "Microsoft" informacinių interneto paslaugų** **\\\\** (IIS) mažmeninės prekybos serverio svetainėje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt komponentas

1. Raskite **Runtime.Extensions.SalesPaymentTransExt** projektą ir sukurkite jį.
2. Aplanke **Extensions.SalesPaymentTransExt talpyklos derinimo raskite \\\\ failą** **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway komponentas

1. Suraskite **Runtime.Extensions.XZReportsNorway** projektą ir sukurkite jį.
2. Aplanke **Extensions.XZReportsNorway \\ bin \\ Debug** raskite failą **Contoso.Commerce.Runtime.XZReportsNorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

# <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent pavyzdžio komponentas

1. Raskite **Runtime.Extensions.RegisterAuditEventSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.RegisterAuditEventSample bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSitraukimo pavyzdžio komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSiprojektsample** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SalesTransactionSi visų prekių \\ pripildės \\ debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SalesTransactionSi contosotureSample.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SalesTransactionSi pstple.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

# <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent pavyzdžio komponentas

1. Raskite **Runtime.Extensions.RegisterAuditEventSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.RegisterAuditEventSample bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSitraukimo pavyzdžio komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSiprojektsample** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SalesTransactionSi visų prekių \\ pripildės \\ debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SalesTransactionSi contosotureSample.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SalesTransactionSi pstple.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSiverstureSample.Messages komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSiprojektSample.Messages** projektą.
2. Aplanke **Extensions.SalesTransactionSi contosotureSample.Messages talpyklos derinimo raskite \\\\ failą** **Contoso.Commerce.Runtime.SalesTransactionSidulple.Messages.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

# <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent pavyzdžio komponentas

1. Raskite **Runtime.Extensions.RegisterAuditEventSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.RegisterAuditEventSample bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSitraukimo pavyzdžio komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSiprojektsample** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SalesTransactionSi visų prekių \\ pripildės \\ debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SalesTransactionSi contosotureSample.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SalesTransactionSi pstple.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSi sutureRegister.Contracts komponentas

1. Suraskite **Runtime.Extensions.SequentialSi turi turimosRegister.Contracts** projektą.
2. Aplanke **Extensions.SequentialSi contosotureRegister.Contracts \\ talpyklos \\ derinimo** raskite failą **Contoso.Commerce.Runtime.SequentialSi sutar.Register.Contracts.dll** rinkinys.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent pavyzdžio komponentas

1. Raskite **Runtime.Extensions.RegisterAuditEventSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.RegisterAuditEventSample bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregister-component"></a>SequentialSitureRegister komponentas

1. Rasti **Runtime.Extensions.SequentialSi turinasRegister** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SequentialSi eilėsregister \\ bin \\ Debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSinorway komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSinorway** projektą.
2. Aplanke **Extensions.SalesTransactionSi contosotureNorway bin Debug raskite \\\\ failą** **Contoso.Commerce.Runtime.SalesTransactionSinorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSi sutureRegister.Contracts komponentas

1. Suraskite **Runtime.Extensions.SequentialSi turi turimosRegister.Contracts** projektą.
2. Aplanke **Extensions.SequentialSi contosotureRegister.Contracts \\ talpyklos \\ derinimo** raskite failą **Contoso.Commerce.Runtime.SequentialSi sutar.Register.Contracts.dll** rinkinys.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponentas

1. Raskite **Runtime.Extensions.SalesPaymentTransExtNorway** projektą ir sukurkite jį.
2. Aplanke **Extensions.SalesPaymentTransExtNorway bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponentas

1. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

2. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregister-component"></a>SequentialSitureRegister komponentas

1. Rasti **Runtime.Extensions.SequentialSi turinasRegister** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SequentialSi eilėsregister \\ bin \\ Debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSinorway komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSinorway** projektą.
2. Aplanke **Extensions.SalesTransactionSi contosotureNorway bin Debug raskite \\\\ failą** **Contoso.Commerce.Runtime.SalesTransactionSinorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSi sutureRegister.Contracts komponentas

1. Suraskite **Runtime.Extensions.SequentialSi turi turimosRegister.Contracts** projektą.
2. Aplanke **Extensions.SequentialSi contosotureRegister.Contracts \\ talpyklos \\ derinimo** raskite failą **Contoso.Commerce.Runtime.SequentialSi sutar.Register.Contracts.dll** rinkinys.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponentas

1. Raskite **Runtime.Extensions.SalesPaymentTransExtNorway** projektą ir sukurkite jį.
2. Aplanke **Extensions.SalesPaymentTransExtNorway bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway komponentas

1. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

2. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregister-component"></a>SequentialSitureRegister komponentas

1. Rasti **Runtime.Extensions.SequentialSi turinasRegister** projektą.
2. Modifikuokite failą App.config nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo **operacijoms** pasirašyti, pavadinimą.
3. Kurti projektą.
4. Aplanke **Extensions.SequentialSi eilėsregister \\ bin \\ Debug** raskite šiuos failus:

    - Rinkinio **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll**
    - Konfigūracijos **failas Contoso.Commerce.Runtime.SequentialSi contosotureRegister.dll.config**

5. Nukopijuokite failus į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

6. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

7. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSinorway komponentas

1. Raskite **Runtime.Extensions.SalesTransactionSinorway** projektą.
2. Aplanke **Extensions.SalesTransactionSi contosotureNorway bin Debug raskite \\\\ failą** **Contoso.Commerce.Runtime.SalesTransactionSinorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSi sutureRegister.Contracts komponentas

1. Suraskite **Runtime.Extensions.SequentialSi turi turimosRegister.Contracts** projektą.
2. Aplanke **Extensions.SequentialSi contosotureRegister.Contracts \\ talpyklos \\ derinimo** raskite failą **Contoso.Commerce.Runtime.SequentialSi sutar.Register.Contracts.dll** rinkinys.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway komponentas

1. Raskite **Runtime.Extensions.SalesPaymentTransExtNorway** projektą ir sukurkite jį.
2. Aplanke **Extensions.SalesPaymentTransExtNorway bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **Parduotuvės serveris:** kopijuokite surinkimą į **\\\\ talpyklos** išorės aplanką, esantį IIS "Retail Server" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite surinkimą **\\ į iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **Parduotuvės serveris: failo vardas yra** **commerceruntime.ext.config, jis yra talpyklos išoriniame aplanke, kuris yra** **\\** IIS "Retail Server" svetainėje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Ne **redaguoti** failų commerceruntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

---

### <a name="the-retail-server-extension-components"></a>"Retail Server" plėtinio komponentai

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSi egzemplioriaus "Retail Server" pavyzdžio komponentas

1. Aplanke **RetailSDK \\ SampleExtensions \\\\ RetailServer RetailServer.Extensions.SalesTransactionSitraukimoSample** raskite **RetailServer.Extensions.SalesTransactionSitureSample** projektą ir sukurkite jį.
2. Aplanke **RetailServer \\ plėtiniai.SalesTransactionSibugtureSample \\ bin \\ Debug** raskite failą **Contoso.RetailServer.SalesTransactionSi pstple.dll.**
3. Nukopijuokite surinkimo failą į "Retail Server" plėtinių aplanką.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    Aplankas yra talpyklos **\\** aplankas, siųstas IIS mažmeninės prekybos serverio svetainėje.

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    Aplankas yra talpyklos **\\** aplankas, siųstas IIS mažmeninės prekybos serverio svetainėje.

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    Aplankas yra talpyklos **\\\\ išorinis** aplankas, įsikūręs IIS mažmeninės prekybos serverio svetainėje.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    Aplankas yra talpyklos **\\\\ išorinis** aplankas, įsikūręs IIS mažmeninės prekybos serverio svetainėje.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    Aplankas yra talpyklos **\\\\ išorinis** aplankas, įsikūręs IIS mažmeninės prekybos serverio svetainėje.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    Aplankas yra talpyklos **\\\\ išorinis** aplankas, įsikūręs IIS mažmeninės prekybos serverio svetainėje.

    ---

4. Raskite "Retail Server" konfigūracijos failą. Failas pavadintas web.config ir jis yra IIS "Retail Server" svetainės vietoje **šakniniame** aplanke.
5. Užregistruokite "Retail Server" **plėtinius konfigūracijos failo skyriuje extensionComposition.**

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Užregistruokite "Retail Server" plėtinių priklausomybes.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4/)

    1. Aplanke **CommerceRuntime \\ Extensions.SalesTransactionSiruntureSample talpyklos derinimo \\\\** raskite šiuos failus:

        - Rinkinio **failas Contoso.Commerce.Runtime.SalesTransactionSi contosotureSample.dll**
        - Konfigūracijos **failas Contoso.Commerce.Runtime.SalesTransactionSi pstple.dll.config**

    2. Nukopijuokite failus į **\\ talpyklos** aplanką, esantį IIS mažmeninės prekybos serverio svetainėje.
    3. CRT Užregistruokite pakeitimą plėtinio konfigūracijos CRT faile. Šio failo vardas **yra commerceruntime.ext.config. Jis yra IIS mažmeninės prekybos serverio** svetainės **vietoje**, talpyklos aplanke.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later/)

    1. Aplanke **CommerceRuntime \\ Extensions.SalesTransactionSi parametrų Sample.Pranešimų talpyklos derinimo aplankas \\\\** raskite **Contoso.Commerce.Runtime.SalesTransactionSi parametrų Sample.Messages.dll** surinkimo failą.
    2. Nukopijuokite failą į **\\ talpyklos** aplanką, esantį IIS mažmeninės prekybos serverio svetainėje.
    3. CRT Užregistruokite pakeitimą plėtinio konfigūracijos CRT faile. Šio failo vardas **yra commerceruntime.ext.config. Jis yra IIS mažmeninės prekybos serverio** svetainės **vietoje**, talpyklos aplanke.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Nereikia jokių veiksmų.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    > [!NOTE]
    > Nereikia jokių veiksmų.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    > [!NOTE]
    > Nereikia jokių veiksmų.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    > [!NOTE]
    > Nereikia jokių veiksmų.

    ---

### <a name="the-modern-pos-extension-components"></a>Modernaus EKA plėtinio komponentai

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Įdiegti autonominio režimo tarpinio serverio kodą

Ši dalis lygi "Retail Server" valdikliui, bet išplečia vietinį, kuris CRT naudojamas, kai kliento programa neprijungta.

1. Faile **customization.settings pakeiskite skyrių** **@(RetailServerLibraryPathForProxyGeneration) taip, kad tarpinio serverio generavimui naudojamas naujas** "Retail Server" surinkimas.
2. Klasėje **StoreOperationsManager įdiegti šiuos sąsajos** metodus. Norėdami naudoti pirmą pašalinį, pridėkite šį kodą:

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    ---

3. Norėdami iš naujo generuoti tarpinio serverio kodą, iš komandų eilutės sukurkite tarpinių serverių aplanką naudodami **komandą** **msbuild /t:Rebuild.**
4. **Išspręskite Proxies.RetailProxy** projekto priklausomybes:

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    Atidarykite **RetailSDK \\\\ Proxies RetailProxy \\ Proxies.RetailProxy.csproj, įtraukite** **RetailSDK \\ SampleExtensions \\ CommerceRuntime \\ extensions.SalesTransactionSimediaSample \\ CommerceRuntime.Extensions.SalesTransactionSitraukimoSample projektą ir įtraukite projekto nuorodą į RetailProxy projektą, kad nuoroda** **·** **SalesTransactionSi readtureSample** būtų nuoroda.

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    Atidarykite **RetailSDK \\\\ Proxies RetailProxy \\ Proxies.RetailProxy.csproj, įtraukite** **RetailSDK \\ SampleExtensions \\ CommerceRuntime \\ extensions.SalesTransactionSimediaSample.Messages \\ CommerceRuntime.Extensions.SalesTransactionSictionSample.Messages projekto nuorodą į RetailProxy projektą įtraukite į nuorodą į** **·** **SalesTransactionSi latepleSample.Messages.**

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    ---

5. Koreguokite sąsajos metodus **storeOperationsManager** klasėje:

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    > [!NOTE]
    > Šis veiksmas netaikomas šiai versijai.

    ---

6. Atnaujinkite **failą dllhost.exe.config,** kad kliento brokeris įkelia naują RetailProxy surinkimą.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>"Retail" tarpinio serverio plėtinio komponentas ("Retail 7.3.1" ir naujesnė versija)

Šią procedūrą atlikite tik tada, jei naudojate "Retail 7.3.1" ir vėliau.

1. Aplanke **RetailSDK \\ SampleExtensions \\\\ RetailProxy.Extensions.SalesTransactionSitraukimoSample** raskite **RetailServer.Extensions.SalesTransactionSitureSample** projektą ir sukurkite jį.
2. Aplanke **RetailProxy \\ RetailProxy.Extensions.SalesTransactionSitraukimoSample bin Debug raskite \\ rinkinio failą \\** **Contoso.Commerce.RetailProxy.SalesTransactionSitraukimoSample.**
3. Nukopijuokite surinkimo failus į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.
4. Užregistruokite "Retail" tarpinio serverio keitimą plėtinio konfigūracijos faile. Failas pavadintas **RetailProxy.MPOSOffline.ext.config,** jis yra vietinio kliento CRT brokerio vietoje.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modernūs EKA plėtinio komponentai

1. Atidarykite sprendimą **RetailSdk POS ModernPOS.sln ir įsitikinkite, kad jį galima \\\\** sukompiliuoti be klaidų. Be to, įsitikinkite, kad naudodami komandą Vykdyti galėsite paleisti "Modern Visual Studio POS" **iš** "Microsoft".

    > [!NOTE]
    > "Modern POS" negalima pritaikyti. Turite įgalinti vartotojo abonemento valdymo programą (UAC) ir, jei reikia, pašalinti anksčiau įdiegtus "Modern POS" egzempliorius.

2. Įtraukite šiuos esamus šaltinio kodų aplankus į **EKA plėtinių** projektą.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    ---

3. Įjunkite plėtinius, kad jie būtų sukompiliuoti **tsconfig.json, pašalindami** šiuos aplankus iš neįtrauktinųjų sąrašo.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    ---

4. Įjunkite plėtinius, kad juos būtų **galima įkelti į plėtinius.json,** į atitinkamą vietą įtraukdami šias eilutes.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. instrukcijas eka readme.md failo **plėtinių** projekte.

5. Perkurti sprendimą.
6. Paleiskite modernų EKA derintuve ir patikrinkite funkcijas.

### <a name="cloud-pos-extension-components"></a>"Cloud POS" plėtinio komponentai

1. Atidarykite sprendimą **RetailSdk POS CloudPOS.sln ir įsitikinkite, kad jį galima \\\\** sukompiliuoti be klaidų.
2. Įtraukite šiuos esamus šaltinio kodų aplankus į **EKA plėtinių** projektą.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    ---

3. Įjunkite plėtinius, kad jie būtų sukompiliuoti **tsconfig.json,** pašalindami šiuos aplankus iš neįtrauktinųjų sąrašo.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    - SalesTransactionSiverstureSample
    - SalesTransactionSitoritureNorway
    - SequentialSiture

    ---

4. Įjunkite plėtinius, kad juos būtų **galima įkelti į plėtinius.json,** į atitinkamą vietą įtraukdami šias eilutes.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. instrukcijas eka readme.md failo **plėtinių** projekte.

5. Perkurti sprendimą.
6. Paleiskite sprendimą naudodami komandą **Vykdyti** ir vykdykite "Retail SDK" vadove nurodytus veiksmus.
7. Patikrinti funkciją.

### <a name="set-up-required-parameters-in-headquarters"></a>Reikalingų parametrų nustatymas "Headquarters"

Daugiau informacijos ieškokite Norvegijos [grynųjų pinigų registro](./emea-nor-cash-registers.md) funkcijos.

## <a name="production-environment"></a>Gamybos aplinka

Atlikite šiuos veiksmus, jei norite kurti diegiamus paketus, kuriuose yra "Commerce" komponentai, ir taikyti šiuos paketus gamybos aplinkoje.

1. Atlikite veiksmus skyriuje ["Cloud POS" plėtinio komponentai arba](#cloud-pos-extension-components)["Modern POS"](#modern-pos-extension-components) plėtinio komponentai, kuriuos reikia atlikti anksčiau šioje temoje.
2. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk \\** Assets":

    1. Konfigūracijos **failuose commerceruntime.ext.config ir** **CommerceRuntime.MPOSOffline.Ext.config į sudėties skyrių įtraukite** **šias** eilutes:

        # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Įgalinti "Commerce" tarpinio serverio tinkinimą:

        # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

        Konfigūracijos faile dllhost.exe.config įtraukite šias eilutes į konfigūracijos **skyriaus** **appSettings** **poskyrį**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

        Konfigūracijos faile dllhost.exe.config įtraukite šias eilutes į konfigūracijos **skyriaus** **appSettings** **poskyrį**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

        Konfigūracijos faile **RetailProxy.MPOSOffline.ext.config įtraukite** šias eilutes į **skyriaus** sudėtį:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

        Konfigūracijos faile **RetailProxy.MPOSOffline.ext.config įtraukite** šias eilutes į **skyriaus** sudėtį:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

        Konfigūracijos faile **RetailProxy.MPOSOffline.ext.config įtraukite** šias eilutes į **skyriaus** sudėtį:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

        Konfigūracijos faile **RetailProxy.MPOSOffline.ext.config įtraukite** šias eilutes į **skyriaus** sudėtį:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Atlikite šiuos pakeitimus **customization.settings paketo** tinkinimo konfigūracijos faile:

    1. Įgalinkite "Retail" tarpinio serverio tinkinimą.

        # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

        ItemGroup **&lt; condition="@(RetailServerLibraryPathForProxyGeneration)' == "", įtraukite šias &gt;** eilutes.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

        ItemGroup **&lt; condition="@(RetailServerLibraryPathForProxyGeneration)' == "", įtraukite šias &gt;** eilutes.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

        Įtraukite šias eilutes į skyrių **ItemGroup**, kad mažmeninės prekybos tarpinio serverio plėtinys būtų įtraukti į diegiamus paketus:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

        Įtraukite šias eilutes į skyrių **ItemGroup**, kad mažmeninės prekybos tarpinio serverio plėtinys būtų įtraukti į diegiamus paketus:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

        Įtraukite šias eilutes į skyrių **ItemGroup**, kad mažmeninės prekybos tarpinio serverio plėtinys būtų įtraukti į diegiamus paketus:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

        Įtraukite šias eilutes į skyrių **ItemGroup**, kad mažmeninės prekybos tarpinio serverio plėtinys būtų įtraukti į diegiamus paketus:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Įtraukite šias eilutes į **skyrių** ItemGroup, kad įtraukumėte CRT plėtinius į diegiamus paketus:

        # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Įtraukite šias eilutes į **skyrių** ItemGroup, kad į diegtimus paketus įtraukumėte "Retail Server" plėtinį:

        # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Modifikuokite šiuos failus norėdami įtraukti išteklių failus Norvegijai į diegiamus paketus:
    - Pakuotės \_ SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Paketai \RetailServer\Sdk.RetailServerSetup.proj
  
  - Failui **Sdk.ModernPos.Shared.csproj** 
    - Įtraukti eilutę į **ItemGroup** skyrių
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Užuot <File_name> nustatyti išteklių failo pavadinimą. Tas pats taikoma ir kitiems toliau pateiktiems pavyzdžiui.
 
    - Įtraukite eilutę į **skyriaus Target Name = "CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - **Sdk.RetailServerSetup.proj** failui 
    - Įtraukti eilutę į **ItemGroup** skyrių
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Įtraukite eilutę į **skyriaus Target Name = "CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Modifikuokite sertifikato konfigūracijos failą nurodydami nykščio atspaudą, parduotuvės vietą ir sertifikato, kuris turi būti naudojamas pardavimo operacijoms pasirašyti, pavadinimą. Tada nukopijuokite konfigūracijos failą į **nuorodų** aplanką.

    # <a name="application-update-4"></a>[„Application update 4“](#tab/app-update-4)

    Failas pavadintas **Contoso.Commerce.Runtime.SalesTransactionSitraukimoSample.dll.config ir jis nurodytas dalyje** **CommerceRuntime \\ Extensions.SalesTransactionSirunple \\ bin \\ Debug**.

    # <a name="application-update-5-and-later"></a>[5 ir naujesnės programos naujinimas](#tab/app-update-5-and-later)

    Failas pavadintas **Contoso.Commerce.Runtime.SalesTransactionSitraukimoSample.dll.config ir jis nurodytas dalyje** **CommerceRuntime \\ Extensions.SalesTransactionSirunple \\ bin \\ Debug**.

    # <a name="retail-731"></a>[Mažmeninės 7.3.1](#tab/retail-7-3-1)

    Failas pavadintas **Contoso.Commerce.Runtime.SalesTransactionSitraukimoSample.dll.config ir jis nurodytas dalyje** **CommerceRuntime \\ Extensions.SalesTransactionSirunple \\ bin \\ Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ir vėlesnės versijos](#tab/retail-7-3-2)

    Failo vardas yra **Contoso.Commerce.Runtime.SequentialSiintuvtureRegister.dll.config, jis nurodytas** plėtiniai.SequentialSi **procesoregister \\ talpyklos \\** debug.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ir vėlesnės versijos](#tab/retail-7-3-5)

    Failo vardas yra **Contoso.Commerce.Runtime.SequentialSiintuvtureRegister.dll.config, jis nurodytas** plėtiniai.SequentialSi **procesoregister \\ talpyklos \\** debug.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ir vėlesnės versijos](#tab/retail-8-1-1)

    Failo vardas yra **Contoso.Commerce.Runtime.SequentialSiintuvtureRegister.dll.config, jis nurodytas** plėtiniai.SequentialSi **procesoregister \\ talpyklos \\** debug.

    ---

6. Atnaujinkite "Retail Server" konfigūracijos failą. Faile **RetailSDK \\ packages RetailServer Code web.config įtraukite šias eilutes \\ į skyrių \\\\** **extensionComposition.**

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Paleiskite **"Retail SDK" "msbuild",** kad sukurtumėte diegiamus paketus.
8. Pritaikykite paketus Microsoft Dynamics per ciklo tarnybas (LCS) arba rankiniu būdu. Daugiau informacijos ieškokite [Create deployable](../dev-itpro/retail-sdk/retail-sdk-packaging.md) packages.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>"Modern POS" skaitmeninio parašo įgalinimas neprisijungus

Norėdami įjungti skaitmeninį parašą "Modern POS" neprisijungus, turite atlikti šiuos veiksmus, kai naujame įrenginyje suaktyvinsite "Modern POS".

1. Prisijunkite prie POS.
2. Duomenų bazės **ryšio būsenos** puslapyje įsitikinkite, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių **atsisiuntimų lauko vertė** yra **0** (nulis), duomenų bazė yra visiškai sinchronizuojama.
3. Atsijungti nuo EKA.
4. Palaukite, kol autonominė duomenų bazė bus visiškai sinchronizuojama.
5. Prisijunkite prie POS.
6. Duomenų bazės **ryšio būsenos** puslapyje įsitikinkite, kad autonominė duomenų bazė yra visiškai sinchronizuota. Kai laukiančių operacijų **vertė autonominės duomenų bazės lauke** yra **0** (nulis), duomenų bazė visiškai sinchronizuojama.
7. Iš naujo paleiskite modernų EKA.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
