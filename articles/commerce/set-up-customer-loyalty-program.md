---
title: Lojalumo apžvalga
description: Šioje temoje aprašomos lojalumo galimybės programoje „Dynamics 365 Commerce“ ir atitinkami nustatymo veiksmai, padedantys mažmenininkui lengvai pradėti dirbti su savo lojalumo programomis.
author: scott-tucker
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 337ede63cb9175f2674bae8f2caaac5f1ba5f5cb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023455"
---
# <a name="loyalty-overview"></a>Lojalumo apžvalga

[!include [banner](includes/banner.md)]

Lojalumo programos gali padėti padidinti klientų lojalumą atlyginant klientams už veiksmus su mažmenininko ženklu. Naudodami „Dynamics 365 Commerce“, galite nustatyti paprastas arba sudėtingas lojalumo programas, taikomas visiems jūsų juridiniams subjektams visuose prekybos kanaluose. Šioje temoje aprašomos lojalumo galimybės programoje „Commerce“ ir atitinkami sąrankos veiksmai, padedantys mažmenininkui lengvai pradėti dirbti su savo lojalumo programomis.

Galite nustatyti savo lojalumo programą, kad į ją būtų įtrauktos nurodytos parinktys.

- Nustatykite kelis lojalumo programose siūlomų atlygių tipus ir sekite dalyvavimą jūsų lojalumo programose.
- Nustatykite lojalumo programas skirtingiems siūlomiems skatinamiesiems atlygiams nurodyti. Galite įtraukti lojalumo programos pakopas, norėdami pasiūlyti didesnes paskatas klientams, kurie jūsų parduotuvėse dažniau perka ar daugiau išleidžia.
- Nustatykite uždarbio taisykles, norėdami identifikuoti veiklas, kurias klientai turi įvykdyti, kad užsidirbtų atlygį. Taip pat galite nurodyti apmokėjimo taisykles, norėdami nustatyti, kada ir kaip klientas gali išnaudoti atlygius.
- Išduokite lojalumo korteles iš bet kurio kanalo, dalyvaujančio jūsų lojalumo programose, ir susiekite lojalumo korteles su viena ar daugiau lojalumo programų, kuriose klientas gali dalyvauti. Be to, kliento įrašą galite susieti su lojalumo kortele, kad klientas galėtų kaupti lojalumo taškus iš kelių kortelių ir juos panaudoti.
- Neautomatiniu būdu koreguokite lojalumo korteles arba perkelkite lojalumo atlygio balansą iš vienos kortelės į kitą, norėdami patenkinti kliento prašymą ar klientą apdovanoti.

## <a name="setting-up-loyalty-programs"></a>Lojalumo programų nustatymas

Turite nustatyti kelis komponentus, kad įgalintumėte „Commerce“ lojalumo funkciją. Toliau pateiktoje diagramoje parodyti lojalumo komponentai ir kaip jie susiję tarpusavyje.

![Lojalumo nustatymo proceso srautas](./media/loyaltyprocess.gif "Lojalumo komponentai ir kaip jie susiję tarpusavyje")

## <a name="loyalty-components"></a>Lojalumo komponentai

Toliau pateikiamoje lentelėje aprašomas kiekvienas komponentas ir kur jis naudojamas lojalumo nustatyme.

| Komponentas                                        | aprašymas | Kur jis naudojamas |
|--------------------------------------------------|-------------|-----------------|
| Nustatykite nuolaidas (būtina)                  | Nustatyti nuolaidas, kurias norite pasiūlyti savo lojaliems klientams. Pvz., galite pasiūlyti 5 proc. nuolaidą visiems drabužiams. | Nuolaidos turi būti įtrauktos į kainų grupes prieš jas įtraukiant į lojalumo programą. Kainų grupės priskirtos lojalumo programoms ir lojalumo pakopoms. |
| Nustatykite kainų grupes (prerequisite)               | Kainų grupės naudojamos kurti ir valdyti produktų kainas ir nuolaidas. Nustatykite kainų grupes, į kurias būtų įtrauktos nuolaidos, galiojančios jūsų lojalumo programoms. | Kainų grupės priskiriamos lojalumo programoms ir lojalumo programų pakopoms. |
| Nustatykite kanalus (būtina)                   | Prekybos kanalai yra parduotuvės, dalyvaujančios jūsų lojalumo programose, pvz., plytų ir skiedinio parduotuvė, interneto parduotuvė arba skambučių centras. Turite nustatyti savo kanalus prieš jiems priskirdami lojalumo programas. | Galite priskirti kanalus lojalumo programai, jei kanalas dalyvauja lojalumo programoje. |
| Lojalumo mokesčio metodo nustatymas (būtina) | Turite nustatyti lojalumo mokėjimo metodą, kad būtų galima lojalumo kortelę naudoti kasoje, ir išnaudoti lojalumo taškus dalyvaujant lojalumo programoje. Taip pat turite prie kanalo pridėti lojalumo mokėjimo būdą, kad klientai galėtų išnaudoti lojalumo taškus mokėdami už prekes. | Nustatykite lojalumo tipo mokėjimo būdą ir tuomet priskirkite lojalumo mokėjimo būdą kanalams, dalyvaujantiems lojalumo programoje. |
| Nustatykite datų intervalus                            | Datų intervalai leidžia lanksčiai nustatyti laiko tarpą, taikomą lojalumo pakopoms. Norėdami nurodyti, kiek laiko klientas gali likti pakopoje arba kiek laiko klientas turi veiklai, leidžiančiai gauti pakopą, atlikti, naudokite datų intervalus. | Datų intervalai taikomi, tik jei naudojate pakopas savo lojalumo programose. Pasirinkite datų intervalą, taikomą programos pakopoms ir datų intervalus, taikomus programos pakopos taisyklėms. |
| Nustatykite atlygio taškus                             | Atlygio taškų tipai yra tipai atlygio, kurį siūlote savo klientams. Atlygio taškai gali būti išnaudojami arba neišnaudojami. Išnaudojami atlygio taškai gali būti iškeisti į prekes. Neišnaudojami atlygio taškai naudojami stebėjimui arba tam, kad klientas galėtų pereiti į kitą lojalumo programos pakopą. | Atlygio taškai nurodomi pakopos taisyklėse ir yra naudojami norint perkelti klientą į konkrečią pakopą. Atlygio taškai taip pat nurodomi lojalumo planuose, uždarbio ir naudojimo taisyklėse. Uždarbio taisyklėse nurodote atlygius, kuriuos klientas gali uždirbti už konkrečią veiklą. Apmokėjimo taisyklėse nurodote atlygį, kurį klientas gali panaudoti. |
| Nustatykite lojalumo programas                          | Lojalumo programos yra pagrindinis lojalumo objektas, kurį galite pasiūlyti. Kiekvienai lojalumo programai taip pat galima priskirti lojalumo pakopas. Nuolaidos ir kainų grupės priskiriamos lojalumo programoms programos arba pakopos lygmenyje. | Jūs kuriate savo lojalumo programų lojalumo planus. Priskiriate lojalumo korteles lojalumo programoms ir lojalumo kortelės gali būti priskirtos klientui. Kanalai dalyvauja lojalumo programose, kurios priskirtos lojalumo planams. Bet kuris lojalumo kortelę turintis klientas gali dalyvauti kortelei priskirtose lojalumo programose. |
| Nustatykite lojalumo pakopas ir pakopų taisykles              | Lojalumo pakopos yra pasirinktiniai lygiai, kuriuos galite apibrėžti savo lojalumo programoms. Galite nustatyti pagrindines nuolaidas ir atlygius visiems klientams, kurie dalyvauja lojalumo programoje ir galite nustatyti papildomas nuolaidas ir atlygius klientams, kurie gauna skirtingus lygius programoje. Galite kiekvienai nurodytai lojalumo pakopai nustatyti taisykles, pagal kurias klientas priskiriamas tai pakopai. Taip pat galite nurodyti, kiek laiko klientai gali likti toje pakopoje po to, kai ją pasiekė. | Lojalumo pakopos ir lojalumo pakopos taisyklės nustatomos lojalumo programose. Jei nenustatote jokių lojalumo pakopų, visi lojalumo programoje dalyvaujantys klientai gaus nuolaidas, kurias priskirsite lojalumo programos kainų grupėje. Jei nustatote lojalumo kategorijas, galite nustatyti lojalumo plano lojalumo kategorijų uždarbio taisykles ir naudojimo taisykles. |
| Lojalumo planų nustatymas                           | Lojalumo planuose nustatote uždarbio taisykles ir naudojimo taisykles, galiojančias pasirinktai lojalumo programai. Kanalus priskiriate lojalumo planui, kad nurodytumėte, kuri lojalumo programa, uždarbio taisyklės ir naudojimo taisyklės taikomos parduotuvei. | Lojalumo planas priskiriamas lojalumo programai ir kanalams. Tai pačiai lojalumo programai galite pritaikyti daug lojalumo planų ir galite pritaikyti daug lojalumo planų dideliam kiekiui kanalų. |
| Lojalumo kortelių nustatymas                             | Lojalumo kortelė leidžia kortelės turėtojui dalyvauti lojalumo programose, kurios priskirtos kortelei. Lojalumo kortelės gali būti išduotos anonimiškai arba gali būti priskirtos konkrečiam klientui. Galite peržiūrėti konkrečios kortelės lojalumo operacijas ir peržiūrėti kortelėje sukauptų lojalumo taškų suvestinę. Galite išduoti lojalumo korteles bet kuriame kanale. Galite rankiniu būdu koreguoti lojalumo kortelę, norėdami perkelti klientą į kitą pakopą, pridėti lojalumo taškų arba perkelti lojalumo taškų balansą iš vienos kortelės į kitą. | Jūs lojalumo kortelei priskiriate lojalumo programas. |

## <a name="loyalty-processes"></a>Lojalumo procesai

Toliau pateikiamoje lentelėje aprašomi procesai, kuriuos reikia vykdyti, norint lojalumo konfigūracijas ir duomenis siųsti savo parduotuvėms ir iš jų gauti lojalumo operacijas.

| Proceso pavadinimas                         | Prekės/Paslaugos pavadinimas | Puslapio pavadinimas |
|--------------------------------------|-------------|-----------|
| 1050 (lojalumo informacija)           | Vykdykite šį procesą, norėdami siųsti lojalumo konfigūracijos duomenis iš „Commerce“ į parduotuves. Naudinga šį procesą planuoti vykdyti dažnai, kad lojalumo duomenys būtų perduodami į visas parduotuves. | Paskirstymo grafikas |
| Apdoroti lojalumo planus              | Paleiskite šį procesą, norėdami susieti lojalumo planus su kanalais, kuriems priskirtas lojalumo planas. Šis procesas gali būti planuojamas paketiniam vykdymui. Jei pakeisite lojalumo konfigūracijos duomenis, pvz., lojalumo planus, lojalumo programas arba lojalumo atlygio taškus, turite vykdyti šį procesą. | Apdoroti lojalumo planus |
| Registruoti gautus lojalumo taškus paketuose | Vykdykite šį procesą, norėdami atnaujinti lojalumo korteles, kad į jas būtų įtrauktos operacijos, apdorotos neprisijungus. Šis procesas taikomas, tik jei pažymėtas puslapio **Bendrai naudojami prekybos parametrai** žymės langelis **Registruoti gautus taškus paketuose**, kad atlygį būtų galima gauti neprisijungus. | Registruoti gautus lojalumo taškus paketuose |
| Naujinti lojalumo kortelių pakopas            | Vykdykite šį procesą, norėdami palyginti kliento uždarbio veiklą su kategorijos taisyklėmis, taikomomis lojalumo programai, ir norėdami atnaujinti kliento būseną. Šis procesas reikalingas tik tada, jei pakeitėte lojalumo programų pakopų taisyklės ir norite, kad atnaujintas taisykles būtų pritaikytos atgaline data jau išduotoms lojalumo kortelėms. Šis procesas gali būti vykdomas arba paketiniu būdu, arba atskiroms kortelėms. | Naujinti lojalumo kortelių pakopas |

## <a name="loyalty-enhancements"></a>Lojalumo patobulinimai

„Commerce“ 2018 m. spalio mėn. leidime yra naujų lojalumo funkcijų. Visi nauji patobulinimai yra paaiškinti toliau.

- Pagal ankstesnių leidimų lojalumo planą mažmenininkai galėtų sukurti skirtingas uždarbio ir apmokėjimo taisykles pagal pakopas, kad būtų atskirtas skirtingų pakopų klientų atlygis. Dabar mažmenininkai kaip uždarbio ir apmokėjimo taisyklių dalį gali įtraukti „priskyrimus“, kad tam tikra klientų grupė galėtų būti esamų pakopų dalis, tačiau atlyginama skirtingai. Tai padeda išvengti papildomų pakopų kūrimo.
    
    > [!NOTE]
    > Uždarbio taisyklės lojalumo plane yra papildomos. Pavyzdžiui, jei sukuriate taisyklę atlyginti auksinės pakopos nariui 10 taškų už kiekvieną JAV dolerį, taip pat sukuriate taisyklę atlyginti klientui „veteranui“ 5 taškais už kiekvieną JAV dolerį, tada veteranas, kuris taip pat yra auksinės pakopos narys, už 1 JAV dolerį gaus 15 taškų, nes klientas atitinka abi eilutes. Tačiau jei klientas veteranas nebuvo auksinės pakopos narys, tada už kiekvieną dolerį gautų 5 taškus. Kad pokyčiai įsigaliotų kanaluose, vykdykite užduotis **Apdoroti lojalumo planus** ir **1050** (lojalumo informacija).
    
    ![Uždarbis pagal priskyrimą](./media/Affiliation-based-earning.png "Uždarbiai pagal priskyrimą")

- Mažmenininkai dažnai turi specialias kainas tam tikrai klientų grupei, kuriai nenori taikyti lojalumo programų. Pavyzdžiui, didmenininkams arba darbuotojams, kurie gauna specialias kainas, bet negauna lojalumo taškų. Paprastai „priskyrimai“ yra naudojami specialioms kainoms tokių klientų grupėms suteikti. Norėdamas apriboti tam tikrų klientų grupių galimybę gauti lojalumo taškų, mažmenininkas gali nustatyti vieną arba daugiau priskyrimų lojalumo plano skyriuje **Neįtraukti priskyrimai**. Tada, kai neįtrauktiems priskyrimams priklausantys klientai yra lojalumo plano nariai, jie negaus lojalumo taškų už savo pirkinius. Kad pokyčiai įsigaliotų kanaluose, vykdykite užduotis **Apdoroti lojalumo planus** ir **1050** (lojalumo informacija).

    ![Neįtraukti priskyrimai](./media/Excluded-affiliations.png "Pašalinti priskyrimus, kad nebūtų duodama lojalumo taškų")
    
- Mažmenininkai gali kanaluose generuoti lojalumo kortelių numerius. Iki 2018 m. spalio mėn. naujinimo mažmenininkai galėjo naudoti fizines lojalumo korteles arba sugeneruoti lojalumo kortelę naudodami unikalią kliento informaciją, pvz., telefono numerį. Norėdami įgalinti automatinį lojalumo kortelių generavimą parduotuvėse, įjunkite **Generuoti lojalumo kortelės numerį** su parduotuve susietame funkcijų profilyje. Interneto kanaluose mažmenininkai gali naudoti IssueLoyaltyCard API norėdami išduoti lojalumo korteles klientams. Mažmenininkai gali suteikti lojalumo kortelės numerį šiai API, kuris bus naudojamas generuojant lojalumo kortelę, arba sistema naudos lojalumo kortelių numeraciją, nustatytą „Commerce“. Tačiau jei numeracijos nėra ir mažmenininkas nesuteikia lojalumo kortelės numerio iškvietus API, tada rodoma klaida.

    ![Sugeneruoti lojalumo kortelę](./media/Generate-loyalty-card.png "Automatiškai generuoti lojalumo kortelės numerį")

- Gauti ir panaudoti lojalumo taškai dabar saugomi kiekvienai operacijai ir pardavimo užsakymams pagal pardavimo eilutę, kad tą pačią sumą būtų galima grąžinti arba atsiimti visiškų ar dalinių grąžinimų atvejais. Be to, matydami taškus pardavimo eilutės lygiu, skambučių centro vartotojai gali atsakyti į klientų klausimus, kiek taškų gauta arba panaudota kiekvienoje eilutėje. Iki šio pakeitimo atlygio taškai visada buvo perskaičiuojami grąžinant, todėl suma skirdavosi nuo originalios, jei uždarbio arba apmokėjimo taisyklės pasikeisdavo; be to, skambučių centrų vartotojai nemato taškų analizės. Taškus galima pamatyti naudojant kiekvienos lojalumo kortelės formą **Kortelės operacijos**. Norėdami įjungti šią funkciją, įjunkite konfigūraciją **Registruoti lojalumo taškų skaičius pagal pardavimo eilutę** skirtuke **Bendrai naudojami prekybos parametrai** \> **Bendra**.

    > [!NOTE]
    > Primygtinai rekomenduojame įjungti šią funkciją, kad užtikrintumėte, jog gavimo metu tiksli taškų suma būtų grąžinta arba atskaityta iš kliento.

- Mažmenininkai dabar gali nustatyti kiekvieno atlygio taško paskirstymo laikotarpį. Paskirstymo laikotarpio konfigūracija nustatys trukmę nuo gavimo datos, po kurios atlygio taškai taps pasiekiami klientams. Nepaskirstytus taškus galima peržiūrėti puslapio **Lojalumo kortelės** stulpelyje **Nepaskirstyti taškai**. Be to, mažmenininkai gali nustatyti didžiausią lojalumo atlygio taškų ribą kiekvienai lojalumo kortelei. Šį lauką galima naudoti norint sumažinti lojalumo apgaulės poveikį. Pasiekus didžiausią atlygio taškų skaičių, vartotojas negali gauti daugiau taškų. Mažmenininkas gali nuspręsti blokuoti tokias korteles, kol bus ištirta galima apgaulė. Jei mažmenininkas nustato apgaulę, jis negali tik užblokuoti kliento lojalumo kortelės, bet turi ir pažymėti, kad klientas užblokuotas. Norėdami tai padaryti nustatykite ypatybę **Blokuoti kliento įtraukimą į lojalumo programą** į **Taip** „FastTab“ **Commerce** dalyje **Visi klientai**. Užblokuoti klientai negalės gauti lojalumo kortelės jokiais kanalais.

    ![Paskirstymo ir didžiausio atlygio taškų skaičius](./media/Vesting-and-maximum-reward-points.png "Nustatyti paskirstymą ir didžiausio atlygio taškų skaičių")

- Priskyrimai naudojami siekiant suteikti specialias kainas ir nuolaidas, tačiau pasitaiko priskyrimų, kurių mažmenininkai nenori rodyti klientams. Pvz., priskyrimas pavadinimu „Daug išleidžiantis klientas“ gali patikti ne visiems klientams. Be to, yra priskyrimų, kurie neturi būti tvarkomi parduotuvėje, pvz., darbuotojai, nes nenorite, kad kasininkai nuspręstų, kas yra darbuotojas, ir taip suteiktų darbuotojams skirtas nuolaidas. Dabar mažmenininkai gali pasirinkti priskyrimus, kurie kanaluose turėtų būti paslėpti. Priskyrimų, kurie pažymėti **Slėpti kanaluose**, negalima peržiūrėti, pridėti arba pašalinti EKA. Tačiau produktams vis tiek bus taikomos kainos ir nuolaidos, susijusios su priskyrimu.

    ![Slėpti priskyrimus](./media/Hide-affiliations.png "Slėpti priskyrimus kanaluose")
    
- Skambučių centro vartotojai dabar gali lengviau ieškoti kliento naudodami savo lojalumo kortelės informaciją ir pasiekti kliento lojalumo kortelę bei kortelės operacijų puslapį iš puslapio **Klientų aptarnavimas**.

    ![Klientų aptarnavimo tarnyba](./media/Customer-service.png "Rasti kliento lojalumo informaciją")
    
- Jei lojalumo kortelė sugadinama, reikia sugeneruoti pakaitinę kortelę ir į ją perkelti esamus taškus. Pakaitinės kortelės srautas šiame leidime yra supaprastintas. Be to, klientai gali dalį arba visus savo lojalumo taškus padovanoti draugams ir šeimai. Kai taškai perkeliami, kiekvienai lojalumo kortelei sukuriami taškų koregavimo įrašai. Pakaitinės kortelės ir perkėlimo balanso funkciją galima pasiekti iš puslapio **Lojalumo kortelės**.

    ![Pakeisti ir perkelti taškus](./media/Replace-and-transfer-points.png "Pakeisti lojalumo kortelę arba perkelti balansą")
    
- Mažmenininkai gali norėti užfiksuoti konkretaus kanalo efektyvumą registruodami klientus į lojalumo programą. Išsaugomas lojalumo kortelių registracijos šaltinis, kad mažmenininkai galėtų sukurti šių duomenų ataskaitas. Registracijų šaltinis yra automatiškai užfiksuojamas visoms MPOS/CPOS arba „e-Commerce“ kanalais išduotoms lojalumo kortelėms. Kad lojalumo kortelės būtų išduotos naudojant tarnybinio biuro programą, skambučių centro vartotojas gali pasirinkti atitinkamą kanalą.
- Ankstesniuose leidimuose mažmenininkai galėjo naudoti MPOS/CPOS norėdami panaudoti klientų lojalumo taškus parduotuvėje. Tačiau šiuose leidimuose, kadangi lojalumo balansas rodomas lojalumo taškais, kasininkas negalėdavo pamatyti valiutos vertės sumos, kuri galėjo būti taikoma dabartinei operacijai. Kasininkas prieš suteikdamas lojalumo taškus turėjo konvertuoti juos į valiutą. Dabartiniame leidime, kai eilutės pridedamos prie operacijos, kasininkas gal matyti sumą, kurią lojalumo taškai gali padengti dabartinėje operacijoje, todėl lengva operacijai pritaikyti dalį arba visus lojalumo taškus. Be to, kasininkas gali matyti taškus, kurie baigs galioti po 30 dienų, kad galėtų papildomai parduoti ar pritaikyti kryžminį pardavimą ir taip motyvuoti klientą išleisti baigiančius galioti taškus tai operacijai.

    ![Taškai, kuriuos apima lojalumo balansas](./media/Points-covered-by-loyalty-balance.png "Rodyti lojalumo taškų apimamą balansą")

    ![Baigiantys galioti taškai](./media/Expiring-points.png "Peržiūrėti baigiančius galioti taškus")

- Išleidę 8.1.3 leidimą mes įjungėme parinktį „mokėjimas pagal lojalumą“ skambučių centro kanale. Norėdami įjungti šią parinktį, sukurkite lojalumo mokėjimo priemonės tipą ir susiekite jį su skambučių centru. 

    > [!NOTE]
    > Kadangi lojalumo mokėjimai nustatomi kaip mokėjimai kortele, turėsite pasirinkti kortelę puslapyje **Kortelės sąranka**. 

    ![Lojalumo kortelės sąranka](./media/LoyaltyCardSetup.png "Lojalumo kortelės sąranka")

    Tai nustačius klientai gali panaudoti savo lojalumo taškus skambučių centre. Be to, papildomai patobulinome vartotojo sąsają patirtį, kad būtų rodoma parinktis „Suma, padengta lojalumo taškais“, kad skambučių centro vartotojams nereikėtų atidaryti kito ekrano norint peržiūrėti lojalumo balansą.

- Daugelis mažmenininkų teikia lojalumo taškus tik pagal pardavimo operacijas, tačiau daugiau į klientą orientuoti mažmenininkai nori apdovanoti klientus už bet kokią veiklą su prekės ženklu. Pavyzdžiui, jie nori apdovanoti už internetinės apklausos užpildymą, parduotuvės lankymą, mažmenininkų įvertinimą paspaudžiant Patinka „Facebook“ ar „Twitter“ žinutę apie mažmenininką. Norėdamas tai padaryti mažmenininkas gali nustatyti bet kokį skaičių objektų „Kitas veiklos tipas“ ir apibrėžti atitinkamas tokios veiklos uždarbio taisykles. Taip pat atskleistas „Commerce Scale Unit“ API PostNonTransactionalActivityLoyaltyPoints, kurį galima iškviesti nustačius veiklą, už kurią klientui turi būti skirtą lojalumo taškų. Šis API tikisi lojalumo kortelės ID, kanalo ID ir kitos veiklos tipo ID, kad būtų galima nustatyti klientą, kuriam turėtų būti skirta taškų, ir veiklos pajamų taisyklę. 

    Taškų skyrimas už ne operacijų veiklas paprastai vykdomas dviem pagrindiniais veiksmais.

    - Nustatymas, kad įvyko veikla, kuri turi būti atlyginta.
    - Atitinkamo taškų kiekio skyrimas.

    Pirmas veiksmas yra išorinis „Commerce“ veiksmas, pavyzdžiui, „Twitter“ žinutės apie prekių ženklą paskelbimas arba „Facebook“ paspaudimas „Patinka“. Kai ši veikla nustatyta, mažmenininkai gali iškviesti pirmiau minėtą „Commerce Scale Unit“ API ir skirti lojalumo taškų tikruoju laiku. Tokiais atvejais peržiūros veiksmas nereikalingas, nes veikla įvyko ir atitinkamas taškų kiekis turi būti skirtas. Tačiau yra scenarijų, kai mažmenininkas nori peržiūrėti įrašus prieš skirdamas taškus. Pavyzdžiui, mažmenininkas nustatė darbo grupę parduotuvėje, prie kurios klientai prisiregistruoja naudodami el. prekybos svetainę arba bet kurią kitą įvykių registravimo programą. Tačiau tik dalyvaujantys klientai turėtų gauti lojalumo taškų. Tokiais atvejais 10.0 leidime mes pristatėme duomenų objektą pavadinimu **Mažmeninės prekybos lojalumo kitos veiklos tipo eilutės**. Šis duomenų objektas suteikia galimybę mažmenininkams naudoti duomenų importavimo / eksportavimo sistemą (DIXF) arba „OData“ API norint įrašyti veiklas, už kurias klientams turėtų būti skiriama lojalumo taškų. Duomenų objektas išsaugo veikloas žurnale pavadinimu **Kitų veiklų lojalumo eilutės**, kurį galima naudoti peržiūros ir modifikavimo tikslais. Peržiūrėjus duomenis, IT vartotojas gali neautomatiškai registruoti veiklos eilutes arba vykdyti užduotį pavadinimu **Apdoroti lojalumo eilučių kitos veiklos tipą**, kuri užregistruos neužregistruotas veiklos eilutes ir skirs taškų klientams pagal uždarbio taisykles. Pirmiau pateiktame scenarijuje įvykių registravimo programa iškviestų „OData“ API siųsti kliento informaciją į „Commerce“. Tačiau IT vartotojas gali registruoti tik tų klientų, kurie dalyvavo darbo grupėje, veiklos eilutes, o kitų klientų veiklos eilutes jis gali panaikinti. 

    > [!NOTE]
    > Šiuo metu sistema liepia vartotojams nustatyti objekto „kitos veiklos tipai“ numeraciją, tačiau būsimuose leidimuose tai nebus būtinas veiksmas. Norėdami nustatyti numeraciją, pasirinkite **Bendrai naudojami prekybos parametrai** \> **Numeracijos** ir pasirinkite objekto **Lojalumo kitos veiklos tipo ID** numeraciją.

- Siekiant teikti geras klientų aptarnavimo paslaugas ir efektyviai išspręsti klientų užklausas, kasininkams svarbu turėti preigą prie viso kliento profilio. Išleidus 10.0 leidimą, kasininkai galės EKA matyti lojalumo retrospektyvos informaciją kartu su susietos lojalumo programos ir pakopos informacija.
- Nemokamas pristatymas arba pristatymas su nuolaida yra vienas iš labiausiai pirkti internetu motyvuojančių veiksnių. Norėdami įgalinti mažmenininkus nustatyti siuntimo akcijas, išleisdami 10.0 leidimą pristatėme naujo tipo akciją pavadinimu „Ribinė siuntimo nuolaidos vertė“, kuria naudodamasis mažmenininkas galės nustatyti ribines vertes, kurias pasiekus bus suteikta siuntimo nuolaida arba nemokamas siuntimas. Pavyzdžiui, 35 USD išlaidų suma norint nemokėti už „dviejų dienų siuntimą“ arba nemokamas „dviejų dienų siuntimas“ visiems lojalumo klientams. Ši funkcija naudoja naują funkciją Išplėstinės automatinės išlaidos. Žr. [dokumentaciją apie išplėstines automatines išlaidas](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges). Šios išplėstinės automatinės išlaidos turi būti įjungtos, kad veiktų siuntimo akcija. Jas galima įjungti skirtuke **Klientų užsakymai**, pateiktame puslapyje **Prekybos parametrai**; taip pat įjunkite konfigūraciją „Naudoti išplėstines automatines išlaidas“. Be to, kadangi mažmenininkas gali nustatyti kelių tipų išlaidas, pvz., tvarkymo arba diegimo, mažmenininkas turi nurodyti, kurios išlaidos yra laikomos siuntimo išlaidomis. Siuntimo nuolaidos taikomos tik siuntimo išlaidoms. Norėdami nurodyti išlaidas kaip siuntimo išlaidas, atidarykite formą **Išlaidų kodai** pasirinkdami **Mažmeninė prekyba ir prekyba** \> **Mažmeninės prekybos ir prekybos IT** \> **Kanalo sąranka** \> **Išlaidos** ir įjunkite pageidaujamų išlaidų žymės langelį „Siuntimo išlaidos“. Dabar galite atidaryti formą **Ribinė siuntimo nuolaidos vertė** ir nustatyti nuolaidą.

    Ši nuolaida kaip ir produktų nuolaidos atsižvelgia į visas esamas standartines nuolaidų galimybes, pavyzdžiui, ji suteikia galimybę mažmenininkui apriboti šias nuolaidas naudojant kuponus, kad nuolaidomis galėtų pasinaudoti tik kuponus turintys klientai. Be to, šios nuolaidos naudoja kainų grupių galimybę, kad nustatytų tokių nuolaidų tinkamumą. Pavyzdžiui, mažmenininkas gali pasirinkti taikyti šias akcijas tik interneto kanalu ir (arba) tam tikrų klientų grupių kanaluose, pvz., lojalių klientų kanale. Kai užsakymo eilučių, kuriose nurodytas pristatymo būdas, reikšmės pasiekia nustatytą ribą, tada taikoma siuntimo nuolaida ir sumažinamas siuntimo išlaidos atsižvelgiant į nustatytą nuolaidą. 

    > [!NOTE]
    > Skirtingai nuo kitų laikotarpio nuolaidų, pvz., kiekio, paprastos, nuolaidos prekių rinkiniui ir ribinės vertės nuolaidos, siuntimo nuolaida nesukuria nuolaidos eilučių, bet redaguoja siuntimo išlaidas tiesiogiai ir prideda nuolaidos pavadinimą prie išlaidų aprašymo.
