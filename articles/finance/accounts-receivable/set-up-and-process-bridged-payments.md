---
title: Nustatyti ir apdoroti tarp nustatytus mokėjimus
description: Šioje temoje paaiškinama, kaip nustatyti ir apdoroti tarp nustatytus kliento mokėjimus. Tarpinis mokėjimas yra mokėjimas, kuris dviem veiksmais registruojamas DK.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca93d99ce04e607b137a2755d507022a33ab1be8
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734197"
---
# <a name="set-up-and-process-bridged-payments"></a>Nustatyti ir apdoroti tarp nustatytus mokėjimus

[!include [banner](../includes/banner.md)]

Tarpinis mokėjimas yra mokėjimas, kuris dviem veiksmais registruojamas DK. Paprastai šis būdas naudojamas, kai **mokėjimo** būdas nustatytas kaip Bankas, ir operacijas į banko sąskaitą reikia užregistruoti tik tada, kai operacija išvalo banką. Tačiau galite naudoti ją ir DK sąskaitai. Šiuo atveju, apdorodama tarpąjį registravimą sistema perkelia sumą iš vienos pagrindinės sąskaitos į kitą.

Galite sukurti tarpinius mokėjimus iš mokėtinų sumų arba gautinų sumų. Nors šioje temoje paaiškinama, kaip konfigūruoti tarpinius gautinų sumų registravimus, mokėtinų sumų operacijų veiksmai yra panašūs.

## <a name="set-up-bridging-posting"></a>Nustatyti tarpinę registravimą

Norėdami naudoti tarpinę registravimą, turite nustatyti vieną ar daugiau mokėjimo būdų, kad jie galėtų naudoti **tarpinę registravimo** metodą. Tada turite pasirinkti tarpinę sąskaitą.

1. Eiti į **gautinų sumų &gt; mokėjimo nustatymo &gt; mokėjimo metodus**.
2. Pasirinkite esamą mokėjimo būdą, kad įgalintumėte tarpąjį registravimą. Arba galite sukurti naują mokėjimo būdą.
3. Pažymėkite žymės **langelį Tarpinis** registravimas.
4. Tarpinės **sąskaitos lauke pasirinkite** pagrindinę sąskaitą, į kurią mokėjimai turėtų būti registruojami prieš išvalant juos į banko sąskaitą.
5. Uždarykite puslapį.

## <a name="process-and-transfer-bridging-posting"></a>Apdoroti ir perkelti tarpinę registravimą

Norėdami sukurti ir apdoroti tarpinį registravimą, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos &gt; Mokėjimai &gt; Klientų mokėjimo žurnalas**.
2. Pasirinkite **Naujas** žurnalui sukurti.
3. **Lauke Pavadinimas** pasirinkite pavadinimą.
4. Įtraukite eilutes į kliento mokėjimų žurnalą ir pasirinkite mokėjimo būdą, kuris sukonfigūruotas naudoti tarpinis registravimas.
5. Registruoti žurnalą. Operacijos bus registruojamos pagrindinėje sąskaitoje, kurią pasirinkote **ankstesnės procedūros tarpinės** sąskaitos lauke.

Kai operacijos išvalo banką ir norite perkelti mokėjimą iš tarpinės sąskaitos į nurodytą mokėjimo metodo mokėjimo sąskaitą, atlikite šiuos veiksmus.

1. Eikite į **Didžioji knyga &gt; Žurnalų įrašai &gt; Bendrieji žurnalai**.
2. Pasirinkite **Naujas** žurnalui sukurti.
3. **Lauke Pavadinimas** pasirinkite pavadinimą.
4. Pasirinkite **eilutes,** kad atidarytumėte žurnalo informaciją.
5. Pasirinkti **funkcijas &gt; Tarpines operacijas**.
6. Pažymėkite kiekvieną mokėjimą, kuris buvo išvalytas, tada pasirinkite **Priimti**.
7. Registruoti žurnalą.
