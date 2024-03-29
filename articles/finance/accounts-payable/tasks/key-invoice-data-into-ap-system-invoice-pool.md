---
title: Pagrindiniai SF duomenys apie AP sistemą naudojant SF telkinį
description: Šiame straipsnyje aprašoma, kaip naudoti SF registrą SF kurti.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc3f1107a9564120aae77a75e6232879bf3c51af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858446"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Pagrindiniai SF duomenys apie AP sistemą naudojant SF telkinį

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti SF registrą SF kurti. Tada naudodami SF telkinį sugretinkite SF su pirkimo užsakymu ir baikite išlaidas tiekėjo SF puslapyje.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai**.
2. Pasirinkite **Naujas**, kad sukurtumėte pirkimo užsakymą.
3. Lauke **Tiekėjo sąskaita** išplečiamajame sąraše pasirinkite tiekėją. Pavyzdžiui, pasirinkite tiekėją **1001**.
4. Pasirinkite **Gerai**.
5. Lauke **Prekės numeris** išplečiamajame sąraše pasirinkite paslaugų prekės numerį. Pavyzdžiui, pasirinkite **S0001**. Grynoji suma yra 75,00.  Tai suma, kurios tikėsimės SF.  
6. Veiksmų srityje pasirinkite **Pirkimas**.
7. Pasirinkite **„Patvirtinti“**.

## <a name="create-and-post-and-invoice"></a>Kurti ir registruoti SF
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų registras**.
2. Pasirinkite **Naujas**.
3. Atidarykite peržvalgą, kad pasirinktumėte norimo naudoti SF registro pavadinimą.
4. Pasirinkite norimo naudoti SF registro pavadinimą.
5. Pasirinkę **Eilutės**, atidarykite registrą ir įveskite išlaidų eilutes.
6. Peržvalgoje pasirinkite tiekėją. Pavyzdžiui, pasirinkite tiekėją **1001**.
7. Lauke **Sąskaita faktūra** įveskite SF numerį.
8. Lauke **Aprašo laukas** surinkite reikšmę.
9. Lauke **Kreditas** įveskite skaičių.
10. Lauke **Pirkimo užsakymas** atidarykite išplečiamąjį sąrašą ir pasirinkite anksčiau sukurtą pirkimo užsakymą.
11. Lauke **Patvirtino** išplečiamajame sąraše pažymėkite tvirtintoją ir spustelėkite **Pasirinkti**, kad jį pasirinktumėte.
12. Pasirinkite **Registruoti**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Atidarykite SF iš telkinio ir sugretinkite ją su pirkimo užsakymu, kad užbaigtumėte SF procesą
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų telkinys**.
2. Pasirinkę **Pirkimo užsakymas**, sukursite tiekėjo sąskaitą faktūrą pagal telkinyje esančią sąskaitą faktūrą.
3. Pasirinkite sąskaitą faktūrą, kurią norite peržiūrėti.
4. Pasirinkę **Naujinti gretinimo būseną**, užbaikite gretinimą.
5. Veiksmų srityje pasirinkite **Parinktys**.
6. Pasirinkite **Keisti rodinį**.
7. Pasirinkite **Tinklelio rodinys**.
8. Pasirinkite **Registruoti**.
9. Uždarykite puslapį.
10. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Tiekėjai > Tiekėjai**.
11. Pasirinkite tiekėją, kuris buvo ant pirkimo užsakymo. Pavyzdžiui, pasirinkite tiekėją **1001**.
12. Veiksmų srityje pasirinkite **Tiekėjas**.
13. Pasirinkite **Operacijos**.
14. Pasirinkite savo sukurtą sąskaitą faktūrą. SF registro kaupimas buvo atšauktas ir užregistruotas į atitinkamą išlaidų sąskaitą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
