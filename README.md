# 3x3 Tile Puzzle Game

A dynamic 3x3 tile puzzle game built with React and Express that allows players to upload and solve custom image puzzles through intuitive drag-and-drop or click-to-swap interactions.

## Features

- **Custom Image Upload**: Upload any JPEG or PNG image to create your puzzle
- **Dual Interaction Methods**: 
  - Drag and drop tiles to swap positions
  - Click-to-select tiles for touch-friendly devices
- **Real-time Progress Tracking**: Visual progress bar and correct tile counter
- **Game Statistics**: Move counter and timer with best score tracking
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Success Celebration**: Animated completion modal with game statistics

## Technology Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Shadcn/ui
- **Backend**: Express.js, Node.js
- **Image Processing**: Sharp library for tile generation
- **State Management**: React Query for API state management
- **File Upload**: Multer for handling image uploads

## Getting Started

### Prerequisites

- Node.js 20 or higher
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ashoksriram92/3x3-puzzle-game.git
cd 3x3-puzzle-game
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5000`

## How to Play

1. **Upload an Image**: Click or drag an image file (JPEG/PNG) into the upload area
2. **Scramble the Puzzle**: Click "Scramble Puzzle" to mix up the tiles
3. **Solve the Puzzle**: 
   - **Drag & Drop**: Drag tiles to swap their positions
   - **Click to Swap**: Click one tile (it highlights blue), then click another to swap
4. **Complete the Puzzle**: Arrange all tiles in the correct order with minimum moves!

## Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── lib/            # Utility functions and API client
│   │   └── hooks/          # Custom React hooks
├── server/                 # Express backend
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   ├── storage.ts         # In-memory storage interface
│   └── vite.ts            # Vite development server setup
├── shared/                 # Shared types and schemas
│   └── schema.ts          # Database schemas and types
└── uploads/               # Generated puzzle images (git-ignored)
```

## API Endpoints

- `POST /api/upload-image` - Upload and process image into puzzle tiles
- `GET /api/uploads/:filename` - Serve uploaded images and tiles
- `POST /api/puzzle-games` - Save completed puzzle game statistics
- `GET /api/puzzle-games` - Retrieve all puzzle game records

## Development

The project uses:
- **Vite** for fast development and building
- **TypeScript** for type safety
- **Tailwind CSS** for styling
- **ESLint** and **Prettier** for code quality

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Built with modern web technologies for optimal performance
- Responsive design ensures great experience across all devices
- Image processing powered by Sharp for high-quality tile generation