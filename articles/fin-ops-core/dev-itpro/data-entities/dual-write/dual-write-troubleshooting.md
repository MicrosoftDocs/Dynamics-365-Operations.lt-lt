---
title: Bendroji trikčių šalinimo informacija
description: Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų bendroji trikčių šalinimo informacija.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d5d9dbce0c74d32107db6bbae033b921e4201693
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275655"
---
# <a name="general-troubleshooting"></a>Bendroji trikčių šalinimo informacija

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų bendroji trikčių šalinimo informacija.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Kai bandote įdiegti dvigubo rašymo paketą naudodami įrankį „Package Deployer“, nerodoma pasiekiamų sprendimų

Kai kurios įrankio „Package Deployer“ versijos yra nesuderinamos su dvigubo rašymo sprendimo paketu. Norėdami sėkmingai įdiegti paketą, įsitikinkite, kad naudojate įrankio „Package Deployer“ [9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) arba naujesnę versiją.

Įdiegę įrankį „Package Deployer“, įdiekite sprendimo paketą atlikdami šiuos veiksmus.

1. Atsisiųskite naujausią sprendimo paketo failą iš Yammer.com. Atsisiuntus paketo ZIP failą, spustelėkite jį dešiniuoju pelės klavišu ir pasirinkite **Ypatybės**. Pažymėkite žymės langelį **Atblokuoti**, tada pasirinkite **Taikyti**. Jei nematote žymės langelio **Atblokuoti**, ZIP failas jau yra atblokuotas ir galite praleisti šį veiksmą.

    ![Ypatybių dialogo langas](media/unblock_option.png)

2. Išskleiskite paketo ZIP failą ir nukopijuokite visus failus, esančius aplanke **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Aplanko „Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438” turinys](media/extract_package.png)

3. Įklijuokite visus nukopijuotus failus į „Package Deployer” įrankio aplanką **Įrankiai**. 
4. Norėdami pasirinkti „Common Data Service” aplinką ir įdiegti sprendimus, vykdykite **PackageDeployer.exe**.

    ![Aplanko „Įrankiai” turinys](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Įgalinkite ir peržiūrėkite priedo sekimo žurnalą „Common Data Service”, kad peržiūrėtumėte klaidos informaciją

**Reikiamas vaidmuo, norint įjungti sekimo žurnalą ir peržiūrėti klaidas:** sistemos administratorius

Norėdami įjungti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Sistema** pasirinkite **Administravimas**.
2. Puslapyje **Administravimas** pasirinkite **Sistemos parametrai**.
3. Skirtuko **Tinkinimas** lauke **Priedo ir pasirinktinės darbo eigos veiklos sekimas** pasirinkite **Viskas**, kad įgalintumėte priedo sekimo žurnalą. Jei norite registruoti sekimo žurnalus tik tada, kai įvyksta išimtys, vietoje to galite pasirinkti **Išimtis**.


Norėdami peržiūrėti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Finance and Operations” programos, atidarykite puslapį **Parametrai**, tada dalyje **Tinkinimas** pasirinkite **Priedo sekimo žurnalas**.
2. Raskite sekimo žurnalus, kuriuose laukas **Tipo pavadinimas** nustatytas kaip **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dukart spustelėkite elementą, kad peržiūrėtumėte visą žurnalą, tada „FastTab” **Vykdymas** peržiūrėkite tekstą **Pranešimų blokas**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Norėdami šalinti tiesioginio sinchronizavimo triktis „Finance and Operations” programose, įgalinkite derinimo režimą

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratoriaus dvigubos rašymo klaidos, sukurtos „Common Data Service”, gali atsirasti „Finance and Operations” programoje. Kai kuriais atvejais visas klaidos pranešimo tekstas nepasiekiamas, nes pranešimas yra per ilgas arba jame yra asmens identifikavimo informacijos (PII). Galite įjungti daugiažodį klaidų registravimą atlikdami šiuos veiksmus.

1. Visų „Finance and Operations” programų projektų konfigūracijų objekte **DualWriteProjectConfiguration** yra ypatybė **IsDebugMode**. Atidarykite objektą **DualWriteProjectConfiguration** naudodami „Excel“ papildinį.

    > [!TIP]
    > Galite lengvai atidaryti objektą, „Excel” papildinyje įjungdami režimą **Dizainas** ir į darbalapį įtraukdami **DualWriteProjectConfigurationEntity**. Daugiau informacijos žr. [Objektų duomenų atidarymas programoje „Excel“ ir jų atnaujinimas naudojant „Excel“ papildinį](../../office-integration/use-excel-add-in.md).

2. Nustatykite projekto ypatybę **IsDebugMode** kaip **Taip**.
3. Vykdyti scenarijų, kuris generuoja klaidas.
4. Daugiažodžiai žurnalai pasiekiami lentelėje „DualWriteErrorLog”. Norėdami peržiūrėti duomenis lentelės naršyklėje, naudokite šį URL (atitinkamai pakeiskite **XXX**):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Patikrinkite sinchronizavimo klaidas „Finance and Operations” programos virtualiojoje mašinoje

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius

1. Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).
2. Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.
3. Pasirinkite plytelę **Aplinkos diegimo debesyje įrankis**.
4. Norėdami prisijungti prie „Finance and Operations” programos virtualiosios mašinos, naudokite nuotolinį darbalaukį. Naudokite vietinę paskyrą, kurį yra rodoma LCS.
5. Atidarykite įvykių peržiūros programą.
6. Pasirinkite **Programų ir paslaugų žurnalai \> „Microsoft“ \> „Dynamics“ \> „AX-DualWriteSync“ \> Veikia**.
7. Peržiūrėti naujausių klaidų sąrašą.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Atsieti ir susieti kitą „Common Data Service” aplinką iš „Finance and Operations” programos

**Būtinas vaidmuo, norint atsieti aplinką:** „Finance and Operations” programų arba „Common Data Service” sistemos administratorius.

1. Prisijungimas prie „Finance and Operations” programos.
2. Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.
3. Pasirinkite visus veikiančius susiejimus, tada pasirinkite **Stabdyti**.
4. Pasirinkite **Atsieti aplinką**.
5. Kad patvirtintumėte operaciją, pasirinkite **Taip**.

Dabar galite susieti naują aplinką.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nepavyko peržiūrėti pardavimo užsakymo eilutės informacijos formos 

Sukurę pardavimo užsakymą „Dynamics 365 Sales”, paspaudę **+ Įtraukti produktus** galite būti nukreipti į „Dynamics 365 Project Operations” užsakymo eilutės formą. Nėra būdo toje formoje peržiūrėti pardavimo užsakymo eilutės formą **Informacija**. Parinktis **Informacija** neatsiranda toliau esančiame išplečiamajame lauke **Nauja užsakymo eilutė**. Taip nutinka, nes jūsų aplinkoje įdiegta „Project Operations”.

Norėdami iš naujo įgalinti formos parinktį **Informacija**, atlikite toliau pateiktus veiksmus.
1. Pereikite į objektą **Užsakymo eilutė**.
2. Formų mazge raskite formą **Informacija**. 
3. Pasirinkite formą **Informacija** ir spustelėkite **Įgalinti saugos vaidmenis**. 
4. Pakeiskite saugos parametro parinktį į **Rodyti visiems**.
