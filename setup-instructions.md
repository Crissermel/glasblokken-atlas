# Setup Instructions for GlassBlock Atlas

## Option 1: Install Node.js (Recommended)

### Windows
1. Download Node.js from: https://nodejs.org/
2. Choose the LTS (Long Term Support) version
3. Run the installer and follow the setup wizard
4. Restart your terminal/PowerShell
5. Verify installation:
   ```bash
   node --version
   npm --version
   ```

### macOS
1. Install using Homebrew (if you have it):
   ```bash
   brew install node
   ```
2. Or download from: https://nodejs.org/

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install nodejs npm
```

## Option 2: Use the Standalone HTML Version

If you prefer not to install Node.js, you can use the standalone HTML version:

1. Open `index-standalone.html` in your web browser
2. The application will work with basic functionality
3. Note: Some features may be limited compared to the full React version

## Running the Application

Once Node.js is installed:

1. Open terminal/PowerShell in the project directory
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
4. Open your browser to `http://localhost:3000`

## Troubleshooting

### "npm is not recognized"
- Make sure Node.js is properly installed
- Restart your terminal after installation
- Check if Node.js is in your system PATH

### "Permission denied" errors
- On Windows: Run PowerShell as Administrator
- On macOS/Linux: Use `sudo` if needed

### Port 3000 already in use
- The app will automatically try the next available port
- Or manually specify a different port in `vite.config.ts` 