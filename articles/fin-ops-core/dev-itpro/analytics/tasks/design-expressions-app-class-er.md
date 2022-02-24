---
title: ER išraiškų kūrimas siekiant iškviesti programos klasių metodus
description: Šiame vadove pateikiama informacija, kaip pakartotinai naudoti esamą programos logiką naudojantis elektroninių ataskaitų (ER) konfigūracijomis ir iškviečiant reikiamus ER išraiškų programos klasių metodus.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d79d1a4e86731a62de4896a489a13f624ce159f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682026"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ER išraiškų kūrimas siekiant iškviesti programos klasių metodus

[!include [banner](../../includes/banner.md)]

Šiame vadove pateikiama informacija, kaip pakartotinai naudoti esamą programos logiką naudojantis elektroninių ataskaitų (ER) konfigūracijomis ir iškviečiant reikiamus ER išraiškų programos klasių metodus. Klasių iškvietimo argumentų vertės gali būti nurodytos dinamiškai vykdymo laiku: pavyzdžiui, pagal analizavimo dokumente pateikiamą informaciją, kad būtų užtikrinamas jos tikslumas. Šiame vadove kursite reikiamas ER konfigūracijas pavyzdinei įmonei „Litware, Inc.“. Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo. 

Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį. Taip pat turite atsisiųsti ir įrašyti šį failą vietiniame diske: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Patikrinkite, ar pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra galimas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu” veiksmus.   
    * Jūs kuriate gaunamų banko išrašų analizavimo procesą, skirtą atlikti programos duomenų naujinimą. Banko išrašus gausite kaip TXT failus, kuriuose nurodyti IBAN kodai. Kadangi atliekamas banko išrašo importavimo procesas, turite patikrinti, ar šie IBAN kodai teisingi, naudodami logiką, kuri jau prieinama.   

## <a name="import-a-new-er-model-configuration"></a>Importuoti naują ER modelio konfigūraciją
1. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite plytelę „Microsoft“ teikėjas.  
2. Spustelėkite Saugyklos.
3. Spustelėkite Rodyti filtrus.
4. Pridėti filtro lauką „Įvesti pavadinimą“. Lauke Pavadinimas įveskite reikšmę „ištekliai”, pasirinkite filtro operatorių „apima” ir spustelėkite Taikyti.
5. Spustelėkite Atidaryti.
6. Medyje pasirinkite Mokėjimo modelis.
    * Jei neįgalintas „FastTab“ Versijos mygtukas Importuoti, gali būti, kad jau importavote 1 versiją į vieną iš ER konfigūracijų „Mokėjimo modelis“. Galite praleisti kitus šios antrinės užduoties veiksmus.   
7. Spustelėkite Importuoti.
8. Spustelėkite Taip.
9. Uždarykite puslapį.
10. Uždarykite puslapį.

## <a name="add-a-new-er-format-configuration"></a>Įtraukite naują ER formato konfigūraciją
1. Spustelėkite Ataskaitų konfigūracijos.
    * Įtraukite naują ER formatą, kad galėtumėte analizuoti gaunamus banko išrašus TXT formatu.  
2. Medyje pasirinkite Mokėjimo modelis.
3. Spustelėdami Kurti konfigūraciją atidarykite dialogo meniu.
4. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.
5. Lauke Oavadinimas įveskite „Banko išrašo importavimo formatas (pavyzdys)“.
    * Banko išrašo importavimo formatas (pavyzdys)  
6. Lauke Palaikomas duomenų importavimas pasirinkite Taip.
7. Spustelėkite Sukurti konfigūraciją.

## <a name="design-the-er-format-configuration---format"></a>ER formato konfigūracijos kūrimas – formatas
1. Spustelėkite Konstruktorius.
    * Sukurtas formatas atitinka numatytą išorinio TXT formatu pateikiamo failo struktūrą.  
2. Spustelėdami Įtraukti šakninį elementą atidarykite dialogo meniu.
3. Medyje pasirinkite Text\Sequence.
4. Lauke Pavadinimas įveskite Šaknis.
    * Šaknis  
5. Lauke Specialieji simboliai pasirinkite Nauja eilutė – „Windows“ (CR LF).
    * Lauke „Specialieji simboliai“ pažymėta parinktis „Nauja eilutė – „Windows“ (CR LF)“. Pagal šį parametrą kiekviena analizavimo failo eilutė laikoma atskiru įrašu.  
6. Spustelėkite GERAI.
7. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
8. Medyje pasirinkite Text\Sequence.
9. Lauke Pavadinimas įveskite „Eilutės“.
    * Eilutės  
10. Lauke Daugialypumas pasirinkite „Vienas daug“.
    * Lauke „Įvairovė“ pažymėta parinktis „Vienas daug“. Pagal šį parametrą tikimasi, kad analizavimo faile sutaps mažiausiai viena eilutė.  
11. Spustelėkite GERAI.
12. Medyje pasirinkite „Root\Rows“ (šaknis\eilutės).
13. Spustelėkite Įtraukti seką.
14. Lauke Pavadinimas įveskite „Laukai“.
    * Laukai  
15. Lauke Daugialypumas pasirinkite „Tiksliai vienas“.
16. Spustelėkite GERAI.
17. Medyje pasirinkite „Root\Rows\Fields“ (šaknis\eilutės\laukai).
18. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
19. Medyje pasirinkite „Tekstas \ Eilutė‟.
20. Lauke „Pavadinimas“, įveskite „IBAN“.
    * IBAN  
21. Spustelėkite GERAI.
    * Sukonfigūruota, kad kiekvienoje analizavimo failo eilutėje būtų tik vienas IBAN kodas.  
22. Spustelėkite Įrašyti.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>ER formato konfigūracijos kūrimas – susiejimas su duomenų modeliu
1. Spustelėkite Susieti formatą su modeliu.
2. Spustelėkite Naujas.
3. Lauke Aprašas įveskite „BankToCustomerDebitCreditNotificationInitiation“.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges – aprašas.
5. Lauke Pavadinimas įveskite „Susiejimas su duomenų modeliu“.
    * Susiejimas su duomenų modeliu  
6. Spustelėkite Įrašyti.
7. Spustelėkite Konstruktorius.
8. Medyje pasirinkite „Dynamics 365 for Operations\Class“.
9. Spustelėkite „Įtraukti šaknį“.
    * Įtraukite naują duomenų šaltinį, skirtą iškviesti esamą programos logiką, kad būtų galima patikrinti IBAN kodus.  
10. Lauke Pavadinimas įveskite „check_codes“.
    * check_codes  
11. Lauke Klasė įveskite „ISO7064“.
    * ISO7064  
12. Spustelėkite GERAI.
13. Medyje išplėskite „format“.
14. Medyje išplėskite „formatas\Šaknis: seka(šaknis)“.
15. Medyje pasirinkite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)“.
16. Spustelėkite Susieti.
17. Medyje išplėskite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)“.
18. Medyje išplėskite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)\Laukai: seka 1..1 (laukai)“.
19. Medyje pasirinkite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)\Laukai: seka 1..1 (laukai)\IBAN: eilutė(IBAN)“.
20. Medyje išplėskite „Payments = format.Root.Rows“ (mokėjimai = formatas, šaknis, eilutės).
21. Medyje išplėskite „Mokėjimai = formatas.Šaknis.Eilutės\Kreditoriaus sąskaita(KreditoriausSąskaita)“.
22. Medyje išplėskite „Mokėjimai = formatas.Šaknis.Eilutės\Kreditoriaus sąskaita(KreditoriausSąskaita)\Identifikacija“.
23. Medyje pasirinkite „Mokėjimai = formatas.Šaknis.Eilutės\Kreditoriaus sąskaita(KreditoriausSąskaita)\Identifikacija\IBAN“.
24. Spustelėkite Susieti.
25. Spustelėkite skirtuką Tikrinimai.
26. Spustelėkite Naujas.
    * Įtraukite naują tikrinimo taisyklę, kuri rodo bet kurios analizavimo failo eilutės klaidą, kai įvedamas netinkamas IBAN kodas.  
27. Spustelėkite Redaguoti sąlygą.
28. Medyje išplėskite „check_codes“.
29. Medyje pasirinkite „check_codes\verifyMOD1271_36“.
30. Spustelėkite „Įtraukti duomenų šaltinį“.
31. Lauke Formulė įveskite „check_codes.verifyMOD1271_36(“.
    * check_codes.verifyMOD1271_36(  
32. Medyje išplėskite „format“.
33. Medyje išplėskite „formatas\Šaknis: seka(šaknis)“.
34. Medyje išplėskite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)“.
35. Medyje išplėskite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)\Laukai: seka 1..1 (laukai)“.
36. Medyje pasirinkite „formatas\Šaknis: seka(šaknis)\Eilutės: seka 1..* (eilutės)\Laukai: seka 1..1 (laukai)\IBAN: eilutė(IBAN)“.
37. Spustelėkite „Įtraukti duomenų šaltinį“.
38. Lauke Formulė įveskite „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)“.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Spustelėkite Įrašyti.
40. Uždarykite puslapį.
    * Sukonfigūruota, kad bet kuriuo netinkamo IBAN kodo atveju tikrinimo sąlygos pateiktų rezultatą FALSE (klaidinga), o esamas programos klasės „ISO7064“ metodas būtų pavadintas „verifyMOD1271_36“. Atkreipkite dėmesį į tai, kad IBAN kodo vertė nurodoma dinamiškai vykdymo laiku kaip metodo iškvietimo argumentas pagal analizavimo TXT failo turinį.   
41. Spustelėkite Redaguoti pranešimą.
42. Lauke Formulė įveskite „CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)“.
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)  
43. Spustelėkite Įrašyti.
44. Uždarykite puslapį.
45. Spustelėkite Įrašyti.
46. Uždarykite puslapį.

## <a name="run-the-format-mapping"></a>Paleisti formato susiejimą
Bandymams atlikti formato susiejimą vykdykite naudodami anksčiau atsisiųstą failą SampleIncomingMessage.txt. Sugeneruotoje išvestyje pateikiami iš pasirinkto TXT failo importuoti duomenys, kurie realiojo importo metu bus automatiškai įvesti į pasirinktinių duomenų modelį.   
1. Spustelėkite Vykdyti.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą SampleIncomingMessage.txt.  
2. Spustelėkite GERAI.
    * Peržiūrėkite išvestį XML formatu, kuriuo rodomi iš pasirinkto failo importuoti ir į duomenų modelį perkelti duomenys. Atkreipkite dėmesį, kad apdorotos tik 3 importuojamo TXT failo eilutės. 4 eilutėje esantis netinkamas IBAN kodas praleistas ir sistemos pranešime pateikiamas klaidos pranešimas.  

