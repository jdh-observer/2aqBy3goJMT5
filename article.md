---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.19.1
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

<!-- #region slideshow={"slide_type": ""} tags=["title"] -->
# Shelters for All? Spatial Equity and Civil Defence Planning in Postwar Aarhus
<!-- #endregion -->

<!-- #region jp-MarkdownHeadingCollapsed=true tags=["contributor"] -->
### Adela Sobotkova [![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-4541-3963) 
Aarhus University
<!-- #endregion -->

<!-- #region jp-MarkdownHeadingCollapsed=true slideshow={"slide_type": ""} tags=["contributor"] -->
### Rosanna Farbøl [![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-5186-4701) 
Aarhus University/University of Oslo
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["contributor"] -->
### Aiswarya Roy [![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0009-0009-7352-9291) 
Aarhus University
<!-- #endregion -->

<!-- #region tags=["copyright"] -->
[![cc-by](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/) 
©<AUTHOR or ORGANIZATION / FUNDER>. Published by De Gruyter in cooperation with the University of Luxembourg Centre for Contemporary and Digital History. This is an Open Access article distributed under the terms of the [Creative Commons Attribution License CC-BY](https://creativecommons.org/licenses/by/4.0/)

<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["copyright"] -->
[![cc-by-nc-nd](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/) 
©<AUTHOR or ORGANIZATION / FUNDER>. Published by De Gruyter in cooperation with the University of Luxembourg Centre for Contemporary and Digital History. This is an Open Access article distributed under the terms of the [Creative Commons Attribution License CC-BY-NC-ND](https://creativecommons.org/licenses/by-nc-nd/4.0/)

<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["keywords"] -->
civil defense, historical accessibility, preparedness, Denmark
<!-- #endregion -->

<!-- #region tags=["abstract"] -->
This paper addresses the overlooked spatial dimensions of civil defence infrastructure during the Cold War, focusing on Aarhus, Denmark’s second-largest city. While Cold War military facilities have received considerable attention, civil defence systems have been largely neglected in spatial research. This study fills that gap by exploring the development and distribution of civilian shelters in Aarhus, managed by the local Civil Defence Commission (CDC) from 1950 to 1989. Using data digitised by the [MELICA project](https://cas.au.dk/en/melica/) from the Aarhus City Archive, the paper analyses shelter distribution and urban preparedness as it was implemented in the second-biggest Danish city. Our results show that while most buildings were within the maxium distance to a shelter as defined by the authorities, the question of equality and universality depends on calculation methods, and moreover, that no matter the methods, aggregate capacity remained inadequate in the early postwar years. The paper highlights the importance of reflection on the compatibility of concepts and methods when assessing historical data through modern digital tools, such as geospatial analysis. 
In relation to JDH structure; the narrative presents the national guidelines for civil defense and contrasts them with the results of the field survey and analysis of documents pertaining to implementation of civil defense in Aarhus. The hermeneutic layer focuses on the methodology of data capture and processing and analysis, where the latter especially is dominated by methods developed after the date of the historical urban planning being assessed, which of course impacts the perceived gap between the civil defense coverage and the Aarhus stakeholders. The data layer documents the spatial equity outcomes using a building-shelter distance matrix where inputs consisting of historical records on 1951 shelters, buildings and urban extent of Aarhus are used to calculate accessibility indeces, via the osm, sfnetworks, and kdetrees R packages and standard place-based measures.  This study is not feasible without the requisite digital elements and methods, as they provide a prism through which historical plans and implementation of mass population preparedness is measured and assessed. 
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
## Building Shelters for All
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"talen": []}} slideshow={"slide_type": ""} -->
Emily Talen opened her 1998 article by stating that “the achievement of equity in the distribution of public resources is a goal of paramount importance to planners” (<cite id="talen"><a href="#zotero%7C6622720%2PM382J7">(Talen, 1998: 22)</a></cite>). This message resonates powerfully in the context of Cold War Aarhus. While local planners were always concerned with equitable distribution of public amenities, no planning exercise was perhaps as consequential as establishing emergency services to improve the odds of civilian survival in wartime, a task rendered urgent by the looming prospect of nuclear war and the constant risk of a Third World War. Construction of air-raid shelters had begun in Denmark during the last years of the Second World War and continued after a brief break in the wake of the Cold War. The national goals were ambitious: shelter places for everyone, day or night. To make sure this came to be, planners envisioned an overdimensioning of shelters for 200% of the population. More specifically, a shelter was to be available to all urban residents within 200-300m at all times.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
 Despite such precise benchmarks for civilian protection, however, we lack understanding of how these strategies were realised in practice: how many shelters were built, where they were built, and, not least, which assumptions and priorities guided their emplacement.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"3t1rc": [{"id": "15824328/M9TJ4CD4", "source": "zotero"}], "bjoer": [], "farba": [], "farbl": [], "farnn": [], "faror": [], "peder": [], "sylve": [], "sylvs": [], "sylvt": []}} slideshow={"slide_type": ""} -->
Unlike other NATO countries such as the US and the UK, where shelters were a matter for private (sufficiently affluent or concerned and DIY-capable) property owners, the Danish state sought to build, facilitate or impose on private contractors the duty to construct shelters to ensure complete coverage for the entire population. The aims of universal protection followed the general ambition of Danish civil defence to provide welfare even in warfare: if not total or perfect protection, then the best possible, despite the overwhelming and unprecedented threat from nuclear weapons - and despite varying political attention and funding levels (<cite id="faror"><a href="#zotero%7C15824328%2FS83XKK39">(Farbøl, 2020a)</a></cite>; <cite id="3t1rc"><a href="#zotero%7C15824328%2FM9TJ4CD4">(Bjørnsson et al., 2020)</a></cite>). Hence, as the blooming field of civil defence research has demonstrated, Danish civil defence and emergency preparedness developed into an extensive system with shelters, evacuation and emergency accommodation plans, weekly siren testings, psychological defence and media preparedness plans, educated professional and conscript civil defence personnel, a network of regional seats of government, depots and storages of everything from baby clothing to stretchers to rationing coupons (<cite id="sylve"><a href="#zotero%7C15824328%2FM3GFQX66">(Sylvest, 2018)</a></cite>; <cite id="sylvt"><a href="#zotero%7C15824328%2FARP3UTAQ">(Sylvest, 2022)</a></cite>; <cite id="sylvs"><a href="#zotero%7C15824328%2FHI5N4CRR">(Sylvest, 2020)</a></cite>; <cite id="3t1rc"><a href="#zotero%7C15824328%2FEUNFC4HT">(Bjørnsson et al., 2020)</a></cite>; <cite id="bjoer"><a href="#zotero%7C15824328%2FZDW5BRHJ">(Bjørnsson, 2020)</a></cite>; <cite id="farba"><a href="#zotero%7C15824328%2F4756RGVE">(Farbøl et al., 2024)</a></cite>; <cite id="farnn"><a href="#zotero%7C15824328%2FMHVD88GC">(Farbøl, 2022b)</a></cite>; <cite id="farbl"><a href="#zotero%7C15824328%2FQTXMU8P7">(Farbøl, 2022c)</a></cite>; <cite id="farbl"><a href="#zotero%7C15824328%2FQTXMU8P7">(Farbøl, 2022c)</a></cite>; <cite id="peder"><a href="#zotero%7C15824328%2FBASC7Z6X">(Pedersen et al., 2020)</a></cite>).
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"farbe": [], "sobot": []}} slideshow={"slide_type": ""} -->
Compared to other NATO countries, the Danish civil defence system looked impressive. However, new research suggests considerable gaps between defence plans and the reality on the ground (<cite id="farbe"><a href="#zotero%7C15824328%2FRMA6VS2U">(Farbøl, 2021)</a></cite>; <cite id="sobot"><a href="#zotero%7C15824328%2FUMD83UTK">(Sobotkova & Farbøl, forthcoming)</a></cite>). Taking the case of shelters, for instance, preliminary evidence points to broadly equitable spatial coverage of public shelters in the city centre (varying with distance from the core), but actual equity and adequacy remain unproven. Thus, it remains unclear who the protective footprint included or excluded. No complete catalog of shelters existed until the MELICA project digitized the Aarhus Civil Defence Commission archives in 2024. Now, however, with a verified dataset, we can put the implementation of national directives in Aarhus to test: did the supply meet the demand? How did urban protection play out spatially?

Civilian shelters in Denmark provide a model case for studying spatial equity in modern urban environments. Unlike everyday public facilities, civil defence shelters are called upon under extreme and urgent conditions when time and information are scarce. Under such conditions, fairness cannot be reduced to nominal proximity alone: equitable provision requires that residents, commuters, and other mobile populations can reach a shelter rapidly and that aggregate capacity is sufficient to absorb concurrent demand where it actually arises. In this sense, shelters constitute a “stress test” par excellence of urban equity: distribution must be even enough to avoid systematic exclusion, and the network must be functionally adequate when it matters most. Still, although both international Cold War civil defence and spatial equity studies are plentiful, research combining the two fields is lacking
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
## Spatial Equity
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"07rd5": [], "12gqm": [], "54i2i": [], "7d8ib": [], "9jprb": [], "abulj": [], "eadah": [], "knadq": [], "kunzm": [], "lineb": [], "lmqli": [], "neute": [], "omeri": [], "rdlza": [], "talan": [], "tsoue": []}} -->
The concept of spatial equity generally rests on the principle that all residents should be treated equally, regardless of who they are and where they live, a spatial extension of the broader notion of social equity (<cite id="lineb"><a href="#zotero%7C6622720%2F8UJADEGR">(Lineberry, 1977)</a></cite>;<cite id="kunzm"><a href="#zotero%7C6622720%2FZZZCKDM6">(Kunzmann, 1998)</a></cite>; <cite id="9jprb"><a href="#zotero%7C6622720%2FIJ8B5CBF">(Garnier, 2014)</a></cite>). While its definition varies, most studies emphasise the relationship between equity and location, and aim for the distribution of services that is equitable and correlates with the observed spatial patterns of “need” (<cite id="eadah"><a href="#zotero%7C6622720%2FJC3PUXPF">(Feitosa et al., 2024)</a></cite>; <cite id="abulj"><a href="#zotero%7C6622720%9KE5ZI6E">(Lefebvre, 1968)</a></cite>; <cite id="rdlza"><a href="#zotero%7C6622720%NBJQ333D">(Harvey, 1996)</a></cite>). In urban planning, particularly in the context of public services like hospitals (<cite id="7d8ib"><a href="#zotero%7C6622720%N8TM4I9E">(Faraji Sabokbar et al., 2021)</a></cite>), green spaces (<cite id="knadq"><a href="#zotero%7C6622720%M2685VEA">(Ma, 2020)</a></cite>;<cite id="07rd5"><a href="#zotero%7C6622720%DRI3ZNFV">(Wei, 2017)</a></cite>), playgrounds or libraries (<cite id="12gqm"><a href="#zotero%7C6622720%8954MTJU">(Taleai et al., 2014)</a></cite>), spatial equity involves ensuring equal proximity or accessibility for all residents (<cite id="54i2i"><a href="#zotero%7C6622720%K7M5TBAW">(Gandy, 2002)</a></cite>; <cite id="lmqli"><a href="#zotero%7C6622720%MN6ANFTM">(Werna, 2000)</a></cite>). Accessibility indices have become the dominant method for measuring such equity (<cite id="talan"><a href="#zotero%7C6622720%4RQSDRZH">(Talen and Anselin, 1998)</a></cite>; <cite id="tsoue"><a href="#zotero%7C6622720%MG434KTD">(Tsou et al., 2005)</a></cite>;<cite id="neute"><a href="#zotero%7C6622720%CJACW6S7">(Neutens et al., 2010)</a></cite>; <cite id="12gqm"><a href="#zotero%7C6622720%8954MTJU">(Taleai et al., 2014)</a></cite>), though the concept also includes dimensions like facility capacity, service adequacy, and the ability to meet peak demand, particularly critical in the case of emergency infrastructure (<cite id="omeri"><a href="#zotero%7C6622720%J43U2K9P">(Omer, 2006)</a></cite>).
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"kwan1": [], "kwan2": [], "mille": [], "neute": [], "ogryc": [], "talan": [], "talen": [], "tsoue": [], "weber": []}} -->
This paper focuses on accessibility and this concept’s operationalisation as a place-based measure (<cite id="talen"><a href="#zotero%7C6622720%2PM382J7">(Talen, 1998)</a></cite>;<cite id="talan"><a href="#zotero%7C6622720%4RQSDRZH">(Talen and Anselin, 1998)</a></cite>;<cite id="ogryc"><a href="#zotero%7C6622720%SP6SKPWN">(Ogryczak, 2000)</a></cite>;<cite id="neute"><a href="#zotero%7C6622720%CJACW6S7">(Neutens et al., 2010)</a></cite>). Place-based measures evaluate accessibility from fixed locations such as residences or workplaces and include coverage measures (percentage of population within a threshold distance), proximity measures (distance to nearest facility), and gravity-based measures (facility attractiveness, such as type or capacity, is measured against distance decay) (<cite id="mille"><a href="#zotero%7C15824328%2FT5QIET3N">(Miller, 2007)</a></cite>; <cite id="talan"><a href="#zotero%7C6622720%4RQSDRZH">(Talen and Anselin, 1998)</a></cite>; <cite id="tsoue"><a href="#zotero%7C6622720%MG434KTD">(Tsou et al., 2005)</a></cite>). Accessibility can also be operationalised through person-based measures, which account for individual mobility patterns and time constraints (<cite id="kwan1"><a href="#zotero%7C6622720%CA8UMNT7">(Kwan, 1999)</a></cite>;<cite id="kwan2"><a href="#zotero%7C6622720%G8RCX3KI">(Kwan, 2000)</a></cite>;<cite id="neute"><a href="#zotero%7C6622720%CJACW6S7">(Neutens et al., 2010)</a></cite>;<cite id="weber"><a href="#zotero%7C6622720%9MH83834">(Weber, 2003)</a></cite>). While person-based measures are more nuanced and qualitatively superior to place-based measures and more feasible given the computational power of geographic toolkits today, such individual measures were hardly available to the mid-century urban planners. Archival sources show that objectives were mostly articulated in terms of distance and time:
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"eschu": []}} slideshow={"slide_type": ""} -->
> “In Denmark, only a very short period can be expected between the air-raid warning and the overflight. Public shelters must therefore be distributed throughout the densely built-up areas so that people can reach cover quickly. The shelters should be located in such a way that, when the civil defence system is fully developed, the distance to a public shelter is, as far as possible, no more than 300 meters.”

> *Original (Danish):*  
> “Da der i Danmark kun kan regnes med et ganske kort tidsrum mellem luftalarmen og overflyvningen, må de offentlige beskyttelsesrum være spredt inden for det tæt bebyggede område, således at det er muligt hurtigt at nå i dækning. Rummene bør placeres således, at der ved den endelige udbygning af beredskabet så vidt muligt ikke er mere end 300 m’s afstand til et offentligt beskyttelsesrum" (<cite id="eschu"><a href="#zotero%7C15824328%2FP7JZZXNL">(Schultz, 1950, 10)</a></cite>).

Desirable shelter placement in 1950s’ sources often takes the form of ‘within a short walk’ or ‘short time’. The language is generic but mostly deals with distances and places. We therefore utilise compatible measures in our evaluation.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"7d8ib": [], "970ye": [{"id": "6622720/SCHC3PRS", "source": "zotero"}], "abulj": [{"id": "6622720/NBJQ333D", "source": "zotero"}], "lxn9v": [{"id": "6622720/95SGSHZX", "source": "zotero"}], "rao58": [{"id": "6622720/8JF2XJXH", "source": "zotero"}], "rdlza": [{"id": "6622720/9KE5ZI6E", "source": "zotero"}]}} slideshow={"slide_type": ""} -->
In the past two decades, rising concern over social justice has sharpened attention to the multiple dimensions of spatial equity. Researchers now distinguish several different perspectives. Horizontal equity asks whether comparable populations receive comparable levels of service, while vertical equity considers whether groups with greater needs — such as residents of high-density or vulnerable areas — receive proportionally more resources. Territorial equity focuses on the evenness of provision across geographic areas, and social equity on whether disadvantaged populations enjoy adequate access (<cite id="7d8ib"><a href="#zotero%7C15824328%2FQGRQ6CGM">(Faraji Sabokar et al., 2021)</a></cite>; <cite id="rao58"><a href="#zotero%7C6622720%2F5AUZVSGM">(He et al., 2020)</a></cite>). Most of these perspectives seek to redress gaps and disadvantage, reflecting a Marxist view of equity, which compels the public sector to favor the “needy” (<cite id="rdlza"><a href="#zotero%7C6622720%2FCZRUWJAM">(Harvey, 1996)</a></cite>; <cite id="abulj"><a href="#zotero%7C6622720%2FEDFZWXEC">(Lefebvre, 1968)</a></cite>) in order to balance the tendencies which favor pro-development, efficiency and utility- or entitlement-based allocation (<cite id="970ye"><a href="#zotero%7C6622720%2FSCHC3PRS">(Dynes, 2020)</a></cite>; as evidenced by spending studies in e.g. <cite id="lxn9v"><a href="#zotero%7C6622720%2F95SGSHZX">(Talen &#38; Anselin, 2021)</a></cite>).

In the context of civil defence in Denmark, all these dimensions intersect. A spatially equitable shelter system should ensure citywide coverage (territorial equity), maintain capacity commensurate with population density (horizontal equity), and, where possible, prioritise dense areas and those less able to reach safety quickly (vertical equity). Mid-century urban planners may not have used any of these recent terms but their agenda nonetheless aimed at universal and equitable results (maximising population protection), raising the question of: what did equity mean to them? 

Whereas the ambition of universal coverage, indeed, of providing shelters for 200% of the population, suggests that hard decisions of whom to include or exclude in the protective footprint were irrelevant - because everybody would have access to at least one shelter - the reality on the ground was different. Planners had to face the task of where to locate shelters. But what assumptions and priorities guided them? Was their notion of equity shaped by the principle of merit, need or utility? Were shelters located where they presumably were going to be needed the most, where vociferous groups advocated emplacement or simply where space was available?

<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
## Methods and Data
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"talen": []}} slideshow={"slide_type": ""} -->
In this paper we evaluate the equal distribution of Cold War civilian shelters using place-based accessibility measures, evaluating the proximity of the nearest sheltering facility to the workplaces and homes in Aarhus during 1951. Specifically, we assess (1) shelter coverage, i.e. what percentage of houses in Aarhus have civil defence facilities within the critical distance of 300m; (2) minimum distance distribution: the spread of distances to the nearest facility; and (3) a gravity model where the accessibility score factors in shelter attractiveness (i.e. its type or capacity) against the friction of its distance from the building served (<cite id="talen"><a href="#zotero%7C6622720%2FPJUMB8EA">(Talen, 1998)</a></cite>). These are computationally simple and widely used measures, whose main downside is that they tend to ignore the dynamic and individualised constraints of daily life - such as limited time windows, limited knowledge (not knowing where a shelter is during an errand to a new part of town) and complex travel patterns (e.g. the compulsion to fetch one’s children before sheltering). Although these measures ignore individual behaviour and constraints, they provide a glimpse into the baseline shelter provision in Aarhus, emphasising relational accessibility rather than absolute precision.  Moreover, we seek to take a reflexive approach that transforms anachronism into analytical transparency. We provide reproducible, city-wide metrics of spatial friction and equity while acknowledging epistemic limits.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Specifically, Aarhus city planners in the 1940s and 1950s did not have the computational capacity to calculate individual travel preferences or times, as evidenced by the suburb-based aggregate numbers of residents and shelter places visible in the archive of the Civil Defence Commission. They relied on aggregate spatial indices for buildings and population, and on distance-based planning standards with the 300-meter benchmark being the most explicit. By evaluating the implemented shelter network using place-based accessibility measures, we assess it on its own terms, asking whether the planning goals were achieved according to the criteria planners themselves would have recognised. 
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Shelters and Buildings
<!-- #endregion -->

Denmark employed several shelter types, but only a subset is relevant from a 1951 vantage point. Foremost among these were the public shelters called "concrete cover trenches" (*Betondækningsgrave*, BDG). These were each sized for about fifty occupants and aimed principally at commuters and others caught in public spaces. This type of shelter was primarily built during the last years of the Second World War, but the Korean War sparked a new round of shelter building. In 1951, 301 concrete cover trenches existed in Aarhus. Although the strategic environment had shifted with the advent of nuclear weapons, contemporary assessments by the Danish Civil Defence Directorate held that these trenches, while never bomb-proof, offered reasonable protection against heat, blast, and initial radiation—so long as they lay beyond a weapon’s immediate blast radius. 

Public provision alone, however, could not keep pace with demographic growth. Aarhus’s population rose from about 50,000 in 1901 to over 150,000 by 1950, with further increases anticipated. A 1950 building law therefore introduced a second pillar: “reinforced rooms” (*Sikringsrum*, SR) in the basements of new multi-family dwellings, workplaces with ten or more employees, and public institutions. These privately provided shelters were intended for people likely to be at home or at work at the moment of alarm; in peacetime, they could serve routine functions (e.g., storage) provided they could be made shelter-ready within twenty-four hours. In 1951, only 17 such private shelters existed in Aarhus.

<!-- #region citation-manager={"citations": {"erbbr": [], "erfil": []}} slideshow={"slide_type": ""} tags=["hermeneutics"] -->
The shelter data in the study had been digitized during 2024-2025 from the Civil Defence Commission (CDC) collection held at the Aarhus City Archive (see [Figure 1](#m_overview)). We traced each public shelter (BDG) location through the archival documents. Locations were then geocoded, verified in historical maps, archival photographs, and historical satellite imagery (in Google Earth Pro). Surviving shelters were documented by teams of students during field visits. Private shelter (SR) locations were extracted from the archival documents and cross-checked against a historical version of the Building Register of Denmark (BRD), which the BRD team generated on our request. Building centroids for the 1950s urban layout were also acquired from the BRD, which offers an open dataset of all buildings in Denmark online (<cite id="erbbr"><a href="#zotero%7C15824328%2FDS3A7BAH">(Erhvervsstyrelsen, n.d.-a)</a></cite>; <cite id="erfil"><a href="#zotero%7C15824328%2FFRCF6BPE">(Erhvervsstyrelsen, n.d.-b)</a></cite>). We acquired the 1951 state of Aarhus by downloading the 2023 version of the BRD register, selecting centroids that fell within the 1952 urban boundary of Aarhus, digitized from a historical map of the town, and filtering for building construction dates that predated 1952. 
<!-- #endregion -->

### Road Network and Distance Measurements

<!-- #region citation-manager={"citations": {"barre": [], "jeffe": [], "vande": [], "weyen": []}} slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Our analysis models distances between buildings and civil defence shelters in Aarhus using both Euclidean and network measures. No digital road network from the early 1950s exists and reconstructing a “1952” network from historical maps is challenging due to the requirement for intersecting line geometries and full connectivity - conditions impossible to guarantee and likely to produce false precision. We instead opted to use the modern OpenStreetMap (OSM) network as a consistent spatial proxy for pedestrian movement.  We extracted road data from OSM for Aarhus municipality using the *osmdata* R package and clipped them to the 1951 urban boundary. We then combined road geometries and streamlined them into a network using *sfnetworks* R package (<cite id="vande"><a href="#zotero%7C15824328%2F3M5KJQ94">(van der Meer et al., 2024)</a></cite>). This network served as the foundation for calculating network distances between buildings and shelters. While the shelter and building data offer a reasonable approximation of 1950s conditions, the road network is modern. This obviously presents a challenge for a historically accurate survey of network distances, yet the use of a contemporary digital network can be justified within a reflexive methodological framework. 

The study assumes short-range evacuation on foot (within 300–500 m), where the precise vintage of the network has a limited effect compared to its topological completeness. Even contemporary OSM data leaves about sixty buildings disconnected despite extensive cleaning and snapping, and a reconstructed version would introduce far greater uncertainty. The modern network reproduces the city’s enduring core structure - radial roads, inner ring road and the downtown grid, which has remained largely unchanged since before 1952 - while later additions (outer ring roads, motorways) mainly influence car travel, which is beyond our analytical scale. For pedestrians, these changes either have a negligible impact or slightly increase friction, making the modern model a conservative approximation of historical access. 

To handle spatial uncertainty explicitly, we pair Euclidean and network distances. While Euclidean distances exaggerate coverage and offer an optimistic scenario, network distances suppress coverage, offering a more realistic, if occasionally too pessimistic, reading. The true 1951 accessibility lies somewhere between these two poles. By presenting both, we bracket the plausible range rather than claiming deterministic accuracy.

All spatial processing and mapping was carried out in R. Locational data on buildings, roads, public and private shelter facilities in Aarhus in 1951 were imported, distance measurements performed, and accessibility scores generated following established mathematical expressions, with code available in Github. Given the large size of the resulting network, packages such as *data.table*, *RANN*, and *kdetrees* were used to efficiently generate distance matrices (<cite id="barre"><a href="#zotero%7C15824328%2F8K3PTJQI">(Barrett et al., 2025)</a></cite>;<cite id="jeffe"><a href="#zotero%7C15824328%2FUSP3FTAI">(Jefferis et al., 2024)</a></cite>;<cite id="weyen"><a href="#zotero%7C15824328%2FC668RPSB">(Weyenberg, 2014)</a></cite>). The resulting maps elucidate the spatial relationships between historical need and service distribution, highlighting spatial gaps and incongruities.
<!-- #endregion -->

```python slideshow={"slide_type": ""}
## LOADING IN DATA

import geopandas as gpd
import pandas as pd
import numpy as np

# ==== CORE DATA ====

buildings = gpd.read_file('script/buildings.gpkg')                               # Buildings

aarhus_city1952 = gpd.read_file('script/aarhus_city1952.gpkg')                   # Aarhus Municipal Boundaries

shelters = gpd.read_file('script/shelters.gpkg')                                 # Combined Shelters Dataset

# ==== DISTANCE MATRIX ====

dma = pd.read_csv('script/dma.csv')

# Merge geometry
dma = dma.merge(buildings[['id_lokalId', 'geometry']], 
                left_on='building_id', 
                right_on='id_lokalId', 
                how='left')
dma = gpd.GeoDataFrame(dma, geometry='geometry', crs=buildings.crs)

# Filter for valid data
dma = dma[
    (dma['net_m'].notna()) &
    (dma['euclid_distance'].notna()) &
    (dma['net_m'] != np.inf) &
    (dma['shelter_id'].isin(shelters['shelterID']))
].copy()

# ==== ANALYSIS SETUP ====

# For initial use (transformed later as needed)
# Transform to EPSG:25832 for analysis
buildings = buildings.to_crs('EPSG:25832')
aarhus_city1952 = aarhus_city1952.to_crs('EPSG:25832')
shelters = shelters.to_crs('EPSG:25832')
dma = dma.to_crs('EPSG:25832')

# Spatial trim
dma = dma[dma.geometry.notna()].copy()
dma = dma[dma.within(aarhus_city1952.union_all())].copy()
```

```python jdh={"object": {"source": ["Public and private shelter distribution in Aarhus, Denmark, in 1951; dots mark the footprints of extant buildings within the city\u2019s historical boundary."]}} slideshow={"slide_type": ""} tags=["figure-aarhus-1951-overview-*"]
import folium
from folium import plugins

# ==== SETUP ====

# Filter to only buildings and shelters WITHIN city boundary
buildings_in_city = buildings[buildings.within(aarhus_city1952.union_all())].copy()
shelters_in_city = shelters[shelters.within(aarhus_city1952.union_all())].copy()

# Convert to EPSG:4326 for mapping
buildings_map = buildings_in_city.to_crs('EPSG:4326')
shelters_map = shelters_in_city.to_crs('EPSG:4326')
aarhus_map = aarhus_city1952.to_crs('EPSG:4326')

# Separate shelters by type for mapping
bdg_shelters = shelters_map[shelters_map['shelter_type'] == 'BDG'].copy()
sr_shelters = shelters_map[shelters_map['shelter_type'] == 'SR'].copy()

# ==== CONSTRUCT MAP ====

# Create base map
m_overview = folium.Map(location=[56.16, 10.20],
                        zoom_start=12,
                        tiles=None,
                        control_scale=True)

# Add tile layers for different viewing options
folium.TileLayer(
    tiles='https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}',
    attr='Esri',
    name='Esri WorldImagery',
    overlay=False,
    control=True
).add_to(m_overview)

folium.TileLayer('OpenStreetMap', name='OpenStreetMap').add_to(m_overview)
folium.TileLayer('CartoDB dark_matter', name='CartoDB Dark').add_to(m_overview)
folium.TileLayer('CartoDB Positron', name='CartoDB Positron').add_to(m_overview)

# Add city boundary
folium.GeoJson(
    aarhus_map,
    style_function=lambda x: {
        'fillColor': 'white',
        'color': 'darkgrey',
        'weight': 1,
        'fillOpacity': 0.5
    }
).add_to(m_overview)

# Add buildings
for _, row in buildings_map.iterrows():
    # Create popup with ALL available building info
    popup_text = f"""
        <div style='font-family: Arial; font-size: 12px;'>
            <b>Building</b><br><br>
            <b>Year Built:</b> {int(row['byg026Year']) if pd.notna(row['byg026Year']) else 'Unknown'}<br>
            <b>Floors:</b> {int(row['byg054AntalEtager']) if pd.notna(row['byg054AntalEtager']) else 'Unknown'}<br>
            <b>Est. Population:</b> {int(row['est_pop']) if pd.notna(row['est_pop']) else 'Unknown'}<br><br>
            <b>City:</b> {row['city'] if pd.notna(row['city']) else 'Unknown'}<br>
            <b>Coordinate System:</b> {row['byg406Koordinatsystem'] if pd.notna(row['byg406Koordinatsystem']) else 'Unknown'}<br><br>
            <b>Code:</b> {row['Code'] if pd.notna(row['Code']) else 'Unknown'}<br>
            <b>ID:</b> {row['id_lokalId']}<br>
        </div>
    """
    
    folium.CircleMarker(
        location=[row.geometry.y, row.geometry.x],
        radius=0.7,
        color='steelblue',
        opacity=0.4,
        fill=True,
        fillColor='skyblue',
        fillOpacity=0.3,
        weight=0.3,
        popup=folium.Popup(popup_text, max_width=250)
    ).add_to(m_overview)

# Add BDG (public) shelters
for i, (idx, row) in enumerate(bdg_shelters.iterrows()):
    # Scale radius by capacity
    base_radius = np.sqrt(row['Seats']) * 0.8
    
    # Handle numeric shelter ID and store as string
    if pd.notna(row['shelterID']) and row['shelterID'] != '':
        shelter_id_value = str(row['shelterID'])
    else:
        shelter_id_value = 'Unknown'
    
    popup_text = f"""
    <div style='font-family: Arial; font-size: 12px;'>
        <b>Public Shelter (BDG)</b><br><br>
        <b>Capacity:</b> {int(row['Seats'])} seats<br>
        <b>Year:</b> {int(row['Year']) if pd.notna(row['Year']) else 'Unknown'}<br><br>
        <b>Shelter ID:</b> {shelter_id_value}<br>
    </div>
    """
    
    folium.CircleMarker(
        location=[row.geometry.y, row.geometry.x],
        radius=base_radius,
        color='lightseagreen',
        fill=True,
        fillColor='mediumaquamarine',
        fillOpacity=0.7,
        weight=1.5,
        popup=folium.Popup(popup_text, max_width=250)
    ).add_to(m_overview)

# Add SR (private) shelters
for i, (idx, row) in enumerate(sr_shelters.iterrows()):
    # Scale radius by capacity
    base_radius = np.sqrt(row['Seats']) * 0.8
    
    # Show shelter ID
    if pd.notna(row['shelterID']) and row['shelterID'] != '':
        shelter_id_value = str(row['shelterID'])[:].upper()
    else:
        shelter_id_value = 'Unknown'
    
    popup_text = f"""
    <div style='font-family: Arial; font-size: 12px;'>
        <b>Private Shelter (SR)</b><br><br>
        <b>Capacity:</b> {int(row['Seats'])} seats<br>
        <b>Year:</b> {int(row['Year']) if pd.notna(row['Year']) else 'Unknown'}<br><br>
        <b>Shelter ID:</b> {shelter_id_value}<br>
    </div>
    """
    
    folium.CircleMarker(
        location=[row.geometry.y, row.geometry.x],
        radius=base_radius,
        color='#CC8800',
        fill=True,
        fillColor='#FFA500',
        fillOpacity=0.7,
        weight=1.5,
        popup=folium.Popup(popup_text, max_width=250)
    ).add_to(m_overview)

# Add layer control to LEFT corner (collapsed by default)
folium.LayerControl(collapsed=True, position='topleft').add_to(m_overview)

# Add fullscreen button
plugins.Fullscreen().add_to(m_overview)

# Add minimap
minimap = plugins.MiniMap(toggle_display=True, position='bottomleft')
m_overview.add_child(minimap)

# Add legend
legend_html = '''
<div style="position: fixed; top: 10px; right: 10px; background-color: white; 
     border:2px solid grey; z-index:9999; padding: 10px; font-size: 12px;">
<p style="margin: 0 0 10px 0; font-weight: bold;">private / SR</p>
<p style="margin: 2px 0;"><span style="color:#FFA500; font-size: 14px;">●</span> 100</p>
<p style="margin: 2px 0;"><span style="color:#FFA500; font-size: 18px;">●</span> 200</p>
<p style="margin: 2px 0;"><span style="color:#FFA500; font-size: 22px;">●</span> 300</p>
<p style="margin: 2px 0;"><span style="color:#FFA500; font-size: 26px;">●</span> 400</p>
<p style="margin: 2px 0;"><span style="color:#FFA500; font-size: 30px;">●</span> 500</p>
<p style="margin: 15px 0 5px 0; font-weight: bold;">public / BDG</p>
<p style="margin: 2px 0;"><span style="color:mediumaquamarine; font-size: 16px;">●</span> 50-100</p>
</div>
'''
m_overview.get_root().html.add_child(folium.Element(legend_html))

# ==== SAVE FIGURE ====

m_overview.save('media/m_overview_interactive.html')
```

<a id='m_overview'></a>

```python
from IPython.display import HTML
HTML('''
<iframe
    src="./media/m_overview_interactive.html"
    width="100%"
    height="600"
    style="border: 0;"
    loading="lazy"
    referrerpolicy="no-referrer"
>    
</iframe>
''')
```

<!-- #region slideshow={"slide_type": ""} -->
## Results
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
The results and maps presented illustrate different aspects of accessibility to civil defence shelters in Aarhus in 1951. We evaluate whether shelters were present everywhere within the cut-off distance of 300m as specified by the civil defence; we quantify how many amenities were available within this threshold and we map the variation in minimum distance to nearest shelter across town. Euclidean and network distance measures appear side-by-side allowing the reader to gauge the difference arising from the two different conceptualisations of travel. Three overall conclusions emerge from the coverage and minimum distance patterns, first that shelter accessibility favours the city’s historical core - within the inner Ring road - over the peripheral areas, and, second, that shelter provision is far from adequate, but, third that the difference in provision is consistent with the vertical perspective of spatial equity.

Looking at Aarhus in 1951, [Figure 1](#m_overview) shows the configuration of private (SR) and public (BDG) shelters within the urban fabric.  The downtown is shaped as a semicircle of 1.5 km radius centred on the historical harbour, roughly at the intersection of the numerous protruding piers and harbour extensions. Urban growth extends in all directions from this core avoiding existing parks and forests as well as swamp- and flooding-prone areas.  While the private shelters are few and far between, numbering some 17 locations at this time, public shelters are abundant, especially in the downtown area, numbering 301 in total. Most co-locate with the dense city centre, serving the high-rise buildings and associated arteries. The white areas, devoid of both kinds of shelters, are usually building-free areas on the edges of the urban sprawl or parks, forests, cemeteries or other infrastructure (Moesgaard forest stretching south of the city along the beach, the Risskov forest to the north, undeveloped land in Vejlby, the harbour). At first glance, the downtown features a dense protective net of shelters, which grows progressively thinner as it stretches to the outskirts of the city, the villa suburbs and newly developed areas in the southwest, west and north. 

<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Who is within the threshold distance?
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
The maps of shelter coverage in [Figure 2](#m_binary_threshold) indicate that when it comes to having a shelter within 300m of a location, the downtown area is mostly better covered than the southern, western and northern suburbs, at least if we use Euclidean distance as the measuring stick. With few exceptions, the buildings in the “latin quarter” of the city center as well as in the old working class areas Trøjborg, Frederiksbjerg and Øgaderne live up to the national aims. The network model complicates the picture, showing many more ‘uncovered’ red buildings in the map, both in the downtown and towards the periphery. The newly developed villa areas of Hasle, Aarhus N and Åby present seas of “at risk” buildings no matter the model. The formal assessment of shelter provision within the threshold distance of 300m shows that 52% of buildings are within the threshold, while 47% fall outside if we look at the network model. Euclidean obstacle-free distance makes the situation seem less bad: 77% of buildings make it within the 300m limit, and only 23% lack coverage, being more than 300m away.  Which of these scenarios should we trust? Which is correct? 
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Both models are wrong, and their results need to be taken with a grain of salt. Each model comes from a different end of the realism spectrum. Euclidean measures represent theoretical distance calculated either along a straight line from point A to point B, or as a radius from a given building. It is the most basic model of distance, and one that is simplistic except in open landscapes and where people have grown wings.
<!-- #endregion -->

```python slideshow={"slide_type": ""}
# ==== COVERING MODEL - BINARY 300M THRESHOLD ====

import pandas as pd

# ==== SETUP ====

# For each building, pick the record with shortest distance for BOTH types

buildings_by_eucdistance = (
    dma.sort_values('euclid_distance')
    .groupby('building_id', as_index=False)
    .first()
)

buildings_by_netdistance = (
    dma.sort_values('net_m')
    .groupby('building_id', as_index=False)
    .first()
)

# Create distance groups function
def assign_distance_group(dist):
    if pd.isna(dist):
        return None
    elif dist <= 200:
        return "0–200m"
    elif dist <= 300:
        return "201–300m"
    else:
        return ">300m"

# Apply to euclidean distance data
buildings_by_eucdistance['distance_group'] = buildings_by_eucdistance['euclid_distance'].apply(assign_distance_group)
buildings_by_eucdistance['distance_group'] = pd.Categorical(
    buildings_by_eucdistance['distance_group'],
    categories=["0–200m", "201–300m", ">300m"],
    ordered=True
)

# Apply to network data
buildings_by_netdistance['distance_group'] = buildings_by_netdistance['net_m'].apply(assign_distance_group)
buildings_by_netdistance['distance_group'] = pd.Categorical(
    buildings_by_netdistance['distance_group'],
    categories=["0–200m", "201–300m", ">300m"],
    ordered=True
)

# ==== RISK ASSESSMENT ====

# Safe (<300m) / At Risk (>300)
def assign_risk(distance_group):
    if distance_group in ["0–200m", "201–300m"]:
        return "Safe (≤300 m)"
    elif distance_group == ">300m":
        return "At Risk (>300 m)"
    else:
        return None

# ==== RISK ASSESSMENT: EUCLIDEAN DISTANCE ====

# Add risk category to Euclidean distance data
buildings_by_eucdistance['risk'] = buildings_by_eucdistance['distance_group'].apply(assign_risk)

# Make categorical with proper ordering
buildings_by_eucdistance['risk'] = pd.Categorical(
    buildings_by_eucdistance['risk'],
    categories=["Safe (≤300 m)", "At Risk (>300 m)"],
    ordered=True
)

# ==== RISK ASSESSMENT: NETWORK DISTANCE ====

# Add risk category to network distance data
buildings_by_netdistance['risk'] = buildings_by_netdistance['distance_group'].apply(assign_risk)

# Make categorical with proper ordering
buildings_by_netdistance['risk'] = pd.Categorical(
    buildings_by_netdistance['risk'],
    categories=["Safe (≤300 m)", "At Risk (>300 m)"],
    ordered=True
)
```

```python jdh={"object": {"source": ["Data source: MELICA, DBR, OSM 2025"]}} tags=["figure-binary-threshold-*"]
# ==== BINARY THRESHOLD COMBINATION MAP ====

import matplotlib.pyplot as plt
import matplotlib.ticker as ticker
import geopandas as gpd
import pandas as pd
from IPython.display import Image, display

# ==== SETUP ===

# Unified Dataset
## Select relevant columns and standardize field names
euclid_sf = buildings_by_eucdistance[['building_id', 'euclid_distance', 'distance_group', 'risk', 'geometry']].copy()
euclid_sf = euclid_sf.rename(columns={'euclid_distance': 'distance_m'})
euclid_sf['distance_type'] = "Euclidean"

network_sf = buildings_by_netdistance[['building_id', 'net_m', 'distance_group', 'risk', 'geometry']].copy()
network_sf = network_sf.rename(columns={'net_m': 'distance_m'})
network_sf['distance_type'] = "Network"

## Combine both datasets
distance_compare_sf = pd.concat([euclid_sf, network_sf], ignore_index=True)
distance_compare_sf = gpd.GeoDataFrame(distance_compare_sf, geometry='geometry', crs='EPSG:25832')

# ==== CONSTRUCT MAP ====

distance_compare_sf = distance_compare_sf.to_crs('EPSG:4326')

# Initialize map
fig, axes = plt.subplots(1, 2, figsize=(16, 10))

# Color mapping
colors = {"Safe (≤300 m)": "lightblue", "At Risk (>300 m)": "red"}

# ==== LEFT: EUCLIDEAN ====

euclid_data = distance_compare_sf[distance_compare_sf['distance_type'] == 'Euclidean']
for risk_val, color in colors.items():
    subset = euclid_data[euclid_data['risk'] == risk_val]
    subset.plot(ax=axes[0], color=color, markersize=0.6, alpha=0.9, label=risk_val)

axes[0].set_title('Euclidean Distance', fontsize=12, fontweight='bold')

# ==== RIGHT: NETWORK ====

network_data = distance_compare_sf[distance_compare_sf['distance_type'] == 'Network']
for risk_val, color in colors.items():
    subset = network_data[network_data['risk'] == risk_val]
    subset.plot(ax=axes[1], color=color, markersize=0.6, alpha=0.9, label=risk_val)

axes[1].set_title('Network Distance', fontsize=12, fontweight='bold')

# ====  ADD FEATURES TO BOTH PLOTS ====

for idx, ax in enumerate(axes):
    
    # Set labels
    ax.set_xlabel('Longitude')
    
    # Format coordinates
    ax.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, p: f'{x:.2f}°E'))
    if idx == 0:  # Only show y-axis ticks on left plot
        ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda y, p: f'{y:.2f}°N'))
        ax.set_ylabel('Latitude')
    else:
        ax.set_yticklabels([])  # Hide y-axis labels on right plot for neater layout
        ax.tick_params(left=False)
        
    # Remove frame
    for spine in ax.spines.values():
        spine.set_visible(False)

    # Add grid to background
    ax.grid(True, alpha=0.3, linestyle='-', linewidth=0.5)

# Add overall title
fig.suptitle('Comparison of Shelter Coverage by Distance (1951)', 
             fontsize=14, fontweight='bold', y=1.01)

# Add subtitle
fig.text(0.5, 0.96, 'Buildings beyond the 300m threshold are shown in red', 
         ha='center', fontsize=11, fontweight='normal')

# Create single legend for both plots
handles, labels = axes[0].get_legend_handles_labels()
fig.legend(handles, labels, loc='upper center', bbox_to_anchor=(0.53, 0.95), 
           title='Distance Threshold', title_fontsize=12, fontsize=12, markerscale=5,
           frameon=True, edgecolor='black')

plt.subplots_adjust(hspace=0.03)
plt.tight_layout(rect=[0, 0.03, 1, 0.93])

# ==== SAVE FIGURE ====

plt.savefig('media/m_binary_threshold.png', dpi=400, bbox_inches='tight')
plt.close()
```

<a id='m_binary_threshold'></a>

```python
display(Image('media/m_binary_threshold.png'))
```

<!-- #region slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Network distances are longer, sometimes twice as long as Euclidean distances, for most building-shelter pairs in Aarhus. This is because, unlike the “as-the-crow-flies” distance, they are more realistic in that they follow the existing grid of roads and paths. They mimic actual walking around buildings and obstacles rather than flying through buildings. Following paths and road networks, however, is not what human pedestrians always do. Sometimes it leads to exaggerated distance - especially at short scale and in the historical downtown, where local inhabitants may know and use passages through buildings, which are not logged in the OpenStreetMap (OSM) network. Sometimes the network distances underestimate reality. In long transfers across town, for example, modern thoroughfares have increased connectivity where none existed in 1951.  Both have shortcomings, and we work with both because we recognize that the reality is hidden somewhere in between. Moreover, it is not clear from the historical sources how civil defence calculated the 200-300 meter distance, whether Euclidean or network.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"farbe": [], "soros": []}} slideshow={"slide_type": ""} -->
According to [Figure 2](#m_binary_threshold), 50% coverage is the worst-case (network-distance) scenario in Aarhus of 1951. The saving grace to the dire percentage is that the insufficiency is distributed fairly evenly throughout the city. Gaps are everywhere, but shelters are too. Red spots in the downtown network scenario are particularly interesting as they point to considerable amounts of friction. Buildings in the city centre are clustered in blocks with paths on the outside, demanding that one turns many corners to get to a shelter location, even if it is at a relatively short radius. Yet, Aarhus downtown is not that impermeable, with lots of shortcuts facilitating fluid pedestrian movement in the historical centre. The extended distances in the downtown partially arise from the representation of the road network, which puts emphasis on vehicular movement and may be less ‘aware’of / informed by the pedestrian possibilities.  The lived reality of historic city centres is that there is more than one way to get to any place. In an emergency, local residents in Aarhus would have used bikes or run, treading paths across lawns where convenient, taking narrow passages or passing through multiple entryways as shortcuts between streets and buildings, and this pedestrian efficacy is likely lost in the OSM network, whose creation mostly relies on vehicle-based route registration. To justify the OSM product, however, we must admit that the habitus of city dwellers and their tight control of local space has not been put to the test under an emergency, and so we do not know which of the two scenarios is more probable.

The reality check comes when we review shelter capacity.  The aggregate number of places shelters offer is just around ~17,000, which covers some 11% of the Aarhus population (150,000 in 1951). This means that even if most could reach a shelter within the mandated distance (and therefore escape time), many would have found no place inside because the shelter would already be full. Of the total shelter place number, ~15,000 places were in the public shelters (BDGs), located in the space between buildings for people on-the-go, along major roads, at the entrances to schools and public spaces. Private shelters (SRs), basements, garages and other reinforced rooms that serve families at home or workers in factories and offices, offered only two thousand places at this time, pointing to another axis of inequity. While kids in urban schools and workers doing business in the downtown had a choice of shelters available, housewives with small kids in the peripheries were likely left to their own devices. 

Civil defence planners were aware of the problem. The far-less-than-optimal capacity figures likely catalysed the construction of large-capacity public combined shelters in Aarhus during the 1950s and 1960s (<cite id="farbe"><a href="#zotero%7C15824328%2FRMA6VS2U">(Farbøl, 2021)</a></cite>; <cite id="soros"><a href="#zotero%7C15824328%2F7BQTHZ78">(Sobotkova & Farbøl, 2025)</a></cite>). These shelters could accommodate hundreds, even in some cases thousands of people at a time, and solved some of the bottleneck problems that would have arisen as panic-stricken residents flooded the BDG doors. While combined public shelters eventually alleviated the pressure on downtown facilities, the suburbs and their protection were left to the incentive of individual households and household organisations (“if they can afford a villa, they can organise to build a shelter”) or to the economic power of development. Private shelter construction followed the ordinary building activity, leading to constantly rising numbers until the mid 1990s. This two-prong solution eventually solved the adequacy and proximity problem across the 1951 suburb.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### How far to the nearest shelter? 
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
Let us look at Aarhus from yet another perspective. Given that the shelter capacity was a bigger problem than distance, it is perhaps fair to assume that only individuals from the closest proximity could have found a spot in the shelter, even in the best-provided areas. To represent spatial proximity, we need more than a binary Safe/At Risk map. 
[Figure 3](#m_dmin_with_threshold) refines the picture by mapping minimum distance to the nearest shelter. Dark blues mark areas close to a shelter; greens show locations farther away but still within the 300 m threshold; reds fall outside it. In the Euclidean model, the downtown forms a dense blue-green mosaic where multiple shelter catchments overlap, leaving few genuine gaps. Along the southern and northern fringes, however, those colours thin into isolated halos - indicating lone installations scattered across the periphery rather than a coherent safety network.
The network-distance panel tightens the screws. Red areas expand, indicating reduced coverage once street geometry is taken into account. Short-distance blues also contract, showing how quickly accessibility decays under network conditions. Compared with the more forgiving Euclidean model, the network view exposes both central and peripheral weaknesses more sharply, revealing a system far less cohesive once real travel paths are considered.
<!-- #endregion -->

```python jdh={"object": {"source": ["Data source: MELICA, DBR, OSM 2025"]}} slideshow={"slide_type": ""} tags=["figure-dmin-w-threshold-*"]
# ==== DMIN MAP WITH THRESHOLD ====

import matplotlib.pyplot as plt
import pandas as pd
import warnings
warnings.filterwarnings("ignore")

# ==== SETUP ====

# We use the combined dataset we created earlier
# distance_compare_sf has both Euclidean and Network with 'distance_m' column

# ==== CONSTRUCT FIGURE ====

# Initialize plot
fig, axes = plt.subplots(1, 2, figsize=(16, 10))
max_dist = distance_compare_sf['distance_m'].max()

for idx, dist_type in enumerate(['Euclidean', 'Network']):
    ax = axes[idx]
    
    # Get data for this distance type
    data = distance_compare_sf[distance_compare_sf['distance_type'] == dist_type]
    
    # Plot safe buildings (≤300m) with viridis
    safe = data[data['distance_m'] <= 300]
    safe.plot(
        ax=ax,
        column='distance_m',
        cmap='viridis',
        markersize=0.5,
        alpha=0.9,
        vmin=0,
        vmax=300,
        legend=False
    )
    
    # Overlay at-risk buildings (>300m) in red
    at_risk = data[data['distance_m'] > 300]
    at_risk.plot(
        ax=ax,
        color='#d73027',
        markersize=0.7,
        alpha=0.8
    )
    
    ax.set_title(dist_type, fontsize=12, fontweight='bold')

    # Add grid
    ax.grid(True, alpha=0.3, linestyle='-', linewidth=0.5)
    ax.set_axisbelow(True)
    
    # Set labels
    ax.set_xlabel('Longitude')
    if idx == 0:  # Only left plot
        ax.set_ylabel('Latitude')
    
    # Format coordinates
    ax.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, p: f'{x:.2f}°E'))
    if idx == 0:  # Only left plot
        ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda y, p: f'{y:.2f}°N'))
    else:
        ax.set_yticklabels([])  # Hide y-axis on right
        ax.tick_params(left=False)
    
    # Remove spines
    for spine in ax.spines.values():
        spine.set_visible(False)

# Add overall title
fig.suptitle('Minimum Distances to Nearest Shelter Compared (1951)',
             fontsize=14, fontweight='bold')
# Add Subtitle
fig.text(0.5, 0.93, '\nBuildings beyond 300m threshold are shown in red',
         ha='center', fontsize=12)

# Add colorbar
sm = plt.cm.ScalarMappable(cmap='viridis', norm=plt.Normalize(vmin=0, vmax=300))
sm.set_array([])

# Adjust positioning
cbar_ax = fig.add_axes([0.98, 0.15, 0.02, 0.7])
cbar = fig.colorbar(sm, cax=cbar_ax, orientation='vertical')
cbar.set_label('Distance (m)', fontsize=12, fontweight='bold')
cbar.ax.tick_params(labelsize=12)

# Adjust layout
plt.tight_layout(rect=[0, 0.03, 1, 0.93], w_pad=0.5) 

# ==== SAVE FIGURE ====

plt.savefig('media/m_dmin_with_threshold.png', dpi=400, bbox_inches='tight')
plt.close()
```

<a id='m_dmin_with_threshold'></a>

```python
display(Image('media/m_dmin_with_threshold.png'))
```

<!-- #region slideshow={"slide_type": ""} tags=["hermeneutics"] -->
We have mentioned already that the way we operationalise distance matters. The difference in accessibility visible in the maps of Aarhus in Figures 2 and 3 is not fully representative as the building centroids treat all buildings equally; however, not all buildings represent the same number of people. Buildings in the downtown contain, on average, more residents than buildings in the suburbs. Assuming that the city center is the target for a strike, the red dots signalling poor proximity of shelters in the downtown can possibly spell a disaster for more residents than a red dot in the periphery, something that we will explore in the gravity-weighted section below. For now, to lay the difference between the two models before the eyes, the cumulative distribution plots in [Figure 4](#ecdf_weighted) show the lag of the network model behind the straight distance model with curves differentiating buildings into three groups by height. The numbers in the aggregate agree with the maps: at least ~75% of buildings fall within the recommended threshold if using a radius of 300m, while only ~50% of buildings fall within it if we use network distance. The colors indicate that low-rise buildings are the least provisioned with shelters, while mid-rise and high-rise buildings are better-off by a difference of 15-20% regardless of how distance is measured. This shows high-density areas have better accessibility to shelters, while areas with a lot of single-floor houses, such as villa quarters in the suburbs, have shelters farther away. For the swift-footed residents, it is perhaps a consolation that 75-80% of low-rise buildings have a shelter within 500m distance; and all buildings regardless of height have a shelter within 1000m.
<!-- #endregion -->

```python jdh={"object": {"source": ["Cumulative distribution of distances to shelters in Aarhus 1951, weighted by building height, a proxy for population"]}} slideshow={"slide_type": ""} tags=["figure-cumaccess-buildheight-*"]
# ==== CUMULATIVE ACCESSIBILITY TO SHELTERS BY BUILDING HEIGHT (EUCLIDEAN VS NETWORK) ====

import matplotlib.pyplot as plt

# ==== SETUP ====

# Shortest EUCLIDEAN distance per building
euclid_shortest = euclid_sf[['building_id', 'distance_m']].copy()
euclid_shortest['distance_type'] = "Euclidean"

# Shortest NETWORK distance per building  
network_shortest = network_sf[['building_id', 'distance_m']].copy()
network_shortest['distance_type'] = "Network"

# Combine
distances_combo = pd.concat([euclid_shortest, network_shortest], ignore_index=True)

# Join with building attributes
distances_weighted = distances_combo.merge(
    buildings[['id_lokalId', 'est_pop', 'byg054AntalEtager']],
    left_on='building_id',
    right_on='id_lokalId',
    how='left'
)

# Fill missing population with 1
distances_weighted['est_pop'] = distances_weighted['est_pop'].fillna(1)

def classify_height(floors):
    if pd.isna(floors):
        return "Low-rise (1–2)"
    elif floors <= 2:
        return "Low-rise (1–2)"
    elif floors <= 4:
        return "Mid-rise (3–4)"
    else:
        return "High-rise (5+)"

distances_weighted['height_class'] = distances_weighted['byg054AntalEtager'].apply(classify_height)

# Make categorical with proper order
distances_weighted['height_class'] = pd.Categorical(
    distances_weighted['height_class'],
    categories=["Low-rise (1–2)", "Mid-rise (3–4)", "High-rise (5+)"],
    ordered=True
)

# ==== CONSTRUCT FIGURE ====

# Initialize plot
fig, axes = plt.subplots(1, 2, figsize=(14, 6), sharey=True)
colors = {"Low-rise (1–2)": "#1b9e77", "Mid-rise (3–4)": "#7570b3", "High-rise (5+)": "#d95f02"}

for idx, dist_type in enumerate(["Euclidean", "Network"]):
    ax = axes[idx]
    
    data = distances_weighted[distances_weighted['distance_type'] == dist_type]
    
    # Plot ECDF for each height class
    for height_class in ["Low-rise (1–2)", "Mid-rise (3–4)", "High-rise (5+)"]:
        subset = data[data['height_class'] == height_class]['distance_m'].dropna()
        
        if len(subset) > 0:
            # Calculate ECDF
            sorted_data = np.sort(subset)
            y = np.arange(1, len(sorted_data) + 1) / len(sorted_data)
            
            ax.plot(sorted_data, y, color=colors[height_class], linewidth=2, label=height_class)
    
    # Add 300m threshold line
    ax.axvline(x=300, color='red', linestyle='--', linewidth=1.5)
    
    ax.set_xlim(0, 1250)
    ax.set_xticks(np.arange(0, 1251, 250))
    ax.set_xlabel('Distance to Nearest Shelter (m)', fontsize=11)
    ax.set_title(dist_type, fontsize=12, fontweight='bold')
    ax.grid(True, alpha=0.3)
    ax.set_axisbelow(True)

# Y-axis formatting
axes[0].set_ylabel('Cumulative Share of Buildings', fontsize=11)
axes[0].yaxis.set_major_formatter(plt.FuncFormatter(lambda y, _: f'{int(y*100)}%'))

# Overall title
fig.suptitle('Cumulative Accessibility to Shelters by Building Height', 
             fontsize=15, fontweight='bold')

# Add Subtitle
fig.text(0.5, 0.90, '\nVertical red dotted line marks the 300m threshold',
         ha='center', fontsize=12)

# Legend at bottom
handles, labels = axes[0].get_legend_handles_labels()
fig.legend(handles, labels, loc='lower center', bbox_to_anchor=(0.5, -0.05),
           ncol=3, title='Building Height (floors)', title_fontsize=11, 
           fontsize=11, frameon=True)

plt.tight_layout(rect=[0, 0.05, 1, 0.95])

# ==== SAVE FIGURE ====

plt.savefig('media/ecdf_weighted.png', dpi=400, bbox_inches='tight')
plt.close()
```

<a id='ecdf_weighted'></a>

```python
display(Image('media/ecdf_weighted.png'))
```

<!-- #region slideshow={"slide_type": ""} -->
### Which places enjoy the best protection?
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"bettc": [], "bette": [], "bettn": [], "civio": [], "hanse": [], "ortma": [], "ortmn": []}} slideshow={"slide_type": ""} -->
Urban planners and archaeologists have long underscored that cities and peripheries are subject to different types of scaling across population, infrastructure and productivity (<cite id="bette"><a href="#zotero%7C15824328%2FNM2JCUS2">(Bettencourt, 2013)</a></cite>; <cite id="ortmn"><a href="#zotero%7C15824328%2FSDJPPFJN">(Ortman, 2023)</a></cite>; <cite id="ortma"><a href="#zotero%7C15824328%2F98CWTCCG">(Ortman et al., 2014)</a></cite>). City centres with their compact and vertical architecture house denser populations and foster intensified social interaction. This intensive social scaling has a positive impact on innovation and economic productivity but poses an extra challenge for emergency planning due to greater risk to more inhabitants (<cite id="bettn"><a href="#zotero%7C15824328%2FSZ48JCI5">(Bettencourt et al., 2007b)</a></cite>; <cite id="bettc"><a href="#zotero%7C15824328%2FUEXT7RQK">(Bettencourt et al., 2007a)</a></cite>). During the early Cold War, the civil defence considered the city centre to be the most vulnerable space (dense in terms of buildings and populations in addition to being the most likely target of air raids), hence state directives ordered that the core should be the main focus of shelter building (<cite id="civio"><a href="#zotero%7C15824328%2F7SMI3F5M">(Civilforsvarets arbejdsplan IV Oktober 1953-1955, 1953)</a></cite>). Peripheries scale materially, offering residents more living space and comfort within their spatially extensive environs. Their extent and low density make them less vulnerable as an eventual threat, as it would affect a smaller fraction of the population in the suburb than an emergency of similar extent in the downtown, and it was also considered a less likely target. However, this prioritisation resulted in the paradox that though the core was (considered) more vulnerable, it became better sheltered than the “safer” periphery areas, where residents were virtually unsheltered.

Like most European cities, Aarhus reveals a densely occupied and vibrant historical core surrounded by quieter, more spacious and newer suburbs. The previous coverage and distance maps already hinted at a dividing line in shelter provision that runs between the centre and periphery. To move beyond visual impressions, we turn to a gravity-weighted accessibility index developed by Hansen (<cite id="hanse"><a href="#zotero%7C15824328%2FK68E7NZM">(Hansen, 1959)</a></cite>), which integrates shelter network distance with shelter capacity into a single cumulative measure. Aggregate capacity matters, as many buildings downtown have more than a single shelter within the distance of 300m. [Figure 5](#m_shelter_count) shows that downtown buildings have on average five shelters within the recommended distance, while the best provisioned ones have between 10 to 20 shelters within network and Euclidean distance respectively. 
<!-- #endregion -->

```python
import matplotlib.pyplot as plt
import matplotlib.ticker as ticker
from matplotlib.colors import Normalize

# ==== SETUP ====

# Define threshold in meters
threshold_m = 300

# Filter and count how many shelters are within threshold for each building

## Calculate EUCLIDEAN CUM scores
num_scores_euc = (
    dma[dma['euclid_distance'].notna() & (dma['euclid_distance'] <= threshold_m)]
    .groupby('building_id') # for each building record there is a different shelter, so counting building IDs gets us the number of shelters
    .size()
    .reset_index(name='num_euclid')
)

## Calculate NETWORK CUM scores
num_scores_net = (
    dma[dma['net_m'].notna() & (dma['net_m'] <= threshold_m)]
    .groupby('building_id') # for each building record there is a different shelter, so counting building IDs gets us the number of shelters
    .size()
    .reset_index(name='num_net')
)

# Join with buildings
# Filter buildings to 1952 boundary
buildings_in_city = buildings[buildings.within(aarhus_city1952.union_all())].copy()

# Merge CUM scores
buildings_num = buildings_in_city.merge(num_scores_net, left_on='id_lokalId', right_on='building_id', how='left')
buildings_num = buildings_num.merge(num_scores_euc, left_on='id_lokalId', right_on='building_id', how='left', suffixes=('', '_euc'))

# Fill NaN with 0 (buildings with no shelters within 300m)
buildings_num['num_net'] = buildings_num['num_net'].fillna(0).astype(int)
buildings_num['num_euclid'] = buildings_num['num_euclid'].fillna(0).astype(int)

# Combine both for plotting
buildings_long = pd.concat([
    buildings_num[['num_euclid', 'geometry']].assign(distance_type='Euclidean').rename(columns={'num_euclid': 'shelter_count'}),
    buildings_num[['num_net', 'geometry']].assign(distance_type='Network').rename(columns={'num_net': 'shelter_count'})
], ignore_index=True)
buildings_long = gpd.GeoDataFrame(buildings_long, geometry='geometry', crs='EPSG:25832')
buildings_long = buildings_long.to_crs('EPSG:4326')
```

```python jdh={"object": {"source": ["Data source: MELICA, DBR, OSM 2025"]}} slideshow={"slide_type": ""} tags=["figure-sheltercount-availibility-300m-*"]
# ==== SHELTER COUNT / AVAILABILITY WITHIN 300M ====

import matplotlib.pyplot as plt
import matplotlib.ticker as ticker
import pandas as pd
import numpy as np
import warnings
warnings.filterwarnings("ignore")

# ==== SETUP ====

# Combine Euclidean and Network columns into long format for faceting
buildings_long = pd.concat([
    buildings_num[['num_euclid', 'geometry']].assign(distance_type='Euclidean').rename(columns={'num_euclid': 'shelter_count'}),
    buildings_num[['num_net', 'geometry']].assign(distance_type='Network').rename(columns={'num_net': 'shelter_count'})
], ignore_index=True)

buildings_long = gpd.GeoDataFrame(buildings_long, geometry='geometry', crs='EPSG:25832')

# ==== CONSTRUCT MAP ====

buildings_long = buildings_long.to_crs('EPSG:4326') 

# Initialize plot
fig, axes = plt.subplots(1, 2, figsize=(16, 10))
max_count = buildings_long['shelter_count'].max()

for idx, dist_type in enumerate(['Euclidean', 'Network']):
    ax = axes[idx]
    
    # Get data for this distance type
    data = buildings_long[buildings_long['distance_type'] == dist_type]
    
    # Plot buildings with 0 shelters in grey
    zero_shelters = data[data['shelter_count'] == 0]
    if len(zero_shelters) > 0:
        zero_shelters.plot(ax=ax, color='lightgrey', markersize=1.5, alpha=0.5)
    
    # Plot buildings with shelters using plasma
    has_shelters = data[data['shelter_count'] > 0]
    if len(has_shelters) > 0:
        has_shelters.plot(
            ax=ax,
            column='shelter_count',
            cmap='plasma',
            markersize=1.5,
            alpha=0.9,
            vmin=1,
            vmax=max_count,
            legend=False
        )
    
    # Set title
    ax.set_title(dist_type, fontsize=12, fontweight='bold')
    
    # Add grid
    ax.grid(True, alpha=0.3, linestyle='-', linewidth=0.5)
    ax.set_axisbelow(True)
    
    # Set labels
    ax.set_xlabel('Longitude')
    if idx == 0:  # Only left plot
        ax.set_ylabel('Latitude')
    
    # Format coordinates
    ax.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, p: f'{x:.2f}°E'))
    if idx == 0:  # Only left plot
        ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda y, p: f'{y:.2f}°N'))
    else:
        ax.set_yticklabels([])  # Hide y-axis on right
        ax.tick_params(left=False)
        
    # Remove spines
    for spine in ax.spines.values():
        spine.set_visible(False)

# Add overall title
fig.suptitle('Number of Shelters Within 300m of Buildings in Aarhus (1951)', 
             fontsize=14, fontweight='bold', y=1.01)

# Add subtitle
fig.text(0.5, 0.96, 'Grey indicates no shelters within the threshold', 
         ha='center', fontsize=11, fontweight='normal')

# Add colorbar
sm = plt.cm.ScalarMappable(cmap='plasma', norm=plt.Normalize(vmin=1, vmax=max_count))
sm.set_array([])

# Adjust positioning
cbar_ax = fig.add_axes([0.98, 0.15, 0.02, 0.7])
cbar = fig.colorbar(sm, cax=cbar_ax, orientation='vertical')
cbar.set_label('Available shelters', fontsize=12, fontweight='bold')
cbar.ax.tick_params(labelsize=12)

# Adjust layout
plt.tight_layout(rect=[0, 0.15, 1, 0.96])  # add more bottom space

# ==== DISPLAY FIGURE ====

plt.savefig('media/m_shelter_count.png', dpi=400, bbox_inches='tight')
plt.close()
```

<a id='m_shelter_count'></a>

```python
display(Image('media/m_shelter_count.png'))
```

<!-- #region slideshow={"slide_type": ""} -->
The Relative Accessibility Index (RAI) expresses how well each location compares to the citywide average (see [Figure 6A](#m_rai_lisa)). It combines the number and capacity of nearby shelters with a distance-decay function applied to network distance, producing unitless scores centred on 1. RAI score 1 marks average accessibility, while values below 1 indicate below-average accessibility (underserved area) and values above 1 mark above-average accessibility (well-served areas). RAI score values that approach zero means that the building has no realistic access to shelter at all.  As shown in [Figure 6A](#m_rai_lisa), the RAI surface recasts the city’s geography of preparedness. Dark, near-black zones in Risskov, Egå, and Malling–Holme mark the worst-off suburbs, where shelter opportunities are almost absent. Other suburban areas - Viby, Højbjerg, Åbyhøj - hover around the citywide average, suggesting modest but not catastrophic gaps. In contrast, bright clusters blaze across the historic downtown, where multiple shelters overlap to create well-above-average accessibility hotspots.

Although the overall shelter capacity was far from sufficient, the RAI shows that downtown residents and workers stood a far better chance of finding cover than their suburban counterparts.  The 1951 shelter system thus exhibits a vertical logic of spatial equity: protection clustered where the city was densest and most at risk, while the outlying neighbourhoods were left to fend for themselves.
<!-- #endregion -->

```python
# ==== COMPUTING ACCESSIBILITY SCORES ====

import pandas as pd
import numpy as np

# ==== SETUP ====

# Define beta parameter
beta = 1.5  # Distance decay factor

# Prepare DMA for gravity calculation
## Filter valid data
dma_gravity = dma[
    (dma['shelter_id'].isin(shelters['shelterID'])) &
    (dma['net_m'].notna())
].copy()

# ==== GRAVITY CALCULATIONS ====

## Calculate distance in km and access component
dma_gravity['net_distance_km'] = dma_gravity['net_m'] / 1000
dma_gravity['access_component'] = (
    dma_gravity['shelter_capacity'] / 
    (dma_gravity['net_distance_km'] ** beta)
)

## Aggregate to building-level accessibility
building_accessibility = (
    dma_gravity.groupby('building_id')['access_component']
    .sum()
    .reset_index()
    .rename(columns={'access_component': 'accessibility'})
)

## Cap at 95th Percentile
access_cutoff = building_accessibility['accessibility'].quantile(0.95)
building_accessibility['access_capped'] = building_accessibility['accessibility'].clip(upper=access_cutoff)
```

```python
# ==== RAI CALCULATION ====

import matplotlib.pyplot as plt
import matplotlib.ticker as ticker
import numpy as np
import geopandas as gpd
import pandas as pd
from matplotlib.colors import PowerNorm

# ==== SETUP ====

# Filter to finite values
buildings_with_access = building_accessibility[
    building_accessibility['access_capped'].notna() & 
    np.isfinite(building_accessibility['access_capped'])
].copy()

# ==== COMPUTE RAI ====

# Calculate mean accessibility for RAI
mean_access = buildings_with_access['access_capped'].mean()

# Calculate RAI
buildings_with_access['rai'] = buildings_with_access['access_capped'] / mean_access

# Standardized RAI interpretation summary
rai_summary = pd.cut(buildings_with_access['rai'], 
                     bins=[0, 0.5, 1.0, 1.5, np.inf], 
                     labels=['Under-served (<0.5)', 'Below average (0.5-1.0)', 
                            'Above average (1.0-1.5)', 'Well-served (>1.5)'])

# Merge with building geometry
buildings_with_access = buildings_with_access.merge(
    buildings[['id_lokalId', 'geometry']],
    left_on='building_id',
    right_on='id_lokalId',
    how='left'
)
buildings_with_access = gpd.GeoDataFrame(buildings_with_access, geometry='geometry', crs='EPSG:25832')

# Convert to EPSG:4326 for plotting
buildings_plot = buildings_with_access.to_crs('EPSG:4326')
```

```python
# ==== LISA ====

from libpysal.weights import DistanceBand
from esda.moran import Moran_Local
import numpy as np
import warnings
warnings.filterwarnings("ignore")

# ==== SETUP ====

# Transform to projected CRS (EPSG:25832) for analysis
buildings_proj = buildings_with_access.to_crs('EPSG:25832')

# Get coordinates
coords = np.column_stack([buildings_proj.geometry.x, buildings_proj.geometry.y])

# Create spatial weights - 250m distance threshold
weights = DistanceBand(coords, threshold=250, binary=True, silence_warnings=True)

# Compute Local Moran's I
lisa = Moran_Local(buildings_proj['rai'].values, weights)

# Attach results to dataframe
buildings_proj['Ii'] = lisa.Is
buildings_proj['p_value'] = lisa.p_sim
buildings_proj['Z_Ii'] = lisa.z_sim

# ==== CLASSIFY LISA CLUSTERS ====

mean_rai = buildings_proj['rai'].mean()

def classify_lisa(row):
    if row['p_value'] >= 0.05:
        return "Not Significant"
    elif row['rai'] >= mean_rai and row['Ii'] >= 0:
        return "High-High"
    elif row['rai'] < mean_rai and row['Ii'] >= 0:
        return "Low-Low"
    elif row['rai'] >= mean_rai and row['Ii'] < 0:
        return "High-Low"
    elif row['rai'] < mean_rai and row['Ii'] < 0:
        return "Low-High"
    else:
        return "Not Significant"

buildings_proj['lisa_cluster'] = buildings_proj.apply(classify_lisa, axis=1)
```

```python tags=["figure-rai-lisa-*"]
# ==== DUAL MAP: RAI & LISA ====

import folium
from folium import plugins
from matplotlib.colors import PowerNorm
import matplotlib.cm as cm
import matplotlib.pyplot as plt

# ==== SETUP ====

# Convert to EPSG:4326 for mapping
buildings_rai_map = buildings_with_access.to_crs('EPSG:4326')
buildings_lisa_map = buildings_proj.to_crs('EPSG:4326')

# ==== CONSTRUCT DUAL MAP ====

m_rai_lisa = plugins.DualMap(
    location=[56.16, 10.20],
    zoom_start=13,
    tiles=None  # Don't set default tiles here
)

# Add tile layers to LEFT map (m1) - last added = default
folium.TileLayer(
    tiles='https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}',
    attr='Esri',
    name='Esri WorldImagery',
    overlay=False,
    control=True
).add_to(m_rai_lisa.m1)
folium.TileLayer('OpenStreetMap', name='OpenStreetMap').add_to(m_rai_lisa.m1)
folium.TileLayer('CartoDB dark_matter', name='CartoDB Dark').add_to(m_rai_lisa.m1)
folium.TileLayer('CartoDB Positron', name='CartoDB Positron').add_to(m_rai_lisa.m1)

# Add tile layers to RIGHT map (m2) - last added = default
folium.TileLayer(
    tiles='https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}',
    attr='Esri',
    name='Esri WorldImagery',
    overlay=False,
    control=True
).add_to(m_rai_lisa.m2)
folium.TileLayer('OpenStreetMap', name='OpenStreetMap').add_to(m_rai_lisa.m2)
folium.TileLayer('CartoDB dark_matter', name='CartoDB Dark').add_to(m_rai_lisa.m2)
folium.TileLayer('CartoDB Positron', name='CartoDB Positron').add_to(m_rai_lisa.m2)

# Add layer controls (collapsed) to both maps
folium.LayerControl(collapsed=True, position='topleft').add_to(m_rai_lisa.m1)
folium.LayerControl(collapsed=True, position='topleft').add_to(m_rai_lisa.m2)

# ==== LEFT MAP: RAI ====

# Create colormap for RAI values with sqrt transformation
rai_min = buildings_rai_map['rai'].min()
rai_max = buildings_rai_map['rai'].max()
norm = PowerNorm(gamma=0.5, vmin=rai_min, vmax=rai_max)
cmap = plt.get_cmap('magma')

# Add buildings to left map
for _, row in buildings_rai_map.iterrows():
    if pd.notna(row['rai']):
        color_val = norm(row['rai'])
        color = cm.colors.rgb2hex(cmap(color_val))
        
        folium.CircleMarker(
            location=[row.geometry.y, row.geometry.x],
            radius=2,
            color=color,
            fill=True,
            fillColor=color,
            fillOpacity=0.8,
            weight=0,
            popup=folium.Popup(f"""
                <div style='font-family: Arial; font-size: 12px;'>
                    <b>RAI:</b> {row['rai']:.2f}<br><br>
                    <b>Building ID:</b> {row['building_id']}
                </div>
            """, max_width=200)
        ).add_to(m_rai_lisa.m1)


# Add RAI legend
rai_legend = f'''
<div style="position: fixed; bottom: 20px; right: 52%; background-color: white; 
     border:2px solid grey; z-index:9999; padding: 10px; font-size: 12px; width: 200px;">
<p style="margin: 0 0 10px 0;"><b>Relative Accessibility Index (RAI)</b></p>
<div style="background: linear-gradient(to right, #000004, #8c2981, #de4968, #fe9f6d, #fcfdbf); 
     height: 20px; width: 100%; margin-bottom: 8px; border: 1px solid #ccc;"></div>
<div style="display: flex; justify-content: space-between; font-size: 10px;">
    <span>Low ({rai_min:.2f})</span>
    <span>High ({rai_max:.2f})</span>
</div>
</div>
'''
m_rai_lisa.m1.get_root().html.add_child(folium.Element(rai_legend))

title_rai = '<h4 style="position: absolute; top: 10px; left: 25%; transform: translateX(-50%); z-index: 9999; background: white; padding: 5px; border: 2px solid grey;">Relative Accessibility Index (RAI)</h4>'
m_rai_lisa.m1.get_root().html.add_child(folium.Element(title_rai))

# ==== RIGHT MAP: LISA ====

# LISA colors
lisa_colors = {
    "High-High": "#2c7bb6",
    "Low-Low": "#d7191c",
    "High-Low": "#abd9e9",
    "Low-High": "#fdae61",
    "Not Significant": "grey"
}

# Add buildings to right map

for _, row in buildings_lisa_map.iterrows():
    folium.CircleMarker(
        location=[row.geometry.y, row.geometry.x],
        radius=2,
        color=lisa_colors[row['lisa_cluster']],
        fill=True,
        fillColor=lisa_colors[row['lisa_cluster']],
        fillOpacity=0.9,
        weight=0,
        popup=folium.Popup(f"""
            <div style='font-family: Arial; font-size: 12px;'>
                <b>RAI:</b> {row['rai']:.2f}<br>
                <b>Cluster:</b> {row['lisa_cluster']}<br><br>
                <b>Building ID:</b> {row['building_id']}
            </div>
        """, max_width=200)
    ).add_to(m_rai_lisa.m2)

# Add LISA legend

lisa_legend = '''
<div style="position: fixed; bottom: 20px; right: 2%; background-color: white; 
     border:2px solid grey; z-index:9999; padding: 10px; font-size: 12px;">
<p style="margin: 0 0 10px 0;"><b>Hot- and Cold-Spots</b></p>
<p><span style="color:#2c7bb6; font-size: 16px;">●</span> High-High (hot spot)</p>
<p><span style="color:#d7191c; font-size: 16px;">●</span> Low-Low (cold spot)</p>
<p><span style="color:#abd9e9; font-size: 16px;">●</span> High-Low (outlier)</p>
<p><span style="color:#fdae61; font-size: 16px;">●</span> Low-High (outlier)</p>
<p><span style="color:grey; font-size: 16px;">●</span> Not Significant</p>
</div>
'''

title_lisa = '<h4 style="position: absolute; top: 10px; left: 75%; transform: translateX(-50%); z-index: 9999; background: white; padding: 5px; border: 2px solid grey;">LISA Clusters</h4>'
m_rai_lisa.m2.get_root().html.add_child(folium.Element(title_lisa))

m_rai_lisa.m2.get_root().html.add_child(folium.Element(lisa_legend))

# ==== SAVE FIGURE ====
m_rai_lisa.save('media/m_rai_lisa_dual.html')
```

<a id='m_rai_lisa'></a>

```python
from IPython.display import HTML
HTML('''
<iframe
    src="./media/m_rai_lisa_dual.html"
    width="100%"
    height="600"
    style="border: 0;"
    loading="lazy"
    referrerpolicy="no-referrer"
>    
</iframe>
''')
```

<!-- #region slideshow={"slide_type": ""} -->
Most of the previous measures showed that the accessibility deteriorates as we go to the periphery. Yet, a reader might ask if there is a difference concealed within the peripheral and downtown clusters. It is hard to spot individual buildings which stand out from their neighbourhood in the binary color scales of Figures 2 or the subtle shading of the minimum distance or RAI visualisation (Fig. 3 and 6). LISA scores are better suited to visually differentiate intra-cluster variation by means of hot- and cold-spots and their outliers. In [Figure 6B](#m_rai_lisa), each building is assigned to one of five categories of shelter provisioning: high-high, high-low, low-low, low-high, and insignificant, where the first term refers to how well the individual building is served, and the second term marks the provisioning of its neighbourhood as a whole. Thus ‘high-high’ label marks a hotspot where a well-served building sits in a well-served area, while the reverse is a coldspot. A ‘high-low’ label means that a well-served building sits inside an underserved neighbourhood and is therefore a positive outlier. The ‘low-high’ label inverts the situation, indicating a poorly served outlier among well-served counterparts. If plotted with a diverging color scheme, it becomes easier to detect and address underserved outliers inside downtown as well as better-off clusters within the periphery. Beginning with the downtown, Nørreport and Brammervej stand out as the largest underserved sections. While everything to the east of Strandvejen (ie. harbour area and the beach) is underserved, the scores are statistically not significant enough to be flagged as coldspots. Within the poorly provisioned margins of the town, the lucky buildings are the ones closest to the few extant shelters, mostly near childcare facilities, libraries, bus stops, parks and other public amenities.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
All in all, all measures point to moderate inequality in the allocation of shelters within the urban landscape of Aarhus in 1951, with the city centre and periphery being clearly divided. In Aarhus of 1951, only one person in ten would find a spot in the shelter. This ratio would be slightly higher in the downtown and lower in the suburbs. In the suburbs, low capacity and long distances combine to disadvantage the residents.  This relative lack of preparedness should be balanced with an assumed greater safety because of the lesser risk of being bombed. On closer inspection the downtown is not bullet-proof either. While poorly provisioned buildings (outside of the 300m threshold distance) are less frequent than in the suburbs, higher-density occupation means the demand on shelters would be higher, cancelling out the better provisioning. 
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
## Discussion
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"dahlr": []}} slideshow={"slide_type": ""} -->
Before we criticise civil defence too severely for failing to live up to their own universal ambition, we should remember that this study centres on the year 1951. The Danish civil defence organisation was only two years old, having been created in 1949, and shelter building had been going on for a limited period of time. Even the most committed and optimistic civil defenders realised the deficiency of shelters should the war have come by 1951. (<cite id="dahlr"><a href="#zotero%7C15824328%2F9QTPJXDH">(Dahl, 1950)</a></cite>)

Our results demonstrate agreement between the national guidelines of prioritising the city cores and local implementation of preparedness on - or, perhaps, rather below - the ground in Aarhus. Public shelters broadly follow residential distribution across the study area, but their concentration and accessibility peak in the urban center and gradually diminish toward the margins, where shelters become sparse. Hence, our results testify to the fact that shelter accessibility in Aarhus was moderately uneven by 1951. Although aggregate shelter capacity was inadequate throughout the city, access was nevertheless easier for people working, shopping, and moving through the city centre than for families in homes outside the city centre, who relied on *sikringsrum* (private shelter rooms).
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Dimensions of Equity
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"byhis": [], "monte": []}} slideshow={"slide_type": ""} -->
In Aarhus, civil defence shelters concentrated downtown where high-rise buildings, factories, churches, and shopping areas attracted higher-density occupation and social interaction. While precise occupancy figures for buildings and factories are unavailable, the density of the built environment ([Figure 4](#ecdf_weighted)) serves as a reasonable proxy for both residents and commuters, justifying higher risk rankings. From this perspective, the proliferation of shelters downtown responds to a greater need for them. Urban centre residents and workers could not independently establish civil defence amenities while suffering greater risk and potential harm, whereas peripheral residents were perhaps seen as less at risk by virtue of their extensive spread. While the territorial distribution of shelters is distinctly unequal, the civil defense provision is satisfied when seen from the vertical equity prism, by scaling amenities according to the urban occupation density. 

Aarhus's demographic make-up in the 1950s offers additional insight into the mid-century notion of equity. Aarhus was dominated by a population of Danish or Nordic origin. The affluent residents occupied villas in suburban areas like Risskov in the north or Aaby in the west, while lower socio-economic classes resided in the center in old working-class neighborhoods such as Øgaderne, Frederiksbjerg and Trøjborg. The downtown, however, was far from the target of boutique urbanism that it is today, where festivals chase one another across the different cafe-and-culture districts. The central streets around the Aa river were once slum areas, and the ‘high-rises’ in the nearby surroundings were built by social housing organisations and workers’ unions for the benefit of the harbour workshops and downtown factories - they were ensuring a steady supply of working force (<cite id="byhis"><a href="#zotero%7C15824328%2FZN3ZS6A7">(Aarhus Universitet, 2024)</a></cite>). 

The spatial distribution of socioeconomic groups in 1951 Aarhus - with poorer residents in the downtown and wealthier populations in the outskirts - meant that social and horizontal equity coincided with the occupation-, density- and need-based criteria. In this sense, Aarhus diverged from the American experience, where civil-defence debates were often racialised and where vulnerable central districts were associated with immigrants and poverty (<cite id="monte"><a href="#zotero%7C15824328%2FVEKQAF7U">(Monteyne, 2011)</a></cite>). Mid-century Denmark, by contrast, remained comparatively homogeneous, creating a different equity baseline for shelter planning.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Commuters and the Limits of Place-Based Measures
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
While our results are already sobering, one important dimension of need remains unaccounted for: the mobile population of commuters and people on the move. Mobility resists the place-based logic of accessibility analysis, as these individuals cannot be tied to a fixed residential or origin point. Consequently, they fall outside the formal assessment.

Yet this group clearly mattered to mid-century planners. Public shelters (BDGs) were deliberately placed near bus stops, major roads, and park entrances—sites chosen with commuters in mind. This design choice may even have put those in transit on a more equal footing with static residents, perhaps at an advantage, if warnings reached them while already outdoors rather than at home or work.

The magnitude of this mobile population, however, is impossible to quantify: we lack data on how many people were commuting, where, and when during the 1950s. The geography of movement thus remains absent from our analysis and one best explored in future research through person-based or agent-based modelling approaches.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Digital Methods and Retrospective Fairness
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"civif": [], "dahla": [], "dahlr": [], "komis": []}} slideshow={"slide_type": ""} -->
Our results of moderate inequity must be interpreted with caution. Archival sources make clear that civil-defence planners at local as well as national level were well aware of these shortcomings and actively sought to address them, pressing the state for funds to build and upgrade shelters and improve both national and local preparedness. (<cite id="dahlr"><a href="#zotero%7C15824328%2F9QTPJXDH">(Dahl, 1950)</a></cite>; <cite id="civif"><a href="#zotero%7C15824328%2FW3MHPRHH">(Møde i Civilforsvarsstyrelsen - Stockholmsgade 27 KBH, 1951)</a></cite>; <cite id="dahla"><a href="#zotero%7C15824328%2FUTRIQTG2">(Dahl, 1953)</a></cite>; <cite id="komis"><a href="#zotero%7C15824328%2FFH7UP7VQ">(Referat C.F.-kommissionens møde,1956)</a></cite>) 

In this sense, our results validate rather than indict the civil defense agenda at the time; they capture a system at mid-course rather than at completion. 
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"kunzm": []}} slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Applying today’s highly granular spatial metrics to a mid-century planning context is only partially fair. Civil-defence planning in 1940s - 1950s Aarhus operated under vastly different epistemic and administrative conditions. Planners lacked the fine-grained digital data and modelling tools we now use to simulate travel behaviour or time-distance surfaces. Instead, they worked with coarse indicators - population and building counts aggregated by civil-defence zone - and made decisions within a logic of urban-wide strategic adequacy rather than individual optimisation. What appears to us as spatial inequity may thus have represented, in their own terms, an acceptable and evolving level of coverage within the practical limits of their time.

The preparedness geography of the time reflected this aggregate orientation. During the twentieth century, Denmark underwent multiple administrative reforms that reorganised the territory from a thousand small *sogne* (parishes) and *købstæder* (market towns) into successively larger kommuner. In 1952, the relevant planning units were neither present urban neighbourhoods nor modern statistical districts but a set of civil-defence zones defined by strategic necessity rather than demographic coherence. The available data - population totals by suburb, number of buildings, number of shelter places - were suited to this scale. As the borderlines of the original suburbs and districts are not accessible, we now evaluate accessibility at the level of individual buildings. This way we unavoidably project a later, more granular epistemology onto a system conceived for an entirely different order of spatial knowledge.

From the standpoint of historical method, this calls for source criticism in the digital domain. The apparent precision of modern geospatial data and computational models can create a false sense of equivalence with the past. We are not merely adding more detail to their picture; we are producing a qualitatively different picture, grounded in data infrastructures and political expectations that postdate the Cold War. Since the late twentieth century, spatial (environmental) equity has become a normative policy value - reinforced by European integration and regional cohesion agendas (<cite id="kunzm"><a href="#zotero%7C6622720%2FV4BSVG7D">(Kunzmann, 1998)</a></cite>) - but such assumptions were absent from early Cold War planning. The civil defence effort sought to distribute shelters according to risk exposure and district size, not to guarantee uniform walking access for every inhabitant.

In that sense, our digital reconstruction should not be read as a simple “test” that the 1951 planners failed, but as a dialogue between two epistemic worlds: theirs, aggregate and strategic; and ours, granular, data-rich, and equity-oriented. The numerical inequities we detect—longer walking distances or lower coverage in certain suburbs—must be interpreted through this double historical lens. They reveal not only differences in urban form but also the changing regimes of knowledge that define what counts as adequate protection. Digital history here becomes a form of source criticism of spatial models: by quantifying inequities we also expose the historical limits of quantification itself.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
### Scales of Provisioning
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
A second, closely related issue concerns the spatial scales at which accessibility was imagined and achieved. The notion of “adequate access” is inherently scale-dependent: different kinds of urban facilities are designed to serve different catchments. In planning theory, the service range of municipal-scale institutions such as hospitals, universities, or waste sites typically extends across the entire city; community-scale facilities like secondary schools, transformer stations, or sports halls serve zones of roughly two kilometres; while neighbourhood-scale amenities such as playgrounds or elementary schools should lie within one kilometre of users. Oh and Jeong (2007) point to different distance thresholds for different levels of public parks in Seoul, Korea; while Larsen and Gilliland (2008) map how gaps between supermarket service areas in a Canadian city widen over time. Each type of amenity comes with its service range and thus a slightly different logic of equity.

Civil-defence shelters were conceived in a similarly tiered hierarchy. Plans were laid for large *combined public shelters* (kombinerede offentlige beskyttelsesrum or KOBs) intended to protect whole communities, such as commuters and shoppers in the downtown. Small to mid-size BDGs could house people on the go, while *sikringsrum* (SRs) served individual buildings or immediate neighbourhoods. The “inequity” and “inadequacy” we revealed partly stem from the fact that this layered infrastructure was planned but not built yet by 1951.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"robin": [], "subma": []}} editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Recognising this hierarchy also highlights the tension between aggregate planning and granular evaluation. The civil defence administration designed its network at the level of community or suburb—ensuring that each major residential zone contained at least some protective capacity—rather than at the fine-grained level of individual buildings. Our digital workflow, by contrast, computes distances from every building centroid to every shelter centroid, yielding insights that would have been inaccessible to mid-century planners. To assess their implementation fairly, we would therefore have to “compare apples with apples”: aggregate our granular results to the same spatial scale at which the original planning decisions were made. Doing so might reveal that, at the district level, the Aarhus system was more balanced than the building-level inequities suggest; however, at this point, we cannot put this proposition to the test as no map of the original borders of civil-defence districts survives.

Our results nonetheless underscore the geographic sophistication of mid-century planners operating under significant constraints. Working only with aggregated data and without digital modelling capacity, Aarhus civil defence planners achieved a shelter distribution that broadly followed principles of vertical equity, effectively navigating what we now recognise as the Modifiable Areal Unit Problem (MAUP) - a concept formalised in the 1950s (<cite id="robin"><a href="#zotero%7C15824328%2FWB7HMGGW">(Robinson, 1950)</a></cite>; <cite id="subma"><a href="#zotero%7C15824328%2FJDH7C4SF">(Subramanian et al., 2009)</a></cite>), just as shelter planning was underway. Geography is inherently scale-dependent, and the planners’ “common sense” understanding of this principle allowed them to prioritise high-density, high-risk areas without the computational tools we take for granted today.

The difference between these scales is not merely technical but conceptual. The planners’ task was to ensure resilience at the community level, where shelters acted as collective infrastructure; our task is to evaluate equity at the individual level, where shelters become personal entitlements. The former logic was defensive and probabilistic, providing “enough” protection for likely targets, while the latter is distributive and normative, ensuring “equal” protection for everyone. Seen from this angle, the city’s pattern of shelters represents not a failure of foresight but a historical expression of the planning rationality at the time.

This scale-sensitive interpretation also clarifies how our dual-model distance framework can be meaningfully related to the historical planning hierarchy. Euclidean distances capture the idealised geometric reach of shelters, the way the planners likely visualised coverage on paper, using circular radii drawn on city maps. Network distances, meanwhile, approximate the friction of actual pedestrian movement within those circles. The divergence between the two measures does not invalidate the original plan; it quantifies the difference between planned intent and experienced accessibility. In this sense, digital modelling complements rather than contradicts historical urbanism: it reconstructs the operational realities underlying schematic plans.
<!-- #endregion -->

The Aarhus case shows that digital spatial history can move beyond mere visualisation toward a genuine critique of historical data regimes. The disparities we observe between Euclidean and network models, between downtown and suburban zones, or between our building-level metrics and the planners’ district-level aggregates, are not simply measurement errors. They are manifestations of changing ways of knowing and governing space - from strategic adequacy to distributive fairness, from community resilience to individual entitlement.

Both themes - epistemic change over time and scale-sensitive interpretation - point to the same methodological conclusion. A digital reconstruction of past spatial systems should not be treated as a retrospective audit, but as an instrument of historical understanding. By confronting mid-century aggregate planning with contemporary granular analysis, we expose the layered epistemologies of spatial equity itself.

In this light, the uneven accessibility of shelters in 1951 Aarhus is less an indictment of Cold War planning than an illustration of how the city - and our expectations of it - have evolved. The same infrastructure that once embodied collective security now becomes a dataset through which we can interrogate the epistemological transformation of urban equity itself.

<!-- #region slideshow={"slide_type": ""} -->
## Conclusion
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
This study has reconstructed the spatial distribution of civil defence shelters in Aarhus, Denmark, as of 1951, revealing a moderately unequal but strategically rational pattern of urban protection. Using digitized archival records and place-based accessibility measures, we found that approximately 50–77% of buildings fell within the mandated 300-meter threshold (depending on whether network or Euclidean distance was applied), but that aggregate capacity remained severely inadequate—covering only 11% of the city’s population. Shelters concentrated in the densely built urban core, where occupation density, social interaction, and perceived vulnerability were highest, while suburban areas remained comparatively underserved. This distribution fulfilled vertical equity requirements: protection scaled with need, prioritising workers and lower socioeconomic residents in the downtown over more affluent suburban villa-dwellers.

Our findings also illuminate a deeper methodological and historiographical point. The apparent inequities we detected at the building level may not reflect failures of planning so much as differences in the scales at which equity was conceived and measured. Mid-century civil defence administrators worked with aggregate data—population totals by suburb, counts of buildings and shelter places—and designed their protective network at the district or community scale. Our analysis, by contrast, evaluates accessibility at the granular level of individual building centroids, employing computational tools and data infrastructures that postdate the Cold War entirely. The mismatch between these two epistemic regimes means we are not simply adding detail to the planners’ picture; we are producing a qualitatively different picture, one grounded in contemporary expectations of distributive fairness and individual entitlement rather than collective resilience and strategic adequacy.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In contemporary Denmark, we are fortunate to work at multiple analytical scales simultaneously. For this study, we chose the individual building level and assembled a reasonably realistic - if imperfect - historical dataset from digitized archival sources, modern building registers, and OpenStreetMap road networks. While uncertainties remain (incomplete records of private shelters, approximations in the road network, challenges in geocoding), this dataset has allowed us to revisit historical claims and planning outcomes in far greater detail than was previously possible. Importantly, our fine-grained analysis does not contradict the knowledge or intentions of mid-century planners. On the contrary, the results are reasonably compatible with their aggregate assessments and demonstrate that effective, equity-conscious urban design was possible before computers—a testament to the enduring value of geographic reasoning and strategic spatial thinking.

By confronting mid-century aggregate planning with contemporary granular analysis, this study reveals not only the uneven geography of Cold War preparedness but also the evolving epistemologies of spatial equity itself. The same infrastructure that once embodied collective security now becomes a dataset through which we can interrogate how cities - and our expectations of them - have transformed. Digital spatial history, in this sense, is less a retrospective audit than an instrument of historical understanding, one that makes visible the layered rationalities and changing scales through which urban justice has been imagined and enacted.
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
In 2025 there is renewed attention - both in Denmark and abroad - to civil defence shelters as a core element of preparedness. Since the early 1990s, many shelters have been closed, repurposed, or simply left to deteriorate, and officials are again surveying location, capacity, and condition amidst incomplete national records. In that context, the Aarhus case is directly relevant: our reconstructed, city-wide dataset fills historical gaps (no comprehensive catalogue existed until recently) and shows how equity depends on both distance and capacity—offering concrete guidance for where new shelters would do the most good today. With fewer shelters today than during the Cold War and a larger population, any ambition for a high protection factor will require tough siting choices that jointly optimise accessibility and capacity—not one without the other—and explicitly weigh centre–periphery trade-offs. Equity and “distance” are not single ideas but families of choices that generate different, yet defensible, pictures of fairness. Equity in shelter planning is not straightforward, because different measurement frameworks—proximity vs. network access, distance-based coverage vs. capacity-based availability—highlight different needs and beneficiaries. As priorities shift with the metric, “who is protected first” becomes a question of explicit trade-offs rather than a single, objective answer. This article makes such assumptions visible and offers a structured way to compare metrics and articulate equity choices in future planning.
<!-- #endregion -->

## Acknowledgments


This work was made possible thanks to the funding from the Augustinus Fonden grant no. 22-1546. We are grateful to our partners at the Aarhus City Archive, Danish Cold War Association, East-Jutland Firebrigade, and Danish Building Register for their guidance and assistance in data discovery and processing. Special thanks to Ulrik Nielsen from VurderingsStyrelsen.dk for the digitized historical BRD data. We also owe great thanks to our student research assistants and volunteers who helped with shelter data streamlining and verification: Lise S Jensen, Maria Christensen, Agnes Rosendal, Andreas Mikkelsen, Aiswarya Roy, Vasilia Georgoudi, Carl Emil Thomassen, Stine Lykke Thomassen, Angel Bogdanov Grigorov, and Sahel Samsam. 

```python slideshow={"slide_type": ""}
# Check your Python version
from platform import python_version
python_version()

#!python -V
```

```python
import sys
import pkg_resources

# Get all imported top-level modules from current session
imported_modules = set()
for module_name in sys.modules.keys():
    # Get top-level package name (before first dot)
    top_level = module_name.split('.')[0]
    # Skip built-ins and private modules
    if not top_level.startswith('_') and top_level not in ['sys', 'os', 'builtins']:
        imported_modules.add(top_level)

# Get installed versions for imported packages
requirements = []
for package in sorted(imported_modules):
    try:
        version = pkg_resources.get_distribution(package).version
        requirements.append(f"{package}=={version}")
    except:
        # Not an installable package (built-in or standard library)
        pass

# Write to requirements.txt
with open('requirements.txt', 'w') as f:
    f.write('\n'.join(requirements))
```

<!-- #region slideshow={"slide_type": ""} -->
## BIBLIOGRAPHY
<!-- #endregion -->

<!-- #region slideshow={"slide_type": ""} -->
<!-- BIBLIOGRAPHY START -->
<div class="csl-bib-body">
  <div class="csl-entry"><i id="zotero|15824328/M9TJ4CD4"></i>Bjørnsson, I., Farbøl, R., &#38; Sylvest, C. (2020). Hvis krigen kommer. Forestillinger om fremtiden under den kolde krig. <i>Kulturstudier</i>, <i>1</i>. <a href="https://www.politics-society.aau.dk/research/projects/project/hvis-krigen-kommer.cid471739">https://www.politics-society.aau.dk/research/projects/project/hvis-krigen-kommer.cid471739</a></div>
  <div class="csl-entry"><i id="zotero|15824328/HZA9IWBR"></i>Brown, J. (1988). “A Is for Atom, B Is for Bomb”: Civil Defense in American Public Education, 1948–1963. <i>The Journal of American History (Bloomington, Ind.)</i>, <i>75</i>(1), 68–90. <a href="https://doi.org/10.2307/1889655">https://doi.org/10.2307/1889655</a></div>
  <div class="csl-entry"><i id="zotero|6622720/SCHC3PRS"></i>Dynes, A. M. (2020). Which citizens do elected officials target with distributive spending? A survey experiment on U.s. municipal officials. <i>American Politics Research</i>, <i>48</i>, 579–595.</div>
  <div class="csl-entry"><i id="zotero|6622720/N8TM4I9E"></i>Faraji Sabokbar, H., Mohammadi, H., Tahmasbi, S., Rafii, Y., &#38; Hosseini, A. (2021). Measuring spatial accessibility and equity to healthcare services using fuzzy inference system. <i>Appl. Geogr.</i>, <i>136</i>(102584), 102584.</div>
  <div class="csl-entry"><i id="zotero|6622720/JC3PUXPF"></i>Feitosa, F. O., Wolf, J. H., &#38; Lourenço Marques, J. (2024). Operationalizing spatial justice in urban planning: bridging theory with practice. <i>Urban Res. Pract.</i>, <i>17</i>(5), 720–736.</div>
  <div class="csl-entry"><i id="zotero|6622720/K7M5TBAW"></i>Gandy, M. (2002). Between Borinquen and the <i>barrio</i>: Environmental justice and New York city’s Puerto Rican community, 1969–1972. <i>Antipode</i>, <i>34</i>(4), 730–761.</div>
  <div class="csl-entry"><i id="zotero|6622720/6I29TNNW"></i>Gandy, O. H., Jr. (2013). Wedging equity and environmental justice into the discourse on sustainability. <i>tripleC Commun. Capital. Crit. Open Access J. Glob. Sustain. Inf. Soc.</i>, <i>11</i>(1), 221–236.</div>
  <div class="csl-entry"><i id="zotero|6622720/IJ8B5CBF"></i>Garnier, J.-P. (2014). Le droit à la ville de Henri Lefebvre à David Harvey: Entre théorisations et réalisation. <i>L’Homme &#38; La Société</i>, <i>n° 191</i>(1), 59–70.</div>
  <div class="csl-entry"><i id="zotero|6622720/NBJQ333D"></i>Harvey, D. (1996). <i>Justice, nature and the geography of difference</i>. Blackwell.</div>
  <div class="csl-entry"><i id="zotero|6622720/8JF2XJXH"></i>He, S., Wu, Y., &#38; Wang, L. (2020). Characterizing horizontal and vertical perspectives of spatial equity for various urban green spaces: A case study of Wuhan, China. <i>Front. Public Health</i>, <i>8</i>, 10.</div>
  <div class="csl-entry"><i id="zotero|6622720/ZZZCKDM6"></i>Kunzmann, K. R. (1998). Planning for spatial equity in Europe. <i>Int. Plan. Stud.</i>, <i>3</i>(1), 101–120.</div>
  <div class="csl-entry"><i id="zotero|6622720/9KE5ZI6E"></i>Lefebvre, H. (1968). <i>Le Droit À La Ville</i>. Anthropos.</div>
  <div class="csl-entry"><i id="zotero|6622720/8UJADEGR"></i>Lineberry, R. L. (1977). <i>Equality and urban policy</i>. SAGE Publications.</div>
  <div class="csl-entry"><i id="zotero|6622720/M2685VEA"></i>Ma, F. (2020). Spatial equity analysis of urban green space based on spatial design network analysis (sDNA): A case study of central Jinan, China. <i>Sustainable Cities and Society</i>, <i>60</i>, 102256.</div>
  <div class="csl-entry"><i id="zotero|6622720/8954MTJU"></i>Taleai, M., Sliuzas, R., &#38; Flacke, J. (2014). An integrated framework to evaluate the equity of urban public facilities using spatial multi-criteria analysis. <i>Cities</i>, <i>40</i>, 56–69.</div>
  <div class="csl-entry"><i id="zotero|6622720/95SGSHZX"></i>Talen, E., &#38; Anselin, L. (2021). City cents: Tracking the spatial imprint of urban public expenditures. <i>Cities</i>, <i>108</i>, 102962.</div>
  <div class="csl-entry"><i id="zotero|6622720/DRI3ZNFV"></i>Wei, F. (2017). Greener urbanization? Changing accessibility to parks in China. <i>Landsc. Urban Plan.</i>, <i>157</i>, 542–552.</div>
  <div class="csl-entry"><i id="zotero|6622720/MN6ANFTM"></i>Werna, E. (2000). Urban management and the pluralistic supply of services. In <i>Combating Urban Inequalities</i> (pp. 15–32). Edward Elgar Publishing.</div>
</div>
<!-- BIBLIOGRAPHY END -->
<!-- #endregion -->
