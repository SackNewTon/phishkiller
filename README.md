# WebPhishkiller

## Overview
This script is designed to combat phishing attacks by flooding phisher databases with false information by flooding attacker database.

## Forked from the [phishkiller](https://github.com/CybrZone/phishkiller/tree/main)

## How It Works
Using multi-threading, the script generates random email addresses and passwords from a predefined list of names. Each thread independently sends POST requests to a specified URL, submitting fictitious data to overwhelm phisher databases. This proactive approach aims to dilute and disrupt the accuracy of stolen data, offering a layer of protection to potential victims.

## Purpose of This Script
- Stop Phising


## WebPhishkiller usage

- Copy the The "webphishkiller.py" Or The Download It Here and click the "Download raw file" <a href="https://github.com/SackNewTon/phishkiller/blob/main/webphishkiller" download>Download Here</a>

## Create a file Called

- config.json

## Note!
- Make sure The "webphishkiller.py" and "config.json" has to be in the directory/folder

## Copy and Paste This Code in The json config

```
{
    "url": "https://add-the-actual-url-phishing-link-here",
    "num_threads": 25,
    "max_concurrent_requests": 5,
    "proxy": null,
    "auth_token": "your_auth_token_here"
}
```

## Edit The "url": in the json file with the actual phishing website

## Run The Script

```
python3 webphishkiller.py
 ```
 


 ## New Functionalities Added From The Forked Python Script
 
## HTTP POST Request Handling:

- send_posts(url, session, semaphore, proxy=None): Sends POST requests to a specified URL
(url). It includes randomized email and password data in the request payload. The
function handles retries and timeout with a session (session) object and uses a semaphore
(semaphore) to limit concurrent requests. Optionally, it supports proxy usage (proxy parameter).

## Configuration Management:

- load_config(filename='config.json'): Loads configuration settings from a JSON file
(config.json) or environment variables. It retrieves settings such as url, num_threads, max_concurrent_requests, proxy, and auth_token.


## Main Program Execution:

- main(): Coordinates the main execution flow of the script. It initializes configurations, sets up
a session with retry mechanisms, applies authentication headers if an auth_token is provided,
creates threads (num_threads) to send POST requests concurrently, and manages their 
lifecycle.


## Thread Management:

- Threads are created to execute the send_posts() function concurrently. Each thread operates independently to send HTTP POST requests with randomized data.


## Error Handling and Logging:

- logging: The script logs successful requests (including email, password, status code, and User-Agent) and failed requests (with error messages) to a requests.log file using the logging module.

## Dependencies:

- The script depends on several third-party libraries: requests, names, fake_useragent. These are used for HTTP requests, name generation, and generating random User-Agent headers respectively.

## Customization:

- Users can customize the script's behavior by modifying the config.json file or adjusting environment variables to fit their specific API endpoint, concurrency requirements, proxy configurations, and authentication needs.

Overall, the script provides a framework for performing multithreaded HTTP POST requests with randomized data and robust error handling/logging, making it suitable for testing or automation tasks where concurrent API interactions are necessary.


### Overall, the script provides a framework for performing multithreaded HTTP POST requests with
randomized data and robust error handling/logging, making it suitable for testing or automation tasks
where concurrent API interactions are necessary.

 ### Disclaimer
**Note:** This script should be used responsibly and only on systems you have explicit permission to test against.
