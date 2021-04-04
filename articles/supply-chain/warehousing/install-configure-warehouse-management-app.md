---
title: Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas
description: Šioje temoje aiškinama, kaip įdiegti sandėlio valdymo programėlę kiekviename jūsų mobiliajame įrenginyje ir sukonfigūruoti ją, kad prijungtumėte prie „Microsoft Dynamics 365 Supply Chain Management“ aplinkos.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e1e8c8b1464a38a0145cbdcdcb4882db00d3c4c1
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487030"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Šioje temoje aprašoma, kaip sukonfigūruoti naująją „Warehouse Management“ mobiliąją programėlę. Jei ieškote informacijos apie tai, kaip konfigūruoti seną sandėlio programą, žiūrėkite [Sandėlio programos diegimas ir prijungimas](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Šioje temoje paaiškinama, kaip atsisiųsti ir įdiegti „Warehouse Management“ programėlę kiekviename mobiliajame įrenginyje ir sukonfigūruoti programėlę, kad prijungtumėte prie „Supply Chain Management“ aplinkos. Kiekvieną įrenginį galite konfigūruoti neautomatiniu būdu arba galite importuoti ryšio parametrus naudodami failą arba nuskaitydami QR kodą.

## <a name="system-requirements"></a>Sistemos reikalavimai

Sandėlio valdymo mobiliųjų įrenginių programėlę galima naudoti tiek „Windows“, tiek „Google Android“ operacinėse sistemose. Norėdami naudoti programą, savo mobiliuosiuose įrenginiuose turite būti įdiegę vieną iš toliau nurodytų operacinių sistemų:

- „Windows 10” („Universal Windows Platform“ \[„UWP”\]) 2018 m. spalio mėn atnaujinimas 1809 (10.0.17763 komponavimo versija) arba naujesnė
- „Android 4.4“ arba naujesnė versija

## <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Norint naudoti programą, susijusi funkcija turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Naujos sandėlio programos vartotojo parametrai, piktogramos ir veiksmų pavadinimai*

## <a name="get-the-warehouse-management-mobile-app"></a>Gauti Sandėlio valdymo mobiliųjų įrenginių programėlę

Nedidelių diegimų atveju paprastai galite įdiegti programą iš atitinkamos parduotuvės kiekviename įrenginyje, o tada neautomatiniu būdu sukonfigūruoti ryšį su naudojamomis aplinkomis.

Diegdami didesniu mastu, galite automatizuoti programos diegimą ir (arba) konfigūraciją, nes taip gali būti patogiau valdant daug įrenginių. Pavyzdžiui, galite naudoti mobiliojo įrenginio valdymo ir mobiliųjų programų valdymo sprendimą, pvz., [„"Microsoft Intune“](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Norėdami gauti informacijos apie tai, kaip naudojant „Intune“ įtraukti programas, žr. [Programų įtraukimas į „Microsoft Intune“](https://docs.microsoft.com/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Programos diegimas iš programų parduotuvės

Paprasčiausias būdas įdiegti programą viename įrenginyje yra įdiegti ją iš programų parduotuvės, kur visada pateikiama naujausia bendrai prieinama versija. „Microsoft Intune“ taip pat gali rasti programėles iš programėlių parduotuvių. Norėdami įdiegti programą iš programų parduotuvės, naudokite vieną iš nurodytų nuorodų:

- **„Windows“ (UWP):**[Sandėlio valdymas „Microsoft Store“](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **„Android”:** [„Warehouse Management“ „Google Play“ parduotuvėje](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Atsisiųskite programą iš „Microsoft App Center“

Vietoje diegimo iš programų parduotuvės galite atsisiųsti programą iš „Microsoft App Center“. „App Center“ rasite įdiegiamus paketus, kuriuos galėsite perduodami naudodami artimojo ryšio duomenų perdavimą. Be dabartinės versijos, programų centre taip pat galėsite atsisiųsti ankstesnes versijas ir gauti ankstesnes versijas su būsimomis funkcijomis, kurias galite išbandyti. Norėdami atsisiųsti dabartines, ankstesnes arba peržiūrėti „Warehouse Management“ mobiliųjų įrenginių programos versijas iš „Microsoft App Center“, naudokite vieną iš šių nuorodų:

- **„Windows“ (UWP):** [„Warehouse Management“ („Windows“)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Instrukcijų apie tai, kaip įdiegti atsisiųstą paketą į „Windows“ įrenginį ir tada nustatyti reikiamus sertifikatus, ieškokite skyriuje [diegti versiją iš „App Center“](https://docs.microsoft.com/appcenter/distribution/installation).

- **„Android“:** [„Warehouse Management“ („Android“)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Jei atsisiųsite peržiūros versiją, jai įdiegti turėsite atlikti kelis papildomus veiksmus. Norėdami gauti daugiau informacijos, žiūrėkite [Android programų testavimas](https://docs.microsoft.com/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“

Norėdami įjungti Sandėlio valdymo mobiliųjų įrenginių programėlę, kad ji sąveikautų su konkrečiu „Supply Chain Management“ serveriu, turite užregistruoti žiniatinklio tarnybos programą, skirtą „Supply Chain Management“ nuomotojui „Azure Active Directory“ („Azure AD“). Toliau aprašyta procedūra pateikia vieną būdą, kaip atlikti šią užduotį. Išsamios informacijos ir alternatyvų ieškokite po procedūra pateiktuose saituose.

1. Interneto naršyklėje eikite į [https://portal.azure.com](https://portal.azure.com/).
1. Įveskite vartotojo, kuris turi prieigą prie „Azure“ prenumeratos, vardą ir slaptažodį.
1. „Azure“ portalo kairiajame naršymo skyde pasirinkite **Azure Active Directory**.

    ![Azure Active Directory](media/app-connect-azure-aad.png "„Azure Active Directory“")

1. Įsitikinkite, kad dirbate su „Azure AD“ egzemplioriumi, kurį naudoja „Supply Chain Management“.
1. Sąraše **Valdyti** pasirinkite **Programų registracijos**.

    ![Programų registracijos](media/app-connect-azure-register.png "Programų registracijos")

1. Įrankių juostoje pasirinkite **Nauja registracija**, kad būtų atidarytas vedlys **Registruoti programą**.
1. Įveskite programos pavadinimą, pasirinkite parinktį **Paskyros tik šiame organizaciniame kataloge**, tada pasirinkite **Registruoti**.

    ![Vedlys registruoti programą](media/app-connect-azure-register-wizard.png "Vedlys registruoti programą")

1. Atidaroma nauja programos registracija. Pasižymėkite **Programos (kliento) ID** reikšmę, nes jos reikės vėliau. Šis ID vėliau šioje temoje bus minimas kaip *kliento ID*.

    ![Programos (kliento) ID](media/app-connect-azure-app-id.png "Programos (kliento) ID")

1. Sąraše **Valdyti** pasirinkite **Sertifikatas ir slaptieji raktai**. Tada, atsižvelgdami į tai, kaip norite konfigūruoti programą autentifikavimui, pasirinkite vieną iš toliau pateiktų mygtukų. (Daugiau informacijos žr. tolesniame šios temos skyriuje [Autentifikavimas naudojant sertifikatą arba kliento slaptąjį raktą](#authenticate).)

    - **Įkelti sertifikatą** – įkelkite sertifikatą, kuris bus naudojamas kaip slaptasis raktas. Rekomenduojame šį būdą, nes jis saugesnis ir gali būti visiškai automatizuotas. Jei Sandėlio valdymo mobiliųjų įrenginių programėlę naudojate „Windows“ įrenginiuose, pasižymėkite rodomą **Nykščio antspaudas** vertę, po to kai įkeliate sertifikatą. Jums reikės šios reikšmės, kai konfigūruosite sertifikatą „Windows“ įrenginiuose.
    - **Naujas kliento slaptasis raktas** – sukurkite raktą įvesdami rakto aprašą ir trukmę dalyje **Slaptažodžiai**, tada pasirinkite **Įtraukti**. Sukurkite rakto kopiją ir saugiai išsaugokite.

    ![Sertifikatas ir slaptieji raktai](media/app-connect-azure-authentication.png "Sertifikatas ir slaptieji raktai")

Daugiau informacijos apie tai, kaip konfigūruoti žiniatinklio tarnybos programas „Azure AD“, ieškokite toliau nurodytuose ištekliuose.

- Instrukcijų, nurodančių, kaip naudoti „Windows PowerShell“ konfigūruojant žiniatinklio tarnybos programas „Azure AD“, ieškokite straipsnyje [Kaip naudoti „Azure PowerShell“ kuriant pagrindinę tarnybą su sertifikatu](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Norėdami gauti išsamios informacijos apie tai, kaip rankiniu būdu kurti žiniatinklio tarnybos programą „Azure AD“, žr. toliau nurodytas temas.

    - [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Kaip naudoti portalą kuriant „Azure AD“ programą ir pagrindinę tarnybą, galinčią pasiekti išteklius](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vartotojo paskyros kūrimas ir konfigūravimas programoje „Supply Chain Management“

Norėdami įgalinti „Supply Chain Management“, kad galėtumėte naudoti savo „Azure AD“ programą, atlikite toliau nurodytus veiksmus.

1. Sukurkite vartotoją, atitinkantį Sandėlio valdymo mobiliųjų įrenginių programėlės vartotojo kredencialus:

    1. Programoje „Supply Chain Management“ eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
    1. Sukurkite vartotoją.
    1. Priskirkite sandėliavimo mobiliojo įrenginio vartotoją.

    ![Sandėliavimo mobiliojo įrenginio vartotojo priskyrimas](media/app-connect-app-users.png "Sandėliavimo mobiliojo įrenginio vartotojo priskyrimas")

1. Susiekite savo „Azure AD“ programą su Sandėlio valdymo mobiliųjų įrenginių programėlės vartotoju:

    1. Eikite į **Sistemos administravimas \> Sąranka \> „Azure Active Directory“ programos**.
    1. Sukurkite eilutę.
    1. Įveskite kliento ID, kurį pasižymėjote ankstesniame skyriuje, suteikite jam pavadinimą ir pasirinkite ką tik sukurtą vartotoją. Rekomenduojame pažymėti visus savo įrenginius. Tada, jei prarasite įrenginį, galėsite lengvai pašalinti jo prieigą prie „Supply Chain Management“ šiame puslapyje.

    ![„Azure Active Directory“ programos](media/app-connect-aad-apps.png "„Azure Active Directory“ programos")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentifikavimas naudojant sertifikatą arba kliento slaptąjį raktą

Autentifikavimas su „Azure AD“ leidžia saugiai prijungti mobilųjį įrenginį prie „Supply Chain Management“. Autentifikuoti galite naudodami kliento slaptąjį raktą arba sertifikatą. Jei importuosite ryšio parametrus, rekomenduojame vietoj kliento slaptojo rakto naudoti sertifikatą. Kliento slaptasis raktas turi būti visada saugomas saugiai, todėl negalite jo importuoti iš ryšio parametrų failo arba QR kodo, kaip aprašyta toliau šioje temoje.

Sertifikatai gali būti naudojami kaip slaptieji raktai programos tapatybei įrodyti, kai prašomas atpažinimo ženklas. Viešoji sertifikato dalis įkeliama į programos registraciją „Azure“ portale, o visas sertifikatas turi būti įdiegtas kiekviename įrenginyje, kuriame įdiegta Sandėlio valdymo mobiliųjų įrenginių programėlė. Jūsų organizacija atsakinga už sertifikato rotacijos valdymą ir pan. Galite naudoti pasirašomus sertifikatus, bet visada turite naudoti neeksportuotinus sertifikatus.

Turite nustatyti, kad sertifikatas būtų pasiekiamas kiekviename įrenginyje, kuriame paleidžiate Sandėlio valdymo mobiliųjų įrenginių programėlę. Norėdami gauti daugiau informacijos apie tai, kaip valdyti „Intune“ kontroliuojamų įrenginių sertifikatus, jei naudojate „Intune“, žr. [Sertifikatų naudojamas autentifikavimui programoje „Microsoft Intune“](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Programos konfigūravimas importuojant ryšio parametrus

Kad būtų lengviau prižiūrėti ir diegti programą daugelyje mobiliųjų įrenginių, ryšio parametrus galite importuoti, o ne įvesti juos neautomatiniu būdu kiekviename įrenginyje. Šiame skyriuje aiškinama, kaip kurti ir importuoti parametrus.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Ryšio parametrų failų arba QR kodo kūrimas

Ryšio parametrus galite importuoti iš failo arba QR kodo. Abiem atvejais pirmiausia turite sukurti parametrų failą, kuris naudoja „JavaScript Object Notation“ (JSON) formatą ir sintaksę. Faile turi būti ryšių sąrašas, kuriame būtų atskiri įtrauktini ryšiai. Toliau pateiktoje lentelėje apibendrinami parametrai, kuriuos turite nurodyti ryšio parametrų faile.

| Parametras | aprašymas |
|---|---|
| ConnectionName | Nurodykite ryšio parametro pavadinimą. Maksimalus ilgis yra 20 simbolių. Ši reikšmė yra unikalus ryšio parametro identifikatorius, todėl įsitikinkite, ar ji sąraše yra unikali. Jei įrenginyje jau yra ryšys tokiu pačiu pavadinimu, parametrai iš importuoto failo jį panaikins. |
| ActiveDirectoryClientAppId | Nurodykite kliento ID, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service). |
| ActiveDirectoryResource | Nurodyti „Supply Chain Management“ šakninį URL. |
| ActiveDirectoryTenant | Nurodykite „Azure AD“ nuomotoją, kurį naudojate su „Supply Chain Management“ serveriu. Ši reikšmė yra tokio formato: `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Pavyzdys: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Įmonė | Programoje „Supply Chain Management‟ nurodykite juridinį subjektą, prie kurio norite prijungti programą. |
| ConnectionType | (Pasirinktinai) Nurodykite, ar norint prisijungti prie aplinkos ryšio parametras turi naudoti sertifikatą ar kliento slaptąjį raktą. Leistinos reikšmės yra *„certificate“* ir *„clientsecret“*. Numatytoji reikšmė yra *„certificate“*.<p>**Pastaba:** kliento slaptųjų raktų importuoti negalima.</p> |
| IsEditable | (Pasirinktinai) Nurodykite, ar programos vartotojas gali redaguoti ryšio parametrą. Leistinos reikšmės yra *„teisinga“* ir *„klaidinga“*. Numatytoji reikšmė yra *„teisinga“*. |
| IsDefault | (Pasirinktinai) Nurodykite, ar ryšys yra numatytasis. Ryšys, kuris yra nustatytas kaip numatytasis, atidarius programą bus pasirinktas automatiškai. Tik vienas ryšys gali būti nustatytas kaip numatytasis. Leistinos reikšmės yra *„teisinga“* ir *„klaidinga“*. Numatytoji reikšmė yra *„klaidinga“*. |
| CertificateThumbprint | (Pasirinktinai) „Windows“ įrenginiuose ryšiui galite nurodyti sertifikato kontrolinį kodą. „Android“ įrenginiuose, pirmą kartą naudojant ryšį, programos vartotojas turi pasirinkti sertifikatą. |

Toliau pateiktame pavyzdyje parodytas galiojantis ryšio parametrų failas, kuriame yra du ryšiai. Kaip matote, ryšių sąrašas (faile pavadintas *„ConnectionList“*) yra objektas, turintis masyvą, kuriame kiekvienas ryšys saugomas kaip objektas. Kiekvienas objektas turi būti nurodytas riestiniuose skliaustuose ({}) ir atskirtas kableliais, o masyvas turi būti riestiniuose skliaustuose (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Informaciją galite įrašyti kaip JSON failą arba sugeneruoti QR kodą su tokiu pačiu turiniu. Jei informaciją įrašote kaip failą, rekomenduojame jį įrašyti naudojant numatytąjį vardą *connections.json*, ypač, jei jį saugosite numatytoje vietoje kiekviename mobiliajame įrenginyje.

### <a name="save-the-connection-settings-file-on-each-device"></a>Ryšio parametrų failo įrašymas kiekviename įrenginyje

Paprastai ryšio parametrų failams paskirtyti kiekviename savo valdomame įrenginyje naudojate įrenginių valdymo įrankį arba scenarijų. Jei kiekviename įrenginyje naudojate numatytąjį pavadinimą ir vietą, kai įrašote ryšių nustatymų failą kiekviename įrenginyje, Sandėlio valdymo mobiliųjų įrenginių programėlė automatiškai jį importuos net ir pirmą kartą paleidus programėlę po jos įdiegimo. Jei naudosite pasirinktinį failo vardą arba vietą, pirmą kartą paleidus programą, vartotojas turi nurodyti reikšmes. Tačiau programa vėliau naudos nurodytą vardą ir vietą.

Kaskart paleidus programą, ji iš naujo importuoja ryšio parametrus iš ankstesnės vietos, kad nustatytų, ar buvo pakeitimų. Programa atnaujins tik tuos ryšius, kurių pavadinimai sutampa su ryšio parametrų faile esančių ryšių pavadinimais. Vartotojo sukurti ryšiai, kurie turi kitokius pavadinimus, atnaujinti nebus.

Negalite pašalinti ryšio naudodami ryšio parametrų failą.

Kaip buvo minėta, numatytasis failo vardas yra *connections.json*. Numatytoji failo vieta priklauso nuo to, ar naudojate „Windows“, ar „Android“ įrenginį:

- **„Windows“:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **„Android”:** `Android\data\com.Microsoft.WarehouseManagement\files`

Paprastai keliai automatiškai sukuriami po pirmo programos paleidimo. Tačiau galite juos sukurti neautomatiniu būdu, jei prieš diegdami turite perkelti ryšio parametrų failą į įrenginį.

> [!NOTE]
> Išdiegus programą, numatytasis kelias ir jo turinys yra pašalinami.

### <a name="import-the-connection-settings"></a>Ryšio parametrų importavimas

Norėdami importuoti ryšio parametrus iš failo arba QR kodo, atlikite toliau nurodytus veiksmus.

1. Paleiskite Sandėlio valdymo mobiliųjų įrenginių programėlę jūsų įrenginyje. Pirmą kartą paleidus programą rodomas pasveikinimo pranešimas. Paspauskite **Pasirinkti ryšį**.

    ![Pasveikinimo pranešimas](media/app-configure-welcome-screen.png "Pasveikinimo pranešimas")

1. Jei ryšio parametrus importuojate iš failo ir jį įrašant buvo naudojamas numatytasis vardas ir vieta, gali būti, kad programa jau rado failą. Tokiu atveju pereikite prie 4 veiksmo. Kitu atveju pasirinkite **Nustatyti ryšį**, o tada tęskite nuo 3 veiksmo.

    ![Nustatyti ryšį](media/app-configure-set-up-connection.png "Nustatyti ryšį")

1. Dialogo lange **Ryšio nustatymas** pasirinkite **Pridėti iš failo** arba **Pridėti iš QR kodo**, atsižvelgiant į tai, kaip norite importuoti parametrus:

    - Jei importuojate ryšio parametrus iš failo, pasirinkite **Pridėti iš failo**, naršykite į failą jūsų vietiniame įrenginyje ir jį pasirinkite. Jei pasirinksite pasirinktinę vietą, programa ją išsaugos ir automatiškai naudos kitą kartą.
    - Jei importuojate ryšio parametrus nuskaitydami QR kodą, pasirinkite **Pridėti iš QR kodo**. Programa paprašo leidimo naudoti įrenginio fotoaparatą. Kai suteikiate leidimą, fotoaparatas įjungiamas, kad galėtumėte jį naudoti nuskaitydami. Priklausomai nuo įrenginio fotoaparato kokybės ir QR kodo sudėtingumo, gali būti sunku gauti tinkamą nuskaitytą vaizdą. Tokiu atveju bandykite sumažinti QR kodo sudėtingumą sugeneruodami tik vieną ryšį vienam QR kodui. (Šiuo metu QR kodui nuskaityti galite naudoti tik įrenginio fotoaparatą.)

    ![Ryšio nustatymo meniu](media/app-configure-connection-setup-flyout.png "Ryšio nustatymo meniu")

1. Kai ryšio nustatymai įkelti sėkmingai, rodomas pasirinktas ryšys.

    ![Įkelti ryšio parametrai](media/app-configure-select-connection.png "Įkelti ryšio parametrai")

1. Jei naudojate „Android“ įrenginį ir autentifikavimui naudojate sertifikatą, įrenginys paragins pasirinkti sertifikatą.

    ![Sertifikato pasirinkimo raginimas „Android“ įrenginyje](media/app-configure-select-certificate.png "Sertifikato pasirinkimo raginimas „Android“ įrenginyje")

1. Programa prisijungia prie „Supply Chain Management“ serverio ir parodo prisijungimo puslapį.

    ![Prisijungimo puslapis](media/app-configure-sign-in-page.png "Prisijungimo puslapis")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Neautomatinis programos konfigūravimas

Jei neturite failo ar QR kodo, galite rankiniu būdu konfigūruoti programą įrenginyje, kad ji prie „Supply Chain Management“ serverio jungtųsi per „Azure AD“ programą.

1. Paleiskite Sandėlio valdymo mobiliųjų įrenginių programėlę jūsų įrenginyje.
1. Jei programa paleista **Demonstraciniu režimu**, pasirinkite **Ryšio parametrai**. Jei paleidus programą atsiranda **Prisijungimo** puslapis, pasirinkite **Keisti ryšį**.
1. Pasirinkite **Nustatyti ryšį**.

    ![Nustatyti ryšį](media/app-configure-set-up-connection.png "Nustatyti ryšį")

1. Pasirinkite **Įvesti rankiniu būdu**.

    ![Ryšio nustatymo meniu](media/app-configure-connection-setup-flyout.png "Ryšio nustatymo meniu")

    Pasirodo **Naujo ryšio** puslapis, rodantis išplėstumėte parametrus, kurių reikia norint neautomatiniu būdu įvesti ryšio informaciją.

    ![Neautomatiniai ryšio laukai](media/app-configure-input-manually.png "Neautomatiniai ryšio laukai")

1. Įveskite šią informaciją:

    - **Naudoti kliento slaptąjį raktą** – nustatykite šios pasirinkties reikšmę kaip _Taip_, kad galėtumėte naudoti kliento slaptąjį raktą atlikdami autentifikaciją „Supply Chain Management“. Nustatykite reikšmę _Ne_, kai autentifikavimui norite naudoti sertifikatą. (Daugiau informacijos ieškokite ankstesniame šios temos skyriuje [Žiniatinklio tarnybos prašymo kūrimas „Azure Active Directory”](#create-service).)
    - **Ryšio pavadinimas** – įveskite naujo ryšio pavadinimą. Šis pavadinimas bus rodomas lauke **Pasirinkti ryšį**, kai kitą kartą atidarysite ryšio parametrus. Jūsų įvestas pavadinimas turi būti unikalus. (Kitaip tariant, jis turi skirtis nuo visų kitų ryšių pavadinimų, saugomų jūsų įrenginyje, jei jame saugomi kokie nors ryšių pavadinimai.)
    - **„Azure Active Directory“ kliento ID** – įveskite kliento ID, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ kliento slaptasis raktas** – šis laukas galimas tik kai parinkties **Naudoti kliento slaptąjį raktą** reikšmė nustatyta kaip _Taip_. Įveskite kliento slaptąjį raktą, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ sertifikato kontrolinis kodas** – šis laukas galimas tik „Windows“ įrenginiuose ir tik tada, kai parinkties **Naudoti kliento slaptąjį raktą** reikšmė nustatyta į _Ne_. Įveskite sertifikato kontrolinį kodą, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ ištekliai** – nurodykite „Supply Chain Management“ šakninį URL.

        > [!IMPORTANT]
        > Šios reikšmės gale negali būti pasvirojo brūkšnio (/).

    - **„Active Directory“ nuomotojas** – įveskite „Azure AD“ nuomotoją, kurį naudojate su „Supply Chain Management“ serveriu. Ši reikšmė yra tokio formato: `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Pavyzdys: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!IMPORTANT]
        > Šios reikšmės gale negali būti pasvirojo brūkšnio (/).

    - **Įmonė** – „Supply Chain Management‟ įveskite juridinį subjektą (įmonę), prie kurio norite prijungti programą.

1. Viršutiniame dešiniajame puslapio kampe pasirinkite mygtuką **Įrašyti**.
1. Jei naudojate „Android“ įrenginį ir autentifikavimui naudojate sertifikatą, įrenginys paragins pasirinkti sertifikatą.
1. Programa prisijungia prie „Supply Chain Management“ serverio ir parodo prisijungimo puslapį.

## <a name="remove-access-for-a-device"></a>Įrenginio prieigos šalinimas

Jeigu įrenginys buvo pamestas arba pažeista jo sauga, turite pašalinti jo prieigą prie „Supply Chain Management“. Tolesni veiksmai aprašo rekomenduojamą prieigos šalinimo procesą.

1. Eikite į **Sistemos administravimas \> Sąranka \> „Azure Active Directory“ programos**.
1. Panaikinkite eilutę, atitinkančią įrenginį, kurio prieigą norite šalinti. Pasižymėkite kliento ID, kuris naudojamas su įrenginiu, nes jo prireiks vėliau.

    Jei esate užregistravę tik vieną kliento ID, ir keli įrenginiai naudoja tą patį kliento ID, tuose įrenginiuose turite nustatyti naujus ryšio parametrus. Priešingu atveju jie praras prieigą.

1. Prisijunkite prie „Azure“ portalo adresu [https://portal.azure.com](https://portal.azure.com/).
1. Kairiojoje naršymo srityje pasirinkite **Active Directory** ir įsitikinkite, kad esate tinkamame kataloge.
1. Sąraše **Valdyti** pasirinkite **Programų registracijos**, tada pasirinkite programą, kurią norite konfigūruoti. Atidaromas puslapis **Parametrai** ir rodoma konfigūravimo informacija.
1. Įsitikinkite, kad programos kliento ID sutampa su kliento ID, kurį pasižymėjote atlikdami 2 veiksmą.
1. Įrankių juostoje pasirinkite **Naikinti**.
1. Pasirodžiusiame patvirtinimo pranešime pasirinkite **Taip**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]