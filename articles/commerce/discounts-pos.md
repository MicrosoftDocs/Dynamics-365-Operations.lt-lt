---
title: Nuolaidų rodymas EKA
description: Šioje temoje paaiškinama, kaip „Microsoft Dynamics 365 Commerce“ padeda pardavimo partneriams sužinoti apie akcijas ir kaip jos gali būti naudojamos kryžminiams ir papildomiems pardavimams.
author: ShalabhjainMSFT
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 9e3fa5030cb684c01153d255ca2bd34d9be7dc9945f0c7ec26985cf74540b73d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731672"
---
# <a name="show-discounts-in-pos"></a>Nuolaidų rodymas EKA

[!include [banner](includes/banner.md)]

Akcijos vaidina svarbų vaidmenį motyvuojant klientus, kurie priima pirkimo sprendimus. Pavyzdžiui, atostogos gali sudaryti didžiausią mažmenininkų pardavimo skaičių, nes visa mažmeninės prekybos rinka yra užtvindyta viliojančiomis akcijomis ir nuolaidomis. Jei parduotuvės darbuotojai žino ir supranta siūlomas akcijas, jie gali nesunkiai pasinaudoti šių nuolaidų privalumais, kad parduotų prekes kryžminio ir papildomo pardavimų būdais. Šioje temoje paaiškinama, kaip „Microsoft Dynamics 365 Commerce“ padeda pardavimo partneriams sužinoti apie akcijas ir kaip jos gali būti naudojamos kryžminiams ir papildomiems pardavimams.

## <a name="learn-about-store-discounts"></a>Sužinokite apie parduotuvių nuolaidas

„Commerce“ yra veiksmas pavadinimu „Peržiūrėti visas nuolaidas.“ Šis veiksmas parodo visas nuolaidas, kurios šiuo metu galioja parduotuvėje. Veiksmą „Peržiūrėti visas nuolaidas“ galima susieti su elektroninio kasos aparato (EKA) mygtuku, o tas mygtukas gali būti įtraukas į puslapius **Pasisveikinimas** arba **Operacija**. Toliau pateiktame paveikslėlyje pavaizduotas atverto **Visos nuolaidos** puslapio pavyzdys.

![Visų nuolaidų puslapis.](./media/View_all_discounts.png "Visų nuolaidų puslapis")

Kad parodytų nuolaidas, sistema ieško visų nuolaidų, atitinkančių vieną ar daugiau iš šių sąlygų:

- Nuolaidos kainų grupė atitinka parduotuvės kainų grupę.
- Nuolaidos kainų grupė susieta su priskyrimo ar lojalumo programa.
- Nuolaidos kainų grupė yra susieta su katalogu, kuris susietas su parduotuve.

**Visų nuolaidų** puslapyje rodomos tik kai kurios kupono nuolaidos, nes mažmenininkai paprastai sukuria tūkstančius kuponų ir atitinkamų nuolaidų unikaliems klientams, o šis puslapis nėra skirtas rodyti klientui būdingas nuolaidas. Kuponų nuolaidos rodomos tik tada, jei kiekvieno kupono antraštėje įgalinta parinktis **Taikyti be kupono kodo**. Tokiu atveju kasininkai gali taikyti kuponą neįvedant ar nenuskaitant jokio kupono kodo ar brūkšninio kodo.

Kai parinktis **Taikyti be kupono kodo** įjungta, atsiranda įvairių scenarijų. Pavyzdžiui, kasininkai gali suteikti klientams papildomas nuolaidas kliento nuraminimo tikslais arba dėl produkto defektų. Spausdintų kupono kodų ar brūkšninių kodų nereikia pateikit kasininkams. Užuot, kasininkai gali pasirinkti mygtuką **Taikyti kuponą**. Tada kuponas automatiškai taikomas operacijai. Jei kupono antraštėje yra keli kuponai, sistema automatiškai pasirenka pirmą aktyvų kupono operacijoje.

**Visų nuolaidų** puslapyje pardavimų darbuotojai taip pat gali ieškoti nuolaidų pagal raktinius žodžius. Raktinio žodžio ieška ieško laukuose, kuriuose yra nuolaidos pavadinimas ir nuolaidos aprašymas. Pardavimų darbuotojai taip pat gali filtruoti nuolaidas, atsižvelgiant į tai, ar nuolaidai reikalingas kupono kodas.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Kryžminis ir papildomas pardavimai naudojant nuolaidas

Kelių eilučių nuolaidos, pvz., kiekio nuolaidos, prekių rinkinių nuolaidos ir slenksčio nuolaidos, yra puikus būdas motyvuoti klientus pirkti daugiau produktų, kad būtų galima gauti didesnių nuolaidų. Todėl jie taip pat padeda didinti kliento krepšelio ir mažmeninės prekybos įplaukų dydį. Šias nuolaidas galima publikuoti „e-Commerce“ svetainėse, socialiniuose tinkluose ir reklaminėse juostose parduotuvėse.

Tačiau net naudojant visus šiuos viešumo metodus klientai gali praleisti galimybę pasinaudoti akcijų siūlomais privalumais. Tam, kad palengvintų su prekyba susijusių asmenų supratimą, kokios akcijos yra taikomos pasirinktai eilutei arba visam vežimėliui, mažmenininkai gali įtraukti mygtuką **"Peržiūrėti esamas nuolaidas"** veiksmą tinklo mygtukui **Perlaidos** puslapyje. Dėl to, su prekyba susiję asmenys gali pasirinkti perlaidos eilutę ir tuomet pasirinkti mygtuką, kuriuo rodomos nuolaidos, galimos pasirinktai eilutei. Be to, pardavimų darbuotojas gali pasirinkti kitą skirtuką, norėdamas rodyti visas operacijai taikomas nuolaidas. Svarbu pastebėti, kad **Peržiūrėti esamas nuolaidas** nerodo nuolaidų, kurios jau yra taikomos prekybos eilutei, nes nuolaidos informacija jau yra rodoma prekybos eilutėje. Šio scenarijaus tikslas yra tik parodyti dar netaikomas nuolaidas. Išimtis šiam atvejui yra nuolaidos, kurios yra taikomos pagal kuponą pažymėtą „Taikyti be kupono kodo". Dėl to su prekyba susijusiam asmeniui tampa lengva pašalinti jau pritaikytą kuponą.

Puslapyje **Visos nuolaidos** rodomos tik nuolaidos, kurios nekonkuruoja su jokiomis pritaikytomis nuolaidomis. Taip užtikrinama, kad, jei pardavimų darbuotojas informuos klientą apie nuolaidą, o klientas imsis reikalaujamo veiksmo (pvz., klientas nusiperka dar vieną prekę, kad gautų 10 procentų nuolaidą), nuolaida taikoma operacijai. Kuponų nuolaidos rodomos tik tada, kai kupono antraštėje įgalinta parinktis **Taikyti be kupono kodo**.

Paprastame scenarijuje, kur visos nuolaidos turi tą pačią pirmenybę, nuolaidos sutapimo režimas yra **skaičiuojamas**, o nuolaidos sutapimo valdiklis nustatytas į **Geriausia kaina ir apskaičiuota pirmenybėje, niekada neskaičiuoti už pirmenybės ribų**, puslapyje **Visos nuolaidos** rodomos visos produktui prieinamos nuolaidos, nes visos nuolaidos yra apskaičiuojamos ir nekonkuruoja tarpusavyje.

Toliau pateiktoje iliustracijoje pristatyta logika, apibrėžianti, kurios nuolaidos rodomos išplėstiniuose scenarijuose, pvz., kai nuolaidos sutapimo režimas yra **Geriausia kaina** ar **Išskirtinis**, ir naudojami du ar daugiau prioritetų. Šiuose scenarijuose rodomos nuolaidos yra paveiktos, atsižvelgiant į tai, ar nuolaidos sutapimo valdiklis nustatytas į **Geriausia kaina ir apskaičiuota pirmenybėje, niekada neskaičiuoti už pirmenybės ribų** arba **Geriausia kaina tik pirmenybėje, visada skaičiuoti už pirmenybės ribų**.

Toliau pateiktoje iliustracijoje vaizduojama logika, naudojama, kai nuolaidos sutapimo valdiklis nustatomas kaip **Geriausia kaina ir apskaičiuota pirmenybėje, niekada neskaičiuoti už pirmenybės ribų**.

![Logika, skirta „Geriausia kaina ir apskaičiuota pirmenybėje, niekada neskaičiuoti už pirmenybės ribų“.](./media/Model_1.png "Logika, skirta „Geriausia kaina ir apskaičiuota pirmenybėje, niekada neskaičiuoti už pirmenybės ribų“").

Toliau pateiktoje iliustracijoje vaizduojama logika, naudojama, kai nuolaidos sutapimo valdiklis nustatomas kaip **Geriausia kaina tik pirmenybėje, visada skaičiuoti už pirmenybės ribų**.

![Logika, skirta „Geriausia kaina tik pirmenybėje, visada skaičiuoti už pirmenybės ribų“.](./media/Model_2.png "Logika, skirta „Geriausia kaina tik pirmenybėje, visada skaičiuoti už pirmenybės ribų“").


[!INCLUDE[footer-include](../includes/footer-banner.md)]