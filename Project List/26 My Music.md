
# My Music

Build a website that allows users to upload music files and create playlists.

---

## Testing

The system should include 5 tracks uploaded for each of the user accounts listed below.

You are required to create the following accounts to allow the system to be tested. All accounts should have the password `p455w0rd`:

1. `user1`
2. `user2`
3. `user3`

---

## Feature 1

Users need to be logged in to view any pages. Any user who is not logged in should be redirected to the login page.

The _Homepage_ should display an **Upload track** link or button that takes the `user` to the _Upload Track_ screen. This screen should display a form that contains a single file upload field which only accepts files with a mime-type of audio/mp3.

When the file get uploaded to the server, the following ID3 data needs to be extracted and stored in a database:

1. Track name.
2. Album name.
3. Artist name.

In addition, if the mp3 file includes album art, this should be saved as an image. The name and path of both the mp3 file and the album part also need to be stored in the database.

> Note: the user must __not__ be asked to input the track, artist name or duration, nor upload album art, this information **must** be extracted directly from the uploaded file.

In addition the database should also store the following without requesting it from the user:

1. The username of the user uploading the file.
2. The current date and time.

> To demonstrate this feature and to prove that the form works correctly you will need to show that the data is being persisted correctly, either by running a database query or an API call depending on the platform and technology you are using.

## Feature 2

The home screen should display all the tracks uploaded by the currently logged-in user. Each trach should display:

1. The name of the track.
2. The artist name.
3. The album art.
4. The duration (in minutes and seconds).

The user should not be able to play the tracks from the home screen.

## Feature 3

Each track should have a **Details** button or link that takes the user to the _Track Details_ screen. This should display all the information about the selected track, specifically:

1. The track name.
2. The artist name.
2. The album name.
3. The album art.
4. The duration (in minutes and seconds).

The page should also allow the track to be played, paused and should also include a scrub bar to track how much of the track has been played and allow the user to scrub forward and backward.

## Feature 4

The intermediate tasks require you to make changes to the functionality:

1. The home screen should include a **Playlists** link or button to display the _Playlists_ screen.
2. This screen should include a **New playlist** link or button to take the user to a screen where they can:
    1. Give the playlist a name.
    2. Choose some album art.
    3. Use checkboxes to choose which tracks to include in the playlist.
3. The playlist screen should display the following for each playlist:
    1. The name.
    2. a thumbnail of the album art.
4. Selecting a playlist should display the list of songs and start playing from the top.

---

## Extras

In some assignment briefs you are given marks for the appropriate use of media and using sensors built into the user's device.

### Sensors

In some assignment briefs you are given marks for the appropriate use of sensors and sensor data. You should be implementing:

1. Each track should keep track of where ther person was when they last listened to it and when.
2. This information should be displayed next to any track that has been played. If the person has never listened to a track this should be flagged up.
3. If the device is shaken it should play a random song.
4. When asked for a playlist image the user should be provided with the option of using the device camera (if available)

### Media

In the requirements listed above you need to provide the user with the ability to upload photos. For the extra media marks you will need to expand this by:

1. Providing the user with the choice of uploading photos, video clips or audio clips.
2. Giving users the option to directly capture images, audio and video clips using the built-in camera and/or microphone if available.

### Data

There are lots of online RESTful APIs you can make use of when developing this system. You should consider:

1. [Deezer API](https://rapidapi.com/deezerdevs/api/deezer-1)
2. [iTunes API](https://rapidapi.com/volodimir.kudriachenko/api/iTunes)
3. [Spotify API](https://rapidapi.com/search/spotify)
4. [LastFM API](https://rapidapi.com/dimashirokov/api/LastFm)
5. [LocationIQ](https://locationiq.com)
