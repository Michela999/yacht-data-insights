Datasets Descriptions 📂
This document provides details about the datasets used in the Yacht Data Insights & Prediction project.

1. Boats_Cleaned_dataset.csv (Yacht Sales Dataset)
📌 Purpose: This dataset contains cleaned yacht sales data, which is essential for predicting sales trends and prices. It can be used to model yacht pricing and sales demand over time.
🔹 Key Columns:
    • Boat Name & Type: Identifies the yacht, which can influence its price and demand (e.g., motor yacht, sailing yacht).
    • Length & Beam: These are physical specifications, typically correlated with price. Larger yachts may demand higher prices.
    • Price: The target variable for regression models, representing the sale price of each yacht.
    • Manufacturing Year: Older yachts may depreciate faster, while newer models may demand higher prices.
    • Brand/Manufacturer: Influences the price and demand based on brand reputation and popularity.
    • Location: The geographical location where the yacht is sold, important for determining regional price trends and seasonal demand variations.
    • Sale Date: Helps understand seasonality patterns—some yachts may sell better in specific months or seasons.
    • Condition: Describes the state of the yacht (new, used, refurbished), which can influence the sales price.
🔍 Usage in the Project:
    • Regression models (Linear Regression, Random Forest, SVR) to predict yacht prices and sales trends based on the boat's features (e.g., size, brand, year).
    • Sales forecasting for optimizing maintenance schedules and sales strategies based on the predicted price.

2. Boats_No_Price_dataset.csv (Yacht Data Without Price)
📌 Purpose: Contains yacht data similar to Boats_Cleaned_dataset.csv, but without the price column. This dataset can be used for model training to predict missing prices or for classification tasks.
🔹 Key Columns:
    • Boat Name & Type: Identifies the yacht.
    • Length & Beam: Physical attributes that typically influence pricing.
    • Brand/Manufacturer: Affects the demand and perceived value of the yacht.
    • Year Built: Affects both depreciation and potential future sales trends.
    • Location: Shows the geographical area where the yacht is based or listed for sale.
    • Condition: Indicates whether the yacht is new or used, which can affect pricing.
    • Engine Type & Size: Critical for pricing, as engine specifications often influence a yacht's performance and value.
    • Hull Material & Type: Different materials and hull types can impact a yacht's price, maintenance cost, and demand.
🔍 Usage in the Project:
    • Regression models can be used to predict the missing price by training on the Boats_Cleaned_dataset.csv (which contains the price column) and applying the trained model to this dataset.
    • Alternatively, it can be used for classification tasks (e.g., categorizing yachts based on price ranges or popularity).
    • The data can be used to test feature engineering or optimize predictive models for yacht sales.
3. Boat_Data.csv
📌 Purpose: This dataset contains cleaned yacht and boat sales data, designed for predicting sales trends, pricing, and demand.
🔹 Key Columns:
    • Price: Sales price of the boat.
    • Boat Type: Type of boat (e.g., Motor Yacht, Sport Boat).
    • Manufacturer: Brand of the boat.
    • Type: Sale condition (e.g., new, used, electric-powered).
    • Year Built: Year of manufacture.
    • Length (m): Length of the boat.
    • Width (m): Width of the boat.
    • Material: Construction material (e.g., Aluminium, GRP).
    • Location: Sale region.
    • Number of Views (Last 7 Days): Popularity measure.
🔍 Usage in the Project:
    • Regression Models: Predicting price based on specifications.
    • Sales Forecasting: Optimizing inventory and pricing strategies.

4. Boat_dataset.csv
📌 Purpose: Foundational dataset for predicting trends and optimizing maintenance schedules for yachts.
🔹 Key Columns:
    • Price, Category, Boat Type, Manufacturer, Model, Boat Name.
    • Condition, Year Built, Dimensions, Displacement.
    • CE Design Category, Capacity (People, Cabins, Beds, Toilets, Bathrooms, Showers).
    • Hull Color, Material, Engine Information (Type, Performance, Hours).
    • Fuel & Water Systems (Fuel Capacity, Fresh Water Cap, Holding Tank).
    • Location, Advertisement Date & Views, Comments & Equipment.
🔍 Usage in the Project:
    1. Price Trends Analysis.
    2. Maintenance Optimization.
    3. Predicting Sales and Market Demand.
    4. Developing Predictive Models for Maintenance and Pricing.

5. CVP_encounters_202411.csv (Routes & Sailing Patterns Dataset)
📌 Purpose: Contains data on yacht encounters and routes, which can be used to analyze sailing activity patterns. This dataset can inform predictive maintenance models and provide insight into yacht demand based on location and activity.
🔹 Key Columns:
    • Vessel ID or Boat Name: Identifies the specific yacht associated with each encounter.
    • Date & Time of Encounter: Indicates when the encounter occurred, allowing analysis of seasonal or time-based trends.
    • Latitude & Longitude (Geographical Coordinates): Maps the yacht's position during encounters, important for identifying popular sailing routes or regions with higher demand.
    • Encounter Type: Describes the type of encounter (e.g., near collision, port entry, etc.), providing insights into yacht traffic density and usage.
    • Distance Traveled: The total distance covered, useful for identifying frequently traveled routes or areas.
    • Speed: Represents the yacht's speed, which can provide data for predicting wear and tear or fuel consumption.
    • Port or Harbor ID: Indicates where the yacht entered or exited, providing insights into popular sailing locations and demand hotspots.
🔍 Usage in the Project:
    • Predictive maintenance models can use this data to identify high-traffic routes that may cause more wear and tear on yachts, helping schedule maintenance better.
    • Can be analyzed for seasonality trends by correlating with yacht sales data to identify high-demand locations and times of the year.
    • Demand forecasting can be refined by identifying key regions or routes where yachts are most frequently used, helping companies optimize their sales and maintenance strategies.

6. CVP_loitering_202411.csv (Vessel Loitering Events Dataset)
📌 Purpose: This dataset contains cleaned and structured data on vessel loitering events, which are essential for monitoring maritime activity, detecting suspicious behavior, and analyzing vessel movement patterns. It can be used for anomaly detection, risk assessment, and maritime security applications.
🔹 Key Columns:
    • Event ID: Unique identifier for each detected loitering event.
    • Event Type: Specifies the type of event recorded (e.g., "loitering").
    • Vessel ID: Unique identifier for the vessel involved in the event.
    • Event Start & End: Timestamps (UTC) marking the beginning and end of the loitering event.
    • Lat/Lon Mean: Average latitude and longitude of the vessel during the event.
    • Lat/Lon Min & Max: The minimum and maximum latitudes/longitudes recorded during the event, defining the spatial boundaries of the vessel's movement.
    • Event Info: JSON-structured details including:
        ◦ Median Speed (knots): The vessel’s median speed while loitering.
        ◦ Total Distance (km): Distance traveled during the event.
        ◦ Loitering Hours: Total duration of the loitering event.
        ◦ Distance from Shore (m): Proximity of the vessel to the nearest coastline.
        ◦ Distance from Port (m): Distance to the closest port.
        ◦ Elevation (m): Seabed depth at the vessel’s location (negative values indicate depth).
        ◦ Origin & Destination Port: Details of the port where the vessel departed and its intended destination (if available).
        ◦ Regions: Maritime zones relevant to the event (FAO fishing areas, RFMO zones, EEZ boundaries).
    • Event Vessels: A list of vessels involved in the loitering event, with details such as:
        ◦ Vessel ID: Unique vessel identifier.
        ◦ SSVID: Tracking identifier (e.g., MMSI, IMO).
        ◦ Vessel Name: Official name of the vessel.
        ◦ Flag: Country under which the vessel is registered.
    • Event Geography: Geospatial representation of the event’s central location (POINT lon lat).
🔍 Usage in the Project:
    • Anomaly Detection: Identify suspicious loitering patterns that could indicate illegal fishing, smuggling, or unauthorized vessel activity.
    • Maritime Security & Risk Assessment: Analyze vessel behavior near restricted or high-risk areas.
    • Pattern Recognition & Predictive Modeling: Use clustering algorithms (e.g., DBSCAN) and machine learning models to classify loitering events and predict potential risks.
    • Operational Optimization: Assist maritime authorities and fleet managers in monitoring vessel movement for regulatory compliance and efficiency.
      
      
7. CVP_ports_202411.csv
📌 Purpose: This dataset contains data related to CVP (Customer Value Prediction) ports, essential for analyzing customer behavior in various ports or locations. It can be used to predict customer preferences, port usage, and optimize service offerings.
🔹 Key Columns:
    • Port ID: Unique identifier for each port, allowing tracking of data specific to each location.
    • Port Name: The name of the port, providing clarity on which location the data refers to.
    • Customer ID: Identifies the customer interacting with the port, helping analyze behavior and preferences.
    • Arrival Time: Timestamp of when a customer arrives at the port, useful for analyzing peak usage times.
    • Departure Time: Timestamp of when the customer departs, helping assess the duration of stay and potential usage patterns.
    • Port Type: Specifies the type of port (e.g., commercial, recreational, industrial), influencing customer behavior and port usage.
    • Services Used: A list or categorization of services the customer has used (e.g., docking, fueling, maintenance).
    • Frequency of Visits: Number of visits made by the customer to the port over a certain period, identifying loyal customers or high-traffic users.
    • Spending: Amount spent by the customer at the port during their visit, providing insights into revenue generation.
    • Visit Purpose: Describes the reason for the visit (e.g., leisure, business, transit), useful for targeting specific customer groups.
    • Customer Segment: Customer’s demographic or behavioral classification (e.g., VIP, casual, first-time), useful for personalized marketing strategies.
🔍 Usage in the Project:
    • Customer Segmentation: Identifying different customer types based on visit frequency, spending, and service usage.
    • Regression Models: Predicting customer spending and behavior based on port type, services used, and visit duration.
    • Market Trend Analysis: Understanding service demand at various ports to optimize resource allocation.
    • Predictive Analytics: Using visit data to predict future behavior, return visits, spending habits, and port usage patterns.
    • Customer Lifetime Value (CLV): Estimating long-term customer value based on port interaction history.

8. Weather-for-Boating-Activities.csv
📌 Purpose: This dataset provides information on weather conditions and their impact on boating activities, helping to make decisions regarding boating suitability. It can predict whether the conditions are ideal for boating, based on factors like wind speed, wave height, weather, and boat condition.
🔹 Key Columns:
    • Wind Speed: The speed of the wind (Low, Medium, High), affecting stability and safety.
    • Wave Height: The height of the waves (Low, Medium, High), indicating unsafe conditions for boating.
    • Weather: General weather condition (e.g., Cloudy, Sunny, Rainy), affecting visibility and comfort.
    • Day of the Week: Indicates whether it's a weekday or weekend, influencing boating activity volume.
    • Boat Technical Condition: The state of the boat (Poor, Average, Good), affecting safety and performance.
    • Decision: The final decision (Yes or No) indicating whether conditions are suitable for boating.
🔍 Usage in the Project:
    • Classification Models: Predicting whether weather conditions allow safe boating.
    • Safety Recommendations: Helping boaters and operators make informed decisions.
    • Decision Support System: Forecasting suitable boating days.
    • Pattern Recognition: Identifying patterns in weather and boat condition data for planning purposes.


9. named_anchorages_v1_20181108.csv
📌 Purpose: Provides geospatial information on yacht anchorages, enhancing predictions on yacht routes, maintenance schedules, and sales strategies.
🔹 Key Columns:
    • s2id: Unique identifier for each anchorage.
    • lat, lon: Geographical coordinates.
    • anchorage_group: Classification or grouping of anchorages.
    • country: Country where the anchorage is located.
    • distance_to_marina (m): Distance from anchorage to the nearest marina.
    • marina_name: Name of the nearest marina.
    • num_nearby_services: Number of services available near the anchorage.
    • popular_route: Whether the anchorage is along a commonly used yacht route.
🔍 Usage in the Project:
    • Route Optimization: Predicting optimal yacht routes based on anchorage popularity.
    • Maintenance Insights: Identifying anchorages that may lead to higher maintenance needs due to environmental factors.
    • Sales Strategy: Assessing demand in specific locations to guide inventory placement and marketing strategies.
      
10. named_anchorages_v1_20191205
    • Purpose:
This dataset provides detailed information on maritime anchorages worldwide. It is used to identify and analyze anchorage locations for ships and yachts, including geographic details, distances from shore, and anchorage classifications.
    • Dataset Description:
The dataset contains the following columns:
        ◦ s2id: Unique identifier for the anchorage
        ◦ lat, lon: Geographic coordinates of the anchorage
        ◦ label: Name of the anchorage or destination
        ◦ sublabel: Additional information (if available)
        ◦ label_source: Source of categorization (e.g., "top_destination", "anchorage_overrides")
        ◦ iso3: Three-letter ISO country code where the anchorage is located
        ◦ distance_from_shore_m: Distance of the anchorage from the shore in meters
        ◦ drift_radius: Drift radius of the anchorage (safe space around the vessel)
        ◦ at_dock: Indicates whether the anchorage is actually a dock (TRUE/FALSE)
    • Usage in the "Yacht Data Insights" Project:
This dataset can be used for:
        ◦ Analysis of yacht anchorage destinations: Identifying popular and frequently visited anchorages
        ◦ Route optimization: Helping to plan optimal yacht routes based on shore distance and anchorage safety
        ◦ Anchorage condition forecasting: Combining this data with weather and oceanographic conditions to suggest the best anchorages based on season and real-time conditions
        ◦ Safety and planning: Evaluating anchorages with a low drift radius to ensure vessel stability

11. named_anchorages_v2_20201104
    • Purpose:
This dataset provides an updated collection of maritime anchorage locations worldwide. It is used to analyze and optimize anchorage points for yachts and ships, offering insights into safe docking areas, offshore anchorage zones, and key maritime destinations.
    • Dataset Description:
The dataset contains the following fields:
        ◦ s2id: Unique identifier for the anchorage
        ◦ lat, lon: Latitude and longitude coordinates of the anchorage
        ◦ label: Name of the anchorage or maritime destination
        ◦ sublabel: Additional classification or designation of the anchorage (e.g., "offshore" zones)
        ◦ label_source: Source of the classification (e.g., "anchorage_overrides", "top_destination", "geonames_1000")
        ◦ iso3: Three-letter country code where the anchorage is located
        ◦ distance_from_shore_m: Distance of the anchorage from the nearest shoreline (in meters)
        ◦ drift_radius: Radius indicating the allowable drifting area for vessels at the anchorage
        ◦ at_dock: Boolean flag indicating whether the anchorage is an actual dock (TRUE) or an offshore anchorage (FALSE)
    • Usage in the "Yacht Data Insights" Project:
This dataset is used for:
        ◦ Identification of key yacht anchorage zones: Analyzing popular yacht anchorage destinations and offshore docking areas
        ◦ Route planning and optimization: Suggesting efficient yacht routes based on proximity to shore and designated safe anchorage zones
        ◦ Anchorage safety assessment: Evaluating offshore anchorages based on drift radius, dock availability, and distance from shore
        ◦ Integration with weather and marine traffic data: Combining with real-time weather and maritime traffic data to provide dynamic recommendations for yacht anchoring

12. named_anchorages_v2_20221206.csv
    • Purpose:
The named_anchorages_v2_20221206.csv dataset provides detailed geospatial information about various anchorages, ports, and marine facilities, which can be used for AI-powered systems in the maritime, yachting, and navigation industries. The data helps to analyze geographical locations, docking facilities, distance from shore, and drift radius, offering valuable insights for applications such as route optimization, predictive maintenance, and operational safety.
    • Dataset Description:
The dataset contains the following columns:
        ◦ s2id: Unique identifier for the location
        ◦ lat: Latitude of the anchorage or docking site
        ◦ lon: Longitude of the anchorage or docking site
        ◦ label: Main name/identifier of the anchorage
        ◦ sublabel: Secondary or descriptive name associated with the anchorage
        ◦ label_source: The data source or system from which the information was gathered
        ◦ iso3: The 3-letter ISO code of the country where the anchorage is located
        ◦ distance_from_shore_m: Distance from the nearest shore or coast, in meters
        ◦ drift_radius: Radius indicating how far the vessel can drift in meters from the anchorage point
        ◦ dock: Indicates whether a dock is available at the anchorage (true/false)
    • Usage in the "Yacht Data Insights" Project:
This dataset plays a key role in the project by providing:
        ◦ Route Optimization: Helps identify the most efficient routes for yachts, minimizing fuel consumption and time at sea
        ◦ Predictive Maintenance: Assists in predicting maintenance or emergency repair needs based on docking locations
        ◦ Sales Strategies: Provides insights into popular regions for yacht traffic, influencing demand forecasts
        ◦ Eco-friendly Impact: Helps reduce fuel consumption by optimizing routes and schedules

13. sar_vessel_detections_pipev20231026_202410.csv
    • Purpose:
The SAR Vessel Detections dataset provides synthetic aperture radar (SAR) data for vessel detection in maritime environments. It includes timestamped ship positions, vessel length, detection confidence scores, and classification details. This dataset is valuable for analyzing maritime traffic, vessel presence in specific regions, and optimizing navigation and maintenance strategies.
    • Dataset Description:
The dataset contains the following columns:
        ◦ scene_id: Unique identifier for the SAR image
        ◦ timestamp: Date and time of vessel detection (UTC)
        ◦ lat, lon: Geographic coordinates of detected vessels
        ◦ presence_score: Probability score of the vessel's presence
        ◦ length_m: Estimated vessel length in meters
        ◦ mmsi: Maritime Mobile Service Identity (ship identification number)
        ◦ matching_score: Confidence score for vessel identification
        ◦ fishing_score: Likelihood that the vessel is a fishing boat
        ◦ matched_category: Classification of the vessel (e.g., bunker ship, fishing vessel)
    • Usage in the "Yacht Data Insights" Project:
This dataset is used for:
        ◦ Maritime Traffic Analysis & Route Optimization: Identifying busy zones and optimizing yacht routes
        ◦ Predictive Maintenance & Operational Planning: Evaluating frequent anchorages and environmental factors for maintenance
        ◦ Sales Strategy & Market Demand Forecasting: Identifying high yacht traffic regions for better sales strategies
        ◦ Sustainability & Eco-friendly Impact: Minimizing fuel consumption by analyzing optimal routes and refueling locations

14. sar_vessel_detections_pipev3_202411.csv
📌 Purpose
The SAR Vessel Detections v3 dataset provides updated synthetic aperture radar (SAR) vessel detection data for maritime analysis. It offers precise vessel tracking through timestamped coordinates, vessel size estimations, and classification metrics. This dataset is critical for monitoring maritime traffic, optimizing yacht routes, and enhancing predictive maintenance strategies.
📂 Description
This dataset captures maritime vessel movements via SAR satellite imaging, providing essential attributes such as:
    • scene_id – Unique identifier for the SAR image.
    • timestamp – Date and time of vessel detection (UTC).
    • lat, lon – Geographic coordinates of detected vessels.
    • presence_score – Confidence score indicating vessel presence.
    • length_m – Estimated vessel length (in meters).
    • mmsi – Maritime Mobile Service Identity, a unique ship identification number.
    • matching_score – Confidence level of vessel identification.
    • fishing_score – Probability of vessel being a fishing boat.
    • matched_category – Vessel classification (e.g., bunker, cargo, fishing).
This dataset enables real-time vessel tracking and enhances maritime operational planning by identifying patterns in vessel movement.
🛠 Usage in Yacht Data Insights & Prediction 🚢📊
This dataset plays a key role in the optimization of yacht navigation, sales forecasting, and maintenance scheduling within the Yacht Data Insights & Prediction project.
🔍 Key Applications in the Project:
    1. Real-time Maritime Traffic Monitoring
        ◦ Identify high-density maritime areas to optimize yacht routes and avoid congested shipping lanes.
        ◦ Track large vessel movements (e.g., tankers, bunkers) that impact yacht navigation and docking schedules.
    2. Predictive Maintenance & Operational Efficiency
        ◦ Analyze vessel activity near yacht docking areas to assess the potential impact on hull maintenance.
        ◦ Use historical movement patterns to anticipate periods of increased maritime activity that may accelerate yacht wear and tear.
    3. Sales Strategy & Demand Forecasting
        ◦ Correlate vessel traffic trends with yacht sales and rental demand across different regions and seasons.
        ◦ Use MMSI and vessel categories to distinguish between luxury yachts and commercial vessels for better market segmentation.
    4. Eco-friendly & Sustainable Business Practices
        ◦ Optimize fuel consumption and route planning by avoiding heavy traffic areas.
        ◦ Reduce unnecessary maintenance waste by predicting high-impact areas where yachts require frequent servicing.
🚀 Example Integration with Other Data:
    • Combining with weather datasets to analyze how maritime conditions affect vessel movement and yacht operations.
    • Merging with yacht sales data to identify high-demand regions for yacht rentals and purchases.
    • Using detection timestamps to plan efficient yacht docking and maintenance schedules.
This dataset enhances data-driven decision-making for yacht navigation, maintenance, and business operations, helping companies optimize efficiency and sustainability in the maritime sector.

15. sar_vessel_detections_pipev3_202412.csv
📌 Purpose
The SAR Vessel Detections v3 (December 2024 dataset) provides updated synthetic aperture radar (SAR) vessel detection data for tracking maritime traffic. This dataset is essential for monitoring vessel movements, optimizing yacht navigation, and improving predictive maintenance for maritime operations.
📂 Description
This dataset captures maritime vessel detections using SAR satellite imaging, providing key attributes such as:
    • scene_id – Unique identifier for the SAR image capture.
    • timestamp – Date and time of vessel detection (UTC).
    • lat, lon – Geographic coordinates of detected vessels.
    • presence_score – Confidence score indicating vessel presence.
    • length_m – Estimated vessel length in meters.
    • mmsi – Maritime Mobile Service Identity, a unique ship identification number.
    • matching_score – Confidence level of vessel identification.
    • fishing_score – Probability that the vessel is engaged in fishing activities.
    • matched_category – Vessel classification (e.g., bunker, cargo, fishing).
This dataset provides valuable insights into real-time vessel tracking and maritime activity trends to enhance operational planning.
🛠 Usage in Yacht Data Insights & Prediction 🚢📊
The SAR Vessel Detections v3 (December 2024) dataset plays a critical role in the Yacht Data Insights & Prediction project by improving yacht navigation, predictive maintenance, and sales strategies in the maritime sector.
🔍 Key Applications in the Project:
    1. Maritime Traffic Optimization
        ◦ Identifies high-traffic maritime areas, allowing for more efficient yacht route planning.
        ◦ Detects bunker vessels and large cargo ships, which can impact yacht docking schedules.
    2. Predictive Maintenance & Yacht Safety
        ◦ Analyzes SAR-detected vessel activity near yacht docking zones to anticipate maintenance needs.
        ◦ Correlates presence scores and vessel size to assess risks posed by larger commercial ships.
    3. Market Analysis & Yacht Sales Forecasting
        ◦ Helps forecast yacht demand by analyzing vessel traffic patterns in key maritime regions.
        ◦ Segments maritime zones by vessel type and activity, providing insights into potential yacht customer demographics.
    4. Sustainability & Eco-Friendly Operations
        ◦ Assists in fuel-efficient route planning by identifying traffic-heavy zones.
        ◦ Reduces unnecessary yacht maintenance through data-driven wear-and-tear predictions.
🚀 Example Use Cases & Integrations:
    • Combining with past SAR datasets to analyze seasonal changes in maritime traffic.
    • Merging with weather data to assess how maritime conditions affect vessel movements.
    • Incorporating into predictive models to anticipate yacht maintenance needs based on historical vessel traffic patterns.
This dataset is a key asset for AI-driven maritime analytics, supporting more efficient, data-driven decision-making for yacht navigation, sales, and operational planning. 🚢📊

Both datasets play significant roles in improving the operational efficiency, predictive maintenance, and sustainability of yacht operations, using SAR technology to track and analyze maritime traffic in real time.
