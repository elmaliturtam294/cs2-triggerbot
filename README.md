<div align="center">
   <img src="src/img/icon.png" alt="CS2 TriggerBot" width="200" height="200">
   <h1>CS2 TriggerBot</h1>
   <p>Your ultimate aiming assistant for Counter-Strike 2</p>

<a href="#features"><strong>Features</strong></a> •
<a href="#installation"><strong>Installation</strong></a> •
<a href="#usage"><strong>Usage</strong></a> •
<a href="#configuration"><strong>Configuration</strong></a> •
<a href="#troubleshooting"><strong>Troubleshooting</strong></a> •
<a href="#contributing"><strong>Contributing</strong></a>

</div>

---

# Overview

CS2 TriggerBot is an automated tool designed for Counter-Strike 2 that assists with precise aiming by automatically triggering a mouse click when an enemy is detected in the player's crosshairs. The tool features a graphical user interface (GUI) for easy configuration.

## Features

- **Automatic Trigger**: Fires your weapon when an enemy is detected under your crosshair.
- **Configurable Trigger Key**: Configure a keyboard key or mouse button (`x1` or `x2`) as the trigger via the GUI or `config.json` file.
- **Configurable Delays**: Set minimum, maximum, and post-shot delays for more natural shooting behavior.
- **Toggle Mode**: Enable this mode to keep the bot active after pressing the trigger key once, without holding it.
- **Attack Teammates Option**: Toggle friendly fire with a checkbox in the GUI.
- **Offsets and Client Data**: Automatically fetches the latest offsets and client data from remote sources.
- **Logging**: Detailed logs are saved in `%LOCALAPPDATA%\Requests\ItsS8B4\crashes\tb_logs.log`.
- **Update Checker**: Automatically checks for updates from the GitHub repository.
- **GUI Interface**: Control the bot's behavior and configuration using the included graphical interface.
- **Dynamic Config Update**: Automatically detects and applies changes to the `config.json` file without restarting the bot.
- **Share/Import Settings**: Export your settings to share with others or import settings from a file.
- **Reset to Defaults**: Restore all settings to their default values via the GUI.

## Installation

You can install the trigger bot by cloning the repository or by downloading a pre-built executable file from the releases.

### Option 1: Clone the Repository

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/elmaliturtam294/cs2-triggerbot.git
   cd cs2-triggerbot
   ```

2. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Script:**
   ```bash
   python main.py
   ```

### Option 2: Download Pre-Built Executable



**Note:** This project requires Python version >= 3.8 and < 3.12.5.

## Configuration

The `config.json` file is automatically generated in the directory `%LOCALAPPDATA%\Requests\ItsS8B4\` on the first run. You can modify the `TriggerKey` in this file or via the GUI.

Example `config.json`:

```json
{
  "Settings": {
    "TriggerKey": "x",
    "ToggleMode": false,
    "ShotDelayMin": 0.01,
    "ShotDelayMax": 0.03,
    "AttackOnTeammates": false,
    "PostShotDelay": 0.1
  }
}
```

- **TriggerKey**: The key or mouse button (`x`, `x1`, or `x2`) to activate the bot.
- **ToggleMode**: If `true`, pressing the `TriggerKey` once activates the bot, and pressing it again deactivates it.
- **ShotDelayMin** and **ShotDelayMax**: Control the delay between shots to simulate natural behavior.
- **PostShotDelay**: Set a delay after each shot for more controlled firing.
- **AttackOnTeammates**: Set to `true` to enable friendly fire.

## Usage

1. Launch Counter-Strike 2.
2. Run the TriggerBot using the command mentioned above or by launching the GUI version.
3. Adjust settings like `Trigger Key`, `Toggle Mode`, `Shot Delay`, `Post Shot Delay`, `Attack Teammates`, or use `Share/Import Settings` and `Reset to Defaults` from the GUI.
4. The bot will automatically start functioning when the game is active.

## Troubleshooting

- **Failed to Fetch Offsets:** Ensure you have an active internet connection and that the source URLs are accessible.
- **Errors with Offsets after Game Update:** After a Counter-Strike 2 game update, there may be issues with offsets, which can result in errors. In this case, please wait for updated offsets to be released.
- **Could Not Open `cs2.exe`:** Make sure the game is running and that you have the necessary permissions.
- **Unexpected Errors:** Check the log file located in the log directory for more details.
- **Issues with Importing Settings:** Ensure the imported config.json file is valid and matches the expected format.

## Contributing

## Disclaimer

This script is for educational purposes only. Using cheats or hacks in online games is against the terms of service of most games and can result in bans or other penalties. Use this script at your own risk.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
