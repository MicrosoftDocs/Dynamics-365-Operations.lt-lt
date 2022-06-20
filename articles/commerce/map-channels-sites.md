---
title: Susieti kanalus su elektroninės prekybos svetainėmis
description: Šiame straipsnyje aprašomi kai kurie į bendruosius kanalų susiejimo Microsoft Dynamics 365 Commerce scenarijus, kuriuose galima atsiskaityti pagal daugelį kitų verslo reikalavimų.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902768"
---
# <a name="map-channels-to-e-commerce-sites"></a>Susieti kanalus su elektroninės prekybos svetainėmis

Šiame straipsnyje aprašomi kai kurie į bendruosius kanalų susiejimo Microsoft Dynamics 365 Commerce scenarijus, kuriuose galima atsiskaityti pagal daugelį kitų verslo reikalavimų.

Dynamics 365 Commerce palaiko daugelį verslo scenarijų, siekiant [susieti interneto](#channels) kanalus, kurie turi sukonfigūruotą produktų rinkinį, kainas ir nuolaidas su klientų el. komercijos [svetainės](#e-commerce-sites) patirtimi.

Šiame straipsnyje pateikiami šie scenarijai:

- **Vienos kalbos kanalas, kuriame yra viena el. komercijos svetainės patirtis.** Pavyzdžiui, į šį scenarijų gali būti įeis vieno ženklo svetainė, sukonfigūruota JAV anglų rinkai.
- **Kelių kalbų kanalas, turintis vieną lokalizuotą svetainės patirtį.** Pavyzdžiui, šiame scenarijuje gali būti viena prekės ženklo svetainė, sukonfigūruota Kanadai naudojant prancūzų ir anglų kalbos palaikymą. Tokiu atveju vartotojai, kurie pasirenka skirtingas kalbas, turi tokią pačią svetainės patirtį, bet lokalizuota į kiekvieno vartotojo pasirinktą kalbą.
- **Kelių kalbų kanalas, kuriame turite skirtingas svetainės funkcijas kalba.** Pavyzdžiui, šiame scenarijuje gali būti viena prekės ženklo svetainė, sukonfigūruota Kanadai naudojant prancūzų ir anglų kalbos palaikymą. Šiame scenarijuje kiekviena kalba turi unikalią svetainės patirtį.
- **Keli kanalai (vienos kalbos ir (arba) kelių kalbų), kurie turi vieną lokalizuotą svetainės patirtį.** Pavyzdžiui, šiame scenarijuje gali būti viena prekės ženklo svetainė, sukonfigūruota Australijos ir Naujosios Zelandijos. Tokiu atveju abi šalys dalijasi tokią pačią svetainės patirtį anglų kalba, bet kiekviena šalis yra sukonfigūruota su skirtingais produktais, valiuta, kainomis, nuolaidomis ir siuntimo būdais.
- **Keli kanalai (vienos kalbos ir (arba) kelių kalbų), kurie kanalui turi skirtingą svetainės patirtį.** Pavyzdžiui, šiame scenarijuje gali būti viena prekės ženklo svetainė, sukonfigūruota Australijos, Kanados ir Vokietijos keliomis kalbomis. Tokiu atveju kiekviena šalis turi unikalią svetainės patirtį, sukonfigūruotą su skirtingais produktais, valiuta, kainomis, nuolaidomis ir siuntimo būdais.

## <a name="channels"></a>Kanalai

Kanalas (taip pat vadinamas interneto parduotuve arba interneto kanalu) reiškia interneto el. komercijos parduotuvės kompiuterį, naudojamą produktams, kainoms, nuolaidoms, kalboms, mokėjimo metodams, pristatymo metodams, vykdymo centrams ir kitiems interneto patirties aspektams, kurie bus pasiekiami jūsų el. komercijos klientams, susieti. Kanalai sukuriami ir valdomi "Commerce Headquarters" ir susieti su vienu juridiniu [subjektu](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Juridinis subjektas paprastai yra vienoje šalyje, kurioje reikia kanalo mokesčių ataskaitų, ir gali būti sukonfigūruotas tik viena valiuta.

Daugiau informacijos apie kanalus ieškokite Kanalo [peržiūra](channels-overview.md). Daugiau informacijos apie tai, kaip sukurti interneto kanalą, ieškokite [interneto kanalo nustatyti](channel-setup-online.md).

Toliau pateiktas "Commerce Headquarters" pavyzdys rodo numatytuosius interneto kanalus, kurie diegiami pasirinkus Dynamics 365 Commerce demonstracinių duomenų pasirinktį.

![Numatytieji demonstraciniai duomenų kanalai "Commerce Headquarters".](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>El. komercijos svetainės

El. komercijos svetainėje yra svetainės puslapių rinkinys, kurį klientai naudoja naršydami ir pirkdami. El. "Commerce" svetainės valdomos "Commerce" svetainių generatoriuje.

Daugiau informacijos apie tai, kaip kurti ir valdyti svetaines svetainės generatoriuje, ieškokite [el. komercijos svetainės peržvalgoje](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Į bendrą kanalų susiejimo scenarijų

Dynamics 365 Commerce palaiko platų kanalų susiejimo scenarijų diapazoną. Toliau pateikiami kanalo susiejimo scenarijai yra tik visų galimų kanalo susiejimo scenarijų antrinis rinkinys. Jie skirti kaip vadovas, padėsiančių jums suplanuoti bet kuriuos unikalius verslo scenarijus. Fiktyvi Adventure Works versija prekių parduotuvė, Dynamics 365 Commerce įtraukta į demonstracinius duomenis, naudojama kaip kiekvieno scenarijaus pavyzdys.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Vienos kalbos kanalas, kuriame yra viena el. komercijos svetainės patirtis

Dažniausiai, viename kanale yra viena kalba, skirta parduoti vienoje rinkoje. Šio scenarijaus pavyzdys yra internetinė parduotuvė Adventure Works, kuri nustatyta tik JAV anglų rinkai.

Šiame pavyzdyje parodyta kanalo konfigūracija "Commerce Headquarters". Šioje konfigūracijoje interneto kanalas palaiko tik vieną kalbą (**en-us**), vieną valiutą (**USD**) ir vieną verslo objektą (**usvz**., naudojamą mokesčių ataskaitoms).

!["Commerce Headquarters" išryškintos "Commerce Headquarters" internetinės parduotuvės juridinio subjekto, valiutos ir kalbos vertės.](media/channel-mapping-3.png)

Vieno interneto kanalo, svetainės generatoriuje, galima susieti su viena el. komercijos svetaine. Informacijos apie tai, kaip sukurti naują svetainę ir susieti ją su kanalu, [ieškokite](#map-a-channel-to-a-site-in-site-builder) šio straipsnio skyriuje Susieti kanalą su svetaine svetainės generatoriaus skyriuje.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Kelių kalbų kanalas, turintis vieną lokalizuotą svetainės patirtį

Šiame scenarijuje vienas kanalas palaiko daugiau nei vieną kalbą. Todėl produktų pavadinimus, aprašus ir atributus galima lokalizuoti "Commerce Headquarters". Siekiant užtikrinti visišką lokalizuotą svetainės patirtį, rinkodaros turinį svetainėje galima lokalizuoti ir "Commerce" svetainių generatoriuje.

Šio scenarijaus apribojimas yra tas, kad vieną kanalą galima konfigūruoti tik su viena valiuta, vienu juridiniu subjektu ir vienu produktų ir kainų rinkinys. Ši konfigūracija tinka geriausiai šalims, turioms vieną valiutą ir kelias kalbas (pavyzdžiui, Kanadą, kuri turi anglų ir prancūzų kalbas), vieną juridinį subjektą ir vieną produktų ir kainų rinkinį.

Kiekviena kanalo kalba gali būti konfigūruota su savo domeno pavadinimu. Pavyzdžiui, domeną `www.adventure-works.ca` galima konfigūruoti Kanados anglų kalba, `www.adventure-works-fr.ca` o domeną galima konfigūruoti Kanados prancūzijos versijai. Kitaip skirtingas kanalo kalbas galima konfigūruoti viename domene, tada kiekvienai kalbai galima naudoti skirtingą maršrutą. Pavyzdžiui, domeną `www.adventure-works.ca` galima konfigūruoti Kanados anglų kalba, `www.adventure-works.ca/fr` o tada maršrutas gali būti naudojamas Kanados prancūzų versijai. [Geografinės](geo-detection-redirection.md) vietovės aptikimas taip pat gali būti įgalintas, kad pagal vartotojo vietą būtų automatiškai peradresuojamas į tinkamą svetainę.

Informacijos apie tai, kaip įgalinti klientus rankiniu būdu perjungti kalbas, [žr](#add-and-configure-the-site-picker-module). šio straipsnio skyriuje Įtraukti ir konfigūruoti svetainės parinkiklio modulį. Informacijos, kaip pritaikyti lokalizuotus puslapius ir fragmentus, žr. svetainės turinį, [kuriame yra keli kanalai ir kalbos](#manage-site-content-that-has-multiple-channels-and-languages) skyrius.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Kelių kalbų kanalas, kuriame turite skirtingas svetainės funkcijas pagal kalbą

Galite pasirinkti scenarijų, pagal kurį vienas kanalas palaiko daugiau nei vieną kalbą, bet kiekvienai kalbai atvaizduojamas visiškai skirtinga svetainės naudojimo patirtis. Rekomenduojamas šio scenarijaus vykdymo metodas yra naudoti [puslapių variantus](#implement-page-variants-for-each-language) vienoje svetainėje.

Kitas būdas yra sukurti naują el. komercijos svetainę kiekvienai svetainės generatoriaus kalbai ir tada susieti kiekvieną svetainę su vienu interneto kanalu ir kalba. Rezultatas bus vienas interneto kanalas, susietas su keliomis el. komercijos svetainėmis, po vieną kiekvienai kalbai. Šiam kelių svetainių metodui reikia papildomų valdymo išteklių, nes svetainės generatoriuje bus daugiau nei viena svetainė valdyti.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Keli kanalai (vienos kalbos ir (arba) kelių kalbų), kurie turi vieną lokalizuotą svetainės patirtį

Tam, kad svetainė būtų žinoma kaip prekės ženklas, gali reikėti kelių interneto kanalų vienam regionui, kad būtų galima palaikyti skirtingą valiutą, produktų rinkinį ir kiekvieno kanalo kainų rinkinį vienoje teritorijoje. Pavyzdžiui, Adventure Works svetainėje gali būti interneto kanalas Kanados rinkai, kuri turi kelias kalbas, JAV rinkos kanalą, kuriame yra viena kalba, ir kanalą Vokietijos rinkai, kuri turi vieną kalbą. Tokiu atveju kiekvienas interneto kanalas bus sukonfigūruotas konkrečiam regionui juridiniam subjektui ir gali turėti tą patį produktų rinkinį, kurį turi kiti kanalai, šių produktų subgrupę ar kitą produktų rinkinį. Kiekvienas kanalas turės savo kainas regiono valiuta, mokesčiais, nuolaidomis ir siuntimo būdais.

Tokiu atveju kiekviena rinka gali būti sukonfigūruota su savo domenų pavadinimais. Pavyzdžiui, domeną `www.adventure-works.com` galima konfigūruoti JAV rinkai, `www.adventure-works.de` o domeną galima konfigūruoti Vokietijos rinkai. Taip pat kiekvieną rinką galima sukonfigūruoti taip, kad būtų naudojamas skirtingas maršrutas. Pavyzdžiui, domeną `www.adventure-works.com` galima konfigūruoti JAV rinkai, o tada `www.adventure-works.com/de` maršrutas gali būti naudojamas Vokietijos rinkai. [Geografinius](geo-detection-redirection.md) aptikimus taip pat galima įgalinti, kad vartotojai būtų automatiškai nukreipti į tinkamą svetainę, remiantis jų regionu.

Taip pat galite norėti, kad jūsų svetainė pateiktų išplečiamąjį sąrašą, kuris leidžia vartotojams rankiniu būdu pereiti į konkrečią rinką. Norėdami gauti daugiau informacijos, žr. [šio straipsnio skyriuje Įtraukti ir konfigūruoti svetainės išrinkiklio](#add-and-configure-the-site-picker-module) modulį.

Informacijos, kaip konfigūruoti kelis kanalus vienoje svetainėje, [žr. el. komercijos svetainės skyriuje Konfigūruoti kelis kanalus](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Keli kanalai (vienos kalbos ir (arba) kelių kalbų), kurie kanalui turi skirtingą svetainės patirtį

Galbūt norėsite turėti kelis kanalus vienam prekės ženklui skirtinguose regionuose ir galbūt norėsite, kad kiekvienas regionas turėtų skirtingą svetainės patirtį. Yra du šio scenarijaus vykdymo metodai:

- Naudokite [puslapių variantus](#implement-page-variants-for-each-language).
- Sukonfigūruokite skirtingą svetainę kiekvienam interneto kanalui svetainės generatoriuje, tada susiekite kiekvieną svetainę su skirtingu interneto kanalu ir kalba. Šiam metodui reikia papildomų valdymo išteklių, nes bus daugiau nei viena svetainė, kuri bus valdoma svetainės generatoriuje.

## <a name="cross-channel-sharing"></a>Kryžminio kanalo bendras naudojimas

Kelių kanalų bendrinimo funkcija naudinga, kai keli vienos svetainės kanalai gali bendrinti turinį. Pavyzdžiui, mažmenininkas, turintis kelis prekės ženklus ir parduotuves, sugrupuotus pagal vieną svetainę, gali bendrinti turinį su kai kuriomis arba visomis parduotuvėmis. Bendrai naudojamas turinys gali apimti sąlygų ir sąlygų, mokėjimo sąlygų, siuntimo metodų ir dažnai užduodamų klausimų puslapius. Daugiau informacijos rasite parinktį Įgalinti [ir naudoti kryžminio kanalo bendrą naudojimą](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Susieti kanalą su svetaine svetainės generatoriuje

Yra keli metodai svetainėms kurti ir konfigūruoti, kad būtų galima naudoti įvairius interneto kanalus.

### <a name="create-a-new-site"></a>Sukursite naują vietą

Galite sukurti prekės ženklo naują svetainę svetainės generatoriuje, nueidami į " **Sites** " sąrašo puslapį ir pasirinkdami **Nauja svetainė**. Tada pasirodome naujos **svetainės** dialogo lange galite pasirinkti numatytąjį interneto kanalą ir svetainės kalbą, kaip parodyta šiame pavyzdyje.

![Kuriamas naujas kanalas svetainės generatoriuje.](media/channel-mapping-4.png)

Tokiu būdu sukurta svetainė bus tuščia ir nebus įtraukti svetainės puslapiai (pvz., pagrindinis puslapis, kategorijos puslapiai ir produkto puslapiai).

Dėl daugiau informacijos, žr. [Sukurti e-komercijos saitą](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Kurti naują svetainę naudojant svetainės kopijavimo operaciją

Užuot kūrę naują, tuščią, ankstesniame skyriuje apibūdintą svetainę, geriau būtų pradėti nuo vienos iš paleidininko svetainių, kurios pateiktos "Commerce" modulių bibliotekoje, pavyzdžiui, "Fabrikam" arba "Adventure Works" svetainės, kopijos.

Norėdami kopijuoti esamą svetainę, eikite į svetainės **generatoriaus "Sites** " sąrašo puslapį ir pasirinkite Kopijuoti **svetainę**. Tada rodomame **dialogo lange** Kopijuoti svetainę galite pasirinkti šaltinį ir nurodyti paskirties vietos pavadinimą.

Šiuo metu dar negalite pasirinkti numatytojo interneto kanalo ir svetainės kalbos. Tačiau, baigę svetainės kopijavimo operaciją, galite konfigūruoti šias ypatybes. Kai pirmą kartą pasirenkate svetainę **svetainių** sąrašo puslapyje svetainės generatoriuje, **atliekant** nustatymą pasirodys svetainės dialogo langas, kuriame galėsite pasirinkti numatytąjį kanalą ir kalbą.

Daugiau informacijos apie svetainės kopijavimo operaciją ieškokite el [. komercijos svetainės kopijavimas](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Valdyti esamą svetainės kanalą

Kai svetainė sukonfigūruota naudojant kanalą, **\>** galite valdyti ir atnaujinti kanalą pasirinktoje svetainės generatoriaus svetainėje, prie svetainės nustatymų kanalų, kaip parodyta šiame pavyzdyje.

![Kanalo susiejimo svetainės generatoriuje valdymas.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Palaiko kelias vieno nuomininko svetaines

Viename nuomininke gali būti daug prekės ženklo teritorijų. Šiame pavyzdyje vaizduojamos trys skirtingos prekės ženklo svetainės (Adventure Works, Adventure Works Business ir Fabrikam), kiekviena iš jų yra susietas su skirtingu interneto kanalu.

![Svetainės sąrašas svetainės generatoriuje.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Vieno domeno pavadinimo konfigūravimas su kelių svetainių maršrutais

Vieną domeno pavadinimą galima naudoti kelioms svetainėms, tada maršrutai gali būti naudojami svetainėms arba kalboms atskirti. Pavyzdžiui, domenas `www.mycompany.com` sukonfigūruotas dviem skirtingoms el. komercijos svetainėms: "Fabrikam" ir "Adventure Works". Šiuo atveju, numatytasis maršrutas (`www.mycompany.com` taip pat vadinamas tuščiu maršrutu) gali būti naudojamas Fabrikam svetainei, o kitas maršrutas (pvz., `www.mycompany.com/adventureworks`) gali būti naudojamas Adventure Works svetainei. Kita pasirinktis – vietoj numatytojo Fabrikam site maršruto naudoti pasirinktinį maršrutą (`www.mycompany.com/fabrikam` pvz.,).

Taip pat kiekvienai svetainei galima naudoti skirtingą domeno pavadinimą (pvz., `www.adventure-works.com` ir `www.fabrikam.com`). Maršrutai gali būti naudojami skirtingoms kalboms ar regionams (pavyzdžiui, `www.adventure-works.com/fr-ca` Kanados prancūzų).

## <a name="configure-multiple-languages-on-a-site"></a>Kelių kalbų konfigūravimas svetainėje

Svetainės parametrų kanaluose galima konfigūruoti el. komercijos svetainės kalbas svetainės **generatoriuje \>**. Šiame pavyzdyje kiekviena kalba konfigūruota naudojant maršruto lokalę, kad kiekviena kalba turėtų unikalų URL.

![Svetainėje sukonfigūruotos kelios kalbos.](media/channel-mapping-10.png)

Norėdami įtraukti naują kanalo kalbą, eikite į svetainės **nustatymų \> kanalus** ir pasirinkite kanalo saitą. Dešinėje pasiroda esančioje srityje pasirinkite Įtraukti lokalę **,** kad pasirinktumėte kanalą ir lokalę, kurią norite įtraukti. Tada nurodykite pasirinkto kanalo maršrutą.

### <a name="add-and-configure-the-site-picker-module"></a>Įtraukti ir konfigūruoti svetainės parinkiklio modulį

Sukonfigūrę svetainę su keliomis kalbomis arba kanalais, galite norėti į svetainės puslapio antraštę įtraukti kalbos išrinkiklį, kad vartotojai galėtų rankiniu būdu pasirinkti savo kalbą arba šalį. Modulio bibliotekos [antraštės](author-header-module.md) modulis turi integruotą vartotojų palaikymą, kad vartotojai galėtų pasirinkti kalbą naudodami svetainės parinkiklio [modulį](site-selector.md). Svetainės išrinkiklio modulį galima įtraukti į antraštės fragmento antraštės modulį.

Daugiau informacijos, kaip pridėti ir konfigūruoti svetainės išrinkiklio modulį, žr. vietos [išrinkiklio modulį](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Taikyti puslapių variantus kiekviena kalba

Šiame scenarijuje yra tik vienas kanalas, tačiau yra kelios kalbos. Sukurdami puslapio variantą, galite keisti puslapio išvaizdą pagal pasirinktą kalbą. Tada į variantą galėsite įtraukti lokalizuotą turinį.

Kai svetainės generatoriuje atidarysite puslapį, o viršutiniame dešiniajame lange pasirinksite saitą, kuriame rodomas dabartinis kanalas ir kalba, atsiras kanalas ir kalbos parinkiklis, kaip parodyta toliau pateiktame pavyzdyje. Jei norite nepaisyti dabartinės kalbos puslapio, pasirinkite kitą vietą ir pasirinkite **Keisti**. Kanalą taip pat galite pakeisti, jei valdote [svetainę, turintį kelis kanalus ir kalbas](#manage-site-content-that has-multiple-channels-and-languages).

![Svetainės generatoriaus puslapio kalbos keitimas.](media/channel-mapping-14.png)

Jei pasirinkto puslapio ar fragmento variantas dar nesukurtas, gausite perspėjimo pranešimą, kaip parodyta toliau pateiktame pavyzdyje. Šiuo atveju pranešimo tekste **pasirinkite saitą** Kurti puslapio variantą. Pasirodęs dialogo langas pateikia pasirinktis, kurios leidžia arba pradėti nuo esamo varianto kopijos, arba iš šablono sukurti prekės ženklo naują puslapį.

![Raginti kurti puslapio variantą svetainės generatoriuje](media/channel-mapping-16.png)

Jei nesukursite varianto, pradinis puslapis bus atvaizduotas ir rodanti atitinkamą modulio eilučių kalbą ir produkto informaciją iš "Commerce Headquarters". Tačiau jei tekstas, pavyzdžiui, puslapio pavadinimas ar kitas rinkodaros turinys, nurodytas tiesiogiai numatytuose puslapių moduliuose, to teksto eilutės liks originalia kalba.

Užuot rankiniu būdu kurę kiekvieną puslapį ir fragmentą, galite eksportuoti kiekvieną puslapį ir fragmentą į XML lokalizavimo mainų failo formatą (XLIFF), kurį bus galima siųsti lokalizavimui. Kai kiekvienas XLIFF yra lokalizuotas, jį galima importuoti kaip lokalizuotą puslapio variantą. Norėdami eksportuoti XLIFF failą iš svetainės generatoriaus puslapio ar fragmento arba importuoti XLIFF failą į puslapį ar fragmentą, **komandų** juostoje pasirinkite Lokalizavimas. Tada pasirinkite Arba **Export XLIFF,** arba **Import XLIFF**, kaip parodyta toliau pateiktame pavyzdyje.

![Importuojamas arba eksportuojamas puslapis ar fragmentas XLIFF formatu.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Tvarkyti svetainės turinį, kuriame yra keli kanalai ir kalbos

Svetainė, kurioje yra keli kanalai ir (arba) kalbos, saugomas unikalus kiekvieno puslapio variantas ir kiekvieno kanalo bei kalbos derinio fragmentas. Toks veikimo būdas leidžia puslapių variantams turėti lokalizuotus duomenis, bet taip pat suteikia galimybę lanksčiau pakeisti konkretaus varianto puslapio išvaizdą.

Informacijos, kaip dirbti su puslapio variantais, ieškokite šio [straipsnio skyriuje Kiekvienos kalbos](#implement-page-variants-for-each-language) puslapių variantai.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Kelių kanalų konfigūravimas el. komercijos svetainėje

Kanalus į el. komercijos svetainę galite įtraukti svetainės generatoriuje, pereidami prie **svetainės nustatymų kanalų \>** ir pasirinkdami **Įtraukti kanalą**. Tada parodę **dialogo langą Įtraukti** kanalą galite pasirinkti interneto kanalą ir numatytąją lokalę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Interneto kanalo nustatymas](channel-setup-online.md)

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Geografinės srities aptikimo ir peradresavimo nustatymas](geo-detection-redirection.md)

[Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas](cross-channel-sharing.md)

[El. prekybos svetainės kūrimas](create-ecommerce-site.md)

[El. prekybos svetainės kopijavimas](copy-ecommerce-site.md)

[Svetainės išrinkiklio modulis](site-selector.md)
