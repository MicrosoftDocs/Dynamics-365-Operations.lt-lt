---
title: "Gamybos užsakymų kaštų analizė"
description: "Šiame straipsnyje pateikiama informacija apie galimą atlikti baigtų ir dabartinių gamybos užsakymų išlaidų analizę. Analizuoti įvertintas savikainas ir faktines išlaidas galite naudodami puslapį Kainos skaičiavimas arba ataskaitą Išlaidų įvertinimas ir įkainojimas. Galite peržiūrėti kiekvienos sudedamosios prekės, nukreipimo operacijos ir netiesioginių išlaidų informaciją apie numatytąsias ir faktines išlaidas (ir kiekį)."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1905749fa8db33b960d082d1e22f11206b400eb0
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="production-order-cost-analysis"></a>Gamybos užsakymų kaštų analizė

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie galimą atlikti baigtų ir dabartinių gamybos užsakymų išlaidų analizę. Analizuoti įvertintas savikainas ir faktines išlaidas galite naudodami puslapį Kainos skaičiavimas arba ataskaitą Išlaidų įvertinimas ir įkainojimas. Galite peržiūrėti kiekvienos sudedamosios prekės, nukreipimo operacijos ir netiesioginių išlaidų informaciją apie numatytąsias ir faktines išlaidas (ir kiekį).

Gamybos užsakymo faktinės išlaidos pagrįstos suvartotų medžiagų ir nukreipimo operacijų ataskaitomis. Išsamias operacijas, susijusias su suvartotomis medžiagomis, nukreipimo operacijomis ir netiesioginėmis išlaidomis, rasite puslapyje **Gamybos registravimas**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Užbaigto gamybos užsakymo nuokrypių analizė
Nuokrypiais palyginamos deklaruotos gamybos veiklos ir apskaičiuotos standartinės gamybos prekės išlaidos. Nuokrypiais nelyginama su gamybos užsakymo įvertintomis savikainomis. Deklaruotos gamybos veiklos apima medžiagos suvartojimą, nukreipimo operacijas ir susijusias netiesiogines išlaidas bei baigtu paskelbtą kiekį. Skaičiuojami tolesni keturi nuokrypių tipai.

-   Partijos dydžio nuokrypis
-   Gamybos kiekio nukrypimas
-   Gamybos kainų nuokrypis
-   Gamybos pakaitalo nukrypimas

Šioje diagramoje rodomi keturis nuokrypiai, kurie parodo skirtumą tarp gamybos užsakymo faktinių išlaidų ir paskaičiuotų išlaidų įrašuose, gamybos užsakymo pabaigoje. 

![Nuokrypiai, nurodantys skirtumus baigtame gamybos užsakyme](./media/control.jpg) 

Gamybos nuokrypius galite analizuoti naudodami puslapį **Nuokrypis** arba ataskaitą **Gamybos nuokrypis**. Norėdami nuokrypius peržiūrėti išsamiai, pagal prekę ir operacijų išteklių ar pagal išlaidų grupę, naudokite rodymo parinktis. Išlaidų paskirstymo strategija atsargų parametruose lemia ar nukrypimai sekami išlaidų grupėse. Taip pat peržiūrėti nuokrypių suvestinę galite naudodami **vieno**, **kelių** ir **bendro** rodymo parinktis. Išsami informacija apie nuokrypius gali padėti suprasti kiekvieno nuokrypio šaltinį. Norėdami numatyti nuokrypius prieš baigdami gamybos užsakymą, analizuokite išsamią informaciją, kuri pateikta ataskaitoje **Išlaidų įvertinimas ir įkainojimas**.

## <a name="cost-analysis-for-current-production-orders"></a>Dabartinių gamybos užsakymų išlaidų analizė
Atskirose ataskaitose pateikiama informacija apie kiekvieną operacijų tipą. Naudokite šias ataskaitas ataskaitose pateikiamos gamybos veiklos išlaidoms analizuoti. Rodoma tik esamų gamybos užsakymų, kurių būsena **Pradėtas** arba **Paskelbtas baigtu**, informacija.

-   **Apdorojamos medžiagos** − šioje ataskaitoje išvardijamos važtaraščio operacijos, kurios paskelbtos pagal esamus gamybos užsakymus nuo nurodytos operacijos datos. Ataskaitoje rodomas išduotas komponentų kiekis ir kiekvienos operacijos išlaidų suma. Naudokite vienos sudedamosios prekės pasirinkimo kriterijus. Pavyzdžiui, galite spausdinti informaciją apie komponentų išdavimo kiekį pagal taikomus gamybos užsakymus. Išduotas kiekis nėra atnaujinamas praneštais baigtais pirminės prekės užsakymais. Taip gali būti apskaičiuojamas per didelis faktinis gamyboje naudojamas žaliavų kiekis.
-   **Nebaigta gamyba** − šioje ataskaitoje išvardijamos maršruto operacijos (arba užduoties operacijos), kurios paskelbtos pagal esamus gamybos užsakymus nuo nurodytos operacijos datos. Šioje ataskaitoje pateikiamos valandos, suma ir kiekis (prekių ir klaidų), kurio ataskaitos pateiktos kiekvienai operacijai. Joje taip nurodoma tokia informacija kaip operacijos numeris, operacijos ID ir operacijų išteklius. Be to, šioje ataskaitoje rodomas bendras visų operacijų laikas ir suma pagal gamybos užsakymą ir baigtu paskelbtas kiekis.
-   **Vykdomos netiesioginės išlaidos** − ataskaitoje išvardytos netiesioginės išlaidos, patirtos dėl gamybos užsakymų. Šie duomenys pateikiami atsižvelgiant į ataskaitose pateiktą suvartojimą nukreipimo operacijų metu ir komponentus nuo nurodytos operacijų datos. Ataskaita nurodo netiesioginių išlaidų tipą (papildomas mokestis ar tarifas), netiesioginių išlaidų įkainojimo lapo kodą ir kiekvienos operacijos išlaidų sumą. Ataskaitoje neteikiama informacijos apie technologinę kortelę ar išrinkimo dokumento operaciją, sugeneravusią netiesiogines išlaidas.
-   **Vykdomas gamybos įkainojimas** − šioje ataskaitoje išvardytas bendras medžiagų suvartojimas, nukreipimo operacijos ir netiesioginės išlaidos palyginti su gamybos užsakymais nuo nurodytos operacijos datos.
-   **Baigtos prekės** − šioje ataskaitoje išvardyti esami gamybos užsakymai ir paskelbtos baigtomis operacijos nuo nurodytos operacijos datos.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Bendrieji gamybos nuokrypių šaltiniai](common-sources-of-production-variances.md)




