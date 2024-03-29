---
title: Pasiūlymų patvirtinimų (RFQ) apžvalga
description: Šiame straipsnyje pateikiama pasiūlymų patvirtinimų (RFQ) apžvalga. Organizacijos išduoda RFQ, kai nori pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų.
author: GalynaFedorova
ms.date: 10/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2154"
- intro-internal
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89abf82879ab08f2341ce5b14e6af1d5c42140b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895589"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Pasiūlymų patvirtinimų (RFQ) apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama pasiūlymų patvirtinimų (RFQ) apžvalga. Organizacijos išduoda RFQ, kai nori pirkti prekes arba paslaugas ir gauti konkurencingų pasiūlymų iš kelių tiekėjų. RFQ tiekėjų prašoma pateikti nurodyto prekių kiekio kainas ir pristatymo laiką.
Be to, galite paprašyti tiekėjų nurodyti, ar bus papildomų išlaidų, pvz., siuntimo išlaidų, arba nuolaidų didelių užsakymų ar ankstyvo tiekėjo SF apmokėjimo atveju.

RFQ procesą sudaro toliau pateiktos užduotys.

1. RFQ kūrimas ir siuntimas vienam ar keliems tiekėjams.
1. Kainos siūlymų (RFQ atsakymų) gavimas ir registravimas.
1. Priimtų kainos siūlymų perkėlimas į pirkimo užsakymą, pirkimo sutartį ar pirkimo paraišką.

Toliau esančiame paveikslėlyje pateikiama RFQ proceso apžvalga.

[![RFQ procesas.](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Galite kurti RFQ atvejį iš suplanuotų užsakymų, pirkimo paraiškos arba įvesti neautomatiniu būdu. RFQ atvejis yra pagrindinis dokumentas, naudojamas išduodant RFQ kiekvienam tiekėjui.

Paruošę RFQ atvejį ir įtraukę tiekėjų, RFQ atvejyje pasirinkite **Siųsti** (viešajame sektoriuje – **Siųsti ir publikuoti**). Generuojamas kiekvieno tiekėjo, kuriam siunčiate RFQ, RFQ žurnalas. Galite konfigūruoti siuntimo veiksmo spausdinimo parinktis, kad kiekvieno tiekėjo ataskaita būtų spausdinama arba siunčiama kiekvieno tiekėjo el. pašto adresu. Be to, naudojant kiekvieno tiekėjo RFQ žurnalą galima generuoti ataskaitą, kurią galima siųsti arba pakartotinai siųsti tiekėjui vėliau. Taip pat galite konfigūruoti siuntimo veiksmą, kad būtų sugeneruotas atsakymo lapas, kurį tiekėjas gali užpildyti.

Šiame straipsnyje aprašomas RFQ tvarkymo procesas, kai tiekėjobendradarbiavimo programa nenaudota. Jei jūsų sistemoje nustatytas tiekėjų bendradarbiavimas, tiekėjai gali įvesti kainos siūlymus tiesiai į „Supply Chain Management”. Daugiau informacijos apie tiekėjo bendradarbiavimą žr. puslapiuose [Tiekėjo bendradarbiavimas su klientais](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) ir [Tiekėjo bendradarbiavimas su išoriniais tiekėjais](vendor-collaboration-work-external-vendors.md).

Jei reikia pakeisti išsiųstą RFQ, baigę galite pakartotinai išsiųsti RFQ tiekėjams naudodami du keitimo veiksmus: kurti ir baigti.

Gavę pasiūlymų el. paštu, šiuos pasiūlymus galite tvarkyti puslapyje **Pasiūlymų patvirtinimai**.

Jei reikalingas tiekėjo antras atsakymo pakartojimas, puslapyje **Pasiūlymo patvirtinimas** pasirinkite **Grąžinti**. Grąžinimo veiksmas sugeneruoja naują žurnalą ir ataskaitą, kuri bus išspausdinta, archyvuota ir išsiųsta pagal jūsų spausdinimo parametrus.

Jei į RFQ atvejį įtraukiate vertinimo kriterijų, RFQ turės vertinimo sritį, kurioje galima įvesti rezultatus. Bendras rezultatas bus rodomas RFQ ir kai palyginsite atsakymus puslapyje **Palyginti atsakymus**. Puslapyje **Atsakymų palyginimas** taip pat galima palyginti kitus atsakymų duomenis, pvz., eilutės kainą, pristatymo datą ir bendrąją kainą.

Pasirinkę kainos pasiūlymą arba kainos pasiūlymo eilučių skaičių, galite priimti visas arba kai kurias eilutes ir atmesti kitas. Generuojami priėmimo žurnalai, atmetimo žurnalai ir atitinkamos ataskaitos ir jie bus išspausdinti, archyvuoti bei išsiųsti pagal jūsų spausdinimo parametrus. Priėmus kainos pasiūlymą arba konkrečias kainos pasiūlymo eilutes sugeneruojama pirkimo sutartis arba pirkimo užsakymas arba atnaujinama pirkimo paraiška, atsižvelgiant į RFQ pirkimo tipą. Galite sukurti prekybos sutartį, kurią vėliau galėsite naudoti bet kuriuose atsakymuose, nepaisant to, ar juos priėmėte, ar atmetėte.

RFQ atvejo būsenos tipai gali būti du: žemiausia ir aukščiausia. Būseną galite peržiūrėti sąrašo puslapyje **Visi pasiūlymų patvirtinimai**. Mažiausia būsena yra mažiausiai pažengęs etapas iš visų RFQ atvejo eilučių, o didžiausia būsena yra labiausiai pažengęs etapas iš visų RFQ atvejo eilučių. Pavyzdžiui, tarkime, kad yra RFQ atvejis, kuriame yra trys eilutės, siunčiamas dviem tiekėjams, todėl sukuriami du RFQ, o kiekviename iš jų yra trys eilutės. Visų eilučių būsena yra **Išsiųsta**. Dabar pasiūlymas įvedamas iš vieno iš tiekėjų ir RFQ eilučių būsena tampa **Gauta**. Tai reiškia, kad iš trijų RFQ atvejo eilučių visų vieno RFQ eilučių būsena yra **Išsiųsta**, o visų kito RFQ eilučių būsena yra **Gauta**. Tada žemiausia būsena yra **Išsiųsta**, o aukščiausia yra **Gauta.**

Šios būsenos bus išsamiau aprašytos toliau šiame straipsnyje.

## <a name="setting-up-rfq-functionality"></a>RFQ funkcijų nustatymas

Prieš kurdami RFQ atvejį, turite nustatyti RFQ informaciją puslapyje **Paraiškų parametrai**. Kai kuriate yra RFQ atvejį, galite nurodyti numatytąsias vertes, kurios yra kopijuojamos į RFQ. Galite nurodyti šias numatytąsias vertes:

- Naujų RFQ pirkimo tipas: **Pirkimo užsakymas** arba **Pirkimo sutartis**
- Galiojimo data ir dienos, kurią RFQ atvejis sukurtas, kompensuotas laikas.
- Siūlymo tipas, kuris gali nustatyti numatytąjį RFQ atvejo vertinimo būdą.
- Pristatymo informacija ir mokėjimo sąlygos.

Galite nepaisyti šių verčių konkrečiame RFQ atvejyje.

Taip pat turite sukonfigūruoti pakeitimo procesą. Kaip šios konfigūracijos dalį galite įjungti lauko blokavimo funkciją. Kai įjungta lauko blokavimo funkcija, įsigijimo specialistas, kuris nori pakeisti RFQ, pirma turi pasirinkti mygtuką **Kurti**, esantį RFQ atvejo skirtuko **Pasiūlymas** dalyje **Pakeitimas**. Tada, atnaujinus RFQ pakeitimu, įsigijimo specialistas turi užbaigti procesą pasirinkdamas **Baigti**. Atlikus veiksmą Baigti sugeneruojamas el. laiškas, kuriuo tiekėjams pranešama apie pakeistą RFQ.

Pasirinkite tiekėjui siunčiamo el. pašto pranešimo šabloną puslapyje **Paraiškų parametrai**. Kai puslapyje **El. laiškų šablonai** sukuriamas šablonas, jame gali būti toliau nurodytų pakeitimo atpažinimo ženklų.

- %RFQ atvejis%
- %Kainos pasiūlymo grąžinimo priežastis%
- %Pakeitimo priežastis%
- %Pakeitimą parengė%
- „%Company%“
- %RFQ atvejo pavadinimas%
- %Galiojimo pabaigos data ir laikas%
- „%Date%“

Atpažinimo ženklus %Kainos pasiūlymo grąžinimo priežastis% ir %Pakeitimo priežastis% įsigijimo specialistas pakeičia tekstu, kurį gali įvesti užbaigęs šiuos pakeitimus vedlyje **Pakeitimas**. Atpažinimo ženklų %Amendment prepared by% ir %Company% vertės automatiškai paimamos iš RFQ. Atpažinimo ženklas %Date% pakeičiamas esama data.

Jei norite atšaukti RFQ po to, kai jis buvo išsiųstas, tai galite atlikti iš RFQ atvejo. Norint atšaukti, atšaukimo pranešimui nusiųsti tiekėjo kontaktiniams asmenims turi būti naudojamas el. laiško šablonas. Šabloną reikia pasirinkti puslapyje **Paraiškų parametrai**. Kai sukuriamas šablonas, jame gali būti toliau nurodytų pakeitimo atpažinimo ženklų.

- %Nutraukimo priežastis%
- %RFQ atvejis%
- %RFQ nutraukta%
- „%Company%“
- %RFQ atvejo pavadinimas%
- „%Date%“

Atpažinimo ženklas %Reason for cancellation% pakeičiamas tekstu, kurį įsigijimo specialistas gali įvesti vedlyje **Atšaukimas**. Atpažinimo ženklas %Date% pakeičiamas esama data.

Jei kainos pasiūlyme siekdami nurodyti, kodėl jis buvo atmestas ar priimtas, norite naudoti priežasčių kodus, turite nustatyti priežasčių kodus puslapyje **Tiekėjų priežastys**.

Galite konfigūruoti išspausdintų arba saugomų RFQ dokumentų išvaizdą dalies paraiškų puslapyje **Formos nustatymas**.

> [!NOTE]
> Jei naudojama viešojo sektoriaus konfigūracija, norint atlikti jau išsiųsto RFQ keitimus reikia naudoti pakeitimo procesą. Išsiuntus RFQ laukai užrakinami.
Todėl, norint atlikti RFQ keitimus, reikia pasirinkti **Kurti** ir pradėti keitimo procesą, kaip aprašyta pirmiau. Tai valdo lauko blokavimo parinktis **Užrakinti išsiųstus RFQ**, esanti puslapyje **Paraiškų parametrai**. Pagal numatytuosius parametrus šis parametras nustatytas į parinktį **Taip** ir naudojant viešojo sektoriaus konfigūraciją tai yra numatytoji reikšmė, kurios negalima keisti. Todėl, nors pakeitimo procesą galima tvarkyti neautomatiniu būdu viešojo sektoriaus konfigūracijoje, jį reikia naudoti viešojo sektoriaus konfigūracijoje.

Kai sukuriate tipo Pirkimo užsakymas RFQ atvejį ir prie RFQ pridedate atsargų prekę, sugeneruojama atsargų operacija, kurios gavimo būsena yra **Pasiūlymo gavimas**. Kai naudojate bendrąjį planą apskaičiuodami atsargas, atsižvelgiama tik į šios būsenos RFQ atvejo eilutes. Jei norite, kad į bendrąjį planą kaip numatomas gavimas būtų įtrauktos RFQ atvejo eilutės, turite sukonfigūruoti šią veikseną bendrojo planavimo nustatyme.

Pirkimo vadovas arba agentas gali kurti ir tvarkyti siūlymų tipus, kad atitiktų jūsų organizacijos įsigijimo poreikius. Kiekvieno siūlymo tipą galima susieti su vertinimo būdu. Vertinimo metodus sudaro tam tikri kriterijai, kuriuos galima naudoti vertinant kainos pasiūlymus. Siūlymų tipus, vertinimo būdus ir vertinimo kriterijus turite nustatyti puslapiuose **Siūlymo tipas** ir **Vertinimo būdas**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Pasirinkti numatytuosius laukus, įtraukiamus į tiekėjo RFQ atsakymo formas

Galite nurodyti tam tikrus tipus informacijos, kurią norite gauti iš tiekėjų, kai jie atsakys (siūlys kainą) į pasiūlymo patvirtinimą (RFQ). Laukai, kurie pažymėti kaip numatytieji, yra įtraukti į elektroninę formą, skirtą bendradarbiavimui su tiekėju. Norėdami konfigūruoti parametrus:

1. Jei to dar nepadarėte, naudokite [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį, kad suaktyvintumėte funkciją *Pasirinkti RFQ laukus, įtraukiamus į tiekėjo RFQ atsakymo formas*.
1. Eikite į **Įsigijimas ir šaltinio pasirinkimas > Sąranka > Įsigijimo ir šaltino pasirinkimo parametrai**.
1. Atidarykite skirtuką **Pasiūlymo patvirtinimas**.
1. Pasirinkite **Numatytieji pasiūlymo patvirtinimai** atsakymo laukų nuorodą po antrašte **Nustatyti numatytąsias pasiūlymų patvirtinimo vertes**.
1. Atidaromas dialogo langas **Numatytieji pasiūlymo patvirtinimo atsakymo laukai**.
1. Srityje **RFQ laukai, įtraukti į tiekėjo RFQ atsakymo formas** kiekvienas laukas, kurį galima naudoti RFQ atsakymo formose, turi slankiklį. Šis srities laukai, kurių reikšmė yra *Taip*, bus įtraukti (kartu su jų vertėmis) į RFQ atsakymo formas. Kiekvienam laukui, kurio duomenų tiekėjai neturi matyti peržiūrėdami pasiūlymus, slankikliu nustatykite reikšmę *Ne*. Tai leidžia vidiniams tikslams įvesti apytiksles arba prognozuojamas vertes RFQ įvedimo metu taip, kad tiekėjas nematytų įvestų duomenų.

Jei reikia, atskirais RFQ atvejais šiuos parametrus galite pakeisti.

## <a name="creating-and-sending-an-rfq"></a>RFQ kūrimas ir siuntimas

Sukuriate RFQ atvejį, pasirenkate tiekėjus, kurių kainų pasiūlymus norite gauti į RFQ atvejį, ir išsiunčiate RFQ tiekėjams. Spausdinimo parametrus galite naudoti, kad nukreiptumėte RFQ ataskaitas ir atsakymų lapų ataskaitas į pasirinktą vietą.

Galite neautomatiniu būdu kurti pirkimo tipo **Pirkimo užsakymas** arba **Pirkimo sutartis** RFQ atvejį.

Jei RFQ atvejo tipas yra **Pirkimo užsakymas** tipas, vykdomi toliau nurodyti veiksmai, kurie skiriasi nuo kitų tipų RFQ atvejų veiksmų.

- Kuriant RFQ atvejo eilutes generuojamos atsargų operacijos, kurių gavimo būsena yra **Pasiūlymo gavimas**.
- Priėmus kainos pasiūlymą generuojamas pirkimo užsakymas.

Jei RFQ tipas yra **Pirkimo sutartis** tipas, vykdomi toliau nurodyti veiksmai, kurie skiriasi nuo kitų RFQ atvejų veiksmų.

- RFQ atvejis naudojamas kaip sutartis tam tikram produkto kiekiui arba vertei pirkti per tam tikrą laikotarpį. Turite pasirinkti datų intervalą, kuris bus taikomas pirkimo sutarčiai, ir asmens, kuris valdo pirkimo sutartį, vardą.
- Priėmus kainos pasiūlymą generuojama pirkimo sutartis.

Jei RFQ atvejis generuojamas iš pirkimo paraiškos, automatiškai priskiriamas tipas **Pirkimo paraiška**. Negalima neautomatiniu būdu sukurti tipo **Pirkimo paraiška** RFQ atvejo.

RFQ atvejį iš pirkimo paraiškos galite sukurti tik jei pirkimo paraiškos būsena yra **Peržiūrima** ir jūs esate priskirti atlikti kitą darbo eigos užduotį. Pirkimo paraiškos eilutės naujinamos automatiškai, kai priimate eilutes iš kainos pasiūlymų (RFQ atsakymų), kuriuos gavote iš tiekėjų. Negalima baigti, atmesti, patvirtinti arba atlikti jokių kitų veiksmų su pirkimo paraiška, kol paraiškos eilutė neatnaujinta įvedant priimtą RFQ eilutę arba kol RFQ atvejis neatšauktas.

Kai kuriate RFQ atvejį, galite pasirinkti siūlymo tipą. Pagal siūlymo tipą nustatomas vertinimo kriterijų rinkinys, naudojamas RFQ atsakymams RFQ atvejyje vertinti.

Prie RFQ atvejo galite pridėti klausimyną. Šis klausimynas rodomas visuose RFQ atsakymuose išsiuntus RFQ. Klausimyno baigimas yra privaloma užduotis norint pateikti kainos pasiūlymą.

Nors numatytosios vertės yra pateiktos, esant poreikiui kiekvienam atskiram RFQ atvejui galite pakeisti **RFQ laukai, įtraukti į tiekėjo RFQ atsakymo formas** parametrus. Norėdami tai atlikti, sukurkite arba atidarykite RFQ atvejį. Tada veiksmų srityje atidarykite skirtuką **Pasiūlymas** ir srityje **Atsakymai** pasirinkite **Nustatyti RFQ atsakymo numatytąsias vertes**. Atidaromas dialogo langas **Numatytieji pasiūlymo patvirtinimo atsakymo laukai**, kurio funkcija yra tokia pati kaip ir tiekėjo RFQ atsakymo formų numatytųjų verčių nustatymo, išskyrus tai, kad jūsų pakeitimai bus taikomi tik dabartiniam RFQ atvejui. Norėdami gauti daugiau informacijos apie tai, kaip įjungti šią funkciją ir kaip ji veikia, žr. [Pasirinkti numatytuosius laukus, įtraukiamus į tiekėjo RFQ atsakymo formas](#default-reply-fields).

Pasirinkti tiekėjus, įtrauktinus į RFQ atvejį, galima trimis būdais:

- Įtraukti tiekėjus po vieną.
- Ieškoti visų tiekėjų, atitinkančių nurodytus kriterijus.
- Automatiškai įtraukti visus tiekėjus, patvirtintus pagal įsigijimo kategorijas, naudojamas RFQ atvejo eilutėse.

Kai RFQ atvejis bus paruoštas, pasirinkite **Siųsti**. Siuntimo veiksmas sugeneruoja žurnalus ir ataskaitas, kurie bus išspausdinti, archyvuoti ir išsiųsti pagal jūsų spausdinimo parametrus.

Jei išsiųsdami RFQ tiekėjui puslapyje **Pasiūlymo patvirtinimo siuntimas** nustatėte parinktis **Naudoti tiekėją perskaičiuojant kainas** ir **Naudoti prekių informaciją pagal tiekėją** į **Taip**, tam tikra konkretaus tiekėjo informacija įvedama automatiškai to tiekėjo RFQ.

## <a name="amending-an-rfq-case"></a>RFQ atvejo keitimas

Kartais turite pakeisti išsiųstą RFQ atvejį. RFQ atvejį gali reikėti pakeisti, pavyzdžiui, jei pasikeitė pristatymo datos, norite papildomų produktų arba kitokio produktų kiekio. Galite konfigūruoti pakeitimo procesą, kad jis būtų labiau arba mažiau ribojamas.

Jei sukonfigūruojate mažiau ribojamą pakeitimo procesą, prieš keisdami jau išsiųsto RFQ atvejo laukus RFQ atvejyje turite pasirinkti **Kurti**, kad pradėtumėte keitimą. Atlikę keitimus turite pasirinkti **Baigti**. Jums bus pateikiami nurodymai, kaip įtraukti informaciją į el. laišką, siunčiamą norint perspėti tiekėjus apie pakeitimą. Atnaujinta RFQ ataskaita, kurioje yra pastaba apie pakeitimą, automatiškai pridedama prie el. laiško.

Jei sukonfigūruosite mažiau ribojamą pakeitimo procesą, neturite pasirinkti **Kurti** prieš keisdami jau išsiųsto RFQ atvejo laukus. Tačiau turite patys į RFQ atvejį įtraukti pakeitimo pastabą ir pakartotinai išsiųsti atvejį. Turėkite omenyje, kad šį metodą galima naudoti tik jei nė vienas atsakymas (kainos siūlymas) nebuvo redaguotas. Jei įvedėte atsakymą ir jo būsena yra **Gauta**, mygtuko **Siųsti** naudoti negalima. Tokiu atveju turite pasirinkti **Kurti** ir **Baigti**, kaip turite daryti vykdydami labiau apribotą procesą. Tada atsakymas nustatomas iš naujo, kad atspindėtų RFQ atvejo keitimus.

Jei tiekėjai naudoja tiekėjo bendradarbiavimo sąsają pasiūlymams įvesti, visada turite naudoti pakeitimo procesą, kad praneštumėte tiekėjams apie RFQ atvejo keitimus. Šis procesas padeda išvengti atvejų, kai tiekėjai teikia kainos siūlymus naudodami pasenusį RFQ atvejį, kol jų kainos siūlymas vis dar tvarkomas. Daugiau informacijos apie tiekėjo bendradarbiavimą žr. puslapyje [Tiekėjo bendradarbiavimas su išoriniais tiekėjais](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Jei norite pakviesti papildomus tiekėjus siūlyti kainą ir nebuvo atlikta jokių RFQ atvejo keitimų, galite naudoti mygtuką **Siųsti**. Įtraukti tiekėjai bus rodomi puslapyje **Siųsti** ir gaus kvietimą el. paštu.

## <a name="receiving-and-registering-rfq-replies"></a>RFQ atsakymų gavimas ir registravimas

Siunčiant RFQ atsakymo lapas bus sugeneruotas automatiškai. Kai gaunate RFQ pasiūlymų, juos turite įvesti puslapyje **Pasiūlymo patvirtinimas** spustelėdami veiksmą **Redaguoti RFQ atsakymą.** Tai suteikia galimybę įvesti kainos pasiūlymo informaciją tam skirtoje kainos pasiūlymo formoje. Iš pradžių **Atsakymo eiga** bus **Nepradėta**. Kai spustelėsite **Redaguoti RFQ atsakymą**, eigos būsena bus **Atnaujina pirkėjas**, kol kainos pasiūlymas bus pateiktas. Spustelėkite **Pateikti**, kai įvesite kainos pasiūlymo informaciją. Atsakymo eigos būsena pasikeis į **Pateikė pirkėjas.** Panašiai, kai įjungtas tiekėjo bendradarbiavimas, **Atsakymo eiga** bus atnaujinta tiekėjui atliekant veiksmus su kainos pasiūlymu. Tada būsena pasikeičia iš **Atnaujina tiekėjas** į **Pateikė tiekėjas**. Pateikus kainos pasiūlymą, sukuriamas žurnalas, kurio būsena **Gautas**. Atsakymas (kainos pasiūlymas) turi būti pateiktas norint užregistruoti jį kaip gautą, tik tada jis gali būti toliau apdorojamas kaip priimtas ar atmestas.

Jei reikia atnaujinti kainos pasiūlymą, turėtumėte vykdyti pirmiau aprašytą procesą ir pateikti jį dar kartą.

Atkreipkite dėmesį, kad formoje **Pasiūlymo patvirtinimas** galima redaguoti tik informaciją, kuri susijusi su kainos pasiūlymo apdorojimu, o ne su kainos pasiūlymo įvedimu. Norėdami įvesti arba modifikuoti kainos pasiūlymą, spustelėkite **Redaguoti RFQ atsakymą.**

Kai įvedate kainos pasiūlymo informaciją, jei RFQ atvejyje galimos alternatyvios eilutės, galite įtraukti eilučių, kurioms priskirta tik įsigijimo kategorija ir kuriose nenurodyta katalogo prekė, alternatyvių eilučių. Spustelėkite **Įtraukti pakaitą**, kad įtrauktumėte alternatyvių eilučių.

Jeigu įvedėte atsakymą, bet jums reikalingas naujas tiekėjo pasiūlymas, galite RFQ grąžinti. Sugeneruojami nauji žurnalas ir ataskaita, kuriuos galima siųsti tiekėjui.

Puslapyje **Pasiūlymo patvirtinimo stebėjimas** galite matyti visų RFQ ir jų būsenų apžvalgą: **Išsiųstas, Gautas, Priimtas, Atmestas, Atšauktas, Nepriimtas**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Kainos pasiūlymų priėmimas ir atmetimas bei priimtų kainos pasiūlymų perkėlimas į tolesnius dokumentus

Radę geriausią kainos pasiūlymą, pvz., pasiūlymą su geriausia bendrąja kaina, jį priimkite. Galite priimti kai kurias kainos pasiūlymo eilutes ir atmesti kitas.
Taip pat galite priimti eilutes iš įvairių tiekėjų. Turėkite omenyje, kad, jei priimate kai kurias eilutes, būsite paraginti atmesti visas kitas. Todėl, jei norite priimti kitų eilučių, gavę raginimą turite pasirinkti **Atšaukti**. Kiekvieno tiekėjo, kurio kainos siūlymą arba eilutes priimate, RFQ atsakymo būsena atnaujinama į **Priimta**.

Jei ruošiant pirkimo užsakymą arba pirkimo sutartį į RFQ reikia įtraukti papildomą eilutę, galite tai padaryti puslapio **Pasiūlymo patvirtinimas** eilučių tinklelyje spustelėdami **Įtraukti eilutę**. Šią eilutę galite peržiūrėti ir redaguoti tik puslapyje **Pasiūlymo patvirtinimas**. Kai ji bus priimta, ji bus rodoma kainos pasiūlymo puslapyje.

Kai priimate kainos pasiūlymą arba vieną ar kelias kainos siūlymo eilutes, automatiškai sugeneruojamas pirkimo užsakymas arba pirkimo sutartis. Tada galite atmesti kitų tiekėjų kainos siūlymus.

Atsakyme galite įtraukti priežasties kodą, norėdami paaiškinti, kodėl priimtas arba atmestas kainos pasiūlymas.

Kai priimate tipo **Pirkimo paraiška** kainos pasiūlymą, pirkimo paraiškos eilutės bus atnaujintos įvedant toliau nurodytą informaciją, kuri atspindi priimto kainos pasiūlymo informaciją.

- Vnt. kaina
- Nuolaida procentais
- Nuolaidos suma
- Pirkimo išlaidos
- Eilutės išlaidos
- Tiekėjas
- Išorinis skaičius
- Išorinis aprašymas

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena, kai priimate ir atmetate tiekėjų kainos pasiūlymus.

## <a name="statuses--highest-and-lowest"></a>Būsenos – aukščiausia ir žemiausia

RFQ atvejo skirtuke Tiekėjas galite matyti konkretaus tiekėjo eilutes, kurių būsena aukščiausia ir žemiausia. Kai tiekėjas įtraukas, bet dar nėra išsiųstų eilučių, tiek žemiausia, tiek aukščiausia būsena yra <strong>Sukurta.</strong> Kai RFQ yra išsiųstas tiekėjui su visomis eilutėmis, dviejų eilučių būsena bus <strong>Išsiųsta</strong>. Jei kai kurios tiekėjo kainos pasiūlymo eilutės priimamos, o kitos – atmetamos, atmestų eilučių būsena bus žemiausia – <strong>Atmesta</strong>, o priimtų eilučių būsena bus aukščiausia – <strong>Priimta</strong>.

RFQ atvejo eilutėse galite matyti kiekvienos visų tiekėjų eilutės aukščiausią ir žemiausią būsenas. Jei išsiuntėte eilutę visiems RFQ atvejo tiekėjams ir nė vienas dar neatsakė, žemiausia ir aukščiausia būsena yra **Išsiųsta.** Kai bent vienas tiekėjas atsako, aukščiausia būsena pasikeis į **Gauta**. Jei į atvejį įtrauksite naują tiekėją, žemiausia būsena pasikeis į **Sukurta**

Aukščiausia ir žemiausia RFQ atvejo būsenos yra sutelktos skirtuko \<Tiekėjas ir skirtuko Eilutės būsenos.

Būsenos rikiuojamos tokiu būdu nuo žemiausios iki aukščiausios: Sukurtas, Išsiųstas, Gautas, Atmestas, Priimtas, Nepriimtas, Atšauktas.

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ atvejo būsena, kai sukuriate RFQ atvejį su eilutėmis ir siunčiate jį tiekėjams.

| **Veiksmas**                                | **Žemiausia RFQ atvejo būsena** | **Aukščiausia RFQ atvejo būsena** | **Žemiausia RFQ atvejo eilutės būsena** | **Aukščiausia RFQ atvejo eilutės būsena** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Sukurkite RFQ atvejo antraštę ir eilutę.      | Sukurta                    | Sukurta                     | Sukurta                         | Sukurta                          |
| Išsiųskite RFQ visiems RFQ atvejo tiekėjams. | Išsiųstas                       | Išsiųstas                        | Išsiųstas                            | Išsiųstas                             |
| Pridėti kitą tiekėją.                       | Sukurta                    | Išsiųstas                        | Sukurta                         | Išsiųstas                             |
| Išsiųsti RFQ antram tiekėjui.        | Išsiųstas                       | Išsiųstas                        | Išsiųstas                            | Išsiųstas                             |

Visų RFQ eilučių, kurios yra susijusios su RFQ atveju, būsena bus **Išsiųsta**.

Toliau pateikiamoje lentelėje parodoma, kaip keičiasi RFQ būsena gaunant kainų pasiūlymus ir registruojant informaciją RFQ atsakymo lape.

| **Veiksmas**                                               | **Žemiausia būsena visose visų RFQ eilutėse** | **Aukščiausia būsena visose visų RFQ eilutėse** | **Žemiausia RFQ atvejo antraštės būsena** | **Aukščiausia RFQ atvejo antraštės būsena** | **Žemiausia RFQ atvejo eilutės būsena** | **Aukščiausia RFQ atvejo eilutės būsena** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| RFQ užregistruokite vieno tiekėjo kainos siūlymą ir jį išsaugokite.        | Išsiųstas                                           | Gauta                                        | Išsiųstas                              | Gauta                           | Išsiųstas                            | Gauta                         |
| RFQ užregistruokite antro tiekėjo kainos pasiūlymą ir jį išsaugokite. | Gauta                                       | Gauta                                        | Gauta                          | Gauta                           | Gauta                        | Gauta                         |


Tolesniame pavyzdyje galite matyti RFQ atvejo aukščiausią ir žemiausią būsenas, kai vienas kainos pasiūlymas buvo gautas, o kitas kainos pasiūlymas buvo priimtas. Kai gautas kainos pasiūlymas atmetamas, RFQ atvejo antraštėje ir eilutėje žemiausia būsena pasikeičia iš gautos į atmestą.


|            <strong>Veiksmas</strong>             | <strong>Žemiausia būsena visose visų RFQ eilutėse</strong> | <strong>Aukščiausia būsena visose visų RFQ eilutėse</strong> | <strong>Žemiausia RFQ atvejo antraštės būsena</strong> | <strong>Aukščiausia RFQ atvejo antraštės būsena</strong> | <strong>Žemiausia RFQ atvejo eilutės būsena</strong> | <strong>Aukščiausia RFQ atvejo eilutės būsena</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Priimti vieną pasiūlymų. (arba bent vieną eilutę) |                          Gauta                           |                           Priimta                           |                    Gauta                    |                    Priimta                     |                   Gauta                   |                   Priimta                    |
|           Atmeskite visus kitus kainos siūlymus.           |                          Atmestas                           |                           Priimta                           |                    Atmestas                    |                    Priimta                     |                   Atmestas                   |                   Priimta                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]