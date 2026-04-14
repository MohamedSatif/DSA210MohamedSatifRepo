# Analyzing how we mistakenly use Milk for calcium by loosing its benifits through heat!

DSA 210 – Introduction to Data Science (Spring 2026)

Student - Mohamed Satif 

# Project Title:
Temperature and Nutrient Stability: An Analysis on the effect of heat on the calcium content within milk. 

# Research Question: 
Does heating milk affect its calcium content enough to impact its nutritional reliability?

# Motivation:
Milk and plant-based alternatives are widely recognized as primary dietary sources of calcium, a mineral essential for bone strength, muscle function, and overall physical performance. As someone who regularly goes to the gym and has experienced multiple bone fractures in the past, maintaining adequate calcium intake has become personally important to me. This led me to question whether common habits, such as heating milk or consuming it at different temperatures, could influence its nutritional reliability. In a previous experiment, I investigated how temperature affects the calcium content of hazelnut milk, which provided a foundation for understanding temperature-related changes at a chemical level. Building on this, the current study aims to explore whether such variations may have practical implications for individuals who rely on milk and similar beverages as consistent sources of calcium in their daily diet.

# Overview:
This project explores the relationship between temperature and the stability of calcium in milk. By analyzing experimental data collected across different temperature conditions and integrating it with external nutritional and sports science sources, the study investigates whether heating affects the reliability of milk as a primary source of calcium. The goal is to determine whether temperature-induced changes in calcium content may have practical implications for individuals who rely on milk for bone health and athletic performance.

# Data Sources:
1-  Mejares, C.T., Chandrapala, J., & Huppertz, T. (2023). Influence of Calcium-Sequestering Salts on Heat-Induced Changes in Blends of Skimmed Buffalo and Bovine Milk. Foods, 12(12), 2260. MDPI.
URL: https://pmc.ncbi.nlm.nih.gov/articles/PMC10253084/
Data used: Table 1 (particle size, zeta potential), Table 2 (pH, Ca²⁺ activity, viscosity) at 0°C, 85°C, 95°C for bovine skim, buffalo skim, and 50:50 blends.
2-  Magee, H.E., & Harvey, D. (1926). Studies on the Effect of Heat on Milk. Biochemical Journal, 20(4), 873–884. PMC.
URL: https://pmc.ncbi.nlm.nih.gov/articles/PMC1251792/
Data used: Soluble CaO loss percentages at 77°C and after pasteurisation (Bell & Grosser data cited within).
3-  Schreiber, R., Schreiber, G., et al. (2022). Heat-induced changes in milk salts. International Dairy Journal, 129. Elsevier ScienceDirect.
URL: https://www.sciencedirect.com/science/article/pii/S095869462100248X
Data used: Qualitative and quantitative description of Ca-phosphate precipitation thresholds and salt balance shifts under heat.
4-  Pouliot, Y., Boulet, M., & Paquin, P. (1999). Heat-induced changes in the calcium sensitivity of caseins. International Dairy Journal, 9(3–6). Elsevier ScienceDirect.
URL: https://www.sciencedirect.com/science/article/pii/S0958694600000121
Data used: Relative calcium retention (%) at temperatures 0°C, 70°C, 80°C, 90°C, 120°C.
5-  Rahimi, A., et al. (2024). The Impact of Thermal Treatment Intensity on Proteins, Fatty Acids, Macro/Micro-Nutrients, Flavor, and Heating Markers of Milk. International Journal of Molecular Sciences, 25(16), 8670. MDPI.
URL: https://www.mdpi.com/1422-0067/25/16/8670
Data used: Relative calcium retention (%) at 0°C, 63°C, 72°C, 85°C, 95°C, and 121°C (UHT).
6-  On-Nom, N., Grandison, A.S., & Lewis, M.J. (2010). Measurement of Ionic Calcium, pH, and Soluble Divalent Cations in Milk at High Temperature. Journal of Dairy Science, 93(2), 515–523. Elsevier.
URL: https://www.journalofdairyscience.org/article/S0022-0302(10)71494-6/fulltext
Data used: Ionic Ca²⁺ (mM) measured via dialysis at 20°C, 40°C, 60°C, 80°C, 90°C, 100°C, and 110°C in bovine semi-skim milk. Provides the densest continuous temperature coverage in the dataset (20–110°C).
7-  Tessier, H., & Rose, D. (1958). Calcium Ion Concentration in Milk. Journal of Dairy Science, 41(3). Elsevier.
URL: https://www.journalofdairyscience.org/article/S0022-0302(58)90927-5/pdf
Data used: Ionic Ca²⁺ (mM) at 20°C, 66°C, and 82°C in bovine skim milk. One of the earliest direct Ca²⁺ measurement studies, providing historical validation of the heating trend.
8-  Choi, J., et al. (2013). Effect of Heat-Treatment Methods on the Soluble Calcium Levels in Commercial Milk Products. Food Science of Animal Resources (Korea Science), 33(2).
URL: https://koreascience.or.kr/article/JAKO201319850774909.page
Data used: Soluble Ca (mg/kg) in raw milk (450.2), LTLT-treated (340.7), HTST-treated (309.4), and UHT-treated (375.2) commercial bovine milk. Enables a bar chart comparison of commercial processing methods.

Data Collection Process:
The data will be collected through a literature review process. Relevant studies will be identified, read, and compared based on the heating temperature, heating time, type of milk used, and calcium-related outcomes measured. The data used in this project will mainly be quantitative and experimental. It will include measurements such as temperature, heat treatment, calcium activity, and percentage changes in calcium concentration or solubility.

# Hypothesis:
Increasing the heating temperature and duration of milk will decrease its measurable calcium content due to structural and chemical changes. However, this decrease will plateau after a certain threshold, as milk contains a finite amount of calcium. Therefore, calcium loss will follow a diminishing trend rather than a continuous linear decline.

