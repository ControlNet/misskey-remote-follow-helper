# Misskey Remote Follow Helper

A Tampermonkey userscript that lets you remotely follow a user on your Misskey instance from any Mastodon/Misskey profile URL.

## Supported URL formats

1. `https://{remote_host}/@{remote_username}`
2. `https://xxx.yyy/@{remote_username}@{remote_host}`

## Setup

1. Install [Tampermonkey](https://www.tampermonkey.net/).
2. Download the script from https://greasyfork.org/scripts/556144
3. In your browser’s Tampermonkey menu:
   - Click **“Set Your Misskey instance”** and enter e.g. `https://misskey.io`.
   - Click **“Set Your Misskey API token”** and paste a token with `users.read` + `following.write` (or equivalent) permissions.

## Usage

1. Open a remote user profile whose URL matches one of the supported formats.
2. Open the Tampermonkey menu.
3. Click **“Remote follow on Misskey”**.
4. The script will:
   - Parse `remote_host` and `remote_username` from the URL.
   - Call your Misskey instance API to send a follow request.
