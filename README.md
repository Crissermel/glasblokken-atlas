# GlassBlock Atlas

A community-driven web application that allows users to document and map the presence of architectural glass blocks in the real world. By leveraging geolocation and user-generated content, the app creates a visual archive of glass blocks from around the world.

## Features

- **Interactive Map**: Explore glass block installations on an interactive map powered by OpenStreetMap
- **Add New Pins**: Document glass blocks with photos, descriptions, and detailed metadata
- **Geolocation**: Automatically get your current location or manually enter coordinates
- **Rich Metadata**: Include architectural style, building type, unique features, and tags
- **Community-Driven**: All content is saved locally and shared within the community
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

- **Frontend**: React 18 with TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Mapping**: React Leaflet with OpenStreetMap
- **Icons**: Lucide React
- **Routing**: React Router DOM

## Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd glassblock-atlas
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:3000`

### Building for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Usage

### Adding a Glass Block

1. Click the "Add Glass Block" button in the header
2. Fill in the required information:
   - **Title**: A descriptive name for the glass block installation
   - **Description**: Detailed description of the glass block
   - **Location**: Use "Use my current location" or enter coordinates manually
   - **Photo**: Upload a photo of the glass block
3. Optionally add:
   - **Architectural Style**: e.g., Art Deco, Modern, Brutalist
   - **Building Type**: e.g., Office building, Church, School
   - **Unique Features**: Any notable characteristics
   - **Tags**: Keywords to help categorize the installation
4. Click "Add Glass Block" to save

### Exploring the Map

- **View Pins**: All documented glass blocks appear as pins on the map
- **Click Pins**: Click any pin to view detailed information
- **Map Navigation**: Zoom, pan, and explore different areas
- **Location Services**: The map automatically centers on your location when available

### Managing Content

- **View Details**: Click any pin to see full information including photos
- **Delete Pins**: Use the trash icon in pin details to remove entries
- **Local Storage**: All data is saved locally in your browser

## Data Structure

Each glass block pin contains:

```typescript
interface GlassBlockPin {
  id: string
  title: string
  description: string
  location: {
    lat: number
    lng: number
  }
  imageUrl: string
  architecturalStyle?: string
  buildingType?: string
  uniqueFeatures?: string
  createdAt: string
  tags?: string[]
}
```

## Contributing

This is a community-driven project! Here are some ways you can contribute:

1. **Add Glass Blocks**: Document glass block installations in your area
2. **Improve Documentation**: Help improve this README or add code comments
3. **Feature Requests**: Suggest new features or improvements
4. **Bug Reports**: Report any issues you encounter

## Privacy

- All data is stored locally in your browser's localStorage
- No personal information is collected or transmitted
- Photos are converted to data URLs and stored locally
- Location data is only used when you explicitly grant permission

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **OpenStreetMap**: For providing the map tiles and data
- **Leaflet**: For the interactive mapping library
- **React Community**: For the excellent ecosystem of tools and libraries
- **Glass Block Enthusiasts**: For inspiring this project

---

**Happy Glass Block Hunting! 🏢✨** 