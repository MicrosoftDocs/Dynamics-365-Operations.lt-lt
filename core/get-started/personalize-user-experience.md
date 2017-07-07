---
title: Vartotojo patirties personalizavimas
description: "Šiame straipsnyje paaiškinama, kaip galite personalizuoti „Microsoft Dynamics 365 for Finance and Operations‟."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b338a930777a5945eb6318dc8066fb3649c79dbe
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017


---

# <a name="personalize-the-user-experience"></a>Vartotojo patirties personalizavimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje paaiškinama, kaip galite personalizuoti „Microsoft Dynamics 365 for Finance and Operations‟.

Yra daug „Microsoft Dynamics 365 for Finance and Operations“ personalizavimo būdų. Kai kurie personalizavimo būdai priklauso nuo jūsų pasirinkimų sąrankos puslapio parinkčių sąraše. Kai kurios personalizavimo parinktys yra netiesioginės, pvz., „Finance and Operations“ seka jūsų keičiamą tinklelio stulpelių plotį ir „FastTab“ sutrauktą / išplėstą būseną. Kitos personalizavimo parinktys yra tiesioginės. Norint keisti tiesiogines personalizavimo parinktis, naudojamas interaktyvaus personalizavimo režimas ir puslapio išvaizda modifikuojama tiesiogiai valdant elementų rodymą ir elgseną puslapyje. 

Bet kurio tipo personalizavimo parametrai, kuriuos „Finance and Operations“ nustato vartotojas, taikomi tik tam vartotojui, nepriklausomai nuo to, su kokia įmone jis sąveikauja. Vartotojo atlikti puslapio keitimai neturi įtakos kitiems sistemos vartotojams.

## <a name="systemwide-options-for-the-current-user"></a>Dabartinio vartotojo visos sistemos parinktys
Naršymo juostoje galite rasti krumpliaračio vaizdą, kuris vadinamas meniu mygtuku **Parametrai**. Atidarius meniu **Parametrai** rodomas pasirinkimų sąrašas. Pasirinkus **Parinktys** atidaromas vartotojo puslapis **Parinktys**. Ten rasite keturis parinkčių skirtukus: **Vaizdas**, **Nuostatos**, **Paskyra** ir **Darbo eiga**.

-   **Vaizdas:** galima pasirinkti puslapio elementų spalvų temą ir dydį.
-   **Nuostatos:** galima pasirinkti numatytuosius parametrus, taikytinus kiekvieną kartą atidarant „Finance and Operations“, įskaitant įmonę, pradinį puslapį ir numatytąjį rodymo / redagavimo režimą (kuris nustato, ar kiekvieną kartą atidarius puslapį jis yra užrakintas ir jį galima tik peržiūrėti, ar jį galima redaguoti). Taip pat rasite kalbos, laiko juostos ir datos, laiko ir bei skaičių formato parinktis. Galiausiai šiame puslapyje yra papildomų nuostatų, kurios skiriasi priklausomai nuo versijos.
-   **Paskyra:** galima nurodyti vartotojo ID ir kitas su paskyra susijusias parinktis.
-   **Darbo eiga:** galima pasirinkti su darbo eiga susijusias parinktis.

## <a name="implicit-personalizations"></a>Netiesioginis personalizavimas
Netiesioginis yra personalizavimas, kurį atliekate tiesiog sąveikaudami su tam tikrais valdikliais, kurie įsimeną savo esamą matomą būseną. 

**Tinklelio stulpeliai:** sąraše galite koreguoti stulpelio plotį, pasirinkdami dydžio keitimo juostą kairėje arba dešinėje stulpelio antraštės pusėje ir slinkdami ją į kairę arba į dešinėje. „Finance and Operations“ išsaugos jūsų norimą plotį ir kiekvieną kartą atidarius puslapį su tuo sąrašu rodomas stulpelis bus to pločio. 

**FastTabs:** kai kuriuose puslapiuose yra išplečiamos dalys, vadinamos „FastTab“. „Finance and Operations“ išsaugos išplėstų ir sutrauktų „FastTab“ rodinius. Kiekvieną kartą vėl atidarę puslapį matysite tuos pačius „FastTab“ išplėstus arba sutrauktus, atsižvelgiant į tai, kaip paskutinį kartą juos naudojote. Šiame straipsnyje paaiškinsime, kaip keisti „FastTab“dalių tvarką. Kai kuriais atvejais sutraukus „FastTab“ galima padidinti efektyvumą, nes „Finance and Operations“ nereikės nuskaityti to „FastTab“ informacijos, kol „FastTab“ neišskleistas. 

**Fact Boxes:** kai kuriuose puslapiuose yra dalis, vadinama „Fact Box“ sritimi. Šioje srityje yra tik skaityti skirta informacija, susijusi su dabartine puslapio tema. Kiekviena „Fact Box“ srities dalis yra vadinama „Fact Box“. „Fact Box“ galite išplėsti arba sutraukti, o „Finance and Operations“ išsaugos jūsų nuostatą. Kai kuriais atvejais sutraukus „Fact Box“ galima padidinti efektyvumą, nes „Finance and Operations“ nereikės nuskaityti to „Fact Box“ informacijos, kol „Fact Box“ neišskleistas.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Tiesioginis personalizavimas naudojant personalizavimo įrankių juostą
Kiekvienas asmuo ir įmonė turi skirtingą nuomonę apie tai, kurie duomenys yra jiems svarbiausi ir kurie nėra reikalingi jų verslui vykdyti. Galimybė pritaikyti asmeniniams poreikiams tai, kaip informacija yra užsakoma, kaip su ja sąveikaujama arba net kaip ji slepiama, yra pagrindinis būdas „Finance and Operations“ personalizuoti ir produktyviai naudoti. 

Tiesioginės personalizavimo parinktys – tai tokios parinktys, kurias pasirenkate turėdami aiškų tikslą naudodami personalizavimo meniu pakeisti elemento arba puslapio išvaizdą arba elgesį. Paties paprasčiausio tipo tiesioginio personalizavimo parinktys – tai parinktys, kurios pasirenkamos dešiniuoju pelės klavišu spustelint elementą ir pasirenkant **Personalizuoti**. (Atkreipkite dėmesį, kad personalizuoti galima ne visus jūsų puslapyje esančius elementus.) Pasirinkę šį personalizavimo metodą matysite elemento ypatybių langą. 

[![Elemento ypatybių personalizavimas](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Savo puslapio elementą galite personalizuoti šiuo būdu, jei tiesiog norite keisti elemento žymę, slėpti elementą, kad jis nebūtų rodomas puslapyje (jokie duomenys nėra keičiami, tiesiog nerodoma informacija), įtraukti informaciją į „FastTab“ suvestinės dalį (jei elementas yra „FastTab“), naudojant tabuliavimo klavišą praleisti lauką arba išjungti duomenų keitimo funkciją pažymint juos kaip „Neredaguoti“. 

Kai norite elementus perkelti ar slėpti arba atlikti kelis keitimus, galite naudoti personalizavimo įrankių juostą, kurią galima rasti elemento lange Ypatybės pasirinkus **Pritaikyti šią formą asmeniniams poreikiams**. Personalizavimo įrankių juostą taip pat galima rasti formos veiksmų srityje po skirtuko **Parinktys** personalizavimo grupe. Pasirinkite **Pritaikyti šią formą asmeniniams poreikiams** ir pamatysite personalizavimo įrankių juostą. 

[![Personalizavimo įrankių juosta](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Naudojant personalizavimo įrankių juostą galima atlikti kelis personalizavimo veiksmus. Pasirinkite įrankį **Pasirinkti**, jei vienu metu norite pasirinkti ir pakeisti kelių elementų ypatybes. Pirmiausia pasirinkite įrankį Pasirinkti, o tada spustelėkite elementą, kurio ypatybes norite modifikuoti. Kai pasirenkate elementą, atsidaro elemento ypatybių langas ir jūs galite keisti visas elemento ypatybes. Galite pakartoti procesą su kitais formos elementais, kuriuos galima personalizuoti. Kai kuriais atvejais galite pasirinkti elementą ir matyti, kad kai kurių ypatybių modifikuoti negalima. Tai reiškia, kad atsižvelgdama į tai, kaip dabartinis elementas yra naudojamas, „Finance and Operations“ negali jums leisti tos ypatybės keisti. Pavyzdžiui, negalite slėpti reikiamo lauko. 

Pasirinkite įrankį **Perkelti**, jei norite elementą pasirinkti ir perkelti į kitą dabartinės elementų grupės vietą. (Negalima perkelti elemento už jo pirminės grupės ribų). Pirmiausia pasirinkite įrankį Perkelti, o tada spustelėkite elementą, kurį norite perkelti. Spustelėjus norimą perkelti elementą, „Finance and Operations“ nuskaitys formą, kad išsiaiškintų, kur galima šį elementą perkelti, ir sukurs „nuvilkimo zonas“, rodomas kaip spalvota, paryškinta linija šalia dabartinės grupės srities, į kurią galima perkelti velkamą elementą. 

Pasirinkite įrankį **Slėpti**, jei norite elementą pasirinkti ir slėpti. Norėdami slėpti elementą, tiesiog pasirinkite įrankį Slėpti ir spustelėkite elementą, kurį norite slėpti. Kai pasirenkate įrankį Slėpti, visi šiuo metu paslėpti elementai bus matomi ir rodomi užtamsintame fone, kad būtų galima pasirinkti elementą, kurio norite nebeslėpti. Pasirinkite įrankį Pasirinkti, norėdami pamatyti, kaip puslapis atrodys, jei pasirinkti elementai bus paslėpti. Pasirinkite įrankį **Suvestinė**, jei skaitinį arba eilutės lauką norite rodyti „FastTab“ suvestinės srityje. Įrankis Suvestinė bus taikomas tik laukams, esantiems „FastTab“ dalyje. Kai pasirenkate įrankį Suvestinė, „Finance and Operations“ rodys visus laukus, kurie kaip suvestinės laukai buvo pasirinkti perkeliant juos užtamsintą foną. Interaktyviai galite įtraukti ir šalinti laukus iš „FastTab“ suvestinės, spustelėdami lauką. 

Pasirinkite įrankį **Praleisti**, norėdami pašalinti elementą iš puslapio klaviatūros tabuliavimo sekos. Pasirinkus įrankį Praleisti, visi šiuo metu praleidžiami elementai bus rodomi užtamsintame fone, kad praleidžiamą elementą galėtumėte vėl pasirinkti ir įtraukti į tabuliavimo seką. 

Pasirinkite įrankį **Redaguoti**, jei elementas turi būti pažymėtas kaip Redaguojamas arba Neredaguojamas. Kai pasirenkate įrankį Redaguoti, visi šiuo metu neredaguojami elementai bus rodomi užtamsintame fone, kad būtų galima juos pasirinkti ir padaryti redaguojamais. Atminkite, kad kai kurie laukai būtini ir jų begalima padaryti neredaguojamais. Šie laukai bus rodomi su šalia jų esančia spynos piktograma. 

Pasirinkite įrankį **Įtraukti**, norėdami lauką įtraukti į puslapį. Naudodami įtraukimo įrankį kurti naujo lauko negalite, bet galite įtraukti laukus, kurie yra dabartinio puslapio aprašo dalis, bet nėra rodomi puslapyje. Prieš naudojant įrankį Įtraukti, pirmiausia turėsite pasirinkti grupę arba sritį, kurioje norite įtraukti lauką. Dialogo lange bus rodomas laukų, susijusių su pasirinkta sritimi, sąrašas. Iš to dialogo lange pasirinkite vieną ar kelis įtrauktinus laukus ir spustelėkite Įterpti. Jei vėliau norite pašalinti anksčiau įtrauktą lauką, pakartokite šį procesą, bet tiesiog išvalykite anksčiau įtrauktą lauką. 

Paspauskite mygtuką **Valdyti**, kad pamatytumėte su visomis dabartinio puslapio personalizacijomis susijusių valdymo parinkčių sąrašą. 

Paspauskite **Valyti**, kad atkurtumėte numatytąją įdiegus puslapį naudotą būseną. Visos dabartinio puslapio personalizacijos bus panaikintos. Veiksmo atšaukti negalima, todėl naudokite šią parinktį tik tada, kai tikrai žinote, kad norite atkurti puslapį. 

Pasirinkite **Importuoti**, jei norite naudoti šio puslapio personalizavimo parametrus iš personalizavimo failo, kurį jūs arba kas nors kitas anksčiau sukūrė. Importuojant personalizavimo parametrus bus išvalyti visi nustatyti viso puslapio personalizavimo parametrai ir bus naudojami visi pasirinkto failo personalizavimo parametrai. Jei personalizavimo parametrus norite įrašyti arba naudoti bendrai, pasirinkite parinktį **Eksportuoti** ir įrašykite juos į failą. 

Pasirinkite mygtuką **Uždaryti**, norėdami uždaryti įrankių juostą ir vėl įjungti ankstesnę puslapio interaktyvią būseną. 

Naudojant personalizavimo įrankių juostą lengva įrašyti keitimus. Jūsų pakeisti personalizavimo parametrai bus įrašyti iš karto, todėl mygtuko **Įrašyti** spustelėti nereikia. Kai kuriais atvejais pasirinkę įrankį šalia elemento matysite spynos piktogramą. Tai reiškia, kad norint, jog puslapis veiktų tinkamai, negalima modifikuoti su pasirinktu įrankiu susijusių ypatybių. Atidarius personalizavimo įrankių juostą, puslapis tampa neinteraktyvus. Įvesti duomenų arba išplėsti ar sutraukti skyrių negalima.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Tiesioginis personalizavimas: išklotinės arba sąrašo įtraukimas į darbo sritį
Kai kurie puslapiai su sąrašais turės papildomą personalizavimo funkciją, kurią galima rasti veiksmų srityje, esančioje skirtuko Parinktys personalizavimo grupėje. Pasirinkite **Įtraukti į darbo sritį**, norėdami atidaryti išplečiamąjį sąrašą, kuris suteikia galimybę dabartinio sąrašo informaciją (filtruotą ir rūšiuotą arba numatytąją) darbo srityje rodyti kaip sąrašą arba suvestinę (kuriuos galima naudoti norint rodyti sąrašo elementų skaičių). 

[![Įtraukti į darbo sritį](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Norėdami sąrašą įtraukti į darbo sritį, pirmiausia pasirinktinai rūšiuokite arba filtruokite informacijos sąrašą, kad jį pamatytumėte darbo srityje, tada pasirinkite dialogo langą Įtraukti į darbo sritį. Tada pasirinkite norimą sritį ir išplečiamajame sąraše Pristatymas pasirinkite **Sąrašas**. Pasirinkus **Sąrašas**, atidaromas dialogo langas, kuriame galima pasirinkti stulpelius, kuriuos norite matyti sąraše, ir sąrašo žymę, kuri bus rodoma darbo srityje. 

Norėdami suvestinę įtraukti į darbo sritį, pirmiausia filtruokite sąrašą, kad būtų rodomi duomenys, kuriuos norite apibendrinti (arba kuriuos norite greitai rasti). Tada atidarykite išplečiamąjį dialogo langą Įtraukti į darbo sritį. Tada pasirinkite norimą sritį ir išplečiamajame meniu Pristatymas pasirinkite **Išklotinė**. Pasirinkus **Išklotinė**, rodomas dialogo langas, kuriame galima pasirinkti išklotinės žymę, ar išklotinė rodys skaičių. Į darbo sritį įtraukta išklotinė suteikia galimybę atidaryti esamą puslapį iš darbo srities ir rodyti informacijos, susijusios su išklotine, sąrašą. 

Kai sąrašas arba išklotinė įtraukiama į darbo sritį, galite atidaryti tą darbo sritį ir pertvarkyti sąrašo arba išklotinės išdėstymą grupėje, kurioje ji buvo sukurta.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Tiesioginis personalizavimas: suvestinės iš darbo srities įtraukimas į ataskaitų sritį
Kai kuriose srityse yra skaičių išklotinės (išklotinės su skaičiais), kurias taip pat galite norėti matyti įrankių juostoje. Darbo srityje dešiniuoju pelės mygtuku spustelėkite skaičių išklotinę ir pasirinkite **Pritaikyti**. Pasirinkite **Prisegti prie ataskaitų srities**. Kitą kartą atidarę (ir atnaujinę) pasirinktą ataskaitų sritį, tą skaičių matysite po tos darbo srities naršymo išklotine ataskaitų srityje.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Tiesioginis personalizavimas: įrankių juostos personalizavimas
Ataskaitų sritis dažnai yra pirmas rodomas puslapis atidarius „Finance and Operations“. Galite personalizuoti ataskaitų sritį norėdami pervardyti darbo srities naršymo išklotines, rodyti tik išklotines, kurias norite matyti, pervardyti išklotines arba išdėstyti išklotines norima tvarka. Norėdami personalizuoti ataskaitų sritį, pasirinkite bet kurą išklotinę ir spustelėję dešinįjį pelės mygtuką atidarykite kontekstinį meniu. Kontekstiniame meniu pasirinkite **Pritaikyti**. Jei pasirinktą išklotiną norite paslėpti, pervardyti arba praleisti, galite šį keitimą atlikti tiesiai rodomame lange Ypatybės. Jei norite keisti išklotinių išdėstymą, lange Ypatybės pasirinkite **Pritaikyti šią formą asmeniniams poreikiams** ir atidarykite personalizavimo įrankių juostą. Tada galite naudoti įrankį Perkelti ir pakeisti išklotinių išdėstymą.

## <a name="administration-of-personalization"></a>Personalizavimo parametrų administravimas
Personalizavę puslapį galite bendrinti personalizavimą su kitais vartotojo vartotojais. Tiesiog eksportuokite personalizuotą puslapį. Tada kitų vartotojų galite paprašyti atsidaryti personalizuotą puslapį ir importuoti personalizavimo failą, kurį sukūrėte.

Vartotojai, turintys administratoriaus teises, taip pat gali valdyti kitų vartotojų personalizavimą puslapyje **Personalizavimas**. Šiame puslapyje yra keturi skirtukai: **Sistema**, **Vartotojai**, **Importuoti** ir **Išvalyti**.

- **Sistema** – galite laikinai pasyvinti arba išjungti visus sistemos personalizavimus. Tokiu atveju jūs nepanaikinate personalizavimo. Užuot panaikinę, tiesiog iš naujo nustatote visus puslapius į jų numatytąją būseną. Jeigu vėliau iš naujo suaktyvinate personalizavimą, visi personalizavimai iš naujo pritaikomi kiekvienam vartotojo puslapiui. Taip pat galite visų vartotojų personalizavimo parametrus naikinti. Atkreipkite dėmesį, kad panaikinus sistemos personalizavimo parametrus, nėra būdo juos automatiškai vėl suaktyvinti. Todėl prieš atlikdami šį veiksmą įsitikinkite, kad eksportavote visu personalizavimus, kuriuos vėliau galite norėti importuoti.
- **Vartotojai** – galite nurodyti, ar kiekvienas vartotojas gali atlikti netiesioginį personalizavimą arba tiesioginį personalizavimą. Taip pat galite nurodyti, kurie vartotojai gali tiesiogiai arba netiesiogiai personalizuoti konkretų puslapį. Galiausiai galite importuoti, eksportuoti arba panaikinti kiekvieno vartotojo personalizavimą.
- **Importuoti** – galite importuoti personalizavimą vienam ar daugiau vartotojų. Šį skirtuką naudokite, kai sukūrėte puslapio ar darbo srities personalizavimą ir eksportavote šį personalizavimą kaip personalizavimo failą. Kad importuotumėte personalizavimo failą ir taikytumėte jį vienam ar daugiau vartotojų, vartotojų sąraše pasirinkite konkrečius vartotojus arba filtruokite pagal tam tikrą vaidmenį, tada pasirinkite vartotojus šiam vaidmeniui. Pasirinkus vartotojus, kurie naudos jūsų personalizavimą, spustelėkite **Importuoti** ir pasirinkite savo personalizavimo failą. Personalizavimas bus patikrintas ir taikomas visiems pasirinktiems vartotojams, kai jie kitą kartą atidarys pasirinktą puslapį.
- **Išvalyti** – galite išvalyti vieno ar daugiau vartotojų puslapio ar darbo srities personalizavimą. Pirmiausia pasirinkite puslapį arba darbo sritį, kurios personalizavimą norite išvalyti. Tada visų vartotojų sąraše pasirinkite atskirus vartotojus arba filtruokite pagal tam tikrą jo vaidmenį ir pasirinkite vartotojus šiam vaidmeniui. Kai pasirinkote puslapį arba darbo sritį ir vartotojus, spustelėkite **Išvalyti**. Išvalomi visi personalizavimai, kuriuos pasirinkti vartotojai taikė pasirinktam puslapiui arba darbo sričiai. Šio veiksmo anuliuoti negalima. Tačiau jei puslapyje ar darbo srityje yra įrašytas personalizavimas, toks personalizavimas gali būti iš naujo importuojamas.




