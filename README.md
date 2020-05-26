# Google Maps API security test automation
Determining whether a leaked Google Maps API Key ( often found in index.html/index.php) files is vulnerable to unauthorized access by other applications or not.  

## How to the code:
- Clone the repository using the below command on terminal

```
https://github.com/vikpande/googleapi-security-automation.git
```
- Change directory to the right folder 

```
cd googleapi-security-automation
```

- Open the code in sublime/vscode/pycharm and run the below code/file

```
python3 maps_api_scanner_python3.py
```

- When prompted on the terminal, paste API key that u want to test 7 press enter

- The automation script will return `API key is vulnerable for XXX API!` message and the PoC link/code if determines any unauthorized access within this API key within any API's.

## The code checks for the below GoogleAPI's vulnerabilities:
- Staticmap API
- Streetview API
- Embed (Basic-Free) API
- Embed (Advanced-Paid) API
- Directions API
- Geocode API
- Distance Matrix API
- Find Place From Text API
- Autocomplete API
- Elevation API
- Timezone API
- Roads API

## Google API key security best practices
- Vulnerability !== Insecured
- Read this to make your API key more secured : https://support.google.com/googleapi/answer/6310037?hl=en

## To-do : 
- Automate JavaScript API vulnerability test

## Notes:
- The JavaScript API is not checked by the code because JavaScript API needs manual confirmation from a web browser directly.
- Reference : https://developers.google.com/maps/documentation/javascript/tutorial URL & copying HTML code and changing 'key' parameter with the one wanted to test. 
- After opening file on the browser, if loaded without errors, then the API key is also vulnerable for JavaScript API.
- For Staticmap, Streetview and Embed API's, if used from another domain instead of just testing from browser; whether referer checks are enabled or not on the server-side for the key, script still could return it as vulnerable due to a server-side vulnerability. 

## Contributions:
- If you find other Google Maps API's which are not mentioned in this script, please create a new branch, commit your code and send a pull request explaining improvements and benefits.

