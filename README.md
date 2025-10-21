# CS-FLARE

**Citizen Science: Fire Likelihood and Risk Evaluation**

A mobile application that empowers citizens to assess wildfire risk on their properties using machine learning and citizen science data.

## Overview

CS-FLARE analyzes wildfire risk at the community level by combining:
- Image analysis of flammable vegetation (trees, brush, grass, leaf litter)
- Ground moisture assessment
- Satellite data (temperature, precipitation, elevation)

The app provides users with a quantified wildfire risk rating and actionable recommendations to reduce fire hazards.

## Features

- 📸 **Image-based Risk Assessment**: Analyze photos in all four cardinal directions plus downward view
- 🤖 **AI-Powered Detection**: Uses YOLOv8 for vegetation segmentation and Google Teachable Machine for moisture classification
- 🛰️ **Satellite Data Integration**: Incorporates real-time environmental data for comprehensive risk evaluation
- 📱 **Cross-Platform**: Built with Flutter for iOS and Android
- 💡 **Actionable Insights**: Provides specific recommendations to minimize wildfire risk

## Technology Stack

- **Mobile Framework**: Flutter (Dart)
- **Image Segmentation**: YOLOv8
- **Moisture Classification**: Google Teachable Machine (TensorFlow Lite)
- **Satellite Data**: U-Net model with Google Earth Engine data
- **Data Source**: GLOBE Observer Land Cover Database

## Getting Started

### Prerequisites

- Flutter SDK (latest stable version)
- Dart
- Android Studio / Xcode (for mobile development)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/AmoghThodati2/cs-flare.git
cd cs-flare
```

2. Install dependencies:
```bash
flutter pub get
```

3. Run the app:
```bash
flutter run
```

## How It Works

1. **Capture Images**: Take photos in North, East, South, West directions, plus a downward view
2. **AI Analysis**: Models detect vegetation types and assess ground moisture
3. **Risk Calculation**: Algorithm combines image analysis with satellite data
4. **Get Results**: Receive a risk rating with recommendations for mitigation

## Models

- **YOLOv8 Segmentation Model**: Identifies trees, brush, grass, and leaf litter (mAP50: 0.439)
- **Grass Moisture Model**: Classifies ground as healthy, slightly dry, or very dry (94% accuracy)
- **U-Net Satellite Model**: Predicts fire risk using temperature, precipitation, and terrain data

## Data Sources

- GLOBE Observer Land Cover Database
- NASA Daymet V4 (weather/climate data)
- TerraClimate (precipitation)
- MODIS (fire mask labels)

## Research Team

**Student Researchers**: Leena Dudi, Sanaa Mulay, Anjali Singh, Ashvin Tiwari, Amogh Thodati, Vincent Villarreal, Zane Zacharia, Arnold Zhang, Charlotte Zhou

**Mentors**: Dr. Russanne Low, Cassie Soeffing, Peder Nelson, James Ervin, Nikita Agrawal

**Program**: NASA SEES ESE 2024, Working Group 5

## Future Goals

- Expand dataset for improved model accuracy
- Integrate with local fire departments and environmental agencies
- Enable community-wide data collection and analysis
- Develop tiered risk assessment combining all models

## Contributing

This project was developed as part of NASA's STEM Enhancement in Earth Sciences (SEES) program. For questions or collaboration opportunities, please open an issue.

## License

This project uses data from the GLOBE Program, which is freely available for research, publications, and commercial applications.

## Acknowledgments

- NASA SEES Virtual High School Internship Program
- GLOBE Observer community contributors
- Institute for Global Environmental Strategies
- Texas Space Grant Consortium

---

*Empowering communities to prevent wildfires, one assessment at a time.*