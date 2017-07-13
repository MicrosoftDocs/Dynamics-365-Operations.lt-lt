---
title: "Duomenų atnaujinimas smėlio dėžės aplinkoje"
description: "Šioje temoje paaiškinama, kaip atnaujinti duomenis iš „AX 2012“ į „Dynamics 365 for Finance and Operations“ smėlio dėžės aplinkoje."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: lt-lt
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Duomenų atnaujinimas smėlio dėžės aplinkoje

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Šios užduoties išvestis yra atnaujinta duomenų bazė, kurią galite naudoti smėlio dėžės aplinkoje. Smėlio dėžės aplinkoje verslo vartotojai ir funkcinės komandos nariai gali tikrinti programos funkcijas. Šios funkcijos apima tinkinimus ir duomenis, kurie buvo perkelti iš „Microsoft Dynamics AX 2012“.

Primygtinai rekomenduojame paleisti duomenų naujinimo procesą programavimo aplinkoje prieš paleidžiant jį bendrinamoje smėlio dėžės aplinkoje – toks būdas padės sutrumpinti bendrą laiką, reikalingą norint sėkmingai atnaujinti duomenis. Daugiau informacijos rasite [Duomenų naujinimas programavimo aplinkoje](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Smėlio dėžės duomenų naujinimo proceso apžvalga

Prieš pradėdami naujinti duomenis smėlio dėžės aplinkoje jau turėsite atnaujintus duomenis programavimo aplinkoje, kaip paaiškinta dalyje [Duomenų naujinimas programavimo aplinkoje](prepare-data-upgrade.md). Du procesai yra labai panašūs. Pagrindinis skirtumas yra tas, kad smėlio dėžės aplinkoje duomenims saugoti naudojama „Microsoft Azure SQL“ duomenų bazė, o programavimo aplinkoje naudojama „Microsoft SQL Server“. Šis techninis duomenų bazės sluoksnio skirtumas reikalauja šiek tiek pakeisti duomenų naujinimo procedūrą smėlio dėžės aplinkoje, nes atsarginė kopija iš „AX 2012“ duomenų bazės egzemplioriaus negali būti atkurta SQL duomenų bazėje.

![Smėlio dėžės duomenų naujinimo procesas](./media/data-upgrade-sandbox.png)

Čia pateikti naujinimo proceso aukšto lygio veiksmai.

1. Sukurkite „AX 2012“ duomenų bazės kopiją. Primygtinai rekomenduojame naudoti kopiją, nes turite panaikinti kai kuriuos kopijos, kuri bus eksportuojama, objektus.
2. Eksportuokite nukopijuotą duomenų bazę į „bacpac“ failą naudodami nemokamą „SQL Server“ įrankį, pavadintą SQLPackage.exe. Šis įrankis suteikia specialaus tipo duomenų bazės atsarginę kopiją, kurią galima importuoti į SQL duomenų bazę.
3. Įkelkite „bacpac“ failą į „Azure“ saugyklą.
4. Atsisiųskite „bacpac“ failą į Programos objektų serverio (AOS) įrenginį smėlio dėžės aplinkoje, tada importuokite naudodami SQLPackage.exe. Tada turite vykdyti scenarijų su importuota duomenų baze norėdami iš naujo nustatyti SQL duomenų bazės vartotojus.
5. Paleiskite MajorVersionDataUpgrade.zip paketą norėdami atnaujinti duomenis pagal importuotą duomenų bazę.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Sukurkite „AX 2012“ duomenų bazės kopiją

Turite sukurti „AX 2012“ duomenų bazės, kurią naujinate, kopiją, nes reikia panaikinti kai kuriuos duomenų bazės objektus. Šie objektai apima visus „Microsoft Windows“ autentifikavimo vartotojus. Šie pakeitimai lėmė, kad modifikuota duomenų bazė netinkama naudoti „AX 2012“. Atlikdami šį veiksmą sukursite duomenų bazės kopiją ir panaikinsite šiuos objektus.

Šį veiksmą turi atlikti duomenų bazės administratorius (DBA) arba asmuo, turintis panašių žinių ir patirties.

Norėdami sukurti duomenų bazės kopiją, sukurkite pradinės duomenų bazės atsarginę kopiją ir atkurkite ją nauju pavadinimu. Įsitikinkite, kad abiem duomenų bazėms pakanka vietos. Galite sukurti kopiją kitame serveryje. Svarbi yra „SQL Server“ egzemplioriaus versija, kurioje naudojama duomenų bazė.

Čia yra kodo, kuris sukuria duomenų bazės kopiją, pavyzdys. Šį pavyzdį turite modifikuoti, kad būtų perteikti jūsų konkrečios duomenų bazės pavadinimai.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Sukūrę kopiją paleiskite šį „Transact-SQL“ (T-SQL) scenarijų.
UŽDUOTIS 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Eksportuokite nukopijuotą duomenų bazę į „bacpac“ failą

Eksportuokite nukopijuotą duomenų bazę į „bacpac“ failą naudodami SQLPackage.exe įrankį. Šį veiksmą turėtų atlikti DBA arba komandos narys, turintis lygiaverčių žinių.

Labai svarbu, kad prieš pradėdami šį veiksmą įdiegtumėte naujausią „SQL Server Management Studio“ versiją. Nors „SQLPackage“ yra ankstesnės „Management Studio“, ji šiame veiksme tinkamai neveiks pirmiau neįdiegus naujausios versijos.

Šis veiksmas yra svarbus, nes vėl reikės eksportuoti prastovos metu prieš galutinai paleidžiant. Štai keletas patarimų:

- „Bacpac“ procesas labai intensyviai naudoja įvestį / išvestį ir procesorių. Todėl eksportavimą atlikite didelės galios įrenginyje.
- „SQLPackage“ turėtų būti vykdomas vietoje, įrenginyje, kuriame yra duomenų bazė. Neleiskite „SQLPackage“ vietiniame nešiojamajame kompiuteryje, kurį prijungiate prie duomenų bazės įrenginio, nes šis procesas intensyviai naudoja ir tinklą.

Tada kaip administratorius atidarykite langą **Komandinė eilutė** ir vykdykite nurodytas komandas.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Čia yra paaiškinti parametrai:

- **ssn** (šaltinio serverio pavadinimas) – „SQL Server“, iš kurio eksportuojama, pavadinimas. Mūsų procese šis parametras visada turėtų būti nustatytas į **localhost**.
- **sdn** (šaltinio duomenų bazės pavadinimas) – eksportuotinos duomenų bazės pavadinimas.
- **tf** (paskirties failas) – failo, į kurį bus eksportuojama, maršrutas ir pavadinimas. Aplankas jau turėtų būti, o failą sukurs procesas.
- **/p:CommandTimeout** – užklausos skirtojo laiko vertė. Šis parametras leidžia eksportuoti didesnes lenteles neišnaudojant skirtojo laiko.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>„bacpac“ failo nusiuntimas į „Azure“ saugyklą

Įkelkite savo „bacpac“ failą į „Azure“ saugyklą. Žr. UsingStorageExplorer.docx UŽDUOTĮ

### <a name="import-the-bacpac-file-into-sql-database"></a>Importuoti „bacpac“ failą į SQL duomenų bazę

Atlikdami šį veiksmą galite importuoti eksportuotą „bacpac“ failą į SQL duomenų bazės egzempliorių, kurį naudoja jūsų smėlio dėžės aplinka. Pirmiausia AOS kompiuteryje turite įdiegti naujausią „Management Studio“ versiją. Tada importuosite failą naudodami SQLPackage.exe įrankį.

Šias užduotis atliksite tiesiai AOS kompiuteryje smėlio dėžės aplinkoje, nes yra užkardos taisyklės, kurios riboja prieigą prie SQL duomenų bazės egzemplioriaus. Tačiau naudodami AOS kompiuterį galite gauti prieigą.

Kaip ir atliekant eksportavimo veiksmą, prieš importuojant reikia turėti naujausią „Management Studio“ versiją. Šis veiksmas neveiks, jei turite senesnę versiją.

Dėl efektyvumo priežasčių rekomenduojame „bacpac“ laikyti AOS kompiuterio D diske. „Azure“ virtualiuosiuose įrenginiuose (VM) D diskas yra fizinis diskas, kuris paprastai yra našesnis nei kiti pasiekiami diskai.

Kaip administratorius atidarykite langą **Komandinė eilutė** ir vykdykite nurodytas komandas.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Čia yra paaiškinti parametrai:

- **tsn** (paskirties serverio pavadinimas) – „SQL Azure server“, į kurį importuojama, pavadinimas. Pavadinimą galima rasti LCS. Pridėkite **. database.windows.net**.
- **tdn** (paskirties duomenų bazės pavadinimas) – duomenų bazės, į kurią importuojama, pavadinimas. Duomenų bazės neturėtų būti. Ją sukurs importavimo procesas.
- **sf** (šaltinio failas) – failo, iš kurio importuojama, maršrutas ir pavadinimas.
- **tp** (paskirties slaptažodis) – paskirties SQL duomenų bazės egzemplioriaus SQL slaptažodis.
- **tu** (paskirties vartotojas) – paskirties SQL duomenų bazės egzemplioriaus SQL vartotojo vardas. Rekomenduojame naudoti **sqladmin**. Šio vartotojo slaptažodį galite gauti iš savo LCS projekto.
- **/p:CommandTimeout** – užklausos skirtojo laiko vertė. Šis parametras leidžia eksportuoti didesnes lenteles neišnaudojant skirtojo laiko.
- **/p:DatabaseServiceObjective** – sukurtos duomenų bazės paslaugų pakopos lygis Galite patikrinti esamos duomenų bazės vertę naudodami „Management Studio“. Dešiniuoju pelės mygtuku spustelėkite duomenų bazę, tada pasirinkite **Ypatybės**.

Įvykdę komandas, gausite toliau nurodytą įspėjimą. Galite jo nepaisyti.

![Smėlio dėžės klaida](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Paleiskite MajorVersionDataUpgrade.zip paketą

Paleiskite duomenų naujinimo diegimo paketą kaip aprašyta [Duomenų naujinimas diegimo, demonstravimo arba smėlio dėžės aplinkose](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Atnaujinti duomenų bazės kopiją programavimo aplinkoje

Naudinga atnaujinti tą pačią duomenų bazę programavimo aplinkoje. Jei turite programavimo aplinkai tinkamos duomenų bazės kopiją, bus lengviau ištirti klaidas, kurios randamos atnaujintoje smėlio dėžės aplinkoje.

