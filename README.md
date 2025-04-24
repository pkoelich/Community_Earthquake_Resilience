# Community Earthquake Resilience Visualizer

## 1. Introduction
The entirety of British Columbia's south coast experiences frequent seismic activity as it sits on top of the Cascadia Subduction Zone, where the Juan de Fuca plate subducts beneath the North American plate. As it is a hotspot for seismic activity, residents of the area usually hear about "The Big One", a magnitude 9.0 earthquake projected to happen at some point, whenever an earthquake is felt. Even if it isn't 'The Big One' earthquakes are a credible threat to public safety and it is important that we are constantly improving our preparedness in case of an emergency.

Also important is identifying vulnerable areas, where people might be more at risk of suffering severe consequences should an earthquake occur. We have chosen the city of Surrey, British Columbia, as the subject for a proof-of-concept
We have identified several factors that might lead to populations being more vulnerable to earthquakes, and have generated a map scoring these factors via an Analytic Heirarchy Process(AHP), to perform a Multiple-Criteria Decision Analysis(MCDA), identifying areas where community resilience is likely to be higher in case of an earthquake emergency scenario. 

### Factors:
1. Building age - older buildings are usually not built to the same standard as newer ones, and have wear-and-tear applied to them which makes them more vulnerable to earthquakes.
2. Housing suitability - shows where more people live in housing that requires major repairs or is considered unsuitable according to Statistics Canada. This means either overcrowded housing or houses that might suffer more damage in case of an earthquake
3. Age of residents - people under the age of 14 and over the age of 65 were considered more vulnerable, as they are likely to require more care in an emergency scenario.
4. Language/Communication -  using the number of people who do not speak either English or French, the two official languages of Canada, we can find areas where there might be difficulty communicating with emergency services.
5. Proximity to hospitals - assuming the hospital does not get severely damaged by an earthquake, how close you are to the hospital means greater access to treatment 
6. Proximity to urgent care centres -  assuming the buildings do not get damaged by the earthquake, it is easier to recieve treatment there the closer you are to it.


## 2. App description

This application is an interactive dashboard that showcases earthquake resilience by census dissemination in Surrey, BC. The user can switch from looking at the overal resilience score, to the individual indices that make up the score by selecting an indices in the Display Index dropdown. There is also a chart widget, where users can select an individual dissemination area to show a bar chart or a radar chart to showcase the distribution of scores in a specific dissemination area. When mousing over a dissemination area, a popup shows some more relevant information as well. 

## Features

- Interactive map visualization of earthquake resilience metrics across different regions
- Color-coded regions based on various resilience indicators
- Multiple visualization metrics with detailed legends
- Interactive charts (bar and radar) for comparing different resilience factors
- Detailed region-specific information displayed on selection
- Responsive design that works on desktop and tablet devices
- Dark mode UI for improved visibility of data

## Getting Started

### Prerequisites

- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/community-earthquake-resilience.git
   cd community-earthquake-resilience
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open your browser and navigate to `http://localhost:3000`

### Project Structure

```
community-earthquake-resilience/
├── public/
│   ├── data/
│   │   └── map-data.geojson   # GeoJSON data with resilience metrics
│   └── index.html
├── src/
│   ├── components/
│   │   └── LeafletDashboard/
│   │       ├── LeafletDashboard.jsx
│   │       └── LeafletDashboard.css
│   ├── App.js
│   └── index.js
└── README.md
```

### Technologies Used

- [React](https://reactjs.org/) - Frontend framework
- [Leaflet](https://leafletjs.com/) - Interactive maps
- [Recharts](https://recharts.org/) - Data visualization charts
- [GeoJSON](https://geojson.org/) - Geographic data format

### License

This project is licensed under the MIT License - see the LICENSE file for details.

### Acknowledgments
- Map data © OpenStreetMap contributors

## 2. Methods

This information product is derived from a series of indices, which were derived from raw open data, some of which was obtained from geo.ca. The methods for deriving the 

### Proximity to hospital

This was created using a road network for the City of Surrey, and scores were assigned based on whether most of the dissemination area was within an appropriate walking distance of a hospital. The distance thresholds used were 500, 1000, and 1500 metres. The score was then min-max normalized for use in the AHP.

### Proximity to urgent care centres

This was created using a road network for the City of Surrey, and scores were assigned based on whether most of the dissemination area was within an appropriate walking distance of an urgent care centre. The distance thresholds used were 500, 1000, and 1500 metres. The score was then min-max normalized for use in the AHP.

### Communication

Using census data, we are able to find out what proportion of a Dissemination area did not speak either official language in Canada. The score was then min-max normalized for use in the AHP.

### Building Age



### Housing Suitability

### Age of Resident





## References

## Information Sources

| Name    | Source |    link | 
| -------- | ------- |  ------- |
| Dissemination area digital boundary 2021 | Statistics Canada | [Link](https://www150.statcan.gc.ca/n1/en/catalogue/92-169-X) |
| 2021 Surrey Census - Dissemination Area Level| City of Surrey   | [Link]([https://data.surrey.ca/dataset/2021-surrey-census/resource/808a285b-268a-4e3b-9493-78208c6d0481)     |
| Road Centrelines    | City of Surrey    |  [Link](https://data.surrey.ca/dataset/road-centrelines)   |
| Building Inventory | City of Surrey  | [Link](https://data.surrey.ca/dataset/building-inventory) |
| Hospitals in BC | BC Open Data via geo.ca | [Link](https://app.geo.ca/result?id=383eaf98-afd7-436a-9556-67ecf14f64a7&lang=en) |
| Primary and Urgent Care Centres | BC Open Data via geo.ca | [Link](https://catalogue.data.gov.bc.ca/dataset/urgent-and-primary-care-centres)

### Articles

[CTV News - When will the 'Big One' earthquake hit? Scientists weigh in](https://www.ctvnews.ca/climate-and-environment/article/when-will-the-big-one-earthquake-hit-scientists-weigh-in/#:~:text=In%20the%20context%20of%20Canada,is%20a%20game%20of%20probability.&text=It's%20like%20guessing%20exactly%20which,rough%20estimates%20based%20on%20probability.) <br>

[CTV News - B.C. earthquake highlights Vancouver’s vulnerability should the ‘Big One’ arrive](https://www.ctvnews.ca/vancouver/article/bc-earthquake-highlights-vancouvers-vulnerability-should-the-big-one-arrive/#:~:text=According%20to%20the%20City%20of,city's%20residents%20would%20be%20displaced.) <br>

[Statistics Canada - Housing Suitability](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=4610005901)

### Video Sources

[Pexels Video by Everett Bumstead](https://www.pexels.com/video/aerial-view-of-surrey-cityscape-with-skyscrapers-28939455/)
[Pexels Video by Vlad Vasnetsov](https://www.pexels.com/video/flying-over-lagoon-28167396/)

### Image Sources
[Carie Frantz (Carie027), CC0, via Wikimedia Commons](https://upload.wikimedia.org/wikipedia/commons/0/0e/Cascadia_Subduction_Zone.svg)


