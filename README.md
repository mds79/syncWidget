# syncWidget
A scriptable-app widget to sync files between iPhone, iPad and a server like Synology Diskstation, Nextcloud, Owncloud.

<img width="345" alt="widget-screenshot" src="https://user-images.githubusercontent.com/26939017/115142423-f80f4200-a041-11eb-9821-d8e74a76374f.png">

Main Feature
============
This is a very primitive sync-tool to synchronize a folder on iPhone/iPad with a server folder. The files within the folders are available for offline access. As the widgets are triggered from time to time automatically by iOS/iPadOS or whenever you swip across the widgets the selected folders are kept in sync without starting an app. This script is necessary because the Synology Drive-app has no option to select files, which are stored local (offline) and are kept synchronuous with the server file AND having these files available for other apps, e.g. scriptable-app or shortcuts (via x-callback-URL). All difficult file handling jobs are managed from the operation system and the scriptable-app.

Requirements
============
1. You need access to a file server like Synology Diskstation or owncloud/nextcloud.
2. The files on the server must be accessable for the operation system (iOS/iPadOS). Therefore a interface system should be available. You could use SMB (Synology Diskstation) or a WebDAV server (NextCloud, OwnCloud).

Installation
============
1. Create an appropriate backup
2. Include the server file system within the iOS-App Files via the option "Connect to server" within the Files-App.
3. Create a local folder on your iPhone/iPad.
4. Start the scriptable-app and create two "File Bookmarks". Use "Pick Folder".
  a) Select the folder on the server (server-Folder) and give it a bookmark name
  b) select the folder on iPhone/iPad (local-Folder) and give it a bookmark name
4. Replace the bookmark names for the constant "localPath" with the bookmark name of your local-Folder and replace the bookmark name for "serverPath" with the bookmark name of your server-Folder within the script.
5. Install the script as widget. It is designed for the size LARGE.

Limitations
===========
The script does not support large files or subfolders. I haven't included any management for the case that the sync process is not finished within the execution time of the widget.


Hints
=====
I recommand to select a folder within the drive subfolders of a Diskstation for sync. When versioning within Synology Drive is activated this should create backups from your synced files automatically (hopefully).
