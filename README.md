# F1 Race Winner Prediction Model

## Project Overview
Machine learning model to predict Formula 1 race winners using historical race data and driver/team performance metrics.

## Current Model Architecture (9/13)
- **Algorithm**: Random Forest Classifier
- **Training Data**: Hungarian Grand Prix & Dutch Grand Prix (2025)
- **Prediction Target**: Italian Grand Prix 2025 race winner
- **Validation Approach**: Known race results for model performance evaluation

## Dataset Features

### Driver Performance Metrics
- **Starting Position**: Grid position from qualifying (`GridPosition`)
- **Finishing Position**: Final race classification (`Position`)
- **Classified Position**: Official race standing accounting for DNFs (`ClassifiedPosition`)
- **Race Points**: Championship points earned per race (`Points`)
- **DNF Status**: Did Not Finish indicator for reliability analysis

### Championship Standings
- **Driver Championship Points**: Cumulative points after each race
- **Driver Championship Position**: Current standings rank
- **Constructor Championship Points**: Team's total accumulated points
- **Constructor Championship Position**: Team's current standings rank

### Derived Features
- **Position Change**: Grid position vs finishing position delta
- **Team Performance**: Constructor championship standing as performance proxy

## 2025 F1 Season - Teams & Drivers

| Constructor | Driver 1 | Driver 2 |
|-------------|----------|----------|
| **Red Bull Racing** | Max Verstappen | Yuki Tsunoda |
| **Ferrari** | Charles Leclerc | Lewis Hamilton |
| **McLaren** | Lando Norris | Oscar Piastri |
| **Mercedes** | George Russell | Kimi Antonelli |
| **Aston Martin** | Fernando Alonso | Lance Stroll |
| **Alpine** | Pierre Gasly | Franco Colapinto |
| **Haas** | Oliver Bearman | Esteban Ocon  |
| **Kick Sauber** | Nico Hulkenberg | Gabriel Bortoleto |
| **Racing Bulls** | Isack Hadjar | Liam Lawson |
| **Williams** | Alexander Albon | Carlos Sainz |

## Implementation

### Data Sources
- **FastF1**: Official F1 telemetry and race results API
- **Race Sessions**: Hungarian GP, Dutch GP (training); Italian GP (prediction target)

### Key Dependencies
```python
fastf1>=3.0.0
pandas>=1.3.0
scikit-learn>=1.0.0
numpy>=1.20.0
```

## Expected Outcomes
- Race winner prediction accuracy comparison against baseline (random chance: 5%)
- Feature importance analysis to identify key predictive factors
- Model performance metrics on known race results for validation
