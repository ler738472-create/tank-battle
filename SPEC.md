# Tank Battle - HTML5 Game Specification

## Project Overview
- **Project Name**: Tank Battle
- **Type**: 2D Canvas Game (Single HTML File)
- **Core Functionality**: Classic tank battle game with player tank, enemy tanks, bullets, explosions, and score system
- **Target Users**: Casual gamers

## Visual & Rendering Specification

### Scene Setup
- **Canvas**: Full viewport 2D canvas (800x600 logical, responsive scaling)
- **Background**: Dark military green terrain with grid pattern
- **Camera**: Fixed top-down 2D view

### Visual Style
- **Aesthetic**: Retro pixel-art inspired with modern glow effects
- **Color Palette**:
  - Player tank: Bright green (#00FF88)
  - Enemy tanks: Red/Orange (#FF4444)
  - Bullets: Yellow with glow (#FFFF00)
  - Background: Dark olive (#1a1a0a)
  - UI: White text with green accents

### Visual Effects
- Muzzle flash on firing
- Explosion particles on tank/bullet destruction
- Tank treads visual trail
- Screen shake on big explosions

## Game Mechanics

### Player Tank
- WASD movement (up/down/left/right)
- Mouse aim + Left click to fire
- Health: 3 hits
- Movement speed: 3px/frame
- Fire rate: 1 bullet per 300ms

### Enemy Tanks
- Spawn from top/sides of screen
- Random patrol movement
- Auto-fire when player in line of sight
- Health: 1 hit
- Speed: 1.5px/frame
- Spawn rate: Every 2 seconds, increasing over time

### Bullets
- Speed: 8px/frame
- Damage: 1 hit
- Destroyed on collision with tanks or walls

### Scoring
- Enemy tank destroyed: +100 points
- Wave clear bonus: +500 points
- High score tracked in localStorage

### Waves
- Wave 1: 5 enemies
- Each wave: +3 enemies
- Brief pause between waves

## Interaction Specification

### Controls
- **W/A/S/D**: Move tank
- **Mouse**: Aim turret
- **Left Click**: Fire
- **R**: Restart game (when game over)

### UI Elements
- Score display (top-left)
- Wave number (top-center)
- Health bar (top-right)
- Game Over screen with restart option

## Audio
- No audio (keeping it simple single HTML)

## Acceptance Criteria
1. Player can move and aim tank smoothly
2. Bullets fire and detect collisions correctly
3. Enemy tanks spawn and patrol
4. Score updates on enemy kill
5. Health decreases on player hit
6. Game over when health reaches 0
7. Restart works correctly
8. Game runs at 60fps without lag
