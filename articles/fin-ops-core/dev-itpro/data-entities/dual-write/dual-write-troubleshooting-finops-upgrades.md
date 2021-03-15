---
title: „Finance and Operations“ programų plėtočių problemų sprendimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131226"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>„Finance and Operations“ programų plėtočių problemų sprendimas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su „Finance and Operations” programų naujinimais.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="database-synchronization-errors"></a>Duomenų bazės sinchronizavimo klaidos

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai bandote naudoti **„DualWriteProjectConfiguration”** lentelę, kad atnaujintumėte „Finance and Operations” programą į „Platform Update 30“, galite gauti klaidos pranešimą, panašų į šį pavyzdį.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.
2. Atidarykite  „Visual Studio” kaip administratorius, taip pat atidarykite programos objektų medį (AOT).
3. Ieškoti **DualWriteProjectConfiguration**.
4. Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite **DualWriteProjectConfiguration** ir pasirinkite **Įtraukti į naują projektą**. Pasirinkite **Gerai**, kad sukurtumėte naują projektą, kuriame naudojamos numatytosios parinktys.
5. Sprendimų naršyklėje dešiniuoju pelės klavišu spustelėkite **Projekto ypatybės** ir nustatykite **Kuriant sinchronizuoti duomenų bazę** kaip **Teisinga**.
6. Sukurkite projektą ir patvirtinkite, kad sėkmingai pavyko sukurti.
7. **„Dynamics 365”** meniu pasirinkite **Sinchronizuoti duomenų bazę**.
8. Norėdami sinchronizuoti visą duomenų bazę, pasirinkite **Sinchronizuoti**.
9. Sėkmingai atlikę visos duomenų bazės sinchronizavimą, iš naujo įvykdykite duomenų bazės sinchronizavimo veiksmą „Microsoft Dynamics Lifecycle Services (LCS)” portale ir, jei taikytina, naudokite neautomatizuoto naujinimo scenarijus, kad galėtumėte tęsti naujinimą.

## <a name="missing-table-columns-issue-on-maps"></a>Trūksta lentelės stulpelių schemose

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

**Dvigubo rašymo** funkcijos puslapyje galite gauti klaidos pranešimų, panašių į toliau pateiktą pavyzdį:

*Trūksta šaltinio lauko \<field name\> schemoje.*

![Trūkstamo šaltinio stulpelio klaidos pranešimo pavyzdys](media/error_missing_field.png)

Norėdami išspręsti problemą, pirmiausia atlikite šiuos veiksmus, kad įsitikintumėte, kad stulpeliai yra lentelėje.

1. Prisijunkite prie „Finance and Operations” programos VM.
2. Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite plytelę **Sistemos parametrai**, tada skirtuke **Lentelės parametrai** pasirinkite **Atnaujinti lentelių sąrašą** tam, kad atnaujintumėte lenteles.
3. Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite skirtuką **Duomenų lentelės** ir įsitikinkite, kad lentelė yra sąraše. Jei lentelės nėra sąraše, prisijunkite prie „Finance and Operations” programos VM ir įsitikinkite, kad lentelė yra pasiekiama.
4. Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su lentele**.
5. Pasirinkite **Atnaujinti lentelių sąrašą** tam, kad susiejimų su lentele stulpeliai būtų užpildyti automatiškai.

Jei problema išlieka, atlikite šiuos veiksmus.

> [!IMPORTANT]
> Šie veiksmai padės jums pašalinti lentelę ir vėl ją pridėti. Norėdami išvengti problemų, tiksliai atlikite nurodytus veiksmus.

1. „Finance and Operations” programoje eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Duomenų lentelės**.
2. Raskite lentelę, kuriai trūksta atributo. Įrankių juostoje spustelėkite **Modifikuoti paskirties vietos susiejimą**.
3. Srityje **Susieti išdėstymą su paskirties vieta** spustelėkite **Generuoti susiejimą**.
4. Eikite į „Finance and Operations” programos **dvigubo rašymo puslapį** ir atidarykite puslapį **Susiejimas su lentele**.
5. Jei atributas nėra automatiškai užpildomas schemoje, įtraukite jį neautomatiniu būdu spustelėdami mygtuką **Įtraukti atributą**, o tada – **Įrašyti**. 
6. Pasirinkite schemą ir spustelėkite **Vykdyti**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]