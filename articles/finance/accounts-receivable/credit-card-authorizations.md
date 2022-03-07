---
title: Kredito kortelių nustatymas, autorizacija ir patvirtinimas
description: Šiame straipsnyje pateikiama kredito kortelės autorizavimo programoje „Microsoft Dynamics 365 Finance“ apžvalga. Jame pateikiama informacija apie tai, kaip nustatyti mokėjimo tarnybą, į pardavimo užsakymą įtraukti kredito kortelę ir anuliuoti autorizaciją.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 502fe22aa0caafbcff059c9d0ae83c7cd030e8d0
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190314"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Kredito kortelių nustatymas, autorizacija ir patvirtinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama kredito kortelės autorizavimo programoje „Microsoft Dynamics 365 Finance“ apžvalga. Jame pateikiama informacija apie tai, kaip nustatyti mokėjimo tarnybą, į pardavimo užsakymą įtraukti kredito kortelę ir anuliuoti autorizaciją.

## <a name="setting-up-the-credit-card-payment-service"></a>Kredito kortelės mokėjimo paslaugos nustatymas

Norėdami naudotis kredito kortelėmis, turite sukurti ir aktyvuoti mokėjimo paslaugą Mokėjimo paslaugų puslapyje. Mokėjimo paslauga veikia kaip tiltas, jungiantis jūsų organizaciją su klientų kreditinių kortelių mokėjimus apdorojančiu banku. Turite dirbti su kredito kortelių teikėju, nurodytu mokėjimo jungties lauke ir sukurti sąskaitą su tuo teikėju. Tada turite sukurti kitas parinktis Mokėjimo paslaugų puslapyje, nustatyti kredito kortelių rūšis, skirtas „American Express“, „Discover“, „MasterCard“ ir „Discover“ Kredito kortelių rūšių puslapyje, ir aktyvuoti teikėją kaip numatytąjį teikėją. Taip pat, norėdami baigti sąranką, turite atlikti šiuos žingsnius:
-   Gautinų sumų parametrų puslapyje nurodykite parametrus, naudotinus kreditinių kortelių autorizavimui.
-   Mokėjimo sąlygų puslapyje nustatykite kredito kortelės mokėjimo sąlygas. Mokėjimo tipo lauke pasirinkite Kreditinę kortelę.
-   Kliento kredito kortelių puslapyje įveskite kredito kortelės informaciją klientams.

## <a name="adding-a-new-credit-card"></a>Kaip pridėti naują kreditinę kortelę
Naujos kredito kortelės duomenis galite sukurti Klientų puslapyje naudodami Klientas, Nustatyti, Kreditinė kortelė. Taip pat galite sukurti kreditinių kortelių įrašus, įvesdami pardavimų užsakymus Pardavimų užsakymų puslapyje, naudodami Tvarkyti, Klientas, Kreditinė kortelė, Registruoti.

## <a name="adding-a-credit-card-to-a-sales-order"></a>Kaip pridėti kreditinę kortelę pardavimo užsakymui

Galite pridėti kreditinę kortelę pardavimo užsakymui, pasirinkdami kredito kortelę iš kredito kortelių paieškos iš Kainų ir nuolaidų „FastTab“ Pardavimų užsakymo puslapyje. Norėdami pradėti autorizavimo procesą, Veiksmų srityje, Tvarkyti kortelę, pasirinkite Kredito kortelė ir Autorizuoti.

## <a name="authorizing-a-credit-card"></a>Kredito kortelės autorizacija

Autorizavus kredito kortelę, patikrinamas kortelės numeris ir kortelės savininko vardas ir patvirtinamas turimas kredito likutis. Pasirinktinai tikrinama kortelės patvirtinimo vertė ir kortelės savininko adresas. Kliento turimas kredito likutis sumažinamas pardavimo sąskaitoje faktūroje nurodyta suma. Mokėjimo paslauga siunčia informaciją, kad kredito kortelė buvo patvirtinta arba atmesta. Pardavimo pavedimi išrašius sąskaitą, sąskaitos faktūros suma nurašoma iš kredito kortelės.

### <a name="card-verification-value"></a>Kortelės tikrinimo vertė

Galite reikalauti kortelės patvirtinimo vertės, kuri kartais vadinama kortelės apsaugos kodu. „American Express“ kortelėms tai keturių skaitmenų reikšmė. „Discover“, „MasterCard“ ir „Visa“ kortelėms šis skaičius yra triženklis.

### <a name="address-verification"></a>Adreso tikrinimas

Adreso patikrinimo informacija visada siunčiama mokėjimo paslaugų teikėjui. Galite nuspręsti, kiek informacijos reikia, kad operacija būtų priimta. Būtinai pasitikrinkite, ar jūsų teikėjas priima šią informaciją. Adreso patvirtinimo variantai yra šie:
-   **Visada priimti sandorį** – priimti sandorį, neatsižvelgiant į adreso patikrinimo rezultatus.
-   **Sąskaitos turėtojas** – palyginti kortelės savininko vardą iš sandorio su kredito kortelės įmonės informacija.
-   **Atsiskaitymo adresas** – palyginti kortelės savininko vardą ir atsiskaitymo adresą iš sandorio su kredito kortelės įmonės informacija.
-   **Atsiskaitymo pašto kodas** – palyginti kortelės savininko vardą, pavardę, atsiskaitymo adresą ir pašto kodą iš sandorio su kredito kortelės įmonės informacija.

## <a name="data-support"></a>Duomenų palaikymas
Kiekvienam palaikomam kredito kortelės tipui galite nurodyti duomenų palaikymo lygį. Lygis nurodo, kiek informacijos apie sandorį perduodama mokėjimo paslaugai. Būtinai paklauskite savo paslaugų teikėjo, ar jis gali suteikti šią informaciją. Duomenų palaikymo lygio variantai yra šie:
-   **1 lygis** – perduoti sandorio datą, sandorio vertę ir aprašymą.
-   **2 lygis** – perduoti visą 1 lygio informaciją, siuntimo ir prekybininko adresus, ir informaciją apie mokesčius.
-   **3 lygis** – perduoti visą 2 lygio informaciją, siuntimo ir prekybininko adresus bei užsakymo eilutės informaciją.

## <a name="partial-payments"></a>Daliniai mokėjimai
Jei gabenate dalį užsakymo, fiksuojama dalinio užsakymo suma, o autorizacija visai užsakymo sumai uždaroma. Tada pateikiama nauja autorizacija likusio neišsiųsto užsakymo sumai.

## <a name="voiding-an-authorization"></a>Autorizavimo anuliavimas 
Norėdami anuliuoti kreditinių kortelių autorizavimą, galite pakeisti mokėjimo būdą į kitą metodą, kuris neturi kredito kortelės tipo.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]