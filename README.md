# AVT_Marigold_Analysis-SQL

# AVT_Marigold_Analysis

USE AVT_Marigold_LE_24;

CREATE TABLE LuteinesterProduction (
    LotNumber VARCHAR(255) PRIMARY KEY,
    MarigoldFlowerWeightUttarakhand DECIMAL(10, 2),
    MarigoldFlowerWeightKarnataka DECIMAL(10, 2),
    MarigoldFlowerWeightTamilNadu DECIMAL(10, 2),
    HexaneUsedKG DECIMAL(10, 2),
    MethanolUsedKG DECIMAL(10, 2),
    AcetoneUsedKG DECIMAL(10, 2),
    LuteinesterProducedBeforeDryingKG DECIMAL(10, 2),
    TotalLuteinesterProductionKG DECIMAL(10, 2),
    TotalLuteinesterOversForRegrinding DECIMAL(10, 2),
    DateOfWork DATE,
    TotalCarotenoids DECIMAL(10, 2),
    TotalResidualSolventPPM INT,
    TotalTimeTakenHours DECIMAL(10, 2),
    TimeBefore2ndWaterMixingHours DECIMAL(10, 2),
    TimeAfter2ndWaterMixingHours DECIMAL(10, 2),
    Yield DECIMAL(10, 4),
    WetCakeTC DECIMAL(10, 2),
    WetCakeRSPPM INT
);


INSERT INTO LuteinesterProduction VALUES 
('MLE 01/23 B1',	0,	0,	10000,	30000,	30000,	120000,	57.5,	46.46,	0.5,	'04/01/23',	66.31,	74,	44,	28,	16,	0.004646,	69.51,	357),
('MLE 01/23 B2A',	0,	0,	1250,	3750,	3750,	15000,	7.5,	6.63,	0.1,	'04/01/23',	66.79,	114,	44,	28,	16,	0.005304,	69.79,	465),
('MLE 01/23 B2B',	0,	0,	10000,	30000,	30000,	120000,	48.5,	44.86,	0.7,	'06/01/23',	63.55,	106,	46,	29,	17,	0.004486,	67.55,	527),
('MLE 02/23 B1',	10000,	0,	0,	30000,	30000,	120000,	14.5,	13.23,	0.2,	'06/01/23',	64.34,	91,	58,	29,	29,	0.001323,	66.84,	399),
('MLE 02/23 B2',	10000,	0,	0,	30000,	30000,	120000,	15.1,	13.7,	0.0,	'09/01/23',	64.43,	56,	47,	26,	21,	0.00137,	67.93,	367),																		
('MLE 03/23 B1',	20000,	0,	0,	60000,	60000,	240000,	29.0,	23.82,	0.1,	'09/01/23',	64.43,	80,	47,	25,	22,	0.001191,	68.63,	380),
('MLE 03/23 B2',	10000,	0,	0,	30000,	30000,	120000,	12.7,	9.00,	0.3,	'09/01/23',	55.82,	127,	51,	32,	19,	0.0009,	60.82,	468),
('MLE 04/23 B1' ,	0,	15000,	0,	45000,	45000,	180000,	21.25,	19.85,	0.4,	'13/01/23',	61.85,	140,	30,	22,	8,	0.001323333,	64.55,	521),
('MLE 64/23 B1',	0,	0,	10000,	30000,	30000,	120000,	42.0,	40.0,	0.4,	'07/11/23',	63.79,	189,	30,	24,	6,	0.004,	67.89,	567),																			
('MLE 64/23 B1B',	0,	0,	5000,	15000,	15000,	60000,	24.0,	19.98,	0.2,	'10/11/23',	63.6,	56,	35,	25,	10,	0.003996,	66.9,	345),	
('MLE 58/23 B1',	0,	0,	5000,	15000,	15000,	60000,	24.3,	20.0,	0.1,	'13/10/23',	64.4,	54,	32,	22,	10,	0.004,	67.9,	387),
('15000/25/23',	0,	2000,	0,	6000,	6000,	24000,	5.4,	3.7,	0.0,	'13/07/23',	57,	46,	45,	30,	15,	0.00185,	60.6,	388),																			 																																							
('15000/26/23',	0,	2500,	0,	7500,	7500,	30000,	6.3,	4.8,	0.0,	'14/07/23',	64.39,	49,	40,	29,	11,	0.00192,	69.79,	334),																				
('Old Lot-02',	500,	0,	0,	1500,	1500,	6000,	0.7,	0.50,	0.0,	'05/03/23',	60.64,	36,	39,	26,	13,	0.001,	64.14,	332),	
('Old Lot-03',	1500,	0,	0,	4500,	4500,	18000,	1.6,	1.3,	0.0,	'05/03/23',	60.2,	78,	40,	27,	13,	0.000866667,	63.3,	391),
('Old Lot-04',	2000,	0,	0,	6000,	6000,	24000,	1.8,	1.4,	0.0,	'05/03/23',	49.7,	49,	49,	35,	14,	0.0007,	53.8,	342),
('MLE 67/23 B1',	0,	0,	20000,	60000,	60000,	240000,	98.5,	92.0,	0.6,	'23/11/23',	63.65,	67,	30,	23,	7,	0.0046,	67.55,	331),
('MLE 68/23 B1',	0,	0,	20000,	60000,	60000,	240000,	96.4,	92.2,	0.5,	'26/11/23',	61.05,	157,	40,	26,	14,	0.00461,	65.15,	531),	
('15000/27 B1&B2&B3',	0,	5000,	0,	15000,	15000,	60000,	12,	10.7,	0.1,	'26/11/23',	61.1,	60,	45,	31,	14,	0.00214,	64.7,	372),																			
('MLE 69/23 B1',	0,	10000,	0,	30000,	30000,	120000,	22.0,	21.3,	0.1,	'28/11/23',	58.76,	72,	45,	29,	16,	0.00213,	62.36,	377),																		
('15000/28 B1&B2&B3',	0,	4000,	0,	12000,	12000,	48000,	13.6,	9.3,	0,	'30/11/23',	60.3,	59,	46,	34,	12,	0.002325,	63.8,	312),																				
('MLE 70/23 B1',	20000,	0,	0,	60000,	60000,	240000,	32.0,	30.0,	0.0,	'03/12/23',	63.33,	126,	30,	14,	16,	0.0015,	66.63,	563),																			
('MLE 71/23 B1', 	0,	5000,	0,	15000,	15000,	60000,	15.5,	11.4,	0.1,	'05/12/23',	58.73,	110,	24,	20,	4,	0.00228,	61.13,	478),																			
('MLE 41/23 B1 (REDRY)',	10000,	0,	0,	30000,	30000,	120000,	15,	13,	0.1,	'07/12/23',	61.68,	108,	16,	16,	0,	0.00133,	63.68,	245),																				
('MLE 43/23 B1 (REDRY)',	10000,	0,	0,	30000,	30000,	120000,	15.7,	13.3,	0.1,	'07/12/23',	60.44,	90,	14,	14,	0,	0.00133,	62.44,	234),																				
('MLE 73/23 B1',	0,	0,	10000,	30000,	30000,	120000,	43.4,	41.5,	0.1,	'12/12/23',	63.8,	84,	40,	29,	11,	0.00415,	66.9,	356),																				
('MLE 72/23 B1',	0,	0,	10000,	30000,	30000,	120000,	44.0,	42.0,	0.3,	'12/12/23',	58.26,	92,	38,	27,	11,	0.0042,	61.76,	360),																				
('MLE 74/23 B1',	0,	0,	10000,	30000,	30000,	120000,	42.0,	38.0,	0.0,	'14/12/23',	61,	70,	46,	28,	18,	0.0038,	64,	371);																																																																																																	)																		;

SELECT *
FROM LuteinesterProduction
ORDER BY  TotalCarotenoids;

#This proves that the MARIGOLD RM Taken from TAMIL NADU usually gives HIGHEST TOTAL PRODUCTION

SELECT LotNumber, MarigoldFlowerWeightUttarakhand, MarigoldFlowerWeightKarnataka, MarigoldFlowerWeightTamilNadu, TotalLuteinesterProductionKG
FROM LuteinesterProduction
ORDER BY TotalLuteinesterProductionKG DESC;

#This proves that the MARIGOLD RM Taken from TAMIL NADU gives BEST CONVERSION (YIELD)

SELECT LotNumber, MarigoldFlowerWeightUttarakhand, MarigoldFlowerWeightKarnataka, MarigoldFlowerWeightTamilNadu, Yield
FROM LuteinesterProduction
ORDER BY Yield DESC;

#This shows the LOT NUMBERS with MAXIMUM CONVERSION from each STATE

WITH StateYields AS (
  SELECT
    LotNumber,
    CASE
      WHEN MarigoldFlowerWeightUttarakhand >= MarigoldFlowerWeightKarnataka AND MarigoldFlowerWeightUttarakhand >= MarigoldFlowerWeightTamilNadu THEN 'Uttarakhand'
      WHEN MarigoldFlowerWeightKarnataka >= MarigoldFlowerWeightUttarakhand AND MarigoldFlowerWeightKarnataka >= MarigoldFlowerWeightTamilNadu THEN 'Karnataka'
      ELSE 'Tamil Nadu'
    END AS State,
    Yield
  FROM LuteinesterProduction
  WHERE MarigoldFlowerWeightUttarakhand > 0 OR MarigoldFlowerWeightKarnataka > 0 OR MarigoldFlowerWeightTamilNadu > 0
),
MaxStateYields AS (
  SELECT State, MAX(Yield) AS MaxYield
  FROM StateYields
  GROUP BY State
)
SELECT sy.State, sy.LotNumber, sy.Yield
FROM StateYields AS sy
JOIN MaxStateYields AS my ON sy.State = my.State AND sy.Yield = my.MaxYield
ORDER BY sy.State;

#Data regarding all works done WITHIN FIRST 2 QUARTERS of 2023

SELECT *
FROM LuteinesterProduction
WHERE DateOfWork >= '2023-01-01' AND DateOfWork <= '2023-06-30'
ORDER BY DateOfWork;

#ALL LOT NUMBERS Where TOTAL CAROTENOID VALUE is ABOVE 60 And TOTAL RESIDUAL SOLVENT VALUE is BELOW 60

SELECT LotNumber, MarigoldFlowerWeightUttarakhand, MarigoldFlowerWeightKarnataka, MarigoldFlowerWeightTamilNadu, TotalCarotenoids, TotalResidualSolventPPM, Yield
FROM LuteinesterProduction
WHERE TotalCarotenoids > 60 AND TotalResidualSolventPPM < 60;

#Data Regarding LOT NUMBERS where TOTAL CAROTENOID VALUE is AMONG TOP 5 And TOTAL RESIDUAL SOLVENT VALUE is in LEAST 5

WITH TopCarotenoids AS (
    SELECT LotNumber, TotalCarotenoids
    FROM (
        SELECT LotNumber, TotalCarotenoids, RANK() OVER (ORDER BY TotalCarotenoids DESC) AS CarotenoidRank
        FROM LuteinesterProduction
    ) AS RankedCarotenoids
    WHERE CarotenoidRank <= 5
),
LowestSolvents AS (
    SELECT LotNumber, TotalResidualSolventPPM
    FROM (
        SELECT LotNumber, TotalResidualSolventPPM, RANK() OVER (ORDER BY TotalResidualSolventPPM ASC) AS SolventRank
        FROM LuteinesterProduction
    ) AS RankedSolvents
    WHERE SolventRank <= 5
)
SELECT 
    tc.LotNumber, 
    ls.TotalResidualSolventPPM AS ResidualSolvent, 
    tc.TotalCarotenoids, 
    lp.MarigoldFlowerWeightUttarakhand, 
    lp.MarigoldFlowerWeightKarnataka, 
    lp.MarigoldFlowerWeightTamilNadu
FROM TopCarotenoids AS tc
JOIN LowestSolvents AS ls ON tc.LotNumber = ls.LotNumber
JOIN LuteinesterProduction AS lp ON tc.LotNumber = lp.LotNumber
ORDER BY tc.TotalCarotenoids DESC, ls.TotalResidualSolventPPM ASC;

#Data Regarding the TOP 5 TOTAL CAROTENOIDS Values & LEAST 5 RESIDUAL SOLVENT VALUES

WITH CarotenoidRanks AS (
    SELECT LotNumber, TotalCarotenoids, RANK() OVER (ORDER BY TotalCarotenoids DESC) AS CarotenoidRank
    FROM LuteinesterProduction
),
SolventRanks AS (
    SELECT LotNumber, TotalResidualSolventPPM, RANK() OVER (ORDER BY TotalResidualSolventPPM ASC) AS SolventRank
    FROM LuteinesterProduction
),
TopCarotenoids AS (
    SELECT LotNumber FROM CarotenoidRanks WHERE CarotenoidRank <= 5
),
LowSolvents AS (
    SELECT LotNumber FROM SolventRanks WHERE SolventRank <= 5
),
EligibleLots AS (
    SELECT tc.LotNumber
    FROM TopCarotenoids tc
    INNER JOIN LowSolvents ls ON tc.LotNumber = ls.LotNumber
)
SELECT lp.LotNumber, 
       lp.TotalResidualSolventPPM AS ResidualSolvent, 
       lp.TotalCarotenoids, 
       lp.MarigoldFlowerWeightUttarakhand, 
       lp.MarigoldFlowerWeightKarnataka, 
       lp.MarigoldFlowerWeightTamilNadu
FROM LuteinesterProduction lp
INNER JOIN EligibleLots el ON lp.LotNumber = el.LotNumber
ORDER BY lp.TotalCarotenoids DESC, lp.TotalResidualSolventPPM ASC;

#Data of TOP 5 TIME TAKEN

SELECT 
    LotNumber, 
    TotalTimeTakenHours, 
    MarigoldFlowerWeightUttarakhand, 
    MarigoldFlowerWeightKarnataka, 
    MarigoldFlowerWeightTamilNadu, 
    TotalResidualSolventPPM, 
    TotalCarotenoids,
    YIELD
FROM LuteinesterProduction
ORDER BY TotalTimeTakenHours DESC
LIMIT 5;

#Data of LEAST 5 TIME TAKEN

SELECT LotNumber, 
    TotalTimeTakenHours, 
    MarigoldFlowerWeightUttarakhand, 
    MarigoldFlowerWeightKarnataka, 
    MarigoldFlowerWeightTamilNadu, 
    TotalResidualSolventPPM, 
    TotalCarotenoids,
    YIELD
FROM LuteinesterProduction
ORDER BY TotalTimeTakenHours ASC
LIMIT 5;

#Comparison between TOTAL CAROTENOIDS, & TOTAL CAROTENOIDS in WET CAKE AND RESIDUAL SOVENTS, & RESIDUAL SOVENTS in WET CAKE

SELECT 
    LotNumber, 
    WetCakeTC, 
    WetCakeRSPPM AS WetCakeRS, 
    TotalCarotenoids AS TC, 
    TotalResidualSolventPPM AS RS,
    (-(TotalCarotenoids - WetCakeTC)) AS TotalCarotenoidDifference,
    (-(TotalResidualSolventPPM - WetCakeRSPPM)) AS TotalResidualSolventDifference
FROM LuteinesterProduction;
