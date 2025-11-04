# Gotta-Scan-Em-All
**Mobile App for Collecting /Scanning/ Tracking your Pokemon Cards **

🃏 Gotta Scan 'Em All — Pokémon Card Digital Vault
A SwiftUI iOS app for scanning, collecting, and managing Pokémon cards in a digital vault.
Built with modern iOS frameworks and real-time camera recognition powered by Vision and the Pokémon TCG API.
🎯 Features
Core Functionality
Card Scanning: Use your device’s camera to scan and identify Pokémon cards.
Digital Vault: Store and organize your cards in a beautiful, searchable interface.
Manual Entry: Add cards manually when scanning isn’t available.
Collection Management: Search, filter, and categorize your Pokémon cards.
Collection Tools
Search & Filter: Find cards by name, set, rarity, or type.
Statistics: Track collection value, rarity distribution, and progress.
Export/Import: Backup and restore your digital vault data.
📱 App Structure
Tab	Description
Scanner	Camera interface for scanning cards.
Collection	Grid view of collected cards with search and filters.
Statistics	Analytics and collection insights.
Settings	App configuration, backups, and data management.
🧩 Card Information
Each card contains comprehensive details:
Basic Info: Name, set, number, rarity.
Game Stats: HP, types, attacks, weaknesses, resistances.
Market Data: TCGPlayer prices and market value.
Meta Info: Artist, date added, and collection status.
⚙️ Technical Architecture
Data Models
PokemonCard: Core card data structure.
CardCollection: Observable collection manager.
CardRarity: Enum for card rarity levels.
PokemonType: Enum for Pokémon types with color and icon mapping.
Technologies Used
SwiftUI — Modern declarative UI framework.
UserDefaults — Local data persistence.
AVFoundation — Camera integration.
Vision Framework — Image and text recognition.
Pokémon TCG API (v2) — Real card data and pricing.
📸 Real Camera Implementation — Complete! 🎉
Implemented Features
Camera & Permissions
Full AVFoundation integration for real-time camera sessions.
Automatic permission handling and user-friendly error recovery.
Live preview with custom overlay and scanning guides.
Front/back camera switching support.
Image Processing & Recognition
Vision Framework OCR for card text recognition.
Rectangle detection for auto-cropping and perspective correction.
Image enhancement (contrast, brightness, saturation).
Photo Library integration for selecting existing images.
Smart Card Recognition
Text extraction → name & set recognition via pattern matching.
Confidence scoring for recognition accuracy.
Fallback handling and manual edit override when uncertain.
User Experience
Professional UI with scanning guides and live feedback.
Real-time progress and error indicators.
Smooth transition from scanning → recognition → editing.
🧠 Architecture Overview
Managers/
├── CameraManager.swift          # AVFoundation camera management
└── ImageProcessor.swift         # Vision-based image processing

Services/
└── CardRecognitionService.swift # OCR and card identification

Views/
├── CameraView.swift             # Main camera interface
├── CameraPreviewView.swift      # Live preview layer
├── ImagePicker.swift            # Photo library integration
└── ManualEditView.swift         # Manual card detail editing
🔗 Pokémon TCG API Integration
Client: PokemonTCGAPIService
Base URL: https://api.pokemontcg.io/v2
Endpoints
GET /cards — Search cards (e.g., q=name:*pikachu* with pagination).
GET /cards/{id} — Fetch a specific card by ID.
GET /sets — Retrieve list of card sets.
Recognition Flow
The CardRecognitionService uses the PokémonTCGAPIService via the PokemonCardSearching protocol to:
Search the API using text detected by the camera (OCR).
Convert PokemonTCGCard responses into the app’s internal PokemonCard model.
Extract pricing data from the tcgplayer.prices fields.
🧪 Testing Recommendations
Test on real devices (camera required).
Try different cards for recognition accuracy.
Deny/allow camera permissions to test error handling.
Test photo library imports and manual entry edits.
🚀 Getting Started
Open Project: Gotta Scan 'Em All.xcodeproj in Xcode.
Build & Run: Choose your target device and run.
Load Sample Data: Go to Settings → Load Sample Data.
Start Collecting: Use the Scanner tab to scan and save cards.
🧩 Sample Data
Includes classic Base Set examples:
Pikachu (Common)
Charizard (Rare Holo)
Blastoise (Rare Holo)
Venusaur (Rare Holo)
Mewtwo (Rare Holo)
And more!
🔮 Future Enhancements
Phase 2 – Recognition & API
Pokémon TCG API lookup for richer data.
Barcode scanning and price tracking.
Machine learning for improved recognition accuracy.
iCloud sync for cross-device collection.
Phase 3 – Advanced Features
Batch scanning for multiple cards.
Condition grading and market tracking.
Deck building and tournament tracking.
Social sharing and collection trading.
💡 Design Philosophy
Local-First: Offline-first design using UserDefaults.
SwiftUI-Native: 100% SwiftUI interface for modern UX.
Modular Architecture: Models, Views, and Services are cleanly separated.
Extensible: Easy to add new card types, sets, and recognition logic.
🤝 Contributing
This project was built for learning and experimentation with SwiftUI, Vision, and camera frameworks.
Feel free to fork, learn from, or extend this app for your own Pokémon collection projects!
🪪 License
This project is for educational purposes only.
Pokémon and all related properties are trademarks of Nintendo, Game Freak, and Creatures Inc.

