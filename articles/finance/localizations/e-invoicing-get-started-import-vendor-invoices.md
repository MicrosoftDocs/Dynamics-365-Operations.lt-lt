---
title: Norėdami importuoti tiekėjo SF naudokite elektroninę SF išrašymo paslaugą
description: Šioje temoje pateikiama informacija apie tai, kaip importuoti tiekėjo SF naudojantis elektroninių SF išrašymo tarnyba.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751257"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Norėdami importuoti tiekėjo SF naudokite elektroninę SF išrašymo paslaugą

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti importuojant tiekėjo sąskaitas su SF paslaugomis. Tai padės jums atlikti konfigūracijos veiksmus, aprašytus „Regulatory Configuration Services“ (RCS), ir kad turite gauti elektroninių tiekėjų „Dynamics 365 Finance“ bei „Dynamics 365 Supply Chain Management“ SF iš tiekėjų.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Tiekėjo SF importavimo į RCS nustatymai
Norėdami nustatyti tiekėjo SF importavimą RCS, atlikite šiuos veiksmus:

1. Pasikonsultuokite su bendrai [prieinamų elektroninių SF išrašymo priemonių sąrašu](e-invoicing-configuration-rcs.md#generally-available-features).
2. Rinkitės ir importuokite jūsų sukurtą elektroninės sąskaitos funkciją. Dėl daugiau informacijos, žr. [Importuoti elektroninių SF funkciją iš „Microsoft“ konfigūracijos tiekėjo](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Sukurkite elektroninių sąskaitų funkciją jūsų organizacijos tiekėjuje. Dėl daugiau informacijos, žr. [Kurti elektroninių SF funkciją Jūsų organizacijos tiekėjo asmenyje](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Konfigūruoti el. pašto sąskaitos kanalą

Konfigūruokite el. pašto sąskaitos kanalą, jei jūsų sukurta elektroninių SF išrašymo priemonė importuoja elektronines tiekėjo SF iš pridėtų failų, kurios gautos el. paštu.

1. RCS rinkitės jūsų sukurtą elektroninės sąskaitos funkciją. Įsitikinkite, kad pasirenkate versiją, kurios būsena **Juodraštis**.
2. Skirtuke **Nustatymai** tinklelyje rinkitės funkcijos nustatymus ir tada rinkitės **Redaguoti**.
3. Laukų grupės **Parametrai skirtuke** Duomenų kanalas **pasirinkite** šį **Serverio adresas** ir įveskite el. pašto sąskaitos teikėją.
4. Pasirinkite **serverio prievadą** ir įveskite el. pašto abonemento teikėjo naudojamą prievadą.
5. Pasirinkite **vartotojo vardo slaptą** ir įveskite rakto saugyklos slaptojo vardo, kuriame yra el. pašto vartotojo sąskaitos ID, pavadinimą.
6. Pasirinkite **vartotojo slaptažodžio slaptą** ir įveskite rakto saugyklos slaptojo vardo, kuriame yra el. pašto slaptažodžio sąskaitos ID, pavadinimą.
7. Pasirinkite **temos filtrą**. Peržiūrėkite ir atnaujinkite eilutę, kurioje yra numatytasis el. pašto subjektas, identifikuojant el. laišką, kuriame yra importuojama elektroninio tiekėjo SF.
8. Jei reikia skirtuke **Taikymo taisyklės** peržiūrėkite ir atnaujinkite kriterijus. Daugiau informacijos žr. [Taikomumo taisyklės](e-invoicing-configuration-rcs.md#applicability-rules).
9. Pasirinkite **Išsaugoti** ir uždarykite puslapį.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Kanalo „Microsoft SharePoint“ konfigūravimas

Konfigūruoti „Microsoft SharePoint“ kanalą, jei elektroninių SF išrašymo priemonė importuoja elektronines tiekėjo SF iš aplankuose dėtių „SharePoint“ failų.

1. RCS rinkitės jūsų sukurtą elektroninės sąskaitos funkciją. Įsitikinkite, kad pasirenkate **versiją** su būsena **Juodraštis**.
2. Skirtuke **Nustatymai** tinklelyje rinkitės funkcijos nustatymus ir tada rinkitės **Redaguoti**.
3. Skirtuke **Duomenų kanale** lauko grupe **Parameterai** rinkitės **„SharePoint“ adresas** ir įveskite „SharePoint“ URL.
4. Pasirinkite **serverio prievadą** ir įveskite el. pašto abonemento teikėjo naudojamą prievadą.
5. Pasirinkite **Vartotojo Id** ir įveskite rakto saugyklos slaptojo vardo, kuriame yra „SharePoint“ ID klientą.
6. Pasirinkite **Vartotojo kodą** ir įveskite rakto saugyklos slaptojo vardo, kuriame yra „SharePoint“ slaptažodžio klientą.
7. Pasirinkite **Failo filtras**. Peržiūrėkite ir atnaujinkite šabloną, norėdami filtruoti failus, kuriuose yra importuojama elektroninio tiekėjo SF.
8. Jei reikia skirtuke **Taikymo taisyklės** peržiūrėkite ir atnaujinkite kriterijus. Daugiau informacijos žr. [Taikomumo taisyklės](e-invoicing-configuration-rcs.md#applicability-rules).
9. Pasirinkite **Išsaugoti** ir uždarykite puslapį

### <a name="deploy-an-electronic-invoicing-feature"></a>Talpinkite elektroninės sąskaitos išrašymo funkciją

Norėdami įdiegti elektroninių SF išrašymo funkciją į paslaugų aplinką, žr. skyrių [Elektroninės SF talpinimo funkcija į paslaugų aplinką](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Nustatykite tiekėjo sąskaitos importavimą į „Finance and Supply Chain Management“
Norėdami nustatyti skirtingus tiekėjo SF importavimo tipus, atlikite veiksmus, nurodytus tolesniuose dviejuose skyriuose.

### <a name="import-vendor-invoices-from-email"></a>Importuoti tiekėjo SF iš el. pašto

1. Prisijunkite prie „Finance or Supply Chain Management“ aplinką ir patikrinkite, ar esate tinkamame juridiniame asmenyje.
2. Eikite į **Organizacijos administravimas** > **Nustatymas** > **Elektroninių dokumentų parametrai**.
3. Skirtuke **Priemonės** įsitikinkite, kad pasirinktas **NF-e Federal - Brazilinė elektroninė SF**.
4. **Išorinių kanalų** skirtuko laukų **grupėje** Kanalai pasirinkite **Įtraukti**.
5. Lauke **Kanalas** įveskite **NFe** (kanalo pavadinimą, nurodytą RCS elektroninių SF išrašymo priemonės duomenų kanalo konfigūracijoje).
6. Lauke **Aprašas** įveskite aprašą. Lauke **Įmonė** pasirinkite juridinį subjektą.
7. Lauke **Dokumento kontekstas** pasirinkite **Kliento sąskaitos konteksto modelis – finansinio dokumento kontekstas**.
8. Laukų **grupėje Importuoti** šaltinius pasirinkite **Įtraukti**.
9. Lauke **Pavadinimas** įveskite **XmlFile** (pavadinimą **Priedo filtras** suteiktas duomenų kanalo konfigūracijos elektroninės sąskaitos funkcijos RCS).
10. Aprašymo **lauke**, įveskite aprašymą ir duomenų objekto pavadinimo **Duomenų objekto pavadinimas** rinktis **Gauti NF-e XML dokumentai**.
11. Modelio **susiejimo lauke** pasirinkite **NF-el. pašto importavimą – NF-e el. pašto importavimą (BR)** tada pasirinkite **Įrašyti**.
12. Skirtuko **Elektroninis dokumentas** skirtuke, laukelio grupėje **Elektroninė ataskaitos** rinkitės **Įtraukti** ir **Lentelės pavadinimas** laukelyje rinkitės **Gauti NF-e XML dokumentai**.
13. Lauke **Dokumento kontekstas** pasirinkite **Užklausos mokesčių dokumento kontekstas - Kliento sąskaitos kontekstas**.
14. Elektroninio **dokumento modelio susiejimo lauke** pasirinkite **Užklausų susiejimas – finansinio dokumento susiejimas**.
15. Pasirinkite **Atsakymų tipai**, o tada pasirinkite **Nauja**.
16. Lauke **Atsakymo tipas** įveskite **Atsakymas**. Lauke **Pateikimo būsena** pasirinkite **Grafikas**.
17. Lauke **Modelio susiejimas** pasirinkite **Atsakymo pranešimo importavimo formatas – modelio susiejimas iš atsakymo pranešimo**.
18. Pasirinkite **Įrašyti** ir uždarykite puslapį.

### <a name="import-peppol-electronic-vendor-invoices"></a>Importuoti PEPPOL elekronines tiekėjo sąskaitas

1. Eikite į darbo sritį **Elektroninės ataskaitos** ir pasirinkite plytelę **Ataskaitų konfigūracijos**.
2. Pasirinkite **kliento SF konteksto modelį** ir sukurkite išvestinį konfigūraciją.
3. **Juodraščio versijoje** pasirinkite **Konstruktorius**.
4. Medyje **Duomenų modelio** pasirinkite **Kliento SF**, tada pasirinkite **Susieti modelį su duomenų šaltiniu**.
5. Medyje **Aprašai** pasirinkite **CustomerInvoice** ir pasirinkite **Konstruktorius**.
6. Medyje **Duomenų šaltiniai** pasirinkite **Kontekstas\_Kanalas**. Lauke **Vertė** rinkitės **PEPPOL**. Kanalas įveskite NFe (kanalo pavadinimą, nurodytą RCS elektroninių SF išrašymo priemonės duomenų kanalo konfigūracijoje). 
7. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
8. Uždarykite puslapį.
9. Pasirinkite **Kliento sąskaitos konteksto modelis**, „FastTab“ **Versijos** rinkitės **Keisti būseną** > **baigta**.
10. Eikite į **organizacijos administravimo** > **nustatymo** > **Elektroninio dokumento parametrai** ir **Funkcijos**, kad įsitikinkite **PEPPOL bendrosios elektroninės sąskaitos** rya pasirinktas. 
11. **Išorinių kanalų** skirtuko laukų **grupėje** Kanalai pasirinkite **Įtraukti**.
12. Lauke **Kanalas** įveskite **PEPPOL**. Lauke **Aprašas** įveskite aprašą.
13. Lauke **Įmonė** pasirinkite juridinį subjektą. Lauke **Dokumento kontekstas** pasirinkite **Kliento sąskaitos konteksto modelis – finansinio dokumento kontekstas**.
14. Pasirinkite **Įrašyti** ir uždarykite puslapį.


## <a name="receive-electronic-invoices"></a>Gauti elektronines sąskaitas
Norėdami gauti rinkėjo sąskaitas faktūras, atlikite šiuos veiksmus:

1. Eikite į **Organizacijos administravimas** > **Periodinė** > **Elektroniniai dokumentai** > **Gauti elektroniniai dokumentai**.
2. Pasirinkite **Gerai** ir uždarykite puslapį.

## <a name="view-receive-logs-for-electronic-invoices"></a>Peržiūrėti elektroninių SF gavimo žurnalus

Norėdami peržiūrėti elektroninių SF gavimo žurnalus, eikite į **organizacijos administravimo** > **periodinių** > **elektroninių dokumentų** > **elektroninių dokumentų gavimo žurnalas**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
