---
title: Banko išrašo failo importavimo trikčių šalinimas
description: Šiame straipsnyje paaiškinama, kaip spręsti problemas, kurias lemia maži banko išrašo failo skirtumai.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151767"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Banko išrašo failo importavimo trikčių šalinimas

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Ši funkcija bus pasenusi 2022 m. rugsėjo mėn., nauji vartotojai turės naudoti elektronines ataskaitas.

Svarbu, kad banko išrašo failas atitiktų maketą, kurį palaiko Microsoft Dynamics 365 finansai. Dėl griežtų banko išrašų standartų, dauguma integravimų veiks tinkamai. Tačiau kartais išrašo failo nepavyksta importuoti arba rezultatai yra neteisingi. Paprastai šios problemos kyla dėl mažų skirtumų banko išrašo faile. Šiame straipsnyje paaiškinama, kaip pašalinti šiuos skirtumus ir išspręsti problemas.

## <a name="what-is-the-error"></a>Kokia klaida?

Pabandę importuoti banko išrašo failą, atidarykite užduoties Duomenų valdymas retrospektyvą ir jos vykdymo informaciją, kad rastumėte klaidą. Klaida gali suteikti pagalbos, nurodydama išrašą, balansą arba išrašo eilutę. Tačiau nėra tikėtina, kad ji suteiks pakankamai informacijos, padėsiančios jums nustatyti lauką arba elementą, dėl kurio kyla problema.

> [!NOTE]
> Importuoti banko išrašai gali persidengti tik viename taške.  Pavyzdžiui, jei išrašas baigiasi 2021 m. sausio 1 d. 12:00 val., tada kito išrašo pradžios data gali būti 12:00 AM, jarnuary 1, 2021 12:00:00 AM.

## <a name="what-are-the-differences"></a>Kokie skirtumai?
Palyginkite banko failo maketo apibrėžimą su „Finance“ importo apibrėžimu ir pasižymėkite bet kokius laukų ir elementų skirtumus. Palyginkite banko išrašo failą su susijusiu „Finance“ failo pavyzdžiu. ISO20022 failuose skirtumus pastebėti turėtų būti lengva.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Importuotų banko išrašų laiko juostų skirtumai
Importavimo rinkmenos datos ir laiko vertės gali skirtis nuo datos ir laiko verčių, rodomos finansuose ir operacijose. Norėdami išvengti šio neatitikimo, puslapyje **Konfigūruoti duomenų šaltinius** pasirinkite laiko juostos nustatymus. Daugiau informacijos apie laiko juostos nustatymų nurodymą žr. [Išplėstinio banko derinimo importo nustatymo procesas](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Pakeitimai
Paprastai keitimą reikia atlikti vienoje iš trijų transformacijų. Kiekviena transformacija parašyta konkrečiam standartui.

| Išteklių pavadinimas                                         | Failo vardas                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Transformacijų derinimas
### <a name="adjust-the-bai2-and-mt940-files"></a>BAI2 ir MT940 failų koregavimas

BAI2 ir MT940 failai yra tekstiniai failai ir juos reikia koreguoti, norint įjungti išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) derinimą. Programa atlieka šį koregavimą, kai failas importuojamas.

1.  Kurkite XML failą ir į jį nukopijuokite tolesnį tekstą.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Nukopijuokite banko išrašo failo turinį ir įklijuokite jį į XML failą, kad jis pakeistų **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>XSLT derinimas

Daugiau informacijos rasite <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Paleiskite „Visual Studio“.
2.  Kurkite konsolės programą.
3.  Atidarykite atitinkamą XSLT.
4.  Spustelėkite XLST ir jos ypatybių puslapį.
5.  Nustatykite įvestį į banko išrašo failo vietą.
6.  Nurodykite išvesties vietą ir failo vardą.
7.  Nustatykite reikiamus ribinius taškus.
8.  Meniu spustelėkite **XML** &gt; **Pradėti derinti XSLT**.

### <a name="format-the-xslt-output"></a>XSTL išvesties formatavimas

Kai transformacija paleidžiama, ji sukuria išvesties failą, kurį galima peržiūrėti „Visual Studio“. Naudokite CTRL + A, CTRL + K ir CTRL + D, norėdami greitai formatuoti išvesties failą.

### <a name="adjust-the-transformation"></a>Transformacijos koregavimas

Koreguokite transformaciją, norėdami banko išrašo faile gauti atitinkamą lauką arba elementą. Tada susiekite tą lauką arba elementą su atitinkamu „Finance“ elementu.

### <a name="debitcredit-indicator"></a>Debeto / kredito indikatorius

Kartais debetai gali būti importuoti kaip kreditai, o kreditai gali importuoti kaip debetai. Norėdami išspręsti šią problemą, pakeiskite atitinkamą XSLT. Jeigu banko išrašai pateikiami iš kelių bankų, įsitikinkite, kad jie visi naudoja tą patį debeto / kredito metodą, arba sukurkite atskiras transformacijas.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator šablonas
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit šablonas
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator šablonas

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banko išrašų formatų ir techninių maketų pavyzdžiai
Tolesnėje lentelėje pateikiami išplėstinio banko derinimo importavimo failo techninio maketo aprašų pavyzdžiai ir trys susijusių banko išrašo failų pavyzdžiai. Failų pavyzdžius ir techninius maketus galite atsisiųsti čia: [importuoti failo pavyzdžius](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Techninio maketo aprašas                             | Banko išrašo failo pavyzdys          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

