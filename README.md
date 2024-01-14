# Weather Monitoring and Alert System
## Overview
The system utilizes the OpenWeatherMap API to fetch and process real-time weather data, storing it in files. It calculates trends, sends email alerts based on atmospheric pressure thresholds, and logs email details in email_log.txt.
## Features
*Data Retrieval:* 

	Data Retrieval through API: The project initiated by fetching real-time weather data from the "open-meteo" API. This step provided a consistent and up-to-date source of atmospheric information crucial for subsequent analysis. 

	Data Storage in JSON File: After obtaining the data, the raw JSON information was directly saved to a file using the " save_raw_data " function. This approach ensured the preservation of the raw data in a JSON format, allowing for future reference or more advanced processing if needed. 


*Processing, and Storage:* 

	Data Processing with C Programming: After obtaining the data, the project transitioned to the processing phase. Leveraging the capabilities of the C programming language, the fetched data from the API was meticulously handled to prepare it for further utilization. 

	Data Storage: To facilitate seamless access and maintain data integrity, the processed information was systematically stored in a file named " data.txt ". This structured approach ensured efficient organization and ease of retrieval for subsequent stages of analysis. 


*Trends:*

	After saving the data from weather API , it is then analyzed for finding trend and those trends are saved in a file named "processed.txt ". 

*Monitoring and Alert System:*

	Dynamic Threshold Comparison: Upon successful retrieval and processing of real-time weather data, the system dynamically compares the atmospheric pressure against a predefined threshold value. 

	Email Alerting Mechanism: If the current atmospheric pressure exceeds the established threshold, the system initiates an automated email alert. This functionality is executed through the send_email function, generating an email with the subject line "WEATHER ALERT!!!" and a corresponding body message. The email serves as a timely notification, emphasizing the exceeded atmospheric pressure and urging recipients to take necessary precautions. 

*Creating Log Files:*

	A log file titled "email_log.txt" is diligently maintained to record every sent email and document any encountered error messages during the process. 

*Automation:*

	Automation was established through cron jobs, leveraging crontab, to send email alerts every day at a specified time automatically when the atmospheric pressure value surpasses the predefined threshold.
## Dependencies
- [cURL](https://curl.haxx.se/libcurl/)
- [jansson](https://digip.org/jansson/) (JSON library)
- [time.h](http://www.cplusplus.com/reference/ctime/time.h/) (C Standard Library)

Feel free to contribute, report issues, or suggest improvements!
