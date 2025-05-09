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

