---
title: Uždarymo metų pabaigoje trūkstami pradiniai balansai
description: Šioje temoje paaiškinama, kodėl uždarius metus gali trūkti pradinių balansų ir kaip atkurti tuos balansus, jei jų trūksta.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028577"
---
# <a name="year-end-close-missing-opening-balances"></a>Uždarymo metų pabaigoje trūkstami pradiniai balansai

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kodėl uždarius metus gali trūkti pradinių balansų ir kaip atkurti tuos balansus, jei jų trūksta.

### <a name="symptom"></a>Požymis

Kodėl nėra pradinių balansų paleidus didžiosios knygos uždarymą metų pabaigoje? 

### <a name="resolution"></a>Sprendimas

Štai ką reikia patikrinti, jei metus uždarėte didžiojoje knygoje ir vėliau sugeneravote bandomąjį balansą, kuriame nerodomi kitų finansinių metų pradiniai balansai.

Jei laukas **Anuliuoti ankstesnį uždarymą** nustatytas į **Taip**, ankstesnis tų pačių finansinių metų uždarymas metų pabaigoje yra atšaukiamas. Paleidus uždarymo metų pabaigoje atšaukimo procesą, visi uždarymo ir pradinių balansų įrašai bus panaikinti, tarytum metai niekada nebūtų uždaryti. Kvitai taip pat panaikinami. Uždarymo metų pabaigoje procesas nebus paleistas automatiškai. Būtina iš naujo pradėti procesą šį kartą parinktį **Anuliuoti ankstesnį uždarymą** atnaujinant į **Ne**.

Šis scenarijus įtrauktas į DUK apie uždarymą metų pabaigoje temą. Daugiau informacijos ieškokite dalyje [DUK apie metų pabaigos veiklas](faq-year-end-activities.md).

### <a name="symptom"></a>Požymis

Uždarymas metų pabaigoje buvo paleistas parinktį **Anuliuoti ankstesnį uždarymą** nustačius į **Ne**, tačiau vis dar neturiu finansinių metų pradinių balansų.

### <a name="resolution"></a>Sprendimas

Pirmiausia patikrinkite paketinės užduoties būseną. Uždarant metus atliekamos įvairios atskiros užduotys, tačiau svarbiausias veiksmas yra paketinė užduotis su užduoties aprašu **5.0.0 veiksmas**. Atliekant šį veiksmą didžiojoje knygoje registruojamos atidarymo operacijos ir pasirinktinai uždaromos operacijos. 

[![Paketo retrospektyvų sąrašas](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Jei šis veiksmas atliktas sėkmingai, bet puslapyje **Bandomojo balanso užklausa** (**Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas**) nematote pradinių balansų, peržiūrėkite uždarymo metų pabaigoje paketinės užduoties rezultatus, kad sužinotumėte, ar perkėlimo balansų veiksmas atliktas sėkmingai.

[![Uždarymo metų pabaigoje paketinės užduoties rezultatai](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Jei šis veiksmas dėl kokių nors priežasčių nepavyko, atidarymo (ir pasirinktinai uždarymo) operacijos greičiausiai buvo sėkmingai užregistruotos. Galite patikrinti, ar didžiosios knygos operacijos buvo sėkmingai užregistruotos, puslapyje **Kvito operacijų užklausa** nurodydami kvito numerį ir datą, pateiktą uždarymo metų pabaigoje dialogo lange jūsų uždarytiems metams (**Didžioji knyga > Užklausos ir ataskaitos > Kvito operacijos**).

[![Kvito operacijų užklausa](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Jei yra atidarymo (ir pasirinktinai uždarymo) kvitai, metų pabaigos dar kartą uždaryti nereikia. Informacijos apie tai, kaip pereiti prie kitų veiksmų, ieškokite kitame skyriuje.

### <a name="symptom"></a>Požymis

Veiksmas „Atkurti balansus“ uždarymo metų pabaigoje nepavyko, ar man reikia iš naujo paleisti visą uždarymo metų pabaigoje procesą?

### <a name="resolution"></a>Sprendimas

Veiksmu Atkurti balansus atnaujinami didžiosios knygos balansai, kurie naudojami generuojant bandomojo balanso užklausą.  Tai paskutinis veiksmas uždarymo metų pabaigoje procese.  Jei šis veiksmas yra vienintelis nesėkmingas veiksmas, didžiosios knygos operacijos sėkmingai užregistruotos.  Neturite dar kartą paleisti uždarymo metų pabaigoje. Galite rankiniu būdu paleisti balansų atkūrimo procesą puslapyje **Finansinių dimensijų rinkiniai** (**Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinių dimensijų rinkiniai**).

[![Mygtukas Atkurti balansus puslapyje Finansinių dimensijų rinkiniai](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Jei šis veiksmas užtrunka ilgai, rekomenduojame peržiūrėti geriausią finansinių dimensijų rinkinių praktiką, aprašytą dalyje [Geriausia finansinių dimensijų rinkinių naujinimo praktika](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

