# Backup Files to Google Drive with API
This Python script allows you to backup all files in a local folder to a specific folder on your Google Drive. It compares the timestamps of the local files with the ones on Google Drive and uploads/downloads the files accordingly to keep them in sync.

## Features
- Automatically uploads new or modified files from the local folder to the Google Drive folder.
- Downloads updated files from Google Drive to the local folder if they are newer than the local version.
- Compares file timestamps to avoid unnecessary uploads/downloads.

## Prerequisites
1. A Google account with access to Google Drive.
2. Python 3.6 or later installed on your local machine.

## Getting Started
1. Clone or download this repository to your local machine.
2. Go to the [Google API Console](https://console.developers.google.com/) and create a new project.
3. Enable the Google Drive API for your project.
4. Create new OAuth 2.0 credentials:
    - Click on "Create credentials" and select "OAuth client ID".
    - Select "Desktop app" as the Application type.
    - Enter a name for your credentials (e.g., "Backup Files to Google Drive").
    - Click "Create" and download the credentials JSON file.
5. Move the downloaded credentials JSON file to the same directory as the script and rename it to `credentials.json`.
6. Open the script in a text editor and replace the following variables with your own values:
    - `SAVE_FOLDER_PATH`: The local folder path you want to backup (e.g., `C:\\Users\\username\\Documents\\MyBackupFolder\\`).
    - `YOUR_FOLDER_ID`: The ID of the folder in Google Drive where you want to backup your files. You can find the folder ID in the URL when you open the folder in Google Drive (e.g., `https://drive.google.com/drive/folders/1AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPp`).
7. Install the required Python packages:
```
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```
8. Run the script:
```
python backup_files_to_google_drive.py
```
9. On the first run, a browser window will open asking you to authorize the application to access your Google Drive. Log in with your Google account and grant the requested permissions. The script will create a `token.json` file to store your access and refresh tokens so that you don't need to authorize the application again the next time you run it.
10. The script will now start syncing the files between your local folder and the Google Drive folder.

## Contributing
Please feel free to submit issues or pull requests if you encounter any problems or have suggestions for improvements.

## License
This project is licensed under the MIT License. See the [LICENSE](/LICENSE) file for details.
