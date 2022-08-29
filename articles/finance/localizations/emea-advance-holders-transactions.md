---
title: Išankstinio savininko operacijos
description: Sužinokite, kaip dirbti su išankstinio savininko operacijomis Microsoft Dynamics "365 Finance".
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 262554
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
ms.openlocfilehash: c192a5db65b2f0f98fad5a11d968034c984659d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267139"
---
# <a name="advance-holder-transactions"></a>Išankstinio savininko operacijos

[!include [banner](../includes/banner.md)]

Sužinokite, kaip tvarkyti avanso turėtojo operacijas.

Šių darbuotojų, kurie yra avanso turėtojai, operacijas galima registruoti naudojant avanso turėtojo sąskaitas. Darbuotojo ID, kuris priskirtas kiekvienam išankstiniams savininkui, galima naudoti norint sekti visas avanso turėtojo operacijas. Šis numeris nuskaitomas kaip avanso turėtojo operacijų sąskaitos numeris puslapiuose **Bendrieji žurnalai** ir **Avanso turėtojo operacijos**.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Pirkimo užsakymo su avanso turėtojo informacija kūrimas ir registravimas
Daugiau bendros informacijos apie pirkimo užsakymus žr. temoje [Pirkimo užsakymo apžvalga](../../supply-chain/procurement/purchase-order-overview.md). Jei tiekėjo SF sukuriama ir užregistruojama su avanso turėtojo informacija, avanso turėtojo balansas bus užregistruotas darbuotojo balanso sąskaitoje, o ne tiekėjo balanso sąskaitoje. Norėdami avanso turėtojo informaciją įtraukti į pirkimo užsakymą, atlikite tolesnius veiksmus.

-   Dalies **Kaina ir nuolaida** lauke **Mokėjimo sąlygos** pasirinkite mokėjimo sąlygą. <!---For more information about **Terms of payment**, see [Define vendor payment terms](../accounts-payable/tasks/define-vendor-payment-terms.md).--> Pasirinkite mokėjimo sąlygą, kurios parinktis **Iš avanso turėtojo**, esanti puslapyje **Mokėjimo sąlygos**, pažymėta. Norėdami gauti daugiau informacijos apie avanso turėtojų mokėjimo sąlygų nustatymą, žr. [Avanso turėtojų apžvalga](emea-advance-holders.md).
-   „FastTab“ **Kaina ir nuolaida** lauke **Avanso turėtojas** pasirinkite pirkimo užsakymo avanso turėtoją.

Pirkimo užsakymo registravimo proceso metu sukuriamos dvi tiekėjo operacijos su priešingomis sumomis ir viena avanso turėtojo operacija. Sukuriama tik viena tiekėjo operacija be avanso turėtojo informacijos.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Avanso turėtojo balanso sudengimas per banką
Kai avanso turėtojų balansus sudengiate per banką, žurnalo įrašai apie avanso turėtojo balansų uždarymą sukuriami pagrindiniame žurnale. Žurnalo ir banko kodus galite nustatyti puslapio **Mokėtinų sumų parametrai** dalyje **Avanso turėtojai**. Norėdami gauti daugiau informacijos, žr. [Avanso turėtojų apžvalga](emea-advance-holders.md). Norėdami uždaryti avanso turėtojo balansą per banką, atidarykite **Mokėtinos sumos** &gt; **Avanso turėtojai** &gt; **Avanso turėtojai**. Veiksmų srityje spustelėkite mygtuką **Balansas** ir tada spustelėkite **Uždaryti per banką**. Puslapyje **Uždaryti per banką** įveskite toliau nurodytą informaciją.

| Laukas                    | Aprašymas |
|------------------------------|-------------------|
| **Mokėjimo data**          | Įvesti mokėjimo registravimo datą.|
| **Suma, skirta perkelti** | Įveskite balanso sumą uždarymo metu. Suma, kuri yra nurodyta formos **Balansas** lauke **Suma**, rodoma pagal numatytuosius parametrus. |
| **Automatiškai**                | Norėdami kurti ir registruoti žurnalą, kuris yra iš anksto nustatytas puslapyje **Gautinų sumų parametrai**, pažymėkite žymės laukelį **Automatiškai**.|

## <a name="settle-advance-holder-balances-via-cash"></a>Avanso turėtojo balanso sudengimas per kasą
Kai avanso turėtojų balansus sudengiate per kasą, žurnalo įrašai apie avanso turėtojo balansų uždarymą sukuriami važtaraščių žurnale. Žurnalo ir kasos kodus galite nustatyti puslapio **Mokėtinų sumų parametrai** skirtuke **Avanso turėtojai**. Norėdami gauti daugiau informacijos, žr. [Avanso turėtojų apžvalga](emea-advance-holders.md). Norėdami uždaryti avanso turėtojo balansą per kasą, atidarykite **Mokėtinos sumos** &gt; **Avanso turėtojai** &gt; **Avanso turėtojai**. Veiksmų srityje spustelėkite mygtuką **Balansas** ir tada spustelėkite **Uždaryti per kasą**. Puslapyje **Uždaryti per kasą** įveskite toliau nurodytą informaciją.

| Laukas                    | Aprašymas
|------------------------------|-----------------|
| **Mokėjimo data**          | Įvesti mokėjimo registravimo datą.|
| **Suma, skirta perkelti** | Įveskite balanso sumą uždarymo metu. Suma, kuri yra nurodyta formos **Balansas** lauke **Suma**, rodoma pagal numatytuosius parametrus. |
| **Automatiškai**                | Norėdami automatiškai kurti ir registruoti žurnalą, kuris yra iš anksto nustatytas puslapyje **Gautinų sumų parametrai**, pažymėkite žymės laukelį **Automatiškai**.     |

Apdorojus važtaraščių žurnalą, jei suma, esanti lauke **Suma, skirta perkelti** yra neigiama, uždarius balansą generuojamas avanso turėtojo išmokėjimo kvitas. Jei suma lauke **Suma, skirta perkelti** yra teigiama, generuojamas kompensacijos kvitas.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Išankstinis mokėjimas darbuotojui (Rytų Europa)](tasks/advance-payment-employee.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
