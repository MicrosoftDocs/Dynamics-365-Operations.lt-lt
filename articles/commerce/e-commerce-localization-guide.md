---
title: Dynamics 365 Commerce El. komercijos lokalizavimo vadovas
description: Šiame straipsnyje aprašoma, kaip lokalizuoti el Microsoft Dynamics 365 Commerce . komercijos svetainę į papildomas kalbas ir konfigūruoti svetainę, kad būtų palaikomi keli kanalai.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873389"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce El. komercijos lokalizavimo vadovas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma Microsoft Dynamics 365 Commerce, kaip lokalizuoti el. komercijos svetainę į papildomas kalbas ir konfigūruoti svetainę, kad būtų palaikomi keli kanalai, ir taip pat apima su procesu susijusias sąvokas ir terminologiją.

El. komercijos galimybės sukurtos siekiant įgalinti patirtį internete, kuri gali būti konkrečiose šalyse ir kalbose Dynamics 365 Commerce, tačiau tuo pačiu metu leidžia maksimalią pakartotinio šablonų, puslapių, turinio ir laikmenų naudojimą. Be to, galite sukurti pagrindinę svetaines, o tada išplėsti naujas rinkas, sudedant papildomų šalių ir kalbų palaikymą laikui bėgant.

## <a name="definitions"></a>Sąvokos

**Lokalė, vietos identifikatorius**: lokalė (taip pat vadinama lokalės identifikatoriumi) apibrėžia kalbą, susietą su šalimi arba regionu. Pavyzdžiui, lokalės identifikatorius "fr-ca" yra susietas su Kanados prancūzų kalba.

**Pagrindinė kalba**: kalba, kuria kuriate svetainės turinį prieš eksportuojant lokalizavimui.

**Kanalas, interneto parduotuvė**: kanalas (taip pat vadinamas interneto parduotuve) apibrėžia mokėjimo būdus, kainų grupes, produktų hierarchijas, asortimentus ir produktus interneto el. komercijos parduotuvėsfrontui.

## <a name="concepts"></a>Koncepcijos

### <a name="url-driven-experience"></a>URL valdoma patirtis

Dynamics 365 Commerce El. komercijos svetainės suteikia unikalią rinkos ir lokalizuotą patirtį klientams, naudojant kanalus ir vietos identifikatorius. Kanalai nustato unikalius rinkos produktus, kategorijas, valiutas ir mokėjimo būdus, o vietos identifikatoriai lemia turinio, kurį mato klientai, kalbą. El. komercijos svetainė naudoja URL, siekiant atskirti rinkos ir lokalizuotą patirtį. Šių unikalių kanalo ir vietos patirties svetainės URL apibrėžti svetainei svetainės **parametrų puslapyje \> svetainės** generatoriaus Dynamics 365 Commerce kanalų puslapyje.

Svetainės generatoriuje URL yra domeno ir maršruto derinys, nurodantis unikalaus kanalo ir vietos derinio įvesties tašką. Toliau pateiktame pavyzdyje fiktyvi interneto parduotuvė vadinama Fabrikam Inc. Apibrėžia keturias unikalias kanalo ir vietos kombinacijas bei kiekvieną jų kombinaciją schema su unikaliu URL, kuris naudojamas turiniui su klientais.

| Domenas                     |  Kelias      | Kanalas       |   Lokalė     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam išplėstinė interneto parduotuvė | lt  |
| `https://fabrikam.com` | "/es"    | Fabrikam išplėstinė interneto parduotuvė | es     |
| `https://fabrikam.ca`  | /      | "Contoso" internetinė parduotuvė    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | "Contoso" internetinė parduotuvė    | en-ca  |

#### <a name="domain"></a>Domenas

Domenai nustatomi nustatant savo el. komercijos Microsoft Dynamics svetainę ciklo tarnybose (LCS). Su atidarę savo el. komercijos aplinką, galite įtraukti daugiau domenų atidarydami aptarnavimo užklausą. Daugiau informacijos apie tai, kaip nustatyti domenus savo el. komercijos svetainei, rasite [domenuose.Dynamics 365 Commerce](domains-commerce.md)

#### <a name="path"></a>Kelias

- Kelias yra daug eilučių, kurios kartu su domenu yra susietos su unikaliu kanalo ir vietos deriniu. Ankstesniame pavyzdyje eilutė, kuri naudojama kaip maršrutas, atitinka vietos identifikatorių, su kuriuo susietas maršrutas. Tačiau galite naudoti kitą būdą.
- Kanalo ir vietos derinį galima susieti su domenu ir tuščiu maršrutu ("/"). Ankstesniame pavyzdyje klientai `https://fabrikam.ca/`, kurie lankosi, gaus Kanados prancūzijos rinkos produktus ir asortimentus.
- "Commerce" svetainių generatorius neleidžia kurti domeno ir maršruto kombinacijų dublikatų. Tačiau galite susieti kanalo ir vietos dublikatų derinius su skirtingu domeno ir maršruto deriniu.

#### <a name="channel"></a>Kanalas

- Kanalai (taip pat vadinami interneto parduotuvėmis) apibrėžia mokėjimo metodus, kainų grupes, produktų hierarchijas, asortimentus ir produktus interneto el. komercijos parduotuvėse.
- Kanalai apibrėžiami, konfigūruojami ir publikuojami Dynamics 365 Commerce būstinėje.
- Svetainės generatorius gali aptikti interneto parduotuves, kurios sukonfigūruotos "Commerce Headquarters" ir kurias galima susieti su svetaine.

Daugiau informacijos apie kanalus ieškokite Kanalų [peržiūra](channels-overview.md). Daugiau informacijos apie tai, kaip nustatyti interneto kanalą, ieškokite [interneto kanalo nustatyti](channel-setup-online.md).

#### <a name="locale"></a>Lokalė

- Lokalė yra faktinis identifikatorius, naudojamas, kai atimsite XML lokalizavimo mainų failo formato (XLIFF) failus, naudojamus lokalizavimui. Nustatomos ir publikuojamas kiekvieno "Commerce Headquarters" kanalo vietos. Informacijos, kaip konfigūruoti kalbas ir kanalus svetainės generatoriuje, ieškokite kitame skyriuje.
- Tą pačią vietą galima susieti su keliais kanalais. Tokiu būdu bendra kalba gali būti siūloma keliose rinkose.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Jūsų el. komercijos svetainės kalbų ir kanalų konfigūravimas

Jei ne, Dynamics 365 Commerce visos el. komercijos svetainės sukonfigūruotos naudoti vieną interneto kanalą ir vieną kalbą, nepaisant to, ar pradedate nuo Fabrikam demonstracinės svetainės, ar nuo pradžių kuriate naują svetainę.

Šioje konfigūracijoje klientai ir partneriai paprastai kuria visą turtą, kuris bus naudojamas įvairiose šalyse ir kalbose. Šis turtas apima šablonus, puslapius, fragmentus, turinį ir laikmenas. Visas svetainės turinys kuriamas pirmą jūsų svetainei pasirinkta kalba arba jei naudojate Fabrikam demonstracinę svetainę, svetainės turinys bus sukurtas anglų kalba.

![Į lauką neįeis Dynamics 365 Commerce el. komercijos svetainė](media/loc-guide-1.png)

> [!NOTE]
> Galite konfigūruoti Fabrikam demonstracinę svetainę papildoma kalba, kad turinio kūrimas būtų galimas ta kalba. Informacijos, kaip įtraukti naują kalbą į svetainę ir kanalą, [ieškokite](#configure-an-additional-language-for-your-site) toliau šiame straipsnyje skyriuje Konfigūruoti papildomą savo svetainės kalbą.

Tačiau turinio valdymo sistema (CMS) Dynamics 365 Commerce ir puslapių modelis el. komercijos svetainėms sukurti siekiant leisti išplėtimą į naujas rinkas ir vietas. Todėl, per vieną el. prekybos svetainę, galima valdyti interneto parduotuvės, kuri apima kelias rinkas ir kalbas, turtą.

![Dynamics 365 Commerce El. komercijos svetainė, kuri apima kelias rinkas ir kalbas](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Sukonfigūruokite papildomą svetainės kalbą

Naujos el. komercijos svetainės kalbos konfigūravimo procesas turi tris žingsnius.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>1 veiksmas: įtraukite kalbą į kanalą (interneto parduotuvę) "Commerce Headquarters"

1. "Commerce Headquarters" eikite į kanalą, į kurį norite įtraukti naują kalbą. Norėdami rasti kanalų, kuriuos sukonfigūravote "Commerce Headquarters", sąrašą, eikite į mažmeninės **prekybos ir komercijos kanalų \> interneto \> parduotuves**.
1. Atidarykite interneto parduotuvę, kuri susietas su jūsų svetaine, pasirinkdami jos mažmeninės **prekybos kanalo ID vertę**. Galite patikrinti interneto **parduotuvę**, kuri susietas su jūsų svetaine, atidarydami kanalų svetainės parametrų puslapį "Commerce" svetainių generatoriuje **ir ieškodami interneto parduotuvės pavadinimo kanalų stulpelyje**. 
1. „FastTab“ elemente **Kalbos** pasirinkite **Įtraukti**. **Lauke Kalba** pasirinkite naujos kalbos vietos kodą. Tada pasirinkite **Įrašyti**.
1. Pereikite į " **Retail" ir "Commerce \> Retail" ir "Commerce IT \> Distribution"** grafiką ir vykdykite **1070 kanalo konfigūravimo užduotį**. Baigę vykdyti užduotį, galite pereiti prie 2 veiksmo ir pridėti kalbą prie svetainės generatoriaus kanalo.

!["Commerce Headquarters" internetinės parduotuvės "FastTab" kalbomis](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>2 žingsnis: kalbos įtraukimas į kanalą svetainės generatoriuje

Norėdami į kanalą įtraukti kalbą svetainės generatoriuje, atlikite šiuos veiksmus.

1. Commerce svetainės generatoriuje atidarykite savo svetainę ir atidarykite puslapį Kanalai **svetainės** parametruose.
1. Pasirinkite kanalo, į kurį norite įtraukti kalbą, pavadinimą.
1. Dešiniajame lange pasirinkite **Įtraukti lokalę**.
1. Dialogo lange **Įtraukti vietą pasirinkite** vietos kalbą, **kurią** anksčiau pridėjote prie "Commerce Headquarters" kanalo.
1. Pasirinkite domeną ir kelią, kuriuos klientai nurodys peržiūrėti jūsų svetainę šiame kanale ir kalba.
1. Jei norite, kad kalba būtų numatytoji svetainės generatoriaus puslapių ir fragmentų peržiūros, kūrimo ir atnaujinimo kalba, **pažymėkite žymės langelį Naudoti kaip numatytąją kūrimo kanalo** kalbą. 
    > [!NOTE]
    > Šis parametras veikia tik svetainės generatorių. Tai neturi įtakos jūsų klientams paskelbtiems vartotojams.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti ir publikuoti**.

#### <a name="step-3-localize-your-site-content"></a>3 žingsnis: svetainės turinio lokalizuoti

Kai grįžtate į " **Commerce"** svetainių generatoriaus puslapių rodinį, kanale, o viršutiniame dešiniajame vietos parinkinyje bus galima naudoti naują kalbą. Dabar galite kurti lokalizuotas puslapių versijas savo bazine kalba.

Toliau šiame straipsnyje skyriuje Lokalizuoti el. komercijos [svetainės](#localize-e-commerce-site-content) turinį taikomas jūsų puslapių ir fragmentų turinio lokalizavimo procesas.

### <a name="configure-a-new-channel-for-your-site"></a>Konfigūruokite naują savo svetainės kanalą

Dynamics 365 Commerce El. "Commerce Sites" gali turėti patirties, kuri apibrėžiama keliuose interneto kanaluose, kurie sukonfigūruoti "Commerce Headquarters". Svetainė naudoja kelis kanalus, kad parodytų klientams unikalią mokėjimo metodų, kainų grupių, produktų hierarchijų, asortimentų ir produktų rinkinio konfigūraciją. Kanalas paprastai naudojamas norint konfigūruoti šias dimensijas, kad jos atitiktų su atskiromis šalimis siejamos patirties reikalavimus ir nuostatas. Tačiau šis būdas yra verslo sprendimas, kurį atlieka klientas. Tai nėra reikalavimas.

Su kanalo (interneto parduotuvės) nustatymu susijusios būtinosios sąlygos ir užduotys viršija šio dokumento aprėptį. Daugiau informacijos apie tai, kaip nustatyti interneto kanalą "Commerce Headquarters", ieškokite kanalo [nustatymo pagrindai.](channels-overview.md#channel-setup-basics) Informacijos apie interneto kanalams aprašytus veiksmus ir reikalavimus ieškokite [interneto kanalo nustatyti](channel-setup-online.md).

Norėdami įtraukti kanalą į savo svetainę svetainės generatoriuje, atlikite šiuos veiksmus.

1. Komercijos svetainės generatoriuje eikite į svetainės **parametrų kanalus \>**. 
1. Pasirinkite **Įtraukti kanalą**.
1. Dalyje Kanalas **pasirinkite kanalą**, kurį **norite įtraukti**, dialogo lange Įtraukti kanalą. 
    > [!NOTE]
    > Galite įtraukti tik kanalus, kurie dar nebuvo įtraukti į jūsų svetainę.
1. Pasirinkti numatytąją kanalo lokalę. Jei į kanalą įtrauksite naujų kalbų, galėsite keisti numatytąją kalbą į vieną iš jų.
1. Nurodykite domeną ir kelią, kurie sudaro URL, kuris šiam kanalo ir kalbos deriniui tinka turiniui ir patirčiai.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti ir publikuoti**.

## <a name="localize-e-commerce-site-content"></a>Lokalizuoti el. komercijos svetainės turinį

### <a name="xliff-basics"></a>XLIFF pagrindai

XLIFF yra standartinis pramonės failo formatas, skirtas lokalizuojamame turinyje perduoti tarp turinio valdymo įrankių. "Commerce" svetainės generatorius naudoja XLIFF failo formatą puslapio, fragmento ir vaizdo metaduomenų turiniui eksportuoti, kad būtų galima lokalizuoti ir importuoti iš naujo.

Microsoft Dynamics klientai paprastai dirba su trečiosios šalies lokalizavimo tiekėjais, tokiais Translated.com [, kad išverstų savo XLIFF failus į jiems reikalingas kalbas](https://translated.com/welcome).

### <a name="localize-assets-in-site-builder"></a>Lokalizuoti turtą svetainės generatoriuje

Toliau nurodytas el. komercijos svetainės turtas gali būti lokalizuojamas svetainės generatoriuje:

- Puslapiai
- Fragmentai
- Medijų turtas
- Moduliai

Visi nauji puslapiai, fragmentai ir laikmenų turtas sukuriami kanalo ir kalbos, šiuo metu pasirinktos kanalo ir vietos parinkikliuose, kontekste. Ši kalba dažniausiai yra jūsų pagrindinė kalba, jei nekonfigūravote papildomų kalbų ar kanalų. Svetainėse, kuriose sukonfigūruoti keli kanalai ir kalbos, "pagrindinę kalbą" **apibrėžia** kanalas ir lokalė, kurią nustatėte kaip numatytąją svetainės parametrų puslapyje Kanalai.

Puslapių, fragmentų ir laikmenų turto lokalizavimo veiksmai yra panašūs. Išimtys ir skirtumai nurodyti tolesniuose skyriuose. Tačiau skiriasi modulio lokalizavimo veiksmų turinys. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr.](#localize-modules) skyrių Lokalizuoti modulius.

#### <a name="step-1-export-an-xliff-file"></a>1 žingsnis: XLIFF failo eksportavimas

Norėdami eksportuoti XLIFF failą, skirtas puslapiui, fragmentui arba vaizdui svetainės generatoriuje, atlikite šiuos veiksmus.

1. Atidarykite turtą, kuriam norite eksportuoti pagrindinės kalbos turinį, kad būtų galima jį lokalizuoti.
1. Komandų juostoje pasirinkite Lokalizavimo **eksportavimo \> XLIFF**.
    > [!NOTE]
    > Lokalizavimo **pasirinktis** matoma tik tada, kai turto būsena **Redaguoti**.

XLIFF failas, pavadintas **\<assetname\>.xlf**, bus atsisiųstas į jūsų naršyklės atsisiuntimo aplanką. Šis XLIFF failas yra konkretus turtui, kurį lokalizuojate. Eksportuotite XLIFF failą kiekvienam turtui, kurį norite lokalizuoti.

#### <a name="step-2-localize-the-xliff-file"></a>2 žingsnis: XLIFF failo lokalizuoti

Daugeliu atvejų, norėdami išversti XLIFF failus, turėsite dirbti su lokalizavimo tiekėju. Tačiau jei turto lokalizuojate viduje ar tik norite patikrinti lokalizavimo procesą, XLIFF faile turite atlikti šiuos pakeitimus:

- Įtraukite tikslinį kalbos atributą į /xliff/failo elementą ir nustatykite vertę kaip kalbos, į kurią lokalizuojate, vietos identifikatorių. 
    > [!NOTE]
    > Šis lokalės identifikatorius turi atitikti vietos parametrų puslapio **Kanalai** vietos identifikatorių.
- Kiekvienam /šaltinio elementui pridėkite tikslinį elementą to paties elemento dukterinį elementą, kur teksto vertė yra to šaltinio elemento turinio lokalizuota versija.

Daugiau informacijos apie XLIFF rinkmenų schemą ieškokite [XLIFF 1.2 specifikacijoje](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Norėdami lokalizuoti turtą keliomis kalbomis, turite kiekvienai iš šių kalbų sukurti lokalizuotą XLIFF failą.

#### <a name="step-3-import-the-localized-xliff-file"></a>3 žingsnis: lokalizuoto XLIFF failo importavimas

Norėdami importuoti XLIFF failą turtui, atlikite šiuos veiksmus.

1. Commerce site builder atidarykite turtą, kuriam norite importuoti XLIFF failą.
1. Kanalo ir vietos parinkiklis viršutinėje dešinėje pasirinkite kanalą ir kalbą, į kurią importuojate lokalizuotą turinį.
1. Komandų juostoje pasirinkite Lokalizavimo **importavimo \> XLIFF**. Tada naršykite ir pasirinkite pasirinkto turto ir kalbos lokalizuotą XLIFF failą.

Po to, kai XLIFF failas sėkmingai importuotas, sukuriamas puslapio, fragmento ar turto variantas. Nuo tada visi atlikti lokalizuoto varianto pakeitimai turės įtakos tik tam variantui. Jie neturės įtakos baziniam turtui, iš kur buvo išvestas variantas. Taip pat, pagrindinio turto pakeitimai neturės įtakos to turto variantui. 

Tačiau puslapių atveju galite atlikti įvairių variantų pakeitimus, modifikuodami šabloną ar maketą, su kuriuo tie puslapiai susieti. Taip pat, fragmento pakeitimai turės įtakos visiems puslapiams, kurie priklauso nuo to varianto.

### <a name="images"></a>Vaizdai

Vaizdai gali būti atvaizduoti puslapyje arba modulio variante tik tada, jei su šiais paveikslėliais susiję turinio metaduomenys yra lokalizuoti. Šiuo metu šie publikavimo laikmenos turto metaduomenys yra lokalizuojami:

- Alternatyvusis tekstas
- Aprašymas
- Pavadinimas

Šiuo metu negalite lokalizuoti skaitmeninio turto, pvz., vaizdo ar vaizdo įrašo, dvejetainio. Produkto Dynamics 365 Commerce komanda šiuo metu naudoja šį pajėgumą.

### <a name="localize-modules"></a>Lokalizuoti modulius

Eilutės, atvaizduotos kaip paties modulio dalis (pvz., "Ankstesnis" ir "Paskesnis" karuso modulyje) yra lokalizuojamos atskirai nuo modulio turinio. Instrukcijų ieškokite Modulyje [Lokalizuoti](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Puslapio modelio žodynas](page-elements-overview.md)

[Kryžminio kanalo bendras naudojimas](cross-channel-sharing.md)

[Lokalizuoti modulį](e-commerce-extensibility/localize-module.md)

[Modulio apibrėžties failas](e-commerce-extensibility/module-definition-file.md)

[„Commerce“ plėtinių išteklių ir žymų failų lokalizavimas](dev-itpro/extension-resource-localization.md)

[Globalizuoti modulius naudojant CultureInfoFormatter klasę](e-commerce-extensibility/globalize-modules.md)

[Programos parametrai: temos](e-commerce-extensibility/app-settings.md#themes-section)
