---
title: Klientų skirstymo pagal terminus ataskaita
description: Ataskaita Klientų skirstymas pagal terminus nurodo iš klientų gautinus balansus, surūšiuotus pagal datos intervalą arba skirstymo pagal terminus laikotarpį.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c1e3b724c95aa91192c77d5f3b8be4f93f0357f5f2f940c198bc8da47933fa0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769088"
---
# <a name="customer-aging-report"></a>Klientų skirstymo pagal terminus ataskaita 

Ataskaita **Klientų skirstymas pagal terminus** nurodo iš klientų gautinus balansus, surūšiuotus pagal datos intervalą arba skirstymo pagal terminus laikotarpį.

Kai generuojate šią ataskaitą, rodomi toliau pateikti numatytieji parametrai. Šiuos parametrus galite naudoti norėdami filtruoti duomenis, kurie bus rodomi ataskaitoje. Daugiau informacijos žr. [Mokėjimų priežiūros nustatymas](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Laukas</p></th>
<th><p>Aprašas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Atsiskaitymo klasifikacija</strong></p></td>
<td><p>Pasirinkite vieną ar kelias atsiskaitymo klasifikacijas, kurias norite įtraukti į ataskaitą.</p>
<div class="alert">

**Pastaba:** šis valdiklis galimas tik tada, kai pasirinktas <STRONG>viešojo sektoriaus</STRONG> konfigūracijos raktas.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Įtraukti operacijų be atsiskaitymo klasifikacijos</strong></p></td>
<td><p>Jei šis žymės langelis pasirinktas, ataskaitoje bus rodomos visos operacijos, neturinčios joms priskirtos atsiskaitymo klasifikacijos.</p>
<div class="alert">

**Pastaba:** šis valdiklis galimas tik tada, kai pasirinktas <STRONG>viešojo sektoriaus</STRONG> konfigūracijos raktas.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Skirstymas pagal terminus nuo</strong></p></td>
<td><p>Įveskite datą, naudojamą dabartiniame skirstymo pagal terminus rinkinyje.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Balansas nuo</strong></p></td>
<td><p>Įveskite datą, kurios klientų balansus norite peržiūrėti. Ji dar vadinama operacijų galutine data.</p></td>
</tr>
<tr class="even">
<td><p><strong>Pradžios data</strong></p></td>
<td><p>Įveskite datą, patenkančią į pirmojo laikotarpio intervalą arba skirstymo pagal terminus intervalą, kuri bus įtraukta į ataskaitą.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kriterijai</strong></p></td>
<td><p>Pasirinkite datos tipą, kuriuo remiantis bus kuriama ataskaita.</p>
<ul>
<li><p><strong>Operacijos data</strong> – operacijų registravimo data. Pavyzdžiui, tai gali būti SF data, kuri yra termino skaičiavimo pagrindas.</p></li>
<li><p><strong>Terminas</strong> – operacijų terminas, sukuriamas pagal mokėjimo sąlygas.</p></li>
<li><p><strong>Dokumento data</strong> – vartotojo nurodyta dokumento data, pagal kurią skaičiuojamas terminas.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Skirstymo pagal terminus laikotarpio apibrėžimas</strong></p></td>
<td><p>Pasirinkite skirstymo pagal terminus laikotarpio apibrėžimą. Laukas <strong>Intervalas</strong> nenaudojamas, jei pasirenkate skirstymo pagal terminus laikotarpio apibrėžimą.</p>
<p>Skirstymo pagal terminus laikotarpio apibrėžimų, kuriuose yra daugiau nei šeši skirstymo pagal terminus laikotarpiai, negalima naudoti spausdintoje ataskaitoje.</p>
<div class="alert">

**Pastaba:** skirstymo pagal terminus laikotarpius galite nustatyti pyslapyje <STRONG>Skirstymo pagal terminus laikotarpio apibrėžimai</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Spausdinti skirstymo pagal terminus laikotarpio apibrėžimą</strong></p></td>
<td><p>Pasirinkite <strong>Taip</strong>, jei norite kiekvieno skirstymo pagal terminus laikotarpio stulpelio, esančio ataskaitoje, viršuje įterpti skirstymo pagal terminus laikotarpių apibrėžimus. Pasirinkite <strong>Ne</strong>, norėdami spausdinti ataskaitą be stulpelių antraščių.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intervalas</strong></p></td>
<td><p>Nurodykite laikotarpį, kuris bus naudojamas, įvedę kiekvieno laikotarpio dienos ar mėnesio vienetų skaičių. Pvz., norėdami peržiūrėti skirstymo pagal terminus informaciją pagal savaitę, šiame lauke įveskite 7 ir pasirinkite <strong>Diena</strong> lauke <strong>Diena / mėnuo</strong>.</p>
<div class="alert">

**Pastaba:** jūsų šiame lauke įvesta informacija naudojama tik jei nesate pasirinkę skirstymo pagal terminus laikotarpio apibrėžimo. Kitu atveju spausdinimo kryptis nurodoma skirstymo pagal terminus laikotarpio apibrėžime.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Diena / mėnuo</strong></p></td>
<td><p>Pasirinkite vienetą <strong>Diena</strong> arba <strong>Mėnuo</strong>, kuris bus naudojamas laikotarpiui apibrėžti, lauke <strong>Intervalas</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Spausdinimo kryptis</strong></p></td>
<td><p>Pasirinkite, kokių laikotarpių balansus skaičiuoti ir skirstymo pagal terminus ataskaitą spausdinti – buvusių ar būsimų. Datos įvertinamos atsižvelgiant į datą, kuri pasirinkta lauke <strong>Balansas nuo</strong>. Pasirinkite <strong>Atgal</strong>, kad būtų rodoma buvusių laikotarpių informacija. Pasirinkite <strong>Pirmyn</strong>, kad būtų rodoma būsimų laikotarpių informacija.</p>
<div class="alert">
  
<STRONG>Pastaba:</STRONG> jūsų šiame lauke įvesta informacija naudojama tik jei nesate pasirinkę skirstymo pagal terminus laikotarpio apibrėžimo.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Išsamiai</strong></p></td>
<td><p>Pasirinkite, kad būtų pateiktos operacijos, įtrauktos į ataskaitoje nurodytus balansus.</p></td>
</tr>
<tr class="even">
<td><p><strong>Įtraukti sumas operacijos valiuta</strong></p></td>
<td><p>Pasirinkite, kad būtų įtrauktos sumos operacijos valiuta ir sumos apskaitos valiuta. Jei šis žymės langelis nepasirinktas, sumos ataskaitoje rodomos tik apskaitos valiuta.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Neigiamas balansas</strong></p></td>
<td><p>Pasirinkite, kad būtų įtrauktos kliento sąskaitos, kurių balansai yra neigiami.</p></td>
</tr>
<tr class="even">
<td><p><strong>Neįtraukti sąskaitų su nuliniu balansu</strong></p></td>
<td><p>Pasirinkite, kad nebūtų įtrauktos kliento sąskaitos, kurių balansai yra nuliniai.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Mokėjimo padėties nustatymas</strong></p></td>
<td><p>Pasirinkite, kad būtų rodomi nesudengti mokėjimai. Jie rodomi pirmame ataskaitos stulpelyje.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]