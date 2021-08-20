---
title: Projekto SF mokėjimo kvito formato nustatymas
description: Įmonės dažnai prideda išspausdintus mokėjimo kvitus prie SF, norėdamos padėti klientams ir nurodyti mokėjimo registravimo ir sudengimo nuorodą.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb0d1d95013b3eac3131064992920da5fa9bea5a1f6d554e6be1d5006a9b21fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732905"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Projekto SF mokėjimo kvito formato nustatymas

[!include [banner](../../includes/banner.md)]

Įmonės dažnai prideda išspausdintus mokėjimo kvitus prie SF, norėdamos padėti klientams ir nurodyti mokėjimo registravimo ir sudengimo nuorodą. Mokėjimo kvitas gali būti naudojamas projekto arba paslaugų SF, priminimo laiškuose, delspinigių pažymose ir sąskaitos išrašuose bei pardavimo ir laisvos formos SF. Norėdami apdoroti mokėjimo kvitus, pirmiausia nustatykite savo kreditoriaus identifikavimo numerį ir mokėjimo kvito priedų formatus.

Šioje procedūroje naudojama demonstracinė įmonė DEMF. 

Šią funkciją gali naudoti juridiniai subjektai, kurių pagrindinis adresas yra Danijoje.


## <a name="set-up-a-creditor-id-number"></a>Nustatyti kreditoriaus ID numerį
1. Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.
2. Išplėskite arba sutraukite dalį Banko sąskaitos informacija.
3. Spustelėkite Redaguoti.
4. Lauke FI-Creditor ID įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Uždarykite puslapį.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Nustatyti SF, pažymų, raštų ir išrašų mokėjimo kvito formatą
1. Eikite į Gautinos sumos > Sąranka > Formos > Formos nustatymas.
2. Spustelėkite skirtuką Sąskaita faktūra.
3. Susijusio mokėjimo priedo kliento SF lauke pasirinkite parinktį.
    * Nėra – nespausdinkite mokėjimo kvito. Pasirinkite šią parinktį, jei mokėjimo suma yra kita valiuta nei Danijos krona (DKK).   FIK 751 – spausdinkite FIK 751 mokėjimo kvitą, jei norite rankiniu būdu įrašyti mokėjimo sumą ir terminą mokėjimo kvite.   FIK 752 – spausdinti FIK 752 mokėjimo kvitą, jei jūs ketinate naudoti kompiuterio sugeneruotą mokėjimo kvitą, kuriame yra iš anksto atspausdinta mokėjimo suma ir terminas.  
4. Spustelėkite Įrašyti.
5. Spustelėkite skirtuką Laisvos formos SF.
6. Susijusio mokėjimo priedo laisvos formos SF lauke pasirinkite parinktį.
    * Nėra – nespausdinkite mokėjimo kvito. Pasirinkite šią parinktį, jei mokėjimo suma yra kita valiuta nei Danijos krona (DKK).   FIK 751 – spausdinkite FIK 751 mokėjimo kvitą, jei norite neautomatiškai įrašyti mokėjimo sumą ir terminą mokėjimo kvite.   FIK 752 – spausdinti FIK 752 mokėjimo kvitą, jei jūs ketinate naudoti kompiuterio sugeneruotą mokėjimo kvitą, kuriame yra iš anksto atspausdinta mokėjimo suma ir terminas.  
7. Spustelėkite Įrašyti.
8. Spustelėkite skirtuką Delspinigių pažyma.
9. Susijusio mokėjimo priedo delspinigių pažymos lauke pasirinkite parinktį.
    * Nėra – nespausdinkite mokėjimo kvito. Pasirinkite šią parinktį, jei mokėjimo suma yra kita valiuta nei Danijos krona (DKK).   FIK 751 – spausdinkite FIK 751 mokėjimo kvitą, jei norite neautomatiškai įrašyti mokėjimo sumą ir terminą mokėjimo kvite.   FIK 752 – spausdinti FIK 752 mokėjimo kvitą, jei jūs ketinate naudoti kompiuterio sugeneruotą mokėjimo kvitą, kuriame yra iš anksto atspausdinta mokėjimo suma ir terminas.  
10. Spustelėkite Įrašyti.
11. Spustelėkite skirtuką Priminimo laiškas.
12. Susijusio mokėjimo priedo priminimo laiško lauke pasirinkite parinktį.
    * Nėra – nespausdinkite mokėjimo kvito. Pasirinkite šią parinktį, jei mokėjimo suma yra kita valiuta nei Danijos krona (DKK).   FIK 751 – spausdinkite FIK 751 mokėjimo kvitą, jei norite neautomatiškai įrašyti mokėjimo sumą ir terminą mokėjimo kvite.   FIK 752 – spausdinti FIK 752 mokėjimo kvitą, jei jūs ketinate naudoti kompiuterio sugeneruotą mokėjimo kvitą, kuriame yra iš anksto atspausdinta mokėjimo suma ir terminas.  
13. Spustelėkite Įrašyti.
14. Spustelėkite skirtuką Sąskaitos išrašas.
15. Susijusio mokėjimo priedo laisvos formos sąskaitos išrašo lauke pasirinkite parinktį.
    * Nėra – nespausdinkite mokėjimo kvito. Pasirinkite šią parinktį, jei mokėjimo suma yra kita valiuta nei Danijos krona (DKK).   FIK 751 – spausdinkite FIK 751 mokėjimo kvitą, jei norite neautomatiškai įrašyti mokėjimo sumą ir terminą mokėjimo kvite.   FIK 752 – spausdinti FIK 752 mokėjimo kvitą, jei jūs ketinate naudoti kompiuterio sugeneruotą mokėjimo kvitą, kuriame yra iš anksto atspausdinta mokėjimo suma ir terminas.  
16. Spustelėkite Įrašyti.
17. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]