---

title: "Assignment #1"
date: 2026-10-03
tags:
- Assignment

---

## Background & Expectations

Being born and raised in Saudi Arabia, I chose it since I already had deep knowledge about its history, geography, and features. Geographically, it straddles the Arabian Peninsula, which means the landscape is dominated by arid desert plateaus and vast sand expanses like the Rub' al-Khali. Simultaneously, it has long stretches of coastline along the Red Sea and Arabian Gulf, and this is where the majority of the population density is naturally concentrated (Central Intelligence Agency, 2026). Economically, the country has been a textbook petro-state (although this is slowly changing), wherein the economy, government revenue, and political power depend heavily on the extraction and export of oil (International Monetary Fund, 2024). Thus, I predicted that the map would cluster tightly around the coastal peripheries and eastern oil basins, while the desert interior would be mostly unmapped.

## Feature Selection & Justification

Immediately, I noticed that the 27,719 Saudi records on GeoNames were dominated by physical features; it contained 10,436 terrain records and 8,040 hydrographic records, compared with just 2,307 spot features (i.e., buildings) and 1,224 area features (i.e., parks). Despite the dataset being weighted towards physical features instead of man-made features, I decided to focus on oilfields (OILF), ports (PRT), and airports (AIRP) as my feature codes. After filtering for these, my map contained only 80 records, including 26 oilfields, 12 ports, and 42 airports. The reason I selected these codes was because they seemed capable of telling a connected story. Specifically, oilfields represent extraction, ports connect production/trade to maritime routes, and airports show yet another form of domestic and international connectivity. The choice also connects to my background as a Business major because infrastructure like the ones mentioned above obviously affects where firms operate, how goods and people move, and which regions become integrated into wider markets.

*Interactive Map 1 - Visualization displaying the distribution of oilfields (OILF), ports (PRT), and airports (AIRP) across Saudi Arabia, rendered over Esri topographical basemap tiles.*
<div style="width:100%; height:70vh;">
  <iframe
    src="{{ '/assets/maps/SA_featuremap.html' | relative_url }}"
    style="width:100%; height:100%; border:0;"
    loading="lazy"
    title="Interactive map of Saudi Arabian oilfields, ports, and airports">
  </iframe>
</div>

## Map Analysis

The first and clearest pattern is the cluster of orange oilfield points in the Eastern Province and along the Arabian Gulf. This definitely matched my expectations, since Saudi Aramco's own account places the beginnings of its exploration in the Eastern Province and identifies Ghawar and Safaniya (one onshore and one offshore) as two of the world's largest oilfields. (Saudi Arabian Oil Company, 2025) Similarly, the Sharqia Development Authority (the premier authority in developing the Eastern Province) states that the region's development clusters around oilfields, refineries, pipelines, and the cities of Dammam and Jubail (Sharqia Development Authority, n.d.). Thus, the GeoNames points correspond to a real and well-established concentration of petroleum activity.

*Figure 2. Eastern Saudi Arabia contains the map's densest overlap of oilfields, ports, and airports*
<img
  src="{{ '/assets/images/figure-2.png' | relative_url }}"
  alt="Map showing the concentration of oilfields, ports, and airports in Eastern Saudi Arabia"
  style="width:100%; height:auto;"
/>

Alongside the oilfields that span both inland and offshore, ports appear around the Dammam Jubail coast. As a result, the map reveals that this is an integrated system in which extraction sites connect to industrial cities and ports. In other words, raw petroleum is extracted, refined, and distributed through supertankers operating in the Arabian Gulf.

Airports, on the other hand, produce a very different pattern. Blue points appear across the north, west, center, and south, including places where neither oilfields nor ports are visible. This makes airports the most nationally distributed layer and reflects the fact that Saudi Arabia has over 2 million square kilometers of desert terrain through which intercity road networks and passenger railways were historically tough to build (Central Intelligence Agency, 2026). Consequently, airports became the essential connective tissue that links even the most far flung provinces to the rest of the country.

*Figure 3. Airports are spread throughout inland regions, thereby connecting otherwise more isolated parts of the country, while ports hug the Red Sea and no OILF points appear.*
<img
  src="{{ '/assets/images/figure-3.png' | relative_url }}"
  alt="Map showing airports and ports across western and southern Saudi Arabia"
  style="width:100%; height:auto;"
/>

## Linking to Kitchin and Lauriault

One surprising note was how small the oil layer looked, with just 26 oilfields shown for a country that produces approx. 10% of global crude oil. Even the other elements of Saudi petroleum infrastructure are lacking: GeoNames lists only 3 refineries, 9 oil pumping stations, 15 gas-oil separator plants, and 3 oil pipeline terminals. This really dismantles the assumption that GeoNames provides a complete and objective catalog of reality. This is also exactly where Kitchin and Lauriault's idea of a data assemblage becomes useful. They argue that data cannot be thought of just as a raw representation of the world waiting to be mined. Instead, they argue that data is always already cooked and situated within complex socio-technical systems that they term data assemblages. More specifically, a data assemblage involves things like standards, political priorities, economic interests, and methods of classification (Kitchin & Lauriault, 2014).

When seen through this lens, GeoNames is an open data assemblage that still has some biases and gaps in its data. In particular, the primary source of international data is the National Geospatial-Intelligence Agency's GEOnet Names Server, a database maintained by the U.S. military and foreign intelligence apparatus (National Geospatial-Intelligence Agency, n.d.). This means the ontology (system of categories used to organize the database) of GeoNames was not authored by local voices (e.g., local communities or municipal planners in Saudi Arabia) and instead originates from the U.S. government's standards. In addition, unlike many European countries, Saudi Arabia has no domestic ambassador to notice missing, outdated, or mistranslated information. So, in our case, the reason there are only 26 recorded oilfields and low amounts of oil infrastructure data points is not because that's the truth on the ground of Saudi infrastructure, but because of the gaps in the data assemblage-this being an external intelligence dataset that only records general landmarks rather than compiling a truly complete inventory of the country's energy grid.

## Linking to Do Maps Lie

The *Do Maps Lie?* video showcases how two maps can use the same underlying data and still support different arguments through classification/design. Its broader point is that maps are not neutral, and viewers should ask who made a map, why it was made, and what it actually shows (Do Maps Lie?, n.d.). Of course, my map does not deliberately present false data, but it can still lead to misleading conclusions. For instance, the bright eastern oilfield cluster can make Saudi Arabia appear economically defined by one region and one industry, even though there has been increasing amounts of diversification away from oil as well as economic dynamism in regions aside from the Eastern Province (International Monetary Fund, 2024). In addition, the many airport markers can suggest uniform levels of connectivity even though the map provides no information about passenger traffic, destinations, capacity, or frequency of service associated with those airports.

The interactive controls partly address this problem because readers can switch layers on and off, zoom into particular regions, and click individual points. That allows them to see how the story changes when one category disappears. Yet, interactivity does not remove the author's power. I selected the country, the three codes, the colors, the basemap, the opening zoom, and the screenshots. Thus, even such a clean and technically accurate visualization was still built from my choices at the end of the day.

## Transferability And Final Takeaways

This workflow would definitely be useful in future work since the steps it combines (data cleaning, filtering, visualization, and critical interpretation) can be generalized to basically any job. As an example, a similar process could map branch locations, suppliers, customers, transport infrastructure, competitors, etc. Thus, it is infinitely transferable to a range of use cases I might encounter in my future career (I'm not sure about what career it might be yet, but these skills transfer onto any of the sorts of careers that a business major usually goes into).

Also, while the technical steps are important, another thing to note is that the critical-data perspective adds an equally important habit in my mind: to always check who produced the data, what categories were used, what is missing, and what claims the map can actually support. This is especially important considering the fact that, in corporate environments, analysts frequently treat third-party market data and corporate databases as indisputable facts. Working directly with GeoNames showed me that every database is an assemblage shaped by things like omissions, commercial biases, and structural limitations.

## Generative AI Statement

I used Gemini AI and Perplexity AI to check my grammar and spelling as well as to generate the transcript of the *Do Maps Lie?* Video so I could read it instead of watching (I prefer being able to have the full thing in front of me in text format).

## References

Central Intelligence Agency. (2026). *Saudi Arabia*. In *The World Factbook*. https://www.cia.gov/the-world-factbook/countries/saudi-arabia/

*Do maps lie?* (n.d.). [Video transcript]. Course material.

International Monetary Fund. (2024, September 4). *IMF Executive Board concludes 2024 Article IV consultation with Saudi Arabia*. https://www.imf.org/en/news/articles/2024/09/03/pr24316-saudi-arabia-imf-exec-board-concludes-2024-art-iv-consult

Kitchin, R., & Lauriault, T. P. (2014). *Towards critical data studies: Charting and unpacking data assemblages and their work* (The Programmable City Working Paper No. 2). National University of Ireland Maynooth. https://doi.org/10.2139/ssrn.2474112

National Geospatial-Intelligence Agency. (n.d.). *About NGA*. Retrieved October 3, 2026, from https://www.nga.mil/about/About_Us.html

Saudi Arabian Oil Company. (2025). *Saudi Aramco annual report 2024*. https://www.aramco.com/en/investors/annual-report

Sharqia Development Authority. (n.d.). About Sharqia. Retrieved May 18, 2024, from https://sda.gov.sa/about-sharqia?ltr=true

READY FOR GRADING

```