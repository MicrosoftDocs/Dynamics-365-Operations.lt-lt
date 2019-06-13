<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="lt-LT">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Šioje temoje aprašomas savikainos konfigūravimas naudojant „Microsoft Dynamics 365 for Retail“ paskirstytų užsakymų tvarkymo (DOM) funkciją.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Siekdamos nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymą, organizacijos apsvarsto keletą savikainos komponentų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kai kurie iš šių savikainos komponentų yra siuntimo savikaina, tvarkymo savikaina ir pakavimo savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Siekiant nustatyti įvykdymo vietą, apskaičiuojamas šių savikainų derinys.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kai, naudojant pirmąją „Microsoft Dynamics 365 for Retail“ paskirstytų užsakymų tvarkymo (DOM) funkciją, optimizuotas užsakymų priskyrimas įvykdymo vietoms, buvo atsižvelgiama tik į atstumą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nors atstumas gali būti susijęs su savikaina, tai nėra tas pats.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Pavyzdžiui, kai atstumas yra toks pats, siuntimo naktį būdas kainuoja daugiau, nei siuntimas per tris dienas ar siuntimas per septynias dienas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Savikainos konfigūravimo funkcija mažmenininkams leidžia nustatyti ir konfigūruoti papildomus savikainos komponentus, kurie bus apskaičiuojami ir į kuriuos bus atsižvelgiama siekiant nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymų eilutes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kai sukonfigūruojami savikainos komponentai, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė naudoja tik tas savikainos apibrėžtis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Atstumo komponento ji nelaiko savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Tačiau, jei savikainos komponentų nėra sukonfigūruota, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė atstumo komponentą kaip savikainą naudoja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Savikainos komponentų nustatymas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sistemoje galima nustatyti du pagrindinius savikainos komponentų tipus: <bpt id="p1">**</bpt>Siuntimo<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Kitas<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Abu savikainos komponentų tipai palaiko keletą skaičiavimo pagrindų, kaip parodyta tolesnėje lentelėje.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Savikainos komponento tipas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Skaičiavimo pagrindas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Siuntimo</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Paprastas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Pakopinis</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Kitas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Pardavimo užsakymas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Pardavimo eilutė</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Vieta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Siuntimo savikainos komponento tipas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo <bpt id="p1">**</bpt>Siuntimo<ept id="p1">**</ept> derinį ir siuntimo savikainos skaičiavimo pagrindą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Paprastas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jei yra naudojamas savikainos komponento tipo <bpt id="p1">**</bpt>Siuntimo<ept id="p1">**</ept> ir skaičiavimo pagrindo <bpt id="p2">**</bpt>Paprastas<ept id="p2">**</ept> derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Savikainos faktorius<ept id="p1">**</ept> – įveskite unikalų savikainos faktoriaus identifikatorių.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Aprašas<ept id="p1">**</ept> – įveskite savikainos faktoriaus pavadinimą ir aprašą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Pradžios data<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Pabaigos data<ept id="p2">**</ept> – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Aktyvus<ept id="p1">**</ept> – nurodykite, ar savikainos faktorius yra aktyvus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Įmonė<ept id="p1">**</ept> – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Pristatymo būdai<ept id="p1">**</ept> – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Skaičiavimo tipas<ept id="p1">**</ept> – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Palaikomi du tolesni skaičiavimo tipai.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Fiksuotasis<ept id="p1">**</ept> – pristatymo būdui naudojama fiksuotoji savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke <bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Pagal atstumo vienetą<ept id="p1">**</ept> – pristatymo būdo savikaina apskaičiuojama kaip lauke <bpt id="p2">**</bpt>Savikaina<ept id="p2">**</ept> nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept> – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku <bpt id="p2">**</bpt>Skaičiavimo tipas<ept id="p2">**</ept> apskaičiuojama pristatymo būdo savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Pakopinis</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Jei yra naudojamas savikainos komponento tipo <bpt id="p1">**</bpt>Siuntimo<ept id="p1">**</ept> ir skaičiavimo pagrindo <bpt id="p2">**</bpt>Pakopinis<ept id="p2">**</ept> derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tačiau šiame derinyje atstumas nustatomas pagal pakopinį atstumų intervalą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Savikainos faktorius<ept id="p1">**</ept> – įveskite unikalų savikainos faktoriaus identifikatorių.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aprašas<ept id="p1">**</ept> – įveskite savikainos faktoriaus pavadinimą ir aprašą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Numatytoji savikaina<ept id="p1">**</ept> – nurodykite pristatymo būdo savikainą, kuri turi būti naudojama, jei atstumas tarp pristatymo adreso ir vietos nepatenka į jokį iš pristatymo būdo pakopinių atstumų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pradžios data<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Pabaigos data<ept id="p2">**</ept> – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktyvus<ept id="p1">**</ept> – nurodykite, ar savikainos faktorius yra aktyvus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Įmonė<ept id="p1">**</ept> – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pristatymo būdai<ept id="p1">**</ept> – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Atstumo tipas<ept id="p1">**</ept> – nurodykite, ar pakopinis atstumas apibrėžiamas kaip atstumas oru, ar atstumas keliais.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Atstumo vienetai<ept id="p1">**</ept> – nurodyti vienetą, kuriuo matuojamas pakopinis atstumas.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Atstumas nuo<ept id="p1">**</ept> – nurodykite pakopinio atstumo intervalo pradžią.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Atstumas iki<ept id="p1">**</ept> – nurodykite pakopinio atstumo intervalo pabaigą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Skaičiavimo tipas<ept id="p1">**</ept> – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo ir pakopinio atstumo savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Palaikomi du tolesni skaičiavimo tipai.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Fiksuotasis<ept id="p1">**</ept> – pristatymo būdui naudojama fiksuotoji savikaina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke <bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Pagal atstumo vienetą<ept id="p1">**</ept> – pristatymo būdo ir pakopinio atstumo savikaina apskaičiuojama kaip lauke <bpt id="p2">**</bpt>Savikaina<ept id="p2">**</ept> nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept> – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku <bpt id="p2">**</bpt>Skaičiavimo tipas<ept id="p2">**</ept> apskaičiuojama pristatymo būdo savikaina.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kai nustatote pakopinius atstumus, sistema patikrina, kad atstumų netrūktų ir kad jie nepersidengtų.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Naudojamas tam tikro pristatymo būdo atstumo tipas turi būti toks pats visuose pakopiniuose atstumuose.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Savikainos komponento tipas Kitas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo <bpt id="p1">**</bpt>Kitas<ept id="p1">**</ept> derinį ir kitą su siuntimu nesusijusių savikainų tipą.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo užsakymas</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Naudojant savikainos komponento tipo <bpt id="p1">**</bpt>Kitas<ept id="p1">**</ept> ir kito savikainos tipo <bpt id="p2">**</bpt>Pardavimo užsakymas<ept id="p2">**</ept> derinį, pardavimo užsakymo lygiu apibrėžiamos su siuntimu nesusijusios savikainos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Savikainos faktorius<ept id="p1">**</ept> – įveskite unikalų savikainos faktoriaus identifikatorių.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aprašas<ept id="p1">**</ept> – įveskite savikainos faktoriaus pavadinimą ir aprašą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pradžios data<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Pabaigos data<ept id="p2">**</ept> – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktyvus<ept id="p1">**</ept> – nurodykite, ar savikainos faktorius yra aktyvus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept> – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo lygiu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo eilutė</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Naudojant savikainos komponento tipo <bpt id="p1">**</bpt>Kitas<ept id="p1">**</ept> ir kito savikainos tipo <bpt id="p2">**</bpt>Pardavimo eilutė<ept id="p2">**</ept> derinį, pardavimo užsakymo eilutės lygiu apibrėžiamos su siuntimu nesusijusios savikainos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Savikainos faktorius<ept id="p1">**</ept> – įveskite unikalų savikainos faktoriaus identifikatorių.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aprašas<ept id="p1">**</ept> – įveskite savikainos faktoriaus pavadinimą ir aprašą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pradžios data<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Pabaigos data<ept id="p2">**</ept> – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktyvus<ept id="p1">**</ept> – nurodykite, ar savikainos faktorius yra aktyvus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept> – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo eilutės lygiu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Vieta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Naudojant savikainos komponento tipo <bpt id="p1">**</bpt>Kitas<ept id="p1">**</ept> ir kito savikainos tipo <bpt id="p2">**</bpt>Vieta<ept id="p2">**</ept> derinį, apibrėžiamos vietų grupės arba atskiros vietos su siuntimu nesusijusios savikainos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Savikainos faktorius<ept id="p1">**</ept> – įveskite unikalų savikainos faktoriaus identifikatorių.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aprašas<ept id="p1">**</ept> – įveskite savikainos faktoriaus pavadinimą ir aprašą.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pradžios data<ept id="p1">**</ept> ir <bpt id="p2">**</bpt>Pabaigos data<ept id="p2">**</ept> – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktyvus<ept id="p1">**</ept> – nurodykite, ar savikainos faktorius yra aktyvus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Įvykdymo grupė<ept id="p1">**</ept> – nurodykite vietų grupę, kuriai apibrėžta su siuntimu nesusijusi savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Įvykdymo vieta<ept id="p1">**</ept> – nurodykite vietą, kuriai apibrėžta su siuntimu nesusijusi savikaina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Toje pačioje vieta pagrįstų skaičiavimo kriterijų eilutėje negalite nurodyti ir įvykdymo grupės, ir įvykdymo vietos.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Savikaina<ept id="p1">**</ept> – nurodykite su siuntimu nesusijusios savikainos reikšmę įvykdymo grupės lygiu arba įvykdymo vietos lygiu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Norint, kad vykdoma DOM funkcija svarstytų šias savikainas, į atitinkamą įvykdymo profilį turite įtraukti savikainos faktorių.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>