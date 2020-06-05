---
title: Sandėliavimo programos diegimas ir prijungimas
description: Šioje temoje aiškinama, kaip įdiegti sandėliavimo programą kiekviename mobiliajame įrenginyje ir kaip ją sukonfigūruoti, kad būtų galima prisijungti prie „Microsoft Dynamics 365 Supply Chain Management“ aplinkos. Kiekvieną įrenginį galite konfigūruoti neautomatiniu būdu arba galite importuoti ryšio parametrus naudodami failą arba nuskaitydami QR kodą.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 290888dbf7d194b8cf259d7218d01d4a4f911db0
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367087"
---
# <a name="install-and-connect-the-warehousing-app"></a>Sandėliavimo programos diegimas ir prijungimas

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šioje temoje aprašoma, kaip sukonfigūruoti visuotinėms debesies įdiegtims skirtą sandėliavimo funkciją. Jei ieškote informacijos, kaip konfigūruoti vietinėms visuotinėms įdiegtims skirtą sandėliavimo funkciją, žr. [Vietinėms visuotinėms įdiegtims skirtas sandėliavimas](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Sandėliavimo programą galima atsisiųsti iš „Google Play" parduotuvės ir „Microsoft Store“ parduotuvės. Ji teikiamas kaip atskiras komponentas. Todėl ją turite atsisiųsti į kiekvieną įrenginį ir sukonfigūruoti, kad būtų galima prisijungti prie „Microsoft Dynamics 365 Supply Chain Management“ aplinkos.

Šioje temoje aiškinama, kaip įdiegti sandėliavimo programą kiekviename mobiliajame įrenginyje ir kaip ją sukonfigūruoti, kad būtų galima prisijungti prie „Supply Chain Management“ aplinkos. Kiekvieną įrenginį galite konfigūruoti neautomatiniu būdu arba galite importuoti ryšio parametrus naudodami failą arba nuskaitydami QR kodą.

## <a name="system-requirements"></a>Sistemos reikalavimai

Sandėliavimo programą galima naudoti ir „Windows“, ir „Android“ operacinėse sistemoje. Norėdami naudoti naujausią programos versiją, savo mobiliuosiuose įrenginiuose turite būti įdiegę vieną iš toliau nurodytų operacinių sistemų.

- „Windows 10 Fall Creators Update“ („Universal Windows Platform“ \[UWP\]) 1709 (10.0.16299 komponavimo versija) arba naujesnė versija
- „Android 4.4“ arba naujesnė versija

> [!NOTE]
> Jei turite palaikyti senesnius „Windows“ įrenginius, kuriuose neveikia naujausia „Windows“ versija, vis tiek galite iš „Microsoft Store“ parduotuvės atsisiųsti sandėliavimo programos 1.6.3.0 versiją. Ši versija veiks „Windows 10 November Update“ (UWP) 1511 (10.0.10586 komponavimo versija) arba naujesnėje versijoje. Tačiau atminkite, kad ši sandėliavimo programos versija nepalaiko masinio ryšio parametrų diegimo. Todėl turite [rankiniu būdu sukonfigūruoti ryšį](#config-manually) kiekviename įrenginyje, kuriame veikia ši programos versija.

## <a name="get-the-warehousing-app"></a>Sandėliavimo programos įsigijimas

Norėdami atsisiųsti programą, naudokite vieną iš toliau nurodytų saitų.

- **„Windows“ (UWP):** [„Dynamics 365 for Finance and Operations - Warehousing“ parduotuvėje „Microsoft Store“](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [„Warehousing - Dynamics 365“ parduotuvėje „Google Play“](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Nedidelių diegimų atveju galite kiekviename įrenginyje įdiegti programą iš atitinkamos parduotuvės, o tada neautomatiniu būdu sukonfigūruoti ryšį su naudojamomis aplinkomis. Tačiau 1.7.0.0 ir naujesnėse sandėliavimo programos versijose programos diegimą ir (arba) konfigūravimą galite automatizuoti. Šis būdas patogus, jei valdote daug įrenginių ir naudojate mobiliųjų įrenginių bei mobiliųjų programų valdymo sprendimą, pvz., [„Microsoft Intune“](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Norėdami gauti informacijos apie tai, kaip naudojant „Intune“ įtraukti programas, žr. [Programų įtraukimas į „Microsoft Intune“](https://docs.microsoft.com/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“

Norėdami įjungti sandėliavimo programos sąveiką su konkrečiu „Supply Chain Management“ serveriu, žiniatinklio tarnybos programą turite užregistruoti „Supply Chain Management“ nuomotojo „Azure Active Directory“ („Azure AD“). Toliau aprašyta procedūra pateikia vieną būdą, kaip atlikti šią užduotį. Išsamios informacijos ir alternatyvų ieškokite po procedūra pateiktuose saituose.

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

    - **Įkelti sertifikatą** – įkelkite sertifikatą, kuris bus naudojamas kaip slaptasis raktas. Rekomenduojame šį būdą, nes jis saugesnis ir gali būti visiškai automatizuotas. Jei sandėliavimo programą naudojate „Windows“ įrenginiuose, pasižymėkite **Kontrolinis kodas** reikšmę, kuri rodoma nusiuntus sertifikatą. Jums reikės šios reikšmės, kai konfigūruosite sertifikatą „Windows“ įrenginiuose.
    - **Naujas kliento slaptasis raktas** – sukurkite raktą įvesdami rakto aprašą ir trukmę dalyje **Slaptažodžiai**, tada pasirinkite **Įtraukti**. Sukurkite rakto kopiją ir saugiai išsaugokite.

    ![Sertifikatas ir slaptieji raktai](media/app-connect-azure-authentication.png "Sertifikatas ir slaptieji raktai")

Daugiau informacijos apie tai, kaip konfigūruoti žiniatinklio tarnybos programas „Azure AD“, ieškokite toliau nurodytuose ištekliuose.

- Instrukcijų, nurodančių, kaip naudoti „Windows PowerShell“ konfigūruojant žiniatinklio tarnybos programas „Azure AD“, ieškokite straipsnyje [Kaip naudoti „Azure PowerShell“ kuriant pagrindinę tarnybą su sertifikatu](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Norėdami gauti išsamios informacijos apie tai, kaip rankiniu būdu kurti žiniatinklio tarnybos programą „Azure AD“, žr. toliau nurodytas temas.

    - [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Kaip naudoti portalą kuriant „Azure AD“ programą ir pagrindinę tarnybą, galinčią pasiekti išteklius](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Vartotojo paskyros kūrimas ir konfigūravimas programoje „Supply Chain Management“

Norėdami įgalinti „Supply Chain Management“, kad galėtumėte naudoti savo „Azure AD“ programą, atlikite toliau nurodytus veiksmus.

1. Sukurkite vartotoją, kuris atitinka sandėliavimo programos vartotojo kredencialus.

    1. Programoje „Supply Chain Management“ eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
    1. Sukurkite vartotoją.
    1. Priskirkite sandėliavimo mobiliojo įrenginio vartotoją.

    ![Sandėliavimo mobiliojo įrenginio vartotojo priskyrimas](media/app-connect-app-users.png "Sandėliavimo mobiliojo įrenginio vartotojo priskyrimas")

1. Susiekite savo „Azure AD“ programą su sandėliavimo programos vartotoju atlikdami toliau nurodytus veiksmus.

    1. Eikite į **Sistemos administravimas \> Sąranka \> „Azure Active Directory“ programos**.
    1. Sukurkite eilutę.
    1. Įveskite kliento ID, kurį pasižymėjote ankstesniame skyriuje, suteikite jam pavadinimą ir pasirinkite ką tik sukurtą vartotoją. Rekomenduojame pažymėti visus savo įrenginius. Tada, juos praradus, galėsite lengvai pašalinti jų prieigą prie „Supply Chain Management“ šiame puslapyje.

    ![„Azure Active Directory“ programos](media/app-connect-aad-apps.png "„Azure Active Directory“ programos")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Autentifikavimas naudojant sertifikatą arba kliento slaptąjį raktą

Autentifikavimas su „Azure AD“ leidžia saugiai prijungti mobilųjį įrenginį prie „Supply Chain Management“. Autentifikuoti galite naudodami kliento slaptąjį raktą arba sertifikatą. Jei importuosite ryšio parametrus, rekomenduojame vietoj kliento slaptojo rakto naudoti sertifikatą. Kliento slaptasis raktas turi būti visada saugomas saugiai, todėl negalite jo importuoti iš ryšio parametrų failo arba QR kodo, kaip aprašyta toliau šioje temoje.

Sertifikatai gali būti naudojami kaip slaptieji raktai programos tapatybei įrodyti, kai prašomas atpažinimo ženklas. Viešoji sertifikato dalis nusiunčiama į programos registraciją „Azure“ portale, o visas sertifikatas turi būti įdiegtas kiekviename įrenginyje, kuriame įdiegta sandėliavimo programa. Jūsų organizacija atsakinga už sertifikato rotacijos valdymą ir pan. Galite naudoti pasirašomus sertifikatus, bet visada turite naudoti neeksportuotinus sertifikatus.

Turite nustatyti, kad sertifikatas būtų pasiekiamas kiekviename įrenginyje, kuriame paleidžiate sandėliavimo programą. Norėdami gauti daugiau informacijos apie tai, kaip valdyti „Intune“ kontroliuojamų įrenginių sertifikatus, jei naudojate „Intune“, žr. [Sertifikatų naudojamas autentifikavimui programoje „Microsoft Intune“](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Programos konfigūravimas importuojant ryšio parametrus

Kad būtų lengviau prižiūrėti ir diegti programą daugelyje mobiliųjų įrenginių, ryšio parametrus galite importuoti, o ne įvesti juos neautomatiniu būdu kiekviename įrenginyje. Šiame skyriuje aiškinama, kaip kurti ir importuoti parametrus.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Ryšio parametrų failų arba QR kodo kūrimas

Ryšio parametrus galite importuoti iš failo arba QR kodo. Abiem atvejais pirmiausia turite sukurti parametrų failą, kuris naudoja „JavaScript Object Notation“ (JSON) formatą ir sintaksę. Faile turi būti ryšių sąrašas, kuriame būtų atskiri įtrauktini ryšiai. Toliau pateiktoje lentelėje apibendrinami parametrai, kuriuos turite nurodyti ryšio parametrų faile.

| Parametras | aprašymas |
| --- | --- |
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

Paprastai ryšio parametrų failams paskirtyti kiekviename savo valdomame įrenginyje naudojate įrenginių valdymo įrankį arba scenarijų. Jei kiekviename įrenginyje įrašydami ryšio parametrų failą naudosite numatytąjį vardą ir vietą, sandėliavimo programa jį importuos automatiškai, net kai programa bus paleista pirmą kartą po įdiegimo. Jei naudosite pasirinktinį failo vardą arba vietą, pirmą kartą paleidus programą, vartotojas turi nurodyti reikšmes. Tačiau programa vėliau naudos nurodytą vardą ir vietą.

Kaskart paleidus programą, ji iš naujo importuoja ryšio parametrus iš ankstesnės vietos, kad nustatytų, ar buvo pakeitimų. Programa atnaujins tik tuos ryšius, kurių pavadinimai sutampa su ryšio parametrų faile esančių ryšių pavadinimais. Vartotojo sukurti ryšiai, kurie turi kitokius pavadinimus, atnaujinti nebus.

Negalite pašalinti ryšio naudodami ryšio parametrų failą.

Kaip buvo minėta, numatytasis failo vardas yra *connections.json*. Numatytoji failo vieta priklauso nuo to, ar naudojate „Windows“, ar „Android“ įrenginį:

- **„Windows“:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **„Android“:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Paprastai keliai automatiškai sukuriami po pirmo programos paleidimo. Tačiau galite juos sukurti neautomatiniu būdu, jei prieš diegdami turite perkelti ryšio parametrų failą į įrenginį.

> [!NOTE]
> Išdiegus programą, numatytasis kelias ir jo turinys yra pašalinami.

### <a name="import-the-connection-settings"></a>Ryšio parametrų importavimas

Norėdami importuoti ryšio parametrus iš failo arba QR kodo, atlikite toliau nurodytus veiksmus.

1. Atidarykite sandėliavimo programą savo mobiliajame įrenginyje.
1. Eikite į **Ryšio parametrai**.
1. Nustatykite parinkties **Naudoti demonstracinį režimą** reikšmę kaip _Ne_.

    ![Demonstracinio režimo parinkties naudojimas](media/app-connect-app-demo-mode.png "Demonstracinio režimo parinkties naudojimas")

1. Atsižvelgdami į tai, kaip norite importuoti parametrus, pasirinkite **Pasirinkti failą** arba **Nuskaityti QR kodą**.

    - Jei ryšio parametrus importuojate iš failo, gali būti, kad programa jau rado failą, jeigu jį įrašant buvo naudojamas numatytasis vardas ir numatytoji vieta. Kitu atveju pasirinkite **Pasirinkti failą**, pereikite prie failo vietiniame įrenginyje ir jį pasirinkite. Jei pasirinksite pasirinktinę vietą, programa ją išsaugos ir automatiškai naudos kitą kartą.
    - Jei importuojate ryšio parametrus nuskaitydami QR kodą, pasirinkite **Nuskaityti QR kodą**. Programa paprašo leidimo naudoti įrenginio fotoaparatą. Kai suteikiate leidimą, fotoaparatas įjungiamas, kad galėtumėte jį naudoti nuskaitydami. Priklausomai nuo įrenginio fotoaparato kokybės ir QR kodo sudėtingumo, gali būti sunku gauti tinkamą nuskaitytą vaizdą. Tokiu atveju bandykite sumažinti QR kodo sudėtingumą sugeneruodami tik vieną ryšį vienam QR kodui. (Šiuo metu QR kodui nuskaityti galite naudoti tik įrenginio fotoaparatą.)

    ![Ryšio parametrų importavimas](media/app-connect-app-select-file.png "Ryšio parametrų importavimas")

1. Kai ryšio parametrai sėkmingai įkeliami, viršutiniame kairiajame puslapio kampe pasirinkite mygtuką **Atgal** (rodyklė kairėn).

    ![Įkelti ryšio parametrai](media/app-connect-app-settings-loaded.png "Įkelti ryšio parametrai")

1. Jei naudojate „Android“ įrenginį ir autentifikavimui naudojate sertifikatą, įrenginys paragins pasirinkti sertifikatą.

    ![Raginimas pasirinkti sertifikatą „Android“ įrenginyje](media/app-connect-app-choose-cert.png "Raginimas pasirinkti sertifikatą „Android“ įrenginyje")

1. Programa prisijungia prie „Supply Chain Management“ serverio ir parodo prisijungimo puslapį.

    ![Prisijungimo puslapis](media/app-connect-sign-in.png "Prisijungimo puslapis")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Neautomatinis programos konfigūravimas

Galite neautomatiškai konfigūruoti programą įrenginyje, kad ji prie „Supply Chain Management“ serverio jungtųsi per „Azure AD“ programą.

1. Atidarykite sandėliavimo programą savo mobiliajame įrenginyje.
1. Eikite į **Ryšio parametrai**.
1. Nustatykite parinkties **Naudoti demonstracinį režimą** reikšmę kaip _Ne_.

    ![Demonstracinis režimas išjungtas](media/app-connect-app-select-file.png "Demonstracinis režimas išjungtas")

1. Bakstelėkite lauką **Pasirinkti ryšį**, kad išplėstumėte parametrus, kurių reikia norint neautomatiniu būdu įvesti ryšio informaciją.

    ![Neautomatiniai ryšio laukai](media/app-connect-manual-connect.png "Neautomatiniai ryšio laukai")

1. Įveskite šią informaciją:

    - **Naudoti kliento slaptąjį raktą** – nustatykite šios pasirinkties reikšmę kaip _Taip_, kad galėtumėte naudoti kliento slaptąjį raktą atlikdami autentifikaciją „Supply Chain Management“. Nustatykite reikšmę _Ne_, kai autentifikavimui norite naudoti sertifikatą. (Daugiau informacijos žr. [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).)
    - **Ryšio pavadinimas** – įveskite naujo ryšio pavadinimą. Šis pavadinimas bus rodomas lauke **Pasirinkti ryšį**, kai kitą kartą atidarysite ryšio parametrus. Jūsų įvestas pavadinimas turi būti unikalus. (Kitaip tariant, jis turi skirtis nuo visų kitų ryšių pavadinimų, kurie yra saugomi jūsų įrenginyje, jei jame saugomi kokie nors ryšių pavadinimai.)
    - **„Azure Active Directory“ kliento ID** – įveskite kliento ID, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ kliento slaptasis raktas** – šis laukas galimas tik kai parinkties **Naudoti kliento slaptąjį raktą** reikšmė nustatyta kaip _Taip_. Įveskite kliento slaptąjį raktą, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ sertifikato kontrolinis kodas** – šis laukas galimas tik „Windows“ įrenginiuose, kai parinkties **Naudoti kliento slaptąjį raktą** reikšmė nustatyta kaip _Ne_. Įveskite sertifikato kontrolinį kodą, kurį pasižymėjote, kai konfigūravote „Azure AD“ dalyje [Žiniatinklio tarnybos programos kūrimas naudojant „Azure Active Directory“](#create-service).
    - **„Active Directory“ ištekliai** – nurodykite „Supply Chain Management“ šakninį URL.

        > [!NOTE]
        > Šios reikšmės gale negali būti pasvirojo brūkšnio (/).

    - **„Active Directory“ nuomotojas** – įveskite „Azure AD“ nuomotoją, kurį naudojate su „Supply Chain Management“ serveriu. Ši reikšmė yra tokio formato: `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Pavyzdys: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Šios reikšmės gale negali būti pasvirojo brūkšnio (/).

    - **Įmonė** – programoje „Supply Chain Management‟ įveskite juridinį subjektą, prie kurio norite prijungti programą.

1. Viršutiniame dešiniajame puslapio kampe pasirinkite mygtuką **Įrašyti**.
1. Jei naudojate „Android“ įrenginį ir autentifikavimui naudojate sertifikatą, įrenginys paragins pasirinkti sertifikatą.
1. Programa prisijungia prie „Supply Chain Management“ serverio ir parodo prisijungimo puslapį.

## <a name="remove-access-for-a-device"></a>Įrenginio prieigos šalinimas

Jei įrenginys buvo pamestas arba pažeista jo sauga, turite pašalinti įrenginio prieigą prie „Supply Chain Management“. Tolesni veiksmai aprašo rekomenduojamą prieigos šalinimo procesą.

1. Eikite į **Sistemos administravimas \> Sąranka \> „Azure Active Directory“ programos**.
1. Panaikinkite eilutę, atitinkančią įrenginį, kurio prieigą norite šalinti. Pasižymėkite kliento ID, kuris naudojamas su šalinamu įrenginiu, nes jo prireiks vėliau.

    Jei esate užregistravę tik vieną kliento ID, ir keli įrenginiai naudoja tą patį kliento ID, tuose įrenginiuose turite nustatyti naujus ryšio parametrus. Priešingu atveju jie praras prieigą.

1. Prisijunkite prie „Azure“ portalo adresu [https://portal.azure.com](https://portal.azure.com/).
1. Kairiojoje naršymo srityje pasirinkite **Active Directory** ir įsitikinkite, kad esate tinkamame kataloge.
1. Sąraše **Valdyti** pasirinkite **Programų registracijos**, tada pasirinkite programą, kurią norite konfigūruoti. Atidaromas puslapis **Parametrai** ir rodoma konfigūravimo informacija.
1. Įsitikinkite, kad programos kliento ID sutampa su kliento ID, kurį pasižymėjote atlikdami 2 veiksmą.
1. Įrankių juostoje pasirinkite **Naikinti**.
1. Pasirodžiusiame patvirtinimo pranešime pasirinkite **Taip**.
