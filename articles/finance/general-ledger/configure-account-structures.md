---
title: Sukonfigūruoti sąskaitų struktūras
description: Šiame straipsnyje pateikiama informacija apie sąskaitų struktūras ir finansines dimensijas.
author: aprilolson
ms.date: 10/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3fbdd6e2cac61c358848a21e1126bea900e86b2
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713949"
---
# <a name="configure-account-structures"></a>Sukonfigūruoti sąskaitų struktūras

[!include[banner](../includes/banner.md)]

Kuriant taisyklių, kurias naudojant nustatoma tvarka ir reikšmės, kai įvedamas sąskaitos numeris, rinkinį, sąskaitų struktūrose naudojama pagrindinė sąskaita ir finansinės dimensijos. Sąskaitų struktūrų galite sukurti tiek, kiek reikia jūsų verslui. Sąskaitų struktūros priskiriamos įmonės DK nustatymui, kad jas būtų galima bendrai naudoti.

Kuriant sąskaitos struktūrą didžiausias segmentų skaičius yra 11. Jei reikia daugiau nei 11 segmentų, atidžiai įvertinkite savo nustatymus ir reikalavimus, nes tai turės įtakos vartotojų patirtimi. Apsvarstykite, ar segmento negalima išvesti iš ataskaitų scenarijaus naudojant hierarchiją, o ne vedant duomenis arba naudojant vartotojo nustatytą lauką. Pavyzdžiui, jei norite pranešti apie vietą, bet galite figūruoti apie vietą pagal padalinį arba išlaidų centrą, jums nereikės vietos kaip finansinės dimensijos. Jei įvertinę visgi nustatote, kad reikia daugiau kaip 11 segmentų, papildomų segmentų galite įtraukti naudodami išplėstines taisykles.

Sąskaitų struktūroms reikalinga pagrindinė sąskaita. Pagrindinė sąskaita neturi būti pirmasis struktūros segmentas, tačiau nustato, kokia sąskaitos struktūra naudojama sąskaitos numerio įvedimo metu. Todėl pagrindinės sąskaitos vertė gali būti tik vienoje struktūroje, priskirtą DK, kad nepersidengtų. Nustačius sąskaitos struktūrą, filtruojamas leidžiamų verčių sąrašas, siekiant nukreipti vartotoją taip, kad jis pasirinktų tik tinkamas dimensijų reikšmes ir taip sumažėtų galimybė sukurti neteisingą žurnalo įrašą.

> [!NOTE] 
> Jei biudžetą planuojate pagal finansinę dimensiją, ji turės būti sąskaitos struktūros dalimi. Dabar sudarant biudžetą išplėstinės taisyklės nenaudojamos.

## <a name="example"></a>Pavyzdys
Pateikdami šį geriausios praktikos pavyzdį, skirtą sąskaitos struktūrai nustatyti, laikysime, kad įmonė nori sekti savo balanso sąskaitas (100000..399999) sąskaitos ir verslo struktūros vieneto finansinės dimensijos lygiu. Įplaukų ir išlaidų sąskaitų atveju (400000..999999) galima sekti finansinių dimensijų verslo struktūros vienetą, skyrių ir išlaidų centrą. Atlikus pardavimą, taip pat galima sekti klientą. Naudojant šį scenarijų, rekomenduojama, kad dvi sąskaitų struktūros būtų priskirtos įmonės DK – vieną balanso sąskaitoms ir vieną pelno ir nuostolio sąskaitoms. Norint optimizuoti vartotojo patirtį ir tikrinimą, klientui reikia taikyti išplėstinę taisyklę, taikomą tik tada, kai naudojama pardavimo sąskaita.

**Balanso sąskaitos struktūra**

|Pagrindinė sąskaita          | Verslo struktūros vienetas    |
|----------------------|-----------|
|100000..399999 | *;"&nbsp;"|

**Pelno ir nuostolio sąskaitos struktūra**

|Pagrindinė sąskaita          | Verslo struktūros vienetas    |Padalinys          | Išlaidų centras    | &nbsp; |
|----------------------|------------------|--------------------|-----------|---|
|400000..999999 | \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"| \*;"&nbsp;"|

**Išplėstinė taisyklė klientui įtraukti**

Kriterijai: klientą įtraukite tarp pagrindinės sąskaitos numerių 400000 ir 499999. Jo negalima palikti tuščio.

|Klientas         |
|-----------------|
|\* |

Šiame supaprastintoje pavyzdyje leidžiama naudoti visas reikšmes ir tarp jų, \* ir "&nbsp;".

## <a name="segments-and-allowed-values"></a>Segmentai ir leidžiamos reikšmės
Skyriuje **Segmentai** ir **Leidžiama verčių informacija** pateikiamas į vartotojo patirtį panašus tinklelis, skirtas taisyklėms, kurių bus laikomasi registravimo metu atliekant tikrinimą, įvesti. Galite rašyti tiesiai tinklelio langeliuose, importuoti tinklelį iš „Excel“ arba naudotis skyriumi **Leidžiama reikšmės informacija**, kuriame pateikta informacija padės jums atlikti šį procesą.

Skyriuje **Leidžiama reikšmės informacija** pateikta informacija padės jums sukurti kriterijus naudojant **operatorius**, pvz., „prasideda“, „yra tarp“, „apima“ ir daugelį kitų.

[![Leidžiamos reikšmės.](./media/account.png)](./media/account.png) 

Leistinos vertės bus nustatytos į numatytąsias vertes žurnale arba apskaitos paskirstymo įrašo puslapyje, kai nėra kitų galimų verčių, kurias būtų galima pasirinkti pagal sąskaitos struktūros nustatymą.

Čia pateikiamas tipo **Pelno ir nuostolio sąskaitos struktūra** pavyzdys.

|Korespondentinė sąskaita, subsąskaita          | Verslo struktūros vienetas    |Skyrius          | Išlaidų centras    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Kai atidarote žurnalą ir pasirenkate sąskaitą pelno ir nuostolių intervale, pasirinkus 002 verslo vienetą, bus nustatytos numatytosios verčių 022 ir 014 reikšmės sąskaitos valdiklyje. Tai taip pat nutiks ir apskaitos paskirstymo puslapyje. 

## <a name="more-than-seven-criteria-needed"></a>Reikia daugiau nei septynių kriterijų

Jei turite daugiau nei septynis reikalingus kriterijus, galite toliau juos pridėti prie kitos eilutės. Paisysite, kai **dirbate skyriuje Leidžiama vertė,** kad **+Įtraukti naujus** kriterijus nebėra aktyvus po to, kai įvedamas septintas kriterijus. Toliau nurodyta keletas veiksnių, dėl kurių taip nutinka. 
 - Stulpelio plotis 
 - Duomenų saugojimo būdas 
 - Skyriaus **Leidžiama reikšmės informacija** našumo kontrolė
 - Naudojimas  

> [!NOTE]
> 2012 Microsoft Dynamics AX m. atnaujinimas, kuriame nurodyti daugiau nei septyni kriterijai, nepalaikomas. Prieš užbaigdami finansų ir operacijų programėlių atnaujinimą, turite jį ištaisyti. 

Norėdami tęsti papildomų kriterijų įtraukimą, spustelėkite **Dubliuoti segmente** ir **Leidžiamų reikšmių skyrius**. Tai atlikus kriterijai bus nukopijuoti į naują eilutę. Tada galite įvesti arba keisti skyriuje **Leidžiama reikšmės informacija** pateiktą informaciją.

## <a name="best-practices"></a>Geriausia praktika
Nustatant sąskaitų struktūras, galima sekti kelis geriausios praktikos pavyzdžius. Tačiau jie tik rekomendaciniai, todėl rengiant diskusiją turite visapusiškai aptarti savo verslo, augimo ir priežiūros planą.

- Pirmiausiai arba kaip artimai padarykite pagrindinę sąskaitą prieš sąskaitos struktūrą, kad vartotojai turėtų geriausią valdomą patirtį sąskaitos įvedimo metu.
  
  - Patikrinkite, ar bet kuriuos trečiosios šalies sprendimus, kuriuos ketinate naudoti, palaiko pagrindinę sąskaitą pirmose pareigose.

- Pakartotinai naudokite kuo įmanoma daugiau sąskaitų struktūrų, kad visus juridinius subjektus reikėtų kuo mažiau tikrinti.

- Apsvarstykite, ar juridinių subjektų variantams nereikėtų taikyti išplėstinių taisyklių, kad būtų galima pakartotinai naudoti sąskaitų struktūras.

- Apibrėždami leistinas reikšmes kuo įmanoma dažniau naudokite diapazonus ir pakaitos simbolius. Taip sistema ne tik leis augti ir atlikti pakeitimų be priežiūros, bet ir, esant šiai konfigūracijai, geriau veiks.

- Neprirašykite žvaigždutės ties kiekvienu segmentu sąskaitos struktūroje ir nepasikliaukite vien tik išplėstinėmis taisyklėmis. Tai gali būti sunkiai valdoma ir atliekant priežiūrą ištikti vartotojo klaida, dėl kurios sistemai gali nepavykti atlikti registravimo procedūros.

## <a name="account-structure-activation"></a>Sąskaitos struktūros aktyvinimas
Kai jūsų naujas nustatymas arba sąskaitos struktūros pakeitimas jus tenkina, turite jį suaktyvinti. Jei sąskaitos struktūra priskirta didžiajai knygai, aktyvinimo procesas gali būti ilgas, nes visos sistemoje neužregistruotos operacijos turės būti sinchronizuotos pagal naują struktūrą. Užregistruotos operacijos neturi įtakos sąskaitos struktūros pokyčiams. Kaip ir programos 10.0.31 versiją, funkcijų valdymas gali naudoti naują funkciją, **pavadintą** Sąskaitos struktūros suaktyvinimo našumo patobulinimas. Daugiau informacijos apie šią naują sąskaitos struktūros aktyvinimo funkciją ieškokite sąskaitos struktūros suaktyvinimo [našumo patobulinimuose](account-structure-improvement.md). 

Daugiau informacijos rasite Sąskaitų [plano, finansinių dimensijų](plan-chart-of-accounts.md)[...](financial-dimensions.md)[ir sąskaitų bei dimensijų kombinacijų (segmentuoto įrašo valdiklio) įvedimas.](enter-account-dimension-combinations-segmented-entry-control.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
