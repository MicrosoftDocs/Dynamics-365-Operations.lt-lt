---
title: Garantinio rašto operacija
description: Ši procedūra padeda apdoroti garantinius raštus.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786aecf69bae3d07ac80a55b4dc835dd8129bd59
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803970"
---
# <a name="letter-of-guarantee-transaction"></a>Garantinio rašto operacija

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda apdoroti garantinius raštus.



Prieš baigdami šitą procedūrą, turite įvykdyti toliau nurodytas užduotis:

- Nustatyti garantinio rašto banko priemones ir registravimo šablonus.

- Kurti garantinio rašto banko priemonės sutartį.



Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Kurti pardavimo užsakymą su garantiniu raštu
1. Pereikite į Gautinų **sumų >, > visus pardavimo užsakymus**.
2. Spustelėkite **Naujas**.
3. Lauke **Kliento sąskaita** įveskite arba pasirinkite reikšmę.
4. Išplėskite skyrių **Bendra**.
5. Lauke **Teritorija** įveskite arba pasirinkite reikšmę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Banko **dokumento tipas pasirinkite** Garantinis **raštas**.
10. Spustelėkite **Gerai**.
11. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
12. Lauke **Vieneto kaina** įveskite skaičių.
13. Išplėskite skyrių **Eilutės informacija** section.
14. Spustelėkite skirtuką **Pristatymas**.

>[!Note] 
>Pasirinkti **pristatymo datos valdymo nėra** = **·**  

15. Pageidaujamos **siuntimo datos** lauke įveskite datą.
16. Į lauką **Patvirtinta** siuntimo data įveskite datą.

## <a name="process-letter-of-guarantee_request"></a>Apdoroti garantinį raštą Užklausa
1. Veiksmų srityje spustelėkite **Valdyti**.
2. Spustelėkite **garantinį raštą**.
3. Veiksmų srityje spustelėkite Garantinis **raštas**.
4. Norėdami atidaryti **numetimo** dialogo langą, spustelėkite Užklausa.
5.  **Lauke Tipas** įveskite arba pasirinkite vertę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke **Reikšmė** įveskite skaičių.
8. Lauke Galiojimo **data** įveskite datą ir laiką.
9. Spustelėkite **Gerai**.
10. Uždarykite puslapį.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Apdoroti garantinį raštą Pateikti bankui
1. Eikite į **grynųjų pinigų ir banko > garantiniai > garantiniai raštai**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Norėdami **atidaryti numetimo dialogo** langą, spustelėkite Pateikti bankui.
4. Lauke **Banko sąskaita** įveskite arba pasirinkite reikšmę.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Gerai**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Apdoroti garantinį raštą Gauti iš banko
1. Norėdami **atidaryti numetimo dialogo** langą, spustelėkite Gauti iš banko.
2. Į lauką **Banko** numeris įveskite vertę.
    * Patikrinkite vertes apskaičiuotuose maržos **ir**  **išlaidų laukuose** .  
3. Spustelėkite **Gerai**.
4. Išplėskite **skyrių** Veiksmai.
    * Patikrinkite įrašą „Gauti iš banko“.  
5. Spustelėti norint vadovautis žurnalo paketo **numerio lauke esatidarykite** saitą.
6. Spustelėkite **Eilutės**.
    * Patikrinkite žurnalo įrašų registravimą.  
7. Uždarykite puslapį.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Apdoroti garantinį raštą Duoti gavėjui
1. Pereikite į Gautinų **sumų >, > visus pardavimo užsakymus**.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite **Valdyti**.
4. Spustelėkite **garantinį raštą**.
5. Veiksmų srityje spustelėkite Garantinis **raštas**.
6. Norėdami **atidaryti numesti dialogo** langą, spustelėkite Duoti gavėjui.
7. Spustelėkite **Gerai**.
8. Eikite į **grynųjų pinigų ir banko > garantiniai > garantiniai raštai**.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Norėdami **atidaryti numesti dialogo** langą, spustelėkite Duoti gavėjui.
11. Spustelėkite **Gerai**.
12. Išplėskite **skyrių** Veiksmai.
    * Patikrinkite įrašą „Duoti gavėjui“.  

## <a name="process-letter-of-guarantee_increase-value"></a>Apdoroti garantinį raštą Didinti vertę
1. Pereikite į Gautinų **sumų >, > visus pardavimo užsakymus**.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite **Valdyti**.
4. Spustelėkite **garantinį raštą**.
5. Veiksmų srityje spustelėkite Garantinis **raštas**.
6. Norėdami atidaryti **numetimo** dialogo langą, spustelėkite Padidinti reikšmę.
7. Norėdami pridėti **lauką**, įveskite skaičių.
8. Spustelėkite **Gerai**.
9. Eikite į **grynųjų pinigų ir banko > garantiniai > garantiniai raštai**.
10. Sąraše raskite ir pasirinkite norimą įrašą.
11. Norėdami atidaryti **numetimo** dialogo langą, spustelėkite Padidinti reikšmę.
12. Spustelėkite **Gerai**.
13. Išplėskite **skyrių** Veiksmai.
    * Patikrinkite įrašą „Didinti vertę“.  
14. Sąraše raskite ir pasirinkite norimą įrašą.
15. Spustelėti norint vadovautis žurnalo paketo **numerio lauke esatidarykite** saitą.
16. Spustelėkite **Eilutės**.
    * Patikrinkite užregistruotus žurnalo įrašus.  

## <a name="process-letter-of-guarantee_liquidate"></a>Apdoroti garantinį raštą Likviduoti
1. Pereikite į Gautinų **sumų >, > visus pardavimo užsakymus**.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite **Valdyti**.
4. Spustelėkite **garantinį raštą**.
5. Veiksmų srityje spustelėkite Garantinis **raštas**.
6. Norėdami **atidaryti numetimo** dialogo langą, spustelėkite Likviduoti.
7. Spustelėkite **Gerai**.
8. Eikite į **grynųjų pinigų ir banko > garantiniai > garantiniai raštai**.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Norėdami **atidaryti numetimo** dialogo langą, spustelėkite Likviduoti.
11. Spustelėkite **Gerai**.
12. Išplėskite **skyrių** Veiksmai.
    * Patikrinkite įrašą „Likviduoti“.  
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Spustelėti norint vadovautis žurnalo paketo **numerio lauke esatidarykite** saitą.
15. Spustelėkite **Eilutės**.
    * Patikrinkite užregistruotus žurnalo įrašus.  
16. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
