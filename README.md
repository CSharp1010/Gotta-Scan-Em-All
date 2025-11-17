**🃏 Gotta Scan 'Em All — Pokémon Card Digital Vault**

A SwiftUI iOS app for scanning, recognizing, and managing Pokémon cards in a digital vault.
Powered by real-time camera recognition, Vision, and the Pokémon TCG API.

**📑 Table of Contents**
📱 App Structure
🎨 Theme Management
🧩 Card Information
⚙️ Technical Architecture
📸 Camera & Recognition
🧠 Architecture Overview
🔗 Pokémon TCG API Integration
🧪 Testing Recommendations
🚀 Getting Started
🧩 Sample Data
🔮 Future Enhancements
💡 Design Philosophy
🤝 Contributing
👥 Team
🪪 License

**🎯 Core Functionality**

Card Scanning using live camera

Digital Vault storage

Manual Entry option

Advanced search, filter, and categorization tools

**📚 Collection Tool**

Search cards by name/set/type

Collection statistics and analytics

Import/Export collection backups

**📱 App Structure**

Tab	Description

Scanner	Camera interface for scanning cards

Collection	Grid of collected cards

Statistics	Collection analysis

Settings	App preferences and backup tools

**🎨 Theme Management**

The app supports System, Light, and Dark appearance modes with persistent user preferences.

**🧠 Theme System Overview**

Feature	Description

Theme Options	System, Light, Dark

Persistence	Saved using UserDefaults

SwiftUI Integration	Applies ColorScheme globally

UI Support	Picker in Settings tab

**🧩 Card Information**

Each card includes:

Name, set, number, rarity

HP, types, weaknesses, attacks

Market values from TCGPlayer

Artist and date added

**⚙️ Technical Architecture**

📁 Data Models

PokemonCard

CardCollection

CardRarity

PokemonType

**🧰 Technologies Used**

SwiftUI

UserDefaults

AVFoundation

Vision Framework

Pokémon TCG API v2

**📸 Camera & Recognition**
Camera & Permissions - 
Full AVFoundation camera session - 
Live preview with scanning guides - 
Permission error handling - 
Camera switching - 
Image Processing - 
OCR using Vision - 
Card rectangle detection - 
Auto-cropping & enhancement - 
Perspective correction - 
Photo library integration - 
Recognition Intelligence - 
OCR text → API search - 
Name / set matching - 
Confidence scoring - 
Manual correction workflow - 
User Flow - 
Open Scanner - 
Position Card - 
Capture - 
Auto-recognize - 
Review - 
Edit - 
Save to collection 

**🧠 Architecture Overview**
Managers - 
CameraManager.swift - 
ImageProcessor.swift - 
Services - 
CardRecognitionService.swift - 
Views - 
CameraView.swift - 
CameraPreviewView.swift - 
ImagePicker.swift - 
ManualEditView.swift - 
🔗 Pokémon TCG API Integration - 
Base URL: https://api.pokemontcg.io/v2 - 
Client: PokemonTCGAPIService - 
Endpoints - 
/cards – Search cards by query - 
/cards/{id} – Fetch specific card details - 
/sets – List all card sets - 
Recognition Flow - 
OCR extracts text from the card - 
Search request sent to Pokémon TCG API -
API results converted to app’s internal models -
Pricing read from tcgplayer.prices

**🧪 Testing Recommendations**

Test on real devices

Try different lighting conditions

Import images from photo library

Validate API search accuracy

Test camera permission denial flows

**🚀 Getting Started**

Open the Xcode project

Select a physical device

Build and run

Load sample data in Settings

Start scanning cards

**🧩 Sample Data**

The app includes iconic base-set cards such as:
Pikachu
Charizard
Blastoise
Venusaur
Mewtwo
And more

**🔮 Future Enhancements**

Phase 2 — Recognition & API

Barcode scanning

Machine learning card model

iCloud sync support

Phase 3 — Advanced Features

Batch scanning

Condition/grade detection

Deck builder

Social sharing and trading

Tournament tracking

**💡 Design Philosophy**

Local-first storage

Fully SwiftUI-native

Modular structure

Built for extensibility

**🤝 Contributing**

Created as a SwiftUI learning and collaboration project.

Open for forks, customizations, and extensions.

**👥 Team**

Gotta Scan ’Em All Development Team

Jersain Hermosillo — iOS Developer / Project Lead

Bradley Everett - UI Developer / PowerPoint Developer

Casey Sharp - UI Developer / ReadMe Developer

Anthonie Quintela - UI Developer

**🪪 License**
This project is for educational purposes only.
Pokémon and related trademarks belong to Nintendo, Game Freak, and Creatures Inc.
