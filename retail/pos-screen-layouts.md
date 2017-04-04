---
title: "Konfigūruoti ekrano išdėstymas POS"
description: "Šioje temoje pateikta informacija apie ekrano maketus Microsoft Dynamics &quot;365&quot; operacijų - mažmeninė point of pardavimo (PV) patirtimi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Konfigūruoti ekrano išdėstymas POS

Šioje temoje pateikta informacija apie ekrano maketus Microsoft Dynamics "365" operacijų - mažmeninė point of pardavimo (PV) patirtimi.

Microsoft Dynamics 365 operacijų - mažmeninė point of pardavimo (PV) vartotojo sąsajos gali būti konfigūruojamas naudojant vaizdo šablonų ir ekrano maketai, priskirtas parduotuves, registrų ir (arba) naudotojams.

## <a name="visual-profile"></a>Vaizdo šablonas
Vaizdo šablonų priskirtus registrus ir naudojamos nurodant vizualiniai elementai, kurie registre konkrečių ir bendrai visoje vartotojams. Vartotojo, kuris įeina į registrą turės pačią temą, spalvas bei vaizdus. **Profilio numeris** -profilis yra unikalus identifikatorius, vizualiai profilį. **Aprašymas** -aprašyme galima nurodyti prasmingą pavadinimą, kuris padės nustatyti tinkamą profilį į savo situaciją. **Temos** -vartotojai gali pasirinkti tarp šviesos ir tamsos programos temos. Šių parametrų įtakos, šrifto ir fono spalvas visą programą. **Paryškinimo spalva** -ryškesnės spalvos yra naudojamas per Go atskirti ar išryškinti tam tikri regimi elementai, pavyzdžiui, plytelės, komandų mygtukų arba hipersaitų. Šie elementai yra paprastai galima pareikšti ieškinį. **Antraštės spalva** -antraštės spalva leidžia vartotojui konfigūruoti spalvą, puslapio antraštę mažmenininko prekės ženklo naudojimo poreikiams patenkinti. Ši funkcija galima tik Dynamics 365 operacijų versija 1611. **Prisijungimo fonas** -vartotojai gali nurodyti prisijungimo ekrano fono paveikslėlį. Failo dydį, fono paveikslėlius turėtų būti laikomos kuo mažiau, nes saugojimui ir pakrovimo didelius failus gali turėti įtakos programos veikimą ir efektyvumą. **Taikyti fono** -The POS taip pat galite naudoti atvaizdą kaip fono visoje taikymas vietoj kietas tema spalva. Kaip ir prisijungimo fonas, patartina išsaugoti failo dydis būtų kuo mažesnis.

## <a name="screen-layouts"></a>Ekrano maketai
Ekrano išdėstymo konfigūracijos nurodo veiksmus, turinį ir vietą UI kontrolė POS Sveiki ekranas ir sandorio ekrano. ** Darbo pradžios ekrane **-daugeliu atvejų, darbo pradžios ekrane yra puslapis, kurį matys vartotojai, kai jie pirmą kartą prisijungti prie POS. Darbo pradžios ekrane gali būti sudaryta iš prekės ženklo įvaizdį ir mygtukynų, kurie teikia prieigą prie POS operacijas. Paprastai čia dedami operacijas, kurios nebūdingos šią operaciją. **Sandorio ekrano** -The operacijos ekranas yra pagrindinis ekranas pos pardavimo sandorių ir užsakymų perdirbimui. Operacijos ekranas gali būti konfigūruojamas naudojant ekrano maketo konstruktorių. **Numatytasis pradžios ekranas** -kai kurie mažmenininkai nori kad kasa eiti tiesiai į sandorio ekrano prisijungus. Pagal nutylėjimą pradžios ekrano leidžia vartotojams nustatyti, tai kiekvieno ekrano išdėstymas.

### <a name="assignment"></a>Priskyrimas

Ekrano maketai gali būti priskirtas parduotuvėje, registre arba vartotojo lygiu. Vartotojo priskyrimas pakeičia registrą ir saugoti priskyrimo ir registro priskyrimas perrašymus saugyklos priskyrimas. Paprastas tokiu, kur visi vartotojai naudoja pats išdėstymas, nepriklausomai nuo to, registro ar vaidmenį, ekrano išdėstymas gali būti nustatytas tik parduotuvėje. Tais atvejais, kai tam tikrų registruose ar vartotojai reikalauja specializuotos maketai, jie gali paskirti tinkamai.

### <a name="layout-sizes"></a>Maketo dydžiai

Ši ypatybė taikoma tik operacijoms versija 1611 Dynamics 365. Nes daugeliu atvejų ekrano maketai gali būti naudojami keliuose ekrano dydžio ir rezoliucijas, vartotojai gali konfigūruoti savo išdėstymas ir turinys kiekvienam. POS programa automatiškai pasirinks arčiausiai maketo dydis įrenginio paleidimo metu. Ekrano išdėstymas taip pat gali būti visiškai ir kompaktiškų įrenginių konfigūracijos. Ši konfigūracija leidžia vartotojui priskirti vieną ekrano išdėstymas, kuris veiks visoje įvairių dydžių ir formos veiksniai parduotuvėje. **Šiuolaikinės EKA - pilnas** -pilnas maketai paprastai geriausia naudoti vis didesnių ekranų, pvz., kompiuterio monitorių ar tablečių. Vartotojai gali pasirinkti kurie UI elementai apima, nustatyti jų dydį ir paskirties vietą, ir konfigūruoti savo išsamias apgyvendinimo įstaigos. Visą maketų remti tiek portreto ir kraštovaizdžio konfigūracijų. **Šiuolaikinės EKA - kompaktiškas** -kompaktiškas maketai paprastai geriausia naudoti telefonuose ir mažuose planšetiniuose kompiuteriuose. Dizaino galimybės yra ribotos kompaktiškų įrenginių. Vartotojai gali konfigūruoti gavimo ir sumų sritis laukų ir stulpelių.

### <a name="screen-layout-designer"></a>Ekrano maketo dizaineris

Kiekvieno maketo dydis per ekrano išdėstymas turi būti konfigūruojamas naudojant ekrano maketo konstruktorių. Dizaineris vartotojai gali nurodyti ir konfigūruoti sandorio ekrano vartotojo sąsajos elementai. Ekrano maketo konstruktorių naudoja "ClickOnce" taikomosios parsisiųsti, įdiegti ir paleisti naujausią programos kiekvieną kartą, kai vartotojas prisijungia prie jos. Patikrinkite naršyklės naudojant "ClickOnce" taikomosios — kai kuriose naršyklėse, pvz., "Chrome", reikia pratęsti. **Skaičių klaviatūrą** -skaičių klaviatūrą yra pagrindinis vartotojo įvesties EKA operacijų ekrane. Jis gali būti konfigūruojamas ekrane parodyti visą padą, kuris yra idealus jautriais ekranais, ar tik įvesties srityje, kuris gali būti naudojamas su fizinės klaviatūros. Skaičių pad nustatymai galimi tik visiškai išdėstymą. Dynamics 365 operacijų versija 1611, kompaktiškas maketus visuomet pasiekiamos sandorio ekrane pilną skaičių klaviatūrą. **Sumos grupės** - sumos skydas gali būti konfigūruojamas vieną arba du stulpeliai būtų rodomi papildomi laukai, pvz., eilučių skaičius, nuolaidos suma, mokesčiai, tarpinę sumą ir mokesčių. Dynamics 365 operacijų versija 1611, kompaktiškas išdėstymas palaiko tik vieną suvestinių stulpelis. **Gavimo** -** ** gavimo skyde yra pardavimų eilutes, mokėjimo eilutės ir pristatymo informaciją apie produktus ir paslaugas, apdorojama go. Vartotojai gali nurodyti stulpelius, pločių ir įdarbinimo. Kompaktiškas maketuose Dynamics 365 operacijų versija 1611, galite konfigūruoti papildomos informacijos, kuri bus rodomi eilutėje pagal pagrindinės linijos. **Pirk** - kliento kortelė rodo informaciją, susijusią su klientų, šiuo metu susiję su operacija. Pirkėjo kortelėje gali būti konfigūruojamas Slėpti arba Rodyti papildomos informacijos. **Skirtuką valdiklis** - skirtukų valdiklio gali būti dedamas ant ekrano išdėstymo ir kiti valdikliai, pavyzdžiui skaičių klaviatūrą, pirkėjo kortelėje arba mygtukynų gali būti įdedama viduje skirtuką. Slinkčių valdiklis yra konteineris, kuris padeda vartotojams ekrane pritaikytumėte didesnį turinį. Slinkčių valdiklis skirtas tik visą maketų. ** Nuotraukos **-vaizdo valdiklis gali būti naudojamas Rodyti parduotuvėje logotipą ar kitą prekės ženklo vaizdą ekrane operacijos. Vaizdo valdiklis skirtas tik visiškai maketus. **Rekomenduojama produktus** - jei sukonfigūruotas naudoti aplinkai, rekomenduojamų produktų kontrolės parodys produkto pasiūlymus, pagrįstus mokymosi mašinos. Rekomenduojama produktų kontrolė galima tik visą maketų Dynamics 365 operacijų versija 1611. ** Pasirinktinio valdiklio **-pasirinktinį valdiklį veikia kaip vietos rezervavimo ženklas per vaizdo ekrane formatą į leidžia vartotojams ieškant vietos pasirinktinį turinio. Pasirinktinį valdiklį galima tik visiškai maketus.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


