---
title: Ilgalaikio turto integravimas
description: Ilgalaikį turtą galima integruoti į didžiąją knygą, atsargų valdymą, gautinas sumas ir mokėtinos sumas. Taip pat galite nustatyti, kad ilgalaikis turtas būtų integruojamas į pirkimo užsakymus.
author: ShylaThompson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 290cf4bb28c07dc8ba11250da0fa3af5a8e9cfd7b7c36f688c7f40742dc57b31
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761283"
---
# <a name="fixed-assets-integration"></a>Ilgalaikio turto integravimas

[!include [banner](../includes/banner.md)]

Ilgalaikį turtą galima integruoti į didžiąją knygą, atsargų valdymą, gautinas sumas ir mokėtinos sumas. Taip pat galite nustatyti, kad ilgalaikis turtas būtų integruojamas į pirkimo užsakymus.

## <a name="general-ledger"></a>DK

DK viso ilgalaikio turto vertė paprastai sumuojama keliose pagrindinėse sąskaitose, kurių reikia finansinėse ataskaitose. Tačiau puslapyje **Ilgalaikis turtas** galima sukurti daug ilgalaikio turto įrašų. Šiuose įrašuose gali būti tokia informacija, kaip įsigijimo kaina, nusidėvėjimas ir įvertinimas. Kiekvieną kartą užregistravus ilgalaikio turto operaciją atnaujinamos atitinkamos pagrindinės sąskaitos. Ilgalaikio turto pagrindinėse sąskaitose visada rodoma atnaujinta ilgalaikio turto vertė.

Puslapyje **Ilgalaikio turto registravimo šablonai** nurodomos pagrindinės sąskaitos, kuriose registruojamos ilgalaikio turto knygos operacijos. Taip pat nurodomi kiekvienoje pagrindinėje sąskaitoje užregistruotų ilgalaikio turto operacijų tipai. Galite kurti įvairius ilgalaikio turto pagrindinių sąskaitų derinius atsižvelgdami į tai, kiek išsami turi būti ilgalaikio turto informacija didžiojoje knygoje. Pagrindinės sąskaitos gali būti pagrįstos operacijų tipais, knygomis ir kitomis pagrindinėmis sąskaitomis.

## <a name="inventory-management"></a>Atsargų valdymas
Ilgalaikio turto atsargų žurnale galite įvesti juridinio subjekto sau pagaminto arba sukurto ilgalaikio turto įsigijimo informaciją. Tada atsargų prekes galite perkelti į ilgalaikį turtą kaip įsigijimą arba jo dalį. 

Įsigyti turtą galite ir naudodami pirkimo užsakymus. Kai pirkimo užsakymuose yra atsargų prekių, kurios pažymėtos kaip ilgalaikis turtas, puslapio **Ilgalaikio turto parametrai** parinktimi **Leisti turto įsigijimą iš pirkimo** nustatoma, ar registruojant SF užregistruotas ilgalaikio turto įsigijimas. Viena pirkimo eilutė sukurs vieną ilgalaikį turtą, neatsižvelgiant į kiekį. Atsargoms daromas ilgalaikio turto įsigijimo poveikis priklauso nuo juridinio subjekto nustatymo. 

Kai atsargų prekė tampa įsigytu ilgalaikiu turtu, per atsargų žurnalą, pirkimo užsakymą arba įsigijimo pasiūlymą, sukuriama ilgalaikio turto knygos įsigijimo operacija. Jei knygos įsigijimas apima išvestinę knygą, taip pat sukuriama išvestinės knygos įsigijimo operacija. 

Atsargų sumažėjimą užregistravus įsigijimą kontroliuoja registravimo taisyklės, nustatomos puslapyje **Registravimas**, esančiame dalyje Atsargų valdymas. Tačiau registruojant su ilgalaikiu turtu susijusias SF atsargos sumažinamos ne visada. Kai kuriais atvejais, ilgalaikis turtas įsigyjamas vidiniam naudojimui. Pavyzdžiui, kai paradavimo skyriui perkamas nešiojamasis kompiuteris. Dirbdami su pirkimo užsakymais galite naudoti prekes, nustatytas ir perpardavimui, ir vidiniam naudojimui. 

Jei su ilgalaikio turto prekių grupėms naudojate konkrečias gavimo ir išdavimo sąskaitas, tą pačią atsargų prekę galite naudoti tiek atlikdami vidinį pirkimą, tiek kaip perpardavimo atsargas. 

Vidinio naudojimo ilgalaikis turtas nustatomas taip, kad jo sąskaitos tipas būtų **Ilgalaikio turto gavimas**. Šis sąskaitos tipas naudojamas stebint ilgalaikio turto gavimą. Registruodami tiekėjo SF naudokite ilgalaikio turto gavimo sąskaitą, jei vykdoma kuri nors iš toliau nurodytų sąlygų.

-   SF eilutėje yra esamas vidinio naudojimo ilgalaikis turtas.
-   Pažymėtas registruojamos produkto gavimo eilutės žymės langelis **Naujas ilgalaikis turtas?**.
-   Tiekėjo SF eilutėje pažymėtas žymės langelis **Kurti naują ilgalaikį turtą**.

Paprastai ši sąskaita yra išlaidų sąskaita. Naudodami puslapio **Prekių grupė** arba **Registravimas** skirtuką **Pirkimo užsakymas** galite nustatyti prekių grupės arba atskiros prekės sąskaitos tipą **Ilgalaikio turto gavimas**.

Panašiai vidinio naudojimo ilgalaikį turtą galima nustatyti, kad jo sąskaitos tipas būtų **Ilgalaikio turto išdavimas**. Šis sąskaitos tipas naudojamas stebint ilgalaikio turto išdavimą gavėjui. Kai turtas įsigyjamas naudojant pirkimo užsakymą, ilgalaikio turto išdavimo sąskaita kompensuoja ilgalaikio turto debeto sąskaitą. Turto įsigijimą galima užregistruoti registruojant tiekėjo SF arba žurnale Ilgalaikis turtas registruojant turto gavimą (gali būti naudojamas įsigijimo pasiūlymas). Naudodami puslapio **Prekių grupė** arba **Prekės registravimas** skirtuką **Atsargos** galite nustatyti prekių grupės arba atskiros prekės sąskaitos tipą **Ilgalaikio turto išdavimas**. 

Galų gale registruojant naudojamos pagrindinės sąskaitos nustatomos nurodytomis prekių modelių grupės didžiosios knygos integravimo parinktimis. Be to, naudojamos pagrindinės sąskaitos skiriasi atsižvelgiant į tai, ar turtas priskirtas pirkimo užsakymo eilutei. Sąskaitos išvedamos iš registravimo šablono kiekvienai prekių grupei. 
**Note.** Jei registruojant produktų gavimo kvitus naudojamas atsargų rezervavimas, priskirti ilgalaikio turto arba sukurti ilgalaikio turto iš eilutės negalima. 

Sąskaitos, kuriose registruojamos ilgalaikio turto operacijos, priklauso nuo to, ar juridinis subjektas turtą nusipirko, ar sukūrė pats ir nuo turto operacijos tipo. 

Operacijos tipas atsargų operaciją sujungia su ilgalaikio turto registravimo šablonu. Ilgalaikio turto registravimo šablonas nustato, kurios sąskaitos bus atnaujinamos, todėl pasirenkant ilgalaikio turto operacijos tipą netiesiogiai pasirenkamos ir pagrindinės sąskaitos, kuriose bus registruojama operacija. Tiek sukurto, tiek įsigyto ilgalaikio turto operacijų tipas paprastai yra **Įsigijimas** arba **Įsigijimo koregavimas**.

## <a name="accounts-receivable"></a>Gautinos sumos
Integruojant ilgalaikį turtą ir gautinas sumas naudojami nustatomi ilgalaikio turto registravimo šablonai. Šie registravimo šablonai suaktyvinami, kai prieš registruojant kliento SF pasirenkamas kliento SF ilgalaikis turtas, knyga ir ilgalaikio turto operacijos tipas. Dėl to, kad ilgalaikis turtas nėra Atsargų valdymas dalis, parduodami ilgalaikį turtą turite naudoti puslapį **Laisvos formos SF**. 

Jei knygoje yra išvestinė knyga, registruojant kliento SF sukuriama išvestinės knygos operacija.

## <a name="accounts-payable"></a>Mokėtinos sumos
Ilgalaikis turtas paprastai įsigyjamas iš išorinių tiekėjų. Galite naudoti puslapį **Ilgalaikio turto parametrai**, kad nurodytumėte, ar turto įsigijimus visada registruoti registruojant tiekėjo SF, ar turto įsigijimus galima registruoti tik iš ilgalaikio turto. Jei turto įsigijimą leisite registruoti dalyje Mokėtinos sumos, ilgalaikio turto sąskaitos bus atnaujinamos registruojant ilgalaikio turto įsigijimo tiekėjo SF. 

Jei sistema nustatyta registruoti turto įsigijimą registruojant SF, operacija užregistruojama pagal dalyje Ilgalaikis turtas nustatytus įvairių ilgalaikio turto operacijų tipų registravimo šablonus. Registravimą kontroliuoja prieš registruojant tiekėjo SF puslapyje **Pirkimo užsakymas** pasirinkti ilgalaikis turtas, knyga ir ilgalaikio turto operacijos tipas. 

Jei knygoje yra išvestinė knyga, registruojant tiekėjo SF sukuriama išvestinės knygos operacija.

Kiekvienos užsakymo eilutės integravimas suaktyvinamas puslapio **Pirkimo užsakymas** „FastTab“ **Eilutės informacija** skirtuke **Ilgalaikis turtas**. Ilgalaikio turto pirkimo užsakymą galite nusiųsti tiekėjui. Tačiau ilgalaikis turtas ir pagrindinės sąskaitos atnaujinami tik gavus ilgalaikį turtą, kai registruojama tiekėjo SF. Pirkimo užsakymuose gali būti tik atsargų prekės, todėl ilgalaikio turto įsigijimo atsargoms daromas poveikis priklauso nuo juridinio subjekto nustatymo.

## <a name="project-management-and-accounting"></a>Projektų valdymas ir apskaita
Galite projektą susieti su turtu, kuriam įtakos turėjo šis projektas. Be to, kiekvieną etapą, užduotį arba subprojektą galite susieti su skirtingu turtu. Vieną turtą galima susieti su kiekvienu projekto įrašu. Viename įraše leidžiamas vienas turtas, sąsają sukuriate ilgalaikio turto numerį įvedę lauke **Ilgalaikio turto numeris**, esančiame puslapyje **Projektai**. Projekto tipas turi būti **Vidinis** arba **Išlaidų projektas**. 

Taip pat galite naudoti puslapį **Projektai**, kad peržiūrėtumėte informaciją apie turtą, susietą su projektais. Norėdami peržiūrėti ilgalaikio turto įrašą „FastTab“ **Sąranka** spustelėkite turto saitą, kad atidarytumėte puslapį **Ilgalaikis turtas**. Tada spustelėkite **Projektai** &gt; **Visi projektai**, kad peržiūrėtumėte su ilgalaikiu turtu susietus projektus. 

Paprastai ilgalaikį turtą susiejate su projektais, kai projektai susiję su turto darbu, priežiūra ar patobulinimais. Baigus projektą turto vertės didinimas automatiškai nesukuriamas. Todėl, jei reikia, vertės didinimą turite sukurti patys. 

Norėdami panaikinti projekto ir turto susiejimą išvalykite puslapio **Projektai** lauką **Ilgalaikio turto numeris**. 

Be to, kuriamą arba gaminamą ilgalaikį turtą galite apibrėžti kaip vertinamo projekto dalį. Vertinamo projekto pabaigoje galite automatiškai užregistruoti turto įsigijimo operaciją.

Norėdami gauti daugiau informacijos, žr. [Turto pirkimas įsigyjant](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]