---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Human Resources“ išplėtimo scenarijų pavyzdžiai, kai naudojama „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859523"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Išplėtimas su „Power Apps“ ir „Power Automate“


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Human Resources“ išplėtimo scenarijų pavyzdžiai, kai naudojama „Microsoft Power Apps“ ir „Microsoft Power Automate“. Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką. Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.

> [!IMPORTANT]
> Jei norite naudoti šablonus ir programėles, aprašytus šiame straipsnyje "taip kaip yra", būtinai patikrinkite juos ir įsitikinkite, kad jie apima visus scenarijus, kurie yra specifiniai jūsų įdiegtims.

## <a name="prerequisites"></a>Būtinieji komponentai

- Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.
- Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „Power Apps“ 2 plano licenciją arba bandomąją „Power Apps“ 2 plano licenciją.

## <a name="integration-with-microsoft-365-power-automate"></a>Integravimas su „Microsoft 365“, „Power Automate“

Naudojantis programa **Integravimas su „Microsoft 365“**, iš „Microsoft 365“ galima gauti prisijungusių vartotojų komandos informaciją. Nurodomi „Human Resources“ darbuotojai, kurių darbuotojų identifikacijos tipai bus gaunami. Vadybininkai gali patikrinti darbuotojų ID tipų galiojimo pabaigos datas. Jie taip pat gali nusiųsti priminimą el. paštu, jei darbuotojo ID tipo galiojimas greitai pasibaigs. „Power Automate“ integruojama su „Power Apps“, kad būtų galima išsiųsti šį priminimą. Nusiuntus priminimą, patvirtinimas bus atsiųstas atgal į „Power Apps“ iš „Power Automate“. Identifikavimo tipai yra vairuotojo pažymėjimas, pasas ir kitos priimtinos tapatybės nustatymo formos.

Galite naudoti šią programą ir kituose scenarijuose. Pavyzdžiui, galite ją naudoti, kad būtų rodoma komandos atostogų informaciją, kalendoriaus įvykiai ir visi konkrečios komandos įvykiai.

Norėdami atsisiųsti **integravimo su „Microsoft 365“ programą „Power Automate“**, „Microsoft“ atsisiuntimo centre eikite į skyrių [Integravimas su „Microsoft 365“](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--sql-connect-and-execute"></a>„Power Automate – SQL prisijungimas ir vykdymas“

**Power Automate – SQL prisijungimas ir vykdymas** šablonas prisijungia prie „Microsoft SQL Server“ ir leidžia vykdyti SQL užklausas.

Nors šis šablonas skaito ir atnaujina SQL lenteles, taip pat galite jį naudoti kituose scenarijuose. Pavyzdžiui, jį galima naudoti „Dataverse“ išdėstymo lentelėje norint įvesti duomenis iš SQL serverio ir periodiškai sinchronizuojant išdėstymo lentelę naudojantis papildančiuoju skirstymu iš SQL serverio.

Išplėstinė užklausa yra integruota su srautu, kad būtų įjungtas duomenų perkėlimas ir papildantysis skirstymas.

Norėdami atsisiųsti **Power Automate – SQL prisijungimas ir vykdymas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – SQL prisijungimas ir vykdymas](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Microsoft Power Platform“](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
