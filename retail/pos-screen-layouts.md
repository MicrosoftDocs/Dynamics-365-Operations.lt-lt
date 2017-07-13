---
title: "EKA ekrano maketų konfigūravimas"
description: "Šioje temoje pateikiama informacija apie „Microsoft Dynamics 365 for Retail“ elektroninio kasos aparato (EKA) patirčių ekrano išdėstymus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 9f7f46c1bae5bac6eefa0b8c70b079cab76aa8b6
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017


---

# <a name="configure-screen-layouts-for-pos"></a>EKA ekrano maketų konfigūravimas

[!include[banner](includes/banner.md)]


Šioje temoje pateikiama informacija apie „Microsoft Dynamics 365 for Retail“ elektroninio kasos aparato (EKA) patirčių ekrano išdėstymus.

„Microsoft Dynamics 365 for Retail“ elektroninio kasos aparato (EKA) vartotojo sąsają galima sukonfigūruoti naudojant parduotuvėms, registrams ir (arba) vartotojams priskirtų vaizdo šablonų ir ekrano išdėstymų kombinaciją.

## <a name="visual-profile"></a>Vaizdo šablonas
Vaizdo šablonai priskiriami registrams ir naudojami norint nurodyti pagal registrą suskirstytus ir vartotojų bendrai naudojamus vaizdo elementus. Visi prie registro prisijungę vartotojai turi tą pačią temą, spalvas ir vaizdus. 

**Šablono numeris** – tai unikalus vaizdo šablono identifikavimo numeris. 

**Aprašas** – naudodami aprašą galite nurodyti prasmingą pavadinimą, kuris padėtų nuspręsti, kuris šablonas tinkamas jūsų atveju.

**Tema** – vartotojai gali pasirinkti šviesią arba tamsią programos temą. Nuo šių parametrų priklauso visoje programoje naudojamos šrifto ir fono spalvos.

**Akcento spalva** – tai spalva, kuri naudojama EKA norint atskirti arba paryškinti tam tikrus vaizdo elementus, pavyzdžiui, plyteles, komandų mygtukus arba hipersaitus. Paprastai veiksmingi šie elementai.

**Antraštės spalva** – naudodamas antraštės spalvą vartotojas gali konfigūruoti puslapio antraštės spalvą, kad ji atitiktų mažmenininko keliamus reikalavimus prekės ženklui. Ši funkcija pasiekiama tik „Dynamics 365 for Retail‟ 1611 versijoje.

**Prisijungimo fonai** – vartotojai gali nurodyti, koks fono paveikslėlis bus naudojamas prisijungimo ekrane. Fono vaizdų failo dydis turėtų būti kuo mažesnis, nes įrašant ir įkeliant didelius failus tai gali turėti įtakos programos veikimui ir našumui.

**Programos fonas** – EKA taip pat gali naudoti vaizdą kaip foną visoje programoje vietoje vienspalvės temos. Patariama, kad prisijungimo fonų failų dydžiai būtų kuo mažesni.

## <a name="screen-layouts"></a>Ekrano maketai
Nuo ekrano išdėstymo konfigūracijos priklauso, kokie bus UI valdiklių veiksmai, turinys ir išdėstymo tvarka EKA darbo pradžios ekrane ir operacijos ekrane. 

**Darbo pradžios ekranas** – daugeliu atvejų tai puslapis, kurį vartotojai matys pirmą kartą prisijungę prie EKA. Darbo pradžios ekrane gali būti prekės ženklo vaizdas ir mygtukynai, suteikiantys prieigą prie EKA operacijų. Paprastai čia pateikiamos operacijos, kurios priklauso nuo dabartinės operacijos. 

**Operacijos ekranas** – tai pagrindinis EKA ekranas, skirtas apdoroti pardavimo operacijas ir užsakymus. Operacijos ekraną galima sukonfigūruoti naudojant ekrano išdėstymo kūrimo įrankį. 

**Numatytasis pradžios ekranas** – kai kurie mažmenininkai pageidauja, kad prisijungęs kasininkas iš karto eitų į operacijos ekraną. Naudodami numatytojo pradžios ekrano nuostatą vartotojai gali nustatyti šią parinktį kiekvienam ekrano išdėstymui.

### <a name="assignment"></a>Priskyrimas

Ekranų išdėstymus galima priskirti pagal parduotuvę, registrą arba vartotoją. Pasirinkus vartotojo priskyrimą nepaisoma registro ir parduotuvės priskyrimo, o pasirinkus registro priskyrimą nepaisoma parduotuvės priskyrimo. Paprastame scenarijuje, kai visi vartotojai naudoja tą patį išdėstymą nepriklausomai nuo registro ar vaidmens, ekrano išdėstymą galima nnustatyti tik parduotuvėje. Tais atvejais, kai tam tikriems registrams arba vartotojams reikalingi specialūs išdėstymai, galima juos priskirti.

### <a name="layout-sizes"></a>Maketo dydžiai

Ši funkcija taikoma tik „Dynamics 365 for Retail“ 1611 versijai. Kadangi daugeliu atvejų ekranų išdėstymus galima naudoti naudojant kelis ekrano dydžius ir skiriamąsias gebas, vartotojai kiekvienam iš jų gali sukonfigūruoti savo išdėstymą ir turinį. Kai paleidžiamas įrenginys, EKA programa automatiškai pasirenka artimiausią įrenginio išdėstymo dydį. Ekrano išdėstyme taip pat gali būti konfigūracijų, skirtų pilnoms ir kompaktinėms įrenginių versijoms. Naudojant šią konfigūraciją vartotojui gali būti priskirtas vienas ekrano išdėstymas, kuris veiks su įvairiais parduotuvėje esančiais dydžiais ir formos veiksniais. 

**Modernus EKA – pilnas** – pilnus išdėstymus paprastai geriausia naudoti didesniems ekranams, pavyzdžiui, kompiuterių monitoriams arba planšetiniams kompiuteriams. Vartotojai gali pasirinkti, kokius vartotojo sąsajos elementus įtraukti, nustatyti jų dydį ir išdėstymo tvarką ir sukonfigūruoti išsamias jų ypatybes. Pasirinkus pilnus išdėstymus palaikomos vertikalios ir horizontalios konfigūracijos. 

**Modernus EKA – kompaktinis** – kompaktiniai išdėstymai paprastai naudojami telefonams arba nedideliems planšetiniams kompiuteriams. Kompaktinių įrenginių dizaino galimybės ribotos. Vartotojai gali sukonfigūruoti kvito ir bendrųjų sumų sričių stulpelius ir laukus.

### <a name="screen-layout-designer"></a>Ekrano maketo dizaineris

Kiekvieno ekrano išdėstymo dydį būtina sukonfigūruoti naudojant ekrano išdėstymo kūrimo įrankį. Naudodami kūrimo įrankį vartotojai gali nurodyti ir konfigūruoti operacijos ekrano vartotojo sąsajos elementus. Ekrano išdėstymo kūrimo įrankis kiekvieną kartą vartotojui įjungus programą, jei norima atsisiųsti, įdiegti ir paleisti naujausią versiją, naudoja „ClickOnce“. Būtinai patikrinkite naršyklės reikalavimus naudojant „ClickOnce“ – naudojant kai kurias naršykles, pavyzdžiui, „Chrome“ reikalingi plėtiniai. 

**Skaičių klaviatūra** – tai pagrindinė vartotojo įvestis EKA operacijos ekrane. Galima sukonfigūruoti, kad būtų rodoma viso ekrano klaviatūra, o tai idealiai tinka naudojant jutiklinius ekranus, arba tik įvesties laukas, kurį galima naudoti naudojant faktinę klaviatūrą. Skaičių klaviatūros parametrus galima naudoti tik naudojant pilną išdėstymą. Naudojant „Dynamics 365 for Retail“ 1611 versiją, kompaktinių išdėstymų operacijos ekrane visada galima naudoti visą skaičių klaviatūrą.

**Bendrųjų sumų sritis** – galima sukonfigūruoti, kad bendrųjų sumų sritis būtų rodoma vienu arba dviem stulpeliais, kuriuose pateikiami tam tikri laukai, pavyzdžiui, eilučių skaičius, nuolaidos suma, išlaidos, tarpinė suma ir mokestis. Naudojant „Dynamics 365 for Retail“ 1611 versiją kompaktiniai išdėstymai palaiko tik vieną bendrųjų sumų stulpelį. 

**Gavimo kvitas** – gavimo kvito srityje pateikiamos pardavimų eilutės, mokėjimo eilutės ir naudojant EKA apdorotų produktų bei paslaugų pristatymo informacija. Vartotojai gali nurodyti stulpelius, pločius ir išdėstymo tvarką. „Dynamics 365 for Retail“ 1611 versijos kompaktiniuose išdėstymuose taip pat galite sukonfigūruoti papildomą informaciją, kuri bus rodoma po pagrindine eilute esančioje eilutėje. 

**Kliento kortelė** – kliento kortelėje rodoma su šiuo metu su operacija susietu vartotoju susijusi informacija. Galima sukonfigūruoti, kad papildoma informacija kliento kortelėje būtų slepiama arba rodoma. 

**Skirtuko valdiklis** – skirtuko valdiklį galima patalpinti ekrano išdėstyme, o skirtuko viduje galima patalpinti kitus valdiklius, pavyzdžiui, skaičių klaviatūrą, kliento kortelę arba mygtukyną. Skirtuko valdiklis – tai konteineris, padedantis vartotojams ekrane sutalpinti daugiau turinio. Skirtuko valdiklį galima naudoti tik naudojant pilnus išdėstymus. 

**Vaizdas** – vaizdo valdiklį galima naudoti norint, kad operacijos ekrane būtų rodomas parduotuvės logotipas arba kitas prekės ženklo vaizdas. Vaizdo valdiklį galima naudoti tik naudojant pilnus išdėstymus. 

**Rekomenduojami produktai** – jei sukonfigūruota aplinkai, rekomenduojamų produktų valdiklyje rodomi produktų pasiūlymai pagal mašininį mokymą. Rekomenduojamų produktų valdiklį galima naudoti tik naudojant „Dynamics 365 for Retail“ 1611 versijos pilnus išdėstymus. **Pasirinktinis valdiklis **– pasirinktinis valdiklis ekrano išdėstyme veikia kaip vietos rezervavimo ženklas, kad vartotojai galėtų rezervuoti vietą pasirinktam turiniui. Pasirinktinį valdiklį galima naudoti tik naudojant pilnus išdėstymus.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Mažmeninės prekybos EKA išdėstymo kūrimo įrankio diegimas](install-pos-layout-designer.md)




