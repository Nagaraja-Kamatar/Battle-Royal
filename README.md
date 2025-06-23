# 3D Battle Game

This is a web-based 3D battle game featuring animated avatars, crowd effects, and interactive gameplay. Built with React, Three.js, and Express.

## Features
- Two-player local battle with animated 3D avatars
- Realistic crowd and arena environment
- Sound effects and particle effects
- Customizable player models and assets
- Hot Module Reloading for rapid development

## Gameplay
- Two players compete in a dynamic arena.
- Each player controls a 3D avatar and can move, attack, dodge, and block.
- The goal is to knock out the opponent and score points.
- The crowd reacts to gameplay events, adding atmosphere.

## Controls
- **Player 1:**
  - Move: Arrow keys or WASD
  - Attack: Spacebar
  - Dodge: Shift
- **Player 2:**
  - Move: IJKL or Numpad
  - Attack: Enter
  - Dodge: Right Shift

## Getting Started

### Prerequisites
- Node.js (v18 or higher recommended)
- npm (comes with Node.js)

### Installation
1. Clone the repository:
   ```sh
   git clone <your-repo-url>
   cd battle
   ```
2. Install dependencies:
   ```sh
   npm install
   ```

### Running the Game (Development)
Start the development server:
```sh
npm run dev
```
The game will be available at [http://localhost:5000](http://localhost:5000).

### Building for Production
To build the client and server for production:
```sh
npm run build
```
To start the production server:
```sh
npm start
```

## Project Structure
- `client/` - React frontend and 3D assets
- `server/` - Express backend
- `shared/` - Shared code (e.g., schema)
- `client/public/models/` - 3D models (GLB/GLTF)
- `client/public/sounds/` - Sound effects
- `client/public/textures/` - Textures

## Asset Management
- **3D Models:** Place `.glb` or `.gltf` files in `client/public/models/`.
- **Sounds:** Place `.mp3` or `.wav` files in `client/public/sounds/`.
- **Textures:** Place image files in `client/public/textures/`.
- **Animations:** Ensure your 3D models are rigged and include required animations (idle, walk, attack, knockout).

## Customizing Player Avatars
- To use a custom avatar, export your model as `.glb` or `.gltf` and place it in `client/public/models/`.
- Update the model path in `client/src/components/game/Player.tsx`.
- For best results, use models with humanoid rigs and animation clips named appropriately (e.g., `Idle`, `Walk`, `Attack`, `Knockout`).
- You can use Blender or similar tools to rig and animate your models.

## Development Tips
- The project uses Vite for fast development and hot module reloading.
- Most game logic is in `client/src/components/game/`.
- UI components are in `client/src/components/ui/`.
- State management uses Zustand (`client/src/lib/stores/`).
- For 3D and animation, Three.js and @react-three/fiber are used.
- To debug 3D issues, use the browser console and Three.js inspector tools.

## Troubleshooting
- **Models not visible:**
  - Check the browser console for loading errors.
  - Ensure the model file is in the correct directory and the path is correct.
  - Verify the model is not too small or outside the camera view.
- **Animation issues:**
  - Make sure your model is rigged and has the required animation clips.
  - Use Blender to inspect and export animations.
- **Sound not playing:**
  - Check that sound files are present and paths are correct.
- **Other issues:**
  - Restart the dev server after adding new assets.
  - Clear browser cache if assets are not updating.

## Adding New Features or Assets
- To add new 3D models, place them in `client/public/models/` and update the relevant code.
- To add new sound effects, place them in `client/public/sounds/` and reference them in the sound manager.
- To add new UI elements, create components in `client/src/components/ui/`.
- For new gameplay features, modify or add components in `client/src/components/game/`.

## Contribution Guidelines
1. Fork the repository and create a new branch for your feature or fix.
2. Write clear, concise commit messages.
3. Test your changes locally before submitting a pull request.
4. Describe your changes and reference any related issues in your PR.
5. Follow the existing code style and structure.

## License
MIT 
