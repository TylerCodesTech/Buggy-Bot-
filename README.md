# 🤖 Buggy Bot - Discord Music & Utility Bot

Buggy Bot is a versatile Discord bot that brings music, moderation, and fun to your server - and yes, despite the name, it actually works great! Built with Discord.js, it's your all-in-one solution for playing music, managing your server, and entertaining your community.

[![Discord.js](https://img.shields.io/badge/discord.js-v14-blue.svg)](https://discord.js.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Node](https://img.shields.io/badge/node-%3E%3D%2018.0.0-green.svg)](https://nodejs.org)

## 🎮 What Can Buggy Bot Do?

### 🎵 Music Features
- Play your favorite tunes from YouTube
- Search and pick songs without leaving Discord
- Manage a queue of songs
- Skip, stop, and remove tracks easily

### 🛠️ Server Management
- Clear messages in bulk
- Channel management tools
- Server statistics

### 🎲 Fun Stuff
- Get dad jokes that are so bad they're good
- Roll dice for your D&D sessions
- Flip a coin when you can't make decisions

## 🚀 Getting Started

### Prerequisites
- Node.js 18.0.0 or newer
- npm
- A Discord bot token (get it from Discord Developer Portal)
- FFmpeg installed on your system

### Quick Setup

1. **Clone Buggy Bot**
```bash
git clone https://github.com/yourusername/buggy-bot.git
cd buggy-bot
```

2. **Install What It Needs**
```bash
npm install
```

3. **Set Up Your Bot's Secret Stuff**
Create a `.env` file:
```env
BOT_TOKEN=your_discord_bot_token
CLIENT_ID=your_client_id
GUILD_ID=your_guild_id
```

4. **Deploy Commands**
```bash
node scripts/deploy-commands.js
```

5. **Start Your Bot**
```bash
node src/Bot.js
```

## 📝 Commands

### Music Commands
| Command | What It Does | How to Use It |
|---------|-------------|--------|
| `/play` | Start the tunes | `/play never gonna give you up` |
| `/search` | Find a song | `/search lofi beats` |
| `/queue` | See what's playing next | `/queue` |
| `/skip` | Skip the current track | `/skip` |
| `/stop` | Stop the music | `/stop` |
| `/remove` | Remove a song from queue | `/remove 3` |

### Utility Commands
| Command | What It Does | How to Use It |
|---------|-------------|--------|
| `/help` | Show all commands | `/help` |
| `/clear` | Clean up messages | `/clear 10` |
| `/stats` | Show bot stats | `/stats` |
| `/nuke` | Reset a channel | `/nuke` |

## 🔧 Configuration

### Default Settings
Found in `src/config/settings.js`:
```javascript
{
    prefix: '/',
    leaveChannelDelay: 300000, // 5 minutes
    maxQueueSize: 100,
    defaultVolume: 50
}
```

### What Permissions Buggy Bot Needs
- Voice channel access (Connect & Speak)
- Message management for clear command
- Channel management for nuke command

## 🐳 Running with Docker

### Easy Mode (Docker Compose)
```bash
docker-compose up -d
```

### Manual Mode
```bash
docker build -t buggy-bot .
docker run -d --env-file .env buggy-bot
```

## 🔍 Troubleshooting

### Common Problems

1. **Bot Won't Join Voice**
   - Check if bot has server permissions
   - Make sure voice channel isn't full
   - Verify FFmpeg installation

2. **Music Not Playing**
   - Check if YouTube link is valid
   - Ensure bot has proper permissions
   - Look at console for error messages

3. **Commands Not Working**
   - Redeploy commands with deploy script
   - Check bot's role permissions
   - Make sure all intents are enabled in Developer Portal

## 👋 Need Help?

- Check out our [Issues](https://github.com/yourusername/buggy-bot/issues) page
- Create a new issue if you found a bug (ironic, we know)

## 📄 License

Buggy Bot is licensed under the MIT License - see [LICENSE](LICENSE) for details.

## 🙏 Credits

Built using these awesome tools:
- [Discord.js](https://discord.js.org/)
- [play-dl](https://github.com/play-dl/play-dl)
- [FFmpeg](https://ffmpeg.org/)
