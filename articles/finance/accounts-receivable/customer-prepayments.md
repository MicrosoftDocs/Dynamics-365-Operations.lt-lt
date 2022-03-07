---
title: Kliento išankstiniai mokėjimai
description: Šioje temoje paaiškinama, kaip nustatyti ir apdoroti kliento išankstinius apmokėjimus (dar vadinamus klientų depozitais).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e83c8be1b397f90445230835e415ea4fcea5a8d0bf695e6cc5eadc55275ded7f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768968"
---
# <a name="customer-prepayments"></a>Kliento išankstiniai mokėjimai

[!include [banner](../includes/banner.md)]

Kliento išankstiniai mokėjimai naudojami tada, kai gaunate mokėjimą iš kliento, bet nėra SF, pagal kurią būtų galima sudengti mokėjimą. Šie mokėjimų tipai dar vadinami klientų depozitais.

Išankstinių kliento mokėjimų nustatymo ir darbo su klientais procesą sudaro šie pagrindiniai veiksmai.

1. Sukurkite kliento registravimo profilį išankstiniams mokėjimams.
2. Nustatykite **Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu** parametrą.
3. Sukurkite kliento mokėjimų žurnalą ir kiekvienoje eilutėje **pažymėkite žymės langelį Išankstinio mokėjimo** žurnalo kvitas.
4. Registruokite kliento mokėjimų žurnalą.
5. Sugener pasirinkę SF sudengkite išankstinį mokėjimą naudodami puslapį **Sudengti atviras operacijas**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Sukurkite kliento registravimo profilį išankstiniams mokėjimams

Paprastai, kai priimate išankstinius apmokėjimus ar depozitus iš savo klientų prieš pritaikant prekes ar paslaugas, arba kol sistemoje yra SF, norėsite įrašyti grynuosius pinigus kaip įsipareigojimus, o ne kaip turtą savo sąskaitų lentelėje. Tačiau šių sumų įrašymo į jūsų DK reikalavimai gali skirtis, atsižvelgiant į šalį arba regioną. Todėl kreipkitės į savo apskait specialistus dėl bet kokių vietinių taisyklių, kurios yra taikomos.

Apskritai, registravimo šablono, kurį galima naudoti išankstiniams mokėjimams, sukūrimo procesas yra toks pat kaip ir kitų registravimo šablonų kūrimo procesas. Pirminis skirtumas yra pagrindinė sąskaita, kurią pasirenkate lauke **Suminė sąskaita**. Daugiau informacijos žr. [Kliento publikavimo profiliai](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Nustatyti kliento išankstinių mokėjimų parametrus

Yra du pagrindiniai gautinų sumų parametrai, kuriuos turite apsvarstyti konfigūruokite klientų išankstinių mokėjimų sistemą. Atlikite šiuos veiksmus, norėdami sukonfigūruoti parametrus.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
2. Pasirinktinas: Skirtuke **Didžioji knyga ir pardavimo mokesčiai** „FastTab“ **Mokėjimas** nustatykite **Išankstinio mokėjimo žurnalo kvito PVM** pasirinktį į **Taip**.
3. Lauke **Registravimo šablonas su išankstinio mokėjimo** žurnalo kvitu pasirinkite kliento registravimo šabloną, kuris bus naudojamas registruojant kliento išankstinius apmokėjimus.
4. Uždarykite puslapį.

## <a name="create-customer-prepayment-vouchers"></a>Kurti kliento išankstinio apmokėjimo kvitus

Kai sukuriate kliento mokėjimų žurnalą, kiekvienam išankstiniam mokėjimui turite nustatyti **išankstinio mokėjimo žurnalo** pasirinktį į **Taip** puslapyje **Kliento mokėjimo žurnalas**. Atlikite šiuos veiksmus norėdami sukurti kliento išankstinį mokėjimą.

1. Eikite į **Gautinos sumos \> Mokėjimai \> Klientų mokėjimo žurnalas**.
2. Pasirinkite **Naujas** žurnalui sukurti.
3. Lauke **Pavadinimas** pasirinkite norimo naudoti žurnalo pavadinimą.

    > [!IMPORTANT]
    > Jei nustatėte **PVM išankstinio mokėjimo žurnalo kvite** parinktį į **Taip** anstesnėje procedūroje, turite pasirinkti žurnalo pvadinimą, kuriame **Suma apima PVM** pasirinktą paramtrą. 

4. Pasirinktinai: Laukelyje **Aprašas** įveskite išsamų aprašą.
5. Pasirinkite **Eilutės**.
6. Jei nėra tuščios eilutės, pasirinkite **Nauja,** kad sukurtumėte eilutę.
7. Lauke **Data** įveskite datą, nuo kurios turi būti užregistruotas išankstinis mokėjimas.
8. Lauke **Klientas** pasirinkite klientą išankstiniam mokėjimui.
9. Pasirinktinai: Laukelyje **Aprašas** įveskite išsamų transakcijos aprašą.
10. Lauke **Kreditas** įveskite išankstinio mokėjimo sumą.
11. Lauke **Korespondentinė sąskaita** pasirinkite sąskaitą norėdami kompensuoti mokėjimą. Pavyzdžiui, pasirinkite banką arba pagrindinę sąskaitą, į kurios norite registruoti mokėjimą.
12. Lauke **Mokėjimo būdas** pasirinkite kliento mokėjimo metodą.
13. Skirtuke **Mokėjimas** nustatykite **išankstinio mokėjimo žurnalo** pasirinktį į **Taip**.
14. Su kiekvienu papildomu išankstiniu apmokėjimu, kuris turi būti užregistruotas, pakartokite veiksmus nuo 7 iki 13.
15. Pasirinkę **Publikuoti** užbaigsite žurnalą.

## <a name="settle-prepayments-with-invoices"></a>Išankstinių mokėjimų sudengimas su SF

Kliento mokėjimų darbo sritį **galite naudoti** norėdami lengvai rasti ir sudengti mokėjimus, kurie nebuvo visiškai sudengti.

1. Namų **skelbimų** skelbimų srityje pasirinkite kliento **mokėjimų išklotąją** sritį.
2. Kliento operacijų **skyriaus skirtuke** Mokėjimai **nesudengti ieškoti ir** pasirinkti sudengti norimą mokėjimą.
3. Pasirinkite **Nustatyti operacijas**
4. Pažymėkite **SF** ir mokėjimo, kuris bus sudengtas, žymės langelį Žymėti.
5. Pasirinkite **Registruoti**.

Daugiau informacijos apie tai, kaip sudengti atviras operacijas, ieškokite [Sudengimo peržiūra](/cash-bank-management/settlement-overview.md).
