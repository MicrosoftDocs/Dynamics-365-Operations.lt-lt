---
title: Tiesioginio sinchronizavimo trikčių šalinimas
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginį sinchronizavimą.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9d27331b940a95168810c2f1ec4ae240a9df93a8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896711"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Tiesioginio sinchronizavimo trikčių šalinimas

[!include [banner](../../includes/banner.md)]



Šiame straipsnyje pateikiama trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Microsoft Dataverse. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.

> [!IMPORTANT]
> Kai kurioms šio straipsnio adresams gali reikėti sistemos administratoriaus Azure Active Directory vaidmens arba () nuomininkų Azure AD administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia specifinio vaidmens ar kredencialų.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Tiesioginis sinchronizavimas rodo klaidą, kai kuriate eilutę

Kurdami eilutę finansų ir operacijų programoje galite gauti toliau nurodytą klaidos pranešimą:

*\[{\\"klaida\\":{\\"kodas\\":\\"0x80072560\\",\\"pranešimas\\":\\"Vartotojas nėra organizacijos narys.\\"}}\], Nuotolinis serveris pateikė klaidą: (403) draudžiama."}}".*

Norėdami išspręsti problemą, atlikite veiksmus, pateiktus skyriuje [Sistemos reikalavimai ir būtinosios sąlygos](requirements-and-prerequisites.md). Norėdami atlikti šiuos veiksmus, dvigubo rašymo programos vartotojai buvo sukurti „Dataverse”, privalo turėti sistemos administratoriaus vaidmenį. Numatytoji komanda savininkė taip pat turi turėti sistemos administratoriaus vaidmenį.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Tiesioginis sinchronizavimas rodo klaidą, kai bandote įrašyti lentelės duomenis

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai bandysite įrašyti lentelės duomenis finansų ir operacijų programoje, galite gauti toliau nurodytą klaidos pranešimą:

*Nepavyksta įrašyti duomenų bazės pakeitimų. Darbo vienetas negali įvykdyti operacijos. Nepavyksta įrašyti duomenų į objekto uoms. Įrašyti į UnitOfMeasureEntity nepavyko, nes nepavyko sinchronizuoti klaidos pranešimo su objekto uoms.*

Norėdami išspręsti problemą, įsitikinkite, kad yra būtinųjų komponentų nuorodos duomenų ir finansų ir operacijų programoje, ir programoje Dataverse. Pavyzdžiui, jei kliento įrašas, kuriame esate programoje, priklauso konkrečiai klientų grupei, įsitikinkite, kad ši klientų įrašų grupė yra „Dataverse“.

Jei duomenys yra abiejose programose ir patvirtinote, kad problema nėra susijusi su duomenimis, atlikite šiuos veiksmus.

1. Atidarykite objektą **DualWriteProjectConfigurationEntity** naudodami „Excel“ papildinį. Norėdami naudoti papildinį, įgalinkite kūrimo režimą finansų ir operacijų "Excel" papildinį ir **pridėkite DualWriteProjectConfigurationEntity** į darbalapį. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
2. Pasirinkti ir naikinti įrašus, kurie turi dvigubo rašymo schemos ir projekto problemų. Kiekvienam dvigubo rašymo susiejimui bus skirti du įrašai.
3. Publikuokite keitimus naudodami „Excel" papildinį. Šis veiksmas svarbus, nes jis panaikina įrašus iš objekto ir po juo esančių lentelių.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Tvarkyti skaitymo arba rašymo teisių klaidas kuriant duomenis finansų ir operacijų programoje

Kai kuriate duomenis finansų ir operacijų programoje, galite gauti klaidos pranešimą "Bloga užklausa".

![Klaidos pranešimo „Netinkama užklausa“ pavyzdys.](media/error_record_id_source.png)

Norėdami išspręsti šią problemą, turite įjungti misijos teises priskirdami tinkamą saugos vaidmenį susieto „Dynamics 365 Sales” arba „Dynamics 365 Customer Service” verslo struktūros vieneto komandai, kad įgalintumėte trūkstamą teisę.

1. Finansų ir operacijų programoje raskite verslo vienetą, kuris susietas duomenų integravimo ryšių rinkinys.

    ![Organizacijos susiejimas.](media/mapped_business_unit.png)

2. Prisijunkite prie aplinkos „Customer Engagement” programoje, prisijunkite prie aplinkos ir eikite į **Parametrai \> Sauga** ir raskite susieto verslo struktūros vieneto komandą.

    ![Susieto verslo struktūros vieneto komanda.](media/setting_security_page.png)

3. Atidarykite komandos puslapį, kad ją būtų galima redaguoti, tada pasirinkite **Tvarkyti vaidmenis**.

    ![Vaidmenų tvarkymo mygtukas.](media/manage_team_roles.png)

4. Teksto lauke **Tvarkyti komandos vaidmenis** priskirkite vaidmenį, turintį skaitymo / rašymo teisę, skirtą atitinkamoms lentelėms, tada pasirinkite **Gerai**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Sinchronizavimo problemų aplinkoje, kurioje neseniai buvo pakeista „Dataverse” aplinka, sprendimas

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai kuriate duomenis finansų ir operacijų programoje, galite gauti toliau nurodytą klaidos pranešimą:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nepavyksta sugeneruoti mokamosios krovos objektui CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Nepavyko sukurti mokamosios krovos, įvyko klaida „Netinkamas URI“: URI yra tuščias."}\],"isErrorCountUpdated":true}*

Štai kaip atrodo klaidos pranešimas „Customer Engagement” programoje:

> Įvyko netikėta klaida iš ISV kodo. Įvyko netikėta ISV kodo klaida. (ErrorType = ClientError) Netikėta priedo išimtis (vykdyti): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: nepavyko apdoroti objekto sąskaitos – nepavyko užmegzti ryšio, nes šalis, prie kurios buvo jungiamasi, tinkamai neatsakė praėjus tam tikram laiko tarpui, arba užmegztas ryšys nutruko, nes prijungtas pagrindinis kompiuteris neatsakė.

Ši klaida įvyksta, jei Dataverse bandant sukurti duomenis finansų ir operacijų programoje aplinka yra netinkamai nustatytas iš naujo.

> [!IMPORTANT]
> Jei susiesite aplinkas, turite sustabdyti visas objekto schemas ir tada tęsti mažinimo veiksmus.

Norėdami išspręsti problemą, turite atlikti veiksmus ir finansų, Dataverse ir operacijų programoje.

1. Finansų ir operacijų programoje atlikite šiuos veiksmus:

    1. Atidarykite objektą **DualWriteProjectConfigurationEntity** naudodami „Excel“ papildinį. Norėdami naudoti papildinį, įgalinkite kūrimo režimą finansų ir operacijų "Excel" papildinį ir **pridėkite DualWriteProjectConfigurationEntity** į darbalapį. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
    2. Pasirinkti ir naikinti įrašus, kurie turi dvigubo rašymo schemos ir projekto problemų. Kiekvienam dvigubo rašymo susiejimui bus skirti du įrašai.
    3. Publikuokite keitimus naudodami „Excel" papildinį. Šis veiksmas svarbus, nes jis panaikina įrašus iš objekto ir po juo esančių lentelių.
    4. Norėdami išvengti klaidų atsiedami finansus ir Dataverse operacijas ar aplinkas, įsitikinkite, kad nelieka dvigubo rašymo konfigūracijų.

2. „Dataverse“, atlikite šiuos veiksmus:

    1. Prisijunkite prie savo aplinkos „Dataverse“ (pavyzdžiui, `https://*****.crm.dynamics.com/`).
    2. Eiti į **išplėstinių parametrų** \> **išplėstinę iešką**.
    3. Pasirinkite **Dvigubowrite vykdyklės konfigūraciją**.
    4. Pasirinkite stulpelį, kurį norite peržiūrėti.
    5. Norėdami **peržiūrėti** konfigūracijas, pasirinkite Rezultatai.
    6. Naikinti visus egzempliorius.

3. Finansų ir operacijų programoje atlikite šiuos veiksmus:

    1. Atidarykite objektą **DualWriteProjectConfigurationEntity** naudodami „Excel“ papildinį. Norėdami naudoti papildinį, įgalinkite kūrimo režimą finansų ir operacijų "Excel" papildinį ir **pridėkite DualWriteProjectConfigurationEntity** į darbalapį. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
    2. Pasirinkti ir naikinti įrašus, kurie turi dvigubo rašymo schemos ir projekto problemų. Kiekvienam dvigubo rašymo susiejimui bus skirti du įrašai.
    3. Publikuokite keitimus naudodami „Excel" papildinį. Šis veiksmas svarbus, nes jis panaikina įrašus iš objekto ir po juo esančių lentelių.
    4. Norėdami išvengti klaidų atsiedami finansus ir Dataverse operacijas ar aplinkas, įsitikinkite, kad nelieka dvigubo rašymo konfigūracijų.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Tiesioginio sinchronizavimo klaida atlikus visą duomenų bazės kopiją

Jums gali būti rodomas šis klaidos pranešimas, kai paleidžiate visą duomenų bazės kopiją iš vienos sistemos į kitą ir bandote paleisti duomenų bazės operaciją:

*SecureConfig organizacija (???) neatitinka faktinės CRM organizacijos (???).*

Klaidos pranešimas yra rodomas dvigubo rašymo vykdyklės priede, siekiant užtikrinti, kad vienoje sistemoje nustatytos dvigubo rašymo konfigūracijos negalima naudoti kitoje sistemoje.

Norėdami išspręsti problemą, atkurę duomenų bazę panaikinkite visus **msdyn_dualwriteruntimeconfig** įrašus. Norėdami gauti daugiau informacijos, [atsiekite ir pereikite dvigubo rašymo aplinkas](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Tiesioginio sinchronizavimo problemos, kurias lemia neteisinga užklausų filtro sintaksė dvigubo rašymo schemose

Net jei dvigubo rašymo schemos filtro užklausos išraiška yra tinkama, gali neveikti kaip tikėtasi. Filtro išraiška yra objekte, o ne individualaus užklausos objekto duomenų šaltinyje. Todėl sugeneruota SQL užklausa negrąžina numatomų rezultatų.

Toliau pateikiamas pavyzdys.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Galite tikėtis, kad projektai, kuriuose nėra pirminio objekto, būtų filtruojami. Tačiau filtras neveikia, nes jis išverstas į užklausą, panašią į pateiktą pavyzdį.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Faktinis rezultatas yra `parentProject` toks, kaip laukas vertinamas `null`. Tačiau, `null` nėra tas pats, kas tuščia eilutė. Dėl šio neatitikimo, užklausos filtras negrąžina galiojančių rezultatų.

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Įtraukti apskaičiuoto stulpelio, kurį galima pridėti prie plėtinio modelio ir kuris yra atsarginis logikos, konvertuojančio į `null` tuščią eilutę, dalis.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Vietoj numatytojo stulpelio naudoti filtrą naujame apskaičiuotame stulpelyje.

Norėdami įvertinti filtrą programavimo aplinkoje, rezultatams patikrinti galite naudoti nurodytą X++ kodą. Vykdyti šį kodą kaip atskirą programą. Galite naudoti jį norėdami įvertinti skirtingas filtrus, taikomus objektui, prieš naudodami šiuos filtrus dvigubo rašymo schemose. Norint įvertinti nesutapimų, užklausą galima vykdyti naudojant duomenų bazę.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Duomenys iš finansų ir operacijų programėlių nesinchronizuoti su Dataverse

Sinchronizuojant tiesiogiai, gali kilti problema, Dataverse kuri leidžia sinchronizuoti tik dalį duomenų iš finansų ir operacijų programėlių arba duomenys nesinchronizuojami iš viso.

> [!NOTE]
> Programavimo metu turite išspręsti šią problemą.

Prieš pradėdami spręsti problemą, peržiūrėkite šiuos būtinuosius komponentus:

+ Įsitikinkite, kad pasirinktiniai pakeitimai įrašyti į vieną operacijos aprėptį.
+ Verslo įvykiai ir dvigubo rašymo sistema nesutvarkyti, `doinsert()`, `doUpdate()` ir operacijos ar `recordset()` įrašai, kur jie `skipBusinessEvents(true)` pažymėti. Jei jūsų kodas yra šiose funkcijose, dvigubo rašymo funkcija nebus suaktyvinta.
+ Reikia užregistruoti duomenų šaltinio, kuris susietas, verslo įvykius. Kai kurie duomenų šaltiniai gali naudoti išorinę jungtį, jie gali būti pažymėti kaip skaitomi finansų ir operacijų programėlėse. Šie duomenų šaltiniai nėra sekami.
+ Pakeitimai bus suaktyvinti tik tada, jei modifikacijos bus susietose laukuose. Nesusietų laukų modifikacijos neįjungs dvigubo rašymo.
+ Įsitikinkite, kad filtrų vertinimai pateikia tinkamą rezultatą.

### <a name="troubleshooting-steps"></a>Trikčių šalinimo veiksmai

1. Peržiūrėkite laukų susiejimus dvigubo rašymo administratoriaus puslapyje. Jei laukas nėra susietas su finansų ir operacijų programėle Dataverse, jis nebus sekamas. Pavyzdžiui, pagal šį pavyzdį aprašymo laukas **sekamas** iš Dataverse, o ne iš finansų ir operacijų programėlių. Nebus sekami jokie finansų ir operacijų programėlių lauko pakeitimai.

    ![Sekamas laukas.](media/live-sync-troubleshooting-1.png)

2. Nustatykite, ar duomenų šaltinis sekamas verslo įvykių apibrėžime. Pavyzdžiui, pagal šį pavyzdį nebus sekamas joks lentelės **DefaultDimensionDAVs** ir po jos esančių lentelių laukas, kad būtų galima atlikti keitimus. Duomenų šaltiniai, kurie naudoja išorinę jungtį ir yra pažymėti kaip tik skaitomi, nėra sekami.

    ![Laukas, kuris nėra sekamas.](media/live-sync-troubleshooting-2.png)

3. Nustatykite, ar lentelėje **BUSINESSEVENTSDEFINITION** pasirodys susieti lentelės laukai, kaip parodyta toliau pateiktame pavyzdyje. Jei nerandate lauko, kurio ieškote užklausos rezultate, jis nebus suaktyvintas dvigubo rašymo.

    ![Sekamas lentelės laukas.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Pavyzdinis scenarijus

Finansų ir operacijų programėlėse yra kontakto įrašo adreso naujinimas, bet adreso pakeitimas nesinchronizuotas Dataverse su. Šis scenarijus įvyksta todėl, kad lentelėje **BusinessEventsDefinition** nėra įrašo, paveiktos lentelės ir objekto derinio. Tiksliau tariant, lentelė **LogisticsPostalAddress** nėra tiesioginis **smmContactpersonCDSV2Entity** objekto duomenų šaltinis. **smmContactpersonCDSV2Entity** objekto duomenų šaltinis yra **smmContactPersonV2Entity** kaip duomenų šaltinis **smmContactPersonV2Entity** savo ruožtu kaip duomenų šaltinis yra **LogisticsPostalAddressBaseEntity**. Lentelė **LogisticsPostalAddress** yra **LogisticsPostalAddressBaseEntity** duomenų šaltinis.

Panaši situacija gali įvykti ir kai kuriuose nestandartuose šablonuose, pvz., atvejus, kai finansų ir operacijų programėlėse modifikuojamas lentelė nėra susieta su objektu, kuriame ji yra. Pvz., pirminio adreso duomenys apskaičiuoti objekto **smmContactPersonCDSV2Entity** dalyje. Dvigubo rašymo sistema bando nustatyti, kaip pateiktoje lentelėje pakeitimas susietas su objektais. Paprastai šis būdas pakanka. Tačiau kai kuriais atvejais saitas toks sudėtingas, kad jūs turite būti konkretus. Turite užtikrinti, kad susijusios lentelės **RecId** tiesiogiai pasiekiamas objektui. Tada įtraukite statinį metodą lentelės pokyčiams stebėti.

Pavyzdžiui, peržiūrėkite **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** metodą. **CustCustomerV3entity** ir **VendVendorV2Entity** buvo modifikuota apdoroti šią situaciją.

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Įtraukti **PrimaryPostalAddressRecId** lauką į objektą **smmContactPersonV2Entity**. Padaryti vidinį.

    ![Laukas įtrauktas į objektą smmContactPersonV2Entity entity.](media/Troubleshoot_live_sync_issue_1.png)

2. Įtraukite tą patį laukelį į **smmContactPersonCDSV2Entity** objektą.

    ![Laukas įtrauktas į objektą smmContactPersonCDSV2Entity entity.](media/Troubleshoot_live_sync_issue_2.png)

3. Įtraukite šį metodą į **smmContactPersonCDSV2Entity** klasę.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Sinchronizuokite duomenų bazę ir sukurkite programą.
5. Sustabdykite visas dvigubo rašymo schemas, sukurtas **smmContactPersonCDSV2Entity** objektui.
6. Paleisti schemą. Šiame pavyzdyje turėtumėte matyti naują lentelę (**LogisticsPostalAddress** šiame pavyzdyje) kurią pradėjote sekti naudodami eilutės, kurios **RefTableName** stulpelis eilutei, kurioje **refentityname** vertės lygios **smmContactPersonCDSV2Entity** lentelėje **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Kuriant įrašą, kuriame iš finansų ir operacijų programos į tą patį paketą siunčiami keli Dataverse įrašai, įvyko klaida

Finansų ir operacijų programa sukuria bet kurios operacijos duomenis pakete ir siunčia juos kaip paketą Dataverse. Jei du įrašai sukuriami kaip tos pačios operacijos dalis ir jie nurodo vienas kitą, finansų ir operacijų programoje galite gauti klaidos pranešimą, kuris yra panašus į toliau pateiktą pavyzdį:

*Nepavyko įrašyti duomenų į objekto aaa_fundingsources. Nepavyko peržiūrėti duomenų ebecsfs_contracts {PC00...} reikšmių. Nepavyko peržiūrėti duomenų aaa_fundingsources {PC00...} reikšmių. Nepavyko įrašyti aaa_fundingsources klaidos pranešimas Išimtis: nuotolinis serveris pateikė klaidą: (400) Netinkama užklausa.*

Norėdami išspręsti problemą, sukurkite objektų ryšius finansų ir operacijų programoje ir nurodykite, kad du objektai yra susiję vienas su kitu ir susiję įrašai yra tvarkomi toje pačioje operacijoje.

## <a name="enable-verbose-logging-of-error-messages"></a>Įgalinti klaidų pranešimų daugiažodį registravimą

Finansų ir operacijų programoje galite susidurti su klaidomis, susijusiomis su Dataverse aplinka. Klaidos pranešime gali būti ne visas pranešimo tekstas ar kiti susiję duomenys. Norėdami gauti daugiau informacijos, galite įgalinti daugiažodį registravimą, nustatydami vėliavėlę IsDebugMode, **kuri yra įraše DualWriteProjectConfigurationEntity** visose finansų ir operacijų programėlių projektų **konfigūracijose**.

1. Atidarykite objektą **DualWriteProjectConfigurationEntity** naudodami „Excel“ papildinį. Norėdami naudoti papildinį, įgalinkite kūrimo režimą finansų ir operacijų "Excel" papildinį ir **pridėkite DualWriteProjectConfigurationEntity** į darbalapį. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
2. Nustatykite projekto vėliavą **IsDebugMode** kaip **Taip**.
3. Scenarijaus vykdymas.
4. Daugiažodžiai žurnalai pasiekiami lentelėje **DualWriteErrorLog**. Norėdami peržiūrėti duomenis naudodami lentelių naršyklę, naudokite šį URL: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Norėdami fiksuoti daugiau žurnalų derinimo režimu, įdiekite naujinimą [KB 4595434 (Taisyti už tuščias vertes, kurios platinamos dvigubo rašymo tiesioginio sinchronizavimo)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Klaida, kai pridedate kliento arba kontakto adresą

Kai bandysite įtraukti kliento arba kontakto adresą į finansų ir operacijų programėles, galite gauti toliau nurodytą klaidos pranešimą, arba Dataverse:

*Nepavyko įrašyti duomenų į objekto msdyn_partypostaladdresses. DirPartyPostalAddressLocationCDSEntity nepavyko, nes nepavyko pateikti klaidos pranešimo užklausos, kurios būsenos kodas BadRequest ir CDS, klaidos kodas: 0x80040265 atsakymo pranešimas: "be" įvyko klaida. Įrašas, kuriame yra atributų verčių vietos ID, jau yra. Objekto rakto vietos ID raktas reikalauja, kad šiame atributų rinkinį būtų unikalios vertės. Pasirinkite unikalias vertes ir bandykite dar kartą.*

Norėdami išspręsti problemą, įdiekite dvigubo rašymo instrumento paketo (2.2.2.60), kad adresų lentelėje esantys raktai būtų nurodyti kaip **parodyta** šioje lentelėje.

| Ypatybė | Reikšmė |
|---|---|
| Rodyti pavadinimą | **Vietos raktas** |
| Pavadinimas / vardas ir (arba) pavardė | **msdyn_locationkey** |
| Laukai | **msdyn_locationid**, **parentid** |
| Būsena | **Aktyvusis** |
| Sistemos užduotis | Tuščias |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Klaida, kai įtraukiate klientą į „Dataverse“

Kai „Dataverse” programoje kuriate duomenis, bando įtraukti klientą gauti tokį klaidos pranešimą:

*"RecordError0":"Rašyti nepavyko objekto klientams V3 su nežinoma išimtimi – įrašo, kurio tipas Organizacija, nerasta"}.*

Kai klientas „Dataverse“ sukuriamas, sugeneruojamas naujas šalies numeris. Klaidos pranešimas rodomas, kai kliento įrašas (kartu su įrašu) sinchronizuojamas su finansų ir operacijų programėle, tačiau jau yra kliento įrašas, kuriame nurodytas kitas šalies numeris.

Norėdami išspręsti problemą, suraskite klientą per šalių peržvalgą. Klientui sukurkite kliento įrašą, jei jo nėra. Jei kliento nėra, naudokite esamą šalį, kad sukurtumėte naują kliento įrašą.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Kuriant naują klientą, tiekėją arba kontaktą formoje „Dataverse“

Kai mėginsite įtraukti kliento arba kontakto adresą į programėle norėdami sukurti naują klientą, tiekėją ar kontaktą „Dataverse“:

*Negalima atnaujinti įrašo tipo nuo „DirOrganization" iki „DirPerson", todėl reikia panaikinti esamą šalį ir įterpti su nauju tipu.*

Lentelėje „Dataverse“ yra numerių seka **msdyn_party** numeracija. Kai sąskaita sukuriama, sukuriama „Dataverse“ nauja šalis (pvz., organizacijos tipo **šalis-001**, kuri yra tipe **Organizacija**). Šie duomenys siunčiami į finansų ir operacijų programą. Dataverse Jei aplinka yra iš naujo sukurta arba finansų ir operacijų aplinka susieta su kita aplinka, Dataverse tada sukuriamas naujas kontakto įrašas, Dataverse kuriama nauja įrašo vertė, **kuri prasideda Party-001**. Šį kartą sukurtas šalies įrašas bus asmens tipo įrašas **Šalis-001** tipo **Asmens**. Kai šie duomenys sinchronizuojami, finansų ir operacijų programėlės rodo ankstesnį klaidos pranešimą, **nes organizacijos tipo šalies įrašas 001** **jau** yra.

Norėdami išspręsti problemą, pakeiskite automatinę lentelės **msdyn_partynumber** laukelis **msdyn_party** lentelė „Dataverse“ į skirtingą automatinio numerio seką.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Efektyvumo problema su klientų arba kontaktų susiejimais

Gali būti, kad galite šiek tiek padidinti klientų ir kontaktų tiesioginio sinchronizavimo našumą pritaikant **getEntityDataSourceToFieldMapping** metodas (objektas **CustCustomerV3Entity**) metodas ir **getEntityDataSourceToFieldMapping** metodas (**smmContactPersonCDSV2Entity** objektas). Šie tinkinimai sumažina lentelės **BusinessEventsDefinition** įrašų skaičių. Savo ruožtu dėl šio įrašų skaičiaus sumažinimas sumažina pakeltų įvykių skaičių.

Metodas **GetEntityDataSourceToFieldMapping metodas** objektas **custCustomerV3Entity** užtikrina, kad kliento elektroninio adreso arba pašto adreso naujinimas suaktyvina verslo įvykius, todėl atnaujinti duomenys bus „Dataverse“ siunčiami. Jei nenaudokite visų laukų ir nereikia informacijos dvigubo rašymo metu, aprašykite atitinkamas metodo eilutes. Kiekvienas sekamas laukas ir lentelė, įtraukti į šį metodą, prideda įrašą lentelėje **BusinessEventsDefinition** skirta sekamos lentelės ir sekamos objekto kombinacijai.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Panašiu būdu, **GetEntityDataSourceToFieldMapping metodas** objektas **smmContactPersonCDSV2Entity** užtikrina, kad kliento elektroninio adreso arba pašto adreso naujinimas suaktyvina verslo įvykius, todėl atnaujinti duomenys bus „Dataverse“ siunčiami. Šiame metode galite pakomentuoti visų norimų naudoti laukų eilutes.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Atnaujinę metodus, atlikite šiuos veiksmus.

1. Sinchronizuokite duomenų bazę ir sukurkite programą.
2. Sustabdykite visas dvigubo rašymo schemas, sukurtas **smmContactPersonCDSV2Entity** ir **CustCustomerV3Entity** objektai.
3. Paleisti žemėlapius. Turėtumėte matyti mažiau įrašų **smmContactPersonCDSV2Entity** ir **CustCustomerV3Entity** objektuose ir lentelėje **BusinessEventsDefinition**, o našumas gali šiek tiek pagerinti.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
