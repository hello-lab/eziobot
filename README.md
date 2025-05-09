# Discord Music Bot with Voice Commands

This is my first coding project, a Discord music bot that allows users to play music in voice channels using both text commands and voice commands. It supports YouTube and Spotify, including playlists, and features functionalities like queue management, skipping, pausing, resuming, shuffling, favorites, and genre-based recommendations.

## Features

-   **Voice Commands:** Control the bot using your voice after joining a voice channel. Just say "please" followed by a command (e.g., "please play [song name]", "please skip", "please pause").
-   **Text Commands:** A comprehensive set of text-based commands for music control and bot interaction.
-   **YouTube Support:** Play individual songs and entire playlists from YouTube.
-   **Spotify Support:** Play individual tracks and playlists from Spotify.
-   **Queue Management:** View, clear, and shuffle the music queue.
-   **Playback Control:** Pause, resume, and skip songs.
-   **Favorites:** Save and play your favorite tracks.
-   **Genre-Based Playback:** Get recommendations and play music based on specific genres.
-   **Random Playback:** Discover new music with the random new releases feature from Spotify.
-   **Language Support (via Wit.ai):** The bot attempts to process voice commands in various languages by updating the Wit.ai app language.
-   **Debug Mode:** A debug option for development and troubleshooting.

## Commands

### Voice Commands

After joining a voice channel, use the prefix "please" followed by:

-   `help`: Displays available voice commands.
-   `play [random, favorites, <genre> or query]`: Plays music based on your input.
    -   `random`: Plays a random selection of new releases.
    -   `favorites`: Plays your saved favorite tracks.
    -   `<genre>`: Plays music based on the specified genre (use `e genres` to see available genres).
    -   `query`: Searches for and plays the provided song or video title.
-   `skip`: Skips the currently playing song.
-   `shuffle`: Shuffles the music queue.
-   `genres`: Lists available music genres.
-   `pause`: Pauses the current playback.
-   `resume`: Resumes the paused playback.
-   `clear list`: Clears the music queue.
-   `list`: Shows the current music queue.
-   `hello`: A simple test command.
-   `favorites`: Lists your favorite tracks.
-   `set favorite`: Adds the currently playing song to your favorites.

### Text Commands

Use the prefix `e` followed by:

-   `help`: Displays this help message.
-   `join`: Makes the bot join your current voice channel.
-   `leave`: Makes the bot leave the current voice channel.
-   `play [query]`: Searches for and plays the provided song or video title. Supports YouTube and Spotify links.
-   `genre [name]`: Plays music based on the specified genre.
-   `random`: Plays a random selection of new releases.
-   `pause`: Pauses the current playback.
-   `resume`: Resumes the paused playback.
-   `skip`: Skips the currently playing song.
-   `shuffle`: Shuffles the music queue.
-   `favorite`: Adds the currently playing song to your favorites.
-   `unfavorite [name]`: Removes a specific song (by query) from your favorites.
-   `favorites`: Lists your favorite tracks.
-   `genres`: Lists available music genres.
-   `list`: Shows the current music queue.
-   `clear`: Clears the music queue.
-   `speak`: Text To Speech
-   `debug`: Toggles debug mode for console logging.
-   `hello`: A simple test command.
-   `lang [language code]`: Attempts to update the Wit.ai app language for voice command processing.

## Setup

### Prerequisites

-   **Node.js** (latest LTS version recommended)
-   **npm** (Node Package Manager)
-   **Discord Bot Token:** You'll need to create a Discord bot application and obtain its token from the Discord Developer Portal.
-   **Wit.ai API Key:** Create a Wit.ai app and get the API key. This is required for voice command processing.
-   **Spotify API Credentials (Optional but recommended for full functionality):**
    -   **Client ID**
    -   **Client Secret**
-   You can either set these as environment variables or in a `settings.json` file.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [repository URL]
    cd [repository directory]
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Configure the bot:**

    **Option 1: Using Environment Variables (Recommended for production)**

    Set the following environment variables:

    ```bash
    DISCORD_TOK="YOUR_DISCORD_BOT_TOKEN"
    WITAPIKEY="YOUR_WIT_AI_API_KEY"
    SPOTIFY_TOKEN_ID="YOUR_SPOTIFY_CLIENT_ID"
    SPOTIFY_TOKEN_SECRET="YOUR_SPOTIFY_CLIENT_SECRET"
    ```

    **Option 2: Using `settings.json` (For local development)**

    Create a file named `settings.json` in the project root with the following structure:

    ```json
    {
      "discord_token": "YOUR_DISCORD_BOT_TOKEN",
      "wit_ai_token": "YOUR_WIT_AI_API_KEY",
      "spotify_token_id": "YOUR_SPOTIFY_CLIENT_ID",
      "spotify_token_secret": "YOUR_SPOTIFY_CLIENT_SECRET"
    }
    ```

4.  **Run the bot:**
    ```bash
    node .
    ```

### Inviting the Bot to Your Server

1.  Go to the Discord Developer Portal.
2.  Select your bot application.
3.  Navigate to the "OAuth2" tab.
4.  Under "Scopes," select `bot`.
5.  Under "Bot Permissions," select the necessary permissions (at a minimum, "View Channels," "Send Messages," "Connect," and "Speak").
6.  Copy the generated OAuth2 URL and paste it into your web browser.
7.  Select the server you want to invite the bot to and authorize it.

## Usage

1.  Join a voice channel in your Discord server.
2.  Use the `e join` command in a text channel to make the bot join your voice channel.
3.  Start playing music using the `e play [query]` command or by using voice commands after saying "please".
4.  Explore other commands to manage the queue, favorites, and playback.

## Notes

-   Voice command accuracy depends on the quality of the user's microphone and the effectiveness of the Wit.ai service.
-   Spotify functionality requires valid Spotify API credentials.
-   The bot stores favorite tracks per Discord guild in a local file (`./data/guild_favorites.json`). Ensure the bot has write permissions to this directory.

## Contributing

[If you'd like others to contribute, add information here about how they can do so. For example: "Pull requests are welcome. Please ensure your code follows the existing style and includes tests."]

## License

[Optionally include license information here. For example: "MIT License"]

## Acknowledgements

[You can acknowledge any libraries, APIs, or resources you used here. For example: "This bot uses the discord.js library, ytdl-core for YouTube streaming, and the Spotify Web API."]
