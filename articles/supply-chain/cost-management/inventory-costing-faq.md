---
title: Atsargų įkainojimo DUK
description: Šioje temoje atsakinėja keletas dažnai užduodamų klausimų apie atsargų įkainojimo programoje Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809306"
---
# <a name="inventory-costing-faq"></a>Atsargų įkainojimo DUK

[!include [banner](../includes/banner.md)]

Šioje temoje atsakinėja keletas dažnai užduodamų klausimų apie atsargų įkainojimo programoje Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Atsargų uždarymas, koregavimas ir perskaičiavimas

### <a name="is-the-inventory-close-required"></a>Ar atsargų uždarymas būtinas?

Jei planuojate naudoti atsargų archyvavimo priemonę, atsargų uždarymas yra būtinas. Jei planuojate naudoti atsargų archyvavimo funkciją, primygtinai rekomenduojame vis tiek vykdyti atsargų uždarymą, nepaisant jūsų esančių įkainojimo modelių.

### <a name="how-often-should-the-inventory-close-be-run"></a>Kaip dažnai vykdyti atsargų uždarymą?

Atsargų uždarymas turėtų būti vykdomas bent vieną kartą per DK laikotarpį. Pavyzdžiui, jei jūsų DK nustatytas kalendorinis mėnuo, remiantis finansiniu kalendoriumi, atsargų uždarymą turėtumėte vykdyti kartą per mėnesį.

### <a name="is-the-inventory-recalculation-required"></a>Ar reikia perskaičiuoti atsargas?

Ne, atsargų perskaičiavimas nebūtinas. Jei naudojate periodinį įkainojimo modelį, pvz., "pirmasis į, pirmasis iš" (FIFO), "paskutinis į, pirmasis iš" (LIFO) arba svertinis vidurkis, turėtumėte atidžiai apsvarstyti, ar paleisite atsargų perskaičiavimą. Joje galima pateikti tikslesnes išlaidas pasirinktuose heursijos modeliuose.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Kaip dažnai vykdyti atsargų perskaičiavimą?

Jei planuojate vykdyti atsargų perskaičiavimą, rekomenduojame apsvarstyti galimybę paleisti jį kasdien kaip paketinį procesą. Jei jūsų organizacijai nereikia dažnai teikti periodinių įkainojimo modelių atsargų verčių ataskaitų, galite apsvarstyti galimybę atsargų skaičiavimą vykdyti ne taip dažnai.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Kada naudoti turimų atsargų koregavimą uždarymo ir koregavimo puslapyje?

Turimų atsargų koregavimą galima atlikti tik baigus atsargų uždarymą. Paprastai jis vykdomas po paskutinio uždarymo. Koreguojant atsargas galima koreguoti tik tas atsargas, kurios dar turimos tą datą, kai vykdomas koregavimas.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Kada naudoti atsargų operacijos koregavimą uždarymo ir koregavimų puslapyje?

Turėtumėte naudoti atsargų operacijos koregavimą prieš pradėdami atsargų uždarymą. Paprastai naudojama taisyti neteisingą gavimą. Negalite registruoti atsargų operacijos koregavimo po atsargų uždarymo vykdymo ir operacija sudengta.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Ar pirkimo užsakymo grąžinimai per atsargų uždarymą laikomi kitais dalykais?

Taip. Pirkimo užsakymo gavimas yra išdavimas, kuris sudengtas su gavimu, esamu duomenų modelyje, kurį pasirenkate prekei. Jei naudojate periodinį įkainojimo modelį, galite naudoti žymėjimą, norėdami nepaisyti heursinių išlaidų.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Kas atsitinka su pardavimo užsakymų grąžinimais per atsargų uždarymą?

Kai vykdote atsargų uždarymą, pardavimo užsakymo grąžinimas yra laikomas gavimu į atsargas. Problemos sudengijamos su atsargomis, remiantis jūsų pasirinktu prekės heursiniu modeliu.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Kokia savikaina naudojama grąžinant pardavimo užsakymą?

Kai sukuriate su pardavimo užsakymu susijusį grąžinimą, **vieneto** kainos lauko vertė nukopijuojama iš pradinio pardavimo užsakymo, **o** grąžinimo grąžinimo savikainos lauke nustatoma pakoreguota savikaina iš pradinės grąžinamos pardavimo užsakymo eilutės atsargų operacijos. Jei susijusios **atsargų** operacijos vertės atidarymo pasirinktis *nustatyta kaip Taip*, atsargų uždarymas gali sukelti pradinio pardavimo užsakymo išdavimo išlaidų atnaujinimų. Šiame **scenarijuje** grąžinimo savikainos laukas nėra atnaujinamas. Tačiau kai registruojate grąžinimo užsakymo važtaraštį, sistema patikrins savikainą ir naudos atnaujintas išlaidas grąžinimo atsargų operacijoje.

Standartinių išlaidų prekės, susijusios su pardavimo užsakymu, grąžinimui sistema naudos standartines išlaidas nuo pradinio pardavimo užsakymo dienos, net jei prekei yra aktyvios naujos standartinės išlaidos.

Kai sukuriate grąžinimą, kuris nėra susijęs su pardavimo užsakymu, **grąžinimo** savikainos laukas yra nustatomas į aktyvią prekės kainą, kurią turite turite prekei svetainėje, kurios grąžinimo užsakymą kuriate. Jei neturite aktyvios prekės įkainojimo versijos savikainos, vertė bus 0 (nulis). Jei vertę paliksite 0 (nuliu), gausite perspėjimą, kuriame nurodoma, kad grąžinamos partijos ID arba grąžinimo savikaina nenurodyta.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Koks yra numatomas atsargų uždarymo našumas?

Daug faktorių gali turėti įtakos atsargų uždarymo našumui. Šie faktoriai apima bendrą prekių skaičių, bendrą laikotarpio operacijų skaičių, jūsų naudojamas atsargų modelius ir paketų pagalbos priemonių, kurias konfigūruojate atsargų ir sandėlio valdymo parametruose, skaičių. Galite tikėtis, kad uždarymas gali užtrukti tiek kiek minučių, ar kiek kelių valandų. Nėra specialių patarimų apie laiko, kurį uždarymas turėtų užtrukti, įvertinimą. Turite nurodyti savo nefunkcijos verslo reikalavimus atsargų uždarymo našumui ir dirbti kartu su savo partneriu, kad apibrėžtumėte atsargų uždarymo proceso vykdymo grafiką. Jei netikėtai patiriate žemą atsargų uždarymo proceso našumą, turėtumėte atidaryti palaikymo bilietą.

## <a name="costing-sheet-and-indirect-costs"></a>Įkainojimo lapas ir netiesioginės išlaidos

### <a name="which-costing-models-support-the-costing-sheet"></a>Kurie įkainojimo modeliai palaiko įkainojimo lapą?

Nors įkainojimo lapas dažniausiai naudojamas organizacijose, kurios naudoja standartinį įkainojimo lapą, galite jį naudoti su bet kuriuo įkainojimo modeliu, kuris yra tiekimo grandinės valdymo metu.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Ar galima turėti keletą įkainojimo lapų įvairioms mano organizacijos dalims?

Ne. Vienam juridiniam subjektui galite turėti tik vieną įkainojimo lapą.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Ar galima turėti skirtingus kiekvienos svetainės įkainojimo lapus?

Ne, negalite turėti skirtingo įkainojimo lapo kiekvienai svetainei. Kiekvienam juridiniam subjektui galite sukurti tik vieną įkainojimo lapą. Tačiau galite konfigūruoti visų mazgų, išlaidų grupių arba netiesioginių išlaidų mazgus pagal svetainę. Ši konfigūracija yra neautomatinis procesas, o kai įvyksta organizacijos ar veiklos pakeitimai, įkainojimo lape turite prižiūrėti hierarchiją ir prekių priskyrimus. Jei viena prekė gaminama arba perkama daugiau nei vienoje teritorijoje, nėra mechanizmo, kuris leistų jums su preke elgtis skirtingai įkainojimo lape kiekvienai teritorijojei. Be to, atkreipkite dėmesį, kad visi netiesioginių išlaidų kodai turi tarifą ar papildomą mokestį, nustatytą jūsų įkainojimo versijoje. Išlaidos, kurias nurodote, visada yra konkrečios tam tikrai vietai.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Ar galima išjungti ir aktyvinti įkainojimo lapo versijas?

Nors įkainojimo lapui neįrašomos jokios išsamios versijos retrospektyvos, galite atlikti įkainojimo lapo pakeitimus ir tada, kai jis parengtas, išsaugoti ir patikrinti. Nėra mechanizmo, kuris leidžia grįžti prie senesnės įkainojimo lapo versijos arba peržiūrėti įkainojimo lape atliktus pakeitimus. Jei pakeitimus pradedate ir nenorite, kad jie imtų galioti, galite uždaryti puslapį neįrašę ir nepateikite pakeitimų. Jums bus pasiūlyta atmesti pakeitimus.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Ar galima sukurti kiekvienos prekės netiesiogines išlaidas?

Savo įkainojimo lape galite sukurti **netiesioginių** išlaidų kodus, kur mazgo tipo laukas *nustatytas į Papildomas* mokestis, *Tarifas* arba Išeigos *vienetas.* Tada galite nurodyti tarifą arba papildomą mokestį, kad jis būtų konkretus prekės numeriui. Į "**FastTab"** tarifą **arba** papildomą mokestį įtraukite eilutę į tinklelį. Lauke Galioja **nustatykite** lentelę *ir* ryšio **lauką** su konkrečiu prekės numeriu.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Ar galima sukurti netiesiogines išlaidas, kurios nėra susijusios su konkrečia preke?

Taip. Galite sukurti netiesioginių išlaidų kodą, kur mazgo **tipo laukas** nustatytas į Išeigos *vienetas.* Potipio **lauką** *galite* nustatyti kaip Kiekis, *·* *Svoris* arba Tūris, kad nurodydami gaminamos prekės kiekį, svorį arba tūrį. Kursas, kurį nurodote tarifo **"** FastTab", bus taikomas jūsų pasirinktam potipiui. Pavyzdžiui, nustatote **potipio** *·* **·** *lauką kaip Kiekis ir Tarifas į 1,00 USD*, tada sukuriate 10 kiekio gamybos arba paketinį užsakymą. Šiuo atveju netiesioginės išlaidos, kurios bus pridėtos prie baigtos prekės, 10.00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Ar norėčiau naudoti įkainojimo lapą mano gamybos išlaidoms išskaidyti pagal valandas ir medžiagas?

Taip. Norėdami išlaidas atskirti iš **bet** kurios jūsų pasirinktų grupavimų, savo įkainojimo lape galite sukurti mazgus Total. Pavyzdžiui, galite sukurti vieną bendrą mazgą **,** kurio pavadinimas Valandos *,* ir kitą, pavadintą *Medžiagos*. **Prie valandų mazgo** pridėkite kiekvieną su valandomis susijusią kodų grupę. Po medžiagų **mazgu** pridėkite kiekvieną su jūsų medžiagomis susijusią išlaidų grupę.

## <a name="dimension-groups"></a>Dimensijų grupės

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Ar galima valdyti išlaidas paketo ar serijos numerio lygiu?

Taip, jei naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO, LIFO datą, svertinį vidurkį arba svertinio vidurkio datą, **·** **·** **galite** įgalinti paketo arba serijos numerio dimensijos pasirinktį, kad būtų galima stebėti išlaidas išsamaus lygio metu.

### <a name="can-i-manage-costs-at-the-location-level"></a>Ar galima valdyti išlaidas vietos lygiu?

Ne, saugojimo dimensijų grupėje **negalima** įgalinti vietos dimensijos **parinkties** Finansinės atsargos. Jei jūsų organizacija turi sekti išlaidas išsamesniu lygiu, apsvarstykite, ar galite kurti virtualiuosius sandėlius, **·** **ir** saugojimo dimensijų grupėje pasirinkite sandėlio dimensijos pasirinktį Finansinės atsargos.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Ar įjungti saugojimo dimensijų grupės parinktį Naudoti sandėlio valdymo procesus?

Jei manote, kad galbūt norėsite ateityje naudoti išplėstines sandėlio valdymo priemones, turėtumėte įgalinti parinktį Naudoti **sandėlio valdymo** procesus. Įrašę saugojimo dimensijų grupę, nebegalite pakeisti jai **parinkties Naudoti sandėlio valdymo procesus** parametro. Jei nuspręsite vėliau naudoti sandėlio valdymo procesus, turėsite sukurti naują sandėlį, kuriame įgalinta parinktis. Nėra automatinio proceso, kurį naudodami galite perkelti visas atsargas iš vieno sandėlio į kitą arba kopijuoti susijusias konfigūracijas į naują sandėlį.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Ar galima įgalinti saugojimo dimensijų grupės sandėlio valdymo procesus, net jei nesuplanuoju naudoti išplėstinio sandėliavimo?

Taip, net jei planuojate naudoti išplėstines sandėlio valdymo priemones, **galite** įgalinti saugojimo dimensijų grupės parinktį Naudoti sandėlio valdymo procesus. Norėdami kurti ir apdoroti operacijas, turite užbaigti minimalią konfigūraciją, pvz., rezervavimo hierarchijas ir vienetų sekų grupes. Tačiau išplėstinio sandėliavimo parametrų paprastai nepaisoma, kai neautomatiniu būdu apdorojate išrinkimo dokumentus, važtaraščius ir gavimo dokumentus (pvz., pardavimo užsakymo ir pirkimo užsakymo puslapiuose).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kada įjungti saugojimo ar sekimo dimensijų grupės parinktį Faktinės atsargos?

Turite įgalinti saugojimo ir **sekimo dimensijų** grupių parinktį Faktinės atsargos, kai turite išsaugoti išsamius atsargų įrašus, pagrįstus ta dimensija. Paprastai bet kuri aktyvi dimensija taip pat bus faktiškai sekama. Todėl bet koks atsargų gavimas, išdavimas arba judėjimas bus sekamas pagal pasirinktą dimensiją. Jei dimensija neprivaloma (pvz., numerio lentelė), **·** **galite** įgalinti leidžiamą tuščią gavimą ir leistinas tuščias išdavimas pasirinktis, kad vartotojai galėtų gauti, išduoti ar perkelti atsargas net tada, kai dimensija nenurodyta.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Kada įjungti saugojimo ar sekimo dimensijų grupės parinktį Finansinės atsargos?

Turite įgalinti saugojimo ir **sekimo dimensijų** grupių parinktį Finansinės atsargos, kai turite išsaugoti išsamius finansinius įrašus, pagrįstus ta dimensija. Vietos **dimensijos** visada sekamos finansiškai, o kitos dimensijos finansinio sekimo metu yra pasirenkamos. Jei naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO ar svertinį vidurkį, **dimensijos** finansinių atsargų pasirinktis nurodo, kad sudengsite tik tais atvejais, kai gavimas ir išdavimas turi tas pačias dimensijų vertes. Pavyzdžiui, jei **·** **įgalinsite** sandėlio dimensijos parinktį Finansinės atsargos, turėsite skirtingas išlaidas kiekviename sandėlyje, o skirtingų sandėlių gavimų ir gavimų nebus galima sudengti.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Ar po operacijų galima pakeisti produktų, saugojimo ar sekimo dimensijų grupę?

Sukūrę prekės modelių grupę galite **keisti padengimo plano nustatymą pagal dimensiją,** **laukuose Pirkimo kainos ir Pardavimo kainos,** **·** **jei pažymėtas dimensijos žymės langelis Aktyvus prekės modelių grupėje.** Kitų pakeitimų keisti negalima. Pavyzdžiui, negalima įjungti arba išjungti **aktyvių,** **leidžiamų tuščių išdavimų,** **leidžiamų tuščių gavimų,** **faktinių** atsargų ir finansinių atsargų pasirinkčių.**·**

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Ar galima pakeisti išleisto produkto produkto, saugojimo arba sekimo dimensijų grupę?

Jei turimos produkto atsargos yra 0 (nulis), **·** *o visų atsargų operacijų vertės atidarymo pasirinktis nustatyta kaip Ne*, galite pakeisti išleisto gamybos puslapio saugojimo ir sekimo dimensijų grupes. Sukūrus įrašą produkto dimensijų grupės keisti negalima.

## <a name="item-model-groups"></a>Prekių modelių grupės

### <a name="when-should-i-enable-the-stocked-product-option"></a>Kada įjungti produkto atsargų parinktį?

Turite įgalinti bet kurios **prekės,** kuri bus sekama atsargose, parinktį Laikomas produktas. Įgalinus šią pasirinktį, prekės gavimą ir išdavimą sekamos išsamios atsargų operacijos. Ši pasirinktis paprastai įgalinami, pvz., bet kokiai materialiai prekei, kurią laikote savo sandėlyje. Taip pat turėtumėte įgalinti šią pasirinktį, jei planuojate į savo KS ar formules įtraukti nematerialią prekę, pvz., aptarnavimo prekę. Jei įgalinsite **pasirinktį** Atsargose esantis produktas, atsargų papildomose knygose nebus sekamos jokios atsargų operacijos, o prekių išlaidos paprastai į jūsų DK bus įkainojamos. Ši pasirinktis dažnai naudojama, pavyzdžiui, parduotuvės tiekimui ar paslaugoms, kurios nėra įtrauktos į KS arba formules.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Kada įjungti pasirinktį Registruoti faktines atsargas?

Parinktis **Registruoti faktines** atsargas paprastai įgalinamas, kai **įgalinta parinktis** Sandėliuotas produktas. Kai įgalinsite šią pasirinktį, sistema atseis fizinį prekės atnaujinimą atsargų operacijoje. Ši pasirinktis naudojama kartu su parametrais mokėtinų sumų, gautinų sumų ir gamybos kontrolės, kuri nurodo, kad faktinis atnaujinimas turėtų sukurti kvitą. Paprastai ši pasirinktis įgalinsite, kai norite, kad DK būtų atnaujinta, kai tik faktiškai atnaujinate atsargas. Jei tiekimo grandinės valdymas nėra jūsų finansinių duomenų įrašo sistema, galite norėti išjungti šią pasirinktį.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Kada įjungti parinktį Registruoti finansines atsargas?

Parinktis **Registruoti finansines atsargas** paprastai įgalinamas, kai įgalinta **parinktis** Sandėliuotas produktas. Ši pasirinktis naudojama kartu su parametrais mokėtinų sumų, gautinų sumų ir gamybos kontrolės, kuri nurodo, kad finansinis atnaujinimas turėtų sukurti kvitą. Paprastai šią pasirinktį įgalinsite, kai norite, kad DK būtų atnaujinta kaskart finansiškai atnaujinant atsargas (pavyzdžiui, išrašant pardavimo užsakymų IR pirkimo užsakymų SF arba baigiant gamybos užsakymą). Jei tiekimo grandinės valdymas nėra jūsų finansinių duomenų įrašo sistema, galite norėti išjungti šią pasirinktį.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Kada įjungti pasirinktį Registruoti atidėtų įplaukų sąskaitoje pardavimo pristatyme?

Naudokite pasirinktį **Registruoti** atidėtų įplaukų sąskaitoje pardavimo pristatyme, norėdami nurodyti, ar registruojant pardavimo užsakymo važtaraštį DK norite atpažinti įplaukas. Ši pasirinktis paprastai naudojama, kai yra ilgas delsa tarp pardavimo užsakymo važtaraščio ir SF arba kai neįmanoma išrašyti visų laikotarpio pardavimo užsakymų SF. Paprastai šią pasirinktį išjungsite, jei pardavimo užsakymų SF registruosite iš karto po to, kai užregistruosite važtaraštį. Tokiu būdu išvengsite papildomų DK registravimus, kurie bus nedelsiant atšaukti išrašant pardavimo užsakymo SF.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Kada įjungti kaupimo įsipareigojimus produkto gavimo kvito pasirinktį?

Daugelyje organizacijų norite įgalinti visų prekių modelių grupių gavimo įsipareigojimų kaupimo parinktį, neatsižvelgdami į tai, ar turite atsargų produktą, **ar** nekaupiate produkto. Ši pasirinktis naudojama kaupimo registravimui DK, remiantis gavimo dokumento kaina. Kadangi pirkimo užsakymo produkto gavimo kvito registravimas paprastai uždelsimas ir SF registravimas, dauguma organizacijų turi pripažinti balanso įsipareigojimą, kad atitiktų vietinius nuostatus, pvz., bendrai priimtų apskaitos praktikos (GAAP). Jei tiekimo grandinės valdymas nėra jūsų finansinių duomenų įrašo sistema, galite norėti išjungti šią pasirinktį. Jei jūsų organizacija naudoja įsigijimo kategorijas pirkimo užsakymuose, **·** **galite valdyti kaupimo reikalavimus, įjungę kategorijos strategijos taisyklės kategorijos strategijos taisyklės parinktį Kaupti pirkimo išlaidas** pirkimo strategijos puslapyje.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Kaip neleisti vartotojui registruoti pirkimo užsakymo gavimo dokumento, jei gavimo dokumento registracija dar neužregistruota?

Jei pirkimo užsakymo registracija dar **neateis**, vartotojui galite neleisti registruoti pirkimo užsakymo gavimo dokumento, įjungę prekių modelių grupės parinktį Registravimo reikalavimai. Ši pasirinktis paprastai naudojama organizacijose, kurios naudoja dviejų veiksmų gavimo procesą, arba scenarijuose, kuriuose turite užregistruoti paketo ar serijos numerį, pavyzdžiui, gaunamuose elementuose. Registravimo **reikalavimo** pasirinktis taikoma *visiems* prekės atsargų gavimų atvejais, o ne tik pirkimo užsakymams. Pavyzdžiui, jis taikomas atsargų žurnalui, kuriame yra teigiamas kiekis, o gamybos užsakymo skelbimo baigtu žurnalas.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Kaip neleisti vartotojui registruoti pirkimo užsakymo SF, jei produkto gavimo kvitas dar neužregistruotas?

Galite neleisti vartotojui **registruoti** pirkimo užsakymo produkto SF, jei pirkimo užsakymo produkto gavimo kvitas dar nebuvo įvykęs, įgalindami prekių modelių grupės parinktį Gavimo reikalavimai. Ši pasirinktis paprastai naudojama organizacijose, kurioms reikia, kad gavimų gavimas būtų faktiškai atpažintas DK kaupimų metu. Gavimo **poreikio** pasirinktis taikoma *visiems* prekės atsargų gavimų atvejais, o ne tik pirkimo užsakymams. Pavyzdžiui, jis taikomas atsargų žurnalui, kuriame yra teigiamas kiekis, o gamybos užsakymo skelbimo baigtu žurnalas. Jei jūsų organizacija pirkimo užsakymuose naudoja įsigijimo kategorijas, **·** **galite valdyti gavimo reikalavimą, įjungę kategorijos strategijos taisyklės parinktį Gavimo reikalavimai pirkimo strategijų** puslapyje.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Kaip neleisti vartotojui registruoti pardavimo užsakymo važtaraščio, jei pardavimo užsakymo išrinkimo sąrašas dar neužregistruotas?

Galite neleisti vartotojui **registruoti** pardavimo užsakymo važtaraščio arba SF, jei pardavimo užsakymų išrinkimo dokumento dar nebuvo, įgalindami prekių modelių grupės pasirinktį Išrinkimo reikalavimai. Ši pasirinktis paprastai naudojama organizacijose, kurios sandėlyje atlieka fizinį paėmimo procesą (pavyzdžiui, naudodamas sandėlio mobilųjį įrenginį paėmimui). Išrinkimo **reikalavimų pasirinktis** taikoma visiems *prekės* atsargų užsakymams, ne tik pardavimo užsakymams. Pavyzdžiui, jis taikomas atsargų žurnalui, kuriame yra neigiamas kiekis, ir gamybos užsakymų išrinkimo dokumento žurnalui.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Kaip neleisti vartotojui registruoti pardavimo užsakymo SF, jei pardavimo užsakymo važtaraštis dar neužregistruotas?

Galite neleisti vartotojui **registruoti** pardavimo užsakymo SF, jei pardavimo užsakymo važtaraštis dar nebuvo įvykęs, įgalindami prekių modelių grupės parinktį Atskaitymo reikalavimai. Ši pasirinktis paprastai naudojama organizacijose, kurios sandėlyje atlieka pakavimo procesą (pavyzdžiui, naudodama sandėlio valdymo mobiliąją programą, kad pakuotų, arba sugeneruodama dokumentą, kuris bus įtrauktas su siunčiamomis prekėmis). Parinktis **Atskaitymo** reikalavimas taikoma visiems *prekės* atsargų išduotims, ne tik pardavimo užsakymams. Pavyzdžiui, jis taikomas atsargų žurnalui, kuriame yra neigiamas kiekis, ir gamybos užsakymų išrinkimo dokumento žurnalui.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Ar galima neleisti parduoti užregistruotų prekių?

Kai prekė užregistruojama jūsų atsargose tiekimo grandinės valdymo sistemoje, kiekis yra faktiškai galimas išduoti sistemoje. *Jei* prekės, kurios buvo užregistruotos, bet dar negauto, turėtų būti išduodamos pardavimo arba gamybos užsakymams, pavyzdžiui, apsvarstyti galimybę naudoti atsargų būseną, atsargų blokavimą, kokybės užsakymus, sulaikymo užsakymus arba rezervavimo funkcijas, siekiant valdyti verslo procesą.

## <a name="production-costing"></a>Gamybos įkainojimas

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Ar galima naudoti vieną žaliavų įkainojimo modelį ir kitą baigtų prekių įkainojimo modelį?

Taip, kiekvienai prekei galima naudoti skirtingus įkainojimo modelius. Gamintojai nepastebėti žaliavų periodinio įkainojimo modelio ir standartinės pusiau baigtų ir baigtų prekių savikainos.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Kaip galima įrenginių pridėtines išlaidas išjungti?

Norėdami sumažinti įrenginio pridėtines išlaidas, pagal savo verslo reikalavimus turite sukurti kiekvieno įrenginio išteklius ir išteklių grupes. Kiekvienas išteklius ar išteklių grupė gali būti priskirti išlaidų kategorijoms, kad būtų galima kontroliuoti įrenginio išlaidas. Kiekvieną išlaidų kategoriją galima susieti su išlaidų grupe, kiekviena išlaidų grupė gali būti naudojama kaip netiesioginių išlaidų apskaičiavimo įkainojimo lape pagrindas.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Kaip įkainojimo lape atpažinti išlaidas, susijusias su energijos suvartojimu (pvz., vandentiekiu, energija ar dujų suvartojimu)?

Paprastai galite atpažinti išlaidas, susijusias su energijos suvartojimu, vienu iš dviejų būdų:

- Sukurkite savo KS arba formulės eilutę. Paprastai ši eilutė kuriama kaip aptarnavimo prekė, ir galima nurodyti matavimo vienetą, kurį imate ryšio su gaminamu kiekiu. Tokiu būdu gamybos proceso metu vartotojas gali naudoti kitą sumą. Galite automatiškai naudoti prekes, remdamasis verte, kurią pasirenkate lauke Sunaudojimo **principas**.
- Sukurkite netiesiogines išlaidas savo įkainojimo lape. Paprastai šis būdas naudojamas paskirstyti bendras jūsų energijos suvartojimo išlaidas gamybos procese. Galite naudoti išlaidų grupę ir absorbavimo pagrindą suvartojimui pagal, pvz., medžiagas ar darbą jūsų maršrute, nustatyti.

Atsižvelgdami į savo ataskaitų, suderinimo ir veiklos reikalavimus, turėtumėte pasirinkti geriausią pasirinktį.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Ar galima perimti išteklių informaciją KS arba formulėje?

Išteklių informaciją galima užfiksuoti tik maršruto operacijoje. Nors galite sukurti aptarnavimo prekę, norėdami pateikti išteklius ir priskirti išlaidas, kad būtų padidintas baigtos prekės išlaidų skaičiavimas, šis būdas paprastai nerekomenduojame. Todėl rekomenduojame sukurti paprastą maršrutą, kuriame būtų viena eilutė išteklių išlaidoms sekti, ir konfigūruoti operaciją, kad ji būtų automatiškai suvartota gamybos užsakymo pradžioje arba pabaigoje.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Ar galima peržiūrėti skaičiavimo informaciją, jei išlaidos įvestos rankiniu būdu?

Ne. Jei kainą įvedate rankiniu būdu **prekių kainos** puslapyje, **nėra** **mygtukų Peržiūrėti skaičiavimo** informaciją ir Ataskaitos skaičiavimo informaciją. Jei pasirenkate **neautomatiniu** būdu įvestos savikainos išlaidų sumavimo pagal išlaidų grupę mygtuką, rodoma apibendrinta eilutė, ir visos išlaidos sumuojami iki baigtos prekės.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Ar sistema skaičiuoja gamybos užsakymo nuokrypius, kai aš neautomatiniu būdu įvesiu išlaidas?

Taip, sistema skaičiuoja nukrypimus, kai neautomatiniu būdu įvedate standartines išlaidas. Tačiau skaičiuojant standartines išlaidas neautomatiniu būdu, visos medžiagų, maršruto ir netiesioginių išlaidų sąnaudos gamybos užsakyme laikomos pakaitalo nuokrypiu. Jei yra papildomų nuokrypių, pvz., papildomų medžiagų suvartojimo ar darbo, jie taip pat bus įrašyti kaip gamybos KS nuokrypiai. Dėl to primygtinai rekomenduojame visada vykdyti prekių, kurios turi KS, maršrutą arba netiesiogines išlaidas, skaičiavimą.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Kaip galima perkelti nuokrypius nuo tarpinės gamybos užsakymo iki pirminio gamybos užsakymo?

Kai naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO ar svertinį vidurkį, tarpinės gamybos išlaidos bus atpažintos jūsų pasirinktame prekių heursio modelyje. Jei jums reikia faktinių išlaidų, galite naudoti žymėjimo principą, kad nurodykite, kuri tarpinė gamyba išduota pirminiu gamybos užsakymui. Arba galite apsvarstyti, pavyzdžiui **, sekimo dimensijų** **·** **grupės paketo arba serijos numerio** dimensijos pasirinktį Finansinės atsargos.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Kaip sunaudojimo principas paveikia suvartojimą?

Sunaudojimo principas KS, formulėje ar maršruto eilutėje valdo laiką ir techniką, naudojamą prekei ar darbui naudoti. Jei pasirenkate *Pradėti*, prekė arba darbas suvartojamas automatiškai, kai pradedate gamybos užsakymą. Jei pasirenkate *Baigti*, prekė arba darbas suvartojamas automatiškai, kai pranešate, kad gamybos užsakymas baigtas. Jei pasirenkate *Rankinis*, vartotojas turi rankiniu būdu paimti medžiagas arba įrašyti laiką užduoties ar maršruto kortelės žurnale. KS ir formulėse taip pat galima *pasirinktiS vietoje*. Jei pasirenkate šią pasirinktį, prekės automatiškai suvartojamos po to, kai perkeliamos į gamybos laiko vietą.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Kaip vykdyti išlaidų skaičiavimus, jei aš esu kelių lygių KS ar formulių?

Apie tai, rekomenduojame pradėti nuo žemiausio skaičiavimo KS ar formulių lygio. Norėdami palengvinti filtravimą masinės veiklos išlaidų skaičiavimuose, galite naudoti skaičiavimo grupes, kad būtų lengviau atskirti produktus. Taip pat rekomenduojame paleisti periodinę KS *lygių perskaičiavimo užduotį* prieš pradedant masinį išlaidų skaičiavimą. Kiekviena organizacija turi atsižvelgti į produktų derinį ir nustatyti strategiją, kuri atitiktų konkrečius jūsų produkto bei KS arba formulės struktūros poreikius.

## <a name="transfer-order-costing"></a>Perkėlimo užsakymo įkainojimas

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Ar yra būdas paskirstyti transportą į perkėlimo užsakymo išlaidas?

Norėdami pridėti išlaidų, galite pridėti išlaidas prie perkėlimo užsakymo. Išlaidų kodas nurodo pridedamas išlaidas debeto ir kredito. Pirmiausia turite sukurti išlaidų kodus atsargų **valdymo modulyje**. Norėdami pridėti mokestį prie perkėlimo užsakymo, perkėlimo **užsakymo** eilutėje pasirinkite Mokesčiai, prie kurių norite pridėti mokestį.

## <a name="variances"></a>Nuokrypiai

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Ar norėčiau nuokrypius laikyti skirtingais, priklausomai nuo vietos ar sandėlio?

Nėra pasirinkties konfigūruoti nuokrypio sąskaitas pagal vietą. Kai išleistam produktui naudojate standartinį įkainojimo kodą, galite pasirinkti pagrindinę sąskaitą, kuri naudojama standartinių išlaidų nuokrypio registravimui **registravimo** puslapyje. Galite pasirinkti konfigūruoti vienos prekės, prekių grupės arba visų prekių sąskaitas. Taip pat galite konfigūruoti vieną išlaidų grupę, išlaidų grupių grupę ar visas išlaidų grupes.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Ar gali atskirti nuokrypius, kurie yra valiutos kursų rezultatas, nuo kitų nuokrypių tipų?

Jei nuokrypis yra valiutos kurso skirtumas tarp pirkimo užsakymo kainos ir standartinės prekės savikainos, nėra būdo atskirti valiutos kurso skirtumą nuo kitų nuokrypių.

## <a name="reporting"></a>Ataskaitos

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Kiek atsargų vertės ataskaitų konfigūracijų aš esu sukurtas ir naudojamas?

Nėra jokio atsargų vertės ataskaitos konfigūracijų, kurias galite sukurti, skaičiaus apribojimo. Turite įvertinti savo konkrečius ataskaitų reikalavimus ir sukurti konfigūracijų, kurios turi būti atitikti tuos reikalavimus, skaičių. Jums reikės bent vienos atsargų vertės ataskaitos konfigūracijos, kad būtų galima vykdyti ataskaitą arba ataskaitos saugojimo pasirinktį.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Ar aš noriu naudoti atsargų vertės ataskaitą prekės kainai kiekviename sandėlyje analizuoti?

Taip. Atsargų vertės ataskaitos **konfigūracijoje** **galite** įgalinti kiekvienos **sandėlio** dimensijos pasirinktį Peržiūrėti arba Bendroji suma. Tačiau ataskaitoje bus tik dimensijų, kuriose saugojimo dimensijų **grupei** taikoma parinktis Finansinės atsargos, vertės. Kitų dimensijų stulpeliuose bus rodomi tušti stulpeliai. Daugiau informacijos ieškokite atsargų [vertės ataskaitos pavyzdžiai ir logika](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Kaip peržiūrėti atsargų kiekį tam tikrą datą naudojant svertinį vidurkį?

Galite naudoti atsargų **skirstymo pagal terminus** ataskaitą, **kurioje** yra stulpelis Vidutinė vieneto savikaina, kurioje rodoma atsargų vertė nuo tam tikros datos. Daugiau informacijos ieškokite atsargų skirstymo [pagal terminus ataskaitos pavyzdžiai ir logika](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Kaip peržiūrėti, kurios gavimo operacijos sudengios su išdavimo operacija?

Atsargų operacijos sudengimą **galite peržiūrėti pasirinkdami Sudengimą arba Išlaidų naršyklę atsargų skirtuke, atsargų operacijos veiksmų srityje arba informacijos apie atsargų operacijas** **·** **·** **·** **puslapyje**. Jei pasirenkate gavimą, kad būtų galima peržiūrėti su operacija susijusius gavimus, išlaidų naršyklė nerodo išsamios informacijos. Informacija rodoma tik pasirinkus išdavimo operaciją.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Kaip atsargų vertės ataskaitoje parodytos prekės, kurių faktinis kiekis ir neigiama finansinė vertė yra teigiamas?

Atsargų vertės ataskaita atskiria faktines ir finansines sumas bei kiekius į savo stulpelius. Ataskaitoje rodomos vertės yra datų intervalo, pasirinkto ataskaitos metu, metu. Rodomas apibendrinimo lygis priklauso nuo pasirinktų parametrų. Jei yra faktiškai gautų ir finansiškai išduotų operacijų, kiekiai ir vertės sumuojamos atskirai. Jei pasirinkote peržiūrėti išsamumo lygį kaip operacijas, kiekvieno gavimo ir išdavimo eilutės rodomos atskirai, atitinkamai rodomi faktiniai ir finansiniai kiekiai bei sumos. Daugiau informacijos ieškokite atsargų [vertės ataskaitos pavyzdžiai ir logika](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Koks saugojimo ir sekimo dimensijų grupių poveikis atsargų vertės ataskaitai?

Jei saugojimo arba **sekimo dimensijų grupėje įgalinate dimensijos parinktį Finansinė vertė,** **·** **atsargų vertės ataskaitos konfigūracijoje galite pasirinkti dimensijos pasirinktį Peržiūrėti arba Bendroji suma.** Jei pasirinksite dimensijos, **kurioje** **nėra** pasirinkta finansinės vertės pasirinktis, **pasirinktį** Rodinys arba Bendroji suma, ataskaitos išeigos stulpelis bus tuščias. **Jei** saugojimo ar sekimo dimensijų grupėje įgalinote dimensijos finansinės vertės pasirinktį **ir** **atsargų** vertės ataskaitos konfigūracijoje nepasirinkote pasirinkties Peržiūrėti arba Bendroji suma, sistema susumuos pasirinktų dimensijų, kuriose jos finansiškai sekamos, vertes.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Ar galima pritaikyti įdėtąsias Power BI ataskaitas įkainoti?

Taip, vartotojai, kurie turi tinkamas saugos teises, gali atnaujinti ataskaitos kūrimo sritį bet kuriai tiekimo Power BI grandinės valdymo ataskaitoje. Daugiau informacijos ieškokite Įdėtųjų ataskaitų [pritaikymas analitinėse darbo erdvėse](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Kur galima peržiūrėti nuokrypio analizės išrašą?

Nuokrypio analizės išrašą **\> galite pasiekti nueię į Išlaidų valdymo užklausas \> ir ataskaitas Atsargų apskaita –** **\>\> analizės ataskaitos ar Išlaidų valdymo užklausos ir ataskaitos Gamybos apskaita – analizės ataskaitos.** Abi pasirinktys atidaro tą pačią ataskaitą ir jos veikimo būdas yra toks pats.

## <a name="item-prices-and-default-costs"></a>Prekių kainos ir numatytosios išlaidos

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Ar galima prižiūrėti kiekvieno produkto varianto išlaidas?

Taip. Norėdami įgalinti kainas pagal **produkto variantą,** galite įjungti parinktį **Naudoti** savikainą pagal variantą puslapyje Tvarkyti išlaidas "FastTab **·**". (Ši pasirinktis galima tik visiems produktams.) Tada prekės kainos **puslapyje (** **·** **kurį galite atidaryti iš įkainojimo versijos puslapio arba išleisto produkto puslapio)** **·** **galite pasirinkti Dimensijų rodymą, kad nurodydami, ar norite, kad būtų rodoma dimensija Konfigūracija,** **Dydis,** Spalva **arba** **Stilius.** Norėdami įrašyti nustatymą ir naudoti pasirinktas dimensijas kiekvieną kartą, kai atidarysite puslapį, įgalinkite **pasirinktį** Įrašyti nustatymą ir pasirinkite **Gerai**. Galite įvesti tik prekių, kurių dimensijos yra aktyvios produkto dimensijų grupėje, dimensijas.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Ar galima prižiūrėti kiekvieno sandėlio išlaidas?

Ne, prekės kainos pagal sandėlį tvarkyti negalite. Tačiau galite tvarkyti prekybos sutartis dėl pirkimo kainų arba pardavimo kainų pagal sandėlį. Pirmiausia pasirinkite dimensijos **parinktį Skirta pirkimo** kainoms **arba** Pardavimo kainų, kuri bus skirta dimensijai, saugojimo **dimensijų grupės** puslapyje. Tada, kai sukuriate prekybos sutarčių žurnalą ir atidarote dimensijų eilutes, pasirinkite Atsargų rodymo dimensijos, kad pasirinktumėte, **\>** kuri dimensija tinklelyje turi būti rodoma. Norėdami įrašyti nustatymą ir naudoti pasirinktas dimensijas kiekvieną kartą, kai atidarysite puslapį, įgalinkite **pasirinktį** Įrašyti nustatymą ir pasirinkite **Gerai**. Galite įvesti tik prekių, kurių dimensijos yra aktyvios produkto dimensijų grupėje, dimensijas.

### <a name="what-are-price-charges"></a>Kokie kainos mokesčiai?

Kainos išlaidos suteikia būdą pridėti fiksuotą sumą prie prekės kainos arba prekybos sutarties vieneto kainos. Kai į lauką Kainos išlaidos **įvedate** sumą, taip pat galite įvesti vertę lauke **Mokesčių** kiekis. Kainos išlaidos amortizuoja jūsų nurodytą išlaidų kiekį. Įjunkite **parinktį Įtraukta į vieneto** kainą, jei norite įtraukti kainos išlaidas į prekės vieneto kainą. Ši pasirinktis visada įgalinta dėl standartinių išlaidų.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Kaip konfigūruoti prekių, įsigytų keliomis valiutomis, kainas?

Jei **išleisto** **produkto** puslapio lauke Pirkimo kaina įvesite numatytąją kainą, laikoma, kad ji bus juridinio subjekto, kuriame esate, apskaitos valiuta. Taip pat, **·** *jei* įkainojimo versijoje įvedate pirkimo kainą, kai kainos tipo laukas nustatytas kaip Pirkimas, kaina laikoma savo juridinio subjekto apskaitos valiuta. Kai sukuriate pirkimo užsakymą tiekėjui, kuris turi kitą valiutą, **sistema automatiškai konvertuos valiutą iš apskaitos valiutos sumos į operacijos valiutą naudodama valiutos kursą, kurį nurodėte DK lauke Apskaitos valiutos** kurso tipas.

Kai sukuriate prekybos sutarčių žurnalą, galite nurodyti valiutą, kuria išreiškiama kaina kiekvienoje eilutėje. Galite kurti kelių valiutų, konkrečių tiekėjų ir daugelio kitų koeficientų derinių prekybos sutartis. Jei sukuriate pirkimo užsakymą, kuriame yra pasirinktos valiutos prekybos sutartis, sistema naudos prekybos sutartį, kurioje naudojama atitinkama valiuta. Kai registruojate operacijas, pvz., produkto gavimo kvitus arba SF, suma bus konvertuojama į DK apskaitos valiutą naudojant apskaitos valiutos kursą, kurį nurodote DK.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Kaip konfigūruoti prekių, įsigytų keliomis valiutomis, išlaidas?

Išlaidų negalima sukonfigūruoti daugiau nei viena valiuta. **·** **Išlaidos**, kurias nurodote prekės kainai arba numatytosios išlaidos, kurias įvedate lauke Kaina, esančio išleisto produkto puslapio "FastTab **·**" Valdyti išlaidas, visada išreiškiamos pasirinkto juridinio subjekto DK apskaitos valiuta.

Jei jūsų organizacija naudoja standartinį įkainojimo kursą, turite apibrėžti išlaidų, kai yra kelios valiutos, nustatymo strategiją. Taip pat turite nurodyti reguliariai atnaujinamų išlaidų procesą, kad būtų galima sumažinti užregistruotų nuokrypių skaičių.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Ar skaičiuojant pardavimo kainas galima naudoti išlaidų grupės puslapio parametrą Pelnas?

Taip, galite naudoti parametrą **Pelnas išlaidų** **grupės** puslapyje, norėdami pridėti procentą, kai pardavimo kainos skaičiuojamos naudojant išlaidų skaičiavimą. Daugiau informacijos ieškokite KS [skaičiavimuose](bom-calculations.md).

## <a name="marking"></a>Žymėjimas

### <a name="how-does-marking-affect-periodic-costing-models"></a>Kaip žymėjimas paveikia periodinius įkainojimo modelius?

Jei naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO ar svertinį vidurkį, ir pažymėjote gavimo operaciją pagal išdavimo operaciją, heursinis prekės modelis ignoruojamas atsargų uždarymo proceso metu. Vietoj to sistema iš išdavimo išlaidų naudos faktines gavimo išlaidas.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Kas įvyksta per atsargų uždarymą, kai aš naudojau žymėjimą?

Pažymėjus gavimus ir gavimus, atsargų uždarymas sudengs kartu pažymėtas operacijas. Kai naudojant sudengimą kurti naudojamas žymėjimas, puslapio **Sudengimas** **laukas** Principas bus nustatytas kaip *Žymėjimas*. Jei operacija pažymėta prieš faktiškai arba finansiškai atnaujinant, išdavimas vietoj einamųjų vidurkio išlaidų naudos pažymėtas gavimo išlaidas. Jei operacijos pažymimos po finansinio atnaujinimo, atsargų uždarymo ir koregavimo procesas koreguos išdavimo išlaidas, kad jos sutaps su gavimo išlaidomis.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Ar galima operacijas žymėti rankiniu būdu, kai aš esu naudodami standartinį įkainojimo ar slankusį vidurkį?

Ne, naudodami standartinę įkainojimo ar slankusį vidurkį, negalite neautomatiniu būdu pažymėti gavimų ar gavimų. Jei operacijos (pvz., tiesioginio pristatymo arba vidinės įmonės užsakymai) pažymimos automatiškai, žymėjimo įrašas lieka ir veiks kaip sunkus rezervavimas. Tačiau jei naudojate standartinį įkainojimo ar slankusį vidurkį, įrašų žymėjimas neturi įtakos prekių kainai.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Kaip žymėjimas veikia pelno ir nuostolio išrašą?

Kai išdavimo operaciją pažymite prieš gavimą, išdavimo išlaidos atitiks pasirinktą gavimą. Kai faktiškai ir finansiškai registruojate išdavimą, **registravimas turės įtakos parduotų, pristatytų prekių savikainai ir parduotų prekių savikainai,** **sąskaitose, kurioms išrašytos SF,** kurias nurodėte atsargų registravimo šablone. Jei operacija pažymėta po faktinio ar finansinio atnaujinimo, *atsargų* uždarymo ir koregavimo proceso metu bus sukurtas koregavimas, atitinkantis **kvitą, kuris koreguos** parduotų prekių savikainą, sf sąskaitą ir korespondentų sąskaitą, **kurią nurodėte vienetų savikainai,** išrašytai SF (atsargoms).

### <a name="how-does-marking-affect-master-planning"></a>Kaip žymėjimas paveikia bendrąjį planavimą?

Bendrojo **planavimo parametrų** puslapio standartinio **atnaujinimo skirtuke** yra laukas, pavadintas Atnaujinimo **žymėjimas**. Pasirinktis, kurią pasirenkate, naudojama, kai galutinai sugeneruojamas bendrojo planavimo suplanuotas užsakymas. Galimos toliau nurodytos parinktys:

- *Ne* – sistema nežymi.
- *Standartinis* – sistema pažymi gavimus prieš išdavimus pagal iškvietimą. Poreikio užsakymas žymimas pagal įvykdymo užsakymą. Jei įvykdymo metu lieka dalis kiekio, įvykdymo užsakymas nepažymimas.
- *Išplėstas* – sistema pažymi ir poreikio užsakymus, ir įvykdymo užsakymus, neatsižvelgdama į tai, ar įvykdymo užsakyme kiekis lieka atviras.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Neigiamos atsargos

### <a name="when-should-i-allow-physical-negative-inventory"></a>Kada leisti faktines neigiamas atsargas?

Apskritai, rekomenduojame leisti faktines neigiamas atsargas, nes jūsų sandėlyje neįmanoma turėti mažiau nei 0 (nulių) materialios prekės. Tačiau kai kurių pramonės šakų ir verslo scenarijų verslo procesai gali apriboti operacijas, kurioms būtina, kad atsargos būtų faktiškai neigiamos. Pavyzdžiui, mažmenininkai gali nenori uždrausti parduoti prekę, kuri pristatoma į kasos aparatą, net jei sistema nurodo, kad prekių nėra. Apdoroti gamintojai pateikia kitą pavyzdį. Šiems gamintojams suvartojama suma gali viršyti formulėje rekomenduojamą sumą. Taip pat galima vietoj tiksliai įvertinti suvartojimą, kad jis viršytų konkrečios vietos, pvz., talpyklos, sumą.

Kai įmanoma, turite įvertinti savo verslo procesą ir bandyti jį patobulinti, kad užtikrinti, jog atsargų nebus galima neigiamas. Jei turite leisti neigiamas atsargas, turite turėti aiškų verslo procesą neigiamoms atsargoms taisyti, nes tai gali neigiamai paveikti įkainojimas.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Kada leisti neigiamas finansines atsargas?

Apskritai, rekomenduojame dauguma organizacijų leisti neigiamas finansines atsargas. (Dažniausiai pirkimo užsakymo SF nėra apdorojamos prieš tai, kai galėsite siųsti prekes.) Jūs turėtumėte įgalinti šią pasirinktį, kai turite konkrečius verslo procesus, kuriems reikia, kad pardavimo kaina atspindėtų galutinę pirkimo užsakymo kainą. Pvz., šis reikalavimas gali būti taikomas gamybos pagal užsakymą pramonėje arba tam tikroje regionuose, kur jis diktuojamas įstatymo.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Kas atsitinka su mano problemų išlaidomis, kai atsargų kiekis neigiamas?

Kai jūsų prekės atsargos yra neigiamos, o jūs išduodate daugiau prekių nei fiziškai turite, sistema naudos numatytąją prekės kainą veikiančiam vidurkiui apskaičiuoti, jei naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO arba svertinį vidurkį. Jei nenurodyta numatytoji prekės kaina, sistema išduoda atsargas 0 (nuliais) verte. Dėl to gali būti atlikti būsimi jūsų einamosios vidurkio arba slankusio vidurkio skaičiavimai.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Ar galima neleisti paimti, supakuoti arba parduoti prekių pardavimo užsakymuose ir gamybos užsakymuose, jei nepakanka turimų atsargų?

Taip. Rekomenduojame išjungti prekių modelių **grupės** parinktį Faktinis neigiamas, kad prekės nebūtų paimtos, supakuotos arba parduotos pardavimo užsakymuose ir gamybos užsakymuose.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Ar galima neleisti išrašyti prekių SF pardavimo užsakyme, jei nebuvo išrašyta tos pačios prekės pirkimo užsakymų SF?

Taip. Patariame išjungti **prekių** modelių grupės parinktį Finansinė neigiama, kad nebūtų galima išrašyti prekių SF pardavimo užsakyme, jei nebuvo išrašyta tos pačios prekės pirkimo užsakymų SF.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Kaip neigiamos atsargos paveikia finansinius koeficientus, pvz., bendrojo pelno maržą?

Kai leisite savo atsargai gauti neigiamą vertę, balanso lape gali būti nuvertinta atsargų vertė ir jūsų pelno ir nuostolio išraše parduotų prekių išlaidos, ypač jei nėra konfigūruotos jūsų prekių numatytosios kainos. Todėl finansinės ataskaitos ir koeficientai, pvz., bendrojo pelno maržos, gali būti pervertinti, nes išlaidos yra klaidingos. Jei naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO ar svertinį vidurkį, paleidus atsargų uždarymą ir koregavimo procesą, po to, kai buvo pakoreguoti neigiami atsargų kiekiai, galima koreguoti problemų vertę. Tačiau jei naudojate slankusį vidurkį, nėra būdo perkainoti atskiras operacijas.

### <a name="how-should-i-correct-negative-inventory"></a>Kaip taisyti neigiamas atsargas?

Rekomenduojame dažnai stebėti ir taisyti neigiamas atsargas, kai jūsų organizacija arba verslo reikalavimai diktuoja, kad leistumėte, jog jūsų atsargos turėtų būti neigiamos. Atsargų vertes galima koreguoti atliekant ciklų skaičių, registruojant koregavimą arba registruojant judėjimo žurnalą. Jei turite atpažinti netikėtą atsargų pelną tam tikroje DK sąskaitoje, turite planuoti naudoti judėjimo žurnalą. Kitu atveju, kai naudojate ciklų skaičiavimo arba atsargų koregavimo procesą, **·** **sistema užregistruos atsargų koregavimą atsargų gavimo sąskaitoje ir paslinks atsargų išlaidas, pelno sąskaitas,** kurias nurodote atsargų registravimo šablone.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Ar man reikia sukurti naują prekę, jei mano atsargų rezultatai neigiami, ir aš esu naudoja slankusį vidurkį?

Ne. Jei jūsų organizacija leidžia atsargai pasiekti fiziškai neigiamą ir naudojate slankusį vidurkį kaip atsargų modelį, **sistema** naudos atsarginę savikainos seką, priskirtą atsargų ir sandėlio valdymo parametrų puslapyje, kad nustatytų, kaip išlaidos bus priskirtos jūsų problemų metu. Apskritai, rekomenduojame išvengti faktinio atsargų neigiamo leidžiant. Daugiau informacijos rasite kitų klausimų šios temos skyriuje [Neigiamos](#negative-inventory) atsargos.

## <a name="not-stocked-products"></a>Ne atsargose neturimi produktai

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Ar galima registruoti atsargose nepardavimo produktų pardavimo užsakymo išrinkimo dokumentus?

Kai generuojate pardavimo užsakymo, kuriame yra prekių, esančių prekių modelių grupėje, kuri nėra sandėliuota, išrinkimo sąrašą, nematysite jokių tų atsargose neįrašomų prekių eilučių. Negalite naudoti sandėlio valdymo mobiliosios programos prekėms apdoroti.

Kai generuojate pardavimo užsakymo, kuriame yra prekių, esančių prekių modelių grupėje, kuri nėra sandėliuojant, važtaraštį, **·** *lauke* Kiekis nustatykite paimtą kiekį, o ne atsargose atsargose neįduotas prekes, kad į dokumento generavimą būtų įtrauktos atsargos. Pasirinkus *Visi*, į važtaraštį bus įtrauktos tik atsargose laikomas prekes.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Ar naudoti ne sandėliuojamas produktas ar kategoriją (pardavimo kategorija ar įsigijimo kategorija)?

Ne atsargose produkto ir kategorijos pasirinkimas priklauso nuo jūsų konkrečių verslo poreikių. Neparduoti produktai paprastai labiau kontroliuoja numatytąsias vertes, pvz., pirkimo užsakymų ir pardavimo užsakymų kiekius ir kainas. Todėl ne atsargose esantys produktai pageidaujami scenarijuose, kuriuose tas pats produktas ar paslauga perkami arba parduodami daugiau nei vieną kartą. Kategorijos naudingos scenarijuose, kuriuose kaina, prekės, aprašymai ir t. t. yra prieštaringi tarp operacijos ir operacijos. Kategorijos taip pat gali būti naudojamos bet kuriame produkte norint padėti klasifikuoti parduodamo arba nupirkto produkto tipą.

## <a name="service-items"></a>Aptarnavimo prekės

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Koks skirtumas tarp aptarnavimo prekės ir ne sandėliuojami produktai?

Aptarnavimo prekė yra produkto tipas. Kai kuriate naujai išleistą produktą, produkto tipo **lauką** galite nustatyti kaip Prekė *arba* *Paslauga*. *Prekė* paprastai pasirenkama nurodyti, kad prekė materiali, *o paslauga paprastai* pasirenkama norint nurodyti, kad prekė nemateriali.

Bet koks išleistas produktas, neatsižvelgiant į tai, ar tai prekė, ar paslaugų produktas, gali būti laikomas kaip atsargos, ar ne. Atsargų arba ne atsargose laikomą parametrą kontroliuoja prekių modelių grupė, kurią pasirenkate išleistiam produktui. Kai pasirenkate prekių grupę, kuri nėra sandėliuojami, sistema nekuria, pvz., susijusio pardavimo užsakymo arba pirkimo užsakymo atsargų operacijų.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Ar į KS galima įtraukti ne sandėliuojamas prekes?

Ne, išleisti produkto, susieto **su** prekių modelių grupe, kurioje parinktis Atsargos išjungta KS arba formulėje, negalima. Nesvarbu, ar laukas Produkto **tipas nustatytas** kaip Prekė *, Ar* *Paslauga*. Į KS arba formulės eilutes galima įtraukti tik atsargose laikomas prekes.

## <a name="costing-modelspecific-questions"></a>Įkainojimo modelis – konkretūs klausimai

### <a name="which-costing-model-should-i-use"></a>Kurį įkainojimo modelį naudoti?

Įkainojimo modeliai, kuriuos turėtumėte pasirinkti, priklauso nuo jūsų verslo poreikių. Prieš pasirinksite įkainojimo modelį, kurį naudosite tiekimo grandinės valdymo srityje, turite patikrinti, ar šis modelis leidžiamas pagal jūsų vietines taisykles. Rekomenduojame patvirtinti savo pasirinkimą patvirtintu buhalteriu jūsų regione.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Ar mano organizacijoje galima naudoti daugiau nei vieną įkainojimo modelį?

Taip. Nėra riboti prekių modelių grupių ar įkainojimo modelių, kuriuos galite pasirinkti tiekimo grandinės valdymo srityje, skaičiaus.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Ar kiekvienai prekei galima naudoti daugiau nei vieną įkainojimo modelį?

Ne. Kiekvienam išleistaam produktui galite pasirinkti tik vieną įkainojimo modelį. Šią elgseną kontroliuoja prekės modelio grupė. Jei atsargų verčių ataskaitai pateikti turite naudoti daugiau nei vieną įkainojimo modelį, turėtumėte apsvarstyti galimybę naudoti visuotinių atsargų apskaitos priedą.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Naudojant gamybos vykdymą, kurią įkainojimo metodologiją naudoti?

Įkainojimo modeliai, kuriuos turėtumėte pasirinkti, priklauso nuo jūsų verslo poreikių. Nėra konkretaus įkainojimo modelio naudojimo pranašumas ar pranašumas, kai jūsų organizacija taip pat naudoja gamybos vykdymą.

### <a name="when-is-fefo-used"></a>Kada naudojamas FEFO?

Pirma pasibaigė, pirma iš (FEFO) nėra įkainojimo metodologija. Vietoj to, tai yra rezervavimo technika, kuri dažnai naudojama gamybos organizacijose. Galite įgalinti FEFO rezervavimus prekės modelio **grupei, įjungę FEFO** datos kontroliuojamą pasirinktį ir pasirinkdami vertę išrinkimo **kriterijų** lauke.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Ar yra našumo išmokų pasirenkant vieną įkainojimo modelį per kitą?

Apskritai, jūsų parenkamas prekės įkainojimo modelis turi minimalią įtaką bendram sistemos našumui. Tačiau jūsų naudojamas atsargų įkainojimo modelis gali paveikti laiko, kurio reikia atsargų uždarymui arba perskaičiavimui vykdyti, kiekį. Pavyzdžiui, jei naudojate standartines išlaidas arba slankusį vidurkį, atsargų uždarymo procesas sistemai turi minimalios įtakos, nes ji neat atnaujinti kiekvienos atsargų operacijos ir kurti sudengimų. Tačiau periodinis įkainojimo modelis, pavyzdžiui, FIFO, LIFO ar svertinis vidurkis, gali padidinti laiko, kuris reikalingas atsargų uždarymo procesui užbaigti, kiekį. **Uždarymo procesas gali būti ilgesnis** **·** *·*, kai lauke Uždarymo atsargų procesas įvedate didžiausią leidžiamą pašalinės vertės kiekį: lauke Uždaromos prekės – mažas skaičius.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Kada naudoti parinktį Fiksuota gavimo kaina?

Kai prekių modelių **grupės puslapyje** **pažymite** prekės žymės langelį Fiksuota gavimo kaina, sistema naudos gavimo kainą kaip standartines atsargų gavimo išlaidas. Jei yra skirtumas tarp pirkimo kainos ir numatytosios prekės savikainos, sukonfigūruotos produktui, **·** **skirtumas bus registruojamas fiksuotos gavimo kainos pelno arba fiksuotos gavimo kainos nuostolio sąskaitoje** ir **korespondentinę** sąskaitą Fiksuotos gavimo kainos korespondentinė sąskaita. (Visos šios sąskaitos nurodytos **Registravimo** puslapis.)

Turite pažymėti **žymės** langelį Fiksuota gavimo kaina, kai naudojate periodinį įkainojimo modelį, pvz., FIFO, LIFO ar svertinį vidurkį, ir reikalaujate, kad pirkimo kainų nuokrypis būtų sekamas DK, jei kvito kaina skiriasi nuo numatytosios prekės savikainos.

### <a name="moving-average"></a>Slankusis vidurkis

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Ar slankusis vidurkis yra toks pat kaip slankiojo vidurkio?

Terminai slankiojo vidurkio, slankiojo vidurkio ir slankiojo vidurkio dažnai naudojami sinonimu. Iš šių sąlygų, slankusis vidurkis yra vienintelis oficialus įkainojimo modelis, kurį galima naudoti tiekimo grandinės valdymo metu. Nors einamas vidurkis nėra oficialus įkainojimo modelis, tai technika, naudojama naudojant periodinį įkainojimo modelį, pvz., FIFO, LIFO arba svertinį vidurkį. Terminas "nefiksuotis vidurkis" nėra naudojamas tiekimo grandinės valdymo metu ir kitose sistemose gali turėti skirtingų konteimentų.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Kaip, naudojant slankusį vidurkį, galima talpinti skirtumą tarp produkto gavimo kvito kainos ir SF kainos?

Kai naudojate slankusį vidurkį, faktinė kaina (gavimo kaina) naudojama visų išdavimo operacijų slankusis vidurkiui apskaičiuoti. Jei yra skirtumas tarp faktinių išlaidų (gavimo kainos) ir finansinių išlaidų (SF kainos), **·** **·** **sistema** automatiškai užregistruos skirtumą pagrindinėje sąskaitoje, kuri nurodyta svertinio vidurkio registravimo tipo kaina, atsargų registravimo šablono puslapio skirtuke Atsargos.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Kur DK pateikiamas slankusio vidurkio kainų skirtumas?

Kai yra faktinio atnaujinimo registravimo ir gavimo finansinio atnaujinimo kainų skirtumas, skirtumas užregistruojamas pagrindinėje sąskaitoje, **·** **·** **kuri** nurodyta kaip svertinio vidurkio registravimo tipo kaina, atsargų registravimo šablono puslapio skirtuke Atsargos. Daugiau informacijos ieškokite slankusis [vidurkis](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Jei naudojate slankusį vidurkį, kas atsitinka, jei išdavimas yra prieš gavimą?

Paprastai prieš gavimą gali būti išdavimas, nes leidžiate prekių modelių grupės faktines neigiamas atsargas arba išdavimas vėluojamas kurti. Daugiau informacijos ieškokite šios temos [skyriuje Neigiamos](#negative-inventory) atsargos.

Jei operacijas vėluojate, rekomenduojame atidžiai apsvarstyti savo verslo procesą ir operacijas, siekiant nustatyti, ar yra būdas išvengti šio scenarijaus. Jei operacijai, kuri naudoja slankusį vidurkį, sukurkite operacijos datą, sistema operacijai priskirs dabartinį slankusį vidurkį. Vėlesnės problemos nereguliuojamas. Daugiau informacijos apie slankusį vidurkį su atgalinės prekybos operacijomis ieškokite slankusis [vidurkis](moving-average.md).

### <a name="standard-costing"></a>Standartinis įkainojimas

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Koks skirtumas tarp standartinės įkainojimo ir fiksuotos gavimo kainos?

Standartinis įkainojimas reikalauja, kad jūs nurodytumėte prekės kainą ir suaktyvintumėte įkainojimo versijos išlaidas. Šios išlaidos naudojamos visiems gavimų ir gavimų kvitams. Gavimų į atsargas **nuokrypiai** **įrašomi** DK naudojant standartinių išlaidų nuokrypio sąskaitas, kurias nurodote atsargų registravimo šablono puslapio skirtuke Standartinė savikaina.

Tačiau, kai naudojate fiksuotą gavimo kainą, tik gavimų išlaidos yra fiksuotos, **ir** sistema naudoja išlaidas, kurias nurodėte puslapyje Tvarkyti išlaidas "FastTab **", skirtame išleistame** produkte. Dėl numatytųjų išlaidų ir pirkimo užsakymo kainos skirtumų pirkimo kainos nuokrypis bus registruojamas fiksuotos gavimo kainos pelno ir nuostolio sąskaitose. Išduodant naudojama ne fiksuota gavimo kaina. Užregistravimo metu išduodami duomenys bus įvertinti pagal paleidimo vidurkį (nebent naudojate žymėjimą), ir jie bus perkainoti į euristinį modelį, kurį pasirenkate paleisdami atsargų uždarymą.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Ar galima naudoti FEFO rezervavimus su standartine savikaina?

Taip, galite naudoti FEFO rezervavimus prekių modelių grupėje, kai pasirenkate standartinę savikainą. FEFO rezervavimai kontroliuoja rezervavimo logiką, kuri naudojama faktiniam prekių tvarkymui, tuo tarpu standartinė savikaina kontroliuoja faktines ir finansines prekės išlaidas.

### <a name="can-i-upload-pending-prices"></a>Ar galima įkelti laukiančias kainas?

Taip, norėdami įkelti laukiamą kainą galite naudoti "Excel" priedą arba duomenų valdymo sistemą. Rekomenduojame naudoti šiuos objektus:

- Laukiančios prekių kainos (V2)
- Laukiančios maršruto išlaidų kategorijų vienetų savikainos
- Įkainojimo lapo mazgo skaičiavimo koeficientai (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Kaip dažnai galima atnaujinti standartines prekės išlaidas?

Nėra dažnio ribos, kada galima suaktyvinti naujas standartines išlaidas. Jei aktyvinsite naujas prekės išlaidas tą pačią dieną, kai buvo suaktyvintos paskutinės išlaidos, sistema naudos naujausias naujų operacijų ar atnaujinimų (pvz., esamų operacijų naujinimus).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Ar galima išjungti ar panaikinti suaktyvintas išlaidas?

Ne, suaktyvintos savikainos išjungti ar panaikinti negalima. Jei išlaidos netinkamai suaktyvintos, galite suaktyvinti naujas išlaidas, kurių išlaidos teisingos.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Ar skaičiavimo grupės naudojamos su standartine savikaina?

Skaičiavimo grupes galima naudoti su bet kuria preke, neatsižvelgiant į jūsų naudojamą prekės modelių grupę. Skaičiavimo grupės naudojamos išlaidų sumavimo arba išlaidų skaičiavimo proceso metu, kad būtų nustatyti parametrai, kurie turėtų būti naudojami prekėms, kurioms vykdomas skaičiavimas. Daugiau informacijos apie skaičiavimo grupes ieškokite KS [skaičiavimų grupėse](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Kada naudoti suplanuotą įkainojimo versiją?

Įkainojimo versijų tipas gali būti Standartinė *savikaina arba* Suplanuota *savikaina*. Standartinis *išlaidų* tipas naudojamas išlaidoms, kurios yra aktyvios sistemoje ir bus registruojamos operacijose. Suplanuotų *išlaidų* tipas naudojamas modeliuojant išlaidas ir neturi įtakos operacijų išlaidoms.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Ar gali bendros vieno objekto išlaidos būti perkeltos į kitą objektą kaip pardavimo išlaidas?

Nėra automatinio išlaidų kopijavimo iš vienos įmonės į kitą būdo. Be to, nėra automatinio išlaidų kopijavimo iš pirkimo kainos į pardavimo kainą būdo. Jei jūsų organizacija turi atlikti vieną iš šių užduočių, apsvarstykite, ar galite naudoti duomenų valdymo sistemą, norėdami eksportuoti duomenis iš įkainojimo versijos ir įkelti į kitą įmonę, kaip pardavimo kainą įkainojimo versijoje arba kaip prekybos sutartį. Gali reikėti neautomatinio failų valdymo.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Koks geriausias būdas nukopijuoti planuojamas išlaidas į standartinę įkainojimo versiją?

Galite naudoti mygtuką Kopijuoti **įkainojimo** **versijų** puslapyje, norėdami kopijuoti prekių kainas, išlaidų kategorijos kainas ar netiesiogines išlaidas iš vienos įkainojimo versijos į kitą.
