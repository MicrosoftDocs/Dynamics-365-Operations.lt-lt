---
title: Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su dvigubo rašymo moduliu „Finance and Operations” programose.
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172765"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Trikčių, susijusių su dvigubo rašymo moduliu „Finance and Operations” programose, šalinimas

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, naudojant **dvigubo rašymo** modulį „Finance and Operations” programose.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Negalite įkelti dvigubo rašymo modulio „Finance and Operations” programoje

Jeigu negalite atidaryti **dvigubo rašymo** puslapio darbo srityje **Duomenų valdymas** pasirinkdami plytelę **Dvigubas rašymas**, tikriausiai duomenų integravimo paslauga neveikia. Norėdami paprašyti iš naujo paleisti duomenų integravimo paslaugą, sukurkite palaikymo bilietą.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Bandant sukurti naują susiejimą su objektu įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius

Kai bandote konfigūruoti naują dvigubo rašymo objektą, galite gauti tokį klaidos pranešimą:

*Atsakymo būsenos kodas nenurodo sėkmės: 401 (neautorizuota)*

Ši klaida įvyksta, nes tik „Azure AD” nuomotojo administratorius gali pridėti naują susiejimą su objektu.

Norėdami išspręsti šią problemą, prisijunkite prie „Finance and Operations” programos kaip „Azure AD” nuomotojo administratorius. Taip pat turite eiti į web.PowerApps.com ir iš naujo patikrinti ryšį.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Atidarant dvigubo rašymo vartotojo sąsają įvyko klaida

Kai bandote pasiekti dvigubą rašymą iš darbo srities **Duomenų valdymas**, galbūt gausite tokį klaidos pranešimą:

*Nepavyko užmegzti ryšio su login.microsoftonline.com*.

Norėdami išspręsti šią problemą, prisijunkite, naudodami „Microsoft Edge” langą „InPrivate”, inkognito langą „Chromium” arba inkognito langą „Google Chrome”. Taip pat turite atblokuoti arba išvalyti trečiosios šalies slapukus.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Susiejant dvigubo rašymo aplinką arba pridedant naują susiejimą su objektu įvyko klaida

**Reikiami kredencialai, norint išspręsti problemą:** „Azure AD” nuomotojo administratorius

Kai susiejate arba kuriate schemas, gali įvykti tokia klaida:

*Atsakymo būsenos kodas nenurodo sėkmės: 403 (tokenexchange).<br> Seanso ID: \<jūsų seanso id\><br> Šakninės veiklos ID: \<jūsų šakninės veiklos id\>*

Ši klaida gali įvykti, jei neturite pakankamai teisių susieti dvigubą rašymą arba kurti schemas. Norėdami sieti aplinkas ir pridėti naujų siejimų su objektu, turite naudoti „Azure AD” nuomotojo administratoriaus paskyrą. Tačiau atlikę sąranką galite naudoti ne administratoriaus paskyrą, kad stebėtumėte būseną ir redaguotumėte susiejimus.

## <a name="error-when-you-stop-the-entity-mapping"></a>Stabdant susiejimą su objektu įvyko klaida

Kai bandote sustabdyti susiejimus su objektu, galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], \[{"būsena":403,"šaltinis":"","pranešimas":"atpažinimo ženklo keitimo klaida: vartotojui neleidžiama pasiekti ryšį dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], nuotolinis serveris pateikė klaidą: (403) draudžiama.*

Ši klaida įvyksta, kai nėra susietos „Common Data Service” aplinkos.

Norėdami išspręsti šią problemą, sukurkite duomenų integravimo komandai skirtą bilietą. Pridėkite tinklo sekimą, kad duomenų integravimo komanda galėtų pažymėti vidines schemas kaip **Nevykdomos**.
