---
title: Laisvos formos sąskaitos faktūros šablono priskyrimas klientui
description: Ši užduotis parodo, kaip klientui priskirti laisvos formos SF šabloną.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0219521867d1cfb1fa4edcdf20dd70eea8a3d0e1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819895"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Laisvos formos sąskaitos faktūros šablono priskyrimas klientui

[!include [banner](../../includes/banner.md)]

Ši užduotis parodo, kaip klientui priskirti laisvos formos SF šabloną. Ši užduotis naudoja USMF demonstracinę įmonę ir yra skirta naudotojui, kuris yra atsakingas už A/R SF valdymą ir apdorojimą.

1. **Naršymo srityje** eikite į **Moduliai > Gautinos sumos > Klientai > Visi klientai**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. **Veiksmų sritis** spustelėkite **Sąskaita faktūra**.
4. Spustelėkite **Pasikartojančios sąskaitos faktūros**. Naudokite šį puslapį, kad laisvos formos SF šablonus priskirtumėte klientams ir nurodytumėte, kaip dažnai SF bus siunčiamos klientui.  
5. Spustelėkite **Naujas**, kad klientui priskirtumėte naują šabloną.
6. Lauke **Šablonas** pažymėkite laisvą tekstinį sąskaitos faktūros šabloną, kurį norite priskirti klientui.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke **Atsiskaitymo pradžios data** įveskite datą, kada bus sugeneruota pirma sąskaita faktūra.
10. Skyriuje **Pasikartojimo pabaiga** įveskite pasikartojimo pabaigos datą.  
    * Pasirinkite vieną iš šių parinkčių: Nėra pabaigos datos – SF bus generuojamos neribotą laiką, kol šablonas bus pašalintas iš kliento sąskaitos.
    * Atsiskaitymo pabaigos data – pasirinkite šią parinktį ir įveskite paskutinę galimą SF generavimo datą.  
11. Lauke **Didžiausia sukaupta suma** įveskite didžiausią sukauptą sumą, po kurios sąskaitos faktūros generavimas bus sustabdytas. Įveskite maksimalią kaupiamąją sumą, kurią galima pasiekti naudojant pasirinktą šabloną. Pvz., jei įvesite 1 000,00 ir generuosite mėnesines 100,00 SF, SF nebebus generuojamos sugeneravus dešimtąją SF.  
12. Skyriuje **Generuoti pasikartojančias sąskaitas faktūras naudojant numatytąsias reikšmes iš** pažymėkite laisvą tekstinį sąskaitos faktūros šabloną arba kliento sąskaitą. Pasirinkite laisvos formos SF šabloną arba kliento sąskaitą, pagal kurią bus nustatomos kalbos, registravimo šablono, PVM grupės, prekės PVM grupės, sąrašo kodo, pristatymo šalies / regiono, valiutos, mokėjimo sąlygų, mokėjimo būdo, mokėjimo specifikacijos, mokėjimo grafiko, mokėjimo nuolaidos, finansinių dimensijų ir žiro mokėjimo dokumento numatytosios vertės, kai kuriamos SF.  
13. Lauke **Pasikartojimo modelis** pažymėkite pasikartojimo modelį.
    + Kasdien – pasirinkite šią parinktį ir lauke Per įveskite dienų skaičių. Pavyzdžiui, jei įvesite 15, šio kliento SF bus generuojama kas 15 dienų.
    + Kas savaitę – pasirinkite šią parinktį ir lauke Per įveskite savaičių skaičių. Pavyzdžiui, jei įvesite 2, šio kliento SF bus generuojama kas dvi savaites.
    + Kas mėnesį – pasirinkite šią parinktį ir lauke Per įveskite mėnesių skaičių. Pavyzdžiui, jei įvesite 6, šio kliento SF bus generuojama kas šešis mėnesius.
    + Kas metus – pasirinkite šią parinktį ir lauke Per įveskite metų skaičių. Pavyzdžiui, jei įvesite 2, šio kliento SF bus generuojama kas dvejus metus.  
14. Lauke **Per** įveskite skaičių.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]