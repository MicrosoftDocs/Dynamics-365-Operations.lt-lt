---
title: Atsargų uždarymas
description: Kaip išdavimo operacijų su gavimo operacijomis proceso dalį, taip pat galite atnaujinti didžiąją knygą, kad joje atsispindėtų atlikti pakeitimai.
author: AndersGirke
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d55ee9a851e2a7bfbba7d60b0b1fc774c4f6c170
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830321"
---
# <a name="inventory-close"></a>Atsargų uždarymas

[!include [banner](../includes/banner.md)]

Kaip išdavimo operacijų su gavimo operacijomis proceso dalį, taip pat galite atnaujinti didžiąją knygą, kad joje atsispindėtų atlikti pakeitimai.

Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Vykstant sudengimo procesui, galite nurodyti, kad būtų atnaujinta didžioji knyga ir joje atsispindėtų atlikti koregavimai. Tačiau, kol neuždaromos atsargos ar nevykdomas perskaičiavimas, išdavimo operacijos registruojamos pagal paskaičiuoto slankiojo vidurkio savikainą. 

Uždarę atsargas, nebegalėsite registruoti laikotarpiais iki atsargų uždarymo datos, kurią nustatėte, nebent atšauksite baigtą atsargų uždarymo procesą. Pvz., jei atliekamas laikotarpio, kuris baigiasi sausio 31 d., atsargų uždarymas, negalite registruoti operacijų, kurių data yra ankstesnė už sausio 31 d. 

Atsargų prekės priskiriamos vienam iš dviejų atsargų tipų: prekių arba aptarnavimo. Uždarant atsargas su abiem tipais atliekamos tos pačios funkcijos. Tačiau uždarant aptarnavimo prekių atsargas išdavimai vis tiek sudengiami pagal gavimus. 

Kaip dažnai vykdomas atsargų uždarymo procesas, priklauso nuo įmonės. Tačiau padėti nustatyti, kaip dažnai reikėtų atlikti atsargų uždarymą, turėtų operacijų apimtis. Paprastai, dauguma įmonių atsargų uždarymus vykdo kartu su jų mėnesio pabaigos uždarymo ir suderinimo procedūromis.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Atsargų perskaičiavimas ir didžioji knyga
Jei per mėnesį ar kitą operacijų laikotarpį reikalingi atsargų ir didžiosios knygos koregavimai, galite vykdyti atsargų perskaičiavimą, o ne atsargų uždarymą. Atsargų perskaičiavimas atlieka atsargų operacijų koregavimą, bet neatlieka atsargų operacijų sudengimo. 

Perskaičiuojant atsargas, pakoreguojamos turimos atsargos, koreguojamos atsargų operacijos ir vykdomas atsargų perskaičiavimas ir atsargų uždarymas. Šios užduotys paveikia bet kurią DK sąskaitą, kuri susieta su pradine atsargų operacija. 

**Pavyzdys** 

Kai pirkimo užsakymą kuriate iš pardavimo užsakymo, atnaujinamos originalaus pardavimo užsakymo DK sąskaitos. Net jei šiai prekei priskirtos prekių grupės DK sąskaitos nuo pardavimo užsakymo užregistravimo pasikeitė ir sukurta atsargų perskaičiavimo koregavimo suma, koregavimo suma užregistruojama į originalias DK sąskaitas. Pakoreguota suma nėra užregistruojama į naujas DK sąskaitas, kurios yra joms priskirtos. 

Kai naujinimas atliktas, galite peržiūrėti DK kvitą, užregistruotą dėl vienos iš šių užduočių.

1.  Puslapio **Uždarymas ir koregavimas** skirtuke **Peržiūra** pasirinkite norimą peržiūrėti atnaujinimą.
2.  Spustelėkite **Informacija**, tada pasirinkite **Kvitas**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Atsargų uždarymo proceso poveikis didžiajai knygai
Keletas užduočių, kurias galite atlikti puslapyje **Uždarymas ir koregavimas**, lemia didžiosios knygos atnaujinimą. Pvz., DK atnaujinama atliekant turimų atsargų koregavimą, atsargų operacijų koregavimą, vykdant atsargų perskaičiavimą ir atsargų uždarymą. 

DK sąskaitos, atnaujinamos dėl šių užduočių, yra susietos su pradine atsargų operacija. Pvz., jeigu pardavimo užsakymas sudengiamas su pirkimo užsakymu, pakoreguojamos DK sąskaitos, naudotos pirminiam pardavimo užsakymui. Tai atliekama net jei šiai prekei priskirtos prekių grupės DK sąskaitos pakeičiamos po to, kai užregistruojamas pardavimo užsakymas. Kai atsargų uždarymas sukuria sudengimo sumą, sudengimo suma vis tiek užregistruojama pirminėse DK sąskaitose, o ne naujose prekei priskirtų DK sąskaitose. DK taip pat gali būti atnaujinta, jei atšauksite atsargų uždarymą. 

> [!NOTE] 
> - Atsargų uždarymas yra būtinas mėnesio pabaigos uždarymo procedūros veiksmas visų atsargų modeliams, išskyrus slankiojo vidurkio.  Jūs gausite įspėjimą, jei bandysite uždaryti finansinį laikotarpį prieš tai neatlikę atsargų uždarymo iki laikotarpio pabaigos datos.
> - Prieš vykdydami uždarymo procedūrą, galite peržiūrėti prekių, kurios negali būti sudengtos atnaujinant, sąrašą.
> - Rekomenduojame vykdyti atsargų uždarymą ne piko valandomis, kad skaičiavimo ištekliai būtų paskirstyti tolygiau.

## <a name="the-inventory-close-log"></a>Atsargų uždarymo žurnalas
Kai atsargų uždarymas baigtas, pranešimų centro pranešimas gali jums pranešti, kad vieneto savikaina gali būti neteisinga, nes operacijos nepavyko visiškai sudengti. 

Prieš rodydama šį pranešimą programa sistema praneš prekės numerį ir paveiktą operaciją. Šis pranešimas informuos, kad šioje operacijoje naudojama savikainos suma nebuvo atnaujinta dėl atsargų uždarymo. Šis pranešimas rodomas, kai negalima sudengti išdavimo tipo operacijos. 

Atsargų uždarymo proceso metu sistema tikrina kiekvieną finansinę dimensiją, kad nustatytų, ar iki nurodytos uždarymo datos yra daugiau išdavimų negu gavimų. Tokio tipo disbalansas gali atsirasti, kai pirkimo užsakymo atsargų operacija nebūna galutinai finansiškai užregistruota, arba kol negauta tiekėjo SF, arba jei į aukštesnį gamybos lygį įtrauktas KS komponentas nėra finansiškai užregistruotas. (Antrinė gamyba neįtraukiama skaičiuojant savikainą.) Tokiu atveju vėlesnis uždarymas nepakoreguos visų išdavimų pagal teisingą savikainą, nes nėra pakankamai informacijos apie gavimą. 

Po kiekvieno uždarymo procedūros vykdymo sistema nurodo, ar žurnalas su perspėjimais saugomas ir ar jį galima peržiūrėti. 

Jei pranešime gaunate daug perspėjimų, rekomenduojame atlikti tolesnius veiksmus.

-   Finansiškai atnaujinkite gavimus.
-   Paankstinti uždarymo datą.
-   Perskaičiuokite verslo procedūras.

Tam tikromis aplinkybėmis gavus perspėjimų neįmanoma nieko padaryti. Pavyzdžiui, jei naudojamas žymėjimas ir pažymėto pirkimo užsakymo finansinė data yra vėlesnė už uždarymo datą, uždarymo datos pakeisti negalima.

## <a name="reversing-a-completed-inventory-close"></a>Užbaigto atsargų uždarymo atšaukimas
Kartais jums gali reikėti atšaukti atliktą atsargų uždarymą, taip grąžinant sudengimus į anksčiau, prieš koregavimą, buvusią būseną. Kai atšaukiate atliktą atsargų uždarymą, atsargos vėl atidaromos, kad būtų galima skelbti laikotarpiu, kurį apima atsargų uždarymas. Susiję keitimai taip pat gali būti atliekami didžiojoje knygoje. Baigę koreguoti galite vėl paleisti atsargų uždarymą laikotarpiu, su kuriuo dirbate. 

> [!NOTE] 
> Vėl atidaryti galima tik paskutinį uždarytą atsargų laikotarpį. Norėdami atšaukti ankstesnį atsargų uždarymą, po vieną, pradėdami nuo naujausio, turite atšaukti kiekvieną tolesnį atsargų uždarymą.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]