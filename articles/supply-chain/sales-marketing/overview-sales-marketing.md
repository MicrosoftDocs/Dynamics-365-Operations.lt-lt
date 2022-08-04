---
title: Pardavimo ir rinkodaros apžvalga
description: Galite naudoti pardavimą ir rinkodarą norėdami gauti, saugoti ir naudoti įvairių tipų pardavimo srauto duomenis. Šie duomenys apima pradinę pardavimo iniciatyvą, tolesnę sekimo veiklą ir papildomą pardavimą.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92303"
- intro-internal
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25b87f45e43350f6c5e6ea775ebc3fcd74ec5187
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103807"
---
# <a name="sales-and-marketing-overview"></a>Pardavimo ir rinkodaros apžvalga

[!include [banner](../includes/banner.md)]

Galite naudoti pardavimą ir rinkodarą norėdami gauti, saugoti ir naudoti įvairių tipų pardavimo srauto duomenis. Šie duomenys apima pradinę pardavimo iniciatyvą, tolesnę sekimo veiklą ir papildomą pardavimą.

## <a name="marketing"></a>Rinkodara

Rinkodaros kampanijos ir veiklos naudojamos, norint atrasti ir užmegzti ryšius su potencialiais klientais, kad pirminiai santykiai galėtų išsivystyti į pardavimo ryšius. Tolesnis procesų srautas vaizduoja rinkodaros verslo procesą. [![Rinkodaros verslo procesas.](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Ryšiai

Pardavimų ir rinkodaros srityje pirminius santykius su potencialiais klientais galima užmegzti įvairiose situacijose. Pavyzdžiui, galite rasti potencialų klientą dalyvaudami prekybos parodoje arba galite turėti galimą klientą po to, kai jūsų organizacija suorganizavo masiškai siunčiamų laiškų kampaniją. Labai svarbu suprasti šalies objekto ryšių eigą, prieš tai šaliai tampant klientu. Tolesniame grafike vaizduojama objekto ryšių eiga, kurios metu potencialus klientas tampa faktiniu klientu. [![„SalesandMarketing01”.](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampanijos

Kampanijos tikslas yra potencialių klientų, galimų klientų, galimybių ir klientų, kurie buvo atrinkti dalyvauti kampanijoje, kontaktai. „Supply Chain Management“ galite sukurti kelių tipų kampanijas, pvz., telerinkodaros, pašto ir el. pašto kampanijas, siekdami maksimaliai padidinti savo klientų potencialą. Kampanijos eigoje gavus teigiamų atsakymų, galima pradėti pardavimo procesą su tais gavėjais, kurie į kampaniją sureagavo teigiamai.

## <a name="sales"></a>Pardavimas
Pardavimo funkcija naudojama norint kurti pasiūlymus, vykdyti papildomo / kryžminio pardavimo veiklas naujiems ir esamiems klientams, kurti pardavimo užsakymus ir kurti klientų pardavimo SF. Tolesnis procesų srautas vaizduoja pardavimo verslo procesą. [![Pardavimo verslo procesas.](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Pardavimo pasiūlymai

Pardavimo pasiūlymai kuriami siekiant pateikti klientams jūsų tiekiamų prekių ar teikiamų paslaugų pasiūlymą. Klientas gali prašyti pasiūlymo arba jūs galite sukurti pasiūlymą, atsakydami į potencialaus ar esamo kliento užklausą. Kai klientas patvirtina pardavimo pasiūlymą, galite jį konvertuoti į pardavimo užsakymą.

### <a name="up-sellcross-sell"></a>Papildomas / kryžminis pardavimas

Papildomas ir kryžminis pardavimas yra produktų pardavimo metodai, kai įvedamas kliento užsakymas. Naudojant papildomo pardavimo metodą, vietoje dabartinio produkto siūlomas kitas produktas. Naudojant kryžminio pardavimo metodą, be dabartinio produkto, siūlomas kitas produktas. Nustatydami produktų sąrašus galite sukurti specialias taisykles, kad nurodytumėte, kada produktas turėtų būti siūlomas naudojant kryžminio arba papildomo pardavimo metodą.

### <a name="sales-orders"></a>Pardavimo užsakymai

Kai kuriate naują pardavimo užsakymą, turite pasirinkti kuriamo pardavimo užsakymo tipą. Galite rinktis iš penkių parinkčių. **Pastaba.** Sukūrus pardavimo užsakymą, galima keisti bet kokį užsakymo tipą, išskyrus tipą **Prekių poreikiai**, jei pardavimo užsakymo būsena yra **Pristatytas**.

| Pardavimo užsakymo tipas  | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žurnalas           | Šį tipą naudokite kaip pardavimo užsakymo juodraštį. Šis tipas neturi įtakos atsargų kiekiams ir negeneruoja prekės operacijų.                                                                                                                                                                    |
| Prenumerata      | Naudokite šį tipą pasikartojančiuose užsakymuose. Kai išrašoma užsakymo SF, užsakymo būsena automatiškai nustatoma kaip atviras užsakymas. Atnaujinamas pristatytas kiekis, kuriam išrašyta SF, ir likę pristatymai. Negalite naudoti šio pardavimo užsakymo tipo, jei naudojate sandėlio valdymo funkciją. |
| Pardavimo užsakymas       | Naudokite šį tipą, kai klientas pateikia arba patvirtina užsakymą.                                                                                                                                                                                                                                        |
| Grąžintas užsakymas    | Naudokite šį tipą, kai klientas grąžina prekę. Grąžintos prekės numeris (RMA numeris) priskiriamas automatiškai.                                                                                                                                                                                            |
| Prekių poreikis | Šis tipas sukuriamas automatiškai, kai parduodate prekę naudodami projektą.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Pardavimo sutartys

Pardavimo sutartis yra sutartis, kuri įpareigoja klientą pirkti tam tikrą produkto kiekį per tam tikrą laiką už specialias kainas ir taikant specialias nuolaidas. Pardavimo sutarties kainos ir nuolaidos turi pirmenybę prieš kainas ir nuolaidas, kurios nurodytos bet kuriose esamose prekybos sutartyse. Pardavimo sutartis galioja nustatytą laikotarpį. Pageidaujama pardavimo siuntimo data, nurodyta puslapyje **Pardavimo užsakymas**, turėtų galiojančio laikotarpio data. Pagal numatytuosius parametrus pardavimo sutartis yra sulaikyta. Galite užsakyti iš pardavimo sutarties tik kai ji nustatyta kaip **Galiojanti**.

### <a name="backorders"></a>Neįvykdyti užsakymai

Įvedant ir tikrinant užsakymus, prieš užbaigiant pardavimą gali reikėti sutvarkyti neįvykdytus užsakymus ir išimtis. Neįvykdyti užsakymai yra pirkimo užsakymai, kurių tiekėjas dar nepristatė, arba pardavimo užsakymai, kurie dar nebuvo pristatyti klientui. Svarbu, kad sektumėte neįvykdytus užsakymus. Pavyzdžiui, jei tiekėjas produktų laiku nepristato, gali tekti keisti pristatymo klientui datą ir informuoti klientą apie atidėjimą. Neįvykdytus užsakymus galima peržiūrėti pagal prekę, klientą arba tiekėją.

#### <a name="viewing-backorders-by-item"></a>Neįvykdytų užsakymų peržiūra pagal prekes

Peržiūrėdami neįvykdytus užsakymus pagal prekę, galite sekti numatomą operacijų, susijusių su preke, srautą. Pavyzdžiui, jūs galite patikrinti toliau nurodytą informaciją.

-   Prekės pardavimo užsakymo skaičių.
-   Ar tiekėjai vis dar nepristatę prekių.
-   Ar reikia užsakyti daugiau prekių, kad visus pardavimo užsakymus būtų įmanoma pristatyti laiku.

Patikrinę šią informaciją galite atsakyti į klientų užklausas apie prekių pristatymo laiką. Be to, galite išdėstyti neįvykdytus pardavimo užsakymus pagal svarbą ir turimas prekes padalinti pagal užsakymus.

#### <a name="viewing-backorders-by-customer"></a>Neįvykdymų užsakymų peržiūra pagal klientą

Neįvykdytų užsakymų peržiūra pagal klientą suteikia galimybę matyti likusių kliento užsakymų būseną. Tikrinti šią informaciją naudinga atsakant į prekių pristatymo laukiančių klientų klausimus.

#### <a name="viewing-backorders-by-vendor"></a>Neįvykdytų užsakymų peržiūra pagal tiekėją

Neįvykdytų užsakymų peržiūra pagal tiekėją naudinga sekant trūkstamus pristatymus ir žiūrint numatomas pristatymų datas. Peržiūra taip pat naudinga pagal svarbą išdėstant iš tiekėjų gaunamus produktus ir pardavimo užsakymų, kuriuos reikia pristatyti, paėmimą.

### <a name="invoices"></a>SF

Pardavimo proceso metu galima kurti trijų tipų SF.

-   Kliento SF
-   Laisvos formos SF
-   Išankstinė SF

#### <a name="customer-invoice"></a>Kliento SF

Kliento SF yra sąskaita, kurią organizacija pateikia klientui pardavimo metu. Šio tipo kliento SF kuriama pagal pardavimo užsakymą, kuriame yra antraštė ir viena arba kelios prekių ar paslaugų eilutės. Kliento SF užbaigia pardavimo užsakymo, važtaraščio ir pardavimo SF ciklą.  

Galite registruoti ir spausdinti vieną kliento SF pagal pardavimo užsakymą arba važtaraštį ir datą. Taip pat galite kartu registruoti ir spausdinti kelias kliento SF pagal važtaraščius ir datas. Kai registruojate vieną kliento SF naudodami pardavimo užsakymą, kiekvienos prekės **likusių išrašyti SF** kiekis atnaujinamas nurodant bendruosius SF kiekius iš pasirinkto pardavimo užsakymo.  

Jei visų prekių **likusių išrašyti SF** kiekiai ir **pristatymo likučio** kiekiai pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jei bet kurio iš dviejų laukų kiekis nėra 0, pardavimo užsakymo būsena nėra keičiama ir jame galima įvesti papildomas SF. Jei ketinate registruoti ir spausdinti vieną ar daugiau klientų SF pagal važtaraščius, turite būti jau užregistravote bent vieną kiekvieno pardavimo užsakymo važtaraštį. Kliento SF grindžiama važtaraščiais ir atspindi nurodytus kiekius.  

Galima sukurti kliento SF, kuri paremta važtaraščio eilutės prekėmis, išsiųstomis iki dabar, net jei dar ne visos konkretaus pardavimo užsakymo prekės yra išsiųstos. Tai galite atlikti, jei, pavyzdžiui, jūsų juridinis subjektas per mėnesį vienam klientui išduoda vieną SF, kurioje pateikiama informacija apie visus siuntinius, išsiųstus tą mėnesį. Kiekvienas važtaraštis reiškia iš dalies arba visiškai atliktą pardavimo užsakymo prekių pristatymą.  

Jums užregistravus SF, **SF likučio** kiekis kiekvienai prekei yra atnaujinamas bendra pristatytų kiekių iš pasirinktų važtaraščių suma. Jei visų prekių **likusių išrašyti SF** kiekiai ir **pristatymo likučio** kiekiai pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**. Jei kiekis nėra 0, pardavimo užsakymo būsena nėra keičiama ir jame galima įvesti papildomas SF. Atsargų operacijos yra atnaujinamos su SF numeriu, o būsena pardavimo užsakymo eilutėje pasikeičia į **SF išrašyta**.

#### <a name="free-text-invoice"></a>Laisvos formos SF

Laisvos formos SF – tai sąskaita faktūra, nesusieta su pardavimo užsakymu. Joje pateikiamos užsakymo eilutės, kuriose yra DK sąskaitos, laisvo pobūdžio aprašymai ir pardavimo kiekis. Į šios rūšies SF prekės numerio įvesti negalite, turite įvesti atitinkamą PVM informaciją. Pagrindinė pardavimo sąskaita nurodoma kiekvienoje SF eilutėje Kliento balansas suminėje sąskaitoje registruojamas iš naudojamo laisvos formos SF registravimo profilio.

#### <a name="pro-forma-invoice"></a>Išankstinė SF

Išankstinė SF yra tokia sąskaita, kuri parengiama kaip faktinių sąskaitos sumų įvertinimas, prieš užregistruojant SF. Galite išspausdinti arba kliento SF išankstinę SF, arba laisvos formos SF išankstinę SF.

### <a name="additional-resources"></a>Papildomi ištekliai

#### <a name="blogs"></a>Tinklaraščiai

Pardavimo proceso apžvalgą galite rasti " [Dynamics 365" finansų ir operacijų skelbime Kaip dirbti su pardavimais](https://financefunction.tech/2018/05/15/how-sales-work-in-dynamics-365-for-finance-and-operations).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
