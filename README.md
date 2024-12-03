# LogSeq Trello Integration Plugin

A seamless integration between LogSeq and Trello that allows you to import Trello cards as LogSeq pages and keep them in sync.

## Features

### 🔄 Bi-directional Sync
- Import Trello cards as LogSeq pages
- Smart version control to prevent accidental overwrites
- Preserves your local edits when they're newer than Trello changes
- Intelligent duplicate handling on both LogSeq and Trello sides

### 📝 Content Management
- Clean, block-based formatting of card content
- Preserves Unicode characters (including Chinese)
- Imports both card descriptions and comments
- Each paragraph and comment in separate blocks for easy editing

### 🛠️ Commands
- `/Send Block to Trello`: Create a Trello card from current block
- `/Send Page to Trello`: Create a Trello card from current page
- `/Trello Get Lists`: Discover your Trello boards and lists
- `/Trello Pull Cards`: Import cards from a specified Trello list

## Installation

1. Open LogSeq
2. Go to Settings > Plugins
3. Search for "Trello Integration"
4. Click Install

## Configuration

1. Get your Trello Token:
   - Visit https://trello.com/1/authorize?expiration=never&name=LogSeq%20Integration&scope=read,write&response_type=token&key=9537467993aefd6dca9ee7788179c298
   - Click "Allow"
   - Copy the token shown on the page

2. Configure the Plugin:
   - Open LogSeq Settings
   - Go to Plugin Settings > Trello Integration
   - Paste your Trello Token
   - Use `/Trello Get Lists` to find and set your default List ID

## Usage

### Creating Trello Cards
1. Write your content in LogSeq
2. Use `/Send Block to Trello` to create a card from current block
3. Or use `/Send Page to Trello` to create a card from entire page
4. The Trello card URL will be added as a property

### Importing Cards
1. Place your cursor where you want to import cards
2. Type `/Trello Pull Cards`
3. Cards will be imported as separate pages with:
   - Card description (in blocks)
   - Comments section (if comments exist)
   - Each comment with timestamp

### Finding List IDs
1. Type `/Trello Get Lists`
2. View your boards and lists
3. Copy the desired List ID to plugin settings

## Smart Features

### Version Control
- Tracks last update time of both Trello cards and LogSeq pages
- Only updates pages when Trello content is newer
- Preserves your local edits when they're more recent
- Prevents accidental overwrites

### Duplicate Handling
- Checks for existing cards before creating new ones
- Updates existing cards instead of creating duplicates
- Maintains consistent links between LogSeq and Trello
- Preserves card history and comments

## Support

If you encounter any issues or have suggestions:
- Open an issue on GitHub
- Include steps to reproduce the problem
- Attach relevant error messages

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## License

MIT License - feel free to use this plugin in your projects!

---

Made with ❤️ for the LogSeq community