# Spotify Playlist Builder Bot (UiPath)

A UiPath RPA bot that turns an Excel list of songs into Spotify
playlists, one playlist per genre, without any manual clicking.

## How it works
1. Reads the songs from an Excel file (columns: Genre, Song Name,
   Artist)
2. Finds the unique genres
3. Opens Spotify Web in Chrome
4. For each genre:
   - Creates a new playlist named "<Genre> Mix"
   - Filters the songs of that genre
   - Searches each song by name and artist, then adds it to
     the playlist

## Tools used
UiPath Studio, Excel activities, UI automation (Chrome),
DataTable activities (Filter Data Table, For Each Row)

## How to run it
1. Open the project in UiPath Studio (project.json)
2. Create an Excel file with the columns Genre, Song Name, Artist
3. In Main.xaml, set the path of the Excel file and the sheet name
   in the Read Range activity
4. Log in to open.spotify.com in Chrome and install the UiPath
   Chrome extension
5. Run the workflow

## Notes
- Uses UI automation, not the Spotify API. If Spotify changes its
  web page, the selectors may need to be updated.
- You must be logged in to Spotify in Chrome before running.

## Screenshot
<img width="1366" height="726" alt="Screenshot 2026-11-13 014127" src="https://github.com/user-attachments/assets/6ef419bf-9b68-4d1a-9d16-e5a0889a6b97" />
<img width="1366" height="724" alt="Screenshot 2026-11-13 013953" src="https://github.com/user-attachments/assets/be4ab559-b508-42ea-b014-4f194e18b6d8" />
<img width="1366" height="724" alt="Screenshot 2026-11-13 013858" src="https://github.com/user-attachments/assets/d5ed81c9-174e-430d-9028-c193f76dd883" />
<img width="1366" height="726" alt="Screenshot 2026-11-13 014303" src="https://github.com/user-attachments/assets/97a78dfa-c0b7-4bd7-b8d3-64381593a730" />
