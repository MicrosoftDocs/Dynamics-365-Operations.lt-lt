---
title: Reisų valdymas
description: Ši tema aprašo, kaip dirbti su reisais. Reisas paprastai nurodo laivą. Tačiau, atsižvelgiant į jūsų praktiką ir procedūras, jis gali nurodyti tiekėją, pirkimo užsakymą arba kitą jūsų organizacijai tinkamą prekę.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 0b39279d17af4fc02c4394b7a69d654317512646
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019207"
---
# <a name="manage-voyages"></a>Reisų valdymas

[!include [banner](../../includes/banner.md)]

Reisas paprastai nurodo laivą. Tačiau, atsižvelgiant į jūsų praktiką ir procedūras, jis gali nurodyti tiekėją, pirkimo užsakymą arba kitą jūsų organizacijai tinkamą prekę.

Puslapyje **Visi reisai** pateikiama reiso informacija, pristatymo ir įkainojimo informacija bei informacija apie prekes, pirkimo užsakymus ir perkėlimo užsakymus. Norėdami atidaryti puslapį **Visi reisai**, eikite į **Iškrovimo kaina \> Reisai \> Visi reisai**. Šiame puslapyje rodomas visų dabartinių reisų sąrašas. Veiksmų srities mygtukus galite naudoti norėdami kurti, naikinti ir dirbti su reisais. Norėdami peržiūrėti išsamią reiso informaciją, pasirinkite jį sąraše.

> [!NOTE]
> Gabenimo konteineriai ir sąskaitos lapai yra susieti su reisu. Pirkimo eilutės yra susietos su gabenimo konteineriu. Jei gabenimo konteineriai ir sąskaitos lapai išjungti, jie taip pat gali būti tiesiogiai susieti su reisu. Be to, čia įvestos išlaidos yra priskiriamos prie visų pridėtų pirkimo eilučių.

## <a name="action-pane"></a>Veiksmų sritis

Puslapio **Reisai** veiksmų srityje pateikiami mygtukai, leidžiantys dirbti su pasirinktu reisu. Kiekvienas mygtukas atlieka vieną veiksmą. Veiksmų srityje taip pat yra skirtukai, iš kurių kiekvienas pateikia susijusių mygtukų rinkinį. Išskyrus atvejus, kai nurodyta, visus mygtukus ir skirtukus galima rasti puslapio **Visi reisai** sąrašo rodinyje ir išsamiame vieno pasirinkto reiso rodinyje.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Mygtukai, rodomi tiesiogiai veiksmų srityje

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus tiesiogiai veiksmų srityje.

| Mygtukas | Aprašymas |
|---|---|
| Naujos | Kurkite reisą. <!-- KFM: Link to scenario --> |
| Panaikinti | Naikinkite esamą reisą. Galima panaikinti tik reisus, kurių reiso būsena yra *Patvirtinta*. Laivui išvykus iš uosto ir apdorojus tranzito prekes, reiso nebegalima panaikinti. |
| Reiso redagavimo įrankis | Atidarykite puslapį **Reiso rengyklė**, kuriame galite įtraukti arba pašalinti reiso pirkimo eilutes, kurti naujus konteinerius ir modifikuoti išsamią reiso informaciją. |
| Reiso išlaidos | Atidarykite puslapį **Reiso išlaidos**, kuriame galite peržiūrėti ir pridėti reiso išlaidų prie visų reiso prekių. Kai reiso išlaidos į reisą įtraukiamos rankiniu būdu, jos automatiškai įtraukiamos į puslapį **Išlaidų užklausa** ir priskiriamos prie kiekvienos prekės pagal būdą, nurodytą puslapyje **Reiso išlaidos**. |

### <a name="buttons-on-the-voyage-tab"></a>Mygtukai, esantys skirtuke Reisas

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus veiksmų srities skirtuke **Reisas**. Šis skirtukas galimas tik kai dirbate puslapio **Visi reisai** sąrašo rodinyje.

| Mygtukas | Aprašymas |
|---|---|
| Gabenimo konteineris | Atidarykite puslapį, kuriame parodyti visi su pasirinktu reisu susieti gabenimo konteineriai. Gali būti vienas konteineris arba daug konteinerių. |
| Sąskaitos lapas | Atidarykite puslapį, kuriame parodyti visi su pasirinktu reisu susieti sąskaitos lapai. Gali būti vienas sąskaitos lapas arba daug sąskaitos lapų. |

### <a name="buttons-on-the-manage-tab"></a>Mygtukai, esantys skirtuke Valdymas

Toliau pateikta lentelė aprašo veiksmus, pasiekiamus veiksmų srities skirtuke **Valdymas**.

| Mygtukas | Aprašymas |
|---|---|
| Gauti dokumentai | Atnaujinkite reisą, kad parinktis **Gauti dokumentai** būtų nustatyta į *Taip*. Galite naudoti šį mygtuką, norėdami užrakinti prekę ir (arba) pirkimo eilutę, kad jos nebūtų galima atnaujinti. |
| Gabenama | Atnaujinkite lauką **Reiso būsena** į tranzito būseną, kuri nustatyta puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)**. Šiame procese nėra jokios kitos logikos. Reisas taip pat gali būti automatiškai atnaujintas į tranzito būseną, remiantis parametrais, nurodytais [sekimo kontrolės centre](delivery-information-setup.md).
| Paruošta įkainojimui | Atnaujinkite lauką **Reiso būsena** į būseną Paruošta įkainoti, kuri nustatyta puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)**. Reisas gali būti įkainotas, kai visos SF apdorotos (tiek atsargų SF, tiek reiso išlaidų SF) ir prekės gautos. Jei įvertintos savikainos, susijusios su reisu, nebuvo įkainotos, bandant apdoroti reiso įkainojimą įvyksta klaida. |
| Įkainota | Išvalykite visas įkainojimo klaidas po to, kai yra visų pirkimo užsakymų ir reiso išlaidų SF. Pasirinkus šį mygtuką, atsiranda dialogo langas **Reiso naujinimas – įkainota**. Ten galite pasirinkti registruoti standartinę finansinę datą arba nurodyti registravimo datą, o tada vykdyti veiksmą. Galite vykdyti veiksmą iš naujo tiek kartų, kiek norite. Taip pat galite naudoti dialogo langą **Reiso naujinimas – įkainota**, norėdami nustatyti grafiką, pagal kurį veiksmas bus vykdomas kaip periodinė užduotis (paketinė užduotis). Rekomenduojame reguliariai atlikti veiksmą, nustatant jį kaip paketinę užduotį. |
| Užregistruoti gavimo kvitų sąrašą | Registruokite visų reiso pirkimo užsakymo eilučių gavimo kvitų sąrašą. Jei naudojami kelių įmonių reisai, atidaromas naujas kiekvienos įmonės gavimo kvitų sąrašo registravimo dialogo langas, kuris turi būti apdorotas kiekviename juridiniame subjekte. |
| Registruoti produkto gavimo kvitą | Registruokite visų reiso pirkimo užsakymo eilučių produktų gavimo kvitus. Pirkimo užsakymo eilučių, susietų su reisu, produktų gavimo procesas bus naudojamas tik tada, jei prekės **nebus** apdorotos tranzito prekių apdorojimo būdu. Jei prekės bus apdorotos tranzito prekių apdorojimo būdu, bandydami užregistruoti pirkimo užsakymo eilutės produkto gavimo kvitą gausite klaidos pranešimą. Jei vykdomi kelių įmonių reisai, kiekvienai įmonei atidaromas naujas pristatymo pažymos registravimo dialogo langas. |
| Registruoti SF | Registruokite visų reiso pirkimo užsakymo eilučių SF. Jei reiso prekės bus apdorotos tranzito prekių apdorojimo būdu, pirkimo užsakymo eilučių SF bus išrašytos prieš pasibaigiant gavimo procesui. Kai išrašoma pradinio pirkimo užsakymo SF, bus sukurti tranzito prekių užsakymai, susieti su pradinio pirkimo užsakymo eilutėmis. Tada šiuos užsakymus gali priimti sandėlis. Jei vykdomos kelių įmonių siuntos, kiekvienai įmonei atidaromas naujas SF registravimo dialogo langas. |
| Siuntimo perkėlimo užsakymas | Registruokite visų reiso perkėlimo užsakymo eilučių perkėlimo užsakymo reisus. Pasirinkus šį mygtuką, bus galima atnaujinti tik perkėlimo užsakymus. |
| Gauti perkėlimo užsakymą | Registruokite visų reiso perkėlimo užsakymo eilučių perkėlimo užsakymo gavimo kvitus. |
| Gauti tranzito prekes | Gaukite visas užsakymo eilutes, kurios vykdomos reiso tranzito metu. Šis mygtukas yra viena iš trijų parinkčių, kurias galima naudoti reiso metu gaunant tranzito prekes. (Kitos dvi parinktys yra mygtukas **Kurti gavimo žurnalą**, kuris aprašytas toliau šioje lentelėje, ir sandėlio valdymo mobiliųjų įrenginių programėlė) Ši parinktis yra paprasčiausia ir ją naudojant tranzito prekės bus apdorojamos iš tranzito prekių sandėlio į galutinės paskirties sandėlį. Norėdami labiau kontroliuoti procesą, naudokite gavimo žurnalą arba mobilųjį įrenginį, kad galėtumėte apdoroti prekių gavimą. |
| Rasti aut. išlaidas | Raskite visas susijusias reiso išlaidas. Jei šios išlaidos jau buvo surastos arba atnaujintos, gausite šį pranešimą: „Yra išlaidų eilučių, kurių SF neišrašytos. Ar norite perrašyti?” Bus rastos visos išlaidos, kurios sukūrimo metu nebuvo susietos su reisu. Reiso išlaidos, kurios pridėtos prie reiso ir kurių SF išrašytos, nebus perrašytos. |
| Kurti pristatymo žurnalą | <p>Atidarykite dialogo langą **Kurti gavimo žurnalą**, kuriame galima kurti vietą nurodantį gavimo žurnalą. Šiame dialogo lange pateikiamos toliau nurodytos parinktys.</p><ul><li>**Kurti iš tranzito prekių** arba **Kurti iš perkėlimo užsakymo** – šios parinkties žyma keičiasi atsižvelgiant į tai, ar naudojate tranzito prekių procesą. Nustatykite į *Taip*, norėdami atidaryti gavimo žurnalo puslapį, leidžiantį apdoroti standartinį tranzito prekių, susijusių su reisu, gavimo žurnalą. Jei prekė jau gauta galutiniame paskirties sandėlyje, ji nebus įtraukta į gavimo žurnalo eilutes.</li><li>**Inicijuoti kiekį** – nustatykite šią parinktį į *Taip*, jei norite inicijuoti kiekį, kuris bus gautas, remdamiesi prekių kiekiu, nurodytu reiso eilutėje. Jei reiso eilutė iš dalies gauta, šis kiekis bus likęs kiekis. Rekomenduojame šią pasirinktį nustatyti į *Taip*.</li><li>**Kurti iš užsakymo eilučių** – nustatykite šią pasirinktį į *Taip*, kad būtų galima naudoti vertę iš užsakymo eilučių.</li></ul><p>Šis mygtukas yra viena iš trijų parinkčių, kurias galima naudoti reiso metu gaunant prekes. (Kitos parinktys yra mygtukas **Gauti tranzito prekes**, kuris buvo aprašytas anksčiau šioje lentelėje, ir sandėlio valdymo mobiliųjų įrenginių programėlė.)</p> |
| Kaupti išlaidas | Galite kaupti išlaidas, kai nurodyta išlaidų tipo debeto didžiosios knygos sąskaita. Šis mygtukas paprastai naudojamas, kai atsargos gabenamos tranzitu arba kai prekės yra gautos ir išrašytos jų SF. |
| Sujungti išlaidas | Perkelkite išlaidas iš gabenimo konteinerio lygio į reiso lygį. Galite naudoti šį mygtuką bendrai naudojamų paslaugų / siuntimo atveju, kai keli objektai dalijasi vieta gabenimo konteineryje arba dėžėje. Pavyzdžiui, reiso metu naudojamas 40 kv. pėdų gabenimo konteineris ir 20 kv. pėdų gabenimo konteineris, o paskirstymas vykdomas pagal tūrį. Tokiu atveju už prekių / objektų, kurie dalijasi vieta 20 kv. pėdų gabenimo konteineryje, gabenimą gali būti baudžiama. Siekdamos sąžiningai paskirstyti išlaidas, kai kurios organizacijos gali norėti perkelti išlaidas į reisą ir paskirstyti jas pagal reiso lygio paskirstymo būdą. |
| Keisti kelionės šabloną | Atidarykite dialogo langą, kuriame galite pakeisti veiklos ciklo šabloną. Pakeitus šabloną, reiso išlaidos bus panaikintos. Todėl gali tekti pasirinkti **Rasti aut. išlaidas** (žr. aprašymą anksčiau šioje lentelėje) arba dar kartą įtraukti išlaidas rankiniu būdu. |

### <a name="buttons-on-the-general-tab"></a>Mygtukai, esantys skirtuke Bendra

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus veiksmų srities skirtuke **Bendra**.

| Mygtukas | aprašymas |
|---|---|
| Gavimų sąrašas | Atidarykite visų reiso pirkimo užsakymo eilučių produktų gavimo kvitų sąrašą. Jei vykdomi kelių įmonių reisai, atidaromas naujas kiekvienos įmonės gavimo kvitų sąrašas. Jei nėra apdorotų produktų gavimo kvitų sąrašų, šis mygtukas negalimas. |
| Produkto gavimo kvitas | Atidarykite pirkimo užsakymo eilučių, susietų su reisu, produkto gavimo kvito įrašą, jei tas įrašas naudojamas. Jei nėra užregistruotų produktų gavimo kvitų, šis mygtukas negalimas. Produktų gavimo kvitų procesas nebus naudojamas, jei naudojate tranzito prekių apdorojimą. |
| Prekių gavimas | Atidarykite prekių gavimo žurnalą, jei jis naudojamas. |
| Sekimas | Atidarykite puslapį **Gaunamų prekių sekimas**, kuriame galite atnaujinti numatomą reiso prekių, esančių gabenimo konteineryje, pristatymo datą, o tada atnaujinti numatomas pirkimo užsakymo eilučių pristatymo datas. |
| Išlaidų tyrimas | <p>Atidarykite puslapį **Išlaidų užklausa**, kuriame rodomos visos reiso išlaidos.</p><p>Veiksmų srityje pasirinkite **Peržiūrėti**, norėdami pakoreguoti rodinį. Galite peržiūrėti visus lygius, prekes ir išlaidų tipo kodus.</p><p>Puslapyje **Išlaidų užklausa** rodomi tik tiesiogiai su atsargų operacijomis susiję išlaidų tipo kodai. Pašalinę išlaidų tipo kodus, galite koreguoti puslapį, sugrupuodami išlaidas kartu. Ši galimybė gali būti naudinga, jei naudojate dydžius ir spalvas.</p><p>Puslapyje **Išlaidų užklausa** rodomi tik tie išlaidų tipo kodai, kurių laukas **Debetas** nustatytas į *Prekė*.</p> |
| Tranzito prekių užsakymai | Atidarykite puslapį **Tranzito prekių užsakymai**, kuriame rodomi tik pasirinkto reiso tranzito prekių įrašai. |

## <a name="lines-view"></a>Rodinys Eilutės

Norėdami atidaryti rodinį **Eilutės**, atidarykite reisą ir reiso antraštės viršutinėje dešinėje pusėje pasirinkite skirtuką **Eilutės**.

### <a name="information-on-the-voyage-header-fasttab"></a>Informacija, esanti „FastTab” Reiso antraštė

Reiso rodinio **Eilutės** „FastTab” **Reiso antraštė** apima pagrindinę informaciją, apibūdinančią reisą. Daugelis laukų, rodomų šiame „FastTab”, taip pat rodomi rodinyje **Antraštė**, kaip toliau aprašyta šioje temoje.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informacija, esanti „FastTab” Reiso eilutės

Reiso rodinio **Eilutės** „FastTab” **Reiso eilutės** yra susijęs su reiso informacija ir įkainojimo informacija, kuri taikoma reiso lygiu. Čia galite peržiūrėti gabenimo konteinerius, sąskaitos lapus ir prie reiso pridėtas prekes. Taip pat rodoma reiso prekių kaina ir kiekis. Pasirinkę tinkamą saitą galite peržiūrėti bet kokį pateiktą gabenimo konteinerį ar sąskaitos lapą.

### <a name="information-on-the-line-details-fasttab"></a>Informacija, esanti „FastTab” Eilutės informacija

Reiso rodinio **Eilutės** „FastTab” **Eilutės informacija** pateikia daugiau informacijos apie eilutę, kuri šiuo metu pasirinkta „FastTab” **Reiso eilutės**. Atkreipkite dėmesį, kad šiame „FastTab” pateikiama informacija apie kiekvienos eilutės užimamą vietą konteineryje ir deklaruotą kiekį.

## <a name="header-view"></a>Antraštės rodinys

Norėdami atidaryti rodinį **Antraštė**, atidarykite reisą ir reiso antraštės viršutinėje dešinėje pusėje pasirinkite skirtuką **Antraštė**.

### <a name="settings-on-the-general-fasttab"></a>Parametrai, esantys Bendra „FastTab”

Toliau pateikiamoje lentelėje aprašomi laukai, galimi reiso rodinio **Antraštė** „FastTab” **Bendra**.

| Laukas | aprašymas |
|---|---|
| Reisas | Įveskite reiso arba skrydžio numerį. |
| Rezervavimo nuoroda | Jei jūsų siuntėjas arba siuntimo centras pateikia nuorodos numerį, skirtą reisui identifikuoti (t. y. siuntėjo arba siuntimo centro vidinę nuorodą), įveskite jį čia. |
| Transporto priemonė | Įveskite arba pasirinkite laivą. Jei laivas nėra nurodytas kaip reikšmė, galite įvesti laivo ID kaip laisvos formos tekstą. Tokiu atveju pagrindinė lentelė nėra atnaujinama, kad vėliau šiame lauke būtų galima pasirinkti laivo ID. |
| Išorinis reiso ID | Įveskite viešai prieinamą reiso ID (pvz., skrydžio numerį). |
| Pagrindinis oro transporto važtaraštis / važtaraštis | Įveskite pagrindinio oro arba kito transporto važtaraščio numerį. Galite nurodyti šią vertę, kai siunčiate oru. |
| Namų oro transporto važtaraštis / važtaraštis | Įveskite gabenimo konteinerio namų oro arba kito transporto važtaraštį. |
| Nuoma | Pasirinkite šį žymės langelį, norėdami nurodyti, kad konteineris yra nuomojamas konteineris, kuris turi būti grąžintas. |
| aprašymas | Įveskite reiso aprašymą, kad būtų lengviau atpažinti. |
| Reiso būsena | Reiso būsena. Reikšmės gali būti *Sukurta*, *Tranzitas*, *Gauti dokumentai* ir *Įkainota*. Šis laukas nėra apskaičiuojamas pagal logiką. Jis atnaujinamas tik registravimo veiksmo metu. Reikšmė *Įkainota* nurodo, kad gauta atsargų SF ir visos reiso išlaidos. Reiso būsena gali būti *Įkainota* tik tuo atveju, jei SF gauta. |
| Pirkimo užsakymo būsena | Aukščiausia visų pirkimo užsakymų, susietų su reisu, pasiekta būsena. |
| Gauti dokumentai | Vertė, nurodanti, ar jūsų įmonė gavo visus su reisu susijusius dokumentus. Norėdami pakeisti vertę, veiksmų srities skirtuko **Valdymas** grupėje **Reiso naujinimas** pasirinkite **Gauti dokumentai**. |
| Gabenimo įmonė | Pasirinkite šio reiso gabenimo įmonę. Šis laukas gali būti naudojamas aut. išlaidoms nustatyti. |
| Pavadinimas / vardas ir (arba) pavardė | Įmonės, pasirinktos lauke **Gabenimo įmonė**, pavadinimas. |
| Matas | Šis laukas leidžia automatinėse išlaidose nurodyti matavimo vienetą. Matavimo vienetus dažnai naudoja organizacijos, kurios nežino atskirų prekių tūrio ar svorio, bet reikalauja tikslesnio paskirstymo, nei pateikia suma ar kiekis. Krovinių ekspeditorius pateiks svorį arba kubinį matavimo vienetą, o jūs galėsite pateikti jį prekės arba pirkimo užsakymo lygiu. Jį galima atnaujinti automatiškai, jei pasirinktas parametras, arba įvesti rankiniu būdu. |
| Matavimo vienetas | Matavimo vienetas, kuris taikomas skaičiui lauke **Matavimo vienetas**. |
| Padėklų skaičius | Nurodykite padėklų skaičių, pateiktą reiso eilutėje. Šis laukas automatiškai atnaujinamas, jei puslapio **Iškrovimo kainos parametrai** skirtuke **Bendra** parinktis **Automatiškai atnaujinti dėžių skaičių** nustatyta į *Taip*. |

### <a name="settings-on-the-delivery-fasttab"></a>„FastTab” Pristatymas parametrai

Toliau pateikiamoje lentelėje aprašomi laukai, galimi reiso rodinio **Antraštė** „FastTab” **Pristatymas**.

| Laukas | aprašymas |
|---|---|
| Sukūrimo data ir laikas | Reiso įrašo sukūrimo data ir laikas. |
| Pagaminimo data | Šis laukas iš pirkimo užsakymų, susietų su reisu, pasirenka anksčiausią buvusios gamyklos datą. Buvusios gamyklos data galima pirkimo užsakymo antraštėje ir yra atnaujinama naudojant sekimo kontrolės funkciją. |
| Siuntimo data | Numatoma data, kai lėktuvas arba laivas išvyksta iš siuntos kilmės vietos. |
| Išvykimo data | Išvykimo data paprastai yra data, kai lėktuvas ar laivas išvyksta iš užjūrio uosto. Nebūtina, kad siuntimo data ir išvykimo data sutaptų. Laukas **Išvykimo data** skirtas tik informacijai. Jis nėra naudojamas norint apskaičiuoti numatomą pristatymo datą. Sekimo kontrolės funkcija naudojama numatomai pristatymo datai apskaičiuoti. Šį lauką galima nustatyti taip, kad jį automatiškai užpildytų sekimo kontrolės funkcija. |
| Saugojimo data | Šis laukas pasirenka anksčiausią datą, kai bus galima parduoti pirkimo užsakymų, susietų su reisu, prekes. |
| Įvertinta pristatymo data | Numatoma pristatymo data paprastai yra data, kai prekes reikia pristatyti į sandėlį. Šis laukas naudojamas tik informaciniais tikslais. Jis nėra naudojamas bendrojo prekių planavimo metu. Numatoma pristatymo data, nurodyta pirkimo užsakymo eilutėje, naudojama reiso prekių bendrojo planavimo metu ir yra atnaujinama naudojant sekimo kontrolės funkciją. Šį lauką galima nustatyti taip, kad jį užpildytų sekimo kontrolės funkcija. |
| Faktinė pristatymo data | Anksčiausia pristatymo data, nustatyta remiantis prekėmis, susietomis su reisu. |
| ETA siuntimo uoste | Įveskite datą, kada tikitės, kad transporto priemonė atvyks į uostą, remdamiesi informacija, kurią pateikė jūsų siuntimo agentas. |
| Gauti originalūs dokumentai | Įveskite pradinių dokumentų gavimo datą. |
| Tarpininkui patarta | Įveskite datą, kada tarpininkui patarta. |
| Pradinis važtaraštis išsiųstas | Įveskite pradinio važtaraščio išsiuntimo datą. |
| Išleistos prekės | Įveskite prekių išsiuntimo iš muitinės datą. |
| Kliento paskyrimas | Įveskite kliento paskyros datą, kada tikimasi, kad klientas perims prekių nuosavybės teises. |
| Pristatymas į sandėlį | Įveskite datą, kada prekės buvo pristatytos į sandėlį. |
| Patikrinimo data | Įveskite patikrinimo datą. |
| Pristatymo instrukcijos | Įveskite pristatymo instrukcijų gavimo datą. |
| Pristatymo būdas | Šiame lauke pateikiama informacija apie būdą, kuris naudojamas reisui įvykdyti, ir automatinių išlaidų, susijusių su tuo pristatymo būdu, pasirinkimą. |
| Kilmės uostas | Uostas, iš kurio išvyksta transporto priemonė. |
| Paskirties uostas | Uostas, į kurį atvyksta transporto priemonė. Gabenimo konteinerių paskirties uostai gali būti skirtingi, nes laivas gali sustoti keliuose uostuose. Patikrinę paskirties uostą gabenimo konteinerio lygiu, pateikite tikslią kiekvieno reiso gabenimo konteinerio uosto informaciją. Aut. išlaidos, susijusios su kroviniu, nustatomos pagal gabenimo konteinerio tipą, paskirties uostą ir kilmės uostą. |
| Vietinis ekspeditorius | Šis laukas naudojamas tik informaciniais tikslais. Vietinį ekspeditorių galima pasirinkti iš tiekėjo lentelės. |
| Vietinio transporto data | Vietinio transporto rezervavimo data. Šis laukas gali padėti sandėliui atlikti planavimą. |
| Vietinio transporto laikas | Vietinio transporto rezervavimo laiko atkarpa. Šis laukas gali padėti sandėliui atlikti planavimą. |
| Kelionės šablonas | Nurodytas reiso veiklos ciklo šablonas. Veiklos ciklo šablonas naudojamas norint įvesti gabenimo konteinerio ir reiso kilmės uostą bei paskirties uostą. Šios vertės padeda nustatyti aut. išlaidas, susijusias su reisu. |

### <a name="settings-on-the-other-fasttab"></a>„FastTab” Kita parametrai

Toliau pateikiamoje lentelėje aprašomi laukai, galimi reiso rodinio **Antraštė** „FastTab” **Kita**.

| Laukas | Aprašymas |
|---|---|
| Pastabos | Įveskite papildomą informaciją, susijusią su reisu. |
| Vertinimo data | Pasirinkite anksčiausią pirkimo užsakymų, susietų su reisu, buvusios gamyklos datą. |
| Laukiantis reisas | Jį galite naudoti norėdami nurodyti, ar jūsų siunta išsiųsta arba ar reisas pradėtas. Jis naudojamas tik informaciniais tikslais.  |
| Gabenimo konteinerių pervardijimas | Dirbant su reisais, kurių metu siunčiama daugiau nei vienas konteineris, tai dar negautų konteinerių skaičius. |

## <a name="voyage-update-periodic-tasks"></a>Reiso naujinimo periodinės užduotys

Modulyje **Iškrovimo kaina** yra kelios su reisu susijusios periodinės užduotys, galinčios masiškai atnaujinti keletą reisų aspektų. Norėdami paleisti arba suplanuoti šias periodines užduotis, eikite į **Iškrovimo kaina \> Periodinės užduotys \> Reiso naujinimai** ir pasirinkite vieną iš toliau pateiktų užduočių tipų.

- **Gauti dokumentai** – ši užduotis leidžia nustatyti kelių reisų parinktį **Gauti dokumentai** į *Taip* tuo pačiu metu. Norėdami nustatyti atnaujinamų reisų rinkinį, naudokite parametrus **Filtruoti**.
- **Tranzitas** – ši užduotis leidžia nustatyti lauką **Reiso būsena** į tranzito būseną, kuri nustatyta kelių reisų puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)** tuo pačiu metu. Norėdami nustatyti atnaujinamų reisų rinkinį, naudokite parametrus **Filtruoti**.
- **Paruošta įkainoti** – ši užduotis leidžia nustatyti lauką **Reiso būsena** į būseną Paruošta įkainoti, kuri nustatyta kelių reisų puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)** tuo pačiu metu. Paprastai nustatote, kad ši užduotis būtų vykdoma pagal reguliarų grafiką.
- **Įkainota** – ši užduotis leidžia nustatyti lauką **Reiso būsena** į būseną Įkainota, nustatytą kelių reisų puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)** tuo pačiu metu, su sąlyga, kad jie buvo įkainoti, bet dar nebuvo atnaujinti reiso metu. Paprastai nustatote, kad ši užduotis būtų vykdoma pagal reguliarų grafiką.
