# Google Authenticator
> TYPO3 CMS extension to enable Google 2FA (two factor authentication) for both, frontend- and backend accounts.

## Getting Started
Follow these instructions to enable Google 2FA in your TYPO3 CMS installation.

### Installation
The extension needs to be installed as any other extension of TYPO3 CMS:
1. Switch to the module “Extension Manager”.
2. Get the extension
    1. **Get it from the Extension Manager**: Press the “Retrieve/Update” button, search for the extension key cf_google_authenticator and import the extension from the repository.
    2. **Get it from typo3.org**: You can always get current version from [https://extensions.typo3.org/extension/cf_google_authenticator/](https://extensions.typo3.org/extension/cf_google_authenticator/) by downloading either the t3x or zip version. Upload the file afterwards in the Extension Manager.
3. Change the extension configuration to your needs

### Usage
After installing and activating the extension you'll be able to activate 2FA for backend and frontend users.

#### Backend
1. Switch to the module "Backend Users"
2. Select a user you wish to enable 2FA for
3. Navigate to tab "Google Authenticator"
4. Check "Enable Google Authenticator"
5. Within the Google Authenticator App: scan the provided QR code or setup the authenticator manually by using the given secret
6. Fillout "One-time password" with the code created by your App
7. Save

On the TYPO3 CMS backend login screen you'll notice a new field "Google Authenticator Code".
If you've activated Google 2FA for your backend user, you'll need to enter the code, generated by
the app, to log into your backend account.

If you'll ever lost your Google Authenticator, the only way to disable 2FA is via the database,
by setting "tx_cfgoogleauthenticator_enable" to 0, for the desired user.

#### Frontend
Unfortunately, 2FA for frontend users can currently only be set up via the backend.

## History
See [CHANGELOG.md](CHANGELOG.md)

## License
[GNU Public License](http://opensource.org/licenses/gpl-license.php)