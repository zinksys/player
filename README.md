# Bloom Music Player 🌸

A minimalist web music player with a blooming flower progress visualization. Built with vanilla HTML, CSS, and JavaScript.

## Features

- **Blooming Flower Progress**: Watch a flower bloom as your song plays
- **Minimalist Design**: Soft, earthy color palette with gentle animations
- **Mock Playlist**: Four demo tracks with artist names
- **Playback Controls**: Play/pause, next track, and loop functionality
- **Responsive Design**: Works beautifully on mobile and desktop
- **Session Persistence**: Stay logged in during your session

## Design Philosophy

Inspired by calm, floral, vintage aesthetics with:
- Warm beige/sand tones
- Muted accent colors (dusty pink, sage green, soft teal)
- Soft serif typography (Cormorant, Playfair Display)
- Gentle, intentional animations
- No harsh contrasts or neon colors

## Deployment on Vercel

### Quick Deploy

1. **Install Vercel CLI** (if you haven't already):
   ```bash
   npm i -g vercel
   ```

2. **Deploy**:
   ```bash
   vercel
   ```

3. Follow the prompts to link to your Vercel account

### Deploy via Git

1. Push this repository to GitHub/GitLab/Bitbucket
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your repository
5. Vercel will auto-detect the configuration and deploy

## File Structure

```
bloom-music-player/
├── index.html          # Main application file
├── vercel.json         # Vercel configuration
└── README.md           # This file
```

## How It Works

### Flower Progress Visualization

The flower consists of 8 petals that animate from a closed bud to full bloom:
- Each petal starts rotated and scaled down (closed state)
- As the song plays, petals gradually rotate to 0° and scale to 100%
- Progress is calculated: `currentTime / songDuration`
- Each petal has a slight delay for a staggered bloom effect

### Mock Audio

Currently uses a JavaScript timer to simulate playback. To integrate real audio:
1. Add an `<audio>` element
2. Replace the animation loop with actual audio events
3. Sync flower bloom to `audio.currentTime`

## Customization

### Change Colors

Edit the CSS variables in `index.html`:

```css
:root {
    --bg-sand: #E8DCC8;
    --card-beige: #D4C4AC;
    --text-dark: #3D3128;
    --muted-yellow: #E8D09A;
    --dusty-pink: #D4A5A5;
    --sage-green: #A8B5A0;
    --soft-teal: #9FB8B3;
    --button-outline: #8B7355;
}
```

### Update Playlist

Modify the `playlist` array in the JavaScript:

```javascript
const playlist = [
    { title: 'Your Song', artist: 'Artist Name', duration: 180 },
    // Add more songs...
];
```

## Browser Support

- Chrome/Edge: ✅
- Firefox: ✅
- Safari: ✅
- Mobile browsers: ✅

## License

Free to use and modify for personal or commercial projects.

## Credits

Created with attention to minimalist design principles and gentle user experience.
