---
title: Finansų ir operacijų programų versijos naujinimų trikčių šalinimas
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, kuri gali padėti išspręsti problemas, susijusias su finansų ir operacijų programėlių atnaujinimais.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7ab75c3a7b6c53982a32658f376a9fd148c023e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289551"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finansų ir operacijų programų versijos naujinimų trikčių šalinimas

[!include [banner](../../includes/banner.md)]





Šiame straipsnyje pateikiama trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse. Taigi, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su finansų ir operacijų programėlių atnaujinimu.

> [!IMPORTANT]
> Kai kurioms šio straipsnio adresams gali reikėti sistemos administratoriaus vaidmens arba "Microsoft Azure Active Directory " () nuomininkų Azure AD administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="database-synchronization-errors"></a>Duomenų bazės sinchronizavimo klaidos

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai mėginsite **naudoti lentelę DualWriteProjectConfiguration**, norėdami atnaujinti finansų ir operacijų programą į platformos naujinimą 30, galite gauti klaidos pranešimą, panašią į šį pavyzdį.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisiregistruokite prie virtualiosios mašinos (VM) finansų ir operacijų programai.
2. Atidarykite „Visual Studio” kaip administratorius, taip pat atidarykite programos objektų medį (AOT).
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

![Trūkstamo šaltinio stulpelio klaidos pranešimo pavyzdys.](media/error_missing_field.png)

Norėdami išspręsti problemą, pirmiausia atlikite šiuos veiksmus, kad įsitikintumėte, kad stulpeliai yra lentelėje.

1. Prisiregistruokite prie finansų ir operacijų programos VM.
2. Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite plytelę **Sistemos parametrai**, tada skirtuke **Lentelės parametrai** pasirinkite **Atnaujinti lentelių sąrašą** tam, kad atnaujintumėte lenteles.
3. Eikite į **Darbo sritys \> Duomenų valdymas**, pasirinkite skirtuką **Duomenų lentelės** ir įsitikinkite, kad lentelė yra sąraše. Jei lentelės nėra, prisiregistruokite prie finansų ir operacijų programos VM ir įsitikinkite, kad lentelė yra pasiekiama.
4. Atidarykite **lentelės susiejimo** puslapį dvigubo **rašymo** puslapyje, finansų ir operacijų programoje.
5. Pasirinkite **Atnaujinti lentelių sąrašą** tam, kad susiejimų su lentele stulpeliai būtų užpildyti automatiškai.

Jei problema išlieka, atlikite šiuos veiksmus.

> [!IMPORTANT]
> Šie veiksmai padės jums pašalinti lentelę ir vėl ją pridėti. Norėdami išvengti problemų, tiksliai atlikite nurodytus veiksmus.

1. Finansų ir operacijų programoje eikite į Darbo **sričių duomenų \> valdymą** ir pasirinkite duomenų lentelių **išklotinę** lentelę.
2. Raskite lentelę, kuriai trūksta atributo. Įrankių juostoje spustelėkite **Modifikuoti paskirties vietos susiejimą**.
3. Srityje **Susieti išdėstymą su paskirties vieta** spustelėkite **Generuoti susiejimą**.
4. Atidarykite **lentelės susiejimo** puslapį dvigubo **rašymo** puslapyje, finansų ir operacijų programoje.
5. Jei atributas nėra automatiškai užpildomas schemoje, įtraukite jį neautomatiniu būdu spustelėdami mygtuką **Įtraukti atributą**, o tada – **Įrašyti**. 
6. Pasirinkite schemą ir spustelėkite **Vykdyti**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
