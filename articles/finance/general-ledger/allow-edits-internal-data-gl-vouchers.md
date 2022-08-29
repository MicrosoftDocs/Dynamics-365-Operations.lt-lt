---
title: Leisti redaguoti didžiosios knygos kvitų vidinius duomenis
description: Šiame straipsnyje pateikiama informacija apie tai, kaip redaguoti vidinius DK kvitų duomenis.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220718"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Leisti redaguoti didžiosios knygos kvitų vidinius duomenis

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Kai DK registruojate apskaitos įrašus, aprašymo **laukas** dažnai naudojamas vidinėms pastaboms arba dokumentacijai saugoti. Jei informacija neteisinga, dėl jos gali kilti painiavos, o laikotarpio pabaigos uždarymas gali būti sudėtingiau. Naudojant šią priemonę apskaitos vadovas arba apskaitos prižiūrėtojas gali ištaisyti klaidas **redaguodami** DK užregistruotų kvitų aprašymo lauką.

DK užregistruotų kvitų pakeitimai yra apriboti vidinio pobūdžio duomenimis. Ši priemonė niekada neleis redaguoti duomenų, pvz., sumų, registravimo datų, DK sąskaitų ir operacijos valiutos. Šių duomenų pakeitimai turės įtakos išorinėms finansinių ataskaitų ataskaitoms ir turi būti atlikti tik naujais DK kvitais.

> [!NOTE]
> Naudojant "Dynamics 365" 10.0.29 finansų versiją, ši funkcija gali redaguoti tik aprašo **lauką**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Redaguoti DK kvitų vidinius duomenis

Kad galėtumėte redaguoti vidinius DK kvitų duomenis, **·** **turite įgalinti funkciją Leisti redaguoti vidinius DUOMENIS DK kvitų ypatybėje Funkcijų valdymo** darbo sritis.
Įgalinus funkciją, vartotojas, kuris redaguos užregistruotus kvitus, turi būti priskirtas apskaitos vadovo arba apskaitos prižiūrėtojo vaidmeniui. Teises prie kitų vaidmenų taip pat galima pridėti pritaikant saugos vaidmenis.

Redagavimo procesas leidžiamas tik iš kvito operacijų puslapio.

1. Eikite į **DK užklausas** > **ir ataskaitas kvitų** > **operacijas**.
2. Dialogo lange **SysQuery** įveskite ieškos kriterijus, pagal kuriuos reikia pasirinkti kvitus.
3. Pasirinkite kvitų, kuriuos norite redaguoti, eilutes, tada pasirinkite Redaguoti kvito **Redaguoti** > **vidinio kvito duomenis**.

    [![Kvito operacijų puslapis.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
Vidinio **kvito duomenų** redagavimo puslapyje rodomi šie kiekvienos pasirinktos eilutės duomenys:
  
  - Didžiosios knygos sąskaita
  - Abonemento pavadinimas
  - Kvitas
  - Dabartinis aprašas
  - Naujas aprašas

    [![Žurnalo kvitas.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Galima redaguoti **tik** lauką Naujas aprašymas. Pagal numatytuosius nustatymus, vertė atitinka **dabartinio** aprašymo lauko vertę, kad aprašyme galėtumėte greitai ištaisyti neesminius klaidas.

4. Modifikuokite **kiekvienos** eilutės naujo aprašymo lauką arba panaikinkite kiekvienos eilutės aprašymą.

   Arba jeigu turite atnaujinti kelias eilutes, kurių vertė tokia pati, atlikite šiuos veiksmus:

      1. Pasirinkite eilutes, kurių eilutes norite redaguoti, tada pasirinkite Masinis **pasirinktų įrašų atnaujinimas**.
      2. Lauke, **norimą redaguoti,** pasirinkite norimą redaguoti lauką. Šiuo metu peržvalgoje yra tik naujo **aprašymo** laukas.
      3. **Lauke Nauja vertė** įveskite naują aprašymą.
      4. Pasirinkite **Naujinti**. Visi pasirinkti įrašai atnaujinami nauja verte.

      [![Masinio atnaujinimo pasirinktų įrašų dialogo langas.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Lauke Redagavimo **priežastis įveskite** pastabą, paaiškina datą, kodėl buvo redaguojant. Ši pastaba rodoma kvito **redagavimo puslapio sekimo puslapyje**.

   Tam pačiam kvitui galima atlikti keletą redagavimų ir kiekvienas redagavimas bus sekamas.

## <a name="audit-trail-of-voucher-edits"></a>Kvito redagavimų įrašo sekimas

Įrašo sekmas tvarkomas specialiai tam, kad būtų sekami naudojant šią priemonę atliekami pakeitimai. Kvitų redagavimų sekimo prieigą galite pasiekti dviem būdais:

  - Eikite į **DK užklausas** > **ir ataskaitas kvitų** > **operacijas**. Kvitų **užklausų puslapyje pasirinkite** Redaguoti kvito **redagavimo** > **kvito sekimą**. Įrašo sekmas rodomas tik pasirinktame kvito įraše. 
   
    Tokiu būdu atidarydami užklausą galite sutelkti dėmesį į visus redagavimus, kurie buvo atlikti viename kvito įraše.
  
  - Eiti į** DK** > periodinių **užduočių kvitų** > **redagavimų įrašo sekimą**. Dialogo lange įveskite kriterijus, pagal kuriuos nurodysite kvitus, kurių redagavimus norite peržiūrėti. Norėdami peržiūrėti visų kvitų žurnalų sekimą, palikite kriterijus tuščius ir pasirinkite **Gerai**. 
    
    Tokiu būdu atidarydami užklausą galite filtruoti redagavimus, kurie buvo padaryti konkrečia data arba tam tikro vartotojo.

Redagavimo **puslapio įraše** rodoma ši informacija:

- **Sukurta data ir laikas** – redagavimo data ir laikas.
- **Redagavimo priežastis** – priežastis, dėl kurios vartotojas įvedė redagavimą.
- **Sukūrė** – vartotojas, kuris atliko redagavimą.

Norėdami peržiūrėti išsamią kiekvieno sekimo informaciją, detalizuoti pagal Sukurtą **datą ir laiko** vertę. Redaguotų **kvito ypatybės puslapio** peržiūra rodo tą pačią informaciją kaip ir originalaus redagavimo puslapyje, įskaitant ankstesnį aprašymą ir atnaujintą aprašymą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
