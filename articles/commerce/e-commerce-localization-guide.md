---
title: Dynamics 365 Commerce elektroninės prekybos lokalizavimo vadovas
description: Šioje temoje aprašoma, kaip lokalizuoti Microsoft Dynamics 365 Commerce el. prekybos svetainę į papildomas kalbas ir sukonfigūruoti svetainę, kad ji palaikytų kelis kanalus.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661506"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce elektroninės prekybos lokalizavimo vadovas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip lokalizuoti Microsoft Dynamics 365 Commerce elektroninės prekybos svetainę į papildomas kalbas ir sukonfigūruoti svetainę, kad palaikytų kelis kanalus, taip pat apima sąvokas ir terminologiją, susijusią su procesu.

Elektroninės prekybos galimybės Dynamics 365 Commerce sukurtos taip, kad būtų galima naudotis internetinėmis funkcijomis, kurios gali būti pritaikytos konkrečioms šalims ir kalboms, tačiau tuo pačiu metu leidžiančios maksimaliai pakartotinai naudoti šablonus, puslapius, turinį ir laikmenas. Taip pat galite sukurti pagrindinę svetainę ir tada išplėsti į naujas rinkas, laikui bėgant pridėdami paramą papildomoms šalims ir kalboms.

## <a name="definitions"></a>Sąvokos

**Lokalė, lokalės identifikatorius**: lokalė (taip pat žinoma kaip lokalės identifikatorius) apibrėžia kalbą, susietą su šalimi ar regionu. Pavyzdžiui, lokalės identifikatorius "fr-ca" yra susietas su Kanados prancūzų kalba.

**Pagrindinė kalba**: kalba, kuria kuriate svetainės turinį prieš eksportuodami jį lokalizacijai.

**Kanalas, internetinė parduotuvė**: kanalas (taip pat žinomas kaip internetinė parduotuvė) apibrėžia mokėjimo būdus, kainų grupes, produktų hierarchijas, asortimentus ir produktus internetinei elektroninės prekybos parduotuvei.

## <a name="concepts"></a>Koncepcijos

### <a name="url-driven-experience"></a>URL pagrįsta patirtis

Dynamics 365 Commerce elektroninės prekybos svetainės teikia klientams unikalią paklausią ir lokalizuotą patirtį per kanalus ir lokalės identifikatorius. Kanalai apibrėžia unikalius rinkos produktus, kategorijas, valiutas ir mokėjimo būdus, o lokalės identifikatoriai nustato klientų matomo turinio kalbą. Elektroninės prekybos svetainė naudoja URL, kad atskirtų paklausią ir lokalizuotą patirtį. Šių unikalių kanalų ir lokalių funkcijų svetainės URL apibrėžiami svetainės **parametrų \> kanalų** puslapyje svetainės daryklėje Dynamics 365 Commerce.

Svetainės daryklėje URL yra domeno ir maršruto derinys, apibrėžiantis unikalaus kanalo ir lokalės derinio įvedimo tašką. Toliau pateiktame pavyzdyje fiktyvi internetinė parduotuvė "Fabrikam Inc." apibrėžia keturis unikalius kanalo ir lokalės derinius ir susieja kiekvieną derinį su unikaliu URL, kuris teikia turinį klientams.

| Domenas                     |  Kelias      | Kanalas       |   Lokalė     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam išplėstinė internetinė parduotuvė | lt  |
| `https://fabrikam.com` | /es    | Fabrikam išplėstinė internetinė parduotuvė | es     |
| `https://fabrikam.ca`  | /      | Contoso internetinė parduotuvė    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso internetinė parduotuvė    | en-ca  |

#### <a name="domain"></a>Domenas

Domenai nustatomi, kai nustatote savo el. prekybos svetainę Microsoft Dynamics "Lifecycle Services" (LCS). Parengę el. prekybos aplinką, galite pridėti daugiau domenų atidarę paslaugos užklausą. Daugiau informacijos apie tai, kaip nustatyti el. prekybos svetainės domenus, ieškokite [Domains in Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Kelias

- Kelias yra savavališka eilutė, kuri kartu su domenu susiejama su unikaliu kanalo ir lokalės deriniu. Ankstesniame pavyzdyje eilutė, naudojama kaip kelias, atitinka lokalės identifikatorių, su kuriuo susietas kelias. Tačiau galite naudoti kitokį požiūrį.
- Kanalo ir lokalės derinį galima susieti su domenu ir tuščiu keliu ("/"). Ankstesniame pavyzdyje apsilankę `https://fabrikam.ca/` klientai kanados prancūzų kalba gaus kanados rinkai skirtus produktus ir asortimentus.
- "Commerce" svetainių daryklė neleidžia kurti pasikartojančių domeno ir maršruto derinių. Tačiau galite susieti pasikartojančius kanalo ir lokalės derinius su kitu domeno ir maršruto deriniu.

#### <a name="channel"></a>Kanalas

- Kanalai (taip pat žinomi kaip internetinės parduotuvės) apibrėžia internetinės elektroninės prekybos parduotuvės mokėjimo būdus, kainų grupes, produktų hierarchijas, asortimentus ir produktus.
- Kanalai apibrėžiami, konfigūruojami ir publikuojami būstinėje Dynamics 365 Commerce.
- Svetainių kūrėjas gali aptikti internetines parduotuves, kurios buvo sukonfigūruotos "Commerce" būstinėje ir kurias galima susieti su svetaine.

Daugiau informacijos apie kanalus ieškokite [Channels overview](channels-overview.md). Daugiau informacijos apie tai, kaip nustatyti internetinį kanalą, ieškokite [Set up a online channel](channel-setup-online.md).

#### <a name="locale"></a>Lokalė

- Lokalė yra faktinis identifikatorius, naudojamas perduodant XML lokalizacijos mainų failo formato (XLIFF) failus lokalizacijai. Vietovės apibrėžiamos ir skelbiamos kiekvienam kanalui "Commerce" būstinėje. Informacijos apie tai, kaip konfigūruoti kalbas ir kanalus svetainės daryklėje, ieškokite kitame skyriuje.
- Tą pačią lokalę galima susieti su keliais kanalais. Tokiu būdu bendra kalba gali būti siūloma keliose rinkose.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>El. prekybos svetainės kalbų ir kanalų konfigūravimas

Iš dėžutės visos Dynamics 365 Commerce el. prekybos svetainės sukonfigūruotos naudoti vieną internetinį kanalą ir vieną kalbą, neatsižvelgiant į tai, ar pradedate nuo "Fabrikam" demonstracinės svetainės, ar kuriate naują svetainę nuo nulio.

Šioje konfigūracijoje klientai ir partneriai paprastai kuria visą turtą, kuris bus naudojamas įvairiose šalyse ir kalbose. Šie ištekliai apima šablonus, puslapius, fragmentus, turinį ir laikmeną. Visas svetainės turinys yra sukurtas pirmąja kalba, kurią pasirinkote savo svetainei, arba jei naudojate "Fabrikam" demonstracinę svetainę, svetainės turinys bus sukurtas anglų kalba.

![Iš langelio Dynamics 365 Commerce el. prekybos svetainės](media/loc-guide-1.png)

> [!NOTE]
> Fabrikam demonstracinę svetainę galite sukonfigūruoti papildomai kalbai, kad turinio kūrimą būtų galima atlikti ta kalba. Informacijos apie tai, kaip įtraukti naują kalbą į svetainę ir kanalą, ieškokite [svetainės skyriaus konfigūravimas papildoma kalba](#configure-an-additional-language-for-your-site) vėliau šioje temoje.

Tačiau elektroninės prekybos svetainių turinio valdymo sistema (TVS) ir puslapių Dynamics 365 Commerce modelis buvo sukurti taip, kad būtų galima plėstis į naujas rinkas ir vietoves. Todėl per vieną elektroninės prekybos svetainę galite valdyti internetinės parduotuvės, apimančios kelias rinkas ir kalbas, turtą.

![Dynamics 365 Commerce Elektroninės prekybos svetainė, apimanti kelias rinkas ir kalbas](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Papildomos svetainės kalbos konfigūravimas

Naujos el. prekybos svetainės kalbos konfigūravimo procesas turi tris veiksmus.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>1 veiksmas: kalbos įtraukimas į kanalą (internetinę parduotuvę) "Commerce" būstinėje

1. "Commerce" būstinėje eikite į kanalą, į kurį norite įtraukti naują kalbą. Norėdami rasti kanalų, kuriuos sukonfigūravote "Commerce Headquarters", sąrašą, eikite į mažmeninės **prekybos ir komercijos kanalų \> interneto \> parduotuves**.
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

Toliau šios temos skyriuje Lokalizuoti el. komercijos [svetainės](#localize-e-commerce-site-content) turinį taikomas jūsų puslapių ir fragmentų turinio lokalizavimo procesas.

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

Puslapių, fragmentų ir laikmenų turto lokalizavimo veiksmai yra panašūs. Išimtys ir skirtumai nurodyti tolesniuose skyriuose. Tačiau skiriasi modulio lokalizavimo veiksmų turinys. Norėdami gauti daugiau informacijos, toliau šioje temoje [žr.](#localize-modules) skyrių Lokalizuoti modulius.

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
