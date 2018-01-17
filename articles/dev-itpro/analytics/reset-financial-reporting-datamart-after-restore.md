---
title: "Finansinių ataskaitų duomenų srities nustatymas iš naujo"
description: "Šioje temoje aprašoma, kaip iš naujo nustatyti finansinių ataskaitų duomenų sritį."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: lt-lt
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Finansinių ataskaitų duomenų srities nustatymas iš naujo

[!include[banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip iš naujo nustatyti finansinių ataskaitų duomenų sritį naudojant šias versijas:

- „Microsoft Dynamics 365 for Finance and Operations‟ finansinių ataskaitų leidimas 7.2.6.0 ir naujesnė versija
- „Microsoft Dynamics 365 for Finance and Operations‟ finansinių ataskaitų leidimas 7.0.10000.4 ir naujesnė versija
- „Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimas (vietinis)

Norėdami gauti „Finance and Operations“ finansinių ataskaitų leidimą 7.2.6.0, galite atsisiųsti KB 4052514 iš <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>„Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 ir naujesnės versijos finansinių ataskaitų duomenų srities nustatymas iš naujo

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Finansinių ataskaitų duomenų srities nustatymas iš naujo ataskaitų kūrimo įrankyje

> [!NOTE]
> Šio proceso veiksmai palaikomi „Finance and Operations“ finansinių ataskaitų leidime 7.2.6.0 ir naujesnėse versijose. Jei turite ankstesnį leidimą, kreipkitės pagalbos į palaikymo komandą.

Konkrečiais atvejais gali tekti iš naujo nustatyti finansinių ataskaitų duomenų sritį. Galite atlikti šią užduotį naudodami ataskaitų kūrimo įrankio klientą. Čia pateikti kai kurie atvejai, kai gali teikti iš naujo nustatyti duomenų sritį:

- „Finance and Operations“ duomenų bazė buvo atkurta, tačiau nebuvo atkurta duomenų srities duomenų bazė.
- Matote neteisingus laikotarpio duomenis.
- Palaikymo komanda nurodo nustatyti duomenų sritį iš naujo kaip dalį trikčių šalinimo veiksmo.

Duomenų srities nustatymą iš naujo reikėtų atlikti tik tuo metu, kai duomenų bazėje duomenų apdorojama nedaug. Nustatant iš naujo, finansinės ataskaitų bus nepasiekiamos.

#### <a name="reset-the-data-mart"></a>Duomenų srities nustatymas iš naujo

Norėdami iš naujo nustatyti duomenų sritį, ataskaitos kūrimo priemonės meniu **Įrankiai** pasirinkite **Iš naujo nustatyti duomenų sritį**. Pasirodžiusiame dialogo lange yra dvi dalys: **Statistika** ir **Nustatyti iš naujo**.

[![Dialogo langas Nustatyti duomenų sritį iš naujo](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Integravimo bandymai

Tinklelis **Integravimo bandymai** rodo, kiek kartų sistema bandė integruoti operacijas. Jei keletas pirmų bandymų yra nesėkmingi, keletą dienų sistema toliau bando integruoti duomenis. Žinosite, kad duomenų sritį reikės nustatyti iš naujo, jei bandymų skaičius yra 8 arba daugiau ir jei yra daug dimensijų kombinacijų arba operacijų įrašų. Tokiu atveju duomenys į ataskaitą nebus įtraukiami.

##### <a name="data-status"></a>Duomenų būsena

Tinklelyje **Duomenų būsena** apžvelgiamos operacijos, valiutų kursai ir dimensijų reikšmės duomenų srityje. Daug senų įrašų reiškia, kad įrašai buvo atnaujinti daug kartų. Dėl to ataskaitų generavimas gali sulėtėti.

##### <a name="misaligned-main-account-categories"></a>Nesulygiuotos pagrindinės sąskaitos kategorijos

Jei naudojate leidimą, kuris yra ankstesnis nei „Microsoft Dynamics 365 for Finance and Operations“ finansinių ataskaitų leidimas 7.2.1, gali tekti nustatyti duomenų sritį iš naujo, jei pervardijate sąskaitas ir perkeliate sąskaitas iš vienos kategorijos į kitą. Dėl šių veiksmų pagrindinės sąskaitos kategorijos gali tapti nesulygiuotos. Laukas **Nesulygiuotos pagrindinės sąskaitos kategorijos** rodo, ar susiduriate su ta problema.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>„Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 duomenų srities nustatymas iš naujo

Norėdami nustatyti „Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 duomenų sritį iš naujo, dialogo lange **Nustatyti duomenų sritį iš naujo** pasirinkite žymės langelį **Nustatyti duomenų sritį iš naujo** ir pasirinkite **Gerai**. Iš naujo nustatykite duomenų sritį tik suplanuotos prastovos metu.

[![Žymės langelis Nustatyti duomenų sritį iš naujo](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>„Microsoft Dynamics 365 for Finance and Operations“ finansinių ataskaitų leidimo 7.3.0 duomenų srities nustatymas iš naujo ir priežasties pasirinkimas

Jei nustatote, kad duomenų srities nustatymas iš naujo yra būtinas, pažymėkite žymės langelį **Nustatyti duomenų sritį iš naujo** ir pasirinkite priežastį lauke **Priežastis**. Galimos toliau nurodytos parinktys.

- **Trūksta duomenų arba jie neteisingi**: remdamiesi statistika nustatėte, kad gali trūkti duomenų. Prieš tęsiant, rekomenduojame dirbti su palaikymo tarnyba, kad būtų nustatyta pagrindinė priežastis.
- **Duomenų bazės atkūrimas**: „Finance and Operations“ duomenų bazė buvo atkurta, tačiau nebuvo atkurta finansinių ataskaitų duomenų srities duomenų bazė.
- **Kita**: iš naujo nustatote duomenų sritį dėl kitos priežasties. Jei manote, kad galėjo kilti problema, susisiekite su palaikymo tarnyba, kad problema būtų identifikuota.

[![Iš naujo nustatyti duomenų sritį](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Prieš pradėdami nustatymą iš naujo patikrinkite, ar baigtas visų duomenų srities nustatymo iš naujo užduočių pirminis įkėlimas. Norėdami tai patikrinti, peržiūrėkite reikšmę stulpelyje Paskutinio vykdymo laikas pasirinkdami **Įrankiai** &gt; **Integravimo būsena**.

#### <a name="clear-users-and-companies"></a>Išvalyti vartotojus ir įmones

Pažymėkite žymės langelį **Išvalyti vartotojus ir įmones**, jei atkūrėte duomenų bazę, bet tada atlikote vartotojų ar įmonių keitimų. Pažymėti šį žymės langelį turėtų tekti retai.

Kai būsite pasiruošę pradėti nustatymą iš naujo, pasirinkite **Gerai**. Būsite paraginti patvirtinti, kad esate pasiruošę pradėti procesą. Atkreipkite dėmesį, kad nustatymo iš naujo metu nebus galima pasiekti finansinių ataskaitų ir pradinės duomenų integracijos, kuri atsiranda po to.

Jei norite peržiūrėti integravimo būseną, pasirinkite **Įrankiai** &gt; **Integravimo būsena**, kad pamatytumėte, kada paskutinį kartą buvo vykdoma integracija ir jos būseną.

[![Peržiūrėkite integravimo būseną.](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Nustatymas iš naujo baigtas, kai visų susiejimų būsena yra RanToCompletion ir lango Integravimo būsena apatiniame kairiajame kampe nurodyta Integravimas baigtas.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>„Finance and Operations“ finansinių ataskaitų leidimo 7.0.10000.4 ir naujesnės versijos finansinių ataskaitų duomenų srities nustatymas iš naujo

Jei atkuriate „Finance and Operations“ duomenų bazę iš atsarginės kopijos arba duomenų bazės iš kitos aplinkos, atlikite šiame skyriuje nurodytus veiksmus, kad padėtumėte užtikrinti tinkamą finansinių ataskaitų nustatymo naudojimą atkurtoje „Finance and Operations“ duomenų bazėje.

> [!NOTE]
> Šio proceso veiksmai palaikomi naudojant „Microsoft Dynamics AX“ programos versiją 7.0.1 (2016 m. gegužės mėn.) (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus. Jei naudojate ankstesnę „Finance and Operations“ versiją, pagalbos kreipkitės į palaikymo tarnybą.

### <a name="export-report-definitions"></a>Ataskaitų aprašų eksportavimas

Pirmiausia atlikite šiuos veiksmus, kad eksportuotumėte ataskaitų dizainus iš ataskaitų kūrimo įrankio.

1. Įjungę ataskaitų kūrimo įrankį pasirinkite **Įmonė** &gt; **Kūrimo blokų grupės**.
2. Norėdami eksportuoti, pasirinkite kūrimo blokų grupę, tada spustelėkite **Eksportuoti**.

    > [!NOTE]
    > Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.

3. Pasirinkite norimus eksportuoti ataskaitos aprašus:

    - Norėdami eksportuoti visus ataskaitos aprašus ir susijusius kūrimo blokus, pasirinkite **Žymėti viską**.
    - Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite atitinkamą skirtuką, tada pasirinkite norimus eksportuoti elementus. Norėdami pasirinkti keletą skirtuko elementų, paspauskite ir laikykite klavišą „Ctrl“. Pažymėjus norimas eksportuoti ataskaitas, pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.

4. Pasirinkite **Eksportuoti**.
5. Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitų aprašus.
6. Pasirinkite **Įrašyti**.

Failą galėsite nukopijuoti arba nusiųsti į saugią vietą. Tokiu būdu failas vėliau gali būti importuojamas į kitą aplinką. Informacijos apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, žr. [Duomenų perkėlimas naudojant „AzCopy“ komandų eilučių programą](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Pasirašius „Finance and Operations“ sutartį, „Microsoft“ nesuteikia saugyklos abonemento. Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos.

> [!WARNING]
> Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose (VM). Visam laikui nesaugokite savo eksportuotų kūrimo blokų grupių diske D. Daugiau informacijos apie laikinuosius diskus žr. [Kaip veikia laikinasis diskas „Windows Azure“ virtualiuosiuose kompiuteriuose](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Tarnybų stabdymas

Šios „Microsoft Windows“ tarnybos turės atvirus ryšius su „Finance and Operations“ duomenų baze. Todėl, norėdami prisijungti prie visų aplinkos kompiuterių, turite naudoti „Microsoft“ nuotolinį darbalaukį, tada norėdami sustabdyti toliau nurodytas tarnybas – services.msc.

- Žiniatinklio publikavimo tarnyba (visuose programos objektų serverių (AOS) kompiuteriuose)
- „Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
- „Management Reporter 2012“ proceso tarnyba (tik verslo įžvalgų [BI] kompiuteriuose)

### <a name="reset"></a>Nustatyti iš naujo

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Naujausio MinorVersionDataUpgrade.zip paketo atsisiuntimas

Atsisiųskite naujausią MinorVersionDataUpgrade.zip paketą. Instrukcijas, kaip rasti ir atsisiųsti duomenų naujinimo paketo versija, žr. toliau[Atsisiųskite naujausią duomenų išskleidimo naujinimo paketą](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Norint atsisiųsti MinorVersionDataUpgrade.zip paketą, naujinimas nėra būtinas. Todėl tereikia atlikti veiksmus, nurodytus šios temos skyriuje „Naujausių duomenų naujinimo diegimo paketų atsisiuntimas“. Galite praleisti visus kitus veiksmus šioje temoje.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>„Finance and Operations“ duomenų bazės scenarijų vykdymas

Vykdykite toliau nurodytus „Finance and Operations“ duomenų bazės scenarijus (ne finansinių ataskaitų duomenų bazės):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Naudojant šiuos scenarijus padedama užtikrinti, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo parametrai.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Paleiskite „Windows PowerShell“ komandą, kad iš naujo nustatytumėte duomenų bazę

AOS kompiuteryje paleiskite „Microsoft PowerShell“ administratoriaus teisėmis ir vykdykite toliau nurodytas komandas, kad iš naujo nustatytumėte „Finance and Operations“ ir finansinių ataskaitų integravimą.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Čia pateikiamas komandos **Reset-DatamartIntegration** parametrų paaiškinimas:

- Tinkamos **-Reason** reikšmes yra **SERVICING**, **BADDATA** ir **OTHER**.
- Parametras **-ReasonDetail** yra laisvos formos.
- „Reason“ ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.

> [!NOTE]
> Įvykdę komandas, būsite paprašyti įvesti **Y**, kad patvirtintumėte, jog norite iš naujo nustatyti duomenų bazę.

#### <a name="restart-services"></a>Tarnybų paleidimas iš naujo

Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:

- Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)
- „Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)
- „Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)

#### <a name="import-report-definitions"></a>Ataskaitų aprašų importavimas

Importuokite savo ataskaitos dizainus iš ataskaitų kūrimo įrankio naudodami eksportuojant sukurtą failą.

1. Įjungę ataskaitų kūrimo įrankį pasirinkite **Įmonė** &gt; **Kūrimo blokų grupės**.
2. Norėdami eksportuoti, pasirinkite kūrimo blokų grupę, tada spustelėkite **Eksportuoti**.

    > [!NOTE]
    > Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.

3. Pasirinkite kūrimo bloką **Numatytasis**, tada pasirinkite **Importuoti**.
4. Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, tada pasirinkite **Atidaryti**.
5. Dialogo lange **Importuoti** pasirinkite importuotinus ataskaitos aprašus:

    - Norėdami importuoti visus ataskaitos aprašus ir susijusius kūrimo blokus, pasirinkite **Žymėti viską**.
    - Norėdami importuoti tam tikras ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius pasirinkite importuotinas ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

6. Pasirinkite **Importuoti**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>„Finance and Operations“ (vietinės versijos) finansinių ataskaitų duomenų srities nustatymas iš naujo

1. Nurodykite visiems vartotojams išeiti iš ataskaitų kūrimo įrankio ir „Finance and Operations“ finansinių ataskaitų srities.
2. Vykdykite toliau nurodytą finansinių ataskaitų duomenų bazės (MRDB) scenarijų.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Sutrumpinkite arba panaikinkite visus įrašus iš lentelės FINANCIALREPORTS „Finance and Operations“ duomenų bazėje (AXDB).
4. Sutrumpinkite arba panaikinkite visus įrašus iš lentelės FINANCIALREPORTVERSION, jei ši lentelė yra „Finance and Operations“ duomenų bazėje. Jei lentelės nėra „Finance and Operations“ duomenų bazėje, praleiskite šį veiksmą.
5. Vykdykite finansinių ataskaitų duomenų bazės scenarijų **ResetDatamart.sql**. Šis scenarijus išjungia duomenų srities integravimą, panaikina visus duomenų srities duomenis, tada iš naujo įgalina duomenų srities integravimą.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Nustačius iš naujo, galite neautomatiniu būdu patikrinti duomenis, paleisdami toliau nurodytą finansinių ataskaitų duomenų bazės užklausą.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Užtikrinkite, kad visose eilutėse yra **LastRunTime** reikšmė ir kad **StateType** nustatyta kaip **5**. **StateType** reikšmė **5** nurodo, kad duomenys buvo sėkmingai įkelti iš naujo. Reikšmė **7** nurodo triktį. Kartais organizacijos hierarchijos schema yra šios būsenos, kai ji vykdoma pirmą kartą. Tačiau trikties būsena turėtų būti pašalinta automatiškai.

